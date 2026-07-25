# Javascript 元编程






## 这是什么？

> “编写那些编写或操纵其他程序（或自身）作为其数据的计算机程序”

## 用 JavaScript 实现？！

- 体小而精悍但被广泛误解
- 依赖于少数但强大的构造结构
- 你可以在运行时与函数、参数、内置类型以及继承等机制进行操作
- 这些技术支撑了许多 JS 库

## 揭秘 JavaScript：失控的对象！

## 一来尝试吧！

```javascript
>>> var add = function(a, b) { return a + b }
>>> add(2,3)
5
>>> typeof add
"function"
>>> function adder(a) { return function(b) { return add(a, b) } }
>>> addS = adder(5)
function()
>>> addS(10)
15
>>> typeof addS
"function"
```

## 4 个构建块

### （几乎）一切都是哈希表 (hash)

数字 (number)
字符串 (string)
布尔值 (boolean)
未定义 (undefined)

### 其他所有都是对象 (Object)

```javascript
var myObj = new Object;
myObj['myProperty'] = 454;
myObj[45435] = true;
myObj[true] = 'hello';
```

# 这对任何对象有效

```javascript
var now = new Date;
now[5] = 'hello!';

console.log(now[5]); //=> 'hello!'
```

### 访问器 (Accessors)：一种特殊情况

```javascript
location['thing'] = 'a';
// 等同于...
location.thing = 'a';

console.log(location['thing']);
console.log(location.thing);
// => 'a'
```

```javascript
// 坏做法！
eval("window.forms." + form + ".reset()");

// 好做法！
window.forms[form].reset();
```

```javascript
var tags = ['a', 'div', 'span', 'p'];

for (var i, l = tags.length; i < l; i++)
    find[tags[i] + 'Elements'] = createFinder(tags[i]);

find.aElements();
find.pElements();
// 等此类推...
```

### 检查对象

```javascript
var person = {
  name: 'Bob',
  email: 'bob@bob.com',
  tel: '0258305964'
};

for (var key in person) {
  console.log(key);
} //=> 'name', 'email', 'tel'
```

```javascript
// 使用上一个示例中的 
// person 对象...
if ("tel" in person) {
  alert(person.tel);
}
```

### 检查类型

```javascript
var a = 5;
typeof a //=> 'number'
var name = 'Sam';
typeof name //=> 'string'
typeof doesntExist //=> 'undefined'
```

```javascript
function doSomething() {
  console.log('yay!');
}

typeof doSomething //=> 'function'
```

```javascript
var anObject = {};
typeof anObject //=> 'object'
var anArray = [1,2,3,4,5,6];
typeof anArray //=> 'object'
```

### 啥？！

```javascript
anArray instanceof Array //=> true
an0 instanceof Array //=> false
```

### 第一个 typeof
然后 instanceof

### 函数也是对象

```javascript
var sum = function(n1, n2) {
  return n1 + n2;
}

var a = {};
a.sum = sum;

a.sum(1, 2); // => 3
```

### ‘方法’只是赋值给对象属性的函数

```javascript
var a = { counter : 5 };
var b = { counter : 10 };

a.increment = function(amount) {
  this.counter += amount;
};

a.increment(1)
a.counter; // => 6
```

```javascript
b.increment = a.increment;
b.increment(1);
console.log(b.counter); // => 11
```

```javascript
function (amount) {
  this.counter += amount;
}

a.increment(5); // => 10
```

```javascript
function (amount) {
  this.counter += amount;
}

b.increment(5); // => 15
```

```javascript
var slideshow = {
  init: function() {
    this.start();
  },
  start: function() {
  }
}

window.onload = slideshow.init;
```

```javascript
window.onload();
```

```javascript
window.onload = function() {
  start();
}
```

```javascript
a.increment.call(b, 1); // => 6
a.increment.apply(b, [1]); // => 7
```

### arguments (参数)

```javascript
// 所有发送到函数的
// 参数，无论有多少个
function sum() {
  var total = 0;
  for (var i = 0, l = arguments.length; i < l; i++) {
    total += arguments[i];
  }
  return total;
}

console.log(sum(2, 5)); //=> 7
console.log(sum(10, 20, 30)); //=> 60
```

```javascript
validate('name');
validate('email', { min: 4, max: 10 });
```

```javascript
function validate() {
  var options = {};
  // 从 Array.prototype 窃取
  var slice = Array.prototype.slice;

  if (typeof arguments === 'object') {
    options = slice.call(arguments, 1);
  }
  // 此处代码
```

### 函数可以返回其他函数

```javascript
function add(a, b) { return a + b }

function adder(a) {
  return function(b) {
    return add(a, b);
  }
}

add(5, 5); //=> 10

var add5 = adder(5);
add5(10); //=> 15
```

```javascript
function add(a, b) { return a + b }

function adder(a) {
  return function(b) {
    return add(a, b);
  }
}

add(5, 5); //=> 10

var add5 = adder(5);
add5(10); //=> 15
```

### 闭包 (Closure)

### 回到 Wikipedia...

当一个函数定义在另一个函数内部，且内部函数引用了外部函数的局部变量时，发生了闭包。

```javascript
function attachHelpEvents() {
  var windowRef = null;
  var openLink = document.getElementById('open_help');
  var closeLink = document.getElementById('close_help');

  var openWindow = function() {
    windowRef = this.href;
  };

  var onClose = function() {
    if (windowRef) windowRef.close();
  };

  openLink.onclick = openWindow;
  closeLink.onclick = onClose;
}

window.onload = attachHelpEvents;
```

```javascript
function attachHelpEvents() {
  var windowRef = null;
  var openLink = document.getElementById('open_help');
  var closeLink = document.getElementById('close_help');

  var openWindow = function() {
    windowRef = this.href;
  };

  var onClose = function() {
    if (windowRef) windowRef.close();
  };

  openLink.onclick = openWindow;
  closeLink.onclick = onClose;
}

window.onload = attachHelpEvents;
```

### 这为什么很有用？

```javascript
var slideshow = {
  init: function() {
    this.start();
  },
  start: function() {
  }
}

window.onload = slideshow.init;
```

```javascript
function bind(func, context) {
  return function() {
    return func.apply(context, arguments);
  }
}
```

```javascript
var slideshow = {
  init: function() {
    this.start();
  },
  start: function() {
  }
}

window.onload = bind(slideshow.init, slideshow);
```

### 函数可以用来创建对象

```javascript
function Coord(x, y) {
  this.x = x;
  this.y = y;
}
var home = new Coord(132, 223);
console.log(home.x); //=> 132
console.log(home.y); //=> 223
console.log(home.constructor); //=> Coord
```

### 构造函数只是函数

### 魔法在于 new 运算符

```javascript
var london = new Coord(32, 13);
```

```javascript
var london = {};
Coord.call(london, 32, 13);
```

```javascript
var london = {};

Coord.call(london, 32, 13);
london.__proto__ = Coord.prototype;
```

### 继承 (inheritance)

```javascript
Coord.prototype = {
  toString: function() {
    return [this.x, this.y].join(', ');
  }
};

home.toString(); // 132, 223
```

```javascript
home.toString? // 没有...继续寻找
home.__proto__.toString? // 找到了！
```

```javascript
home.__proto__ == Coord
```

```javascript
function Marker(name, x, y) {
  this.name = name;
  this.x = x;
  this.y = y;
}

Marker.prototype = new Coord;

var pub = new Marker('Party!', 12, 54);
pub.toString(); //=> 12, 54
```

```javascript
pub.toString // 没有...
pub.__proto__.toString // 没有...
pub.__proto__.__proto__.toString // 找到了！
```

```javascript
pub.__proto__ == Marker.prototype
pub.__proto__.__proto__ == Coord
```

### 重点在于：
它们都只是函数、
对象和属性

### 我们可以对它们进行任何操作。

### 所以用这些东西能做什么？

### 修复糟糕实现中的漏洞

```javascript
// 为 IE 5 修复 Array#push
if (!Array.prototype.push) {
  Array.prototype.push = function(item) {
    return this[this.length] = item;
  }
}
```

```javascript
// 为旧浏览器添加 1.6 风格的 Array#forEach
if (!Array.prototype.forEach) {
  Array.prototype.forEach = function(func, scope) {
    scope = scope || this;
    for (var i = 0, l = this.length; i < l; i++) {
      func.call(scope, this[i], i, this);
    }
  }
}
```




### 自优化代码

```
function addEvent(element, type, func) {
  if (document.addEventListener)
    element.addEventListener(type, func);
  else
    element.attachEvent(type, func);
}
```

```javascript
function addEvent(element, type, func) {
  if (document.addEventListener) {
    addEvent = function(element, type, func) {
      element.addEventListener(type, func);
    };
  } else {
    addEvent = function(element, type, func) {
      element.attachEvent(type, func);
    };
  }
  addEvent(element, type, func);
}
```

### 美优的 APIs

```
Event.observe(window, 'load', function() {
  Event.observe($('country'), 'change', function() {
    if ($F('country') == 'United States') {
      return $('state').show();
    }
    $('state').hide()
  });
});
```

```javascript
// see: http://www.adamlogic.com/

show('state').when('country').is('United States');
```

#领域特定语言

### DOMBuilder

http://danwebbb.net/lowpro

```javascript
var ul = document.createElement('ul');
ul.setAttribute('id', 'my_list');
var li = document.createElement('li');
var text = document.createTextNodeNode('Some text');
li.appendChild(text);
ul.appendChild(li);
```

```javascript
var ul = DOMBuilder.create('ul', { id : 'my_list' }, [
  DOMBuilder.create('li', null, 'Some text')
]);
```

```javascript
var ul = $ul({ id : 'my_list' },
  $li('Some text')
);
```

## DIY 语言特性

### John Resig 的方法重载

http://ejohn.org/blog/javascript-method-overloading/

```javascript
var users = new Users();
users.find(); // 查找所有
users.find("John"); // 按名字查找
users.find("John", "Resig"); // 按姓和名查找
```

```javascript
function Users() {

  addMethod(Users.prototype, "find", function(){
    // 查找所有用户...
  });

  addMethod(Users.prototype, "find", function(name){
    // 按名字查找用户
  });

  addMethod(Users.prototype, "find", function(first, last){
    // 按姓和名查找用户
  });
}

```

```javascript
function addMethod(object, name, fn){
  var old = object[ name ];
  object[ name ] = function(){
    if ( fn.length == arguments.length ) {
      return fn.apply( this, arguments );
    } else if ( typeof old == 'function' ) {
      return old.apply( this, arguments );
    }
  };
}
```

## Prototype 1.6 类

http://prototypejs.org/learn/class-inheritance

```javascript
var Person = Class.create({
  initialize: function(name) {
    this.name = name;
  },
  say: function(message) {
    return this.name + ': ' + message;
  }
});
```

```javascript
var Pirate = Class.create(Person, {
  // 重定义 speak 方法
  say: function($super, message) {
    return $super(message) + ' , yarr!';
  }
});

var john = new Pirate('Long John');
john.say('ahoy matey');
// => "Long John: ahoy matey, yarr!"
```

## 还有更多...

## 回顾...

- JavaScript 虽然很小，但完全灵活
- 掌握少数技巧就能提供你所需的一切
- 核心在于对象、属性和函数
- 如果还没有完全理解，不要担心。试着玩一下。稍后提供幻灯片。

## 敬请期待...

