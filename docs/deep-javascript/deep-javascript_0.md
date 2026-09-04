
# 深入 JavaScript

## 1 关于本书

### 1.1 本书的主页在哪里？

《深入 JavaScript》的主页是[`exploringjs.com/deep-js/`](https://exploringjs.com/deep-js/)。

### 1.2 本书包含哪些内容？

本书深入探讨 JavaScript：

- 教授更好地使用该语言的实用技巧。
- 讲解语言的工作原理及其原因。所教内容严格基于 ECMAScript 规范（本书会解释并引用该规范）。
- 仅涵盖语言本身（忽略平台特定特性，如浏览器 API），但并非详尽无遗，而是聚焦于一系列重要主题。

### 1.3 付费后我能得到什么？

购买本书后，您将获得：

- 当前内容的四种无 DRM 版本：
  - PDF 文件
  - 包含无广告 HTML 的 ZIP 压缩包
  - EPUB 文件
  - MOBI 文件
- 未来添加到本版本中的任何内容。我能添加多少内容取决于本书的销量。

当前价格为优惠价。随着内容增加，价格将会上涨。

### 1.4 如何预览内容？

[在本书的主页上](https://exploringjs.com/deep-js/#previews)，有本书所有版本的广泛预览。

### 1.5 如何报告错误？

- 本书的 HTML 版本在每个章节末尾都有指向评论的链接。
- 它们会跳转到 GitHub 问题，[您也可以直接访问](https://github.com/rauschma/deep-js/issues)。

### 1.6 阅读建议

- 您可以按任意顺序阅读各章节。每个章节都是独立的，但偶尔会引用其他章节以提供更多信息。
- 某些章节的标题标有“（可选）”，表示它们并非必需内容。跳过它们，您仍然能理解该章节的其余部分。

### 1.7 符号与约定

#### 1.7.1 什么是类型签名？为什么我在本书中看到静态类型？

例如，您可能会看到：

```js
Number.isFinite(num: number): boolean
```

这被称为`Number.isFinite()`的类型签名。这种表示法，特别是`num`的静态类型`number`和结果的`boolean`，并不是真正的 JavaScript。这种表示法借用于编译到 JavaScript 的语言 TypeScript（它基本上就是 JavaScript 加上静态类型）。

为什么要使用这种表示法？它有助于让你快速了解函数的工作方式。这种表示法在[一篇 2ality 博客文章](https://2ality.com/2018/04/type-notation-typescript.html)中有详细解释，但通常相对直观。

#### 1.7.2 带图标的注释是什么意思？

![](img/file0.svg) **阅读说明**

解释如何最好地阅读内容。

![](img/file1.svg) **外部内容**

指向额外的外部内容。

![](img/file2.svg) **提示**

给出与当前内容相关的提示。

![](img/file3.svg) **问题**

提出并回答与当前内容相关的问题（类似于常见问题解答）。

![](img/file4.svg) **警告**

警告陷阱等。

![](img/file5.svg) **详情**

提供补充当前内容的额外细节。类似于脚注。

![](img/file6.svg) **练习**

提及一个测试驱动练习的路径，你可以在该处进行练习。

![](img/file7.svg) **测验**

表示当前（部分）章节有一个测验。

### 1.8 致谢

- 感谢 Allen Wirfs-Brock 通过 Twitter 和博客文章评论提供的建议。这有助于使本书变得更好。
- 更多做出贡献的人已在各章节中致谢。

## 2 JavaScript 中的类型强制转换

在本章中，我们将探讨 JavaScript 中类型强制转换的作用。我们将相对深入地研究这个主题，例如，了解 ECMAScript 规范如何处理强制转换。

### 2.1 什么是类型强制转换？

每个操作（函数、运算符等）都期望其参数具有特定类型。如果某个值的参数类型不正确，例如函数通常有三种常见选择：

1. 函数可以抛出异常：

```js
function multiply(x, y) {
  if (typeof x !== 'number' || typeof y !== 'number') {
    throw new TypeError();
  }
  // ···
}
```

2. 函数可以返回错误值：

```js
function multiply(x, y) {
  if (typeof x !== 'number' || typeof y !== 'number') {
    return NaN;
  }
  // ···
}
```

3. 函数可以将其参数转换为有用的值：

```js
function multiply(x, y) {
  if (typeof x !== 'number') {
    x = Number(x);
  }
  if (typeof y !== 'number') {
    y = Number(y);
  }
  // ···
}
```

在 (3) 中，操作执行了隐式类型转换。这被称为类型强制转换。

JavaScript 最初没有异常，这就是为什么它的大多数操作都使用强制转换和错误值：

```js
// 强制转换
assert.equal(3 * true, 3);

// 错误值
assert.equal(1 / 0, Infinity);
assert.equal(Number('xyz'), NaN);
```

然而，也存在一些情况（尤其是涉及新特性时），如果参数类型不正确，它会抛出异常：

- 访问`null`或`undefined`的属性：

```text
> undefined.prop
TypeError: Cannot read property 'prop' of undefined
> null.prop
TypeError: Cannot read property 'prop' of null
> 'prop' in null
TypeError: Cannot use 'in' operator to search for 'prop' in null
```

- 使用符号：

```text
> 6 / Symbol()
TypeError: Cannot convert a Symbol value to a number
```

- 混合 bigint 和 number：

```text
> 6 / 3n
TypeError: Cannot mix BigInt and other types
```

- 对不支持该操作的值进行`new`调用或函数调用：

```text
> 123()
TypeError: 123 is not a function
> (class {})()
TypeError: Class constructor  cannot be invoked without 'new'

> new 123
TypeError: 123 is not a constructor
> new (() => {})
TypeError: (intermediate value) is not a constructor
```

- 更改只读属性（仅在严格模式下抛出）：

```text
> 'abc'.length = 1
TypeError: Cannot assign to read only property 'length'
> Object.freeze({prop:3}).prop = 1
TypeError: Cannot assign to read only property 'prop'
```

#### 2.1.1 处理类型强制转换

处理强制转换的两种常见方式是：

- 调用者可以显式转换值，使其具有正确的类型。例如，在以下交互中，我们想要将两个编码为字符串的数字相乘：

```js
let x = '3';
let y = '2';
assert.equal(Number(x) * Number(y), 6);
```

- 调用者可以让操作自行进行转换：

```js
let x = '3';
let y = '2';
assert.equal(x * y, 6);
```

我通常更喜欢前者，因为它明确了我的意图：我期望`x`和`y`不是数字，但想要将两个数字相乘。

### 2.2 ECMAScript 规范中帮助实现强制转换的操作

以下各节描述了 ECMAScript 规范用于将实际参数转换为预期类型的最重要的内部函数。

例如，在 TypeScript 中，我们会这样写：

```ts
function isNaN(number: number) {
  // ···
}
```

在规范中，这看起来[如下所示](https://tc39.es/ecma262/#sec-multiplicative-operators-runtime-semantics-evaluation)（翻译成 JavaScript，以便更容易理解）：

```js
function isNaN(number) {
  let num = ToNumber(number);
  // ···
}
```

#### 2.2.1 转换为原始类型和对象

每当期望原始类型或对象时，会使用以下转换函数：

- `ToBoolean()`
- `ToNumber()`
- `ToBigInt()`
- `ToString()`
- `ToObject()`

这些内部函数在 JavaScript 中有非常相似的对应物：

```text
> Boolean(0)
false
> Boolean(1)
true

> Number('123')
123
```

在引入 bigint（与 number 并存）之后，规范中之前使用`ToNumber()`的地方现在经常使用`ToNumeric()`。请继续阅读以了解更多信息。

#### 2.2.2 转换为数值类型

目前，JavaScript 有[两种内置数值类型](https://tc39.es/ecma262/#sec-numeric-types)：number 和 bigint。

- `ToNumeric()`返回一个数值`num`。它的调用者通常调用`num`的规范类型的方法`mthd`：

  ```js
  Type(num)::mthd(···)
  ```

  以下操作使用了`ToNumeric`：

  - 前缀和后缀`++`运算符
  - `*`运算符

- `ToInteger(x)`用于需要不带小数的数字时。结果的范围之后通常会进一步限制。
  - 它调用`ToNumber(x)`并移除小数部分（类似于`Math.trunc()`）。
  - 使用`ToInteger()`的操作：
    - `Number.prototype.toString(radix?)`
    - `String.prototype.codePointAt(pos)`
    - `Array.prototype.slice(start, end)`
    - 等等。

- `ToInt32()`、`ToUint32()`将数字强制转换为 32 位整数，并由位运算符使用（见表 1）。
  - `ToInt32()`：有符号，范围 [−2³¹, 2³¹−1]（包含边界）
  - `ToUint32()`：无符号（因此有`U`），范围 [0, 2³²−1]（包含边界）

表 1：位数值运算符操作数的强制转换（`BigInt`运算符不限制位数）。

| 运算符 | 左操作数 | 右操作数 | 结果类型 |
| --- | --- | --- | --- |
| `<<` | `ToInt32()` | `ToUint32()` | `Int32` |
| 有符号`>>` | `ToInt32()` | `ToUint32()` | `Int32` |
| 无符号`>>>` | `ToInt32()` | `ToUint32()` | `Uint32` |
| `&`、`^`、`&#124;` | `ToInt32()` | `ToUint32()` | `Int32` |
| `~` | — | `ToInt32()` | `Int32` |

#### 2.2.3 转换为属性键

`ToPropertyKey()`返回一个字符串或符号，并由以下操作使用：

- 方括号运算符`[]`
- 对象字面量中的计算属性键
- `in`运算符的左侧
- `Object.defineProperty(_, P, _)`
- `Object.fromEntries()`
- `Object.getOwnPropertyDescriptor()`
- `Object.prototype.hasOwnProperty()`
- `Object.prototype.propertyIsEnumerable()`
- `Reflect`的若干方法

#### 2.2.4 转换为数组索引

- `ToLength()`（直接）主要用于字符串索引。
  - `ToIndex()`的辅助函数
  - 结果`l`的范围：0 ≤ `l` ≤ 2⁵³−1
- `ToIndex()`用于类型化数组索引。
  - 与`ToLength()`的主要区别：如果参数超出范围则抛出异常。
  - 结果`i`的范围：0 ≤ `i` ≤ 2⁵³−1
- `ToUint32()`用于数组索引。
  - 结果`i`的范围：0 ≤ `i` < 2³²−1（上限不包含，以便为`.length`留出空间）

#### 2.2.5 转换为类型化数组元素

当我们设置类型化数组元素的值时，会使用以下转换函数之一：

- `ToInt8()`
- `ToUint8()`
- `ToUint8Clamp()`
- `ToInt16()`
- `ToUint16()`
- `ToInt32()`
- `ToUint32()`
- `ToBigInt64()`
- `ToBigUint64()`

### 2.3 插曲：用 JavaScript 表达规范算法

在本章的剩余部分，我们将遇到几个规范算法，但“实现”为 JavaScript。以下列表展示了一些常用模式如何从规范翻译为 JavaScript：

- 规范：如果`Type(value)`是 String

  JavaScript：`if (TypeOf(value) === 'string')`

  （非常宽松的翻译；`TypeOf()`定义如下）

- 规范：如果`IsCallable(method)`为 true

  JavaScript：`if (IsCallable(method))`

  （`IsCallable()`定义如下）

- 规范：令`numValue`为`ToNumber(value)`

  JavaScript：`let numValue = Number(value)`

- 规范：令`isArray`为`IsArray(O)`

  JavaScript：`let isArray = Array.isArray(O)`

- 规范：如果 O 有一个`[[NumberData]]`内部槽

  JavaScript：`if ('__NumberData__' in O)`

- 规范：令`tag`为`Get(O, @@toStringTag)`



JavaScript：`let tag = O[Symbol.toStringTag]`

- 规范：返回字符串拼接 `"[object "`, `tag` 和 `"]"`

JavaScript：

```javascript
return '[object ' + tag + ']';
```

使用 `let`（而不是 `const`）以匹配规范的语言。

某些内容被省略了——例如，[ReturnIfAbrupt 简写](https://tc39.es/ecma262/#sec-returnifabrupt-shorthands) `?` 和 `!`。

```javascript
/**
 * typeof 的改进版本
 */
function TypeOf(value) {
  const result = typeof value;
  switch (result) {
    case 'function':
      return 'object';
    case 'object':
      if (value === null) {
        return 'null';
      } else {
        return 'object';
      }
    default:
      return result;
  }
}

function IsCallable(x) {
  return typeof x === 'function';
}
```

## 2.4 示例强制转换算法

### 2.4.1 `ToPrimitive()`

[操作 `ToPrimitive()`](https://tc39.es/ecma262/#sec-toprimitive) 是许多强制转换算法的中间步骤（我们将在本章后面看到其中一些）。它将任意值转换为原始值。

`ToPrimitive()` 在规范中经常使用，因为大多数运算符只能处理原始值。例如，我们可以使用加法运算符（`+`）来加数字和拼接字符串，但不能用它来拼接数组。

以下是 `ToPrimitive()` 的 JavaScript 版本：

```typescript
/**
 * @param  hint 结果的首选类型：
 *              string、number 或不关心？
 */
function ToPrimitive(
  input: any,
  hint: 'string'|'number'|'default' = 'default') {
    if (TypeOf(input) === 'object') {
      let exoticToPrim = input[Symbol.toPrimitive]; // (A)
      if (exoticToPrim !== undefined) {
        let result = exoticToPrim.call(input, hint);
        if (TypeOf(result) !== 'object') {
          return result;
        }
        throw new TypeError();
      }
      if (hint === 'default') {
        hint = 'number';
      }
      return OrdinaryToPrimitive(input, hint);
    } else {
      // input 已经是原始值
      return input;
    }
  }
```

`ToPrimitive()` 允许对象通过 `Symbol.toPrimitive`（第 A 行）覆盖到原始值的转换。如果对象没有这样做，则将其传递给 `OrdinaryToPrimitive()`：

```typescript
function OrdinaryToPrimitive(O: object, hint: 'string' | 'number') {
  let methodNames;
  if (hint === 'string') {
    methodNames = ['toString', 'valueOf'];
  } else {
    methodNames = ['valueOf', 'toString'];
  }
  for (let name of methodNames) {
    let method = O[name];
    if (IsCallable(method)) {
      let result = method.call(O);
      if (TypeOf(result) !== 'object') {
        return result;
      }
    }
  }
  throw new TypeError();
}
```

#### 2.4.1.1 `ToPrimitive()` 的调用者使用哪些提示？

参数 `hint` 可以取三个值之一：

- `'number'` 表示：如果可能，`input` 应转换为数字。
- `'string'` 表示：如果可能，`input` 应转换为字符串。
- `'default'` 表示：对数字或字符串没有偏好。

以下是一些示例，展示各种操作如何使用 `ToPrimitive()`：

- `hint === 'number'`。以下操作优先使用数字：
  - `ToNumeric()`
  - `ToNumber()`
  - `ToBigInt()`、`BigInt()`
  - 抽象关系比较（`<`）

- `hint === 'string'`。以下操作优先使用字符串：
  - `ToString()`
  - `ToPropertyKey()`

- `hint === 'default'`。以下操作对返回的原始值类型保持中立：
  - 抽象相等比较（`==`）
  - 加法运算符（`+`）
  - `new Date(value)`（`value` 可以是数字或字符串）

如我们所见，默认行为是将 `'default'` 当作 `'number'` 处理。只有 `Symbol` 和 `Date` 的实例会覆盖此行为（稍后展示）。

#### 2.4.1.2 将对象转换为原始值时调用哪些方法？

如果通过 `Symbol.toPrimitive` 未覆盖转换为原始值的行为，则 `OrdinaryToPrimitive()` 会调用以下两个方法中的一个或两个：

- 如果 `hint` 表示我们希望原始值为字符串，则首先调用 `'toString'`。
- 如果 `hint` 表示我们希望原始值为数字，则首先调用 `'valueOf'`。

以下代码演示了其工作原理：

```javascript
const obj = {
  toString() { return 'a' },
  valueOf() { return 1 },
};

// String() 优先使用字符串：
assert.equal(String(obj), 'a');

// Number() 优先使用数字：
assert.equal(Number(obj), 1);
```

属性键为 `Symbol.toPrimitive` 的方法会覆盖正常的转换为原始值的过程。在标准库中，这种情况只出现了两次：

- `Symbol.prototypeSymbol.toPrimitive`
  - 如果接收者是 `Symbol` 的实例，此方法始终返回包装后的符号。
  - 其原理是：`Symbol` 的实例有一个返回字符串的 `.toString()` 方法。但即使 `hint` 是 `'string'`，也不应调用 `.toString()`，以免意外将 `Symbol` 实例转换为字符串（字符串是完全不同种类的属性键）。

- `Date.prototypeSymbol.toPrimitive`
  - 接下来将详细解释。

#### 2.4.1.3 `Date.prototype[Symbol.toPrimitive]()` 

以下是 Date 处理转换为原始值的方式：

```typescript
Date.prototype[Symbol.toPrimitive] = function (
  hint: 'default' | 'string' | 'number') {
    let O = this;
    if (TypeOf(O) !== 'object') {
      throw new TypeError();
    }
    let tryFirst;
    if (hint === 'string' || hint === 'default') {
      tryFirst = 'string';
    } else if (hint === 'number') {
      tryFirst = 'number';
    } else {
      throw new TypeError();
    }
    return OrdinaryToPrimitive(O, tryFirst);
  };
```

与默认算法的唯一区别在于，`'default'` 被当作 `'string'`（而不是 `'number'`）。如果我们使用将 `hint` 设置为 `'default'` 的操作，可以观察到这一点：

- `==` 运算符在另一个操作数是除 `undefined`、`null` 和 `boolean` 之外的原始值时，会将对象强制转换为原始值（使用默认 `hint`）。在以下交互中，我们可以看到强制转换日期对象的结果是一个字符串：

  ```javascript
  const d = new Date('2222-03-27');
  assert.equal(
    d == 'Wed Mar 27 2222 01:00:00 GMT+0100'
         + ' (Central European Standard Time)',
    true);
  ```

- `+` 运算符将两个操作数都强制转换为原始值（使用默认 `hint`）。如果其中一个结果是字符串，则执行字符串拼接（否则执行数字加法）。在以下交互中，我们可以看到强制转换日期对象的结果是一个字符串，因为运算符返回了字符串。

  ```javascript
  const d = new Date('2222-03-27');
  assert.equal(
    123 + d,
    '123Wed Mar 27 2222 01:00:00 GMT+0100'
      + ' (Central European Standard Time)');
  ```

### 2.4.2 `ToString()` 及相关操作

这是 `ToString()` 的 JavaScript 版本：

```javascript
function ToString(argument) {
  if (argument === undefined) {
    return 'undefined';
  } else if (argument === null) {
    return 'null';
  } else if (argument === true) {
    return 'true';
  } else if (argument === false) {
    return 'false';
  } else if (TypeOf(argument) === 'number') {
    return Number.toString(argument);
  } else if (TypeOf(argument) === 'string') {
    return argument;
  } else if (TypeOf(argument) === 'symbol') {
    throw new TypeError();
  } else if (TypeOf(argument) === 'bigint') {
    return BigInt.toString(argument);
  } else {
    // argument 是一个对象
    let primValue = ToPrimitive(argument, 'string'); // (A)
    return ToString(primValue);
  }
}
```

注意，该函数对于对象，在将原始结果转换为字符串之前，会使用 `ToPrimitive()` 作为中间步骤（第 A 行）。

`ToString()` 与 `String()` 的工作方式有一个有趣的差异：如果 `argument` 是一个符号，前者会抛出 `TypeError`，而后者不会。这是为什么？符号的默认行为是，将其转换为字符串会抛出异常：

```javascript
> const sym = Symbol('sym');

> ''+sym
TypeError: Cannot convert a Symbol value to a string
> `${sym}`
TypeError: Cannot convert a Symbol value to a string
```

在 `String()` 和 `Symbol.prototype.toString()` 中覆盖了该默认行为（两者将在下一小节中描述）：

```javascript
> String(sym)
'Symbol(sym)'
> sym.toString()
'Symbol(sym)'
```

#### 2.4.2.1 `String()`

```javascript
function String(value) {
  let s;
  if (value === undefined) {
    s = '';
  } else {
    if (new.target === undefined && TypeOf(value) === 'symbol') {
      // 此函数被作为函数调用，且 value 是一个符号
      return SymbolDescriptiveString(value);
    }
    s = ToString(value);
  }
  if (new.target === undefined) {
    // 此函数被作为函数调用
    return s;
  }
  // 此函数被通过 new 调用
  return StringCreate(s, new.target.prototype); // 简化版！
}
```

`String()` 的工作方式取决于它是通过函数调用还是通过 `new` 调用的。它使用 [`new.target`](https://exploringjs.com/es6/ch_classes.html#sec_allocating-and-initializing-instances) 来区分这两种情况。

以下是辅助函数 `StringCreate()` 和 `SymbolDescriptiveString()`：

```javascript
/**
 * 创建一个包装了 value 的 String 实例，
 * 并具有给定的原型。
 */
function StringCreate(value, prototype) {
  // ···
}

function SymbolDescriptiveString(sym) {
  assert.equal(TypeOf(sym), 'symbol');
  let desc = sym.description;
  if (desc === undefined) {
    desc = '';
  }
  assert.equal(TypeOf(desc), 'string');
  return 'Symbol('+desc+')';
}
```

#### 2.4.2.2 `Symbol.prototype.toString()`

除了 `String()`，我们还可以使用方法 `.toString()` 将符号转换为字符串。其规范如下所示。



```javascript
Symbol.prototype.toString = function () {
  let sym = thisSymbolValue(this);
  return SymbolDescriptiveString(sym);
};

function thisSymbolValue(value) {
  if (TypeOf(value) === 'symbol') {
    return value;
  }
  if (TypeOf(value) === 'object' && '__SymbolData__' in value) {
    let s = value.__SymbolData__;
    assert.equal(TypeOf(s), 'symbol');
    return s;
  }
}
```

#### 2.4.2.3 `Object.prototype.toString`

`.toString()` 的默认规范如下：

```javascript
Object.prototype.toString = function () {
  if (this === undefined) {
    return '[object Undefined]';
  }
  if (this === null) {
    return '[object Null]';
  }
  let O = ToObject(this);
  let isArray = Array.isArray(O);
  let builtinTag;
  if (isArray) {
    builtinTag = 'Array';
  } else if ('__ParameterMap__' in O) {
    builtinTag = 'Arguments';
  } else if ('__Call__' in O) {
    builtinTag = 'Function';
  } else if ('__ErrorData__' in O) {
    builtinTag = 'Error';
  } else if ('__BooleanData__' in O) {
    builtinTag = 'Boolean';
  } else if ('__NumberData__' in O) {
    builtinTag = 'Number';
  } else if ('__StringData__' in O) {
    builtinTag = 'String';
  } else if ('__DateValue__' in O) {
    builtinTag = 'Date';
  } else if ('__RegExpMatcher__' in O) {
    builtinTag = 'RegExp';
  } else {
    builtinTag = 'Object';
  }
  let tag = O[Symbol.toStringTag];
  if (TypeOf(tag) !== 'string') {
    tag = builtinTag;
  }
  return '[object ' + tag + ']';
};
```

当我们把普通对象转换为字符串时，会使用这个操作：

```javascript
> String({})
'[object Object]'
```

默认情况下，当我们把类的实例转换为字符串时，也会使用它：

```javascript
class MyClass {}
assert.equal(
  String(new MyClass()), '[object Object]');
```

通常，我们会重写 `.toString()` 来配置 `MyClass` 的字符串表示形式，但我们也可以更改方括号内“`object`”后面的内容：

```javascript
class MyClass {}
MyClass.prototype[Symbol.toStringTag] = 'Custom!';
assert.equal(
  String(new MyClass()), '[object Custom!]');
```

将 `.toString()` 的重写版本与 `Object.prototype` 中的原始版本进行比较是很有趣的：

```javascript
> ['a', 'b'].toString()
'a,b'
> Object.prototype.toString.call(['a', 'b'])
'[object Array]'

> /^abc$/.toString()
'/^abc$/'
> Object.prototype.toString.call(/^abc$/)
'[object RegExp]'
```

### 2.4.3 `ToPropertyKey()`

`ToPropertyKey()` 被方括号运算符等使用。它的工作方式如下：

```javascript
function ToPropertyKey(argument) {
  let key = ToPrimitive(argument, 'string'); // (A)
  if (TypeOf(key) === 'symbol') {
    return key;
  }
  return ToString(key);
}
```

再次强调，在处理原始值之前，对象会被转换为原始值。

### 2.4.4 `ToNumeric()` 及相关操作

`ToNumeric()` 被乘法运算符（`*`）等使用。它的工作方式如下：

```javascript
function ToNumeric(value) {
  let primValue = ToPrimitive(value, 'number');
  if (TypeOf(primValue) === 'bigint') {
    return primValue;
  }
  return ToNumber(primValue);
}
```

#### 2.4.4.1 `ToNumber()`

`ToNumber()` 的工作方式如下：

```javascript
function ToNumber(argument) {
  if (argument === undefined) {
    return NaN;
  } else if (argument === null) {
    return +0;
  } else if (argument === true) {
    return 1;
  } else if (argument === false) {
    return +0;
  } else if (TypeOf(argument) === 'number') {
    return argument;
  } else if (TypeOf(argument) === 'string') {
    return parseTheString(argument); // 此处未展示
  } else if (TypeOf(argument) === 'symbol') {
    throw new TypeError();
  } else if (TypeOf(argument) === 'bigint') {
    throw new TypeError();
  } else {
    // argument 是一个对象
    let primValue = ToPrimitive(argument, 'number');
    return ToNumber(primValue);
  }
}
```

`ToNumber()` 的结构与 `ToString()` 的结构类似。

## 2.5 强制类型转换操作

### 2.5.1 加法运算符（`+`）

JavaScript 的加法运算符规范如下：

```javascript
function Addition(leftHandSide, rightHandSide) {
  let lprim = ToPrimitive(leftHandSide);
  let rprim = ToPrimitive(rightHandSide);
  if (TypeOf(lprim) === 'string' || TypeOf(rprim) === 'string') { // (A)
    return ToString(lprim) + ToString(rprim);
  }
  let lnum = ToNumeric(lprim);
  let rnum = ToNumeric(rprim);
  if (TypeOf(lnum) !== TypeOf(rnum)) {
    throw new TypeError();
  }
  let T = Type(lnum);
  return T.add(lnum, rnum); // (B)
}
```

该算法的步骤：

- 两个操作数都被转换为原始值。
- 如果其中一个结果是字符串，则两个操作数都被转换为字符串并拼接（第 A 行）。
- 否则，两个操作数都被转换为数值并相加（第 B 行）。`Type()` 返回 `lnum` 的 ECMAScript 规范类型。`.add()` 是[数值类型](https://tc39.es/ecma262/#sec-numeric-types)的一个方法。

### 2.5.2 抽象相等比较（`==`）



```javascript
/** Loose equality (==) */
function abstractEqualityComparison(x, y) {
  if (TypeOf(x) === TypeOf(y)) {
    // Use strict equality (===)
    return strictEqualityComparison(x, y);
  }

  // Comparing null with undefined
  if (x === null && y === undefined) {
    return true;
  }
  if (x === undefined && y === null) {
    return true;
  }

  // Comparing a number and a string
  if (TypeOf(x) === 'number' && TypeOf(y) === 'string') {
    return abstractEqualityComparison(x, Number(y));
  }
  if (TypeOf(x) === 'string' && TypeOf(y) === 'number') {
    return abstractEqualityComparison(Number(x), y);
  }

  // Comparing a bigint and a string
  if (TypeOf(x) === 'bigint' && TypeOf(y) === 'string') {
    let n = StringToBigInt(y);
    if (Number.isNaN(n)) {
      return false;
    }
    return abstractEqualityComparison(x, n);
  }
  if (TypeOf(x) === 'string' && TypeOf(y) === 'bigint') {
    return abstractEqualityComparison(y, x);
  }

  // Comparing a boolean with a non-boolean
  if (TypeOf(x) === 'boolean') {
    return abstractEqualityComparison(Number(x), y);
  }
  if (TypeOf(y) === 'boolean') {
    return abstractEqualityComparison(x, Number(y));
  }

  // Comparing an object with a primitive
  // (other than undefined, null, a boolean)
  if (['string', 'number', 'bigint', 'symbol'].includes(TypeOf(x))
    && TypeOf(y) === 'object') {
      return abstractEqualityComparison(x, ToPrimitive(y));
    }
  if (TypeOf(x) === 'object'
    && ['string', 'number', 'bigint', 'symbol'].includes(TypeOf(y))) {
      return abstractEqualityComparison(ToPrimitive(x), y);
    }

  // Comparing a bigint with a number
  if ((TypeOf(x) === 'bigint' && TypeOf(y) === 'number')
    || (TypeOf(x) === 'number' && TypeOf(y) === 'bigint')) {
      if ([NaN, +Infinity, -Infinity].includes(x)
        || [NaN, +Infinity, -Infinity].includes(y)) {
          return false;
        }
      if (isSameMathematicalValue(x, y)) {
        return true;
      } else {
        return false;
      }
    }

  return false;
}
```

以下操作未在此处展示：

* [`strictEqualityComparison()`](https://tc39.es/ecma262/#sec-strict-equality-comparison)
* [`StringToBigInt()`](https://tc39.es/ecma262/#sec-stringtobigint)
* [`isSameMathematicalValue()`](https://tc39.es/ecma262/#mathematical-value)

## 2.6 术语表：与类型转换相关的术语

现在我们已经更深入地了解了 JavaScript 的类型强制转换是如何工作的，让我们用一个与类型转换相关的简短术语表来总结一下：

* 在*类型转换*中，我们希望输出值具有给定的类型。如果输入值已经具有该类型，则直接返回不变。否则，将其转换为具有所需类型的值。
* *显式类型转换*意味着程序员使用某个操作（函数、运算符等）来触发类型转换。显式转换可以是：
  * *受检的*：如果无法转换值，则抛出异常。
  * *非受检的*：如果无法转换值，则返回错误值。
* *类型转换*（type casting）的含义取决于编程语言。例如，在 Java 中，它是显式的受检类型转换。
* *类型强制转换*是隐式类型转换：操作自动将其参数转换为所需的类型。可以是受检的、非受检的或介于两者之间的。

[来源：[维基百科](https://en.wikipedia.org/wiki/Type_conversion)]

# 3 解构算法

## 3.1 为模式匹配算法做准备

### 3.1.1 使用声明式规则指定匹配算法

### 3.1.2 基于声明式规则求值表达式

## 3.2 模式匹配算法

### 3.2.1 模式

### 3.2.2 变量的规则

### 3.2.3 对象模式的规则

### 3.2.4 数组模式的规则

## 3.3 空对象模式和数组模式

## 3.4 应用算法

### 3.4.1 背景：通过匹配传递参数

### 3.4.2 使用 `move2()`

### 3.4.3 使用 `move1()`

### 3.4.4 结论：默认值是模式部分的一个特性

在本章中，我们将从另一个角度看待解构：作为一种递归的模式匹配算法。

该算法将让我们更好地理解默认值。这在最后会很有用，我们将尝试弄清楚以下两个函数有何不同：

```javascript
function move({x=0, y=0} = {})         { ··· }
function move({x, y} = { x: 0, y: 0 }) { ··· }
```

## 3.1 为模式匹配算法做准备

解构赋值看起来像这样：

```javascript
«pattern» = «value»
```

我们想使用`pattern`从`value`中提取数据。

现在我们将研究一种执行这种赋值的算法。该算法在函数式编程中被称为*模式匹配*（简称：*匹配*）。它指定了运算符`←`（“匹配于”），该运算符将`pattern`与`value`进行匹配，并在此过程中为变量赋值：

```javascript
«pattern» ← «value»
```

我们将只探讨解构赋值，但解构变量声明和解构参数定义的工作方式类似。我们也不会深入探讨高级特性：计算属性键、属性值简写，以及将对象属性和数组元素作为赋值目标，这些都不在本章的讨论范围内。

匹配运算符的规范由声明式规则组成，这些规则深入到两个操作数的结构中。声明式表示法可能需要一些时间来适应，但它使规范更加简洁。

### 3.1.1 使用声明式规则指定匹配算法

本章使用的声明式规则对输入进行操作，并通过副作用产生算法的结果。以下是这样一个规则（我们稍后会再次看到）：

* (2c) `{key: «pattern», «properties»} ← obj`

  ```javascript
  «pattern» ← obj.key
  {«properties»} ← obj
  ```

该规则包含以下部分：

* (2c) 是规则的*编号*。该编号用于引用规则。
* *头部*（第一行）描述了输入必须满足的条件，以便应用此规则。
* *主体*（其余行）描述了应用规则时发生的情况。

在规则 (2c) 中，头部表示：如果存在一个至少包含一个属性（其键为 `key`）且剩余属性为零个或多个的对象模式，则可以应用此规则。此规则的效果是，继续执行时，将属性值模式与 `obj.key` 进行匹配，并将剩余属性与 `obj` 进行匹配。

让我们考虑本章中的另一条规则：

* (2e) `{} ← obj`（没有剩余属性）

  ```javascript
  // 我们完成了
  ```

在规则 (2e) 中，头部表示：如果空对象模式 `{}` 与值 `obj` 匹配，则执行此规则。主体表示：在这种情况下，我们就完成了。

规则 (2c) 和规则 (2e) 共同构成一个声明式循环，该循环遍历箭头左侧模式的属性。

### 3.1.2 基于声明式规则求值表达式

完整算法通过一系列声明式规则来指定。假设我们要求值以下匹配表达式：

```javascript
{first: f, last: l} ← obj
```

要应用一系列规则，我们从上到下遍历它们，并执行第一个可应用的规则。如果该规则的主体中存在匹配表达式，则再次应用这些规则。依此类推。

有时头部包含一个条件，该条件也决定规则是否可应用——例如：

* (3a) `[«elements»] ← non_iterable`

  `if (!isIterable(non_iterable))`

  ```javascript
  throw new TypeError();
  ```

## 3.2 模式匹配算法

### 3.2.1 模式

模式可以是：

* 变量：`x`
* 对象模式：`{«properties»}`
* 数组模式：`[«elements»]`

接下来的三节将指定在匹配表达式中处理这三种情况的规则。

### 3.2.2 变量的规则

* 1. `x ← value`（包括 `undefined` 和 `null`）

  ```javascript
  x = value
  ```

### 3.2.3 对象模式的规则

* (2a) `{«properties»} ← undefined`（非法值）

  ```javascript
  throw new TypeError();
  ```

* (2b) `{«properties»} ← null`（非法值）

  ```javascript
  throw new TypeError();
  ```

* (2c) `{key: «pattern», «properties»} ← obj`

  ```javascript
  «pattern» ← obj.key
  {«properties»} ← obj
  ```

* (2d) `{key: «pattern» = default_value, «properties»} ← obj`

  ```javascript
  const tmp = obj.key;
  if (tmp !== undefined) {
    «pattern» ← tmp
  } else {
    «pattern» ← default_value
  }
  {«properties»} ← obj
  ```

* (2e) `{} ← obj`（没有剩余属性）

  ```javascript
  // 我们完成了
  ```

规则 2a 和 2b 处理非法值。规则 2c–2e 遍历模式的属性。在规则 2d 中，我们可以看到，如果 `obj` 中没有匹配的属性，默认值提供了另一种匹配方式。

### 3.2.4 数组模式的规则

**数组模式与可迭代对象。** 数组解构的算法从一个数组模式和一个可迭代对象开始：

* (3a) `[«elements»] ← non_iterable`（非法值）

  `if (!isIterable(non_iterable))`

  ```javascript
  throw new TypeError();
  ```

* (3b) `[«elements»] ← iterable`

  `if (isIterable(iterable))`

  ```javascript
  const iterator = iterable[Symbol.iterator]();
  «elements» ← iterator
  ```

辅助函数：

```javascript
function isIterable(value) {
  return (value !== null
    && typeof value === 'object'
    && typeof value[Symbol.iterator] === 'function');
}
```

**数组元素与迭代器。** 算法继续处理：

* 模式的元素（箭头左侧）
* 从可迭代对象获取的迭代器（箭头右侧）

以下是规则：

* (3c) `«pattern», «elements» ← iterator`

  ```javascript
  «pattern» ← getNext(iterator) // 最后一项之后为 undefined
  «elements» ← iterator
  ```

* (3d) `«pattern» = default_value, «elements» ← iterator`

  ```javascript
  const tmp = getNext(iterator);  // 最后一项之后为 undefined
  if (tmp !== undefined) {
    «pattern» ← tmp
  } else {
    «pattern» ← default_value
  }
  «elements» ← iterator
  ```

* (3e) `, «elements» ← iterator`（空洞，省略）

  ```javascript
  getNext(iterator); // 跳过
  «elements» ← iterator
  ```

* (3f) `...«pattern» ← iterator`（始终是最后一部分！）



```javascript
const tmp = [];
for (const elem of iterator) {
  tmp.push(elem);
}
«pattern» ← tmp
```

*   (3g) `← iterator`（没有剩余元素）

```javascript
// 我们完成了
```

辅助函数：

```javascript
function getNext(iterator) {
  const {done,value} = iterator.next();
  return (done ? undefined : value);
}
```

迭代器完成类似于对象中缺少属性。

## 3.3 空对象模式和空数组模式

算法规则的一个有趣结果：我们可以使用空对象模式和空数组模式进行解构。

给定一个空对象模式`{}`：如果要解构的值既不是`undefined`也不是`null`，则什么也不会发生。否则，会抛出`TypeError`。

```javascript
const {} = 123; // OK，既不是 undefined 也不是 null
assert.throws(
  () => {
    const {} = null;
  },
  /^TypeError: Cannot destructure 'null' as it is null.$/)
```

给定一个空数组模式`[]`：如果要解构的值是可迭代的，则什么也不会发生。否则，会抛出`TypeError`。

```javascript
const [] = 'abc'; // OK，可迭代
assert.throws(
  () => {
    const [] = 123; // 不可迭代
  },
  /^TypeError: 123 is not iterable$/)
```

换句话说：空的解构模式强制值具有某些特征，但没有其他效果。

## 3.4 应用算法

在 JavaScript 中，命名参数通过对象来模拟：调用者使用对象字面量，被调用者使用解构。这种模拟在[“JavaScript for impatient programmers”](https://exploringjs.com/impatient-js/ch_callables.html#named-parameters)中有详细解释。以下代码展示了一个示例：函数`move1()`有两个命名参数`x`和`y`：

```javascript
function move1({x=0, y=0} = {}) { // (A)
  return [x, y];
}
assert.deepEqual(
  move1({x: 3, y: 8}), [3, 8]);
assert.deepEqual(
  move1({x: 3}), [3, 0]);
assert.deepEqual(
  move1({}), [0, 0]);
assert.deepEqual(
  move1(), [0, 0]);
```

在 A 行中有三个默认值：

*   前两个默认值允许我们省略`x`和`y`。

*   第三个默认值允许我们在没有参数的情况下调用`move1()`（如最后一行所示）。

但为什么我们要像前面的代码片段那样定义参数呢？为什么不如下所示？

```javascript
function move2({x, y} = { x: 0, y: 0 }) {
  return [x, y];
}
```

为了理解为什么`move1()`是正确的，我们将在两个示例中使用这两个函数。在此之前，让我们看看如何通过匹配来解释参数的传递。

### 3.4.1 背景：通过匹配传递参数

对于函数调用，*形式参数*（在函数定义内部）与*实际参数*（在函数调用内部）进行匹配。例如，以下函数定义和函数调用：

```javascript
function func(a=0, b=0) { ··· }
func(1, 2);
```

参数`a`和`b`的设置方式类似于以下解构：

```javascript
[a=0, b=0] ← [1, 2]
```

### 3.4.2 使用`move2()`

让我们来看看`move2()`的解构是如何工作的。

**示例 1。** 函数调用`move2()`会导致以下解构：

```javascript
[{x, y} = { x: 0, y: 0 }] ← []
```

左侧的单个数组元素在右侧没有匹配项，因此`{x,y}`与默认值匹配，而不是与右侧的数据匹配（规则 3b、3d）：

```javascript
{x, y} ← { x: 0, y: 0 }
```

左侧包含*属性值简写*。它是以下内容的缩写：

```javascript
{x: x, y: y} ← { x: 0, y: 0 }
```

这个解构会导致以下两个赋值（规则 2c、1）：

```javascript
x = 0;
y = 0;
```

这正是我们想要的。然而，在下一个示例中，我们就没有这么幸运了。

**示例 2。** 让我们来看看函数调用`move2({z: 3})`，它会导致以下解构：

```javascript
[{x, y} = { x: 0, y: 0 }] ← [{z: 3}]
```

右侧索引 0 处有一个数组元素。因此，默认值被忽略，下一步是（规则 3d）：

```javascript
{x, y} ← { z: 3 }
```

这导致`x`和`y`都被设置为`undefined`，这不是我们想要的。问题在于`{x,y}`不再与默认值匹配，而是与`{z:3}`匹配。

### 3.4.3 使用`move1()`

让我们试试`move1()`。

**示例 1：** `move1()`

```javascript
[{x=0, y=0} = {}] ← []
```

右侧索引 0 处没有数组元素，因此我们使用默认值（规则 3d）：

```javascript
{x=0, y=0} ← {}
```

左侧包含属性值简写，这意味着这个解构等价于：

```javascript
{x: x=0, y: y=0} ← {}
```

右侧没有匹配`x`或`y`属性。因此，使用默认值，接下来执行以下解构（规则 2d）：

```javascript
x ← 0
y ← 0
```

这导致以下赋值（规则 1）：

```javascript
x = 0
y = 0
```

这里我们得到了想要的结果。让我们看看下一个示例是否还能保持好运。

**示例 2：** `move1({z: 3})`

```javascript
[{x=0, y=0} = {}] ← [{z: 3}]
```

数组模式的第一个元素在右侧有匹配项，并且该匹配项用于继续解构（规则 3d）：

```javascript
{x=0, y=0} ← {z: 3}
```

与示例 1 一样，右侧没有`x`和`y`属性，因此使用默认值：

```javascript
x = 0
y = 0
```

它按预期工作！这次，`x`和`y`的模式与`{z:3}`匹配并不是问题，因为它们有自己的局部默认值。

### 3.4.4 结论：默认值是模式部分的特性

这些示例表明，默认值是模式部分（对象属性或数组元素）的特性。如果某个部分没有匹配项或与`undefined`匹配，则使用默认值。也就是说，模式会与默认值进行匹配。

# 4 全局变量的详细探讨

*   4.1 作用域
*   4.2 词法环境
*   4.3 全局对象
*   4.4 在浏览器中，`globalThis`并不直接指向全局对象
*   4.5 全局环境
    *   4.5.1 脚本作用域和模块作用域
    *   4.5.2 创建变量：声明式记录与对象记录
    *   4.5.3 获取或设置变量
    *   4.5.4 全局 ECMAScript 变量与全局宿主变量
*   4.6 结论：为什么 JavaScript 同时拥有普通全局变量和全局对象？
*   4.7 本章的进一步阅读和资料来源

在本章中，我们将详细探讨 JavaScript 的全局变量是如何工作的。其中涉及几个有趣的现象：脚本的作用域、所谓的*全局对象*等等。

## 4.1 作用域

变量的*词法作用域*（简称：*作用域*）是程序中可以访问该变量的区域。JavaScript 的作用域是*静态的*（它们在运行时不会改变），并且可以嵌套——例如：

```javascript
function func() { // (A)
  const aVariable = 1;
  if (true) { // (B)
    const anotherVariable = 2;
  }
}
```

由`if`语句（第 B 行）引入的作用域嵌套在函数`func()`（第 A 行）的作用域内部。

作用域 S 的最内层外围作用域称为 S 的*外部作用域*。在示例中，`func`是`if`的外部作用域。

## 4.2 词法环境

在 JavaScript 语言规范中，作用域是通过*词法环境*“实现”的。它们由两个组件组成：

*   一个*环境记录*，将变量名映射到变量值（类似于字典）。这是作用域中变量的实际存储空间。记录中的名称-值条目称为*绑定*。

*   一个指向*外部环境*的引用——即外部作用域的环境。

嵌套作用域的树因此由通过外部环境引用链接的环境树来表示。

## 4.3 全局对象

全局对象是一个其属性成为全局变量的对象。（我们很快就会研究它如何精确地融入环境树。）它可以通过以下全局变量访问：

*   所有平台都可用：[`globalThis`](https://exploringjs.com/impatient-js/ch_variables-assignment.html#globalThis)。这个名称基于这样一个事实：它在全局作用域中与`this`具有相同的值。

*   其他用于全局对象的变量并非在所有平台上都可用：

    *   `window`是引用全局对象的经典方式。它在普通浏览器代码中有效，但在*Web Workers*（与普通浏览器进程并发运行的进程）和 Node.js 上无效。

    *   `self`在浏览器中随处可用（包括 Web Workers）。但 Node.js 不支持它。

    *   `global`仅在 Node.js 上可用。

## 4.4 在浏览器中，`globalThis`并不直接指向全局对象

在浏览器中，`globalThis`并不直接指向全局对象，而是存在一个间接层。例如，考虑网页上的一个 iframe：

*   每当 iframe 的`src`发生变化时，它都会获得一个新的全局对象。

*   然而，`globalThis`始终具有相同的值。可以从 iframe 外部检查该值，如下所示（灵感来自[`globalThis`提案中的一个示例](https://github.com/tc39/proposal-global#html-and-the-windowproxy)）。

文件`parent.html`：

```html
<iframe src="iframe.html?first"></iframe>
<script>
  const iframe = document.querySelector('iframe');
  const icw = iframe.contentWindow; // iframe 的 `globalThis`

  iframe.onload = () => {
    // 访问 iframe 全局对象的属性
    const firstGlobalThis = icw.globalThis;
    const firstArray = icw.Array;
    console.log(icw.iframeName); // 'first'

    iframe.onload = () => {
      const secondGlobalThis = icw.globalThis;
      const secondArray = icw.Array;

      // 全局对象不同
      console.log(icw.iframeName); // 'second'
      console.log(secondArray === firstArray); // false

      // 但 globalThis 仍然相同
      console.log(firstGlobalThis === secondGlobalThis); // true
    };
    iframe.src = 'iframe.html?second';
  };
</script>
```

文件`iframe.html`：

```html
<script>
  globalThis.iframeName = location.search.slice(1);
</script>
```

浏览器如何确保在这种场景下`globalThis`不​​会改变？它们在内部区分了两个对象：

*   [`Window`](https://html.spec.whatwg.org/multipage/window-object.html#the-window-object)是全局对象。每当位置发生变化时，它就会改变。

*   [`WindowProxy`](https://html.spec.whatwg.org/multipage/window-object.html#the-windowproxy-exotic-object)是一个将所有访问转发到当前`Window`的对象。这个对象永远不会改变。

在浏览器中，`globalThis`指向`WindowProxy`；在其他地方，它直接指向全局对象。

## 4.5 全局环境

全局作用域是“最外层”的作用域——它没有外层作用域。它的环境是*全局环境*。每个环境都通过由外层环境引用链接的环境链与全局环境相连。全局环境的外层环境引用是`null`。

全局环境记录使用两个环境记录来管理其变量：

*   *对象环境记录*具有与普通环境记录相同的接口，但将其绑定保存在一个 JavaScript 对象中。在这种情况下，该对象就是全局对象。

*   一个普通的（*声明式*）环境记录，它有自己的存储空间来保存绑定。

这两个记录何时被使用，将在稍后解释。

### 4.5.1 脚本作用域和模块作用域

在 JavaScript 中，我们只有在脚本的顶层才处于全局作用域。相比之下，每个模块都有自己的作用域，该作用域是脚本作用域的子作用域。

如果我们忽略变量绑定如何添加到全局环境中的相对复杂的规则，那么全局作用域和模块作用域的工作方式就像它们是嵌套的代码块一样：

```javascript
{ // 全局作用域（所有*脚本*的作用域）

  // （全局变量）

  { // 模块 1 的作用域
    ···
  }
  { // 模块 2 的作用域
    ···
  }
  // （更多模块作用域）
}
```

### 4.5.2 创建变量：声明式记录与对象记录

为了创建一个真正全局的变量，我们必须处于全局作用域中——这只有在脚本的顶层才成立：

*   顶层的`const`、`let`和`class`在声明式环境记录中创建绑定。

*   顶层的`var`和函数声明在对象环境记录中创建绑定。

```html
<script>
  const one = 1;
  var two = 2;
</script>
<script>
  // 所有脚本共享同一个顶层作用域：
  console.log(one); // 1
  console.log(two); // 2

  // 并非所有声明都会创建全局对象的属性：
  console.log(globalThis.one); // undefined
  console.log(globalThis.two); // 2
</script>
```

### 4.5.3 获取或设置变量

当我们获取或设置一个变量，并且两个环境记录都有该变量的绑定时，声明式记录获胜：

```html
<script>
  let myGlobalVariable = 1; // 声明式环境记录
  globalThis.myGlobalVariable = 2; // 对象环境记录

  console.log(myGlobalVariable); // 1（声明式记录获胜）
  console.log(globalThis.myGlobalVariable); // 2
</script>
```

### 4.5.4 全局 ECMAScript 变量与全局宿主变量

除了通过`var`和函数声明创建的变量之外，全局对象还包含以下属性：

*   所有 ECMAScript 的内置全局变量

*   所有宿主平台（浏览器、Node.js 等）的内置全局变量

使用`const`或`let`可以保证全局变量声明不会影响（或受制于）ECMAScript 和宿主平台的内置全局变量。

例如，浏览器有[全局变量`.location`](https://developer.mozilla.org/en-US/docs/Web/API/Window/location)：



```javascript
// 更改当前文档的位置：
var location = 'https://example.com';

// 遮蔽 window.location，但不更改它：
let location = 'https://example.com';
```

如果变量已经存在（例如本例中的`location`），那么带有初始化器的`var`声明行为类似于赋值。这就是为什么在这个例子中我们会遇到麻烦。

请注意，这仅在全局作用域中是一个问题。在模块中，我们永远不会处于全局作用域（除非我们使用`eval()`或类似方法）。

图 1 总结了我们在本节中学到的所有内容。

![](img/file8.svg)

图 1：全局作用域的环境通过一个*全局环境记录*来管理其绑定，而该记录又基于两个环境记录：一个*对象环境记录*（其绑定存储在全局对象中）和一个*声明式环境记录*（使用内部存储来保存其绑定）。因此，可以通过向全局对象添加属性或通过各种声明来创建全局变量。全局对象使用 ECMAScript 和宿主平台的内置全局变量进行初始化。每个 ECMAScript 模块都有自己的环境，其外层环境是全局环境。

## 4.6 结论：为什么 JavaScript 既有普通的全局变量又有全局对象？

全局对象通常被认为是一个错误。因此，较新的构造（如`const`、`let`和类）会创建普通的全局变量（当处于脚本作用域时）。

值得庆幸的是，现代 JavaScript 编写的大部分代码都存在于[ECMAScript 模块和 CommonJS 模块](https://exploringjs.com/impatient-js/ch_modules.html)中。每个模块都有自己的作用域，因此管理全局变量的规则很少对基于模块的代码产生影响。

## 4.7 本章的进一步阅读和来源

ECMAScript 规范中的环境和全局对象：

- [“词法环境”一节](https://tc39.es/ecma262/#sec-lexical-environments)提供了环境的总体概述。
- [“全局环境记录”一节](https://tc39.es/ecma262/#sec-global-environment-records)涵盖了全局环境。
- [“ECMAScript 标准内置对象”一节](https://tc39.es/ecma262/#sec-ecmascript-standard-built-in-objects)描述了 ECMAScript 如何管理其内置对象（其中包括全局对象）。

`globalThis`：

- 2ality 文章[“ES 特性：`globalThis`”](https://2ality.com/2019/08/global-this.html)
- 访问全局`this`值的多种方式：Mathias Bynens 的[“通用 JavaScript 中可怕的`globalThis` polyfill”](https://mathiasbynens.be/notes/globalthis)

浏览器中的全局对象：

- 浏览器中发生情况的背景：Anne van Kesteren 的[“定义 WindowProxy、Window 和 Location 对象”](https://blog.whatwg.org/windowproxy-window-and-location)
- 非常技术性：WHATWG HTML 标准中的[“领域、设置对象和全局对象”一节](https://html.spec.whatwg.org/multipage/webappapis.html#realms-settings-objects-global-objects)
- 在 ECMAScript 规范中，我们可以看到 Web 浏览器如何自定义全局`this`：[“InitializeHostDefinedRealm()”一节](https://tc39.es/ecma262/#sec-initializehostdefinedrealm)

# 5 `%`是余数运算符，而不是模运算符

## 5.1 余数运算符`rem`与模运算符`mod`

在本章中，我们假设 JavaScript 有以下两个运算符：

- *余数运算符*`rem`
- *模运算符*`mod`

这将帮助我们研究底层操作的工作原理。

## 5.2 对余数运算的直观理解

余数运算符的操作数称为*被除数*和*除数*：

```
remainder = dividend rem divisor
```

结果是如何计算的呢？考虑以下表达式：

```
7 rem 3
```

我们从被除数中不断减去 3，直到剩下的值小于 3：

```
7 rem 3 = 4 rem 3 = 1 rem 3 = 1
```

如果被除数为负数呢？

```
-7 rem 3
```

这次，我们不断向被除数加上 3，直到得到一个小于 -3 的值：

```
-7 rem 3 = -4 rem 3 = -1 rem 3 = -1
```

对于固定的除数，列出结果会很有启发性：

```
x:       -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
x rem 3: -1  0 -2 -1  0 -2 -1  0  1  2  0  1  2  0  1
```

在结果中，我们可以看到一种对称性：`x`和`-x`产生相同的结果，但符号相反。

## 5.3 对模运算的直观理解

同样，操作数称为*被除数*和*除数*（暗示`rem`和`mod`的相似性）：

```
modulus = dividend mod divisor
```

考虑以下示例：

```
x mod 3
```

此操作将`x`映射到范围：

```
[0,3) = {0,1,2}
```

也就是说，包含 0（左方括号），排除 3（右圆括号）。

`mod`如何执行此映射？如果`x`已经在范围内，则很简单：

```
> 0 mod 3
0
> 2 mod 3
2
```

如果`x`大于或等于范围的上限，则从`x`中减去上限，直到它适合该范围：

```
> 4 mod 3
1
> 7 mod 3
1
```

这意味着对于非负整数，我们得到以下映射：

```
x:       0 1 2 3 4 5 6 7
x mod 3: 0 1 2 0 1 2 0 1
```

此映射扩展如下，以包含负整数：

```
x:       -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
x mod 3:  2  0  1  2  0  1  2  0  1  2  0  1  2  0  1
```

注意范围`[0,3)`是如何不断重复的。

## 5.4 `rem`和`mod`的异同

`rem`和`mod`非常相似——它们仅在除数和被除数符号不同时有区别：

- 对于`rem`，结果与除数（第一个操作数）符号相同：

  ```
  > 5 rem 4
  1
  > -5 rem 4
  -1
  > 5 rem -4
  1
  > -5 rem -4
  -1
  ```

- 对于`mod`，结果与除数（第二个操作数）符号相同：

  ```
  > 5 mod 4
  1
  > -5 mod 4
  3
  > 5 mod -4
  -3
  > -5 mod -4
  -1
  ```

## 5.5 余数和模背后的等式

以下两个等式定义了余数和模：

```
dividend = (divisor * quotient) + remainder
|remainder| < |divisor|
```

给定被除数和除数，我们如何计算余数和模？

```
remainder = dividend - (divisor * quotient)
quotient = dividend div divisor
```

`div`运算符执行整数除法。

### 5.5.1 `rem`和`mod`执行整数除法的方式不同

这些等式如何同时包含*两种*运算的解？如果变量`remainder`不为零，等式总是允许两个值：一个正，一个负。要理解原因，我们来看确定商时提出的问题：

> 我们需要将除数乘以多少次才能尽可能接近被除数？

例如，对于被除数 -2 和除数 3，这给出了两个不同的结果：

- `-2 rem 3 = -2`

  3 × 0 使我们接近 -2。0 与被除数 -2 的差是 -2。

- `-2 mod 3 = 1`

  3 × -1 也使我们接近 -2。-3 与被除数 -2 的差是 1。

对于被除数 2 和除数 -3，也给出了两个不同的结果：

- `2 rem -3 = 2`

  -3 × 0 使我们接近 2。

- `2 mod -3 = -1`

  -3 × -1 使我们接近 2。

结果的不同取决于整数除法`div`的实现方式。

### 5.5.2 实现`rem`

```javascript
function rem(dividend, divisor) {
  const quotient = Math.trunc(dividend / divisor);
  return dividend - (divisor * quotient);
}
```

### 5.5.3 实现`mod`

```javascript
function mod(dividend, divisor) {
  const quotient = Math.floor(dividend / divisor);
  return dividend - (divisor * quotient);
}
```

## 5.6 编程语言中`rem`和`mod`的使用场景

### 5.6.1 JavaScript 的`%`运算符计算余数

例如（Node.js REPL）：

```
> 7 % 6
1
> -7 % 6
-1
```

### 5.6.2 Python 的`%`运算符计算模

例如（Python REPL）：

```
>>> 7 % 6
1
>>> -7 % 6
5
```

### 5.6.3 JavaScript 中模运算的用途

ECMAScript 规范多次使用模运算——例如：

- 将[`>>>`运算符](https://tc39.es/ecma262/#sec-unsigned-right-shift-operator)的操作数转换为无符号 32 位整数（`x mod 2**32`）：

  ```
  > 2**32 >>> 0
  0
  > (2**32)+1 >>> 0
  1
  > (-1 >>> 0) === (2**32)-1
  true
  ```

- 将任意数字转换为适合 Typed Arrays 的形式。例如，`x mod 2**8`用于将数字转换为无符号 8 位整数（先将其转换为整数）：

  ```javascript
  const tarr = new Uint8Array(1);

  tarr[0] = 256;
  assert.equal(tarr[0], 0);

  tarr[0] = 257;
  assert.equal(tarr[0], 1);
  ```

## 5.7 本章的进一步阅读和资料来源

- [关于“模运算”的维基百科页面](https://en.wikipedia.org/wiki/Modulo_operation)包含大量信息。
- ECMAScript 规范[提到](https://tc39.es/ecma262/#sec-applying-the-mod-operator)`%`是通过“截断除法”计算的。
- 《JavaScript 快速入门》中的[“四舍五入”一节](https://exploringjs.com/impatient-js/ch_math.html#math-rounding)描述了 JavaScript 中几种四舍五入的方法。

# 6 复制对象和数组

## 6.1 浅拷贝与深拷贝

数据复制有两种“深度”：

- *浅拷贝*只复制对象和数组的顶层条目。条目值在原始和副本中仍然相同。
- *深拷贝*还会复制条目值的条目等。也就是说，它遍历以要复制的值为根的完整树，并复制所有节点。

接下来的章节将介绍这两种复制。不幸的是，JavaScript 只内置支持浅拷贝。如果我们需要深拷贝，则需要自己实现。

## 6.2 JavaScript 中的浅拷贝

让我们看看浅拷贝数据的几种方法。

### 6.2.1 通过展开复制普通对象和数组

我们可以通过展开[到对象字面量](https://exploringjs.com/impatient-js/ch_single-objects.html#spreading-into-object-literals)和[到数组字面量](https://exploringjs.com/impatient-js/ch_arrays.html#spreading-into-array-literals)来制作副本：

```javascript
const copyOfObject = {...originalObject};
const copyOfArray = [...originalArray];
```

唉，展开有几个问题。这些将在接下来的小节中介绍。其中，有些是真正的限制，有些只是特性。

#### 6.2.1.1 原型不会被复制

例如：

```javascript
class MyClass {}

const original = new MyClass();
assert.equal(original instanceof MyClass, true);

const copy = {...original};
assert.equal(copy instanceof MyClass, false);
```

注意以下两个表达式是等价的：

```javascript
obj instanceof SomeClass
SomeClass.prototype.isPrototypeOf(obj)
```

因此，我们可以通过给副本赋予与原始相同的原型来修复这个问题：

```javascript
class MyClass {}

const original = new MyClass();

const copy = {
  __proto__: Object.getPrototypeOf(original),
  ...original,
};
assert.equal(copy instanceof MyClass, true);
```

或者，我们可以在创建副本后通过`Object.setPrototypeOf()`设置其原型。

#### 6.2.1.2 许多内置对象具有特殊的“内部插槽”，这些插槽不会被复制

此类内置对象的示例包括正则表达式和日期。如果我们复制它们，就会丢失其中存储的大部分数据。

#### 6.2.1.3 只复制自有（非继承）属性



鉴于[原型链](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains)的工作方式，这通常是正确的方法。但我们仍然需要意识到这一点。在以下示例中，`original` 的继承属性 `.inheritedProp` 在 `copy` 中不可用，因为我们只复制了自有属性，而没有保留原型。

```js
const proto = { inheritedProp: 'a' };
const original = {__proto__: proto, ownProp: 'b' };
assert.equal(original.inheritedProp, 'a');
assert.equal(original.ownProp, 'b');

const copy = {...original};
assert.equal(copy.inheritedProp, undefined);
assert.equal(copy.ownProp, 'b');
```

#### 6.2.1.4 只复制可枚举属性

例如，数组实例的自有属性 `.length` 是不可枚举的，因此不会被复制：

```js
const arr = ['a', 'b'];
assert.equal(arr.length, 2);
assert.equal({}.hasOwnProperty.call(arr, 'length'), true);

const copy = {...arr};
assert.equal({}.hasOwnProperty.call(copy, 'length'), false);
```

这也很少成为限制，因为大多数属性都是可枚举的。如果需要复制不可枚举属性，可以使用 `Object.getOwnPropertyDescriptors()` 和 `Object.defineProperties()` 来复制对象（如何操作将在后面解释）：

- 它们考虑所有属性（不仅仅是 `value`），因此能正确复制 getter、setter、只读属性等。
- `Object.getOwnPropertyDescriptors()` 检索可枚举和不可枚举属性。

有关可枚举性的更多信息，请参见 §12 “属性的可枚举性”。

#### 6.2.1.5 属性描述符并不总是被忠实地复制

无论属性的描述符如何，其副本始终是一个可写且可配置的数据属性。

例如，这里我们创建了属性 `original.prop`，其描述符 `writable` 和 `configurable` 均为 `false`：

```js
const original = Object.defineProperties(
  {}, {
    prop: {
      value: 1,
      writable: false,
      configurable: false,
      enumerable: true,
    },
  });
assert.deepEqual(original, {prop: 1});
```

如果我们复制 `.prop`，那么 `writable` 和 `configurable` 都变为 `true`：

```js
const copy = {...original};
// Attributes `writable` and `configurable` of copy are different:
assert.deepEqual(
  Object.getOwnPropertyDescriptors(copy),
  {
    prop: {
      value: 1,
      writable: true,
      configurable: true,
      enumerable: true,
    },
  });
```

因此，getter 和 setter 也无法被忠实地复制：

```js
const original = {
  get myGetter() { return 123 },
  set mySetter(x) {},
};
assert.deepEqual({...original}, {
  myGetter: 123, // 不再是 getter！
  mySetter: undefined,
});
```

前面提到的 `Object.getOwnPropertyDescriptors()` 和 `Object.defineProperties()` 总是会完整地转移自有属性及其所有特性（稍后展示）。

#### 6.2.1.6 复制是浅层的

复制会为 `original` 中的每个键值对创建新版本，但 `original` 的值本身不会被复制。例如：

```js
const original = {name: 'Jane', work: {employer: 'Acme'}};
const copy = {...original};

// .name 属性是副本：修改副本不会影响原对象
copy.name = 'John';
assert.deepEqual(original,
  {name: 'Jane', work: {employer: 'Acme'}});
assert.deepEqual(copy,
  {name: 'John', work: {employer: 'Acme'}});

// .work 的值是共享的：修改副本会影响原对象
copy.work.employer = 'Spectre';
assert.deepEqual(
  original, {name: 'Jane', work: {employer: 'Spectre'}});
assert.deepEqual(
  copy, {name: 'John', work: {employer: 'Spectre'}});
```

我们将在本章后面讨论深拷贝。

### 6.2.2 通过 `Object.assign()` 进行浅拷贝（可选）

`Object.assign()` 的工作方式与展开到对象中大致相同。也就是说，以下两种复制方式基本等价：

```js
const copy1 = {...original};
const copy2 = Object.assign({}, original);
```

使用方法而非语法的好处是，可以通过库在较旧的 JavaScript 引擎上进行 polyfill。

不过，`Object.assign()` 并不完全等同于展开。它在一个相对微妙的点上有所不同：创建属性的方式不同。

- `Object.assign()` 使用*赋值*来创建副本的属性。
- 展开在副本中*定义*新属性。

其中，赋值会调用自有和继承的 setter，而定义则不会（关于赋值与定义的更多信息）。这种差异很少被注意到。以下代码是一个例子，但有些刻意：

```js
const original = {['__proto__']: null}; // (A)
const copy1 = {...original};
// copy1 拥有自有属性 '__proto__'
assert.deepEqual(
  Object.keys(copy1), ['__proto__']);

const copy2 = Object.assign({}, original);
// copy2 的原型为 null
assert.equal(Object.getPrototypeOf(copy2), null);
```

通过在 A 行使用计算属性键，我们将 `.__proto__` 创建为自有属性，并且没有调用继承的 setter。然而，当 `Object.assign()` 复制该属性时，它会调用 setter。（关于 `.__proto__` 的更多信息，请参见[《JavaScript 面向不耐烦程序员》](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#proto)）

### 6.2.3 通过 `Object.getOwnPropertyDescriptors()` 和 `Object.defineProperties()` 进行浅拷贝（可选）

JavaScript 允许我们通过*属性描述符*（用于指定属性特性的对象）来创建属性。例如，通过 `Object.defineProperties()`，我们之前已经见过它的用法。如果将该方法与 `Object.getOwnPropertyDescriptors()` 结合使用，我们可以更忠实地进行复制：

```js
function copyAllOwnProperties(original) {
  return Object.defineProperties(
    {}, Object.getOwnPropertyDescriptors(original));
}
```

这消除了通过展开复制对象的两个问题。

首先，所有自有属性的特性都被正确复制。因此，我们现在可以复制自有 getter 和自有 setter：

```js
const original = {
  get myGetter() { return 123 },
  set mySetter(x) {},
};
assert.deepEqual(copyAllOwnProperties(original), original);
```

其次，得益于 `Object.getOwnPropertyDescriptors()`，不可枚举的属性也会被复制：

```js
const arr = ['a', 'b'];
assert.equal(arr.length, 2);
assert.equal({}.hasOwnProperty.call(arr, 'length'), true);

const copy = copyAllOwnProperties(arr);
assert.equal({}.hasOwnProperty.call(copy, 'length'), true);
```

## 6.3 JavaScript 中的深拷贝

现在是时候解决深拷贝问题了。首先，我们将手动进行深拷贝，然后探讨通用方法。

### 6.3.1 通过嵌套展开进行手动深拷贝

如果嵌套使用展开，我们可以得到深拷贝：

```js
const original = {name: 'Jane', work: {employer: 'Acme'}};
const copy = {name: original.name, work: {...original.work}};

// 复制成功：
assert.deepEqual(original, copy);
// 拷贝是深层的：
assert.ok(original.work !== copy.work);
```

### 6.3.2 技巧：通过 JSON 进行通用深拷贝

这是一种技巧，但在紧急情况下能提供快速解决方案：为了深拷贝对象 `original`，我们首先将其转换为 JSON 字符串，然后解析该 JSON 字符串：

```js
function jsonDeepCopy(original) {
  return JSON.parse(JSON.stringify(original));
}
const original = {name: 'Jane', work: {employer: 'Acme'}};
const copy = jsonDeepCopy(original);
assert.deepEqual(original, copy);
```

这种方法的一个显著缺点是，我们只能复制键和值受 JSON 支持的属性。

一些不支持的键和值会被直接忽略：

```js
assert.deepEqual(
  jsonDeepCopy({
    // 符号不支持作为键
    [Symbol('a')]: 'abc',
    // 不支持的值
    b: function () {},
    // 不支持的值
    c: undefined,
  }),
  {} // 空对象
);
```

其他情况则会引发异常：

```js
assert.throws(
  () => jsonDeepCopy({a: 123n}),
  /^TypeError: Do not know how to serialize a BigInt$/);
```

### 6.3.3 实现通用深拷贝

以下函数可以通用地深拷贝一个值 `original`：

```js
function deepCopy(original) {
  if (Array.isArray(original)) {
    const copy = [];
    for (const [index, value] of original.entries()) {
      copy[index] = deepCopy(value);
    }
    return copy;
  } else if (typeof original === 'object' && original !== null) {
    const copy = {};
    for (const [key, value] of Object.entries(original)) {
      copy[key] = deepCopy(value);
    }
    return copy;
  } else {
    // 原始值：原子性，无需复制
    return original;
  }
}
```

该函数处理三种情况：

- 如果 `original` 是数组，我们创建一个新数组，并将 `original` 的元素深拷贝进去。
- 如果 `original` 是对象，我们采用类似的方法。
- 如果 `original` 是原始值，我们无需做任何操作。

让我们试试 `deepCopy()`：

```js
const original = {a: 1, b: {c: 2, d: {e: 3}}};
const copy = deepCopy(original);

// Are copy and original deeply equal?
assert.deepEqual(copy, original);

// Did we really copy all levels
// (equal content, but different objects)?
assert.ok(copy     !== original);
assert.ok(copy.b   !== original.b);
assert.ok(copy.b.d !== original.b.d);
```

请注意，`deepCopy()` 只解决了展开操作的一个问题：浅拷贝。其他问题依然存在：原型不会被拷贝，特殊对象只能部分拷贝，不可枚举属性被忽略，大多数属性特性被忽略。

完全通用地实现拷贝通常是不可能的：并非所有数据都是树形结构，有时我们不想拷贝所有属性等。

#### 6.3.3.1 更简洁的 `deepCopy()` 版本

如果我们使用 `.map()` 和 `Object.fromEntries()`，可以使之前的 `deepCopy()` 实现更加简洁：

```js
function deepCopy(original) {
  if (Array.isArray(original)) {
    return original.map(elem => deepCopy(elem));
  } else if (typeof original === 'object' && original !== null) {
    return Object.fromEntries(
      Object.entries(original)
        .map(([k, v]) => [k, deepCopy(v)]));
  } else {
    // 原始值：原子性，无需拷贝
    return original;
  }
}
```

## 6.4 延伸阅读

- §14 “拷贝类实例：`.clone()` 与拷贝构造函数”解释了基于类的拷贝模式。
- [“展开到对象字面量”章节](https://exploringjs.com/impatient-js/ch_single-objects.html#spreading-into-object-literals) 出自《JavaScript 快速入门》
- [“展开到数组字面量”章节](https://exploringjs.com/impatient-js/ch_arrays.html#spreading-into-array-literals) 出自《JavaScript 快速入门》
- [“原型链”章节](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains) 出自《JavaScript 快速入门》

# 7 破坏性更新与非破坏性更新数据

### 7.1 示例：破坏性更新与非破坏性更新对象



### 7.2 示例：破坏性更新与非破坏性更新数组

### 7.3 手动深度更新

### 7.4 实现通用深度更新

---

在本章中，我们将学习两种不同的数据更新方式：

- **破坏性更新**会改变数据本身，使其达到所需形式。
- **非破坏性更新**会创建数据的副本，并使副本达到所需形式。

后一种方式类似于先复制再破坏性修改，但它是同时进行的。

## 7.1 示例：破坏性更新与非破坏性更新对象

以下代码展示了一个破坏性更新对象属性的函数，并在一个对象上使用它。

```javascript
function setPropertyDestructively(obj, key, value) {
  obj[key] = value;
  return obj;
}

const obj = {city: 'Berlin', country: 'Germany'};
setPropertyDestructively(obj, 'city', 'Munich');
assert.deepEqual(obj, {city: 'Munich', country: 'Germany'});
```

以下代码演示了对象的非破坏性更新：

```javascript
function setPropertyNonDestructively(obj, key, value) {
  const updatedObj = {};
  for (const [k, v] of Object.entries(obj)) {
    updatedObj[k] = (k === key ? value : v);
  }
  return updatedObj;
}

const obj = {city: 'Berlin', country: 'Germany'};
const updatedObj = setPropertyNonDestructively(obj, 'city', 'Munich');

// 我们创建了一个更新后的对象：
assert.deepEqual(updatedObj, {city: 'Munich', country: 'Germany'});

// 但原始对象并未改变：
assert.deepEqual(obj, {city: 'Berlin', country: 'Germany'});
```

使用展开操作可以使`setPropertyNonDestructively()`更加简洁：

```javascript
function setPropertyNonDestructively(obj, key, value) {
  return {...obj, [key]: value};
}
```

`setPropertyNonDestructively()`的两个版本都是**浅层更新**：它们只改变对象的顶层。

## 7.2 示例：破坏性更新与非破坏性更新数组

以下代码展示了一个破坏性更新数组元素的函数，并在一个数组上使用它。

```javascript
function setElementDestructively(arr, index, value) {
  arr[index] = value;
}

const arr = ['a', 'b', 'c', 'd', 'e'];
setElementDestructively(arr, 2, 'x');
assert.deepEqual(arr, ['a', 'b', 'x', 'd', 'e']);
```

以下代码演示了数组的非破坏性更新：

```javascript
function setElementNonDestructively(arr, index, value) {
  const updatedArr = [];
  for (const [i, v] of arr.entries()) {
    updatedArr.push(i === index ? value : v);
  }
  return updatedArr;
}

const arr = ['a', 'b', 'c', 'd', 'e'];
const updatedArr = setElementNonDestructively(arr, 2, 'x');
assert.deepEqual(updatedArr, ['a', 'b', 'x', 'd', 'e']);
assert.deepEqual(arr, ['a', 'b', 'c', 'd', 'e']);
```

使用`.slice()`和展开操作可以使`setElementNonDestructively()`更加简洁：

```javascript
function setElementNonDestructively(arr, index, value) {
  return [
    ...arr.slice(0, index), value, ...arr.slice(index+1)];
}
```

`setElementNonDestructively()`的两个版本都是**浅层更新**：它们只改变数组的顶层。

## 7.3 手动深度更新

到目前为止，我们只进行了浅层数据更新。现在来应对深度更新。以下代码展示了如何手动进行深度更新。我们正在更改姓名和雇主。

```javascript
const original = {name: 'Jane', work: {employer: 'Acme'}};
const updatedOriginal = {
  ...original,
  name: 'John',
  work: {
    ...original.work,
    employer: 'Spectre'
  },
};

assert.deepEqual(
  original, {name: 'Jane', work: {employer: 'Acme'}});
assert.deepEqual(
  updatedOriginal, {name: 'John', work: {employer: 'Spectre'}});
```

## 7.4 实现通用深度更新

以下函数实现了通用的深度更新。

```javascript
function deepUpdate(original, keys, value) {
  if (keys.length === 0) {
    return value;
  }
  const currentKey = keys[0];
  if (Array.isArray(original)) {
    return original.map(
      (v, index) => index === currentKey
        ? deepUpdate(v, keys.slice(1), value) // (A)
        : v); // (B)
  } else if (typeof original === 'object' && original !== null) {
    return Object.fromEntries(
      Object.entries(original).map(
        (keyValuePair) => {
          const [k,v] = keyValuePair;
          if (k === currentKey) {
            return [k, deepUpdate(v, keys.slice(1), value)]; // (C)
          } else {
            return keyValuePair; // (D)
          }
        }));
  } else {
    // 原始值
    return original;
  }
}
```

如果我们将`value`视为正在更新的树的根节点，那么`deepUpdate()`只会深度修改单个分支（第 A 行和第 C 行）。所有其他分支都是浅拷贝（第 B 行和第 D 行）。

以下是使用`deepUpdate()`的示例：

```javascript
const original = {name: 'Jane', work: {employer: 'Acme'}};

const copy = deepUpdate(original, ['work', 'employer'], 'Spectre');
assert.deepEqual(copy, {name: 'Jane', work: {employer: 'Spectre'}});
assert.deepEqual(original, {name: 'Jane', work: {employer: 'Acme'}});
```

# 8 共享可变状态的问题及如何避免

---

- 8.1 什么是共享可变状态，为什么它有问题？
- 8.2 通过复制数据避免共享
  - 8.2.1 复制如何帮助解决共享可变状态？
- 8.3 通过非破坏性更新避免修改
  - 8.3.1 非破坏性更新如何帮助解决共享可变状态？
- 8.4 通过使数据不可变来防止修改
  - 8.4.1 不可变性如何帮助解决共享可变状态？
- 8.5 用于避免共享可变状态的库
  - 8.5.1 Immutable.js
  - 8.5.2 Immer

---

本章回答以下问题：

- 什么是共享可变状态？
- 为什么它有问题？
- 如何避免其问题？

## 8.1 什么是共享可变状态，为什么它有问题？

共享可变状态的工作原理如下：

- 如果两个或多个参与者可以更改相同的数据（变量、对象等）。
- 并且它们的生命周期重叠。
- 那么一个参与者的修改可能会阻止其他参与者正常工作。

请注意，这个定义适用于函数调用、协作式多任务（例如 JavaScript 中的异步函数）等。每种情况下的风险类似。

以下代码是一个示例。该示例并不真实，但它展示了风险且易于理解：

```javascript
function logElements(arr) {
  while (arr.length > 0) {
    console.log(arr.shift());
  }
}

function main() {
  const arr = ['banana', 'orange', 'apple'];

  console.log('Before sorting:');
  logElements(arr);

  arr.sort(); // changes arr

  console.log('After sorting:');
  logElements(arr); // (A)
}
main();

// Output:
// 'Before sorting:'
// 'banana'
// 'orange'
// 'apple'
// 'After sorting:'
```

在这个例子中，有两个独立的参与者：

- 函数`main()`希望在排序前后记录一个数组。
- 函数`logElements()`记录其参数`arr`的元素，但在记录时将其移除。

`logElements()`破坏了`main()`，导致它在第 A 行记录了一个空数组。

在本章的剩余部分，我们将探讨三种避免共享可变状态问题的方法：

- 通过复制数据避免共享
- 通过非破坏性更新避免修改
- 通过使数据不可变来防止修改

特别是，我们将回到刚刚看到的示例并修复它。

## 8.2 通过复制数据避免共享

复制数据是避免共享的一种方式。

![](img/file0.svg) **背景**

关于在 JavaScript 中复制数据的背景知识，请参阅本书的以下两章：

- §6 “复制对象和数组”
- §14 “复制类的实例：`.clone()`与复制构造函数”

### 8.2.1 复制如何帮助解决共享可变状态？

只要我们只*读取*共享状态，就不会有任何问题。在*修改*它之前，我们需要通过复制（根据需要尽可能深）来“取消共享”。

*防御性复制*是一种在可能出现问题的地方始终进行复制的技术。其目标是保护当前实体（函数、类等）的安全：

- 输入：复制传递给我们的（可能）共享数据，使我们能够使用这些数据而不受外部实体的干扰。
- 输出：在将内部数据暴露给外部方之前复制它，意味着该方无法破坏我们的内部活动。

请注意，这些措施保护我们免受其他方的侵害，同时也保护其他方免受我们的侵害。

接下来的部分将说明两种防御性复制。

#### 8.2.1.1 复制共享输入

回想一下本章开头的激励示例，我们遇到麻烦是因为`logElements()`修改了其参数`arr`：

```javascript
function logElements(arr) {
  while (arr.length > 0) {
    console.log(arr.shift());
  }
}
```

让我们向这个函数添加防御性复制：

```javascript
function logElements(arr) {
  arr = [...arr]; // defensive copy
  while (arr.length > 0) {
    console.log(arr.shift());
  }
}
```

现在，如果在`main()`内部调用`logElements()`，它不会再引起问题：

```javascript
function main() {
  const arr = ['banana', 'orange', 'apple'];

  console.log('Before sorting:');
  logElements(arr);

  arr.sort(); // changes arr

  console.log('After sorting:');
  logElements(arr); // (A)
}
main();

// Output:
// 'Before sorting:'
// 'banana'
// 'orange'
// 'apple'
// 'After sorting:'
// 'apple'
// 'banana'
// 'orange'
```

#### 8.2.1.2 复制暴露的内部数据

让我们从一个类`StringBuilder`开始，它没有复制暴露的内部数据（第 A 行）：

```java
class StringBuilder {
  _data = [];
  add(str) {
    this._data.push(str);
  }
  getParts() {
    // We expose internals without copying them:
    return this._data; // (A)
  }
  toString() {
    return this._data.join('');
  }
}
```

只要不使用`.getParts()`，一切正常：

```javascript
const sb1 = new StringBuilder();
sb1.add('Hello');
sb1.add(' world!');
assert.equal(sb1.toString(), 'Hello world!');
```

然而，如果`.getParts()`的结果被修改（第 A 行），那么`StringBuilder`将无法正常工作：



```java
const sb2 = new StringBuilder();
sb2.add('Hello');
sb2.add(' world!');
sb2.getParts().length = 0; // (A)
assert.equal(sb2.toString(), ''); // 不正常
```

解决方案是在暴露内部`._data`之前进行防御性复制（第 A 行）：

```java
class StringBuilder {
  this._data = [];
  add(str) {
    this._data.push(str);
  }
  getParts() {
    // 防御性复制
    return [...this._data]; // (A)
  }
  toString() {
    return this._data.join('');
  }
}
```

现在修改`.getParts()`的结果不会再干扰`sb`的操作：

```java
const sb = new StringBuilder();
sb.add('Hello');
sb.add(' world!');
sb.getParts().length = 0;
assert.equal(sb.toString(), 'Hello world!'); // 正常
```

## 8.3 通过非破坏性更新避免变更

如果我们只进行非破坏性数据更新，就可以避免变更。

![](img/file0.svg) **背景**

关于数据更新的更多信息，请参见§7 “破坏性与非破坏性数据更新”。

### 8.3.1 非破坏性更新如何帮助处理共享可变状态？

通过非破坏性更新，共享数据变得毫无问题，因为我们从不修改共享数据。（这只有在所有访问数据的人都这样做时才有效！）

有趣的是，复制数据变得非常简单：

```java
const original = {city: 'Berlin', country: 'Germany'};
const copy = original;
```

这之所以可行，是因为我们只进行非破坏性更改，因此按需复制数据。

## 8.4 通过使数据不可变来防止变更

我们可以通过使共享数据不可变来防止对其的修改。

![](img/file0.svg) **背景**

关于如何在 JavaScript 中使数据不可变的背景知识，请参考本书的以下两章：

- §10 “保护对象不被更改”
- §15 “集合的不可变包装器”

### 8.4.1 不可变性如何帮助处理共享可变状态？

如果数据是不可变的，那么共享它就没有任何风险。特别是，不需要进行防御性复制。

![](img/file2.svg) **非破坏性更新是不可变数据的重要补充**

如果我们将两者结合，不可变数据实际上可以像可变数据一样灵活，但没有相关风险。

## 8.5 避免共享可变状态的库

JavaScript 中有几个库支持不可变数据和非破坏性更新。两个流行的库是：

- [Immutable.js](https://github.com/immutable-js/immutable-js) 提供了列表、栈、集合、映射等不可变数据结构。
- [Immer](https://immerjs.github.io/immer/) 也支持不可变性和非破坏性更新，但针对普通对象、数组、集合和映射。也就是说，不需要新的数据结构。

这些库将在接下来的两节中详细介绍。

### 8.5.1 Immutable.js

在其仓库中，[Immutable.js 库](https://github.com/immutable-js/immutable-js) 被描述为：

> 用于 JavaScript 的不可变持久数据集合，可提高效率和简洁性。

Immutable.js 提供了诸如以下不可变数据结构：

- `List`
- `Stack`
- `Set`（与 JavaScript 内置的 `Set` 不同）
- `Map`（与 JavaScript 内置的 `Map` 不同）
- 等等。

在以下示例中，我们使用了一个不可变的 `Map`：

```java
import {Map} from 'immutable/dist/immutable.es.js';
const map0 = Map([
  [false, 'no'],
  [true, 'yes'],
]);

// 我们创建 map0 的一个修改版本：
const map1 = map0.set(true, 'maybe');

// 修改后的版本与原版本不同：
assert.ok(map1 !== map0);
assert.equal(map1.equals(map0), false); // (A)

// 我们撤销刚才所做的更改：
const map2 = map1.set(true, 'yes');

// map2 是与 map0 不同的对象，
// 但内容相同
assert.ok(map2 !== map0);
assert.equal(map2.equals(map0), true); // (B)
```

注意：

- “破坏性”操作（如`.set()`）不会修改接收者，而是返回修改后的副本。
- 要检查两个数据结构是否具有相同的内容，我们使用内置的`.equals()`方法（第 A 行和第 B 行）。

### 8.5.2 Immer

在其仓库中，[Immer 库](https://immerjs.github.io/immer/) 被描述为：

> 通过修改当前状态来创建下一个不可变状态。

Immer 帮助非破坏性地更新（可能嵌套的）普通对象、数组、集合和映射。也就是说，不涉及自定义数据结构。

以下是使用 Immer 的样子：

```java
import {produce} from 'immer/dist/immer.module.js';

const people = [
  {name: 'Jane', work: {employer: 'Acme'}},
];

const modifiedPeople = produce(people, (draft) => {
  draft[0].work.employer = 'Cyberdyne';
  draft.push({name: 'John', work: {employer: 'Spectre'}});
});

assert.deepEqual(modifiedPeople, [
  {name: 'Jane', work: {employer: 'Cyberdyne'}},
  {name: 'John', work: {employer: 'Spectre'}},
]);
assert.deepEqual(people, [
  {name: 'Jane', work: {employer: 'Acme'}},
]);
```

原始数据存储在`people`中。`produce()`为我们提供了一个变量`draft`。我们假装这个变量就是`people`，并使用通常用于破坏性更改的操作。Immer 会拦截这些操作。它不会修改`draft`，而是非破坏性地更改`people`。结果由`modifiedPeople`引用。作为额外的好处，它是深度不可变的。

`assert.deepEqual()`之所以有效，是因为 Immer 返回普通对象和数组。

# 9 属性特性：简介

- 9.1 对象的结构
  - 9.1.1 内部槽位
  - 9.1.2 属性键
  - 9.1.3 属性特性
- 9.2 属性描述符
- 9.3 检索属性的描述符
  - 9.3.1 `Object.getOwnPropertyDescriptor()`：检索单个属性的描述符
  - 9.3.2 `Object.getOwnPropertyDescriptors()`：获取对象所有属性的描述符
- 9.4 通过描述符定义属性
  - 9.4.1 `Object.defineProperty()`：通过描述符定义单个属性
  - 9.4.2 `Object.defineProperties()`：通过描述符定义多个属性
- 9.5 `Object.create()`：通过描述符创建对象
- 9.6 `Object.getOwnPropertyDescriptors()`的使用场景
  - 9.6.1 使用场景：将属性复制到对象中
  - 9.6.2 `Object.getOwnPropertyDescriptors()`的使用场景：克隆对象
- 9.7 省略描述符属性
  - 9.7.1 创建属性时省略描述符属性
  - 9.7.2 修改属性时省略描述符属性
- 9.8 内置构造使用了哪些属性特性？
  - 9.8.1 通过赋值创建的自身属性
  - 9.8.2 通过对象字面量创建的自身属性
  - 9.8.3 数组的自身属性`.length`
  - 9.8.4 内置类的原型属性
  - 9.8.5 用户定义类的原型属性和实例属性
- 9.9 API：属性描述符
- 9.10 延伸阅读

---

在本章中，我们将更深入地了解 ECMAScript 规范如何看待 JavaScript 对象。特别地，在规范中，属性并非原子性的，而是由多个*特性*（可以理解为记录中的字段）组成。即使是数据属性的值，也存储在一个特性中！

## 9.1 对象的结构

[在 ECMAScript 规范中](https://tc39.es/ecma262/#sec-object-type)，一个对象由以下部分组成：

- *内部槽*，这些是 JavaScript 无法访问的存储位置，只能由规范中的操作访问。
- 一个*属性*集合。每个属性将一个*键*与*特性*（可以理解为记录中的字段）关联起来。

### 9.1.1 内部槽

[规范](https://tc39.es/ecma262/#sec-object-internal-methods-and-internal-slots)对内部槽的描述如下。我添加了项目符号并强调了其中一部分：

- 内部槽对应于与对象关联的内部状态，并被各种 ECMAScript 规范算法使用。
- 内部槽不是对象属性，也不会被继承。
- 根据具体的内部槽规范，这种状态可能由以下内容组成：
  - 任何 ECMAScript 语言类型的值，或
  - 特定的 ECMAScript 规范类型值。
- 除非另有明确说明，内部槽是在创建对象的过程中分配的，并且不能动态添加到对象中。
- 除非另有说明，内部槽的初始值为`undefined`。
- 本规范中的各种算法会创建具有内部槽的对象。然而，**ECMAScript 语言没有提供将内部槽与对象关联的直接方法**。
- 内部方法和内部槽在本规范中使用双中括号`[[ ]]`括起来的名称进行标识。

内部槽有两种：

- 用于操作对象（获取属性、设置属性等）的方法槽。
- 用于存储值的数据槽。

普通对象具有以下数据槽：

- `.[[Prototype]]: null | object`
  - 存储对象的原型。
  - 可以通过`Object.getPrototypeOf()`和`Object.setPrototypeOf()`间接访问。
- `.[[Extensible]]: boolean`
  - 指示是否可以向对象添加属性。
  - 可以通过`Object.preventExtensions()`设置为`false`。
- `.[[PrivateFieldValues]]: EntryList`
  - 用于管理[私有类字段](https://2ality.com/2019/07/private-class-fields.html)。

### 9.1.2 属性键

属性的键可以是：

- 字符串
- 符号（Symbol）

### 9.1.3 属性特性

有两种属性，它们通过各自的特性来区分：

- *数据属性*存储数据。其特性`value`保存任何 JavaScript 值。
- *访问器属性*由一个 getter 函数和/或一个 setter 函数组成。前者存储在特性`get`中，后者存储在特性`set`中。

此外，两种属性都共有一些特性。下表列出了所有特性及其默认值。

| 属性类型 | 特性的名称和类型 | 默认值 |
| --- | --- | --- |
| 数据属性 | `value: any` | `undefined` |
|  | `writable: boolean` | `false` |
| 访问器属性 | `get: (this: any) => any` | `undefined` |
|  | `set: (this: any, v: any) => void` | `undefined` |
| 所有属性 | `configurable: boolean` | `false` |
|  | `enumerable: boolean` | `false` |

我们已经遇到过特性`value`、`get`和`set`。其他特性的作用如下：

- `writable`决定数据属性的值是否可以被更改。
- `configurable`决定属性的特性是否可以被更改。如果它为`false`，则：
  - 我们不能删除该属性。
  - 我们不能将数据属性更改为访问器属性，反之亦然。
  - 我们不能更改除`value`之外的任何特性。
  - 然而，允许更改一个额外的特性：我们可以将`writable`从`true`改为`false`。这一异常背后的原因是[历史原因](https://stackoverflow.com/questions/9829817/why-can-i-set-enumerability-and-writability-of-unconfigurable-property-descrip/9843191#9843191)：数组的`.length`属性一直是可写且不可配置的。允许更改其`writable`特性使我们能够冻结数组。
- `enumerable`影响某些操作（例如`Object.keys()`）。如果它为`false`，则这些操作会忽略该属性。大多数属性都是可枚举的（例如通过赋值或对象字面量创建的属性），这就是为什么你在实践中很少注意到这个特性的原因。如果你仍然对其工作原理感兴趣，请参阅§12 “属性的可枚举性”。

#### 9.1.3.1 陷阱：继承的不可写属性阻止通过赋值创建自身属性

如果继承的属性是不可写的，我们就不能通过赋值来创建具有相同键的自身属性：

```java
const proto = {
  prop: 1,
};
// 使 proto.prop 不可写：
Object.defineProperty(
  proto, 'prop', {writable: false});

const obj = Object.create(proto);

assert.throws(
  () => obj.prop = 2,
  /^TypeError: Cannot assign to read only property 'prop'/);
```

更多信息，请参见§11.3.4 “继承的只读属性阻止通过赋值创建自有属性”。

## 9.2 属性描述符

*属性描述符*将属性的特性编码为一个 JavaScript 对象。它们的 TypeScript 接口如下所示。

```java
interface DataPropertyDescriptor {
  value?: any;
  writable?: boolean;
  configurable?: boolean;
  enumerable?: boolean;
}
interface AccessorPropertyDescriptor {
  get?: (this: any) => any;
  set?: (this: any, v: any) => void;
  configurable?: boolean;
  enumerable?: boolean;
}
type PropertyDescriptor = DataPropertyDescriptor | AccessorPropertyDescriptor;
```

问号表示所有属性都是可选的。§9.7 “省略描述符属性”描述了省略它们时会发生什么。

## 9.3 检索属性的描述符

### 9.3.1 `Object.getOwnPropertyDescriptor()`：检索单个属性的描述符

考虑以下对象：

```java
const legoBrick = {
  kind: 'Plate 1x3',
  color: 'yellow',
  get description() {
    return `${this.kind} (${this.color})`;
  },
};
```

首先，获取数据属性`.color`的描述符：

```java
assert.deepEqual(
  Object.getOwnPropertyDescriptor(legoBrick, 'color'),
  {
    value: 'yellow',
    writable: true,
    enumerable: true,
    configurable: true,
  });
```

这是访问器属性`.description`的描述符：



```javascript
const desc = Object.getOwnPropertyDescriptor.bind(Object);
assert.deepEqual(
  Object.getOwnPropertyDescriptor(legoBrick, 'description'),
  {
    get: desc(legoBrick, 'description').get, // (A)
    set: undefined,
    enumerable: true,
    configurable: true
  });
```

在 A 行使用工具函数`desc()`确保`.deepEqual()`正常工作。

### 9.3.2 `Object.getOwnPropertyDescriptors()`：检索对象所有属性的描述符

```javascript
const legoBrick = {
  kind: 'Plate 1x3',
  color: 'yellow',
  get description() {
    return `${this.kind} (${this.color})`;
  },
};

const desc = Object.getOwnPropertyDescriptor.bind(Object);
assert.deepEqual(
  Object.getOwnPropertyDescriptors(legoBrick),
  {
    kind: {
      value: 'Plate 1x3',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    color: {
      value: 'yellow',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    description: {
      get: desc(legoBrick, 'description').get, // (A)
      set: undefined,
      enumerable: true,
      configurable: true,
    },
  });
```

在 A 行使用辅助函数`desc()`确保`.deepEqual()`正常工作。

## 9.4 通过描述符定义属性

如果我们通过属性描述符`propDesc`定义键为`k`的属性，则会发生以下情况：

- 如果不存在键为`k`的属性，则会创建一个新的自有属性，该属性具有`propDesc`指定的特性。
- 如果存在键为`k`的属性，则定义会更改该属性的特性，使其与`propDesc`匹配。

### 9.4.1 `Object.defineProperty()`：通过描述符定义单个属性

首先，通过描述符创建一个新属性：

```javascript
const car = {};

Object.defineProperty(car, 'color', {
  value: 'blue',
  writable: true,
  enumerable: true,
  configurable: true,
});

assert.deepEqual(
  car,
  {
    color: 'blue',
  });
```

接下来，通过描述符更改属性的种类；我们将一个数据属性转换为 getter：

```javascript
const car = {
  color: 'blue',
};

let readCount = 0;
Object.defineProperty(car, 'color', {
  get() {
    readCount++;
    return 'red';
  },
});

assert.equal(car.color, 'red');
assert.equal(readCount, 1);
```

最后，通过描述符更改数据属性的值：

```javascript
const car = {
  color: 'blue',
};

// 使用与赋值相同的属性：
Object.defineProperty(
  car, 'color', {
    value: 'green',
    writable: true,
    enumerable: true,
    configurable: true,
  });

assert.deepEqual(
  car,
  {
    color: 'green',
  });
```

我们使用了与赋值相同的属性特性。

### 9.4.2 `Object.defineProperties()`：通过描述符定义多个属性

`Object.defineProperties()`是`Object.defineProperty()`的多属性版本：

```javascript
const legoBrick1 = {};
Object.defineProperties(
  legoBrick1,
  {
    kind: {
      value: 'Plate 1x3',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    color: {
      value: 'yellow',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    description: {
      get: function () {
        return `${this.kind} (${this.color})`;
      },
      enumerable: true,
      configurable: true,
    },
  });

assert.deepEqual(
  legoBrick1,
  {
    kind: 'Plate 1x3',
    color: 'yellow',
    get description() {
      return `${this.kind} (${this.color})`;
    },
  });
```

## 9.5 `Object.create()`：通过描述符创建对象

`Object.create()`创建一个新对象。它的第一个参数指定该对象的原型。可选的第二个参数指定该对象属性的描述符。在下一个示例中，我们创建与上一个示例相同的对象。

```javascript
const legoBrick2 = Object.create(
  Object.prototype,
  {
    kind: {
      value: 'Plate 1x3',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    color: {
      value: 'yellow',
      writable: true,
      enumerable: true,
      configurable: true,
    },
    description: {
      get: function () {
        return `${this.kind} (${this.color})`;
      },
      enumerable: true,
      configurable: true,
    },
  });

// 我们真的创建了相同的对象吗？
assert.deepEqual(legoBrick1, legoBrick2); // 是的！
```

## 9.6 `Object.getOwnPropertyDescriptors()`的用例

`Object.getOwnPropertyDescriptors()`在与`Object.defineProperties()`或`Object.create()`结合使用时，能帮助我们解决两个用例。

### 9.6.1 用例：将属性复制到对象中

自 ES6 起，JavaScript 已经有一个用于复制属性的工具方法：`Object.assign()`。然而，该方法使用简单的 get 和 set 操作来复制键为`key`的属性：

```javascript
target[key] = source[key];
```

这意味着它只有在以下情况下才能忠实地复制属性：

- 属性的`writable`属性为`true`，且`enumerable`属性为`true`（因为赋值操作就是这样创建属性的）。
- 它是一个数据属性。

以下示例说明了这一限制。对象`source`有一个键为`data`的 setter。

```javascript
const source = {
  set data(value) {
    this._data = value;
  }
};

// 因为只有 setter，属性 `data` 存在，
// 但值为 `undefined`。
assert.equal('data' in source, true);
assert.equal(source.data, undefined);
```

如果我们使用`Object.assign()`复制属性`data`，那么访问器属性`data`会被转换为数据属性：

```javascript
const target1 = {};
Object.assign(target1, source);

assert.deepEqual(
  Object.getOwnPropertyDescriptor(target1, 'data'),
  {
    value: undefined,
    writable: true,
    enumerable: true,
    configurable: true,
  });

// 作为对比，原始属性：
const desc = Object.getOwnPropertyDescriptor.bind(Object);
assert.deepEqual(
  Object.getOwnPropertyDescriptor(source, 'data'),
  {
    get: undefined,
    set: desc(source, 'data').set,
    enumerable: true,
    configurable: true,
  });
```

幸运的是，使用`Object.getOwnPropertyDescriptors()`配合`Object.defineProperties()`可以忠实地复制属性`data`：

```javascript
const target2 = {};
Object.defineProperties(
  target2, Object.getOwnPropertyDescriptors(source));

assert.deepEqual(
  Object.getOwnPropertyDescriptor(target2, 'data'),
  {
    get: undefined,
    set: desc(source, 'data').set,
    enumerable: true,
    configurable: true,
  });
```

#### 9.6.1.1 陷阱：复制使用`super`的方法

使用`super`的方法与其所在的*宿主对象*（存储该方法的对象）紧密绑定。目前还没有办法将这样的方法复制或移动到另一个对象。

### 9.6.2 `Object.getOwnPropertyDescriptors()`的用例：克隆对象

浅克隆与复制属性类似，因此`Object.getOwnPropertyDescriptors()`在这里也是一个不错的选择。

要创建克隆，我们使用`Object.create()`：

```javascript
const original = {
  set data(value) {
    this._data = value;
  }
};

const clone = Object.create(
  Object.getPrototypeOf(original),
  Object.getOwnPropertyDescriptors(original));

assert.deepEqual(original, clone);
```

有关此主题的更多信息，请参见第 6 章“复制对象和数组”。

## 9.7 省略描述符属性

描述符的所有属性都是可选的。省略某个属性时会发生什么取决于操作。

### 9.7.1 创建属性时省略描述符属性

当我们通过描述符创建新属性时，省略属性意味着使用它们的默认值：

```javascript
const car = {};
Object.defineProperty(
  car, 'color', {
    value: 'red',
  });
assert.deepEqual(
  Object.getOwnPropertyDescriptor(car, 'color'),
  {
    value: 'red',
    writable: false,
    enumerable: false,
    configurable: false,
  });
```

### 9.7.2 修改属性时省略描述符属性

相反，如果我们修改一个现有属性，省略描述符属性意味着相应的属性不会被触及：

```javascript
const car = {
  color: 'yellow',
};
assert.deepEqual(
  Object.getOwnPropertyDescriptor(car, 'color'),
  {
    value: 'yellow',
    writable: true,
    enumerable: true,
    configurable: true,
  });
Object.defineProperty(
  car, 'color', {
    value: 'pink',
  });
assert.deepEqual(
  Object.getOwnPropertyDescriptor(car, 'color'),
  {
    value: 'pink',
    writable: true,
    enumerable: true,
    configurable: true,
  });
```

## 9.8 内置构造使用了哪些属性特性？

关于属性特性的一般规则（少数例外情况除外）是：

- 原型链起始处的对象属性通常是`writable`、`enumerable`和`configurable`的。
- 如可枚举性章节所述，大多数继承的属性是不可枚举的，以便将它们隐藏起来，避免被`for-in`循环等旧式构造访问。继承的属性通常是`writable`和`configurable`的。

### 9.8.1 通过赋值创建的自身属性

```javascript
const obj = {};
obj.prop = 3;

assert.deepEqual(
  Object.getOwnPropertyDescriptors(obj),
  {
    prop: {
      value: 3,
      writable: true,
      enumerable: true,
      configurable: true,
    }
  });
```

### 9.8.2 通过对象字面量创建的自身属性

```javascript
const obj = { prop: 'yes' };

assert.deepEqual(
  Object.getOwnPropertyDescriptors(obj),
  {
    prop: {
      value: 'yes',
      writable: true,
      enumerable: true,
      configurable: true
    }
  });
```

### 9.8.3 数组的自身属性`.length`

数组的自身属性`.length`是不可枚举的，这样它就不会被`Object.assign()`、展开操作等复制。它也是不可配置的：

```javascript
> Object.getOwnPropertyDescriptor([], 'length')
{ value: 0, writable: true, enumerable: false, configurable: false }
> Object.getOwnPropertyDescriptor('abc', 'length')
{ value: 3, writable: false, enumerable: false, configurable: false }
```

`.length`是一个特殊的数据属性，因为它会受到其他自有属性（特别是索引属性）的影响，同时也会影响这些属性。

### 9.8.4 内置类的原型属性

```javascript
assert.deepEqual(
  Object.getOwnPropertyDescriptor(Array.prototype, 'map'),
  {
    value: Array.prototype.map,
    writable: true,
    enumerable: false,
    configurable: true
  });
```

### 9.8.5 用户自定义类的原型属性和实例属性



```js
class DataContainer {
  accessCount = 0;
  constructor(data) {
    this.data = data;
  }
  getData() {
    this.accessCount++;
    return this.data;
  }
}
assert.deepEqual(
  Object.getOwnPropertyDescriptors(DataContainer.prototype),
  {
    constructor: {
      value: DataContainer,
      writable: true,
      enumerable: false,
      configurable: true,
    },
    getData: {
      value: DataContainer.prototype.getData,
      writable: true,
      enumerable: false,
      configurable: true,
    }
  });
```

请注意，`DataContainer` 实例的所有自有属性都是可写、可枚举和可配置的：

```js
const dc = new DataContainer('abc')
assert.deepEqual(
  Object.getOwnPropertyDescriptors(dc),
  {
    accessCount: {
      value: 0,
      writable: true,
      enumerable: true,
      configurable: true,
    },
    data: {
      value: 'abc',
      writable: true,
      enumerable: true,
      configurable: true,
    }
  });
```

## 9.9 API：属性描述符

以下工具方法使用了属性描述符：

- `Object.defineProperty(obj: object, key: string|symbol, propDesc: PropertyDescriptor): object` ^([ES5])

  在 `obj` 上创建或修改一个属性，其键为 `key`，属性特性通过 `propDesc` 指定。返回修改后的对象。

  ```js
  const obj = {};
  const result = Object.defineProperty(
    obj, 'happy', {
      value: 'yes',
      writable: true,
      enumerable: true,
      configurable: true,
    });

  // obj 被返回并修改：
  assert.equal(result, obj);
  assert.deepEqual(obj, {
    happy: 'yes',
  });
  ```

- `Object.defineProperties(obj: object, properties: {[k: string|symbol]: PropertyDescriptor}): object` ^([ES5])

  `Object.defineProperty()` 的批量版本。对象 `properties` 的每个属性 `p` 指定一个要添加到 `obj` 的属性：`p` 的键指定属性的键，`p` 的值是一个描述符，指定该属性的特性。

  ```js
  const address1 = Object.defineProperties({}, {
    street: { value: 'Evergreen Terrace', enumerable: true },
    number: { value: 742, enumerable: true },
  });
  ```

- `Object.create(proto: null|object, properties?: {[k: string|symbol]: PropertyDescriptor}): object` ^([ES5])

  首先，创建一个原型为 `proto` 的对象。然后，如果提供了可选参数 `properties`，则按照与 `Object.defineProperties()` 相同的方式向该对象添加属性。最后，返回结果。例如，以下代码片段产生与前一个片段相同的结果：

  ```js
  const address2 = Object.create(Object.prototype, {
    street: { value: 'Evergreen Terrace', enumerable: true },
    number: { value: 742, enumerable: true },
  });
  assert.deepEqual(address1, address2);
  ```

- `Object.getOwnPropertyDescriptor(obj: object, key: string|symbol): undefined|PropertyDescriptor` ^([ES5])

  返回 `obj` 中键为 `key` 的自有（非继承）属性的描述符。如果不存在这样的属性，则返回 `undefined`。

  ```js
  assert.deepEqual(
    Object.getOwnPropertyDescriptor(Object.prototype, 'toString'),
    {
      value: {}.toString,
      writable: true,
      enumerable: false,
      configurable: true,
    });
  assert.equal(
    Object.getOwnPropertyDescriptor({}, 'toString'),
    undefined);
  ```

- `Object.getOwnPropertyDescriptors(obj: object): {[k: string|symbol]: PropertyDescriptor}` ^([ES2017])

  返回一个对象，其中 `obj` 的每个属性键 `'k'` 都映射到 `obj.k` 的属性描述符。结果可用作 `Object.defineProperties()` 和 `Object.create()` 的输入。

  ```js
  const propertyKey = Symbol('propertyKey');
  const obj = {
    [propertyKey]: 'abc',
    get count() { return 123 },
  };

  const desc = Object.getOwnPropertyDescriptor.bind(Object);
  assert.deepEqual(
    Object.getOwnPropertyDescriptors(obj),
    {
      [propertyKey]: {
        value: 'abc',
        writable: true,
        enumerable: true,
        configurable: true
      },
      count: {
        get: desc(obj, 'count').get, // (A)
        set: undefined,
        enumerable: true,
        configurable: true
      }
    });
  ```

  在第 A 行使用 `desc()` 是一种变通方法，以便 `.deepEqual()` 能够正常工作。

## 9.10 延伸阅读

接下来的三章提供了关于属性特性的更多细节：

- §10 “保护对象不被修改”
- §11 “属性：赋值 vs. 定义”
- §12 “属性的可枚举性”

# 10 保护对象不被修改

## 10.1 保护级别：禁止扩展、密封、冻结

## 10.2 禁止扩展

### 10.2.1 检查对象是否可扩展

## 10.3 密封

### 10.3.1 检查对象是否被密封

## 10.4 冻结

### 10.4.1 检查对象是否被冻结

### 10.4.2 冻结是浅层的

### 10.4.3 实现深度冻结

## 10.5 延伸阅读

在本章中，我们将探讨如何保护对象不被修改。示例包括：禁止添加属性和禁止修改属性。

![](img/file0.svg) **必备知识：属性特性**

阅读本章前，你应该熟悉属性特性。如果不熟悉，请查看 §9 “属性特性：入门”。

## 10.1 保护级别：阻止扩展、密封、冻结

JavaScript 提供了三种对象保护级别：

- *阻止扩展*：禁止向对象添加新属性，但仍可删除和修改现有属性。

  - 方法：`Object.preventExtensions(obj)`

- *密封*：阻止扩展，并使所有属性变为*不可配置*（大致意思是：无法再更改属性的工作方式）。

  - 方法：`Object.seal(obj)`

- *冻结*：在将所有属性设置为不可写后密封对象。也就是说，对象不可扩展，所有属性均为只读，且无法改变这一状态。

  - 方法：`Object.freeze(obj)`

## 10.2 阻止扩展

```ts
Object.preventExtensions<T>(obj: T): T
```

该方法的工作方式如下：

- 如果 `obj` 不是对象，则直接返回它。
- 否则，修改 `obj` 使其无法再添加新属性，然后返回它。
- 类型参数 `<T>` 表示返回结果与参数类型相同。

下面通过示例演示 `Object.preventExtensions()` 的用法：

```js
const obj = { first: 'Jane' };
Object.preventExtensions(obj);
assert.throws(
  () => obj.last = 'Doe',
  /^TypeError: Cannot add property last, object is not extensible$/);
```

但我们仍然可以删除属性：

```js
assert.deepEquals(
  Object.keys(obj), ['first']);
delete obj.first;
assert.deepEquals(
  Object.keys(obj), []);
```

### 10.2.1 检查对象是否可扩展

```ts
Object.isExtensible(obj: any): boolean
```

检查 `obj` 是否可扩展——例如：

```text
> const obj = {};
> Object.isExtensible(obj)
true
> Object.preventExtensions(obj)
{}
> Object.isExtensible(obj)
false
```

## 10.3 密封

```ts
Object.seal<T>(obj: T): T
```

该方法说明：

- 如果 `obj` 不是对象，则直接返回它。
- 否则，阻止 `obj` 扩展，使其所有属性变为*不可配置*，然后返回它。属性不可配置意味着无法再更改它们（除了值）：只读属性保持只读，可枚举属性保持可枚举，等等。

以下示例演示了密封会使对象不可扩展，且其属性变为不可配置。

```js
const obj = {
  first: 'Jane',
  last: 'Doe',
};

// 密封前
assert.equal(Object.isExtensible(obj), true);
assert.deepEqual(
  Object.getOwnPropertyDescriptors(obj),
  {
    first: {
      value: 'Jane',
      writable: true,
      enumerable: true,
      configurable: true
    },
    last: {
      value: 'Doe',
      writable: true,
      enumerable: true,
      configurable: true
    }
  });

Object.seal(obj);

// 密封后
assert.equal(Object.isExtensible(obj), false);
assert.deepEqual(
  Object.getOwnPropertyDescriptors(obj),
  {
    first: {
      value: 'Jane',
      writable: true,
      enumerable: true,
      configurable: false
    },
    last: {
      value: 'Doe',
      writable: true,
      enumerable: true,
      configurable: false
    }
  });
```

我们仍然可以修改属性 `.first` 的值：

```js
obj.first = 'John';
assert.deepEqual(
  obj, {first: 'John', last: 'Doe'});
```

但无法更改其属性描述符：

```js
assert.throws(
  () => Object.defineProperty(obj, 'first', { enumerable: false }),
  /^TypeError: Cannot redefine property: first$/);
```

### 10.3.1 检查对象是否已密封

```ts
Object.isSealed(obj: any): boolean
```

检查 `obj` 是否已密封——例如：

```text
> const obj = {};
> Object.isSealed(obj)
false
> Object.seal(obj)
{}
> Object.isSealed(obj)
true
```

## 10.4 冻结

```ts
Object.freeze<T>(obj: T): T;
```

- 如果 `obj` 不是对象，则立即返回 `obj`。
- 否则，将所有属性设置为不可写，密封 `obj`，然后返回它。也就是说，`obj` 不可扩展，所有属性均为只读，且无法改变这一状态。



```js
const point = { x: 17, y: -5 };
Object.freeze(point);

assert.throws(
  () => point.x = 2,
  /^TypeError: Cannot assign to read only property 'x'/
);

assert.throws(
  () => Object.defineProperty(point, 'x', {enumerable: false}),
  /^TypeError: Cannot redefine property: x$/
);

assert.throws(
  () => point.z = 4,
  /^TypeError: Cannot add property z, object is not extensible$/
);
```

### 10.4.1 检查对象是否已冻结

```js
Object.isFrozen(obj: any): boolean
```

检查`obj`是否已冻结——例如：

```js
> const point = { x: 17, y: -5 };
> Object.isFrozen(point)
false
> Object.freeze(point)
{ x: 17, y: -5 }
> Object.isFrozen(point)
true
```

### 10.4.2 冻结是浅层的

`Object.freeze(obj)`仅冻结`obj`及其属性，不会冻结这些属性的值——例如：

```js
const teacher = {
  name: 'Edna Krabappel',
  students: ['Bart'],
};
Object.freeze(teacher);

// 无法修改自有属性：
assert.throws(
  () => teacher.name = 'Elizabeth Hoover',
  /^TypeError: Cannot assign to read only property 'name'/
);

// 但遗憾的是，我们仍然可以修改自有属性的值：
teacher.students.push('Lisa');
assert.deepEqual(
  teacher, {
    name: 'Edna Krabappel',
    students: ['Bart', 'Lisa'],
  });
```

### 10.4.3 实现深度冻结

如果需要深度冻结，我们需要自己实现：

```js
function deepFreeze(value) {
  if (Array.isArray(value)) {
    for (const element of value) {
      deepFreeze(element);
    }
    Object.freeze(value);
  } else if (typeof value === 'object' && value !== null) {
    for (const v of Object.values(value)) {
      deepFreeze(v);
    }
    Object.freeze(value);
  } else {
    // 无需操作：原始值已经是不可变的
  }
  return value;
}
```

重新审视上一节的示例，检查`deepFreeze()`是否真正实现了深度冻结：

```js
const teacher = {
  name: 'Edna Krabappel',
  students: ['Bart'],
};
deepFreeze(teacher);

assert.throws(
  () => teacher.students.push('Lisa'),
  /^TypeError: Cannot add property 1, object is not extensible$/
);
```

## 10.5 延伸阅读

* 关于防止数据结构被更改的更多模式：参见 §15“集合的不可变包装器”。

# 11 属性：赋值 vs. 定义

## 11.1 赋值 vs. 定义

### 11.1.1 赋值

### 11.1.2 定义

## 11.2 理论中的赋值与定义（可选）

### 11.2.1 为属性赋值

### 11.2.2 定义属性

## 11.3 实践中的定义与赋值

### 11.3.1 只有定义允许我们创建具有任意属性的属性

### 11.3.2 赋值运算符不会更改原型中的属性

### 11.3.3 赋值调用 setter，定义不调用

### 11.3.4 继承的只读属性阻止通过赋值创建自有属性

## 11.4 哪些语言结构使用定义，哪些使用赋值？

### 11.4.1 对象字面量的属性通过定义添加

### 11.4.2 赋值运算符`=`始终使用赋值

### 11.4.3 公共类字段通过定义添加

## 11.5 本章的进一步阅读和资料来源

创建或更改对象`obj`的属性`prop`有两种方式：

* *赋值*：`obj.prop = true`

* *定义*：`Object.defineProperty(obj, '', {value: true})`

本章将解释它们的工作原理。

![](img/file0.svg) **所需知识：属性特性和属性描述符**

阅读本章前，你应该熟悉属性特性和属性描述符。如果不熟悉，请查看 §9“属性特性：简介”。

## 11.1 赋值 vs. 定义

### 11.1.1 赋值

我们使用赋值运算符`=`将值`value`赋给对象`obj`的属性`.prop`：

```js
obj.prop = value
```

该运算符的工作方式取决于`.prop`的外观：

* **更改属性**：如果存在自有数据属性`.prop`，赋值会将其值更改为`value`。

* **调用 setter**：如果`.prop`存在自有或继承的 setter，赋值会调用该 setter。

* **创建属性**：如果`.prop`没有自有数据属性，也没有自有或继承的 setter，赋值会创建一个新的自有数据属性。

也就是说，赋值的主要目的是进行更改。这就是它支持 setter 的原因。

### 11.1.2 定义

要定义对象`obj`的键为`propKey`的属性，我们使用如下方法：

```js
Object.defineProperty(obj, propKey, propDesc)
```

该方法的工作方式取决于属性的外观：

* **更改属性**：如果存在键为`propKey`的自有属性，定义会（如果可能）按照属性描述符`propDesc`指定的方式更改其属性特性。

* **创建属性**：否则，定义会（如果可能）创建一个具有`propDesc`指定特性的自有属性。

也就是说，定义的主要目的是创建自有属性（即使存在继承的 setter，它也会忽略）以及更改属性特性。

## 11.2 理论中的赋值与定义（可选）

![](img/file2.svg) **ECMAScript 规范中的属性描述符**

在规范操作中，属性描述符不是 JavaScript 对象，而是[记录](https://tc39.es/ecma262/#sec-list-and-record-specification-type)，这是一种规范内部的数据结构，包含*字段*。字段的键用双括号表示。例如，`Desc.[[Configurable]]`访问`Desc`的字段`.[[Configurable]]`。在与外部世界交互时，这些记录会与 JavaScript 对象相互转换。

### 11.2.1 为属性赋值

为属性赋值的实际工作由 ECMAScript 规范中的[以下操作](https://tc39.es/ecma262/#sec-ordinarysetwithowndescriptor)处理：

```text
OrdinarySetWithOwnDescriptor(O, P, V, Receiver, ownDesc)
```

参数如下：

* `O`是当前正在访问的对象。

* `P`是我们正在赋值的属性的键。

* `V`是我们赋值的值。

* `Receiver`是赋值开始的对象。

* `ownDesc`是`O[P]`的描述符，如果该属性不存在则为`null`。

返回值是一个布尔值，指示操作是否成功。如本章后面所述，严格模式下的赋值会在`OrdinarySetWithOwnDescriptor()`失败时抛出`TypeError`。

以下是该算法的高级摘要：

* 它遍历`Receiver`的原型链，直到找到键为`P`的属性。遍历通过递归调用`OrdinarySetWithOwnDescriptor()`完成。在递归过程中，`O`会改变并指向当前正在访问的对象，但`Receiver`保持不变。

* 根据遍历结果，会在`Receiver`（递归开始的地方）中创建一个自有属性，或者发生其他情况。

更详细地说，该算法的工作方式如下：

* 如果`ownDesc`是`undefined`，则我们尚未找到键为`P`的属性：

  * 如果`O`有原型`parent`，则返回`parent.[[Set]](P, V, Receiver)`。这将继续我们的搜索。该方法调用通常最终会递归调用`OrdinarySetWithOwnDescriptor()`。

  * 否则，我们对`P`的搜索失败，并按如下方式设置`ownDesc`：

    ```js
    {
      [[Value]]: undefined, [[Writable]]: true,
      [[Enumerable]]: true, [[Configurable]]: true
    }
    ```

    使用这个`ownDesc`，下一个`if`语句将在`Receiver`中创建一个自有属性。

* 如果`ownDesc`指定了一个数据属性，则我们找到了一个属性：

  * 如果`ownDesc.[[Writable]]`为`false`，则返回`false`。这意味着任何不可写的属性`P`（自有或继承的！）都会阻止赋值。

  * 令`existingDescriptor`为`Receiver.[[GetOwnProperty]](P)`。即，检索赋值开始处的属性描述符。现在我们有了：

    * 当前对象`O`和当前属性描述符`ownDesc`。

    * 原始对象`Receiver`和原始属性描述符`existingDescriptor`。

  * 如果`existingDescriptor`不是`undefined`：

    * （如果执行到这里，说明我们仍处于原型链的开头——我们仅在`Receiver`没有属性`P`时才递归。）

    * 以下两个`if`条件不应为`true`，因为`ownDesc`和`existingDesc`应该相等：

      * 如果`existingDescriptor`指定了一个访问器，则返回`false`。

      * 如果`existingDescriptor.[[Writable]]`为`false`，则返回`false`。

    * 返回`Receiver.[[DefineOwnProperty]](P, { [[Value]]: V })`。这个内部方法执行定义，我们用它来更改属性`Receiver[P]`的值。定义算法将在下一小节中描述。

  * 否则：

    * （如果执行到这里，说明`Receiver`没有键为`P`的自有属性。）

    * 返回`CreateDataProperty(Receiver, P, V)`。（[此操作](https://tc39.es/ecma262/#sec-createdataproperty)在其第一个参数中创建一个自有数据属性。）

* （如果执行到这里，说明`ownDesc`描述了一个自有或继承的访问器属性。）

* 令`setter`为`ownDesc.[[Set]]`。

* 如果`setter`是`undefined`，则返回`false`。

* 执行`Call(setter, Receiver, «V»)`.`Call()`会调用函数对象`setter`，并将`this`设置为`Receiver`，同时传入单个参数`V`（规范中列表使用法式引号`«»`表示）。

* 返回`true`。

#### 11.2.1.1 如何从赋值操作到达`OrdinarySetWithOwnDescriptor()`？

对非解构赋值进行求值涉及以下步骤：

* 在规范中，求值从[关于`AssignmentExpression`运行时语义的章节](https://tc39.es/ecma262/#sec-assignment-operators-runtime-semantics-evaluation)开始。该章节处理匿名函数的命名、解构等操作。

* 如果没有解构模式，则使用[`PutValue()`](https://tc39.es/ecma262/#sec-putvalue)执行赋值。

* 对于属性赋值，`PutValue()`会调用内部方法`.[[Set]]()`。

* 对于普通对象，[`.[[Set]]()`](https://tc39.es/ecma262/#sec-ordinary-object-internal-methods-and-internal-slots-set-p-v-receiver)会调用`OrdinarySet()`（进而调用`OrdinarySetWithOwnDescriptor()`）并返回结果。

值得注意的是，在严格模式下，如果`.[[Set]]()`的结果为`false`，`PutValue()`会抛出`TypeError`。

### 11.2.2 定义属性

定义属性的实际工作由 ECMAScript 规范中的[以下操作](https://tc39.es/ecma262/#sec-validateandapplypropertydescriptor)处理：

```text
ValidateAndApplyPropertyDescriptor(O, P, extensible, Desc, current)
```

参数如下：

* 对象`O`，我们想要在其上定义属性。存在一种特殊的仅验证模式，其中`O`为`undefined`。此处我们忽略该模式。

* 要定义的属性的键`P`。

* `extensible`指示`O`是否可扩展。

* `Desc`是一个属性描述符，指定我们希望属性具有的特性。

* `current`包含自有属性`O[P]`的属性描述符（如果存在）。否则，`current`为`undefined`。

操作的结果是一个布尔值，指示是否成功。失败可能产生不同的后果。某些调用者忽略该结果。其他调用者（如`Object.defineProperty()`）在结果为`false`时会抛出异常。

以下是该算法的总结：

* 如果`current`为`undefined`，则属性`P`当前不存在，必须创建。

  * 如果`extensible`为`false`，则返回`false`，表示无法添加该属性。

  * 否则，检查`Desc`并创建数据属性或访问器属性。

  * 返回`true`。

* 如果`Desc`没有任何字段，则返回`true`，表示操作成功（因为无需进行任何更改）。

* 如果`current.[[Configurable]]`为`false`：



- (`Desc` 不允许更改除 `value` 以外的特性。)

- 如果`Desc.[[Configurable]]`存在，则其值必须与`current.[[Configurable]]`相同。否则返回`false`。

- 同样的检查：`Desc.[[Enumerable]]`

- 接下来，我们验证属性描述符`Desc`：`current`描述的特性能否更改为`Desc`指定的值？如果不能，返回`false`。如果可以，继续。

  - 如果描述符是通用的（没有数据属性或访问器属性特有的特性），则验证成功，可以继续。

  - 否则，如果一个描述符指定了数据属性，另一个指定了访问器属性：

    - 当前属性必须是可配置的（否则无法按需更改其特性）。如果不是，则返回`false`。

    - 将当前属性从数据属性更改为访问器属性，或反之。在此过程中，保留`.[[Configurable]]`和`.[[Enumerable]]`的值，所有其他特性获得默认值（对象值特性为`undefined`，布尔值特性为`false`）。

  - 否则，如果两个描述符都指定了数据属性：

    - 如果`current.[[Configurable]]`和`current.[[Writable]]`均为`false`，则不允许任何更改，`Desc`和`current`必须指定相同的特性：

      - （由于`current.[[Configurable]]`为`false`，`Desc.[[Configurable]]`和`Desc.[[Enumerable]]`已在之前检查过，且值正确。）

      - 如果`Desc.[[Writable]]`存在且为`true`，则返回`false`。

      - 如果`Desc.[[Value]]`存在且与`current.[[Value]]`的值不同，则返回`false`。

      - 无需进一步操作。返回`true`，表示算法成功。

      - （注意，通常情况下，我们无法更改不可配置属性的任何特性，除了其值。此规则的一个例外是，我们始终可以从可写变为不可写。该算法正确处理了这一例外。）

  - 否则（两个描述符都指定了访问器属性）：

    - 如果`current.[[Configurable]]`为`false`，则不允许任何更改，`Desc`和`current`必须指定相同的特性：

      - （由于`current.[[Configurable]]`为`false`，`Desc.[[Configurable]]`和`Desc.[[Enumerable]]`已在之前检查过，且值正确。）

      - 如果`Desc.[[Set]]`存在，则其值必须与`current.[[Set]]`相同。否则返回`false`。

      - 同样的检查：`Desc.[[Get]]`

      - 无需进一步操作。返回`true`，表示算法成功。

- 将键为`P`的属性的特性设置为`Desc`指定的值。由于已经过验证，我们可以确信所有更改都是允许的。

- 返回`true`。

## 11.3 定义与赋值的实际应用

本节介绍属性定义和赋值工作方式的一些后果。

### 11.3.1 只有定义才能创建具有任意特性的属性

如果通过赋值创建自有属性，它总是创建`writable`、`enumerable`和`configurable`均为`true`的属性。

```js
const obj = {};
obj.dataProp = 'abc';
assert.deepEqual(
  Object.getOwnPropertyDescriptor(obj, 'dataProp'),
  {
    value: 'abc',
    writable: true,
    enumerable: true,
    configurable: true,
  });
```

因此，如果我们想指定任意特性，必须使用定义。

虽然我们可以在对象字面量中创建 getter 和 setter，但之后无法通过赋值添加它们。同样，我们需要定义。

### 11.3.2 赋值运算符不会更改原型中的属性

考虑以下设置，其中`obj`从`proto`继承了属性`prop`。

```js
const proto = { prop: 'a' };
const obj = Object.create(proto);
```

我们无法通过赋值给`obj.prop`来（破坏性地）更改`proto.prop`。这样做会创建一个新的自有属性：

```js
assert.deepEqual(
  Object.keys(obj), []);

obj.prop = 'b';

// 赋值生效了：
assert.equal(obj.prop, 'b');

// 但我们创建了一个自有属性并覆盖了 proto.prop，
// 并没有更改它：
assert.deepEqual(
  Object.keys(obj), ['prop']);
assert.equal(proto.prop, 'a');
```

这种行为的基本原理如下：原型可以拥有其所有后代共享的属性。如果我们只想更改某个后代的此类属性，必须通过覆盖以非破坏性方式进行。这样更改就不会影响其他后代。

### 11.3.3 赋值会调用 setter，定义不会

定义`obj`的属性`.prop`与对其赋值有什么区别？

如果进行定义，那么我们的意图是创建或更改`obj`的自身（非继承）属性。因此，定义会忽略继承的`.prop`设置器，如下例所示：

```js
let setterWasCalled = false;
const proto = {
  get prop() {
    return 'protoGetter';
  },
  set prop(x) {
    setterWasCalled = true;
  },
};
const obj = Object.create(proto);

assert.equal(obj.prop, 'protoGetter');

// 定义 obj.prop：
Object.defineProperty(
  obj, 'prop', { value: 'objData' });
assert.equal(setterWasCalled, false);

// 我们已经覆盖了获取器：
assert.equal(obj.prop, 'objData');
```

相反，如果对`.prop`进行赋值，那么我们的意图通常是更改已经存在的内容，并且该更改应由设置器处理：

```js
let setterWasCalled = false;
const proto = {
  get prop() {
    return 'protoGetter';
  },
  set prop(x) {
    setterWasCalled = true;
  },
};
const obj = Object.create(proto);

assert.equal(obj.prop, 'protoGetter');

// 对 obj.prop 赋值：
obj.prop = 'objData';
assert.equal(setterWasCalled, true);

// 获取器仍然有效：
assert.equal(obj.prop, 'protoGetter');
```

### 11.3.4 继承的只读属性阻止通过赋值创建自身属性

如果原型中的`.prop`是只读的，会发生什么？

```js
const proto = Object.defineProperty(
  {}, 'prop', {
    value: 'protoValue',
    writable: false,
  });
```

在任何从`proto`继承只读`.prop`的对象中，我们无法使用赋值来创建具有相同键的自身属性——例如：

```js
const obj = Object.create(proto);
assert.throws(
  () => obj.prop = 'objValue',
  /^TypeError: Cannot assign to read only property 'prop'/);
```

为什么不能赋值？其理由是：通过创建自身属性来覆盖继承属性可以被视为非破坏性地更改继承属性。可以说，如果属性不可写，我们就不应该能够这样做。

然而，定义`.prop`仍然有效，并允许我们覆盖：

```js
Object.defineProperty(
  obj, 'prop', { value: 'objValue' });
assert.equal(obj.prop, 'objValue');
```

没有设置器的访问器属性也被视为只读：

```js
const proto = {
  get prop() {
    return 'protoValue';
  }
};
const obj = Object.create(proto);
assert.throws(
  () => obj.prop = 'objValue',
  /^TypeError: Cannot set property prop of #<Object> which has only a getter$/);
```

![](img/file5.svg) **“覆盖错误”：利弊**

- 该特性在 ECMAScript 5.1 中引入。

- 一方面，这种行为与原型继承和设置器的工作方式一致。（因此，可以说它不是一个错误。）

- 另一方面，这种行为会导致深度冻结全局对象时产生不必要的副作用。

- 曾有人试图改变这种行为，但破坏了 Lodash 库，因此被放弃（[GitHub 上的拉取请求](https://github.com/tc39/ecma262/pull/1320#issuecomment-443485524)）。

- 背景知识：
  - [GitHub 上的拉取请求](https://github.com/tc39/ecma262/pull/1307)
  - [ECMAScript.org 上的 Wiki 页面](http://wiki.ecmascript.org/doku.php?id=strawman:fixing_override_mistake)（[存档](https://web.archive.org/web/20141230041441/http://wiki.ecmascript.org/doku.php?id=strawman:fixing_override_mistake)）

## 11.4 哪些语言结构使用定义，哪些使用赋值？

在本节中，我们将考察语言在哪些地方使用定义，在哪些地方使用赋值。我们通过跟踪是否调用了继承的设置器来检测使用了哪种操作。更多信息请参见 §11.3.3“赋值调用设置器，定义不调用”。

### 11.4.1 对象字面量的属性通过定义添加

当我们通过对象字面量创建属性时，JavaScript 始终使用定义（因此从不调用继承的设置器）：

```js
let lastSetterArgument;
const proto = {
  set prop(x) {
    lastSetterArgument = x;
  },
};
const obj = {
  __proto__: proto,
  prop: 'abc',
};
assert.equal(lastSetterArgument, undefined);
```

### 11.4.2 赋值运算符`=`始终使用赋值

赋值运算符`=`始终使用赋值来创建或更改属性。

```js
let lastSetterArgument;
const proto = {
  set prop(x) {
    lastSetterArgument = x;
  },
};
const obj = Object.create(proto);

// 普通赋值：
obj.prop = 'abc';
assert.equal(lastSetterArgument, 'abc');

// 通过解构赋值：
[obj.prop] = ['def'];
assert.equal(lastSetterArgument, 'def');
```

### 11.4.3 公共类字段通过定义添加

遗憾的是，尽管公共类字段的语法与赋值相同，但它们不使用赋值来创建属性，而是使用定义（就像对象字面量中的属性一样）：

```js
let lastSetterArgument1;
let lastSetterArgument2;
class A {
  set prop1(x) {
    lastSetterArgument1 = x;
  }
  set prop2(x) {
    lastSetterArgument2 = x;
  }
}
class B extends A {
  prop1 = 'one';
  constructor() {
    super();
    this.prop2 = 'two';
  }
}
new B();

// 公共类字段使用定义：
assert.equal(lastSetterArgument1, undefined);
// 在构造函数内部，我们触发了赋值：
assert.equal(lastSetterArgument2, 'two');
```

## 11.5 本章的进一步阅读和资料来源

- [“原型链”章节](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains)（来自《JavaScript 快速入门》）
- [Allen Wirfs-Brock 发送给 es-discuss 邮件列表的邮件](https://mail.mozilla.org/pipermail/es-discuss/2012-July/024227.html)：“赋值与定义之间的区别……在 ES 只有数据属性且 ES 代码无法操作属性特性时并不重要。”[这种情况在 ECMAScript 5 中发生了变化。]

# 12 属性的可枚举性

## 目录

- 12.1 可枚举性如何影响属性迭代结构
  - 12.1.1 仅考虑可枚举属性的操作
  - 12.1.2 同时考虑可枚举和不可枚举属性的操作
- 12.1.3 内省操作的命名规则
- 12.2 预定义属性和创建属性的可枚举性
- 12.3 可枚举性的使用场景
  - 12.3.1 使用场景：从`for-in`循环中隐藏属性
  - 12.3.2 使用场景：标记属性为不可复制
  - 12.3.3 将属性标记为私有
  - 12.3.4 从`JSON.stringify()`中隐藏自有属性
- 12.4 总结

可枚举性是对象属性的一个属性。在本章中，我们将深入探讨它的使用方式以及它如何影响诸如`Object.keys()`和`Object.assign()`等操作。

![](img/file0.svg) **必备知识：属性特性**

阅读本章前，你需要熟悉属性特性。如果不熟悉，请查阅 §9“属性特性：简介”。

## 12.1 可枚举性如何影响属性遍历结构

为了演示各种操作如何受可枚举性影响，我们使用以下对象`obj`，其原型为`proto`。



```js
const protoEnumSymbolKey = Symbol('protoEnumSymbolKey');
const protoNonEnumSymbolKey = Symbol('protoNonEnumSymbolKey');
const proto = Object.defineProperties({}, {
  protoEnumStringKey: {
    value: 'protoEnumStringKeyValue',
    enumerable: true,
  },
  [protoEnumSymbolKey]: {
    value: 'protoEnumSymbolKeyValue',
    enumerable: true,
  },
  protoNonEnumStringKey: {
    value: 'protoNonEnumStringKeyValue',
    enumerable: false,
  },
  [protoNonEnumSymbolKey]: {
    value: 'protoNonEnumSymbolKeyValue',
    enumerable: false,
  },
});

const objEnumSymbolKey = Symbol('objEnumSymbolKey');
const objNonEnumSymbolKey = Symbol('objNonEnumSymbolKey');
const obj = Object.create(proto, {
  objEnumStringKey: {
    value: 'objEnumStringKeyValue',
    enumerable: true,
  },
  [objEnumSymbolKey]: {
    value: 'objEnumSymbolKeyValue',
    enumerable: true,
  },
  objNonEnumStringKey: {
    value: 'objNonEnumStringKeyValue',
    enumerable: false,
  },
  [objNonEnumSymbolKey]: {
    value: 'objNonEnumSymbolKeyValue',
    enumerable: false,
  },
});
```

### 12.1.1 仅考虑可枚举属性的操作

表 2：忽略不可枚举属性的操作。

| 操作 |  | 字符串键 | Symbol 键 | 继承属性 |
| --- | --- | --- | --- | --- |
| `Object.keys()` | ES5 | `✔` | `✘` | `✘` |
| `Object.values()` | ES2017 | `✔` | `✘` | `✘` |
| `Object.entries()` | ES2017 | `✔` | `✘` | `✘` |
| 展开 `{...x}` | ES2018 | `✔` | `✔` | `✘` |
| `Object.assign()` | ES6 | `✔` | `✔` | `✘` |
| `JSON.stringify()` | ES5 | `✔` | `✘` | `✘` |
| `for-in` | ES1 | `✔` | `✘` | `✔` |

以下操作（总结于表 2）仅考虑可枚举属性：

- `Object.keys()` ^([ES5]) 返回可枚举自有字符串键属性的键。

  ```js
  > Object.keys(obj)
  [ 'objEnumStringKey' ]
  ```

- `Object.values()` ^([ES2017]) 返回可枚举自有字符串键属性的值。

  ```js
  > Object.values(obj)
  [ 'objEnumStringKeyValue' ]
  ```

- `Object.entries()` ^([ES2017]) 返回可枚举自有字符串键属性的键值对。（注意：`Object.fromEntries()` 确实接受 Symbol 作为键，但只创建可枚举属性。）

  ```js
  > Object.entries(obj)
  [ [ 'objEnumStringKey', 'objEnumStringKeyValue' ] ]
  ```

- 展开到对象字面量 ^([ES2018]) 仅考虑自有可枚举属性（字符串键或 Symbol 键）。

  ```js
  > const copy = {...obj};
  > Reflect.ownKeys(copy)
  [ 'objEnumStringKey', objEnumSymbolKey ]
  ```

- `Object.assign()` ^([ES6]) 仅复制可枚举的自有属性（字符串键或 Symbol 键）。

  ```js
  > const copy = Object.assign({}, obj);
  > Reflect.ownKeys(copy)
  [ 'objEnumStringKey', objEnumSymbolKey ]
  ```

- `JSON.stringify()` ^([ES5]) 仅序列化可枚举的自有字符串键属性。

  ```js
  > JSON.stringify(obj)
  '{"objEnumStringKey":"objEnumStringKeyValue"}'
  ```

- `for-in` 循环 ^([ES1]) 遍历自身和继承的可枚举字符串键属性的键。

  ```js
  const propKeys = [];
  for (const propKey in obj) {
    propKeys.push(propKey);
  }
  assert.deepEqual(
    propKeys, ['objEnumStringKey', 'protoEnumStringKey']);
  ```

`for-in` 是唯一一个可枚举性影响继承属性的内置操作。所有其他操作仅处理自有属性。

### 12.1.2 同时考虑可枚举和不可枚举属性的操作

表 3：同时考虑可枚举和不可枚举属性的操作。

| 操作 |  | 字符串键 | Symbol 键 | 继承属性 |
| --- | --- | --- | --- | --- |
| `Object.getOwnPropertyNames()` | ES5 | `✔` | `✘` | `✘` |
| `Object.getOwnPropertySymbols()` | ES6 | `✘` | `✔` | `✘` |
| `Reflect.ownKeys()` | ES6 | `✔` | `✔` | `✘` |
| `Object.getOwnPropertyDescriptors()` | ES2017 | `✔` | `✔` | `✘` |

以下操作（总结于表 3）同时考虑可枚举和不可枚举属性：

- `Object.getOwnPropertyNames()` ^([ES5]) 列出所有自有字符串键属性的键。

  ```js
  > Object.getOwnPropertyNames(obj)
  [ 'objEnumStringKey', 'objNonEnumStringKey' ]
  ```

- `Object.getOwnPropertySymbols()` ^([ES6]) 列出所有自有 Symbol 键属性的键。

  ```js
  > Object.getOwnPropertySymbols(obj)
  [ objEnumSymbolKey, objNonEnumSymbolKey ]
  ```

- `Reflect.ownKeys()` ^([ES6]) 列出所有自有属性的键。

  ```js
  > Reflect.ownKeys(obj)
  [
    'objEnumStringKey',
    'objNonEnumStringKey',
    objEnumSymbolKey,
    objNonEnumSymbolKey
  ]
  ```

- `Object.getOwnPropertyDescriptors()` ^([ES2017]) 列出所有自有属性的属性描述符。

  ```js
  > Object.getOwnPropertyDescriptors(obj)
  {
    objEnumStringKey: {
      value: 'objEnumStringKeyValue',
      writable: false,
      enumerable: true,
      configurable: false
    },
    objNonEnumStringKey: {
      value: 'objNonEnumStringKeyValue',
      writable: false,
      enumerable: false,
      configurable: false
    },
    [objEnumSymbolKey]: {
      value: 'objEnumSymbolKeyValue',
      writable: false,
      enumerable: true,
      configurable: false
    },
    [objNonEnumSymbolKey]: {
      value: 'objNonEnumSymbolKeyValue',
      writable: false,
      enumerable: false,
      configurable: false
    }
  }
  ```

### 12.1.3 内省操作的命名规则

*内省*使程序能够在运行时检查值的结构。这是一种*元编程*：普通编程是关于编写程序；元编程是关于检查和/或修改程序。

在 JavaScript 中，常用的内省操作名称较短，而不常用的操作名称较长。忽略不可枚举属性是常态，因此执行该操作的操作名称较短，而不执行该操作的操作名称较长：

- `Object.keys()` 忽略不可枚举属性。

- `Object.getOwnPropertyNames()` 列出所有自身属性的字符串键。

然而，`Reflect` 方法（例如 `Reflect.ownKeys()`）偏离了这一规则，因为 `Reflect` 提供了更“元”且与代理相关的操作。

此外，还做出了以下区分（自引入符号的 ES6 起）：

- *属性键* 是字符串或符号。

- *属性名* 是字符串类型的属性键。

- *属性符号* 是符号类型的属性键。

因此，`Object.keys()` 现在更好的名称应该是 `Object.names()`。

## 12.2 预定义属性和创建属性的可枚举性

在本节中，我们将 `Object.getOwnPropertyDescriptor()` 缩写如下：

```js
const desc = Object.getOwnPropertyDescriptor.bind(Object);
```

大多数数据属性创建时具有以下属性描述符：

```js
{
  writable: true,
  enumerable: false,
  configurable: true,
}
```

这包括：

- 赋值

- 对象字面量

- 公共类字段

- `Object.fromEntries()`

最重要的不可枚举属性是：

- 内置类的原型属性

  ```js
  > desc(Object.prototype, 'toString').enumerable
  false
  ```

- 通过用户定义类创建的原型属性

  ```js
  > desc(class {foo() {}}.prototype, 'foo').enumerable
  false
  ```

- 数组的 `.length` 属性：

  ```js
  > Object.getOwnPropertyDescriptor([], 'length')
  { value: 0, writable: true, enumerable: false, configurable: false }
  ```

- 字符串的 `.length` 属性（注意，原始值的所有属性都是只读的）：

  ```js
  > Object.getOwnPropertyDescriptor('', 'length')
  { value: 0, writable: false, enumerable: false, configurable: false }
  ```

接下来我们将探讨可枚举性的使用场景，这将告诉我们为什么某些属性是可枚举的，而其他属性则不是。

## 12.3 可枚举性的使用场景

可枚举性是一个不一致的特性。它确实有使用场景，但总是存在某种注意事项。在本节中，我们将介绍这些使用场景及其注意事项。

### 12.3.1 使用场景：从 `for-in` 循环中隐藏属性

`for-in` 循环遍历对象的所有可枚举字符串键属性，包括自身属性和继承属性。因此，属性 `enumerable` 用于隐藏不应被遍历的属性。这就是在 ECMAScript 1 中引入可枚举性的原因。

一般来说，最好避免使用 `for-in`。接下来的两个小节将解释原因。以下函数将帮助我们演示 `for-in` 的工作原理。

```js
function listPropertiesViaForIn(obj) {
  const result = [];
  for (const key in obj) {
    result.push(key);
  }
  return result;
}
```

#### 12.3.1.1 对对象使用 `for-in` 的注意事项

`for-in` 遍历所有属性，包括继承的属性：

```js
const proto = {enumerableProtoProp: 1};
const obj = {
  __proto__: proto,
  enumerableObjProp: 2,
};
assert.deepEqual(
  listPropertiesViaForIn(obj),
  ['enumerableObjProp', 'enumerableProtoProp']);
```

对于普通对象，`for-in` 不会看到继承的方法（如 `Object.prototype.toString()`），因为它们都是不可枚举的：

```js
const obj = {};
assert.deepEqual(
  listPropertiesViaForIn(obj),
  []);
```

在用户定义的类中，所有继承的属性也是不可枚举的，因此被忽略：

```js
class Person {
  constructor(first, last) {
    this.first = first;
    this.last = last;
  }
  getName() {
    return this.first + ' ' + this.last;
  }
}
const jane = new Person('Jane', 'Doe');
assert.deepEqual(
  listPropertiesViaForIn(jane),
  ['first', 'last']);
```

**结论：** 在对象中，`for-in` 会考虑继承属性，而我们通常希望忽略这些属性。此时，最好将 `for-of` 循环与 `Object.keys()`、`Object.entries()` 等结合使用。

#### 12.3.1.2 对数组使用 `for-in` 的注意事项

数组和字符串的自身属性 `.length` 是不可枚举的，因此 `for-in` 会忽略它：

```js
> listPropertiesViaForIn(['a', 'b'])
[ '0', '1' ]
> listPropertiesViaForIn('ab')
[ '0', '1' ]
```

然而，通常使用 `for-in` 遍历数组索引是不安全的，因为它会考虑所有继承属性和非索引的自身属性。以下示例演示了当数组具有非索引自身属性时会发生什么：

```js
const arr1 = ['a', 'b'];
assert.deepEqual(
  listPropertiesViaForIn(arr1),
  ['0', '1']);

const arr2 = ['a', 'b'];
arr2.nonIndexProp = 'yes';
assert.deepEqual(
  listPropertiesViaForIn(arr2),
  ['0', '1', 'nonIndexProp']);
```

**结论：** 不应使用 `for-in` 遍历数组的索引，因为它会同时考虑索引属性和非索引属性：

- 如果你对数组的键感兴趣，请使用数组方法 `.keys()`：

  ```js
  > [...['a', 'b', 'c'].keys()]
  [ 0, 1, 2 ]
  ```

- 如果你想遍历数组的元素，请使用 `for-of` 循环，它还有一个额外的好处，即也适用于其他可迭代数据结构。

### 12.3.2 使用场景：标记属性为不可复制

通过将属性设置为不可枚举，我们可以将它们隐藏在某些复制操作之外。让我们先检查两个历史复制操作，然后再转向更现代的复制操作。

#### 12.3.2.1 历史复制操作：Prototype 的 `Object.extend()`



[Prototype](https://en.wikipedia.org/wiki/Prototype_JavaScript_Framework) 是一个 JavaScript 框架，由 Sam Stephenson 于 2005 年 2 月创建，作为 Ruby on Rails 中 Ajax 支持的基础部分。

[Prototype 的 `Object.extend(destination, source)`](http://api.prototypejs.org/language/Object/extend/) 将 `source` 的所有可枚举自身属性和继承属性复制为 `destination` 的自身属性。[它的实现](https://github.com/prototypejs/prototype/blob/5fddd3e/src/prototype/lang/object.js#L88)如下：

```js
function extend(destination, source) {
  for (var property in source)
    destination[property] = source[property];
  return destination;
}
```

如果我们对对象使用 `Object.extend()`，可以看到它将继承属性复制为自身属性，并忽略不可枚举属性（它也忽略符号键属性）。所有这些都源于 `for-in` 的工作方式。

```js
const proto = Object.defineProperties({}, {
  enumProtoProp: {
    value: 1,
    enumerable: true,
  },
  nonEnumProtoProp: {
    value: 2,
    enumerable: false,
  },
});
const obj = Object.create(proto, {
  enumObjProp: {
    value: 3,
    enumerable: true,
  },
  nonEnumObjProp: {
    value: 4,
    enumerable: false,
  },
});

assert.deepEqual(
  extend({}, obj),
  {enumObjProp: 3, enumProtoProp: 1});
```

#### 12.3.2.2 历史上的复制操作：jQuery 的 `$.extend()`

[jQuery 的 `$.extend(target, source1, source2, ···)`](https://api.jquery.com/jquery.extend/) 与 `Object.extend()` 的工作方式类似：

- 它将 `source1` 的所有可枚举自有属性和继承属性复制为 `target` 的自有属性。
- 然后对 `source2` 执行相同操作。
- 以此类推。

#### 12.3.2.3 基于可枚举性进行复制的缺点

基于可枚举性进行复制存在几个缺点：

- 虽然可枚举性对于隐藏继承属性很有用，但之所以主要采用这种方式，是因为我们通常只想将自有属性复制为自有属性。通过忽略继承属性可以更好地实现同样的效果。
- 要复制哪些属性通常取决于当前任务；很少有一个单一标志能适用于所有用例。更好的做法是提供一个带有*谓词*（返回布尔值的回调函数）的复制操作，由它决定何时忽略属性。
- 可枚举性在复制时方便地隐藏了数组的自有属性 `.length`。但这是一种极其罕见的特殊情况：一个既影响兄弟属性又受兄弟影响的魔法属性。如果我们自己实现这种魔法，我们会使用（继承的）getter 和/或 setter，而不是（自有的）数据属性。

#### 12.3.2.4 `Object.assign()` ^([ES5])

在 ES6 中，[`Object.assign(target, source_1, source_2, ···)`](https://exploringjs.com/impatient-js/ch_single-objects.html#object.assign) 可用于将源对象合并到目标对象。所有源对象的自有可枚举属性（无论是字符串键还是符号键）都会被考虑。`Object.assign()` 使用“get”操作从源对象读取值，使用“set”操作向目标对象写入值。

关于可枚举性，`Object.assign()` 延续了 `Object.extend()` 和 `$.extend()` 的传统。[引用 Yehuda Katz 的话](https://mail.mozilla.org/pipermail/es-discuss/2012-October/025934.html)：

> `Object.assign` 将铺平所有已流通的 `extend()` API 的牛道。我们认为，在这些情况下不复制可枚举方法的先例足以让 `Object.assign` 采用这种行为。

换句话说：`Object.assign()` 的创建考虑到了从 `$.extend()`（及类似方法）的升级路径。它的方法比 `$.extend` 更清晰，因为它忽略了继承属性。

#### 12.3.2.5 一个罕见的例子：复制时非可枚举性有用的情况

非可枚举性有帮助的情况很少。一个罕见的例子是[库 `fs-extra` 最近遇到的一个问题](https://github.com/jprichardson/node-fs-extra/issues/577)：

- 内置的 Node.js 模块 `fs` 有一个属性 `.promises`，它包含一个对象，该对象提供了基于 Promise 的 `fs` API 版本。在该问题出现时，读取 `.promise` 会导致以下警告被记录到控制台：

  ```text
  ExperimentalWarning: The fs.promises API is experimental
  ```

- 除了提供自身功能外，`fs-extra` 还重新导出了 `fs` 中的所有内容。对于 CommonJS 模块，这意味着将 `fs` 的所有属性复制到 `fs-extra` 的 `module.exports` 中（[通过 `Object.assign()`](https://github.com/jprichardson/node-fs-extra/blob/master/lib/index.js)）。当 `fs-extra` 这样做时，就会触发该警告。这令人困惑，因为每次加载 `fs-extra` 时都会发生。
- [一个快速修复](https://github.com/nodejs/node/pull/20504)是将属性 `fs.promises` 设为不可枚举。之后，`fs-extra` 就忽略了它。

### 12.3.3 将属性标记为私有

如果我们将属性设为不可枚举，那么 `Object.keys()`、`for-in` 循环等就无法再看到它。对于这些机制而言，该属性是私有的。

然而，这种方法存在几个问题：

- 复制对象时，我们通常希望复制私有属性。这与将不应复制的属性设为不可枚举相冲突（参见上一节）。
- 该属性并非真正私有。获取、设置以及其他几种机制并不区分可枚举和不可枚举属性。
- 无论是查看源代码还是交互式操作，我们无法立即看出一个属性是否可枚举。命名约定（例如在属性名前加下划线）更容易被发现。
- 我们无法使用可枚举性来区分公共方法和私有方法，因为原型中的方法默认是不可枚举的。

### 12.3.4 从 `JSON.stringify()` 中隐藏自有属性

`JSON.stringify()` 不会在其输出中包含不可枚举的属性。因此，我们可以利用可枚举性来决定哪些自有属性应导出为 JSON。这个用例与上一个（将属性标记为私有）类似，但也有不同之处，因为它更侧重于导出，并且需要考虑一些细微差别。例如：能否从 JSON 完全重建对象？

作为可枚举性的替代方案，对象可以实现 `.toJSON()` 方法，`JSON.stringify()` 会将该方法返回的内容序列化为字符串，而不是对象本身。下一个示例演示了其工作原理。

```js
[](#cb247-1)class Point {
[](#cb247-2)  static fromJSON(json) {
[](#cb247-3)    return new Point(json[0], json[1]);
[](#cb247-4)  }
[](#cb247-5)  constructor(x, y) {
[](#cb247-6)    this.x = x;
[](#cb247-7)    this.y = y;
[](#cb247-8)  }
[](#cb247-9)  toJSON() {
[](#cb247-10)    return [this.x, this.y];
[](#cb247-11)  }
[](#cb247-12)}
[](#cb247-13)assert.equal(
[](#cb247-14)  JSON.stringify(new Point(8, -3)),
[](#cb247-15)  '[8,-3]'
[](#cb247-16));
```

我认为 `toJSON()` 比可枚举性更清晰。它还让我们在存储格式方面拥有更多自由。

## 12.4 结论

我们已经看到，几乎所有非可枚举性的应用都是变通方法，而现在已经有了其他更好的解决方案。

对于我们自己的代码，我们通常可以假装可枚举性不存在：

- 通过对象字面量和赋值创建属性时，总是创建可枚举属性。
- 通过类创建的原型属性总是不可枚举的。

也就是说，我们自动遵循了最佳实践。

# 13 实例化类的技术

- 13.1 问题：异步初始化属性
- 13.2 解决方案：基于 Promise 的构造函数
  - 13.2.1 使用立即调用的异步箭头函数
- 13.3 解决方案：静态工厂方法
  - 13.3.1 改进：通过秘密令牌实现私有构造函数
  - 13.3.2 改进：构造函数抛出异常，工厂方法借用类原型
  - 13.3.3 改进：实例默认处于非活动状态，由工厂方法激活
  - 13.3.4 变体：独立的工厂函数
- 13.4 子类化基于 Promise 的构造函数（可选）
- 13.5 结论
- 13.6 延伸阅读

在本章中，我们将通过多次解决一个具体问题来探讨创建类实例的几种方法：构造函数、工厂函数等。本章的重点是类，因此忽略了类的替代方案。

## 13.1 问题：异步初始化属性

以下容器类旨在异步接收其属性 `.data` 的内容。这是我们的首次尝试：

```js
class DataContainer {
  #data; // (A)
  constructor() {
    Promise.resolve('downloaded')
      .then(data => this.#data = data); // (B)
  }
  getData() {
    return 'DATA: '+this.#data; // (C)
  }
}
```

这段代码的关键问题：属性 `.data` 初始为 `undefined`。

```js
const dc = new DataContainer();
assert.equal(dc.getData(), 'DATA: undefined');
setTimeout(() => assert.equal(
  dc.getData(), 'DATA: downloaded'), 0);
```

在第 A 行，我们声明了[私有字段](https://2ality.com/2019/07/private-class-fields.html) `.#data`，并在第 B 行和第 C 行中使用它。

`DataContainer` 构造函数内部的 `Promise` 是异步完成的，这就是为什么我们只能通过 `setTimeout()` 完成当前任务并启动新任务后才能看到 `.data` 的最终值。换句话说，当我们首次看到 `DataContainer` 的实例时，它尚未完全初始化。

## 13.2 解决方案：基于 Promise 的构造函数

如果我们延迟对 `DataContainer` 实例的访问，直到它完全初始化，会怎样？我们可以通过从构造函数返回一个 `Promise` 来实现这一点。默认情况下，构造函数返回该类的一个新实例。如果我们显式返回一个对象，则可以覆盖该行为：

```js
class DataContainer {
  #data;
  constructor() {
    return Promise.resolve('downloaded')
      .then(data => {
        this.#data = data;
        return this; // (A)
      });
  }
  getData() {
    return 'DATA: '+this.#data;
  }
}
new DataContainer()
  .then(dc => assert.equal( // (B)
    dc.getData(), 'DATA: downloaded'));
```

现在我们必须等待才能访问我们的实例（第 B 行）。它在数据“下载”完成后传递给我们（第 A 行）。这段代码中有两个可能的错误来源：

- 下载可能失败并产生拒绝。
- 第一个 `.then()` 回调的主体中可能抛出异常。

无论哪种情况，错误都会成为从构造函数返回的 `Promise` 的拒绝。

优点和缺点：

- 这种方法的一个好处是，我们只能在实例完全初始化后才能访问它。并且没有其他方法可以创建 `DataContainer` 的实例。
- 一个缺点是，构造函数返回 `Promise` 而不是实例可能会令人惊讶。

### 13.2.1 使用立即调用的异步箭头函数

我们可以使用[立即调用的异步箭头函数](https://exploringjs.com/impatient-js/ch_async-functions.html#immediately-invoked-async-arrow-functions)，而不是直接使用 `Promise` API 来创建从构造函数返回的 `Promise`：

```js
constructor() {
  return (async () => {
    this.#data = await Promise.resolve('downloaded');
    return this;
  })();
}
```

## 13.3 解决方案：静态工厂方法

类的*静态工厂方法* `C` 创建 `C` 的实例，是使用 `new C()` 的替代方案。JavaScript 中静态工厂方法的常见名称：

- `.create()`：创建一个新实例。示例：`Object.create()`
- `.from()`：基于不同的对象创建新实例，通过复制和/或转换。示例：`Array.from()`
- `.of()`：通过组合参数指定的值来创建新实例。示例：`Array.of()`

在以下示例中，`DataContainer.create()` 是一个静态工厂方法。它返回 `DataContainer` 实例的 `Promise`：

```js
class DataContainer {
  #data;
  static async create() {
    const data = await Promise.resolve('downloaded');
    return new this(data);
  }
  constructor(data) {
    this.#data = data;
  }
  getData() {
    return 'DATA: '+this.#data;
  }
}
DataContainer.create()
  .then(dc => assert.equal(
    dc.getData(), 'DATA: downloaded'));
```

这次，所有异步功能都包含在 `.create()` 中，这使得类的其余部分完全同步，因此更简单。

优点和缺点：

- 这种方法的一个好处是构造函数变得简单。
- 一个缺点是现在可以通过 `new DataContainer()` 创建设置不正确的实例。

### 13.3.1 改进：通过秘密令牌实现私有构造函数

如果我们希望确保实例始终正确设置，我们必须确保只有 `DataContainer.create()` 可以调用 `DataContainer` 的构造函数。我们可以通过秘密令牌来实现这一点：

```js
const secretToken = Symbol('secretToken');
class DataContainer {
  #data;
  static async create() {
    const data = await Promise.resolve('downloaded');
    return new this(secretToken, data);
  }
  constructor(token, data) {
    if (token !== secretToken) {
      throw new Error('Constructor is private');
    }
    this.#data = data;
  }
  getData() {
    return 'DATA: '+this.#data;
  }
}
DataContainer.create()
  .then(dc => assert.equal(
    dc.getData(), 'DATA: downloaded'));
```

如果 `secretToken` 和 `DataContainer` 位于同一模块中，并且只导出后者，那么外部方无法访问 `secretToken`，因此无法创建 `DataContainer` 的实例。

优点和缺点：



- 优点：安全且直接。
- 缺点：略显冗长。

### 13.3.2 改进：构造函数抛出异常，工厂方法借用类原型

我们解决方案的以下变体禁用了`DataContainer`的构造函数，并使用技巧以另一种方式创建其实例（第 A 行）：

```js
class DataContainer {
  static async create() {
    const data = await Promise.resolve('downloaded');
    return Object.create(this.prototype)._init(data); // (A)
  }
  constructor() {
    throw new Error('Constructor is private');
  }
  _init(data) {
    this._data = data;
    return this;
  }
  getData() {
    return 'DATA: '+this._data;
  }
}
DataContainer.create()
  .then(dc => {
    assert.equal(dc instanceof DataContainer, true); // (B)
    assert.equal(
      dc.getData(), 'DATA: downloaded');
  });
```

在内部，`DataContainer`的实例是其原型为`DataContainer.prototype`的任何对象。这就是为什么我们可以通过`Object.create()`（第 A 行）创建实例，以及为什么`instanceof`在第 B 行有效。

优点和缺点：

- 优点：优雅；`instanceof`有效。
- 缺点：
  - 并不能完全阻止创建实例。不过公平地说，通过`Object.create()`的变通方法也可以用于我们之前的解决方案。
  - 我们不能在`DataContainer`中使用[私有字段](https://2ality.com/2019/07/private-class-fields.html)和[私有方法](https://2ality.com/2019/07/private-methods-accessors-in-classes.html)，因为这些仅对通过构造函数创建的实例正确设置。

### 13.3.3 改进：实例默认不激活，通过工厂方法激活

另一种更冗长的变体是，默认情况下，实例通过标志`.#active`关闭。用于激活实例的初始化方法`.#init()`无法从外部访问，但`Data.container()`可以调用它：

```js
class DataContainer {
  #data;
  static async create() {
    const data = await Promise.resolve('downloaded');
    return new this().#init(data);
  }

  #active = false;
  constructor() {
  }
  #init(data) {
    this.#active = true;
    this.#data = data;
    return this;
  }
  getData() {
    this.#check();
    return 'DATA: '+this.#data;
  }
  #check() {
    if (!this.#active) {
      throw new Error('Not created by factory');
    }
  }
}
DataContainer.create()
  .then(dc => assert.equal(
    dc.getData(), 'DATA: downloaded'));
```

标志`.#active`通过私有方法`.#check()`强制执行，该方法必须在每个方法的开头调用。

此解决方案的主要缺点是冗长。此外，还存在在每个方法中忘记调用`.#check()`的风险。

### 13.3.4 变体：独立的工厂函数

为了完整性，我将展示另一种变体：除了使用静态方法作为工厂，你还可以使用一个独立的函数。

```js
const secretToken = Symbol('secretToken');
class DataContainer {
  #data;
  constructor(token, data) {
    if (token !== secretToken) {
      throw new Error('Constructor is private');
    }
    this.#data = data;
  }
  getData() {
    return 'DATA: '+this.#data;
  }
}

async function createDataContainer() {
  const data = await Promise.resolve('downloaded');
  return new DataContainer(secretToken, data);
}

createDataContainer()
  .then(dc => assert.equal(
    dc.getData(), 'DATA: downloaded'));
```

作为工厂的独立函数偶尔有用，但在这种情况下，我更喜欢静态方法：

- 独立函数无法访问`DataContainer`的私有成员。
- 我更喜欢`DataContainer.create()`的写法。

## 13.4 继承基于 Promise 的构造函数（可选）

一般来说，继承应谨慎使用。

使用独立的工厂函数，扩展`DataContainer`相对容易。

然而，继承基于 Promise 的构造函数会导致严重的限制。在下面的示例中，我们继承了`DataContainer`。子类`SubDataContainer`拥有自己的私有字段`.#moreData`，它通过挂钩到其超类构造函数返回的 Promise 来异步初始化该字段。

```js
class DataContainer {
  #data;
  constructor() {
    return Promise.resolve('downloaded')
      .then(data => {
        this.#data = data;
        return this; // (A)
      });
  }
  getData() {
    return 'DATA: '+this.#data;
  }
}

class SubDataContainer extends DataContainer {
  #moreData;
  constructor() {
    super();
    const promise = this;
    return promise
      .then(_this => {
        return Promise.resolve('more')
          .then(moreData => {
            _this.#moreData = moreData;
            return _this;
          });
      });
  }
  getData() {
    return super.getData() + ', ' + this.#moreData;
  }
}
```

遗憾的是，我们无法实例化这个类：

```js
assert.rejects(
  () => new SubDataContainer(),
  {
    name: 'TypeError',
    message: 'Cannot write private member #moreData ' +
      'to an object whose class did not declare it',
  }
);
```

为什么会失败？构造函数总是将其私有字段添加到其`this`上。然而，在这里，子构造函数中的`this`是超构造函数返回的 Promise（而不是通过 Promise 传递的`SubDataContainer`实例）。

但是，如果`SubDataContainer`没有任何私有字段，这种方法仍然有效。

## 13.5 结论

对于本章讨论的场景，我更喜欢基于 Promise 的构造函数，或者使用秘密令牌的静态工厂方法加私有构造函数。

然而，这里介绍的其他技术在其他场景中仍然有用。

## 13.6 延伸阅读

- 异步编程：
  - [《JavaScript 面向急躁的程序员》中的“用于异步编程的 Promise”一章](https://exploringjs.com/impatient-js/ch_promises.html)
  - [《JavaScript 面向急躁的程序员》中的“异步函数”一章](https://exploringjs.com/impatient-js/ch_async-functions.html)
  - [《JavaScript 面向急躁的程序员》中的“立即调用的异步箭头函数”一节](https://exploringjs.com/impatient-js/ch_async-functions.html#immediately-invoked-async-arrow-functions)
- 面向对象编程：
  - [《JavaScript 面向急躁的程序员》中的“原型链和类”一章](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html)
  - [博客文章“ES 提案：私有类字段”](https://2ality.com/2019/07/private-class-fields.html)
  - [博客文章“ES 提案：JavaScript 类中的私有方法和访问器”](https://2ality.com/2019/07/private-methods-accessors-in-classes.html)

# 14 复制类的实例：`.clone()`与复制构造函数

- 14.1 `.clone()`方法
- 14.2 静态工厂方法
- 14.3 致谢

在本章中，我们探讨两种实现类实例复制的方法：

- `.clone()`方法
- 所谓的复制构造函数，即接收当前类的另一个实例并用其初始化当前实例的构造函数。

## 14.1 `.clone()`方法

这种技术为每个需要复制实例的类引入一个`.clone()`方法。它返回`this`的深拷贝。以下示例展示了三个可克隆的类。

```js
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }
  clone() {
    return new Point(this.x, this.y);
  }
}
class Color {
  constructor(name) {
    this.name = name;
  }
  clone() {
    return new Color(this.name);
  }
}
class ColorPoint extends Point {
  constructor(x, y, color) {
    super(x, y);
    this.color = color;
  }
  clone() {
    return new ColorPoint(
      this.x, this.y, this.color.clone()); // (A)
  }
}
```

第 A 行展示了这种技术的一个重要方面：复合实例属性值也必须递归地克隆。

## 14.2 静态工厂方法

`copy constructor`（复制构造函数）是一种构造函数，它使用当前类的另一个实例来初始化当前实例。复制构造函数在 C++ 和 Java 等静态语言中很常见，在这些语言中，你可以通过`static overloading`（静态重载）提供多个版本的构造函数。这里的`static`意味着在编译时决定使用哪个版本。

在 JavaScript 中，我们必须在运行时做出这个决定，这会导致代码不够优雅：

```js
class Point {
  constructor(...args) {
    if (args[0] instanceof Point) {
      // 复制构造函数
      const [other] = args;
      this.x = other.x;
      this.y = other.y;
    } else {
      const [x, y] = args;
      this.x = x;
      this.y = y;
    }
  }
}
```

以下是使用这个类的方式：

```js
const original = new Point(-1, 4);
const copy = new Point(original);
assert.deepEqual(copy, original);
```

`Static factory methods`（静态工厂方法）是构造函数的替代方案，在这种情况下效果更好，因为我们可以直接调用所需的功能。（这里的`static`意味着这些工厂方法是类方法。）

在下面的例子中，三个类`Point`、`Color`和`ColorPoint`各自都有一个静态工厂方法`.from()`：

```js
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }
  static from(other) {
    return new Point(other.x, other.y);
  }
}
class Color {
  constructor(name) {
    this.name = name;
  }
  static from(other) {
    return new Color(other.name);
  }
}
class ColorPoint extends Point {
  constructor(x, y, color) {
    super(x, y);
    this.color = color;
  }
  static from(other) {
    return new ColorPoint(
      other.x, other.y, Color.from(other.color)); // (A)
  }
}
```

在第 A 行，我们再次递归地进行复制。

以下是`ColorPoint.from()`的工作方式：

```js
const original = new ColorPoint(-1, 4, new Color('red'));
const copy = ColorPoint.from(original);
assert.deepEqual(copy, original);
```

## 14.3 致谢

- [Ron Korvig](https://github.com/ronkorving) 提醒我在 JavaScript 中应使用静态工厂方法而非重载构造函数来进行深拷贝。

# 15 集合的不可变包装器

- 15.1 包装对象
  - 15.1.1 通过包装使集合不可变
- 15.2 `Map`的不可变包装器
- 15.3 `Array`的不可变包装器

集合的不可变包装器通过将集合包装在一个新对象中，使其变得不可变。在本章中，我们将探讨其工作原理以及为什么它很有用。

## 15.1 包装对象

如果有一个对象，我们希望减少其接口，可以采取以下方法：

- 创建一个新对象，将原始对象存储在私有字段中。这个新对象被称为“包装”了原始对象。新对象称为`wrapper`（包装器），原始对象称为`wrapped object`（被包装对象）。
- 包装器只将接收到的部分方法调用转发给被包装对象。

这就是包装的样子：



```js
class Wrapper {
  #wrapped;
  constructor(wrapped) {
    this.#wrapped = wrapped;
  }
  allowedMethod1(...args) {
    return this.#wrapped.allowedMethod1(...args);
  }
  allowedMethod2(...args) {
    return this.#wrapped.allowedMethod2(...args);
  }
}
```

相关的软件设计模式：

- 包装与[四人组设计模式 `Facade`（外观模式）](https://en.wikipedia.org/wiki/Facade_pattern)相关。
- 我们使用[`forwarding`（转发）](https://en.wikipedia.org/wiki/Forwarding_(object-oriented_programming))来实现[`delegation`（委托）](https://en.wikipedia.org/wiki/Delegation_pattern)。委托意味着一个对象让另一个对象（`delegate`，委托对象）处理其部分工作。它是继承的一种替代方案，用于共享代码。

### 15.1.1 通过包装使集合不可变

要使集合不可变，我们可以使用包装，并从其接口中移除所有破坏性操作。

这种技术的一个重要用例是：一个对象拥有内部可变数据结构，希望在不复制的情况下安全地导出它。导出是“实时的”也可能是一个目标。该对象可以通过包装内部数据结构并使其不可变来实现其目标。

接下来的两节展示了 `Map` 和 `Array` 的不可变包装器。它们都有以下限制：

- 它们是草图。需要更多工作才能使其适用于实际使用：更好的检查、支持更多方法等。
- 它们只进行浅层操作：每个包装器使被包装对象不可变，但不会使其返回的数据不可变。这可以通过包装方法返回的部分结果来修复。

## 15.2 Map 的不可变包装器

类 `ImmutableMapWrapper` 为 `Map` 生成包装器：

```js
class ImmutableMapWrapper {
  static _setUpPrototype() {
    // 只将非破坏性方法转发给被包装的 Map：
    for (const methodName of ['get', 'has', 'keys', 'size']) {
      ImmutableMapWrapper.prototype[methodName] = function (...args) {
        return this.#wrappedMapmethodName;
      }
    }
  }

  #wrappedMap;
  constructor(wrappedMap) {
    this.#wrappedMap = wrappedMap;
  }
}
ImmutableMapWrapper._setUpPrototype();
```

原型的设置必须通过静态方法执行，因为我们只能从类内部访问私有字段 `.#wrappedMap`。

以下是 `ImmutableMapWrapper` 的实际使用：

```js
const map = new Map([[false, 'no'], [true, 'yes']]);
const wrapped = new ImmutableMapWrapper(map);

// 非破坏性操作正常工作：
assert.equal(
  wrapped.get(true), 'yes');
assert.equal(
  wrapped.has(false), true);
assert.deepEqual(
  [...wrapped.keys()], [false, true]);

// 破坏性操作不可用：
assert.throws(
  () => wrapped.set(false, 'never!'),
  /^TypeError: wrapped.set is not a function$/);
assert.throws(
  () => wrapped.clear(),
  /^TypeError: wrapped.clear is not a function$/);
```

## 15.3 Array 的不可变包装器

对于数组 `arr`，普通的包装是不够的，因为我们不仅需要拦截方法调用，还需要拦截属性访问，例如 `arr[1] = true`。[JavaScript 代理](https://exploringjs.com/es6/ch_proxies.html)使我们能够做到这一点：

```js
const RE_INDEX_PROP_KEY = /^[0-9]+$/;
const ALLOWED_PROPERTIES = new Set([
  'length', 'constructor', 'slice', 'concat']);

function wrapArrayImmutably(arr) {
  const handler = {
    get(target, propKey, receiver) {
      // We assume that propKey is a string (not a symbol)
      if (RE_INDEX_PROP_KEY.test(propKey) // simplified check!
        || ALLOWED_PROPERTIES.has(propKey)) {
          return Reflect.get(target, propKey, receiver);
      }
      throw new TypeError(`Property "${propKey}" can’t be accessed`);
    },
    set(target, propKey, value, receiver) {
      throw new TypeError('Setting is not allowed');
    },
    deleteProperty(target, propKey) {
      throw new TypeError('Deleting is not allowed');
    },
  };
  return new Proxy(arr, handler);
}
```

让我们包装一个数组：

```js
const arr = ['a', 'b', 'c'];
const wrapped = wrapArrayImmutably(arr);

// 非破坏性操作是允许的：
assert.deepEqual(
  wrapped.slice(1), ['b', 'c']);
assert.equal(
  wrapped[1], 'b');

// 破坏性操作是不允许的：
assert.throws(
  () => wrapped[1] = 'x',
  /^TypeError: Setting is not allowed$/);
assert.throws(
  () => wrapped.shift(),
  /^TypeError: Property "shift" can’t be accessed$/);
```

# 16 正则表达式：通过示例理解环视断言

- 16.1 速查表：环视断言
- 16.2 本章注意事项
- 16.3 示例：指定匹配前后内容（正向环视）
- 16.4 示例：指定匹配前后不应出现的内容（负向环视）
  - 16.4.1 负向环视断言没有简单的替代方案
- 16.5 插曲：将环视断言指向内部
- 16.6 示例：匹配不以 `'abc'` 开头的字符串
- 16.7 示例：匹配不包含 `'.mjs'` 的子串
- 16.8 示例：跳过带注释的行
- 16.9 示例：智能引号
  - 16.9.1 支持通过反斜杠转义
- 16.10 致谢
- 16.11 延伸阅读

在本章中，我们通过示例来探索正则表达式中的环视断言。环视断言是非捕获性的，它必须匹配（或不匹配）输入字符串中当前位置之前（或之后）的内容。

## 16.1 速查表：环视断言

表 4：可用的环视断言概览。

| 模式 | 名称 |  |
| --- | --- | --- |
| `(?=«模式»)` | 正向先行断言 | ES3 |
| `(?!«模式»)` | 负向先行断言 | ES3 |
| `(?<=«模式»)` | 正向后行断言 | ES2018 |
| `(?<!«模式»)` | 负向后行断言 | ES2018 |

共有四种环视断言（表 4）：

- 先行断言（ECMAScript 3）：
  - 正向先行断言：`(?=«模式»)` 如果 `模式` 匹配输入字符串中当前位置之后的内容，则匹配成功。
  - 负向先行断言：`(?!«模式»)` 如果 `模式` 不匹配输入字符串中当前位置之后的内容，则匹配成功。
- 后行断言（ECMAScript 2018）：
  - 正向后行断言：`(?<=«模式»)` 如果 `模式` 匹配输入字符串中当前位置之前的内容，则匹配成功。
  - 负向后行断言：`(?<!«模式»)` 如果 `模式` 不匹配输入字符串中当前位置之前的内容，则匹配成功。

## 16.2 本章注意事项

- 示例展示了通过环视断言可以实现的功能。然而，正则表达式并非总是最佳解决方案。其他技术（如适当的解析）可能是更好的选择。
- 后行断言是一个相对较新的特性，可能并非所有目标 JavaScript 引擎都支持。
- 环视断言可能会对性能产生负面影响，尤其是当它们的模式匹配较长的字符串时。

## 16.3 示例：指定匹配前后内容（正向环视）

在以下交互中，我们提取被引号括起来的单词：

```js
> 'how "are" "you" doing'.match(/(?<=")[a-z]+(?=")/g)
[ 'are', 'you' ]
```

这里使用了两个环视断言：

- `(?<=")`：“前面必须有一个引号”
- `(?=")`：“后面必须有一个引号”

环视断言在 `/g` 模式下的 `.match()` 中特别方便，该方法返回整个匹配（捕获组 0）。环视断言模式匹配的内容不会被捕获。如果没有环视断言，引号会出现在结果中：

```js
> 'how "are" "you" doing'.match(/"([a-z]+)"/g)
[ '"are"', '"you"' ]
```

## 16.4 示例：指定匹配前后不应出现的内容（负向环视）

如何实现与上一节相反的效果，从字符串中提取所有未被引号括起来的单词？

- 输入：`'how "are" "you" doing'`
- 输出：`['how', 'doing']`

我们的第一次尝试是简单地将正向环视断言转换为负向环视断言。可惜，这失败了：

```js
> 'how "are" "you" doing'.match(/(?<!")[a-z]+(?!")/g)
[ 'how', 'r', 'o', 'doing' ]
```

问题在于我们提取的是不被引号括起来的字符序列。这意味着在字符串 `'"are"'` 中，中间的 “r” 被视为未加引号，因为它前面是 “a”，后面是 “e”。

我们可以通过规定前缀和后缀既不能是引号也不能是字母来解决这个问题：

```js
> 'how "are" "you" doing'.match(/(?<!["a-z])[a-z]+(?!["a-z])/g)
[ 'how', 'doing' ]
```

另一种解决方案是通过 `\b` 要求字符序列 `[a-z]+` 在单词边界处开始和结束：

```js
> 'how "are" "you" doing'.match(/(?<!")\b[a-z]+\b(?!")/g)
[ 'how', 'doing' ]
```

负向后行断言和负向先行断言的一个优点是它们也能在字符串的开头或结尾处工作——如示例所示。

### 16.4.1 负向环视断言没有简单的替代方案

负向环视断言是一个强大的工具，通常无法通过其他正则表达式手段来模拟。

如果我们不想使用它们，通常必须采用完全不同的方法。例如，在这种情况下，我们可以将字符串拆分为（带引号和不带引号的）单词，然后过滤它们：

```js
const str = 'how "are" "you" doing';

const allWords = str.match(/"?[a-z]+"?/g);
const unquotedWords = allWords.filter(
  w => !w.startsWith('"') || !w.endsWith('"'));
assert.deepEqual(unquotedWords, ['how', 'doing']);
```

这种方法的好处：

- 在较旧的引擎上也能工作。
- 易于理解。

## 16.5 插曲：将环视断言指向内部

到目前为止，我们看到的例子都有一个共同点：环视断言规定了匹配之前或之后必须出现什么，但不会将这些字符包含在匹配结果中。

本章剩余部分展示的正则表达式则不同：它们的环视断言指向内部，并限制匹配内容中的部分。

## 16.6 示例：匹配不以 `'abc'` 开头的字符串

假设我们要匹配所有不以 `'abc'` 开头的字符串。我们的第一次尝试可能是正则表达式 `/^(?!abc)/`。

这对于 `.test()` 来说效果很好：

```js
> /^(?!abc)/.test('xyz')
true
```

然而，`.exec()` 返回了一个空字符串：

```js
> /^(?!abc)/.exec('xyz')
{ 0: '', index: 0, input: 'xyz', groups: undefined }
```

问题在于，像环视这样的断言不会扩展匹配的文本。也就是说，它们不会捕获输入字符，它们只对输入中的当前位置提出要求。

因此，解决方案是添加一个能够捕获输入字符的模式：

```js
> /^(?!abc).*$/.exec('xyz')
{ 0: 'xyz', index: 0, input: 'xyz', groups: undefined }
```

正如所期望的，这个新的正则表达式拒绝了以 `'abc'` 开头的字符串：

```js
> /^(?!abc).*$/.exec('abc')
null
> /^(?!abc).*$/.exec('abcd')
null
```

并且它接受了没有完整前缀的字符串：

```js
> /^(?!abc).*$/.exec('ab')
{ 0: 'ab', index: 0, input: 'ab', groups: undefined }
```

## 16.7 示例：匹配不包含 `'.mjs'` 的子字符串

在下面的例子中，我们想要找到：

```text
import ··· from '«模块标识符»';
```

其中 `模块标识符` 不以 `'.mjs'` 结尾。

```js
const code = `
import {transform} from './util';
import {Person} from './person.mjs';
import {zip} from 'lodash';
`.trim();
assert.deepEqual(
  code.match(/^import .*? from '[^']+(?<!\.mjs)';$/umg),
  [
    "import {transform} from './util';",
    "import {zip} from 'lodash';",
  ]);
```

这里，后顾断言 `(?<!\.mjs)` 充当了一个*守卫*，阻止正则表达式匹配在该位置包含 `'.mjs'` 的字符串。

## 16.8 示例：跳过注释行

场景：我们想要解析带有设置的行，同时跳过注释。例如：



```js
const RE_SETTING = /^(?!#)([^:]*):(.*)$/

const lines = [
  'indent: 2', // 设置
  '# Trim trailing whitespace:', // 注释
  'whitespace: trim', // 设置
];

for (const line of lines) {
  const match = RE_SETTING.exec(line);
  if (match) {
    const key = JSON.stringify(match[1]);
    const value = JSON.stringify(match[2]);
    console.log(`KEY: ${key} VALUE: ${value}`);
  }
}

// 输出：
// 'KEY: "indent" VALUE: " 2"'
// 'KEY: "whitespace" VALUE: " trim"'
```

我们是如何得到正则表达式 `RE_SETTING` 的呢？

我们从以下用于设置的正则表达式开始：

```
/^([^:]*):(.*)$/
```

直观上，它由以下部分组成：

- 行首
- 非冒号字符（零个或多个）
- 一个冒号
- 任意字符（零个或多个）
- 行尾

这个正则表达式确实拒绝了*一些*注释：

```
> /^([^:]*):(.*)$/.test('# Comment')
false
```

但它接受了其他注释（那些包含冒号的）：

```
> /^([^:]*):(.*)$/.test('# Comment:')
true
```

我们可以通过在前面加上 `(?!#)` 作为守卫来解决这个问题。直观上，它的意思是：“输入字符串中的当前位置后面不能跟着字符 `#`。”

新的正则表达式按预期工作：

```
> /^(?!#)([^:]*):(.*)$/.test('# Comment:')
false
```

## 16.9 示例：智能引号

假设我们想要将成对的直双引号转换为弯引号：

- 输入：`` `"yes" and "no"` ``
- 输出：`` `“yes” and “no”` ``

这是我们的第一次尝试：

```
> `The words "must" and "should".`.replace(/"(.*)"/g, '“$1”')
'The words “must" and "should”.'
```

只有第一个引号和最后一个引号变成了弯引号。这里的问题是 `*` 量词是*贪婪*匹配（尽可能多）。

如果在 `*` 后面加上问号，它就会变成*懒惰*匹配：

```
> `The words "must" and "should".`.replace(/"(.*?)"/g, '“$1”')
'The words “must” and “should”.'
```

### 16.9.1 支持通过反斜杠转义

如果我们想要允许通过反斜杠转义引号呢？我们可以通过在引号前使用守卫 `(?<!\\)` 来实现：

```
> const regExp = /(?<!\\)"(.*?)(?<!\\)"/g;
> String.raw`\"straight\" and "curly"`.replace(regExp, '“$1”')
'\\"straight\\" and “curly”'
```

作为后处理步骤，我们仍然需要执行：

```
.replace(/\\"/g, `"`)
```

然而，这个正则表达式在遇到反斜杠转义的反斜杠时可能会失败：

```
> String.raw`Backslash: "\\"`.replace(/(?<!\\)"(.*?)(?<!\\)"/g, '“$1”')
'Backslash: "\\\\"'
```

第二个反斜杠阻止了引号变成弯引号。

如果我们让守卫更复杂一些，就可以解决这个问题（`?:` 使分组变为非捕获）：

```
(?<=^\\*)
```

新的守卫允许在引号前出现成对的反斜杠：

```
> const regExp = /(?<=^\\*)"(.*?)(?<=^\\*)"/g;
> String.raw`Backslash: "\\"`.replace(regExp, '“$1”')
'Backslash: “\\\\”'
```

还有一个问题。如果第一个引号出现在字符串的开头，这个守卫会阻止它被匹配：

```
> const regExp = /(?<=^\\*)"(.*?)(?<=^\\*)"/g;
> `"abc"`.replace(regExp, '“$1”')
'"abc"'
```

我们可以通过将第一个守卫改为 `(?<=^\\*|^)` 来解决这个问题：

```
> const regExp = /(?<=^\\*|^)"(.*?)(?<=^\\*)"/g;
> `"abc"`.replace(regExp, '“$1”')
'“abc”'
```

## 16.10 致谢

- 第一个处理引号前转义反斜杠的正则表达式[由 `@jonasraoni` 在 Twitter 上提出](https://twitter.com/jonasraoni/status/992506010454683650)。

## 16.11 延伸阅读

- [《JavaScript 快速入门》中的“正则表达式（`RegExp`）”章节](https://exploringjs.com/impatient-js/ch_regexps.html)

# 17 通过 `re-template-tag` 组合正则表达式

---

- 17.1 基础
- 17.2 功能概览
  - 17.2.1 主要功能
  - 17.2.2 细节与高级功能
- 17.3 这为什么有用？
- 17.4 `re` 与命名捕获组

---

我的小型库 [`re-template-tag`](https://github.com/rauschma/re-template-tag) 提供了一个用于组合正则表达式的模板标签函数。本章解释其工作原理。目的是介绍该库背后的思想（而不仅仅是库本身）。

## 17.1 基础

该库实现了用于正则表达式的模板标签 `re`。

安装：

```
npm install re-template-tag
```

导入：

```js
import {re} from 're-template-tag';
```

使用：以下两个表达式产生相同的正则表达式。

```js
assert.deepEqual(
  re`/abc/gu`,
  /abc/gu);
```

## 17.2 功能概览

[单元测试](https://github.com/rauschma/re-template-tag/blob/master/test/index_test.js) 是 `re-template-tag` 功能的一个很好的概览。

### 17.2.1 主要功能

你可以使用 `re` 从片段组装一个正则表达式：

```js
const RE_YEAR = /([0-9]{4})/;
const RE_MONTH = /([0-9]{2})/;
const RE_DAY = /([0-9]{2})/;
const RE_DATE = re`/^${RE_YEAR}-${RE_MONTH}-${RE_DAY}$/u`;
assert.equal(RE_DATE.source, '^([0-9]{4})-([0-9]{2})-([0-9]{2})$');
```

你插入的任何字符串都会被正确转义：

```js
assert.equal(re`/-${'.'}-/u`.source, '-\\.-');
```

无标志模式：

```js
const regexp = re`abc`;
assert.ok(regexp instanceof RegExp);
assert.equal(regexp.source, 'abc');
assert.equal(regexp.flags, '');
```

### 17.2.2 细节与高级特性

你可以像在正则表达式字面量内部一样使用反斜杠：

```js
assert.equal(re`/\./u`.source, '\\.');
```

正则表达式标志（如前面例子中的 `/u`）也可以动态计算：

```js
const regexp = re`/abc/${'g'+'u'}`;
assert.ok(regexp instanceof RegExp);
assert.equal(regexp.source, 'abc');
assert.equal(regexp.flags, 'gu');
```

## 17.3 这为什么有用？

- 你可以从片段组合正则表达式，并通过注释记录这些片段。这使得正则表达式更容易理解。
- 你可以为正则表达式片段定义常量并复用它们。
- 你可以通过字符串定义纯文本常量，将其插入正则表达式，并在必要时进行转义。

## 17.4 `re` 与命名捕获组

`re` 从[命名捕获组](https://exploringjs.com/impatient-js/ch_regexps.html#named-capture-groups)中获益，因为它使片段更加独立。

没有命名组时：

```js
const RE_YEAR = /([0-9]{4})/;
const RE_MONTH = /([0-9]{2})/;
const RE_DAY = /([0-9]{2})/;
const RE_DATE = re`/^${RE_YEAR}-${RE_MONTH}-${RE_DAY}$/u`;

const match = RE_DATE.exec('2017-01-27');
assert.equal(match[1], '2017');
```

使用命名组时：

```js
const RE_YEAR = re`(?<year>[0-9]{4})`;
const RE_MONTH = re`(?<month>[0-9]{2})`;
const RE_DAY = re`(?<day>[0-9]{2})`;
const RE_DATE = re`/${RE_YEAR}-${RE_MONTH}-${RE_DAY}/u`;

const match = RE_DATE.exec('2017-01-27');
assert.equal(match.groups.year, '2017');
```

# 18 通过实现 Promise 来探索 Promise

---

- 18.1 回顾：Promise 的状态
- 18.2 版本 1：独立 Promise
  - 18.2.1 方法 `.then()`
  - 18.2.2 方法 `.resolve()`
- 18.3 版本 2：链式调用 `.then()`
- 18.4 便捷方法 `.catch()`
- 18.5 省略反应
- 18.6 实现
- 18.7 版本 3：扁平化从 `.then()` 回调返回的 Promise
  - 18.7.1 从 `.then()` 的回调中返回 Promise
  - 18.7.2 扁平化使 Promise 状态更复杂
  - 18.7.3 实现 Promise 扁平化
- 18.8 版本 4：反应回调中抛出的异常
- 18.9 版本 5：揭示构造函数模式

---

![](img/file1.svg) **必备知识：Promise**

阅读本章前，你应对 Promise 有大致了解，但许多相关知识也会在此回顾。如有需要，你可以阅读[《JavaScript 给不耐烦的程序员》中关于 Promise 的章节](https://exploringjs.com/impatient-js/ch_promises.html)。

在本章中，我们将从另一个角度探讨 Promise：不是使用这个 API，而是创建一个简单的实现。这个不同的角度曾极大地帮助我理解 Promise。

这个 Promise 实现是 `ToyPromise` 类。为了更容易理解，它并未完全匹配 API，但已经足够接近，能让我们深入了解 Promise 的工作原理。

![](img/file1.svg) **代码仓库**

`ToyPromise` 可在 GitHub 仓库 [`toy-promise`](https://github.com/rauschma/toy-promise) 中找到。

## 18.1 回顾：Promise 的状态

![](img/file9.svg)

图 2：Promise 的状态（简化版）：Promise 初始为待定。如果兑现它，则变为已兑现。如果拒绝它，则变为已拒绝。

我们从 Promise 状态如何工作的简化版本开始（图 2）：

- Promise 初始为*待定*（pending）。
- 如果 Promise 被*兑现*（resolved）为一个值 `v`，则变为*已兑现*（fulfilled）（稍后我们会看到兑现也可能导致拒绝）。`v` 现在是 Promise 的*兑现值*。
- 如果 Promise 被*拒绝*（rejected）为一个错误 `e`，则变为*已拒绝*（rejected）。`e` 现在是 Promise 的*拒绝值*。

## 18.2 版本 1：独立 Promise

我们的第一个实现是一个功能最简的独立 Promise：

- 我们可以创建一个 Promise。
- 我们可以兑现或拒绝一个 Promise，并且只能执行一次。
- 我们可以通过 `.then()` 注册*反应*（回调）。无论 Promise 是否已被敲定，注册都必须正确工作。
- `.then()` 目前不支持链式调用——它不返回任何内容。

`ToyPromise1` 是一个具有三个原型方法的类：

- `ToyPromise1.prototype.resolve(value)`
- `ToyPromise1.prototype.reject(reason)`
- `ToyPromise1.prototype.then(onFulfilled, onRejected)`

也就是说，`resolve` 和 `reject` 是方法（而不是传递给构造函数回调参数的函数）。

以下是第一个实现的使用方式：

```js
// .resolve() 在 .then() 之前
const tp1 = new ToyPromise1();
tp1.resolve('abc');
tp1.then((value) => {
  assert.equal(value, 'abc');
});
```

```js
// .then() 在 .resolve() 之前
const tp2 = new ToyPromise1();
tp2.then((value) => {
  assert.equal(value, 'def');
});
tp2.resolve('def');
```

图 3 说明了我们的第一个 `ToyPromise` 是如何工作的。

![](img/file0.svg) **Promise 数据流图是可选的**

这些图的目的是提供一种可视化解释来说明 Promise 的工作原理。但它们是可选的。如果你觉得它们令人困惑，可以忽略它们，专注于代码。

![](img/file10.svg)

图 3：`ToyPromise1`：如果 Promise 被兑现，提供的值会传递给*兑现反应*（`.then()` 的第一个参数）。如果 Promise 被拒绝，提供的值会传递给*拒绝反应*（`.then()` 的第二个参数）。

### 18.2.1 方法 `.then()`

我们先来看 `.then()`。它需要处理两种情况：

- 如果 Promise 仍处于待定状态，它会将 `onFulfilled` 和 `onRejected` 的调用排队。这些调用将在 Promise 被敲定后使用。
- 如果 Promise 已经已兑现或已拒绝，则可以立即调用 `onFulfilled` 或 `onRejected`。



```javascript
then(onFulfilled, onRejected) {
  const fulfillmentTask = () => {
    if (typeof onFulfilled === 'function') {
      onFulfilled(this._promiseResult);
    }
  };
  const rejectionTask = () => {
    if (typeof onRejected === 'function') {
      onRejected(this._promiseResult);
    }
  };
  switch (this._promiseState) {
    case 'pending':
      this._fulfillmentTasks.push(fulfillmentTask);
      this._rejectionTasks.push(rejectionTask);
      break;
    case 'fulfilled':
      addToTaskQueue(fulfillmentTask);
      break;
    case 'rejected':
      addToTaskQueue(rejectionTask);
      break;
    default:
      throw new Error();
  }
}
```

前面的代码片段使用了以下辅助函数：

```javascript
function addToTaskQueue(task) {
  setTimeout(task, 0);
}
```

Promise 必须始终异步地解决。这就是为什么我们不直接执行任务，而是将它们添加到事件循环（浏览器、Node.js 等）的任务队列中。请注意，真正的 Promise API 并不使用普通任务（如`setTimeout()`），而是使用[微任务](https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/)，它们与当前普通任务紧密耦合，并始终在其之后立即执行。

### 18.2.2 方法`.resolve()`

`.resolve()`的工作方式如下：如果 Promise 已经解决，则不做任何操作（确保 Promise 只能被解决一次）。否则，Promise 的状态变为`'fulfilled'`，并将结果缓存到`this.promiseResult`中。接着，所有已入队的完成反应都会被调用。

```javascript
resolve(value) {
  if (this._promiseState !== 'pending') return this;
  this._promiseState = 'fulfilled';
  this._promiseResult = value;
  this._clearAndEnqueueTasks(this._fulfillmentTasks);
  return this; // enable chaining
}
```

```javascript
_clearAndEnqueueTasks(tasks) {
  this._fulfillmentTasks = undefined;
  this._rejectionTasks = undefined;
  tasks.map(addToTaskQueue);
}
```

`reject()`与`resolve()`类似。

## 18.3 版本 2：链式调用`.then()`

![](img/file11.svg)

图 4：`ToyPromise2`链式调用`.then()`：`.then()`现在返回一个 Promise，该 Promise 由完成反应或拒绝反应返回的任何值来解析。

我们接下来实现的功能是链式调用（图 4）：从完成反应或拒绝反应返回的值可以被后续`.then()`调用中的完成反应处理。（在下一个版本中，由于对返回 Promise 的特殊支持，链式调用将变得更加有用。）

在以下示例中：

- 第一个`.then()`：我们在完成反应中返回一个值。
- 第二个`.then()`：我们通过完成反应接收该值。

```javascript
new ToyPromise2()
  .resolve('result1')
  .then(x => {
    assert.equal(x, 'result1');
    return 'result2';
  })
  .then(x => {
    assert.equal(x, 'result2');
  });
```

在以下示例中：

- 第一个`.then()`：我们在拒绝反应中返回一个值。
- 第二个`.then()`：我们通过完成反应接收该值。

```javascript
new ToyPromise2()
  .reject('error1')
  .then(null,
    x => {
      assert.equal(x, 'error1');
      return 'result2';
    })
  .then(x => {
    assert.equal(x, 'result2');
  });
```

## 18.4 便捷方法`.catch()`

新版本引入了一个便捷方法`.catch()`，使得仅提供拒绝反应更加容易。注意，仅提供完成反应已经很容易——我们只需省略`.then()`的第二个参数（参见前面的示例）。

如果使用它（第 A 行），前面的示例看起来更简洁：

```javascript
new ToyPromise2()
  .reject('error1')
  .catch(x => { // (A)
    assert.equal(x, 'error1');
    return 'result2';
  })
  .then(x => {
    assert.equal(x, 'result2');
  });
```

以下两个方法调用是等价的：

```javascript
.catch(rejectionReaction)
.then(null, rejectionReaction)
```

这是`.catch()`的实现方式：

```javascript
catch(onRejected) { // [new]
  return this.then(null, onRejected);
}
```

## 18.5 省略反应

新版本还支持：如果我们省略完成反应，则传递完成；如果我们省略拒绝反应，则传递拒绝。为什么这很有用？

以下示例演示了传递拒绝：

```javascript
someAsyncFunction()
  .then(fulfillmentReaction1)
  .then(fulfillmentReaction2)
  .catch(rejectionReaction);
```

现在`rejectionReaction`可以处理`someAsyncFunction()`、`fulfillmentReaction1`和`fulfillmentReaction2`的拒绝。

以下示例演示了传递完成：

```javascript
someAsyncFunction()
  .catch(rejectionReaction)
  .then(fulfillmentReaction);
```

如果`someAsyncFunction()`拒绝了它的 Promise，`rejectionReaction`可以修复任何问题并返回一个完成值，然后由`fulfillmentReaction`处理。

如果`someAsyncFunction()`完成了它的 Promise，`fulfillmentReaction`也可以处理它，因为`.catch()`被跳过了。

## 18.6 实现

这一切在底层是如何处理的？

- `.then()`返回一个 Promise，该 Promise 由`onFulfilled`或`onRejected`返回的值来解析。
- 如果缺少`onFulfilled`或`onRejected`，则它们本应接收的值会被传递给`.then()`返回的 Promise。

只有`.then()`发生了变化：

```javascript
then(onFulfilled, onRejected) {
  const resultPromise = new ToyPromise2(); // [new]

  const fulfillmentTask = () => {
    if (typeof onFulfilled === 'function') {
      const returned = onFulfilled(this._promiseResult);
      resultPromise.resolve(returned); // [new]
    } else { // [new]
      // `onFulfilled` is missing
      // => we must pass on the fulfillment value
      resultPromise.resolve(this._promiseResult);
    } 
  };

  const rejectionTask = () => {
    if (typeof onRejected === 'function') {
      const returned = onRejected(this._promiseResult);
      resultPromise.resolve(returned); // [new]
    } else { // [new]
      // `onRejected` is missing
      // => we must pass on the rejection value
      resultPromise.reject(this._promiseResult);
    }
  };

  ···

  return resultPromise; // [new]
}
```

`.then()`创建并返回一个新的 Promise（方法的第一行和最后一行）。此外：

- `fulfillmentTask`的工作方式不同。完成之后现在发生的情况如下：
  - 如果提供了`onFulfilled`，则调用它，并使用其结果来解析`resultPromise`。
  - 如果缺少`onFulfilled`，则使用当前 Promise 的完成值来解析`resultPromise`。
- `rejectionTask`的工作方式不同。以下是拒绝发生后现在的情况：
  - 如果提供了`onRejected`，则会调用它，并使用其结果来解决`resultPromise`。请注意，`resultPromise`不会被拒绝：我们假设`onRejected()`修复了存在的任何问题。
  - 如果缺少`onRejected`，则使用当前 Promise 的拒绝值来拒绝`resultPromise`。

## 18.7 版本 3：扁平化从`.then()`回调返回的 Promise

### 18.7.1 从`.then()`的回调中返回 Promise

Promise 扁平化主要是为了让链式调用更方便：如果我们想将一个值从一个`.then()`回调传递到下一个，我们就在前一个回调中返回它。之后，`.then()`会将其放入它已经返回的 Promise 中。

如果从`.then()`回调中返回一个 Promise，这种方法就会变得不方便。例如，基于 Promise 的函数的结果（第 A 行）：

```javascript
asyncFunc1()
.then((result1) => {
  assert.equal(result1, 'Result of asyncFunc1()');
  return asyncFunc2(); // (A)
})
.then((result2Promise) => {
  result2Promise
  .then((result2) => { // (B)
    assert.equal(
      result2, 'Result of asyncFunc2()');
  });
});
```

这次，将第 A 行返回的值放入`.then()`返回的 Promise 中，迫使我们在第 B 行解包该 Promise。如果第 A 行返回的 Promise 能够替换`.then()`返回的 Promise，那就更好了。具体如何实现尚不明确，但如果可行，我们就可以这样编写代码：

```javascript
asyncFunc1()
.then((result1) => {
  assert.equal(result1, 'Result of asyncFunc1()');
  return asyncFunc2(); // (A)
})
.then((result2) => {
  // result2 是兑现值，而不是 Promise
  assert.equal(
    result2, 'Result of asyncFunc2()');
});
```

在第 A 行，我们返回了一个 Promise。得益于 Promise 扁平化，`result2`是该 Promise 的兑现值，而不是 Promise 本身。

### 18.7.2 扁平化使 Promise 状态更复杂

![](img/file5.svg)

**ECMAScript 规范中的 Promise 扁平化**

在 ECMAScript 规范中，Promise 扁平化的细节在[“Promise 对象”部分](https://tc39.es/ecma262/#sec-promise-objects)中描述。

Promise API 如何处理扁平化？

如果一个 Promise P 被一个 Promise Q 解决，那么 P 不会包装 Q，而是 P“变成”Q：P 的状态和解决值现在始终与 Q 相同。这对`.then()`有帮助，因为`.then()`用其某个回调返回的值来解决它返回的 Promise。

P 如何变成 Q？通过锁定 Q：P 变得外部不可解决，并且 Q 的解决会触发 P 的解决。锁定是一种额外的不可见 Promise 状态，使状态更加复杂。

Promise API 还有一个额外特性：Q 不必是一个 Promise，只需是一个所谓的`thenable`。thenable 是一个具有`.then()`方法的对象。这种额外灵活性的目的是让不同的 Promise 实现能够协同工作（这在 Promise 首次添加到语言中时很重要）。

图 5 可视化了新状态。

![](img/file12.svg)

图 5：Promise 的所有状态：Promise 扁平化引入了不可见的伪状态“locked-in”。如果 Promise P 被一个 thenable Q 解决，则达到该状态。之后，P 的状态和解决值始终与 Q 相同。

请注意，解决的概念也变得更加复杂。现在，解决一个 Promise 仅意味着它不能再被直接解决：

- 解决可能会拒绝一个 Promise：我们可以用一个被拒绝的 Promise 来解决一个 Promise。
- 解决甚至可能不会解决一个 Promise：我们可以用一个始终处于待定状态的 Promise 来解决一个 Promise。

ECMAScript 规范是这样表述的：“未解决的 Promise 始终处于待定状态。已解决的 Promise 可能处于待定、兑现或拒绝状态。”

### 18.7.3 实现 Promise 扁平化

图 6 展示了`ToyPromise3`如何处理扁平化。

![](img/file13.svg)

图 6：`ToyPromise3`扁平化已解决的 Promise：如果第一个 Promise 被一个 thenable `x1`解决，它会锁定`x1`，并用`x1`的解决值来结算。如果第一个 Promise 被一个非 thenable 的值解决，则一切照旧。

我们通过以下函数检测 thenable：

```javascript
function isThenable(value) { // [new]
  return typeof value === 'object' && value !== null
    && typeof value.then === 'function';
}
```

为了实现锁定，我们引入了一个新的布尔标志`._alreadyResolved`。将其设置为`true`会停用`.resolve()`和`.reject()`——例如：

```javascript
resolve(value) { // [new]
  if (this._alreadyResolved) return this;
  this._alreadyResolved = true;

  if (isThenable(value)) {
    // 将 `value` 的兑现和拒绝转发给 `this`。
    // 回调始终异步执行
    value.then(
      (result) => this._doFulfill(result),
      (error) => this._doReject(error));
  } else {
    this._doFulfill(value);
  }

  return this; // 启用链式调用
}
```

如果`value`是一个 thenable，那么我们将当前 Promise 锁定在它上面：

- 如果`value`被一个结果兑现，当前 Promise 也会被该结果兑现。
- 如果`value`被一个错误拒绝，当前 Promise 也会被该错误拒绝。

结算通过私有方法`._doFulfill()`和`._doReject()`执行，以绕过`._alreadyResolved`的保护。

`._doFulfill()`相对简单：



```
_doFulfill(value) { // [new]
  assert.ok(!isThenable(value));
  this._promiseState = 'fulfilled';
  this._promiseResult = value;
  this._clearAndEnqueueTasks(this._fulfillmentTasks);
}
```

此处未展示 `.reject()`。它唯一的新功能是现在也遵守 `._alreadyResolved`。

## 18.8 版本 4：反应回调中抛出的异常

![](img/file14.svg)

图 7：`ToyPromise4` 将 Promise 反应中的异常转换为 `.then()` 返回的 Promise 的拒绝。

作为我们的最后一个特性，我们希望 Promise 能够将用户代码中的异常作为拒绝处理（图 7）。在本章中，“用户代码”指的是 `.then()` 的两个回调参数。

```
new ToyPromise4()
  .resolve('a')
  .then((value) => {
    assert.equal(value, 'a');
    throw 'b'; // 触发拒绝
  })
  .catch((error) => {
    assert.equal(error, 'b');
  })
```

现在，`.then()` 通过辅助方法 `._runReactionSafely()` 安全地运行 Promise 反应 `onFulfilled` 和 `onRejected`——例如：

```
const fulfillmentTask = () => {
  if (typeof onFulfilled === 'function') {
    this._runReactionSafely(resultPromise, onFulfilled); // [new]
  } else {
    // `onFulfilled` 缺失
    // => 我们必须传递兑现值
    resultPromise.resolve(this._promiseResult);
  } 
};
```

`._runReactionSafely()` 的实现如下：

```
_runReactionSafely(resultPromise, reaction) { // [新增]
  try {
    const returned = reaction(this._promiseResult);
    resultPromise.resolve(returned);
  } catch (e) {
    resultPromise.reject(e);
  }
}
```

## 18.9 版本 5：揭示构造器模式

我们还差最后一步：如果想把 `ToyPromise` 变成真正的 `Promise` 实现，还需要实现[揭示构造器模式](https://blog.domenic.me/the-revealing-constructor-pattern/)：JavaScript 的 Promise 不是通过方法来解决或拒绝的，而是通过传递给 *executor*（构造函数的回调参数）的函数来完成的。

```
const promise = new Promise(
  (resolve, reject) => { // executor
    // ···
  });
```

如果 executor 抛出异常，则 `promise` 被拒绝。

# 19 函数的 `.name` 属性

* * *

*   19.1 函数的名称
    *   19.1.1 函数名称用于堆栈跟踪
*   19.2 为函数提供名称的构造
    *   19.2.1 函数声明
    *   19.2.2 变量声明与匿名函数
    *   19.2.3 赋值与匿名函数
    *   19.2.4 默认值与匿名函数
    *   19.2.5 具名函数表达式
    *   19.2.6 对象字面量中的方法
    *   19.2.7 类定义中的方法
    *   19.2.8 类的名称
    *   19.2.9 默认导出与匿名构造
    *   19.2.10 其他编程构造
*   19.3 函数名称的注意事项
    *   19.3.1 函数名称总是在创建时赋值
    *   19.3.2 警告：代码压缩
*   19.4 修改函数名称
*   19.5 ECMAScript 规范中的函数属性 `.name`

* * *

在本章中，我们将探讨函数的名称：

*   所有函数都有 `.name` 属性
*   该属性对调试（其值会出现在堆栈跟踪中）以及某些元编程任务（按名称选取函数等）很有用。

## 19.1 函数的名称

函数的 `.name` 属性包含函数的名称：

```
function myBeautifulFunction() {}
assert.equal(myBeautifulFunction.name, 'myBeautifulFunction');
```

在 ECMAScript 6 之前，大多数引擎已经支持该属性。随着 ES6 的发布，它成为了语言标准的一部分。

语言在给函数命名方面变得出奇地擅长，即使它们最初是匿名的（例如箭头函数）。

### 19.1.1 函数名称用于堆栈跟踪

函数名称的一个好处是它们会出现在堆栈跟踪中。在下面的示例中，`callFunc()` 的参数没有名称，因此堆栈跟踪的第二行没有函数名称。

```
function callFunc(func) {
  return func();
}

function func1() {
  throw new Error('Problem');
}

function func2() {
  // 下面的箭头函数没有名称
  callFunc(() => func1());
}

function func3() {
  func2();
}

try {
  func3();
} catch (err) {
assert.equal(err.stack, `
Error: Problem
 at func1 (ch_function-names.mjs:6:9)
 at ch_function-names.mjs:11:18
 at callFunc (ch_function-names.mjs:2:10)
 at func2 (ch_function-names.mjs:11:3)
 at func3 (ch_function-names.mjs:15:3)
 at ch_function-names.mjs:19:3
`.trim());

}
```

## 19.2 为函数提供名称的构造

以下各节描述了各种编程构造如何自动设置 `.name`。

### 19.2.1 函数声明

函数声明长期以来一直拥有 `.name`——例如：

```
function funcDecl() {}
assert.equal(funcDecl.name, 'funcDecl');
```

### 19.2.2 变量声明与匿名函数

由匿名函数表达式创建的函数，如果它是变量声明的初始化值，则会获得一个名称：

```
let letFunc = function () {};
assert.equal(letFunc.name, 'letFunc');

const constFunc = function () {};
assert.equal(constFunc.name, 'constFunc');

var varFunc = function () {};
assert.equal(varFunc.name, 'varFunc');
```

![](img/file0.svg) **箭头函数也会获得名称**

在名称方面，箭头函数与匿名函数表达式类似：

```
const arrowFunc = () => {};
assert.equal(arrowFunc.name, 'arrowFunc');
```

从现在开始，每当你看到匿名函数表达式时，可以假设箭头函数的工作方式相同。

### 19.2.3 赋值与匿名函数

即使是普通的赋值，`.name` 也会被正确设置：

```
let assignedFunc;
assignedFunc = function () {};
assert.equal(assignedFunc.name, 'assignedFunc');
```

### 19.2.4 默认值与匿名函数

如果函数是默认值，它会从其变量或参数中获取名称：

```
const [arrayDestructured = function () {}] = [];
assert.equal(arrayDestructured.name, 'arrayDestructured');

const {prop: objectDestructured = function () {}} = {};
assert.equal(objectDestructured.name, 'objectDestructured');

function createParamDefault(paramDefault = function () {}) {
  return paramDefault;
}
assert.equal(createParamDefault().name, 'paramDefault');
```

### 19.2.5 具名函数表达式

具名函数表达式的名称用于设置 `.name` 属性：

```
const varName = function funcName() {};
assert.equal(varName.name, 'funcName');
```

因为函数表达式的名称 `funcName` 优先于其他名称（本例中为变量名 `varName`）。然而，函数表达式的名称仍然只是函数表达式内部的变量：

```
const varName = function funcName() {
  assert.equal(funcName.name, 'funcName');
};
varName();
assert.throws(
  () => funcName,
  /^ReferenceError: funcName is not defined$/
);
```

### 19.2.6 对象字面量中的方法

如果函数是属性的值，它会从该属性获取名称。无论这是通过方法定义（第 A 行）、传统属性定义（第 B 行）、带计算属性键的属性定义（第 C 行）还是属性值简写（第 D 行）实现的，都没有关系。

```
function shortHand() {}

const obj = {
  methodDef() {}, // (A)
  propDef: function () {}, // (B)
  ['computed' + 'Key']: function () {}, // (C)
  shortHand, // (D)
};

assert.equal(obj.methodDef.name, 'methodDef');
assert.equal(obj.propDef.name, 'propDef');
assert.equal(obj.computedKey.name, 'computedKey');
assert.equal(obj.shortHand.name, 'shortHand');
```

getter 的名称以 `'get'` 为前缀，setter 的名称以 `'set'` 为前缀：

```
const obj = {
  get myGetter() {},
  set mySetter(value) {},
};
const getter = Object.getOwnPropertyDescriptor(obj, 'myGetter').get;
assert.equal(getter.name, 'get myGetter');

const setter = Object.getOwnPropertyDescriptor(obj, 'mySetter').set;
assert.equal(setter.name, 'set mySetter');
```

### 19.2.7 类定义中的方法

类定义中方法的命名与对象字面量类似。例如，下面是一个类声明（命名在类表达式中同样适用）：

```
class ClassDecl {
  methodDef() {}
  ['computed' + 'Key']() {} // 计算属性键

  static staticMethod() {}
}
assert.equal(ClassDecl.prototype.methodDef.name, 'methodDef');
assert.equal(new ClassDecl().methodDef.name, 'methodDef');

assert.equal(ClassDecl.prototype.computedKey.name, 'computedKey');

assert.equal(ClassDecl.staticMethod.name, 'staticMethod');
```

getter 和 setter 同样分别带有名称前缀 `'get'` 和 `'set'`：

```
class ClassDecl {
  get myGetter() {}
  set mySetter(value) {}
}
const getter = Object.getOwnPropertyDescriptor(
  ClassDecl.prototype, 'myGetter').get;
assert.equal(getter.name, 'get myGetter');

const setter = Object.getOwnPropertyDescriptor(
  ClassDecl.prototype, 'mySetter').set;
assert.equal(setter.name, 'set mySetter');
```

#### 19.2.7.1 键为符号的方法

方法的键可以是符号。此类方法的 `.name` 属性仍然是字符串：

*   如果符号有描述，则方法名是方括号中的描述。
*   否则，方法名是空字符串（`''`）。

```
const keyWithDesc = Symbol('keyWithDesc');
const keyWithoutDesc = Symbol();

const obj = {
  [keyWithDesc]() {},
  [keyWithoutDesc]() {},
};
assert.equal(obj[keyWithDesc].name, '[keyWithDesc]');
assert.equal(obj[keyWithoutDesc].name, '');
```

### 19.2.8 类的名称

在底层，类就是函数。此类函数的 `.name` 属性也会被正确设置：

```
class ClassDecl {}
assert.equal(ClassDecl.name, 'ClassDecl');

const AnonClassExpr = class {};
assert.equal(AnonClassExpr.name, 'AnonClassExpr');

const NamedClassExpr = class ClassName {};
assert.equal(NamedClassExpr.name, 'ClassName');
```

### 19.2.9 默认导出与匿名构造

以下所有语句都将 `.name` 设置为 `'default'`：

```
// 匿名函数表达式
export default function () {}
export default (function () {});

// 匿名类表达式
export default class {}
export default (class {});

// 箭头函数
export default () => {};
```

### 19.2.10 其他编程构造

*   生成器函数和生成器方法的命名方式与普通函数和方法相同。它们的名称中不包含星号：

    ```
    function* genFuncDecl() {}
    assert.equal(genFuncDecl.name, 'genFuncDecl');
    ```

*   `new Function()` 生成的函数，其 `.name` 为 `'anonymous'`。[一个 WebKit 错误](https://bugs.webkit.org/show_bug.cgi?id=7726) 描述了为什么这在 Web 上是必要的。

    ```
    assert.equal(new Function().name, 'anonymous');
    ```

*   `func.bind()` 生成的函数，其 `.name` 为 `'bound '+func.name`：

    ```
    function func(x) {
      return x
    }
    const bound = func.bind(undefined, 123);
    assert.equal(bound.name, 'bound func');
    ```

## 19.3 函数名称需要注意的事项

### 19.3.1 函数的名称总是在创建时赋值

只有在创建函数时使用了前面提到的模式之一，函数才会获得名称。之后使用这些模式不会改变任何内容——例如：

```
function functionFactory() {
  return function () {}; // (A)
}
const func = functionFactory(); // (B)
assert.equal(func.name, ''); // 匿名
```



函数`func`在第 A 行创建，同时它获得了非名称，即空字符串`''`。在第 B 行使用赋值不会更新初始名称。缺失的函数名称理论上可以在之后更新，但这样做会对性能产生负面影响。

### 19.3.2 警告：代码压缩

函数名称会受到代码压缩的影响，这意味着在压缩后的代码中它们通常会发生变化。根据我们的需求，我们可能需要通过字符串（不会被压缩）来管理函数名称，或者告诉压缩器哪些名称不要压缩。

## 19.4 更改函数的名称

![](img/file0.svg) **关于属性特性的更多信息**

`Object.getOwnPropertyDescriptor()`和`Object.defineProperty()`用于处理属性特性。有关这些特性的更多信息，请参见 §9“属性特性：入门”。

以下是属性`.name`的特性：

```
const func = function () {};
assert.deepEqual(
  Object.getOwnPropertyDescriptor(func, 'name'),
  {
    value: 'func',
    writable: false,
    enumerable: false,
    configurable: true,
  });
```

该属性不可写，意味着我们无法通过赋值来更改其值：

```
assert.throws(
  () => func.name = 'differentName',
  /^TypeError: Cannot assign to read only property 'name'/
);
```

然而，该属性是可配置的，这意味着我们可以通过重新定义来更改它：

```
Object.defineProperty(
  func, 'name', {
    value: 'differentName',
  });
assert.equal(func.name, 'differentName');
```

## 19.5 ECMAScript 规范中的函数属性`.name`

* 规范操作[`SetFunctionName()`](https://tc39.es/ecma262/#sec-setfunctionname)用于设置属性`.name`。在规范中搜索该名称，可以找到它发生的位置。第三个参数指定了名称前缀：
  * [getter 和 setter](https://tc39.es/ecma262/#sec-method-definitions-runtime-semantics-propertydefinitionevaluation)的前缀为`'get'`和`'set'`。
  * [`Function.prototype.bind()`](https://tc39.es/ecma262/#sec-function.prototype.bind)的前缀为`'bound'`。

* 匿名函数表达式最初没有`.name`属性，这一点可以通过查看规范中函数的创建方式来了解。

* 命名函数表达式的名称通过`SetFunctionName()`设置。在[创建匿名函数表达式](https://tc39.es/ecma262/#sec-function-definitions-runtime-semantics-evaluation)时不会调用该操作。

* 函数声明的名称在进入作用域时（早期激活）在[其他地方](https://tc39.es/ecma262/#sec-function-definitions-runtime-semantics-instantiatefunctionobject)设置。

* 此外，规范[明确说明](https://tc39.es/ecma262/#sec-function-instances-name)：“本规范未为其关联上下文名称的匿名函数对象没有`"name"`自有属性，但继承`%Function.prototype%`的`"name"`属性。”

* [创建箭头函数时](https://tc39.es/ecma262/#sec-arrow-function-definitions-runtime-semantics-evaluation)，也不会设置名称（不调用`SetFunctionName()`）。

大多数 JavaScript 引擎与规范存在差异，它们确实为匿名函数创建了自有属性`.name`：

```
> Reflect.ownKeys(() => {})
[ 'length', 'name' ]
```
