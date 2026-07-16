# 每个 JavaScript 开发者应该了解的 ECMAScript 2015 (OdeToCode 编程系列)



![](img/cover.jpeg)




![otc300](img/00001.jpeg)



# 欢迎

我坐下来写了这本书，我想读关于 2015 年 JavaScript 的新特性。这本书并不是 ECMAScript 2015 规范中包含的所有内容的详尽列表。相反，我特意挑选了我们在日常编程中使用的重要特性。预计读者在 2015 年之前已经很熟悉 JavaScript 语言。书中的代码示例使用 Jasmine 测试框架编写的，以验证我对代码如何工作的假设。特别感谢 Ruben Bartelink 和 Porter T 的反馈。希望你喜欢后续的内容。

# 变量与参数

JavaScript 的变量作用域多年一直是惊喜和 Bug 的来源。ECMAScript 2015 引入了许多新关键字和处理局部变量与函数参数的语法糖。这些特性让 JavaScript 代码更具表现力、更容易使用，并且更安全。

## let

JavaScript 的变量作用域只提供函数作用域和全局作用域来控制变量的生命周期，这一直是一个意外。

```javascript
var doWork = function(flag){
    if(flag) {
      var x = 3;
    }
    return x; // x 仍然可用
};

var result = doWork(true);
expect(result).toBe(3); // 通过通过
```

2015 年新的 `let` 关键字将取代变量声明中的 `var` 并提供块级作用域。

```javascript
let doWork = function(flag) {
    if(flag){
      let x = 3;
    }
    return x; // ReferenceError: x 未定义
};

let result = doWork(true);
expect(result).toBe(3);
```

迭代语句也受益于 `let`。

```javascript
var doWork = function(){
    for(let x = 0; x < 3; x++) {
        // ...
    }
    return x; // ReferenceError: x 未定义
};
```

### 使用 let

ES2015 仍然支持 `var` 关键字，但在编写新代码时，我们应该将 `var` 视为过时的关键字。`let` 是新的 `var`！

`let` 会让 JavaScript 代码变得更好吗？我不确定 `let` 能防止大量的 Bug，但我认为 JavaScript 代码会改进。我们可以在使用变量的地方声明它们，这使得代码更容易追踪。

## const

`const` 关键字将为你提供只读变量。像 `let` 一样，用 `const` 声明的变量具有块作用域，且你不能重新声明它。

```javascript
const MAX_BIES = 3;
```

常量并不要求大写，这只是我喜欢的习惯。

### 使用 const

在完美的世界里，所有的 JavaScript 环境都应该对 `const` 有完美的实现。遗憾的是，`const` 是那些在官方 ECMAScript 规范出现之前就已经存在某些运行时中的关键字之一。

虽然大多数运行时都同意 `const` 应该是常量，但它们对于代码尝试给常量赋值新值时的行为存在分歧。应该导致运行时错误吗？还是静默失败？

官方规范说，如果程序尝试给常量赋值新值，`const` 应该产生运行时错误，而没有初始化器的常量声明应该是语法错误。

```javascript
const MAX_SIZE = 10;
// MAX_SIZE = 12; // 如果执行，会导致 SyntaxError
```

我希望所有的运行时和浏览器很快就能正常并正确运行。目前的情况不应该阻止你尽可能使用 `const`，因为该关键字确实有几个优点：

1. `const` 告诉其他程序员变量的意图行为，这使得脚本更容易维护。
2. `const` 告诉运行时变量的意图行为，允许在时间和空间进行优化。

## 默认参数

如果一个 JavaScript 函数接受两个参数，我们一直都有调用函数并传递两个参数、一个参数、零参数或在我们需要时传递三个参数的能力。在传递参数不足的情况下，函数的作者可能希望指定一个默认值，而不是处理 `undefined`。

在 2015 年之前，开发者在函数内部使用 `||` 表达式给传入的参数应用默认值。在以下函数中，如果调用没有没有 `name` 参数传递值，代码将分配默认值 Scott。

```javascript
let doWork = function(name) {
    name = name || "Scott";
    return name;
};
```

在 2015 年，默认值是显式的，并出现在函数的参数列表中。

```javascript
let doWork = function(name = "Scott") {
    return name;
};

expect(doWork()).toBe("Scott");
```




函数甚至可以使用字面量表达式以外的内容来计算默认值。

```javascript
let doWork = function(x = Math.random()) { return x; }
```

默认参数语法是 ES2015 如何为常见需求提供整洁语法的良好示例。我们再也不需要扫描函数的源代码或文档来发现默认值了。

当然，并不是所有参数都是简单的值。对于涉及复杂配置（如 HTTP 调用）的操作，一种常见的编程技术是接受单个对象参数，通过其属性来设置 URI、HTTP 方法、超时设置等。默认参数在这种情况下也很有用，但我们必须等稍后，先学习对象解构。

## 剩余参数 (Rest Parameters)

剩余参数允许函数处理数量数量的参数。函数的剩余参数始终出现在参数列表的末尾，并使用三个点前缀（`…`），如下所示。

```javascript
let doWork = function(name, ...numbers){
    let result = 0;
    numbers.forEach(function(n){
        result += n;
    });
    return result;
};
```

调用 `doWork` 的调用者可以在剩余参数位置传递零个或多个参数。你可以说 `numbers` 参数将获取调用者传递给 `doWork` 的“剩余”参数，并且 `numbers` 将这些参数存储在一个数组中。在下面的示例中，`numbers` 将引用包含值 1, 2, 3 的数组。

```javascript
let result = doWork("Scott", 1, 2, 3);
expect(result).toBe(6);
```

当调用者在剩余参数位置未传递参数时，剩余参数将是一个空数组。

```javascript
let doWork = function(...numbers){
    return numbers;
};

let result = doWork();
expect(result.length).toBe(0);
```

在 2015 年之前，我们可以通过使用函数内部隐式的 `arguments` 变量允许调用者向函数传递数量数量的参数。`arguments` 变量以类数组的形式包含了函数的所有参数，但 `arguments` 并不是一个数组，这造成了混惑。如果不阅读函数的代码或文档，很难发现一个函数是否使用了 `arguments`。

剩余参数将通过始终为我们提供真正的数组来避免混惑，并通过通过专门的语法，使得在阅读函数签名时剩余参数易于被发现。

## 展开运算符 (Spread Operator)

展开运算符与我们在剩余参数中看到的语法相同，即一系列三个点（`...`）。然而，剩余参数是将单个参数收集到一个数组中，而展开运算符则是将数组展开为多个单个参数。我们可以在定义函数时使用剩余参数，并在调用函数时使用展开运算符。例如：

```javascript
let doWork = function(x, y, z) {
    return x + y + z;
}

let result = doWork(...[1, 2, 3]);
expect(result).toBe(6);
```

在上面的代码中，展开运算符将包含三个值的数组“展开”到参数 `x`、`y` 和 `z` 上。

展开运算符还可以展开数组以在数组字面量中创建单个元素。

```javascript
let a = [4, 5, 6];
let b = [1, 2, 3, ...a, 7, 8, 9];
expect(b).toEqual([1,2,3,4,5,6,7,8,9]);
```

尽管我展示的示例都使用数组配合展开运算符，但展开运算符也适用于任何迭代对象（iterable object）。我们将在书的稍后部分查看迭代对象。

展开运算符还使得在不在乎实际参数值时，将参数传递给另一个函数变得简单（在那种情况下，我们通常会使用 `Function.apply`）。下面的 `doSomething` 方法展示了这种情况。

```javascript
let doWork = function(x, y, z){
    return x + y + z;
}

let doSomething = function(...args){
    return doWork(...args);
}

let result = doSomething(...[1,2,3,4,5]);
expect(result).toBe(6);
```

注意，当使用展开时，数组中的值可以比目标函数需要的更多。展开将从数组的开始填充参数，因此在上面的示例中，`doWork` 只会看到数组中的前三个值。

## 解构 (Destructuring)

解构一个对象就是拆解或撕开一个对象——这与构造（constructing）相反。

在 2015 年，解构赋值允许我们将一个数组或对象拆分成各个部分，并将这些部分赋值给变量。方括号 `[` 和 `]` 用于解构数组，而花括号 `{` 和 `}` 将用于解构对象。

下面的代码将解构一个数组，使得 `x` 包含 22，`y` 包含 44。

```javascript
let values = [22, 44];
let [x, y] = values;
expect(x).toBe(22);
expect(y).toBe(44);
```

你可以将赋值右侧的 `[` 和 `]` 视为构造数组的符号。赋值左侧的 `[` 和 `]` 解构数组并声明两个变量来持有这些部分。

对象的解构遵循相同的模式，但将使用 `{` 和 `}`。

```javascript
let person = { firstName: "Scott", lastName: "Allen" };
let {firstName, lastName} = person;
expect(firstName).toBe("Scott");
expect(lastName).toBe("Allen");
```



## 模板字符串

模板字符串为 JavaScript 提供了字符串格式化能力。与许多模板技术一样，JavaScript 中的模板由字面量和占位符组成，运行时可以在占位符处评估表达式并将数据替换到字面量中。

```javascript
let name = "Scott";
let message = `Hello, ${name}!`;
expect(message).toBe("Hello, Scott!");
```

反引号（`` ` ``）包围整个模板字符串，而 `$` 和 `{}` 则表示替换占位符。在占位符内部，你可以使用标识符和表达式。

```javascript
let showTheMath = function(x,y ){
    return `${x} + ${y} is ${x + y}`;
};

let result = showTheMath(3,4);
expect(result).toBe("3 + 4 is 7");
```

模板字符串也可以跨行。

```javascript
let message = `This is
               a short, but multi-line message`;
```

注意 `message` 将包含一个换行符，因为换行符（以及末尾空格）在模板字符串内部是有意义的。

模板字符串是该语言的一个非常有用的补充。然而，当模板字符串与标签（tag）一起使用时，它们变得异常有趣。

## 标签模板字符串

标签是一个具有解释和处理模板能力的函数。标签出现在模板之前，因此在下面的代码中，标签是 `test`。

```javascript
let name = "Scott";
let result = test `Hello, ${name}!`;
```

在这个示例中，`test` 是我们将编写的一个自定义函数。运行时会调用标签函数并传递两个参数。第一个参数将是一个包含模板中字面量文本部分的数组。

```javascript
let test = function(literals, ...values) {
    expect(literals.length).toBe(2);   
    expect(literals[0]).toBe("Hello, ");
    expect(literals[1]).toBe("!");
    return "test";
};

let name = "Scott";
let result = test `Hello, ${name}!`;
expect(result).toBe("test");
```

上述代码中的模板 `Hello, ${name}!` 生成了一个包含两个字面量文本“Hello”和“!”）的数组。运行时正在为我们拆分模板，并向我们提供不含占位符的字面量文本。

标签函数的其余参数将包含解释后的替换值。如果你不知道模板中会出现多少个占位符，可以使用剩余参数（rest parameter）将所有值捕到一个数组中。这是另一个代码片段，展示了运行时如何传递所有的字面量文本和替换值。

```javascript
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
```

标签函数可以通过拼接字符串来构建模板的输出。对于每个字面量值，你可以将字面量追加到结果中，然后追加一个值。然而，标签可以使用任何它想要的逻辑来解释模板，因此如果标签想无论模板内容如何顾一切地返回字符串“test”，它是可以的（如上面的代码所做的）。标签也可以返回数字 42 或任何对象。

一个更合理的标签实现可能如下：

```javascript
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
```

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。

### 标签模板字符串的力量

标签 `upper` 构建的结果看起来就像模板字符串的正常评估一样，但在返回结果之前使用了 `toUpperCase()`，以确保结果使用所有大写字母。




```javascript
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
```

在底层，`class` 关键字正在为我们设置一个构造函数和原型对象，而我们过去学习的所有原型技巧仍然有效。例如，从原型对象中“借用”方法：

```javascript
class A {
    doWork() {
        return "complete!";
    }
}

var result = A.prototype.doWork.call();
expect(result).toBe("complete!");
```

`instanceof` 运算符也如预期地工作。

```javascript
class A {
    // …
}

var a = new A();

expect(a instanceof A).toBe(true);
expect(a instanceof Object).toBe(true);
```

最后，你仍然可以通过直接修改原型对象来增强类型。

```javascript
class A {
}

A.prototype.newMethod = function() {
    return "new!";
};

var a = new A();

expect(a.newMethod()).toBe("new!");
```

你可以将 `class` 关键字理解为创建构造函数和原型对象的语法糖。然而，`class` 关键字的内容比比我们所看到的更多。

## 静态方法 (Statics)

类可以包含一个或多个使用 `static` 关键字定义的方法。

```javascript
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
```

与其他具有静态类成员的语言一样，`static` 关键字将创建一个与类关联的方法，而不是与类的实例关联。换句话说，你只能通过类名访问静态方法。

`expect(Employee.convert).toBeDefined();`

`expect(new Employee().convert).toBeUndefined();`

静态方法无法通过 `this` 访问类实例上定义的字段、属性和方法。例如，`convert` 方法无法使用 `this.name` 来获取 `Employee` 对象的 `name` 字段，因为 `convert` 内部的 `this` 指针永远不会引用 `Employee` 对象。然而，静态方法通常非常有用，可以充工厂方法、转换方法或通用的类辅助方法。

`let person = { name: "Scott" };`
`let newHire = Employee.convert(person);`
`expect(newHire.name).toBe("Scott");`

在底层，静态方法与构造函数关联，而不是像我们在上一节看到的实例成员那样与原型对象关联。

```javascript
var Employee = function(name) {
    // ...
};

Employee.convert = function(thing) {
    // ...
};
```

## 继承 (Inheritance)

多年来，JavaScript 有多种构建类层次结构的方法。所有方法都是通过组合构造函数和原型对象来实现工作的，并且每种方法都略有不同。

ES2015 允许使用 `class` 和 `extends` 关键字以声明式、一致的方法进行继承。作为一个示例，让我们从一个简单的类开始，表示有一个名字的人。

```javascript
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
```

现在我们还需要一个类来表示既有名字又有职衔的员工。使用 `extends` 关键字，我们可以让 `Employee` 类继承自 `Person` 类，这意味着每个实例化为 `Employee` 的对象都将拥有 `Person` 可用的所有方法和属性。

```javascript
class Employee extends Person {
    get title() {
        return this._title;
    }
    set title(newTitle) {
        this._title = newTitle;
    }
}

var e1 = new Employee();
e1.name = "Scott"; // 继承自 Person
e1.title = "Developer";
expect(e1.name).toBe("Scott");
expect(e1.title).toBe("Developer");
expect(e1 instanceof Employee).toBe(true);
expect(e1 instanceof Person).toBe(true);
```

在描述 `Employee` 和 `Person` 的关系时，我们经常说 `Person` 是 `Employee` 的超类，而 `Employee` 是 `Person` 的子类。我们也可以说每个实例化为 `Employee` 的对象都将拥有 `Person` 可用的所有方法和属性。（等等，原文在此处有一些重复/混乱的句子，我将保持核心逻辑）。

*注：提供的源码在继承部分包含大量的重复和混乱的文本。我在保留技术解释的同时，清理了逻辑流顺度。*

在描述 `Employee` 和 `Person` 的关系时，我们经常说 `Person` 是 `Employee` 的超类，而 `Employee` 是 `Person` 的子类。我们也可以说每个实例化为 `Employee` 的对象都将拥有 `Person` 可用的所有方法和属性。




JavaScript 一直以来都是函数式编程语言。你可以将函数作为参数传递给其他函数，也可以调用一个返回函数的函数。`ES2015` 标准通过提供一种创建函数的全新简洁语法，增强了 JavaScript 的函数式编程能力。此外，`2015` 还引入了与函数式编程密切相关的新特性，如迭代器（iterators）和惰性求值。让我们通过箭头函数来观察这些新功能，对于任何接触过 CoffeeScript 或 C# 代码的人来说，它看起来都很熟悉。

# 箭头函数

箭头函数是一种具有简洁语法的函数表达式。箭头函数不需要 `function` 关键字、大括号或 `return` 语句。然而，箭头函数需要一种新的运算符 `=>`，它看起来像一个指向右侧的箭头，并为这些表达式命名。要构建一个用于两个数字相和的箭头函数，只需编写以下代码：

```
let add = (x,y) => x + y;
```

箭头的左侧是函数的参数列表。在这个例中，有两个参数`x`和`y`。箭头的右侧是函数的待执行代码。在这种情况下，代码返回`x`和`y`之和。你可以将箭头理解为将参数指向使用它们的代码。

调用箭头函数看起来与调用传统函数没有区别。

```
let result = add(3, 5);

expect(result).toBe(8);
```

仅使用一个函数参数的箭头函数不需要在参数周围加上括号。

```
let square = x => x * x;
```

如果箭头函数需要零个参数或多个参数，则必须使用括号。

```
let add = (x,y) => x + y;             // 必须有括号
let square = x => x * x;             // 括号可选
let compute = () => square(add(5,3)); // 必须有括号

let result = compute();

expect(result).toBe(64);
```

到为止，示例在箭头运算符右侧都使用单个表达式。当使用单个表达式时，不需要大括号和 `return` 语句。函数的返回值将是该表达式的值。

然而，箭头函数可以包含更复杂的语句块，但这种方法需要大括号和显式的 `return`（如果函数想要返回一个值）。

```
let add = (x,y) => {
    var result = x + y;
    return result;
};
```

## 箭头函数与 this

每个 JavaScript 程序员都知道 `this` 指针有点难以捉摸。考虑以下类中的代码，特别是 `doWork` 内部的代码。

```javascript
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
```

`doWork` 方法传递给 `setTimeout` 的匿名函数的执行上下文与 `doWork` 本身不同，这意味着`this` 引用会发生。当匿名函数将 `this.name` 传递给 `callback` 时，`this` 将不再指向 person 对象，下面的测试将会失败。

```javascript
var person = new Person("Scott");
person.doWork(function(result) {
    expect(result).toBe("Scott"); // 失败！
    done();
});
```

由于在涉及异步代码和回调时，开发者永远无法依赖 JavaScript 的 `this` 引用，一种常见的做法是将`this`的值捕获在一个局部变量中，并用该变量代替`this`。捕获`this`的常用变量名有`self`、`me`或`that`。

```javascript
doWork(callback) {
    var self = this;
    setTimeout(function() {
        callback(self.name);
    }, 15);
}
```

得益于变量`self` 捕获了`this`引用，上面的代码将通过。

如果我们在 `doWork` 中使用箭头函数，就不再需要捕获`this`引用。

```javascript
doWork(callback) {
    setTimeout(() => callback(this.name), 15);
}
```

之前的测试将通过，因为箭头函数会自动从外部父函数中捕获`this`的值。换句话说，箭头函数内部的`this`值始终与箭头所在闭包函数中的`this`值相同。不再需要使用`self`或`that`，你可以任意深度地嵌套箭头函数，以便在一系列异步操作中保留`this`。

## 每天使用箭头函数

如果你接受了箭头函数的语法，你可能会发现自己每三行代码就会用一次箭头函数。JavaScript 对异步操作的偏睐创建了大量需要回调函数的 API。然而，由于 JavaScript 是一门强大的函数式编程语言，也出现了越来越多带有函数的同步 API。

例如，上一个版本的 ECMAScript 在数组上引入了`forEach`和`map`方法。

```javascript
let result = [1,2,3,4].map(n => n * 2);
expect(result).toEqual([2,4,6,8]);

let sum = 0;
[1,2,3,4].forEach(n => sum += n);
expect(sum).toBe(10);
```

还有许多库（Underscore 和 Lodash 是两个）使用高阶函数来实现过滤、排序和分组。

```javascript
let characters = [
    { name: "barney", age: 36, blocked: false },
    { name: "fred", age: 40, blocked: true },
    { name: "pebbles", age: 1, blocked: false }
];

let result = _.find(characters, function(character) {
    return character.age < 40;
});
```

使用箭头函数后，结果计算变得具表现力。
let result = _.find(characters, character => character.age < 40);
expect(result.name).toBe("barney");

it("can work with Jasmine", () => {
    var numbers = [1,3,4];
    expect(numbers.length).toBe(3);
});
```

最后几个示例都是针对数组操作的，数组是一种集合类型。`2015`还为 JavaScript 引入了迭代器（iterators）和迭代器（iterables）的概念，这些新特性将使集合操作变得明显灵活且可靠。

# 迭代器

`2015` 中迭代器的引入为 JavaScript 开启了新的算法和能力世界。迭代器是一个允许代码遍历对象序列的对象。对象序列可以是数组内部的值，也可以是复杂数据结构（如树或 map）中的值。迭代器的许多优秀特性之一是迭代器不需要了解底层集合的任何细节。迭代器做的只是提供一次遍历序列的能力。

你可能在奇怪为什么我们在关于函数式编程的章节中讨论迭代器。稍后我们会解释，但简单来说，迭代器与许多函数式编程范式配合良好，包括惰性求值和函数组合。在讨论这些主题之前，让我们看看迭代器的基本特性。

在 `ES6` 中，数组对象可以使用一些新方法，其中一个方法就是`values` 方法。`values` 方法返回一个可以访问数组中每个值的迭代器对象。

```javascript
let sum = 0;
let numbers = [1,2,3,4];
let iterator = numbers.values();
let next = iterator.next();

while(!next.done){
    sum += next.value;
    next = iterator.next();
}

expect(sum).toBe(10);
```

迭代器是一个具有`next`方法的对象。程序每次调用`next`方法，该方法都会返回一个包含两个属性的对象：`value`和`done`。`value`属性代表迭代器当前在集合中访问的项目。`done`属性是一个标志位，如果还有项目可以访问，其值为`false`；如果已经过了最后一个项目并完成，则值为`true`。

## 使用 for of 循环




在底层操作迭代器有时是有帮助的，正如我们在这一章中看到的，但 2015 还提供了一种新的循环语法，用于在更高层级处理迭代器——`for of` 循环。

```javascript
let sum = 0;
let numbers = [1,2,3,4];
for(let n of numbers) {
    sum += n;
}
expect(sum).toBe(10);
```

关于上述代码有几点观察。

首先，新的 `for of` 循环看起来像 JavaScript 一直以来存在的 `for in` 循环，但这两种循环的行为不同。`for in` 循环作用于任何对象的可枚举属性。在处理数组时，`for in` 会遍历数组的可用用索引，而不是可用的值。要使用 `for in` 计算出与上述代码相同的和，我们需要在每次迭代时通过索引来访问数组：

```javascript
let sum = 0;
let numbers = [1,2,3,4];
for(let i in numbers) {
    sum += numbers[i]; // 注意这里的索引器
}
expect(sum).toBe(10);
```

`for of` 循环使用迭代器来访问数组中的值，而不是可用的键。

```javascript
for(let n of numbers) {
    sum += n;
}
```

这引出了与 `for of` 的第二个微妙区别。`for of` 循环只适用于可迭代对象。可迭代对象是具有返回迭代器的特殊方法的对象。我们很快会看到这个特殊方法，但注意最后一段代码不需要像我们之前编写的底层迭代器代码那样使用数组的 `values` 方法。相反，`for of` 循环直接使用了 `numbers` 数组。

在 ES6 的世界中有很多对象是可迭代对象，我们将在书中看到更多。我们已经看到数组是如何可迭代的。字符串也是可迭代的，这意味着你可以遍历内部的字符序列。

```javascript
let result = "";
let message = "Hello";
for(let c of message) {
    result += c;
}
expect(result).toBe("Hello");
```

`for of` 如何获取迭代器？是什么让一个对象变得可迭代的？为了回答这两个问题，我们必须简要跳转到 ES2015 的另一个新特性——`symbol`。

## Symbols（符号）

Symbol 是 ES2015 中的一种新原始数据类型。关于 symbol 有两个点需要理解。

1. 每个 symbol 唯一的且不可变的。
2. 在向对象添加属性时，可以使用 symbol 作为标识符。

为了理解这两个陈述的含义以及它们与可迭代对象的关系，让我们从创建一个新的 symbol 开始。创建一个新的 symbol 与调用 `Symbol` 函数一样简单。

```javascript
let s = Symbol();
expect(typeof s).toBe("symbol");
```

注意，在创建 symbol 时不需要使用 `new` 运算符。要创建 symbol，你需要调用 `Symbol` 函数。否则，运行时将抛出异常。

```javascript
let makeSymbol = () => new Symbol();
expect(makeSymbol).toThrow();
```

你创建的每个 symbol 都是唯一且不可变的。

```javascript
let s1 = Symbol();
let s2 = Symbol();
expect(s1).toEqual(s1);
expect(s1).not.toEqual(s2);
```

创建一个 symbol 时，可以通过向 `Symbol` 函数传递一个字符串来添加描述，但用相同描述创建的 symbol 仍然是唯一的，即使它们的字符串版本看起来一样。

```javascript
let s1 = Symbol("some desciption");
let s2 = Symbol("some description");
expect(s1).toEqual(s1);
expect(s1).not.toEqual(s2);
expect(s1.toString()).toBe("Symbol(some description)");
expect(s2.toString()).toBe("Symbol(some description)");
```

你可以使用 symbol 作为对象的键。在下面的代码中，我们使用 `lastName` 创建了一个属性，并用 symbol 创建了另一个属性（`firstName` symbol）。

```javascript
let firstName = Symbol();
let person = {
    lastName: "Allen",
    [firstName]: "Scott",
};
expect(person.lastName).toBe("Allen");
expect(person[firstName]).toBe("Scott");
```

由于 symbol 是唯一的，一个 symbol 可以在对象内部创建一个唯一的属性。你永远不需要担心与现有方法冲突，或被意外覆盖。ES5 库会使用带有时间戳或随机数数的属性名来实现相同的效果，但 symbol 提供了更安全的保障。

使用 symbol 创建的对象成员在使用 `for in` 循环时不会作为对象的一部分出现。

```javascript
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
```

在使用 `Object.getOwnPropertyNames` 时，symbol 也不会出现。

```javascript
expect(Object.getOwnPropertyNames(person)).toEqual(["lastName"]);
```

将对象序列化为 JSON 时，它们也不会出现。

```javascript
expect(JSON.stringify(person)).toBe('{"lastName":"Allen"}');
```

由于这些原因，你可能会认为 symbol 对于隐藏对象中的信息很有用。尽管使用 symbol 隐藏信息是有用的，但我们有一个名为 `getOwnPropertySymbols` 的新方法可以做到。

```javascript
expect(Object.getOwnPropertySymbols(person)).toEqual([firstName]);
let symbol0 = firstName;
expect(person[symbol0])[0]).toBe("Scott");
```

现在我们更多地了解 symbol，让我们看看 symbol 与可迭代对象的关系。

### 可迭代对象与符号

ES2015 定义了几个已知的 symbol。运行时环境使用这些已知的 symbol。其中一种已知的 symbol 是 `Symbol.iterator`。接下来的代码将检查字符串、数组和数字是否是迭代的。

```javascript
let site = "OdeTo.com";
let values = [1,2,3,4];
let number = 45;
expect(site[Symbol.iterator]).toBeDefined();
expect(values[Symbol.iterator]).toBeDefined();
expect(number[Symbol.iterator]).toBeUndefined();
```

证明字符串和数组是可迭代的，但数字不是。

当我们使用 `for of` 循环时，如下例所示，运行时在后台使用 `Symbol.iterator` 获取迭代器。

```javascript
let sum = 0;
let numbers = [1,2,3,4];
for(let n of numbers) {
    sum += n;
}
expect(sum).toBe(10);
```

我们可以重写代码来表示正在发生的情况。

```javascript
let sum = 0;
let numbers = [1,2,3,4];
let iterator = numbers[Symbol.iterator]();
let next = iterator.next();
while(!next.done) {
    sum += next.value;
    next = iterator.next();
}
expect(sum).toBe(10);
```

利用你对 symbol 的知识编写底层迭代器代码并不有趣，但利用 symbol 创建新的可迭代对象是非常有趣的。

## 创建可迭代对象

想象你正在为教室构建一个抽象，教室对象的一个职责是封装教室内学生的名字。你可能会构建这样一个类：

```javascript
class Classroom {
    constructor() {
        this.students = ["Tim", "Joy", "Sue"];
    }
}
```

偶尔，外部世界需要知道教室内部学生的名字。也许程序会在 UI 中显示这些名称，或者将它们保存到数据库中。无论哪种，教室对象如何向调用者提供学生名称？

一种方案是返回数组的引用，这样调用者可能会通过添加或删除项更改数组。如果教室想要保护数组并验证学生的的添加或删除，这种方案不是最佳选择。

另一个方案是复制数组。即使调用者更改了副本，原始学生数组也是安全的。然而，复制操作可能是昂贵的。

有了 ES2015，教室现在可以提供学生名称的访问，而无需交付底层数组的访问权限。我们只需要通过添加 `Symbol.iterator` 方法让教室变得可迭代即可。





首先，让我们通过构建自己的迭代器对象来让教室变得可迭代。这是解决该问题的硬核方法，在涵盖另外几个主题后，我们将看到更容易的方法。

```javascript
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
```

注意 `Symbol.iterator` 需要用方括号括起来方法名。方法内部是返回带有 `next` 方法对象的代码，而 `next` 方法返回带有 `done` 和 `value` 属性的对象。现在，教室的行为应该就像数组一样，并且可以在 `for...of` 循环中使用。

```javascript
let scienceClass = new Classroom();
let result = [];
for(let name of scienceClass){
    result.push(name);
}
expect(result).toEqual(["Tim", "Joy", "Sue"]);
```

教室迭代器方法内部的代码是适用于任何数组的代码。让我们将这些代码提取到一个新的类中。

```javascript
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
```

现在我们可以在应用程序的多个地方复用 `ArrayIterator`。

```javascript
class Classroom {
    constructor() {
        this.students = ["Tim", "Joy", "Sue"];
    }
    [Symbol.iterator]() {
        return new ArrayIterator(this.students);
    }
}
```

尽管 `ArrayIterator` 类很有帮助，但创建可迭代对象的更简单方法是使用生成器（generator）。

## 生成器

当你看到一个生成器函数时，你会知道它的，因为生成器函数在声明中包含一个星号。

```javascript
function*() {

}
```

一旦你有了生成器函数，就可以在函数内部使用 `yield` 关键字向调用者返回多个值。

```javascript
let numbers = function*() {
    yield 1;
    yield 2;
    yield 3;
};
```

然而返回值并不是一次性返回给调用者的。在内部，运行时构建一个迭代器，以便调用者逐个遍历生成器的结果。以下代码使用 `for...of` 循环来遍历 `numbers` 函数。

```javascript
let sum = 0;
for(let n of numbers()) {
    sum += n;
}
expect(sum).toBe(6);
```

回到上一节中使用的 `Classroom` 类，我们现在可以使用生成器函数和 `yield` 让 `Classroom` 可可迭代。

```javascript
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
```

注意 `iterator` 方法需要在方括号之前加上星号。这种语法很奇特，但在定义生成器函数时始终需要星号，因为生成器的行为与普通函数不同。

## 惰性求

大多数语言中的生成器执行的工作最少，但 JavaScript 中的生成器例外。当程序调用普通函数时，你可以想象程序跳进函数并执行直到函数完成。然而，生成器函数的行为是不同的。

例如，让我们使用以下生成器函数。

```javascript
let random = function*() {
    while(true) {
        console.log("make random")
        yield Math.random();
    }
}
```

`random` 函数看起来会在无限循环中消耗 CPU 周期。然而，如果我们调用函数并寻找输出——将没有任何输出！当你调用生成器函数时，可以认为运行时在后台设置了一个状态机。该状态机知道如何获取生成器函数内部的代码并允许按需执行片段。

是什么产生了需求？由于生成器产生迭代器，因此对迭代器 `next` 方法的每次调用都会强制状态机执行足够的代码来产生下一个值，但不再更多。例如，如果我们执行以下代码：

```javascript
let iterator = random();
iterator.next();
```

那么我们在控制台中恰恰看到一次“make random”。向迭代器请求下一个值强制状态机执行函数内部的代码，直到一个 `yield` 语句返回另一个值。每当调用 `next` 时，程序流都会跳回生成器函数程序上次离开的地方，并继续执行直到程序到达另一个 `yield`。

在计算机科学术语中，生成器函数提供了我们所说的惰性求值（lazy evaluation）。为了让函数执行工作，我们需要通过迭代器请求这些值来从函数中提取值。`random` 函数只有在我们请求无限数量的值时，才会创建一个无限循环。

假设我们想要有限数量的随机数，并且只要小于 0.5 的数字。首先，我们可以写一个 `filter` 函数，它接受一个可迭代对象和一个 `predicate`（谓词）函数作为参数。`filter` 函数只会产生 `predicate` 函数返回 true 的项。

```javascript
let filter = function*(items, predicate) {
    for(let item of items){
        console.log("filter", item);
        if(predicate(item)){
            yield item;
        }
    }
};
```

为了确保我们请求有限数量的项，我们还可以写一个 `take` 函数，获取特定数量的项。

```javascript
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
```

注意我们如何在 `take` 函数中使用 `return` 语句来停止迭代。

使用之前的函数（它们都是生成器），我们可以通过以下代码创建两个小于 0.5 的随机数。

```javascript
let result = take(filter(random(), n => n < 0.5), 2);
```

但是，上面的代码并没有创建任何数字！我们创建的只是一个迭代器。控制台中不会出现任何输出，因为没有代码尝试使用迭代器通过生成器拉取数字。

我们可以使用 `for...of` 循环强制函数执行代码，或者使用 `Array.from`，这是一个我们可以用来将任何可迭代对象转换为具体数组的新 API。

```javascript
expect(Array.from(result).length).toBe(2);
```

上述代码的控制台输出如下。

```
make random
filter 0.24152887403033674
take  0.24152887403033674
make random
filter 0.6618692250922322
make random
filter 0.49661534116603434
take  0.49661534116603434
```





```javascript
let range = function*(start, end) {
    let current = start;
    while(current <= end) {
        yield current;
        current += delta || 1;
    }
}
```

如果我们请求 `range` 为我们提供从一到十的数字，`range` 方法的行为将如我们预期。

```javascript
let result = [];
let iterator = range(1,10);
let next = iterator.next();
while(!next.done) {
    result.push(next.value);
    next = iterator.next();
} 
expect(result).toEqual([1,2,3,4,5,6,7,8,9,10]);
```

现在，让我们对 `range` 方法进行一些微小的更改。当我们 `yield` 当前值时，我们将 `yield` 表达式放在赋值表达式的右侧。

```javascript
let range = function*(start, end) {
    let current = start;
    while(current <= end) {
        var delta = yield current;
        current += delta || 1;
    }
}
```

当迭代器消费者调用 `next()` 方法并传递一个参数时，该参数将成为 `yield` 语句的返回值。`range` 方法将此返回值赋值给 `delta` 变量。如果消费者没有传递值，代码将 `delta` 的值默认设为 1。如果我们像以前那样遍历 `range`，我们仍然会看到相同的结果。

```javascript
let result = [];
let iterator = range(1,10);
let next = iterator.next();
while(!next.done) {
    result.push(next.value);
    next = iterator.next();
} 
expect(result).toEqual([1,2,3,4,5,6,7,8,9,10]);
```

然而，如果我们在每次调用 `next()` 方法时都传入数字 2，我们将实际上将迭代器中的 `current` 值加了 2 而不是 1。

```javascript
let result = [];
let iterator = range(1,10);
let next = iterator.next();
while(!next.done) {
    result.push(next.value);
    next = iterator.next(2);
} 
expect(result).toEqual([1,3,5,7,9]);
```

如果我们用硬核的方法（不使用 `yield`）来编写最新的 `range` 方法，它看起来可能会像下面。

```javascript
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
```

在此版本的代码中，更容易看到 `next()` 方法如何接收可以在迭代器逻辑中使用的参数。当使用 `yield` 时，参数作为 `yield` 表达式的返回值到达。此外，当使用 `yield` 实现 `range` 函数时，无法在第一次调用 `next()` 方法时捕获传入的参数。

## 委托 yield (Delegating Yield)

生成器方法可以调用生成器方法。生成器甚至可以使用 `yield*` 将另一个生成器的结果展开到自己的迭代器中。例如，考虑以下生成器方法。

```javascript
let inner = function*() {
    yield "Hello";
    yield "there";
}
```

`outer` 生成器将使用 `yield*` 调用 `inner` 生成器。

```javascript
let outer = function*() {
    yield* inner();
    yield "World";
}
let it = outer();
console.log(it.next().value); // "Hello"
console.log(it.next().value); // "there"
console.log(it.next().value); // "World"
```

`yield*` 语法允许生成器委托给另一个迭代器，从而简化了代码。





假设你需要调用该方法四次，并且每次调用 `calculate` 时，你都需要将上一次调的结果传递给下一次调用（这会模拟 HTTP API，其中你需要发送多个相互依赖的请求，以获取页面所需的所有数据）。使用 promise，这系列方法的调用可能如下所示。

```javascript
let verify = function(result) {
    expect(result).toBe(5);
    done();
};

calculate(1)
    .then(calculate)
    .then(calculate)
    .then(calculate)
    .then(verify);
```

上面的代码还（通过 Jasmine）验证了最终值为 5，因为 `calculate` 在每次被调用时都会在结果上加 1。代码之所以能够工作，是因为对 promise 的 `then` 方法的每次调用都会返回一个新的 promise。你可能认为这种现象是因为 `calculate` 方法返回了一个新的 promise，但即使传递给 `then` 方法的函数没有显式地产生 promise，新的 promise 也会出现。例如，让我们用一个简单返回 `result + 1` 的箭头函数替换其中一次对 `calculate` 的调用。

```javascript
calculate(1)
    .then(calculate)
    .then(result => result + 1)
    .then(calculate)
    .then(verify);
```

上述代码的结果仍然是值 5，且带有箭头函数的 `then` 调用返回的对象仍然是一个 promise。`then` 方法会在必要时通过创建一个新的 promise 包装器来确保返回值是一个 promise。如果成功处理程序没有返回任何值，新的 promise 将将值 `undefined` 传递给下一个处理程序。

# Promise API

JavaScript 中的 `Promise` 提供了几个你可以作为便利方法使用的静态方法。例如，如果你需要向一个调用者返回一个 promise，但你已经有一个值可以解析该 promise 而无需执行任何异步工作，那么 `resolve` 方法非常有用。

```javascript
let doAsyncWork = function () {
    // 注意：没有实际执行的异步工作
    return Promise.resolve(10);
};

doAsyncWork().then(result => {
    expect(result).toBe(10);
    done();
});
```

同样，`reject` 方法会将结果传递给错误处理程序。

```javascript
let doAsyncWork = function () {
    return Promise.reject("error!");
};

doAsyncWork().then(() => { }, message => {
    expect(message).toBe("error!");
    done();
});
```

`race` 方法将多个 promise 合并为一个单一 promise。当第一个通过的 promise 解析时，该单一 promise 就会解析。这是一场看谁先完成的竞赛！

```javascript
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
```

与 `race` 不同，`all` 方法将多个 promise 合并为一个单一 promise。当所有的 promise 都解析时，该单一 promise 就会解析。

```javascript
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
```

合并的结果以数组的形式呈现。数组中的结果顺序与传递给 `all` 方法的 promise 顺序相同。当然，并不是所有的 promise 都能成功解析，所以让我们谈谈错误处理。

## Promise 错误

异步代码中的错误通常需要数量大量的 `if else` 检查和对值的仔细检查。Promise 允许异步代码应用结构化的错误处理。使用 promise 时，你可以向 `then` 方法传递一个错误处理程序，或者使用 `catch` 方法来处理错误。就像普通代码中的异常一样，异步代码中的错误或异常将跳转到最近的错误处理程序。

例如，让我们使用以下函数，它们将执行情况记录在一个字符串变量中。

```javascript
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
```

我们将使用这些函数配合以下代码：

```javascript
doWork()
    .then(doWork)
    .then(doError)
    .then(doWork) // 这行将被跳过
    .then(doWork, errorHandler)
    .then(verify);

function verify() {
    expect(log).toBe("WWEH");
    done();
}
```

我们的预期是 `log` 变量将是 "WWEH"。当代码执行结束，`log` 变量包含 "WWEH"，这意味着我们看到了 `doWork`、`doError`、`errorHandler`。关于这个结果有两个观察点，一个是明显的，一个是微妙的。

第一个观察点是，当 `doError` 抛出异常时，执行会进入拒绝处理程序（`errorHandler`）并跳过任何成功处理程序。一旦你 promise 视为将异步代码转换为过程流的工具，这种行为就是显而易见的。

可能不显而易见的是，在处理了错误后，`verify` 函数会执行。正如同步代码在 `catch` 语句后可以恢复正常执行一样，在 promise 中处理了错误后也可以恢复正常执行。请记住，`then` 方法总是返回一个新的 promise，除非错误处理程序显式地拒绝一个新的 promise，否则新的 promise 将成功解析。

promise 对象还提供了一个 `catch` 方法来处理错误。我们可以用 `catch` 语句如下重写最后的代码示例：

```javascript
doWork()
    .then(doWork)
    .then(doError)
    .then(doWork)
    .catch(errorHandler)
    .then(verify);
```

`catch` 方法只接受拒绝处理程序方法。以下两个代码片段之间存在细微差异：

`.then(doWork, errorHandler)`
……以及……
`.then(doWork)`
`.catch(errorHandler)`

在第一个代码片段中，如果成功处理程序抛出异常或拒绝 promise，执行将进入错误处理程序，因为该 promise 在此层已经解析了。通过 `catch`，你始终可以看到来自上一个成功处理程序的未处理错误。

最后说明一点，如果你没有为 promise 操作设置任何错误处理程序而发生了错误，将没人知道！你可以通过以下行代码来模拟这种场景。

```javascript
Promise.reject("error!");
```

某些环境和 Promise 补丁会在开发者工具的控制台中显示消息来警告你未处理的拒绝。未处理的 promise 拒绝意味着你的应用程序可能丢失关键错误！

# 模块

避免全局作用一直是过去十年编写的每个库和框架的主要架构目标。在浏览器中避免全局作用意味着我们严重依赖闭包和诸如立即调用函数表达式（IIFE）之类的语法特性来提供封装。

```javascript
(function() {
    // 代码写在这里，在 IIFE 内部
}());
```



NodeJS 在 2009 年出现后，Node 开发者们发现自己正在创建更大的代码库，并消耗大量的库。为了管理这个新环境中的作用域和依赖问题，Node 社区创建了一个我们现在称为 CommonJS 模块标准的非官方标准。不久后，另一个社区标准——异步模块定义标准（AMD）为浏览器编程出现。

ES2015 为 JavaScript 语言引入了官方模块标准。该模块标准使用的语法与 CommonJS 和 AMD 都不同，但 WebPack 等工具和运行时补丁（polyfills）使得所有模块标准大部分情况下具有互操作性。在本文写作时，需要一些预处理或补丁才能使新的模块语法生效。尽管语言语法已经完整且标准化，但处理模块的浏览器 API 和行为仍在开发中。

## 为什么需要模块？

模块系统允许 JavaScript 代码在规模上扩展。模块通过提供几个重要的特性，为我们提供了管理大型代码库性的工具。

首先，JavaScript 中的模块是基于文件的。使用 ES2015 时，你不应该仅仅 true 一个脚本文件，而应该将其视为脚本模块。一个文件就是一个模块。默认情况下，你在文件中编写的任何代码都是该模块局部的。变量不再默认处于全局作用域，且无需编写函数或 IIFE（立即调用函数表达式）来控制变量的作用域。模块为我们提供了一个隐式作用域来隐藏实现细节。

当然，你在模块中编写的一些代码可能是你可能想要暴露为 API 并在另一个模块中使用的代码。ES2015 提供了 `export` 关键字来实现此目的。任何你想提供给外部世界的对象、函数、类或变量，都必须使用 `export` 关键字显式导出。

在第二个模块中，你将使用 `import` 关键字来使用第一个模块的部分或全部导出内容。

模块允许我们将代码分散在多个文件和目录中，同时可以在不通过全局中介的情况下引用和使用跨文件的组件。也许书中列出的其他特性中，没有哪个特性对应用、框架和库架构的影响能像模块这么大。让我们来看看语法。

## 模块语法

假设你想使用一个表示人的对象，并在名为 `humans.js` 的文件中放置了以下代码。

```javascript
function work(name) {
    return `${name} is working`;
}

export let person = {
    name: "Scott",
    doWork() {
        return work(this.name);
    }
}
```

由于我们正在处理模块，`work` 函数保持隐藏在模块作用域中，模块外的任何代码无法访问 `work` 函数。`person` 变量是模块的导出内容。更具体地说，我们称 `person` 为命名导出。其他模块的代码可以导入 `person` 并对引用的对象进行操作。

```javascript
import {person} from "./lib/humans"

describe("The humans module", function() {
    it("should have a person", function() {
        expect(person.doWork()).toBe("Scott is working");
    });
});
```

关于上面的代码段有几点需要说明。

首先，注意模块名 `./lib/humans` 不需要 `.js` 扩展名。文件名是 `humans.js`，但文件的模块名是 `humans`。

其次，在这个示例中，`humans` 模块位于测试代码的子文件夹。因此，模块指定符包含了指向模块的相对路径（`./lib/humans`）。

最后，大括号包围了来自 `humans` 模块的导入列表。导入之所以是一个列表，是因为你可以从另一个模块导入多个命名导出内容。例如，如果 `humans` 模块也导出了 `work` 函数，那么测试代码可以通过以下代码访问这两个导出内容。

```javascript
import {person, work} from "./lib/humans"
```

你还有能力将导入重命名为不同的名称。

```javascript
import {person as scott, work} from "./lib/humans"

describe("The humans module", function() {
    it("should have a person", function() {
        // 现在使用 scott 代替 person
        expect(scott.doWork()).toBe("Scott is working");
    });
    it("should have a work function", function() {
        expect(work).toBeDefined();
    });
});
```

除了导出变量、对象和函数外，你还可以导出一个类。假设 `humans` 模块具有以下代码。

```javascript
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
```

现在，测试代码看起来像这样。

```javascript
import {Person} from "./lib/humans"
describe("The humans module", function() {
    it("should have a person class", function() {
        var person = new Person("Scott");
        expect(person.doWork()).toBe("Scott is working");
    });
});
```

模块还可以使用大括号导出符号列表。例如，我们可以重写 `humans` 模块，并将所有导出内容放在文件底部的一个位置。

```javascript
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

export {Person, work }
```

注意导出列表可以重命名导出名称，所以 `work` 函数导出为 `worker`。

### 默认导出

2015 模块标准允许每个模块有一个默认导出。模块可以拥有默认导出并导出其他名称，但拥有默认导出会影响另一个模块如何导入它。首先，这是 `humans` 模块带有 `Person` 类默认导出时的样子。

```javascript
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
```

如代码所示，导入另一个模块默认导出的模块不需要大括号指定绑定列表。相反，模块只需为导入的默认定义一个名称，且该名称不需要与模块内部使用的名称匹配。

```javascript
import Human from "./lib/humans"
describe("The humans module", function() {
    it("should have a default export as a class", function() {
        var person = new Human("Scott");
        expect(person.doWork()).toBe("Scott is working");
    });
});
```

### 批量导出导入

导入语句可以使用星号捕获模块的所有命名导出。让我们再次更改 `humans` 模块，将 `Person` 类同时作为命名导出和默认导出导出。

```javascript
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
```

测试代码现在可以使用 `*` 访问 `humans` 模块的所有命名导出。对导出的访问将通过 `humans` 进行，它的行为类似于其他语言中的命名空间。

```javascript
import * as humans from "./lib/humans"
describe("The humans module", function() {
    it("should have a person class", function() {
        var person = new humans.Person("Scott");
        expect(person.doWork()).toBe("Scott is working");
    });
});
```





```javascript
it("should have a default export", function() {
    expect(humans.default).toBeDefined();
});
```

注意看测试代码现在有两个路径可以到达 `Person` 类。一条路径是通过 `humans.Person`，另一条路径是 `humans.default`。

`export` 语句也可以使用星号 `*`。当你希望一个模块收集许多子模块的导出内容，并将它们作为一个单元一起发布时，星号就非常有用。在 CommonJS 中，这种场景通常使用命名为 `index.js` 的文件，许多现有的模块加载器补丁（polyfills）都支持在导入目录时使用 `index.js` 文件。例如，让我们在 `lib` 文件夹中添加一个名为 `creatures.js` 的文件。

```javascript
export class Animal {
    constructor(name) {
        this.name = name;
    }
}
```

现在 `lib` 文件夹中的 `index.js` 文件可以将 `humans` 和 `creatures` 模块合并为一个单一模块。

```javascript
export * from "./creatures"
export * from "./humans"
```

测试代码现在可以导入 `lib` 目录并访问两个底层模块的特性。

```javascript
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
```

### 为了副作用而导入

最后，`import` 语句不需要命名任何导入内容。在某些情况下，你只想引用一个模块，以便其内部代码可以执行并在环境中产生副作用。

```javascript
import "./lib"
```

# APIs

在最后一个章节中，我想重点介绍一些我认为非常重要的新类型和 API。

## 新集合 (New Collections)

JavaScript 从未提供过多样化的数据结构。如果你需要任何数组更复杂的结构，你必须自己实现或借用一些代码。

2015 规范为语言引入了许多键值集合（keyed collections），包括 `Map`、`Set`、`WeakMap` 和 `WeakSet`。

### Maps

虽然你可以将任何 JavaScript 对象视为字典或键值存储器，但它存在一些缺点。最明显的是，你可以用于索引对象的唯一键类型是字符串或 symbol 类型的键。新的 `Map` 集合消除了对键类型的限制，并提供了一些额外的便利。该 API 的核心围绕 `get` 和 `set` 方法展开。

```javascript
let map = new Map();
// 添加一个新的键值对
map.set("key", 301);
// 覆盖已存在的值
map.set("key", 302);
expect(map.get("key")).toBe(302);
```

`delete` 和 `has` 方法也非常好用。

```javascript
let map = new Map();
map.set("key", 611);
expect(map.has("key")).toBe(true);
map.delete("key");
expect(map.has("key")).toBe(false);
```

现在键可以是任何类型的对象。

```javascript
var someKey = { firstName: "Scott"};
var someValue = { lastName: "Allen"};
var map = new Map();
map.set(someKey, someValue);
expect(map.size).toBe(1);
expect(map.get(someKey).lastName).toBe("Allen");
expect(map.get({firstName:"Scott"})).toBeUndefined();
```

当使用对象作为键时，JavaScript 会在后台比较指针，如上面的代码所示。

你也可以使用键值对的二维数组构造一个 `Map`。

```javascript
let map = new Map([
    [1, "one"],
    [2, "two"],
    [3, "three"]
]);
```

最后，map 有多种迭代方式。你可以获取键的迭代器（使用 `keys()` 方法）、值的迭代器（使用 `values()` 方法）以及键值对迭代器（使用 `entries()` 方法，正如你可能猜的那样）。map 还有一个神奇的 `[Symbol.iterator]` 方法，因此你可以在 `for...of` 循环中使用 map。

```javascript
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
```

在 `for...of` 循环中，每个项目以数组形式输出，`index 0` 是键，`index 1` 是值。这是一个数组解构非常实用的场景。

```javascript
for(let [key, value] of map) {
    sum += key;
    combined += value;
}
```

### Set

`Set` 是一个唯一值的集合。像 `Map` 一样，你可以遍历它并检查某个值是否存在。

```javascript
let set = new Set();
set.add(1);
set.add(2);
expect(set.has(1)).toBe(true);
set.delete(1);
expect(set.has(1)).toBe(false);
```

### 弱集合 (Weak Collections)

`WeakMap` 和 `WeakSet` 是 `Map` 和 `Set` 的“弱”版本。如果对象在程序的其他地方没有被引用，它们允许对键/值进行垃圾回收，从而在某些场景下防止内存泄漏。

```javascript
let wm = new WeakMap();
let obj = { name: "test" };
wm.set(obj, "value");
console.log(wm.get(obj));
```





```javascript
expect(result.a).toBe(1);
expect(result.b).toBe(2);
```

运行时会按照左到右的拷贝属性，并用同名的属性覆盖现有属性。

```javascript
let a = { a: 1};
let b = { b: 2};
let a2 = { a: 2, foo:"baz"};
let result = Object.assign({foo:"bar"}, a, b, a2);
```

```javascript
expect(result.a).toBe(2);
expect(result.b).toBe(2);
expect(result.foo).toBe("baz");
```

# 结束

衷心感谢你购买并阅读本书。祝你在软件开发及其他领域一切顺利。

***[[1]](#part0000_split_004.html__ftnref1) 关于悬挂内容：`try/catch` 块可以有效模拟块级作用域，但在可读性代码中，通过 `try` 和 `catch` 来控制作用域是一种拙劣的权宜之计。

