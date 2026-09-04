
# 关于我

你好，我是[Dumindu Madunuwan](https://lk.linkedin.com/in/dumindunuwan)。我是一名网页开发者，主要使用 PHP。

大约在 2007 年至 2009 年，我选择了网页开发，因为那时我真正相信，网络将成为下一个终极、系统独立和语言独立的平台，下一代软件生态系统将在浏览器之上实现。我期望的网络与此有些相似。

![Web 的未来：Mozilla Labs Aurora 概念浏览器](http://www.youtube.com/watch?v=FZ-zvx1QCcA "Web 的未来：Mozilla Labs Aurora 概念浏览器")

像一些网页开发者一样，我过去确实更看好 HTML5 而不是本机应用程序。我学习了 HTML5、CSS3、RWD、Mobile First Design、UI/UX 等。如今，我们有数百个前端框架，但仍然无法胜过本机应用程序，尤其是在性能方面。

确实，网络技术正在逐渐适应通过 asmjs、NativeScript、Electron、WebAssembly、React Native 进行本机应用程序开发，但由于新兴的联网汽车和虚拟现实生态系统，未来的网络应用程序开发将变得更加复杂。

另一方面，现在我们有许多强大的 PHP 替代品，比如 node 和 Go。所以作为 PHP 开发者，现在是学习新东西的时候，学习一门新的语言。我选择 Rust 是因为它是一门有趣的学习语言，下一代浏览器引擎[Servo](https://servo.org/)是用 Rust 编写的。

* * *

![Medium](https://medium.com/@dumindu "Medium") ![Ycombinator](https://news.ycombinator.com/user?id=dumindunuwan "Ycombinator") ![Reddit](https://www.reddit.com/user/dumindunuwan/ "Reddit") ![Github](https://github.com/dumindu/ "Github") ![LinkedIn](https://lk.linkedin.com/in/dumindunuwan/ "LinkedIn") ![Pinterest](https://www.pinterest.com/dumindu/ "Pinterest") ![Behance](https://www.behance.net/dumindu-madunuwan/ "Behance")

# 为什么选择 Rust？

Rust 最初由 Mozilla 员工 Graydon Hoare 作为个人项目设计和开发。Mozilla 于 2009 年开始赞助该项目，并在 2010 年宣布。但是，第一个稳定版本 Rust 1.0 于 2015 年 5 月 15 日发布。

![重新思考系统编程](http://thoughtram.io/rust-and-nickel/#/11)

Rust 的目标是成为创建高度并发和高度安全系统的良好语言。正如您在上图中所看到的，Rust 旨在同时提供速度和安全性。

> "Rust 是一种专注于三个目标的系统编程语言：安全性、速度和并发性。"
> 
> __ Rust 文档

Rust 是一种非常年轻和现代的语言。它是一种`编译型编程语言`，在后端使用[LLVM](https://en.wikipedia.org/wiki/LLVM)。此外，Rust 是一种`多范式编程语言`，支持命令式过程、并发 actor、面向对象和纯函数式风格。它还支持静态和动态风格的泛型编程和元编程。

其设计元素来自各种来源。

+   抽象机器模型：`C`
+   数据类型：`C, SML, OCaml, Lisp, Limbo`
+   可选绑定：`Swift`
+   卫生宏：`Scheme`
+   函数式编程：`Haskell, OCaml, F#`
+   属性：`ECMA`-335
+   内存模型和内存管理：`C++, ML Kit, Cyclone`
+   类型类：`Haskell`
+   箱：`ECMA`-335 CLI 模型中的汇编
+   通道和并发性：`Newsqueak, Alef, Limbo`
+   消息传递和线程失败：`Erlang`
+   等等。

Rust **默认不使用自动垃圾回收**系统（GC）。

> 🔎 Rust 最独特和引人注目的特性之一是[所有权](https://doc.rust-lang.org/stable/book/ownership.html)，它用于实现内存安全。 Rust 乐观地创建内存指针，通过使用[引用和借用](https://doc.rust-lang.org/stable/book/references-and-borrowing.html)在编译时检查内存指针的有限访问。它通过检查[Lifetimes](https://doc.rust-lang.org/stable/book/lifetimes.html)实现自动的编译时内存管理。

Rust 编译器在编译时观察代码，并帮助[防止许多种可能在 C++ 中编写的错误](https://doc.rust-lang.org/error-index.html)。

# 安装

有许多安装 Rust 的方法。目前官方安装 Rust 的方式是使用[Rustup](https://rustup.rs/)。

[🕮](https://github.com/rust-lang-nursery/rustup.rs) Rustup 从官方发布渠道安装 Rust 编程语言，使您可以轻松在稳定版、测试版和夜间版编译器之间切换并保持其更新。它通过为常见平台提供标准库的二进制构建，简化了交叉编译。

[🕮](https://github.com/rust-lang-nursery/rustup.rs#installation) Rustup 将 `rustc`、`cargo`、`rustup` 和其他标准工具安装到 Cargo 的 `bin` 目录中。在 Unix 上，它位于 `$HOME/.cargo/bin`，在 Windows 上位于 `%USERPROFILE%\.cargo\bin`。这是 `cargo install` 将安装 Rust 程序和 Cargo 插件的相同目录。

**💡** 更多信息可以在[Rustup 项目的 Github 页面](https://github.com/rust-lang-nursery/rustup.rs)找到。

安装 Rust 后，您可以在终端上键入 `rustc --version` 或 `rustc -V` 来检查当前版本，以验证安装成功。

# Hello World

```
fn main() {
    println!("Hello, world!");
} 
```

`fn` 表示函数。主函数是每个 Rust 程序的起点。

`println!` 将文本打印到控制台，其 *!* 表示它是一个 [宏](https://doc.rust-lang.org/book/macros.html) 而不是函数。

> 💡 Rust 文件应该具有 .rs 文件扩展名，如果文件名使用了多个单词，请遵循 [snake_case](https://en.wikipedia.org/wiki/Snake_case)。

通过 `rustc file.rs` 进行编译

在 Linux 和 Mac 上通过 `./file` 执行，在 Windows 上通过 `file.exe` 执行

* * *

💯 这是 println! 宏的其他用法，

```
fn main() {
    println!("{}, {}!", "Hello", "world"); // Hello, world!
    println!("{0}, {1}!", "Hello", "world"); // Hello, world!
    println!("{greeting}, {name}!", greeting="Hello", name="world"); // Hello, world!

    println!("{:?}", [1,2,3]); // [1, 2, 3]
    println!("{:#?}", [1,2,3]);
    /*
        [
            1,
            2,
            3
        ]
    */

    // 🔎 format! macro is used to store the formatted STRING
    let x = format!("{}, {}!", "Hello", "world");
    println!("{}", x); // Hello, world!
} 
```

# Cargo、Crates 和基本项目结构

Cargo 是 Rust 的内置包管理器。但主要用于，

▸ 创建新项目：`cargo new`
▸ 更新依赖：`cargo update`
▸ 构建项目：`cargo build`
▸ 构建并运行项目：`cargo run`
▸ 运行测试：`cargo test`
▸ 通过 rustdoc 生成文档：`cargo doc`

除此之外，还有一些 Cargo 命令，专门用于通过 cargo 直接发布 crates。

▸ `cargo login`：获取 API 令牌
▸ `cargo package`：使本地创建可上传到 crates.io
▸ `cargo publish`：使本地创建可上传到 crates.io 并上传 crate

⭐️ **一个 crate 是一个 package。Crates 可以通过** [**Cargo**](https://crates.io/) **分享。**

* * *

一个 crate 可以生成一个可执行文件或一个库。换句话说，它可以是一个二进制 crate 或一个库 crate。

1.  `cargo new crate_name --bin`：生成一个 **可执行文件**
1.  `cargo new crate_name --lib` 或 `cargo new crate_name`：生成一个 **库**

第一种生成方式为，

```
├── Cargo.toml
└── src
    └── main.rs 
```

第二种生成方式为，

```
├── Cargo.toml
└── src
    └── lib.rs 
```

+   **Cargo.toml**（大写的 c）是配置文件，包含了 Cargo 编译项目所需的所有元数据。
+   **src** 文件夹是存储源代码的地方。
+   每个 crate 都有一个隐式 crate 根 / 入口点。对于二进制 crate，**main.rs** 是 crate 根，对于库 crate，**lib.rs** 是 crate 根。

> 💡 当我们通过 `cargo build` 或 `cargo run` 构建一个二进制 crate 时，可执行文件将存储在 **target/debug/** 文件夹中。但当通过 `cargo build --release` 构建用于发布的版本时，可执行文件将存储在 **target/release/** 文件夹中。

* * *

这是 [Cargo Docs 描述](http://doc.crates.io/guide.html#project-layout) 推荐的项目布局，

```
.
├── Cargo.lock
├── Cargo.toml
├── benches
│   └── large-input.rs
├── examples
│   └── simple.rs
├── src
│   ├── bin
│   │   └── another_executable.rs
│   ├── lib.rs
│   └── main.rs
└── tests
    └── some-integration-tests.rs 
```

▸ 源代码放在 `src` 目录中。
▸ 默认库文件为 `src/lib.rs`。
▸ 默认可执行文件为 `src/main.rs`。
▸ 其他可执行文件可以放在 `src/bin/*.rs` 中。
▸ 集成测试放在 `tests` 目录中（单元测试放在它们所测试的每个文件中）。
▸ 示例放在 `examples` 目录中。
▸ 基准测试放在 `benches` 目录中。

# 注释和代码文档

```
// Line comments
/* Block comments */ 
```

支持嵌套的块注释。

💡 **始终避免使用块注释，改用行注释。**

```
/// Line comments; document the next item
/** Block comments; document the next item */

//! Line comments; document the enclosing item
/*! Block comments; document the enclosing item !*/ 
```

文档注释支持 Markdown 标记。使用 `cargo doc` 命令，可以从这些文档注释生成 HTML 文档。让我们看看这两组文档注释之间的区别。

```
/// This module contains tests
mod test {
    // ...
}

mod test {
    //! This module contains tests

    // ...
} 
```

正如你所看到的，两者都用于记录相同的模块。第一个注释已添加到模块之前，而第二个注释已添加到模块内部。

💡 **只使用//!编写 crate 和模块级文档，不要写其他内容。使用 mod 块时，在块外使用///。**

我们还可以使用**文档属性**来记录代码。

> 🔎 [属性](https://doc.rust-lang.org/reference.html#attributes)是一个通用的、自由形式的**元数据**，根据名称、约定和语言和编译器版本进行解释。任何项目声明都可以应用属性。

这里的每个注释都等同于相关的数据属性。

```
/// Foo
#[doc="Foo"]

//! Foo
#![doc="Foo"] 
```

# 变量绑定，常量和静态变量

⭐️ 在 Rust 中，变量默认是**不可变的**，因此我们称它们为**变量绑定**。要使它们可变，使用`mut` 关键字。

⭐️ Rust 是一种**静态类型**语言；它在编译时检查数据类型。但是**声明变量绑定时不需要实际输入类型**。在这种情况下，编译器会检查用法并为其设置更好的数据类型。但是**常量和静态变量必须注明类型**。类型在冒号(:)之后声明。

+   变量绑定

```
let a = true;
let b: bool = true;

let (x, y) = (1, 2);

let mut z = 5;
z = 6; 
```

+   常量

```
const N: i32 = 5; 
```

+   静态变量

```
static N: i32 = 5; 
```

**let** 关键字用于绑定表面。我们可以将名称绑定到值或函数。此外，由于 let 表达式的左侧是一个‘模式’，您可以将多个名称绑定到一组值或函数值。

**const** 关键字用于定义常量。它在整个程序的生命周期内存在，但在内存中没有固定的地址。**static** 关键字用于定义‘全局变量’类型的设施。每个值只有一个实例，并且位于内存中的**固定位置**。

💡 **始终使用 const**，而不是 static。你实际上很少需要将内存位置与常量关联起来，使用 const 允许进行优化，例如常量传播不仅在你的 crate 中，在下游 crate 中也能进行。

💡 通常静态变量放置在代码文件的顶部，函数之外。

# 函数

+   函数使用关键字 `fn` 声明
+   在使用**参数**时，您**必须声明数据类型**。
+   默认情况下，函数**返回空元组 ()**。如果要返回一个值，必须在**->**之后指定**返回类型**。

```
//Hello world function
fn main() {
    println!("Hello, world!");
}

//Function with arguments 
fn print_sum(a: i8, b: i8) {
    println!("sum is: {}", a + b);
}

//Returning
fn plus_one(a: i32) -> i32 {
    a + 1 //no ; means an expression, return a+1
}

fn plus_two(a: i32) -> i32 {
    return a + 2; //return a+2 but bad practice, 
    //should use only on conditional returnes, except it's last expression 
}

// ⭐️ Function pointers, Usage as a Data Type
let b = plus_one;
let c = b(5); //6

let b: fn(i32) -> i32 = plus_one; //same, with type inference
let c = b(5); //6 
```

# 原始数据类型

+   **bool**：true 或 false

```
let x = true;
let y: bool = false;

// ⭐️ no TRUE, FALSE, 1, 0 
```

+   **char**：一个单一的 Unicode 标量值

```
let x = 'x';
let y = '😎';

// ⭐️ no "x", only single quotes
//because of Unicode support, char is not a single byte, but four. 
```

+   **i8 i16 i32 i64**：固定大小(bit)有符号(+/-)整数类型

| 数据类型 | 最小值 | 最大值 |
| --- | --- | --- |
| i8 | -128 | 127 |
| i16 | -32768 | 32767 |
| i32 | -2147483648 | 2147483647 |
| i64 | -9223372036854775808 | 9223372036854775807 |

💡 最小值和最大值基于 IEEE 标准的二进制浮点算术；从**-2ⁿ⁻¹到 2ⁿ⁻¹-1**。您可以使用 **min_value()** 和 **max_value()** 来找到每种整数类型的最小值和最大值，例如 i8::min_value();

+   **u8 u16 u32 u64**：固定大小(bit)无符号(+)整数类型

| 数据类型 | 最小值 | 最大值 |
| --- | --- | --- |
| u8 | 0 | 255 |
| u16 | 0 | 65535 |
| u32 | 0 | 4294967295 |
| u64 | 0 | 18446744073709551615 |

💡 与有符号数一样，最小值和最大值基于 IEEE 二进制浮点算术标准；从**0 到 2ⁿ-1**。同样，您可以使用**min_value()**和**max_value()**来找到每种整数类型的最小值和最大值，例如 u8::max_value();

+   **isize**：可变大小的有符号（+/-）整数

简单来说，这是一种数据类型，用于涵盖所有有符号整数类型，但内存分配根据指针的大小。最小和最大值类似于 i64。

+   **usize**：可变大小的无符号（+）整数

简单来说，这是一种数据类型，用于涵盖所有无符号整数类型，但内存分配根据指针的大小。最小和最大值类似于 u64。

+   **f32**：32 位浮点数

类似于其他语言中的浮点数，**单精度**。

💡 除非您迫切需要减少内存消耗，或者正在进行低级优化，当目标硬件不支持双精度，或者当单精度比双精度更快时，应避免使用这种类型。

+   **f64**：64 位浮点数

类似于其他语言中的双精度，**双精度**。

+   **数组**：相同数据类型的固定大小元素列表

```
let a = [1, 2, 3]; // a[0] = 1, a[1] = 2, a[2] = 3
let mut b = [1, 2, 3];

let c: [int; 3] = [1, 2, 3]; //[Type; NO of elements]

let d: ["my value"; 3]; //["my value", "my value", "my value"];

let e: [i32; 0] = []; //empty array

println!("{:?}", a); //[1, 2, 3]
println!("{:#?}", a);
//  [
//      1,
//      2,
//      3
//  ] 
```

⭐️ 数组默认为**不可变**，即使使用 mut，其元素数量也不能更改。

> 🔎 如果您正在寻找一个动态/可增长的数组，可以使用**Vec**。向量可以包含任何类型的元���，但所有元素必须是相同的数据类型。

+   **元组**：固定大小的有序元素列表，元素可以是不同（或相同）数据类型

```
let a = (1, 1.5, true, 'a', "Hello, world!");
// a.0 = 1, a.1 = 1.5, a.2 = true, a.3 = 'a', a.4 = "Hello, world!"

let b: (i32, f64) = (1, 1.5);

let (c, d) = b; // c = 1, d = 1.5
let (e, _, _, _, f) = a; //e = 1, f = "Hello, world!", _ indicates not interested of that item

let g = (0,); //single-element tuple

let h = (b, (2, 4), 5); //((1, 1.5), (2, 4), 5)

println!("{:?}", a); //(1, 1.5, true, 'a', "Hello, world!") 
```

⭐️ 元组默认也是**不可变**的，即使使用 mut，其元素数量也不能更改。此外，如果要更改元素的值，新值应与先前的数据类型相同。

+   **切片**：对另一个数据结构的动态大小引用

如果想要获取/传递数组或任何其他数据结构的一部分。而不是将其复制到另一个数组（或相同数据结构）中，Rust 允许创建一个视图/引用，仅访问数据的那部分。它可以是可变的或不可变的。

```
let a: [i32; 4] = [1, 2, 3, 4];//Parent Array

let b: &[i32] = &a; //Slicing whole array
let c = &a[0..4]; // From 0th position to 4th(excluding)
let d = &a[..]; //Slicing whole array

let e = &a[1..3]; //[2, 3]
let e = &a[1..]; //[2, 3, 4]
let e = &a[..3]; //[1, 2, 3] 
```

+   **str**：未定大小的 UTF-8 Unicode 字符串切片

```
let a = "Hello, world."; //a: &'static str
let b: &str = "こんにちは, 世界!"; 
```

⭐️ 这是一个**不可变/静态分配的切片**，其中存储在内存中的某个位置的**未知大小的 UTF-8**代码点序列。**&str**用于借用并将整个数组分配给给定的变量绑定。

> 🔎 [字符串](https://doc.rust-lang.org/std/string/struct.String.html)是一个**堆**分配的字符串。该字符串是可增长的，并且保证为 UTF-8。它们通常通过使用**to_string()**或**String::from()**方法从字符串切片转换而来。例如：`“Hello”.to_string();` `String::from("Hello");`

💡 一般情况下，当您需要**所有权**时应使用**String**，当您只需要**借用字符串**时应使用**&str**。

+   **函数**

正如我们在函数部分讨论的那样，b 是一个函数指针，指向 plus_one 函数

```
fn plus_one(a: i32) -> i32 {
    a + 1
}

let b: fn(i32) -> i32 = plus_one;
let c = b(5); //6 
```

# 运算符

+   **算术运算符**：+ - * / %

```
let a = 5;
let b = a + 1; //6
let c = a - 1; //4
let d = a * 2; //10
let e = a / 2; // ⭐️ 2 not 2.5
let f = a % 2; //1

let g = 5.0 / 2.0; //2.5 
```

> 🔎 还有**+**用于**数组和字符串的连接**

+   **比较运算符**：== != < > <= >=

```
let a = 1;
let b = 2;

let c = a == b; //false
let d = a != b; //true
let e = a < b; //true
let f = a > b; //false
let g = a <= a; //true
let h = a >= a; //true

// 🔎
let i = true > false; //true
let j = 'a' > 'A'; //true 
```

+   **逻辑运算符**：! && ||

```
let a = true;
let b = false;

let c = !a; //false
let d = a && b; //false
let e = a || b; //true 
```

> 🔎 在整数类型上，!会反转值的二进制补码表示中的各个位。

```
let a = !-2; //1
let b = !-1; //0
let c = !0; //-1
let d = !1; //-2 
```

+   **位运算符**：& | ^ << >>

```
let a = 1;
let b = 2;

let c = a & b; //0  (01 && 10 -> 00)
let d = a | b; //3  (01 || 10 -> 11)
let e = a ^ b; //3  (01 != 10 -> 11)
let f = a << b; //4  (add 2 positions to the end -> '01'+'00' -> 100)
let g = a >> a; //0  (remove 2 positions from the end -> o̶1̶ -> 0) 
```

+   **赋值和复合赋值运算符**

=运算符用于将值或函数的名称分配给一个名称。复合赋值运算符是通过将+ - * / % & | ^ << >>运算符之一与=运算符组合而成的。

```
let mut a = 2;

a += 5; //2 + 5 = 7
a -= 2; //7 - 2 = 5
a *= 5; //5 * 5 = 25
a /= 2; //25 / 2 = 12 not 12.5
a %= 5; //12 % 5 = 2

a &= 2; //10 && 10 -> 10 -> 2
a |= 5; //010 || 101 -> 111 -> 7
a ^= 2; //111 != 010 -> 101 -> 5
a <<= 1; //'101'+'0' -> 1010 -> 10
a >>= 2; //101̶0̶ -> 10 -> 2 
```

+   **类型转换运算符**：as

```
let a = 15;
let b = (a as f64) / 2.0; //7.5 
```

+   **借用和解引用运算符**：& &mut *

**&或&mut**运算符用于**借用**，*****运算符用于**解引用**。

> 🔎 这些运算符的使用是一个高级话题，更多信息请参考[Rust 参考文档](https://doc.rust-lang.org/reference.html#unary-operator-expressions)。

# 控制流

+   **if - else if - else**

```
// Simplest Example
let team_size = 7;
if team_size < 5 {
    println!("Small");
} else if team_size < 10 {
    println!("Medium");
} else {
    println!("Large");
}

// partially refactored code
let team_size = 7;
let team_size_in_text;
if team_size < 5 {
    team_size_in_text = "Small";
} else if team_size < 10 {
    team_size_in_text = "Medium";
} else {
    team_size_in_text = "Large";
}
println!("Current team size : {}", team_size_in_text);

//optimistic code
let team_size = 7;
let team_size_in_text = if team_size < 5 {
    "Small" //⭐️no ;
} else if team_size < 10 {
    "Medium"
} else {
    "Large"
};
println!("Current team size : {}", team_size_in_text);

let is_below_eighteen = if team_size < 18 { true } else { false }; 
```

⭐️ **当将其用作表达式时，每个块的返回数据类型应该相同。**

+   **匹配**

```
let tshirt_width = 20;
let tshirt_size = match tshirt_width {
    16 => "S", // check 16
    17 | 18 => "M", // check 17 and 18
    19 ... 21 => "L", // check from 19 to 21 (19,20,21)
    22 => "XL",
    _ => "Not Available",
};
println!("{}", tshirt_size); // L

let is_allowed = false;
let list_type = match is_allowed {
    true => "Full",
    false => "Restricted"
    // no default/ _ condition can be skipped 
    // Because data type of is_allowed is boolean and all possibilities checked on conditions 
};
println!("{}", list_type); // Restricted

let marks_paper_a: u8 = 25;
let marks_paper_b: u8 = 30;
let output = match (marks_paper_a, marks_paper_b) {
    (50, 50) => "Full marks for both papers",
    (50, _) => "Full marks for paper A",
    (_, 50) => "Full marks for paper B",
    (x, y) if x > 25 && y > 25 => "Good",
    (_, _) => "Work hard"
};
println!("{}", output); // Work hard 
```

+   **while**

```
let mut a = 1;
while a <= 10 { 
    println!("Current value : {}", a);
    a += 1; //no ++ or -- on Rust
}

// Usage of break and continue
let mut b = 0;
while b < 5 {
    if b == 0 { 
        println!("Skip value : {}", b);
        b += 1;
        continue;
    } else if b == 2 {
        println!("Break At : {}", b);
        break;
    }
    println!("Current value : {}", b);
    b += 1;
}

// Outer break
let mut c1 = 1;
'outer_while: while c1 < 6 { //set label outer_while
    let mut c2 = 1;
    'inner_while: while c2 < 6 { 
        println!("Current Value : [{}][{}]", c1, c2);
        if c1 == 2 && c2 == 2 { break 'outer_while; } //kill outer_while
        c2 += 1;
    }
    c1 += 1;
} 
```

+   **循环**

```
loop {
    println!("Loop forever!");
}

// Usage of break and continue
let mut a = 0;
loop {
    if a == 0 {
        println!("Skip Value : {}", a);
        a += 1;
        continue;
    } else if a == 2 {
        println!("Break At : {}", a);
        break;
    }
    println!("Current Value : {}", a);
    a += 1;
}

// Outer break
let mut b1 = 1;
'outer_loop: loop { //set label outer_loop
  let mut b2 = 1;
  'inner_loop: loop {
    println!("Current Value : [{}][{}]", b1, b2);
    if b1 == 2 && b2 == 2 {
        break 'outer_loop; // kill outer_loop
    } else if b2 == 5 {
        break;
    }
    b2 += 1;
  }
  b1 += 1;
} 
```

+   **for**

```
for a in 0..10 { //(a = o; a <10; a++) // 0 to 10(exclusive)
  println!("Current value : {}", a);
}

// Usage of break and continue
for b in 0..6 {
  if b == 0 {
    println!("Skip Value : {}", b);
    continue;
  } else if b == 2 {
    println!("Break At : {}", b);
    break;
  }
  println!("Current value : {}", b);
}

// Outer break
'outer_for: for c1 in 1..6 { //set label outer_for
  'inner_for: for c2 in 1..6 {
    println!("Current Value : [{}][{}]", c1, c2);
    if c1 == 2 && c2 == 2 { break 'outer_for; } //kill outer_for
  }
}

// Working with arrays/vectors
let group : [&str; 4] = ["Mark", "Larry", "Bill", "Steve"];

for n in 0..group.len() { //group.len() = 4 -> 0..4 👎 check group.len()on each iteration
  println!("Current Person : {}", group[n]);
}

for person in group.iter() { //👍 group.iter() turn the array into a simple iterator
  println!("Current Person : {}", person);
} 
```

# 向量

如果您记得，数组是相同数据类型的固定大小元素列表。即使使用 mut，其元素计数也不能更改。向量是一种可调整大小的数组，但所有元素必须是相同类型的。

⭐️ 这是一个通用类型，写作 `Vec<T>`。T 可以是任何类型，例如。i32s 的 Vec 的类型是 `Vec<i32>`。此外，向量总是在动态分配的堆中分配它们的数据。

```
//Creating vectors - 2 ways
let mut a = Vec::new(); //1.with new() keyword
let mut b = vec![]; //2.using the vec! macro

//Creating with data types
let mut a2: Vec<i32> = Vec::new();
let mut b2: Vec<i32> = vec![];
let mut b3 = vec![1i32, 2, 3];//sufixing 1st value with data type

//Creating with data
let mut b4 = vec![1, 2, 3];
let mut b5: Vec<i32> = vec![1, 2, 3];
let mut b6  = vec![1i32, 2, 3];
let mut b7 = vec![0; 10]; //ten zeroes

//Accessing and changing exsisting data
let mut c = vec![5, 4, 3, 2, 1];
c[0] = 1;
c[1] = 2;
//c[6] = 2; can't assign values this way, index out of bounds
println!("{:?}", c); //[1, 2, 3, 2, 1]

//push and pop
let mut d: Vec<i32> = Vec::new();
d.push(1); //[1] : Add an element to the end
d.push(2); //[1, 2]
d.pop(); //[1] : : Remove an element from the end

// 🔎 Capacity and reallocation
let mut e: Vec<i32> = Vec::with_capacity(10);
println!("Length: {}, Capacity : {}", e.len(), e.capacity()); //Length: 0, Capacity : 10

// These are all done without reallocating...
for i in 0..10 {
    e.push(i);
}
// ...but this may make the vector reallocate
e.push(11); 
```

⭐️ 主要一个向量代表 3 个东西；指向数据的指针，当前拥有的元素数量（长度），容量（为任何未来元素分配的空间量）。如果向量的长度超过其容量，其容量将自动增加。但其元素将被重新分配（可能会很慢）。因此，尽可能在可能的情况下始终使用 `Vec::with_capacity`。

> 🔎 字符串数据类型是 UTF-8 编码的向量。但由于编码的原因，您无法对字符串进行索引。

向量可以以三种方式与迭代器一起使用，

```
let mut v = vec![1, 2, 3, 4, 5];

for i in &v {
    println!("A reference to {}", i);
}

for i in &mut v {
    println!("A mutable reference to {}", i);
}

for i in v {
    println!("Take ownership of the vector and its element {}", i);
} 
```

# 结构体

⭐️ 结构体用于将相关属性封装成一个统一的数据类型。

💡 按照惯例，结构体的名称以大写字母开头，并遵循驼峰命名法。

有 3 种结构体的变体，

1.  类似 C 的结构体
1.  一个或多个逗号分隔的名称:值对
1.  大括号包围的列表
1.  与其他语言（如 Java）中的类（没有方法）类似
1.  因为字段有名称，所以我们可以通过���符号访问它们
    1.  元组结构体
1.  一个或多个逗号分隔的值
1.  像元组一样用括号括起来的列表
1.  看起来像命名元组
    1.  单元结构体
1.  一个没有任何成员的结构体
1.  它定义了一个新类型，但它类似于一个空元组，()
1.  很少使用，与泛型一起很有用

⭐️ 在 Rust 中涉及面向对象编程时，属性和方法分别放置在结构体和特征上。结构体仅包含属性，特征仅包含方法。它们通过 impls 连接在一起

## 01\. 类 C 结构体

```
// Struct Declaration
struct Color {
    red: u8,
    green: u8,
    blue: u8
}

fn main() {
  // creating an instance
  let black = Color {red: 0, green: 0, blue: 0};

  // accessing it's fields, using dot notation
  println!("Black = rgb({}, {}, {})", black.red, black.green, black.blue); //Black = rgb(0, 0, 0)

  // structs are immutable by default, use `mut` to make it mutable but doesn't support field level mutability
  let mut link_color = Color {red: 0,green: 0,blue: 255};
  link_color.blue = 238;
  println!("Link Color = rgb({}, {}, {})", link_color.red, link_color.green, link_color.blue); //Link Color = rgb(0, 0, 238)

  // copy elements from another instance
  let blue = Color {blue: 255, .. link_color};
  println!("Blue = rgb({}, {}, {})", blue.red, blue.green, blue.blue); //Blue = rgb(0, 0, 255)

  // destructure the instance using a `let` binding, this will not destruct blue instance
  let Color {red: r, green: g, blue: b} = blue;
  println!("Blue = rgb({}, {}, {})", r, g, b); //Blue = rgb(0, 0, 255)

  // creating an instance via functions & accessing it's fields
  let midnightblue = get_midnightblue_color();
  println!("Midnight Blue = rgb({}, {}, {})", midnightblue.red, midnightblue.green, midnightblue.blue); //Midnight Blue = rgb(25, 25, 112)

  // destructure the instance using a `let` binding
  let Color {red: r, green: g, blue: b} = get_midnightblue_color();
  println!("Midnight Blue = rgb({}, {}, {})", r, g, b); //Midnight Blue = rgb(25, 25, 112)
}

fn get_midnightblue_color() -> Color {
    Color {red: 25, green: 25, blue: 112}
} 
```

## 02\. 元组结构体

⭐️ 当元组结构只有一个元素时，我们称之为 'newtype' 模式。因为它有助于创建一个新类型。

```
struct Color (u8, u8, u8);
struct Kilometers(i32);

fn main() {
  // creating an instance
  let black = Color (0, 0, 0);

  // destructure the instance using a `let` binding, this will not destruct black instance
  let Color (r, g, b) = black;
  println!("Black = rgb({}, {}, {})", r, g, b); //black = rgb(0, 0, 0);

  //newtype pattern
  let distance = Kilometers(20);
  // destructure the instance using a `let` binding
  let Kilometers(distance_in_km) = distance;
  println!("The distance: {} km", distance_in_km); //The distance: 20 km
} 
```

## 03\. 单元结构体

这本身很少有用，但与其他功能结合使用时，它可以变得有用。

> 📖 例如：一个库可能会要求您创建一个实现某个特定特征以处理事件的结构。如果您不需要在结构中存储任何数据，可以创建一个类似于单元的结构。

```
struct Electron;

fn main() {
  let x = Electron;
} 
```

# 枚举

⭐️ 枚举是一个单一类型。它包含变体，这些是枚举在给定时间的可能值。例如，

```
enum Day {
    Sunday,
    Monday, 
    Tuesday, 
    Wednesday, 
    Thursday,
    Friday,
    Saturday
}

// Day is the enum
// Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday are the variants 
```

⭐️ 可以通过 :: 符号访问变体，例如 Day::Sunday

⭐️ 每个枚举变体都可以有，

+   无数据（单元变体）
+   未命名的有序数据（元组变体）
+   命名数据（struct 变体）

```
enum FlashMessage {
  Success, //a unit variant
  Warning{ category: i32, message: String }, //a struct variant
  Error(String) //a tuple variant
}

fn main() {
  let mut form_status = FlashMessage::Success;
  print_flash_message(form_status);

  form_status = FlashMessage::Warning {category: 2, message: String::from("Field X is required")};
  print_flash_message(form_status);

  form_status = FlashMessage::Error(String::from("Connection Error"));
  print_flash_message(form_status);
}

fn print_flash_message(m : FlashMessage) {
  // pattern matching with enum
  match m {
    FlashMessage::Success => 
      println!("Form Submitted correctly"),
    FlashMessage::Warning {category, message} => //Destructure, should use same field names
      println!("Warning : {} - {}", category, message),
    FlashMessage::Error(msg) => 
      println!("Error : {}", msg)
  }
} 
```

# 泛型

> 📖 有时，在编写函数或数据类型时，我们可能希望它适用于多种类型的参数。在 Rust 中，我们可以使用泛型来实现这一点。

💭 这个概念是，我们不是声明一个特定的数据类型，而是使用一个大写字母（或 CamelCase 标识符）。例如，代替 x : u8，我们使用 x : T。但我们必须向编译器声明 T 是一个泛型类型（可以是任何类型），通过在最前面添加 <t class="hljs-meta">。</t>

// generalizing functions
//-----------------------
fn takes_anything<T>(x: T) { // x has type T, T is a generic type
}

fn takes_two_of_the_same_things<T>(x: T, y: T) { // both x and y has same type
}

fn takes_two_things<T, U>(x: T, y: U) { // multiple types
}

// generalizing structs
//---------------------
struct Point<T> {
  x: T,
  y: T,
}

fn main() {
  let point_a = Point { x: 0, y: 0 }; // T is a int type
  let point_b = Point { x: 0.0, y: 0.0 }; // T is a float type
}

// 🔎 When addding an implementation for a generic struct, the type parameters should be declared after the impl as well
// impl<T> Point<T> {

// generalizing enums
//-------------------
enum Option<T> {
    Some(T),
    None,
}

enum Result<T, E> {
    Ok(T),
    Err(E),
} 
```

> ⭐️ 上述 Option 和 Result 类型是 Rust 标准库中已经定义的一些特殊泛型类型。

> 
> +   可选值可以是 Some 值，也可以是没有值 / None。
> +   
> +   结果可以表示成功 / Ok 或失败 / Err

```
// 01 - - - - - - - - - - - - - - - - - - - - - -
fn getIdByUsername(username: &str) -> Option<usize> {
    //if username can be found in the system, set userId
        return Some(userId);
    //else
        None
}

//💭 So on above function, instead of setting return type as usize
// set return type as Option<usize>
//Instead of return userId, return Some(userId)
// else None (💡remember? last return statement no need return keyword and ending ;)

// 02 - - - - - - - - - - - - - - - - - - - - - -
struct Task {
    title: String,
    assignee: Option<Person>,
}

//💭 Instead of assignee: Person, we use Option<Person>
//Because the task has not been assigned to a specific person

// - - - - - - - - - - - - - - - - - - - - - - -
//when using Option types as return types on functions
// we can use pattern matching to catch the relevant return type(Some/None) when calling them

fn main() {
    let username = "anonymous"
    match getIdByUsername(username) {
        None => println!("User not found"),
        Some(i) => println!("User Id: {}", i)
    }
} 
```

> 📖 Option 类型是使用 Rust 的类型系统来表达缺失可能性的一种方式。Result 表达了错误的可能性。

```
// - - - - - - - - - - - - - - - - - - - - - -
fn get_word_count_from_file(file_name: &str) -> Result<u32, &str> {
  //if the file is not found on the system, return error
    return Err("File can not be found!")
  //else, count and return the word count 
    //let mut word_count: u32; ....
    Ok(word_count)
}

//💭 on above function, 
// instead panic(break) the app, when a file can not be found; return Err(something)
// or when it could get the relevant data; return Ok(data)

// - - - - - - - - - - - - - - - - - - - - - - -
// we can use pattern matching to catch the relevant return type(Ok/Err) when calling it

fn main() {
    let mut file_name = "file_a";
    match get_word_count_from_file(file_name) {
        Ok(i) => println!("Word Count: {}", i),
        Err(e) => println!("Error: {}", e)
    }
} 
```

> 🔎 在 Option 和 Result 类型周围已经实现了许多有用的方法。关于它们的更多信息可以在 Rust 文档中的 std::option::Option 和 std::result::Result 页面找到。

⭐️ 在 Rust 文档的错误处理部分也可以找到更多关于选项（Options）和结果（Results）的实用示例。

# 实现 & 特征

💡 当我们讨论类似于 C 的结构体时，我提到过它们与其他语言（如 Java）中的类相似，但没有它们的方法。impls 用于为 Rust 结构体和枚举定义方法。

💡 特征与其他语言（如 Java）中的接口有些相似。它们用于定义类型必须提供的功能。一个类型可以实现多个特征。

⭐️⭐️⭐️ 但特征也可以包含方法的默认实现。当实现类型时，可以覆盖默认方法。

```
// 01 -----------------------------------------
// Adding methoids directly; without using traits

struct Player {
    first_name: String,
    last_name: String,
}

impl Player {
    fn full_name(&self) -> String {
        format!("{} {}", self.first_name, self.last_name)
    }
}

fn main() {
    let player_1 = Player {
        first_name: "Rafael".to_string(),
        last_name: "Nadal".to_string(),
    };

    println!("Player 01: {}", player_1.full_name());
}

// 02 -----------------------------------------
// Adding methoids by implementing traits

struct Player {
    first_name: String,
    last_name: String,
}

trait FullName {
    fn full_name(&self) -> String;
}

impl FullName for Player {
    fn full_name(&self) -> String {
        format!("{} {}", self.first_name, self.last_name)
    }
}

fn main() {
    let player_2 = Player {
        first_name: "Roger".to_string(),
        last_name: "Federer".to_string(),
    };

    println!("Player 02: {}", player_2.full_name());
}

// 03 -----------------------------------------
// a trait with default implementations of methods

trait Foo {
    fn bar(&self);
    fn baz(&self) { println!("We called baz."); }
}

// --------------------------------------------
// ⭐️ In case 01, implementation must appear in the same crate as the self type

// 💡 And also in Rust, new traits can be implemented for existing types even for types like i8, f64 and etc.
// Same way existing traits can be implemented for new types you are creating.
// But we can not implement existing traits into existing types

// 🔎 Other than functions, traits can contain constants and types

// 🔎 Traits also supprot generics; should specify after the trait name like generic functions

trait From<T> {
    fn from(T) -> Self;
}
    impl From<u8> for u16 { 
        //... 
    }
    impl From<u8> for u32{
        //...
    } 
```

⭐️ 正如您所见，方法接受一个特殊的第一个参数，即类型本身。它可以是 self、&self 或 &mut self。如果它是堆栈上的值（拥有权），则为 self，如果它是引用，则为 &self，如果它是可变引用，则为 &mut self。

> ⭐️ 一些其他语言支持静态方法。这时，我们可以直接通过类调用一个函数而不创建对象。在 Rust 中，我们称之为关联函数。当从结构体调用它们时，我们使用 :: 而不是 .。例如，Person::new（“埃隆·马斯克·小”）;

```
struct Player {
    first_name: String,
    last_name: String,
}

impl Player {
    fn new(first_name: String, last_name: String) -> Player {
        Player {
            first_name : first_name,
            last_name : last_name,
        }
    }

    fn full_name(&self) -> String {
        format!("{} {}", self.first_name, self.last_name)
    }
}

fn main() {
    let player_name = Player::new("Serena".to_string(), "Williams".to_string()).full_name();
    println!("Player: {}", player_name);
}

// we have used :: notation for `new()` and . notation for `full_name()`

// 🔎 Also in here we have used `Method Chaining`. Instead of using two statements for new() and full_name() 
// calls, we can use a single statement with Method Chaining. 
// ex. player.add_points(2).get_point_count(); 
```

⭐️ 特征可以继承自其他特征。

```
trait Person {
    fn full_name(&self) -> String;
}

    trait Employee : Person { //Employee inherit from person trait
      fn job_title(&self) -> String;
    }

    trait ExpatEmployee : Employee + Expat { //ExpatEmployee inherit from Employee and Expat traits
      fn additional_tax(&self) -> f64;
    } 
```

🔎 虽然 Rust 偏向于静态分派，但也支持通过一种称为‘特质对象’的机制进行动态分派。

> 🅆 动态分派是在运行时选择要调用的多态操作（方法或函数）的过程。

```
trait GetSound {
    fn get_sound(&self) -> String;
}

struct Cat {
    sound: String,
}
    impl GetSound for Cat {
        fn get_sound(&self) -> String {
            self.sound.clone()
        }
    }

struct Bell {
    sound: String,
}
    impl GetSound for Bell {
        fn get_sound(&self) -> String {
            self.sound.clone()
        }
    }

fn make_sound<T: GetSound>(t: &T) {
    println!("{}!", t.get_sound())
}

fn main() {
    let kitty = Cat { sound: "Meow".to_string() };
    let the_bell = Bell { sound: "Ding Dong".to_string() };

    make_sound(&kitty); // Meow!
    make_sound(&the_bell); // Ding Dong!
} 
```

# 拥有权

```
fn main() {
    let a = [1, 2, 3];
    let b = a;
    println!("{:?} {:?}", a, b); // [1, 2, 3] [1, 2, 3]
}

fn main() {
    let a = vec![1, 2, 3];
    let b = a;
    println!("{:?} {:?}", a, b); // Error; use of moved value: `a`
} 
```

在上面的例子中，我们只是尝试**将‘a’的值赋给‘b’**。两个代码块中的代码几乎相同，但有**两种不同的数据类型**。第二个会报错。这是因为**所有权**。

⭐️ 变量绑定拥有它们所绑定的**所有权**。一段数据一次只能有**一个所有者**。当一个绑定超出范围时，Rust 会释放绑定的资源。这就是 Rust 实现**内存安全**的方式。

> [所有权（名词）](https://github.com/nikomatsakis/rust-tutorials-keynote/blob/master/Ownership%20and%20Borrowing.pdf)

> 
> 拥有某物的行为、状态或权利。

⭐️ **当将**一个变量绑定**赋给另一个变量绑定**时（不引用），如果其数据类型是一个

1.  **复制类型**
    +   绑定的资源被**复制并分配**或传递给函数。
    +   原始绑定的所有权状态被设置为**“复制”状态**。
    +   **大多数原始类型**
1.  **移动类型**
    +   绑定的资源被**移动**到新的变量绑定，我们**无法再访问原始的变量绑定**。
    +   原始绑定的所有权状态被设置为**“移动”状态**。
    +   **非原始类型**

> 🔎 一个类型的功能由已实现的特质处理。默认情况下，变量绑定具有‘移动语义’。但是，如果一个类型实现了[**core::marker::Copy trait**](https://doc.rust-lang.org/core/marker/trait.Copy.html)，它具有'复制语义'。

💡 **所以在上面的第二个例子中，Vec 对象的所有权移动到“b”，“a”没有所有权访问资源。**

# 借用

在实际应用中，大多数情况下我们需要将变量绑传递给其他函数或将它们分配给另一个变量绑定。在这种情况下，我们**引用**原始绑定；**借用**它的数据。

> [借用（动词）](https://github.com/nikomatsakis/rust-tutorials-keynote/blob/master/Ownership%20and%20Borrowing.pdf)

> 
> 带有承诺返回的接收。

⭐️ 有两种借用类型，

1.  **共享借用** `(&T)`
    +   一段数据可以被**单个或多个用户借用**，但**数据不应该被更改**。
1.  **可变借用** `(&mut T)`
    +   一段数据可以被**单个用户借用并更改**，但此时其他用户不应该能够访问该数据。

⭐️ 还有关于借用的**非常重要的规则**，

1.  一段数据可以被借用为**共享借用** **或** 作为可变借用 **之一**。但不能同时发生。
1.  借用**适用于复制类型和移动类型**。
1.  **活性**的概念 ↴

```
fn main() {
  let mut a = vec![1, 2, 3];
  let b = &mut a;  //  &mut borrow of a starts here
                   //  ⁝
  // some code     //  ⁝
  // some code     //  ⁝
}                  //  &mut borrow of a ends here

fn main() {
  let mut a = vec![1, 2, 3];
  let b = &mut a;  //  &mut borrow of a starts here
  // some code

  println!("{:?}", a); // trying to access a as a shared borrow, so giving error
}                  //  &mut borrow of a ends here

fn main() {
  let mut a = vec![1, 2, 3];
  {
    let b = &mut a;  //  &mut borrow of a starts here
    // any other code
  }                  //  &mut borrow of a ends here

  println!("{:?}", a); // allow to borrow a as a shared borrow
} 
```

💡 **让我们看看如何在示例中使用共享和可变借用。**

+   共享借用示例

```
fn main() {
    let a = [1, 2, 3];
    let b = &a;
    println!("{:?} {}", a, b[0]); // [1, 2, 3] 1
}

fn main() {
    let a = vec![1, 2, 3];
    let b = get_first_element(&a);

    println!("{:?} {}", a, b); // [1, 2, 3] 1
}

fn get_first_element(a: &Vec<i32>) -> i32 {
    a[0]
} 
```

+   可变借用示例

```
fn main() {
    let mut a = [1, 2, 3];
    let b = &mut a;
    b[0] = 4;
    println!("{:?}", b); // [4, 2, 3]
}

fn main() {
    let mut a = [1, 2, 3];
    {
        let b = &mut a;
        b[0] = 4;
    }

    println!("{:?}", a); // [4, 2, 3]
}

fn main() {
    let mut a = vec![1, 2, 3];
    let b = change_and_get_first_element(&mut a);

    println!("{:?} {}", a, b); // [4, 2, 3] 4
}

fn change_and_get_first_element(a: &mut Vec<i32>) -> i32 {
    a[0] = 4;
    a[0]
} 
```

# 生命周期

当我们处理引用时，我们必须确保引用的数据在我们停止使用引用之前保持存活。

想一想，

+   我们有一个变量绑定，“**a**”。
+   我们正在引用“a”的值，来自另一个变量绑定“**x**”。我们必须确保“a”在我们停止使用“x”之前**存活**。

> 🔎 **内存管理**是应用于计算机内存的资源管理形式。直到 1990 年代中期，大多数编程语言使用**手动内存管理**，需要程序员给出手动指令来识别和释放未使用的对象/垃圾。约 1959 年，约翰·麦卡锡发明了**垃圾收集**(GC)，一种**自动内存管理**(AMM)形式。它确定哪些内存不再使用并自动释放，而不依赖于程序员。然而，**Objective-C 和 Swift**通过**自动引用计数**(ARC)提供类似功能。

在 Rust 中，

+   一个资源一次只能有**一个所有者**。当它超出范围时，Rust 会将其从内存中移除。
+   当我们想要重复使用相同的资源时，我们正在**引用**它/ **借用**其内容。
+   处理**引用**时，我们必须指定**生命周期注解**，以便为**编译器**提供指示，设置这些引用资源**应该存活多久**。
+   ⭐️但是由于生命周期注解使**代码更冗长**，为了使**常见模式**更符合人体工程学，Rust 允许在`fn`定义中**省略**生命周期。在这种情况下，编译器会**隐式**分配生命周期注解。

生命周期注解在**编译时检查**。编译器在数据第一次和最后一次使用时进行检查。根据这一点，Rust 在**运行时**管理内存。这是 Rust 编译时间**较慢**的主要原因。

> +   与 C 和 C++**不同**，Rust 通常不会显式丢弃值。
> +   
> +   与 GC 不同，Rust 不会在数据不再被引用的地方放置释放调用。
> +   
> +   Rust 在数据即将超出范围的地方放置释放调用，然后强制确保在那一点之后不存在对该资源的引用。

💡 生命周期用撇号表示。按照惯例，小写字母用于命名。通常以**'a**开头，并在需要添加**多个生命周期**注解时按字母顺序**跟随**。

在使用引用时，

𝟎𝟏. 在**函数声明**中
+   带有引用的输入和输出参数应在`&`符号后附加生命周期。例如 `..(x: &'a str)`，`..(x: &'a mut str)`
+   在函数名之后，我们应该提到给定的生命周期是泛型类型。例如 `fn foo<'a>(..)`，`fn foo<'a, 'b>(..)`



```
// no inputs, return a reference
fn function<'a>() -> &'a str {} 

// single input
fn function<'a>(x: &'a str) {}

// single input and output, both has same lifetime
// output should live at least as long as input exists
fn function<'a>(x: &'a str) -> &'a str {}

// multiple inputs, only one input and the output share same lifetime
// output should live at least as long as y exists
fn function<'a>(x: i32, y: &'a str) -> &'a str {}

// multiple inputs. both inputs and the output share same lifetime
// output should live at least as long as x and y exist
fn function<'a>(x: &'a str, y: &'a str) -> &'a str {}

// multiple inputs. inputs can have diffent lifetimes 🔎
// output should live at least as long as x exists
fn function<'a, 'b>(x: &'a str, y: &'b str) -> &'a str {} 
```

𝟎𝟐. 在**结构体或枚举声明**中

+   具有引用的元素应在`&`符号后附加生命周期。

+   在结构体或枚举的名称之后，我们应该提到给定的生命周期是泛型类型。

```
// single element
// data of x should live at least as long as Struct exists
struct Struct<'a> { 
    x: &'a str 
}

// multiple elements
// data of x and y should live at least as long as Struct exists
struct Struct<'a> { 
    x: &'a str,
    y: &'a str 
}

// variant with single element
// data of the variant should live at least as long as Enum exists
enum Enum<'a> { 
    Variant(&'a Type)
} 
```

𝟎𝟑. 使用**Impls 和 Traits**

```
struct Struct<'a> { 
    x: &'a str 
}
    impl<'a> Struct<'a> { 
        fn function<'a>(&self) -> &'a str {
            self.x 
        }
    }

struct Struct<'a> { 
    x: &'a str,
    y: &'a str
}
    impl<'a> Struct<'a> { 
        fn new(x: &'a str, y: &'a str) -> Struct<'a> { //no need to specify <'a> after new; impl already has it
          Struct {
              x : x,
              y : y
          }
        }
    }

// 🔎
impl<'a> Trait<'a> for Type
impl<'a> Trait for Type<'a> 
```

𝟎𝟒. 使用**泛型类型**

```
// 🔎
fn function<F>(f: F) where for<'a> F: FnOnce(&'a Type)
struct Struct<F> where for<'a> F: FnOnce(&'a Type) { x: F }
enum Enum<F> where for<'a> F: FnOnce(&'a Type) { Variant(F) }
impl<F> Struct<F> where for<'a> F: FnOnce(&'a Type) { fn x(&self) -> &F { &self.x } } 
```

### 生命周期省略

正如我之前提到的，为了使**常见模式**更符合人体工程学，Rust 允许省略生命周期。这个过程称为**生命周期省略**。

💡 目前 Rust 仅在`fn`定义中支持生命周期省略。但在未来，它也将支持`impl`头部的生命周期省略。

⭐️ fn 定义的生命周期注释可以被省略

如果其**参数列表**中有要么，

+   **只有一个输入参数通过引用传递**。

+   具有**要么** `&self` **要么** **&mut self** 引用的参数。

```
fn triple(x: &u64) -> u64 { //only one input parameter passes by reference
    x * 3
}

fn filter(x: u8, y: &str) -> &str { // only one input parameter passes by reference
    if x > 5 { y } else { "invalid inputs" }
}

struct Player<'a> { 
    id: u8,
    name: &'a str
}
    impl<'a> Player<'a> { //so far Lifetime Elisions are allowed only on fn definitions; but in the future they might support on impl headers as well.
        fn new(id: u8, name: &str) -> Player { //only one input parameter passes by reference
            Player {
                id : id,
                name : name
            }
        }

        fn heading_text(&self) -> String { // a fn definition with &self (or &mut self) reference
            format!("{}: {}", self.id, self.name)
        }
    }

fn main() {
    let player1 = Player::new(1, "Serena Williams");
    let player1_heading_text = player1.heading_text()
    println!("{}", player1_heading_text);
} 
```

> 💡 在 fn 定义的生命周期省略过程中，

> 

> +   每个通过引用传递的参数都有一个不同的生命周期注释。例如 `..(x: &str, y: &str)` 🡒 `..<'a, 'b>(x: &'a str, y: &'b str)`

> +   

> +   如果参数列表只有一个通过引用传递的参数，则该生命周期将分配给该函数返回值中所有省略的生命周期。例如 `..(x: i32, y: &str) -> &str` 🡒 `..<'a>(x: i32, y: &'a str) -> &'a str`

> +   

> +   即使它有多个通过引用传递的参数，如果其中一个有 &self 或 &mut self，self 的生命周期将分配给所有省略的输出生命周期。例如 `impl Impl{ fn function(&self, x: &str) -> &str {} }` 🡒 `impl<'a> Impl<'a>{ fn function(&'a self, x: &'b str) -> &'a str {} }`

> +   

> +   对于所有其他情况，我们必须手动编写生命周期注释。

### 'static

⭐️ `'static` 生命周期注释是一个**保留**的生命周期注释。这些引用在整个程序中都有效。它们保存在二进制文件的数据段中，所引用的数据永远不会超出作用域。

💡 **让我们看看如何在示例中使用生命周期注释。**

```
fn greeting<'a>() -> &'a str {
  "Hi!"
}

fn fullname<'a>(fname: &'a str, lname: &'a str) -> String {
  format!("{} {}", fname, lname)
}

struct Person<'a> { 
    fname: &'a str,
    lname: &'a str
}
  impl<'a> Person<'a> {
      fn new(fname: &'a str, lname: &'a str) -> Person<'a> { //no need to specify <'a> after new; impl already has it
          Person {
              fname : fname,
              lname : lname
          }
      }

      fn fullname(&self) -> String {
          format!("{} {}", self.fname , self.lname)
      }
  }

fn main() {
    let player = Person::new("Serena", "Williams");
    let player_fullname = player.fullname();

    println!("Player: {}", player_fullname);
} 
```
