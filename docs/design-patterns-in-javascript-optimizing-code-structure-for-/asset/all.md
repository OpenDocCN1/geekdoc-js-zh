![](image_rsrc294.jpg)

Design Patterns in JavaScript

Optimizing code structure for robust and scalable JS applications.

By Hernando Abella

Thank you for trusting our publishing house. If you can evaluate our work and give us a comment on amazon, we will appreciate it very much!

This book may not be copied or printed without the permission of the author.

Copyright 2023 Aluna Publishing House

Contents

[Introduction](#part0001.xhtml_a27Z)

[What are Design Patterns?](#part0001.xhtml_a280)

[Types of Design Patterns](#part0001.xhtml_a281)

[Creational Design Patterns](#part0001.xhtml_a282)

[Factory Method](#part0001.xhtml_a283)

[Abstract Factory](#part0001.xhtml_a284)

[Builder](#part0001.xhtml_a285)

[Prototype](#part0001.xhtml_a286)

[Singleton](#part0001.xhtml_a287)

[Structural Design Patterns](#part0001.xhtml_a288)

[Adapter](#part0001.xhtml_a289)

[Bridge](#part0001.xhtml_a28A)

[Composite](#part0001.xhtml_a28B)

[Decorator](#part0001.xhtml_a28C)

[Facade](#part0001.xhtml_a28D)

[Flyweight](#part0001.xhtml_a28E)

[Proxy](#part0001.xhtml_a28F)

[Behavioral Design Patterns](#part0001.xhtml_a28G)

[Chain of Responsability](#part0001.xhtml_a28H)

[Command](#part0001.xhtml_a28J)

[Iterator](#part0001.xhtml_a28K)

[Mediator](#part0001.xhtml_a28M)

[Memento](#part0001.xhtml_a28N)

[Observer](#part0001.xhtml_a28P)

[Visitor](#part0001.xhtml_a28R)

[Strategy](#part0001.xhtml_a28S)

[State](#part0001.xhtml_a28T)

[Template Method](#part0001.xhtml_a28U)

# Introduction

Immerse yourself in the world of design patterns in JavaScript with this comprehensive guide that explores the practical application of the most relevant patterns. From the module pattern to the observer pattern, each section of this guide is carefully crafted to help you tackle development challenges with confidence and clarity. Designed for both beginners and experienced developers, this guide will provide you with the necessary tools to effectively understand and apply design patterns, thus elevating the quality and sustainability of your projects in JavaScript.

# What are Design Patterns?

Design patterns are proven and robust solutions for addressing common problems in software design and other contexts related to interaction and interfaces. These techniques provide structured and effective approaches to solving recurring challenges, promoting efficiency, reusability, and clarity in software development. 

A design pattern is considered a mature and consolidated solution for a specific design problem. To earn the recognition of being a pattern, it must exhibit certain key characteristics. Firstly, it must have demonstrated its effectiveness in solving similar problems in previous situations. Additionally, a pattern should be highly reusable, meaning it is applicable in various contexts and design challenges. 

# Types of Design Patterns

There are three main categories of design patterns, each focusing on a particular dimension of software design: 

Creational Patterns: These patterns center around how class instances and objects are created. They offer flexible solutions for object creation in various scenarios. 

Structural Patterns: Structural patterns deal with the composition of classes and objects to form larger structures. They facilitate the creation of efficient and flexible relationships between parts of the system. 

Behavioral Patterns: These patterns focus on the interaction between objects and how they communicate with each other. They help define workflows and collaborative behaviors. 

# Creational Design Patterns

Creational design patterns focus on how objects are created, providing solutions for instantiating objects appropriately for the situation. They address design and complexity problems that can arise when creating objects in the most basic form. These patterns solve these problems by controlling the object creation in some way. 

Below are the most common creational design patterns in JavaScript: 

Factory Method: Provides an interface for creating objects, allowing subclasses to alter the type of objects that will be created. It's useful when flexible and adaptable creation logic is needed. 

Abstract Factory: Provides an interface for creating families of related or dependent objects without specifying their concrete classes. This promotes the creation of consistent and compatible objects. 

Builder: Is used to construct an object step by step. It allows the creation of complex objects by specifying their type and content incrementally. 

Prototype: Focuses on creating new objects by copying an existing object, called a prototype. It's useful when creating an object is more efficient by duplicating an existing object rather than building it from scratch. 

Singleton: Ensures that a class has a single instance and provides a global point of access to that instance. It is used when a single instance of a class needs to coordinate actions throughout the system.  

# Factory Method

The Factory Method design pattern is a software design technique that relies on creating objects of a specific subtype through a common interface. This pattern is achieved by using an abstract creator class that contains both concrete and abstract methods. The concrete methods handle object creation, while the abstract methods are implemented by concrete subclasses. Depending on the subclass used, specific behavior is obtained. 

Example: To better understand the Factory Method, let's consider a concrete example related to creating points in a two-dimensional plane. Imagine that we are developing an application that needs to work with points in Cartesian and polar coordinates. 

First, we create a class called Point that represents a point in the plane. This class has a constructor that takes the x and y coordinates and a toString() method that returns a readable representation of the point in the format (x, y). 

Step 1: Definition of the Point class representing a point in the plane: 

// Point class representing a point in the plane 

class Point {

constructor(x, y) {

this.x = x;

this.y = y;

}

// Method to obtain a readable representation of the point 

toString() {

return `(${this.x}, ${this.y})`;

}

}

In this step, we have created the Point class with a constructor that takes the x and y coordinates and a toString() method to obtain a readable representation of the point. 

Step 2: Implementation of the Factory Method in the PointFactory class: 

// PointFactory class implementing the Factory Method 

class PointFactory {

// Method to create a point in Cartesian coordinates 

static createCartesianPoint(x, y) {

return new Point(x, y);

}

// Method to create a point in polar coordinates 

static createPolarPoint(rho, theta) {

return new Point(rho * Math.cos(theta), rho * Math.sin(theta));

}

}

In this step, we have created the PointFactory class that implements the Factory Method. This class contains two static methods: createCartesianPoint and createPolarPoint. The first one creates a point in Cartesian coordinates, and the second one creates a point in polar coordinates. 

Step 3: Example of using the Factory Method: 

// Example of using the Factory Method 

const cartesianPoint = PointFactory.createCartesianPoint(5, 6); 

const polarPoint = PointFactory.createPolarPoint(5, Math.PI / 2);

In this step, we have created two points using the PointFactory. One is created in Cartesian coordinates using createCartesianPoint, and the other is created in polar coordinates using createPolarPoint. 

Step 4: Printing the created points: 

// Printing the created points 

console.log("Cartesian Point:", cartesianPoint.toString()); // Cartesian Point: (5, 6) 

console.log("Polar Point:", polarPoint.toString()); // Polar Point: (6.123233995736766e-17, 5)

In this final step, we have printed the created points to verify the result. 

Final Code:

// Point class representing a point in the plane 

class Point {

constructor(x, y) {

this.x = x;

this.y = y;

}

// Method to obtain a readable representation of the point 

toString() {

return `(${this.x}, ${this.y})`;

}

}

// PointFactory class implementing the Factory Method 

class PointFactory {

// Method to create a point in Cartesian coordinates 

static createCartesianPoint(x, y) {

return new Point(x, y);

}

// Method to create a point in polar coordinates 

static createPolarPoint(rho, theta) {

return new Point(rho * Math.cos(theta), rho * Math.sin(theta));

}

}

// Example of using the Factory Method 

const cartesianPoint = PointFactory.createCartesianPoint(5, 6); 

const polarPoint = PointFactory.createPolarPoint(5, Math.PI / 2); 

// Printing the created points 

console.log("Cartesian Point:", cartesianPoint.toString()); // Cartesian Point: (5, 6) 

console.log("Polar Point:", polarPoint.toString()); // Polar Point: (6.123233995736766e-17, 5)

# Abstract Factory

In software design, the Abstract Factory design pattern is a technique used to create families or groups of related objects without specifying their concrete classes. This pattern provides a way to encapsulate a set of individual factories that share a common theme without needing to know the details of the exact classes of the objects that will be created. This promotes consistent and modular object creation, making code management and extension easier. 

Example: To better understand the Abstract Factory pattern, let's consider an example related to preparing beverages, such as tea and coffee. 

Step 1: We define base classes and subclasses to represent beverages, in this case, Beverage, Tea, and Coffee. 

class Beverage {

consume() {

// Abstract method, to be implemented in subclasses

}

}

class Tea extends Beverage { 

consume() {

console.log('This is Tea');

}

}

class Coffee extends Beverage { 

consume() {

console.log('This is Coffee');

}

}

Step 2: We define the base factory class (BeverageFactory) and factory subclasses (TeaFactory and CoffeeFactory) that will be used to create specific beverages. 

class BeverageFactory {

prepare(amount) {

// Abstract method, to be implemented in subclasses

}

}

class TeaFactory extends BeverageFactory { 

makeTea() {

console.log('Tea is prepared');

return new Tea();

}

}

class CoffeeFactory extends BeverageFactory { 

makeCoffee() {

console.log('Coffee is prepared');

return new Coffee();

}

}

Step 3: In this step, we create an instance of the tea factory (teaBeverageFactory), use it to create a tea beverage (tea), and finally, consume the tea beverage, which produces the expected console output. 

let teaBeverageFactory = new TeaFactory(); // Create a tea factory 

let tea = teaBeverageFactory.makeTea(); // Use the factory to create a tea beverage 

tea.consume(); // Consume the tea beverage 

// Expected Output:

// Tea is prepared 

// This is Tea 

Final Code:

// Definition of base classes and subclasses 

class Beverage {

consume() {

// Abstract method, to be implemented in subclasses

}

}

class Tea extends Beverage { 

consume() {

console.log('This is Tea');

}

}

class Coffee extends Beverage { 

consume() {

console.log('This is Coffee');

}

}

// Definition of the base factory class and factory subclasses 

class BeverageFactory {

prepare(amount) {

// Abstract method, to be implemented in subclasses

}

}   

class TeaFactory extends BeverageFactory { 

makeTea() {

console.log('Tea is prepared');

return new Tea();

}

}

class CoffeeFactory extends BeverageFactory { 

makeCoffee() {

console.log('Coffee is prepared');

return new Coffee();

}

}

// Example of usage 

let teaBeverageFactory = new TeaFactory(); // Create a tea factory 

let tea = teaBeverageFactory.makeTea(); // Use the factory to create a tea beverage 

tea.consume(); // Consume the tea beverage 

// Expected Output:

// Tea is prepared 

// This is Tea 

# Builder

Builds complex objects from simple objects. 

The constructor pattern is a design pattern designed to provide a flexible solution to various object creation problems in object-oriented programming. 

Example: Let's use an example of a Person class to store information about a person. 

Step 1\. Definition of the Person Class: In this step, we define the Person class, which is the class we want to build in a structured way. The Person class has several properties like addressStreet, postalCode, city, companyName, position, and annualIncome, which store information about a person. It also has a toString() method that returns a readable string representation of the person's information.

class Person {

constructor() {

this.addressStreet = this.postalCode = this.city = "";

this.companyName = this.position = "";

this.annualIncome = 0;

}

toString() {

return (

`Person lives at

${this.addressStreet}, ${this.city}, ${this.postalCode}

and works at ${this.companyName} as

${this.position} earning ${this.annualIncome}`

);

}

}

In this step, we have created the Person class with a constructor that initializes the properties and a toString() method to obtain a readable representation of the person. 

Step 2. Creating Constructors: In this step, we create three related constructors: PersonBuilder, WorkPersonBuilder, and AddressPersonBuilder.

PersonBuilder: This is the main constructor used to build Person objects. It has two methods, lives and works, to specify the person's address and job. The build() method finalizes the construction and returns the built Person object.

WorkPersonBuilder: Extends PersonBuilder and is used to specify the person's job. It has methods like at, asA, and earning to define the company name, position, and annual income of the person.

AddressPersonBuilder: Also extends PersonBuilder and is used to specify the person's address. It has methods like at, withPostcode, and in to define the address, postal code, and city.

class PersonBuilder {

constructor(person = new Person()) {

this.person = person;

}

get lives() {

return new AddressPersonBuilder(this.person);

}

get works() {

return new WorkPersonBuilder(this.person);

}

build() {

return this.person;

}

}

class WorkPersonBuilder extends PersonBuilder {

constructor(person) {

super(person);

}

at(companyName) {

this.person.companyName = companyName;

return this;

}

asA(position) {

this.person.position = position;

return this;

}

earning(annualIncome) {

this.person.annualIncome = annualIncome;

return this;

}

}

class AddressPersonBuilder extends PersonBuilder {

constructor(person) {

super(person);

}

at(addressStreet) {

this.person.addressStreet = addressStreet;

return this;

}

withPostcode(postalCode) {

this.person.postalCode = postalCode;

return this;

}

in(city) {

this.person.city = city;

return this;

}

}

Step 3\. Using the Constructor: In this step, we create an instance of PersonBuilder called personBuilder. Then, we use a method chain to build a Person instance in a structured way.

let personBuilder = new PersonBuilder();

let person = personBuilder.lives

.at("123 Main Street")

.in("New York")

.withPostcode("10001")

.works.at("ABC Inc.")

.asA("Engineer")

.earning(80000)

.build();

Step 4\. Result and Output: Finally, we can print the information of the built person using the toString() method of the Person class.

console.log(person.toString());

The expected output will be a string representation of the person's information, including details of address and job:

Person lives at 123 Main Street, New York, 10001 and works at ABC Inc. as Engineer earning 80000

Final Code:

// Definition of the Person class to store personal and job-related information

class Person {

constructor() {

this.addressStreet = this.postalCode = this.city = "";

this.companyName = this.position = "";

this.annualIncome = 0;

}

toString() {

return (

`Person lives at

${this.addressStreet}, ${this.city}, ${this.postalCode}

and works at ${this.companyName} as

${this.position} earning ${this.annualIncome}`

);

}

}

// Base class PersonBuilder to build Person objects

class PersonBuilder {

constructor(person = new Person()) {

this.person = person;

}

get lives() {

return new AddressPersonBuilder(this.person);

}

get works() {

return new WorkPersonBuilder(this.person);

}

build() {

return this.person;

}

}

// Constructor for Person's job details

class WorkPersonBuilder extends PersonBuilder {

constructor(person) {

super(person);

}

at(companyName) {

this.person.companyName = companyName;

return this;

}

asA(position) {

this.person.position = position;

return this;

}

earning(annualIncome) {

this.person.annualIncome = annualIncome;

return this;

}

}

// Constructor for Person's address details

class AddressPersonBuilder extends PersonBuilder {

constructor(person) {

super(person);

}

at(addressStreet) {

this.person.addressStreet = addressStreet;

return this;

}

withPostcode(postalCode) {

this.person.postalCode = postalCode;

return this;

}

in(city) {

this.person.city = city;

return this;

}

}

// Using the constructor pattern to create a Person object in a structured way

let personBuilder = new PersonBuilder();

let person = personBuilder.lives

.at("123 Main Street")

.in("New York")

.withPostcode("10001")

.works.at("ABC Inc.")

.asA("Engineer")

.earning(80000)

.build();

// Printing the details of the created Person

console.log(person.toString());

/*

Expected Output:

Person lives at

123 Main Street, New York, 10001

and works at ABC Inc. as

Engineer earning 80000

*/

# Prototype

Creates new objects based on existing objects.

The prototype pattern is a creational design pattern in software development. It is used when the type of objects to create is determined by a prototype instance, which is cloned to produce new objects.

Example: We will use the example of a car.

Step 1: Definition of the Car Class (Prototype)

class Car {

constructor(name, model) {

this.name = name;

this.model = model;

}

// ... (Class methods)

}

Step 2: Method to set the car's name

// Method to set the car's name

setCarName(name) {

this.name = name;

console.log(`Car name adjusted to: ${this.name}`);

}

Step 3: Method to clone the car (create a copy)

// Method to clone the car (create a copy)

clone() {

// Create a new Car instance with the same attributes

return new Car(this.name, this.model);

}

Step 4: Using the Prototype Pattern

// Using the Prototype Pattern

const originalCar = new Car('Audi', 'A3');

// Clone the original car to create a new instance

const clonedCar = originalCar.clone();

clonedCar.setCarName('BMW');

Step 5: Verify that the cars are different

// Verify that the cars are different

console.log('Original Car:', originalCar.name, originalCar.model);

console.log('Cloned Car:', clonedCar.name, clonedCar.model);

This code demonstrates how to use the Prototype Pattern to create a copy of an existing object (originalCar) and adjust its attributes (name) without affecting the original object. In the end, it verifies that the two cars are different, confirming that the clone worked correctly.

Final Code:

// Definition of the Car Class (Prototype)

class Car {

constructor(name, model) {

this.name = name;

this.model = model;

}

// Method to set the car's name

setCarName(name) {

this.name = name;

console.log(`Car name adjusted to: ${this.name}`);

}

// Method to clone the car (create a copy)

clone() {

// Create a new Car instance with the same attributes

return new Car(this.name, this.model);

}

}

// Using the Prototype Pattern

const originalCar = new Car('Audi', 'A3');

// Clone the original car to create a new instance

const clonedCar = originalCar.clone();

clonedCar.setCarName('BMW');

// Verify that the cars are different

console.log('Original Car:', originalCar.name, originalCar.model);

console.log('Cloned Car:', clonedCar.name, clonedCar.model);

// Expected Output:

// Car name adjusted to: BMW

// Original Car: Audi A3

// Cloned Car: BMW A3

# Singleton

Ensures that there is only one object created for a particular class.

In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to a "single" instance. This is useful when you need exactly one object to coordinate actions throughout the system.

Example:

Step 1: Singleton Class Definition:

class Singleton {

constructor() {

// ...

}

// ...

}

Step 2: Check if an instance of the class already exists:

const instance = this.constructor.instance;

if (instance) {

return instance;

}

In this step, within the constructor of the Singleton class, we check if an instance of the class already exists using this.constructor.instance. If an instance exists, we return that instance instead of creating a new one.

Step 3: Create instances of the Singleton class:

let s1 = new Singleton();

let s2 = new Singleton();

In this step, we create two instances, s1 and s2, of the Singleton class.

Step 4: Check if s1 and s2 are the same instance:

console.log('Are they the same? ' + (s1 === s2));

Here, we check if s1 and s2 are the same instance using (s1 === s2) and display the result in the console.

Step 5: Call the say() method: In this final step, we call the say() method of the s1 instance, which will print "Saying..." to the console.

s1.say();

Final Code: In this last step, we call the say() method of the s1 instance, which will print "Saying..." to the console.

// Singleton class definition

class Singleton {

constructor() {

// Check if an instance of the class already exists

const instance = this.constructor.instance;

if (instance) {

// If it exists, return the existing instance

return instance;

}

// If no instance exists, store this as the unique instance

this.constructor.instance = this;

}

// Method to display a message

say() {

console.log('Saying...');

}

}

// Create instances of the Singleton class

let s1 = new Singleton();

let s2 = new Singleton();

// Check if s1 and s2 are the same instance

console.log('Are they the same? ' + (s1 === s2));

// Call the say() method of the s1 instance

s1.say();

// Expected Output:

// Are they the same? true

// Saying...

These creational patterns are valuable tools for addressing object creation problems efficiently and structurally in JavaScript projects. Each one has its specific purpose and application, making them essential resources in software design.

# Structural Design Patterns

Structural design patterns focus on the composition of classes and objects to form more complex structures. They use inheritance and interface composition to create efficient and flexible relationships between entities.

Below are the most common structural design patterns in JavaScript:

Adapter: Allows incompatible interfaces to work together. It converts the interface of one class into another that the client expects. It's useful when you need objects with different interfaces to collaborate.

Bridge: Separates an abstraction from its implementation, allowing them to evolve independently. It's useful when you want to avoid a permanent bond between an abstraction and its implementation.

Composite: Composes objects into tree structures to represent part-whole hierarchies. It allows treating individual objects and object compositions uniformly.

Decorator: Dynamically adds functionality to existing objects without modifying their structure. It's useful when you want to extend an object's functionality flexibly.

Facade: Provides a simplified interface for a set of interfaces in a subsystem. It makes using complex systems easier by providing a more user-friendly interface.

Flyweight: Minimizes memory or disk storage usage by sharing as much as possible with similar objects. It's useful when you need to manage a large number of objects with efficient resource usage.

Proxy: Provides a substitute or placeholder for another object to control access to it. It can be used to add additional functionality like access control or lazy loading.

# Adapter

Enables classes with incompatible interfaces to collaborate by adapting their own interface to fit around the existing class. This is particularly useful when we need objects with different interfaces to work together without altering their source code.

Example:

1\. Definition of Incompatible Interfaces: In this example, we have two calculator interfaces: Calculator1 (old) and Calculator2 (new).

class Calculator1 {

constructor() {

this.operations = function(value1, value2, operation) {

// Implementation of the old calculator

switch(operation) {

case 'sum':

return value1 + value2;

case 'subtract':

return value1 - value2;

}

};

}

}

class Calculator2 {

constructor() {

this.add = function(value1, value2) {

// Implementation of the new calculator

return value1 + value2;

};

this.subtract = function(value1, value2) {

// Implementation of the new calculator

return value1 - value2;

};

}

}

2\. Creating an Adapter: We create a CalcAdapter class that will act as an adapter between the two calculator interfaces. The adapter wraps the new interface (Calculator2) and provides methods for the required operations.

class CalcAdapter {

constructor() {

const cal2 = new Calculator2();

this.operations = function(value1, value2, operation) {

switch(operation) {

case 'sum':

return cal2.add(value1, value2);

case 'subtract':

return cal2.subtract(value1, value2);

}

};

}

}

3\. Using the Adapter: Now, we can use the CalcAdapter to perform operations on the new interface (Calculator2) without modifying its code. This makes transitioning from the old calculator to the new one easier.

// Create an instance of the adapter

const calcAdapter = new CalcAdapter();

// Use the adapter to perform a subtraction operation

console.log(calcAdapter.operations(10, 55, 'subtract'));

Final Code:

// Definition of the Old Calculator Class

class OldCalculator {

constructor() {

this.operations = function(value1, value2, operation) {

switch(operation) {

case 'add':

return value1 + value2;

case 'subtract':

return value1 - value2;

}

};

}

}

// Definition of the New Calculator Class

class NewCalculator {

constructor() {

this.add = function(value1, value2) {

return value1 + value2;

};

this.subtract = function(value1, value2) {

return value1 - value2;

};

}

}

// Definition of the Adapter Class

class CalculatorAdapter {

constructor() {

// Create an instance of the New Calculator

const newCalculator = new NewCalculator();

// Define the operations method that will use the New Calculator

this.operations = function(value1, value2, operation) {

switch(operation) {

case 'add':

return newCalculator.add(value1, value2);

case 'subtract':

return newCalculator.subtract(value1, value2);

}

};

}

}

// Create an instance of the Calculator Adapter

const calculatorAdapter = new CalculatorAdapter();

// Use the Calculator Adapter to perform a subtraction operation

console.log(calculatorAdapter.operations(10, 55, 'subtract')); // -45

console.log(calculatorAdapter.operations(10, 55, 'add')); // 65

# Bridge

The Bridge design pattern is used to separate the abstraction from the implementation, allowing both to evolve independently. In other words, the Bridge pattern is used when you want to avoid a tight connection between an abstract class and its concrete classes, enabling them to evolve independently without affecting each other.

Example:

In this example, we will create classes for rendering geometric shapes. We will use two renderer classes: VectorRenderer and RasterRenderer. Then, we will create an abstract class Shape and a Circle class that inherits from Shape. The key to the Bridge pattern is that Shape has a reference to a renderer and delegates the rendering task to the concrete renderer.

Step 1\. Definition of Renderer Classes: In this step, we create the VectorRenderer and RasterRenderer classes, representing different rendering methods.

class VectorRenderer {

renderCircle(radius) {

console.log(`Drawing a circle of radius ${radius}`);

}

}

class RasterRenderer {

renderCircle(radius) {

console.log(`Drawing pixels for circle of radius ${radius}`);

}

}

Step 2\. Definition of Abstract Class Shape: In this step, we create the abstract class Shape that will act as our abstraction. This class has a renderer attribute that is a reference to the renderer we will use to draw the shape.

class Shape {

constructor(renderer) {

this.renderer = renderer;

}

}

Step 3\. Definition of Circle Class: In this step, we create the Circle class that inherits from Shape. The Circle class has a radius attribute representing the circle's radius.

class Circle extends Shape {

constructor(renderer, radius) {

super(renderer);

this.radius = radius;

}

}

Step 4\. Implementation of the draw Method: In the Circle class, we implement the draw method. This method delegates the rendering task to the concrete renderer (VectorRenderer or RasterRenderer) through the this.renderer reference.

draw() {

this.renderer.renderCircle(this.radius);

}

Step 5\. Creating Instances of Renderers and Circle: In this step, we create instances of the renderer classes VectorRenderer and RasterRenderer. Then, we create an instance of Circle named circle and provide it with the vector renderer and a radius of 5.

let raster = new RasterRenderer();

let vector = new VectorRenderer();

let circle = new Circle(vector, 5);

Step 6\. Drawing the Circle and Changing Its Size: We call the draw method on the circle instance, resulting in the printing of the corresponding message for the vector renderer. Then, we change the size of the circle by calling the resize method, doubling its radius.

circle.draw();

circle.resize(2);

Step 7\. Drawing the Circle After Size Change: We call the draw method again on the circle instance, resulting in the updated message after the size change.

circle.draw();

Final Code:

// Definition of Renderer Classes

class VectorRenderer {

renderCircle(radius) {

console.log(`Drawing a circle of radius ${radius}`);

}

}

class RasterRenderer {

renderCircle(radius) {

console.log(`Drawing pixels for circle of radius ${radius}`);

}

}

// Definition of the Abstract Class `Shape`

class Shape {

constructor(renderer) {

this.renderer = renderer;

}

}

// Definition of the `Circle` Class

class Circle extends Shape {

constructor(renderer, radius) {

super(renderer);

this.radius = radius;

}

// Implementation of the `draw` Method

draw() {

this.renderer.renderCircle(this.radius);

}

resize(factor) {

this.radius *= factor;

}

}

// Creating Instances of Renderers and Circle

let raster = new RasterRenderer();

let vector = new VectorRenderer();

let circle = new Circle(vector, 5);

// Drawing the Circle and Changing Its Size

circle.draw();

circle.resize(2);

// Drawing the Circle After Size Change

circle.draw();

// Expected Output:

// Drawing a circle of radius 5

// Drawing a circle of radius 10

# Composite

The Composite pattern is used to compose objects into tree structures to represent object hierarchies. This allows individual objects and compositions of objects to be treated in the same way, simplifying their manipulation.

Example:

1\. Class Definitions: In this example, we create two classes: Employee to represent individual employees and EmployeeGroup to represent groups of employees.

class Employee {

constructor(name, role) {

this.name = name;

this.role = role;

}

print() {

console.log("Name: " + this.name + ", Role: " + this.role);

}

}

class EmployeeGroup {

constructor(name, composite = []) {

this.name = name;

this.composite = composite;

}

print() {

console.log("Group: " + this.name);

this.composite.forEach(emp => {

emp.print();

})

}

}

2\. Creating Employees and Groups: We create instances of individual employees and then group them into an EmployeeGroup.

// Creating individual employees

let hernando = new Employee("Hernando", "Developer");

let albert = new Employee("Albert", "Developer");

// Creating an employee group and adding individual employees

let developerGroup = new EmployeeGroup("Developers", [hernando, albert]);

// Creating individual employees

let hernando = new Employee("Hernando", "Developer");

let albert = new Employee("Albert", "Developer");

// Creating an employee group and adding individual employees

let developerGroup = new EmployeeGroup("Developers", [hernando, albert]);

3\. Printing the Hierarchical Structure: We use the print() method to display the hierarchical structure, which includes both individual employees and employee groups.

// Print the hierarchical structure

developerGroup.print();

Final Code:

class Employee {

constructor(name, role) {

this.name = name;

this.role = role;

}

print() {

console.log(`Name: ${this.name}, Role: ${this.role}`);

}

}

class EmployeeGroup {

constructor(name, composite = []) {

this.name = name;

this.composite = composite;

}

print() {

console.log(`Group: ${this.name}`);

this.composite.forEach(emp => {

emp.print();

})

}

}

// Creating individual employees

let hernando = new Employee("Hernando", "Developer");

let albert = new Employee("Albert", "Developer");

// Creating an employee group and adding individual employees

let developerGroup = new EmployeeGroup("Developers", [hernando, albert]);

// Print the hierarchical structure

developerGroup.print();

// Expected Output:

// Group: Developers

// Name: Hernando, Role: Developer

// Name: Albert, Role: Developer

# Decorator

The decorator pattern allows dynamically adding or overriding behaviors to an individual object without affecting other objects of the same class. It is especially useful when you want to extend the capabilities of an object without creating subclasses.

Example:

1\. Class Definitions: In this example, we create the Form class as the base and Circle as a concrete shape we want to decorate. We also create a class called ColoredShape that acts as a decorator to add colors to shapes.

class Form {

constructor(color) {

this.color = color;

}

}

class Circle extends Form {

constructor(radius = 0) {

super();

this.radius = radius;

}

resize(factor) {

this.radius *= factor;

}

toString() {

return `A circle of radius ${this.radius}`;

}

}

class ColoredShape extends Form {

constructor(shape, color) {

super();

this.shape = shape;

this.color = color;

}

toString() {

return `${this.shape.toString()}, colored ${this.color}`;

}

}

2\. Using the Decorator: We create an instance of a base circle and then decorate that circle with a red color using the ColoredShape class.

// Create a base circle

let circle = new Circle(2);

console.log(circle.toString()); // Output: A circle of radius 2

// Decorate the circle with red color

let redCircle = new ColoredShape(circle, "red");

console.log(redCircle.toString()); // Output: A circle of radius 2, colored red

Final Code:

// Base class for all shapes

class Form {

constructor(color) {

this.color = color;

}

}

// Concrete class for a circle that inherits from Form

class Circle extends Form {

constructor(radius = 0) {

super();

this.radius = radius;

}

resize(factor) {

this.radius *= factor;

}

toString() {

return `A circle of radius ${this.radius}`;

}

}

// Decorator class that adds color to an existing shape

class ColoredShape extends Form {

constructor(shape, color) {

super();

this.shape = shape;

this.color = color;

}

toString() {

return `${this.shape.toString()}, colored ${this.color}`;

}

}

// Create a base circle

let circle = new Circle(2);

console.log(circle.toString()); // Output: A circle of radius 2

// Decorate the circle with red color

let redCircle = new ColoredShape(circle, "red");

console.log(redCircle.toString()); // Output: A circle of radius 2, colored red

# Facade

The facade pattern is a commonly used software design pattern in object-oriented programming. Analogous to a facade in architecture, a facade is an object that serves as a front-end interface that masks more complex underlying or structural code. It provides a simplified interface for accessing a set of related subsystems or classes, making interaction with the system easier without needing to know the internal details.

Example: In this example, we will simulate the operation of a computer using the facade pattern. The computer consists of various components such as CPU, memory, and hard drive. The ComputerFacade will simplify the interaction with these components.

We define classes for computer components: CPU, Memory, and HardDrive. These classes have methods to perform various operations, such as freezing the CPU, loading data into memory, and reading from the hard drive.

class CPU {

freeze() { console.log("CPU Frozen...") }

jump(position) { console.log("Jump to position " + position) }

execute() { console.log("Execute CPU...") }

}

class Memory {

load(position, data) { console.log("Load data at position " + position + ": " + data) }

}

class HardDrive {

read(lba, size) { console.log("Read from LBA " + lba + " with size " + size) }

}

We create the ComputerFacade, which provides a simplified interface for interacting with computer components. In the start() method, components are used coherently and mask complex details.

class ComputerFacade {

constructor() {

this.processor = new CPU();

this.ram = new Memory();

this.hdd = new HardDrive();

}

start() {

this.processor.freeze();

this.ram.load(this.BOOT_ADDRESS, this.hdd.read(this.BOOT_SECTOR, this.SECTOR_SIZE));

this.processor.jump(this.BOOT_ADDRESS);

this.processor.execute();

}

}

Finally, we create an instance of ComputerFacade and use its start() method to simulate the computer's booting process.

let computer = new ComputerFacade();

computer.start();

Final Code:

// Definition of the CPU class representing the central processing unit.

class CPU {

freeze() { console.log("CPU Frozen...") } // Method to freeze the CPU.

jump(position) { console.log("Jump to position " + position) } // Method to jump to a specific position.

execute() { console.log("Execute CPU...") } // Method to execute the CPU.

}

// Definition of the Memory class representing the computer's memory.

class Memory {

load(position, data) { console.log("Load data at position " + position + ": " + data) } // Method to load data into memory.

}

// Definition of the HardDrive class representing the computer's hard drive.

class HardDrive {

read(lba, size) { console.log("Read from LBA " + lba + " with size " + size) } // Method to read from the hard drive.

}

// Definition of the ComputerFacade class that acts as a facade to interact with computer components.

class ComputerFacade {

constructor() {

this.processor = new CPU(); // Create an instance of CPU.

this.ram = new Memory(); // Create an instance of Memory.

this.hdd = new HardDrive(); // Create an instance of Hard Drive.

}

start() {

this.processor.freeze(); // Freeze the CPU.

this.ram.load(this.BOOT_ADDRESS, this.hdd.read(this.BOOT_SECTOR, this.SECTOR_SIZE)); // Load data into memory from the hard drive.

this.processor.jump(this.BOOT_ADDRESS); // Jump to the start address.

this.processor.execute(); // Execute the CPU.

}

}

// Create an instance of ComputerFacade and use it to simulate the computer's boot process.

let computer = new ComputerFacade();

computer.start();

// Expected output:

// CPU Frozen...

// Load data at position BOOT_ADDRESS: Read from LBA BOOT_SECTOR with size SECTOR_SIZE

// Jump to position BOOT_ADDRESS

// Execute CPU...

# Flyweight

The Flyweight pattern is used to minimize memory usage when creating similar objects by sharing as much data as possible among them. This means that instead of creating multiple instances of objects with identical data, a shared instance is used to represent that common data. This significantly reduces the amount of memory used, especially when working with large quantities of similar objects.

Example:

Step 1\. Definition of User and User2 Classes: In this step, we define two classes: User and User2\. The first represents a simple user with a full name, while the second implements the Flyweight pattern to reduce memory usage by sharing similar full names.

// Definition of the User class

class User {

constructor(fullName) {

this.fullName = fullName;

}

}

// Definition of the User2 class that implements the Flyweight pattern

class User2 {

constructor(fullName) {

let getOrAdd = function(s) {

let idx = User2.strings.indexOf(s);

if (idx !== -1) return idx;

else {

User2.strings.push(s);

return User2.strings.length - 1;

}

};

this.names = fullName.split(' ').map(getOrAdd);

}

}

User2.strings = [];

Step 2\. Auxiliary Functions: In this step, we create two auxiliary functions: getRandomInteger to obtain random integers and getRandomText to generate random text strings.

// Auxiliary functions

function getRandomInteger(max) {

return Math.floor(Math.random() * Math.floor(max));

}

function getRandomText() {

let result = [];

for (let x = 0; x < 10; ++x)

result.push(String.fromCharCode(65 + getRandomInteger(26)));

return result.join('');

}

Step 3\. Creating Random Names: In this step, we create two arrays, names and lastNames, which contain randomly generated names and last names that will be used to create users.

// Creating Random Names

let names = lastNames = [];

for (let i = 0; i < 100; ++i) {

names.push(getRandomText());

lastNames.push(getRandomText());

}

Step 4\. Creating Users: In this step, we create two arrays, users and users2, which will contain the created users. We iterate through the names and last names arrays to create 10,000 users both without the Flyweight pattern and with it.

let users = [];

let users2 = [];

// Creating Users

for (let name of names) {

for (let lastName of lastNames) {

users.push(new User(`${name} ${lastName}`));

users2.push(new User2(`${name} ${lastName}`));

}

}

Step 5\. Memory Usage Comparison: In this step, we compare the memory usage between users without the Flyweight pattern and users with it using JSON.stringify. We print the results to the console.

// Memory Usage Comparison

console.log(`10,000 users occupy approximately ${JSON.stringify(users).length} characters`);

let users2Length = [users2, User2.strings].map(x => JSON.stringify(x).length).reduce((x, y) => x + y);

console.log(`10,000 users with Flyweight occupy ~${users2Length} characters`);

Final Code:

// Definition of the User class

class User {

constructor(fullName) {

this.fullName = fullName;

}

}

// Definition of the User2 class that implements the Flyweight pattern

class User2 {

constructor(fullName) {

let getOrAdd = function(s) {

let idx = User2.strings.indexOf(s);

if (idx !== -1) return idx;

else {

User2.strings.push(s);

return User2.strings.length - 1;

}

};

this.names = fullName.split(' ').map(getOrAdd);

}

}

User2.strings = [];

// Auxiliary functions

function getRandomInteger(max) {

return Math.floor(Math.random() * Math.floor(max));

}

function getRandomText() {

let result = [];

for (let x = 0; x < 10; ++x)

result.push(String.fromCharCode(65 + getRandomInteger(26)));

return result.join('');

}

// Creating Random Names

let names = lastNames = [];

for (let i = 0; i < 100; ++i) {

names.push(getRandomText());

lastNames.push(getRandomText());

}

let users = [];

let users2 = [];

// Creating Users

for (let name of names) {

for (let lastName of lastNames) {

users.push(new User(`${name} ${lastName}`));

users2.push(new User2(`${name} ${lastName}`));

}

}

// Memory Usage Comparison

console.log(`10,000 users occupy approximately ${JSON.stringify(users).length} characters`); // 10,000 users occupy approximately 1720001 characters

let users2Length = [users2, User2.strings].map(x => JSON.stringify(x).length).reduce((x, y) => x + y);

console.log(`10,000 users with Flyweight occupy ~${users2Length} characters`); // 10,000 users with Flyweight occupy ~838602 characters

# Proxy

The Proxy pattern allows one class to represent the functionality of another class, acting as an intermediary or "proxy" between the client and the real object. This can be useful for controlling access to the real object, performing additional operations before or after accessing the real object, or even replacing the real object entirely.

Example:

Let's imagine an example of a Proxy object called "Percentage" used to represent percentages. This Proxy allows manipulating percentage values and performing mathematical operations on them.

class Percentage {

constructor(percentage) {

this.percentage = percentage;

}

toString() {

return `${this.percentage}%`;

}

valueOf() {

return this.percentage / 100;

}

}

// Let's use the Percentage Proxy object

let percentageFive = new Percentage(5);

console.log(percentageFive.toString()); // Output: "5%"

console.log(`5% of 50 is ${50 * percentageFive}`); // Output: "5% of 50 is 2.5"

In this example, the "Percentage" acts as a proxy that allows representing percentage values and performing calculations with them. The Percentage Proxy makes it easy to manipulate percentage values and use them in mathematical operations.

# Behavioral Design Patterns

Behavioral design patterns focus on the communication and interaction between objects in a software system. These patterns identify common patterns of communication and collaboration between objects, increasing flexibility and efficiency in designing and implementing the behavior of a system.

Below are the most common behavioral design patterns in JavaScript:

Chain of Responsibility: Allows multiple objects to handle a request without the sender knowing which one will process it.

Command: Encapsulates a request as an object, allowing clients to parameterize objects with operations, queue requests, log requests, and support undoable operations.

Iterator: Provides a way to access elements of a collection sequentially without exposing its underlying representation.

Mediator: Defines an object that encapsulates how communication occurs between objects in a system, promoting loose coupling by preventing objects from explicitly referring to each other.

Memento: Allows capturing and externalizing an object's internal state so that the object can be restored to that state later.

Observer: Defines a one-to-many dependency between objects so that when one object changes its state, all its dependents are notified and updated automatically.

Visitor: Represents an operation to be performed on the elements of an object structure, allowing defining a new operation without changing the classes of the elements on which it operates.

Strategy: Defines a family of algorithms, encapsulates each one, and makes them interchangeable, allowing the algorithm to vary independently of clients that use it.

State: Allows an object to alter its behavior when its internal state changes, often implemented as a finite state machine.

Template Method: Defines the skeleton of an algorithm in an operation but allows subclasses to redefine parts of the algorithm without changing its structure.

# Chain of Responsability

Create a chain of objects. Starting from a point, it stops until a certain condition is met.

In object-oriented design, the Chain of Responsibility pattern is a design pattern consisting of a source of command objects and a series of processing objects.

Example:

Let's use an example of a game that has a creature. The creature will increase its defense and attack when it reaches a certain point. It will create a chain, and the attack and defense will increase and decrease.

Step 1\. Definition of Key Classes and the Chain of Responsibility Pattern: In this step, we define the main classes, including Creature and CreatureModifier, as well as specific modifier classes.

class Creature {

constructor(name, attack, defense) {

this.name = name;

this.attack = attack;

this.defense = defense;

}

toString() {

return `${this.name} (${this.attack} / ${this.defense})`;

}

}

class CreatureModifier {

constructor(creature) {

this.creature = creature;

this.next = null;

}

add(modifier) {

if (this.next) this.next.add(modifier);

else this.next = modifier;

}

handle() {

if (this.next) this.next.handle();

}

}

Step 2\. Implementation of Specific Modifiers: We create specific modifiers such as NoBonusesModifier, DoubleAttackModifier, and IncreaseDefenseModifier.

class NoBonusesModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

console.log("No bonuses for you!");

}

}

class DoubleAttackModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

console.log(`Doubling attack of ${this.creature.name}`);

this.creature.attack *= 2;

super.handle();

}

}

class IncreaseDefenseModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

if (this.creature.attack <= 2) {

console.log(`Increasing defense of ${this.creature.name}`);

this.creature.defense++;

}

super.handle();

}

}

Step 3\. Using the Chain of Responsibility Pattern: In this step, we create an instance of Creature, then create a chain of responsibility of modifiers and apply it to the creature.

let pikachu = new Creature("Pikachu", 1, 1);

console.log(pikachu.toString());

let root = new CreatureModifier(pikachu);

root.add(new NoBonusesModifier(pikachu));

root.add(new IncreaseDefenseModifier(pikachu));

root.handle();

console.log(pikachu.toString());

This final code combines all the steps and shows the expected output when executed.

Código final:

class Creature {

constructor(name, attack, defense) {

this.name = name;

this.attack = attack;

this.defense = defense;

}

toString() {

return `${this.name} (${this.attack} / ${this.defense})`;

}

}

class CreatureModifier {

constructor(creature) {

this.creature = creature;

this.next = null;

}

add(modifier) {

if (this.next) this.next.add(modifier);

else this.next = modifier;

}

handle() {

if (this.next) this.next.handle();

}

}

class NoBonusesModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

console.log("No bonuses for you!");

}

}

class DoubleAttackModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

console.log(`Doubling attack of ${this.creature.name}`);

this.creature.attack *= 2;

super.handle();

}

}

class IncreaseDefenseModifier extends CreatureModifier {

constructor(creature) {

super(creature);

}

handle() {

if (this.creature.attack <= 2) {

console.log(`Increasing defense of ${this.creature.name}`);

this.creature.defense++;

}

super.handle();

}

}

// Create a creature and show its initial state

let pikachu = new Creature("Pikachu", 1, 1);

console.log(pikachu.toString());

// Create a chain of responsibility and add modifiers

let root = new CreatureModifier(pikachu);

root.add(new NoBonusesModifier(pikachu));

root.add(new IncreaseDefenseModifier(pikachu));

// Apply the modifiers to the creature

root.handle();

// Show the final state of the creature after applying modifiers

console.log(pikachu.toString());

// Expected Output:

// Pikachu (1 / 1)

// Increasing defense of Pikachu

// Pikachu (1 / 2)

# Command

In object-oriented programming, the Command pattern is a behavioral design pattern in which an object is used to encapsulate all the information needed to perform an action or trigger an event at a later time. This information includes the method's name, the object that owns the method, and the method's parameter values.

Example:

We'll take a simple example of a bank account where we issue an order to deposit or withdraw a certain amount of money.

Step 1\. Definition of the BankAccount class: In this step, we define the BankAccount class, which represents a bank account with methods for depositing, withdrawing, and getting the balance.

class BankAccount {

constructor(balance = 0) {

this.balance = balance;

}

deposit(amount) {

this.balance += amount;

console.log(`${amount} deposited into the total balance ${this.balance}`);

}

withdraw(amount) {

if (this.balance - amount >= BankAccount.overdraftLimit) {

this.balance -= amount;

console.log(`${amount} withdrawn from the total balance.`);

} else {

console.log(`Insufficient funds to withdraw ${amount}`);

}

}

toString() {

return `Balance: ${this.balance}`;

}

}

BankAccount.overdraftLimit = -500;

Step 2\. Creating Commands: In this step, we create an enumeration Action to represent deposit and withdraw actions, and then define the BankAccountCommand class that encapsulates an action along with its amount.

let Action = Object.freeze({

deposit: 1,

withdraw: 2,

});

class BankAccountCommand {

constructor(account, action, amount) {

this.account = account;

this.action = action;

this.amount = amount;

}

execute() {

switch (this.action) {

case Action.deposit:

this.account.deposit(this.amount);

break;

case Action.withdraw:

this.account.withdraw(this.amount);

break;

}

}

undo() {

switch (this.action) {

case Action.deposit:

this.account.withdraw(this.amount); // Reversing a deposit is a withdrawal

break;

case Action.withdraw:

this.account.deposit(this.amount); // Reversing a withdrawal is a deposit

break;

}

}

}

Step 3\. Using the Command Pattern: In this step, we create an instance of BankAccount and a command to deposit and then undo that deposit.

let bankAccount = new BankAccount(100);

let cmd = new BankAccountCommand(bankAccount, Action.deposit, 50);

cmd.execute(); // Perform a deposit of 50

console.log(bankAccount.toString()); // Balance: 150

cmd.undo(); // Undo the deposit of 50

console.log(bankAccount.toString()); // Balance: 100

This code demonstrates how the Command pattern allows encapsulating requests as objects, making it easy to execute and undo actions.

Final Code:

class BankAccount {

constructor(balance = 0) {

this.balance = balance;

}

deposit(amount) {

this.balance += amount;

console.log(`${amount} deposited into the total balance ${this.balance}`);

}

withdraw(amount) {

if (this.balance - amount >= BankAccount.overdraftLimit) {

this.balance -= amount;

console.log(`${amount} withdrawn from the total balance.`);

} else {

console.log(`Insufficient funds to withdraw ${amount}`);

}

}

toString() {

return `Balance: ${this.balance}`;

}

}

BankAccount.overdraftLimit = -500;

let Action = Object.freeze({

deposit: 1,

withdraw: 2,

});

class BankAccountCommand {

constructor(account, action, amount) {

this.account = account;

this.action = action;

this.amount = amount;

}

execute() {

switch (this.action) {

case Action.deposit:

this.account.deposit(this.amount);

break;

case Action.withdraw:

this.account.withdraw(this.amount);

break;

}

}

undo() {

switch (this.action) {

case Action.deposit:

this.account.withdraw(this.amount); // Reversing a deposit is a withdrawal

break;

case Action.withdraw:

this.account.deposit(this.amount); // Reversing a withdrawal is a deposit

break;

}

}

}

let bankAccount = new BankAccount(100);

let cmd = new BankAccountCommand(bankAccount, Action.deposit, 50);

cmd.execute(); // Perform a deposit of 50

console.log(bankAccount.toString()); // Balance: 150

cmd.undo(); // Undo the deposit of 50

console.log(bankAccount.toString()); // Balance: 100

# Iterator

Iterator accesses the elements of an object without exposing its underlying representation.

In object-oriented programming, the iterator pattern is a design pattern where an iterator is used to traverse a container and access the elements of the container.

Definition of the 'Thing' Class: First, we define a class called 'Thing' that has two properties 'a' and 'b.'

Step 1: Define the 'Thing' class and its 'a' and 'b' properties.

class Thing {

constructor() {

this.a = 11;

this.b = 22;

}

// Rest of the code

}

Step 2: Implement the Symbol.iterator method to traverse the 'a' and 'b' properties of the 'Thing' class.

class Thing {

// ...

[Symbol.iterator]() {

let i = 0;

let self = this;

return {

next: function() {

return {

done: i > 1,

value: self[i++ === 0 ? 'a' : 'b']

};

}

};

}

// Rest of the code

}

Step 3: Implement the 'backwards' property to traverse the properties in reverse order.

class Thing {

// ...

get backwards() {

let i = 0;

let self = this;

return {

next: function() {

return {

done: i > 1,

value: self[i++ === 0 ? 'b' : 'a']

};

},

[Symbol.iterator]: function() { return this; }

};

}

// Rest of the code

}

class Thing {

// ...

get backwards() {

let i = 0;

let self = this;

return {

next: function() {

return {

done: i > 1,

value: self[i++ === 0 ? 'b' : 'a']

};

},

[Symbol.iterator]: function() { return this; }

};

}

// Rest of the code

}

Step 4: Create an array 'values' with numeric elements.

let values = [100, 200, 300];

Step 5: Use a 'for...in' loop to iterate over the 'values' array.

for (let i in values) {

console.log(`Element at position ${i} is ${values[i]}`);

}

Step 6: Use another 'for...in' loop to iterate over an object (not recommended).

for (let v in values) {

console.log(`The value is ${v}`);

}

Step 7: Create an instance of the 'Thing' class called 'thing'.

let thing = new Thing();

Step 8: Use a 'for...of' loop to iterate over the properties of 'thing.'.

console.log("Iterating over 'a' and 'b':");

for (let element of thing) {

console.log(`${element}`);

}

Step 9: Use another 'for...of' loop to iterate in reverse order.

console.log("Iterating in reverse order:");

for (let element of thing.backwards) {

console.log(`${element}`);

}

Final Code:

We will take the example of an array where we print the values of an array and then, using an iterator, print its values in reverse.

// Define a class called 'Thing'

class Thing {

constructor() {

this.a = 11; // Property 'a' with value 11

this.b = 22; // Property 'b' with value 22

}

// Define an iterator to traverse the elements 'a' and 'b' of this class

[Symbol.iterator]() {

let i = 0; // Initialize an index to keep control

let self = this; // Capture a reference to the current instance ('this')

return {

next: function() {

return {

done: i > 1, // Indicates if everything has been traversed (when 'i' is greater than 1)

value: self[i++ === 0 ? 'a' : 'b'] // Get the corresponding value ('a' or 'b')

};

}

};

}

// Get an iterator to traverse the elements in reverse order

get backwards() {

let i = 0; // Initialize an index to keep control

let self = this; // Capture a reference to the current instance ('this')

return {

next: function() {

return {

done: i > 1, // Indicates if everything has been traversed (when 'i' is greater than 1)

value: self[i++ === 0 ? 'b' : 'a'] // Get the corresponding value ('b' or 'a')

};

},

[Symbol.iterator]: function() { return this; } // Make the iterator iterable

};

}

}

let values = [100, 200, 300];

// Use a for...in loop to traverse an array (Note: not the recommended way for arrays)

for (let i in values) {

console.log(`Element at position ${i} is ${values[i]}`);

}

// Use a for...in loop to traverse an object (Note: not the recommended way for objects)

for (let v in values) {

console.log(`The value is ${v}`);

}

let thing = new Thing(); // Create an instance of the class 'Thing'

console.log("Iterating over 'a' and 'b':");

for (let element of thing) {

console.log(`${element}`);

}

console.log("Iterating in reverse order:");

for (let element of thing.backwards) {

console.log(`${element}`);

}

// Expected output:

// Element at position 0 is 100

// Element at position 1 is 200

// The value is 0

// The value is 1

// The value is 2

// Iterating over 'a' and 'b':

// 11

// 22

// Iterating in reverse order:

// 22

// 11

# Mediator

The mediator pattern adds a third-party object to control the interaction between two objects. It allows for flexible coupling between classes since it is the only class with detailed knowledge of its methods.

The mediator pattern defines an object that encapsulates how a set of objects interact. This pattern is considered a behavioral pattern due to the way it can alter the program's execution behavior. In object-oriented programming, programs often consist of many classes.

We will use an example of a person using a chat room. Here, a chat room acts as a mediator between two people communicating with each other.

Example:

Step 1. Definition of the Person class, which represents people in the chat room:

class Person {

constructor(name, chatRoom) {

this.name = name;         // Person's name

this.chatRoom = chatRoom; // Chat room they belong to

}

// Method to send a message in the chat room

say(message) {

this.chatRoom.sendMessage(this, message);

}

// Method to receive a message

receive(message) {

console.log(`${this.name} receives: ${message}`);

}

}

Step 2. Definition of the ChatRoom class, which acts as a mediator:

class ChatRoom {

constructor() {

this.people = []; // Stores people in the chat room

}

// Method to add a person to the chat room

joinPerson(person) {

this.people.push(person); // Add the person to the list

person.chatRoom = this;  // Set the person's chat room as this room

}

// Method to send a message to all people in the room

sendMessage(sender, message) {

for (const person of this.people) {

if (person !== sender) {

person.receive(`${sender.name}: ${message}`);

}

}

}

}

Step 3. Creation of a chat room (ChatRoom):

const chatRoom = new ChatRoom();

Step 4. Creation of people and joining them to the chat room:

const john = new Person("John", chatRoom);

const tony = new Person("Tony", chatRoom);

chatRoom.joinPerson(john);

chatRoom.joinPerson(tony);

Step 5. John sends a message in the chat room:

john.say("Hello, everyone!");

Step 6. Creation of a new person and joining them to the chat room:

const doe = new Person("Doe", chatRoom);

chatRoom.joinPerson(doe);

Step 7. Doe sends a message in the chat room:

doe.say("Hi, everyone!");

Whenever someone sends a message, the chat room takes care of distributing that message to all the other people in the room.

Final Code:

// Definition of the Person class, which represents people in the chat room

class Person {

constructor(name, chatRoom) {

this.name = name;         // Person's name

this.chatRoom = chatRoom; // Chat room they belong to

}

// Method to send a message in the chat room

say(message) {

this.chatRoom.sendMessage(this, message);

}

// Method to receive a message

receive(message) {

console.log(`${this.name} receives: ${message}`);

}

}

// Definition of the ChatRoom class, which acts as a mediator

class ChatRoom {

constructor() {

this.people = []; // Stores people in the chat room

}

// Method to add a person to the chat room

joinPerson(person) {

this.people.push(person); // Add the person to the list

person.chatRoom = this;  // Set the person's chat room as this room

}

// Method to send a message to all people in the room

sendMessage(sender, message) {

for (const person of this.people) {

if (person !== sender) {

person.receive(`${sender.name}: ${message}`);

}

}

}

}

// Creation of a chat room

const chatRoom = new ChatRoom();

// Creation of people and joining them to the chat room

const john = new Person("John", chatRoom);

const tony = new Person("Tony", chatRoom);

chatRoom.joinPerson(john);

chatRoom.joinPerson(tony);

// John sends a message in the chat room

john.say("Hello, everyone!");

// Creation of a new person and joining them to the chat room

const doe = new Person("Doe", chatRoom);

chatRoom.joinPerson(doe);

// Doe sends a message in the chat room

doe.say("Hi, everyone!");

# Memento

The Memento pattern allows restoring an object to its previous state.

The Memento pattern is a software design pattern that provides the capability to restore an object to a previous state. It is implemented using three objects: the originator, the caretaker, and the memento.

Example:

Let's take an example of a bank account in which we store our previous state and have the functionality to undo.

Step 1\. Definition of the Memento class:

class Memento {

constructor(balance) {

this.balance = balance;

}

}

In this step, we create the Memento class, which will be used to store the state of the bank account at a given moment.

Step 2\. Definition of the CuentaBanco class:

class BankAccount {

constructor(balance = 0) {

this.balance = balance;

}

deposit(amount) {

this.balance += amount;

return new Memento(this.balance);

}

restore(memento) {

this.balance = memento.balance;

}

toString() {

return `Balance: ${this.balance}`;

}

}

Here, we create the BankAccount class, which represents a bank account with the ability to make deposits, save states in the form of Mementos, and restore the previous state.

Step 3\. Definition of the Caretaker class:

class Caretaker {

constructor() {

this.mementos = [];

}

addMemento(memento) {

this.mementos.push(memento);

}

getMemento(index) {

return this.mementos[index];

}

}

The CareTaker class is responsible for storing the Mementos in a list so that previous states can be restored when needed.

Step 4\. Using the Memento pattern:

// Create an instance of BankAccount

const bankAccount = new BankAccount(100);

const caretaker = new Caretaker();

// Make deposits and save states in Mementos

caretaker.addMemento(bankAccount.deposit(50));

console.log(bankAccount.toString()); // Balance: 150

caretaker.addMemento(bankAccount.deposit(25));

console.log(bankAccount.toString()); // Balance: 175

// Restore the previous state

bankAccount.restore(caretaker.getMemento(0));

console.log(bankAccount.toString()); // Balance: 150

bankAccount.restore(caretaker.getMemento(1));

console.log(bankAccount.toString()); // Balance: 175

In this step, we create an instance of BankAcccount and a CareTaker. Then, we make deposits into the bank account and save states as Mementos using the CareTaker. Finally, we restore previous states of the bank account using the Mementos and verify the resulting balances.

Final Code:

class Memento {

constructor(balance) {

this.balance = balance;

}

}

class BankAccount {

constructor(balance = 0) {

this.balance = balance;

}

deposit(amount) {

this.balance += amount;

return new Memento(this.balance);

}

restore(memento) {

this.balance = memento.balance;

}

toString() {

return `Balance: ${this.balance}`;

}

}

class Caretaker {

constructor() {

this.mementos = [];

}

addMemento(memento) {

this.mementos.push(memento);

}

getMemento(index) {

return this.mementos[index];

}

}

// Create an instance of BankAccount

const bankAccount = new BankAccount(100);

const caretaker = new Caretaker();

// Make deposits and save states in Mementos

caretaker.addMemento(bankAccount.deposit(50));

console.log(bankAccount.toString()); // Balance: 150

caretaker.addMemento(bankAccount.deposit(25));

console.log(bankAccount.toString()); // Balance: 175

// Restore the previous state

bankAccount.restore(caretaker.getMemento(0));

console.log(bankAccount.toString()); // Balance: 150

bankAccount.restore(caretaker.getMemento(1));

console.log(bankAccount.toString()); // Balance: 175

# Observer

Allows multiple observer objects to watch an event.

The Observer pattern is a software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and automatically notifies them of any state changes, usually by calling one of their methods.

Example:

Let's take an example of a person where if a person gets sick, it shows a notification.

Step 1\. Definition of classes and the Observer Pattern: In this step, we define three key classes: Event, GetSick, and Person. The Event class represents an observable event and contains the logic for subscribing, unsubscribing, and notifying observers.

The GetSick class is a specific event that contains information about the location where it occurs. The Person class is the observable subject that can "get sick" and notify observers when this happens.

// Event class representing an observable event

class Event {

constructor() {

this.handlers = new Map();

this.counter = 0;

}

// Method to subscribe a handler to the event and return a unique identifier

subscribe(handler) {

this.handlers.set(++this.counter, handler);

return this.counter;

}

// Method to unsubscribe from an event given an identifier

unsubscribe(index) {

this.handlers.delete(index);

}

// Method to notify all observers when the event occurs

fire(sender, args) {

this.handlers.forEach((handler, id) => handler(sender, args));

}

}

// GetSick class representing a specific event

class GetSick {

constructor(location) {

this.location = location;

}

}

// Person class that will be the observable subject

class Person {

constructor(location) {

this.location = location;

this.getSick = new Event(); // Create a "get sick" event

}

// Method to simulate the person getting sick and notify observers

catchCold() {

this.getSick.fire(this, new GetSick(this.location));

}

}

Step 2\. Using the Observer Pattern: In this step, we create an instance of Person and then subscribe an observer to the "get sick" event using the subscribe method of the Event class. We then simulate the person getting sick twice by calling the catchCold method. After that, we unsubscribe the observer using the unsubscribe method. Finally, we call the catchCold method again, but the unsubscribed observer no longer receives notifications.

This pattern allows multiple observers to watch an event (in this case, getting sick) without the Person class needing to know the details of who the observers are or how they react to the event.

// Create an instance of the person

let person = new Person("Route ABC");

// Subscribe an observer to the "get sick" event

let sub = person.getSick.subscribe((subject, event) => {

console.log(`A doctor has been called to ${event.location}`);

});

// The person gets sick twice

person.catchCold();

person.catchCold();

// Unsubscribe the observer

person.getSick.unsubscribe(sub);

// The person gets sick again, but the unsubscribed observer no longer receives the notification

person.catchCold();

Final Code:

// Definition of classes and the Observer Pattern

// Event class representing an observable event

class Event {

constructor() {

this.handlers = new Map();

this.counter = 0;

}

// Method to subscribe a handler to the event and return a unique identifier

subscribe(handler) {

this.handlers.set(++this.counter, handler);

return this.counter;

}

// Method to unsubscribe from an event given an identifier

unsubscribe(index) {

this.handlers.delete(index);

}

// Method to notify all observers when the event occurs

fire(sender, args) {

this.handlers.forEach((handler, id) => handler(sender, args));

}

}

// GetSick class representing a specific event

class GetSick {

constructor(location) {

this.location = location;

}

}

// Person class that will be the observable subject

class Person {

constructor(location) {

this.location = location;

this.getSick = new Event(); // Create a "get sick" event

}

// Method to simulate the person getting sick and notify observers

catchCold() {

this.getSick.fire(this, new GetSick(this.location));

}

}

// Using the Observer Pattern

// Create an instance of the person

let person = new Person("Route ABC");

// Subscribe an observer to the "get sick" event

let sub = person.getSick.subscribe((subject, event) => {

console.log(`A doctor has been called to ${event.location}`);

});

// The person gets sick twice

person.catchCold();

person.catchCold();

// Unsubscribe the observer

person.getSick.unsubscribe(sub);

// The person gets sick again, but the unsubscribed observer no longer receives the notification

person.catchCold();

# Visitor

Add operations to objects without having to modify them.

The visitor design pattern is a way to separate an algorithm from an object structure it operates on. A practical result of this separation is the ability to add new operations to existing object structures without modifying those structures.

Example:

Let's take an example of the NumericExpression class that gives us the result of the given expression.

1\. NumericExpression Class: This class represents a simple numeric expression with a value.

class NumericExpression {

constructor(value) {

this.value = value;

}

print(buffer) {

buffer.push(this.value.toString());

}

}

2\. SumExpression Class: This class represents a sum expression that takes two numeric expressions (left and right) and adds them.

class SumExpression {

constructor(left, right) {

this.left = left;

this.right = right;

}

print(buffer) {

buffer.push('(');

this.left.print(buffer);

buffer.push('+');

this.right.print(buffer);

buffer.push(')');

}

}

3\. Using the Visitor Pattern: Next, you create a composite expression that represents "5 + (1 + 9)" using instances of the NumericExpression and SumExpression classes.

let e = new SumExpression(

new NumericExpression(5),

new SumExpression(

new NumericExpression(1),

new NumericExpression(9)

)

);

Printing the Expression: Finally, you use the print() method to get a readable representation of the expression and store it in a buffer.

let buffer = [];

e.print(buffer);

console.log(buffer.join('')); // Output: (5+(1+9))

This example illustrates how the visitor design pattern allows you to add the printing operation to complex objects without having to modify their internal structure. This makes the code more flexible and extensible for future operations without affecting existing classes.

Final Code:

class NumericExpression {

constructor(value) {

this.value = value;

}

print(buffer) {

buffer.push(this.value.toString());

}

}

class SumExpression {

constructor(left, right) {

this.left = left;

this.right = right;

}

print(buffer) {

buffer.push('(');

this.left.print(buffer);

buffer.push('+');

this.right.print(buffer);

buffer.push(')');

}

}

// Creating a composite expression: 5 + (1 + 9)

let e = new SumExpression(

new NumericExpression(5),

new SumExpression(

new NumericExpression(1),

new NumericExpression(9)

)

);

let buffer = [];

e.print(buffer);

console.log(buffer.join('')); // Expected Output: (5+(1+9))

The expected output is (5+(1+9)), which is the representation of the "5 + (1 + 9)" expression after printing it using the visitor pattern. This code demonstrates how the visitor pattern allows adding the printing operation to complex objects without modifying their internal structure.

# Strategy

Allows selecting one of the algorithms in certain situations.

The strategy pattern is a behavioral software design pattern that allows selecting an algorithm at runtime. Instead of implementing a single algorithm directly, the code receives instructions at runtime on which one to use from a family of algorithms.

Example:

Let's take an example where we have a text processor that will display data based on the chosen strategy (HTML or Markdown).

The strategy design pattern allows selecting an algorithm at runtime. Here's the example step by step:

1\. Definition of Output Formats: An OutputFormat object is defined that lists the available output formats, in this case, Markdown and HTML.

2\. Abstract Strategy Class ListStrategy: An abstract class called ListStrategy is created, which defines abstract methods start, end, and addListItem. These methods will be implemented by specific strategies.

class ListStrategy {

start(buffer) {}

end(buffer) {}

addListItem(buffer, item) {}

}

3\. Specific List Strategies: Two classes are created that inherit from ListStrategy to implement specific strategies: MarkdownListStrategy and HTMLListStrategy. Each one implements the abstract methods of the base strategy according to its specific format.

class MarkdownListStrategy extends ListStrategy {

addListItem(buffer, item) {

buffer.push(` * ${item}`);

}

}

class HTMLListStrategy extends ListStrategy {

start(buffer) {

buffer.push("<ul>");

}

end(buffer) {

buffer.push("</ul>");

}

addListItem(buffer, item) {

buffer.push(` <li>${item}</li>`);

}

}

4\. TextProcessor Class: A TextProcessor class is created that accepts an output format and uses a specific list strategy based on the selected format.

class TextProcessor {

constructor(outputFormat) {

this.buffer = [];

this.setFormat(outputFormat);

}

setFormat(format) {

switch (format) {

case OutputFormat.markdown:

this.listStrategy = new MarkdownListStrategy();

break;

case OutputFormat.html:

this.listStrategy = new HTMLListStrategy();

break;

}

}

appendList(items) {

this.listStrategy.start(this.buffer);

for (let item of items) {

this.listStrategy.addListItem(this.buffer, item);

}

this.listStrategy.end(this.buffer);

}

clear() {

this.buffer = [];

}

toString() {

return this.buffer.join("\\n");

}

}

5\. Using the Text Processor: An instance of TextProcessor is created, the output format is set, and a list is added. Then, the result is displayed.

let textProcessor = new TextProcessor();

textProcessor.setFormat(OutputFormat.markdown);

textProcessor.appendList(["one", "two", "three"]);

console.log(textProcessor.toString());

textProcessor.clear();

textProcessor.setFormat(OutputFormat.html);

textProcessor.appendList(["one", "two", "three"]);

console.log(textProcessor.toString());

Final Code:

// Enumeration of output formats

let OutputFormat = Object.freeze({

markdown: 0,

html: 1,

});

// Abstract class ListStrategy

class ListStrategy {

start(buffer) {}

end(buffer) {}

addListItem(buffer, item) {}

}

// Specific strategy for Markdown format

class MarkdownListStrategy extends ListStrategy {

addListItem(buffer, item) {

buffer.push(` * ${item}`);

}

}

// Specific strategy for HTML format

class HTMLListStrategy extends ListStrategy {

start(buffer) {

buffer.push("<ul>");

}

end(buffer) {

buffer.push("</ul>");

}

addListItem(buffer, item) {

buffer.push(` <li>${item}</li>`);

}

}

// TextProcessor class

class TextProcessor {

constructor(outputFormat) {

this.buffer = [];

this.setFormat(outputFormat);

}

setFormat(format) {

switch (format) {

case OutputFormat.markdown:

this.listStrategy = new MarkdownListStrategy();

break;

case OutputFormat.html:

this.listStrategy = new HTMLListStrategy();

break;

}

}

appendList(items) {

this.listStrategy.start(this.buffer);

for (let item of items) {

this.listStrategy.addListItem(this.buffer, item);

}

this.listStrategy.end(this.buffer);

}

clear() {

this.buffer = [];

}

toString() {

return this.buffer.join("\\n");

}

}

// Create an instance of the text processor

let textProcessor = new TextProcessor();

// Set the output format to Markdown

textProcessor.setFormat(OutputFormat.markdown);

// Append a list of items

textProcessor.appendList(["one", "two", "three"]);

// Display the output in Markdown format

console.log("Markdown Format Output:");

console.log(textProcessor.toString());

// Clear the text processor

textProcessor.clear();

// Set the output format to HTML

textProcessor.setFormat(OutputFormat.html);

// Append a list of items

textProcessor.appendList(["one", "two", "three"]);

// Display the output in HTML format

console.log("\\nHTML Format Output:");

console.log(textProcessor.toString());

Salida esperada en formato HTML:

<ul>

<li>one</li>

<li>two</li>

<li>three</li>

</ul>

This code demonstrates how different output format strategies (Markdown and HTML) can be easily switched at runtime using the strategy design pattern.

# State

Modifies the behavior of an object when its internal state changes.

The State pattern is a behavioral software design pattern that allows an object to alter its behavior when its internal state changes. This pattern is closely related to the concept of finite state machines.

Example:

Let's take an example of a light switch in which turning the switch on or off changes its state.

This is an example of the "State" design pattern, which allows an object to change its behavior when its internal state changes. Here is the code with comments explaining each step:

Step 1: We create two state classes, OnState and OffState, which inherit from the base State class. Each state class defines how the switch should behave when it is in that particular state.

class OnState extends State {

constructor() {

super();

console.log("Lights are on");

}

turnOff(sw) {

console.log("Turning off the lights...");

sw.state = new OffState();

}

}

class OffState extends State {

constructor() {

super();

console.log("Lights are off...");

}

turnOn(sw) {

console.log("Turning on the lights...");

sw.state = new OnState();

}

}

Step 2: We create the Switch class, which contains an internal state and turnOn() and turnOff() methods to change the state. We initialize the switch with the off state.

class Switch {

constructor() {

this.state = new OffState();

}

turnOn() {

this.state.turnOn(this);

}

turnOff() {

this.state.turnOff(this);

}

}

Step 3: We create the abstract base class State, which defines the turnOn() and turnOff() methods. Concrete state classes must implement these methods.

class State {

constructor() {

if (this.constructor === State) throw new Error("Abstract!");

}

turnOn(sw) {

console.log("The light is on.");

}

turnOff(sw) {

console.log("The light is off.");

}

}

Step 4: We create an instance of the Switch class and test its methods to change the state of the lights. First, we turn the lights on and then we turn them off.

let lightSwitch = new Switch();

lightSwitch.turnOn();

lightSwitch.turnOff();

This example demonstrates how the "State" design pattern allows an object, in this case, a light switch, to change its behavior based on its internal state (on or off). Each state has its own behaviors defined in the concrete state classes.

Final Code:

// Create two state classes

class OnState extends State {

constructor() {

super();

console.log("Lights are on");

}

turnOff(sw) {

console.log("Turning off the lights...");

sw.state = new OffState();

}

}

class OffState extends State {

constructor() {

super();

console.log("Lights are off...");

}

turnOn(sw) {

console.log("Turning on the lights...");

sw.state = new OnState();

}

}

// Create the Switch class

class Switch {

constructor() {

this.state = new OffState(); // Initialize with the off state

}

turnOn() {

this.state.turnOn(this); // Call the turn-on method of the current state

}

turnOff() {

this.state.turnOff(this); // Call the turn-off method of the current state

}

}

// Create the abstract base class State

class State {

constructor() {

if (this.constructor === State) throw new Error("Abstract!"); // Prevent direct instantiation

}

turnOn(sw) {

console.log("The light is on.");

}

turnOff(sw) {

console.log("The light is off.");

}

}

// Create an instance of the Switch class and test its methods

let lightSwitch = new Switch();

lightSwitch.turnOn(); // Turn on the lights

lightSwitch.turnOff(); // Turn off the lights

# Template Method

Define the skeleton of an algorithm as an abstract class, specifying how it should be performed.

Template Method is a method in a superclass, typically an abstract superclass, that defines the skeleton of an operation in terms of a series of high-level steps.

Example:

Let's take an example of a chess game. The Template Method design pattern is a design pattern that defines the skeleton of an algorithm in a superclass but allows subclasses to implement certain steps of the algorithm without changing its overall structure. Here's the code step by step:

Step 1: We create the base class Game, which will serve as the game's skeleton and defines the overall flow of the game.

class Game {

constructor(numberOfPlayers) {

this.numberOfPlayers = numberOfPlayers;

this.currentPlayer = 0;

}

execute() {

this.initialize();

while (!this.haveWinner) {

this.takeTurn();

}

console.log(`Player ${this.winningPlayer} wins.`);

}

initialize() {}

get haveWinner() {}

takeTurn() {}

get winningPlayer() {}

}

Step 2: We create the Chess class that inherits from Game and customizes specific details of the chess game, such as the number of players and maximum number of turns.

class Chess extends Game {

constructor() {

super(2);

this.maxTurns = 10;

this.turn = 1;

}

initialize() {

console.log(`Starting a chess game with ${this.numberOfPlayers} players.`);

}

get haveWinner() {

return this.turn > this.maxTurns;

}

takeTurn() {

console.log(`Turn ${this.turn} taken by player ${this.currentPlayer}`);

this.currentPlayer = (this.currentPlayer + 1) % this.numberOfPlayers;

this.turn++;

}

get winningPlayer() {

return this.currentPlayer;

}

}

Step 3: We create an instance of the Chess class and execute the game by calling the execute method.

let chess = new Chess();

chess.execute();

This example demonstrates how the Template Method design pattern is used to define the overall flow of the game in the base class Game and how specific game details are customized in the Chess class.

Final Code:

class Game {

constructor(numberOfPlayers) {

this.numberOfPlayers = numberOfPlayers;

this.currentPlayer = 0;

}

execute() {

this.initialize();

while (!this.haveWinner) {

this.takeTurn();

}

console.log(`Player ${this.winningPlayer} wins.`);

}

initialize() {}

get haveWinner() {}

takeTurn() {}

get winningPlayer() {}

}

class Chess extends Game {

constructor() {

super(2);

this.maxTurns = 10;

this.turn = 1;

}

initialize() {

console.log(`Starting a chess game with ${this.numberOfPlayers} players.`);

}

get haveWinner() {

return this.turn > this.maxTurns;

}

takeTurn() {

console.log(`Turn ${this.turn} taken by player ${this.currentPlayer}`);

this.currentPlayer = (this.currentPlayer + 1) % this.numberOfPlayers;

this.turn++;

}

get winningPlayer() {

return this.currentPlayer;

}

}

let chess = new Chess();

chess.execute();

// Expected Output:

// Starting a chess game with 2 players.

// Turn 1 taken by player 0

// Turn 2 taken by player 1

// Turn 3 taken by player 0

// Turn 4 taken by player 1

// Turn 5 taken by player 0

// Turn 6 taken by player 1

// Turn 7 taken by player 0

// Turn 8 taken by player 1

// Turn 9 taken by player 0

// Turn 10 taken by player 1

// Player 1 wins

As you conclude "Advanced Design Patterns in JavaScript," remember: that your coding journey is perpetual. JavaScript's flexibility enables sophisticated design patterns, enhancing code quality.

Keep embracing challenges, sharing knowledge, and engaging with the JavaScript community. Attend events, stay current, and contribute.

Thank you for choosing our resource. Your potential is boundless; each line of code shapes the digital world. Success in your JavaScript adventures!

Explore more at

www.hernandoabella.com