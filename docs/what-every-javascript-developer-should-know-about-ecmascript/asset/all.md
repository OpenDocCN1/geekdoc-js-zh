![](cover.jpeg)

What Every JavaScript Developer Should Know About ECMAScript 2015

By K. Scott Allen

[http://OdeToCode.com](http://OdeToCode.com)

![otc300](images/00001.jpeg)

First Edition

©2015 OdeToCode LLC

[Welcome](#part0000_split_002.html__Toc435998149)

[Variables and Parameters](#part0000_split_003.html__Toc435998150)

[let](#part0000_split_004.html__Toc435998151)

[const](#part0000_split_005.html__Toc435998152)

[Default Parameters](#part0000_split_006.html__Toc435998153)

[Rest Parameters](#part0000_split_007.html__Toc435998154)

[Spread Operator](#part0000_split_008.html__Toc435998155)

[Destructuring](#part0000_split_009.html__Toc435998156)

[Template Literals](#part0000_split_010.html__Toc435998157)

[Tagged Template Literals](#part0000_split_011.html__Toc435998158)

[Classes](#part0000_split_013.html__Toc435998159)

[The Class Keyword](#part0000_split_014.html__Toc435998160)

[Class Constructor and Properties](#part0000_split_015.html__Toc435998161)

[Classes behind the Scenes](#part0000_split_016.html__Toc435998162)

[Statics](#part0000_split_017.html__Toc435998163)

[Inheritance](#part0000_split_018.html__Toc435998164)

[Using Super](#part0000_split_019.html__Toc435998165)

[Super Constructors](#part0000_split_020.html__Toc435998166)

[The Caveat](#part0000_split_021.html__Toc435998167)

[Functional Features](#part0000_split_022.html__Toc435998168)

[Arrow Functions](#part0000_split_023.html__Toc435998169)

[Iterators](#part0000_split_024.html__Toc435998170)

[Looping with for of](#part0000_split_025.html__Toc435998171)

[Symbols](#part0000_split_026.html__Toc435998172)

[Creating Iterables](#part0000_split_027.html__Toc435998173)

[Generators](#part0000_split_028.html__Toc435998174)

[Lazy Evaluation](#part0000_split_029.html__Toc435998175)

[Iterators Revisited](#part0000_split_030.html__Toc435998176)

[Delegating Yield](#part0000_split_031.html__Toc435998177)

[Asynchronous JavaScript](#part0000_split_032.html__Toc435998178)

[Promise Objects](#part0000_split_033.html__Toc435998179)

[Promise Chaining](#part0000_split_034.html__Toc435998180)

[The Promise API](#part0000_split_035.html__Toc435998181)

[Promise Errors](#part0000_split_036.html__Toc435998182)

[Modules](#part0000_split_037.html__Toc435998183)

[Why Modules?](#part0000_split_038.html__Toc435998184)

[Module Syntax](#part0000_split_039.html__Toc435998185)

[APIs](#part0000_split_040.html__Toc435998186)

[New Collections](#part0000_split_041.html__Toc435998187)

[Arrays](#part0000_split_042.html__Toc435998188)

[Strings](#part0000_split_043.html__Toc435998189)

[Objects](#part0000_split_044.html__Toc435998190)

[The End](#part0000_split_045.html__Toc435998191)

# Welcome

I sat down and wrote the book I would like to read about the new JavaScript features in 2015\. This book is not an exhaustive list of everything new in the ECMAScript 2015 specification that governs the JavaScript language. Instead, I purposefully selected what I think are the important features we will use in everyday programming. I expect the reader will already have a good understanding of the JavaScript language as the language existed before 2015.

The majority of code samples in this book are unit tests I authored with the Jasmine testing framework. I find one of the best ways to explore a new language or framework is to write tests and verify my assumptions about how the code should work.

Special thanks to Ruben Bartelink and Porter T. Bear for feedback.

I hope you enjoy what follows.

# Variables and Parameters

ECMAScript 2015 introduces a number of new keywords and syntactic sugar for working with local variables and function parameters. All of these new features make JavaScript more expressive and easier to use, and a few features even make JavaScript code safer.

## let

Variable scope in JavaScript has been a source of surprises and bugs over the years. The surprise is because JavaScript only offers function scope and global scope to control the lifetime of a variable. There is no block scope[[1]](#part0000_split_045.html__ftn1).

var doWork = function(flag){

    if(flag) {

        var x = 3;

    }

    return x; // x is still available

};

var result = doWork(true);

expect(result).toBe(3); // PASS!!!!!

The newlet keyword of 2015will replacevar for variable declarations and provide true block scoping.

let doWork = function(flag) {

    if(flag){

 let x = 3;

    }

    return x; // Will give a ReferenceError: x is not defined

};

let result = doWork(true);

expect(result).toBe(3); 

Iteration statements also benefit fromlet.

var doWork = function(){

    for(let x = 0; x < 3; x++) {

        // ...

    }

    return x; // ReferenceError: x is not defined

};

### Using let

ES2015 still supports thevar keyword, but we should think ofvar as an obsolete keyword when writing newcode.letis the newvar!

Willlet make JavaScript code better?

I doubt iflet will prevent a significant number of bugs, but I do think JavaScript code will improve.

We can declare variables close to where we use the variables instead of declaring all local variables at the top of a function, which is a defensive practice followed today to avoidvar related bugs.

We also don’t need to introduce a second nested function or immediately invoked function expression (IIFE) only to control the scope of a variable (another defensive practice you’ll see in JS libraries).

The result is that programsusinglet should be easier to read, and perhaps just a tiny bit safer, too.

## const

Theconstkeyword will give you a read-only variable. Likelet, a variable declared withconst will have block scope, and you cannot re-declare aconst.

const MAX_BUNNIES = 3;

There is no requirement for a constant variable to use capital letters, that’s just a convention I like to follow.

### Using const

In a perfect world, all the JavaScript environmentswould have a perfect implementation ofconst. Unfortunately,const is one of those keywords that has been around in some runtimes even before the keyword appeared in an official ECMAScript specification.

While most runtimes can agree that aconst should be constant, existing implementations disagree on how to behave when code attempts to assign a new value to a constant. Should the assignment cause a runtime error? Should the assignment fail silently?

The official specification saysconst should fail with a runtime error if a program tries to assign a new value to a constant, and constant declarations without an initializer should be a syntax error.

const MAX_SIZE = 10;

// MAX_SIZE = 12; // If executed, will result in a SyntaxError

I hope it will not take long for all the latest runtimes and browsers to straighten up and behave correctly. The current situation should notstop you from usingconst whenever possible because the keyword does have a few benefits.

1.  const tells other programmers about the intended behavior of a variable, and this makes a script easier to maintain.
2.  const tells the runtime about the intended behavior of a variable, which can allow for optimizations across time and space.

## Default Parameters

If a JavaScript function takes two parameters, we have always had the ability to invoke the function and pass two parameters, or one parameter, or no parameters, or three parameters if we wanted. In cases where we do not pass enough parameters, the author of a function might want to specify a default value instead of working withundefined.

Before 2015, developers applied default values to incoming parameters using|| expressions inside the function. In the following function, if the caller does notpass a value for thename parameter, the code will assign a default of Scott.

let doWork = function(name) {

    name = name || "Scott";

    return name;

};

In 2015, default values are explicit and appear in the parameter list for a function.

let doWork = function(name = "Scott") {

    return name;

};

expect(doWork()).toBe("Scott");

A function can even calculate a default using something more than just a literal expression.

let doWork = function(x = Math.random()) { return x; }

The default parameter syntax is a good example of how ES2015 provides a clean syntax for a common requirement. No longer will we have to scan through a function’s source code or documentation to discover the defaults.

Of course, not all parameters are simple values. A common programming technique for operations involving complex configurations, like an HTTP call, is to accept a single object argument with properties to set the URI, HTTP method, timeout settings, and more. Default parameters are useful in this scenario, too, but we’ll have to wait for later and learn about object destructuring first.

## Rest Parameters

A rest parameter allows a function to work with a variable number of arguments. A function’s rest parameter always appears at the end of the argument list and uses a triple dot prefix (…), as shown below.

let doWork = function(name, ...numbers){

    let result = 0;

    numbers.forEach(function(n){

        result += n;

    });

    return result;

};

A caller invokingdoWork can pass zero or more parameters at the rest parameter position. You can say thenumbers argument will take “the rest” of the parameters a caller passestodoWork, and numbers will hold the parameters in an array. In the following example,numbers will reference an array with the values 1, 2, 3.

let result = doWork("Scott", 1, 2, 3);

expect(result).toBe(6);

In the case where a caller passes no parameters in the rest parameter position, the rest parameter will be an empty array.

let doWork = function(...numbers){

     return numbers;

};

let result = doWork();

expect(result.length).toBe(0);

Before 2015, we could allow callers to pass a variable number of arguments to a function by using the implicit arguments variable inside of the function. The arguments variable contains all the parameters to a function in an array-like object, but arguments isnot an array, which creates confusion. It is also difficult to spot if a function is usingarguments without reading through the code or documentation for the function.

Rest parameters will avoid confusion by always giving us a true array, and by using a dedicated syntax that makes rest parameters easy to spot when reading the function signature.

## Spread Operator

The spread operator shares the same syntax we saw with rest parameters, a series of three dots (...). However, a rest parameter will collect individual parameters into an array while the spread operator expands an array into individual parameters. We can use rest parameters when defining a function and use the spread operator when invoking a function. For example:

let doWork = function(x, y, z) {

    return x + y + z;

}

let result = doWork(...[1, 2, 3]);

expect(result).toBe(6);

In the above code, the spread operator will “spread” the array of three values across the parameters x, y, and z.

The spread operator can also expand an array to create individual elements in an array literal.

let a = [4, 5, 6];

let b = [1, 2, 3, ...a, 7, 8, 9];

expect(b).toEqual([1,2,3,4,5,6,7,8,9]);

Although the examples I've shown all use the spread operator with an array, the spread operator also works with any iterable object. We’ll look at iterable objects a bit later in the book.

The spread operator also makes it easy to pass parameters along to another function when you don’t care about the actual parameter values (a scenario where we typically use Function.apply). This is the case in thedoSomething method below.

let doWork = function(x, y, z){

    return x + y + z;

}

let doSomething = function(...args){

    return doWork(...args);

}

let result = doSomething(...[1,2,3,4,5]);

expect(result).toBe(6);

Notice that when using the spread, you can have more values in the array than the destination function requires. The spread will start from the beginning of the array to populate parameters, so in the above example,doWork will only see the first three values in the array.

## Destructuring

To destructure an object is to dismantle or tear apart an object – the opposite of constructing.

In 2015, a destructuring assignment allows us to tear apart an array or object into individual pieces and assign the pieces into variables. The square brackets[ and ] are used to destructure an array, while curly braces{and} will destructure an object.

The following code will destructure an array so that x contains 22 and y contains 44\.

let values = [22, 44];

let [x, y] = values;

expect(x).toBe(22);

expect(y).toBe(44);

You can think of[ and ] on the right-hand side of an assignment as symbols to construct an array. The[ and ] on the left-hand side of an assignment destructure the array and declare two variables to hold the pieces.

Destructuring objects follows the same pattern, but will use{ and }.

let person = { firstName: "Scott", lastName: "Allen" };

let {firstName, lastName} = person;

expect(firstName).toBe("Scott");

expect(lastName).toBe("Allen");

You do not need to useletorvar with destructuring to create new variables, you can also destructure into existing variables.

let x = 10, y = 20;

// swap!!

[x,y] = [y,x];

expect(x).toBe(20);

expect(y).toBe(10);

You can also destructure arrays and objects returned from a function call.

let doWork = function() {

    return [1, 3, 2];

};

let [, x, y, z] = doWork();

expect(x).toBe(3);

expect(y).toBe(2);

expect(z).toBeUndefined();

Note a couple of special properties in the destructuring ofdoWork’sresult. First, the opening comma will skip the first array element, and you can use additional commas anywhere to skip additional elements. Secondly, if there are not enough array elements to satisfy all the variables required by the destructuring, the extra variables will receive the valueundefined. 

You can also use destructuring in a function parameter list.

let doWork = function({firstName, lastName, role="developer"}) {

    return role + " " + firstName + " " + lastName;

};

let person = {firstName: "Scott", lastName: "Allen"};

let result = doWork(person);

expect(result).toBe("developer Scott Allen");

The above example uses a default parameter value to assign “developer” to theroleparameter in case the incoming object does not have aroleproperty (otherwise,rolewould receive the valueundefined).

Default parameters are not restricted to function declarations when using destructuring.The following code has a default for thecountry variable.

let address = { state:"Maryland" };

let { state="New York", country="USA"} = address;

expect(state).toBe("Maryland");

expect(country).toBe("USA");

Combine destructing with rest parameters to capture the remaining elements of an array.

let odds = [1,3,5,7,9];

let [first, second, ...rest] = odds;

expect(first).toBe(1);

expect(second).toBe(3);

expect(rest).toEqual([5,7,9]);

Destructuring can also drill into complex objects, even objects with collections inside.

let employee = {

    firstName: "Scott",

    address: {

        state: "Maryland",

        country: "USA"

    },

    favoriteNumbers: [45,55,32,13]

};

let { firstName, address: {state}, favoriteNumbers: [,second]} = employee;

expect(firstName).toBe("Scott");

expect(state).toBe("Maryland");

expect(second).toBe(55);

### Destructuring in Practice

One area where destructuring will lead to more maintainable code is in the use of configuration objects, like the configuration object injQuery’sajax method. Finding the available options and the default values for those options is often difficult. Maintaining the options and defaults can also be tricky as an author. With destructuring, configuration options and defaults become more explicit.

let httpPost =

    function(url, {

        cache = true,

        contentType = "application/json",

        timeout = 2500,

        headers = {},

        // ...

    }) {

     // ...

};

## Template Literals

Template literals provide JavaScript with string formatting capabilities. Like many template technologies, templates in JavaScript consist of literal text, and placeholders where the runtime can evaluate an expression and substitute data into the literal text.

        let name = "Scott";

        let message = `Hello, ${name}!`;

        expect(message).toBe("Hello, Scott!");

Backtickcharacters (`) enclose the entire template literal, while$and{} denote the substitution placeholders. Inside a placeholder, you can use identifiers and expressions.

let showTheMath = function(x,y ){

              return `${x} + ${y} is ${x + y}`;

};

let result = showTheMath(3,4);

expect(result).toBe("3 + 4 is 7");

Template literals can also span multiple lines.

let message = `This is

               a short, but multi-line message`;

Note thatmessage will contain a newline character because newlines (and trailing spaces) are significant inside of a template literal.

Template literals are a useful addition to the language. However, template literals become exceptionally interesting when using them with a tag.

## Tagged Template Literals

The tag is a function with the ability to interpret and process a template. The tag appears in front of the template, so in the following code the tag istest.

let name = "Scott";

let result = test `Hello, ${name}!`;

In this example,test is a custom function we’ll write. The runtime invokes a tag function and passes two parameters. The first parameter will be an array containing the literal pieces of text in the template.

let test = function(literals, ...values) {

    expect(literals.length).toBe(2);   

    expect(literals[0]).toBe("Hello, ");

    expect(literals[1]).toBe("!");

    return "test";

};

let name = "Scott";

let result = test `Hello, ${name}!`;

expect(result).toBe("test");

The template in the above code,`Hello, ${name}!`, generates an array with two pieces of literal text,“Hello”, and“!”. The runtime is breaking apart the template for us and giving us the literal text without the placeholders.

The rest of the parameters to the tag function will contain the interpreted substitution values. If you don’t know how many placeholders will appear in a template, you can use a rest parameter to capture all the values in an array. Here is another code snippet showing how the runtime passes all the literal text and substitution values.

let test = function(literals, ...values) {

    expect(literals.length).toBe(3);

    expect(literals[0]).toBe("Hello, ");

    expect(literals[1]).toBe(", ");

    expect(literals[2]).toBe("!");

    expect(values.length).toBe(2);

    expect(values[0]).toBe("Allen");

    expect(values[1]).toBe("Scott");

    return "test";

};

let firstName = "Scott";

let lastName = "Allen";

let result = test `Hello, ${lastName}, ${firstName}!`;

expect(result).toBe("test");

A tag function can build the output of a template by concatenating strings. For each literal value, you can append the literal to the result and then append avalue. However, a tag can interpret a template using any logic it desires, so if the tag wants to heedlessly return the string“test” regardless of the contents of the template, it can (as the code above is doing). The tag could also return the number 42, or any object.

A more reasonable implementation of a tag might look like the following.

let upper = function(strings, ...values) {

    let result = "";

    for(let i = 0; i < strings.length; i++) {

        result += strings[i];

              if(i < values.length){

                  result += values[i];

              }

    }

    return result.toUpperCase();

};

var x = 1;

var y = 3;

var result = upper `${x} + ${y} is ${x+y}`;

expect(result).toBe("1 + 3 IS 4");

The tag  upperbuilds a result that would look just like the normal evaluation of the template literal, but usestoUpperCase before returning the result to ensure the result uses all uppercase letters.

### The Power of Tagged Template Literals

A tag’s ability to modify the output of a template is powerful. Imagine a tag that can build safe URLs by URL encoding a string, or asafehtml tag to build encoded HTML. Since we often use JavaScript to generate content like HTML, JSON, URLs, and form encoded inputs, future tag libraries to make these operations safe and easy will be invaluable.

Even more interesting is the idea that the content inside of a template could be a language unto itself. The tag function could be the gateway to the interpreter for a domain specific language, which opens up many possibilities for the use (and abuse) of tagged template literals.

# Classes

Historically, many developers have learned JavaScript after learning languages like C++, Java, C#, Ruby, or Python. All of these languages have a class keyword, and in many of these languages, the class keyword is a primary building block for constructing software.

Theclasskeyword in JavaScript will play a role similar to theclass keyword in other languages. Classes allow developers to define a blueprint for the construction of objects. The class defines the methods and properties an object will have when a program creates an instance of the class. A program can create as many objects as it needs from a single class definition.

## The Class Keyword

Every class has a name followed by a body containing the method definitions for the class.

class Employee {

    hire() {

        this.hired = true;

    }

    getStatus() {

        if(this.hired) {

            return "hired";

        }

    }

}

The above class has two methods:hireandgetStatus. Notice we do not need to use thefunction keyword to define the methods for the class. These methods will be available on every object we create using the Employee class, and the methods can save and retrieve state inside the object using thethis keyword.

We can create an instance ofEmployeeusing thenew keyword with the class name.

let developer = new Employee();

developer.hire();

expect(developer.hired).toBe(true);

expect(developer.getStatus()).toBe("hired");

We often say thenew keyword instantiates an object, and the variablenameddeveloper holds a reference to an instanceof theEmployee class.

You will often want an object to begin life holding specific pieces of data, or state. We can add initialization logic for every object using a special constructor method.

## Class Constructor and Properties

Every class may specify a single method with the nameconstructor. The runtime will automatically invoke the constructor method when instantiating a class. We can use the constructor to initialize state in an object, often by accepting parameters in the constructor method. In the following code, we want every employee to have a name.

class Employee {

    constructor(name) {

        this.name = name;

    }

    getName() {

        return this.name.toUpperCase();

    }

}

let developer = new Employee("Scott");

expect(developer.name).toBe("Scott");

expect(developer.getName()).toBe("SCOTT");

Notice how the code can pass arguments to the constructor when using thenew keyword.

A class can also define propertieswithget and set to encapsulate a field.

class Employee {

    constructor(name) {

         this._name = name;

    }

    doWork() {

        return `${this._name} is working`;

    }

    get name() {

        return this._name.toUpperCase();

    }

    set name(newName){

        if(newName){

            this._name = newName;

        }

    }

}

let developer = new Employee("Scott");

expect(developer.name).toBe("SCOTT");

developer.name = "Alex";

expect(developer.doWork()).toBe("Alex is working");

## Classes behind the Scenes

Even before the class keyword came along, we had the ability to define a blueprint for object construction in JavaScript. The approach was one we called the “constructor function and prototype object” approach.

let Employee = function(name) {

    this._name = name;

};

Employee.prototype = {

     doWork: function() {

          return `${this._name} is working`;

     },

     get name() {

         return this._name.toUpperCase();

     },

     set name(newName) {

         if(newName) {

              this._name = newName;

         }

     }

};

let developer = new Employee("Scott");

expect(developer.name).toBe("SCOTT");

Behind the scenes, the class keyword is setting up a constructor function and prototype object for us, and all the prototype tricks we’ve learned in the past still work. For example, “borrowing” a method from a prototype object:

class A {

    doWork() {

        return "complete!";

    }

}

var result = A.prototype.doWork.call();

expect(result).toBe("complete!");

Theinstanceof operator also works as expected.

class A {

    // …

}

var a = new A();

expect(a instanceof A).toBe(true);

expect(a instanceof Object).toBe(true);

Finally, you can still augment a type by directly modifying prototype objects.

class A {

}

A.prototype.newMethod = function() {

    return "new!";

};

var a = new A();

expect(a.newMethod()).toBe("new!");

You can think of the class keyword as being syntactic sugar for creating constructor functions and prototype objects. However, there is more to the class keyword than what we’ve seen so far.

## Statics

A class may contain one or more methods defined with the keyword static.

class Employee {

    constructor(name) {

        this._name = name;

    }

    static convert(thing) {

        if(thing.name) {

            return new Employee(thing.name);

        }

    }

}

Like other languages with static class members, the static keyword will create a method associated with the class, and not with an instance of the class. In other words, you can only reach a static method using the name of the class.

expect(Employee.convert).toBeDefined();

expect(new Employee().convert).toBeUndefined();

Static methods have no access to the fields, properties, and methods defined on an instance of the class usingthis.For example, theconvertmethod would not be able to usethis.nameto get to thenamefield of anEmployee object, because thethispointer inside ofconvertwill never reference anEmployee object. However, static methods are often useful and can play the role of factory methods, conversion methods, or general class helper methods.

let person = { name: "Scott" };

let newHire = Employee.convert(person);

expect(newHire.name).toBe("Scott");

Behind the scenes, a static method is associated with the constructor function and not the prototype object like the instance members we saw in the last section.              

var Employee = function(name) {

    // ...

};

Employee.convert = function(thing) {

     // ...

};

## Inheritance

Over the years, there have been various approaches to building class hierarchies in JavaScript. All these approaches worked by stitching together constructor functions and prototype objects and each approach was slightly different from the others.

ES2015allows for a declarative, consistent approach to inheritance using theclassandextends keywords. As an example, let’s start with a simple class to represent a person with a name.

class Person {           

     get name() {

         return this._name;

     }

     set name(newName){

         if(newName){

              this._name = newName;

         }

     }

}

var p1 = new Person();

p1.name = "Scott";

expect(p1.name).toBe("Scott");

Now we also need a class to represent an employee who has both a name and a title. Using theextendskeyword, we can have anEmployeeclass inherit from thePersonclass, meaning every object instantiated as anEmployee will also have all the methods and properties available foraPerson.

class Employee extends Person {

    get title() {

        return this._title;

    }

    set title(newTitle) {

        this._title = newTitle;

    }

}

var e1 = new Employee();

e1.name = "Scott"; // inherited from Person

e1.title = "Developer";

expect(e1.name).toBe("Scott");

expect(e1.title).toBe("Developer");

expect(e1 instanceof Employee).toBe(true);

expect(e1 instanceof Person).toBe(true);

When describing the relationship betweenEmployeeandPersonwe often sayPerson is a super  classofEmployee, whileEmployee is a sub classofPerson. We can also say that every employee is aperson, and as you can see in the above code, theinstanceofcheck in JavaScript confirms that an object created using theEmployee class is also an instance ofPerson.

While everyEmployeeobject will inherit all the state and behavior of aPerson, theEmployee class also has the ability to override the methods and properties defined byPerson. For this example, let’sadd adoWorkmethod to everyPerson.

class Person {

    get name() {

        return this._name;

    }

    set name(newName){

        if(newName){

            this._name = newName;

        }

    }

    doWork() {

        return this.name + " works for free";

    }

}

var p1 = new Person();

p1.name = "Scott";

expect(p1.doWork()).toBe("Scott works for free");

By default, anEmployee will behave the sameas aPerson.

var e1 = new Employee();

e1.name = "Scott";

e1.title = "Developer";

expect(e1.doWork()).toBe("Scott works for free");

However, in theEmployee class we can override the behavior ofdoWork by providing a new implementation.

class Employee extends Person {

    get title() {

        return this._title;

    }

    set title(newTitle) {

        this._title = newTitle;

    }

    doWork() {

        return this.name + " works for a salary";

    }

}

var p1 = new Person();

p1.name = "Scott";

expect(p1.doWork()).toBe("Scott works for free");

var e1 = new Employee();

e1.name = "Scott";

e1.title = "Developer";

expect(e1.doWork()).toBe("Scott works for a salary");

As the test proves, objects instantiated from theEmployee class will behave slightly differently in the doWork method than objects instantiated from thePerson class. In object-oriented programming, we call this behavior polymorphism.

## Using Super

There are times when a class will want to invoke behavior in its super class directly, which can be done with thesuperkeyword. For example, the Employee class could implement thedoWork method as follows.

doWork() {

    return super() + "!";

}

Invokingsuper will execute the super class method of the same name, so with the above code a passing test would look like the following.

var e1 = new Employee();

e1.name = "Alex";

e1.title = "Developer";

expect(e1.doWork()).toBe("Alex works for free!");

A class can also refer explicitly to any method in the super class.

doWork() {

     return super.doWork() + "!";

}

## Super Constructors

One common scenario for usingsuperis when inheriting from a class that requires constructor parameters. The followingPerson class now accepts a name parameter during initialization.

class Person {

    constructor(name) {

        this._name = name;

    }

    get name() {

        return this._name;

    }

}

Now an employee will need both a title and a name during initialization.

class Employee extends Person {

    constructor(name, title) {

        super(name);

         this._title = title;

    }

    get title() {

        return this._title;

    }

}

Notice how theEmployee  constructormethod usessuper to pass along the name parameter to thePerson  constructor and reuse the logic inside the super class.

## The Caveat

Now that we know what inheritance looks like in ES2015, it’s time for a word of caution. Inheritance is a fragile technique to achieve re-use that only works well in a limited number of scenarios. Do a search for “composition over inheritance” to see more details and be wary of misusing inheritance.

# Functional Features

JavaScript has always been a functional programming language. You can pass functions as arguments to other functions, and invoke a function that returns a function back to you. The ES2015 standard improves JavaScript’s functional programming capabilities by offering a new, succinct syntax for creating functions. In addition, 2015 also introduces new features closely associated with functional programming, features like iterators and lazy evaluation. Let’s start looking at the new capabilities by looking at the arrow function, which will look familiar to anyone who has worked with CoffeeScript or C# code.

## Arrow Functions

An arrow function is a function expression with a concise syntax. An arrow function doesn’trequire thefunction keyword, or curly braces, or a return statement. However, arrow functions do require a new operator, =>, which looks like an arrow pointing to the right, and which gives these expressions their name. To build an arrow function for adding two numbers, one simply has to write the following.

let add = (x,y) => x + y;

On the left-hand side of the arrow is the parameter list for the function. In this example there are two parameters,xandy. To the right of the arrow is the executable code for the function. In this case, the code returns the sum ofxandy. You could think of the arrow as pointing the parameters to the code that uses them.

Invoking an arrow function looks no different than invoking a traditional function.

let result = add(3, 5);

expect(result).toBe(8);

Arrow functions that use exactly one function parameter do not need to surround the parameter with parenthesis.

let square = x => x * x;

If an arrow function requires zero parameters, or more than one parameter, then the parenthesis are required.

let add = (x,y) => x + y;             // required parens

let square = x => x * x;              // optional parens

let compute = () => square(add(5,3)); // required parens

let result = compute();

expect(result).toBe(64);

So far, the examples use a single expression to the right of the arrow operator. When using a single expression, curly braces and return statements are not required. The return value of the function will be the value of the expression.

However, an arrow function may contain a more complex block of statements, but this approach does require braces and an explicit return (if the function wants to return a value).

let add = (x,y) => {

    var result = x + y;

    return result;

};

### Arrow Functions and this

Every JavaScript programmer knows that thethis pointer is a bit slippery. Consider the code in the following class, particularly the code inside ofdoWork.

class Person {

    constructor(name) {

        this.name = name;

    }

    doWork(callback) {

        setTimeout(function() {

            callback(this.name);

       }, 15);

    }

}

The anonymous function thedoWorkmethod passes intosetTimeoutwill execute in a different context thandoWork itself, which means thethisreference will change. When the anonymous function passesthis.nameto a callback,this won’t point to a person object and the following test will fail.

var person = new Person("Scott");

person.doWork(function(result) {

    expect(result).toBe("Scott"); // fail!

    done();

});

Since developers can never rely on JavaScript’s this reference when asynchronous code and callbacks are in the mix, a common practice is to capture the value ofthisin a local variable and use the local variable in place ofthis. Common variable names top capturethisareself, orme, orthat.

doWork(callback) {

    var self = this;

    setTimeout(function() {

         callback(self.name);

    }, 15);

}

The above code will pass, thanks to theself variable capturing thethis reference.

If we use an arrow function indoWork, we no longer need to capture thethis reference.

doWork(callback) {

    setTimeout(() => callback(this.name), 15);

}

The previous test will pass because an arrow function will automatically capture the value ofthis from the outer, parent function. In other words, the value ofthis inside anarrow function will always be the same as the value ofthis in the arrow’s enclosing function. There is no more need to useselforthat, and you can nest arrow functions arbitrarily deep to preservethis through a series of asynchronous operations.

### Using Arrow Functions Everyday

If you embrace the arrow function syntax, you might find yourself using arrow functions in every third line of code. JavaScript’s affinity for asynchronous operations has created an enormous number of APIs requiring callback functions. However, as JavaScript is a solid functional programming language, more and more synchronous APIs have appeared with function arguments, too.

For example, the previous release of ECMAScriptintroducedforEachandmap methods on array objects.

let result = [1,2,3,4].map(n => n * 2);

expect(result).toEqual([2,4,6,8]);

let sum = 0;

[1,2,3,4].forEach(n => sum += n);

expect(sum).toBe(10);

There are also many libraries (Underscore and Lodash being two examples) that use higher order functions to implement filtering, sorting, and grouping of data. Before 2015, the code to use with these libraries looked like the following.

let characters = [

    { name: "barney",  age: 36, blocked: false },

    { name: "fred",    age: 40, blocked: true },

    { name: "pebbles", age: 1,  blocked: false }

];

let result = _.find(characters, function(character) {

     return character.age < 40;

});

With arrow functions, the result calculation becomes more expressive.

let result = _.find(characters, character => character.age < 40);

expect(result2.name).toBe("barney");

You can even write a Jasmine test using an arrow function.

it("can work with Jasmine", () => {

    var numbers = [1,3,4];

    expect(numbers.length).toBe(3);

});

The last few examples have all worked against arrays, which are one type of collection. ES2015 also brings the concepts of iterators and iterables to JavaScript, and these new features will make working with collections noticeably more flexible and reliable.

## Iterators

The addition of iterators in 2015 opens up a new world of algorithms and abilities for JavaScript. An iterator is an object that allows code to traverse a sequence of objects. The sequence of objects could be the values inside an array, or values in a more sophisticated data structure like a tree or map. One of the many beautiful characteristics of iterators is how the iterator doesn’t need to know any details about the underlying collection. All an iterator will do is provide the ability to move through a sequence of values one items at a time.

You might be wondering why we are talking about iterators in a chapter devoted to functional programming. We’ll get to that in just a bit, but the short story is that iterators work well with a number of functional programming paradigms, including lazy evaluation and function composition. Before we get to these topics, let’s take a look at the basic characteristics of an iterator.

In ES2015, array objects will have a few new methods available, and one of these methods is thevalues method. Thevalues method returns an iterator object that can visit each value in an array.

let sum = 0;

let numbers = [1,2,3,4];

let iterator = numbers.values();

let next = iterator.next();

while(!next.done){

     sum += next.value;

     next = iterator.next();

}

expect(sum).toBe(10);

Aniterator is an object with anextmethod. Each time the program invokes thenext method, the method returns an object with two properties:valueanddone. Thevalue property represents the current item the iterator is visiting in the collection. Thedoneproperty is a flag holding the valuefalse if there are more items to visit, or the valuetrue if iteration has passed the final item and is complete.

## Looping with for of

Working with iterators at a low level will sometimes be useful, as we’ll see in this chapter, but 2015 also provides a new looping syntax to work with iterators at a higher level – thefor of loop.

    let sum = 0;

    let numbers = [1,2,3,4];

    for(let n of numbers) {

        sum += n;

    }

    expect(sum).toBe(10);

There are a couple observations to make about the above code.

First, the newfor of loop looks like theforin loop which has always been in JavaScript, but the two loops behave differently. Theforin loop works with the enumerable properties of any object. When working with an array, for in  will iterate over the available indexes of the array, not the available values. To compute the same sum as the above code with  for in, we’d need to index into the array with each iteration:

let sum = 0;

let numbers = [1,2,3,4];

for(let i in numbers) {

    sum += numbers[i]; // notice the indexer

}

expect(sum).toBe(10);

Theforof loop uses an iterator to visit the values in an array, not the available keys.

for(let n of numbers) {

    sum += n;

}

This brings up the second subtle difference with  for of. The forof loop only works with iterable objects. Iterable objects are objects with a special method returning an iterator. We’ll look at the special method soon, but notice how the last code snippetdoesn’t need to use thevalues method of the array like the low level iterator code we wrote previously. Instead, theforof loop uses the numbers array directly.

There are many objects in the world of ES6 that will be iterable objects, and we will see more in this book. We’ve already seen how arrays are iterable. Strings are also iterable, meaning you can iterate over the sequence of characters inside.

let result = "";

let message = "Hello";

for(let c of message) {

    result += c;

}

expect(result).toBe("Hello");

How doesfor of retrieve an iterator? What makes an object iterable? To answer these two questions we have to take a brief detour into another new feature of ES2015 – the symbol.

## Symbols

A symbol is a new, primitive data type in ES2015\. There are two key points to understand about symbols.

1.  Every symbol is unique and immutable.
2.  You can use symbols as identifiers when adding properties to an object.

To understand the implications of these two statements, and how they relate to iterable objects, let’s start by creating a new symbol. Creating a new symbol is as easy as invoking the Symbol function.

let s = Symbol();

expect(typeof s).toBe("symbol");

Note that you do not use thenew operator when creating a symbol. To create a symbol you invoke theSymbol function. Otherwise, the runtime will raise an exception.

let makeSymbol = () => new Symbol();

expect(makeSymbol).toThrow();

Each symbol you create is unique and unchangeable.

let s1 = Symbol();

let s2 = Symbol();

expect(s1).toEqual(s1);

expect(s1).not.toEqual(s2);

When you create a symbol, you can add a description by passing a string to theSymbol function, but symbols created with the same description will still be unique, even if the stringified versions look the same.

let s1 = Symbol("some desciption");

let s2 = Symbol("some description");

expect(s1).toEqual(s1);

expect(s1).not.toEqual(s2);

expect(s1.toString()).toBe("Symbol(some description)");

expect(s2.toString()).toBe("Symbol(some description)");

You can use symbols as keys into an object. In the following code,we create one property usinglastName, and we create another property with a symbol (thefirstName symbol).

let firstName = Symbol();

let person = {

    lastName: "Allen",

    [firstName]: "Scott",

};

expect(person.lastName).toBe("Allen");

expect(person[firstName]).toBe("Scott");

Because symbols are unique, a symbol can create a unique property inside an object. You never have to worry about conflicting with existing methods, or being accidently overwritten. ES5 libraries would use property names with timestamps or random numbers to achieve this same effect, but symbols provide a safer guarantee.

Members of an object created using a symbol will not appear as part of the object when using aforin loop.

let firstName = Symbol();

let person = {

    lastName: "Allen",

    [firstName]: "Scott",

};

let names = [];

for(var p in person) {

    names.push(p);

}

expect(names.length).toBe(1);

expect(names[0]).toBe("lastName");

Symbols also won’tappear when usingObject.getOwnPropertyNames.

expect(Object.getOwnPropertyNames(person)).toEqual(["lastName"]);

Nor will they appear when serializing an object to JSON.

expect(JSON.stringify(person)).toBe('{"lastName":"Allen"}');

For these reasons, you might think symbols are useful for hiding information in an object. Although using symbols to hide information is useful, there is a new object method namedgetOwnPropertySymbols that will allow programmers to reflect into hidden symbol properties.

expect(Object.getOwnPropertySymbols(person)).toEqual([firstName]);

let symbol0 = Object.getOwnPropertySymbols(person)[0];

expect(person[symbol0]).toBe("Scott");

Now that we know more about symbols, let’s see how symbols relate to iterable objects.

### Iterables and Symbols

The ES2015 specification defines several well-known symbols. The JavaScript runtime environment uses well-known symbols in the algorithms described by the specification, and each well-known symbol is a property on theSymbol function itself.

One such well-known symbol isSymbol.iterator. If we can access theSymbol.iterator member of an object, the member should be a method we can use to obtain an iterator. The following code will check to see if strings, arrays, and numbers are iterable by looking for this well-known iterator symbol.

let site = "OdeToCode.com";

let values = [1,2,3,4];

let number = 45;

expect(site[Symbol.iterator]).toBeDefined();

expect(values[Symbol.iterator]).toBeDefined();

expect(number[Symbol.iterator]).toBeUndefined();

The tests prove that strings and arrays are iterable, but a number is not iterable.

When we use aforofloop, like in the following code, the JavaScript runtime usesSymbol.iterator behind the scenes to obtain the iterator.

let sum = 0;

let numbers = [1,2,3,4];

for(let n of numbers) {

    sum += n;

}

expect(sum).toBe(10);

We can rewrite the code to represent what is really happening behind the scenes.

let sum = 0;

let numbers = [1,2,3,4];

let iterator = numbers[Symbol.iterator]();

let next = iterator.next();

while(!next.done) {

    sum += next.value;

    next = iterator.next();

}

expect(sum).toBe(10);

Using your knowledge of symbols to write low-level iterator code isn’t exciting, but using symbols to make new iterable objects is exciting.

## Creating Iterables

Imagine you are building an abstraction for a classroom, and one responsibility of a classroom object is to encapsulate the names of the students in the classroom. You might build a class like the following.

class Classroom {

    constructor() {

        this.students = ["Tim", "Joy", "Sue"];

    }

}

On occasion, the outside world needs to know the names of the students inside the classroom. Perhaps the program will show the names in a UI, or save the names in a database. In either case, how should a classroom object give the student names to a caller?

One option is to return a reference to the students array, in which case the caller might change the array by adding or removing items. This option isn’t the best option if the classroom wants to protect the array and validate the addition or removal of a student.

Another option is to make a copy of the array. Even if a caller changes the copy, the original student array remains safe. However, copy operations can be expensive.

With ES2015, the classroom can now provide access to the student names without handing out access to the underlying array. All we need is to make the classroom iterable by adding aSymbol.iterator method.

First, let’s make the classroom iterable by building our own iterator objects. This is the hard way to solve the problem, and we’ll see easier approaches after covering a few more topics.

class Classroom {

    constructor() {

        this.students = ["Tim", "Joy", "Sue"];

    }

    [Symbol.iterator]() {

        var index = 0;

        return {

            next: () => {

                if(index < this.students.length){

                    index += 1;

                    return {done: false, value: this.students[index-1]};

                }

                return { value: undefined, done: true };

            }

        }

    }

}

Notice howSymbol.iterator needs square brackets to surround the method name. Inside the method is the code to return objects with anext method, and thenext method returns objects withdoneandvalue properties. A classroom should now behave just like an array and work in aforof loop.

let scienceClass = new Classroom();

let result = [];

for(let name of scienceClass){

    result.push(name);

}

expect(result).toEqual(["Tim", "Joy", "Sue"]);

The code inside the classroom’s iterator method is the type of code that works with any array. Let’s extract the code into a new class.

class ArrayIterator {

    constructor(array) {

        this.array = array;

        this.index = 0;

    }

    next() {

        let result = { value: undefined, done: true};

        if(this.index < this.array.length) {

            result.value = this.array[this.index];

            result.done = false;

            this.index += 1;

        }

        return result;

    }

}

Now we can reuseArrayIterator from several places in an application.

class Classroom {

    constructor() {

        this.students = ["Tim", "Joy", "Sue"];

    }

    [Symbol.iterator]() {

        return new ArrayIterator(this.students);

    }

}

Even though theArrayIterator class is helpful, an easier approach to creating an iterable is to use a generator.

## Generators

You’ll know when you are looking at a generator function, because a generator function contains an asterisk in the declaration.

function*() {

}

Once you have a generator function, you can use theyield keyword inside the function to return multiple values to the caller.

let numbers = function*() {

        yield 1;

        yield 2;

        yield 3;

};

However, the return values do not return to the caller all at once. Internally, the runtime builds an iterator so a caller can iterate through the generator results one by one. The following code uses aforofloop to iterate over thenumbers function.

let sum = 0;

for(let n of numbers()) {

    sum += n;

}

expect(sum).toBe(6);

Going back to theClassroom class we used in the last section, we can now make aClassroom iterable using a generator function andyield.

class Classroom {

    constructor(...students) {

        this.students = students;

    }

    *[Symbol.iterator]() {

        for(let s of this.students) yield s;

    }

}

var scienceClass = new Classroom("Tim", "Sue", "Joy");

var students = [];

for(let student of scienceClass){

    students.push(student);

}

expect(students).toEqual(["Tim", "Sue", "Joy"])

Notice how the iterator method needs an asterisk before the opening square bracket. The syntax is quirky, but an asterisk is always required when defining a generator function, because generator functions behave differently than normal functions.

## Lazy Evaluation

Generators in most languages do the least amount of work possible, and generators in JavaScript are no different. When a program invokes a normal function, you can imagine the program jumping into the function and executing code until the function completes. However, the behavior of a generator function is different.

As an example, let’s use the following generator function.

let random = function*() {

    while(true) {

        console.log("make random")

        yield Math.random();

    }

}

Therandom function looks like it will burn CPU cycles in an infinite loop. However, if we invoke the function and look for output in the console – there will be no output!

When you invoke a generator function, you can think of the runtime setting up a state machine behind the scenes. The state machine knows how to take the code inside the generator function and allow pieces to execute on demand.

What creates the demand?

Since generators produce iterators, then each call to thenext method of the iterator will force the state machine to execute just enough code to produce the next value, but no more. For example, if we execute the following code:

let iterator = random();

iterator.next();

Then we will see “make random” appear exactly once in the console. Asking the iterator for the next value forced the state machine to execute code inside the function until ayield statement returnedanother value. Each time there is a call tonext on the iterator, the flow of the program jumps back into the generator function at the point the program last left the function, and execution continues until the program reaches anotheryield.

In computer science terminology, a generator function offers what we call lazy evaluation. In order to make the function perform work, we need to pull values out of the function by asking for those values through the iterator API. Therandom function will only create an infinite loop if we ask for an infinite number of values.

Let’s imagine we wanted a finite number of random numbers, and we only want random numbers less than 0.5\. First, we could write a filtering function that will take an iterable object and a predicate function as arguments. The filtering function will only produce the items for which the predicate function returns true.

let filter = function*(items, predicate) {

    for(let item of items){

        console.log("filter", item);

        if(predicate(item)){

            yield item;

        }

    }

};

To make sure we ask for a finite number of items, we can also write atake function, to take a specific number of items.

let take = function*(items, number) {

    let count = 0;

    if(number < 1) return;

    for(let item of items){

       console.log("take", item);

        yield item;

        count += 1;

        if(count >= number) {

            return;

        }

    }

};

Noticehow we can stop iteration using areturnstatement in thetake function.

Using the previous functions, all of which are generators, we can create two random numbers less than 0.5 with the following code.

let result = take(filter(random(), n => n < 0.5), 2);

Except, we have not created any numbers with the above code! All we’ve created is an iterator. No output will appear in the console, because there is no code trying to use the iterator to pull numbers through the generators.

We could force the functions to execute code using aforofloop, or useArray.from, which is a new API we can use to convert any iterable object to a concrete array.

expect(Array.from(result).length).toBe(2);

Console output of the above code will look like the following.

make random

filter 0.24152887403033674

take   0.24152887403033674

make random

filter 0.6618692250922322

make random

filter 0.49661534116603434

take   0.49661534116603434

Notice how the function execution interleaves. You can imagine the iterators pulling values from each function on an as-needed basis.

Lazy evaluation allows for many interesting scenarios with control flow and data structures. We’ll look at some of these scenarios later.

## Iterators Revisited

Earlier in the chapter, we saw how to work with iterators at a low level and use an iterator’snext method to move from one item to the next item. What’s interesting about iterators in JavaScript is how the consumer of an iterator can passa parameter to thenext method.

As an example, let’slook at the followingrange method. You can use therange methodto generate a sequence of numbers fromstarttoend.

let range = function*(start, end) {

    let current = start;

    while(current <= end) {

        yield current;

        current += delta || 1;

    }

}

If we askrange to give us numbers from one to ten, the range method will behave as expected.

let result = [];

let iterator = range(1,10);

let next = iterator.next();

while(!next.done) {

    result.push(next.value);

    next = iterator.next();

} 

expect(result).toEqual([1,2,3,4,5,6,7,8,9,10]);

Now let’smake a small change to therangemethod. When weyield the current value, we’llplace theyield expression on the right-hand side of an assignment expression.

let range = function*(start, end) {

    let current = start;

    while(current <= end) {

        var delta = yield current;

        current += delta || 1;

    }

}

When the iterator consumer invokes thenextmethod and passes a parameter, the parameter will become the return value of theyieldstatement. The range method assigns this return value to thedelta variable. If the consumer does not pass a value, the code defaults the delta value to 1. If we iterate over range as we did before, we will still see the same results.

let result = [];

let iterator = range(1,10);

let next = iterator.next();

while(!next.done) {

    result.push(next.value);

    next = iterator.next();

} 

expect(result).toEqual([1,2,3,4,5,6,7,8,9,10]);

However, if we pass the number 2on each call to thenext method, we will effectively increment the current value in the iterator by 2 instead of 1\.

let result = [];

let iterator = range(1,10);

let next = iterator.next();

while(!next.done) {

    result.push(next.value);

    next = iterator.next(2);

} 

expect(result).toEqual([1,3,5,7,9]);

If we were to write the latestrangemethod the hard way instead of usingyield, it might come out to look like the following.

let range = function(start, end) {

    let firstCall = true;

    let current = start;

    return {

        next(delta = 1) {                                            

            let result = { value: undefined, done: true};

            if(firstCall){

                firstCall = false;

            }

            else {

                 current += delta;

            }

            if(current <= end) {

                 result.value = current;

                 result.done = false;

            }

            return result;

        }

    }

}

In this version of the code it is easier to see howthenext method receivesa parameter you can use in the iterator logic. When usingyield, the parameter arrives as the return value of the yield expression. Also, when implementing therangefunction usingyield, there is no ability to catch the incoming parameter on the first call to thenext method.

## Delegating Yield

Generator methods can call into other generator methods. A generator can even unroll another generator’s result into it’sown iterator usingyield*. As an example, consider the following generator method.

let inner = function*() {

    yield "Hello";

    yield "there";

}

Theoutergenerator will call theinnergenerator using theyield* syntax.

let outer = function*() {

     yield* inner();

     yield "World";

}

Theyield*syntax will flatten the result frominnerso that theouter generator yields three strings.

var result = Array.from(outer());

expect(result).toEqual(["Hello", "there", "World"]);

If the outer generator usedyieldinstead ofyield*, the result of outer would be inner’s iterator object, followed by the string “World”.

# Asynchronous JavaScript

Asynchronous programming has been a hallmark of JavaScript programming since the beginning. Examples include waiting for button clicks, waiting for timers to expire, and waiting for network communications to complete. For most of JavaScript’s life, we’ve implemented these waiting activities using callback functions.

let calculate = function(callback) {

    setTimeout(() => {

       callback("This is the result");

    }, 0);

};

calculate(result => {

     expect(result).toBe("This is the result");

     done(); // done is required to complete an async test in Jasmine

});

Over the years, as JavaScript applications grew in complexity, unofficial specifications started to emerge for a different approach to asynchronous programming using promises. A promise is an object that promises to deliver a result in the future. Promises are now an official part of the JavaScript language and offer advantages over the callback approach to asynchronous programming. Error handling is often easier using promises, and promises make it easier to compose multiple operations together. These advantages make code easier to read and write, and we’ll see these advantages in the next section.

## Promise Objects

We need to look at promises from two different perspectives. One perspective is the perspective of the code consuming a promise. A promise consumer uses a promise to wait for an asynchronous activity to complete. Another perspective is the perspective of a promise producer. A producer uses a promise to deliver the results of an asynchronous operation. Let’s start by looking at a producer.

### A Promise Producer

In the previous example, thecalculate function delivers a result asynchronously after a timer expires by invoking a callback function and passing along the result. When using promises, thecalculate function could look like the following.

let calculate = function () {

        return new Promise((resolve, reject) => {

            setTimeout(() => {

                resolve(96);

            }, 0);   

        });

};

Instead of taking a callback function as a parameter, thecalculate method returns a new promise object. ThePromise constructor takes a parameter known as the executor function. The previous code implements the executor as an arrow function. The executor itself takes two arguments. The first argument is the resolvefunction. Invokingresolve fulfills the promise and delivers a successful value to anyone who is waiting for a result from the promise. The second function is the rejectfunction. Invokingreject will reject the promise, which signals an error. The above code always resolves the promise successfully and passes along a result of 96\.

### A Promise Consumer

Instead of passing a callback function to thecalculatemethod, the consumer now invokes thecalculate method and receives a promise object. A promise object provides an API that allows the consumer to execute code when the producer resolves or rejects the promise. The most important part of the promise API fora consumer is thethenmethod. Thethen method allows the consumer to pass function arguments to execute when the promise resolves or rejects. The consumer code for calculate can now look like the following.

        let success = function(result) {

            expect(result).toBe(96);

            done(); 

        };

        let error = function(reason) {

            // ... error handling code for a rejected promise 

        };

        let promise = calculate();

        promise.then(success, error);

The first argument to thethen method is the success handler, while the second argument is the error handler.

On the surface, using promises might seem more involved than using simple callback functions. However, promises really start to shine when chaining operations, composing operations, and when handling errors.

## Promise Chaining

Chaining promises canmake asynchronous code flow synchronously. For example, consider the followingcalculate method, which delivers a result using a promise.

let calculate = function (value) {

    return new Promise((resolve, reject) => {

        setTimeout(() => {

            resolve(value + 1);

        }, 0);

    });

};

Imagine you need to invoke the method four times, and each time you invokecalculate you need to pass the result from the previous call into the next call (this would simulate HTTP APIs where you need to make multiple requests, all dependent on one another, to fetch all of data required for a page). With promises, the series of method calls could look like the following.

let verify = function(result) {

    expect(result).toBe(5);

    done();

};

calculate(1)

    .then(calculate)

    .then(calculate)

    .then(calculate)

    .then(verify);

The above code also verifies (with Jasmine) that the final value is 5, becausecomputewill add 1 to the result on each invocation. The code works because each call to thethen method of a promise will result in a new promise. You might think this happens because thecalculatemethod returns a new promise, but a new promise will appear even if the function passed to thethen method doesn’t explicitly produce a promise. As an example, let’sreplace one call tocalculate with an arrow function that simply returns result + 1\.

calculate(1)

    .then(calculate)

    .then(result => result + 1)

    .then(calculate)

    .then(verify);

The result of the above code is still the value 5, and the object returned from thethen call with an arrow function is still a promise. Thethen method will ensure the return value is a promise by creating a new promise wrapper, if necessary. If the success handler does not return anyvalue, the new promise will deliver the valueundefined to the next handler.

## The Promise API

APromise in JavaScript offers a few static methods you can use as convenience methods. For example, if you need to return a promise to a caller,but you already have a value to resolve the promise without performing any asynchronous work, theresolve method is handy.

let doAsyncWork = function () {

    // note: no real async work to perform

    return Promise.resolve(10);

};

doAsyncWork().then(result => {

    expect(result).toBe(10);

    done();

});

Likewise, thereject method will deliver a result to an error handler.

let doAsyncWork = function () {

    return Promise.reject("error!");

};

doAsyncWork().then(() => { }, message => {

    expect(message).toBe("error!");

    done();

});

Therace method will combine multiple promises into a single promise. The single promise will resolve when the first passed promise resolves. It’s a race to see who finishes first!

let slowExecutor = function (resolve, reject) {

    setTimeout(() => {

        resolve(9);

    }, 250);

};

let fastExecutor = function (resolve, reject) {

    setTimeout(() => {

        resolve(6);

    }, 100);

};

let p1 = new Promise(slowExecutor);

let p2 = new Promise(fastExecutor);

let p3 = Promise.race([p1, p2]);

p3.then(result => {

    expect(result).toBe(6);

    done();

});

In contrast torace, theall method will combine multiple promises into a single promise. The single promise will resolve when all of the multiple promises resolve.

let slowExecutor = function (resolve, reject) {

    setTimeout(() => {

        resolve(9);

    }, 250);

};

let fastExecutor = function (resolve, reject) {

    setTimeout(() => {

        resolve(6);

    }, 100);

};

let p1 = new Promise(slowExecutor);

let p2 = new Promise(fastExecutor);

let p3 = Promise.all([p1, p2]);

p3.then(result => {

    expect(result[0]).toBe(9);

    expect(result[1]).toBe(6);

    done();

});

The combined resultsarrive in an array. The results in the array will be in the same order as the promises passed to theall method.

Of course, not all promises resolve successfully, so let’s talk about error handling.

## Promise Errors

Errors in asynchronous code typically require a messy number ofif elsechecks and a careful inspection of parameter values. Promises allow asynchronous code to apply structured error handling. When using promises, you can pass an error handler to thethenmethod or use acatch method to process errors. Just like exceptions in regular code, an error or exception in asynchronous code will jump to the nearest error handler.

As an example, let’s use the following functions which log the execution path into a string variable.

var log = "";

function doWork() {

   log += "W";

    return Promise.resolve();

}

function doError() {

    log += "E";

    throw new Error("oops!");

}

function catchHandler() {

    log += "T";

}

function errorHandler(error) {

    log += "H";

}

We’ll use these functions with the following code.

doWork()

    .then(doWork)

    .then(doError)

    .then(doWork) // this will be skipped

    .then(doWork, errorHandler)

    .then(verify);

function verify() {

    expect(log).toBe("WWEH");

    done();

}

The expectation is that thelog variable will contain “WWEH” when the code finishes executing, meaning the flow of calls willreachdoWork, thendoWork, thendoError, thenerrorHandler. There are two observations to make about this result, one obvious, one subtle.

The first observation is that when the call todoError throws an exception, execution jumps to the next rejection handler (errorHandler) and skips over any potential success handlers. This behavior is obvious once you think of promises as a tool to transform asynchronous code into a procedural flow of method calls. In synchronous code, an exception will jump over statements and up the stack to find a catch handler, and the asynchronous code in this example is no different.

What might not be immediately obvious is that theverify function will execute as a success handler after the error. Just as normal execution can resume in synchronous code after a catch statement, normal execution can resume with promises after a handled error. Technically, theverify function executes because the error handler returns a successfully resolved promise. Remember thethen method always returns a new promise, and unless the error handler explicitly rejects a new promise, the new promise resolves successfully.

A promise object also provides acatch method to handle errors. We could write the last code sample with a catch statement as follows.

doWork()

    .then(doWork)

    .then(doError)

    .then(doWork)

    .then(doWork)

    .catch(errorHandler)

    .then(verify);

Thecatch method takes only a rejection handler method. There is a subtle difference in the following two code snippets:

.then(doWork, errorHandler)

… and …

.then(doWork)

.catch(errorHandler)

In the first code snippet, if the success handler throws an exception or rejects a promise, execution will not go into the error handler since the promise was already resolved at this level. Withcatch, you can always see an unhandled error from the previous success handler.

As a final note, if you do not have any error handlers in place for a promise operation and an error occurs, no one will know! You can simulate this scenario with the following line of code.

Promise.reject("error!");

Some environments and Promise polyfills will warn you about unhandled rejections by displaying a message in the console of the developer tools. An unhandled promise rejection means your application could be missing a critical error!

# Modules

Avoiding global scope has been a primary architectural goal of nearly every library and framework authored over the last ten years. Avoiding global scope in the browser has meant we’ve relied heavily on closures and syntactical oddities like the immediately invoked function expression (IIFE) to provide encapsulation.

(function() {

    // code goes here, inside an IIFE

}());

Avoiding global scope also meant nearly every library and framework for the browser would expose functionality through a single global variable. Examples include$orjQuery for the jQuery library, or_ for underscore and lodash.

After NodeJS arrived on the scene in 2009, Node developers found themselves creating larger code bases and consuming a larger number of libraries. To manage scope and dependency issues in this new environment, the Node community created an unofficial standard we now call the CommonJS module standard. Shortly afterward, another community standard, the Asynchronous Module Definition standard (AMD), appeared for browser programming.

ES2015 brings an official module standard to the JavaScript language. This module standard uses a different syntax than both CommonJS and AMD, but tools like WebPack and runtime polyfills make all of the module standards mostly interoperable. At the time of this writing, some preprocessing or polyfills are required to make the new module syntax work. Even though the syntax of the language is complete and standardized, the browser APIs and behaviors for processing modules are still a work in progress.

## Why Modules?

A module system allows JavaScript code to scale up in size. Modules give us a tool to manage the complexity of a large code base by providing just a few important features.

First, modules in JavaScript are file based. When using ES2015, instead of thinking about a script file, you should think of a script module. A file is a module. By default, any code you write inside the file is local to the module. Variables are no longer in the global scope by default, and there is no need to write a function or an IIFE to control the scope of a variable. Modules give us an implicit scope to hide implementation details.

Of course, some of the code you write in a module is code you might want to expose as an API and consume from a different module. ES2015 provides theexport keyword for this purpose. Any object, function, class, or variable that you want to make available to the outside world is something you must explicitly exportwith theexport keyword.

In a second module, you would use theimport keyword to consume some or all of the exports from the first module.

Modules allow us to spread code across multiple files and directories while still being able to reference and use components across files without going through a global mediator. Perhaps no other feature listed in this book will have as much of an impact on the architecture of applications, frameworks, and libraries as modules. Let’s look at the syntax.

## Module Syntax

Imagine you want to use an object that represents a person, and in a file named humans.js you place the following code.

function work(name) {

              return `${name} is working`;

}

export let person = {

              name: "Scott",

              doWork() {

                            return work(this.name);

              }

}

Since we are working with modules, theworkfunction remains hidden in the module scope, and no code outside of the module will have access to theworkfunction. Theperson variable is an export of the module. More specifically, we call person a named export. Code inside of other modules can import person and work with the referenced object.

import {person} from "./lib/humans"

describe("The humans module", function() {             

    it("should have a person", function() {

        expect(person.doWork()).toBe("Scott is working");

    });

});

There are a few points to make about the previous code snippet.

First, notice the module name./lib/humans does not require a .js extension. The filename is humans.js, but the module name for the file ishumans.

Secondly, the humans module is in a subfolder of the test code in this example. Thus, the module specifier includes a relative path to the module (./lib/humans).

Finally, curly braces enclose the import list from the humans module. The imports are a list because you can import more than one named export from another module. For example, if the humans module also exported the work function, the test code could have access to both exports with the following code.

import {person, work} from "./lib/humans"

You also have the ability to alias an import to a different name.

import {person as scott, work} from "./lib/humans"

describe("The humans module", function() {

              it("should have a person", function() {

                            // now using scott instead of person

                            expect(scott.doWork()).toBe("Scott is working");

              });

              it("should have a work function", function() {

                            expect(work).toBeDefined();

              });

});

In addition to exporting variables, objects, values, and functions, you can also export a class. Imagine the humans module with the following code.

function work(name) {

    return `${name} is working`;

}

export class Person {

    constructor(name) {

        this.name = name;

    }

    doWork() {

        return work(this.name);

    }

}

Now the test code would look like the following.

import {Person} from "./lib/humans"

describe("The humans module", function() {             

    it("should have a person class", function() {

        var person = new Person("Scott");

              expect(person.doWork()).toBe("Scott is working");

    });

});

Modules can also export a list of symbols using curly braces. As an example, we could rewrite the humans module and place all the exports in one location at the bottom of the file.

function work(name) {

    return `${name} is working`;

}

class Person {

    constructor(name) {

        this.name = name;

    }

    doWork() {

        return work(this.name);

    }

}

export {Person, work as worker }

Notice how an export list can alias the name of an export, so theworkfunction exports with the nameworker.

### Default Exports

The 2015 module standard allows each module to have a single default export. A module can have a default export and still export other names, but having a default export does impact how another module will import the default. First, here is how the humans module would look with a default export ofthePerson class.

function work(name) {

              return `${name} is working`;

}

export default class Person {

              constructor(name) {

                            this.name = name;

              }

              doWork() {

                            return work(this.name);

              }

}

As the code demonstrates, the default export for a module uses thedefault keyword.

A module who needs to import the default export of another module doesn’t specify a binding list with curly braces for the default export. Instead, the module simply defines a name for the incoming default, and the name doesn’t need to match the name used inside the exporting module.

import Human from "./lib/humans"

describe("The humans module", function() {

              it("should have a default export as a class", function() {

                            var person = new Human("Scott");

                            expect(person.doWork()).toBe("Scott is working");

              });

});

### Mass Exportation and Importation

An import statement can use an asterisk to capture all the named exports of a module. Let’schange the humans module once again to export thePerson class both as a named export and as a default export.

export function work(name) {

    return `${name} is working`;

}

export class Person {

    constructor(name) {

        this.name = name;

    }

    doWork() {

        return work(this.name);

    }

}

export default Person;

The test code can now have access to all the named exports of the humansmodule usingimport *. Access to the exports will happen through thehumans, which behaves much like a namespace in other languages.

import * as humans from "./lib/humans"

describe("The humans module", function() {

    it("should have a person class", function() {

        var person = new humans.Person("Scott");

              expect(person.doWork()).toBe("Scott is working");

    });

    it("should have a default export", function() {

        expect(humans.default).toBeDefined();

    });

});

Notice how the test code now has two paths to reach thePersonclass. One path is viahumans.Person, the other path ishumans.default.

Anexport statement can also use an asterisk. The asterisk is useful in scenarios where you want one module to gather exports from many submodules and publish them together as a unit. In CommonJS this scenario typically uses a file named index.js, and many of the existing module loader polyfills support using an index.js file when importing a directory. For example, let’s add a file named creatures.js to the lib folder.

export class Animal {

    constructor(name) {

        this.name = name;

    }

}

An index.js file in the lib folder can now combine the humans and creatures module into a single module.

export * from "./creatures"

export * from "./humans"

The test code can now import the lib directory and access features of both underlying modules. ]

import {Person, Animal} from "./lib/"

describe("The combined module", function() {

    it("should have a person class", function() {

        var person = new Person("Scott");

              expect(person.doWork()).toBe("Scott is working");

    });

    it("should have an Animal class", function() {

        expect(new Animal("Beaker").name).toBe("Beaker");

    });

});

### Importing For the Side-Effects

Finally, an import statement doesn’t need to name any imports. In some scenarios you only want to reference a module so the code inside can execute and produce side effects in the environment.

import "./lib"

# APIs

In this final chapter I want to highlight new types and APIs I think are important.

## New Collections

JavaScript has never offered a variety of data structures out of the box. If you needed any structure fancier than an array, you'd have to roll your own or borrow some code.

The 2015 specification brings a number of keyed collections to the language, including theMap,Set,WeakMap, andWeakSet.

### Maps

Although you can treat any JavaScript object as a dictionary or key-value store, there are some drawbacks. Most notably, the only type of key you can use to index into an object are keys with a string or symbol type. The newMap collection removes the restriction on key types and offers some additional conveniences. The core of the API revolves around the get and set methods.

let map = new Map();

// add a new key-value pair

map.set("key", 301);

// overwrite an existing value

map.set("key", 302);

expect(map.get("key")).toBe(302);

Thedeleteandhas methods are also handy.

let map = new Map();

map.set("key", 611);

expect(map.has("key")).toBe(true);

map.delete("key");

expect(map.has("key")).toBe(false);

A key can now be any type of object.

var someKey = { firstName: "Scott"};

var someValue = { lastName: "Allen"};

var map = new Map();

map.set(someKey, someValue);

expect(map.size).toBe(1);

expect(map.get(someKey).lastName).toBe("Allen");

expect(map.get({firstName:"Scott"})).toBeUndefined();

When using objects as keys, JavaScript will compare pointers behind the scenes, as the above code demonstrates.

You can also construct aMap using a two dimensional array of key-value pairs.

let map = new Map([

    [1, "one"],

    [2, "two"],

    [3, "three"]

]);

Finally, maps are iterable in a number of ways. You can retrieve an iterator for the keys in a map (using thekeysmethod), the values in a map (using thevaluesmethod), and the key-value entries in a map (using theentriesmethod, as you might have guessed). A map also has the magic [Symbol.iterator] method, so you can use aMap in aforof loop.

let map = new Map([

    [1, "one"],

    [2, "two"],

    [3, "three"]

]);

let sum = 0;

let combined = "";

for(let pair of map) {

    sum += pair[0];

    combined += pair[1];

}

expect(map.size).toBe(3);

expect(sum).toBe(6);

expect(combined).toBe("onetwothree");

map.clear();

expect(map.size).toBe(0);

In thefor of loop, each entry comes out as an array with the key in index 0, and the value in index 1\. This is a scenario where array destructuring is handy.

for(let [key, value] of map) {

    sum += key;

    combined += value;

}

### Set

Just like in mathematics, aSet maintains a collection of distinct objects. The API is slightly different fromMap. For example, you can construct a Set by passing in an iterator.

let animals = ["bear", "snake", "elephant", "snake"];

let animalsSet = new Set(animals.values());

expect(animals.length).toBe(4);

expect(animalsSet.size).toBe(3);

expect(animalsSet.has("bear")).toBe(true);

animalsSet.delete("bear");

expect(animalsSet.size).toBe(2);

Just like a map, a set compares object types by comparing references. Unlike other languages, there is no ability to provide an alternative comparer strategy.

let scott = { name: "Scott "};

let people = new Set();

people.add(scott);

people.add(scott);

people.add( {name:"Scott"});

expect(people.size).toBe(2);

expect(people.has(scott)).toBe(true);

expect(people.has({name:"Scott"})).toBe(false);

### Weak Collections

TheWeakMapandWeakSetcollections serve a similar purpose to their non-weak counterparts, but the objects held in these collections are eligible for garbage collection at any given point in time, making these weak collections ideal for many extensibility scenarios. The special nature of weak collections means you cannot iterate over the collections, because an entry could disappear before the iteration completes. There are also some other small API differences. For example, the keys for aWeakMapand the values for aWeakSet can only be object types (no primitives like strings). In addition, there is no size method to uncover the number of entries in these collections.

## Arrays

ES2015 adds a few new APIs to the built-in array, includingvalues,keys, andentries. These three methods all return iterators we can use to loop over the values inside an array, or the available keys, or each entry. Each entry will be an array itself, where the key is in index 0, and the value is in index 1.

let names = ["Scott", "Alex"];

let values = names.values();

let keys = names.keys();

let entries = names.entries();

expect(values.next().value).toBe("Scott");

expect(keys.next().value).toBe(0);

expect(entries.next().value[1]).toBe("Scott");

There are also new methods we can use to create arrays. Theofmethod constructs an array from a variable number of arguments, while thefrom method constructs an array from any iterable object.

let numbers = Array.of(15, 11, 3);   

expect(numbers.length).toBe(3);

let squared = Array.from(numbers, n => n * n);

expect(squared[2]).toBe(9);

Finally,findandfindIndex are convenient methods for locating items in an array. The callback function for both of these methods can also take a second parameter to hold the index of the current item.

let numbers = [15,11,3];

let people = [{ name: "Scott"}, { name: "Allen"}];

let eleven = numbers.find(n => n === 11);

let index = people.findIndex(p => p.name === "Allen");

expect(eleven).toBe(11);

expect(index).toBe(1);

## Strings

Strings also offer new convenience methods for locating substrings. These methods arestartsWith,endsWith, andincludes.

let name = "porter";

expect(name.startsWith("port")).toBe(true);

expect(name.endsWith("er")).toBe(true);

expect(name.includes("ort")).toBe(true);

Strings are also iterable in ES2015.

let name = "porter";

for(let character of name) {

    expect(name.includes(character)).toBe(true);                                         

}

## Objects

TheObject.assignmethod will copy the property values of one or more source objects into a target object. Many frameworks over the years have included features to merge objects together, for example, jQuery’sextend function, but now this functionality in built into the runtime.

let a = { a: 1};

let b = { b: 2};                           

let result = Object.assign({}, a, b);

expect(result.a).toBe(1);

expect(result.b).toBe(2);

The runtime copies properties in a left to right order and will overwrite existing properties with the same name.

let a = { a: 1};

let b = { b: 2};

let a2 = { a: 2, foo:"baz"};

let result = Object.assign({foo:"bar"}, a, b, a2);

expect(result.a).toBe(2);

expect(result.b).toBe(2);

expect(result.foo).toBe("baz");

# The End

I sincerely thank you for purchasing and reading this book. I wish you all the best in your software development endeavors, and more.

* * *

[[1]](#part0000_split_004.html__ftnref1) For the pendants: a try/catch block can effectively simulate block scope, but controlling scopes via try and catch is an ugly hack in human readable code.