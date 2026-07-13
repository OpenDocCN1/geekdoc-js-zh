![](cover.jpeg)

Index

[Use const and let instead of var for block-scoped variables.](#part0003.xhtml_a640)

[Utilize arrow functions for shorter syntax and lexical this.](#part0004.xhtml_a639)

[Leverage template literals for easier string concatenation.](#part0005.xhtml_a63P)

[Use destructuring assignments for objects and arrays to write cleaner code.](#part0006.xhtml_a659)

[Apply the spread operator to merge arrays and objects.](#part0007.xhtml_a63R)

[Use meaningful variable names that describe their purpose.](#part0008.xhtml_a654)

[Prefix boolean variables with is, has, or can.](#part0009.xhtml_a65Z)

[Include the unit in variable names that hold measurements.](#part0010.xhtml_a635)

[Use nouns for variables and verbs for functions.](#part0011.xhtml_a65P)

[Avoid abbreviations that are not universally understood.](#part0012.xhtml_a650)

[Avoid generic names like data, item, or thing.](#part0013.xhtml_a655)

[Be specific with names to avoid ambiguity.](#part0014.xhtml_a656)

[Use consistent naming conventions throughout the codebase.](#part0015.xhtml_a63Y)

[Avoid using magic numbers; use named constants instead.](#part0016.xhtml_a63F)

[Ensure function names clearly describe their action.](#part0017.xhtml_a65N)

[Utilize default function parameters for cleaner code.](#part0018.xhtml_a65M)

[Use async/await for asynchronous code for better readability.](#part0019.xhtml_a63K)

[Employ Map and Set for collections instead of plain objects and arrays.](#part0020.xhtml_a641)

[Leverage optional chaining to handle nested object properties.](#part0021.xhtml_a63X)

[Use Array.prototype.map and Array.prototype.filter for array transformations.](#part0022.xhtml_a648)

[Comment on the purpose of complex functions or blocks of code.](#part0023.xhtml_a65K)

[Explain non-obvious code logic in comments.](#part0024.xhtml_a631)

[Document the expected input and output for functions.](#part0025.xhtml_a64M)

[Highlight temporary workarounds with comments.](#part0026.xhtml_a65A)

[Use comments to indicate important sections of code.](#part0027.xhtml_a657)

[Keep comments concise and to the point.](#part0028.xhtml_a63S)

[Update comments when code changes to maintain accuracy.](#part0029.xhtml_a64P)

[Avoid redundant comments that state the obvious.](#part0030.xhtml_a64Y)

[Use comments to explain the why, not the what.](#part0031.xhtml_a65W)

[Write comments in proper English with correct grammar.](#part0032.xhtml_a63E)

[Take advantage of ES6 classes for object-oriented programming.](#part0033.xhtml_a65Y)

[Use Promise.all for running multiple promises concurrently.](#part0034.xhtml_a64U)

[Utilize Object.keys and Object.values for object iteration.](#part0035.xhtml_a64B)

[Use the ?? (nullish coalescing) operator for default values.](#part0036.xhtml_a63W)

[Employ fetch for making network requests instead of older methods like XMLHttpRequest.](#part0037.xhtml_a643)

[Consistently format your code with a linter like ESLint.](#part0038.xhtml_a65G)

[Use Prettier for automatic code formatting.](#part0039.xhtml_a62Y)

[Organize your code with consistent indentation.](#part0040.xhtml_a652)

[Group related code together logically.](#part0041.xhtml_a630)

[Limit the length of lines to improve readability.](#part0042.xhtml_a634)

[Use early returns to avoid nested if statements.](#part0043.xhtml_a647)

[Favor switch statements for multiple condition checks.](#part0044.xhtml_a64A)

[Avoid deeply nested loops by breaking them into functions.](#part0045.xhtml_a653)

[Use try/catch blocks for error handling.](#part0046.xhtml_a65R)

[Keep functions short and focused on a single task.](#part0047.xhtml_a649)

[Use descriptive function names that convey their purpose.](#part0048.xhtml_a63G)

[Write pure functions that do not have side effects.](#part0049.xhtml_a63N)

[Avoid using global variables.](#part0050.xhtml_a65V)

[Use constants for values that do not change.](#part0051.xhtml_a62Z)

[Leverage async generators for handling async iteration.](#part0052.xhtml_a65S)

[Utilize WeakMap and WeakSet for managing object keys without preventing garbage collection.](#part0053.xhtml_a64F)

[Use Proxy objects for custom behavior of fundamental operations.](#part0054.xhtml_a63J)

[Leverage Symbol for unique property keys to avoid conflicts.](#part0055.xhtml_a63D)

[Employ tagged template literals for safe HTML or SQL templates.](#part0056.xhtml_a65E)

[Use the Reflect API to perform object operations](#part0057.xhtml_a636)

[Declare variables as close as possible to their usage](#part0058.xhtml_a642)

[Use meaningful names for loop counters.](#part0059.xhtml_a64R)

[Avoid reusing variables for different purposes.](#part0060.xhtml_a632)

[Initialize variables when they are declared.](#part0061.xhtml_a633)

[Use constants for configuration values.](#part0062.xhtml_a64V)

[Break down functions that do multiple things into smaller ones.](#part0063.xhtml_a64J)

[Separate concerns by dividing code into modules.](#part0064.xhtml_a651)

[Limit the number of function parameters](#part0065.xhtml_a65U)

[Use helper functions to encapsulate complex logic](#part0066.xhtml_a63V)

[Write unit tests to ensure functions do one thing correctly.](#part0067.xhtml_a62V)

[Leverage JavaScript modules (ES6 import/export) for better code organization.](#part0068.xhtml_a644)

[Use async functions for cleaner asynchronous code](#part0069.xhtml_a62X)

[Take advantage of for...of for iterable objects](#part0070.xhtml_a64G)

[Employ Array.prototype.reduce for accumulating array values.](#part0071.xhtml_a64T)

[Use Object.assign for merging objects.](#part0072.xhtml_a64S)

[Break down long conditional expressions into multiple lines.](#part0073.xhtml_a64C)

[Use temporary variables to hold intermediate results in expressions.](#part0074.xhtml_a638)

[Refactor complex expressions into helper functions.](#part0075.xhtml_a63A)

[Avoid chaining multiple ternary operators.](#part0076.xhtml_a65T)

[Use parentheses to make the order of operations explicit.](#part0077.xhtml_a64E)

[Encapsulate unrelated functionality into separate functions.](#part0078.xhtml_a63T)

[Use utility libraries for common tasks](#part0079.xhtml_a64W)

[Abstract repetitive code into reusable functions](#part0080.xhtml_a65D)

[Separate data fetching logic from UI rendering logic](#part0081.xhtml_a63Z)

[Use design patterns to solve common problems](#part0082.xhtml_a64Z)

[Utilize the async keyword for asynchronous functions.](#part0083.xhtml_a64D)

[Make use of the await keyword for handling promises.](#part0084.xhtml_a64H)

[Use JSON.stringify and JSON.parse for deep copying objects](#part0085.xhtml_a660)

[Leverage Array.prototype.some and Array.prototype.every for conditional checks](#part0086.xhtml_a63U)

[Utilize Array.prototype.find for locating elements in arrays.](#part0087.xhtml_a63M)

[Choose arrays for ordered collections of data.](#part0088.xhtml_a64K)

[Use objects for key-value pairs.](#part0089.xhtml_a65H)

[Opt for Map when you need ordered key-value pairs.](#part0090.xhtml_a64N)

[Utilize Set for unique values without duplicates.](#part0091.xhtml_a65C)

[Prefer WeakMap and WeakSet for managing memory efficiently.](#part0092.xhtml_a65F)

[Use try/catch blocks to handle exceptions.](#part0093.xhtml_a65X)

[Provide meaningful error messages.](#part0094.xhtml_a65J)

[Log errors to the console or a logging service.](#part0095.xhtml_a63C)

[Gracefully handle rejected promises with .catch.](#part0096.xhtml_a646)

[Validate function inputs to prevent errors.](#part0097.xhtml_a637)

[Write modular code that can be reused in different projects.](#part0098.xhtml_a63B)

[Use higher-order functions to create reusable function patterns.](#part0099.xhtml_a62W)

[Employ mixins for reusing code in multiple classes.](#part0100.xhtml_a65B)

[Use inheritance for extending existing classes](#part0101.xhtml_a64X)

[Leverage function composition for creating complex functionality from simple functions](#part0102.xhtml_a658)

[Use default parameters to handle missing arguments](#part0103.xhtml_a645)

[Avoid side effects to make functions reusable](#part0104.xhtml_a63H)

Introduction

◆

Readable code is the cornerstone of effective programming.

This eBook presents 100 techniques to help you write better JavaScript code.

By leveraging JavaScript's unique features and syntax, these methods aim to make your code as readable as possible for others.

Each technique is illustrated with examples of both good and bad code, ensuring clarity and ease of understanding.

Dive in to discover how you can enhance your coding practices and produce cleaner, more maintainable JavaScript code.

1

# Use const and let instead of var for block-scoped variables.

* * *

Using const and let ensures variables are block-scoped, reducing errors and improving code readability.

* * *

const and let provide block-level scoping, which helps prevent issues related to variable hoisting and scope leakage that are common with var.

< Good Code >

// Using const for constants

const MAX_USERS = 100;

// Using let for variables that may change

let userCount = 0;

if (userCount < MAX_USERS) {

  let newUser = 'John Doe';

  userCount++;

  console.log(newUser); // John Doe

}

console.log(userCount); // 1

<Bad Code>

// Using var, which is function-scoped and can cause issues

var MAX_USERS = 100;

var userCount = 0;

if (userCount < MAX_USERS) {

  var newUser = 'John Doe';

  userCount++;

  console.log(newUser); // John Doe

}

console.log(userCount); // 1

console.log(newUser); // John Doe (newUser is accessible here, which can be problematic)

Using const and let helps to avoid the pitfalls of var, such as accidental global variable creation and unexpected behavior due to hoisting. const is used for variables that should not be reassigned, while let is used for variables that may change.

<Memo>

var declarations are hoisted to the top of their containing function or global scope, which can lead to confusing bugs. const and let declarations are also hoisted but are not initialized until their definition is evaluated, leading to a "temporal dead zone" where accessing them before initialization throws an error.

2

# Utilize arrow functions for shorter syntax and lexical this.

* * *

Arrow functions provide a concise syntax and lexically bind the this value, making them ideal for callbacks and methods.

* * *

Arrow functions offer a shorter syntax compared to traditional function expressions and automatically bind this to the surrounding context, which simplifies code and avoids common pitfalls with this.

< Good Code >

// Using arrow functions for concise syntax and lexical this

const users = ['Alice', 'Bob', 'Charlie'];

users.forEach(user => console.log(user)); // Alice, Bob, Charlie

const user = {

  name: 'John Doe',

  greet: () => {

    console.log(`Hello, my name is ${this.name}`); // 'this' is lexically bound, so it refers to the global object

  }

};

user.greet(); // Hello, my name is undefined

<Bad Code>

// Using traditional function expressions

const users = ['Alice', 'Bob', 'Charlie'];

users.forEach(function(user) {

  console.log(user); // Alice, Bob, Charlie

});

const user = {

  name: 'John Doe',

  greet: function() {

    console.log(`Hello, my name is ${this.name}`); // 'this' refers to the user object

  }

};

user.greet(); // Hello, my name is John Doe

Arrow functions are particularly useful for writing shorter and more readable code, especially in callbacks and methods. However, they do not have their own this context, which can be beneficial or problematic depending on the use case. Traditional function expressions should be used when a dynamic this context is required.

<Memo>

Arrow functions cannot be used as constructors and do not have their own arguments object. They are best suited for non-method functions and callbacks where the lexical this is desired.

3

# Leverage template literals for easier string concatenation.

* * *

Use template literals to simplify string concatenation and improve readability.

* * *

Template literals, introduced in ES6, allow for easier and more readable string concatenation using backticks and embedded expressions.

< Good Code >

// Using template literals for string concatenation

const name = "John";

const age = 30;

const greeting = `Hello, my name is ${name} and I am ${age} years old.`;

console.log(greeting); // Output: Hello, my name is John and I am 30 years old.

<Bad Code>

// Using traditional string concatenation

const name = "John";

const age = 30;

const greeting = "Hello, my name is " + name + " and I am " + age + " years old.";

console.log(greeting); // Output: Hello, my name is John and I am 30 years old.

Template literals use backticks (`) instead of quotes and allow embedding expressions with ${expression}. This makes the code more readable and easier to maintain compared to traditional string concatenation using the + operator.

<Memo>

Template literals also support multi-line strings, which can be very useful for formatting long strings or HTML fragments.

4

# Use destructuring assignments for objects and arrays to write cleaner code.

* * *

Destructuring assignments allow for extracting values from objects and arrays in a concise and readable manner.

* * *

Destructuring assignments, introduced in ES6, enable you to unpack values from arrays or properties from objects into distinct variables.

< Good Code >

// Using destructuring assignment for objects

const person = { name: "Alice", age: 25, city: "Wonderland" };

const { name, age, city } = person;

console.log(name); // Output: Alice

console.log(age); // Output: 25

console.log(city); // Output: Wonderland

// Using destructuring assignment for arrays

const numbers = [1, 2, 3, 4];

const [first, second, , fourth] = numbers;

console.log(first); // Output: 1

console.log(second); // Output: 2

console.log(fourth); // Output: 4

<Bad Code>

// Without destructuring assignment for objects

const person = { name: "Alice", age: 25, city: "Wonderland" };

const name = person.name;

const age = person.age;

const city = person.city;

console.log(name); // Output: Alice

console.log(age); // Output: 25

console.log(city); // Output: Wonderland

// Without destructuring assignment for arrays

const numbers = [1, 2, 3, 4];

const first = numbers[0];

const second = numbers[1];

const fourth = numbers[3];

console.log(first); // Output: 1

console.log(second); // Output: 2

console.log(fourth); // Output: 4

Destructuring assignments make the code more concise and readable by reducing the need for repetitive code. It allows for direct extraction of values from objects and arrays, making the code cleaner and easier to understand.

<Memo>

Destructuring can also be used with function parameters, allowing for more flexible and readable function signatures.

5

# Apply the spread operator to merge arrays and objects.

* * *

Use the spread operator (...) to easily merge arrays and objects in JavaScript.

* * *

The spread operator allows you to expand elements of an array or properties of an object. This makes it simple to merge arrays and objects without using complex methods.

< Good Code >

// Merging arrays

const array1 = [1, 2, 3];

const array2 = [4, 5, 6];

const mergedArray = [...array1, ...array2]; // [1, 2, 3, 4, 5, 6]

// Merging objects

const object1 = { a: 1, b: 2 };

const object2 = { c: 3, d: 4 };

const mergedObject = { ...object1, ...object2 }; // { a: 1, b: 2, c: 3, d: 4 }

<Bad Code>

// Merging arrays

const array1 = [1, 2, 3];

const array2 = [4, 5, 6];

const mergedArray = array1.concat(array2); // [1, 2, 3, 4, 5, 6]

// Merging objects

const object1 = { a: 1, b: 2 };

const object2 = { c: 3, d: 4 };

const mergedObject = Object.assign({}, object1, object2); // { a: 1, b: 2, c: 3, d: 4 }

The good example uses the spread operator, which is more concise and easier to read. The bad example uses older methods like concat for arrays and Object.assign for objects, which are more verbose and less intuitive.

<Memo>

The spread operator was introduced in ES6 (ECMAScript 2015) and has since become a popular feature for handling arrays and objects in a more readable and efficient manner.

6

# Use meaningful variable names that describe their purpose.

* * *

Choose variable names that clearly describe their purpose and content.

* * *

Meaningful variable names make your code more readable and maintainable. They help other developers understand the purpose of the variables without needing additional comments.

< Good Code >

// Good variable names

const totalPrice = 100;

const userAge = 25;

const isUserLoggedIn = true;

<Bad Code>

// Poor variable names

const x = 100;

const y = 25;

const z = true;

The good example uses descriptive names that indicate what the variables represent, making the code self-explanatory. The bad example uses generic names like x, y, and z, which do not convey any meaningful information about the variables' purposes.

<Memo>

Using meaningful variable names is a fundamental practice in clean code principles, as advocated by software engineering experts like Robert C. Martin in his book "Clean Code".

7

# Prefix boolean variables with is, has, or can.

* * *

Use prefixes like "is", "has", or "can" for boolean variables to make their purpose clear.

* * *

Boolean variables represent true/false values. Using prefixes like "is", "has", or "can" helps indicate the nature of the boolean value, making the code more readable and understandable.

< Good Code >

// Good example with clear boolean variable names

let isUserLoggedIn = true;

let hasAdminPrivileges = false;

let canEditProfile = true;

<Bad Code>

// Bad example with unclear boolean variable names

let loggedIn = true;

let admin = false;

let edit = true;

In the good example, the prefixes "is", "has", and "can" clearly indicate that the variables are boolean. This makes it easier for other developers to understand the purpose of these variables at a glance. In the bad example, the variable names are ambiguous and do not clearly convey that they are boolean, which can lead to confusion.

<Memo>

Using descriptive prefixes for boolean variables is a common practice in many programming languages, not just JavaScript. It enhances code readability and maintainability across different codebases.

8

# Include the unit in variable names that hold measurements.

* * *

Always include the unit of measurement in the variable name to avoid confusion.

* * *

When dealing with variables that store measurements, including the unit in the variable name helps clarify what the value represents, reducing the risk of errors and misunderstandings.

< Good Code >

// Good example with units in variable names

let distanceInMeters = 500;

let weightInKilograms = 70;

let timeInSeconds = 120;

<Bad Code>

// Bad example without units in variable names

let distance = 500;

let weight = 70;

let time = 120;

In the good example, the variable names include the units (meters, kilograms, seconds), making it clear what each value represents. This practice helps prevent mistakes, such as mixing up different units of measurement. In the bad example, the lack of units in the variable names can lead to confusion and potential errors, as it is not immediately clear what the values represent.

<Memo>

Including units in variable names is especially important in scientific and engineering applications, where precise measurements are crucial. This practice helps ensure accuracy and clarity in calculations and data representation.

9

# Use nouns for variables and verbs for functions.

* * *

Using nouns for variables and verbs for functions makes the code more readable and intuitive.

* * *

This technique ensures that variables clearly represent entities or objects, while functions represent actions or processes. This naming convention helps others quickly understand the purpose and usage of each element in your code.

< Good Code >

```javascript

// Good Example

let userName = "John"; // Noun for a variable

let age = 30; // Noun for a variable

function calculateAge(birthYear) { // Verb for a function

  return new Date().getFullYear() - birthYear;

}

function printGreeting(name) { // Verb for a function

  console.log(`Hello, ${name}!`);

}

```

<Bad Code>

```javascript

// Bad Example

let calc = "John"; // Confusing variable name

let calcAge = 30; // Confusing variable name

function user(name) { // Confusing function name

  console.log(`Hello, ${name}!`);

}

function age(birthYear) { // Confusing function name

  return new Date().getFullYear() - birthYear;

}

```

In the good example, `userName` and `age` are clear nouns, making it obvious that they represent data. The functions `calculateAge` and `printGreeting` are named with verbs, indicating actions. In the bad example, names like `calc` and `user` are ambiguous, making it hard to understand what they represent or do.

<Memo>

Did you know? Following a consistent naming convention not only improves readability but also helps in maintaining and debugging code efficiently, especially in larger projects.

10

# Avoid abbreviations that are not universally understood.

* * *

Using clear, full names instead of abbreviations enhances code readability and reduces confusion.

* * *

Avoiding non-universal abbreviations in your code ensures that anyone reading it can easily understand what each variable or function does, without needing to guess or look up the meaning.

< Good Code >

```javascript

// Good Example

let totalPrice = 150.00; // Clear and descriptive

function calculateTotalPrice(price, tax) { // Clear and descriptive

  return price + (price * tax);

}

function displayProductDetails(product) { // Clear and descriptive

  console.log(`Product: ${product.name}, Price: ${product.price}`);

}

```

<Bad Code>

```javascript

// Bad Example

let tp = 150.00; // Unclear abbreviation

function calcTP(p, t) { // Unclear abbreviation

  return p + (p * t);

}

function dspPD(p) { // Unclear abbreviation

  console.log(`Product: ${p.n}, Price: ${p.p}`);

}

```

In the good example, names like `totalPrice`, `calculateTotalPrice`, and `displayProductDetails` are self-explanatory. In the bad example, abbreviations like `tp`, `calcTP`, and `dspPD` are unclear, making the code harder to understand and maintain.

<Memo>

Did you know? Consistently using clear and descriptive names in your code can significantly reduce the onboarding time for new team members, as they won't have to decipher cryptic abbreviations.

11

# Avoid generic names like data, item, or thing.

* * *

Using specific names makes your code more readable and maintainable.

* * *

In this section, we'll illustrate why using specific variable names is essential for code clarity.

< Good Code >

```javascript

// Retrieves a user's profile by their ID

function getUserProfile(userId) {

    // Fetch user profile from the database

    let userProfile = database.fetchProfileById(userId);

    return userProfile;

}

```

<Bad Code>

```javascript

// Retrieves something by its ID

function getData(id) {

    // Fetch data from the database

    let data = database.fetch(id);

    return data;

}

```

In the good code example, `userProfile` and `userId` clearly indicate what the function handles, making the code easier to understand and maintain. In the bad code example, `data` and `id` are too generic, leading to potential confusion about what kind of data is being handled.

<Memo>

Good naming conventions can significantly reduce the cognitive load on developers, helping them to quickly grasp the functionality of the code.

12

# Be specific with names to avoid ambiguity.

* * *

Specific names help in understanding the exact purpose and usage of variables and functions.

* * *

This section demonstrates how specificity in naming can prevent misunderstandings and improve code clarity.

< Good Code >

```javascript

// Adds a product to the shopping cart

function addProductToCart(productId, quantity) {

    // Ensure the product exists

    let product = productCatalog.getProductById(productId);

    if (product) {

        cart.addItem(product, quantity);

    }

}

```

<Bad Code>

```javascript

// Adds an item

function addItem(id, num) {

    // Ensure the item exists

    let item = catalog.get(id);

    if (item) {

        cart.add(item, num);

    }

}

```

In the good code example, `addProductToCart`, `productId`, and `quantity` clearly define the function's purpose and its parameters, making it easy to understand and maintain. In the bad code example, `addItem`, `id`, and `num` are ambiguous, making it unclear what is being added and in what context.

<Memo>

Specific names not only help in understanding the code but also aid in debugging, as it's easier to trace the flow of specific entities through the application.

13

# Use consistent naming conventions throughout the codebase.

* * *

Adopt a uniform naming convention for variables, functions, and classes to enhance code readability and maintainability.

* * *

Consistent naming conventions help developers understand the purpose of variables and functions quickly, reducing the cognitive load when reading and maintaining the code.

< Good Code >

// Using camelCase for variables and functions, PascalCase for classes

let userName = 'JohnDoe';

function getUserName() {

    return userName;

}

class UserProfile {

    constructor(name) {

        this.name = name;

    }

}

<Bad Code>

// Inconsistent naming conventions

let User_name = 'JohnDoe';

function GetuserName() {

    return User_name;

}

class userprofile {

    constructor(Name) {

        this.Name = Name;

    }

}

In the good example, camelCase is used for variables and functions, and PascalCase is used for classes, making the code more predictable and easier to read. In the bad example, inconsistent naming conventions make the code harder to follow and maintain.

<Memo>

JavaScript does not enforce any specific naming conventions, but following a consistent style, such as camelCase for variables and functions and PascalCase for classes, is a widely accepted best practice.

14

# Avoid using magic numbers; use named constants instead.

* * *

Replace magic numbers with named constants to make the code more understandable and easier to maintain.

* * *

Magic numbers are hard-coded values that lack context. Using named constants provides meaningful names that explain the purpose of these values.

< Good Code >

// Using named constants

const MAX_USERS = 100;

const TIMEOUT_DURATION = 5000;

function canAddUser(currentUserCount) {

    return currentUserCount < MAX_USERS;

}

setTimeout(() => {

    console.log('Timeout reached');

}, TIMEOUT_DURATION);

<Bad Code>

// Using magic numbers

function canAddUser(currentUserCount) {

    return currentUserCount < 100;

}

setTimeout(() => {

    console.log('Timeout reached');

}, 5000);

In the good example, named constants like MAX_USERS and TIMEOUT_DURATION provide context and make the code self-explanatory. In the bad example, the magic numbers 100 and 5000 do not convey any meaning, making the code harder to understand and maintain.

<Memo>

The term "magic number" refers to the use of numeric literals directly in the code. This practice is discouraged because it can lead to errors and make the code less readable. Using named constants is a simple yet effective way to improve code quality.

15

# Ensure function names clearly describe their action.

* * *

Use descriptive function names that clearly convey the purpose and action of the function.

* * *

Functions should have names that make their purpose and behavior immediately clear to other developers reading the code.

< Good Code >

// Good example

function calculateCircleArea(radius) {

  return Math.PI * radius * radius;

}

<Bad Code>

// Bad example

function doSomething(x) {

  return Math.PI * x * x;

}

The good example uses a descriptive name calculateCircleArea that clearly explains what the function does. The bad example uses a vague name doSomething that provides no information about the function's purpose or behavior.

<Memo>

Descriptive function names improve code readability and maintainability.

16

# Utilize default function parameters for cleaner code.

* * *

Use default parameter values in function definitions to handle undefined or missing arguments.

* * *

Default function parameters allow you to provide default values for arguments, making the code more robust and easier to read.

< Good Code >

// Good example

function greetUser(name = 'User') {

  console.log(`Hello, ${name}!`);

}

greetUser('Alice'); // Output: Hello, Alice!

greetUser(); // Output: Hello, User!

<Bad Code>

// Bad example

function greetUser(name) {

  const userName = name || 'User';

  console.log(`Hello, ${userName}!`);

}

greetUser('Alice'); // Output: Hello, Alice!

greetUser(); // Output: Hello, undefined!

In the good example, the greetUser function uses a default parameter value of 'User' for the name argument. This ensures that the function behaves correctly even when called without an argument. The bad example uses a logical OR operator to handle the missing argument, but it can lead to unexpected behavior (e.g., Hello, undefined!) and is less readable.

<Memo>

Default function parameters were introduced in ECMAScript 2015 (ES6) and provide a more concise and readable way to handle optional arguments.

17

# Use async/await for asynchronous code for better readability.

* * *

Async/await simplifies the syntax of asynchronous code, making it easier to read and maintain.

* * *

Using async/await in JavaScript can improve code readability and structure, making it more understandable than traditional promise chaining.

< Good Code >

// Fetching data with async/await

async function fetchData() {

  try {

    const response = await fetch('https://api.example.com/data');

    const data = await response.json();

    console.log(data); // Output the fetched data

  } catch (error) {

    console.error('Error fetching data:', error);

  }

}

fetchData();

<Bad Code>

// Fetching data with promises

function fetchData() {

  fetch('https://api.example.com/data')

    .then(response => response.json())

    .then(data => {

      console.log(data); // Output the fetched data

    })

    .catch(error => {

      console.error('Error fetching data:', error);

    });

}

fetchData();

The good example uses async/await, making the asynchronous flow linear and easy to follow. The bad example uses promise chaining, which can become difficult to read and manage as the complexity increases. Async/await syntax makes error handling more straightforward and the code cleaner.

<Memo>

Async/await is syntactic sugar built on top of promises. It was introduced in ES2017 (ES8) and has since become the standard for writing asynchronous code in JavaScript.

18

# Employ Map and Set for collections instead of plain objects and arrays.

* * *

Maps and Sets offer more efficient and clearer ways to handle collections of data compared to plain objects and arrays.

* * *

Using Map and Set in JavaScript can provide better performance and functionality for collections, such as ensuring unique elements in Sets or maintaining key-value pairs in Maps.

< Good Code >

// Using Map for key-value pairs

const userRoles = new Map();

userRoles.set('Alice', 'Admin');

userRoles.set('Bob', 'User');

console.log(userRoles.get('Alice')); // Output: Admin

// Using Set for unique values

const uniqueNumbers = new Set([1, 2, 3, 3, 4]);

uniqueNumbers.add(5);

uniqueNumbers.add(1); // Duplicate, won't be added

uniqueNumbers.forEach(number => {

  console.log(number); // Output: 1, 2, 3, 4, 5

});

<Bad Code>

// Using plain object for key-value pairs

const userRoles = {

  Alice: 'Admin',

  Bob: 'User'

};

console.log(userRoles['Alice']); // Output: Admin

// Using array for unique values

const uniqueNumbers = [1, 2, 3, 3, 4];

uniqueNumbers.push(5);

if (!uniqueNumbers.includes(1)) {

  uniqueNumbers.push(1); // Manually checking for duplicates

}

uniqueNumbers.forEach(number => {

  console.log(number); // Output: 1, 2, 3, 3, 4, 5

});

The good example uses Map and Set, which are specifically designed for managing collections of key-value pairs and unique values, respectively. They provide built-in methods that simplify common tasks and improve performance. The bad example uses plain objects and arrays, which require additional logic for tasks like ensuring uniqueness or managing key-value pairs.

<Memo>

Map and Set were introduced in ES6 (ES2015). Maps maintain insertion order for keys, unlike objects, and Sets automatically enforce uniqueness, unlike arrays.

19

# Leverage optional chaining to handle nested object properties.

* * *

Use optional chaining to safely access deeply nested object properties without causing errors.

* * *

Optional chaining allows you to access nested properties of an object without having to check each level for existence, making your code cleaner and more readable.

< Good Code >

// Good example using optional chaining

const user = {

  profile: {

    address: {

      city: 'New York'

    }

  }

};

// Safely access nested property

const city = user?.profile?.address?.city; // 'New York'

<Bad Code>

// Bad example without optional chaining

const user = {

  profile: {

    address: {

      city: 'New York'

    }

  }

};

// Manually checking each level

let city;

if (user && user.profile && user.profile.address) {

  city = user.profile.address.city; // 'New York'

}

The good example uses optional chaining (?.) to access the nested property city safely. If any part of the chain is null or undefined, it will return undefined instead of throwing an error. The bad example manually checks each level, making the code verbose and harder to read.

<Memo>

Optional chaining was introduced in ECMAScript 2020 (ES11) and is now widely supported in modern JavaScript environments.

20

# Use Array.prototype.map and Array.prototype.filter for array transformations.

* * *

Utilize map and filter methods to transform and filter arrays in a concise and readable manner.

* * *

The map method creates a new array populated with the results of calling a provided function on every element in the calling array. The filter method creates a new array with all elements that pass the test implemented by the provided function.

< Good Code >

// Good example using map and filter

const numbers = [1, 2, 3, 4, 5];

// Double each number

const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]

// Filter out odd numbers

const evens = numbers.filter(num => num % 2 === 0); // [2, 4]

<Bad Code>

// Bad example using for loops

const numbers = [1, 2, 3, 4, 5];

// Double each number

const doubled = [];

for (let i = 0; i < numbers.length; i++) {

  doubled.push(numbers[i] * 2);

}

// Filter out odd numbers

const evens = [];

for (let i = 0; i < numbers.length; i++) {

  if (numbers[i] % 2 === 0) {

    evens.push(numbers[i]);

  }

}

The good example uses map and filter to transform and filter the array in a concise and readable way. The bad example uses for loops, which are more verbose and error-prone. Using map and filter makes the code more declarative and easier to understand.

<Memo>

The map and filter methods are part of the ECMAScript 5.1 (ES5) standard, which was released in 2011\. They are now fundamental tools for functional programming in JavaScript.

21

# Comment on the purpose of complex functions or blocks of code.

* * *

Adding comments to explain the purpose of complex functions or blocks of code helps others understand the code's intent and functionality.

* * *

When writing complex functions or blocks of code, it's crucial to include comments that describe their purpose. This practice aids in maintaining and debugging the code.

< Good Code >

// This function calculates the factorial of a number using recursion

function factorial(n) {

    // Base case: if n is 0, return 1

    if (n === 0) {

        return 1;

    }

    // Recursive case: n * factorial of (n-1)

    return n * factorial(n - 1);

}

<Bad Code>

function factorial(n) {

    if (n === 0) {

        return 1;

    }

    return n * factorial(n - 1);

}

In the good example, comments clearly explain the purpose of the function and the logic behind the base and recursive cases. This makes the code easier to understand and maintain. In the bad example, the lack of comments makes it harder for others to grasp the function's intent and logic.

<Memo>

Commenting on complex code is a best practice in software development and is often emphasized in coding standards and guidelines.

22

# Explain non-obvious code logic in comments.

* * *

Use comments to clarify non-obvious or tricky parts of the code to help others understand the logic.

* * *

When code logic is not immediately clear, adding comments to explain the reasoning or approach can prevent confusion and errors during future maintenance.

< Good Code >

// Check if the user is an admin or has a premium account

function hasAccess(user) {

    // Admins have full access

    if (user.role === 'admin') {

        return true;

    }

    // Premium users have access if their subscription is active

    if (user.subscription === 'premium' && user.isActive) {

        return true;

    }

    // All other users do not have access

    return false;

}

<Bad Code>

function hasAccess(user) {

    if (user.role === 'admin') {

        return true;

    }

    if (user.subscription === 'premium' && user.isActive) {

        return true;

    }

    return false;

}

In the good example, comments explain the logic behind each condition, making it clear why certain users have access. This helps other developers understand the decision-making process. In the bad example, the lack of comments leaves the logic open to misinterpretation, which can lead to errors or incorrect assumptions.

<Memo>

Clear and concise comments can significantly reduce the time required for code reviews and debugging, leading to more efficient development processes.

23

# Document the expected input and output for functions.

* * *

Clearly document the expected input parameters and the output of your functions.

* * *

Providing clear documentation for the expected input and output of functions helps other developers understand how to use the function correctly and what to expect from it.

< Good Code >

/**

* Calculates the sum of two numbers.

* @param {number} a - The first number.

* @param {number} b - The second number.

* @returns {number} The sum of the two numbers.

*/

function add(a, b) {

    return a + b;

}

<Bad Code>

function add(a, b) {

    return a + b;

}

In the good example, the function add is documented with comments that describe the input parameters a and b as numbers and the output as a number. This makes it clear to other developers what the function expects and what it returns. In the bad example, there is no documentation, making it harder for others to understand the function's purpose and usage.

<Memo>

Using JSDoc comments is a common practice in JavaScript to provide detailed documentation for functions, classes, and methods. It helps in generating API documentation automatically.

24

# Highlight temporary workarounds with comments.

* * *

Use comments to highlight any temporary workarounds or hacks in your code.

* * *

When you implement a temporary workaround or hack, it's important to leave a comment explaining why it's there and what needs to be done to replace it in the future.

< Good Code >

// Temporary workaround for issue #123

// This is a hack to bypass the bug in the third-party library.

// TODO: Remove this once the library is updated.

function fetchData() {

    // Hack: Manually setting the timeout to avoid the bug

    setTimeout(() => {

        // Original code

        console.log('Fetching data...');

    }, 1000);

}

<Bad Code>

function fetchData() {

    setTimeout(() => {

        console.log('Fetching data...');

    }, 1000);

}

In the good example, the comment clearly indicates that the setTimeout is a temporary workaround for a known issue (#123) and includes a TODO note to remove it once the issue is resolved. This helps other developers understand the context and the temporary nature of the code. In the bad example, there is no comment, leaving other developers unaware of the reason behind the setTimeout and the potential need to revisit this code.

<Memo>

Using TODO comments is a good practice to keep track of temporary solutions and ensure they are addressed in future updates. Many code editors and IDEs can highlight TODO comments, making them easier to find.

25

# Use comments to indicate important sections of code.

* * *

Comments help to highlight and explain significant parts of the code.

* * *

Using comments to mark important sections makes the code easier to navigate and understand.

< Good Code >

// Initialize variables

let total = 0;

let count = 0;

// Loop through array

for (let i = 0; i < numbers.length; i++) {

  total += numbers[i];

  count++;

}

// Calculate average

let average = total / count;

console.log(average);

<Bad Code>

let total = 0;

let count = 0;

for (let i = 0; i < numbers.length; i++) {

  total += numbers[i];

  count++;

}

let average = total / count;

console.log(average);

In the good example, comments clearly indicate the purpose of each section, making it easier for others to follow the logic. The bad example lacks comments, making it harder to understand the structure and purpose of the code.

<Memo>

Comments do not affect the execution of the code but are crucial for maintaining and understanding the codebase, especially in collaborative environments.

26

# Keep comments concise and to the point.

* * *

Comments should be brief and directly related to the code they describe.

* * *

Concise comments prevent clutter and ensure that the code remains readable and maintainable.

< Good Code >

// Sum the values in the array

let sum = numbers.reduce((acc, num) => acc + num, 0);

// Output the result

console.log(sum);

<Bad Code>

// This is a loop that goes through each element in the array called numbers and adds each element to the accumulator, which starts at 0, and then it returns the total sum of all the elements in the array

let sum = numbers.reduce((acc, num) => acc + num, 0);

// This line prints the sum to the console

console.log(sum);

The good example uses short, clear comments that directly explain the code's purpose. The bad example has overly verbose comments that add unnecessary detail, making the code harder to read.

<Memo>

Excessive commenting can be as detrimental as no commenting. Aim for a balance where comments add value without overwhelming the reader.

27

# Update comments when code changes to maintain accuracy.

* * *

Always update comments to reflect changes in the code to ensure they remain accurate and helpful.

* * *

When you modify your code, it's crucial to update the associated comments to prevent misinformation and confusion for future readers.

< Good Code >

// Calculate the area of a rectangle

function calculateArea(width, height) {

    return width * height; // Area = width * height

}

// Updated to include validation

// Calculate the area of a rectangle with validation

function calculateArea(width, height) {

    if (width <= 0 || height <= 0) {

        throw new Error('Width and height must be positive numbers');

    }

    return width * height; // Area = width * height

}

<Bad Code>

// Calculate the area of a rectangle

function calculateArea(width, height) {

    return width * height; // Area = width * height

}

// Updated to include validation, but comment not updated

function calculateArea(width, height) {

    if (width <= 0 || height <= 0) {

        throw new Error('Width and height must be positive numbers');

    }

    return width * height; // Area = width * height

}

In the good example, the comment is updated to reflect the new validation logic, ensuring that anyone reading the code understands the current functionality. In the bad example, the comment remains outdated, which can mislead readers about the code's behavior.

<Memo>

Consistently updating comments helps maintain code quality and reduces the risk of bugs caused by misunderstandings of the code's purpose and functionality.

28

# Avoid redundant comments that state the obvious.

* * *

Avoid writing comments that simply restate what the code is doing, as they add no value and clutter the code.

* * *

Comments should provide additional context or explanations that are not immediately clear from the code itself, rather than stating the obvious.

< Good Code >

// Calculate the area of a rectangle

function calculateArea(width, height) {

    return width * height; // Area = width * height

}

// Check if the user is an adult

function isAdult(age) {

    return age >= 18; // Returns true if age is 18 or older

}

<Bad Code>

// This function calculates the area of a rectangle

function calculateArea(width, height) {

    return width * height; // This returns the area

}

// This function checks if the user is an adult

function isAdult(age) {

    return age >= 18; // This returns true if the age is 18 or older

}

In the good example, comments provide meaningful context that complements the code. In the bad example, comments are redundant and merely restate what the code already clearly expresses, adding unnecessary clutter.

<Memo>

Effective comments should enhance the readability of the code by providing insights that are not immediately obvious, rather than repeating what the code already conveys.

29

# Use comments to explain the why, not the what.

* * *

Comments should provide context and reasoning behind the code, not just describe what the code does.

* * *

The following code demonstrates how to use comments effectively by explaining the purpose behind the code rather than just describing its functionality.

< Good Code >

// Calculate the total price after discount

// This is necessary to provide a better deal for loyal customers

function calculateTotalPrice(price, discount) {

    return price - (price * discount);

}

<Bad Code>

// Subtract discount from price

function calculateTotalPrice(price, discount) {

    return price - (price * discount);

}

In the good example, the comment explains the reason for calculating the total price after discount, providing context for future readers. In the bad example, the comment merely describes what the code does, which is already clear from the code itself.

<Memo>

Effective comments can significantly improve code maintainability and help new developers understand the codebase more quickly.

30

# Write comments in proper English with correct grammar.

* * *

Comments should be written in clear, proper English with correct grammar to ensure they are easily understood by all readers.

* * *

The following code demonstrates the importance of writing comments in proper English with correct grammar.

< Good Code >

// Calculate the total price after applying the discount.

// This ensures that loyal customers receive the best possible deal.

function calculateTotalPrice(price, discount) {

    return price - (price * discount);

}

<Bad Code>

// calc total price after discount

// this make sure loyal customers get best deal

function calculateTotalPrice(price, discount) {

    return price - (price * discount);

}

In the good example, the comments are written in complete sentences with proper grammar, making them clear and professional. In the bad example, the comments are written in shorthand and contain grammatical errors, which can lead to misunderstandings and appear unprofessional.

<Memo>

Using proper English in comments not only improves readability but also reflects a professional coding standard, which is especially important in collaborative environments.

31

# Take advantage of ES6 classes for object-oriented programming.

* * *

Use ES6 classes to create clean, modular, and reusable code in JavaScript.

* * *

ES6 classes provide a clear and concise syntax for creating objects and dealing with inheritance, making your code more readable and maintainable.

< Good Code >

// Good example using ES6 classes

class Animal {

  constructor(name) {

    this.name = name;

  }

  speak() {

    console.log(`${this.name} makes a noise.`);

  }

}

class Dog extends Animal {

  constructor(name) {

    super(name);

  }

  speak() {

    console.log(`${this.name} barks.`);

  }

}

const dog = new Dog('Rex');

dog.speak(); // Rex barks.

<Bad Code>

// Bad example using ES5 function constructors

function Animal(name) {

  this.name = name;

}

Animal.prototype.speak = function() {

  console.log(this.name + ' makes a noise.');

};

function Dog(name) {

  Animal.call(this, name);

}

Dog.prototype = Object.create(Animal.prototype);

Dog.prototype.constructor = Dog;

Dog.prototype.speak = function() {

  console.log(this.name + ' barks.');

};

var dog = new Dog('Rex');

dog.speak(); // Rex barks.

The good example uses ES6 classes, which provide a more intuitive and less error-prone way to create objects and handle inheritance. The bad example uses ES5 function constructors and prototype chaining, which are more verbose and harder to read.

<Memo>

ES6 classes are syntactic sugar over JavaScript's existing prototype-based inheritance model. They do not introduce a new object-oriented inheritance model to the language.

32

# Use Promise.all for running multiple promises concurrently.

* * *

Leverage Promise.all to handle multiple asynchronous operations concurrently and efficiently.

* * *

Promise.all allows you to run multiple promises in parallel and wait for all of them to resolve or any to reject, making it easier to manage concurrent asynchronous tasks.

< Good Code >

// Good example using Promise.all

const promise1 = fetch('https://api.example.com/data1');

const promise2 = fetch('https://api.example.com/data2');

const promise3 = fetch('https://api.example.com/data3');

Promise.all([promise1, promise2, promise3])

  .then(responses => Promise.all(responses.map(response => response.json())))

  .then(data => {

    console.log(data); // Array of results from all promises

  })

  .catch(error => {

    console.error('One of the promises failed:', error);

  });

<Bad Code>

// Bad example without using Promise.all

const promise1 = fetch('https://api.example.com/data1');

const promise2 = fetch('https://api.example.com/data2');

const promise3 = fetch('https://api.example.com/data3');

promise1

  .then(response1 => response1.json())

  .then(data1 => {

    console.log(data1);

    return promise2;

  })

  .then(response2 => response2.json())

  .then(data2 => {

    console.log(data2);

    return promise3;

  })

  .then(response3 => response3.json())

  .then(data3 => {

    console.log(data3);

  })

  .catch(error => {

    console.error('One of the promises failed:', error);

  });

The good example uses Promise.all to run all fetch requests concurrently, which is more efficient and results in cleaner code. The bad example runs the promises sequentially, which is less efficient and harder to read.

<Memo>

Promise.all will reject immediately if any of the input promises reject, and it will resolve only when all input promises have resolved.

33

# Utilize Object.keys and Object.values for object iteration.

* * *

Use Object.keys and Object.values to iterate over object properties and values efficiently.

* * *

When working with objects in JavaScript, iterating over their properties and values can be done more cleanly and readably using Object.keys and Object.values.

< Good Code >

const user = {

  name: 'Alice',

  age: 25,

  city: 'Wonderland'

};

// Iterating over keys

Object.keys(user).forEach(key => {

  console.log(`${key}: ${user[key]}`);

});

// Iterating over values

Object.values(user).forEach(value => {

  console.log(value);

});

<Bad Code>

const user = {

  name: 'Alice',

  age: 25,

  city: 'Wonderland'

};

// Using for...in loop

for (let key in user) {

  if (user.hasOwnProperty(key)) {

    console.log(`${key}: ${user[key]}`);

  }

}

// Using for...in loop for values

for (let key in user) {

  if (user.hasOwnProperty(key)) {

    console.log(user[key]);

  }

}

The good example uses Object.keys and Object.values to iterate over the object's properties and values, making the code more readable and avoiding the need for hasOwnProperty checks. The bad example uses a for...in loop, which requires additional checks to ensure only the object's own properties are iterated over, making the code less clean.

<Memo>

Object.entries can also be used to iterate over both keys and values simultaneously, providing an array of key-value pairs.

34

# Use the ?? (nullish coalescing) operator for default values.

* * *

The ?? operator provides a concise way to assign default values when dealing with null or undefined.

* * *

The nullish coalescing operator (??) is a useful tool in JavaScript for setting default values when a variable is null or undefined, making the code more readable and avoiding common pitfalls with falsy values.

< Good Code >

let userInput = null;

let defaultText = 'Default text';

// Using ?? operator

let displayText = userInput ?? defaultText;

console.log(displayText); // Output: 'Default text'

<Bad Code>

let userInput = null;

let defaultText = 'Default text';

// Using || operator

let displayText = userInput || defaultText;

console.log(displayText); // Output: 'Default text'

The good example uses the ?? operator to assign defaultText only if userInput is null or undefined, ensuring that other falsy values like 0 or '' are not mistakenly replaced. The bad example uses the || operator, which would replace any falsy value, not just null or undefined, potentially leading to unintended behavior.

<Memo>

The ?? operator was introduced in ECMAScript 2020 (ES11) and is particularly useful in scenarios where 0, false, or '' are valid values that should not trigger the default assignment.

35

# Employ fetch for making network requests instead of older methods like XMLHttpRequest.

* * *

Use the modern fetch API for network requests to write cleaner and more readable code.

* * *

The fetch API is a modern, promise-based way to make network requests in JavaScript. It is more powerful and flexible than the older XMLHttpRequest method, and it leads to more readable and maintainable code.

< Good Code >

// Good example using fetch

fetch('https://api.example.com/data')

  .then(response => {

    if (!response.ok) {

      throw new Error('Network response was not ok');

    }

    return response.json();

  })

  .then(data => {

    console.log(data); // Handle the data from the API

  })

  .catch(error => {

    console.error('There was a problem with the fetch operation:', error);

  });

<Bad Code>

// Bad example using XMLHttpRequest

var xhr = new XMLHttpRequest();

xhr.open('GET', 'https://api.example.com/data', true);

xhr.onreadystatechange = function () {

  if (xhr.readyState === 4) {

    if (xhr.status === 200) {

      var data = JSON.parse(xhr.responseText);

      console.log(data); // Handle the data from the API

    } else {

      console.error('There was a problem with the request:', xhr.statusText);

    }

  }

};

xhr.send();

The fetch API simplifies the process of making network requests by using promises, which makes the code more readable and easier to handle asynchronous operations. In contrast, XMLHttpRequest requires more boilerplate code and is less intuitive. The fetch API also provides better error handling and more powerful features.

<Memo>

The fetch API was introduced in 2015 as part of the Fetch Living Standard and is now widely supported in modern browsers. It is designed to be more flexible and easier to use than XMLHttpRequest.

36

# Consistently format your code with a linter like ESLint.

* * *

Use a linter like ESLint to ensure consistent code formatting and catch potential errors early.

* * *

ESLint is a popular JavaScript linter that helps developers maintain consistent code style and catch potential errors before they become issues. By integrating ESLint into your development workflow, you can ensure that your codebase remains clean and readable.

< Good Code >

// Good example with ESLint rules applied

function add(a, b) {

  if (typeof a !== 'number' || typeof b !== 'number') {

    throw new TypeError('Both arguments must be numbers');

  }

  return a + b;

}

const result = add(2, 3);

console.log(result); // Outputs: 5

<Bad Code>

// Bad example without ESLint rules

function add(a, b) {

if (typeof a != 'number' || typeof b != 'number') {

throw new TypeError('Both arguments must be numbers')

}

return a+b;

}

var result = add(2,3)

console.log(result) // Outputs: 5

Using ESLint helps enforce consistent coding standards across your project, making it easier for multiple developers to collaborate. It can automatically fix some issues and provide warnings for others, ensuring that your code adheres to best practices. The bad example shows inconsistent indentation, missing semicolons, and improper use of var instead of const, all of which can be caught and corrected by ESLint.

<Memo>

ESLint was created by Nicholas C. Zakas in 2013 to help developers write consistent and error-free JavaScript code. It is highly configurable and supports custom rules, making it a versatile tool for any JavaScript project.

37

# Use Prettier for automatic code formatting.

* * *

Prettier is a code formatter that enforces a consistent style by parsing your code and re-printing it with its own rules.

* * *

Using Prettier helps maintain a uniform code style across your project, making it easier for others to read and understand your code.

< Good Code >

// Good: Consistent formatting with Prettier

function greet(name) {

  console.log(`Hello, ${name}!`);

}

greet('Alice');

<Bad Code>

// Bad: Inconsistent formatting

function greet(name) { console.log("Hello, " + name + "!"); }

greet( 'Alice' );

Prettier automatically formats your code according to a set of rules, ensuring consistency. In the good example, the code is neatly formatted with proper indentation and spacing. In the bad example, the code has inconsistent spacing and formatting, making it harder to read.

<Memo>

Prettier supports many languages and integrates with most editors, making it a versatile tool for maintaining code quality.

38

# Organize your code with consistent indentation.

* * *

Consistent indentation improves code readability and helps in understanding the structure and flow of the code.

* * *

Proper indentation is crucial for making your code readable and maintainable. It visually separates code blocks and makes it easier to follow the logic.

< Good Code >

// Good: Consistent indentation

if (true) {

  console.log('This is properly indented.');

  if (true) {

    console.log('Nested block is also properly indented.');

  }

}

<Bad Code>

// Bad: Inconsistent indentation

if (true) {

console.log('This is not properly indented.');

  if (true) {

console.log('Nested block is also not properly indented.');

  }

}

Consistent indentation helps in understanding the code structure at a glance. In the good example, each block is indented properly, making the code easy to follow. In the bad example, inconsistent indentation makes it difficult to discern the code structure, leading to potential errors and misunderstandings.

<Memo>

Most modern code editors can be configured to enforce consistent indentation, either with spaces or tabs, according to your project's style guide.

39

# Group related code together logically.

* * *

Organize your code by grouping related functions, variables, and classes together.

* * *

Grouping related code together helps in understanding the structure and flow of the program. It makes the code more maintainable and easier to navigate.

< Good Code >

// User-related functions

function createUser(name, age) {

    return { name, age };

}

function getUser(id) {

    // logic to get user by id

}

// Product-related functions

function createProduct(name, price) {

    return { name, price };

}

function getProduct(id) {

    // logic to get product by id

}

<Bad Code>

function createUser(name, age) {

    return { name, age };

}

function createProduct(name, price) {

    return { name, price };

}

function getUser(id) {

    // logic to get user by id

}

function getProduct(id) {

    // logic to get product by id

}

In the good example, user-related functions are grouped together, and product-related functions are grouped together. This logical grouping makes it easier to find and understand the code related to a specific feature. In the bad example, functions are scattered, making it harder to navigate and understand the code.

<Memo>

Logical grouping of code is a principle of the Single Responsibility Principle (SRP) from SOLID principles, which states that a class or module should have one, and only one, reason to change.

40

# Limit the length of lines to improve readability.

* * *

Keep your lines of code short, ideally under 80 characters, to enhance readability.

* * *

Long lines of code can be difficult to read and understand. Breaking them into shorter lines makes the code more readable and maintainable.

< Good Code >

// Good: Short lines of code

function calculateTotal(price, taxRate) {

    const tax = price * taxRate;

    const total = price + tax;

    return total;

}

const totalPrice = calculateTotal(100, 0.08);

console.log(totalPrice);

<Bad Code>

// Bad: Long line of code

function calculateTotal(price, taxRate) { const tax = price * taxRate; const total = price + tax; return total; } const totalPrice = calculateTotal(100, 0.08); console.log(totalPrice);

In the good example, the code is broken into multiple lines, making it easier to read and understand each part. In the bad example, the code is written in a single long line, which is hard to read and understand quickly.

<Memo>

The 80-character limit for line length is a convention that dates back to the early days of computing and is still widely recommended in many coding standards, including PEP 8 for Python.

41

# Use early returns to avoid nested if statements.

* * *

Simplify your code by using early returns instead of deeply nested if statements.

* * *

Deeply nested if statements can make code difficult to read and understand. Using early returns can simplify the logic and improve readability.

< Good Code >

function processValue(value) {

    if (value === null) {

        return 'Value is null';

    }

    if (value === undefined) {

        return 'Value is undefined';

    }

    if (typeof value !== 'number') {

        return 'Value is not a number';

    }

    return value * 2; // Value is a valid number, process it

}

<Bad Code>

function processValue(value) {

    if (value !== null) {

        if (value !== undefined) {

            if (typeof value === 'number') {

                return value * 2; // Value is a valid number, process it

            } else {

                return 'Value is not a number';

            }

        } else {

            return 'Value is undefined';

        }

    } else {

        return 'Value is null';

    }

}

In the good example, each condition is checked and handled immediately, making the code easy to follow. The bad example nests each condition inside the previous one, leading to deeply nested and hard-to-read code.

<Memo>

Early returns can also help in reducing the cognitive load on the reader, making it easier to identify the main logic of the function.

42

# Favor switch statements for multiple condition checks.

* * *

Use switch statements instead of multiple if-else statements for better readability and maintainability.

* * *

When dealing with multiple conditions that depend on the same variable, switch statements provide a clearer and more organized way to handle the logic.

< Good Code >

function getFruitColor(fruit) {

    switch (fruit) {

        case 'apple':

            return 'red';

        case 'banana':

            return 'yellow';

        case 'grape':

            return 'purple';

        case 'orange':

            return 'orange';

        default:

            return 'unknown';

    }

}

<Bad Code>

function getFruitColor(fruit) {

    if (fruit === 'apple') {

        return 'red';

    } else if (fruit === 'banana') {

        return 'yellow';

    } else if (fruit === 'grape') {

        return 'purple';

    } else if (fruit === 'orange') {

        return 'orange';

    } else {

        return 'unknown';

    }

}

The good example uses a switch statement, which is concise and easy to read. The bad example uses multiple if-else statements, which can be harder to read and maintain, especially as the number of conditions grows.

<Memo>

Switch statements can be more efficient than multiple if-else statements in some cases, as they provide a clear structure for the conditions being checked.

43

# Avoid deeply nested loops by breaking them into functions.

* * *

Simplify complex nested loops by refactoring them into separate functions to improve readability and maintainability.

* * *

Deeply nested loops can make code difficult to read and understand. Breaking them into smaller, well-named functions can help clarify the logic and make the code more maintainable.

< Good Code >

// Good example: Breaking nested loops into functions

function processRow(row) {

  row.forEach(cell => {

    // Process each cell

    console.log(cell);

  });

}

function processTable(table) {

  table.forEach(row => {

    processRow(row);

  });

}

const table = [

  [1, 2, 3],

  [4, 5, 6],

  [7, 8, 9]

];

processTable(table);

<Bad Code>

// Bad example: Deeply nested loops

const table = [

  [1, 2, 3],

  [4, 5, 6],

  [7, 8, 9]

];

for (let i = 0; i < table.length; i++) {

  for (let j = 0; j < table[i].length; j++) {

    // Process each cell

    console.log(table[i][j]);

  }

}

In the good example, the nested loops are broken into processRow and processTable functions, making the code more modular and easier to understand. In the bad example, the deeply nested loops make the code harder to read and maintain.

<Memo>

Refactoring nested loops into functions not only improves readability but also allows for easier testing and debugging of individual parts of the code.

44

# Use try/catch blocks for error handling.

* * *

Implement try/catch blocks to handle errors gracefully and prevent your application from crashing unexpectedly.

* * *

Error handling is crucial in any application to ensure it can handle unexpected situations without crashing. Using try/catch blocks allows you to manage errors and provide meaningful feedback or recovery options.

< Good Code >

// Good example: Using try/catch for error handling

function parseJSON(jsonString) {

  try {

    const data = JSON.parse(jsonString);

    console.log('Parsed data:', data);

  } catch (error) {

    console.error('Failed to parse JSON:', error.message);

  }

}

const jsonString = '{"name": "John", "age": 30}';

parseJSON(jsonString);

const invalidJsonString = '{"name": "John", "age": 30';

parseJSON(invalidJsonString);

<Bad Code>

// Bad example: No error handling

function parseJSON(jsonString) {

  const data = JSON.parse(jsonString);

  console.log('Parsed data:', data);

}

const jsonString = '{"name": "John", "age": 30}';

parseJSON(jsonString);

const invalidJsonString = '{"name": "John", "age": 30';

parseJSON(invalidJsonString); // This will throw an error and crash the application

In the good example, the parseJSON function uses a try/catch block to handle potential errors when parsing JSON. This prevents the application from crashing and provides a clear error message. In the bad example, the lack of error handling means that any error will cause the application to crash.

<Memo>

Using try/catch blocks not only helps in handling errors but also in debugging, as it allows you to log detailed error messages and understand what went wrong in your code.

45

# Keep functions short and focused on a single task.

* * *

Write functions that perform a single, well-defined task to improve readability and maintainability.

* * *

A function should do one thing and do it well. This makes the code easier to understand, test, and debug.

< Good Code >

// Function to calculate the area of a rectangle

function calculateRectangleArea(width, height) {

    return width * height;

}

// Function to calculate the area of a circle

function calculateCircleArea(radius) {

    return Math.PI * radius * radius;

}

<Bad Code>

// Function that calculates the area of a rectangle or a circle based on the shape type

function calculateArea(shape, width, height, radius) {

    if (shape === 'rectangle') {

        return width * height;

    } else if (shape === 'circle') {

        return Math.PI * radius * radius;

    }

    return 0;

}

In the good example, each function has a single responsibility, making it clear what each function does. In the bad example, the function tries to handle multiple shapes, making it more complex and harder to understand.

<Memo>

The Single Responsibility Principle (SRP) is one of the SOLID principles of object-oriented design, which states that a class or function should have only one reason to change.

46

# Use descriptive function names that convey their purpose.

* * *

Choose function names that clearly describe what the function does to improve code readability.

* * *

Descriptive names help other developers understand the purpose of a function without needing to read its implementation.

< Good Code >

// Function to fetch user data from an API

function fetchUserData(userId) {

    // Implementation to fetch user data

}

// Function to validate email format

function isValidEmail(email) {

    // Implementation to validate email

}

<Bad Code>

// Function with a vague name

function getData(id) {

    // Implementation to fetch user data

}

// Function with a non-descriptive name

function checkEmail(e) {

    // Implementation to validate email

}

In the good example, the function names clearly indicate their purpose, making the code easier to read and understand. In the bad example, the names are vague and do not provide enough context about what the functions do.

<Memo>

Using descriptive names is part of the Clean Code principles, which emphasize writing code that is easy to read and understand.

47

# Write pure functions that do not have side effects.

* * *

Pure functions return the same result given the same arguments and do not cause side effects.

* * *

A pure function is a function that, given the same input, will always return the same output and does not have any side effects (like modifying a global variable or outputting to the console).

< Good Code >

// A pure function that adds two numbers

function add(a, b) {

    return a + b; // Always returns the same output for the same inputs

}

console.log(add(2, 3)); // 5

console.log(add(2, 3)); // 5

<Bad Code>

let sum = 0;

// An impure function that adds two numbers

function add(a, b) {

    sum = a + b; // Modifies a global variable

    console.log(sum); // Produces side effects

}

add(2, 3); // Logs 5 and changes sum

add(2, 3); // Logs 5 and changes sum again

Pure functions are easier to test and debug because they do not depend on or alter the state outside their scope. The bad example shows an impure function that modifies a global variable and logs to the console, making it harder to predict and test its behavior.

<Memo>

Pure functions are a fundamental concept in functional programming, which emphasizes immutability and the use of pure functions to create predictable and reliable code.

48

# Avoid using global variables.

* * *

Global variables can lead to code that is difficult to understand and maintain due to their wide-reaching impact.

* * *

Global variables are accessible throughout your entire codebase, which can lead to unintended interactions and bugs. It's better to use local variables or pass variables as parameters to functions.

< Good Code >

// Function that uses local variables

function calculateTotal(price, tax) {

    const total = price + tax;

    return total; // Uses local variable 'total'

}

console.log(calculateTotal(100, 10)); // 110

console.log(calculateTotal(200, 20)); // 220

<Bad Code>

let total = 0; // Global variable

// Function that uses global variable

function calculateTotal(price, tax) {

    total = price + tax; // Modifies global variable

    return total;

}

calculateTotal(100, 10); // 110

console.log(total); // 110

calculateTotal(200, 20); // 220

console.log(total); // 220

Using global variables can cause unexpected behavior and make debugging difficult because any part of the code can change their value. The good example confines variables to the function scope, making the function's behavior more predictable and isolated.

<Memo>

JavaScript's let and const keywords help limit the scope of variables, reducing the chances of accidentally creating global variables and improving code maintainability.

49

# Use constants for values that do not change.

* * *

Using constants for values that do not change improves code readability and maintainability.

* * *

When a value is not supposed to change throughout the execution of a program, it is best to declare it as a constant. This practice helps other developers understand that the value is fixed and should not be modified.

< Good Code >

// Good example: Using constants for fixed values

const MAX_USERS = 100;

const API_URL = 'https://api.example.com/data';

function fetchData() {

  fetch(API_URL)

    .then(response => response.json())

    .then(data => console.log(data));

}

console.log(`The maximum number of users is ${MAX_USERS}`);

<Bad Code>

// Bad example: Using variables for fixed values

let maxUsers = 100;

let apiUrl = 'https://api.example.com/data';

function fetchData() {

  fetch(apiUrl)

    .then(response => response.json())

    .then(data => console.log(data));

}

console.log(`The maximum number of users is ${maxUsers}`);

In the good example, MAX_USERS and API_URL are declared as constants using const, indicating that their values should not change. This makes the code easier to understand and maintain. In the bad example, maxUsers and apiUrl are declared using let, which implies that their values might change, potentially causing confusion.

<Memo>

In JavaScript, constants are block-scoped, similar to variables declared using let. They cannot be reassigned, but if the constant is an object or array, the contents can still be modified.

50

# Leverage async generators for handling async iteration.

* * *

Async generators provide a powerful way to handle asynchronous iteration, making code more readable and efficient.

* * *

Async generators allow you to iterate over asynchronous data sources using the for await...of loop. This technique simplifies the handling of asynchronous operations, such as fetching data from an API, by allowing you to process each piece of data as it becomes available.

< Good Code >

// Good example: Using async generators for async iteration

async function* fetchData() {

  const urls = ['https://api.example.com/data1', 'https://api.example.com/data2'];

  for (const url of urls) {

    const response = await fetch(url);

    const data = await response.json();

    yield data;

  }

}

(async () => {

  for await (const data of fetchData()) {

    console.log(data);

  }

})();

<Bad Code>

// Bad example: Using Promises without async generators

const urls = ['https://api.example.com/data1', 'https://api.example.com/data2'];

function fetchData() {

  return Promise.all(urls.map(url => fetch(url).then(response => response.json())));

}

fetchData().then(dataArray => {

  dataArray.forEach(data => console.log(data));

});

In the good example, an async generator function fetchData is used to fetch data from multiple URLs. The for await...of loop allows processing each piece of data as it is fetched, making the code more readable and efficient. In the bad example, Promise.all is used to fetch all data at once, which can be less efficient and harder to read.

<Memo>

Async generators were introduced in ECMAScript 2018 (ES9). They combine the capabilities of generators and async functions, allowing you to work with asynchronous data streams in a more natural and readable way.

51

# Utilize WeakMap and WeakSet for managing object keys without preventing garbage collection.

* * *

WeakMap and WeakSet allow you to manage object keys without preventing their garbage collection, enhancing memory efficiency.

* * *

Using WeakMap and WeakSet can help manage object keys and references while ensuring that these objects can be garbage collected when no longer needed. This is especially useful for caching or tracking objects in a way that avoids memory leaks.

< Good Code >

// Good Example: Using WeakMap to store metadata for objects

const metadata = new WeakMap();

function addMetadata(obj, info) {

  metadata.set(obj, info); // Associate metadata with the object

}

function getMetadata(obj) {

  return metadata.get(obj); // Retrieve metadata for the object

}

const obj1 = {};

addMetadata(obj1, { role: 'admin' });

console.log(getMetadata(obj1)); // Outputs: { role: 'admin' }

// obj1 can be garbage collected when no longer referenced

<Bad Code>

// Bad Example: Using a regular Map which prevents garbage collection

const metadata = new Map();

function addMetadata(obj, info) {

  metadata.set(obj, info); // Associate metadata with the object

}

function getMetadata(obj) {

  return metadata.get(obj); // Retrieve metadata for the object

}

const obj1 = {};

addMetadata(obj1, { role: 'admin' });

console.log(getMetadata(obj1)); // Outputs: { role: 'admin' }

// obj1 cannot be garbage collected even if it's no longer referenced

In the good example, WeakMap allows obj1 to be garbage collected when it is no longer in use, because WeakMap holds a weak reference to the object. In the bad example, using a regular Map prevents obj1 from being garbage collected due to the strong reference held by the Map.

<Memo>

WeakMap keys must be objects, not primitive values. This is because WeakMaps are designed to allow the keys (objects) to be garbage collected, which is not applicable to primitive values.

52

# Use Proxy objects for custom behavior of fundamental operations.

* * *

Proxy objects in JavaScript allow you to define custom behavior for fundamental operations like property lookup, assignment, enumeration, and function invocation.

* * *

Using Proxy objects can help you intercept and redefine operations for objects. This is useful for logging, validation, or implementing observable objects, among other applications.

< Good Code >

// Good Example: Using Proxy to log property access

const handler = {

  get(target, property) {

    console.log(`Property ${property} has been accessed.`);

    return target[property];

  }

};

const obj = { name: 'John', age: 30 };

const proxy = new Proxy(obj, handler);

console.log(proxy.name); // Logs: Property name has been accessed. Outputs: John

console.log(proxy.age);  // Logs: Property age has been accessed. Outputs: 30

<Bad Code>

// Bad Example: Directly adding logging in every property access

const obj = { name: 'John', age: 30 };

function getName() {

  console.log('Property name has been accessed.');

  return obj.name;

}

function getAge() {

  console.log('Property age has been accessed.');

  return obj.age;

}

console.log(getName()); // Logs: Property name has been accessed. Outputs: John

console.log(getAge());  // Logs: Property age has been accessed. Outputs: 30

In the good example, a Proxy is used to intercept property access operations, providing a clean and reusable way to add custom behavior. In the bad example, logging is added directly to functions, making the code less maintainable and harder to scale as more properties are added.

<Memo>

Proxies can also be used to create virtual objects, which do not have real properties but can respond to property accesses dynamically. This is useful in scenarios like implementing database-backed objects or complex caching mechanisms.

53

# Leverage Symbol for unique property keys to avoid conflicts.

* * *

Use Symbols to create unique property keys in objects, preventing key collisions.

* * *

Symbols in JavaScript offer a way to create unique identifiers for object properties, ensuring that these keys are unique and avoiding potential conflicts with other keys.

< Good Code >

// Create a unique symbol

const uniqueKey = Symbol('uniqueKey');

// Using the symbol as a property key in an object

const myObject = {

  [uniqueKey]: 'This is a unique property value',

  commonKey: 'This is a common property value'

};

console.log(myObject[uniqueKey]); // Output: This is a unique property value

<Bad Code>

// Using a string as a property key

const myObject = {

  uniqueKey: 'This is supposed to be unique',

  commonKey: 'This is a common property value',

  uniqueKey: 'This is overwritten'

};

console.log(myObject.uniqueKey); // Output: This is overwritten

Using Symbols as property keys ensures that each key is unique and cannot be accidentally overwritten. In the bad example, using a string key results in the 'uniqueKey' property being overwritten, whereas in the good example, the Symbol ensures the key remains unique.

<Memo>

Symbols are a primitive data type introduced in ECMAScript 2015 (ES6) and are not enumerable, meaning they do not appear in for...in loops.

54

# Employ tagged template literals for safe HTML or SQL templates.

* * *

Use tagged template literals to create secure and well-formatted HTML or SQL templates.

* * *

Tagged template literals in JavaScript provide a powerful way to process and sanitize template literals, which can be particularly useful for creating safe HTML or SQL templates.

< Good Code >

// Tag function to escape HTML

function escapeHTML(literals, ...placeholders) {

  let result = '';

  // Loop through each literal and placeholder

  for (let i = 0; i < placeholders.length; i++) {

    result += literals[i] + String(placeholders[i]).replace(/&/g, '&amp;')

                                                  .replace(/</g, '&lt;')

                                                  .replace(/>/g, '&gt;')

                                                  .replace(/"/g, '&quot;')

                                                  .replace(/'/g, '&#39;');

  }

  result += literals[literals.length - 1];

  return result;

}

// Usage of tagged template literal

const name = '<script>alert("xss")</script>';

const safeHTML = escapeHTML`<div>Hello, ${name}!</div>`;

console.log(safeHTML); // Output: <div>Hello, &lt;script&gt;alert(&quot;xss&quot;)&lt;/script&gt;!</div>

<Bad Code>

// Directly embedding variables in HTML template

const name = '<script>alert("xss")</script>';

const unsafeHTML = `<div>Hello, ${name}!</div>`;

console.log(unsafeHTML); // Output: <div>Hello, <script>alert("xss")</script>!</div>

Tagged template literals allow you to process template literals with a tag function before embedding values. This is crucial for security, as demonstrated in the good example, where the escapeHTML function sanitizes the input. In the bad example, direct embedding can lead to security vulnerabilities like XSS.

<Memo>

Tagged template literals are an advanced feature introduced in ECMAScript 2015 (ES6), allowing custom processing of template literals using tag functions.

55

# Use the Reflect API to perform object operations

* * *

The Reflect API provides methods for performing operations on objects, avoiding the need for workarounds.

* * *

Instead of using object property accessors directly, the Reflect API provides a cleaner way to perform operations on objects.

< Good Code >

jsconst obj = { x: 1, y: 2 };

// Get property value

console.log(Reflect.get(obj, 'x')); // Output: 1

// Set property value

Reflect.set(obj, 'x', 3);

console.log(obj.x); // Output: 3

// Check if property exists

console.log(Reflect.has(obj, 'y')); // Output: true

<Bad Code>

jsconst obj = { x: 1, y: 2 };

// Get property value

console.log(obj['x']); // Output: 1

// Set property value

obj['x'] = 3;

console.log(obj.x); // Output: 3

// Check if property exists

console.log('y' in obj); // Output: true

The Reflect API provides a more functional approach to working with objects, making the code more readable and maintainable. It also allows for better handling of edge cases and provides a consistent way of performing object operations.

<Memo>

The Reflect API was introduced in ECMAScript 6 (ES6) and is part of the standard library.

56

# Declare variables as close as possible to their usage

* * *

Declare variables as close as possible to where they are used to improve code readability and maintainability.

* * *

By declaring variables closer to their usage, you can better understand the scope and purpose of the variable, making the code easier to read and maintain.

< Good Code >

jsfunction calculateArea(radius) {

  const PI = 3.14159; // Declare PI constant close to its usage

  const area = PI * radius ** 2;

  return area;

}

const radius = 5;

const circleArea = calculateArea(radius);

console.log(circleArea); // Output: 78.53975

<Bad Code>

jsconst PI = 3.14159; // Declare PI constant far from its usage

function calculateArea(radius) {

  const area = PI * radius ** 2;

  return area;

}

const radius = 5;

const circleArea = calculateArea(radius);

console.log(circleArea); // Output: 78.53975

Declaring variables closer to their usage improves code readability by providing context and reducing the cognitive load required to understand the code. It also helps prevent naming conflicts and makes it easier to reason about the scope of variables.

<Memo>

This principle is often referred to as the "Principle of Least Surprise" or the "Principle of Proximity" in software engineering.

57

# Use meaningful names for loop counters.

* * *

Using descriptive names for loop counters improves code readability and maintainability.

* * *

When writing loops, it's common to use single-letter variables like i, j, or k as loop counters. However, using more descriptive names can make your code easier to understand, especially for those who are not familiar with the codebase.

< Good Code >

// Loop through an array of students

for (let studentIndex = 0; studentIndex < students.length; studentIndex++) {

    console.log(students[studentIndex].name);

}

<Bad Code>

// Loop through an array of students

for (let i = 0; i < students.length; i++) {

    console.log(students[i].name);

}

In the good example, studentIndex clearly indicates that the loop counter is related to the index of students in the array. This makes the code more readable and understandable. In the bad example, i is less descriptive, making it harder to understand the purpose of the loop at a glance.

<Memo>

Using meaningful names for loop counters is especially important in nested loops, where multiple counters are used. Descriptive names help avoid confusion and potential errors.

58

# Avoid reusing variables for different purposes.

* * *

Reusing variables for different purposes can lead to confusion and bugs. Always use separate variables for different tasks.

* * *

Reusing the same variable for different purposes within the same scope can make the code difficult to read and maintain. It can also introduce hard-to-find bugs. Instead, use distinct variables for different tasks to keep the code clean and understandable.

< Good Code >

let totalScore = 0;

let averageScore = 0;

// Calculate total score

for (let i = 0; i < scores.length; i++) {

    totalScore += scores[i];

}

// Calculate average score

averageScore = totalScore / scores.length;

console.log("Total Score:", totalScore);

console.log("Average Score:", averageScore);

<Bad Code>

let score = 0;

// Calculate total score

for (let i = 0; i < scores.length; i++) {

    score += scores[i];

}

// Calculate average score

score = score / scores.length;

console.log("Total Score:", score); // Incorrectly labeled as total score

console.log("Average Score:", score);

In the good example, totalScore and averageScore are used for their specific purposes, making the code clear and easy to follow. In the bad example, the variable score is reused for both the total and average score calculations, which can lead to confusion and potential errors in understanding the code's intent.

<Memo>

Reusing variables can also lead to unintended side effects, especially in larger codebases where the variable's value might be changed unexpectedly. Always aim for clarity and separation of concerns in your code.

59

# Initialize variables when they are declared.

* * *

Always initialize variables at the time of declaration to avoid undefined values and improve code readability.

* * *

Initializing variables when they are declared helps prevent bugs related to undefined values and makes the code easier to understand.

< Good Code >

// Good example: Variables are initialized at the time of declaration

let count = 0; // count is initialized to 0

let name = 'John'; // name is initialized to 'John'

let isActive = true; // isActive is initialized to true

<Bad Code>

// Bad example: Variables are declared without initialization

let count; // count is undefined

let name; // name is undefined

let isActive; // isActive is undefined

In the good example, each variable is given an initial value, which makes the code more predictable and easier to debug. In the bad example, the variables are declared without initialization, which can lead to unexpected behavior if they are used before being assigned a value.

<Memo>

JavaScript variables that are declared but not initialized are automatically assigned the value undefined.

60

# Use constants for configuration values.

* * *

Use constants to store configuration values that do not change, ensuring they are easily identifiable and maintainable.

* * *

Storing configuration values in constants makes the code more maintainable and reduces the risk of accidental changes to these values.

< Good Code >

// Good example: Configuration values are stored in constants

const MAX_USERS = 100; // Maximum number of users

const API_URL = 'https://api.example.com'; // Base URL for API

const TIMEOUT = 5000; // Timeout duration in milliseconds

<Bad Code>

// Bad example: Configuration values are hard-coded in the code

let users = 100; // Maximum number of users

let url = 'https://api.example.com'; // Base URL for API

let timeout = 5000; // Timeout duration in milliseconds

In the good example, configuration values are stored in constants, making them easy to identify and change if needed. In the bad example, the values are hard-coded, which can make the code harder to maintain and more prone to errors if the values need to be updated.

<Memo>

Using constants for configuration values can also improve performance, as the values are not re-evaluated each time they are used.

61

# Break down functions that do multiple things into smaller ones.

* * *

Simplify functions by breaking them into smaller, single-purpose functions.

* * *

When functions try to accomplish too much, they become hard to read, understand, and maintain. Breaking them into smaller functions improves clarity and reusability.

< Good Code >

// Good example: Functions are broken down into smaller, single-purpose ones.

function getUserData(userId) {

    // Fetch user data

    return fetch(`/api/user/${userId}`)

        .then(response => response.json());

}

function renderUserData(userData) {

    // Render user data to the UI

    const userDiv = document.getElementById('user');

    userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;

}

function loadUser(userId) {

    getUserData(userId)

        .then(userData => {

            renderUserData(userData);

        });

}

<Bad Code>

// Bad example: Single function does too much.

function loadUser(userId) {

    // Fetch user data

    fetch(`/api/user/${userId}`)

        .then(response => response.json())

        .then(userData => {

            // Render user data to the UI

            const userDiv = document.getElementById('user');

            userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;

        });

}

In the good example, getUserData and renderUserData are single-purpose functions. loadUser coordinates these smaller functions, making the code easier to understand and maintain. In the bad example, one function does both data fetching and rendering, making it harder to read and modify.

<Memo>

The Single Responsibility Principle (SRP) is a fundamental concept in software engineering that states that a function or class should have only one reason to change, which is achieved by making functions do just one thing.

62

# Separate concerns by dividing code into modules.

* * *

Organize code by dividing it into modules, each responsible for a specific part of the functionality.

* * *

Separating concerns means dividing your code into distinct sections (modules), each handling a specific aspect of the application. This enhances code maintainability, reusability, and readability.

< Good Code >

// Good example: Code is divided into modules.

// userData.js

export function getUserData(userId) {

    return fetch(`/api/user/${userId}`)

        .then(response => response.json());

}

// render.js

export function renderUserData(userData) {

    const userDiv = document.getElementById('user');

    userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;

}

// main.js

import { getUserData } from './userData.js';

import { renderUserData } from './render.js';

function loadUser(userId) {

    getUserData(userId)

        .then(userData => {

            renderUserData(userData);

        });

}

<Bad Code>

// Bad example: All code in a single file.

function loadUser(userId) {

    // Fetch user data

    fetch(`/api/user/${userId}`)

        .then(response => response.json())

        .then(userData => {

            // Render user data to the UI

            const userDiv = document.getElementById('user');

            userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;

        });

}

In the good example, functionality is split into different modules (userData.js, render.js, and main.js). This makes the codebase more modular and easier to manage. The bad example keeps all functionality in one place, making it harder to maintain and scale.

<Memo>

Modular programming promotes the use of modules to improve the organization and management of code. JavaScript's ES6 introduced modules, which help in encapsulating code and dependencies.

63

# Limit the number of function parameters

* * *

Reduce the number of parameters in your functions to improve readability and maintainability.

* * *

Functions with too many parameters can become difficult to read and maintain. By limiting the number of parameters, you make your code more understandable and easier to work with.

< Good Code >

// Good example: Using an options object to limit parameters

function createUser({ name, age, email }) {

  // Function implementation

  console.log(`Name: ${name}, Age: ${age}, Email: ${email}`);

}

createUser({ name: "John", age: 30, email: "john@example.com" });

<Bad Code>

// Bad example: Too many parameters

function createUser(name, age, email, address, phone, isAdmin) {

  // Function implementation

  console.log(`Name: ${name}, Age: ${age}, Email: ${email}`);

}

createUser("John", 30, "john@example.com", "123 Main St", "555-5555", false);

In the good example, an options object is used to encapsulate the parameters, making the function call cleaner and more flexible. In the bad example, having too many parameters makes the function call confusing and harder to manage.

<Memo>

Using an options object not only improves readability but also makes it easier to add new parameters in the future without changing the function signature.

64

# Use helper functions to encapsulate complex logic

* * *

Encapsulate complex logic within helper functions to improve readability and reusability.

* * *

Complex logic within a function can make it hard to read and understand. Breaking down complex logic into smaller, reusable helper functions enhances clarity and maintainability.

< Good Code >

// Good example: Using helper functions

function calculateTotal(items) {

  return items.reduce((total, item) => total + calculateItemPrice(item), 0);

}

function calculateItemPrice(item) {

  const tax = calculateTax(item.price);

  return item.price + tax;

}

function calculateTax(price) {

  return price * 0.1;

}

const items = [

  { name: "Book", price: 15 },

  { name: "Pen", price: 5 },

];

console.log(calculateTotal(items)); // Output: 22

<Bad Code>

// Bad example: All logic in one function

function calculateTotal(items) {

  return items.reduce((total, item) => {

    const tax = item.price * 0.1;

    const itemPrice = item.price + tax;

    return total + itemPrice;

  }, 0);

}

const items = [

  { name: "Book", price: 15 },

  { name: "Pen", price: 5 },

];

console.log(calculateTotal(items)); // Output: 22

In the good example, the logic is broken down into smaller, reusable functions: calculateItemPrice and calculateTax. This makes the calculateTotal function cleaner and easier to understand. In the bad example, all the logic is crammed into a single function, making it harder to read and maintain.

<Memo>

Using helper functions not only improves code readability but also promotes code reuse and testing, making it easier to debug and extend functionalities.

65

# Write unit tests to ensure functions do one thing correctly.

* * *

Unit tests help verify that individual functions perform their intended task correctly.

* * *

Writing unit tests ensures that each function in your codebase does exactly what it is supposed to do, making the code more reliable and easier to maintain.

< Good Code >

// Function to add two numbers

function add(a, b) {

  return a + b;

}

// Unit test for the add function

function testAdd() {

  console.assert(add(2, 3) === 5, 'Test failed: 2 + 3 should equal 5');

  console.assert(add(-1, 1) === 0, 'Test failed: -1 + 1 should equal 0');

  console.assert(add(0, 0) === 0, 'Test failed: 0 + 0 should equal 0');

}

testAdd();

<Bad Code>

// Function to add two numbers

function add(a, b) {

  return a + b;

}

// No unit tests provided

Good Code: The good example includes a simple add function and a corresponding testAdd function that checks multiple cases to ensure the add function works correctly. This makes it easy to verify the function's correctness and catch any errors early.

Bad Code: The bad example lacks any unit tests, making it difficult to ensure the add function works as expected. Without tests, any changes to the function could introduce bugs that go unnoticed.

<Memo>

Unit tests are a fundamental part of Test-Driven Development (TDD), a software development process where tests are written before the actual code.

66

# Leverage JavaScript modules (ES6 import/export) for better code organization.

* * *

Using JavaScript modules helps in organizing code into reusable and maintainable pieces.

* * *

JavaScript modules allow you to split your code into separate files, each responsible for a specific functionality. This improves code readability and maintainability.

< Good Code >

// math.js - Module file

export function add(a, b) {

  return a + b;

}

export function subtract(a, b) {

  return a - b;

}

// main.js - Main file

import { add, subtract } from './math.js';

console.log(add(2, 3)); // 5

console.log(subtract(5, 2)); // 3

<Bad Code>

// All functions in one file

function add(a, b) {

  return a + b;

}

function subtract(a, b) {

  return a - b;

}

console.log(add(2, 3)); // 5

console.log(subtract(5, 2)); // 3

Good Code: The good example uses ES6 modules to separate the add and subtract functions into a math.js file, which is then imported into the main.js file. This separation of concerns makes the code more modular, easier to read, and maintain.

Bad Code: The bad example places all functions in a single file, which can become unwieldy as the codebase grows. It makes it harder to manage and understand the code, especially in larger projects.

<Memo>

ES6 modules are statically analyzed, meaning that the import/export statements are checked at compile time, which can help catch errors early.

67

# Use async functions for cleaner asynchronous code

* * *

Async functions provide a cleaner syntax for writing asynchronous code, making it easier to read and maintain.

* * *

Instead of using callbacks or Promise chains, async functions allow you to write asynchronous code that looks and behaves similar to synchronous code.

< Good Code >

async function fetchData() {

  try {

    const response = await fetch('https://api.example.com/data');

    const data = await response.json();

    console.log(data);

  } catch (error) {

    console.error('Error fetching data:', error);

  }

}

fetchData();

<Bad Code>

function fetchData() {

  fetch('https://api.example.com/data')

    .then(response => response.json())

    .then(data => console.log(data))

    .catch(error => console.error('Error fetching data:', error));

}

fetchData();

The async keyword before a function makes it an async function. Inside an async function, you can use the await keyword to pause the execution and wait for a Promise to resolve before continuing. This makes the code more readable and easier to reason about, as it avoids deeply nested callbacks or Promise chains. The try...catch block is used to handle any errors that may occur during the asynchronous operation.

<Memo>

Async functions were introduced in ECMAScript 2017 (ES8) and provide syntactic sugar over Promises.

68

# Take advantage of for...of for iterable objects

* * *

The for...of loop provides a concise way to iterate over iterable objects, making your code more readable and expressive.

* * *

The for...of loop is designed to iterate over iterable objects, such as arrays, strings, maps, sets, and other objects that implement the iterable protocol.

< Good Code >

const fruits = ['apple', 'banana', 'orange'];

for (const fruit of fruits) {

  console.log(fruit);

}

<Bad Code>

const fruits = ['apple', 'banana', 'orange'];

for (let i = 0; i < fruits.length; i++) {

  console.log(fruits[i]);

}

The for...of loop is more concise and expressive than the traditional for loop when iterating over arrays or other iterable objects. It automatically retrieves the values from the iterable object, eliminating the need for manual indexing. This makes the code more readable and less prone to off-by-one errors. Additionally, the for...of loop can be used with other iterable objects like strings, maps, and sets.

<Memo>

The for...of loop was introduced in ECMAScript 2015 (ES6) and is part of the new iteration protocols in JavaScript.

69

# Employ Array.prototype.reduce for accumulating array values.

* * *

Use Array.prototype.reduce to accumulate values in an array for better readability and maintainability.

* * *

Array.prototype.reduce is a powerful method that allows you to accumulate values in an array into a single result. It is particularly useful for summing numbers, concatenating strings, or merging objects.

< Good Code >

// Good example: Using reduce to sum array values

const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);

console.log(sum); // Output: 15

<Bad Code>

// Bad example: Using a for loop to sum array values

const numbers = [1, 2, 3, 4, 5];

let sum = 0;

for (let i = 0; i < numbers.length; i++) {

  sum += numbers[i];

}

console.log(sum); // Output: 15

The good example uses reduce, which is more concise and expressive. It clearly shows the intent of accumulating values. The bad example uses a for loop, which is more verbose and less declarative.

<Memo>

Array.prototype.reduce can also be used for more complex operations, such as flattening arrays or creating lookup tables from arrays.

70

# Use Object.assign for merging objects.

* * *

Use Object.assign to merge multiple objects into one for better code clarity and efficiency.

* * *

Object.assign is a method that copies all enumerable own properties from one or more source objects to a target object. It is useful for merging objects and creating a new object with combined properties.

< Good Code >

// Good example: Using Object.assign to merge objects

const obj1 = { a: 1, b: 2 };

const obj2 = { b: 3, c: 4 };

const mergedObj = Object.assign({}, obj1, obj2);

console.log(mergedObj); // Output: { a: 1, b: 3, c: 4 }

<Bad Code>

// Bad example: Manually merging objects

const obj1 = { a: 1, b: 2 };

const obj2 = { b: 3, c: 4 };

const mergedObj = {};

for (let key in obj1) {

  mergedObj[key] = obj1[key];

}

for (let key in obj2) {

  mergedObj[key] = obj2[key];

}

console.log(mergedObj); // Output: { a: 1, b: 3, c: 4 }

The good example uses Object.assign, which is more concise and avoids potential errors in manual merging. The bad example uses for loops, which are more verbose and error-prone.

<Memo>

Object.assign performs a shallow copy, meaning it only copies properties at the first level. For deep cloning, other methods or libraries like lodash are needed.

71

# Break down long conditional expressions into multiple lines.

* * *

Simplify complex conditional expressions by breaking them into multiple lines for better readability.

* * *

Long conditional expressions can be difficult to read and understand. Breaking them into multiple lines makes the code more readable and maintainable.

< Good Code >

// Good example: breaking down a long conditional expression

if (

    user.isActive &&

    user.isVerified &&

    user.hasSubscription &&

    user.subscription.isValid

) {

    // Perform some action

    console.log("User is active, verified, and has a valid subscription.");

}

<Bad Code>

// Bad example: long conditional expression in a single line

if (user.isActive && user.isVerified && user.hasSubscription && user.subscription.isValid) {

    // Perform some action

    console.log("User is active, verified, and has a valid subscription.");

}

In the good example, the conditional expression is broken down into multiple lines, making it easier to read and understand each condition. In the bad example, the entire expression is on a single line, which can be hard to read and debug.

<Memo>

Breaking down long conditional expressions is not only a good practice in JavaScript but also in other programming languages. It helps in maintaining the code and makes it easier for others to understand the logic.

72

# Use temporary variables to hold intermediate results in expressions.

* * *

Store intermediate results in temporary variables to simplify complex expressions and improve readability.

* * *

Complex expressions can be simplified by storing intermediate results in temporary variables. This makes the code easier to read and debug.

< Good Code >

// Good example: using temporary variables for intermediate results

const isUserActive = user.isActive;

const isUserVerified = user.isVerified;

const hasValidSubscription = user.hasSubscription && user.subscription.isValid;

if (isUserActive && isUserVerified && hasValidSubscription) {

    // Perform some action

    console.log("User is active, verified, and has a valid subscription.");

}

<Bad Code>

// Bad example: complex expression without temporary variables

if (user.isActive && user.isVerified && user.hasSubscription && user.subscription.isValid) {

    // Perform some action

    console.log("User is active, verified, and has a valid subscription.");

}

In the good example, intermediate results are stored in temporary variables, making the final conditional expression simpler and more readable. In the bad example, the complex expression is written directly in the conditional statement, which can be harder to read and maintain.

<Memo>

Using temporary variables not only improves readability but also can help in debugging by allowing you to log intermediate results and understand where the logic might be failing.

73

# Refactor complex expressions into helper functions.

* * *

Simplify complex expressions by breaking them into smaller, reusable helper functions.

* * *

Complex expressions can be difficult to read and maintain. Refactoring them into helper functions improves readability and reusability.

< Good Code >

// Helper function to calculate discount

function calculateDiscount(price, discountRate) {

    return price * (discountRate / 100);

}

// Main function using the helper function

function getTotalPrice(price, discountRate) {

    const discount = calculateDiscount(price, discountRate);

    return price - discount;

}

const price = 100;

const discountRate = 10;

console.log(getTotalPrice(price, discountRate)); // Outputs: 90

<Bad Code>

// Complex expression directly in the main function

function getTotalPrice(price, discountRate) {

    return price - (price * (discountRate / 100));

}

const price = 100;

const discountRate = 10;

console.log(getTotalPrice(price, discountRate)); // Outputs: 90

In the good example, the complex discount calculation is refactored into a helper function calculateDiscount, making the main function getTotalPrice easier to read and understand. In the bad example, the complex expression is embedded directly in the main function, making it harder to read and maintain.

<Memo>

Refactoring complex expressions into helper functions not only improves readability but also makes it easier to test individual parts of your code.

74

# Avoid chaining multiple ternary operators.

* * *

Use if-else statements instead of chaining multiple ternary operators for better readability.

* * *

Chaining multiple ternary operators can make code difficult to read and understand. Using if-else statements can improve clarity.

< Good Code >

// Using if-else statements for clarity

function getStatusMessage(status) {

    if (status === 'success') {

        return 'Operation was successful.';

    } else if (status === 'error') {

        return 'There was an error.';

    } else if (status === 'loading') {

        return 'Loading...';

    } else {

        return 'Unknown status.';

    }

}

const status = 'error';

console.log(getStatusMessage(status)); // Outputs: There was an error.

<Bad Code>

// Chaining multiple ternary operators

function getStatusMessage(status) {

    return status === 'success' ? 'Operation was successful.' :

           status === 'error' ? 'There was an error.' :

           status === 'loading' ? 'Loading...' :

           'Unknown status.';

}

const status = 'error';

console.log(getStatusMessage(status)); // Outputs: There was an error.

In the good example, the use of if-else statements makes the logic clear and easy to follow. In the bad example, chaining multiple ternary operators makes the code harder to read and understand, especially for those unfamiliar with the syntax.

<Memo>

Ternary operators are useful for simple conditional assignments, but for more complex logic, if-else statements are generally preferred for better readability.

75

# Use parentheses to make the order of operations explicit.

* * *

Using parentheses in your code helps clarify the order of operations, making it easier for others to understand and maintain.

* * *

When writing complex expressions, the order in which operations are performed can sometimes be unclear. Using parentheses ensures that the intended order is explicit, reducing the likelihood of errors and improving readability.

< Good Code >

// Good: The use of parentheses makes the order of operations clear

let result = (a + b) * (c - d); // Addition and subtraction are done first, then multiplication

<Bad Code>

// Bad: The order of operations is not immediately clear

let result = a + b * c - d; // Multiplication is done first, but it's not obvious at a glance

In the good example, parentheses are used to explicitly define the order in which operations should be performed, making the code easier to read and understand. In the bad example, the lack of parentheses makes it harder to determine the order of operations, which can lead to misunderstandings and potential bugs.

<Memo>

In JavaScript, the order of operations follows standard mathematical rules: multiplication and division are performed before addition and subtraction. However, using parentheses can override this order to ensure clarity.

76

# Encapsulate unrelated functionality into separate functions.

* * *

Encapsulating unrelated functionality into separate functions improves code modularity, readability, and maintainability.

* * *

When different parts of your code perform distinct tasks, it's best to encapsulate these tasks into separate functions. This practice makes your code more modular, easier to read, and simpler to maintain or debug.

< Good Code >

// Good: Separate functions for unrelated tasks

function calculateSum(a, b) {

    return a + b;

}

function printMessage(message) {

    console.log(message);

}

let sum = calculateSum(5, 10);

printMessage(`The sum is ${sum}`);

<Bad Code>

// Bad: Unrelated tasks are combined in a single function

function calculateAndPrint(a, b) {

    let sum = a + b;

    console.log(`The sum is ${sum}`);

}

calculateAndPrint(5, 10);

In the good example, the calculateSum and printMessage functions each perform a single, well-defined task. This separation makes the code easier to understand and maintain. In the bad example, combining calculation and printing in a single function makes the code less modular and harder to reuse or test.

<Memo>

Modular code is a key principle in software engineering. It allows developers to reuse functions across different parts of an application, reducing redundancy and improving maintainability.

77

# Use utility libraries for common tasks

* * *

Leverage utility libraries like Lodash for common operations on arrays, objects, strings, etc.

* * *

Instead of writing custom functions for common tasks, use utility libraries which provide optimized and well-tested implementations.

< Good Code >

js// Using Lodash

const _ = require('lodash');

const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = _.map(numbers, n => n * 2); // [2, 4, 6, 8, 10]

const users = [

  { name: 'Alice', age: 25 },

  { name: 'Bob', age: 30 },

  { name: 'Charlie', age: 35 }

];

const userNames = _.map(users, 'name'); // ['Alice', 'Bob', 'Charlie']

<Bad Code>

js// Custom implementation

const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = [];

for (let i = 0; i < numbers.length; i++) {

  doubledNumbers.push(numbers[i] * 2);

}

const users = [

  { name: 'Alice', age: 25 },

  { name: 'Bob', age: 30 },

  { name: 'Charlie', age: 35 }

];

const userNames = [];

for (let i = 0; i < users.length; i++) {

  userNames.push(users[i].name);

}

Utility libraries like Lodash provide a wide range of functions for common operations, saving development time and reducing code duplication. They are optimized for performance and thoroughly tested, ensuring reliable behavior.

<Memo>

Lodash is a popular utility library for JavaScript, but there are alternatives like Ramda and Underscore.js.

78

# Abstract repetitive code into reusable functions

* * *

Identify repetitive code patterns and extract them into reusable functions for better code organization and maintainability.

* * *

Repetitive code can make the codebase harder to read and maintain. By abstracting such code into reusable functions, you can improve code clarity and reduce duplication.

< Good Code >

jsfunction calculateTotal(items, taxRate) {

  let total = 0;

  for (const item of items) {

    total += item.price;

  }

  return total * (1 + taxRate);

}

const cart1 = [

  { name: 'Item 1', price: 10 },

  { name: 'Item 2', price: 20 }

];

const cart2 = [

  { name: 'Item 3', price: 15 },

  { name: 'Item 4', price: 25 },

  { name: 'Item 5', price: 5 }

];

const total1 = calculateTotal(cart1, 0.08); // 32.4

const total2 = calculateTotal(cart2, 0.1); // 49.5

<Bad Code>

jsconst cart1 = [

  { name: 'Item 1', price: 10 },

  { name: 'Item 2', price: 20 }

];

const cart2 = [

  { name: 'Item 3', price: 15 },

  { name: 'Item 4', price: 25 },

  { name: 'Item 5', price: 5 }

];

let total1 = 0;

for (const item of cart1) {

  total1 += item.price;

}

total1 *= 1.08; // 32.4

let total2 = 0;

for (const item of cart2) {

  total2 += item.price;

}

total2 *= 1.1; // 49.5

By extracting the repetitive code into a function, you can reuse it across multiple places in your codebase. This not only reduces duplication but also makes the code more readable and easier to maintain. If the logic needs to be updated, you only need to change it in one place.

<Memo>

The principle of "Don't Repeat Yourself" (DRY) is a fundamental concept in software engineering that encourages code reuse and abstraction to reduce redundancy.

79

# Separate data fetching logic from UI rendering logic

* * *

Keep data fetching and UI rendering in separate functions or components.

* * *

Separating data fetching from UI rendering helps maintain a clean and manageable codebase. It allows for easier testing, debugging, and reusability of components.

< Good Code >

// Data fetching function

async function fetchData(url) {

  const response = await fetch(url);

  const data = await response.json();

  return data;

}

// UI rendering function

function renderUI(data) {

  const container = document.getElementById('container');

  container.innerHTML = data.map(item => `<p>${item.name}</p>`).join('');

}

// Main function

async function main() {

  const data = await fetchData('https://api.example.com/data');

  renderUI(data);

}

main();

<Bad Code>

async function main() {

  const response = await fetch('https://api.example.com/data');

  const data = await response.json();

  const container = document.getElementById('container');

  container.innerHTML = data.map(item => `<p>${item.name}</p>`).join('');

}

main();

In the good example, the data fetching logic is separated from the UI rendering logic, making the code more modular and easier to maintain. In the bad example, both logics are mixed in a single function, which can lead to difficulties in testing and debugging.

<Memo>

This separation of concerns is a fundamental principle in software engineering, often referred to as the Single Responsibility Principle (SRP).

80

# Use design patterns to solve common problems

* * *

Implement design patterns to address recurring problems in a standardized way.

* * *

Design patterns provide proven solutions to common problems in software design. Using them can improve code readability, reusability, and maintainability.

< Good Code >

// Singleton Pattern

class Singleton {

  constructor() {

    if (!Singleton.instance) {

      Singleton.instance = this;

    }

    return Singleton.instance;

  }

  // Example method

  log() {

    console.log('Singleton instance');

  }

}

const instance1 = new Singleton();

const instance2 = new Singleton();

console.log(instance1 === instance2); // true

<Bad Code>

class Singleton {

  constructor() {

    // No instance check

  }

  // Example method

  log() {

    console.log('Singleton instance');

  }

}

const instance1 = new Singleton();

const instance2 = new Singleton();

console.log(instance1 === instance2); // false

In the good example, the Singleton pattern ensures that only one instance of the class is created, which is useful for managing global state. In the bad example, the Singleton pattern is not correctly implemented, leading to multiple instances and potential issues with state management.

<Memo>

The Singleton pattern is one of the 23 design patterns introduced by the "Gang of Four" in their seminal book "Design Patterns: Elements of Reusable Object-Oriented Software."

81

# Utilize the async keyword for asynchronous functions.

* * *

Using the async keyword makes a function return a promise, enabling asynchronous operations.

* * *

The async keyword is used to define an asynchronous function, which allows you to write asynchronous code in a more readable and maintainable way.

< Good Code >

// Good example using async keyword

async function fetchData() {

  try {

    const response = await fetch('https://api.example.com/data');

    const data = await response.json();

    console.log(data);

  } catch (error) {

    console.error('Error fetching data:', error);

  }

}

fetchData();

<Bad Code>

// Bad example without async keyword

function fetchData() {

  fetch('https://api.example.com/data')

    .then(response => response.json())

    .then(data => {

      console.log(data);

    })

    .catch(error => {

      console.error('Error fetching data:', error);

    });

}

fetchData();

The good example uses the async keyword to define the fetchData function, making it return a promise and allowing the use of await for asynchronous operations. This makes the code more readable and easier to maintain. The bad example uses traditional promise chaining, which can become harder to read and manage, especially with more complex asynchronous operations.

<Memo>

The async keyword was introduced in ECMAScript 2017 (ES8) and has since become a standard way to handle asynchronous operations in JavaScript.

82

# Make use of the await keyword for handling promises.

* * *

The await keyword pauses the execution of an async function until the promise is resolved, making asynchronous code look synchronous.

* * *

The await keyword is used inside an async function to wait for a promise to resolve, simplifying the handling of asynchronous operations.

< Good Code >

// Good example using await keyword

async function getUserData(userId) {

  try {

    const response = await fetch(`https://api.example.com/users/${userId}`);

    const user = await response.json();

    console.log(user);

  } catch (error) {

    console.error('Error fetching user data:', error);

  }

}

getUserData(1);

<Bad Code>

// Bad example without await keyword

function getUserData(userId) {

  fetch(`https://api.example.com/users/${userId}`)

    .then(response => response.json())

    .then(user => {

      console.log(user);

    })

    .catch(error => {

      console.error('Error fetching user data:', error);

    });

}

getUserData(1);

The good example uses the await keyword to wait for the fetch operation and the JSON parsing to complete, making the code more readable and easier to follow. The bad example uses promise chaining, which can lead to nested and harder-to-read code, especially with multiple asynchronous operations.

<Memo>

The await keyword can only be used inside functions marked with the async keyword. It was also introduced in ECMAScript 2017 (ES8) along with the async keyword.

83

# Use JSON.stringify and JSON.parse for deep copying objects

* * *

Utilize JSON.stringify and JSON.parse to create a deep copy of an object, ensuring that nested objects and arrays are also copied.

* * *

When working with objects in JavaScript, it's important to understand the difference between shallow and deep copying. A shallow copy creates a new object with references to the same nested objects and arrays as the original. In contrast, a deep copy creates a new object with entirely new instances of nested objects and arrays.

< Good Code >

// Original object

const original = {

  name: 'John',

  age: 30,

  hobbies: ['reading', 'hiking'],

  address: {

    street: '123 Main St',

    city: 'Anytown'

  }

};

// Deep copy using JSON.stringify and JSON.parse

const deepCopy = JSON.parse(JSON.stringify(original));

// Modify the nested object in the original

original.address.city = 'New City';

console.log('Original:', original);

// Output: Original: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }

console.log('Deep Copy:', deepCopy);

// Output: Deep Copy: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'Anytown' } }

<Bad Code>

// Original object

const original = {

  name: 'John',

  age: 30,

  hobbies: ['reading', 'hiking'],

  address: {

    street: '123 Main St',

    city: 'Anytown'

  }

};

// Shallow copy using spread operator

const shallowCopy = { ...original };

// Modify the nested object in the original

original.address.city = 'New City';

console.log('Original:', original);

// Output: Original: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }

console.log('Shallow Copy:', shallowCopy);

// Output: Shallow Copy: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }

The JSON.stringify method converts a JavaScript object or value to a JSON string, while JSON.parse takes a JSON string and transforms it into a JavaScript object. By combining these two methods, we can create a deep copy of an object.

In the good code example, we first create an original object with nested objects and arrays. We then use JSON.parse(JSON.stringify(original)) to create a deep copy of the original object. When we modify the nested address.city property in the original object, the deep copy remains unaffected, demonstrating that it is a separate instance.

In the bad code example, we attempt to create a copy using the spread operator ({ ...original }). However, this approach only creates a shallow copy, where nested objects and arrays are still referenced from the original object. As a result, when we modify the nested address.city property in the original object, the shallow copy is also affected because it shares the same reference to the nested address object.

It's important to note that the JSON.stringify and JSON.parse approach has limitations. It cannot handle circular references, functions, or certain data types like undefined, Infinity, and NaN. Additionally, it may cause issues with object properties that have special characters or are not valid JSON keys.

<Memo>

The JSON.stringify and JSON.parse approach for deep copying objects is a widely used technique in JavaScript, but it's not the only way to achieve deep copying. Other methods include using libraries like Lodash's _.cloneDeep function or implementing a custom deep copying function that recursively copies nested objects and arrays.

84

# Leverage Array.prototype.some and Array.prototype.every for conditional checks

* * *

Utilize the Array.prototype.some and Array.prototype.every methods to perform efficient conditional checks on arrays, reducing the need for complex loops and conditional statements.

* * *

In JavaScript, you often need to perform conditional checks on arrays, such as checking if at least one element in an array satisfies a certain condition or if all elements satisfy a condition. The Array.prototype.some and Array.prototype.every methods provide a concise and readable way to perform these checks without the need for complex loops and conditional statements.

< Good Code >

const numbers = [1, 2, 3, 4, 5];

// Check if at least one number is greater than 3

const hasGreaterThanThree = numbers.some(num => num > 3);

console.log(hasGreaterThanThree); // Output: true

// Check if all numbers are positive

const allPositive = numbers.every(num => num > 0);

console.log(allPositive); // Output: true

const users = [

  { name: 'John', age: 25, active: true },

  { name: 'Jane', age: 30, active: false },

  { name: 'Bob', age: 35, active: true }

];

// Check if at least one user is active

const hasActiveUser = users.some(user => user.active);

console.log(hasActiveUser); // Output: true

// Check if all users are over 18

const allOverEighteen = users.every(user => user.age > 18);

console.log(allOverEighteen); // Output: true

<Bad Code>

const numbers = [1, 2, 3, 4, 5];

// Check if at least one number is greater than 3

let hasGreaterThanThree = false;

for (let i = 0; i < numbers.length; i++) {

  if (numbers[i] > 3) {

    hasGreaterThanThree = true;

    break;

  }

}

console.log(hasGreaterThanThree); // Output: true

// Check if all numbers are positive

let allPositive = true;

for (let i = 0; i < numbers.length; i++) {

  if (numbers[i] <= 0) {

    allPositive = false;

    break;

  }

}

console.log(allPositive); // Output: true

The Array.prototype.some method tests whether at least one element in the array passes the test implemented by the provided function. It executes the provided function once for each element of the array until it finds one where the function returns a truthy value (a value that is considered true when encountered in a boolean context), at which point it returns true and stops iterating over the remaining elements. If no elements pass the test, it returns false.

The Array.prototype.every method tests whether all elements in the array pass the test implemented by the provided function. It executes the provided function once for each element of the array until it finds one where the function returns a falsy value (a value that is considered false when encountered in a boolean context), at which point it returns false and stops iterating over the remaining elements. If all elements pass the test, it returns true.

In the good code example, we demonstrate the use of some and every to perform conditional checks on arrays of numbers and objects. The code is concise, readable, and avoids the need for complex loops and conditional statements.

In the bad code example, we achieve the same functionality using traditional for loops and conditional statements. While this approach works, it is more verbose, harder to read, and more prone to errors, especially as the conditions become more complex.

Using some and every not only makes the code more readable but also provides better performance in certain cases, as these methods can short-circuit and stop iterating over the remaining elements once the condition is met or violated.

<Memo>

The Array.prototype.some and Array.prototype.every methods are part of the ECMAScript 5 (ES5) specification, which was released in 2009. They are widely supported in modern browsers and can be used in older environments with the help of polyfills or transpilers like Babel.

85

# Utilize Array.prototype.find for locating elements in arrays.

* * *

Use Array.prototype.find to locate elements in arrays efficiently.

* * *

The find method in JavaScript arrays helps you locate the first element that satisfies a given condition, making your code cleaner and more readable.

< Good Code >

// Good example: Using Array.prototype.find to locate an element

const users = [

  { id: 1, name: 'Alice' },

  { id: 2, name: 'Bob' },

  { id: 3, name: 'Charlie' }

];

const user = users.find(user => user.id === 2);

console.log(user); // { id: 2, name: 'Bob' }

<Bad Code>

// Bad example: Using a for loop to locate an element

const users = [

  { id: 1, name: 'Alice' },

  { id: 2, name: 'Bob' },

  { id: 3, name: 'Charlie' }

];

let user;

for (let i = 0; i < users.length; i++) {

  if (users[i].id === 2) {

    user = users[i];

    break;

  }

}

console.log(user); // { id: 2, name: 'Bob' }

The good example uses Array.prototype.find, which is more concise and easier to read compared to the for loop in the bad example. The find method abstracts the iteration logic, making the code cleaner and reducing the potential for errors.

<Memo>

The find method returns undefined if no elements satisfy the condition, so it's important to handle this case in your code.

86

# Choose arrays for ordered collections of data.

* * *

Use arrays when you need to maintain an ordered collection of data.

* * *

Arrays in JavaScript are ideal for storing ordered collections of data, allowing you to access elements by their index and perform various operations like sorting and filtering.

< Good Code >

// Good example: Using an array to store ordered data

const fruits = ['Apple', 'Banana', 'Cherry'];

console.log(fruits[0]); // 'Apple'

console.log(fruits[1]); // 'Banana'

console.log(fruits[2]); // 'Cherry'

<Bad Code>

// Bad example: Using an object to store ordered data

const fruits = {

  0: 'Apple',

  1: 'Banana',

  2: 'Cherry'

};

console.log(fruits[0]); // 'Apple'

console.log(fruits[1]); // 'Banana'

console.log(fruits[2]); // 'Cherry'

The good example uses an array, which is the appropriate data structure for ordered collections. Arrays provide built-in methods for iteration, sorting, and other operations. The bad example uses an object, which is not intended for ordered collections and lacks these convenient methods.

<Memo>

Arrays in JavaScript are zero-indexed, meaning the first element is accessed with index 0\. This is a common feature in many programming languages.

87

# Use objects for key-value pairs.

* * *

Objects are ideal for storing key-value pairs where the keys are strings.

* * *

Using objects to store key-value pairs is a common practice in JavaScript. It allows for easy access and manipulation of data.

< Good Code >

// Good example: Using an object for key-value pairs

const user = {

  name: 'John Doe',

  age: 30,

  email: 'john.doe@example.com'

};

// Accessing values

console.log(user.name); // Output: John Doe

console.log(user.age);  // Output: 30

<Bad Code>

// Bad example: Using separate variables for each key-value pair

const userName = 'John Doe';

const userAge = 30;

const userEmail = 'john.doe@example.com';

// Accessing values

console.log(userName); // Output: John Doe

console.log(userAge);  // Output: 30

Using objects for key-value pairs makes the code more organized and easier to read. It groups related data together, making it easier to manage and access. In contrast, using separate variables for each piece of data can lead to a cluttered and less maintainable codebase.

<Memo>

Objects in JavaScript are unordered collections of key-value pairs, where the keys are strings or symbols, and the values can be of any type.

88

# Opt for Map when you need ordered key-value pairs.

* * *

Maps maintain the order of key-value pairs and allow for any type of key.

* * *

When the order of key-value pairs matters or when you need non-string keys, using a Map is more appropriate than an object.

< Good Code >

// Good example: Using a Map for ordered key-value pairs

const userMap = new Map();

userMap.set('name', 'John Doe');

userMap.set('age', 30);

userMap.set('email', 'john.doe@example.com');

// Accessing values

console.log(userMap.get('name')); // Output: John Doe

console.log(userMap.get('age'));  // Output: 30

<Bad Code>

// Bad example: Using an object when order matters

const user = {

  name: 'John Doe',

  age: 30,

  email: 'john.doe@example.com'

};

// Accessing values (order is not guaranteed)

console.log(user.name); // Output: John Doe

console.log(user.age);  // Output: 30

Maps maintain the insertion order of key-value pairs, which can be crucial in certain applications. They also allow for keys of any type, not just strings. This makes Maps more versatile than objects when dealing with ordered data or non-string keys.

<Memo>

Maps are part of the ES6 (ECMAScript 2015) specification and provide better performance for frequent additions and removals of key-value pairs compared to objects.

89

# Utilize Set for unique values without duplicates.

* * *

Use the Set object to store unique values, ensuring no duplicates.

* * *

The Set object in JavaScript allows you to store unique values of any type, whether primitive values or object references. This is particularly useful when you need to ensure that a collection of items does not contain any duplicates.

< Good Code >

// Using Set to store unique values

const numbers = [1, 2, 2, 3, 4, 4, 5];

const uniqueNumbers = new Set(numbers);

console.log(uniqueNumbers); // Output: Set { 1, 2, 3, 4, 5 }

<Bad Code>

// Using an array to store unique values (inefficient)

const numbers = [1, 2, 2, 3, 4, 4, 5];

const uniqueNumbers = [];

numbers.forEach((num) => {

  if (!uniqueNumbers.includes(num)) {

    uniqueNumbers.push(num);

  }

});

console.log(uniqueNumbers); // Output: [1, 2, 3, 4, 5]

The good example uses a Set to automatically handle duplicates, making the code more concise and efficient. The bad example manually checks for duplicates using an array, which is less efficient and more verbose.

<Memo>

The Set object was introduced in ECMAScript 2015 (ES6) and provides a more efficient way to handle collections of unique values compared to traditional arrays.

90

# Prefer WeakMap and WeakSet for managing memory efficiently.

* * *

Use WeakMap and WeakSet to manage memory efficiently by allowing garbage collection of unused objects.

* * *

WeakMap and WeakSet are similar to Map and Set, but they allow for efficient memory management by holding "weak" references to objects. This means that if there are no other references to an object stored in a WeakMap or WeakSet, it can be garbage collected.

< Good Code >

// Using WeakMap to manage memory efficiently

let obj = { name: 'John' };

const weakMap = new WeakMap();

weakMap.set(obj, 'some value');

// Later, if obj is no longer needed

obj = null; // obj can be garbage collected

// weakMap no longer holds a strong reference to obj

<Bad Code>

// Using Map which holds strong references

let obj = { name: 'John' };

const map = new Map();

map.set(obj, 'some value');

// Later, if obj is no longer needed

obj = null; // obj cannot be garbage collected because map holds a strong reference

// map still holds a strong reference to obj

The good example uses WeakMap, which allows the object to be garbage collected when it is no longer needed, thus managing memory more efficiently. The bad example uses Map, which holds a strong reference to the object, preventing it from being garbage collected.

<Memo>

WeakMap and WeakSet were introduced in ECMAScript 2015 (ES6) and are particularly useful for cases where you want to associate data with objects without preventing their garbage collection.

91

# Use try/catch blocks to handle exceptions.

* * *

Using try/catch blocks helps manage errors gracefully and ensures the program can handle unexpected situations without crashing.

* * *

Implementing try/catch blocks in your JavaScript code allows you to catch and handle exceptions, providing a way to manage errors and maintain the flow of the program.

< Good Code >

try {

  // Attempt to parse JSON

  let data = JSON.parse(jsonString);

  console.log(data);

} catch (error) {

  // Handle the error

  console.error("Failed to parse JSON:", error.message);

}

<Bad Code>

// Attempt to parse JSON without error handling

let data = JSON.parse(jsonString);

console.log(data);

In the good example, the try/catch block is used to handle any errors that might occur during the JSON parsing process. If an error occurs, it is caught and logged, preventing the program from crashing. In the bad example, there is no error handling, so if the JSON parsing fails, the program will throw an uncaught exception and potentially crash.

<Memo>

JavaScript introduced try/catch blocks in ECMAScript 3, making it easier for developers to handle runtime errors and improve the robustness of their code.

92

# Provide meaningful error messages.

* * *

Meaningful error messages help developers understand what went wrong and how to fix it, improving code maintainability and debugging efficiency.

* * *

When handling errors, providing clear and informative error messages can significantly aid in diagnosing and resolving issues quickly.

< Good Code >

try {

  // Attempt to access a property of an undefined object

  let value = obj.property;

} catch (error) {

  // Provide a meaningful error message

  console.error("Error accessing property: The object 'obj' is undefined.");

}

<Bad Code>

try {

  // Attempt to access a property of an undefined object

  let value = obj.property;

} catch (error) {

  // Provide a generic error message

  console.error("An error occurred.");

}

In the good example, the error message clearly states what went wrong and provides context about the undefined object. This helps developers quickly identify and fix the issue. In the bad example, the generic error message does not provide any useful information, making it harder to diagnose the problem.

<Memo>

Providing meaningful error messages is a best practice in software development and is crucial for effective debugging and maintenance. It is especially important in large codebases and collaborative projects.

93

# Log errors to the console or a logging service.

* * *

Always log errors to the console or a logging service to aid in debugging and monitoring.

* * *

Logging errors helps developers understand what went wrong and where. It is crucial for debugging and maintaining code quality.

< Good Code >

try {

  // Code that may throw an error

  let result = riskyOperation();

} catch (error) {

  console.error('An error occurred:', error); // Logs error to the console

  // Optionally, send the error to a logging service

  sendErrorToLoggingService(error);

}

<Bad Code>

try {

  // Code that may throw an error

  let result = riskyOperation();

} catch (error) {

  // Do nothing with the error

}

In the good example, the error is logged to the console and optionally sent to a logging service, making it easier to diagnose issues. In the bad example, the error is caught but not logged, making it difficult to understand what went wrong.

<Memo>

Logging services like Sentry, Loggly, and Datadog can provide more advanced error tracking and alerting capabilities compared to simple console logging.

94

# Gracefully handle rejected promises with .catch.

* * *

Always handle rejected promises using the .catch method to prevent unhandled promise rejections.

* * *

Handling rejected promises ensures that errors are managed properly, preventing unexpected crashes and improving code reliability.

< Good Code >

fetch('https://api.example.com/data')

  .then(response => response.json())

  .then(data => {

    console.log('Data received:', data);

  })

  .catch(error => {

    console.error('Failed to fetch data:', error); // Handles the rejected promise

  });

<Bad Code>

fetch('https://api.example.com/data')

  .then(response => response.json())

  .then(data => {

    console.log('Data received:', data);

  });

// No .catch to handle potential errors

In the good example, the .catch method is used to handle any errors that occur during the fetch operation, ensuring that the error is logged and can be addressed. In the bad example, there is no .catch method, so any errors will result in unhandled promise rejections, which can lead to application crashes.

<Memo>

Unhandled promise rejections can be caught globally in Node.js using the process.on('unhandledRejection', handler) event, but it is better practice to handle them locally with .catch.

95

# Validate function inputs to prevent errors.

* * *

Ensure that function inputs are validated to avoid unexpected errors and improve code reliability.

* * *

Validating inputs in functions helps catch errors early and ensures that the function behaves as expected. This practice is crucial for maintaining robust and error-free code.

< Good Code >

// Function to add two numbers with input validation

function add(a, b) {

  if (typeof a !== 'number' || typeof b !== 'number') {

    throw new Error('Both arguments must be numbers');

  }

  return a + b;

}

try {

  console.log(add(2, 3)); // 5

  console.log(add(2, '3')); // Error: Both arguments must be numbers

} catch (e) {

  console.error(e.message);

}

<Bad Code>

// Function to add two numbers without input validation

function add(a, b) {

  return a + b;

}

console.log(add(2, 3)); // 5

console.log(add(2, '3')); // '23' (unexpected result)

In the good example, the function checks if the inputs are numbers and throws an error if they are not. This prevents unexpected behavior and makes the code more robust. In the bad example, the function does not validate inputs, leading to potential errors and unexpected results.

<Memo>

Input validation is a common practice in many programming languages and is essential for writing secure and reliable code. It helps prevent bugs and security vulnerabilities by ensuring that inputs meet the expected criteria.

96

# Write modular code that can be reused in different projects.

* * *

Create modular code by breaking down functionality into small, reusable functions or modules.

* * *

Modular code is easier to maintain, test, and reuse across different projects. By encapsulating functionality into small, independent units, you can improve code organization and reduce duplication.

< Good Code >

// Utility module for mathematical operations

const MathUtils = {

  add: function(a, b) {

    return a + b;

  },

  subtract: function(a, b) {

    return a - b;

  }

};

// Using the utility module in different parts of the project

console.log(MathUtils.add(5, 3)); // 8

console.log(MathUtils.subtract(5, 3)); // 2

<Bad Code>

// Non-modular code with repeated logic

function add(a, b) {

  return a + b;

}

function subtract(a, b) {

  return a - b;

}

// Repeating the same logic in different parts of the project

console.log(add(5, 3)); // 8

console.log(subtract(5, 3)); // 2

console.log(add(10, 7)); // 17

console.log(subtract(10, 7)); // 3

In the good example, mathematical operations are encapsulated in a utility module, making the code reusable and easier to manage. In the bad example, the same logic is repeated in different parts of the project, leading to code duplication and making maintenance more difficult.

<Memo>

Modular programming is a software design technique that emphasizes separating functionality into independent, interchangeable modules. This approach is widely used in modern software development to enhance code maintainability and scalability.

97

# Use higher-order functions to create reusable function patterns.

* * *

Higher-order functions are functions that take other functions as arguments or return them as results, enabling reusable and modular code.

* * *

Higher-order functions can simplify code by abstracting common patterns, making it more readable and maintainable.

< Good Code >

// Higher-order function that takes a function and a value, and applies the function to the value

function applyFunction(fn, value) {

  return fn(value);

}

// Example functions to be used with the higher-order function

function double(x) {

  return x * 2;

}

function square(x) {

  return x * x;

}

// Using the higher-order function

console.log(applyFunction(double, 5)); // 10

console.log(applyFunction(square, 5)); // 25

<Bad Code>

// Repeating similar code without using higher-order functions

function double(x) {

  return x * 2;

}

function square(x) {

  return x * x;

}

function applyDouble(value) {

  return double(value);

}

function applySquare(value) {

  return square(value);

}

console.log(applyDouble(5)); // 10

console.log(applySquare(5)); // 25

The good example uses a higher-order function applyFunction to apply different functions (double and square) to a value, making the code more reusable and concise. The bad example repeats similar code for each function application, making it less maintainable.

<Memo>

JavaScript's built-in array methods like map, filter, and reduce are examples of higher-order functions.

98

# Employ mixins for reusing code in multiple classes.

* * *

Mixins are a way to include reusable code in multiple classes without using inheritance.

* * *

Mixins allow you to share functionality between classes by copying methods from one object to another, promoting code reuse and reducing duplication.

< Good Code >

// Mixin for reusable methods

const canEat = {

  eat: function() {

    console.log('Eating...');

  }

};

const canWalk = {

  walk: function() {

    console.log('Walking...');

  }

};

// Class that uses mixins

class Person {

  constructor(name) {

    this.name = name;

  }

}

// Copy methods from mixins to the class prototype

Object.assign(Person.prototype, canEat, canWalk);

const person = new Person('John');

person.eat(); // Eating...

person.walk(); // Walking...

<Bad Code>

// Repeating similar methods in multiple classes without using mixins

class Person {

  constructor(name) {

    this.name = name;

  }

  eat() {

    console.log('Eating...');

  }

  walk() {

    console.log('Walking...');

  }

}

class Animal {

  constructor(type) {

    this.type = type;

  }

  eat() {

    console.log('Eating...');

  }

  walk() {

    console.log('Walking...');

  }

}

const person = new Person('John');

person.eat(); // Eating...

person.walk(); // Walking...

const animal = new Animal('Dog');

animal.eat(); // Eating...

animal.walk(); // Walking...

The good example uses mixins (canEat and canWalk) to add reusable methods to the Person class, reducing code duplication. The bad example repeats the same methods in multiple classes (Person and Animal), making the code harder to maintain.

<Memo>

Mixins can be particularly useful in languages that do not support multiple inheritance, like JavaScript.

99

# Use inheritance for extending existing classes

* * *

Inheritance allows creating new classes based on existing ones, reusing code and promoting modularity.

* * *

When creating a new class that shares properties or methods with an existing class, consider extending the existing class instead of duplicating code.

< Good Code >

class Animal {

  constructor(name) {

    this.name = name;

  }

  speak() {

    console.log(`${this.name} makes a sound.`);

  }

}

class Dog extends Animal {

  constructor(name) {

    super(name); // Call the parent constructor

  }

  speak() {

    console.log(`${this.name} barks.`); // Override the parent method

  }

}

const animal = new Animal('Generic Animal');

const dog = new Dog('Buddy');

animal.speak(); // Output: Generic Animal makes a sound.

dog.speak(); // Output: Buddy barks.

<Bad Code>

class Animal {

  constructor(name) {

    this.name = name;

  }

  speak() {

    console.log(`${this.name} makes a sound.`);

  }

}

class Dog {

  constructor(name) {

    this.name = name;

  }

  speak() {

    console.log(`${this.name} barks.`);

  }

}

const animal = new Animal('Generic Animal');

const dog = new Dog('Buddy');

animal.speak(); // Output: Generic Animal makes a sound.

dog.speak(); // Output: Buddy barks.

In the good code example, the Dog class extends the Animal class, inheriting its properties and methods. The super() method is used to call the parent constructor and initialize the name property. The speak() method is overridden in the Dog class to provide a specific implementation for dogs.

In the bad code example, the Dog class is defined separately, duplicating the name property and the speak() method. This violates the DRY (Don't Repeat Yourself) principle and makes it harder to maintain and extend the codebase.

Inheritance promotes code reuse, modularity, and extensibility, making it easier to create new classes based on existing ones while avoiding duplication.

<Memo>

Inheritance is one of the core principles of Object-Oriented Programming (OOP), along with encapsulation and polymorphism.

100

# Leverage function composition for creating complex functionality from simple functions

* * *

Function composition allows combining multiple simple functions to create more complex functionality, promoting code reusability and modularity.

* * *

When dealing with complex operations, consider breaking them down into smaller, reusable functions and composing them together to achieve the desired functionality.

< Good Code >

const addTax = (amount) => amount * 1.08;

const formatCurrency = (amount) => `$${amount.toFixed(2)}`;

const calculateTotal = (items) =>

  items

    .map((item) => item.price)

    .reduce((total, price) => total + price, 0)

    .then(addTax)

    .then(formatCurrency);

const items = [

  { name: 'Item 1', price: 10 },

  { name: 'Item 2', price: 20 },

  { name: 'Item 3', price: 30 },

];

const total = calculateTotal(items);

console.log(total); // Output: $64.80

<Bad Code>

const calculateTotal = (items) => {

  let total = 0;

  for (const item of items) {

    total += item.price;

  }

  total *= 1.08;

  return `$${total.toFixed(2)}`;

};

const items = [

  { name: 'Item 1', price: 10 },

  { name: 'Item 2', price: 20 },

  { name: 'Item 3', price: 30 },

];

const total = calculateTotal(items);

console.log(total); // Output: $64.80

In the good code example, the calculateTotal function is composed of three smaller functions: map to extract the prices from the items, reduce to sum the prices, addTax to apply the tax rate, and formatCurrency to format the total as a currency string. Each function has a single responsibility, making the code more readable, testable, and maintainable.

In the bad code example, the calculateTotal function contains all the logic in a single function, making it harder to read, test, and reuse parts of the functionality.

Function composition promotes code reusability, modularity, and testability, making it easier to create complex functionality by combining smaller, focused functions.

<Memo>

Function composition is a fundamental concept in functional programming, where functions are treated as first-class citizens and can be passed as arguments to other functions or returned from functions.

101

# Use default parameters to handle missing arguments

* * *

Provide default values for function parameters to handle cases where arguments are missing or undefined.

* * *

When calling a function without providing all required arguments, JavaScript will assign undefined to the missing parameters. This can lead to errors or unexpected behavior. Default parameters allow you to specify a fallback value for missing arguments.

< Good Code >

function greet(name = 'Guest') {

  console.log(`Hello, ${name}!`);

}

greet('John'); // Output: Hello, John!

greet(); // Output: Hello, Guest!

<Bad Code>

function greet(name) {

  const nameToUse = name || 'Guest';

  console.log(`Hello, ${nameToUse}!`);

}

greet('John'); // Output: Hello, John!

greet(); // Output: Hello, Guest!

greet(undefined); // Output: Hello, Guest!

In the good code example, the name parameter has a default value of 'Guest'. If no argument is provided when calling greet(), the default value is used. This approach is more concise and easier to read than the bad code example, which uses a logical OR operator to handle the missing argument case.

<Memo>

Default parameters were introduced in ECMAScript 2015 (ES6).

102

# Avoid side effects to make functions reusable

* * *

Write pure functions that don't modify external state or data to ensure they are reusable and predictable.

* * *

A pure function is a function that, given the same inputs, will always return the same output and has no side effects. Side effects are changes to external state or data outside the function's scope. Avoiding side effects makes functions easier to reason about, test, and reuse in different contexts.

< Good Code >

const addNumbers = (a, b) => a + b;

const result = addNumbers(2, 3); // result is 5

<Bad Code>

let counter = 0;

const incrementCounter = () => {

  counter++;

  return counter;

}

const result = incrementCounter(); // result is 1

const anotherResult = incrementCounter(); // anotherResult is 2

In the good code example, addNumbers is a pure function that takes two numbers as input and returns their sum without modifying any external state. In the bad code example, incrementCounter modifies the external counter variable, making it impure and harder to reason about and test in isolation.

<Memo>

Pure functions are a core concept in functional programming and are often used in reactive programming and state management libraries like React and Redux.

Afterword

◆

Thank you for taking the time to read through this collection of 100 techniques aimed at enhancing the readability of your JavaScript code.

Throughout this book, we have explored various methods to write cleaner and more understandable code by leveraging JavaScript's unique features and syntax.

Our goal has been to equip you with practical strategies that make your code not only functional but also easy for others to read and maintain.

Each technique presented includes both good and bad examples, providing clear contrasts to help you grasp the principles of writing readable code.

We hope these examples have been instructive and have given you a solid foundation to improve your coding practices.

We trust that the insights and tips shared in this book will serve you well in your programming journey, making your code more accessible and enjoyable for everyone who encounters it.

Happy coding!