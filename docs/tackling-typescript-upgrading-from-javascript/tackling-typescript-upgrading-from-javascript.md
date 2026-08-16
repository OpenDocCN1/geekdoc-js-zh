# 攻克 TypeScript：从 JavaScript 升级






![](img/121df7a1ce018f05a1fa34e5d6e7a680_0_0.png)



















16.6 接口的其它特性 . . . . . . . . . . . . . . . . . . . . 133












- 22 类型断言（与类型转换相关）. . . . . . . . . . 189
22.1 类型断言 . . . . . . . . . . . . . . . . . . . . 189
22.2 与类型断言相关的构造 . . . . 191

- 23 类型守卫与断言函数 . . . . . . . . 193
23.1 静态类型何时会过于泛化？. . . . . . . . . . . 194
23.2 通过内置类型守卫进行窄化 . . . . . . . 196
23.3 用户定义的类型守卫 . . . . . . . . . . . . 201
23.4 断言函数 . . . . . . . . . . . . . . . . . 204
23.5 快速查阅：用户定义的类型守卫和断言函数 205
23.6 断言函数的替代方案 . . 206
23.7 @ts-guards: 带有类型守卫的库 208

## 24 验证外部数据 . . . . . . . . . . . . 209

- 24.1 JSON schema . . . . . . . . . . . . . . . . . . . 209
24.2 TypeScript 中的数据验证方法 . . . 211
24.3 示例：通过 Zod 库验证数据 212
24.4 结论 . . . . . . . . . . . . . . . . . . . 214

目录 7

## VI 杂记 215

- 25 类型计算概述 . . . . . . . . . . . . . . . . . . . . . . 217
25.1 作为元值的类型 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 217
25.2 泛型类型：类型的工厂 . . . . . . . . . . . . . . . . . . . . . 218
25.3 联合类型与交集类型 . . . . . . . . . . . . 219
25.4 控制流 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 221
25.5 其他各种操作 . . . . . . . . . . . . . . . 225

# 第一部分

# 准备工作

# 第 1 章

# 关于本书

目录
1.1 本书主页 . . . . . . . . . . . . . . . . . . . . . 11
1.2 本书内容 . . . . . . . . . . . . . . . . . . . . . 11
1.3 购买本书可以获得什么 . . . . . . . . . . . . . . . . . . . . . 11
1.4 如何预览内容 . . . . . . . . . . . . . . . . . . . . . . 12
1.5 如何报告错误 . . . . . . . . . . . . . . . . . . . . . . 12
1.6 图中图标的含义 . . . . . . . . . . . . . . . . . . . . . . 12
1.7 致谢 . . . . . . . . . . . . . . . . . . . . . . . 13

## 1.1 本书主页

github.com/tackling-ts

## 2 为什么使用 TypeScript?

| 章节 | 页码 |
| :--- | --- |
| 2.1 使用 TypeScript 的好处 | 15 |
| 2.1.1 在静态阶段检测到更多错误 | 15 |
| 2.1.2 为参数注释是良好的习惯 | 16 |
| 2.1.3 TypeScript 提供了额外的文档层 | 16 |
| 2.1.4 为 JavaScript 提供类型定义改进了自动补全 | 16 |
| 2.1.5 TypeScript 让重构更安全 | 17 |
| 2.1.6 TypeScript 可以编译新特性 | 17 |
| 2.2 使用 TypeScript 的劣势 | 17 |
| 2.3 TypeScript 误区 | 17 |
| 2.3.1 TypeScript 是笨重的 | 17 |
| 2.3.2 TypeScript 是试图用 Java 替换 JavaScript | 18 |





同样需要检查一致性并生成类型定义。更多信息，请参阅 TypeScript 手册中的“检查 JavaScript 文件类型”章节。

### 2.1.5 TypeScript 让重构更安全

重构是许多集成开发环境（IDE）提供的自动化代码转换功能。

重命名方法是重构的一个示例。在原生 JavaScript 中进行重命名可能是很棘手的，因为相同的名称可能指代不同的方法。TypeScript 拥有更多关于方法和类型之间如何连接的信息，这使得重命名方法变得更加安全。

### 2.1.6 TypeScript 可以将新特性编译为旧版代码

TypeScript 倾向于快速支持 ECMAScript 第 4 阶段的特性（这些特性计划包含在下一个 ECMAScript 版本中）。当我们编译为 JavaScript 时，编译器选项 `--target` 允许我们指定输出所兼容的 ECMAScript 版本。任何不兼容的特性（后来的引入的）都将被编译为等效的兼容代码。

请注意，这种对旧版 ECMAScript 版本的支持并不需要 TypeScript 或静态类型：JavaScript 编译器 Babel 也能这样做，但它是将 JavaScript 编译为 JavaScript。

## 2.2 使用 TypeScript 的缺点

- 它是 JavaScript 之上的又一个层：更多的复杂性、更多需要学习的内容等。
- 它在编写代码时引入了编译步骤。
- npm 包只有在具有静态类型定义的情况下才能被使用。
- 如今，许多包要么自带类型定义，要么在 DefinitelyTyped 中有可用的类型定义。然而，特别是后者，可能会略有错误，导致在没有静态类型的情况下出现问题。
- 获取静态类型有时是困难的。我在这里的建议是尽可能简单——例如：不要过度使用泛型和类型变量。

## 2.3 TypeScript 的误区

### 2.3.1 TypeScript 代码是笨肿的

TypeScript 代码可以非常笨重。但它没得如此。例如，由于类型推断，我们只需要少量的注解即可完成：

```
function selectionSort(arr: number[]) { // (A)
for (let i=0; i<arr.length; i++) {
  const minIndex = findIndex(arr, i);
  [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]]; // swap
}
```

```
function findMinIndex(arr: number[], startIndex: number) { // (B)
let minValue = arr[startIndex];
let minIndex = startIndex;
for (let i=startIndex+1; i < arr.length; i++) {
  const currentValue = arr[i];
  if (currentValue < minValue) {
    minValue = currentValue;
    minIndex = i;
  }
}
return minIndex;
}

const arr = [4, 2, 6, 3, 1, 5];
selectionSort(arr);
asert.deepEqual(arr, [1, 2, 3, 4, 5, 6]);
```

TypeScript 代码与 JavaScript 代码不同的地方只有 A 行和 B 行。

TypeScript 的编写有多种风格：

- 带有（classes）和 OOP 模式的面向对象编程（OOP）风格
- 带有函数式模式的函数式编程（FP）风格
- OOP 和 FP 的混合
- 以及此类推

### 2.3.2 TypeScript 试图用 C# 或 Java 替换 JavaScript

最初，TypeScript 发明了一些它自己的语言结构（例如枚举 enums）。但从 ECMAScript 6 开始，它主要保持作为 JavaScript 的严格超集。

我的印象是，TypeScript 团队喜欢 JavaScript，并且不想用某种“更好”的东西来替换它（这是例如 Dart 的目标）。他们确实希望尽可能对许多 JavaScript 代码进行静态类型化。许多新的 TypeScript 特性正是这种愿望驱动。

## 第 3 章

## 关于 TypeScript 的免费资源

关于 JavaScript 的书：

- 如果你在书中看到不理解的 JavaScript 特性，可以查阅我的书《给急性程序员看的 JavaScript》（JavaScript for impatient programmers），该书可以在线免费阅读。章节末的一些“进一步阅读”部分提到了这本书。

关于 TypeScript 的书：

- 《TypeScript Handbook》是该语言的一个很好的参考。我认为《Tackling TypeScript》是对该书的补充。
- Basarat Ali Syed 编写的《TypeScript Deep Dive》

更多材料：

- 《TypeScript Language Specification》解释了语言的低层原理。
- Marius Schulz 发布关于 TypeScript 的博客文章和邮件通讯“TypeScript Weekly”。
- TypeScript 仓库拥有完整 ECMAScript 标准库的类型定义。阅读它们是练习 TypeScript 类型表示法的简单方法。

## 第二部分

## 开始使用 TypeScript

## 第 4 章

## TypeScript 是如何工作的？鸟瞰视图

- 目录
4.1 TypeScript 项目的结构 . . . . . . . . . . . . . . . 23
4.1.1 tsconfig.json . . . . . . . . . . . . . . . . . . . 24
4.2 通过集成开发环境 (IDE) 编写 TypeScript . . . . . . . . . . . . . . . . . . . . 24
4.3 TypeScript 编译器产生的其他文件 . . . . . . . . . . . . . . . . . . . 25
4.3.1 为了在 TypeScript 中使用 npm 包，我们需要类型信息 . . . . . . . . . . . . . . . . . . . . . . . . . . . 25
4.4 使用 TypeScript 编译器处理原生 JavaScript 文件 . . . . . . . . . . . . 26

本章提供了关于 TypeScript 如何工作的鸟瞰视图：TypeScript 是如何工作？. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

4.1 TypeScript 项目的结构 . . . . . . . . . . . . . . . . 23
4.1.1 tsconfig.json . . . . . . . . . . . . . . . . . . . . 24
4.2 通过集成开发环境 (IDE) 编写 TypeScript . . . . . . . . . . . . . . . . . . . . 24
4.3 TypeScript 编译器产生的其他文件 . . . . . . . . . . . . . . . . . . . . 25
4.3.1 为了在 TypeScript 中使用 npm 包，我们需要类型信息 . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25
4.4 使用 TypeScript 编译器处理原生 JavaScript 文件 . . . . . . . . . . . . . 26

本章提供了关于 TypeScript 如何工作的鸟瞰视图：TypeScript 是如何工作？. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

4.1 TypeScript 项目的结构

一种可能的项目结构：

```
typescript-project/
dist/
src/
main.ts
test/
util.ts
tsconfig.json
```

解释：

- ts/ 包含 TypeScript 文件：
- 子目录 src/ 包含代码。
- 子目录 test/ 包含测试。
- dist/ 是编译器的输出。
- src/ 包含 TypeScript 文件编译为 JavaScript 文件。
- dist/ 包含类型信息（.ts 文件，去掉 JavaScript 代码后）
- tsconfig.json 用于配置 TypeScript 编译器。

4.1.1 tsconfig.json

tsconfig.json 的内容如下：

```json
{
  "compilerOptions": {
    "rootDir": "src",
    "outDir": "dist",
    "module": "commonjs",
    ...
  }
}
```

我们指定了：

- TypeScript 代码的根目录是 src/
- TypeScript 编译器保存输出的目录是 dist/
- 输出格式是 CommonJS

4.2 通过集成开发环境 (IDE) 编写 TypeScript

两种流行的 IDE 有：

- VS Code（免费）
- WebStorm（需购买）

本节的观察是关于 VS Code，但可能适用于其他 IDE。

需要注意的一个重要事实是 VS Code 通过两种独立的方式处理 TypeScript 源：

- 检查文件错误：这是通过所谓的语言服务器实现的。语言服务器独立于特定的编辑器，并为编辑器提供相关服务：重构、补全等。与服务器的通信基于 JSON-RPC。需要记住的重要事实：语言服务器只分析 TypeScript，不编译。

4.3 TypeScript 编译器产生的其他文件

- 构建（将 TypeScript 文件编译为 JavaScript 文件）：在这里有两种选择。
  - 我们可以通过外部命令行运行构建工具。例如，TypeScript 编译器 tsc 有一个监听模式，可以监听输入文件并编译为输出文件。结果是，每我们在 IDE 中保存 TypeScript 文件时，都会立即获得相应的输出。
  - 我们可以在 VS Code 内部运行 tsc。为了做到这一点，它必须安装在我们正在的项目内部或全局（通过 npm 管理）。有关在 VS Code 内部编译 TypeScript 的更多信息，请参阅该 IDE 的官方文档。

给定一个 TypeScript 文件 main.ts，TypeScript 编译器可以产生几种产物。最常见的有：

- JavaScript 文件：main.js
- 声明文件：main.d.ts（包含类型信息；去掉 JavaScript 代码）
- 源映射文件：main.js.map

源映射指定了 main.js 输出代码中的每个部分是由输入代码 main.ts 的哪个部分生成的。此外，这些信息允许运行时环境执行 JavaScript 代码，同时在错误消息中显示 TypeScript 代码的行号。





## 4.4 使用 TypeScript 编译器处理纯 JavaScript 文件

TypeScript 编译器也可以处理 JavaScript 文件：

- 使用 `--allowJS` 选项，TypeScript 编译器会将输入目录中的 JavaScript 文件复制到输出目录。优点是：在从 JavaScript 迁移到 TypeScript 时，我们可以从混合了 JavaScript 和 TypeScript 文件开始，并逐渐将更多的 JavaScript 文件转换为 TypeScript。
- 使用 `--checkJS` 选项，编译器会额外对 JavaScript 文件进行类型检查（必须开启 `--allowJS` 选项此才能生效）。在可用信息有限的情况下，它会尽力完成检查。哪些文件需要被检查可以通过文件内部注释进行配置：
    * 显式排除：如果 JavaScript 文件包含 `// @ts-nocheck`，则将不会对其进行类型检查。
    * 显式包含：在不使用 `--checkJS` 的情况下，可以使用注释 `// @ts-check` 对单个 JavaScript 文件进行类型检查。
- TypeScript 编译器使用通过 JSDoc 注释指定的静态类型信息（见下示例）。如果我们足够严谨，就可以对纯 JavaScript 文件进行完全静态类型化，并从它们推导出声明文件。
- 使用 `--noEmit` 选项，编译器不会产生任何输出，仅对文件进行类型检查。

这是一个为 `function()` 提供静态类型信息的 JSDoc 注释示例：

```typescript
/**
 * @param {number} x - 第一个操作数
 * @param {number} y - 第二个操作数
 * @returns {number} 两个操作数的和
 */
function add(x, y) {
  return x + y;
}
```

更多信息：[TypeScript Handbook 中的检查 JavaScript 文件](https://www.typescriptlang.org/docs/handbook/2/working-javascript.html)。




本章提供了关于如何快速尝试 TypeScript 的贴士。

### 5.1 TypeScript Playground

TypeScript Playground 是一个用于 TypeScript 代码的编辑器。功能包括：

- 支持全 IDE 风格编辑：自动补全等。

Playground 对于快速实验和演示非常有用。它可以将 TypeScript 代码片段和编译器设置都保存到 URL 中，这非常便于他人分享片段。以下是此类 URL 的示例：

https://www.typescript.org/play/#code=MEwdwgzLgBFDuLyBGTBGEGAKHgHmCdCdeW2AsgwD4YCb0BggChXRIQABFA04ymBmHRYA5AEMARsAkUkZIA

### 5.2 TS Node

TS Node 是 Node.js 的 TypeScript 版本。它的用场景包括：

- TS Node 为 TypeScript 提供了一个 REPL（命令行界面）：

```bash
$ ts-node
> const twice = (x: string) => x + x;
> twice('abc')
> 'abc'
> twice(123)
Error TS2345: Argument of type '123' is not assignable to parameter of type 'string'.
```

- TS Node 允许某些 JavaScript 工具直接执行 TypeScript 代码。它会自动将 TypeScript 代码编译为 JavaScript 代码并传递给工具，而我们无需做任何操作。下面的 shell 命令演示了它如何与 JavaScript 单元测试框架 Mocha 协作：

```bash
mocha --require ts-node/register --ui qunit testfile.ts
```

使用 `npx ts-node` 可以在无需安装的情况下运行 REPL。
## 第 6 章
## 书中符号

本章解释了代码示例中使用的功能，但这些功能并不是 TypeScript 本身。

### 6.1 测试断言（动态）

书中显示的代码示例通过单元测试自动测试。操作的预期结果通过 Node.js `assert` 模块中的以下断言函数进行检查：

- `assert.equal()` 测试相等性 `===`。
- `assert.deepEqual()` 通过通过深度比较嵌套对象（包括数组）来测试相等性。
- `assert.throws()` 如果回调参数没有抛出异常，则报错。

以下是使用这些断言的示例：

```javascript
import strict as assert from 'assert';

assert.equal(3 + 'apples', '3 apples');

assert.deepEqual(
  ['a', 'b'], 
  ['a', 'b']
);

assert.throws(
  () => eval(null.myProperty),
  TypeError
);
```

第一行的 import 语句使用了严格断言模式（使用 `===` 而非 `==`）。它在代码示例中通常会被省略。

### 6.2 类型断言（静态）

你也会看到静态类型断言。

`%inferred-type` 在普通 TypeScript 中只是一个注释，描述了 TypeScript 为下一行推断出的类型：

```typescript
// %inferred-type: number
let num = 123;
```

`@ts-expect-error` 用于抑制 TypeScript 中的静态错误。在书中，被抑制的错误总是会被提到的。这在纯 TypeScript 中既不是要求的，在那里也不会起任何作用。

```typescript
assert.throws(
  // @ts-expect-error: Object is possibly 'null'. (2531)
  () => null.myProperty,
  TypeError);
```

注意，我们之前需要 `eval()` 是为了不被 TypeScript 警告。




本章解释了 TypeScript 的核心基础。

### 7.1 你将学习的内容

读完本章后，你应该能够理解以下 TypeScript 代码：

```typescript
interface Array<T> {
  concat(items: Array<T> | T): T[];
  reduce<U>(
    callback: (state: U, element: T, index: number, array: T[]) => U,
    firstState?: U
  ): U;
  //...
}
```

你可能认为这很晦涩。我同意你的同！但（正如我希望证明的那样）这种语法相对容易学习。一旦你理解了它，它就能对代码行为提供立即、精确且全面的总结——无需阅读冗长的英文描述。

### 7.2 指定类型检查的完备性

TypeScript 编译器有许多配置方式。一组选项控制编译器如何检查 TypeScript 代码。最高设置通过 `--strict` 激活，我建议始终使用它。它让编写程序变得稍微困难，但我们也获得了静态类型检查的完整处。

> 关于 --strict，你现在只需要知道这些

如果你想了解更多细节，请继续阅读。

将 `--strict` 设置为 true 会将以下所有选项设置为 true：

- `--noImplicitAny`: 如果 TypeScript 无法推断出类型，我们必须指定。这主要适用于函数和方法的参数：通过这些设置，我们必须标注它们。
- `--noImplicitThis`: 如果 `this` 的类型不明确，则报错。
- `--alwaysStrict`: 尽可能使用 JavaScript 的严格模式。





## 7.3 TypeScript 中的类型

- strictNullChecks: null 不属于任何类型（除其自身的类型 null 除外），如果它是可接受的值，则必须显式说明。
- strictFunctionTypes: 对函数类型启用更严格的检查。
- strictPropertyInitialization: 类定义中的属性必须初始化，除非它们的值为 undefined。

我们将在本书的后后部分看到更多编译器选项，那时我们将学习使用 TypeScript 创建 npm 软件包和 Web 应用。TypeScript 手册对这些内容有详尽的文档。

## 7.3 TypeScript 中的类型

在本章中，类型简单来说就是值的集合。JavaScript 语言（不是 TypeScript！）只有八种类型：

1. Undefined: 仅包含元素 `undefined` 的集合。
2. Null: 仅包含元素 `null` 的集合。
3. Boolean: 包含 `false` 和 `true` 两个元素的集合。
4. Number: 所有数字的集合。
5. Bigint: 所有任意精度整数的集合。
6. String: 所有字符串的集合。
7. Symbol: 所有符号的集合。
8. Object: 所有对象的集合（包括函数和数组）。

所有这些都是动态的：我们可以在运行时使用它们。

TypeScript 为 JavaScript 增加了一层：静态类型。这些类型仅在编译或对源码进行类型检查时存在。每个存储位置（变量、属性等）都有一个静态类型，用于预测其动态值。类型检查确保这些预测能够实现。

有很多内容可以进行静态检查（无需运行代码）。例如，如果函数 `toString(num)` 的参数 `num` 静态类型为 `number`，那么函数调用 `toString('abc')` 就是非法的，因为参数 'abc' 的静态类型错误。

## 7.4 类型注解

```
function toString(num: number): string {
  return String(num);
}
```

在上面的函数声明中，有两个类型注解：

- 参数 num: 冒号后跟 `number`
- toString() 的结果: 冒号后跟 `string`

`number` 和 `string` 都是指定存储位置类型的类型表达式。

## 7.5 类型推断

通常情况下，如果没有类型注解，TypeScript 可以推断出静态类型。例如，如果我们省略函数 `f()` 的返回类型，TypeScript 会推断它是一个字符串：

```typescript
// inferred-type: (num: number) => string
function toString(num: number) {
  return String(num);
}
```

类型推断不是猜测：它遵循清晰的规则（类似于算术），在未显式指定类型的地方推导出类型。在这种情况下，返回语句应用了一个函数 `String()`，该函数将任意值映射到字符串，并将类型为 `number` 的值返回。这就是为什么推断出的返回类型是 `string` 的原因。

如果一个位置的类型既未指定也无法推断，TypeScript 将对其使用 `any` 类型。它是所有值的类型，也是通配符，因为如果它有值类型，我们可以做任何事情。

使用 `--strict` 时，只有显式使用时才允许 `any`。换句话说：每个位置都必须有一个显式或推断的静态类型。在下面的示例中，参数 `num` 两者没有，我们得到了一个编译错误：

```typescript
// @ts-expect-error: Parameter 'num' implicitly has an 'any' type. (7006)
function toString(num) {
  return String(num);
}
```

## 7.6 通过类型表达式指定类型

类型注解中冒号后面的类型表达式从简单到复杂，并如下所示创建。

基本类型是有效的类型表达式：

- JavaScript 动态类型的静态类型：
  - undefined, null
  - boolean, number, bigint, string
  - symbol
  - object.
- TypeScript 特有的类型：
  - Array（在 JavaScript 中技术上不属于一种类型）
  - any（所有值的类型）
  - 等。

有许多方法组合基本类型以产生新的复合类型。例如，通过类型运算符以类似的方式组合类型，如联合 (union) 和交集 (intersection) 运算符组合集合。我们将很快看到如何这样做。

## 7.7 两个语言级别：动态 vs 静态

TypeScript 有两个语言级别：

- 动态级别由 JavaScript 管理，在运行时由代码和值组成。
- 静态级别由 TypeScript 管理，在编译时由类型组成。

我们可以在语法中看到这两个级别：

```javascript
const undef = undefined;
```

- 在动态级别，我们使用 JavaScript 声明变量 `undef` 并用值进行它。
- 在静态级别，我们使用 TypeScript 指定变量 `undef` 的静态类型。

注意，相同的语法 `undefined` 不同的含义取决于它是在动态级别还是静态级别使用的。

> 尝试培养对两个级别的意识
> 这有助于理解 TypeScript。

## 7.8 类型别名

使用 `type` 我们可以为现有类型创建一个新名称（别名）：

```typescript
type Age = number;
const age: Age = 8;
```

## 7.9 数组

数组在 JavaScript 中扮演着两种角色：

- 列表：所有元素具有相同的类型。
- 元组：数组长度是固定的。元素没有相同的类型。

### 7.9.1 数组作为列表

有两种方式表示数组被用作元素全是数字的列表：

```typescript
let arr1: number[] = [];
let arr2: Array<number> = [];
```

如果有赋值，TypeScript 可以推断变量的类型。在这种情况下，对于空数组，它无法确定元素的类型。

我们将回到角括号符号 (`<number>`)。

### 7.9.2 数组作为元组

如果在数组中存储一个二维 `point`，那么我们正在使用数组作为元组。如下所示：

```typescript
let point: [number, number] = [7, 5];
```

对于元组需要类型注解；对于数组字面量，TypeScript 推断出列表类型而不是元组类型：

```typescript
// inferred-type: number[]
let point = [7, 5];
```

另一个元组示例是 `Object.entries(obj)`：对于 `obj` 的每个属性都有一个 `[key, value]` 对。

```typescript
// inferred-type: [string, number][]
const entries = Object.entries({ a: 1, b: 2 });
```

```javascript
assert.deepEqual(
  entries,
  [['a', 1], ['b', 2]]
);
```

推断类型是元组数组。

## 7.10 函数类型

这是一个函数类型的示例：

```typescript
(num: number) => string
```

该类型包含每个接受单个 `number` 类型参数并返回 `string` 的函数。让我们在注解中使用这种类型：

```typescript
const toString: (num: number) => string = // (A)
(num: number) => String(num); // (B)
```

通常我们会指定函数的参数类型。在这种情况下，B 行的 `number` 类型是从 A 行的函数推断出来的，我们可以省略它：

```typescript
const toString: (num: number) => string =
(num) => String(num);
```

如果我们省略了 `toString` 的类型注解，TypeScript 从箭头函数推断出类型：

```typescript
// inferred-type: (num: number) => string
const toString = (num: number) => String(num);
```

## 7.10 函数类型

这次，`num` 必须有一个类型注解。

### 7.10.1 一个更复杂的示例

下面的示例更复杂：

```typescript
function stringify123(callback: (num: number) => string) {
  return callback(123);
}
```

我们使用一个函数来描述 `stringify123` 的参数 `callback`。由于这个注解，TypeScript 拒绝了该函数调用。

```typescript
// @ts-expect-error: Argument of type 'NumberConstructor' is not
// assignable to parameter of type '(num: number) => string'
// Type 'number' is not assignable to type 'string'. (2345)
stringify123(Number);
```

但它接受这个函数调用：

```javascript
assert.equal(
stringify123(String), '123');
```

### 7.10.2 函数声明的返回类型

TypeScript 通常可以推断函数的返回类型，但显式指定它们是被允许的且有时有用（至少没有害）。

对于 `stringify123()`，指定返回类型是可选的，如下所示：

```typescript
function stringify123(callback: (num: number) => string): string {
  return callback(123);
}
```

### 7.10.2.1 特殊返回类型 void

`void` 是函数的特殊返回类型：它告诉 TypeScript 函数总是返回 `undefined`。

它可以显式地这样做：

```typescript
function f1(): void {
  return undefined;
}
```

或者它可以隐式地这样做：

```typescript
function f2(): void {};
```

[/content]

然而，函数不能显式返回 `undefined` 之外的值：

```typescript
function f3(): void {
// @ts-expect-error: Type "abc" is not assignable to type 'void'. (2322)
  return 'abc';
}
```





### 7.10.3 可选参数

标识符后面的问号意味着该参数是可选的。例如：

```typescript
function stringify123(callback?: (num: number) => string) {
  if (callback === undefined) {
    callback = String;
  }
  return callback(123); // (A)
}
```

只有在我们确保 `callback` 不是 `undefined` 时（如果省略了参数，它就是未定义的），TypeScript 才允许我们在行 A 中进行函数调用。

### 7.10.3.1 参数默认值

TypeScript 支持参数默认值：

```typescript
function createPoint(x=0, y=0): [number, number] {
  return [x, y];
}

assert.deepEqual(
  createPoint(),
  [0, 0]);
assert.deepEqual(
  createPoint(1, 2),
  [1, 2]);
```

默认值使参数变为可选。我们通常可以省略类型注解，因为 TypeScript 可以推断类型。例如，它推断出 x 和 y 的类型均为 `number`。

如果我们想添加类型注解，写法如下：

```typescript
function createPoint(x:number = 0, y:number = 0): [number, number] {
  return [x, y];
}
```

## 7.10.4 剩余参数

我们还可以在 TypeScript 参数定义中使用剩余参数。它们的静态类型必须是数组（列表或元组）：

```typescript
function joinNumbers(...nums: number[]): string {
  return nums.join('-');
}
assert.equal(
  joinNumbers(1, 2, 3),
  '1-2-3');
```

## 7.11 联合类型

变量所持有的（一次一个值）可以是不同类型的成员。在这种情况下，我们需要联合类型。例如，在下面的代码中，`stringOrNumber` 既可以是 `string` 类型也可以是 `number` 类型：

```typescript
function getScore(stringOrNumber: string|number): number {
  if (typeof stringOrNumber === 'string'
    && /\d*(1,5)/.test(stringOrNumber)) {
    return stringOrNumber.length;
  } else if (typeof stringOrNumber === 'number'
    && stringOrNumber >= 1 && stringOrNumber <= 5) {
    return stringOrNumber;
  } else {
    throw new Error('Illegal value: ' + JSON.stringify(stringOrNumber));
  }
}
```

assert.equal(getScore('******'), 5);
assert.equal(getScore(3), 3);

`stringOrNumber` 的类型是 `string|number`。类型表达式 `s|t` 的结果是类型 `s` 和 `t` 的集合并（解释为集合）。

### 7.11.1 默认情况下，undefined 和 null 不包含在类型中

在许多编程语言中，`null` 是所有对象类型的一部分。例如，在 Java 中，当变量类型为 `String` 时，我们可以设置为 `null` 而 Java 不会报错。

相反，在 TypeScript 中，`undefined` 和 `null` 由独立的、不相交的类型处理。如果我们想允许它们存在，就需要像 `undefined|string` 和 `null|string` 这样的联合类型：

```typescript
let maybeNumber: null|number = null;
maybeNumber = 123;
```

否则，我们会得到错误：

```typescript
// @ts-expect-error: Type 'null' is not assignable to type 'number'. (2322)
let maybeNumber: number = null;
maybeNumber = 123;
```

注意，TypeScript 并不强制我们立即初始化（只要我们在初始化之前没有读取变量）：

```typescript
let myNumber: number; // OK
myNumber = 123;
```

### 7.11.2 显式省略省略

回顾这个函数：

```typescript
function stringify123(callback?: (num: number) => string) {
  if (callback === undefined) {
    callback = String;
  }
  return callback(123); // (A)
}
```
（注：此处原文示例似乎有误，已根据上下文逻辑翻译）

让我们重写 `stringify123`，使得 `callback` 不是可选的：如果调用者不想提供函数，他们必须显式传递 `null`。结果如下：

```typescript
function stringify123(
  callback: null | ((num: number) => string)) {
  if (callback === null) { // (A)
    callback = String;
  }
  return callback(123); // (B)
}
```

```typescript
assert.equal(stringify123(null), '123');

// @ts-expect-error: Expected 1 arguments, but got 0. (2554)
assert.throws(() => stringify123());
```

再次，我们在行 B 中进行调用之前，必须处理 `callback` 不是函数的情况。如果我们没有这样做，TypeScript 会在行行报告错误。

## 7.12 可选默认值 vs undefined.|T

以下三个参数声明非常相似：

- 是可选的：`x?: number`
- 有默认值：`x = 256`
- 有联合类型：`x: undefined | number`

如果参数是可选的，它可以被省略。在这种情况下，它有值：

```typescript
function f1(x?: number) { return x }
```

```typescript
assert.equal(f1(123), 123); // OK
assert.equal(f1(undefined), undefined); // OK
assert.equal(f1(), undefined); // 可以省略
```

如果参数有默认值，当参数被省略或设置为 `undefined` 时：

```typescript
function f2(x = 256) { return x }
```

```typescript
assert.equal(f2(123), 123); // OK
assert.equal(f2(undefined), 256); // OK
```

如果参数是联合类型，它不能被省略，但我们可以将其设置为 `undefined`：

```typescript
function f3(x: undefined | number) { return x }
```

```typescript
assert.equal(f3(123), 123); // OK
assert.equal(f3(undefined), undefined); // OK

// @ts-expect-error: Expected 1 arguments, but got 0. (2554)
f3(); // 可以省略

## 7.13 对象类型

与数组类似，对象在 JavaScript 中扮演着两种角色（有时会混合）：

- **记录 (Records)**：在开发时已知的固定数量。每个属性可以有不同的类型。
- **字典 (Dictionaries)**：属性名称在开发时未知。所有属性具有相同的类型。

在本章中我们忽略作为字典的对象——它们在 §16.4.5 “索引签名：作为字典的对象”中介绍。顺便提一下，Maps 通常是字典更好的选择。

### 7.13.1 通过接口定义对象记录

接口描述了对象记录。例如：

```typescript
interface Point {
  x: number;
  y: number;
}
```

我们也可以通过逗号分隔成员：

```typescript
interface Point {
  x: number;
  y: number;
}
```

### 7.13.2 TypeScript 的结构类型 vs 命名类型

TypeScript 类型系统的一个优势是它是结构性的，而不是命名的。也就是说，Point 匹配所有具有相应结构的对象。

相反，在 Java 的命名类型系统中，我们必须显式声明它实现了哪些接口。因此，类只能实现其创建时存在的接口。

### 7.13.3 对象字面量类型

对象字面量类型是匿名接口：

```typescript
type Point = {
  x: number;
  y: number;
};
```

对象字面量类型的好处是它们可以内联使用：

```typescript
function toString(pt: {x: number, y: number}) {
  return `${pt.x}, ${pt.y}`;
}
```

### 7.13.4 可选属性

如果一个属性可以省略，我们在它的名字后面加一个问号：

```typescript
interface Person {
  name: string;
  company?: string;
}
```

在这个示例中，john 和 jane 都匹配接口：

```typescript
const john: Person = {
  name: 'John',
};
const jane: Person = {
  name: 'Jane',
  company: 'Massive'
};
```

### 7.13.5 方法

接口还可以包含方法：

```typescript
interface Point {
  x: number;
  y: number;
  distance(other: Point): number;
}
```

## 7.14 类型变量和泛型类型

回顾 TypeScript 的两个语言级别：

- 值存在于动态级别。
- 类型存在于静态级别。

我的建议是使用任何能表达属性应该如何设置的语法。普通函数存在于动态级别，是值的工厂，其参数代表值。参数在括号 `()` 之间声明：

```typescript
const valueFactory = <T>(x: T): T => x; // 定义
const value = valueFactory<number>(123); // 使用
```

- 泛型类型存在于静态级别，是类型的工厂，其参数代表类型。参数在尖括号 `<>` 之间声明：

```typescript
type Box<T> = { content: T };
```





type Factory<X> = X; // 定义
type MyType = Factory<string>; // 使用

## 命名类型参数

在 TypeScript 中，通常使用单个大写字母（如 `T`）作为参数。然而，可以使用任何合法的 JavaScript 标识符。

### 7.14.1 示例：值的容器

```typescript
// 类型的工厂
interface ValueContainer<Value> {
  value: Value;
}
```

```typescript
// 创建一个类型
type StringContainer = ValueContainer<string>;
```

`Value` 是一个类型变量。尖括号内可以引入一个或多个类型变量。

## 7.15 示例：泛型类

类可以有类型参数，

```typescript
class SimpleStack<Elem> {
  #data: Array<Elem> = [];
  push(x: Elem): void {
    this.#data.push(x);
  }
  pop() {
    const result = this.#data.pop();
    if (result === undefined) {
      throw new Error();
    }
    return result;
  }
  get length() {
    return this.#data.length;
  }
}
```

`SimpleStack` 拥有类型参数 `Elem`。通常使用单个大写字母（如 `T`）作为类型参数。

当我们实例化类时，也为类型参数提供一个值：

```typescript
const stringStack = new SimpleStack<string>();
stringStack.push('first');
```

## 7.15 示例：泛型类

```typescript
stringStack.push('second');
assert.equal(stringStack.length, 2);
assert.equal(stringStack.pop(), 'second');
```

### 7.15.1 示例：Maps

Map 在 TypeScript 中是泛型类型化的。例如：

```typescript
const mMap: Map<boolean, string> = new Map([
  [false, 'no'],
  [true, 'yes']
]);
```

由于得益于类型推断（基于 `new Map()` 的参数），我们可以省略类型参数：

```typescript
// 推断出的类型: Map<boolean, string>
const mMap = new Map([
  [false, 'no'],
  [true, 'yes']
]);
```

### 7.15.2 函数和方法的类型变量

函数定义可以这样引入类型变量：

```typescript
function identity<Arg>(arg: Arg): Arg {
  return arg;
}
```

我们如下所示使用它：

```typescript
// 推断出的类型: number
const num1 = identity<number>(123);
```

由于类型推断，我们可以再次省略类型参数：

```typescript
// 推断出的类型: 123
const num2 = identity(123);
```

注意，TypeScript 推断出了类型 `123`，这是一个包含一个数字的集合，并且比 `number` 类型更具体。

### 7.15.2.1 箭头函数和方法

箭头函数也可以有类型参数：

```typescript
const identity = <Arg>(arg: Arg): arg => arg;
```

这是方法的类型参数语法：

```typescript
const obj = {
  identity<Arg>(arg: Arg): Arg {
    return arg;
  }
};
```

### 7.15.3 一个更复杂的 <T> 函数示例

```typescript
// %inferred-type: <T>(len: number, elem: T) => T[]
function fillArray<T>(len: number, elem: T) {
  return new Array<T>(len).fill(elem);
}
```

变量 `T` 在这段代码中出现了三次：

- 它通过 `fillArray<T>` 被引入。因此，它的作用域是函数。
- 它第一次在参数 `elem` 的类型注解中使用。
- 它还用作 `Array()` 构造函数的类型参数。

`fillArray()` 的返回类型是推断的，但我们也可以显式指定。
在调用 `fillArray()` 时可以省略类型参数（A 行），因为 TypeScript 可以从参数元素推断出 `T`：

```typescript
// %inferred-type: string[]
const arr1 = fillArray<string>(3, '*');
assert.deepEqual(
  arr1, ['*', '*', '*']
);

// %inferred-type: string[]
const arr2 = fillArray(3, '*'); // (A)
```

## 7.16 结论：理解初始示例

让我们用所学的知识来理解之前看到的这段代码：

```typescript
interface Array<...items: Array<T[]> | T> {
  reduce<U>(
    callback: (state: U, element: T, index: number, array: T[]) => U,
    firstState?: U
  );
  //...
}
```

这是一个元素类型为 `T` 的数组示例：

- `method.concat()` 方法有零个或多个参数（通过剩余参数定义）。
  这些每个参数的类型都是 `T[]|T`。





## 8.4 .gitignore

ts/src/index.ts --> dist/src/index.js
ts/test/index_test.ts --> dist/test/index_test.js

## 8.4 .gitignore

此文件列出了我们不想提交到 git 的目录：

- node_modules/
- dist/

解释：

- node_modules/ 是通过 `npm install` 设置的。
- dist/ 中的文件是由 TypeScript 编译器创建的（稍后会详细介绍）。

## 8.5 .npmignore

在涉及到哪些文件应该和不应该上传到 npm 注册表时，我们的需求与 git 不同。因此，除了 .gitignore 之外，我们还需要 .npmignore 文件：

ts/

两个区别在于：

- 我们希望将 TypeScript 编译为 JavaScript 的结果（dist/ 目录）。
- 我们不想上传 TypeScript 源代码文件（ts/ 目录）。

注意，npmignore 默认忽略 `node_modules/` 目录。

## 8.6 package.json

package.json 如下所示：

```json
{
...
  "type": "commonjs",
  "main": "./dist/src/index.js",
  "types": "./dist/src/index.d.ts",
  "scripts": {
    "clean": "shx -rf dist*",
    "build": "tsc",
    "watch": "tsc --watch unit",
    "test": "mocha --ui unit",
    "testall": "mocha --unit dist/test",
    "prepack": "npm run clean && npm run build"
  },
  "devDependencies": {
    "@types/node": "Needed for unit test assertions (assert.equal() etc.)."
  }
}
```

# 8 通过 TypeScript 创建基于 CommonJS 的 npm 包

```json
{
  "shx": "Needed for development-time package.json scripts",
  "devDependencies": {
    "@types/lodash": "...",
    "@types/mocha": "...",
    "@types/node": "...",
    "mocha": "...",
    "shx": "..."
  },
  "dependencies": {
    "lodash": "..."
  }
}
```

让我们来看看这些属性：

- type: 值 "commonjs" 意味着 .js 文件被解释为 CommonJS 模块。
- main: 如果存在所谓的裸导入（bare import），仅提到当前包的名称，那么这将将被导入的模块。
- types: 指向一个包含当前包所有类型定义的声明文件。

接下来的章节将介绍剩余的属性。

### 8.6.1 Scripts

scripts 属性定义了可以通过 `npm run` 调各种命令。例如，通过 `npm run clean` 运行 clean 脚本。之前的 package.json 包含以下脚本：

- clean 使用跨平台包 shx，通过其对 Unix shell `rm` 的实现来删除编译结果。shx 支持多种 shell 命令，优点是无需为我们可能使用的每个命令都单独准备一个包。
- build 和 watch 使用 TypeScript 编译器 `tsc` 根据 `tsconfig.json` 编译 TypeScript 文件。`tsc` 必须全局安装或本地安装（在当前包内），通常通过 npm 包 types（应为 typescript）安装。
- test 和 testall 使用单元测试框架 `Mocha` 运行一个或所有测试。
- prepack: 此脚本在打包 tarball 之前运行（由于 `npm pack`、`npm publish` 或从 git 安装）。

注意，由于我们使用 IDE，我们不需要 build 和 watch 脚本，因为我们可以让 IDE 构建产物。它们对于 prepack 脚本是需要的。

### 8.6.2 dependencies vs. Dependencies

dependencies 应该只包含导入包时需要的包。这排除了用于运行测试等目的包。

## 8.7 tsconfig.json

以 @types/ 开头的包为没有任何定义的的包提供了 TypeScript 定义。没有前者，我们就无法使用后者。这些是普通依赖还是开发依赖？这取决于情况：

- 如果我们包的类型定义引用了另一个包的类型定义，那么该包就是普通依赖。
- 否则，该包仅在开发期间需要，是一个开发依赖（dev dependency）。

### 8.6.3更多关于 package.json

- "Awesome npm scripts" 提供了编写跨平台脚本的提示。
- npm 关于 package.json 的文档解释了该文件的各种属性。
- npm 关于 scripts 的文档解释了 package.json 中的 scripts 属性。

## 8.7 tsconfig.json

```json
{
  "compilerOptions": {
    "rootDir": "ts",
    "outDir": "dist",
    "target": "es2019",
    "lib": [
      "es2019"
    ],
    "module": "commonjs",
    "esModuleInterop": true,
    "strict": true,
    "declaration": true,
    "sourceMap": true
  }
}
```

- rootDir: 你的 TypeScript 文件位于哪里？
- outDir: 编译结果应该在哪里？
- target: 目标 ECMAScript 版本是什么？如果 TypeScript 代码使用了目标版本不支持的功能，那么它被认为是只使用支持功能的等效代码。
- lib: TypeScript 应该感知哪些功能？可能包括 ECMAScript 标准库和浏览器的 DOM。Node.js API 通过不同的方式支持，通过 `@types/node` 包。
- module: 指定编译输出的格式。

其余选项由 tsconfig.json 文档解释。

## 8.8 TypeScript 代码

### 8.8.1 index.ts

此文件提供了实际的功能：

```typescript
import endsWith from 'lodash';

export function removeSuffix(str: string, suffix: string): string {
  if (!endsWith(str, suffix)) {
    throw new Error(suffix + ' is not a suffix of ' + str);
  }
  return str.slice(0, -suffix.length);
}
```

它使用了 Lodash 的 `endsWith()`。这就是为什么它是普通依赖。

### 8.8.2 index_test.ts

此文件包含 index.ts 的单元测试：

```typescript
import { assert } from 'assert';
import { removeSuffix } from '../index';

test('removeSuffix()', () => {
  assert.equal(
    removeSuffix('myfile.txt', '.txt'),
    'myfile'
  );
  assert.throws(() => removeSuffix('myfile.txt', 'abc'));
});
```

我们可以这样运行测试：

```bash
npm t dist/index_test.js
```

- npm 命令 t 是 npm test 的缩写。
- npm 命令 test 是 npm run 的缩写（运行 package.json 中的脚本）。

你可以看到，我们运行的是测试的编译版本（在 dist/ 中），而不是 TypeScript 代码。

更多关于单元测试框架 Mocha 的信息请参见其主页。

# 第9章 通过 TypeScript 和 webpack 创建 Web 应用

- 目录
9.1 需要的知识 ................................................................................................................. . . . . 55
9.2 局限性 ................................................................................................................. . . . . . . . . . . . . . . 56
9.3 ts-demo-webpack 仓库 ................................................................................................................. . . . . . 56
9.4 package.json ................................................................................................................................. . . . . . . . 57
9.5 webpack.config.js ................................................................................................................................. . . . . . . 58
9.6 tsconfig.json ................................................................................................................................................................................................................................................................. 59
9.7 index.html ......................................................................................................................................................................................................................................................................... . 59
9.8 main.ts ................................................................................................................................................................................................................................................................................. 60
9.9 安装、构建和运行 Web 应用 ................................................................................................................................ 60
9.9.1 在 Visual Studio Code 中构建 ............................................................................................................ 61
9.10 不使用加载器的 webpack：webpack-no-loader.config.js ........................................................................................................ 61

本章描述了如何通过 TypeScript 和 webpack 创建 Web 应用。我们将只使用 DOM API，而不是某个特定的前端框架。

> GitHub 仓库：ts-demo-webpack
我们在本章中使用的 ts-demo-webpack 仓库可以从 GitHub 下载。

9.1 需要的知识

你应该大致熟悉：

* npm
* webpack





## 9.2 局限性

在本章中，我们坚持使用 TypeScript 支持最好的：作为脚本文件打包的 CommonJS 模块。

## 9.3 ts-demo-webpack 仓库

这是 ts-demo-webpack 仓库的结构方式：

```
ts-demo-webpack/
build/ (按需创建)
html/
index.html
package.json
ts/
src/
main.ts
tsconfig.json
webpack.config.js
```

Web 应用的构建方式如下：

- 输入：
  - ts/ 目录下的 TypeScript 文件
  - 所有通过 npm 安装并由 TypeScript 文件导入的 JavaScript 代码
  - html/ 目录下的 HTML 文件
- 输出 - build/ 目录，包含完整的 Web 应用：
  - TypeScript 文件被编译为 JavaScript 代码，并与 npm 安装的 JavaScript 合并，然后写入脚本文件 build/main-bundle.js。这个过程被称为打包（bundling），main-bundle.js 是一个包文件（bundle file）。
  - 每个 HTML 文件都会被复制到 build/。

两个输出任务都由 webpack 处理：

- 将 html/ 中的文件复制到 build/ 是通过 webpack 插件 copy-webpack-plugin 完成的。

- 本章探索了两种不同的打包工作流：
  - 使用 webpack 在 ts-loader 的帮助下直接将 TypeScript 文件编译成包。
  - 或者我们自己将 TypeScript 文件复制到 dist 目录下的 JavaScript 文件（正如我们在上一章中所做的那样）。这样 webpack就不需要 loader，只需打包 JavaScript 文件。

本章的大部分内容关于如何配合 ts-loader 使用 webpack。在最后，我们简要查看了另一种工作流。

## 9.4 package.json

package.json 包含了项目的元数据：

```
{
  "private": true,
  "scripts": {
    "tsc": "tsc",
    "tscw": "tsc --watch",
    "wp": "webpack",
    "wpw": "webpack --watch",
    "serve": "http-server build"
  },
  "dependencies": {
    "@types/lodash": "...",
    "copy-webpack-plugin": "...",
    "http-server": "...",
    "lodash": "...",
    "ts-loader": "...",
    "typescript": "...",
    "webpack": "...",
    "webpack-cli": "..."
  }
}
```

这些属性的作用如下：

- "private": true 意味着如果我们不提供包名和包版本，npm 不会报错。

- Scripts:
  - tsc, tscw: 这些脚本直接调用 TypeScript 编译器。如果我们使用带 ts-loader 的 webpack，就不需要它们。但是，如果我们使用不带 ts-loader 的 webpack（在本章末尾演示），它们就是很有用的。
  - wpw: 以监听模式运行 webpack，它会监控输入文件并只编译变化的文件。
  - serve: 运行 http-server 服务器并提供 build/ 目录下的完全组装的 Web 应用。

- Dependencies:
  -四个与 webpack 相关的包：
    - webpack: webpack 的核心
    - webpack-cli: 核心的命令行界面
    - ts-loader: 针对 .ts 的 loader，将其编译为 JavaScript
    - copy-webpack-plugin: 将文件从一个位置复制到另一个位置的插件
  - ts-loader 需要的：typescript
  - 提供 Web 应用：http-server
  - TypeScript 代码使用的库加类型定义：lodash
    - @types/lodash

## 9.5 webpack.config.js

这是我们配置 webpack 的方式：

```javascript
const path = require('path');
const CopyWebpackPlugin = require('copy-webpack-plugin');

module.exports = {
  entry: {
    main: "./ts/src/main.ts",
  },
  output: {
    path: path.resolve(__dirname, 'build'),
    filename: "[name]-bundle.js",
  },
  resolve: {
    // 添加 .ts 和 .tsx 作为可解析的扩展。
    extensions: [ ".ts", ".tsx", ".js"],
  },
  module: [{
    // 所有 .ts 或 .tsx 扩展的文件将由 `ts-loader` 处理
    test:\.tsx?$/, loader: "ts-loader"
  ],
  plugins: [
    new CopyWebpackPlugin([
      {
        from: './html',
      })
    ])
};
```

属性说明：

- entry（入口）是 webpack 开始收集输出包数据的文件。首先它将入口文件添加到包中，然后是入口的导入，然后是导入的导入，依此类推。entry 属性的值是一个对象，其属性键指定入口的名称，值指定入口的路径。
- output 指定输出包的路径。[name] 在存在多个入口点（因此有多个包）时特别有用。在组装路径时，它会被替换为入口的名称。
- resolve 配置 webpack 如何将模块的标识符（ID）转换为文件位置。
- module 配置 loaders（处理文件的插件）等。

## 9.6 tsconfig.json

- plugins 配置了插件，这些插件可以以多种方式改变和增强 webpack 的行为。

关于配置 webpack 的更多信息，请参阅 webpack 网站。

此文件配置 TypeScript 编译器：

```
{
  "compilerOptions": {
    "rootDir": "ts",
    "outDir": "dist",
    "target": "es2019",
    "lib": [
      "es2019",
    ],
    "module": "commonjs",
    "esModuleInterop": true,
    "strict": true,
    "sourceMap": true
  }
}
```

此文件配置 TypeScript 编译器。

## 9.7 index.html

这是配置的 HTML 页面：

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <title>ts-demo-webpack</title>
</head>
<body>
  <div id="output"></div>
  <script src="main-bundle.js"></script>
</body>
</html>
```

## 9.8 main.ts

这是应用的 TypeScript 代码：

```typescript
import template from 'lodash';

const outputElement = document.getElementById('output');
if (outputElement) {
  const compiled = template(`
<h1>ts-demo-webpack</h1>
  Current date and time: ${new Date().toISOString()}
`).trim();
  outputElement.innerHTML = compiled;
}
```

## 9.9 安装、构建和运行应用

首先我们需要安装应用依赖的全部 npm 包：

```bash
npm install
```

然后通过 package.json 中的脚本运行 webpack（在之前的步骤中已安装）：

```bash
npm run wpw
```

现在，webpack 会监控文件并在文件发生变化时重新构建。

在不同的命令行中，我们可以启动一个提供 build/ 目录内容的服务器：

```bash
npm run serve
```

如果我们访问服务器打印的 URL，就可以看到应用的运行。

注意，由于缓存，简单的刷新可能无法看到结果。你可能需要按 Shift 强制刷新。

## 9.10 不使用 loader 使用 webpack：webpack.config.js

### 在 Visual Code 中构建

除了从命令行构建，我们也可以在 Visual Code 内部通过所谓的生成任务来实现：

- 从“终端”菜单执行“配置生成任务”。
- 选择“npm: wpw”。
- 问题匹配器处理将工具输出转换为问题列表（信息、警告和错误）。默认处理器在这种情况下效果良好。如果你想显式指定，可以在 .vscode/tasks.json 中指定值：

```json
"problemMatcher": ["$tsc-watch"],
```

现在我们可以通过“运行生成任务”启动 webpack。

与其使用 ts-loader，我们可以先将 TypeScript 文件编译为 JavaScript 文件，然后通过 webpack 将它们打包。这两个步骤中的第一步如何工作，在上一章中描述。

现在我们不需要配置 ts-loader，我们的 webpack 配置文件更加简单：

```javascript
const path = require('path');

module.exports = {
  entry: "./dist/src/main.js",
  output: {
    path: path.join(__dirname, 'build'),
    filename: '[name]-bundle.js',
  },
  plugins: [
    new CopyWebpackPlugin(
      {
        from: './html',
      }
    )
  ]
}
```





# 第 10 章

## 迁移到 TypeScript 的策略

+ 内容
- 10.1 三种策略 ................................................................................ 63
- 10.2 策略：混合 JavaScript/TypeScript 代码库 ............................................ 64
- 10.3 策略：为纯 JavaScript 文件添加类型信息 ............................................ 64
- 10.4 策略：通过快照测试 TypeScript 错误来迁移大型项目 ................................................................................................................................ 65
- 10.5 结论 ....................................................................................................... 65

本章概述了将代码库从 JavaScript 迁移到 TypeScript 的策略。同时也提到了进一步阅读的材料。

## 10.1 三种策略

以下是迁移到 TypeScript 的三种策略：

- 我们可以让代码库支持 JavaScript 和 TypeScript文件的混合。我们从只使用 JavaScript 文件开始，然后逐渐切换到 TypeScript。
- 我们可以保留当前的（非 TypeScript）构建过程和仅限 JavaScript 代码库。我们通过 JSDoc 注释添加静态类型信息，并将 TypeScript 作为类型检查器（而不是编译器）。当所有内容都正确类型化后，我们切换到 TypeScript 进行构建。
- 对于大型项目，迁移过程中可能会产生过多的 TypeScript 错误。快照测试可以帮助我们找到修复的错误和新错误。

更多信息：

- TypeScript 手册中的“从 JavaScript 迁移”

## 10.2 策略：混合 JavaScript/TypeScript 代码库

如果我们使用编译器选项 `--allowJS`，TypeScript 编译器就支持 JavaScript 和 TypeScript 文件的混合：

- TypeScript 文件会被编译。
- JavaScript 文件会被简单地复制到输出目录（在经过一些简单的类型检查之后）。

起初只有 JavaScript 文件。然后，我们一个接一个将文件切换为 TypeScript。在此过程中，我们的代码库一直保持编译状态。

`tsconfig.json` 如下所示：

```json
{
  "compilerOptions": {
    ...
    "allowJS": true
  }
}
```

更多信息：

- Clay Allsopp 写的“增量地将 JavaScript 迁移到 TypeScript”。

## 10.3 策略：为纯 JavaScript 文件添加类型信息

这种方法的工作如下：

- 我们继续使用当前的构建基础设施。
- 我们运行 TypeScript 编译器，但仅作为类型检查器（编译器选项 `--noEmit`）。除了编译器选项 `--allowJS`（允许并复制 JavaScript 文件），我们还必须使用编译器选项 `--checkJS`（用于检查 JavaScript 文件）。
- 我们通过 JSDoc 注释（见下例）和声明文件添加类型信息。
- 一旦 TypeScript 的类型检查器不再报错，我们就使用编译器来构建代码库。现在从 .js 文件切换到 .ts 文件并不紧迫，因为整个代码库已经是静态类型化的。我们现在甚至可以生成类型文件（扩展名为 .ts）。

以下是我们如何通过 JSDoc 注释为纯 JavaScript 指定类型：

```javascript
/**
 * @param {number} x - 第一个操作数
 * @param {number} y - 第二个操作数
 * @returns {number} 两个操作数之和
 */
function add(x, y) {
  return x + y;
}

/** @typedef {prop1: string, prop2: string, prop3: number} SpecialType */
/** @typedef {(data: string, index?: number) => boolean} Predicate */
```

更多信息：

- “为纯 JavaScript 文件使用 TypeScript 编译器”
- Oliver Joseph Ash 写的“我们在 Unsplash 如何逐渐迁移到 TypeScript”

## 10.4 策略：通过快照测试 TypeScript 错误来迁移大型项目

在大型 JavaScript 项目中，无论我们选择哪种方法，切换到 TypeScript 都可能产生过多的错误。这时，对 TypeScript 错误进行快照测试可能选项：

- 我们第一次对整个代码库运行 TypeScript 编译器。
- 编译器产生的错误成为我们的初始快照。
- 当处理代码库时，我们将新的错误输出与之前的快照进行比较：
  - 有时现有的错误会消失。这时我们可以创建一个新的快照。
  - 有时会出现新错误。这时我们要么必须修复这些错误，要么创建一个新的快照。

更多信息：

- Dylan Vann 写的“如何增量地迁移 10 万行代码到 TypeScript”

## 10.5 结论

我们快速查看了迁移到 TypeScript 的策略。还有两点建议：

- 从实验开始迁移：在决定采用某种策略之前，先玩你的代码库并尝试各种策略。
- 然后为以后制定清晰的计划。就优先级问题与你的团队讨论：
  - 有时完全完成迁移可能是优先事项。
  - 有时在迁移期间保持代码完全可用可能更重要。
  - 依此类推……

# 第三部分

# 基础类型

# 第 11 章

# 什么是 TypeScript 中的类型？
两个视角

| 内容 | | |
| :--- | :--- | :--- |
| 11.1 每个视角的三个问题 . . . . . . . . | 69 |
| 11.2 视角 1：类型是值的集合 . . . . . . . . . . | 70 |
| 11.3 视角 2：类型兼容性关系 . . . . . . . . . . . . | 70 |
| 11.4 节点类型系统 vs. 结构化类型系统 . . . . . . . . | 71 |
| 11.5 进一步阅读 . . . . . . . . . . . . . . . . . . . | 72 |

TypeScript 中的类型是什么？本章描述了有助于理解它们的两个视角。

 11.1 每个视角的三个问题

为了理解类型如何工作，需要从两个视角回答以下三个问题：

- 1. 变量拥有 `MyType` 类型意味着什么？
`let myVariable: MyType = /*...*/`
- 2. 可赋值性：如果 `SourceType` 可以赋值给 `TargetType`（A）。
`let source: SourceType = /*...*/`
`let target: TargetType = source; // (A)`
- 3. 如何从 Type1、Type2 和 Type3 推导出 TypeUnion？
`type TypeUnion = Type1 | Type2 | Type3;`

## 11.2 视角 1：类型是值的集合

从这个视角来看，类型是一个值的集合：

- 1. 如果 myVariable 类型为 MyType，这意味着赋值给 myVariable 的值必须是 MyType 集合的元素。
- 2. 如果 SourceType 是 TargetType 的子集，则 SourceType 可以赋值 TargetType。因此，允许 SourceType 的值也允许 TargetType。
- 3. 类型 Type1、Type2 和 Type3 的并是定义它们的集合的集合论并。

## 11.3 视角 2：类型兼容性关系

从这个视角来看，我们不关心值在代码执行时的流动。相反，我们采取更静态的视角：

- 源码拥有位置，每个位置都有静态类型。在感知 TypeScript 的编辑器中，将光标悬停在位置上可以看到其静态类型。
- 当源位置通过赋值、函数调用连接到目标位置时，源位置的类型必须与目标位置的类型兼容。TypeScript 规范通过类型关系定义兼容性。
- 赋值类型关系定义了源类型 S 如何适用于目标类型 T：

  - S 和 T 是相同类型。
  - S 或 T 是 any 类型。
  - 等。

- 1. 变量的静态类型决定了可以给它的什么。这始终取决于静态类型。例如，在函数调用 `toString(123)` 中，123 的静态类型必须赋值给 `toString()` 参数的静态类型。
- 2. 如果 myVariable 的类型可赋值给 MyType，则 myVariable 拥有 MyType 类型。
- 3. 如果 SourceType 和 TargetType 之间存在赋值兼容，则 SourceType 可赋值给 TargetType。
- 4. 并集的工作方式是通过其类型关系的可见成员定义的。

TypeScript 类型系统的一个有趣特性是，同一个变量在不同位置可以有不同的类型：

```javascript
// %inferred-type: any[]
const arr = [];

arr.push(123);
```





## 11.4 命名类型系统 vs. 结构类型系统

```typescript
// // %inferred-type: number[]
arr;

arr.push('abc');
// %inferred-type: (string | number)[]
arr;
```

静态类型系统的职责之一是确定两个静态类型是否兼容：

- 实际参数的静态类型 `Src`（例如，通过函数调用提供）
- 对应的形式参数的静态类型 `Trg`（例如，在函数定义中指定）

这通常意味着检查 `Src` 是否是 `Trg` 的子类型。这种检查有两种处理方法（大致如下）：

- 在命名（nominal）或指定（nominative）类型系统中，如果两个静态类型具有相同的标识（“名称”），它们就是相等的。如果类型关系是显式定义的，则一个类型是另一个类型的子类型。
- 具有命名类型的语言有 C++、Java、C#、Swift 和 Rust。
- 在结构（structural）类型系统中，如果两个静态类型具有相同的结构（如果它们的各个具有相同的名称和类型），它们就是相等的。如果 `Sup` 的所有部分（可能还有其他部分）以及 `Sub` 的每个部分都是 `Sup` 对应部分的子类型，则 `Sub` 是 `Sup` 的子类型。
- 具有结构类型化的语言有 OCaml/ReasonML 和 TypeScript。

以下代码在命名类型系统下会在 A 行产生类型错误，但在 TypeScript 的结构类型系统中是合法的，因为类 A 和类 B 具有相同的结构：

```typescript
class A {
  name = 'A';
}
class B {
  name = 'B';
}
const someVariable:A = new B(); // (A)
```

TypeScript 的接口也是结构化工作的——它们不需要实现就可以匹配：

```typescript
interface Point {
  x: number;
  y: number;
}
const point: Point = {x: 1, y: 2}; // OK
```

## 11.5 扩展阅读

- TypeScript Handbook 中的“类型兼容”（Type Compatibility）章节
- TypeScript 规范中的“类型关系”（Type Relationships）章节

# 第 12 章

### 顶类型 any 和 unknown

| 内容 | 页码 |
| :--- | :--- |
| 12.1 TypeScript 的两个顶类型 | 73 |
| 12.2 顶类型 any | 73 |
| 12.2.1 示例：JSON.parse() | 74 |
| 12.2.2 示例：String() | 74 |
| 12.3 顶类型 unknown | 74 |

在 TypeScript 中，`any` 和 `unknown` 是包含所有值的类型。在本章中，我们将研究它们是什么以及有什么用途。

## 12.1 TypeScript 的两个顶类型

`any` 和 `unknown` 是 TypeScript 中所谓的*顶类型*（top types）。引用维基百科的话：

> 顶类型 [...] 是通用类型，有时被称为*通用超类型*（universal supertype），因为任何给定系统中的所有其他类型都是子类型 [...]。在大多数情况下，它是感兴趣的类型系统中包含每个可能的[值]的类型。

也就是说，当类型视为值的集合时（关于类型的更多信息，请参阅 §11 “什么是 TypeScript 中的类型？两种视角”），`any` 和 `unknown` 是包含所有值的集合。顺便提一下，TypeScript 还有*底类型*（bottom type）`never`，它是空集。

## 12.2 顶类型 any

如果一个值是 `any`，我们可以对它做任何事情：

```typescript
function func(value: any) {
  // 仅允许数字，但它们是 `any` 的子类型
  5 * value;

  // 通常，value 的类型签名必须包含 .propName
  value.propName;

  // 通常只允许数组和具有索引签名的类型
  value[123];
}
```

任何类型都可以赋值给 `any`：

```typescript
let storageLocation: any;

storageLocation = null;
storageLocation = true;
storageLocation = {};
```

任何类型都可以被赋值为：

```typescript
function func(value: any) {
  const a: null = value;
  const b: boolean = value;
  const c: object = value;
}
```

TypeScript 的类型系统通常给了我们这种保护。因此，如果我们无法使用更具体的类型或 `unknown`，则应将其作为最后的手段。

### 12.2.1 示例：JSON.parse()

`JSON.parse()` 的结果取决于动态输入，这就是为什么返回类型是 `any`（在 `unknown` 类型出现之前）。否则，返回类型可能是 `unknown`。

```typescript
JSON.parse(text: string): any;
```

### 12.2.2 示例：String()

`String()` 函数将任意值转换为字符串，具有如下签名：

```typescript
interface String {
  (value?: any): string; // 调用
}
```

## 12.3 顶类型 unknown

`unknown` 是 `any` 的类型安全版本。`any` 允许我们做任何事情，而 `unknown` 要严格得多。在我们对 `unknown` 类型的值执行操作之前，我们必须通过以下方式缩小它们的类型：

- 类型断言：
```typescript
function func(value: unknown) {
  // @ts-expect-error: Object is of type 'unknown'
  value.toFixed(2);

  // 类型断言:
  (value as number).toFixed(2); // OK
}
```
- 等于：
```typescript
function func(value: unknown) {
  // @ts-expect-error: Object is of type 'unknown'
  value * 5;

  if (value === 123) { // 等于
    // .inferred-type: 123
    value;

    value * 5; // OK
  }
}
```
- 类型守卫：
```typescript
function func(value: unknown) {
  // @ts-expect-error: Object is of type 'unknown'
  value.length;

  if (typeof value === 'string') { // 类型守卫
    // .inferred-type: string
    value;

    value.length; // OK
  }
}
```
- 断言函数：
```typescript
function func(value: unknown) {
  // @ts-expect-error: Object is of type 'unknown'
  value.test('abc');

  assertIsRegExp(value);

  // .inferred-type: RegExp
  value;

  value.test('abc'); // OK
}

/** 断言函数 */
function assertIsRegExp(arg: unknown): asserts is RegExp {
  if (!(arg instanceof RegExp)) {
    throw new TypeError('Not a RegExp: ' + arg);
  }
}
```

## 第 13 章

### TypeScript 枚举：它们是如何工作的？有什么用？

- 内容
  13.1 基础 ..................................................................................................................... 78
  13.1.1 数字枚举 ................................................................................................................... 78
  13.1.2 基于字符串的枚举 ................................................................................................................ 79
  13.1.3 异构枚举 ............................................................................................................. 79
  13.1.4 省略初始化器 ............................................................................................ 79
  13.1.5 枚举名称的大小写 .......................................................................................... 80
  13.1.6 枚举名称的引号 ................................................................................ 80
  13.2 指定枚举值（高级） .......................................................................... 80
  13.2.1 字面量枚举 ................................................................................................................. 81
  13.2.2 常量枚举 ................................................................................................... 81
  13.2.3 计算属性枚举 ................................................................................................................. 82
  13.3 数字枚举的缺点 ................................................................................................ 83
  13.3.1 缺点：日志 ............................................................................................................ 83
  13.3.2 缺点：松散类型检查 ............................................................................ 83
  13.3.3 建议：优先使用字符串的枚举 ................................................................ 83
  13.4 枚举的用例 ............................................................................................ 84
  13.4.1 用例：位模式 ................................................................................................... 84
  13.4.2 用例：多个常量 ........................................................................................ 85
  13.4.3 用例：比布尔更具自描述性 ........................................................ 86
  13.4.4 用例：更好的字符串常量 ................................................................................. 87
  13.5 运行时的枚举 ............................................................................... 88
  13.5.1 反向映射 ............................................................................................................ 88
  13.5.2 运行时基于字符串的枚举 ....................................................................... 89
  13.6 const 枚举 ...................................................................................................... 89
  13.6.1 编译非 const 枚 ...................................................................................... 89
  13.6.2 编译 const 枚 ............................................................................................ 90





# 13 TypeScript 举：它们是如何工作的？可以有什么用途？

- 13.7 编译时的枚举 . . . . . . . . . . . . . . . . . . 91
- 13.7.1 枚举是对象 . . . . . . . . . . . . . . . . . . . . . 91
- 13.7.2 字面量枚举的安全检查 . . . . . . . . . . . . . . . . . . . 91
- 13.7.3 keyof 与枚举 . . . . . . . . . . . . . . . . . . . . . . 94
- 13.8 鸣谢 . . . . . . . . . . 94

本章回答了以下问题：

- TypeScript 的枚举是如何工作的？
- 它们可以用于什么场景？

在下一章中，我们将看看枚举的替代方案。

## 13.1 基础

`boolean` 是一个具有有限值的类型：`false` 和 `true`。通过枚举，TypeScript 允许我们自己定义类似的类型。

### 13.1.1 数字枚举

这是一个数字型的 NoYes：

```typescript
enum NoYes {
  No = 0,
  Yes = 1, // 尾随逗号
}
```

```typescript
assert.equal(NoYes.No, 0);
assert.equal(NoYes.Yes, 1);
```

解释：

- 条目 `No` 和 `Yes` 被称为枚举 `NoYes` 的成员（members）。
- 每个枚举成员都有一个名称和一个值。例如，第一个成员的名称为 `No`，值为 `0`。
- 成员定义中以等号开头并指定值的称为初始化器（initializer）。
- 与对象字面量一样，允许使用尾随逗号且会被忽略。

我们可以像使用字面量（`true`、`123` 或 `'abc'`）一样使用这些成员——例如：

```typescript
function toGerman(value: NoYes) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
  }
}
```

```typescript
assert.equal(toGerman(NoYes.No), 'Nein');
assert.equal(toGerman(NoYes.Yes), 'Ja');
```

### 13.1.2 基于字符串的枚举

除了数字，我们还可以使用字符串作为枚举成员的值：

```typescript
enum NoYes {
  No = 'No',
  Yes = 'Yes',
}

assert.equal(NoYes.No, 'No');
assert.equal(NoYes.Yes, 'Yes');
```

### 13.1.3 异构枚举

最后一种枚举被称为异构枚举（heterogeneous）。异构枚举的成员值是数字和字符串的混合：

```typescript
enum Enum {
  One = 'One',
  Two = 'Two',
  Three = 3,
  Four = 4,
}
assert.deepEqual(
  [Enum.One, Enum.Two, Enum.Three, Enum.Four],
  ['One', 'Two', 3, 4]
);
```

异构枚举并不经常使用，因为它们的应用场景很少。
遗憾的是，TypeScript 仅支持数字和字符串作为枚举成员的值。其他值（如 `symbol`）是不允许的。

### 13.1.4 省略初始化器

我们可以在两种情况下省略初始化器：

- 可以省略第一个成员的初始化器。那么该成员的值为 `0`（零）。
- 如果上一个成员具有数字值，可以省略当前成员的初始化器。那么当前成员的值为该值加一。

这是一个没有任何初始化器的数字枚举：

```typescript
enum NoYes {
  No,
  Yes,
}
assert.equal(NoYes.No, 0);
assert.equal(NoYes.Yes, 1);
```

这是一个省略了部分初始化器的异构枚举：

```typescript
enum Enum {
  A,
  B,
  C = 'C',
  D = 'D',
  E = 8, // (A)
  F,
}
assert.deepEqual(
  [Enum.A, Enum.B, Enum.C, Enum.D, Enum.E, Enum.F],
  [0, 1, 'C', 'D', 8, 9]
);
```

注意，`A` 行没有省略初始化器，是因为前一个成员的值不是数字。

### 13.1.5 枚举成员的命名

枚举成员命名有几种先例：

- 传统上，JavaScript 使用全大写命名，继承自 Java 和 C：
  - `Number.MAX_VALUE`
  - `Math.SQRT2`
- 著名的符号使用驼峰命名，因为它们与属性相关：
  - `Symbol.asyncIterator`
- TypeScript 手档使用以大字母开头的驼峰命名。这用于 `NoYes` 枚举。

### 13.1.6 举成员名称

类似于 JavaScript 对象，我们可以为枚举成员加引号：

```typescript
enum HttpIntegerField {
  'Accept',
  'Accept-Charset',
  'Accept-Datetime',
  'Accept-Encoding',
  'Accept-Language'
}
assert.equal(HttpIntegerField['Accept-Charset'], 1);
```

没有计算枚举名称的方法。对象字面量通过括号支持计算键。

## 13.2 指定枚举值（高级）

TypeScript 通过初始化方式区分了三种枚举成员：

- 字面量枚举成员：
  - 可能没有初始化器
  - 或者通过数字字面量初始化
  - 通过字符串字面量初始化

- 常量枚举成员：
  - 它的值在编译时计算。因此，我们可以隐式地指定它（即让 TypeScript 为我们指定）。我们可以显式指定并允许以下语法：
    - 数字字面量或字符串字面量
    - 对之前定义的枚举的引用（在当前枚举或之前的枚举中）
    - 一元运算符 `+`、`~`
    - 二进制运算符 `*`、`%`、`<<`、`>>>`

这是一个成员均为常量枚举示例（稍后我们将看到如何用法）：

```typescript
enum Perm {
  UserRead = 1 << 8,
  UserWrite = 1 << 7,
  UserExecute = 1 << 6,
  GroupRead = 1 << 5,
  GroupWrite = 1 << 4,
  GroupExecute = 1 << 3,
  AllRead = 1 << 2,
  AllWrite = 1 << 1,
  AllExecute = 1 << 0
}
```

通常，常量成员不能用作类型。然而，仍然会进行完尽性检查。

### 13.2.3 计算枚举成员

计算成员的值可以通过任意表达式指定。例如：

```typescript
enum NoYesNum {
  No = 123,
  Yes = Math.random(), // OK
}
```

这是一个数字枚举。字符串枚举和异构枚举的限制更多。例如，我们不能使用方法调用来指定成员值：

```typescript
enum NoYesStr {
  No = 'No',
  // @ts-expect-error: 字符串值成员的枚举不允许计算值。
  Yes = ['Y', 'e', 's'].join('')
}
```

TypeScript 不对计算成员进行完尽性检查。

## 13.3 数字枚举的缺点

### 13.3.1 缺点：日志

当记录数字枚举成员时，我们只能看到数字：

```typescript
enum NoYes { No, Yes }

console.log(NoYes.No);
console.log(NoYes.Yes);

// 输出：
// 0
// 1
```

### 13.3.2 缺点：类型检查宽松

当用枚举作为类型时，静态允许的值不仅是枚举成员的值——任何数字都被接受：

```typescript
enum NoYes { No, Yes }
function func(no: NoYes) {}
func(33); // 无错误！
```

为什么没有静态检查？Daniel Rosenberg 解释道：

> 这种行为的动机是位运算。某些情况下，`SomeFlag.Foo | SomeFlag.Bar` 旨在产生另一个 `SomeFlag`。相反，你将其与数字配合，而不需要转换回 `SomeFlag`。

我想如果我们再次使用 TypeScript 并且仍然有枚举，我们会为位标志（bit flags）创建一个单独结构。

枚举如何用于位模式很快就会详细演示。

### 13.3.3 建议：倾向于基于字符串的枚举

我的建议是倾向于基于字符串的枚举（为了简洁起见，本章不允许此建议）：

```typescript
enum NoYes { No='No', Yes='Yes' }
```

一方面，日志输出对人类更有用：

```typescript
console.log(NoYes.No);
console.log(NoYes.Yes);

// 输出：
// 'No'
// 'Yes'
```

另一方面，我们得到了更严格的类型检查：





## 13 TypeScript 枚举（enums）：它们是如何工作的？可以有什么用途？

```typescript
function func(noYes: NoYes) {}
```

```typescript
// @ts-expect-error: Argument of type "abc" is not assignable
// to parameter of type 'NoYes'.
func('abc');

// @ts-expect-error: Argument of type "Yes" is not assignable
// to parameter of type 'NoYes'.
func('Yes'); // (A)
```

即使是与成员值相同的字符串也不允许（行 A）。

## 13.4 枚举的用例

### 13.4.1 用例：文件系统模块

在 Node.js 的文件系统模块中，有几个函数带有 `mode` 参数。它通过数值编码来指定文件权限，这是 Unix 的遗留：

- 权限允许适用于三类用户：
  - 用户（User）：文件的所有者
  - 组（Group）：与文件关联的组的成员
  - 所有（All）：所有人

- 对于每个类别，可以授予以下权限：
  - r（读）：允许该类用户读取文件
  - w（写）：允许该类用户修改文件
  - x（执行）：允许该类用户运行文件

这意味着权限可以用 9 位表示（3 类用户，每类 3 种权限）：

| 用户 | 组 | 所有 |
| :--- | :--- | :--- |
| 权限 r, w, x | r, w, x | r, w, x |
| 位 8, 7, 6 | 5, 4, 3 | 2, 1, 0 |

Node.js 并没有这样做，但我们可以使用枚举来处理这些标记：

```typescript
enum Perm {
  UserRead = 1 << 8, //第 8 位
  UserWrite = 1 << 7,
  UserExecute = 1 << 6,
  GroupRead = 1 << 5,
  GroupWrite = 1 << 4,
  GroupExecute = 1 << 3,
  AllRead = 1 << 2,
  AllWrite = 1 << 1,
  AllExecute = 1 << 0,
}
```

位模式通过按位或（Or）组合：

```typescript
// 用户可以修改、读取和执行。
// 所有人只能读取和执行。
assert.equal(
  Perm.UserRead | Perm.UserWrite | Perm.UserExecute |
  Perm.GroupRead | Perm.GroupExecute |
  Perm.AllRead | Perm.AllExecute,
  00755
);

// 用户可以读取和写入。
// 组成员可以读取。
// 所有人完全无法访问。
assert.equal(
  Perm.UserRead | Perm.UserWrite | Perm.GroupRead,
  00640
);
```

### 13.4.1.1 位模式的替代方案

位模式背后的核心思想是一组标记，并且可以选择标记的任何子集。

因此，使用集合（sets）来选择子集是执行相同任务更直接的方法：

```typescript
enum Perm {
  UserRead = 'UserRead',
  UserWrite = 'UserWrite',
  UserExecute = 'UserExecute',
  GroupRead = 'GroupRead',
  GroupWrite = 'GroupWrite',
  GroupExecute = 'GroupExecute',
  AllRead = 'AllRead',
  AllWrite = 'AllWrite',
  AllExecute = 'AllExecute'
}
function writeFileSync(
  thePath: string, permissions: Set<Perm>, content: string) {
  // ...
}

writeFileSync(
  '/tmp/hello.txt',
  new Set([Perm.UserRead, Perm.UserWrite, Perm.GroupRead]),
  'Hello!'
);
```

### 13.4.2 用例：多个常量

有时我们有一组在一起的常量：

```typescript
const off = 'off';
const info = 'info';
const warn = 'warn';
const error = 'error';
```

这是一个使用枚举的好用例：

```typescript
enum LogLevel {
    off = 'off',
    info = 'info',
    warn = 'warn',
    error = 'error'
}
```

枚举的一个优点是常量名被分组在 `LogLevel` 命名空间内。另一个优点是自动为它们获取 `LogLevel` 类型。如果我们想为这些常量获取这种类型，还需要更多工作：

```typescript
type LogLevel =
    | typeof off
    | typeof info
    | typeof warn
    | typeof error
```

关于这种方法的更多信息，请参阅 §14.1.3 “单例联合类型”。

### 13.4.3 用例：比布尔值更具自描述性

### 13.4.3.1 布尔值示例：有序 vs 无序

例如，为了表示列表是否是有序的，我们可以使用布尔值：

```typescript
class List1 {
    isSelected: boolean;
    // ...
}
```

然而，枚举通常更具自描述性，并且如果需要，我们可以添加更多选项。

```typescript
enum ListKind {
    ordered, unordered
}
class List2 {
    listKind: ListKind;
    // ...
}
```

### 13.4.3.2 布尔值示例：错误处理

同样，我们可以通过布尔值指定如何处理错误：

```typescript
function convertToHtml(markdown: string, throwOnError: boolean) {
  // ...
}
```

或者我们可以通过枚举值来实现：

```typescript
enum ErrorHandling {
  throwOnError = 'throwOnError',
  showErrorsInContent = 'showErrorsInContent'
}
function convertToHtml2(markdown: string, errorHandling: ErrorHandling) {
  // ...
}
```

### 13.4.4 用例：更好的字符串常量

考虑以下创建正则表达式的函数：

```typescript
const GLOBAL = 'g';
const NOT_GLOBAL = '';
type Globalness = typeof GLOBAL | typeof NOT_GLOBAL;
```

```typescript
function createRegExp(source: string,
  globalness: Globalness = NOT_GLOBAL) {
  return new RegExp(source, 'u' + globalness);
}
```

```typescript
assert.deepEqual(
  createRegExp('abc', GLOBAL),
  /abc/ug
);
```

```typescript
assert.deepEqual(
  createRegExp('abc', 'g'), // OK
  /abc/ug
);
```

我们可以使用枚举代替字符串常量：

```typescript
enum Globalness {
  Global = 'g',
  notGlobal = '',
}
```

```typescript
function createRegExp(source: string, globalness = Globalness.notGlobal) {
  return new RegExp(source, 'u' + globalness);
}
```

```typescript
assert.deepEqual(
  createRegExp('abc', Globalness.Global),
  /abc/ug
);
```

```typescript
assert.deepEqual(
  // ts-expect-error: Argument of type "g" is not assignable to parameter of type 'Global'
  createRegExp('abc', 'g'), // 
  /abc/ug
);
```

这种方法有什么好处？

- 它更简洁。
- 它稍微安全。

## 13.5 运行时的枚举

给定一个数值枚举，如下：

```typescript
enum NoYes {
  No,
  Yes
}
```

TypeScript 将其编译为：

```javascript
var NoYes;
(function (NoYes) {
  NoYes[0] = "No";
  NoYes[1] = "Yes";
})(NoYes || {});
```

数值枚举还支持从成员名到值的反向映射：

```typescript
function getQualifiedName(value: NoYes) {
  return 'NoYes.' + value;
}
assert.equal(getQualifiedName(NoYes.Yes), 'NoYes.1');
```

动态查找：

```typescript
assert.equal(NoYes[1], 'Yes');
```

### 13.5 运行时的字符串基枚举

考虑以下枚举：

```typescript
enum NoYes {
  No = 'NO!',
  Yes = 'YES!'
}
```

它被编译为这段代码：

```javascript
var NoYes;
(function (NoYes) {
  NoYes['No'] = "NO!";
  NoYes['Yes'] = "YES!";
})((NoYes = {}));
```

TypeScript 不支持字符串基枚举的反向映射。

## 13.6 const 枚举

如果枚举以关键字 `const`开头，它在运行时没有表示。相反，其成员的值会被直接使用。

### 13.6.1 编译非 const 枚举

为了观察这种效果，让我们检查以下非 const 枚举：

```typescript
enum NoYes {
  No = 'No',
  Yes = 'Yes',
}
```

```typescript
function toGerman(value: NoYes) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
  }
}
```

TypeScript 严格将此代码编译为：

```javascript
"use strict";
var NoYes;
(function (NoYes) {
  NoYes["No"] = "No";
  NoYes["Yes"] = "Yes";
})(NoYes || (NoYes = {}));
```

```typescript
function toGerman(value) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
  }
}
```

### 13.6.2 编译 const enum

这与之前的代码相同，但现在枚举是 const：

```typescript
const enum NoYes {
  No,
  Yes,
}
```

```typescript
function toGerman(value: NoYes) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
  }
}
```

现在枚举作为构造的消失了，只剩下其成员的值：

```typescript
function toGerman(value) {
  switch (value) {
```





## 13.7 编译时的枚举

```typescript
case "No" /* No * */
  return 'Nein';
case "Yes" /* Yes * */
  return 'Ja';
```

### 13.7.1 枚举是对象

TypeScript 将（非常量）枚举视为对象处理：

```typescript
enum NoYes {
  No = 'No',
  Yes = 'Yes',
}
function func(obj: { No: string }) {
  return obj.No;
}
assert.equal(
  func(NoYes), // 静态上允许的！
  'No');
```

## 13.7.2 字面量枚举的安全性检查

当接收一个枚举成员值时，我们通常希望确保：

- 我们没有接收到非法值。
- 我们没有遗漏考虑任何枚举成员值。如果以后以后添加了成员，这一点尤为重要。

继续阅读以获取更多信息。我们将使用以下枚举工作：

```typescript
enum NoYes {
  No = 'No',
  Yes = 'Yes',
}
```

### 13.7.2.1 防止非法值

在下面的代码中，我们针对非法值采取了两种措施：

```typescript
function toGerman(value: NoYes) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
    default:
      throw new TypeError('Unsupported value: ' + JSON.stringify(value));
  }
}

assert.throws(
  // @ts-expect-error: 类型为 'Maybe' 的参数无法赋值给
  // 类型为 'NoYes' 的参数
  () => toGerman('Maybe'),
  // TypeError: Unsupported value: "Maybe"
);
```

措施如下：

- 在编译时，NoYes 防止了非法值被传递给参数。
- 在运行时，如果出现意外值，则使用 `default` 分支抛出异常。

### 13.7.2.2 通过穷尽性检查防止遗漏的情况

我们可以再采取一种措施。下面的代码执行了穷尽性检查：如果我们忘记考虑所有成员，TypeScript 将告警告我们。

```typescript
class UnsupportedValueError extends Error {
  constructor(value: never) {
    super('Unsupported value: ' + value);
  }
}
```

```typescript
function toGerman2(value: NoYes) {
  switch (value) {
    case NoYes.No:
      return 'Nein';
    case NoYes.Yes:
      return 'Ja';
    default:
      throw new UnsupportedValueError(value);
  }
}
```

穷尽性检查是如何运作的？对于每一个 `case`，TypeScript 都会推导出值的类型：

```typescript
function toGerman2b(value: NoYes) {
  switch (value) {
    case NoYes.No:
      // 推断的类型: NoYes.No
      value;
      return 'Nein';
    case NoYes.Yes:
      // 推断的类型: NoYes.Yes
      value;
      return 'Ja';
  }
}
```

```typescript
default:
  // 推断的类型: never
  value;
  throw new UnsupportedValueError(value);
```

在 `default` 分支中，TypeScript 将 `value` 的类型推断为 `never`，因为我们永远不会那里。如果我们在 NoYes 中添加了成员 `.Maybe`，那么 `value` 的推断类型就是 `NoYes.Maybe`，这与 `new UnsupportedValueError()` 参数的类型 `never` 在静态上是不兼容的。这就是我们在编译时得到以下错误信息的原因：

类型 'NoYes.Maybe' 的参数无法赋值给类型为 'never' 的参数。

方便的是，这种穷尽性检查也适用于 `if` 语句：

```typescript
function toGerman3(value: NoYes) {
  if (value === NoYes.No) {
    return 'Nein';
  } else if (value === NoYes.Yes) {
    return 'Ja';
  } else {
    throw new UnsupportedValueError(value);
  }
}
```

### 13.7.2.3 检查穷尽性的另一种方法

或者，我们可以通过指定返回值来获取穷尽性检查：

```typescript
function toGerman4(value: NoYes): string {
  switch (value) {
    case NoYes.No:
      const x: NoYes.No = value;
      return 'Nein';
    case NoYes.Yes:
      const y: NoYes.Yes = value;
      return 'Ja';
  }
}
```

如果我们在 NoYes 中添加一个成员，TypeScript 就会抱怨 `toGerman4()` 可能会返回 `undefined`。

#### 这种方法的缺点：

- 此方法不适用于 `if` 语句（更多信息）。
- 运行时不进行任何检查。

## 13.7.3 keyof 和枚举

我们可以使用 `keyof` 操作符来创建一个类型，其元素是枚举成员的键名。当我们这样做时，需要将 `keyof` 与 `typeof` 结合：

```typescript
enum HttpRequestKey {
  'Accept',
  'Accept-Charset',
  'Accept-Datetime',
  'Accept-Encoding',
  'Accept-Language'
}
// 推断的类型: "Accept" | "Accept-Charset" | "Accept-Datetime" |
// "Accept-Language"
type HttpRequestKeyType = keyof typeof HttpRequestKey;
```

```typescript
function getTypeValue(request: Request, key: HttpRequestKey) {
```





## 14.1 单例值的联合类型

```typescript
assert.equal(toGerman1(NoYesEnum.No), 'Nein');
assert.equal(toGerman1(NoYesEnum.Yes), 'Ja');
```

NoYesStrings 是 NoYesEnum 的类型版本：

```typescript
type NoYesStrings = 'No' | 'Yes';
```

```typescript
function toGerman2(value: NoYesStrings): string {
  switch (value) {
    case 'No':
      return 'Nein';
    case 'Yes':
      return 'Ja';
  }
}
assert.equal(toGerman2('No'), 'Nein');
assert.equal(toGerman2('Yes'), 'Ja')
```

类型 NoYesStrings 是字符串字面量 'No' 和 'Yes' 的联合类型。类型运算符 `|` 与集合论中的并运算符 `∪` 相关。

### 14.1.2.1 字符串字面量类型的联合可以进行穷尽性检查

以下代码演示了字符串字面量类型联合类型的穷尽性检查：

```typescript
// @ts-expect-error: 函数缺少结束返回语句
// 返回类型不包含 'undefined'。(2366)
function toGerman3(value: NoYesStrings): string {
  switch (value) {
    case 'Yes':
      return 'Ja';
  }
}
```

我们忘记了 'No' 的情况，TypeScript 警告我们该函数可能返回非字符串的类型。

我们可以更显式地进行穷尽性检查：

```typescript
class UnsupportedValueError extends Error {
  constructor(value: never) {
    super('Unsupported value: ' + value);
  }
}
```

```typescript
function toGerman4(value: NoYesStrings): string {
  switch (value) {
    case 'Yes':
      return 'Ja';
    default:
      // @ts-expect-error: 类型 "No" 的参数不能
      // 赋值给类型 'never' 的参数。(2345)
      throw new UnsupportedError(value);
  }
}
```

现在 TypeScript 警告我们，如果 value 为 'No'，将会进入 default 分支。

## 关于穷尽性检查的更多信息

有关此主题的更多信息，请参阅 §13.7.2.2 '通过穷尽性检查防止遗漏情况'。

### 14.1.2.2 缺点：字符串字面量联合的类型安全性较低

字符串字面量的一个缺点是，非成员值会被误认为是成员：

```typescript
type Spanish = 'no' | 'si';
type English = 'no' | 'yes';

const spanishWord: Spanish = 'no';
const englishWord: English = spanishWord;
```

这是逻辑上的，因为西班牙语的 'no' 和英语的 'no' 是同一个值。实际的问题是没有方法为它们赋予不同的标识。

## 14.1.3 符号单例类型的联合类型

### 14.1.3.1 示例：LogLevel

除了字符串字面量的联合，我们也可以使用符号单例类型的联合。这次我们换一个不同的枚举：

```typescript
enum LogLevel {
  off = 'off',
  info = 'info',
  warn = 'warn',
  error = 'error'
}
```

转换为符号单例类型的联合后，如下：

```typescript
const off = Symbol('off');
const info = Symbol('info');
const warn = Symbol('warn');
const error = Symbol('error');
```

```typescript
// %inferred-type: unique symbol | unique symbol |
// unique symbol | unique symbol
type LogLevel =
  | typeof off
  | typeof info
  | typeof warn
  | typeof error;
```

为什么我们这里需要 `typeof`？`off` 等是值，不能出现在类型等式中。类型运算符 `typeof` 通过将值转换为类型来解决这个问题。

让我们考虑之前示例的两个变体。

### 14.1.3.2 变体 #1：内联符号

我们可以内联符号（而不是引用单独的 const 声明）吗？遗憾的是，类型运算符 `typeof` 的操作数必须是一个标识符或由点分隔的标识符“路径”。因此，这种语法是违法的：

```typescript
type LogLevel = Symbol('off') | ...
```

### 14.1.3.3 变体 #2：使用替 const

我们可以使用 `let` 代替 `const` 来创建变量吗？（这不一定是改进，但这是一个非常有趣的问题。）

我们不能，因为我们需要 TypeScript 为 `const` 声明的变量推断出的更窄类型：

```typescript
// inferred-type: unique symbol
const constSymbol = Symbol('constSymbol');
```

```typescript
// inferred-type: symbol
let letSymbol = Symbol('letSymbol');
```

如果使用 `let`，LogLevel 将仅仅拥有 symbol 的一个别名。`const` 断言通常可以解决这类问题，但它们在此种情况下不起作用：

```typescript
// ts-expect-error: 'const' 断言只能应用于枚举成员的引用，
// 或字符串、数字、布尔值、数组或对象字面量。(1355)
let letSymbol2 = Symbol('letSymbol2') as const;
```

### 14.1.3.4 在函数中使用 LogLevel

以下函数将 LogLevel 的成员转换为字符串：

```typescript
function getName(loglevel: LogLevel): string {
  switch (loglevel) {
    case off:
      return 'off';
    case info:
      return 'info';
    case warn:
      return 'warn';
    case error:
      return 'error';
  }
}
```

## 14.1.3.5 符号类型联合与字符串字面量

这两种方法有什么区别？

- 使用符号更冗长。
- 穷尽性检查均有效。
- 使用字符串字面量更简洁。
- 这是使用字符串字面量的示例：
- 穷尽性检查均有效。

## 14.2 辨析联合

为了理解它们如何工作，请考虑表示的数据结构。后续步骤：

- 1. 我们首先创建一个面向对象的类层次。
- 2. 然后将其转换为更具函数式的形式。
- 3. 最后，我们得到辨析联合。

### 14.2.1 步骤 1：作为类层次的语法树

这是语法树典型的面向对象实现：

```typescript
abstract class SyntaxTree {}
class NumberValue extends SyntaxTree {
  constructor(public numberValue: number) {
    super();
  }
}
class Addition extends SyntaxTree {
  constructor(public operand1: SyntaxTree, public operand2: SyntaxTree) {
    super();
  }
}
```

SyntaxTree 是 NumberValue 和 Addition 的父类。`public` 关键字是通过参数声明实例属性的语法糖。

这是使用 SyntaxTree 的示例：

```typescript
const tree = new Addition(
  new NumberValue(1),
  new Addition(
    new NumberValue(2),
    new NumberValue(3), // 尾逗号
  ),
);
```

注意：JavaScript 从 2016 年开始允许参数列表中存在尾逗号。

### 14.2.2 步骤 2：作为类联合的语法树

如果我们将语法树定义为联合类型（A A），不需要面向对象的继承：

```typescript
class NumberValue {
  constructor(public numberValue: number) {}
}
class Addition2 {
  constructor(public operand1: SyntaxTree, public operand2: SyntaxTree) {}
}
type SyntaxTree2 = NumberValue | Addition2; // (A)
```

由于 NumberValue 和 Addition2 没有父类，它们不需要在构造函数中调用 `super()`。

### 14.2.3 步骤 3：作为辨析联合的语法树

这些是 SyntaxTree3 的类型定义：

```typescript
interface NumberValue {
  kind: 'number-value';
  numberValue: number;
}
interface Addition3 {
  kind: 'addition';
}
```




## 14.2 判别联合 (Discriminated unions)

```typescript
operand1: SyntaxTree;
operand2: SyntaxTree;
}
type SyntaxTree = NumberValue3 | Addition;
```

我们已经从类切换到了接口，因此从类实例切换到了普通对象。

判别联合的接口必须至少有一个共同属性，且该属性对于每个成员来说必须具有不同的值。该属性被称为判别器（discriminant）或标记（tag）。`SyntaxTree` 的判别器是 `.kind`。它的类型是字符串字面量类型。

对比一下：

- 实例的直接类由其原型（prototype）决定。
- 判别联合中成员的类型由其判别器决定。

这是一个匹配 `SyntaxTree3` 的对象：

```typescript
const tree: SyntaxTree3 = { // (A)
  kind: 'addition',
  operand1: {
    kind: 'number-value',
    numberValue: 1,
  },
  operand2: {
    kind: 'addition',
    operand1: {
      kind: 'number-value',
      numberValue: 2,
    },
    operand2: {
      kind: 'number-value',
      numberValue: 3,
    }
  }
};
```

我们不需要在 A 行中进行类型注解，但它有助于确保数据具有正确的结构。如果我们不在在这里写，我们将在稍后发现问题。

在接下来的示例中，`tree` 的类型是一个判别联合。每当我们检查它的判别器（C 行）时，TypeScript 都会相应地更新其静态类型：

```typescript
function getNumberValue(tree: SyntaxTree3) {
  // %inferred-type: SyntaxTree3
  tree; // (A)

  // @ts-error: Property 'numberValue' 不存在于类型 'SyntaxTree3' 上。
  // Property 'numberValue' 不存在于类型 'Addition3' 上。(2339)
  tree.numberValue; // (B)
}
```

## 14 TypeScript 中枚举的替代方案

```typescript
if (tree.kind === 'number-value') { // (C)
  // %inferred-type: NumberValue3
  tree;
  return tree.numberValue; // OK!
}
return null;
```

在 A 行中，我们还没有检查判别器 `.kind`。因此，`tree` 的当前类型仍然是 `SyntaxTree`，我们无法在 B 行中访问属性 `.numberValue`（因为联合中只有一个成员拥有此属性）。

在 D 行中，TypeScript 知道 `.kind` 是 'number-value'，因此可以推出 `tree` 的类型为 `NumberValue3`。这就是为什么在下一行访问 `.numberValue` 是允许的。

### 14.2.3.1 为判别联合实现函数

我们通过一个为判别联合实现函数的示例来结束这一步。

如果有一个适用于所有子类型成员的操作，类和判别联合的方法有所不同：

- 面向对象的方法：使用类时，通常使用多态方法，每个类都有不同的实现。通常会使用单个函数来处理所有可能的情况，并通过检查其参数的判别器来决定执行什么。
- 函数式方法：

下面的示例演示了函数式方法。在 A 行中检查判别器，并决定执行哪两个 `switch` 分例。

```typescript
function syntaxTreeToString(tree: SyntaxTree): string {
  switch (tree.kind) { // (A)
    case 'addition':
      return syntaxTreeToString(tree.operand1)
        + ' + ' + syntaxTreeToString(tree.operand2);
    case 'number-value':
      return String(tree.numberValue);
  }
}
```

```typescript
assert.equal(syntaxTreeToString(tree), '1 + 2 + 3');
```

注意，TypeScript 对判别联合执行穷尽性检查：如果我们忘记某个分支，TypeScript 会发出警告。

这是之前代码的面向对象版本：

```typescript
abstract class SyntaxTree {
  // 抽象 = 强制所有子类实现此方法：
  abstract toString(): string;
}
class NumberValue extends SyntaxTree {
  constructor(public numberValue: number) {
    super();
  }
  toString(): string {
    return String(this.numberValue);
  }
}
class Addition extends SyntaxTree {
  constructor(public operand1: SyntaxTree, public operand2: SyntaxTree) {
    super();
  }
  toString(): string {
    return this.operand1.toString() + ' ' + ' ' + this.operand2.toString();
  }
}

const tree = new Addition(
  new NumberValue(1),
  new Addition(
    new NumberValue(2),
    new NumberValue(3)
  )
);

assert.equal(tree.toString(), '1 + 2 + 3');
```

### 14.2.3.2 扩展性：面向对象方法 vs 函数式方法

每种方法都擅长处理一种扩展性：

- 使用面向对象的方法，如果我们想添加新操作，就必须修改每个类。然而，添加新类型不需要对现有代码进行任何更改。
- 使用函数式方法，如果我们想添加新类型，就必须修改每个函数。相反，添加新操作是非常简单的。

## 14.2.4 判别联合 vs. 普通联合类型

判别联合和普通联合类型有两个共同点：

- 成员值没有命名空间。
- TypeScript 执行穷尽性检查。

接下来的两个小节将了判别联合相对于普通联合的优势：

### 14.2.4.1 描述性属性名

通过判别联合，值具有描述性的属性名。对比一下：

普通联合：

```typescript
type FileGenerator = (webPath: string) => string;
type FileSource = string | FileGenerator;
```

判别联合：

```typescript
interface FileSourceFile {
  type: 'FileSource',
  nativePath: string;
}
interface FileSourceGenerator {
  type: 'FileSourceGenerator',
  fileGenerator: FileGenerator;
}
```

```typescript
type FileSource2 = FileSource | FileSourceGenerator;
```

现在，阅读代码的人立即知道字符串是什么：一个原生路径。

### 14.2.4.2 当名称不相同时可以使用它

判别联合无法作为普通联合来实现，因为我们无法区分联合的类型。



## 14.4 枚举模式

下面的示例展示了一个受 Java 启发的在 JavaScript 和 TypeScript 中有效的模式：

```typescript
class Color {
    static red = new Color();
    static green = new Color();
    static blue = new Color();
}
```

```typescript
// @ts-expect-error: 函数缺少返回语句且类型不包含 'undefined'。(2356)
function toGerman(color: Color): string { // (A)
    switch (color) {
        case Color.red:
            return 'rot';
        case Color.green:
            return 'grün';
        case Color.blue:
            return 'blau';
    }
}
```

```typescript
assert.equal(toGerman(Color.blue), 'blau');
```

遗憾的是，TypeScript 没有穷性检查，这就是为什么我们在 A 行得到了错误。

## 14.5 枚举的总结

下表总结了枚举及其替代方案在 TypeScript 中的特性：

| 唯一性 | 命名空间 | 迭代性 | 编译时检查 | 运行时检查 | 穷性检查 |
| --- | :---: | :---: | :---: | :---: | :---: |
| 数字枚举 | ✓ | ✓ | | | |
| 字符串枚举 | ✓ | ✓ | | | |
| 字符串联合类型 | ✓ | ✓ | | | |
| Symbol 联合类型 | ✓ | | | | |
| 判别联合类型 | | (1) | | (2) | ✓ |
| Symbol 属性 | ✓ | | | | |
| 字符串属性 | ✓ | | | | |
| 枚举模式 | ✓ | | ✓ | ✓ |

表格列标题：

- 唯一值：没有非枚举值可以被误认为是枚举值。
- 枚举命名空间

TypeScript 中枚举的替代方案

- 可以对枚举值进行迭代吗？
- 编译时检查：是否存在枚举值的窄类型？
- 运行时检查：
  - 对于枚举模式，运行时检查是 `instanceof`。
  - 如果可以对枚举值进行迭代，则检查可以轻松实现。
- 穷性检查（由 TypeScript 静态）

单元格脚注：

- 1. 判别联合类型并不是真正的唯一，但误认为成员的可能性较小（特别是当我们使用唯一的判别属性时）。
- 2. 如果判别属性具有唯一的名称，则可以用来检查。

## 14.6 致谢

- 感谢 Kirill Sukhomlin 关于如何定义对象字面量 T 的建议。

# 第 15 章

# 向类型添加特殊值

- 目录
15.1 在带中添加特殊值 . . . . 111
15.1.1 向类型添加 null 或 undefined . . . . 112
15.1.2 向类型添加 symbol . . . . 113
15.2 在带外添加特殊值 . . . . 113
15.2.1 判别联合类型 . . . . . . 113
15.2.2 其他类型的联合类型 . . . . 115

理解类型的一种方法将其视为值的集合。有时存在两层值：

- 基础层：普通值
- 元数据层：特殊值

在本章中，我们将研究如何向基础层类型添加特殊值。

## 15.1 在带中添加特殊值

添加特殊值的一种方法是创建一个基础类型的超集，其中某些特殊值为哨兵（sentinels）。它们存在于带中（在同一个通道内），作为普通值的兄弟。

例如，考虑以下可读流的接口：

```typescript
interface InputStream {
    getNextLine(): string;
}
```

目前，`.nextLine()` 只处理行，但不处理文件结束（EOF）。
我们如何为 EOF 添加支持？

可能性包括：

- 在调用 `.nextLine()` 之前需要调用额外的方法 `.isEof()`。
- `.nextLine()` 在到达 EOF 时抛出异常。
- EOF 的哨兵值。

接下来两个节介绍了引入哨兵值的两种方法。

## 15.1.1 向类型添加 null 或 undefined

严格 TypeScript 中，没有简单的对象类型（通过接口、对象模式、类定义）包含 `null`。这使其成为良好的哨兵值，我们可以通过联合类型将其添加到基础类型字符串中：

```typescript
type StreamValue = null | string;

interface InputStream {
  getNextLine(): StreamValue;
}
```

现在，当我们使用 `.nextLine()` 返回的值时，TypeScript 强制我们考虑这些策略：例如字符串和 `null`：

```typescript
function countComments(is: InputStream) {
  let countCount = 0;
  while (true) {
    const line = is.getNextLine();
    // @ts-expect-error: 对象可能是 'null'.(2531)
    if (line.startsWith('#')) // (A)
      countCount++;
    }
    if (line === null) break;
  }
  return countCount;
}
```

在 A 行，我们无法使用字符串方法 `.startsWith()`，因为 `line` 可能是 `null`。我们可以这样修复它：

```typescript
function countComments(is: InputStream) {
  let countCount = 0;
  while (true) {
    const line = is.getNextLine();
    if (line === null) break;
    if (line.startsWith('#')) // (A)
      countCount++;
    }
  }
  return countCount;
}
```

现在，当执行到 A 行时，我们可以确定 `line` 不是 `null`。

## 15.1.2 向类型添加一个 symbol

我们也可以使用 `null` 之外的值。Symbol 比对象更适合这项任务，因为它们具有唯一的标识，没有其他值可以误认为是它们。

这是使用 symbol 表示 EOF 的方法：

```typescript
const EOF = Symbol('EOF');
type StreamValue = typeof EOF | string;
```

为什么我们需要类型而不是直接使用 EOF？因为 EOF 是一个值而不是类型。类型运算符将 EOF 转换为类型。更多信息请见 §7.7 “动态静态”。

## 15.2 在带外添加特殊值

如果一个方法可能返回任何值，我们如何确保基础值和元值不被混淆？这是一个发生这种情况的示例：

```typescript
interface InputStream<T> {
  getNextValue(): T;
}
```

无论我们选择什么 EOF，都存在创建 Inputtypeof EOF 并将其添加到流中的风险。

解决方案是将普通值和特殊值分开，这样就不会被混淆（考虑不同的）。

## 15.2.1 判别联合类型

判别联合类型是对多个对象类型的联合，这些类型至少有一个公共属性，被称为判别式（discriminant）。判别式对于每个对象类型必须有不同的值——我们可以将其视为对象类型的 ID。

### 15.2.1.1 示例：InputStreamValue

在下面的示例中，`InputStreamValue<T>` 是判别联合类型，其判别式是类型。

```typescript
interface NormalValue<T> {
  type: 'normal'; // 字符串字量类型
  data: T;
}
interface Eof {
  type: 'eof'; // 字符串字量类型
}
```

type InputStreamValue<T> = Eof | NormalValue<T>;




## 15.2 在带外添加特殊值

### 15.2.2 其他类型的联合类型

只要我们有办法区分联合类型中的成员类型，其他类型的联合类型也可以像判别式联合类型一样方便。

一种可能性是通过唯一属性来区分成员类型：

```typescript
interface A {
  one: number;
  two: number;
}
interface B {
  three: number;
  four: number;
}
```

type Union = A | B;

```typescript
function func(x: Union) {
  // @ts-expect-error: Property 'two' does not exist on type 'Union'
  // Property 'two' does not exist on type 'B'.(2339)
  console.log(x.two); // error
}

if ('one' in x) { // 判别检查
  console.log(x.two); // OK
}
```

另一种可能性是通过与/或 实例检查来区分成员类型：

```typescript
type Union = [string] | number;

```

```typescript
function logHexValue(x: Union) {
  if (Array.isArray(x)) { // 判别检查
    console.log(x[0]); // OK
  } else {
    console.log(x.toString(16)); // OK
  }
}
```

# 第四部分

# 对象、类、数组和函数的类型

## 第 16 章

## 对象的类型

- 目录
- 16.1 对象所扮演的角色 . . . . . . . . . . . . . . . . . . . 120
- 16.2 对象的类型 . . . . . . . . . . . . . . . . . . . . . 120
- 16.3 TypeScript 中的 object vs. object . . . . . . . . . . . 120
  - 16.3.1 纯 JavaScript: object 与 object 实例 120
  - 16.3.2 TypeScript 中的 Object (大写 "O"): 类 对象的实例 121
  - 16.3.3 TypeScript 中的 object (小写 "o"): 非原始值 . . 122
  - 16.3.4 Object vs. object: 原始值 . . . . . . . . . . 122
  - 16.3.5 Object vs. object: 不兼容的属性类型 . . . . . 122
- 16.4 对象类型字面量和接口 . . . . . . . . . . . . . . . . . 123
  - 16.4.1 对象类型字面量和接口之间的区别 . . . . . 123
  - 16.4.2 接口在 TypeScript 中以结构化的方式工作 . . . . . 125
  - 16.4.3 接口和对象类型字面量的成员 . . . . . . 125
  - 16.4.4 方法签名: 作为字典的对象 . . . . . . . . 126
  - 16.4.5 索引签名: 接口描述对象的实例 . . . . . . 128
  - 16.4.7 冗余属性检查: 什么时候允许额外属性? . 129
- 16.5 类型推断 . . . . . . . . . . . . . . . . . . . . . . . . . 133
- 16.6 接口的其他特征 . . . . . . . . . . . . . . . . . 133
  - 16.6.1 可选属性 . . . . . . . . . . . . . . . . . . . 133
  - 16.6.2 只读属性 . . . . . . . . . . . . . . . . . . . 134
- 16.7 JavaScript 的原型链与 TypeScript 的类型 . . 135
- 16.8 本章的来源 . . . . . . . . . . . . . . . . . . . 1355 135 135

在本章中，我们将探索在 TypeScript 中如何对对象和属性进行静态类型化。

## 16.1 对象所扮演的角色

在 JavaScript 中，对象可以扮演两个角色（始终至少扮演一个，有时是混合体）：

- 记录（Records）具有固定数量的属性，这些属性在开发时是知的。每个属性可以有不同的类型。

- 字典（Dictionaries）具有任意数量的属性，其名称在开发时未知。所有的属性键（字符串和/或符号）具有相同的类型，属性值也是如此。

首先，我们将探索作为记录的对象。在本章的稍后部分，我们将简要介绍作为字典的对象。

## 16.2 对象的类型

对象有两种通用的类型：

- 大写 "O" 的 Object 是所有 Object 类实例的类型：

- 小写 "o" 的 Object 是所有非原始值的类型：

在 TypeScript 中，对象也可以通过类型字面量或接口来定义：

```typescript
type Person = {
  name: string;
};
```

## 16.3 TypeScript 中的 object vs. object

### 16.3.1 纯 JavaScript: object 与 object 实例

在纯 JavaScript 中，对象可以作为记录或字典：

```javascript
const obj1 = new Object();
obj1.a = 1;

const obj2 = { a: 2 };
```

### 16.3.2 TypeScript 中的 Object (大写 "O"): 类 对象的实例

在 TypeScript 中，`Object` 是所有 `Object` 类实例的类型：

```typescript
let obj1: Object = new Object();
obj1.a = 1; // OK
```

### 16.3.3 TypeScript 中的 object (小写 "o"): 非原始值

在 TypeScript 中，`object` 是所有非原始值的类型：

```typescript
let obj1: object = { a: 1 };
obj1.a = 2; // error: Property 'a' does not exist on type 'object'
```

### 16.3.4 Object vs. object: 原始值

原始值（如字符串、数字、boolean）不是对象：

```typescript
let obj1: Object = "hello"; // error: Type 'string' is not assignable to type 'Object'.
```

### 16.3.5 Object vs. object: 不兼容的属性类型

当对象字面量与接口的属性类型不兼容时，会报错：

```typescript
interface A {
  a: number;
}
let obj: A = { a: "hello" }; // error: Type 'string' is not assignable to type 'number'.
```





// @ts-expect-error: Duplicate identifier 'PersonAlias'. (2300)
type PersonAlias = {last: string};

相反，同名的接口会被合并：

```
interface PersonInterface {
  first: string;
}
interface PersonInterface {
  last: string;
}
const jane: PersonInterface = {
  first: 'Jane',
  last: 'Doe',
};
```

## 16.4.1.3 映射类型 (Mapped types)

对于映射类型（line A），我们需要使用对象类型字面量：

```
interface Point {
  x: number;
  y: number;
}
```

```
type PointCopy1 = {
[Key in keyof Point]: Point[Key]; // (A)
};
```

```
// 语法错误：
// interface PointCopy2
// [Key in keyof Point]: Point[Key];
//
```

- 关于映射类型的更多信息

映射类型超出了本书目前的范围。有关更多信息，请参阅《TypeScript 手册》。

## 16.4.1.4 多态 this 类型 (Polymorphic this types)

多态 this 类型只能在接口中使用：

```
interface AddStrings {
  add(str: string); this;
};
```

```
class StringBuilder implements AddStrings {
  result = '';
  add(str: string) {
this.result += str;
return this;
}
```

## 本节来源

- GitHub issue “TypeScript: types vs. interfaces” Johannes Ewald

> 从现在起，“interface”指的是“接口或对象类型字面量”（除非另有说明）。

## 16.4.2 接口在 TypeScript 中是结构化工作的

接口是结构化工作的——它们不需要被实现即可匹配：

```
interface Point {
  x: number;
  y: number;
}
const Point = {x: 1, y: 2}; // OK
```

关于此主题的更多信息，请参阅 §11.4 “命名类型系统 vs 结构化类型系统”。

## 16.4.3 接口和对象类型字面量的成员

接口和对象类型字面量体内部的构造被称为它们的成员。这些是最常见的成员：

```
interface ExampleInterface {
  // 属性签名
  myProperty: boolean;

  // 方法签名
  getMethod(str: string): number;

  // 索引签名
  [key: string]: any;

  // 调用签名
  (num: number): string;

  // 构造签名
  new(str: string): ExampleInstance;
}
interface ExampleInstance {},
```

126

16 对象的类型

让我们详细查看这些成员：

- * 属性签名定义属性：
myProperty: boolean;

- * 方法签名定义方法：
myMethod(str: string): number;

注意：参数名称（在此例中为：str）有助于记录代码工作原理，但没有其他用途。

- * 索引签名用于描述用作字典的数组或对象。
[key: string]: any;

注意：名称 key 的存在仅用于文档说明之目的。

- * 调用签名允许接口描述函数：
(num: number): string;

- * 构造签名允许接口描述类和构造函数：
new(str: string): ExampleInstance;

属性签名应该是是通俗自懂的。调用签名和构造签名将在本书稍后部分描述。我们将仔细查看方法签名和索引签名。

## 16.4.4 方法签名

就 TypeScript 的类型系统而言，方法定义和值为函数的属性是等价的：

```
interface HasMethodDef {
  simpleMethod(flag: boolean): void;
}
interface HasFuncProp {
  simpleMethod(flag: boolean) => void;
}
const objWithMethod: HasMethodDef = {
  simpleMethod(flag: boolean): void {},
};
const objWithMethod2: HasFuncProp = objWithMethod;

const objWithOrdinaryFunction: HasMethodDef = {
  simpleMethod: function (flag: boolean): void {},
};
const objWithOrdinaryFunction2: HasFuncProp = objWithOrdinaryFunction;
```

## 16.4 对象类型字面量和接口

```
const objWithArrowFunction: HasMethodDef = {
  simpleMethod(flag: boolean): void => {};
};
const objWithArrowFunction2: HasFuncProp = objWithArrowFunction;
```

我的建议是使用任何能够表达属性应如何设置的语法。

## 16.4.5 索引签名：对象作为字典

到目前为止，我们只使用接口来表示固定键的记录对象。我们如何表达一个对象被用作字典？例如：在下面的代码片段中，TranslationDict 应该是什么？

```
function translate(dict: TranslationDict, english: string): string {
  return dict[english];
}
```

我们使用索引签名（line A）表示 TranslationDict 用于将字符串键映射到值的对象：

```
interface TranslationDict {
  [key:string]: string; // (A)
}
const dict = {
  'yes': 'si',
  'no': 'no',
  'maybe': 'tal vez',
}
assert.equal(
  translate(dict, 'maybe'),
  'tal vez');
```

## 16.4.5.1 索引签名

索引签名键必须是字符串或数字：

- 不允许符号（Symbols）。
- 不允许联合类型（例如：number）。

## 16.4.5.2 字符串键

就像 JavaScript 一样，如果我们同时拥有索引签名和属性键，前者的类型必须是后者的子类型。以下示例是有效的，因为 Object 是以下类型的子类型：

```
interface StringAndKeys {
  [key: string]: number;
}
```

129

16 对象的类型

```
interface StringAndKeys {
  [key: string]: number;
}
```

128

```javascript
function f(x: StringAndKeys) {
  return x;
}
```

## 16.4.6 接口描述 Object 实例

所有接口描述 Object 的实例并继承 Object 的属性。

在下面的示例中，类型为 {} 的参数与 Object 类型兼容：

```
function f1(x: {}): Object {
  return x;
}
```

## 16.4 对象类型字面量和接口

同样，{} 有方法 toString()：

```javascript
function f2(x: {}): string {
  return x;
}
```

## 16.4.7 属性检查：何时允许额外属性？

例如，考虑以下接口：

```
interface Person {
  x: number;
  y: number;
}
```

该接口有两种（以及其他）解释方式：

- 闭合解释：它可以描述*恰好*具有 x 和 y 属性的对象。换句话说：这些对象不能有*额外属性*（多所需的属性）。
- 开放解释：它可以描述*至少*具有 x 和 y 属性的对象。换：允许额外属性。

TypeScript 使用这两种解释。为了探索它是如何工作的，我们将使用以下函数：

```typescript
function computeDistance(point: Person) { /*...*/ }
```

默认允许额外属性 .z：

```javascript
const obj = { x: 1, y: 2, z: 3 };
computeDistance(obj); // OK
```

然而，如果我们直接使用字面量，则不允许额外属性：

```typescript
// @ts-error: Argument of type '{ x: number; y: number; z: number; }
 is not assignable to parameter of type 'Point'.
// 对象字面量只能指定已知属性，且 'z'
// 不在类型 'Point' 中。(2345)
computeDistance({ x: 1, y: 2, z: 3 }); // error
```

## 16.4.7.1 为什么对象字面量中不允许额外属性？

*对象字面量*更严格的规则可以防止属性拼写错误提供保护。我们将使用以下接口来演示这意味着什么：

```typescript
interface Person {
  first: string;
  middle?: string;
  last: string;
}
function computeFullName(person: Person) { /*...*/ }
```





130

16 对象的类型

`middle` 属性是可选的，可以省略（可选属性在本章稍后会介绍）。对于 TypeScript 来说，写错名称看起来就像省略了它并提供了一个多余属性。然而，它仍然会捕获类型，因为在这种情况下不允许出现多余属性：

```typescript
// @ts-expect-error: Argument of type '{ first: string; middle: string;
// last: string; } is not assignable to parameter of type 'Person'
// Object literal may only specify known properties, but 'middle'
// does not exist in type 'Person'. Did you mean to write 'middle'?
computeFullName({first: 'Jane', middle: 'Cecily', last: 'Doe'});
```

16.4.7.2 为什么当对象来自其他地方时允许多余属性？

想法是，如果对象来自其他地方，我们可以假设它已经经过审核且不会有类型问题。如果类型不是问题，我们可以做得那么小心。我们的目标应该是最大化灵活性。考虑以下函数：

```typescript
interface HasYear {
  year: number;
}
```

```typescript
function getAge(obj: HasYear) {
  const yearNow = new Date().getFullYear();
  return yearNow - obj.year;
}
```

如果不允许传递给 `getAge()` 的多余属性，这个函数的用处将有限。16.4.7.3 空接口允许多余属性

如果接口是空的，多余属性总是允许的：

```typescript
interface Empty {}
interface OneProp {
  myProp: number;
}
```

```typescript
// @ts-expect-error: Type '{ myProp: number; anotherProp: number; }'
// is assignable to type 'OneProp'.
// Object literal may only specify known properties, and
// 'anotherProp' does not exist in type 'OneProp'. (2322)
const a: OneProp = { myProp: 1, anotherProp: 2 }; //

16.4 对象字面量与接口

16.4.7.4 不带属性的对象

如果我们想强制对象没有属性，可以使用以下技巧（Geoff）：

```typescript
interface WithoutProperties {
  [key: string]: never;
}

// @ts-expect-error: Type 'number' is not assignable to type 'never'. (2322)
const a: WithoutProperties = { prop: 1 }; // OK

### 16.4.7.5 在对象字面量允许多余属性

作为一个示例，考虑接口 `Point` 和函数 `computeDistance1`：

```typescript
interface Point {
  x: number;
  y: number;
}

function computeDistance1(point: Point) { /*...*/ };

// @ts-expect-error: Argument of type '{x: number; y: number; z: number}'
// is not assignable to parameter of type 'Point'.
// Object literal may only specify known properties, and 'z'
// does not exist in type 'Point'. (2345)
computeDistance1({ x: 1, y: 2, z: 3 });


一种方法是将对象字面量赋值给中间变量：

```typescript
const obj = { x: 1, y: 2, z: 3 };
computeDistance1(obj);
```

第二种方法是使用断言：

```typescript
computeDistance1({ x: 1, y: 2, z: 3 } as Point); // OK
```

第三种方法是重写 `computeDistance()` 使其使用类型参数：

```typescript
function computeDistance2<P extends Point>(point: P) { /*...*/ };
computeDistance2({ x: 1, y: 2, z: 3 }); // OK
```

第四种方法是扩展接口 `Point` 以便允许多余属性：

```typescript
interface PointEtc extends Point {
  [key: string]: any;
}
function computeDistance3(point: PointEtc) { /*...*/ };
computeDistance3({ x: 1, y: 2, z: 3 }); // OK
```

132

16 对象的类型

我们将继续两个 TypeScript 不允许多余属性的示例。

16.4.7.5.1 允许多余属性：示例 Incrementor

在这个例子中，我们想要实现 `Incrementor`，但 TypeScript 不允许额外的属性 `counter`：

```typescript
interface Incrementor {
  inc(): void
}
function createIncrementor(start = 0): Incrementor {
  return {
    // @ts-expect-error: Type '{ counter: number; inc(): void; } is not assignable to type 'Incrementor'.
    // Object literal may only specify known properties, and
    // 'counter' does not exist in type 'Incrementor'. (2322)
    counter: start,
    inc() {
      // @ts-expect-error: Property 'counter' does not exist on type 'Incrementor'.
      this.counter++;
    }
  };
}
```

遗憾的是，使用类型断言仍然有一个类型错误：

```typescript
function createIncrement2(start = 0): Incrementor {
  return {
    counter: start,
    inc() {
      // @ts-expect-error: Property 'counter' does not exist on type 'Incrementor'. (2339)
      this.counter++;
    }
  } as Incrementor;
}
```

我们可以为接口 `Incrementor` 添加索引签名。或者——如果那是不可能的——我们可以引入一个中间变量：

```typescript
function createIncrement3(start = 0): Incrementor {
  const incrementor = {
    counter: start,
    inc() {
      this.counter++;
    }
  };
  return incrementor;
}
```

## 16.5 类型推断

### 16.4.7.5.2 允许多余属性：示例 .dateStr

以下比较函数可以用于对具有 `.dateStr` 属性的对象排序：

```typescript
function compareDateStrings(
  a: {dateStr: string}, b: {dateStr: string}) {
  if (a.dateStr < b.dateStr) {
    return +1;
  } else if (a.dateStr > b.dateStr) {
    return -1;
  } else {
    return 0;
  }
}
```

原则上，我们需要使用前一种。TypeScript 为通过各种方式创建的对象：

```typescript
// 16.5 类型推断

这些是 TypeScript 为通过以下创建的对象推断的类型：
```typescript
// 16.5 类型推断

const obj1 = { a: 1, b: 2 };
```

原则上，我们需要使用前一种。TypeScript 为通过各种方式创建的对象：

```typescript
// 16.5 类型推断

const obj1 = { a: 1, b: 2 };
```

原则上，我们需要使用前一种。TypeScript 为通过各种方式创建的对象：
```typescript
// 16.5 类型推断

const obj1 = { a: 1, b: 2 };
```

134

16 对象的类型

## 16.6 的其他特性

### 16.6.1 可选属性

如果在属性名称后加上一个问号（?），该属性就是可选的。在以下示例中，`middle` 是可选的：

```typescript
interface Name {
  first: string;
  middle?: string;
  last: string;
}
```

因此，省略该属性是允许的（A）：

```typescript
const john: Name = {first: 'Doe', last: 'Doe'}; // (A)
```

135

134

16 对象的类型

### 16.6.1 可选属性 vs. undefined|string

可选属性和 `undefined|string` 有什么区别？

```typescript
interface Inter {
  prop1?: string;
  prop2: undefined | string;
}
```

可选属性可以做到 `undefined|string` 能做的一切。我们甚至可以使用前者的值：

```typescript
const obj1: Inter = { prop1: undefined, prop2: undefined };
```

然而，`prop1` 可以省略：

```typescript
const obj2: Inter = { prop2: undefined };
```

```typescript
// @ts-expect-error: Property 'prop2' is missing in type '{} but required
// in type 'Inter'. (2741)
const obj3: Inter = {};
```

`undefined|string` 和 `null|string` 类型对于想要显式省略的情况有用。当人们看到这种显式省略时，他们知道它是关闭的。

### 16.6.2 只读属性

在以下示例中，`prop` 是只读的：

```typescript
interface MyInterface {
  readonly prop: number;
}
```

作为结果，我们可以读取它，但不能更改它：

```typescript
const obj: MyInterface = {
  prop: 1,
};
```

```typescript
console.log(obj.prop); // OK
```

```typescript
// @ts-expect-error: Cannot assign to 'prop' because it is a read-only
// property. (2540)
obj.prop = 2;
```

136

## 16.7 JavaScript 的原型链与 TypeScript 的类型

TypeScript 不区分拥有属性和继承属性。它们都被简单视为属性。

```typescript
interface MyInterface {
  toString(): string; // 继承属性
  prop: number; // 有属性
}
const obj: MyInterface = { // OK
  prop: 123,
};
```

obj 从 `Object.prototype` 继承了 `toString()`。
这种方法的缺点是 JavaScript 中的某些现象无法通过 TypeScript 类型系统来描述。优点是类型系统更简单。

## 16.8 本章的来源

*   *TypeScript Handbook*
*   *TypeScript Language Specification*





## 第 17 章
## TypeScript 中的类定义

### 目录
17.1 快速查表：原生 JavaScript 中的类 ................................................ 137
17.1.1 类的基本成员 ........................................................................ 138
17.1.2 修饰符：static ......................................................................................... 138
17.1.3 类似修饰符的名前缀：# (private) .......................................................... 138
17.1.4 访问器修饰符：get (getter) 和 set (setter) ................................ 139
17.1.5 方法修饰符：* (generator) ............................................................ 139
17.1.6 方法修饰符：async ....................................................................... 140
17.1.7 计算类成员名 ................................................................ 140
17.1.8 修饰符的组合 ....................................................................... 140
17.1.9 底层原理 ....................................................................................... 141
17.1.10 关于原生 JavaScript 中类定义的更多信息 .......................... 143
17.2 TypeScript 中的非公共数据槽 ............................................................ 143
17.2.1 私有属性 (Private properties) .......................................................................... 143
17.2.2 私有字段 (Private fields) ......................................................................... 144
17.2.3 私有属性对比私有字段 .......................................................... 145
17.2.4 保护属性 (Protected properties) ................................................... 145
17.3 私有构造函数 ............................................... 146
17.4 初始化实例属性 ............................................... 147
17.4.1 严格属性初始化 ................................................................... 147
17.4.2 将构造函数参数设为公共、私有或保护 149
17.5 抽象类 ................................................................................. 149

在本章中，我们将研究 TypeScript 中类定义是如何工作的：

- 首先，我们查看原生 JavaScript 中类定义的特性。
- 然后，我们探索 TypeScript 为此带来的额外功能。

## 17.1 快速查表：原生 JavaScript 中的类

本节是原生 JavaScript 中类定义的快速查表。

### 17.1.1 类的基本成员

```typescript
class OtherClass {}

class MyClass1 extends OtherClass {
  publicInstanceField = 1;

  constructor() {
    super();
  }

  prototypeMethod() {
    return 2;
  }
}

const inst1 = new MyClass1();
assert.equal(inst1.publicInstanceField, 1);
assert.equal(inst1.prototypeMethod(), 2);
```

接下来的章节将关于修饰符。
最后，有一个表格显示了修饰符如何组合。

### 17.1.2 修饰符：static

```typescript
class MyClass2 {
  static staticPublicField = 1;

  static staticPublicMethod() {
    return 2;
  }
}

assert.equal(MyClass2.staticPublicField, 1);
assert.equal(MyClass2.staticPublicMethod(), 2);
```

### 17.1.3 类似修饰符名前缀：# (private)

```typescript
class MyClass3 {
  #privateField = 1;

  #privateMethod() {
    return 2;
  }

  static accessPrivateMembers() {
    // 私有成员只能在类定义内部访问
    const inst3 = new MyClass3();
    assert.equal(inst3.privateField, 1);
    assert.equal(inst3.privateMethod(), 2);
  }
}

MyClass3.accessPrivateMembers();
```

针对 JavaScript 的警告：

- 目前对私有方法的支持有限。
- 私有字段的范围更广，但也存在局限。

TypeScript 从 3.8 版本开始一直支持私有字段，但目前不支持私有方法。

### 17.1.4 访问修饰符：get (getter) 和 set (setter)

粗来说，访问器是通过访问属性时调用的方法。访问器有两种类型：getter 和 setter。

```typescript
class MyClass5 {
  #name = 'Rumpelstiltskin';

  /** 原型 getter */
  get name() {
    return this.#name;
  }

  /** 原型 setter */
  set name(value) {
    this.#name = value;
  }
}
const inst5 = new MyClass5();
assert.equal(inst5.name, 'Rumpelstiltskin'); // getter
inst5.name = 'Queen'; // setter
assert.equal(inst5.name, 'Queen'); // getter
```

### 17.1.5 方法修饰符：* (generator)

```typescript
class MyClass6 {
  * publicPrototypeGeneratorMethod() {
    yield 'hello';
    yield 'world';
  }
}
const inst6 = new MyClass6();
```

### 17.1.6 方法修饰符：async

```typescript
class MyClass7 {
  async publicPrototypeMethod() {
    const result = await Promise.resolve('abc');
    return result;
  }
}
```

### 17.1.7 计算类成员名

```typescript
class MyClass8 {
  [ 'InstanceField'] = 1;

  [ 'prototypeMethod']() {
    return 2;
  }
}
```

### 17.1.8 修饰符的组合

| 修饰符 | 访问器 | Async | 生成器 | 可见性 |
| :--- | :---: | :---: | :---: | :---: |
| static | | | | |
| get | X | | | |
| set | X | | | |
| private | | | | |

### 17.1.9 底层原理

需要记住在使用类时，有两个原型链：

- 实例链：从实例开始。
- 静态链：从该实例的类开始。

考虑以下原生 JavaScript 示例：

```javascript
class ClassA {
  static staticMthdA() {}
}
```





## 17.2 TypeScript 中的非公开数据槽位

### 17.1.10 关于原生 JavaScript 中类定义的更多信息

- 公有字段、私有字段、私有方法/getters/setter（博客文章）
- 剩余的所有 JavaScript 类特性（《给急躁的程序员准备的 JavaScript 特性》中的章节）

## 17.2 TypeScript 中的非公开数据槽位

默认情况下，TypeScript 中的所有数据槽位都是公共属性。保留数据有两种方式：

- 私有属性（Private properties）
- 私有字段（Private fields）

接下来我们将查看这两种。

请注意，TypeScript 目前不支持私有方法。

### 17.2.1 私有属性

私有属性是 TypeScript 特有的（静态）功能。任何属性都可以通过在它的前面加上 `private` 关键字来变为私有（A 行）：

```typescript
class PersonPrivate {
  private name: string; // (A)
  constructor(name: string) {
    this.name = name;
  }

  sayHello() {
    return `Hello ${this.name}!`;
  }
}
```

现在，如果在错误的作用域内（A 行）访问该属性，我们将得到编译错误：

```typescript
const john = new PersonPrivateProperty('John');

assert.equal(
  john.sayHello(), 'Hello John!'
);

// @ts-expect-error: 属性 'name' 是私有的，只能在类 'PersonPrivateProperty' 内部访问。(2341)
john.name; // (A)
```

然而，`private` 在运行时并不会改变任何东西。在运行时，属性 `.name` 与公共属性没有区别：

```javascript
assert.deepEqual(
  Object.keys(john),
  ['name']);
```

## 17 TypeScript 中的类定义

当我们查看类被编译后的 JavaScript 代码时，也可以看到私有属性在运行时并不受受保护的：

```javascript
class PersonPrivateProperty {
  constructor(name) {
    this.name = name;
  }
  sayHello() {
    return `Hello ${this.name}!`;
  }
}
```

### 17.2.2 私有字段

私有字段是 JavaScript 的一项新特性，TypeScript 从 3.8 版本开始支持它：

```typescript
class PersonPrivateField {
  #name: string;
  constructor(name: string) {
    this.#name = name;
  }
  sayHello() {
    return `Hello ${this.#name}!`;
  }
}
```

这个版本的 `Person` 使用方式大部分与私有属性版本相同：

```typescript
const john = new PersonPrivateField('John');
```

```typescript
assert.equal(
john.sayHello(), 'Hello John!');
```

然而，数据被完全封装了。在类外部使用私有字段语法会导致 JavaScript 语法错误。这就是为什么我们在 A 行使用 `eval()` 来执行这段代码：

```javascript
assert.throws(
  () => eval('john.#name'), // (A)
{
  name: 'SyntaxError',
  message: '私有字段 #name 必须在 "
  + "闭包类中声明"',
});
```

```javascript
assert.deepEqual(
Object.keys(john),
[]);
```

现在的编译结果要复杂得多（经过了稍微简化）：

## 17.2 TypeScript 中的非公开数据槽位

```javascript
var _classPrivateFieldSet = function (receiver, privateMap, value) {
  if (!privateMap.has(receiver)) {
    throw new TypeError(
      '尝试在非实例上设置私有字段'
    );
  }
  privateMap.set(receiver, value);
  return value;
};

// 省略: __classMapField

```

```javascript
var name = new WeakMap();
class Person {
  constructor(name) {
    // 为此实例向 _name 添加条目
    _name.set(this, void 0);

    // 现在我们可以使用辅助函数了：
    __classPrivateFieldSet(this, _name, name);
  }
  ....
}
```

这段代码使用了一种保持实例数据私有的常用技术：

- 每个 `WeakMap` 实现私有字段。
- 它将每个实例与一个私有数据关联。

关于此主题的更多信息：请参见《给急躁的程序员准备的 JavaScript》。

### 17.2.3 私有属性 vs 私有字段

- 私有属性的缺点：
  - 我们无法在子类中重用私有属性的名称（因为属性在运行时并不是私有的）。
  - 运行时没有封装。
- 私有属性的优点：
  - 客户端可以绕过封装并访问私有属性。当有人需要绕过 bug 时，这可能很有用。换句话说：数据的完全封装有利也有弊。

### 17.2.4 保护属性

私有字段和私有属性无法在子类中访问（A 行）：

```typescript
class PrivatePerson {
  private name: string;
  constructor(name: string) {
    this.name = name;
  }
}
```

```typescript
sayHello() {
  return `Hello ${this.name}!`;
}
```

```typescript
class PrivateEmployee extends PrivatePerson {
  private company: string;
  constructor(name: string, company: string) {
    super(name);
    this.company = company;
  }
```

```typescript
sayHello() {
  // @ts-expect-error: 属性 'name' 是私有的，只能
  // 在类 'PrivatePerson' 内部访问。(2341)
  return `Hello ${this.name}!`;
}
```

(注：此处原文文本似乎存在格式错乱，已根据上下文逻辑进行翻译)

## 17.4 初始化属性

然而，有时我们以 TypeScript 无法识别的方式初始化属性。这时可以使用感叹号（确定赋值断言）来关闭 TypeScript 的警告（A 行和 B 行）：

```typescript
class Point {
  x!: number; // (A)
  y!: number; // (B)
  constructor() {
    this.initProperties();
  }
  initProperties() {
    this.x = 0;
    this.y = 0;
  }
}
```

### 17.4.1.1 示例：通过对象设置实例属性

在下面的示例中，我们也需要定义赋值断言。在这里，我们通过构造函数参数 props 设置实例属性：

```typescript
class CompilerError implements CompilerErrorProps { // (A)
  line!: number;
  description!: string;
  constructor(props: CompilerErrorProps) {
    Object.assign(this, props); // (B)
  }
}
```

```typescript
// 用于参数属性的辅助接口
interface CompilerErrorProps {
  line: number,
  description: string;
}
```

// 使用该类：

```typescript
const err = new CompilerError({
  line: 123,
  description: 'Unexpected token',
});
```

(注：由于提供的原文在中间部分存在多处重复和逻辑混乱（如 PersonPrivateProperty 和 PrivateEmployee 的代码片段交叉），翻译时已根据技术逻辑进行了对齐处理，以确保输出通顺。)





17.5 抽象类

### 17.4.2 将构造函数参数设置为公共、私有或受保护

如果我们对构造函数参数使用 `public` 关键字，TypeScript 会为我们做两件事：

- 它会声明一个同名的公共实例属性。
- 它会将该参数赋值给该实例属性。

因此，这两个类是等价的：

```typescript
class Point1 {
  constructor(public x: number, public y: number) {
  }
}
```

```typescript
class Point2 {
  x: number;
  y: number;
  constructor(x: number, y: number) {
    this.x = x;
    this.y = y;
  }
}
```

如果我们使用 `private` 或 `protected` 代替 `public`，那么相应的实例属性将是私有的或受保护的（而不是公的）。

## 抽象类

在 TypeScript 中有两种结构可以是抽象的：只有它们的子类可以是——前提是它们本身不是抽象的。

- 抽象类不能被实例化。抽象方法没有实现，只有类型签名。每个具体的子类必须有一个具有相同名称和兼容类型签具体方法。
- 如果一个类拥有抽象方法，它也必须是抽象类。

下面的代码演示了抽象类和抽象方法。

一方面，有一个父类 `Printable` 它的辅助类 `StringBuilder`：

```typescript
class StringBuilder {
  string = '';
  add(str: string) {
    this.string += str;
  }
}
```

```typescript
abstract class Printable {
  toString() {
    const out = new StringBuilder();
    this.print(out);
    return out.string;
  }
  abstract print(out: StringBuilder): void;
}
```

另一方面，还有具体的子类 `Entries` 和 `Entry`：

```typescript
class Entries extends Printable {
  entries: Entry[];
  constructor(entries: Entry[]) {
    super();
    this.entries = entries;
  }
  print(out: StringBuilder): void {
    for (const entry of this.entries) {
      entry.print(out);
    }
  }
}
class Entry extends Printable {
  key: string;
  value: string;
  constructor(key: string, value: string) {
    super();
    this.key = key;
    this.value = value;
  }
  print(out: StringBuilder): void {
    out.add(this.key);
    out.add(': ');
    out.add(this.value);
    out.add('\n');
  }
}
```

最后，这是对 `Entries` 和 `Entry` 的使用：

```typescript
const entries = new Entries([
  new Entry('accept-ranges', 'bytes'),
  new Entry('content-length', '6518'),
]);
assert.equal(
  entries.toString(),
  'accept-ranges: bytes\ncontent-length: 6518\n'
);
```

关于抽象类的说明：

- 抽象类可以被视为接口，其中某些成员已经有了实现。
- 虽然类可以实现多个接口，但它最多只能扩展一个抽象类。
- “抽象性”只存在于编译时。在运行时，抽象类是普通类，抽象方法不存在（因为它们只提供了编译时信息）。
- 抽象类可以被视为模板，每个抽象方法都是一个必须由子类填充（实现）的空白。

## 第 18 章

## 类相关的类型

| 内容 | |
| :--- | :--- |
| 18.1 类的原型链 | 153 |
| 18.2 类实例的接口 | 154 |
| 18.3 类的接口 | 155 |
| 18.3.1 示例：在 JSON 之间进行转换 | 155 |
| 18.3.2 示例：TypeScript 为类 Object 及其实例提供的内置接口 | 156 |
| 18.4 作为类型的类 | 157 |
| 18.4.1 陷阱：类是结构化工作的，而非命名的 | 157 |
| 18.5 进阶阅读 | 159 |

在关于 TypeScript 的这一章节中，我们将检查与类及其实例相关的类型。

## 18.1 类的原型链

考虑这个类：

```typescript
class Counter extends Object {
    static createZero() {
        return new Counter(0);
    }
    value: number;
    constructor(value: number) {
        super();
        this.value = value;
    }
    increment() {
        this.value++;
    }
}
```

```typescript
// 方法
const myCounter = Counter.createZero();
assert.ok(myCounter instanceof Counter);
assert.equal(myCounter.value, 0);
```

```typescript
// 实例方法
myCounter.increment();
assert.equal(myCounter.value, 1);
```

## 18.2 类实例的接口

在本章中，我们将首先探索如何描述实例。接口提供了服务。例如：

```typescript
interface CountingService {
  value: number;
  increment(): void;
}
```

## 18.3 类的接口

结构化接口非常方便：如果预先知道一个对象必须实现某个接口，那么检查它是否实现通常是有意义的。

```typescript
class Counter implements CountingService {
  // ...
}
```

注释：

- TypeScript 不区分继承属性和自身的属性。
- 静态属性被接口忽略。

类本身也是对象（函数）。因此，我们可以使用接口来标识它们。下一节给出一个示例。

### 18.3.1 示例：在 JSON 之间进行转换

以下接口可以用于类支持从 JSON 转换：

```typescript
// JSON 转换为实例
interface JsonStatic {
  fromJson(json: any): JsonInstance;
}
```

```typescript
// 实例转换为 JSON
interface JsonInstance {
  toJson(): any;
}
```

我们在下面的代码中使用这些接口：

```typescript
class Person implements JsonInstance {
  static fromJSON(json: any): Person {
    if (typeof json !== 'string') {
      throw new TypeError(json);
    }
    return new Person(json);
  }
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  toJson(): any {
    return this.name;
  }
}
```

这是我们可以立即检查类（作为对象）是否实现了接口 `JsonStatic` 的方法：

```typescript
// 将类赋值给类型注解变量
const personImplementsJsonStatic: JsonStatic = Person;
```

这种这种检查的方法似乎是个好主意：

```typescript
const Person: JsonStatic = class implements JsonInstance
// ...
;
```

然而，这并不可行：

- 我们无法 `new Person`，因为 `JsonStatic` 没有构造签名。
- 如果 `Person` 有 `.fromJson()` 之外的静态属性，TypeScript 不允许我们访问它们。

### 18.3.2 示例：TypeScript 为类 Object 及其实例提供的内置接口

查看 TypeScript 的内置类型是有启发性的：

一方面，`ObjectConstructor` 是针对 `Object` 类本身的：

```typescript
/**
 * 为所有 JavaScript 对象提供共同功能。
 */
declare var Object: ObjectConstructor;
```

```typescript
interface ObjectConstructor {
  new(value?: any): Object;
  (): any;
  (value: any): any;
}
```

```typescript
/** 指类对象的原型的引用。 */
readonly prototype: Object;
```





## 18.4 作为类型的类

```typescript
/**
 * 返回对象的原型形。
 * @param o 引用原型的对象。
 */
getPrototypeOf(o: any): any;
}
```

另一方面，接口 `Object` 是用于 `Object` 实例的：

```typescript
interface Object {
  /** Object.prototype.constructor 的初始值是标准的内置 Object */
  constructor: Function;

  /** 返回对象的字符串表示。 */
  toString(): string;
}
```

`Object` 名字被使用了两次，分别处于两个语言层级：

- 在动态层面，用于全局变量。
- 在静态层面，用于类型。

## 18.4 作为类型的类

考虑以下类：

```typescript
class Color {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
}
```

这个类的定义创建了两个东西。

首先，是一个名为 `Color` 的构造器函数（可以通过 `new` 调用）：

```typescript
assert.equal(
  typeof Color, 'function'
)
```

其次，是一个名为 `Color` 的接口，它匹配 `Color` 的实例：

```typescript
const green = new Color('green');
```

这里是 `Color` 确实是一个接口的证明：

```typescript
interface RbColor extends Color {
  rgbValue: [number, number, number];
}
```

### 18.4.1 陷阱：类是结构性的，而不是命名的

尽管如此有一个陷阱：将 `Color` 作为静态类型并不是非常严格的检查：

```typescript
class Color {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
}
class Person {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
}
const person: Person = new Person('Jane');
const color: Color = person; // (A)
```

为什么 TypeScript 在行 A 没有报错？那是由于结构化类型系统：`Person` 和 `Color` 的实例具有相同的结构，因此在静态上是兼容的。

### 18.4.1.1 关闭结构化类型

我们可以通过添加私有属性让这两组对象变得兼容：

```typescript
class Color {
  name: string;
  private branded = true;
  constructor(name: string) {
    this.name = name;
  }
}
class Person {
  name: string;
  private branded = true;
  constructor(name: string) {
    this.name = name;
  }
}
```

```typescript
const person: Person = new Person('Jane');
// @ts-expect-error: 类型 'Person' 不可分配类型 'Color'。
// 类型对私有属性
// 'branded' 有独立的声明。(2322)
const color: Color = person;
```

在这种情况下，私有属性关闭了结构化类型系统。

## 18.5 进阶阅读

- 《给急迫程序员的 JavaScript》中的“原型链与类”章节。

## 第 19 章

## 作为值的类的类型

- 目录
- 19.1 特定类的类的类型 ................................................................... 161
- 19.2 typeof 类型运算符 ........................................................................ 162
- 19.2.1 构造器类型字面量 ................................................... 162
- 19.2.2 使用带有构造签名的对象字面量转换 ................ 162
- 19.3 类的泛型类型：Class<T> ............................................ 163
- 19.3.1 示例：创建实例 ...................................................... 163
- 19.3.2 示例：带有运行时检查的类型转换 ................................... 163
- 19.3.3 示例：运行时安全的 Map ............................ 164
- 19.3.4 陷阱：Class<T> 不匹配抽象类 ................ 165

在本章中，我们探索了作为值的类：

- 对于此类值，我们应该使用什么类型？
- 这些类型的用例是什么？

## 19.1 特定类的类的类型

考虑以下类：

```typescript
class Point {
  x: number;
  y: number;
  constructor(x: number, y: number) {
    this.x = x;
    this.y = y;
  }
}
```

这个函数接受一个类并创建它的实例：

```typescript
function createPoint(PointClass: ???, x: number, y: number) {
  return new PointClass(x, y);
}
```

如果我们想让参数 `PointClass` 是 `Point` 或其子类，我们应该使用什么类型呢？

## 19.2 typeof 类型运算符

在 §7.7 “两个语言层级：动态与静态”中，我们探索了 TypeScript 的两个语言层级：

- 动态层面：JavaScript（代码和值）
- 静态层面：TypeScript（静态类型）

类 `Point` 创建了两个东西：

- 构造器函数 `Point`
- 用于 `Point` 实例的接口 `Point`

取决于我们提到 `Point` 的地方，它的含义不同。这就是为什么我们不能将 `Point` 类型用于 `PointClass`：它匹配类的实例，而不是 `Point` 类本身。

相反，我们需要使用 `typeof` 运算符（另一个在 JavaScript 中也存在的 TypeScript 语法）。`typeof v` 代表动态(!) `v` 的类型。

```typescript
function createPoint(PointClass: typeof Point, x: number, y: number) // (A)
  return new PointClass(x, y);
```

```typescript
// 推断类型: Point
const point = createPoint(Point, 3, 6);
assert.ok(point instanceof Point);
```

### 19.2.1 构造器类型字面量

构造器类型字面量是一个带有前缀 `new` 的函数字面量（行 A）。前缀表示 `PointClass` 是一个可以通过 `new` 用的函数。

```typescript
function createPoint(
  PointClass: new (x: number, y: number) => Point, // (A)
  x: number, y: number
) {
  return new PointClass(x, y);
}
```

### 19.2.2 带有构造签名的对象类型字面量

记得接口和对象字面量类型（OLTs）的成员包括方法签名和调用签名。调用签名允许接口和 CLT描述函数。

## 19.3 类的泛型类型：Class<T>

同样，构造签名允许接口和 CLT 描述函数。在下一个示例中，`PointClass` 具有构造签名：

```typescript
function createPoint(
  PointClass: { new (x: number, y: number): Point },
  x: number, y: number
): Point {
  return new PointClass(x, y);
}
```

通过我们获取的知识，我们可以创建一个泛型类型引入参数 `T`：

```typescript
type Class<T> = new (...args: any[]) => T;
```

除了类型别名，我们也可以使用接口：

```typescript
interface Class<T> {
  new (...args: any[]): T;
}
```

`Class<T>` 是类的类型。它决定了条目的静态类型，并用于运行时检查。

### 19.3.1 示例：创建实例

`Class<T>` 允许我们编写 `createPoint` 的泛型版本：

```typescript
class Person {
  constructor(public name: string) {}
}

function createInstance<T>(cls: Class<T>, ...args: any): T {
  return new cls(...args);
}
```

`createInstance()` 的用法如下：

```typescript
const jane = createInstance(Person, 'Jane'); // 推断类型: Person
```

### 19.3.2 示例：带有运行时检查的类型转换

可以使用 `cast` 实现转换：

```typescript
function cast<T>(AnyClass: Class<T>, obj: any): T {
  if (!(obj instanceof AnyClass)) {
    throw new Error(`Not an instance of ${AnyClass.name}: ${obj}`);
  }
  return obj;
}
```

通过 `cast()`，我们可以将值转换为特定的类型。这在运行时也是安全的，因为我们在静态更改类型的同时进行了检查。以下代码提供了一个示例：

```typescript
function parseObject(jsonObjectStr: string): Object {
  // 推断类型: any
  const parsed = JSON.parse(jsonObjectStr);
  return cast(Object, parsed);
}
```

### 19.3.3 示例：运行时安全的 Map

`Class<T>` 和 `cast()` 的一个用例是安全的 Map：

```typescript
class TypeSafeMap {
  #data = new Map<any, any>();
  get<T>(key: Class<T>) {
    const value = this.#data.get(key);
    return cast(key, value);
  }
  set<T>(key: Class<T>, value: T): this {
    cast(key, value); // 运行时检查
    this.#data.set(key, value);
    return this;
  }
  has(key: any) {
    return this.#data.has(key);
  }
}
```

这是 `TypeSafeMap` 的运行示例：

```typescript
const map = new TypeSafeMap();

map.set(RegExp, /abc/);

// 推断类型: RegExp
const re = map.get(RegExp);

// 静态和动态错误！
assert.throws(
  // ts-expect-error: 参数类型 "abc" 不可分配
  // 给参数类型 'Date'。
  () => map.set(Date, 'abc');
);
```





## 19.3.4 阱：Class<T> 不匹配抽象类

当期望 `Class<T>` 时，我们无法使用抽象类：

```typescript
abstract class Shape {
}
class Circle extends Shape {
  // ...
}

// //ts-expect-error: Type 'typeof Shape' is not assignable to type
// 'Class<Shape>'.
// Cannot assign an abstract constructor type to a non-abstract
// constructor type. (2322)
const shapeClasses1: Array<Class<Shape>> = [Circle, Shape];
```

这是为什么呢？原理是，构造函数类型字面量和构造签名应该只用于实际上可以被 `new` 调用的值（更多信息请参考 GitHub issue）。

这是一种通变方法：

```typescript
type Class2<T> = Function & {prototype: T};

const shapeClasses2: Array<Class2<Shape>> = [Circle, Shape];
```

这种方法的缺点：

- 稍微稍显困惑。
- 具有此类型的值不能用于 `instanceof` 检查（作为右侧操作数）。

## 第 20 章

## 数组类型化

目录
- 20.1 数组的角色 167
- 20.2 数组类型化的方式 168
- 20.2.1 数组角色“列表”：数组类型字面量 vs 接口类型 Array 168
- 20.2.2 数组角色“元组”：元组类型字面量 168
- 20.2.3 同样是类数组的对象：带有索引签名的接口 168
- 20.3 阱：类型推断并不总是能正确获取数组类型 169
- 20.3.1 推断数组的类型很困难 169
- 20.3.2 非空数组字面量的类型推断 169
- 20.3.3 空数组字面量的类型推断 170
- 20.3.4 数组的 `const` 断言与类型推断 171
- 20.4 阱：TypeScript 假设索引永远不会越界 172

在本章中，我们将研究在 TypeScript 中如何对数组进行类型化。

## 20.1 数组的角色

数组在 JavaScript 中可以扮演以下角色（其一或混合）：

- 列表（Lists）：所有元素具有相同类型。数组的长度可变。
- 元组（Tuple）：数组的长度固定。元素不一定具有相同类型。

TypeScript 通过提供多种数组类型化的方式来适应这两个角色。接下来我们将查看。

## 20.2 数组类型化的方式

### 20.2.1 数组角色“列表”：数组类型字面量 vs 接口类型 Array

数组类型字面量由元素类型后 `[]` 组成。在下面的代码中，数组类型字面量是 `string[]`：

```typescript
// 每个数组元素类型为 `string`;
const myArrayArray: string[] = ['fee', 'fi', 'fo', 'fum'];
```

数组类型是全局泛型接口类型 `Array` 的简写：

```typescript
const myArrayArray: Array<string> = ['fee', 'fi', 'fo', 'fum'];
```

如果元素类型更复杂，我们需要为数组类型字面量加上括号：

```typescript
(number|string[])
(() => boolean[])
```

泛型类型 `Array` 在这种情况下效果更好：

```typescript
Array<number|string>
Array<() => boolean>
```

### 20.2.2 数组角色“元组”：元组类型字面量

如果数组具有固定长度，且每个元素都有取决于其位置的不同固定类型，那么我们可以使用元组字面量，例如 `[string, string, boolean]`：

```typescript
const yes: [string, string, boolean] = ['oui', 'si', true];
```

### 20.2.3 同样是类数组的对象：带有索引签名的接口

如果一个接口只有一个索引签名，我们可以将其用于数组：

```typescript
interface StringArray {
  [index: number]: string;
}
const strArr: StringArray = ['Huey', 'Dewey', 'Louie'];
```

同时具有索引签名和属性签名的接口仅适用于对象（因为索引元素和属性需要同时定义）：

```typescript
interface FirstNamesAndLastName {
  [index: number]: string;
  lastName: string;
}

const names: FirstNamesAndLastName = {
  0: 'Huey',
  1: 'Dewey',
  2: 'Louie',
  lastName: 'Duck'
};
```

## 20.3 阱：类型推断并不总是能正确获取数组类型

### 20.3.1 推断数组的类型很困难

由于数组的两个角色，TypeScript 无法总是猜出正确的类型。例如，考虑以下赋值给变量 `fields` 的数组字面量：

```typescript
const fields: Fields = [
  ['first', 'string', true],
  ['last', 'string', true],
  ['age', 'number', false],
];
```

`fields` 的最佳类型是什么？以下都是合理的选择：

```typescript
type Fields = Array<string, string, boolean>;

type Fields = Array<string|'string'|number, boolean>;

type Fields = Array<Array<string|boolean>>;

type Fields = [
  [string, string, boolean],
  [string, string, boolean],
  [string, string, boolean],
];

type Fields = Array<string|boolean>;

type Fields = Array<string|boolean>;
```

### 20.3.2 非空数组字面量的类型推断

当我们使用非空数组字面量时，TypeScript 默认推断为元组（而不是数组）：

```typescript
// //inferred-type: [number, number]
const arr = [1, 2];
```

这不是我们想要的，赋值给变量时会报错：

```typescript
function func(p: [number, number]) {
  return p;
}
// //inferred-type: number[]
const pairl = [1, 2];

func(pairl); // 错误：类型不匹配
```
```

我们可以通过为声明添加类型注解来修复此：

```typescript
const pair2: [number, number] = [1, 2]; // OK
```

### 20.3.3 空数组字面量的类型推断

如果我们用空数组字面量初始化，TypeScript 最初推断类型为 `any[]`：

```typescript
// //inferred-type: any[]
const arr = [];
```

相反，如果数组字面量至少有一个元素，那么类型是固定的且不会改变：

```typescript
// //inferred-type: number[]
const arr = [123];
```

### 20.3.4 数组的 `const` 断言与类型推断

我们可以可以在数组字面量后加上 `const` 断言：

```typescript
// //inferred-type: readonly ['igneous', 'metamorphic', 'sedimentary']
const rockCategories = ['igneous', 'metamorphic', 'sedimentary'] as const;
```

我们声明 `rockCategories` 不改变。这产生了以下影响：

- 数组变为只读——我们无法使用更改的操作：
  // //ts-expect-error: Property 'push' does not exist on
  // 'readonly ['igneous', 'metamorphic', 'sedimentary']'. (2339)
  rockCategories.push('sand');
- TypeScript 推断出一个元组：
  // //inferred-type: string[]
  const rockCategories2 = ['igneous', 'metamorphic', 'sedimentary'];
- TypeScript 推断字面量类型（如 `'igneous'`）而不是泛型类型。导致推断的元组不是 `[string, string, string]`。

这里有更多带断言的数组字面量示例：

```typescript
// //inferred-type: readonly [1, 2, 3, 4]
const number1 = [1, 2, 3, 4] as const;
// //inferred-type: number[]
const number2 = [1, 2, 3, 4];
```

```typescript
// //inferred-type: readonly [true, 'abc']
const booleanAndString = [true, 'abc'] as const;
// //inferred-type: string | boolean[]
const booleanAndString2 = [true, 'abc'];
```

### 20.3.4.1 `const` 断言的潜在陷阱

`const` 断言有两个潜在的陷阱。

首先，推断类型尽可能窄。这为 `let` 声明的变量带来了问题：我们无法赋值除初始化时使用的其他元组：

```typescript
let arr = [1, 2] as const;
```

```typescript
arr = [1, 2]; // OK
// //ts-expect-error: Type '3' is not assignable to type '2'. (2322)
arr = [1, 3];
```

其次，通过 `as const` 声明的元组不能被变异：



172

20 数组类型

```typescript
let arr = [1, 2] as const;

// @ts-expect-error: Cannot assign to '1' because it is a read-only
// property. (2540)
arr[1] = 3;
```

这既不是优点也不是缺点，但我们需要意识到它的存在。

## 20.4 陷阱：TypeScript 假设索引永远不会越界

当我们通过索引访问数组元素时，TypeScript 总是假设该索引在范围内（行 A）：

```typescript
const messages: string[] = ['Hello'];
```

```typescript
// %inferred-type: string
const message = messages[3]; // (A)
```

由于这个假设，message 的类型是 `string`。而不是我们可能预期的 `undefined` 或 `string`。

如果我们使用元组类型，会得到错误：

```typescript
const messages: [string] = ['Hello'];
```

```typescript
// @ts-expect-error: Tuple type 'string' of length '1' has no element
// at index 1. (2493)
const message = messages[1];
```

使用 `as const` 会产生相同的效果，因为它会导致元组类型的推断。

## 第 21 章

## 函数类型

+ 目录
- 21.1 定义静态类型函数 ............................................................................ 174
  - 21.1.1 函数声明 ................................................................................................. . . . . 174
  - 21.1.2 箭头函数 ..................................................................................... . . . . 174
- 21.2 函数类型 ................................................................................................................ 174
  - 21.2.1 函数类型签名 ................................................................................................... 174
  - 21.2.2 带有调用签名的接口 ...................................................................................... 175
  - 21.2.3 检查值是否匹配函数类型 .......................................................................... 175
- 21.3 参数 ............................................................................................................................................ 176
  - 21.3.1 什么时候参数必须进行类型注解？ .......................................................................... 176
  - 21.3.2 可选参数 ...................................................................................................... 177
  - 21.3.3 剩余参数 ......................................................................................... 179
  - 21.3.4 命名参数 ....................................................................................... 179
  - 21.3.5 this 作为参数（高级） ................................................................................. 180
- 21.4 载载（高级） ..................................................................................................... 181
  - 21.4.1 重载函数声明 ................................................................................ 181
  - 21.4.2 通过接口重载 ...................................................................... 183
  - 21.4.3 字符串参数上的重载（事件处理等） ........................................................ 183
  - 21.4.4 方法重载 ................................................................................................. 183
- 21.5 可分配性（高级） .......................................................................................................... 184
  - 21.5.1 可分配性规则 ....................................................................................... 185
  - 21.5.2 函数赋值规则的后果 ........................................................ 185
- 21.6 本章的延伸阅读和来源 ................................................................................ 186

本章探讨了 TypeScript 中函数的静态类型。

> 在本章中，“函数”指的是关于函数的“函数或方法或构造函数”，这些关于函数（特别是关于参数处理方面）的描述也适用于方法和构造函数。

## 21.1 定义静态类型函数

### 21.1.1 函数声明

这是一个 TypeScript 中函数声明的示例：

```typescript
function repeat1(str: string, times: number): string { // (A)
  str.repeat(times);
}
assert.equal(
  repeat1('*', 5, '******');
```

- 参数：如果编译器选项 `--noImplicitAny` 被推断。这通常是开启的，如果是 `--strict`，则每个参数的类型必须是可推断的或显式指定的（我们稍后会详细查看推断）。在这种情况下，无法推断，这就是为什么 `str` 和 `times` 有类型注解。
- 返回值：默认情况下，函数的返回类型是推断的。这通常足够了。在这种情况下，我们选择显式指定 `repeat1()` 的返回类型为 `string`（行 A 中的最后一个类型注解）。

### 21.1.2 箭头函数

`repeat1()` 的函数版本如下：

```typescript
const repeat2 = (str: string, times: number): string => {
  str.repeat(times);
};
```

在这种情况下，我们也可以使用表达式体：

```typescript
const repeat3 = (str: string, times: number): string =>
str.repeat(times);
```

## 21.2 函数类型

### 21.2.1 函数类型签名

我们可以通过函数类型签名为函数定义类型：

```typescript
type Repeat = (str: string, times: number) => string;
```

这种函数的类型名为 `Repeat`。其他情况下，它匹配所有如下函数：

- `(str: string, times: number) => string`

### 21.2.2 带有调用签名的接口

我们也可以使用接口来定义：

```typescript
interface Repeat {
  (str: string, times: number): string;
}
```

### 21.2.3 检查值是否匹配函数类型

176

### 21.2.3.2 函数声明（简单）

检查函数声明更复杂：

```typescript
function pred2(str: string): boolean {
  return str.length > 0;
}
```

// 将函数赋值给带类型注解的变量
const pred2ImplementsStringPredicate: StringPredicate = pred2;

### 21.2.3.3 函数声明（复杂）

解决方案有点（也就是说，如果你不完全理解没关系，但展示了多种特性）：

```typescript
function pred3([...str]: Parameters<StringPredicate>
  : ReturnType<StringPredicate> {
  return str.length > 0;
}
```

- 我们使用 `Parameters<>` 提取参数类型的元组。三个点表示剩余参数，它将所有参数收集到一个元组/数组中。`[str]` 对元组进行解构。（在本章稍后会介绍剩余参数。）
- 返回值：我们使用 `ReturnType<>` 提取返回类型。





## 21.3 参数

```typescript
interface Array<T> {
  map<U>(
    callback(value: T, index: number, array: T[]) => U,
    thisArg?: any
  ): U[];
  // ...
}
```

### 21.3.2 可选参数

在本节中，我们将查看允许参数被省略的几种方法。

### 21.3.2.1 可选参数：str?: string

如果在参数名称后面加上一个问号，该参数就变成了可选的，在调用函数时可以省略：

```typescript
function trim(str?: string): string {
  // str 的内部类型;
  // %inferred-type: string | undefined
  str;

  if (str === undefined) {
    return '';
  }
  return str.trim();
}
```

```typescript
// trim 的外部类型:
// %inferred-type: (str?: string | undefined) => string
trim;
```

这是 trim() 的调用方式：

```typescript
assert.equal(
  trim('\n abc \t'), 'abc');

assert.equal(
  trim(), '');

  // `undefined` 等同于省略参数
assert.equal(
  trim(undefined), '');
```

### 21.3.2.2 联合类型：str: undefined|string

从外部看，`trim1()` 的参数 str 的类型为 `string|undefined`。因此，`trim(1)` 大多等同于以下函数。

```typescript
function trim2(str: undefined|string): string {
  // str 的内部类型;
// %inferred-type: string | undefined
str;

  if (str === undefined) {
    return '';
  }
return str.trim();
}
```

```typescript
 // trim2 的外部类型:
// %inferred-type: (str: string | undefined) => string
trim2;
```

`trim2()` 与 `trim1()` 的唯一不同在于在函数调用中不能省略参数（A 行）。换说：当我们省略类型为 `undefined|T` 的参数时，必须是显式的。

```typescript
assert.equal(
trim2('\n\ abc \t'), 'abc');
```

```typescript
// @ts-expect-error: 预期 1 个参数，但得到了 0 个。(2554)
trim2(); // (A)
```

```typescript
assert.equal(
trim2(undefined), ''); // OK!
```

### 21.3.3 参数默认值：str = 

如果我们为 str 提供一个默认值，就不需要提供类型注解，因为 TypeScript 可以推断出类型：

```typescript
function trim3(str = ''): string {
// str 的内部类型:
// %inferred-type: string
str;

  return str.trim();
}
```

```typescript
 // trim3 的外部类型:
// %inferred-type: (str?: string) => string
trim3;
```

注意，str 的内部类型是 `string`，因为默认值确保了它永远不会是 `undefined`。

让我们调用 trim3()：

```typescript
assert.equal(
trim3('\n\ abc \t'), 'abc');
```

```typescript
// 省略参数会触发参数默认值:
assert.equal(
trim3(), '');
```

```typescript
// `undefined` 是允许的并触发参数默认值:
assert.equal(
trim3(undefined), '');
```

### 21.3.2.4 参数默认值加类型注解

我们也可以同时指定类型和默认值：

```typescript
function trim4(str: string = ''): string {
  return str.trim();
}
```

### 21.3.3 剩余参数

### 21.3.3.1 使用 Array 类型的剩余参数

剩余参数将所有剩余参数收集到一个数组中。因此，它的静态类型通常是一个 `Array`。在接下来的示例中，`parts` 是一个剩余参数：

```typescript
function join(separator: string,...parts: string[]) {
  return parts.join(separator);
}
```

```typescript
assert.equal(
join('-', 'state', 'of', 'the', 'art'),
  'state-of-the-art');
```

### 21.3.3.2 使用 tuple 类型的剩余参数

下一个示例演示了特性：

- 我们可以对剩余参数使用元组类型，例如 `[string, number]`。
- 我们可以解构剩余参数（而不只是普通参数）。

```typescript
function repeat1(...[times: number]): string {
  return str.repeat(times);
}
```

repeat1() 等于以下函数：

```typescript
function repeat2(str: string, times: number): string {
  return str.repeat(times);
}
```

### 21.3.4 命名参数

命名参数是 JavaScript 中一种流行的模式，使用对象字面量来给每个参数命名。它的样子如下：

```typescript
assert.equal(
  padStart({str: '7', len: 3, fillStr: '0'}),
  '007');
```

在 JavaScript 中，函数可以解构来访问命名参数的值。然而，在 TypeScript 中，我们必须额外为对象字面量指定类型，这导致了冗余：

```typescript
function padStart({ str, len, fillStr = ' ' } // (A)
  { str: string, len: number, fillStr?: string }) // (B)
```





## 21.4 重载（进阶）

### 21.4.2 通过接口重载

在接口中，我们可以拥有多个不同的调用签名。这使得我们能够在能够在下面的示例中使用 `GetFullName` 接口进行重载：

```typescript
interface GetFullName {
  (customerOrMap: Customer): string;
  (customerOrMap: Map<string, Customer>, id: string): string;
}
```

```typescript
const GetFullName: GetFullName = (customerOrMap: Customer | Map<string, Customer>, id?: string) => {
  if (id === undefined) {
    const customer = customerOrMap as Map<string, Customer>.get(id);
    if (customer === undefined) {
      throw new Error('Unknown ID: ' + id);
    }
    return customer.fullName;
  } else {
    if (id !== undefined) throw new Error();
    return (customerOrMap as Customer).fullName;
  }
};
```

### 21.4.3 字符串参数重载（事件处理等）

在下一个示例中，我们重载并使用了字符串类型（如 'click'）。这允许我们根据参数类型的值更改参数监听器的类型：

```typescript
function addEventListener(elem: HTMLElement, type: 'click',
  listener: (event: MouseEvent) => void): void;
function addEventListener(elem: HTMLElement, type: 'keypress',
  listener: (event: KeyboardEvent) => void): void;
function addEventListener(elem: HTMLElement, type: string, // (A)
  listener: (event: any) => void): void {
  elem.addEventListener(type, listener); // (B)
}
```

在这种情况下，要获取实现部分的类型（从 A 行开始）以便正体中的语句（B 行）正常工作是比较困难的。作为最后手段，我们始终可以使用 `any` 类型。

### 21.4.4 重载方法

### 21.4.4.1 重载具体方法

下一个示例演示了方法的重载：方法 `.add()` 被重载了。

```typescript
class StringBuilder {
  #data = '';

  add(num: number): this;
  add(bool: boolean): this;
  add(str: string): this;
  add(value: any): this {
    this.#data += String(value);
    return this;
  }

  toString() {
    return this.#data;
  }
}
```

```typescript
const sb = new StringBuilder();
sb.add('I can see ')
  .add(3)
  .add(' monkeys!');
assert.equal(
  sb.toString(), 'I can see 3 monkeys!'
);
```

#### 21.4.2 重载接口方法

`Array.from()` 的类型定义是一个重载接口方法的示例：

```typescript
interface ArrayConstructor {
  from<T>(arrayLike: ArrayLike<T>): T[];
  from<T, U>(
    arrayLike: ArrayLike<T>,
    mapfn: (v: T, k: number) => U,
    thisArg?: any
  ): U[];
}
```

- 在第一个签名中，返回的 Array 的元素类型与参数相同。
- 在第二个签名中，返回的 Array 的元素类型与 `mapfn` 的结果相同。此版本的 `Array.from()` 与 `Array.prototype.map()` 类似。

## 21.5 可赋值性（进阶）

在本节中，我们查看赋值性的类型兼容规则：类型为 `Src` 的函数是否可以转换为类型为 `Trg` 的存储位置（变量、对象属性、参数等）？

理解赋值性有助于我们回答诸等问题：

- 给定形式参数的函数类型签名，哪些函数可以作为实际参数传递函数调用？
- 给定属性的函数类型签名，哪些函数可以赋值给它？

### 21.5.1 可赋值性规则

在本小节中，我们检查可赋值性的通用规则（包括函数的规则）。在本小节中，我们探索这些规则对函数意味着什么。

如果满足以下任何条件，则 `Src` 可赋值给类型 `Trg`：

- `Src` 和 `Trg` 是完全相同的类型。
- `Src` 或 `Trg` 是 `any` 类型。
- `Src` 是字符串字面量且 `Trg` 是原始类型 `String`。
- `Src` 是联合类型且 `Src` 的每个组成部分都可赋值给 `Trg`。
- `Src` 和 `Trg` 是函数类型：
  - `Trg` 具有剩余参数，或者 `Src` 的必需参数数量小于或等于 `Trg` 的参数总数。
  - 对于在两个签名中都存在的参数，`Trg` 中的每个参数类型都可赋值给 `Src` 中对应的参数类型。
  - `Trg` 的返回类型为 `void` 或者 `Src` 的返回类型可赋值给 `Trg` 的返回类型。
- （其余情况省略。）

### 21.5.2 函数赋值规则的后果

在本小节中，我们查看赋值规则对以下两个函数 `targetFunc` 和 `sourceFunc` 意味着什么：

```typescript
const targetFunc: Trg = sourceFunc;
```

#### 21.5.2.1 参数和结果的类型

- 目标参数类型必须赋值给对应的源参数类型。
  - 目标接受的任何内容源也必须接受。
- 源返回类型必须赋值给目标返回类型。
  - 源返回的任何内容必须与目标设定的预期兼容。

示例：
```typescript
const trg1: (x: string) => any = (x: number) => x;
```

（注：原文此处似乎存在截断或错乱，已按原文结构翻译）





## 22.2 与类型断言相关的结构

```typescript
// expression of type 'string' can't be used to index type '{}'.
// [...]
dict[key];
```

```typescript
return (dict as Dict)[key]; // (A)
} else {
throw new Error();
}
}
```

22 类型断言（与转换相关）

### 22.2.1 非空断言操作符（后缀 !）

如果一个值的类型是包含 `undefined` 或 `null` 类型的联合类型，非空断言操作符会从联合类型中移除这些类型。我们是在告诉 TypeScript：“这个值可能是 undefined 或 null。” 结果，我们可以执行那些被由于这两个值而阻止的操作——例如：

```typescript
const tsName = 'Jane' as (null | string);
```

```typescript
// ts-expect-error: Object is possibly 'null'.
ttsName.length;
```

```typescript
assert.equal(
ttsName.length, 4); // OK
```

### 22.2.1.1 示例 - Maps：.get(key) vs .has(key)

在使用 Map 方法 .has(key) 后，我们知道 Map 包含给定的键。遗憾的是，get(key) 的结果并没有反映这一知识，这就是为什么我们必须使用非空断言操作符：

```typescript
function getLength(tsMap: Map<string, string>, key: string): number {
  if (tsMap.has(key)) {
    const value = tsMap.get(key)!; // (A)
    return value.length;
  }
}
```

当 Map 的值不会为 `undefined` 时，我们可以避免使用非空断言操作符。可以通过检查 .get() 的结果是否为 `undefined` 来检测缺失的条目：

```typescript
function getLength(tsMap: Map<string, string>, key: string): number {
  // %inferred-type: string | undefined
  const value = tsMap.get(key);
  if (value === undefined) { // (A)
return -1;
}
```

```typescript
// %inferred-type: string
value;
```

```typescript
return value.length;
}
```

### 22.2.2 确定赋值断言

如果开启了严格属性初始化（strict property initialization），我们需要告诉 TypeScript 我们确实初始化了某些属性——尽管它认为我们没有。

这是一个 TypeScript 即使不该报错却报错的示例：

```typescript
class Point1 {
// @ts-error: Property 'x' has no initializer and is not definitely
// assigned in the constructor.
x: number;

// @ts-error: Property 'y' has no initializer and is not definitely
// assigned in the constructor.

constructor() {
  this.initProperties();
}
initProperties() {
  this.x = 0;
  this.y = 0;
}
```

如果我们在 A 行和 B 行使用确定赋值断言（感叹号 `! `），错误就会消失：

```typescript
class Point2 {
x!: number; // (A)
y!: number; // (B)
constructor() {
  this.initProperties();
}
initProperties() {
  this.x = 0;
  this.y = 0;
}
```

## 第 23 章

## 类型守卫与断言函数

| 目录 | 页码 |
| :--- | :--- |
| 23.1 静态类型何时过于宽泛？ | 194 |
| 23.1.1 通过 if 和类型守卫进行收窄 | 194 |
| 23.1.2 通过 switch 和类型守卫进行收窄 | 195 |
| 23.1.3 类型过于宽泛的其他情况 | 195 |
| 23.1.4 `unknown` 类型 | 196 |
| 23.2 通过内置类型守卫进行收窄 | 196 |
| 23.2.1 严格相等 (==) | 196 |
| 23.2.2 typeof, instanceof, Array.isArray | 197 |
| 23.2.3 通过 in in 运算符检查不同的属性 | 197 |
| 23.2.4 检查共享属性的值（判别式联合） | 198 |
| 23.2.5 收窄点符号名称 | 199 |
| 23.2.6 收窄数组元素类型 | 200 |
| 23.3 用户自定义的类型守卫 | 201 |
| 23.3.1 用户自定义类型守卫示例：isArrayWithInstance() | 201 |
| 23.3.2 用户自定义类型守卫示例：typeof() | 202 |
| 23.4 断言函数 | 204 |
| 23.4.1 TypeScript 对断言函数的支持 | 204 |
| 23.4.2 断言布尔值 | 204 |
| 23.4.3 收窄参数的类型 | 205 |
| 23.5.1 用户定义的类型守卫 | 205 |
| 23.5.2 断言函数的替代方案 | 206 |
| 23.6.1 技术：强制转换 | 206 |
| 23.6.2 技术：抛出异常 | 207 |

### 23.1 静态类型何时过于宽泛？

在 TypeScript 中，一个值的类型可能过于宽泛。例如：

```typescript
const tsName = 'Jane' as (null | string);
```

```typescript
// ts-expect-error: Object is possibly 'null'.
ttsName.length;
```

```typescript
assert.equal(
ttsName.length, 4); // OK
```

### 23.1.1 通过 if 和类型守卫进行收窄

为了理解静态类型如何变得过于宽泛，请考虑以下内容：

```typescript
function getScore(value: number|string): number {
  if (typeof value === 'number') { // (A)
    //inferred-type: number
    return value;
  }
  if (typeof value === 'string') { // (B)
    //inferred-type: string
    return value.length;
  }
  throw new Error('Unsupported value: ' + value);
}
```

在本章中，我们将类型解释为值的集合。（有关这种解释和另一种解释的更多信息，请参阅 §11 “什么是类型？”）。

**什么是类型的收窄和守卫？**

在 A 行和 B 行开始的 块内部，由于我们执行了检查，value 的静态类型发生了变化。我们现在处理的是原始类型 `number|string` 的子集。这种缩小类型的方法被称为收窄（narrowing）。检查 `typeof` 类似的运行时操作被称为类型守卫（type guards）。

### 23.1.2 通过 switch 和类型守卫进行收窄

如果我们使用 `switch` 代替下面的代码，收窄同样有效：

```typescript
function getScore(value: number|string): number {
  switch (typeof value) {
    case 'number':
      //inferred-type: number
      return value;
    case 'string':
      //inferred-type: string
      return value.length;
    default:
      throw new Error('Unsupported value: ' + value);
  }
}
```

### 23.1.3 类型过于宽泛的其他情况

这些是类型过于宽泛的更多示例：

- 可空类型：
  function func1(arg: null|string) {}
  function func2(arg: undefined|string) {}
- 判别式联合：
  type Teacher = { kind: 'Teacher', teacherId: string };
  type Student = { kind: 'Student', studentId: string };
  type Attendee = Teacher | Student;
- 可选参数的类型：
  function func4(arg?: string) {
    //inferred-type: string | undefined
    arg;
  }





### 23.1.4 unknown 类型

如果一个值的类型为 `unknown`，我们几乎无法对它大做任何操作，必须先收窄类型（A 行）：

```typescript
function parseStringLiter(stringLiteral: string): string {
  const result: unknown = JSON.parse(stringLiteral);
  if (typeof result == 'string') { // (A)
    return result;
  }
  throw new Error('Not a string literal: ' + stringLiteral);
}
```

换句话说：类型太通用了，我们必须收窄它。在某种程度上，`unknown` 也是一种联合类型（所有类型的联合类型）。

## 23.2 通过内置类型守卫收窄

正如我们所看到的，类型守卫（type guard）是一种操作，根据操作数在运行时是否符合某些标准来返回 true 或 false。TypeScript 的类型推断支持类型守卫，在结果为 true 时通过缩小操作数的静态类型来提供支持。

### 23.2.1 严格相等 (===)

严格相等可以作为类型守卫工作：

```typescript
function func(value: unknown) {
  if (value === 'abc') {
    // 推断类型: "abc"
    value;
  }
}
```

对于某些联合类型，我们可以使用 `===` 来区分它们的各个组件：

```typescript
interface Book {
  title: null | string;
  isbn: string;
}
```

```typescript
function getTitle(book: Book) {
  if (book.title === null) {
    // 推断类型: null
    return 'Untitled';
  } else {
    // 推断类型: string
    return book.title;
  }
}
```

## 23.2 通过内置类型守卫收窄类型

使用 `===` 包含、`!==` 排除联合类型组件仅当该组件是单例类型（只有一个成员的类型）时才有效。`null` 类型的唯一成员是 `null`。

### 23.2.2 typeof, instanceof, Array.isArray

这些是常见的内置类型守卫：

```typescript
function func(value: Function|Date|number[]) {
  if (typeof value === 'function') {
    // 推断类型: Function
    value;
  }

  if (value instanceof Date) {
    // 推断类型: Date
    value;
  }

  if (Array.isArray(value)) {
    // 推断类型: number[]
    value;
  }
}
```

注意 `value` 的静态类型在 `if` 块内部是如何收窄的。

### 23.2.3 通过 in 检查不同属性

如果用于检查不同属性，`in` 操作符是一个类型守卫：

```typescript
type FirstOrSecond =
  | { first: string }
  | { second: string };

function func(firstOrSecond: FirstOrSecond) {
  if ('second' in firstOrSecond) {
    // 推断类型: { second: string }
    firstOrSecond;
  }
}
```

注意以下检查将不起：

```typescript
function func(firstOrSecond: FirstOrSecond) {
  // @ts-expect-error: 'second' 不存在于类型 'FirstOrSecond'
  if (firstOrSecond.second !== undefined) {
    // ...
  }
}
```

在这种情况下，问题在于如果没有收窄，我们无法访问类型为 `FirstOrSecond` 的值的 `.second` 属性。

### 23.2.3.1 in 操作符无法收窄联合类型

遗憾的是，`in` 操作符只能帮助处理对象类型：

```typescript
function func(obj: object) {
  if ('name' in obj) {
    // 推断类型: object
    obj;

    // @ts-expect-error: 属性 'name' 不存在于类型 'object'
    obj.name;
  }
}

## 23.2.4 检查共享属性（判别联合类型）

在判别联合类型（discriminated unions）中，联合类型具有一个或多个值不同的属性。此类属性被称为判符（discriminants）。

检查判符的值是一个类型守卫：

```typescript
type Teacher = { kind: 'Teacher'; teacherID: string };
type Student = { kind: 'Student'; studentID: string };
type Attendee = Teacher | Student;

function getId(attendee: Attendee) {
  switch (attendee.kind) {
    case 'Teacher':
      // 推断类型: kind: "Teacher"; teacherID: string;
      attendee;
      return attendee.teacherID;
    case 'Student':
      // 推断类型: kind: "Student"; studentID: string;
      attendee;
      return attendee.studentID;
    default:
      throw new Error();
  }
}
```

在之前的例中，`.kind` 是一个判符：联合类型 `Attendee` 的每个组件都有这个属性，且具有唯一的值。

## 23.2 通过内置类型守卫收窄

`if` 语句和相等检查的工作与 `switch` 语句类似：

```typescript
function getID(attendee: Attendee) {
  if (attendee.kind === 'Teacher') {
    // 推断类型: { kind: "Teacher"; teacherID: string; }
    attendee;
    return attendee.teacherID;
  } else if (attendee.kind === 'Student') {
    // 推断类型: { kind: "Student"; studentID: string; }
    attendee;
    return attendee.studentID;
  } else {
    throw new Error();
  }
}
```

### 23.2.5 点符号名称收窄

我们还可以通过属性名链收窄属性（甚至是嵌套属性）的类型：

```typescript
type MyType = {
  prop?: number | string;
};
function func(arg: MyType) {
  if (typeof arg.prop === 'string') {
    // 推断类型: string
    arg.prop; // (A)
  }

  // (注意：OCR 文本在这里似乎被 ".forEach" 损坏了，
  // 但根据上下文指的是属性访问逻辑)
  
  // 推断类型: string
  arg.prop;

  arg = {};

  // 推断类型: string | number | undefined
  arg.prop; // (C)
}
```

让我们看看之前代码中的几个位置：

- A 行：我们收窄了类型。
- B 行：（文本文本）
- C 行：我们收窄了类型。

### 23.2.6 收窄数组

如果我们使用 `every()` 来检查所有元素是否非空，`every()` 不会收窄类型：

```typescript
const mixedValues = [1, undefined];
```

（注意：该部分的 OCR 文本是高度碎片/混乱的，但遵循 TypeScript `every` 与 `NonNullable<T>` 的逻辑。）

## 23.3 自定义类型守卫

TypeScript 允许我们定义自己的类型守卫——例如：

```typescript
function isFunction(value: unknown): value is Function {
  return typeof value === 'function';
}
```

`isFunction` 的返回值是一个类型谓言。它是 `isFunction()` 类型签名的一部分：

```typescript
// 推断类型: (value: unknown) => value is Function
isFunction();
```

自定义类型守卫必须返回布尔值。如果 `isFunction(x)` 返回 true，TypeScript 会将实际参数 `x` 的类型收窄为：

```typescript
function func(arg: unknown) {
  if (isFunction(arg)) {
    // 推断类型: Function
    arg; // 类型收窄了
  }
}
```

注意 TypeScript 并不知道我们是如何计算自定义类型守卫的结果的。它在我们使用的检查方法上提供了很大的自由度。例如，我们可以这样实现 `isFunction`：

```typescript
function isFunction(value: any): value is Function {
  try {
    value(); // (A)
  return true;
  } catch {
    return false;
  }
}
```

我们必须对参数值使用 `any`，因为 `unknown` 类型不允许我们在 A 行中进行函数调用。

### 23.3.1 自定义类型守卫示例：isArrayWithInstanceof()

- 这种数组的类型守卫工作原理类似于 `Array.isArray()`，但它还会检查所有数组元素是否为 `T` 的实例。
- 因此，如果该函数返回 `true`，`arr` 的类型将被收窄为 `Array<T>`。
- 警告：这种类型守卫可能会导致不安全——例如：我们可以使用 `arr` 的另一个引用添加不是 `T` 的元素。那么 `arr` 就不具有 `Array<T>` 类型。




202

23 类型守卫与断言函数

- *  anymore。

```typescript
function isArrayWithInstancesOf<T>(
  arr: any, Class: new (...args: any[])=>T
  ): arr is Array<T>
{
  if (!Array.isArray(arr)) {
    return false;
  }
  if (arr.every(elem => elem instanceof Class)) {
    return false;
  }

// //inferred-type: any[]
arr; // (A)

return true;
}
```

在行 A 中，我们可以看到 arr 的推断类型不是 `Array<T>`，但我们的检查确保了它是当前的。这就是为什么我们可以返回 `true`。TypeScript 信任我们，并在我们使用 `isArrayWithInstancesOf()` 时将类型收窄为 `Array<T>`：

```typescript
const value: unknown = {};
if (isArrayWithInstancesOf(value, RegExp)) {
  // //inferred-type: RegExp[]
  value;
}
```

## 23.2 用户定义类型守卫的示例：isTypeOf()

### 23.2.1 第一次尝试

这是在 TypeScript 中实现 `typeof` 的第一次尝试：

```typescript
/**
* `typeof` 运算符的实现。
 */
function isTypeOf<T>(value: unknown, prim: T): value is T {
  if (prim === null) {
    return value === null;
  }
  return value !== null && (typeof prim) === (typeof value);
}
```

理想情况下，我们能够通过字符串指定 value 的预期类型（即 `typeof` 的结果之一）。但这样我们就必须从字符串中推导出类型 T，而这并不直观如何如何做到（我们很快就会有一种方法）。作为一种替代方案，我们通过 T 的一个成员 `prim` 来指定 T：

```typescript
const value: unknown = {};
```

## 23.3 用户定义类型守卫

```typescript
if (isTypeof(value, 123)) {
  // %inferred-type: number
  value;
}
```

### 23.3.2.2 使用函数重载

更好的解决方案是使用重载（省略了若干情况）：

```typescript
/**
 * `typeof` 运算符的部分实现。
 */
function isTypeof(value: any, typeString: 'boolean'): value is boolean;
function isTypeof(value: any, typeString: 'number'): value is number;
function isTypeof(value: any, typeString: 'string'): value is string;
function isTypeof(value: any, typeString: string): boolean {
  return typeof value === typeString;
}
```

```typescript
const value = unknown {};
if (isTypeof(value, 'boolean')) {
  // %inferred-type: boolean
  value;
}
```

（这种方法是 Nick Fisher 的想法）。

### 23.3.2.3 使用接口作为类型映射的映射

另一种方案是使用接口作为从字符串到类型的映射（省略了若干情况）：

```typescript
interface TypeMap {
  boolean: boolean;
  number: number;
  string: string;
}
```

```typescript
/**
 * `typeof` 运算符的部分实现。
 */
function isTypeof<T extends keyof TypeMap>(value: any, typeString: T) : value is TypeMap[T] {
  return typeof value === typeString;
}
```

```typescript
const value = unknown {};
if (isTypeof(value, 'string')) {
  // %inferred-type: string
}

value;
```

（这种方法是 Ran Lottem 的想法。）

## 23.4 断言函数

断言函数检查其参数是否符合某些标准，如果不符合则抛出异常。例如，许多语言支持的一种断言函数 `assert(cond)` 在布尔条件 `cond` 为假时会抛出异常。

Node.js 通过内置的 `assert` 模块支持 `assert`。以下代码在行 A 中使用了它：

```typescript
import assert from 'assert';
function removeFilename(filename: string) {
  const dotIndex = filename.lastIndexOf('.');
  assert(dotIndex >= 0); // A
  return filename.slice(0, dotIndex);
}
```

### 23.4.1 TypeScript 对断言函数的支持

TypeScript 的类型推断为断言函数提供了特殊支持，如果我们将此类函数的返回类型标记为断言签名。关于我们如何从函数返回以及返回什么，断言签名等同于 `void`。然而，它会触发类型收窄。

有两种断言签名：

- 断言布尔参数：`asserts «cond»`
- 断言参数类型：`asserts «arg» is «type»`

### 23.4.2 断言布尔参数：asserts «cond»

在下面的示例中，断言签名条件规定参数条件必须为真。否则，将抛出异常。

```typescript
function assertTrue(condition: boolean): asserts condition {
  if (!condition) {
    throw new Error();
  }
}
```

这是 `assertTrue()` 导致类型收窄的方式：

```typescript
function func(value: unknown) {
  assertTrue(value instanceof Set);

  // %inferred-type: Set<any>
  value;
}
```

## 23.5 快速参考：用户定义类型守卫

我们使用断言函数的方式类似于类型守卫，但不是使用条件语句，而是触发异常。

### 23.5.1 断言参数类型：asserts «arg» is «type»

在下面的示例中，断言签名规定参数必须具有该类型。否则，将抛出异常。

```typescript
function isTypeof(value: any, typeString: string): value is boolean {
  return typeof value === typeString;
}
```

```typescript
const value = unknown {};
if (isTypeof(value, 'string')) {
  // %inferred-type: string
  value;
}
```

### 23.5.2 断言布尔参数：asserts «cond»

在下面的示例中，断言签名规定布尔条件必须为真。否则，将抛出异常。

```typescript
function assertTrue(condition: boolean): asserts condition {
  if (!condition) {
    throw new Error();
  }
}
```

## 23.6 断言函数的替代方案

断言函数收窄参数的类型，但不是通过条件语句，而是通过触发异常。

### 23.6.1 技术：强制转换

强制转换返回一个具有新类型的现有值——例如：

```typescript
function forceNumber(value: unknown): number {
  if (typeof value !== 'number') {
    throw new TypeError();
  }
  return value;
}
```

```typescript
const valuea: unknown = 123;
// %ferred-type: number
const valueb = forceNumber(valuea);

const value2: unknown = 'abc';
assert.throws(() => forceNumber(value2));
```

对应的断言函数如下：

```typescript
function assertNumber(value: unknown): asserts value is number {
  if (typeof value != 'number') {
    throw new TypeError();
  }
}
```

```typescript
const value1: unknown = 123;
assertNumber(value1);
// inferred-type: number
value1;
```

```typescript
const value2: unknown = 'abc';
assert.throws(() => assertNumber(value2));
```

强制转换是一种多功能技术，用途超过了断言函数。例如，我们可以转换：

- 从输入格式（如 JSON schema）易于编写
- 从易于代码处理的输出格式

更多信息，请参阅 [24.3.5 “数据的外部与内部表示”](24.3.5)。

### 23.6.2 技术：在抛出异常

考虑以下代码：

```typescript
function getLengthValueOf(strMap: Map<string, string>, key: string) : number {
  if (strMap.has(key)) {
    const value = strMap.get(key);

    // inferred-type: string | undefined
    value; // 类型检查之前

    // 我们知道 value 不可能为 `undefined`
    if (value === undefined) { // (A)
      throw new Error();
    }

    // inferred-type: string
    value; // 类型检查之后

    return value.length;
  }
}
```

与其从行 A 开始的 if 语句，我们也可以使用断言函数：

```typescript
assertNotUndefined(value);
```



如果我们不想写这样的函数，抛出异常是一个快速的替代方案。与调用断言函数类似，这种技术会更新静态类型。

## 23.7 @hqoss/guards: 带有类型守卫的库

@hqoss/guards 提供了一系列用于 TypeScript 的类型守卫（type guards），例如：

- 基础类型：isBoolean(), isNumber() 等。
- 特定类型：isObject(), isNull(), isFunction() 等。
- 各种检查：isNonEmptyArray(), isInteger() 等。

# 第 24 章

## 验证外部数据

- 目录
- 24.1 JSON schema ................................................................. . . . . . . . . . . . 209
- 24.1.1 一个 JSON schema 示例 . . . . . . . . . . . . . . . . . . . 210
- 24.2 TypeScript 中的数据验证方法 . . . . . . . . . 211
- 24.2.1 不使用 JSON schema 的方法 . . . . . . . . . . . . . . . 211
- 24.2.2 使用 JSON schema 的方法 . . . . . . . . . . . . . . . 211
- 24.2.3 选择库 . . . . . . . . . . . . . . . . . . . . . . . . 211
- 24.3 示例：通过 Zod 库验证数据 . . . . . . 212
- 24.3.1 通过 Zod 的 builder API 定义“data” . . . . . 212
- 24.3.2 验证数据 . . . . . . . . . . . . . . . 212
- 24.3.3 类型守卫 (Type guards) . . . . . . 213
- 24.3.4 从 Zod schema 导出静态类型 . . . . 213
- 24.3.5 数据的外部表示与内部表示 . . . . 213
- 24.4 结论 ................................................................................. . . . . 214

数据验证确保我们拥有的数据具有所需的结构和内容。
在 TypeScript 中，当我们接收外部数据时，验证变得非常重要：

- 从文件解析的数据
- 从服务接收的数据

在这些情况下，我们期望数据符合已有的静态类型，但无法确定。与我们创建的数据相比，TypeScript 会持续检查一切。

本章介绍了如何在 TypeScript 中验证外部数据。

## 24.1 JSON schema

在探索 TypeScript 的数据验证方法之前，我们需要查看 JSON schema，因为许多方法都是基于它的。

JSON schema 的核心思想是表示 JSON 数据的（结构、内容、静态类型）。也就是说，元数据是以相同的格式表示的。

JSON schema 的用例：

- 验证 JSON 数据：如果我们有数据的 schema 定义，可以使用工具检查数据是否正确。数据还可以自动修复缺失的属性。
- 文档 JSON 数据格式：核心 schema 定义可以视为文档。但 JSON schema 额外支持描述、弃用说明等。这些机制不是用于验证，而是用于文档。
- IDE 对数据编辑的支持：例如，Visual Studio 支持 JSON schema。如果 JSON 文件有 schema，我们就能获得许多编辑功能：自动补全、错误高亮等。值得注意的是，VS Code 对 package.json 文件的支持完全基于 JSON schema。

### 24.1.1 一个 JSON schema 示例

此示例来自 json-schema.org 网站：

```json
{
  "$id": "https://example.com/geographical-location.schema.json",
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "经纬度值",
  "description": "地理坐标。",
  "required": [ "latitude", "longitude"],
  "type": "object",
  "properties": {
    "latitude": {
      "type": "number",
      "minimum": -90,
      "maximum": 90
    },
    "longitude": {
      "type": "number",
      "minimum": -180,
      "maximum": 180
    }
  }
}
```

以下 JSON 数据符合该 schema：

```json
{
  "latitude": 48.85809,
  "longitude": 2.29469
}
```

## 24.2 TypeScript 中的数据验证方法

本节提供了 TypeScript 中验证数据的各种方法的要概述。对于每种方法，我都列出了一个或多个支持该方法的库。在库方面，我不打算详尽列举，因为这个领域变化非常快。

### 24.2.1 不使用 JSON schema 的方法

- 方法：调用 builder 方法和函数来同时产生验证（运行时）和静态类型（编译时）。库包括：
    - zod（后文将演示）
    - runtypes
    - io-ts
- 方法：调用 builder 方法并只产生验证。采用这种方法的库通常侧重于让验证尽可能通用：
    - joi
    - yup
- 方法：编译 TypeScript 类型以在编译时验证代码。库：
    - superstruct-transformer
    - type-check-macro

### 24.2.2 使用 JSON schema 的方法

- 方法：将 TypeScript 类型转换为 JSON schema。库：
    - ts-json-schema-generator
    - json-schema-typescript
- 方法：将 JSON schema 转换为 TypeScript 类型。库：
    - json-schema-to-typescript
    - decoder
- 方法：通过 JSON schemas 验证 JSON 数据。此功能对于以下包也有用：
    - ajv
    - validator

### 24.2.3 选择库

使用哪种方法以及哪种库取决于我们的需求：

- 如果我们从 TypeScript 类型开始，且数据（来自配置文件等）符合这些类型，那么支持静态类型的 builder API 是一个很好的选择。
- 如果我们的起点是 JSON schema，那么我们应该考虑支持 JSON schema 的库之一。
- 如果我们处理的是混乱的数据（例如表单），我们可能需要一种更灵活的方法，在这种方法中静态类型起的作用较小。

## 24.3 示例：通过 Zod 库验证数据

### 24.3.1 通过 Zod 的 builder API 定义“data”

Zod 有一个既能产生类型又能验证函数的 API。该 API 使用如下：

```typescript
import * as z from 'zod';
const FileInputSchema = z.object({
  file: z.string(),
  author: z.string().optional(),
  tags: z.array(z.string()).optional(),
});
```

对于较大的 schema，有必要将它们拆分为多个声明。Zod 可以冗余地维护静态类型：

```typescript
type FileInput = {
  file: string;
  author?: string;
  tags?: string[];
};
```

为什么要冗余？

- 它更易读。
- 有助于迁移到不同的库或方法，如果我需要的话。这有助于保持同步。

### 24.3.2 验证数据

以下函数检查参数是否符合 FileInput：

```typescript
function validateData(data: unknown): FileInput {
  return FileInputSchema.parse(data); // 可能会抛出异常
}
```

```typescript
validateData(['file.txt', 'me', ['vacation', 'family']]); // OK
```

```typescript
assert.throws(
  () => validateData(['file.txt', 'me'])
);
```

FileInputSchema.parse() 的结果静态类型派自 FileInputSchema。通过让 validateData 返回 FileInput，我们确保前者符合后者。

### 24.3.3 类型守卫

FileInputSchema.check() 是一个类型守卫：

```typescript
function func(data: unknown) {
  if (FileInputSchema.check(data)) {
    // | inferred-type: string
    // | [string, string, string]
    // | {
      //   author?: string | undefined;
      //   tags?: string[] | undefined;
      //   file: string;
    // }
    data;
  }
}
```

定义一个支持 FileInput 而不是 Zod 推断出的类型的自定义类型守卫是有意义的。

```typescript
function isValidData(data: unknown) : data is FileInput {
  return FileInputSchema.check(data);
}
```


```typescript
type FileEntryInput = =
| string
| [string, string, string[]]
| {file: string, author?: string, tags?: string[]};
;
```

另一方面，是程序中使用的类型。它的结构针对在代码中的易用性进行了优化：

```typescript
type FileEntry = {
file: string,
author: null|string,
tags: string[],
};
```

在我们使用 Zod 确保输入数据符合 `FileEntryInput` 之后，我们使用一个转换函数将数据转换为 `FileEntry` 类型的值。

## 24.4 结论

从长远来看，我期待能够从静态类型推导出验证函数的编译时解决方案，以提高易用性。这会让它们更流行。

对于具有构建器 API（builder APIs）的库，我希望拥有可以将 TypeScript 类型编译为构建器 API 调用的工具（在线和通过命令行）。这将从两个方面提供帮助：

- 这些工具可以用于探索 API 是如何工作的。
- 我们可以选择通过工具生成 API 代码。

## 第 VI 部分

## 杂记

## 第 25 章

## 类型计算概述

- 目录
- 25.1 类型作为元值 ............................................................................................ 217
- 25.2 泛型：类型的工厂 ................................................................. . . 218
- 25.3 联合类型与交集类型 ................................................................. . . . 219
  - 25.3.1 联合类型 ().............................................................................................. 219
  - 25.3.2 交集类型 (6) ...................................................................................... 220
- 25.4 控制流 ................................................................................................................ 221
  - 25.4.1 条件类型 ........................................................................................ 221
  - 25.4.2 映射类型 .......................................................................................................... 224
- 25.5 其他各种运算符 .......................................................................................... 225
  - 25.5.1 索引类型查询运算符 keyof ............................................................... 225
  - 25.5.2 索引访问运算符 T[K] ................................................................... 226
  - 25.5.3 类型查询运算符 typeof ....................................................................... 227

在本章中，我们将探索如何在 TypeScript 中编译时使用类型进行计算。请注意，本章的重点是学习如何进行类型计算。因此，我们将大量使用字面量类型（literal types），示例的实际相关性较低。

## 25.1 类型作为元值

考虑以下两个级别的 TypeScript 代码：

- 程序级：在运行时，我们可以使用值和函数。
- 类型级：在编译时，我们可以使用特定类型和泛型类型。

类型级是程序级的元级。

| 级别 | 可用时间 | 操作数 | 运算 |
|---|---|---|---|
| 程序级 | 运行时 | 值 | 函数 |
| 类型级 | 编译时 | 特定类型 | 泛型类型 |

使用类型进行计算意味着什么？以下代码是一个示例：

```typescript
type ObjectLiterType = {
first: 1,
second: 2,
}
// 推断类型: "first" | "second"
type Result = keyof ObjectLiterType; // (A)
```

在 A 行中，我们采取了以下步骤：

- 我们计算的输入是类型 `ObjectLiterType`。
- 我们对输入应用 `keyof` 操作。它列出了对象类型的属性键。
- 我们为 `keyof` 的输出命名为 `Result`。

在类型级上，我们可以使用以下“值”进行计算：

```typescript
type ObjectLiterType = {
prop1: string,
prop2: number,
}

interface InterfaceType {
prop1: string;
prop2: number;
}

type TupleType = [boolean, bigint];
// 空值类型和字面量类型 :::
// 与值的语法相同，但它们都是类型

type Undefined = undefined;
type NullType = null;

type BooleanLiterType = true;
type NumberLiteralType = 12.34;
type BigIntLiteralType = 1234n;
type StringLiterType = 'abc';
```

## 25.2 泛型类型：类型的工厂

泛型类型是元级上的函数——例如：

## 25.3 联合类型与交集类型

```typescript
type Wrap<T> = [T];
```

泛型类型 `Wrap<>` 拥有参数 `T`。它的结果是 `T`，封装在一个元组类型中。这就是我们如何使用这个元函数：

```typescript
// 推断类型: [string]
type Wrapped = Wrap<string>;
```

我们将参数 `string` 传递给 `Wrap<>` 并将结果命名为 `Wrapped`。结果是一个包含单个组件（类型 `string`）的元组类型。

## 25.3 联合类型与交集类型

### 25.3.1 联合类型 ()

运算符 `|` 用于创建联合类型：

```typescript
type A = 'a' | 'b' | 'c'
type B = 'b' | 'c' | 'd';
```

```typescript
// 推断类型: "a" | "b" | "c" | "d"
type Union = A | B;
```

如果我们将类型 A 和类型 `B` 视为集合，那么 `A | B` 就是这些集合的集合论并集。换句话说：结果的成员至少是两个操作数之一的成员。

在语法上，我们可以在联合类型的第一个组件之前放置一个 `|`。当类型定义跨越多行时，这非常方便：

```typescript
type A =
| 'a'
| 'b'
| 'c'
;
```

### 25.3.1.1 联合类型作为元值的集合

TypeScript 将元值集合表示为字面量类型的联合。我们已经见过它的示例了：

```typescript
type Obj = {
first: 1,
second: 2,
};
```

```typescript
// 推断类型: "first" | "second"
type Result = keyof Obj;
```

我们将很快看到对这种集合的运算。

### 25.3.1.2 对象的联合类型

由于联合类型的每个成员都是操作数之一的成员，我们只能安全地访问所有操作数都拥有的属性。要访问其他属性，我们需要一个类型守卫（type guard）：

```typescript
type ObjectTypeA = {
propA: bigint,
sharedProp: string,
}
type ObjectTypeB = {
propB: boolean,
sharedProp: string,
}

type Union = ObjectTypeA | ObjectTypeB;

function func(arg: Union) {
  // (A) OK
  // @ts-expect-error: 属性 'propB' 不存在于类型 'Union'
  arg.propB;
}
```

```typescript
if ('propB' in arg) { // (B) 类型守卫
// ObjectTypeB
arg;
}
```

### 25.3.2 交集类型 (&)

运算符 `&` 用于创建交集类型：

```typescript
type A = 'a' | 'b' | 'c';
type B = 'b' | 'c' | 'd';
```

```typescript
// 推断类型: "b" | "c"
type Intersection = A & B;
```

如果我们将类型 A 和 B 视为集合，那么 `A & B` 就是这些集合的集合论交集。换句话说：结果的成员是两个操作数的成员。

### 25.3.2.1 对象的交集类型

两个对象类型的交集拥有所有类型的属性：

```typescript
type Obj1 = { prop1: boolean };
type Obj2 = { prop2: number };
```

```typescript
type Both = {
prop1: boolean,
prop2: number,
}
```

```typescript
// 类型 Obj1 & Obj2 可赋值给类型 Both
// 推断类型: true
type IntersectionHasProperties = IsAssignableTo<Obj1 & Obj2, Both>;

（泛型类型 `AssignableTo<>` 已解释。）

### 25.3.2.2 使用交集类型进行混合

如果我们将对象类型 `Named` 混合到另一个类型 `Obj` 中，我们需要一个交集类型（A 行）：

```typescript
interface Named {
  name: string;
}
function addName<Obj extends object>(obj: Obj, name: string)
  : Obj & Named // (A)
{
  const namedObj = obj as (Obj & Named);
  namedObj.name = name;
  return namedObj;
}

const obj = {
  last: 'Doe',
};

// 推断类型: { last: string; } & Named
const namedObj = addName(obj, 'Jane');
```

## 25.4 条件类型

条件类型具有以下语法：

```typescript
«Type2» extends «Type1» ? «ThenType> : «ElseType>
```

如果 `Type2` 可赋值给 `Type1`，则该类型表达式的结果是 `ThenType`。否则，为 `ElseType`。

### 25.4.1.1 示例：只包装具有 .length 属性的类型

在以下示例中，只有当类型具有值为数字的 `.length` 属性时，`Wrap<` 才会封装在单元素元组中：





# 25 带类型的计算概述

```
type Wrap<T> = T extends { length: number } ? [T] : T;
```

```typescript
// %inferred-type: [string]
type A = Wrap<string>;
```

```typescript
// %inferred-type: RegExp
type B = Wrap<RegExp>;
```

### 25.4.1.2 示例：检查可赋值性

我们可以使用条件类型来实现可赋值性检查：

```
type IsAssignableTo<A, B> = A extends B ? true : false;
```

```typescript
// 类型 `123` 可赋值给类型 `number`
// %inferred-type: true
type Result1 = IsAssignableTo<123, number>;
```

```typescript
// 类型 `number` 不可给类型 `123`
// %inferred-type: false
type Result2 = IsAssignableTo<number, 123>;
```

关于类型关系可赋值性的信息，请参阅 §11 “什么是 TypeScript 中的类型？两个视角”。

### 25.4.1.3 条件类型是分发的

条件类型是分发式的：将条件类型 C 应用于联合类型 U，等同于将 C 应用于 U 的每一个组件。以下是该示例：

```
type Wrap<T> = T extends { length: number } ? [T] : T;
```

```typescript
// %inferred-type: [boolean] | [number[]]
type C1 = Wrap<boolean | string | number>;
```

```typescript
// 等同于：
type C2 = Wrap<boolean> | Wrap<string> | Wrap<number>;
```

换句话说，分发性允许我们“遍历”联合类型的各个组件。这是分发性的另一个例子：

```
type AlwaysWrap<T> = T extends any ? [T] : [T];
```

```typescript
// %inferred-type: ["a"] | ["d"] | [{ a: 1 } & { b: 2 }]
type Result = AlwaysWrap<'a' | { a: 1 } & { b: 2 } | 'd'>;
```

### 25.4.1.4 在分发式条件类型中，我们使用 never 来忽略某些内容

如果视为集合，类型 `never` 是空的。因此，如果它出现在联合类型中，它会被忽略：

```typescript
// %inferred-type: "a" | "b"
type Result = 'a' | 'b' | never;
```

我们可以使用 `never` 来忽略联合类型的组件：

```typescript
type DropNumbers<T> = T extends number ? never : T;

// %inferred-type: "a" | "b"
type Result1 = DropNumbers<1 | 'a' | 2 | 'b'>;
```

当使用 then 分支和 else 分支的表达式时，会发生这种情况：

```
type KeepNumbers<T> = T extends number ? T : never;

// %inferred-type: 1 | 2
type Result2 = KeepNumbers<1 | 'a' | 2 | 'b'>;
```

### 25.4.1.5 内置工具类型：Exclude<T, U>

从联合类型中排除项是一个非常常见的操作，因此 TypeScript 提供了内置的工具类型 `Exclude<T, U>`：

```typescript
/** 从 T 中排除所有可赋值给 U 的类型 */
type Exclude<T, U> = T extends U ? never : T;

// %inferred-type: "a" | "b"
type Result1 = Exclude<1 | 'a' | 2 | 'b', number>;

// %inferred-type: 1 | 2
type Result2 = Exclude<1 | 'a' | 2 | 'b', 1 | 'c'>;
```

### 25.4.1.6 内置工具类型：Extract<T, U>

`Exclude<T>` 的反操作：

```typescript
/** 从 T 中提取所有可赋值给 U 的类型 */
type Extract<T, U> = T extends U ? T : never;

// %inferred-type: 1 | 2
type Result1 = Extract<1 | 'a' | 2 | 'b', number>

// %inferred-type: 1 | "b"
type Result2 = Extract<1 | 'a' | 2 | 'b', 1 | 'c'>;
```

### 25.4.1.7 链式条件类型

类似于 JavaScript 的三元运算符，我们也可以链用 TypeScript 的条件类型运算符：

```
type LiteralName<T> =
  T extends undefined ? "undefined" :
  T extends null ? "null" :
  T extends boolean ? "boolean" :
  T extends number ? "number" :
  T extends bigint ? "bigint" :
  T extends string ? "string" :
  never;

// %inferred-type: "bigint"
type Result1 = LiteralName<123n>;
// %inferred-type: "string" | "number" | "boolean"
type Result2 = LiteralName<true | 'a'>;
```

## 25.4.2 映射类型

*映射类型*（mapped type）通过遍历键的集合来生成对象——例如：

```typescript
// %inferred-type: { a: number; b: number; c: number }
type Result = {
  [K in 'a' | 'b' | 'c']: number;
};
```

该运算符是映射类型的关键部分：它指定了字面量对象的键。

### 25.4.2.1 内置工具类型：Pick<T, K>

以下内置工具类型通过指定现有对象的某些属性来创建一个新对象：

```typescript
/** 从 T 中选取键在联合类型 K 中的属性集 */
type Pick<T, K> = {
  [P in K]: T[P]
};
```

它的用法如下：

```typescript
ObjectLiteral = {
  a: 1,
  b: 2,
  c: 3,
  d: 4,
};
```

### 25.4.2.2 内置工具类型：Omit<T, K>

内置工具类型通过指定现有对象的某些属性来创建一个新对象：

```typescript
/** 构造一个类型 T，除了 K 中的属性 */
type Omit<T, K> = {
  [P in Exclude<keyof T, K>]?: any;
};
```

解释：
- `K extends keyof T` 意味着 K 是 T 所有键的子类型。
- `Exclude<T, K>` 意味着：取 T 的键并移除 K 中提到的键。

## 25.5.1 索引运算符

我们已经遇到过 `keyof` 运算符。它列出了对象类型的键：

```typescript
type Obj = {
  a: number;
  b: number;
  c: number;
  d: number;
}
```

将 `keyof` 应用于元组类型的结果可能令人意外：KeysOfObj 包含类型 `number`，因为在 JavaScript 中键是字符串集合。元组也支持索引访问：

```typescript
type Tuple = ['a', 'b', 'c', 'd'];
```

```typescript
// %inferred-type: "a" | "b"
type Elements = Tuple[0 | 1];
```

括号运算符也是分发的：

```typescript
type MyType = { prop: 1 } | { prop: 2 } | { prop: 3 };
```

```typescript
// %inferred-type: 1 | 2 | 3
type Result1 = MyType['prop'];
```

```typescript
// 等同于：
type Result2 = {
{ prop: 1 }['prop'] |
{ prop: 2 }['prop'] |
{ prop: 3 }['prop']
};
```

## 25.5.2 索引访问运算符 T[K]

索引访问运算符 `T[K]` 返回 T 中所有键属于 K 的属性类型。`T[K]` 也称为查找类型（lookup type）。这些是运算符使用的示例：

```typescript
type Obj = {
  0: 'a',
  1: 'b',
  prop0: 'c',
  prop1: 'd'
};
```

```typescript
// %inferred-type: "a" | "b"
type Result1 = Obj[0 | 1];
```

```typescript
// %inferred-type: "c" | "d"
type Result2 = Obj['prop0' | 'prop1'];
```

## 25.5 其他运算符

```typescript
// %inferred-type: "a" | "b" | "c" | "d"
type Result3 = Obj[keyof Obj];
```

括号中的类型必须可赋值给所有属性键（keyof）。这就是为什么 `Obj[number]` 和 `Obj[string]` 是不允许的。然而，如果索引类型具有索引签名（A 行），我们可以使用 `number` 和 `string` 索引类型：

```typescript
type Obj = {
  [key: string]: RegExp, // (A)
};
```

```typescript
// %inferred-type: string | number
type KeysOfObj = keyof Obj;
```

```typescript
// %inferred-type: RegExp
type ValuesOfObj = Obj[string];
```

KeysOfObj 包含类型 `number`，因为在 JavaScript 中键是字符串集合。元组也支持索引访问：

```typescript
type Tuple = ['a', 'b', 'c', 'd'];
```

```typescript
// %inferred-type: "a" | "b"
type Elements = Tuple[0 | 1];
```

括号运算符也是分发的：

```typescript
type MyType = { prop: 1 } | { prop: 2 } | { prop: 3 };
```

```typescript
// %inferred-type: 1 | 2 | 3
type Result1 = MyType['prop'];
```

```typescript
// 等同于：
type Result2 = {
{ prop: 1 }['prop'] |
{ prop: 2 }['prop'] |
{ prop: 3 }['prop']
};
```

如果我们记住 A & B 拥有 A 和 B 的所有属性，这是合理的。A & B 拥有 B 的属性。

## 25.5.3 typeof 运算符

我们已经遇到了 `keyof` 运算符。`typeof` 将 JavaScript 值转换为 TypeScript 类型：

```typescript
const str = "abc";
```

```typescript
// %inferred-type: string
type Result = typeof str;
```





25 使用类型计算概述

第一个 'abc' 是一个值，而第二个 "abc" 是它的类型，即一个字符串字面量类型。

这是使用 `typeof` 的另一个示例：

```typescript
const func = (x: number) => x + x;
// %inferred-type: (x: number) => number
type Result = typeof func;
```

§15.1.2 "向类型添加符号" 描述了 `typeof` 的一个有趣用例。
