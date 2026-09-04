
# Javascript 面向对象编程实战

## index.js

```
this === window
true
"use strict";
this === window
true
```

## [暂停] index.js

```
1
```

```
$ node
> this === global
true
> .exit
```

```
console.log(this === global);
```

## index.js

```
console.log(this === module.exports);
```

```
$ node index.js
false
$ node index.js
true
$
```

```
function func() {
    console.log(this === global);
}

func();
```

```
$ node index.js
true
```

```
"use strict";

function func() {
    console.log(this === undefined);
}

func();
```

```
$ node index.js
true
$ node index.js
true
$
```

```
function func() {
    "use strict";
    console.log(this === undefined);
}

func();
```

```
$ node index.js
true
$ node index.js
true
$ node index.js
true
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const person = Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
undefined
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const person = Person("Jane", "Doe");
console.log(person);

console.log(global.firstName);
console.log(global.lastName);
```

```
$ node index.js
undefined
$ node index.js
undefined
Jane
Doe
$ 
```

```
"use strict";

function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const person = Person("Jane", "Doe");
console.log(person);

console.log(global.firstName);
console.log(global.lastName);
```

```
$ node index.js
undefined
Jane
Doe
$ node index.js
/Users/marius/Desktop/this/index.js:4
    this.firstName = firstName;
            ^

TypeError: Cannot set property 'firstName' of undefined
    at Person (/Users/marius/Desktop/this/index.js:4:20)
    at Object.<anonymous> (/Users/marius/Desktop/this/index.js:8:16)
    at Module._compile (module.js:635:30)
    at Object.Module._extensions..js (module.js:646:10)
    at Module.load (module.js:554:32)
    at tryModuleLoad (module.js:497:12)
    at Function.Module._load (module.js:489:3)
    at Function.Module.runMain (module.js:676:10)
    at startup (bootstrap_node.js:187:16)
    at bootstrap_node.js:608:3
$ 
```

```
"use strict";

function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const person = new Person("Jane", "Doe");
console.log(person);

console.log(global.firstName);
console.log(global.lastName);
```

```
$ node index.js

/Users/marius/Desktop/this/index.js:4
    this.firstName = firstName;
                   ^

TypeError: Cannot set property 'firstName' of undefined
    at Person (/Users/marius/Desktop/this/index.js:4:20)
    at Object.<anonymous> (/Users/marius/Desktop/this/index.js:8:16)
    at Module._compile (module.js:635:30)
    at Object.Module._extensions..js (module.js:646:10)
    at Module.load (module.js:554:32)
    at tryModuleLoad (module.js:497:12)
    at Function.Module._load (module.js:489:3)
    at Function.Module.runMain (module.js:676:10)
    at startup (bootstrap_node.js:187:16)
    at bootstrap_node.js:608:3

$ node index.js

Person { firstName: 'Jane', lastName: 'Doe' }
undefined
undefined

$
```

```
function Person(firstName, lastName) {
    console.log(this);
    this.firstName = firstName;
    console.log(this);
    this.lastName = lastName;
    console.log(this);
}

const person = new Person("Jane", "Doe");
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const person = new Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;

    return this;
}

const person = new Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;

    return {
        firstName: "John",
        lastName: "Roe"
    };
}

const person = new Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
{ firstName: 'John', lastName: 'Roe' }
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;

    return new Proxy(this, {
        get(target, name) {
            // ...
        }
    });
}

const person = new Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
{ firstName: 'John', lastName: 'Roe' }
$
```

```
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;

    return null;
}

const person = new Person("Jane", "Doe");
console.log(person);
```

```
$ node index.js
Person {}
Person { firstName: 'Jane' }
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ node index.js
{ firstName: 'John', lastName: 'Roe' }
$ node index.js
Person { firstName: 'Jane', lastName: 'Doe' }
$ _
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

person.sayHi();
```

```
$ node index.js
Hi, my name is John!
$
```

```
function sayHi() {
    console.log(`Hi, my name is ${this.firstName}!`);
}

const person = {
    firstName: "John"
};

person.sayHi = sayHi;
person.sayHi();
```

```
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
$
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

const greet = person.sayHi;
greet();
```

```
$ node index.js
Hi, my name is undefined!
$
```

## index.js

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

setTimeout(person.sayHi, 1000);
```

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is undefined!
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

setTimeout(function() {
    person.sayHi();
}, 1000);
```

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is John!
$
```

## index.js

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

setTimeout(person.sayHi.bind(person), 1000);
```

## 终端

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
```

```
function sayHi() {
    console.log(`Hi, my name is ${this.firstName}!`);
}

const person = {
    firstName: "Jane",
    lastName: "Doe"
};

sayHi.call(person);
```

```
$ node index.js
Hi, my name is Jane!
$
```

```
function sayHi() {
    console.log(`Hi, my name is ${this.firstName}!`);
}

const person = {
    firstName: "Jane",
    lastName: "Doe"
};

sayHi.apply(person);
```

```
$ node index.js
Hi, my name is Jane!
$ node index.js
Hi, my name is Jane!
$
```

```
const numbers = [10, 20, 30, 40, 50];

const slice1 = numbers.slice(1, 4);

const slice2 = numbers.slice.call(numbers, 1, 4);

const slice3 = numbers.slice.apply(numbers, [1, 4]);

console.log(slice1);

console.log(slice2);

console.log(slice3);

$ node index.js
[ 20, 30, 40 ]
[ 20, 30, 40 ]
[ 20, 30, 40 ]
$
```

```
const numbers = [10, 20, 30, 40, 50];

const slice1 = numbers.slice(1, 4);

const slice2 = numbers.slice.call(numbers, 1, 4);

const slice3 = numbers.slice.apply(numbers, [1, 4]);

console.log(slice1);

console.log(slice2);

console.log(slice3);

// (c)all => (c)omma

// (a)pply => (a)rray

$ node index.js
[ 20, 30, 40 ]
[ 20, 30, 40 ]
[ 20, 30, 40 ]
$
```

```
function func() {
    console.log(this === global);
}

func.call(null);

func.call(undefined);

func.apply(null);

func.apply(undefined);
```

```
$ node index.js
true
true
true
true
```

```
"use strict";

function func() {
    console.log(this === global);
}

func.call(null);

func.call(undefined);

func.apply(null);

func.apply(undefined);
```

```
$ node index.js
true
true
true
true
$ node index.js
false
false
false
false
$
```

```
const person = {
  firstName: "John",
  sayHi() {
    console.log(`Hi, my name is ${this.firstName}!`);
  }
};

setTimeout(person.sayHi, 1000);
```

```
$ node index.js
Hi, my name is undefined!
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

setTimeout(person.sayHi.bind(person), 1000);
```

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is John!
$
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

const greet = person.sayHi.bind(person);

greet();
```

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
$
```

```
const person = {
    firstName: "John",
    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
};

const greet = person.sayHi.bind(person);

const otherPerson = {
    firstName: "Jane"
};

greet.call(otherPerson);
```

```
$ node index.js
Hi, my name is undefined!
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
$
```

```
Function.prototype.bind = function(thisArg, ...fixedArgs) {
    const func = this;
    return function(...args) {
        return func.apply(thisArg, [...fixedArgs, ...args]);
    };
};
```

```
$
```

```
const outerThis = this;
const func = () => {
    console.log(this === outerThis);
};

func();
```

```
$ node index.js
true
$
```

```
const outerThis = this;
const func = () => {
    console.log(this === outerThis);
};

func();
func.call(null);
func.apply(undefined);
func.bind({})();
```

```
$ node index.js
true
$ node index.js
true
true
true
true
$ 
```

```
const outerThis = this;
const func = () => {
    console.log(this === outerThis);
};

new func();
```

```
true
$ node index.js
/Users/marius/Desktop/this/index.js:7
new func();
^
TypeError: func is not a constructor
    at Object.<anonymous> (/Users/marius/Desktop/this/index.js:7:1)
    at Module._compile (module.js:635:30)
    at Object.Module._extensions..js (module.js:646:10)
    at Module.load (module.js:554:32)
    at tryModuleLoad (module.js:497:12)
    at Function.Module._load (module.js:489:3)
    at Function.Module.runMain (module.js:676:10)
    at startup (bootstrap_node.js:187:16)
    at bootstrap_node.js:608:3
```

```
const counter = {
    count: 0,
    incrementPeriodically() {
        setInterval(function() {
            console.log(++this.count);
        }, 1000);
    }
};

counter.incrementPeriodically();
```

```
$ node index.js
NaN
NaN
NaN
NaN
NaN
NaN
NaN
NaN
NaN
NaN
```

```
const counter = {
    count: 0,
    incrementPeriodically() {
        setInterval(() => {
            console.log(++this.count);
        }, 1000);
    }
};

counter.incrementPeriodically();
```

```
$ node index.js
1
2
3
^C
$
```

```
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
}

const person = new Person("John", "Doe");
person.sayHi();
```

```
$ node index.js
Hi, my name is John!
```

```
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
console.log(`Hi, my name is ${this.firstName}!`);
```

```
TypeError: Cannot read property 'firstName' of undefined
    at sayHi (/Users/marius/Desktop/this/index.js:8:44)
    at Object.<anonymous> (/Users/marius/Desktop/this/index.js:14:1)
    at Module._compile (module.js:635:30)
    at Object.Module._extensions..js (module.js:646:10)
    at Module.load (module.js:554:32)
    at tryModuleLoad (module.js:497:12)
    at Function.Module._load (module.js:489:3)
    at Function.Module.runMain (module.js:676:10)
    at startup (bootstrap_node.js:187:16)
    at bootstrap_node.js:608:3
```

```
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi.bind(person);
greet();
```

```
$ node index.js
Hi, my name is John!
$
```

```
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.sayHi = this.sayHi.bind(this);
    }

    sayHi() {
        console.log(`Hi, my name is ${this.firstName}!`);
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
```

```
$ node index.js
Hi, my name is John!
$ node index.js
Hi, my name is John!
```

```
class Person {
    sayHi = () => {
        console.log(`Hi, my name is ${this.firstName}!`);
    };
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
```

```
$ npm run babel
class Person {
    constructor(firstName, lastName) {
        this.sayHi = () => {
            console.log(`Hi, my name is ${this.firstName}!`);
        };
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
$
```

```
class Person {
    sayHi = () => {
        console.log(`Hi, my name is ${this.firstName}!`);
    };
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
```

```
$ npm run babel
class Person {
    constructor(firstName, lastName) {
        this.sayHi = () => {
            console.log(`Hi, my name is ${this.firstName}!`);
        };
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const person = new Person("John", "Doe");
const greet = person.sayHi;
greet();
```

```
$ npm run babel | node
Hi, my name is John!
```

请不要投票给AKP。我会出版更多书籍。
