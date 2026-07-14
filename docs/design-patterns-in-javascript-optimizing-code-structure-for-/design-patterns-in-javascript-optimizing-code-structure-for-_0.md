# JavaScript 设计模式：优化代码结构以实现健壮且可扩展的JS应用程序

## 引言

通过这本全面指南，深入探索 JavaScript 设计模式的世界，了解最相关模式的实际应用。从模块模式到观察者模式，本指南的每一部分都经过精心设计，帮助您自信而清晰地应对开发挑战。无论是初学者还是经验丰富的开发者，本指南都将为您提供有效理解和应用设计模式所需的工具，从而提升 JavaScript 项目的质量和可持续性。

## 什么是设计模式？

设计模式是解决软件设计以及交互和界面相关上下文中常见问题的成熟且稳健的解决方案。这些技术提供了结构化且有效的方法来解决反复出现的挑战，促进了软件开发中的效率、可重用性和清晰性。

设计模式被认为是针对特定设计问题的成熟且经过验证的解决方案。要获得模式的认可，它必须表现出某些关键特征。首先，它必须证明在以往类似问题中具有有效性。此外，模式应具有高度可重用性，即适用于各种上下文和设计挑战。

## 设计模式的类型

设计模式主要分为三类，每类侧重于软件设计的特定维度：

创建型模式：这类模式关注类实例和对象的创建方式。它们为不同场景下的对象创建提供了灵活的解决方案。

结构型模式：结构型模式处理类和对象的组合，以形成更大的结构。它们有助于在系统各部分之间建立高效且灵活的关系。

行为型模式：这类模式关注对象之间的交互以及它们如何相互通信。它们有助于定义工作流程和协作行为。

## 创建型设计模式

创建型设计模式关注对象的创建方式，为根据情况适当地实例化对象提供解决方案。它们解决了在基本形式下创建对象时可能出现的设计和复杂性问题。这些模式通过以某种方式控制对象创建来解决这些问题。

以下是 JavaScript 中最常见的创建型设计模式：

工厂方法：提供一个创建对象的接口，允许子类更改将要创建的对象的类型。当需要灵活且可适应的创建逻辑时，它非常有用。

抽象工厂：提供一个创建相关或依赖对象家族的接口，而无需指定它们的具体类。这促进了一致且兼容的对象的创建。

建造者：用于逐步构建一个对象。它允许通过增量指定对象的类型和内容来创建复杂对象。

原型：专注于通过复制现有对象（称为原型）来创建新对象。当通过复制现有对象比从头构建更高效时，它非常有用。

单例：确保一个类只有一个实例，并提供对该实例的全局访问点。当需要单个类实例来协调整个系统的操作时使用。

### 工厂方法

工厂方法设计模式是一种软件设计技术，它依赖于通过公共接口创建特定子类型的对象。该模式通过使用一个包含具体方法和抽象方法的抽象创建者类来实现。具体方法处理对象创建，而抽象方法由具体子类实现。根据所使用的子类，可以获得特定的行为。

示例：为了更好地理解工厂方法，让我们考虑一个与在二维平面中创建点相关的具体示例。假设我们正在开发一个需要处理笛卡尔坐标和极坐标点的应用程序。

首先，我们创建一个名为 `Point` 的类，表示平面中的一个点。该类有一个接受 `x` 和 `y` 坐标的构造函数，以及一个返回点可读表示（格式为 (`x`, `y`)）的 `toString()` 方法。

步骤 1：定义表示平面中点的 `Point` 类：

```javascript
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
```

在此步骤中，我们创建了 `Point` 类，其构造函数接受 `x` 和 `y` 坐标，并有一个 `toString()` 方法来获取点的可读表示。

步骤 2：在 `PointFactory` 类中实现工厂方法：

```javascript
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
```

在此步骤中，我们创建了实现工厂方法的 `PointFactory` 类。该类包含两个静态方法：`createCartesianPoint` 和 `createPolarPoint`。第一个方法创建笛卡尔坐标的点，第二个方法创建极坐标的点。

步骤 3：使用工厂方法的示例：

```javascript
// Example of using the Factory Method
const cartesianPoint = PointFactory.createCartesianPoint(5, 6);
const polarPoint = PointFactory.createPolarPoint(5, Math.PI / 2);
```

在此步骤中，我们使用 `PointFactory` 创建了两个点。一个使用 `createCartesianPoint` 以笛卡尔坐标创建，另一个使用 `createPolarPoint` 以极坐标创建。

步骤 4：打印创建的点：

```javascript
// Printing the created points
console.log("Cartesian Point:", cartesianPoint.toString()); // Cartesian Point: (5, 6)
console.log("Polar Point:", polarPoint.toString()); // Polar Point: (6.123233995736766e-17, 5)
```

在最后一步中，我们打印了创建的点以验证结果。

最终代码：

```javascript
// Point class representing a point in the plane
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }
```





```javascript
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
```

### 抽象工厂

在软件设计中，抽象工厂设计模式是一种用于创建相关对象族或组的技术，而无需指定它们的具体类。该模式提供了一种封装一组共享共同主题的独立工厂的方法，而无需了解将要创建的对象的具体类的细节。这促进了一致且模块化的对象创建，使代码管理和扩展更加容易。

示例：为了更好地理解抽象工厂模式，让我们考虑一个与准备饮料（如茶和咖啡）相关的示例。

步骤 1：我们定义基类和子类来表示饮料，在本例中为`Beverage`、`Tea`和`Coffee`。

```javascript
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
```

步骤 2：我们定义基工厂类（`BeverageFactory`）和工厂子类（`TeaFactory`和`CoffeeFactory`），它们将用于创建特定的饮料。

```javascript
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
```

步骤 3：在这一步中，我们创建一个茶工厂实例（`teaBeverageFactory`），用它来创建一杯茶饮料（`tea`），最后消费这杯茶饮料，产生预期的控制台输出。

```javascript
let teaBeverageFactory = new TeaFactory(); // Create a tea factory 

let tea = teaBeverageFactory.makeTea(); // Use the factory to create a tea beverage 

tea.consume(); // Consume the tea beverage 

// Expected Output:

// Tea is prepared 

// This is Tea
```

最终代码：

```javascript
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
```

### 建造者

从简单对象构建复杂对象。

构造器模式是一种设计模式，旨在为面向对象编程中的各种对象创建问题提供灵活的解决方案。

示例：让我们使用一个`Person`类的示例来存储个人信息。

步骤 1. 定义`Person`类：在这一步中，我们定义`Person`类，这是我们希望以结构化方式构建的类。`Person`类有几个属性，如`addressStreet`、`postalCode`、`city`、`companyName`、`position`和`annualIncome`，用于存储个人信息。它还有一个`toString()`方法，返回个人信息的可读字符串表示。

```javascript
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
```

在这一步中，我们创建了`Person`类，其中包含一个初始化属性的构造函数和一个用于获取人员可读表示的`toString()`方法。

步骤 2. 创建建造者：在这一步中，我们创建三个相关的建造者：`PersonBuilder`、`WorkPersonBuilder`和`AddressPersonBuilder`。

`PersonBuilder`：这是用于构建`Person`对象的主要建造者。它有两个方法`lives`和`works`，用于指定人员的地址和工作。`build()`方法完成构建并返回构建好的`Person`对象。

`WorkPersonBuilder`：继承自`PersonBuilder`，用于指定人员的工作。它有`at`、`asA`和`earning`等方法，用于定义公司名称、职位和年收入。

`AddressPersonBuilder`：同样继承自`PersonBuilder`，用于指定人员的地址。它有`at`、`withPostcode`和`in`等方法，用于定义地址、邮政编码和城市。

```javascript
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
```

步骤 3. 使用建造者：在这一步中，我们创建一个名为`personBuilder`的`PersonBuilder`实例。然后，我们使用方法链以结构化方式构建一个`Person`实例。

```javascript
let personBuilder = new PersonBuilder();

let person = personBuilder.lives

.at("123 Main Street")

.in("New York")

.withPostcode("10001")

.works.at("ABC Inc.")

.asA("Engineer")

.earning(80000)

.build();
```

步骤 4. 结果与输出：最后，我们可以使用`Person`类的`toString()`方法打印构建的人员信息。

```javascript
console.log(person.toString());
```

预期输出将是人员信息的字符串表示，包括地址和工作详情：

人员居住在 123 Main Street, New York, 10001，并在 ABC Inc.担任工程师，年收入 80000

最终代码：

```javascript
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
```





```
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
```

### 原型模式

基于现有对象创建新对象。

原型模式是软件开发中的一种创建型设计模式。当需要创建的对象类型由原型实例决定时，通过克隆该原型来生成新对象。

示例：我们将以汽车为例。

步骤 1：定义 `Car` 类（原型）

```
class Car {

constructor(name, model) {

this.name = name;

this.model = model;

}

// ... (Class methods)

}
```

步骤 2：设置汽车名称的方法

```
// Method to set the car's name
setCarName(name) {
this.name = name;
console.log(`Car name adjusted to: ${this.name}`);
}
```

步骤 3：克隆汽车的方法（创建副本）

```
// Method to clone the car (create a copy)
clone() {
// Create a new Car instance with the same attributes
return new Car(this.name, this.model);
}
```

步骤 4：使用原型模式

```
// Using the Prototype Pattern
const originalCar = new Car('Audi', 'A3');
// Clone the original car to create a new instance
const clonedCar = originalCar.clone();
clonedCar.setCarName('BMW');
```

步骤 5：验证两辆汽车是否不同

```
// Verify that the cars are different
console.log('Original Car:', originalCar.name, originalCar.model);
console.log('Cloned Car:', clonedCar.name, clonedCar.model);
```

这段代码演示了如何使用原型模式创建现有对象（`originalCar`）的副本，并调整其属性（`name`），同时不影响原始对象。最后，验证两辆汽车不同，确认克隆操作正确。

最终代码：

```
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
```

### 单例模式

确保某个类只创建一个对象。

在软件工程中，单例模式是一种软件设计模式，它将类的实例化限制为“单个”实例。当整个系统只需要一个对象来协调操作时，这种模式非常有用。

示例：

步骤 1：单例类定义：

```
class Singleton {
constructor() {
// ...
}
// ...
}
```

步骤 2：检查该类的实例是否已存在：

```
const instance = this.constructor.instance;
if (instance) {
return instance;
}
```

在此步骤中，在 `Singleton` 类的构造函数中，我们通过 `this.constructor.instance` 检查该类的实例是否已存在。如果实例已存在，则返回该实例，而不是创建新实例。

步骤 3：创建 `Singleton` 类的实例：

```
let s1 = new Singleton();
let s2 = new Singleton();
```

在此步骤中，我们创建 `Singleton` 类的两个实例 `s1` 和 `s2`。

步骤 4：检查 `s1` 和 `s2` 是否为同一实例：

```
console.log('Are they the same? ' + (s1 === s2));
```

这里，我们通过 `(s1 === s2)` 检查 `s1` 和 `s2` 是否为同一实例，并在控制台显示结果。

步骤 5：调用 `say()` 方法：在最后一步中，我们调用 `s1` 实例的 `say()` 方法，该方法将在控制台打印 "Saying..."。

```
s1.say();
```

最终代码：在最后一步中，我们调用 `s1` 实例的 `say()` 方法，该方法将在控制台打印 "Saying..."。

```
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
```

这些创建型模式是高效且结构化地解决 JavaScript 项目中对象创建问题的宝贵工具。每种模式都有其特定的用途和应用场景，是软件设计中不可或缺的资源。

## 结构型设计模式

结构型设计模式关注类和对象的组合，以形成更复杂的结构。它们利用继承和接口组合，在实体之间创建高效且灵活的关系。

以下是 JavaScript 中最常见的结构型设计模式：

- **适配器模式**：允许不兼容的接口协同工作。它将一个类的接口转换成客户端期望的另一个接口。当需要具有不同接口的对象协作时非常有用。
- **桥接模式**：将抽象与其实现分离，使它们可以独立演化。当希望避免抽象与实现之间永久绑定时非常有用。
- **组合模式**：将对象组合成树形结构以表示“部分-整体”的层次结构。它允许统一处理单个对象和对象组合。
- **装饰器模式**：动态地向现有对象添加功能，而不修改其结构。当希望灵活地扩展对象功能时非常有用。
- **外观模式**：为子系统中的一组接口提供简化接口。通过提供更友好的接口，使复杂系统的使用更加容易。
- **享元模式**：通过尽可能多地与相似对象共享数据，最小化内存或磁盘存储的使用。当需要高效管理大量对象时非常有用。




**代理**：为另一个对象提供替代或占位符以控制对其的访问。可用于添加额外功能，如访问控制或懒加载。

### 适配器

通过调整自身接口以适应现有类，使接口不兼容的类能够协作。当我们需要不同接口的对象在不修改源代码的情况下协同工作时，此模式特别有用。

示例：

1. 不兼容接口的定义：在此示例中，我们有两个计算器接口：`Calculator1`（旧版）和 `Calculator2`（新版）。

```javascript
class Calculator1 {
  constructor() {
    this.operations = function(value1, value2, operation) {
      // 旧计算器的实现
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
      // 新计算器的实现
      return value1 + value2;
    };
    this.subtract = function(value1, value2) {
      // 新计算器的实现
      return value1 - value2;
    };
  }
}
```

2. 创建适配器：我们创建一个 `CalcAdapter` 类，它将作为两个计算器接口之间的适配器。适配器包装新接口（`Calculator2`），并提供所需操作的方法。

```javascript
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
```

3. 使用适配器：现在，我们可以使用 `CalcAdapter` 对新接口（`Calculator2`）执行操作，而无需修改其代码。这使得从旧计算器过渡到新计算器更加容易。

```javascript
// 创建适配器实例
const calcAdapter = new CalcAdapter();
// 使用适配器执行减法操作
console.log(calcAdapter.operations(10, 55, 'subtract'));
```

最终代码：

```javascript
// 旧计算器类的定义
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

// 新计算器类的定义
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

// 适配器类的定义
class CalculatorAdapter {
  constructor() {
    // 创建新计算器实例
    const newCalculator = new NewCalculator();
    // 定义将使用新计算器的 operations 方法
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

// 创建计算器适配器实例
const calculatorAdapter = new CalculatorAdapter();
// 使用计算器适配器执行减法操作
console.log(calculatorAdapter.operations(10, 55, 'subtract')); // -45
console.log(calculatorAdapter.operations(10, 55, 'add')); // 65
```

### 桥接

桥接设计模式用于将抽象与实现分离，使两者可以独立演化。换句话说，当你想避免抽象类与其具体类之间的紧密连接，使它们能够独立演化而不相互影响时，可以使用桥接模式。

示例：

在此示例中，我们将创建用于渲染几何形状的类。我们将使用两个渲染器类：`VectorRenderer` 和 `RasterRenderer`。然后，我们将创建一个抽象类 `Shape` 和一个继承自 `Shape` 的 `Circle` 类。桥接模式的关键在于 `Shape` 持有一个对渲染器的引用，并将渲染任务委托给具体的渲染器。

步骤 1. 渲染器类的定义：在此步骤中，我们创建 `VectorRenderer` 和 `RasterRenderer` 类，代表不同的渲染方法。

```javascript
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
```

步骤 2. 抽象类 `Shape` 的定义：在此步骤中，我们创建抽象类 `Shape`，它将作为我们的抽象。该类有一个 `renderer` 属性，它是对我们将用于绘制形状的渲染器的引用。

```javascript
class Shape {
  constructor(renderer) {
    this.renderer = renderer;
  }
}
```

步骤 3. `Circle` 类的定义：在此步骤中，我们创建继承自 `Shape` 的 `Circle` 类。`Circle` 类有一个 `radius` 属性，表示圆的半径。

```javascript
class Circle extends Shape {
  constructor(renderer, radius) {
    super(renderer);
    this.radius = radius;
  }
}
```

步骤 4. `draw` 方法的实现：在 `Circle` 类中，我们实现 `draw` 方法。该方法通过 `this.renderer` 引用将渲染任务委托给具体的渲染器（`VectorRenderer` 或 `RasterRenderer`）。

```javascript
draw() {
  this.renderer.renderCircle(this.radius);
}
```

步骤 5. 创建渲染器和圆的实例：在此步骤中，我们创建渲染器类 `VectorRenderer` 和 `RasterRenderer` 的实例。然后，我们创建一个名为 `circle` 的 `Circle` 实例，并为其提供向量渲染器和半径为 5。

```javascript
let raster = new RasterRenderer();
let vector = new VectorRenderer();
let circle = new Circle(vector, 5);
```

步骤 6. 绘制圆并改变其大小：我们在 `circle` 实例上调用 `draw` 方法，从而打印出向量渲染器对应的消息。然后，我们通过调用 `resize` 方法改变圆的大小，将其半径加倍。

```javascript
circle.draw();
circle.resize(2);
```

步骤 7. 大小改变后绘制圆：我们再次在 `circle` 实例上调用 `draw` 方法，从而打印出大小改变后的更新消息。

```javascript
circle.draw();
```

最终代码：

```javascript
// 渲染器类的定义
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

// 抽象类 `Shape` 的定义
class Shape {
  constructor(renderer) {
    this.renderer = renderer;
  }
}

// `Circle` 类的定义
class Circle extends Shape {
  constructor(renderer, radius) {
    super(renderer);
    this.radius = radius;
  }

  // `draw` 方法的实现
  draw() {
    this.renderer.renderCircle(this.radius);
  }

  resize(factor) {
    this.radius *= factor;
  }
}

// 创建渲染器和圆的实例
let raster = new RasterRenderer();
let vector = new VectorRenderer();
let circle = new Circle(vector, 5);

// 绘制圆并改变其大小
circle.draw();
circle.resize(2);

// 大小改变后绘制圆
circle.draw();

// 预期输出：
// Drawing a circle of radius 5
// Drawing a circle of radius 10
```

### 组合

组合模式用于将对象组合成树形结构以表示对象层次结构。这使得单个对象和对象的组合能够以相同的方式处理，简化了它们的操作。

示例：

1. 类的定义：在此示例中，我们创建两个类：`Employee` 表示单个员工，`EmployeeGroup` 表示员工组。

```javascript
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
```




2. 创建员工和组：我们创建单个员工的实例，然后将它们分组到 `EmployeeGroup` 中。

```
// Creating individual employees
let hernando = new Employee("Hernando", "Developer");
let albert = new Employee("Albert", "Developer");
// Creating an employee group and adding individual employees
let developerGroup = new EmployeeGroup("Developers", [hernando, albert]);
```

```
// Creating individual employees
let hernando = new Employee("Hernando", "Developer");
let albert = new Employee("Albert", "Developer");
// Creating an employee group and adding individual employees
let developerGroup = new EmployeeGroup("Developers", [hernando, albert]);
```

3. 打印层次结构：我们使用 `print()` 方法显示层次结构，其中包含单个员工和员工组。

```
// Print the hierarchical structure
developerGroup.print();
```

最终代码：

```
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
```

### 装饰器

装饰器模式允许动态地向单个对象添加或覆盖行为，而不影响同一类的其他对象。当你希望在不创建子类的情况下扩展对象的能力时，它特别有用。

示例：

1. 类定义：在此示例中，我们创建 `Form` 类作为基类，`Circle` 作为我们想要装饰的具体形状。我们还创建了一个名为 `ColoredShape` 的类，它充当装饰器，为形状添加颜色。

```
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
```

2. 使用装饰器：我们创建一个基础圆形的实例，然后使用 `ColoredShape` 类将该圆形装饰为红色。

```
// Create a base circle
let circle = new Circle(2);
console.log(circle.toString()); // Output: A circle of radius 2
// Decorate the circle with red color
let redCircle = new ColoredShape(circle, "red");
console.log(redCircle.toString()); // Output: A circle of radius 2, colored red
```

最终代码：

```
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
```

### 外观

外观模式是面向对象编程中常用的软件设计模式。类似于建筑中的外观，外观是一个对象，它作为前端接口，屏蔽了更复杂的底层或结构代码。它提供了一个简化的接口来访问一组相关的子系统或类，使得与系统的交互更加容易，而无需了解内部细节。

示例：在此示例中，我们将使用外观模式模拟计算机的操作。计算机由各种组件组成，如 CPU、内存和硬盘。`ComputerFacade` 将简化与这些组件的交互。

我们定义计算机组件的类：`CPU`、`Memory` 和 `HardDrive`。这些类具有执行各种操作的方法，例如冻结 CPU、将数据加载到内存以及从硬盘读取数据。

```
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
```

我们创建 `ComputerFacade`，它提供了一个简化的接口来与计算机组件交互。在 `start()` 方法中，组件被一致地使用，并屏蔽了复杂的细节。

```
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
```

最后，我们创建一个 `ComputerFacade` 实例，并使用其 `start()` 方法模拟计算机的启动过程。

```
let computer = new ComputerFacade();
computer.start();
```

最终代码：

```
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
```

### 享元





享元模式用于在创建相似对象时通过尽可能多地共享数据来最小化内存使用。这意味着，与其创建多个具有相同数据的对象实例，不如使用一个共享实例来表示这些公共数据。这显著减少了内存使用量，尤其是在处理大量相似对象时。

示例：

步骤 1\. 定义 `User` 和 `User2` 类：在此步骤中，我们定义了两个类：`User` 和 `User2`。第一个类表示一个带有全名的简单用户，而第二个类实现了享元模式，通过共享相似的全名来减少内存使用。

```
// 定义 User 类
class User {
  constructor(fullName) {
    this.fullName = fullName;
  }
}

// 定义实现享元模式的 User2 类
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
```

步骤 2\. 辅助函数：在此步骤中，我们创建了两个辅助函数：`getRandomInteger` 用于获取随机整数，`getRandomText` 用于生成随机文本字符串。

```
// 辅助函数
function getRandomInteger(max) {
  return Math.floor(Math.random() * Math.floor(max));
}

function getRandomText() {
  let result = [];
  for (let x = 0; x < 10; ++x)
    result.push(String.fromCharCode(65 + getRandomInteger(26)));
  return result.join('');
}
```

步骤 3\. 创建随机姓名：在此步骤中，我们创建了两个数组 `names` 和 `lastNames`，其中包含随机生成的名字和姓氏，用于创建用户。

```
// 创建随机姓名
let names = lastNames = [];
for (let i = 0; i < 100; ++i) {
  names.push(getRandomText());
  lastNames.push(getRandomText());
}
```

步骤 4\. 创建用户：在此步骤中，我们创建了两个数组 `users` 和 `users2`，用于存放创建的用户。我们遍历 `names` 和 `lastNames` 数组，分别创建 10,000 个未使用享元模式和使用享元模式的用户。

```
let users = [];
let users2 = [];

// 创建用户
for (let name of names) {
  for (let lastName of lastNames) {
    users.push(new User(`${name} ${lastName}`));
    users2.push(new User2(`${name} ${lastName}`));
  }
}
```

步骤 5\. 内存使用对比：在此步骤中，我们使用 `JSON.stringify` 对比未使用享元模式的用户和使用享元模式的用户的内存使用情况。并将结果打印到控制台。

```
// 内存使用对比
console.log(`10,000 users occupy approximately ${JSON.stringify(users).length} characters`);
let users2Length = [users2, User2.strings].map(x => JSON.stringify(x).length).reduce((x, y) => x + y);
console.log(`10,000 users with Flyweight occupy ~${users2Length} characters`);
```

最终代码：

```
// 定义 User 类
class User {
  constructor(fullName) {
    this.fullName = fullName;
  }
}

// 定义实现享元模式的 User2 类
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

// 辅助函数
function getRandomInteger(max) {
  return Math.floor(Math.random() * Math.floor(max));
}

function getRandomText() {
  let result = [];
  for (let x = 0; x < 10; ++x)
    result.push(String.fromCharCode(65 + getRandomInteger(26)));
  return result.join('');
}

// 创建随机姓名
let names = lastNames = [];
for (let i = 0; i < 100; ++i) {
  names.push(getRandomText());
  lastNames.push(getRandomText());
}

let users = [];
let users2 = [];

// 创建用户
for (let name of names) {
  for (let lastName of lastNames) {
    users.push(new User(`${name} ${lastName}`));
    users2.push(new User2(`${name} ${lastName}`));
  }
}

// 内存使用对比
console.log(`10,000 users occupy approximately ${JSON.stringify(users).length} characters`); // 10,000 users occupy approximately 1720001 characters
let users2Length = [users2, User2.strings].map(x => JSON.stringify(x).length).reduce((x, y) => x + y);
console.log(`10,000 users with Flyweight occupy ~${users2Length} characters`); // 10,000 users with Flyweight occupy ~838602 characters
```

### 代理模式

代理模式允许一个类代表另一个类的功能，充当客户端与真实对象之间的中介或“代理”。这对于控制对真实对象的访问、在访问真实对象之前或之后执行额外操作，甚至完全替换真实对象都非常有用。

示例：

让我们想象一个名为 `Percentage` 的代理对象示例，用于表示百分比。该代理允许操作百分比值并对其执行数学运算。

```
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

// 让我们使用 Percentage 代理对象
let percentageFive = new Percentage(5);
console.log(percentageFive.toString()); // 输出: "5%"
console.log(`5% of 50 is ${50 * percentageFive}`); // 输出: "5% of 50 is 2.5"
```

在这个示例中，`Percentage` 充当了一个代理，允许表示百分比值并执行计算。`Percentage` 代理使得操作百分比值并在数学运算中使用它们变得简单。

## 行为型设计模式

行为型设计模式关注软件系统中对象之间的通信与交互。这些模式识别出对象之间常见的通信与协作模式，从而在设计和实现系统行为时提高灵活性和效率。

以下是 JavaScript 中最常见的行为型设计模式：

责任链模式：允许多个对象处理一个请求，而发送者无需知道哪个对象将处理它。

命令模式：将请求封装为一个对象，从而允许客户端用操作来参数化对象、对请求进行排队、记录请求以及支持可撤销的操作。

迭代器模式：提供一种顺序访问集合元素的方法，而无需暴露其底层表示。

中介者模式：定义一个对象，该对象封装了系统中对象之间如何进行通信，通过防止对象显式地相互引用来促进松耦合。

备忘录模式：允许捕获并外部化对象的内部状态，以便之后可以将对象恢复到此状态。

观察者模式：定义对象之间的一对多依赖关系，使得当一个对象改变状态时，其所有依赖者都会自动收到通知并更新。

访问者模式：表示要对对象结构中的元素执行的操作，允许在不改变元素类的前提下定义新的操作。

策略模式：定义一系列算法，将每个算法封装起来，并使它们可以互换，从而让算法可以独立于使用它的客户端而变化。

状态模式：允许一个对象在其内部状态改变时改变其行为，通常实现为有限状态机。

模板方法模式：定义一个操作中的算法骨架，但允许子类在不改变算法结构的情况下重新定义算法的某些部分。

### 责任链模式

创建一个对象链。从某个点开始，直到满足某个条件才停止。

在面向对象设计中，责任链模式是一种设计模式，由命令对象的源和一系列处理对象组成。

示例：




让我们以一个包含生物的游戏为例。该生物在达到特定条件时会提升其防御和攻击力。它会形成一个链，攻击和防御值会随之增减。

步骤 1\. 关键类与责任链模式的定义：在此步骤中，我们定义主要类，包括 `Creature` 和 `CreatureModifier`，以及具体的修饰器类。

```javascript
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
```

步骤 2\. 具体修饰器的实现：我们创建具体的修饰器，例如 `NoBonusesModifier`、`DoubleAttackModifier` 和 `IncreaseDefenseModifier`。

```javascript
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
```

步骤 3\. 使用责任链模式：在此步骤中，我们创建一个 `Creature` 实例，然后创建一个修饰器责任链并将其应用于该生物。

```javascript
let pikachu = new Creature("Pikachu", 1, 1);
console.log(pikachu.toString());

let root = new CreatureModifier(pikachu);
root.add(new NoBonusesModifier(pikachu));
root.add(new IncreaseDefenseModifier(pikachu));
root.handle();

console.log(pikachu.toString());
```

最终代码整合了所有步骤，并展示了执行后的预期输出。

最终代码：

```javascript
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

// 创建一个生物并显示其初始状态
let pikachu = new Creature("Pikachu", 1, 1);
console.log(pikachu.toString());

// 创建责任链并添加修饰器
let root = new CreatureModifier(pikachu);
root.add(new NoBonusesModifier(pikachu));
root.add(new IncreaseDefenseModifier(pikachu));

// 将修饰器应用于生物
root.handle();

// 显示应用修饰器后生物的最终状态
console.log(pikachu.toString());

// 预期输出：
// Pikachu (1 / 1)
// Increasing defense of Pikachu
// Pikachu (1 / 2)
```

### 命令

在面向对象编程中，命令模式是一种行为设计模式，它使用对象来封装执行某个操作或触发某个事件所需的所有信息。这些信息包括方法名、拥有该方法的对象以及方法的参数值。

示例：

我们以一个简单的银行账户为例，在该账户上执行存款或取款一定金额的指令。

步骤 1\. `BankAccount` 类的定义：在此步骤中，我们定义 `BankAccount` 类，它代表一个银行账户，包含存款、取款和获取余额的方法。

```javascript
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
```

步骤 2\. 创建命令：在此步骤中，我们创建一个枚举 `Action` 来表示存款和取款操作，然后定义 `BankAccountCommand` 类，该类封装了一个操作及其金额。

```javascript
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
        this.account.withdraw(this.amount); // 撤销存款即取款
        break;
      case Action.withdraw:
        this.account.deposit(this.amount); // 撤销取款即存款
        break;
    }
  }
}
```

步骤 3\. 使用命令模式：在此步骤中，我们创建一个 `BankAccount` 实例和一个存款命令，然后执行该命令并撤销它。

```javascript
let bankAccount = new BankAccount(100);
let cmd = new BankAccountCommand(bankAccount, Action.deposit, 50);
cmd.execute(); // 执行存款 50
console.log(bankAccount.toString()); // 余额：150
cmd.undo(); // 撤销存款 50
console.log(bankAccount.toString()); // 余额：100
```

这段代码演示了命令模式如何将请求封装为对象，从而轻松执行和撤销操作。

最终代码：

```javascript
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
        this.account.withdraw(this.amount); // 撤销存款即取款
        break;
      case Action.withdraw:
        this.account.deposit(this.amount); // 撤销取款即存款
        break;
    }
  }
}

let bankAccount = new BankAccount(100);
let cmd = new BankAccountCommand(bankAccount, Action.deposit, 50);
cmd.execute(); // 执行存款 50
console.log(bankAccount.toString()); // 余额：150
cmd.undo(); // 撤销存款 50
console.log(bankAccount.toString()); // 余额：100
```

### 迭代器





### 迭代器

`Iterator` 在不暴露对象底层表示的情况下访问其元素。

在面向对象编程中，迭代器模式是一种设计模式，其中迭代器用于遍历容器并访问容器的元素。

#### `Thing` 类的定义

首先，我们定义一个名为 `Thing` 的类，它有两个属性 `a` 和 `b`。

##### 步骤 1：定义 `Thing` 类及其 `a` 和 `b` 属性。

```
class Thing {
  constructor() {
    this.a = 11;
    this.b = 22;
  }
  // 其余代码
}
```

##### 步骤 2：实现 `Symbol.iterator` 方法以遍历 `Thing` 类的 `a` 和 `b` 属性。

```
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
  // 其余代码
}
```

##### 步骤 3：实现 `backwards` 属性以逆序遍历属性。

```
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
  // 其余代码
}
```

```
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
  // 其余代码
}
```

##### 步骤 4：创建一个包含数字元素的数组 `values`。

```
let values = [100, 200, 300];
```

##### 步骤 5：使用 `for...in` 循环遍历 `values` 数组。

```
for (let i in values) {
  console.log(`Element at position ${i} is ${values[i]}`);
}
```

##### 步骤 6：使用另一个 `for...in` 循环遍历一个对象（不推荐）。

```
for (let v in values) {
  console.log(`The value is ${v}`);
}
```

##### 步骤 7：创建 `Thing` 类的一个实例 `thing`。

```
let thing = new Thing();
```

##### 步骤 8：使用 `for...of` 循环遍历 `thing` 的属性。

```
console.log("Iterating over 'a' and 'b':");
for (let element of thing) {
  console.log(`${element}`);
}
```

##### 步骤 9：使用另一个 `for...of` 循环逆序遍历。

```
console.log("Iterating in reverse order:");
for (let element of thing.backwards) {
  console.log(`${element}`);
}
```

#### 最终代码

我们将以数组为例，打印数组的值，然后使用迭代器逆序打印其值。

```
// 定义一个名为 'Thing' 的类
class Thing {
  constructor() {
    this.a = 11; // 属性 'a'，值为 11
    this.b = 22; // 属性 'b'，值为 22
  }

  // 定义一个迭代器来遍历该类的元素 'a' 和 'b'
  [Symbol.iterator]() {
    let i = 0; // 初始化索引以保持控制
    let self = this; // 捕获当前实例（'this'）的引用
    return {
      next: function() {
        return {
          done: i > 1, // 指示是否已遍历完所有内容（当 'i' 大于 1 时）
          value: self[i++ === 0 ? 'a' : 'b'] // 获取对应的值（'a' 或 'b'）
        };
      }
    };
  }

  // 获取一个迭代器以逆序遍历元素
  get backwards() {
    let i = 0; // 初始化索引以保持控制
    let self = this; // 捕获当前实例（'this'）的引用
    return {
      next: function() {
        return {
          done: i > 1, // 指示是否已遍历完所有内容（当 'i' 大于 1 时）
          value: self[i++ === 0 ? 'b' : 'a'] // 获取对应的值（'b' 或 'a'）
        };
      },
      [Symbol.iterator]: function() { return this; } // 使迭代器可迭代
    };
  }
}

let values = [100, 200, 300];

// 使用 for...in 循环遍历数组（注意：这不是推荐用于数组的方式）
for (let i in values) {
  console.log(`Element at position ${i} is ${values[i]}`);
}

// 使用 for...in 循环遍历对象（注意：这不是推荐用于对象的方式）
for (let v in values) {
  console.log(`The value is ${v}`);
}

let thing = new Thing(); // 创建类 'Thing' 的一个实例

console.log("Iterating over 'a' and 'b':");
for (let element of thing) {
  console.log(`${element}`);
}

console.log("Iterating in reverse order:");
for (let element of thing.backwards) {
  console.log(`${element}`);
}

// 预期输出：
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
```

### 中介者

中介者模式添加一个第三方对象来控制两个对象之间的交互。它允许类之间的灵活耦合，因为它是唯一详细了解其方法的类。

中介者模式定义了一个对象，该对象封装了一组对象如何交互。由于它可以改变程序的执行行为，因此该模式被认为是一种行为模式。在面向对象编程中，程序通常由许多类组成。

我们将使用一个人在聊天室中的示例。在这里，聊天室充当两个相互通信的人之间的中介者。

#### 示例

##### 步骤 1. `Person` 类的定义，表示聊天室中的人：

```
class Person {
  constructor(name, chatRoom) {
    this.name = name;         // 人的名字
    this.chatRoom = chatRoom; // 他们所属的聊天室
  }

  // 在聊天室中发送消息的方法
  say(message) {
    this.chatRoom.sendMessage(this, message);
  }

  // 接收消息的方法
  receive(message) {
    console.log(`${this.name} receives: ${message}`);
  }
}
```

##### 步骤 2. `ChatRoom` 类的定义，充当中介者：

```
class ChatRoom {
  constructor() {
    this.people = []; // 存储聊天室中的人
  }

  // 将一个人加入聊天室的方法
  joinPerson(person) {
    this.people.push(person); // 将此人添加到列表中
    person.chatRoom = this;   // 将此人的聊天室设置为当前房间
  }

  // 向房间中所有人发送消息的方法
  sendMessage(sender, message) {
    for (const person of this.people) {
      if (person !== sender) {
        person.receive(`${sender.name}: ${message}`);
      }
    }
  }
}
```

##### 步骤 3. 创建一个聊天室（`ChatRoom`）：

```
const chatRoom = new ChatRoom();
```

##### 步骤 4. 创建人并将他们加入聊天室：

```
const john = new Person("John", chatRoom);
const tony = new Person("Tony", chatRoom);
chatRoom.joinPerson(john);
chatRoom.joinPerson(tony);
```

##### 步骤 5. John 在聊天室中发送一条消息：

```
john.say("Hello, everyone!");
```

##### 步骤 6. 创建新的人并将其加入聊天室：

```
const doe = new Person("Doe", chatRoom);
chatRoom.joinPerson(doe);
```

##### 步骤 7. Doe 在聊天室中发送一条消息：

```
doe.say("Hi, everyone!");
```

每当有人发送消息时，聊天室负责将该消息分发给房间中的所有其他人。

#### 最终代码

```
// Person 类的定义，表示聊天室中的人
class Person {
  constructor(name, chatRoom) {
    this.name = name;         // 人的名字
    this.chatRoom = chatRoom; // 他们所属的聊天室
  }

  // 在聊天室中发送消息的方法
  say(message) {
    this.chatRoom.sendMessage(this, message);
  }

  // 接收消息的方法
  receive(message) {
    console.log(`${this.name} receives: ${message}`);
  }
}

// ChatRoom 类的定义，充当中介者
class ChatRoom {
  constructor() {
    this.people = []; // 存储聊天室中的人
  }

  // 将一个人加入聊天室的方法
  joinPerson(person) {
    this.people.push(person); // 将此人添加到列表中
    person.chatRoom = this;   // 将此人的聊天室设置为当前房间
  }

  // 向房间中所有人发送消息的方法
  sendMessage(sender, message) {
    for (const person of this.people) {
      if (person !== sender) {
        person.receive(`${sender.name}: ${message}`);
      }
    }
  }
}

// 创建一个聊天室
const chatRoom = new ChatRoom();

// 创建人并将他们加入聊天室
const john = new Person("John", chatRoom);
const tony = new Person("Tony", chatRoom);
```





`chatRoom.joinPerson(john);`

`chatRoom.joinPerson(tony);`

```
// John sends a message in the chat room
john.say("Hello, everyone!");

// Creation of a new person and joining them to the chat room
const doe = new Person("Doe", chatRoom);
chatRoom.joinPerson(doe);

// Doe sends a message in the chat room
doe.say("Hi, everyone!");
```

### 备忘录模式

备忘录模式允许将对象恢复到其先前的状态。

备忘录模式是一种软件设计模式，它提供了将对象恢复到先前状态的能力。它通过三个对象来实现：发起人、看护人和备忘录。

示例：

让我们以银行账户为例，其中我们存储了先前的状态，并具备撤销功能。

步骤 1. 定义备忘录类：

```
class Memento {
  constructor(balance) {
    this.balance = balance;
  }
}
```

在这一步中，我们创建了 `Memento` 类，它将用于存储银行账户在某一时刻的状态。

步骤 2. 定义 `BankAccount` 类：

```
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
```

这里，我们创建了 `BankAccount` 类，它代表一个银行账户，具备存款、以 `Memento` 形式保存状态以及恢复先前状态的能力。

步骤 3. 定义 `Caretaker` 类：

```
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
```

`Caretaker` 类负责将 `Memento` 存储在一个列表中，以便在需要时恢复先前状态。

步骤 4. 使用备忘录模式：

```
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
```

在这一步中，我们创建了一个 `BankAccount` 实例和一个 `Caretaker`。然后，我们向银行账户存款，并使用 `Caretaker` 将状态保存为 `Memento`。最后，我们使用 `Memento` 恢复银行账户的先前状态，并验证结果余额。

最终代码：

```
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
```

### 观察者模式

允许多个观察者对象监视一个事件。

观察者模式是一种软件设计模式，其中一个对象（称为主题）维护其依赖项（称为观察者）的列表，并在状态发生变化时自动通知它们，通常是通过调用它们的方法之一。

示例：

让我们以一个人为例，如果人生病了，就会显示通知。

步骤 1. 定义类和观察者模式：在这一步中，我们定义了三个关键类：`Event`、`GetSick` 和 `Person`。`Event` 类代表一个可观察的事件，包含订阅、取消订阅和通知观察者的逻辑。

`GetSick` 类是一个特定的事件，包含事件发生地点的信息。`Person` 类是可观察的主题，它可以“生病”，并在发生时通知观察者。

```
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
```

步骤 2. 使用观察者模式：在这一步中，我们创建了一个 `Person` 实例，然后使用 `Event` 类的 `subscribe` 方法订阅了一个观察者到“生病”事件。接着，我们通过调用 `catchCold` 方法模拟了人生病两次。之后，我们使用 `unsubscribe` 方法取消订阅观察者。最后，我们再次调用 `catchCold` 方法，但已取消订阅的观察者不再接收通知。

这种模式允许多个观察者监视一个事件（本例中为生病），而 `Person` 类无需知道观察者是谁或它们如何响应事件。

```
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
```

最终代码：

```
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
```





```javascript
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
```

### 访问者模式

在不修改对象的情况下为其添加操作。

访问者设计模式是一种将算法与其操作的对象结构分离的方法。这种分离的一个实际结果是能够在不修改现有对象结构的情况下为其添加新操作。

示例：

让我们以`NumericExpression`类为例，它返回给定表达式的结果。

1. NumericExpression 类：这个类表示一个带有值的简单数值表达式。

    ```javascript
    class NumericExpression {
      constructor(value) {
        this.value = value;
      }
      print(buffer) {
        buffer.push(this.value.toString());
      }
    }
    ```

2. SumExpression 类：这个类表示一个求和表达式，它接受两个数值表达式（左和右）并将它们相加。

    ```javascript
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
    ```

3. 使用访问者模式：接下来，你使用`NumericExpression`和`SumExpression`类的实例创建一个表示“5 + (1 + 9)”的组合表达式。

    ```javascript
    let e = new SumExpression(
        new NumericExpression(5),
        new SumExpression(
            new NumericExpression(1),
            new NumericExpression(9)
        )
    );
    ```

打印表达式：最后，你使用`print()`方法获取表达式的可读表示，并将其存储在缓冲区中。

```javascript
let buffer = [];
e.print(buffer);
console.log(buffer.join('')); // Output: (5+(1+9))
```

这个示例说明了访问者设计模式如何允许你向复杂对象添加打印操作，而无需修改其内部结构。这使得代码更加灵活和可扩展，便于未来添加操作，同时不影响现有类。

最终代码：

```javascript
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
```

预期输出是`(5+(1+9))`，这是使用访问者模式打印“5 + (1 + 9)”表达式后的表示。这段代码演示了访问者模式如何允许在不修改内部结构的情况下向复杂对象添加打印操作。

### 策略模式

允许在特定情况下选择一种算法。

策略模式是一种行为型软件设计模式，允许在运行时选择算法。代码不是直接实现单个算法，而是在运行时接收指令，从一系列算法中选择使用哪一个。

示例：

让我们举一个例子，我们有一个文本处理器，它会根据选择的策略（HTML 或 Markdown）显示数据。

策略设计模式允许在运行时选择算法。以下是逐步示例：

1. 输出格式的定义：定义了一个`OutputFormat`对象，列出了可用的输出格式，本例中为 Markdown 和 HTML。

2. 抽象策略类`ListStrategy`：创建了一个名为`ListStrategy`的抽象类，它定义了抽象方法`start`、`end`和`addListItem`。这些方法将由具体策略实现。

    ```javascript
    class ListStrategy {
      start(buffer) {}
      end(buffer) {}
      addListItem(buffer, item) {}
    }
    ```

3. 具体列表策略：创建了两个继承自`ListStrategy`的类来实现具体策略：`MarkdownListStrategy`和`HTMLListStrategy`。每个类根据其特定格式实现了基策略的抽象方法。

    ```javascript
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
    ```

4. TextProcessor 类：创建了一个`TextProcessor`类，它接受一个输出格式，并根据所选格式使用特定的列表策略。

    ```javascript
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
    ```

5. 使用文本处理器：创建了一个`TextProcessor`实例，设置输出格式，添加列表，然后显示结果。

    ```javascript
    let textProcessor = new TextProcessor();
    textProcessor.setFormat(OutputFormat.markdown);
    textProcessor.appendList(["one", "two", "three"]);
    console.log(textProcessor.toString());
    textProcessor.clear();
    textProcessor.setFormat(OutputFormat.html);
    textProcessor.appendList(["one", "two", "three"]);
    console.log(textProcessor.toString());
    ```

最终代码：

```javascript
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
```




`console.log(textProcessor.toString());`

预期输出为 HTML 格式：

```html
<ul>
<li>one</li>
<li>two</li>
<li>three</li>
</ul>
```

这段代码演示了如何使用策略设计模式在运行时轻松切换不同的输出格式策略（Markdown 和 HTML）。

### 状态模式

当对象的内部状态改变时，修改其行为。

状态模式是一种行为型软件设计模式，它允许对象在其内部状态改变时改变其行为。该模式与有限状态机的概念密切相关。

示例：

以电灯开关为例，打开或关闭开关会改变其状态。

这是“状态”设计模式的一个示例，它允许对象在其内部状态改变时改变其行为。以下是带有注释的代码，解释了每一步：

步骤 1：我们创建两个状态类 `OnState` 和 `OffState`，它们继承自基类 `State`。每个状态类定义了开关在该特定状态下应如何表现。

```javascript
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
```

步骤 2：我们创建 `Switch` 类，它包含一个内部状态以及 `turnOn()` 和 `turnOff()` 方法来改变状态。我们将开关初始化为关闭状态。

```javascript
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
```

步骤 3：我们创建抽象基类 `State`，它定义了 `turnOn()` 和 `turnOff()` 方法。具体状态类必须实现这些方法。

```javascript
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
```

步骤 4：我们创建 `Switch` 类的一个实例，并测试其方法来改变灯的状态。首先，我们打开灯，然后关闭灯。

```javascript
let lightSwitch = new Switch();
lightSwitch.turnOn();
lightSwitch.turnOff();
```

这个示例演示了“状态”设计模式如何允许一个对象（本例中为电灯开关）根据其内部状态（开或关）改变其行为。每个状态在具体状态类中定义了自己的行为。

最终代码：

```javascript
// 创建两个状态类
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

// 创建 Switch 类
class Switch {
  constructor() {
    this.state = new OffState(); // 初始化为关闭状态
  }
  turnOn() {
    this.state.turnOn(this); // 调用当前状态的打开方法
  }
  turnOff() {
    this.state.turnOff(this); // 调用当前状态的关闭方法
  }
}

// 创建抽象基类 State
class State {
  constructor() {
    if (this.constructor === State) throw new Error("Abstract!"); // 防止直接实例化
  }
  turnOn(sw) {
    console.log("The light is on.");
  }
  turnOff(sw) {
    console.log("The light is off.");
  }
}

// 创建 Switch 类的实例并测试其方法
let lightSwitch = new Switch();
lightSwitch.turnOn(); // 打开灯
lightSwitch.turnOff(); // 关闭灯
```

### 模板方法模式

将算法的骨架定义为抽象类，指定其执行方式。

模板方法是超类（通常是抽象超类）中的一个方法，它通过一系列高层步骤定义了操作的骨架。

示例：

以国际象棋游戏为例。模板方法设计模式是一种设计模式，它在超类中定义算法的骨架，但允许子类在不改变整体结构的情况下实现算法的某些步骤。以下是逐步代码：

步骤 1：我们创建基类 `Game`，它将作为游戏的骨架，并定义游戏的总体流程。

```javascript
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
```

步骤 2：我们创建继承自 `Game` 的 `Chess` 类，并自定义国际象棋游戏的特定细节，例如玩家数量和最大回合数。

```javascript
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
```

步骤 3：我们创建 `Chess` 类的一个实例，并通过调用 `execute` 方法执行游戏。

```javascript
let chess = new Chess();
chess.execute();
```

这个示例演示了模板方法设计模式如何用于在基类 `Game` 中定义游戏的总体流程，以及如何在 `Chess` 类中自定义具体的游戏细节。

最终代码：

```javascript
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

// 预期输出：
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
```

在结束“JavaScript 高级设计模式”之际，请记住：你的编程之旅永无止境。JavaScript 的灵活性支持复杂的设计模式，从而提升代码质量。

继续迎接挑战，分享知识，并参与 JavaScript 社区。参加活动，保持与时俱进，并做出贡献。

感谢你选择我们的资源。你的潜力无限；每一行代码都在塑造数字世界。祝你在 JavaScript 的冒险中取得成功！

了解更多，请访问

www.hernandoabella.com

