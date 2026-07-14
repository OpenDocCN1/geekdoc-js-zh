![](media/cover-epub.jpg)

![cover image](media/cover-epub.jpg)

# Deep JavaScript

Dr. Axel Rauschmayer

2019

# Deep JavaScript

1.  [Deep JavaScript](#ch001.xhtml_deep-javascript)
2.  [1 About this book](#ch002.xhtml_ch_about-book)
    1.  [1.1 Where is the homepage of this book?](#ch002.xhtml_where-is-the-homepage-of-this-book)
    2.  [1.2 What is in this book?](#ch002.xhtml_what-is-in-this-book)
    3.  [1.3 What do I get for my money?](#ch002.xhtml_what-do-i-get-for-my-money)
    4.  [1.4 How can I preview the content?](#ch002.xhtml_how-can-i-preview-the-content)
    5.  [1.5 How do I report errors?](#ch002.xhtml_how-do-i-report-errors)
    6.  [1.6 Tips for reading](#ch002.xhtml_tips-for-reading)
    7.  [1.7 Notations and conventions](#ch002.xhtml_notations-and-conventions)
    8.  [1.8 Acknowledgement](#ch002.xhtml_acknowledgement)
3.  [2 Type coercion in JavaScript](#ch003.xhtml_ch_type-coercion)
    1.  [2.1 What is type coercion?](#ch003.xhtml_what-is-type-coercion)
    2.  [2.2 Operations that help implement coercion in the ECMAScript specification](#ch003.xhtml_operations-that-help-implement-coercion-in-the-ecmascript-specification)
    3.  [2.3 Intermission: expressing specification algorithms in JavaScript](#ch003.xhtml_intermission-expressing-specification-algorithms-in-javascript)
    4.  [2.4 Example coercion algorithms](#ch003.xhtml_example-coercion-algorithms)
    5.  [2.5 Operations that coerce](#ch003.xhtml_operations-that-coerce)
    6.  [2.6 Glossary: terms related to type conversion](#ch003.xhtml_glossary-terms-related-to-type-conversion)
4.  [3 The destructuring algorithm](#ch004.xhtml_ch_destructuring-algorithm)
    1.  [3.1 Preparing for the pattern matching algorithm](#ch004.xhtml_preparing-for-the-pattern-matching-algorithm)
    2.  [3.2 The pattern matching algorithm](#ch004.xhtml_the-pattern-matching-algorithm)
    3.  [3.3 Empty object patterns and Array patterns](#ch004.xhtml_empty-object-patterns-and-array-patterns)
    4.  [3.4 Applying the algorithm](#ch004.xhtml_applying-the-algorithm)
5.  [4 A detailed look at global variables](#ch005.xhtml_ch_global-scope)
    1.  [4.1 Scopes](#ch005.xhtml_scopes)
    2.  [4.2 Lexical environments](#ch005.xhtml_lexical-environments)
    3.  [4.3 The global object](#ch005.xhtml_the-global-object)
    4.  [4.4 In browsers, `globalThis` does not point directly to the global object](#ch005.xhtml_window-proxy)
    5.  [4.5 The global environment](#ch005.xhtml_the-global-environment)
    6.  [4.6 Conclusion: Why does JavaScript have both normal global variables and the global object?](#ch005.xhtml_conclusion-why-does-javascript-have-both-normal-global-variables-and-the-global-object)
    7.  [4.7 Further reading and sources of this chapter](#ch005.xhtml_further-reading-and-sources-of-this-chapter)
6.  [5 `%` is a remainder operator, not a modulo operator](#ch006.xhtml_ch_remainder-vs-modulo)
    1.  [5.1 Remainder operator `rem` vs. modulo operator `mod`](#ch006.xhtml_remainder-operator-rem-vs.-modulo-operator-mod)
    2.  [5.2 An intuitive understanding of the remainder operation](#ch006.xhtml_an-intuitive-understanding-of-the-remainder-operation)
    3.  [5.3 An intuitive understanding of the modulo operation](#ch006.xhtml_an-intuitive-understanding-of-the-modulo-operation)
    4.  [5.4 Similarities and differences between `rem` and `mod`](#ch006.xhtml_similarities-and-differences-between-rem-and-mod)
    5.  [5.5 The equations behind remainder and modulo](#ch006.xhtml_the-equations-behind-remainder-and-modulo)
    6.  [5.6 Where are `rem` and `mod` used in programming languages?](#ch006.xhtml_where-are-rem-and-mod-used-in-programming-languages)
    7.  [5.7 Further reading and sources of this chapter](#ch006.xhtml_further-reading-and-sources-of-this-chapter-1)
7.  [6 Copying objects and Arrays](#ch007.xhtml_ch_copying-objects-and-arrays)
    1.  [6.1 Shallow copying vs. deep copying](#ch007.xhtml_shallow-copying-vs.-deep-copying)
    2.  [6.2 Shallow copying in JavaScript](#ch007.xhtml_shallow-copying-in-javascript)
    3.  [6.3 Deep copying in JavaScript](#ch007.xhtml_deep-copying-in-javascript)
    4.  [6.4 Further reading](#ch007.xhtml_further-reading)
8.  [7 Updating data destructively and non-destructively](#ch008.xhtml_ch_updating-destructively-and-nondestructively)
    1.  [7.1 Examples: updating an object destructively and non-destructively](#ch008.xhtml_examples-updating-an-object-destructively-and-non-destructively)
    2.  [7.2 Examples: updating an Array destructively and non-destructively](#ch008.xhtml_examples-updating-an-array-destructively-and-non-destructively)
    3.  [7.3 Manual deep updating](#ch008.xhtml_manual-deep-updating)
    4.  [7.4 Implementing generic deep updating](#ch008.xhtml_implementing-generic-deep-updating)
9.  [8 The problems of shared mutable state and how to avoid them](#ch009.xhtml_ch_shared-mutable-state)
    1.  [8.1 What is shared mutable state and why is it problematic?](#ch009.xhtml_what-is-shared-mutable-state-and-why-is-it-problematic)
    2.  [8.2 Avoiding sharing by copying data](#ch009.xhtml_avoiding-sharing-by-copying-data)
    3.  [8.3 Avoiding mutations by updating non-destructively](#ch009.xhtml_avoiding-mutations-by-updating-non-destructively)
    4.  [8.4 Preventing mutations by making data immutable](#ch009.xhtml_preventing-mutations-by-making-data-immutable)
    5.  [8.5 Libraries for avoiding shared mutable state](#ch009.xhtml_libraries-for-avoiding-shared-mutable-state)
10.  [9 Property attributes: an introduction](#ch010.xhtml_ch_property-attributes-intro)
    1.  [9.1 The structure of objects](#ch010.xhtml_the-structure-of-objects)
    2.  [9.2 Property descriptors](#ch010.xhtml_property-descriptors)
    3.  [9.3 Retrieving descriptors for properties](#ch010.xhtml_retrieving-descriptors-for-properties)
    4.  [9.4 Defining properties via descriptors](#ch010.xhtml_defining-properties-via-descriptors)
    5.  [9.5 `Object.create()`: Creating objects via descriptors](#ch010.xhtml_object.create-creating-objects-via-descriptors)
    6.  [9.6 Use cases for `Object.getOwnPropertyDescriptors()`](#ch010.xhtml_use-cases-for-object.getownpropertydescriptors)
    7.  [9.7 Omitting descriptor properties](#ch010.xhtml_omitting-descriptor-properties)
    8.  [9.8 What property attributes do built-in constructs use?](#ch010.xhtml_what-property-attributes-do-built-in-constructs-use)
    9.  [9.9 API: property descriptors](#ch010.xhtml_api-property-descriptors)
    10.  [9.10 Further reading](#ch010.xhtml_further-reading-1)
11.  [10 Protecting objects from being changed](#ch011.xhtml_ch_protecting-objects)
    1.  [10.1 Levels of protection: preventing extensions, sealing, freezing](#ch011.xhtml_levels-of-protection-preventing-extensions-sealing-freezing)
    2.  [10.2 Preventing extensions](#ch011.xhtml_preventing-extensions)
    3.  [10.3 Sealing](#ch011.xhtml_sealing)
    4.  [10.4 Freezing](#ch011.xhtml_freezing)
    5.  [10.5 Further reading](#ch011.xhtml_further-reading-2)
12.  [11 Properties: assignment vs. definition](#ch012.xhtml_ch_property-assignment-vs-definition)
    1.  [11.1 Assignment vs. definition](#ch012.xhtml_assignment-vs.-definition)
    2.  [11.2 Assignment and definition in theory (optional)](#ch012.xhtml_assignment-and-definition-in-theory-optional)
    3.  [11.3 Definition and assignment in practice](#ch012.xhtml_definition-and-assignment-in-practice)
    4.  [11.4 Which language constructs use definition, which assignment?](#ch012.xhtml_which-language-constructs-use-definition-which-assignment)
    5.  [11.5 Further reading and sources of this chapter](#ch012.xhtml_further-reading-and-sources-of-this-chapter-2)
13.  [12 Enumerability of properties](#ch013.xhtml_ch_enumerability)
    1.  [12.1 How enumerability affects property-iterating constructs](#ch013.xhtml_how-enumerability-affects-property-iterating-constructs)
    2.  [12.2 The enumerability of pre-defined and created properties](#ch013.xhtml_the-enumerability-of-pre-defined-and-created-properties)
    3.  [12.3 Use cases for enumerability](#ch013.xhtml_use-cases-for-enumerability)
    4.  [12.4 Conclusion](#ch013.xhtml_conclusion)
14.  [13 Techniques for instantiating classes](#ch014.xhtml_ch_creating-class-instances)
    1.  [13.1 The problem: initializing a property asynchronously](#ch014.xhtml_the-problem-initializing-a-property-asynchronously)
    2.  [13.2 Solution: Promise-based constructor](#ch014.xhtml_solution-promise-based-constructor)
    3.  [13.3 Solution: static factory method](#ch014.xhtml_solution-static-factory-method)
    4.  [13.4 Subclassing a Promise-based constructor (optional)](#ch014.xhtml_subclassing-a-promise-based-constructor-optional)
    5.  [13.5 Conclusion](#ch014.xhtml_conclusion-1)
    6.  [13.6 Further reading](#ch014.xhtml_further-reading-3)
15.  [14 Copying instances of classes: `.clone()` vs. copy constructors](#ch015.xhtml_ch_copying-class-instances)
    1.  [14.1 `.clone()` methods](#ch015.xhtml_clone-methods)
    2.  [14.2 Static factory methods](#ch015.xhtml_static-factory-methods)
    3.  [14.3 Acknowledgements](#ch015.xhtml_acknowledgements)
16.  [15 Immutable wrappers for collections](#ch016.xhtml_ch_immutable-collection-wrappers)
    1.  [15.1 Wrapping objects](#ch016.xhtml_wrapping-objects)
    2.  [15.2 An immutable wrapper for Maps](#ch016.xhtml_an-immutable-wrapper-for-maps)
    3.  [15.3 An immutable wrapper for Arrays](#ch016.xhtml_an-immutable-wrapper-for-arrays)
17.  [16 Regular expressions: lookaround assertions by example](#ch017.xhtml_ch_regexp-lookaround-assertions)
    1.  [16.1 Cheat sheet: lookaround assertions](#ch017.xhtml_cheat-sheet-lookaround-assertions)
    2.  [16.2 Warnings for this chapter](#ch017.xhtml_warnings-for-this-chapter)
    3.  [16.3 Example: Specifying what comes before or after a match (positive lookaround)](#ch017.xhtml_example-specifying-what-comes-before-or-after-a-match-positive-lookaround)
    4.  [16.4 Example: Specifying what does not come before or after a match (negative lookaround)](#ch017.xhtml_example-specifying-what-does-not-come-before-or-after-a-match-negative-lookaround)
    5.  [16.5 Interlude: pointing lookaround assertions inward](#ch017.xhtml_interlude-pointing-lookaround-assertions-inward)
    6.  [16.6 Example: match strings not starting with `'abc'`](#ch017.xhtml_example-match-strings-not-starting-with-abc)
    7.  [16.7 Example: match substrings that do not contain `'.mjs'`](#ch017.xhtml_example-match-substrings-that-do-not-contain-.mjs)
    8.  [16.8 Example: skipping lines with comments](#ch017.xhtml_example-skipping-lines-with-comments)
    9.  [16.9 Example: smart quotes](#ch017.xhtml_example-smart-quotes)
    10.  [16.10 Acknowledgements](#ch017.xhtml_acknowledgements-1)
    11.  [16.11 Further reading](#ch017.xhtml_further-reading-4)
18.  [17 Composing regular expressions via `re-template-tag`](#ch018.xhtml_ch_re-template-tag)
    1.  [17.1 The basics](#ch018.xhtml_the-basics)
    2.  [17.2 A tour of the features](#ch018.xhtml_a-tour-of-the-features)
    3.  [17.3 Why is this useful?](#ch018.xhtml_why-is-this-useful)
    4.  [17.4 `re` and named capture groups](#ch018.xhtml_re-and-named-capture-groups)
19.  [18 Exploring Promises by implementing them](#ch019.xhtml_ch_implementing-promises)
    1.  [18.1 Refresher: states of Promises](#ch019.xhtml_refresher-states-of-promises)
    2.  [18.2 Version 1: Stand-alone Promise](#ch019.xhtml_version-1-stand-alone-promise)
    3.  [18.3 Version 2: Chaining `.then()` calls](#ch019.xhtml_version-2-chaining-.then-calls)
    4.  [18.4 Convenience method `.catch()`](#ch019.xhtml_convenience-method-.catch)
    5.  [18.5 Omitting reactions](#ch019.xhtml_omitting-reactions)
    6.  [18.6 The implementation](#ch019.xhtml_the-implementation)
    7.  [18.7 Version 3: Flattening Promises returned from `.then()` callbacks](#ch019.xhtml_version-3-flattening-promises-returned-from-.then-callbacks)
    8.  [18.8 Version 4: Exceptions thrown in reaction callbacks](#ch019.xhtml_version-4-exceptions-thrown-in-reaction-callbacks)
    9.  [18.9 Version 5: Revealing constructor pattern](#ch019.xhtml_version-5-revealing-constructor-pattern)
20.  [19 The property `.name` of functions](#ch020.xhtml_ch_function-names)
    1.  [19.1 Names of functions](#ch020.xhtml_names-of-functions)
    2.  [19.2 Constructs that provide names for functions](#ch020.xhtml_constructs-that-provide-names-for-functions)
    3.  [19.3 Things to look out for with names of functions](#ch020.xhtml_things-to-look-out-for-with-names-of-functions)
    4.  [19.4 Changing the names of functions](#ch020.xhtml_changing-the-names-of-functions)
    5.  [19.5 The function property `.name` in the ECMAScript specification](#ch020.xhtml_the-function-property-.name-in-the-ecmascript-specification)

# Deep JavaScript

# 1 About this book

* * *

*   1.1 [Where is the homepage of this book?](#ch002.xhtml_where-is-the-homepage-of-this-book)
*   1.2 [What is in this book?](#ch002.xhtml_what-is-in-this-book)
*   1.3 [What do I get for my money?](#ch002.xhtml_what-do-i-get-for-my-money)
*   1.4 [How can I preview the content?](#ch002.xhtml_how-can-i-preview-the-content)
*   1.5 [How do I report errors?](#ch002.xhtml_how-do-i-report-errors)
*   1.6 [Tips for reading](#ch002.xhtml_tips-for-reading)
*   1.7 [Notations and conventions](#ch002.xhtml_notations-and-conventions)
    *   1.7.1 [What is a type signature? Why am I seeing static types in this book?](#ch002.xhtml_what-is-a-type-signature-why-am-i-seeing-static-types-in-this-book)
    *   1.7.2 [What do the notes with icons mean?](#ch002.xhtml_what-do-the-notes-with-icons-mean)
*   1.8 [Acknowledgement](#ch002.xhtml_acknowledgement)

* * *

## 1.1 Where is the homepage of this book?

The homepage of “Deep JavaScript” is [`exploringjs.com/deep-js/`](https://exploringjs.com/deep-js/)

## 1.2 What is in this book?

This book dives deeply into JavaScript:

*   It teaches practical techniques for using the language better.
*   It teaches how the language works and why. What it teaches is firmly grounded in the ECMAScript specification (which the book explains and refers to).
*   It covers only the language (ignoring platform-specific features such as browser APIs) but not exhaustively. Instead, it focuses on a selection of important topics.

## 1.3 What do I get for my money?

If you buy this book, you get:

*   The current content in four DRM-free versions:
    *   PDF file
    *   ZIP archive with ad-free HTML
    *   EPUB file
    *   MOBI file
*   Any future content that is added to this edition. How much I can add depends on the sales of this book.

The current price is introductory. It will increase as more content is added.

## 1.4 How can I preview the content?

[On the homepage of this book](https://exploringjs.com/deep-js/#previews), there are extensive previews for all versions of this book.

## 1.5 How do I report errors?

*   The HTML version of this book has links to comments at the end of each chapter.
*   They jump to GitHub issues, which [you can also access directly](https://github.com/rauschma/deep-js/issues).

## 1.6 Tips for reading

*   You can read the chapters in any order. Each one is self-contained but occasionally, there are references to other chapters with further information.
*   The headings of some sections are marked with “(optional)” meaning that they are non-essential. You will still understand the remainders of their chapters if you skip them.

## 1.7 Notations and conventions

### 1.7.1 What is a type signature? Why am I seeing static types in this book?

For example, you may see:

```
[](#cb1-1)Number.isFinite(num: number): boolean
```

That is called the *type signature* of `Number.isFinite()`. This notation, especially the static types `number` of `num` and `boolean` of the result, are not real JavaScript. The notation is borrowed from the compile-to-JavaScript language TypeScript (which is mostly just JavaScript plus static typing).

Why is this notation being used? It helps give you a quick idea of how a function works. The notation is explained in detail in [a 2ality blog post](https://2ality.com/2018/04/type-notation-typescript.html), but is usually relatively intuitive.

### 1.7.2 What do the notes with icons mean?

![](media/file0.svg)  **Reading instructions**

Explains how to best read the content.

![](media/file1.svg)  **External content**

Points to additional, external, content.

![](media/file2.svg)  **Tip**

Gives a tip related to the current content.

![](media/file3.svg)  **Question**

Asks and answers a question pertinent to the current content (think FAQ).

![](media/file4.svg)  **Warning**

Warns about pitfalls, etc.

![](media/file5.svg)  **Details**

Provides additional details, complementing the current content. It is similar to a footnote.

![](media/file6.svg)  **Exercise**

Mentions the path of a test-driven exercise that you can do at that point.

![](media/file7.svg)  **Quiz**

Indicates that there is a quiz for the current (part of a) chapter.

## 1.8 Acknowledgement

*   Thanks to Allen Wirfs-Brock for his advice via Twitter and blog post comments. It helped make this book better.

*   More people who contributed are acknowledged in the chapters.

# 2 Type coercion in JavaScript

* * *

*   2.1 [What is type coercion?](#ch003.xhtml_what-is-type-coercion)
    *   2.1.1 [Dealing with type coercion](#ch003.xhtml_dealing-with-type-coercion)
*   2.2 [Operations that help implement coercion in the ECMAScript specification](#ch003.xhtml_operations-that-help-implement-coercion-in-the-ecmascript-specification)
    *   2.2.1 [Converting to primitive types and objects](#ch003.xhtml_converting-to-primitive-types-and-objects)
    *   2.2.2 [Converting to numeric types](#ch003.xhtml_converting-to-numeric-types)
    *   2.2.3 [Converting to property keys](#ch003.xhtml_converting-to-property-keys)
    *   2.2.4 [Converting to Array indices](#ch003.xhtml_converting-to-array-indices)
    *   2.2.5 [Converting to Typed Array elements](#ch003.xhtml_converting-to-typed-array-elements)
*   2.3 [Intermission: expressing specification algorithms in JavaScript](#ch003.xhtml_intermission-expressing-specification-algorithms-in-javascript)
*   2.4 [Example coercion algorithms](#ch003.xhtml_example-coercion-algorithms)
    *   2.4.1 [`ToPrimitive()`](#ch003.xhtml_toprimitive)
    *   2.4.2 [`ToString()` and related operations](#ch003.xhtml_tostring-and-related-operations)
    *   2.4.3 [`ToPropertyKey()`](#ch003.xhtml_topropertykey)
    *   2.4.4 [`ToNumeric()` and related operations](#ch003.xhtml_tonumeric-and-related-operations)
*   2.5 [Operations that coerce](#ch003.xhtml_operations-that-coerce)
    *   2.5.1 [Addition operator (`+`)](#ch003.xhtml_addition-operator)
    *   2.5.2 [Abstract Equality Comparison (`==`)](#ch003.xhtml_abstract-equality-comparison)
*   2.6 [Glossary: terms related to type conversion](#ch003.xhtml_glossary-terms-related-to-type-conversion)

* * *

In this chapter, we examine the role of *type coercion* in JavaScript. We will go relatively deeply into this subject and, e.g., look into how the ECMAScript specification handles coercion.

## 2.1 What is type coercion?

Each operation (function, operator, etc.) expects its parameters to have certain types. If a value doesn’t have the right type for a parameter, three common options for, e.g., a function are:

1.  The function can throw an exception:

```
[](#cb2-1)function multiply(x, y) {
[](#cb2-2)  if (typeof x !== 'number' || typeof y !== 'number') {
[](#cb2-3)    throw new TypeError();
[](#cb2-4)  }
[](#cb2-5)  // ···
[](#cb2-6)}
```

2.  The function can return an error value:

```
[](#cb3-1)function multiply(x, y) {
[](#cb3-2)  if (typeof x !== 'number' || typeof y !== 'number') {
[](#cb3-3)    return NaN;
[](#cb3-4)  }
[](#cb3-5)  // ···
[](#cb3-6)}
```

3.  The function can convert its arguments to useful values:

```
[](#cb4-1)function multiply(x, y) {
[](#cb4-2)  if (typeof x !== 'number') {
[](#cb4-3)    x = Number(x);
[](#cb4-4)  }
[](#cb4-5)  if (typeof y !== 'number') {
[](#cb4-6)    y = Number(y);
[](#cb4-7)  }
[](#cb4-8)  // ···
[](#cb4-9)}
```

In (3), the operation performs an implicit type conversion. That is called *type coercion*.

JavaScript initially didn’t have exceptions, which is why it uses coercion and error values for most of its operations:

```
[](#cb5-1)// Coercion
[](#cb5-2)assert.equal(3 * true, 3);
[](#cb5-3)
[](#cb5-4)// Error values
[](#cb5-5)assert.equal(1 / 0, Infinity);
[](#cb5-6)assert.equal(Number('xyz'), NaN);
```

However, there are also cases (especially when it comes to newer features) where it throws exceptions if an argument doesn’t have the right type:

*   Accessing properties of `null` or `undefined`:

    ```
    > undefined.prop
    TypeError: Cannot read property 'prop' of undefined
    > null.prop
    TypeError: Cannot read property 'prop' of null
    > 'prop' in null
    TypeError: Cannot use 'in' operator to search for 'prop' in null
    ```

*   Using symbols:

    ```
    > 6 / Symbol()
    TypeError: Cannot convert a Symbol value to a number
    ```

*   Mixing bigints and numbers:

    ```
    > 6 / 3n
    TypeError: Cannot mix BigInt and other types
    ```

*   New-calling or function-calling values that don’t support that operation:

    ```
    > 123()
    TypeError: 123 is not a function
    > (class {})()
    TypeError: Class constructor  cannot be invoked without 'new'

    > new 123
    TypeError: 123 is not a constructor
    > new (() => {})
    TypeError: (intermediate value) is not a constructor
    ```

*   Changing read-only properties (only throws in strict mode):

    ```
    > 'abc'.length = 1
    TypeError: Cannot assign to read only property 'length'
    > Object.freeze({prop:3}).prop = 1
    TypeError: Cannot assign to read only property 'prop'
    ```

### 2.1.1 Dealing with type coercion

Two common ways of dealing with coercion are:

*   A caller can explicitly convert values so that they have the right types. For example, in the following interaction, we want to multiply two numbers encoded as strings:

    ```
    [](#cb11-1)let x = '3';
    [](#cb11-2)let y = '2';
    [](#cb11-3)assert.equal(Number(x) * Number(y), 6);
    ```

*   A caller can let the operation make the conversion for them:

    ```
    [](#cb12-1)let x = '3';
    [](#cb12-2)let y = '2';
    [](#cb12-3)assert.equal(x * y, 6);
    ```

I usually prefer the former, because it clarifies my intention: I expect `x` and `y` not to be numbers, but want to multiply two numbers.

## 2.2 Operations that help implement coercion in the ECMAScript specification

The following sections describe the most important internal functions used by the ECMAScript specification to convert actual parameters to expected types.

For example, in TypeScript, we would write:

```
[](#cb13-1)function isNaN(number: number) {
[](#cb13-2)  // ···
[](#cb13-3)}
```

In the specification, this looks [as follows](https://tc39.es/ecma262/#sec-multiplicative-operators-runtime-semantics-evaluation) (translated to JavaScript, so that it is easier to understand):

```
[](#cb14-1)function isNaN(number) {
[](#cb14-2)  let num = ToNumber(number);
[](#cb14-3)  // ···
[](#cb14-4)}
```

### 2.2.1 Converting to primitive types and objects

Whenever primitive types or objects are expected, the following conversion functions are used:

*   `ToBoolean()`
*   `ToNumber()`
*   `ToBigInt()`
*   `ToString()`
*   `ToObject()`

These internal functions have analogs in JavaScript that are very similar:

```
> Boolean(0)
false
> Boolean(1)
true

> Number('123')
123
```

After the introduction of bigints, which exists alongside numbers, the specification often uses `ToNumeric()` where it previously used `ToNumber()`. Read on for more information.

### 2.2.2 Converting to numeric types

At the moment, JavaScript has [two built-in numeric types](https://tc39.es/ecma262/#sec-numeric-types): number and bigint.

*   `ToNumeric()` returns a numeric value `num`. Its callers usually invoke a method `mthd` of the specification type of `num`:

    ```
    Type(num)::mthd(···)
    ```

    Among others, the following operations use `ToNumeric`:

    *   Prefix and postfix `++` operator
    *   `*` operator
*   `ToInteger(x)` is used whenever a number without a fraction is expected. The range of the result is often restricted further afterwards.

    *   It calls `ToNumber(x)` and removes the fraction (similar to `Math.trunc()`).
    *   Operations that use `ToInteger()`:
        *   `Number.prototype.toString(radix?)`
        *   `String.prototype.codePointAt(pos)`
        *   `Array.prototype.slice(start, end)`
        *   Etc.
*   `ToInt32()`, `ToUint32()` coerce numbers to 32-bit integers and are used by bitwise operators (see tbl. [1](#ch003.xhtml_tbl:bitwise-number-operator-coercion)).

    *   `ToInt32()`: signed, range [−2^(31), 2^(31)−1] (limits are included)
    *   `ToUint32()`: unsigned (hence the `U`), range [0, 2^(32)−1] (limits are included)

Table 1: Coercion of the operands of bitwise number operators (BigInt operators don’t limit the number of bits).

| Operator | Left operand | Right operand | result type |
| --- | --- | --- | --- |
| `<<` | `ToInt32()` | `ToUint32()` | `Int32` |
| signed `>>` | `ToInt32()` | `ToUint32()` | `Int32` |
| unsigned `>>>` | `ToInt32()` | `ToUint32()` | `Uint32` |
| `&`, `^`, `&#124;` | `ToInt32()` | `ToUint32()` | `Int32` |
| `~` | — | `ToInt32()` | `Int32` |

### 2.2.3 Converting to property keys

`ToPropertyKey()` returns a string or a symbol and is used by:

*   The bracket operator `[]`
*   Computed property keys in object literals
*   The left-hand side of the `in` operator
*   `Object.defineProperty(_, P, _)`
*   `Object.fromEntries()`
*   `Object.getOwnPropertyDescriptor()`
*   `Object.prototype.hasOwnProperty()`
*   `Object.prototype.propertyIsEnumerable()`
*   Several methods of `Reflect`

### 2.2.4 Converting to Array indices

*   `ToLength()` is used (directly) mainly for string indices.
    *   Helper function for `ToIndex()`
    *   Range of result `l`: 0 ≤ `l` ≤ 2^(53)−1
*   `ToIndex()` is used for Typed Array indices.
    *   Main difference with `ToLength()`: throws an exception if argument is out of range.
    *   Range of result `i`: 0 ≤ `i` ≤ 2^(53)−1
*   `ToUint32()` is used for Array indices.
    *   Range of result `i`: 0 ≤ `i` < 2^(32)−1 (the upper limit is excluded, to leave room for the `.length`)

### 2.2.5 Converting to Typed Array elements

When we set the value of a Typed Array element, one of the following conversion functions is used:

*   `ToInt8()`
*   `ToUint8()`
*   `ToUint8Clamp()`
*   `ToInt16()`
*   `ToUint16()`
*   `ToInt32()`
*   `ToUint32()`
*   `ToBigInt64()`
*   `ToBigUint64()`

## 2.3 Intermission: expressing specification algorithms in JavaScript

In the remainder of this chapter, we’ll encounter several specification algorithms, but “implemented” as JavaScript. The following list shows how some frequently used patterns are translated from specification to JavaScript:

*   Spec: If Type(value) is String
    JavaScript: `if (TypeOf(value) === 'string')`
    (very loose translation; `TypeOf()` is defined below)

*   Spec: If IsCallable(method) is true
    JavaScript: `if (IsCallable(method))`
    (`IsCallable()` is defined below)

*   Spec: Let numValue be ToNumber(value)
    JavaScript: `let numValue = Number(value)`

*   Spec: Let isArray be IsArray(O)
    JavaScript: `let isArray = Array.isArray(O)`

*   Spec: If O has a [[NumberData]] internal slot
    JavaScript: `if ('__NumberData__' in O)`

*   Spec: Let tag be Get(O, @@toStringTag)
    JavaScript: `let tag = O[Symbol.toStringTag]`

*   Spec: Return the string-concatenation of “[object ", tag, and "]”.
    JavaScript: `return '[object ' + tag + ']';`

`let` (and not `const`) is used to match the language of the specification.

Some things are omitted – for example, the [ReturnIfAbrupt shorthands](https://tc39.es/ecma262/#sec-returnifabrupt-shorthands) `?` and `!`.

```
[](#cb17-1)/**
[](#cb17-2) * An improved version of typeof
[](#cb17-3) */
[](#cb17-4)function TypeOf(value) {
[](#cb17-5)  const result = typeof value;
[](#cb17-6)  switch (result) {
[](#cb17-7)    case 'function':
[](#cb17-8)      return 'object';
[](#cb17-9)    case 'object':
[](#cb17-10)      if (value === null) {
[](#cb17-11)        return 'null';
[](#cb17-12)      } else {
[](#cb17-13)        return 'object';
[](#cb17-14)      }
[](#cb17-15)    default:
[](#cb17-16)      return result;
[](#cb17-17)  }
[](#cb17-18)}
[](#cb17-19)
[](#cb17-20)function IsCallable(x) {
[](#cb17-21)  return typeof x === 'function';
[](#cb17-22)}
```

## 2.4 Example coercion algorithms

### 2.4.1 `ToPrimitive()`

[The operation `ToPrimitive()`](https://tc39.es/ecma262/#sec-toprimitive) is an intermediate step for many coercion algorithms (some of which we’ll see later in this chapter). It converts an arbitrary values to primitive values.

`ToPrimitive()` is used often in the spec because most operators can only work with primitive values. For example, we can use the addition operator (`+`) to add numbers and to concatenate strings, but we can’t use it to concatenate Arrays.

This is what the JavaScript version of `ToPrimitive()` looks like:

```
[](#cb18-1)/**
[](#cb18-2) * @param  hint Which type is preferred for the result:
[](#cb18-3) *             string, number, or don’t care?
[](#cb18-4) */
[](#cb18-5)function ToPrimitive(input: any,
[](#cb18-6)  hint: 'string'|'number'|'default' = 'default') {
[](#cb18-7)    if (TypeOf(input) === 'object') {
[](#cb18-8)      let exoticToPrim = input[Symbol.toPrimitive]; // (A)
[](#cb18-9)      if (exoticToPrim !== undefined) {
[](#cb18-10)        let result = exoticToPrim.call(input, hint);
[](#cb18-11)        if (TypeOf(result) !== 'object') {
[](#cb18-12)          return result;
[](#cb18-13)        }
[](#cb18-14)        throw new TypeError();
[](#cb18-15)      }
[](#cb18-16)      if (hint === 'default') {
[](#cb18-17)        hint = 'number';
[](#cb18-18)      }
[](#cb18-19)      return OrdinaryToPrimitive(input, hint);
[](#cb18-20)    } else {
[](#cb18-21)      // input is already primitive
[](#cb18-22)      return input;
[](#cb18-23)    }
[](#cb18-24)  }
```

`ToPrimitive()` lets objects override the conversion to primitive via `Symbol.toPrimitive` (line A). If an object doesn’t do that, it is passed on to `OrdinaryToPrimitive()`:

```
[](#cb19-1)function OrdinaryToPrimitive(O: object, hint: 'string' | 'number') {
[](#cb19-2)  let methodNames;
[](#cb19-3)  if (hint === 'string') {
[](#cb19-4)    methodNames = ['toString', 'valueOf'];
[](#cb19-5)  } else {
[](#cb19-6)    methodNames = ['valueOf', 'toString'];
[](#cb19-7)  }
[](#cb19-8)  for (let name of methodNames) {
[](#cb19-9)    let method = O[name];
[](#cb19-10)    if (IsCallable(method)) {
[](#cb19-11)      let result = method.call(O);
[](#cb19-12)      if (TypeOf(result) !== 'object') {
[](#cb19-13)        return result;
[](#cb19-14)      }
[](#cb19-15)    }
[](#cb19-16)  }
[](#cb19-17)  throw new TypeError();
[](#cb19-18)}
```

#### 2.4.1.1 Which hints do callers of `ToPrimitive()` use?

The parameter `hint` can have one of three values:

*   `'number'` means: if possible, `input` should be converted to a number.
*   `'string'` means: if possible, `input` should be converted to a string.
*   `'default'` means: there is no preference for either numbers or strings.

These are a few examples of how various operations use `ToPrimitive()`:

*   `hint === 'number'`. The following operations prefer numbers:
    *   `ToNumeric()`
    *   `ToNumber()`
    *   `ToBigInt()`, `BigInt()`
    *   Abstract Relational Comparison (`<`)
*   `hint === 'string'`. The following operations prefer strings:
    *   `ToString()`
    *   `ToPropertyKey()`
*   `hint === 'default'`. The following operations are neutral w.r.t. the type of the returned primitive value:
    *   Abstract Equality Comparison (`==`)
    *   Addition Operator (`+`)
    *   `new Date(value)` (`value` can be either a number or a string)

As we have seen, the default behavior is for `'default'` being handled as if it were `'number'`. Only instances of `Symbol` and `Date` override this behavior (shown later).

#### 2.4.1.2 Which methods are called to convert objects to Primitives?

If the conversion to primitive isn’t overridden via `Symbol.toPrimitive`, `OrdinaryToPrimitive()` calls either or both of the following two methods:

*   `'toString'` is called first if `hint` indicates that we’d like the primitive value to be a string.
*   `'valueOf'` is called first if `hint` indicates that we’d like the primitive value to be a number.

The following code demonstrates how that works:

```
[](#cb20-1)const obj = {
[](#cb20-2)  toString() { return 'a' },
[](#cb20-3)  valueOf() { return 1 },
[](#cb20-4)};
[](#cb20-5)
[](#cb20-6)// String() prefers strings:
[](#cb20-7)assert.equal(String(obj), 'a');
[](#cb20-8)
[](#cb20-9)// Number() prefers numbers:
[](#cb20-10)assert.equal(Number(obj), 1);
```

A method with the property key `Symbol.toPrimitive` overrides the normal conversion to primitive. That is only done twice in the standard library:

*   `Symbol.prototype[Symbol.toPrimitive](hint)`
    *   If the receiver is an instance of `Symbol`, this method always returns the wrapped symbol.
    *   The rationale is that instances of `Symbol` have a `.toString()` method that returns strings. But even if `hint` is `'string'`, `.toString()` should not be called so that we don’t accidentally convert instances of `Symbol` to strings (which are a completely different kind of property key).
*   `Date.prototype[Symbol.toPrimitive](hint)`
    *   Explained in more detail next.

#### 2.4.1.3 `Date.prototype[Symbol.toPrimitive]()`

This is how Dates handle being converted to primitive values:

```
[](#cb21-1)Date.prototype[Symbol.toPrimitive] = function (
[](#cb21-2)  hint: 'default' | 'string' | 'number') {
[](#cb21-3)    let O = this;
[](#cb21-4)    if (TypeOf(O) !== 'object') {
[](#cb21-5)      throw new TypeError();
[](#cb21-6)    }
[](#cb21-7)    let tryFirst;
[](#cb21-8)    if (hint === 'string' || hint === 'default') {
[](#cb21-9)      tryFirst = 'string';
[](#cb21-10)    } else if (hint === 'number') {
[](#cb21-11)      tryFirst = 'number';
[](#cb21-12)    } else {
[](#cb21-13)      throw new TypeError();
[](#cb21-14)    }
[](#cb21-15)    return OrdinaryToPrimitive(O, tryFirst);
[](#cb21-16)  };
```

The only difference with the default algorithm is that `'default'` becomes `'string'` (and not `'number'`). This can be observed if we use operations that set `hint` to `'default'`:

*   [The `==` operator](#ch003.xhtml_abstract-equality-comparison) coerces objects to primitives (with a default hint) if the other operand is a primitive value other than `undefined`, `null`, and `boolean`. In the following interaction, we can see that the result of coercing the date is a string:

    ```
    [](#cb22-1)const d = new Date('2222-03-27');
    [](#cb22-2)assert.equal(
    [](#cb22-3)  d == 'Wed Mar 27 2222 01:00:00 GMT+0100'
    [](#cb22-4)       + ' (Central European Standard Time)',
    [](#cb22-5)  true);
    ```

*   [The `+` operator](#ch003.xhtml_addition-operator) coerces both operands to primitives (with a default hint). If one of the results is a string, it performs string concatenation (otherwise it performs numeric addition). In the following interaction, we can see that the result of coercing the date is a string because the operator returns a string.

    ```
    [](#cb23-1)const d = new Date('2222-03-27');
    [](#cb23-2)assert.equal(
    [](#cb23-3)  123 + d,
    [](#cb23-4)  '123Wed Mar 27 2222 01:00:00 GMT+0100'
    [](#cb23-5)    + ' (Central European Standard Time)');
    ```

### 2.4.2 `ToString()` and related operations

This is the JavaScript version of `ToString()`:

```
[](#cb24-1)function ToString(argument) {
[](#cb24-2)  if (argument === undefined) {
[](#cb24-3)    return 'undefined';
[](#cb24-4)  } else if (argument === null) {
[](#cb24-5)    return 'null';
[](#cb24-6)  } else if (argument === true) {
[](#cb24-7)    return 'true';
[](#cb24-8)  } else if (argument === false) {
[](#cb24-9)    return 'false';
[](#cb24-10)  } else if (TypeOf(argument) === 'number') {
[](#cb24-11)    return Number.toString(argument);
[](#cb24-12)  } else if (TypeOf(argument) === 'string') {
[](#cb24-13)    return argument;
[](#cb24-14)  } else if (TypeOf(argument) === 'symbol') {
[](#cb24-15)    throw new TypeError();
[](#cb24-16)  } else if (TypeOf(argument) === 'bigint') {
[](#cb24-17)    return BigInt.toString(argument);
[](#cb24-18)  } else {
[](#cb24-19)    // argument is an object
[](#cb24-20)    let primValue = ToPrimitive(argument, 'string'); // (A)
[](#cb24-21)    return ToString(primValue);
[](#cb24-22)  }
[](#cb24-23)}
```

Note how this function uses `ToPrimitive()` as an intermediate step for objects, before converting the primitive result to a string (line A).

`ToString()` deviates in an interesting way from how `String()` works: If `argument` is a symbol, the former throws a `TypeError` while the latter doesn’t. Why is that? The default for symbols is that converting them to strings throws exceptions:

```
> const sym = Symbol('sym');

> ''+sym
TypeError: Cannot convert a Symbol value to a string
> `${sym}`
TypeError: Cannot convert a Symbol value to a string
```

That default is overridden in `String()` and `Symbol.prototype.toString()` (both are described in the next subsections):

```
> String(sym)
'Symbol(sym)'
> sym.toString()
'Symbol(sym)'
```

#### 2.4.2.1 `String()`

```
[](#cb27-1)function String(value) {
[](#cb27-2)  let s;
[](#cb27-3)  if (value === undefined) {
[](#cb27-4)    s = '';
[](#cb27-5)  } else {
[](#cb27-6)    if (new.target === undefined && TypeOf(value) === 'symbol') {
[](#cb27-7)      // This function was function-called and value is a symbol
[](#cb27-8)      return SymbolDescriptiveString(value);
[](#cb27-9)    }
[](#cb27-10)    s = ToString(value);
[](#cb27-11)  }
[](#cb27-12)  if (new.target === undefined) {
[](#cb27-13)    // This function was function-called
[](#cb27-14)    return s;
[](#cb27-15)  }
[](#cb27-16)  // This function was new-called
[](#cb27-17)  return StringCreate(s, new.target.prototype); // simplified!
[](#cb27-18)}
```

`String()` works differently, depending on whether it is invoked via a function call or via `new`. It uses [`new.target`](https://exploringjs.com/es6/ch_classes.html#sec_allocating-and-initializing-instances) to distinguish the two.

These are the helper functions `StringCreate()` and `SymbolDescriptiveString()`:

```
[](#cb28-1)/** 
[](#cb28-2) * Creates a String instance that wraps `value`
[](#cb28-3) * and has the given protoype.
[](#cb28-4) */
[](#cb28-5)function StringCreate(value, prototype) {
[](#cb28-6)  // ···
[](#cb28-7)}
[](#cb28-8)
[](#cb28-9)function SymbolDescriptiveString(sym) {
[](#cb28-10)  assert.equal(TypeOf(sym), 'symbol');
[](#cb28-11)  let desc = sym.description;
[](#cb28-12)  if (desc === undefined) {
[](#cb28-13)    desc = '';
[](#cb28-14)  }
[](#cb28-15)  assert.equal(TypeOf(desc), 'string');
[](#cb28-16)  return 'Symbol('+desc+')';
[](#cb28-17)}
```

#### 2.4.2.2 `Symbol.prototype.toString()`

In addition to `String()`, we can also use method `.toString()` to convert a symbol to a string. Its specification looks as follows.

```
[](#cb29-1)Symbol.prototype.toString = function () {
[](#cb29-2)  let sym = thisSymbolValue(this);
[](#cb29-3)  return SymbolDescriptiveString(sym);
[](#cb29-4)};
[](#cb29-5)function thisSymbolValue(value) {
[](#cb29-6)  if (TypeOf(value) === 'symbol') {
[](#cb29-7)    return value;
[](#cb29-8)  }
[](#cb29-9)  if (TypeOf(value) === 'object' && '__SymbolData__' in value) {
[](#cb29-10)    let s = value.__SymbolData__;
[](#cb29-11)    assert.equal(TypeOf(s), 'symbol');
[](#cb29-12)    return s;
[](#cb29-13)  }
[](#cb29-14)}
```

#### 2.4.2.3 `Object.prototype.toString`

The default specification for `.toString()` looks as follows:

```
[](#cb30-1)Object.prototype.toString = function () {
[](#cb30-2)  if (this === undefined) {
[](#cb30-3)    return '[object Undefined]';
[](#cb30-4)  }
[](#cb30-5)  if (this === null) {
[](#cb30-6)    return '[object Null]';
[](#cb30-7)  }
[](#cb30-8)  let O = ToObject(this);
[](#cb30-9)  let isArray = Array.isArray(O);
[](#cb30-10)  let builtinTag;
[](#cb30-11)  if (isArray) {
[](#cb30-12)    builtinTag = 'Array';
[](#cb30-13)  } else if ('__ParameterMap__' in O) {
[](#cb30-14)    builtinTag = 'Arguments';
[](#cb30-15)  } else if ('__Call__' in O) {
[](#cb30-16)    builtinTag = 'Function';
[](#cb30-17)  } else if ('__ErrorData__' in O) {
[](#cb30-18)    builtinTag = 'Error';
[](#cb30-19)  } else if ('__BooleanData__' in O) {
[](#cb30-20)    builtinTag = 'Boolean';
[](#cb30-21)  } else if ('__NumberData__' in O) {
[](#cb30-22)    builtinTag = 'Number';
[](#cb30-23)  } else if ('__StringData__' in O) {
[](#cb30-24)    builtinTag = 'String';
[](#cb30-25)  } else if ('__DateValue__' in O) {
[](#cb30-26)    builtinTag = 'Date';
[](#cb30-27)  } else if ('__RegExpMatcher__' in O) {
[](#cb30-28)    builtinTag = 'RegExp';
[](#cb30-29)  } else {
[](#cb30-30)    builtinTag = 'Object';
[](#cb30-31)  }
[](#cb30-32)  let tag = O[Symbol.toStringTag];
[](#cb30-33)  if (TypeOf(tag) !== 'string') {
[](#cb30-34)    tag = builtinTag;
[](#cb30-35)  }
[](#cb30-36)  return '[object ' + tag + ']';
[](#cb30-37)};
```

This operation is used if we convert plain objects to strings:

```
> String({})
'[object Object]'
```

By default, it is also used if we convert instances of classes to strings:

```
[](#cb32-1)class MyClass {}
[](#cb32-2)assert.equal(
[](#cb32-3)  String(new MyClass()), '[object Object]');
```

Normally, we would override `.toString()` in order to configure the string representation of `MyClass`, but we can also change what comes after “`object`” inside the string with the square brackets:

```
[](#cb33-1)class MyClass {}
[](#cb33-2)MyClass.prototype[Symbol.toStringTag] = 'Custom!';
[](#cb33-3)assert.equal(
[](#cb33-4)  String(new MyClass()), '[object Custom!]');
```

It is interesting to compare the overriding versions of `.toString()` with the original version in `Object.prototype`:

```
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

`ToPropertyKey()` is used by, among others, the bracket operator. This is how it works:

```
[](#cb35-1)function ToPropertyKey(argument) {
[](#cb35-2)  let key = ToPrimitive(argument, 'string'); // (A)
[](#cb35-3)  if (TypeOf(key) === 'symbol') {
[](#cb35-4)    return key;
[](#cb35-5)  }
[](#cb35-6)  return ToString(key);
[](#cb35-7)}
```

Once again, objects are converted to primitives before working with primitives.

### 2.4.4 `ToNumeric()` and related operations

`ToNumeric()` is used by, among others, by the multiplication operator (`*`). This is how it works:

```
[](#cb36-1)function ToNumeric(value) {
[](#cb36-2)  let primValue = ToPrimitive(value, 'number');
[](#cb36-3)  if (TypeOf(primValue) === 'bigint') {
[](#cb36-4)    return primValue;
[](#cb36-5)  }
[](#cb36-6)  return ToNumber(primValue);
[](#cb36-7)}
```

#### 2.4.4.1 `ToNumber()`

`ToNumber()` works as follows:

```
[](#cb37-1)function ToNumber(argument) {
[](#cb37-2)  if (argument === undefined) {
[](#cb37-3)    return NaN;
[](#cb37-4)  } else if (argument === null) {
[](#cb37-5)    return +0;
[](#cb37-6)  } else if (argument === true) {
[](#cb37-7)    return 1;
[](#cb37-8)  } else if (argument === false) {
[](#cb37-9)    return +0;
[](#cb37-10)  } else if (TypeOf(argument) === 'number') {
[](#cb37-11)    return argument;
[](#cb37-12)  } else if (TypeOf(argument) === 'string') {
[](#cb37-13)    return parseTheString(argument); // not shown here
[](#cb37-14)  } else if (TypeOf(argument) === 'symbol') {
[](#cb37-15)    throw new TypeError();
[](#cb37-16)  } else if (TypeOf(argument) === 'bigint') {
[](#cb37-17)    throw new TypeError();
[](#cb37-18)  } else {
[](#cb37-19)    // argument is an object
[](#cb37-20)    let primValue = ToPrimitive(argument, 'number');
[](#cb37-21)    return ToNumber(primValue);
[](#cb37-22)  }
[](#cb37-23)}
```

The structure of `ToNumber()` is similar to the structure of `ToString()`.

## 2.5 Operations that coerce

### 2.5.1 Addition operator (`+`)

This is how JavaScript’s addition operator is specified:

```
[](#cb38-1)function Addition(leftHandSide, rightHandSide) {
[](#cb38-2)  let lprim = ToPrimitive(leftHandSide);
[](#cb38-3)  let rprim = ToPrimitive(rightHandSide);
[](#cb38-4)  if (TypeOf(lprim) === 'string' || TypeOf(rprim) === 'string') { // (A)
[](#cb38-5)    return ToString(lprim) + ToString(rprim);
[](#cb38-6)  }
[](#cb38-7)  let lnum = ToNumeric(lprim);
[](#cb38-8)  let rnum = ToNumeric(rprim);
[](#cb38-9)  if (TypeOf(lnum) !== TypeOf(rnum)) {
[](#cb38-10)    throw new TypeError();
[](#cb38-11)  }
[](#cb38-12)  let T = Type(lnum);
[](#cb38-13)  return T.add(lnum, rnum); // (B)
[](#cb38-14)}
```

Steps of this algorithm:

*   Both operands are converted to primitive values.
*   If one of the results is a string, both are converted to strings and concatenated (line A).
*   Otherwise, both operands are converted to numeric values and added (line B). `Type()` returns the ECMAScript specification type of `lnum`. `.add()` is a method of [numeric types](https://tc39.es/ecma262/#sec-numeric-types).

### 2.5.2 Abstract Equality Comparison (`==`)

```
[](#cb39-1)/** Loose equality (==) */
[](#cb39-2)function abstractEqualityComparison(x, y) {
[](#cb39-3)  if (TypeOf(x) === TypeOf(y)) {
[](#cb39-4)    // Use strict equality (===)
[](#cb39-5)    return strictEqualityComparison(x, y);
[](#cb39-6)  }
[](#cb39-7)
[](#cb39-8)  // Comparing null with undefined
[](#cb39-9)  if (x === null && y === undefined) {
[](#cb39-10)    return true;
[](#cb39-11)  }
[](#cb39-12)  if (x === undefined && y === null) {
[](#cb39-13)    return true;
[](#cb39-14)  }
[](#cb39-15)
[](#cb39-16)  // Comparing a number and a string
[](#cb39-17)  if (TypeOf(x) === 'number' && TypeOf(y) === 'string') {
[](#cb39-18)    return abstractEqualityComparison(x, Number(y));
[](#cb39-19)  }
[](#cb39-20)  if (TypeOf(x) === 'string' && TypeOf(y) === 'number') {
[](#cb39-21)    return abstractEqualityComparison(Number(x), y);
[](#cb39-22)  }
[](#cb39-23)
[](#cb39-24)  // Comparing a bigint and a string
[](#cb39-25)  if (TypeOf(x) === 'bigint' && TypeOf(y) === 'string') {
[](#cb39-26)    let n = StringToBigInt(y);
[](#cb39-27)    if (Number.isNaN(n)) {
[](#cb39-28)      return false;
[](#cb39-29)    }
[](#cb39-30)    return abstractEqualityComparison(x, n);
[](#cb39-31)  }
[](#cb39-32)  if (TypeOf(x) === 'string' && TypeOf(y) === 'bigint') {
[](#cb39-33)    return abstractEqualityComparison(y, x);
[](#cb39-34)  }
[](#cb39-35)
[](#cb39-36)  // Comparing a boolean with a non-boolean
[](#cb39-37)  if (TypeOf(x) === 'boolean') {
[](#cb39-38)    return abstractEqualityComparison(Number(x), y);
[](#cb39-39)  }
[](#cb39-40)  if (TypeOf(y) === 'boolean') {
[](#cb39-41)    return abstractEqualityComparison(x, Number(y));
[](#cb39-42)  }
[](#cb39-43)
[](#cb39-44)  // Comparing an object with a primitive
[](#cb39-45)  // (other than undefined, null, a boolean)
[](#cb39-46)  if (['string', 'number', 'bigint', 'symbol'].includes(TypeOf(x))
[](#cb39-47)    && TypeOf(y) === 'object') {
[](#cb39-48)      return abstractEqualityComparison(x, ToPrimitive(y));
[](#cb39-49)    }
[](#cb39-50)  if (TypeOf(x) === 'object'
[](#cb39-51)    && ['string', 'number', 'bigint', 'symbol'].includes(TypeOf(y))) {
[](#cb39-52)      return abstractEqualityComparison(ToPrimitive(x), y);
[](#cb39-53)    }
[](#cb39-54) 
[](#cb39-55)  // Comparing a bigint with a number
[](#cb39-56)  if ((TypeOf(x) === 'bigint' && TypeOf(y) === 'number')
[](#cb39-57)    || (TypeOf(x) === 'number' && TypeOf(y) === 'bigint')) {
[](#cb39-58)      if ([NaN, +Infinity, -Infinity].includes(x)
[](#cb39-59)        || [NaN, +Infinity, -Infinity].includes(y)) {
[](#cb39-60)          return false;
[](#cb39-61)        }
[](#cb39-62)      if (isSameMathematicalValue(x, y)) {
[](#cb39-63)        return true;
[](#cb39-64)      } else {
[](#cb39-65)        return false;
[](#cb39-66)      }
[](#cb39-67)    }
[](#cb39-68) 
[](#cb39-69)  return false;
[](#cb39-70)}
```

The following operations are not shown here:

*   [`strictEqualityComparison()`](https://tc39.es/ecma262/#sec-strict-equality-comparison)
*   [`StringToBigInt()`](https://tc39.es/ecma262/#sec-stringtobigint)
*   [`isSameMathematicalValue()`](https://tc39.es/ecma262/#mathematical-value)

## 2.6 Glossary: terms related to type conversion

Now that we have taken a closer look at how JavaScript’s type coercion works, let’s conclude with a brief glossary of terms related to type conversion:

*   In *type conversion*, we want the output value to have a given type. If the input value already has that type, it is simply returned unchanged. Otherwise, it is converted to a value that has the desired type.

*   *Explicit type conversion* means that the programmer uses an operation (a function, an operator, etc.) to trigger a type conversion. Explicit conversions can be:

    *   *Checked*: If a value can’t be converted, an exception is thrown.
    *   *Unchecked*: If a value can’t be converted, an error value is returned.
*   What *type casting* is, depends on the programming language. For example, in Java, it is explicit checked type conversion.

*   *Type coercion* is implicit type conversion: An operation automatically converts its arguments to the types it needs. Can be checked or unchecked or something in-between.

[Source: [Wikipedia](https://en.wikipedia.org/wiki/Type_conversion)]

# 3 The destructuring algorithm

* * *

*   3.1 [Preparing for the pattern matching algorithm](#ch004.xhtml_preparing-for-the-pattern-matching-algorithm)
    *   3.1.1 [Using declarative rules for specifying the matching algorithm](#ch004.xhtml_using-declarative-rules-for-specifying-the-matching-algorithm)
    *   3.1.2 [Evaluating expressions based on the declarative rules](#ch004.xhtml_evaluating-expressions-based-on-the-declarative-rules)
*   3.2 [The pattern matching algorithm](#ch004.xhtml_the-pattern-matching-algorithm)
    *   3.2.1 [Patterns](#ch004.xhtml_patterns)
    *   3.2.2 [Rules for variable](#ch004.xhtml_rules-for-variable)
    *   3.2.3 [Rules for object patterns](#ch004.xhtml_rules-for-object-patterns)
    *   3.2.4 [Rules for Array patterns](#ch004.xhtml_rules-for-array-patterns)
*   3.3 [Empty object patterns and Array patterns](#ch004.xhtml_empty-object-patterns-and-array-patterns)
*   3.4 [Applying the algorithm](#ch004.xhtml_applying-the-algorithm)
    *   3.4.1 [Background: passing parameters via matching](#ch004.xhtml_background-passing-parameters-via-matching)
    *   3.4.2 [Using `move2()`](#ch004.xhtml_using-move2)
    *   3.4.3 [Using `move1()`](#ch004.xhtml_using-move1)
    *   3.4.4 [Conclusion: Default values are a feature of pattern parts](#ch004.xhtml_conclusion-default-values-are-a-feature-of-pattern-parts)

* * *

In this chapter, we look at destructuring from a different angle: as a recursive pattern matching algorithm.

The algorithm will give us a better understanding of default values. That will be useful at the end, where we’ll try to figure out how the following two functions differ:

```
[](#cb40-1)function move({x=0, y=0} = {})         { ··· }
[](#cb40-2)function move({x, y} = { x: 0, y: 0 }) { ··· }
```

## 3.1 Preparing for the pattern matching algorithm

A destructuring assignment looks like this:

```
[](#cb41-1)«pattern» = «value»
```

We want to use `pattern` to extract data from `value`.

We will now look at an algorithm for performing this kind of assignment. This algorithm is known in functional programming as *pattern matching* (short: *matching*). It specifies the operator `←` (“match against”) that matches a `pattern` against a `value` and assigns to variables while doing so:

```
[](#cb42-1)«pattern» ← «value»
```

We will only explore destructuring assignment, but destructuring variable declarations and destructuring parameter definitions work similarly. We won’t go into advanced features, either: Computed property keys, property value shorthands, and object properties and array elements as assignment targets, are beyond the scope of this chapter.

The specification for the match operator consists of declarative rules that descend into the structures of both operands. The declarative notation may take some getting used to, but it makes the specification more concise.

### 3.1.1 Using declarative rules for specifying the matching algorithm

The declarative rules used in this chapter operate on input and produce the result of the algorithm via side effects. This is one such rule (which we’ll see again later):

*   (2c) `{key: «pattern», «properties»} ← obj`

    ```
    [](#cb43-1)«pattern» ← obj.key
    [](#cb43-2){«properties»} ← obj
    ```

This rule has the following parts:

*   (2c) is the *number* of the rule. The number is used to refer to the rule.
*   The *head* (first line) describes what the input must look like so that this rule can be applied.
*   The *body* (remaining lines) describes what happens if the rule is applied.

In rule (2c), the head means that this rule can be applied if there is an object pattern with at least one property (whose key is `key`) and zero or more remaining properties. The effect of this rule is that execution continues with the property value pattern being matched against `obj.key` and the remaining properties being matched against `obj`.

Let’s consider one more rule from this chapter:

*   (2e) `{} ← obj` (no properties left)

    ```
    [](#cb44-1)// We are finished
    ```

In rule (2e), the head means that this rule is executed if the empty object pattern `{}` is matched against a value `obj`. The body means that, in this case, we are done.

Together, rule (2c) and rule (2e) form a declarative loop that iterates over the properties of the pattern on the left-hand side of the arrow.

### 3.1.2 Evaluating expressions based on the declarative rules

The complete algorithm is specified via a sequence of declarative rules. Let’s assume we want to evaluate the following matching expression:

```
{first: f, last: l} ← obj
```

To apply a sequence of rules, we go over them from top to bottom and execute the first applicable rule. If there is a matching expression in the body of that rule, the rules are applied again. And so on.

Sometimes the head includes a condition that also determines if a rule is applicable – for example:

*   (3a) `[«elements»] ← non_iterable`
    `if (!isIterable(non_iterable))`

    ```
    [](#cb46-1)throw new TypeError();
    ```

## 3.2 The pattern matching algorithm

### 3.2.1 Patterns

A pattern is either:

*   A variable: `x`
*   An object pattern: `{«properties»}`
*   An Array pattern: `[«elements»]`

The next three sections specify rules for handling these three cases in matching expressions.

### 3.2.2 Rules for variable

*   1.  `x ← value` (including `undefined` and `null`)

    ```
    [](#cb47-1)x = value
    ```

### 3.2.3 Rules for object patterns

*   (2a) `{«properties»} ← undefined` (illegal value)

    ```
    [](#cb48-1)throw new TypeError();
    ```

*   (2b) `{«properties»} ← null` (illegal value)

    ```
    [](#cb49-1)throw new TypeError();
    ```

*   (2c) `{key: «pattern», «properties»} ← obj`

    ```
    [](#cb50-1)«pattern» ← obj.key
    [](#cb50-2){«properties»} ← obj
    ```

*   (2d) `{key: «pattern» = default_value, «properties»} ← obj`

    ```
    [](#cb51-1)const tmp = obj.key;
    [](#cb51-2)if (tmp !== undefined) {
    [](#cb51-3)  «pattern» ← tmp
    [](#cb51-4)} else {
    [](#cb51-5)  «pattern» ← default_value
    [](#cb51-6)}
    [](#cb51-7){«properties»} ← obj
    ```

*   (2e) `{} ← obj` (no properties left)

    ```
    [](#cb52-1)// We are finished
    ```

Rules 2a and 2b deal with illegal values. Rules 2c–2e loop over the properties of the pattern. In rule 2d, we can see that a default value provides an alternative to match against if there is no matching property in `obj`.

### 3.2.4 Rules for Array patterns

**Array pattern and iterable.** The algorithm for Array destructuring starts with an Array pattern and an iterable:

*   (3a) `[«elements»] ← non_iterable` (illegal value)
    `if (!isIterable(non_iterable))`

    ```
    [](#cb53-1)throw new TypeError();
    ```

*   (3b) `[«elements»] ← iterable`
    `if (isIterable(iterable))`

    ```
    [](#cb54-1)const iterator = iterable[Symbol.iterator]();
    [](#cb54-2)«elements» ← iterator
    ```

Helper function:

```
[](#cb55-1)function isIterable(value) {
[](#cb55-2)  return (value !== null
[](#cb55-3)    && typeof value === 'object'
[](#cb55-4)    && typeof value[Symbol.iterator] === 'function');
[](#cb55-5)}
```

**Array elements and iterator.** The algorithm continues with:

*   The elements of the pattern (left-hand side of the arrow)
*   The iterator that was obtained from the iterable (right-hand side of the arrow)

These are the rules:

*   (3c) `«pattern», «elements» ← iterator`

    ```
    [](#cb56-1)«pattern» ← getNext(iterator) // undefined after last item
    [](#cb56-2)«elements» ← iterator
    ```

*   (3d) `«pattern» = default_value, «elements» ← iterator`

    ```
    [](#cb57-1)const tmp = getNext(iterator);  // undefined after last item
    [](#cb57-2)if (tmp !== undefined) {
    [](#cb57-3)  «pattern» ← tmp
    [](#cb57-4)} else {
    [](#cb57-5)  «pattern» ← default_value
    [](#cb57-6)}
    [](#cb57-7)«elements» ← iterator
    ```

*   (3e) `, «elements» ← iterator` (hole, elision)

    ```
    [](#cb58-1)getNext(iterator); // skip
    [](#cb58-2)«elements» ← iterator
    ```

*   (3f) `...«pattern» ← iterator` (always last part!)

    ```
    [](#cb59-1)const tmp = [];
    [](#cb59-2)for (const elem of iterator) {
    [](#cb59-3)  tmp.push(elem);
    [](#cb59-4)}
    [](#cb59-5)«pattern» ← tmp
    ```

*   (3g) `← iterator` (no elements left)

    ```
    [](#cb60-1)// We are finished
    ```

Helper function:

```
[](#cb61-1)function getNext(iterator) {
[](#cb61-2)  const {done,value} = iterator.next();
[](#cb61-3)  return (done ? undefined : value);
[](#cb61-4)}
```

An iterator being finished is similar to missing properties in objects.

## 3.3 Empty object patterns and Array patterns

Interesting consequence of the algorithm’s rules: We can destructure with empty object patterns and empty Array patterns.

Given an empty object pattern `{}`: If the value to be destructured is neither `undefined` nor `null`, then nothing happens. Otherwise, a `TypeError` is thrown.

```
[](#cb62-1)const {} = 123; // OK, neither undefined nor null
[](#cb62-2)assert.throws(
[](#cb62-3)  () => {
[](#cb62-4)    const {} = null;
[](#cb62-5)  },
[](#cb62-6)  /^TypeError: Cannot destructure 'null' as it is null.$/)
```

Given an empty Array pattern `[]`: If the value to be destructured is iterable, then nothing happens. Otherwise, a `TypeError` is thrown.

```
[](#cb63-1)const [] = 'abc'; // OK, iterable
[](#cb63-2)assert.throws(
[](#cb63-3)  () => {
[](#cb63-4)    const [] = 123; // not iterable
[](#cb63-5)  },
[](#cb63-6)  /^TypeError: 123 is not iterable$/)
```

In other words: Empty destructuring patterns force values to have certain characteristics, but have no other effects.

## 3.4 Applying the algorithm

In JavaScript, named parameters are simulated via objects: The caller uses an object literal and the callee uses destructuring. This simulation is explained in detail in [“JavaScript for impatient programmers”](https://exploringjs.com/impatient-js/ch_callables.html#named-parameters). The following code shows an example: function `move1()` has two named parameters, `x` and `y`:

```
[](#cb64-1)function move1({x=0, y=0} = {}) { // (A)
[](#cb64-2)  return [x, y];
[](#cb64-3)}
[](#cb64-4)assert.deepEqual(
[](#cb64-5)  move1({x: 3, y: 8}), [3, 8]);
[](#cb64-6)assert.deepEqual(
[](#cb64-7)  move1({x: 3}), [3, 0]);
[](#cb64-8)assert.deepEqual(
[](#cb64-9)  move1({}), [0, 0]);
[](#cb64-10)assert.deepEqual(
[](#cb64-11)  move1(), [0, 0]);
```

There are three default values in line A:

*   The first two default values allow us to omit `x` and `y`.
*   The third default value allows us to call `move1()` without parameters (as in the last line).

But why would we define the parameters as in the previous code snippet? Why not as follows?

```
[](#cb65-1)function move2({x, y} = { x: 0, y: 0 }) {
[](#cb65-2)  return [x, y];
[](#cb65-3)}
```

To see why `move1()` is correct, we are going to use both functions in two examples. Before we do that, let’s see how the passing of parameters can be explained via matching.

### 3.4.1 Background: passing parameters via matching

For function calls, *formal parameters* (inside function definitions) are matched against *actual parameters* (inside function calls). As an example, take the following function definition and the following function call.

```
[](#cb66-1)function func(a=0, b=0) { ··· }
[](#cb66-2)func(1, 2);
```

The parameters `a` and `b` are set up similarly to the following destructuring.

```
[](#cb67-1)[a=0, b=0] ← [1, 2]
```

### 3.4.2 Using `move2()`

Let’s examine how destructuring works for `move2()`.

**Example 1.** The function call `move2()` leads to this destructuring:

```
[](#cb68-1)[{x, y} = { x: 0, y: 0 }] ← []
```

The single Array element on the left-hand side does not have a match on the right-hand side, which is why `{x,y}` is matched against the default value and not against data from the right-hand side (rules 3b, 3d):

```
[](#cb69-1){x, y} ← { x: 0, y: 0 }
```

The left-hand side contains *property value shorthands*. It is an abbreviation for:

```
[](#cb70-1){x: x, y: y} ← { x: 0, y: 0 }
```

This destructuring leads to the following two assignments (rules 2c, 1):

```
[](#cb71-1)x = 0;
[](#cb71-2)y = 0;
```

This is what we wanted. However, in the next example, we are not as lucky.

**Example 2.** Let’s examine the function call `move2({z: 3})` which leads to the following destructuring:

```
[](#cb72-1)[{x, y} = { x: 0, y: 0 }] ← [{z: 3}]
```

There is an Array element at index 0 on the right-hand side. Therefore, the default value is ignored and the next step is (rule 3d):

```
[](#cb73-1){x, y} ← { z: 3 }
```

That leads to both `x` and `y` being set to `undefined`, which is not what we want. The problem is that `{x,y}` is not matched against the default value, anymore, but against `{z:3}`.

### 3.4.3 Using `move1()`

Let’s try `move1()`.

**Example 1:** `move1()`

```
[](#cb74-1)[{x=0, y=0} = {}] ← []
```

We don’t have an Array element at index 0 on the right-hand side and use the default value (rule 3d):

```
[](#cb75-1){x=0, y=0} ← {}
```

The left-hand side contains property value shorthands, which means that this destructuring is equivalent to:

```
[](#cb76-1){x: x=0, y: y=0} ← {}
```

Neither property `x` nor property `y` have a match on the right-hand side. Therefore, the default values are used and the following destructurings are performed next (rule 2d):

```
[](#cb77-1)x ← 0
[](#cb77-2)y ← 0
```

That leads to the following assignments (rule 1):

```
[](#cb78-1)x = 0
[](#cb78-2)y = 0
```

Here, we get what we want. Let’s see if our luck holds with the next example.

**Example 2:** `move1({z: 3})`

```
[](#cb79-1)[{x=0, y=0} = {}] ← [{z: 3}]
```

The first element of the Array pattern has a match on the right-hand side and that match is used to continue destructuring (rule 3d):

```
[](#cb80-1){x=0, y=0} ← {z: 3}
```

Like in example 1, there are no properties `x` and `y` on the right-hand side and the default values are used:

```
[](#cb81-1)x = 0
[](#cb81-2)y = 0
```

It works as desired! This time, the pattern with `x` and `y` being matched against `{z:3}` is not a problem, because they have their own local default values.

### 3.4.4 Conclusion: Default values are a feature of pattern parts

The examples demonstrate that default values are a feature of pattern parts (object properties or Array elements). If a part has no match or is matched against `undefined` then the default value is used. That is, the pattern is matched against the default value, instead.

# 4 A detailed look at global variables

* * *

*   4.1 [Scopes](#ch005.xhtml_scopes)
*   4.2 [Lexical environments](#ch005.xhtml_lexical-environments)
*   4.3 [The global object](#ch005.xhtml_the-global-object)
*   4.4 [In browsers, `globalThis` does not point directly to the global object](#ch005.xhtml_window-proxy)
*   4.5 [The global environment](#ch005.xhtml_the-global-environment)
    *   4.5.1 [Script scope and module scopes](#ch005.xhtml_script-scope-and-module-scopes)
    *   4.5.2 [Creating variables: declarative record vs. object record](#ch005.xhtml_creating-variables-declarative-record-vs.-object-record)
    *   4.5.3 [Getting or setting variables](#ch005.xhtml_getting-or-setting-variables)
    *   4.5.4 [Global ECMAScript variables and global host variables](#ch005.xhtml_global-ecmascript-variables-and-global-host-variables)
*   4.6 [Conclusion: Why does JavaScript have both normal global variables and the global object?](#ch005.xhtml_conclusion-why-does-javascript-have-both-normal-global-variables-and-the-global-object)
*   4.7 [Further reading and sources of this chapter](#ch005.xhtml_further-reading-and-sources-of-this-chapter)

* * *

In this chapter, we take a detailed look at how JavaScript’s global variables work. Several interesting phenomena play a role: the scope of scripts, the so-called *global object*, and more.

## 4.1 Scopes

The *lexical scope* (short: *scope*) of a variable is the region of a program where it can be accessed. JavaScript’s scopes are *static* (they don’t change at runtime) and they can be nested – for example:

```
[](#cb82-1)function func() { // (A)
[](#cb82-2)  const aVariable = 1;
[](#cb82-3)  if (true) { // (B)
[](#cb82-4)    const anotherVariable = 2;
[](#cb82-5)  }
[](#cb82-6)}
```

The scope introduced by the `if` statement (line B) is nested inside the scope of function `func()` (line A).

The innermost surrounding scope of a scope S is called the *outer scope* of S. In the example, `func` is the outer scope of `if`.

## 4.2 Lexical environments

In the JavaScript language specification, scopes are “implemented” via *lexical environments*. They consist of two components:

*   An *environment record* that maps variable names to variable values (think dictionary). This is the actual storage space for the variables of the scope. The name-value entries in the record are called *bindings*.

*   A reference to the *outer environment* – the environment for the outer scope.

The tree of nested scopes is therefore represented by a tree of environments linked by outer environment references.

## 4.3 The global object

The global object is an object whose properties become global variables. (We’ll examine soon how exactly it fits into the tree of environments.) It can be accessed via the following global variables:

*   Available on all platforms: [`globalThis`](https://exploringjs.com/impatient-js/ch_variables-assignment.html#globalThis). The name is based on the fact that it has the same value as `this` in global scope.
*   Other variables for the global object are not available on all platforms:
    *   `window` is the classic way of referring to the global object. It works in normal browser code, but not in *Web Workers* (processes running concurrently to the normal browser process) and not on Node.js.
    *   `self` is available everywhere in browsers (including in Web Workers). But it isn’t supported by Node.js.
    *   `global` is only available on Node.js.

## 4.4 In browsers, `globalThis` does not point directly to the global object

In browsers, `globalThis` does not point directly to the global, there is an indirection. As an example, consider an iframe on a web page:

*   Whenever the `src` of the iframe changes, it gets a new global object.
*   However, `globalThis` always has the same value. That value can be checked from outside the iframe, as demonstrated below (inspired by [an example in the `globalThis` proposal](https://github.com/tc39/proposal-global#html-and-the-windowproxy)).

File `parent.html`:

```
[](#cb83-1)<iframe src="iframe.html?first"></iframe>
[](#cb83-2)<script>
[](#cb83-3)  const iframe = document.querySelector('iframe');
[](#cb83-4)  const icw = iframe.contentWindow; // `globalThis` of iframe
[](#cb83-5)
[](#cb83-6)  iframe.onload = () => {
[](#cb83-7)    // Access properties of global object of iframe
[](#cb83-8)    const firstGlobalThis = icw.globalThis;
[](#cb83-9)    const firstArray = icw.Array;
[](#cb83-10)    console.log(icw.iframeName); // 'first'
[](#cb83-11)
[](#cb83-12)    iframe.onload = () => {
[](#cb83-13)      const secondGlobalThis = icw.globalThis;
[](#cb83-14)      const secondArray = icw.Array;
[](#cb83-15)
[](#cb83-16)      // The global object is different
[](#cb83-17)      console.log(icw.iframeName); // 'second'
[](#cb83-18)      console.log(secondArray === firstArray); // false
[](#cb83-19)
[](#cb83-20)      // But globalThis is still the same
[](#cb83-21)      console.log(firstGlobalThis === secondGlobalThis); // true
[](#cb83-22)    };
[](#cb83-23)    iframe.src = 'iframe.html?second';
[](#cb83-24)  };
[](#cb83-25)</script>
```

File `iframe.html`:

```
[](#cb84-1)<script>
[](#cb84-2)  globalThis.iframeName = location.search.slice(1);
[](#cb84-3)</script>
```

How do browsers ensure that `globalThis` doesn’t change in this scenario? They internally distinguish two objects:

*   [`Window`](https://html.spec.whatwg.org/multipage/window-object.html#the-window-object) is the global object. It changes whenever the location changes.
*   [`WindowProxy`](https://html.spec.whatwg.org/multipage/window-object.html#the-windowproxy-exotic-object) is an object that forwards all accesses to the current `Window`. This object never changes.

In browsers, `globalThis` refers to the `WindowProxy`; everywhere else, it directly refers to the global object.

## 4.5 The global environment

The global scope is the “outermost” scope – it has no outer scope. Its environment is the *global environment*. Every environment is connected with the global environment via a chain of environments that are linked by outer environment references. The outer environment reference of the global environment is `null`.

The global environment record uses two environment records to manage its variables:

*   An *object environment record* has the same interface as a normal environment record, but keeps its bindings in a JavaScript object. In this case, the object is the global object.

*   A normal (*declarative*) environment record that has its own storage for its bindings.

Which of these two records is used when will be explained soon.

### 4.5.1 Script scope and module scopes

In JavaScript, we are only in global scope at the top levels of scripts. In contrast, each module has its own scope that is a subscope of the script scope.

If we ignore the relatively complicated rules for how variable bindings are added to the global environment, then global scope and module scopes work as if they were nested code blocks:

```
[](#cb85-1){ // Global scope (scope of *all* scripts)
[](#cb85-2)
[](#cb85-3)  // (Global variables)
[](#cb85-4)
[](#cb85-5)  { // Scope of module 1
[](#cb85-6)    ···
[](#cb85-7)  }
[](#cb85-8)  { // Scope of module 2
[](#cb85-9)    ···
[](#cb85-10)  }
[](#cb85-11)  // (More module scopes)
[](#cb85-12)}
```

### 4.5.2 Creating variables: declarative record vs. object record

In order to create a variable that is truly global, we must be in global scope – which is only the case at the top level of scripts:

*   Top-level `const`, `let`, and `class` create bindings in the declarative environment record.
*   Top-level `var` and function declarations create bindings in the object environment record.

```
[](#cb86-1)<script>
[](#cb86-2)  const one = 1;
[](#cb86-3)  var two = 2;
[](#cb86-4)</script>
[](#cb86-5)<script>
[](#cb86-6)  // All scripts share the same top-level scope:
[](#cb86-7)  console.log(one); // 1
[](#cb86-8)  console.log(two); // 2
[](#cb86-9) 
[](#cb86-10)  // Not all declarations create properties of the global object:
[](#cb86-11)  console.log(globalThis.one); // undefined
[](#cb86-12)  console.log(globalThis.two); // 2
[](#cb86-13)</script>
```

### 4.5.3 Getting or setting variables

When we get or set a variable and both environment records have a binding for that variable, then the declarative record wins:

```
[](#cb87-1)<script>
[](#cb87-2)  let myGlobalVariable = 1; // declarative environment record
[](#cb87-3)  globalThis.myGlobalVariable = 2; // object environment record
[](#cb87-4)
[](#cb87-5)  console.log(myGlobalVariable); // 1 (declarative record wins)
[](#cb87-6)  console.log(globalThis.myGlobalVariable); // 2
[](#cb87-7)</script>
```

### 4.5.4 Global ECMAScript variables and global host variables

In addition to variables created via `var` and function declarations, the global object contains the following properties:

*   All built-in global variables of ECMAScript
*   All built-in global variables of the host platform (browser, Node.js, etc.)

Using `const` or `let` guarantees that global variable declarations aren’t influencing (or influenced by) the built-in global variables of ECMAScript and host platform.

For example, browsers have [the global variable `.location`](https://developer.mozilla.org/en-US/docs/Web/API/Window/location):

```
[](#cb88-1)// Changes the location of the current document:
[](#cb88-2)var location = 'https://example.com';
[](#cb88-3)
[](#cb88-4)// Shadows window.location, doesn’t change it:
[](#cb88-5)let location = 'https://example.com';
```

If a variable already exists (such as `location` in this case), then a `var` declaration with an initializer behaves like an assignment. That’s why we get into trouble in this example.

Note that this is only an issue in global scope. In modules, we are never in global scope (unless we use `eval()` or similar).

Fig. [1](#ch005.xhtml_fig:global-scope) summarizes everything we have learned in this section.

![](media/file8.svg)

Figure 1: The environment for the global scope manages its bindings via a *global environment record* which in turn is based on two environment records: an *object environment record* whose bindings are stored in the global object and a *declarative environment record* that uses internal storage for its bindings. Therefore, global variables can be created by adding properties to the global object or via various declarations. The global object is initialized with the built-in global variables of ECMAScript and the host platform. Each ECMAScript module has its own environment whose outer environment is the global environment.

## 4.6 Conclusion: Why does JavaScript have both normal global variables and the global object?

The global object is generally considered to be a mistake. For that reason, newer constructs such as `const`, `let`, and classes create normal global variables (when in script scope).

Thankfully, most of the code written in modern JavaScript, lives in [ECMAScript modules and CommonJS modules](https://exploringjs.com/impatient-js/ch_modules.html). Each module has its own scope, which is why the rules governing global variables rarely matter for module-based code.

## 4.7 Further reading and sources of this chapter

Environments and the global object in the ECMAScript specification:

*   [Section “Lexical Environments”](https://tc39.es/ecma262/#sec-lexical-environments) provides a general overview over environments.
*   [Section “Global Environment Records”](https://tc39.es/ecma262/#sec-global-environment-records) covers the global environment.
*   [Section “ECMAScript Standard Built-in Objects”](https://tc39.es/ecma262/#sec-ecmascript-standard-built-in-objects) describes how ECMAScript manages its built-in objects (which include the global object).

`globalThis`:

*   2ality post [“ES feature: `globalThis`”](https://2ality.com/2019/08/global-this.html)
*   Various ways of accessing the global `this` value: [“A horrifying `globalThis` polyfill in universal JavaScript”](https://mathiasbynens.be/notes/globalthis) by Mathias Bynens

The global object in browsers:

*   Background on what happens in browsers: [“Defining the WindowProxy, Window, and Location objects”](https://blog.whatwg.org/windowproxy-window-and-location) by Anne van Kesteren
*   Very technical: [section “Realms, settings objects, and global objects”](https://html.spec.whatwg.org/multipage/webappapis.html#realms-settings-objects-global-objects) in the WHATWG HTML standard
*   In the ECMAScript specification, we can see how web browsers customize global `this`: [section “InitializeHostDefinedRealm()”](https://tc39.es/ecma262/#sec-initializehostdefinedrealm)

# 5 `%` is a remainder operator, not a modulo operator

* * *

*   5.1 [Remainder operator `rem` vs. modulo operator `mod`](#ch006.xhtml_remainder-operator-rem-vs.-modulo-operator-mod)
*   5.2 [An intuitive understanding of the remainder operation](#ch006.xhtml_an-intuitive-understanding-of-the-remainder-operation)
*   5.3 [An intuitive understanding of the modulo operation](#ch006.xhtml_an-intuitive-understanding-of-the-modulo-operation)
*   5.4 [Similarities and differences between `rem` and `mod`](#ch006.xhtml_similarities-and-differences-between-rem-and-mod)
*   5.5 [The equations behind remainder and modulo](#ch006.xhtml_the-equations-behind-remainder-and-modulo)
    *   5.5.1 [`rem` and `mod` perform integer division differently](#ch006.xhtml_rem-and-mod-perform-integer-division-differently)
    *   5.5.2 [Implementing `rem`](#ch006.xhtml_implementing-rem)
    *   5.5.3 [Implementing `mod`](#ch006.xhtml_implementing-mod)
*   5.6 [Where are `rem` and `mod` used in programming languages?](#ch006.xhtml_where-are-rem-and-mod-used-in-programming-languages)
    *   5.6.1 [JavaScript’s `%` operator computes the remainder](#ch006.xhtml_javascripts-operator-computes-the-remainder)
    *   5.6.2 [Python’s `%` operator computes the modulus](#ch006.xhtml_pythons-operator-computes-the-modulus)
    *   5.6.3 [Uses of the modulo operation in JavaScript](#ch006.xhtml_uses-of-the-modulo-operation-in-javascript)
*   5.7 [Further reading and sources of this chapter](#ch006.xhtml_further-reading-and-sources-of-this-chapter-1)

* * *

*Remainder* and *modulo* are two similar operations. This chapter explores how they work and reveals that JavaScript’s `%` operator computes the remainder, not the modulus.

## 5.1 Remainder operator `rem` vs. modulo operator `mod`

In this chapter, we pretend that JavaScript has the following two operators:

*   The *remainder operator* `rem`
*   The *modulo operator* `mod`

That will help us examine how the underlying operations work.

## 5.2 An intuitive understanding of the remainder operation

The operands of the remainder operator are called *dividend* and *divisor*:

```
remainder = dividend rem divisor
```

How is the result computed? Consider the following expression:

```
[](#cb90-1)7 rem 3
```

We remove 3 from the dividend until we are left with a value that is smaller than 3:

```
[](#cb91-1)7 rem 3 = 4 rem 3 = 1 rem 3 = 1
```

What do we do if the dividend is negative?

```
[](#cb92-1)-7 rem 3
```

This time, we add 3 to the dividend until we have a value that is smaller than -3:

```
[](#cb93-1)-7 rem 3 = -4 rem 3 = -1 rem 3 = -1
```

It is insightful to map out the results for a fixed divisor:

```
x:       -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
x rem 3: -1  0 -2 -1  0 -2 -1  0  1  2  0  1  2  0  1
```

Among the results, we can see a symmetry: `x` and `-x` produce the same results, but with opposite signs.

## 5.3 An intuitive understanding of the modulo operation

Once again, the operands are called *dividend* and *divisor* (hinting at how similar `rem` and `mod` are):

```
modulus = dividend mod divisor
```

Consider the following example:

```
[](#cb96-1)x mod 3
```

This operation maps `x` into the range:

```
[0,3) = {0,1,2}
```

That is, zero is included (opening square bracket), 3 is excluded (closing parenthesis).

How does `mod` perform this mapping? It is easy if `x` is already inside the range:

```
> 0 mod 3
0
> 2 mod 3
2
```

If `x` is greater than or equal to the upper boundary of the range, then the upper boundary is subtracted from `x` until it fits into the range:

```
> 4 mod 3
1
> 7 mod 3
1
```

That means we are getting the following mapping for non-negative integers:

```
x:       0 1 2 3 4 5 6 7
x mod 3: 0 1 2 0 1 2 0 1
```

This mapping is extended as follows, so that it includes negative integers:

```
x:       -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
x mod 3:  2  0  1  2  0  1  2  0  1  2  0  1  2  0  1
```

Note how the range [0,3) is repeated over and over again.

## 5.4 Similarities and differences between `rem` and `mod`

`rem` and `mod` are quite similar – they only differ if dividend and divisor have different signs:

*   With `rem`, the result has the same sign as the dividend (first operand):

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

*   With `mod`, the result has the same sign as the divisor (second operand):

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

## 5.5 The equations behind remainder and modulo

The following two equations define both remainder and modulo:

```
dividend = (divisor * quotient) + remainder
|remainder| < |divisor|
```

Given a dividend and a divisor, how do we compute remainder and modulus?

```
remainder = dividend - (divisor * quotient)
quotient = dividend div divisor
```

The `div` operator performs integer division.

### 5.5.1 `rem` and `mod` perform integer division differently

How can these equations contain the solution for *both* operations? If variable `remainder` isn’t zero, the equations always allow two values for it: one positive, the other one negative. To see why, we turn to the question we are asking when determining the quotient:

> How often do we need to multiply the divisor to get as close to the dividend as possible?

For example, that gives us two different results for dividend −2 and divisor 3:

*   `-2 rem 3 = -2`
    3 × 0 gets us close to −2\. The difference between 0 and the dividend −2 is −2.

*   `-2 mod 3 = 1`
    3 × −1 also gets us close to −2\. The difference between −3 and the dividend −2 is 1.

It also gives us two different results for dividend 2 and divisor −3:

*   `2 rem -3 = 2`
    -3 × 0 gets us close to 2.

*   `2 mod -3 = -1`
    -3 × -1 gets us close to 2.

The results differ depending on how the integer division `div` is implemented.

### 5.5.2 Implementing `rem`

The following JavaScript function implements the `rem` operator. It performs integer division by performing floating point division and rounding the result to an integer via `Math.trunc()`:

```
[](#cb106-1)function rem(dividend, divisor) {
[](#cb106-2)  const quotient = Math.trunc(dividend / divisor);
[](#cb106-3)  return dividend - (divisor * quotient);
[](#cb106-4)}
```

### 5.5.3 Implementing `mod`

The following function implements the `mod` operator. This time, integer division is based on `Math.floor()`:

```
[](#cb107-1)function mod(dividend, divisor) {
[](#cb107-2)  const quotient = Math.floor(dividend / divisor);
[](#cb107-3)  return dividend - (divisor * quotient);
[](#cb107-4)}
```

Note that other ways of doing integer division are possible (e.g. based on `Math.ceil()` or `Math.round()`). That means that there are more operations that are similar to `rem` and `mod`.

## 5.6 Where are `rem` and `mod` used in programming languages?

### 5.6.1 JavaScript’s `%` operator computes the remainder

For example (Node.js REPL):

```
> 7 % 6
1
> -7 % 6
-1
```

### 5.6.2 Python’s `%` operator computes the modulus

For example (Python REPL):

```
>>> 7 % 6
1
>>> -7 % 6
5
```

### 5.6.3 Uses of the modulo operation in JavaScript

The ECMAScript specification uses modulo several times – for example:

*   To convert the operands of [the `>>>` operator](https://tc39.es/ecma262/#sec-unsigned-right-shift-operator) to unsigned 32-bit integers (`x mod 2**32`):

    ```
    > 2**32 >>> 0
    0
    > (2**32)+1 >>> 0
    1
    > (-1 >>> 0) === (2**32)-1
    true
    ```

*   To convert arbitrary numbers so that they fit into Typed Arrays. For example, `x mod 2**8` is used to convert numbers to unsigned 8-bit integers (after first converting them to integers):

    ```
    [](#cb111-1)const tarr = new Uint8Array(1);
    [](#cb111-2)
    [](#cb111-3)tarr[0] = 256;
    [](#cb111-4)assert.equal(tarr[0], 0);
    [](#cb111-5)
    [](#cb111-6)tarr[0] = 257;
    [](#cb111-7)assert.equal(tarr[0], 1);
    ```

## 5.7 Further reading and sources of this chapter

*   [The Wikipedia page on “modulo operation”](https://en.wikipedia.org/wiki/Modulo_operation) has much information.
*   The ECMAScript specification [mentions](https://tc39.es/ecma262/#sec-applying-the-mod-operator) that `%` is computed via “truncating division”.
*   [Sect. “Rounding”](https://exploringjs.com/impatient-js/ch_math.html#math-rounding) in “JavaScript for impatient programmers” describes several ways of rounding in JavaScript.

# 6 Copying objects and Arrays

* * *

*   6.1 [Shallow copying vs. deep copying](#ch007.xhtml_shallow-copying-vs.-deep-copying)
*   6.2 [Shallow copying in JavaScript](#ch007.xhtml_shallow-copying-in-javascript)
    *   6.2.1 [Copying plain objects and Arrays via spreading](#ch007.xhtml_copying-plain-objects-and-arrays-via-spreading)
    *   6.2.2 [Shallow copying via `Object.assign()` (optional)](#ch007.xhtml_shallow-copying-via-object.assign-optional)
    *   6.2.3 [Shallow copying via `Object.getOwnPropertyDescriptors()` and `Object.defineProperties()` (optional)](#ch007.xhtml_copying-via-property-descriptors)
*   6.3 [Deep copying in JavaScript](#ch007.xhtml_deep-copying-in-javascript)
    *   6.3.1 [Manual deep copying via nested spreading](#ch007.xhtml_manual-deep-copying-via-nested-spreading)
    *   6.3.2 [Hack: generic deep copying via JSON](#ch007.xhtml_hack-generic-deep-copying-via-json)
    *   6.3.3 [Implementing generic deep copying](#ch007.xhtml_implementing-generic-deep-copying)
*   6.4 [Further reading](#ch007.xhtml_further-reading)

* * *

In this chapter, we will learn how to copy objects and Arrays in JavaScript.

## 6.1 Shallow copying vs. deep copying

There are two “depths” with which data can be copied:

*   *Shallow copying* only copies the top-level entries of objects and Arrays. The entry values are still the same in original and copy.
*   *Deep copying* also copies the entries of the values of the entries, etc. That is, it traverses the complete tree whose root is the value to be copied and makes copies of all nodes.

The next sections cover both kinds of copying. Unfortunately, JavaScript only has built-in support for shallow copying. If we need deep copying, we need to implement it ourselves.

## 6.2 Shallow copying in JavaScript

Let’s look at several ways of shallowly copying data.

### 6.2.1 Copying plain objects and Arrays via spreading

We can spread [into object literals](https://exploringjs.com/impatient-js/ch_single-objects.html#spreading-into-object-literals) and [into Array literals](https://exploringjs.com/impatient-js/ch_arrays.html#spreading-into-array-literals) to make copies:

```
[](#cb112-1)const copyOfObject = {...originalObject};
[](#cb112-2)const copyOfArray = [...originalArray];
```

Alas, spreading has several issues. Those will be covered in the next subsections. Among those, some are real limitations, others mere pecularities.

#### 6.2.1.1 The prototype is not copied

For example:

```
[](#cb113-1)class MyClass {}
[](#cb113-2)
[](#cb113-3)const original = new MyClass();
[](#cb113-4)assert.equal(original instanceof MyClass, true);
[](#cb113-5)
[](#cb113-6)const copy = {...original};
[](#cb113-7)assert.equal(copy instanceof MyClass, false);
```

Note that the following two expressions are equivalent:

```
[](#cb114-1)obj instanceof SomeClass
[](#cb114-2)SomeClass.prototype.isPrototypeOf(obj)
```

Therefore, we can fix this by giving the copy the same prototype as the original:

```
[](#cb115-1)class MyClass {}
[](#cb115-2)
[](#cb115-3)const original = new MyClass();
[](#cb115-4)
[](#cb115-5)const copy = {
[](#cb115-6)  __proto__: Object.getPrototypeOf(original),
[](#cb115-7)  ...original,
[](#cb115-8)};
[](#cb115-9)assert.equal(copy instanceof MyClass, true);
```

Alternatively, we can set the prototype of the copy after its creation, via `Object.setPrototypeOf()`.

#### 6.2.1.2 Many built-in objects have special “internal slots” that aren’t copied

Examples of such built-in objects include regular expressions and dates. If we make a copy of them, we lose most of the data stored in them.

#### 6.2.1.3 Only own (non-inherited) properties are copied

Given how [prototype chains](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains) work, this is usually the right approach. But we still need to be aware of it. In the following example, the inherited property `.inheritedProp` of `original` is not available in `copy` because we only copy own properties and don’t keep the prototype.

```
[](#cb116-1)const proto = { inheritedProp: 'a' };
[](#cb116-2)const original = {__proto__: proto, ownProp: 'b' };
[](#cb116-3)assert.equal(original.inheritedProp, 'a');
[](#cb116-4)assert.equal(original.ownProp, 'b');
[](#cb116-5)
[](#cb116-6)const copy = {...original};
[](#cb116-7)assert.equal(copy.inheritedProp, undefined);
[](#cb116-8)assert.equal(copy.ownProp, 'b');
```

#### 6.2.1.4 Only enumerable properties are copied

For example, the own property `.length` of Array instances is not enumerable and not copied:

```
[](#cb117-1)const arr = ['a', 'b'];
[](#cb117-2)assert.equal(arr.length, 2);
[](#cb117-3)assert.equal({}.hasOwnProperty.call(arr, 'length'), true);
[](#cb117-4)
[](#cb117-5)const copy = {...arr};
[](#cb117-6)assert.equal({}.hasOwnProperty.call(copy, 'length'), false);
```

This is also rarely a limitation because most properties are enumerable. If we need to copy non-enumerable properties, we can use `Object.getOwnPropertyDescriptors()` and `Object.defineProperties()` to copy objects ([how to do that is explained later](#ch007.xhtml_copying-via-property-descriptors)):

*   They consider all attributes (not just `value`) and therefore correctly copy getters, setters, read-only properties, etc.
*   `Object.getOwnPropertyDescriptors()` retrieves both enumerable and non-enumerable properties.

For more information on enumerability, see [§12 “Enumerability of properties”](#ch013.xhtml_ch_enumerability).

#### 6.2.1.5 Property attributes aren’t always copied faithfully

Independently of [the *attributes* of a property](#ch010.xhtml_ch_property-attributes-intro), its copy will always be a data property that is writable and configurable.

For example, here we create the property `original.prop` whose attributes `writable` and `configurable` are `false`:

```
[](#cb118-1)const original = Object.defineProperties(
[](#cb118-2)  {}, {
[](#cb118-3)    prop: {
[](#cb118-4)      value: 1,
[](#cb118-5)      writable: false,
[](#cb118-6)      configurable: false,
[](#cb118-7)      enumerable: true,
[](#cb118-8)    },
[](#cb118-9)  });
[](#cb118-10)assert.deepEqual(original, {prop: 1});
```

If we copy `.prop`, then `writable` and `configurable` are both `true`:

```
[](#cb119-1)const copy = {...original};
[](#cb119-2)// Attributes `writable` and `configurable` of copy are different:
[](#cb119-3)assert.deepEqual(
[](#cb119-4)  Object.getOwnPropertyDescriptors(copy),
[](#cb119-5)  {
[](#cb119-6)    prop: {
[](#cb119-7)      value: 1,
[](#cb119-8)      writable: true,
[](#cb119-9)      configurable: true,
[](#cb119-10)      enumerable: true,
[](#cb119-11)    },
[](#cb119-12)  });
```

As a consequence, getters and setters are not copied faithfully, either:

```
[](#cb120-1)const original = {
[](#cb120-2)  get myGetter() { return 123 },
[](#cb120-3)  set mySetter(x) {},
[](#cb120-4)};
[](#cb120-5)assert.deepEqual({...original}, {
[](#cb120-6)  myGetter: 123, // not a getter anymore!
[](#cb120-7)  mySetter: undefined,
[](#cb120-8)});
```

The aforementioned `Object.getOwnPropertyDescriptors()` and `Object.defineProperties()` always transfer own properties with all attributes intact ([as shown later](#ch007.xhtml_copying-via-property-descriptors)).

#### 6.2.1.6 Copying is shallow

The copy has fresh versions of each key-value entry in the original, but the values of the original are not copied themselves. For example:

```
[](#cb121-1)const original = {name: 'Jane', work: {employer: 'Acme'}};
[](#cb121-2)const copy = {...original};
[](#cb121-3)
[](#cb121-4)// Property .name is a copy: changing the copy
[](#cb121-5)// does not affect the original
[](#cb121-6)copy.name = 'John';
[](#cb121-7)assert.deepEqual(original,
[](#cb121-8)  {name: 'Jane', work: {employer: 'Acme'}});
[](#cb121-9)assert.deepEqual(copy,
[](#cb121-10)  {name: 'John', work: {employer: 'Acme'}});
[](#cb121-11)
[](#cb121-12)// The value of .work is shared: changing the copy
[](#cb121-13)// affects the original
[](#cb121-14)copy.work.employer = 'Spectre';
[](#cb121-15)assert.deepEqual(
[](#cb121-16)  original, {name: 'Jane', work: {employer: 'Spectre'}});
[](#cb121-17)assert.deepEqual(
[](#cb121-18)  copy, {name: 'John', work: {employer: 'Spectre'}});
```

We’ll look at deep copying later in this chapter.

### 6.2.2 Shallow copying via `Object.assign()` (optional)

`Object.assign()` works mostly like spreading into objects. That is, the following two ways of copying are mostly equivalent:

```
[](#cb122-1)const copy1 = {...original};
[](#cb122-2)const copy2 = Object.assign({}, original);
```

Using a method instead of syntax has the benefit that it can be polyfilled on older JavaScript engines via a library.

`Object.assign()` is not completely like spreading, though. It differs in one, relatively subtle point: it creates properties differently.

*   `Object.assign()` uses *assignment* to create the properties of the copy.
*   Spreading *defines* new properties in the copy.

Among other things, assignment invokes own and inherited setters, while definition doesn’t ([more information on assignment vs. definition](#ch012.xhtml_ch_property-assignment-vs-definition)). This difference is rarely noticeable. The following code is an example, but it’s contrived:

```
[](#cb123-1)const original = {['__proto__']: null}; // (A)
[](#cb123-2)const copy1 = {...original};
[](#cb123-3)// copy1 has the own property '__proto__'
[](#cb123-4)assert.deepEqual(
[](#cb123-5)  Object.keys(copy1), ['__proto__']);
[](#cb123-6)
[](#cb123-7)const copy2 = Object.assign({}, original);
[](#cb123-8)// copy2 has the prototype null
[](#cb123-9)assert.equal(Object.getPrototypeOf(copy2), null);
```

By using a computed property key in line A, we create `.__proto__` as an own property and don’t invoke the inherited setter. However, when `Object.assign()` copies that property, it does invoke the setter. (For more information on `.__proto__`, see [“JavaScript for impatient programmers”](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#proto).)

### 6.2.3 Shallow copying via `Object.getOwnPropertyDescriptors()` and `Object.defineProperties()` (optional)

JavaScript lets us create properties via [*property descriptors*](#ch010.xhtml_property-descriptors), objects that specify property attributes. For example, via the `Object.defineProperties()`, which we have already seen in action. If we combine that method with `Object.getOwnPropertyDescriptors()`, we can copy more faithfully:

```
[](#cb124-1)function copyAllOwnProperties(original) {
[](#cb124-2)  return Object.defineProperties(
[](#cb124-3)    {}, Object.getOwnPropertyDescriptors(original));
[](#cb124-4)}
```

That eliminates two issues of copying objects via spreading.

First, all attributes of own properties are copied correctly. Therefore, we can now copy own getters and own setters:

```
[](#cb125-1)const original = {
[](#cb125-2)  get myGetter() { return 123 },
[](#cb125-3)  set mySetter(x) {},
[](#cb125-4)};
[](#cb125-5)assert.deepEqual(copyAllOwnProperties(original), original);
```

Second, thanks to `Object.getOwnPropertyDescriptors()`, non-enumerable properties are copied, too:

```
[](#cb126-1)const arr = ['a', 'b'];
[](#cb126-2)assert.equal(arr.length, 2);
[](#cb126-3)assert.equal({}.hasOwnProperty.call(arr, 'length'), true);
[](#cb126-4)
[](#cb126-5)const copy = copyAllOwnProperties(arr);
[](#cb126-6)assert.equal({}.hasOwnProperty.call(copy, 'length'), true);
```

## 6.3 Deep copying in JavaScript

Now it is time to tackle deep copying. First, we will deep-copy manually, then we’ll examine generic approaches.

### 6.3.1 Manual deep copying via nested spreading

If we nest spreading, we get deep copies:

```
[](#cb127-1)const original = {name: 'Jane', work: {employer: 'Acme'}};
[](#cb127-2)const copy = {name: original.name, work: {...original.work}};
[](#cb127-3)
[](#cb127-4)// We copied successfully:
[](#cb127-5)assert.deepEqual(original, copy);
[](#cb127-6)// The copy is deep:
[](#cb127-7)assert.ok(original.work !== copy.work);
```

### 6.3.2 Hack: generic deep copying via JSON

This is a hack, but, in a pinch, it provides a quick solution: In order to deep-copy an object `original`, we first convert it to a JSON string and parse that JSON string:

```
[](#cb128-1)function jsonDeepCopy(original) {
[](#cb128-2)  return JSON.parse(JSON.stringify(original));
[](#cb128-3)}
[](#cb128-4)const original = {name: 'Jane', work: {employer: 'Acme'}};
[](#cb128-5)const copy = jsonDeepCopy(original);
[](#cb128-6)assert.deepEqual(original, copy);
```

The significant downside of this approach is that we can only copy properties with keys and values that are supported by JSON.

Some unsupported keys and values are simply ignored:

```
[](#cb129-1)assert.deepEqual(
[](#cb129-2)  jsonDeepCopy({
[](#cb129-3)    // Symbols are not supported as keys
[](#cb129-4)    [Symbol('a')]: 'abc',
[](#cb129-5)    // Unsupported value
[](#cb129-6)    b: function () {},
[](#cb129-7)    // Unsupported value
[](#cb129-8)    c: undefined,
[](#cb129-9)  }),
[](#cb129-10)  {} // empty object
[](#cb129-11));
```

Others cause exceptions:

```
[](#cb130-1)assert.throws(
[](#cb130-2)  () => jsonDeepCopy({a: 123n}),
[](#cb130-3)  /^TypeError: Do not know how to serialize a BigInt$/);
```

### 6.3.3 Implementing generic deep copying

The following function generically deep-copies a value `original`:

```
[](#cb131-1)function deepCopy(original) {
[](#cb131-2)  if (Array.isArray(original)) {
[](#cb131-3)    const copy = [];
[](#cb131-4)    for (const [index, value] of original.entries()) {
[](#cb131-5)      copy[index] = deepCopy(value);
[](#cb131-6)    }
[](#cb131-7)    return copy;
[](#cb131-8)  } else if (typeof original === 'object' && original !== null) {
[](#cb131-9)    const copy = {};
[](#cb131-10)    for (const [key, value] of Object.entries(original)) {
[](#cb131-11)      copy[key] = deepCopy(value);
[](#cb131-12)    }
[](#cb131-13)    return copy;
[](#cb131-14)  } else {
[](#cb131-15)    // Primitive value: atomic, no need to copy
[](#cb131-16)    return original;
[](#cb131-17)  }
[](#cb131-18)}
```

The function handles three cases:

*   If `original` is an Array we create a new Array and deep-copy the elements of `original` into it.
*   If `original` is an object, we use a similar approach.
*   If `original` is a primitive value, we don’t have to do anything.

Let’s try out `deepCopy()`:

```
[](#cb132-1)const original = {a: 1, b: {c: 2, d: {e: 3}}};
[](#cb132-2)const copy = deepCopy(original);
[](#cb132-3)
[](#cb132-4)// Are copy and original deeply equal?
[](#cb132-5)assert.deepEqual(copy, original);
[](#cb132-6)
[](#cb132-7)// Did we really copy all levels
[](#cb132-8)// (equal content, but different objects)?
[](#cb132-9)assert.ok(copy     !== original);
[](#cb132-10)assert.ok(copy.b   !== original.b);
[](#cb132-11)assert.ok(copy.b.d !== original.b.d);
```

Note that `deepCopy()` only fixes one issue of spreading: shallow copying. All others remain: prototypes are not copied, special objects are only partially copied, non-enumerable properties are ignored, most property attributes are ignored.

Implementing copying completely generically is generally impossible: Not all data is a tree, sometimes we don’t want to copy all properties, etc.

#### 6.3.3.1 A more concise version of `deepCopy()`

We can make our previous implementation of `deepCopy()` more concise if we use `.map()` and `Object.fromEntries()`:

```
[](#cb133-1)function deepCopy(original) {
[](#cb133-2)  if (Array.isArray(original)) {
[](#cb133-3)    return original.map(elem => deepCopy(elem));
[](#cb133-4)  } else if (typeof original === 'object' && original !== null) {
[](#cb133-5)    return Object.fromEntries(
[](#cb133-6)      Object.entries(original)
[](#cb133-7)        .map(([k, v]) => [k, deepCopy(v)]));
[](#cb133-8)  } else {
[](#cb133-9)    // Primitive value: atomic, no need to copy
[](#cb133-10)    return original;
[](#cb133-11)  }
[](#cb133-12)}
```

## 6.4 Further reading

*   [§14 “Copying instances of classes: `.clone()` vs. copy constructors”](#ch015.xhtml_ch_copying-class-instances) explains class-based patterns for copying.
*   [Section “Spreading into object literals”](https://exploringjs.com/impatient-js/ch_single-objects.html#spreading-into-object-literals) in “JavaScript for impatient programmers”
*   [Section “Spreading into Array literals”](https://exploringjs.com/impatient-js/ch_arrays.html#spreading-into-array-literals) in “JavaScript for impatient programmers”
*   [Section “Prototype chains”](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains) in “JavaScript for impatient programmers”

# 7 Updating data destructively and non-destructively

* * *

*   7.1 [Examples: updating an object destructively and non-destructively](#ch008.xhtml_examples-updating-an-object-destructively-and-non-destructively)
*   7.2 [Examples: updating an Array destructively and non-destructively](#ch008.xhtml_examples-updating-an-array-destructively-and-non-destructively)
*   7.3 [Manual deep updating](#ch008.xhtml_manual-deep-updating)
*   7.4 [Implementing generic deep updating](#ch008.xhtml_implementing-generic-deep-updating)

* * *

In this chapter, we learn about two different ways of updating data:

*   A *destructive update* of data mutates the data so that it has the desired form.
*   A *non-destructive update* of data creates a copy of the data that has the desired form.

The latter way is similar to first making a copy and then changing it destructively, but it does both at the same time.

## 7.1 Examples: updating an object destructively and non-destructively

The following code shows a function that updates object properties destructively and uses it on an object.

```
[](#cb134-1)function setPropertyDestructively(obj, key, value) {
[](#cb134-2)  obj[key] = value;
[](#cb134-3)  return obj;
[](#cb134-4)}
[](#cb134-5)
[](#cb134-6)const obj = {city: 'Berlin', country: 'Germany'};
[](#cb134-7)setPropertyDestructively(obj, 'city', 'Munich');
[](#cb134-8)assert.deepEqual(obj, {city: 'Munich', country: 'Germany'});
```

The following code demonstrates non-destructive updating of an object:

```
[](#cb135-1)function setPropertyNonDestructively(obj, key, value) {
[](#cb135-2)  const updatedObj = {};
[](#cb135-3)  for (const [k, v] of Object.entries(obj)) {
[](#cb135-4)    updatedObj[k] = (k === key ? value : v);
[](#cb135-5)  }
[](#cb135-6)  return updatedObj;
[](#cb135-7)}
[](#cb135-8)
[](#cb135-9)const obj = {city: 'Berlin', country: 'Germany'};
[](#cb135-10)const updatedObj = setPropertyNonDestructively(obj, 'city', 'Munich');
[](#cb135-11)
[](#cb135-12)// We have created an updated object:
[](#cb135-13)assert.deepEqual(updatedObj, {city: 'Munich', country: 'Germany'});
[](#cb135-14)
[](#cb135-15)// But we didn’t change the original:
[](#cb135-16)assert.deepEqual(obj, {city: 'Berlin', country: 'Germany'});
```

Spreading makes `setPropertyNonDestructively()` more concise:

```
[](#cb136-1)function setPropertyNonDestructively(obj, key, value) {
[](#cb136-2)  return {...obj, [key]: value};
[](#cb136-3)}
```

Both versions of `setPropertyNonDestructively()` update *shallowly*: They only change the top level of an object.

## 7.2 Examples: updating an Array destructively and non-destructively

The following code shows a function that updates Array elements destructively and uses it on an Array.

```
[](#cb137-1)function setElementDestructively(arr, index, value) {
[](#cb137-2)  arr[index] = value;
[](#cb137-3)}
[](#cb137-4)
[](#cb137-5)const arr = ['a', 'b', 'c', 'd', 'e'];
[](#cb137-6)setElementDestructively(arr, 2, 'x');
[](#cb137-7)assert.deepEqual(arr, ['a', 'b', 'x', 'd', 'e']);
```

The following code demonstrates non-destructive updating of an Array:

```
[](#cb138-1)function setElementNonDestructively(arr, index, value) {
[](#cb138-2)  const updatedArr = [];
[](#cb138-3)  for (const [i, v] of arr.entries()) {
[](#cb138-4)    updatedArr.push(i === index ? value : v);
[](#cb138-5)  }
[](#cb138-6)  return updatedArr;
[](#cb138-7)}
[](#cb138-8)
[](#cb138-9)const arr = ['a', 'b', 'c', 'd', 'e'];
[](#cb138-10)const updatedArr = setElementNonDestructively(arr, 2, 'x');
[](#cb138-11)assert.deepEqual(updatedArr, ['a', 'b', 'x', 'd', 'e']);
[](#cb138-12)assert.deepEqual(arr, ['a', 'b', 'c', 'd', 'e']);
```

`.slice()` and spreading make `setElementNonDestructively()` more concise:

```
[](#cb139-1)function setElementNonDestructively(arr, index, value) {
[](#cb139-2)  return [
[](#cb139-3)    ...arr.slice(0, index), value, ...arr.slice(index+1)];
[](#cb139-4)}
```

Both versions of `setElementNonDestructively()` update *shallowly*: They only change the top level of an Array.

## 7.3 Manual deep updating

So far, we have only updated data shallowly. Let’s tackle deep updating. The following code shows how to do it manually. We are changing name and employer.

```
[](#cb140-1)const original = {name: 'Jane', work: {employer: 'Acme'}};
[](#cb140-2)const updatedOriginal = {
[](#cb140-3)  ...original,
[](#cb140-4)  name: 'John',
[](#cb140-5)  work: {
[](#cb140-6)    ...original.work,
[](#cb140-7)    employer: 'Spectre'
[](#cb140-8)  },
[](#cb140-9)};
[](#cb140-10)
[](#cb140-11)assert.deepEqual(
[](#cb140-12)  original, {name: 'Jane', work: {employer: 'Acme'}});
[](#cb140-13)assert.deepEqual(
[](#cb140-14)  updatedOriginal, {name: 'John', work: {employer: 'Spectre'}});
```

## 7.4 Implementing generic deep updating

The following function implements generic deep updating.

```
[](#cb141-1)function deepUpdate(original, keys, value) {
[](#cb141-2)  if (keys.length === 0) {
[](#cb141-3)    return value;
[](#cb141-4)  }
[](#cb141-5)  const currentKey = keys[0];
[](#cb141-6)  if (Array.isArray(original)) {
[](#cb141-7)    return original.map(
[](#cb141-8)      (v, index) => index === currentKey
[](#cb141-9)        ? deepUpdate(v, keys.slice(1), value) // (A)
[](#cb141-10)        : v); // (B)
[](#cb141-11)  } else if (typeof original === 'object' && original !== null) {
[](#cb141-12)    return Object.fromEntries(
[](#cb141-13)      Object.entries(original).map(
[](#cb141-14)        (keyValuePair) => {
[](#cb141-15)          const [k,v] = keyValuePair;
[](#cb141-16)          if (k === currentKey) {
[](#cb141-17)            return [k, deepUpdate(v, keys.slice(1), value)]; // (C)
[](#cb141-18)          } else {
[](#cb141-19)            return keyValuePair; // (D)
[](#cb141-20)          }
[](#cb141-21)        }));
[](#cb141-22)  } else {
[](#cb141-23)    // Primitive value
[](#cb141-24)    return original;
[](#cb141-25)  }
[](#cb141-26)}
```

If we see `value` as the root of a tree that we are updating, then `deepUpdate()` only deeply changes a single branch (line A and C). All other branches are copied shallowly (line B and D).

This is what using `deepUpdate()` looks like:

```
[](#cb142-1)const original = {name: 'Jane', work: {employer: 'Acme'}};
[](#cb142-2)
[](#cb142-3)const copy = deepUpdate(original, ['work', 'employer'], 'Spectre');
[](#cb142-4)assert.deepEqual(copy, {name: 'Jane', work: {employer: 'Spectre'}});
[](#cb142-5)assert.deepEqual(original, {name: 'Jane', work: {employer: 'Acme'}});
```

# 8 The problems of shared mutable state and how to avoid them

* * *

*   8.1 [What is shared mutable state and why is it problematic?](#ch009.xhtml_what-is-shared-mutable-state-and-why-is-it-problematic)
*   8.2 [Avoiding sharing by copying data](#ch009.xhtml_avoiding-sharing-by-copying-data)
    *   8.2.1 [How does copying help with shared mutable state?](#ch009.xhtml_how-does-copying-help-with-shared-mutable-state)
*   8.3 [Avoiding mutations by updating non-destructively](#ch009.xhtml_avoiding-mutations-by-updating-non-destructively)
    *   8.3.1 [How does non-destructive updating help with shared mutable state?](#ch009.xhtml_how-does-non-destructive-updating-help-with-shared-mutable-state)
*   8.4 [Preventing mutations by making data immutable](#ch009.xhtml_preventing-mutations-by-making-data-immutable)
    *   8.4.1 [How does immutability help with shared mutable state?](#ch009.xhtml_how-does-immutability-help-with-shared-mutable-state)
*   8.5 [Libraries for avoiding shared mutable state](#ch009.xhtml_libraries-for-avoiding-shared-mutable-state)
    *   8.5.1 [Immutable.js](#ch009.xhtml_immutable.js)
    *   8.5.2 [Immer](#ch009.xhtml_immer)

* * *

This chapter answers the following questions:

*   What is shared mutable state?
*   Why is it problematic?
*   How can its problems be avoided?

## 8.1 What is shared mutable state and why is it problematic?

Shared mutable state works as follows:

*   If two or more parties can change the same data (variables, objects, etc.).
*   And if their lifetimes overlap.
*   Then there is a risk of one party’s modifications preventing other parties from working correctly.

Note that this definition applies to function calls, cooperative multitasking (e.g., async functions in JavaScript), etc. The risks are similar in each case.

The following code is an example. The example is not realistic, but it demonstrates the risks and is easy to understand:

```
[](#cb143-1)function logElements(arr) {
[](#cb143-2)  while (arr.length > 0) {
[](#cb143-3)    console.log(arr.shift());
[](#cb143-4)  }
[](#cb143-5)}
[](#cb143-6)
[](#cb143-7)function main() {
[](#cb143-8)  const arr = ['banana', 'orange', 'apple'];
[](#cb143-9)
[](#cb143-10)  console.log('Before sorting:');
[](#cb143-11)  logElements(arr);
[](#cb143-12)
[](#cb143-13)  arr.sort(); // changes arr
[](#cb143-14)
[](#cb143-15)  console.log('After sorting:');
[](#cb143-16)  logElements(arr); // (A)
[](#cb143-17)}
[](#cb143-18)main();
[](#cb143-19)
[](#cb143-20)// Output:
[](#cb143-21)// 'Before sorting:'
[](#cb143-22)// 'banana'
[](#cb143-23)// 'orange'
[](#cb143-24)// 'apple'
[](#cb143-25)// 'After sorting:'
```

In this case, there are two independent parties:

*   Function `main()` wants to log an Array before and after sorting it.
*   Function `logElements()` logs the elements of its parameter `arr`, but removes them while doing so.

`logElements()` breaks `main()` and causes it to log an empty Array in line A.

In the remainder of this chapter, we look at three ways of avoiding the problems of shared mutable state:

*   Avoiding sharing by copying data
*   Avoiding mutations by updating non-destructively
*   Preventing mutations by making data immutable

In particular, we will come back to the example that we’ve just seen and fix it.

## 8.2 Avoiding sharing by copying data

Copying data is one way of avoiding sharing it.

![](media/file0.svg)  **Background**

For background on copying data in JavaScript, please refer to the following two chapters in this book:

*   [§6 “Copying objects and Arrays”](#ch007.xhtml_ch_copying-objects-and-arrays)
*   [§14 “Copying instances of classes: `.clone()` vs. copy constructors”](#ch015.xhtml_ch_copying-class-instances)

### 8.2.1 How does copying help with shared mutable state?

As long as we only *read* from shared state, we don’t have any problems. Before *modifying* it, we need to “un-share” it, by copying it (as deeply as necessary).

*Defensive copying* is a technique to always copy when issues *might* arise. Its objective is to keep the current entity (function, class, etc.) safe:

*   Input: Copying (potentially) shared data passed to us, lets us use that data without being disturbed by an external entity.
*   Output: Copying internal data before exposing it to an outside party, means that that party can’t disrupt our internal activity.

Note that these measures protect us from other parties, but they also protect other parties from us.

The next sections illustrate both kinds of defensive copying.

#### 8.2.1.1 Copying shared input

Remember that in the motivating example at the beginning of this chapter, we got into trouble because `logElements()` modified its parameter `arr`:

```
[](#cb144-1)function logElements(arr) {
[](#cb144-2)  while (arr.length > 0) {
[](#cb144-3)    console.log(arr.shift());
[](#cb144-4)  }
[](#cb144-5)}
```

Let’s add defensive copying to this function:

```
[](#cb145-1)function logElements(arr) {
[](#cb145-2)  arr = [...arr]; // defensive copy
[](#cb145-3)  while (arr.length > 0) {
[](#cb145-4)    console.log(arr.shift());
[](#cb145-5)  }
[](#cb145-6)}
```

Now `logElements()` doesn’t cause problems anymore, if it is called inside `main()`:

```
[](#cb146-1)function main() {
[](#cb146-2)  const arr = ['banana', 'orange', 'apple'];
[](#cb146-3)
[](#cb146-4)  console.log('Before sorting:');
[](#cb146-5)  logElements(arr);
[](#cb146-6)
[](#cb146-7)  arr.sort(); // changes arr
[](#cb146-8)
[](#cb146-9)  console.log('After sorting:');
[](#cb146-10)  logElements(arr); // (A)
[](#cb146-11)}
[](#cb146-12)main();
[](#cb146-13)
[](#cb146-14)// Output:
[](#cb146-15)// 'Before sorting:'
[](#cb146-16)// 'banana'
[](#cb146-17)// 'orange'
[](#cb146-18)// 'apple'
[](#cb146-19)// 'After sorting:'
[](#cb146-20)// 'apple'
[](#cb146-21)// 'banana'
[](#cb146-22)// 'orange'
```

#### 8.2.1.2 Copying exposed internal data

Let’s start with a class `StringBuilder` that doesn’t copy internal data it exposes (line A):

```
[](#cb147-1)class StringBuilder {
[](#cb147-2)  _data = [];
[](#cb147-3)  add(str) {
[](#cb147-4)    this._data.push(str);
[](#cb147-5)  }
[](#cb147-6)  getParts() {
[](#cb147-7)    // We expose internals without copying them:
[](#cb147-8)    return this._data; // (A)
[](#cb147-9)  }
[](#cb147-10)  toString() {
[](#cb147-11)    return this._data.join('');
[](#cb147-12)  }
[](#cb147-13)}
```

As long as `.getParts()` isn’t used, everything works well:

```
[](#cb148-1)const sb1 = new StringBuilder();
[](#cb148-2)sb1.add('Hello');
[](#cb148-3)sb1.add(' world!');
[](#cb148-4)assert.equal(sb1.toString(), 'Hello world!');
```

If, however, the result of `.getParts()` is changed (line A), then the `StringBuilder` ceases to work correctly:

```
[](#cb149-1)const sb2 = new StringBuilder();
[](#cb149-2)sb2.add('Hello');
[](#cb149-3)sb2.add(' world!');
[](#cb149-4)sb2.getParts().length = 0; // (A)
[](#cb149-5)assert.equal(sb2.toString(), ''); // not OK
```

The solution is to copy the internal `._data` defensively before it is exposed (line A):

```
[](#cb150-1)class StringBuilder {
[](#cb150-2)  this._data = [];
[](#cb150-3)  add(str) {
[](#cb150-4)    this._data.push(str);
[](#cb150-5)  }
[](#cb150-6)  getParts() {
[](#cb150-7)    // Copy defensively
[](#cb150-8)    return [...this._data]; // (A)
[](#cb150-9)  }
[](#cb150-10)  toString() {
[](#cb150-11)    return this._data.join('');
[](#cb150-12)  }
[](#cb150-13)}
```

Now changing the result of `.getParts()` doesn’t interfere with the operation of `sb` anymore:

```
[](#cb151-1)const sb = new StringBuilder();
[](#cb151-2)sb.add('Hello');
[](#cb151-3)sb.add(' world!');
[](#cb151-4)sb.getParts().length = 0;
[](#cb151-5)assert.equal(sb.toString(), 'Hello world!'); // OK
```

## 8.3 Avoiding mutations by updating non-destructively

We can avoid mutations if we only update data non-destructively.

![](media/file0.svg)  **Background**

For more information on updating data, see [§7 “Updating data destructively and non-destructively”](#ch008.xhtml_ch_updating-destructively-and-nondestructively).

### 8.3.1 How does non-destructive updating help with shared mutable state?

With non-destructive updating, sharing data becomes unproblematic, because we never mutate the shared data. (This only works if everyone that accesses the data does that!)

Intriguingly, copying data becomes trivially simple:

```
[](#cb152-1)const original = {city: 'Berlin', country: 'Germany'};
[](#cb152-2)const copy = original;
```

This works, because we are only making non-destructive changes and are therefore copying the data on demand.

## 8.4 Preventing mutations by making data immutable

We can prevent mutations of shared data by making that data immutable.

![](media/file0.svg)  **Background**

For background on how to make data immutable in JavaScript, please refer to the following two chapters in this book:

*   [§10 “Protecting objects from being changed”](#ch011.xhtml_ch_protecting-objects)
*   [§15 “Immutable wrappers for collections”](#ch016.xhtml_ch_immutable-collection-wrappers)

### 8.4.1 How does immutability help with shared mutable state?

If data is immutable, it can be shared without any risks. In particular, there is no need to copy defensively.

![](media/file2.svg)  **Non-destructive updating is an important complement to immutable data**

If we combine the two, immutable data becomes virtually as versatile as mutable data but without the associated risks.

## 8.5 Libraries for avoiding shared mutable state

There are several libraries available for JavaScript that support immutable data with non-destructive updating. Two popular ones are:

*   [Immutable.js](https://github.com/immutable-js/immutable-js) provides immutable data structures for lists, stacks, sets, maps, etc.
*   [Immer](https://immerjs.github.io/immer/) also supports immutability and non-destructive updating but for plain objects, Arrays, Sets, and Maps. That is, no new data structures are needed.

These libraries are described in more detail in the next two sections.

### 8.5.1 Immutable.js

In its repository, [the library Immutable.js](https://github.com/immutable-js/immutable-js) is described as:

> Immutable persistent data collections for JavaScript which increase efficiency and simplicity.

Immutable.js provides immutable data structures such as:

*   `List`
*   `Stack`
*   `Set` (which is different from JavaScript’s built-in `Set`)
*   `Map` (which is different from JavaScript’s built-in `Map`)
*   Etc.

In the following example, we use an immutable `Map`:

```
[](#cb153-1)import {Map} from 'immutable/dist/immutable.es.js';
[](#cb153-2)const map0 = Map([
[](#cb153-3)  [false, 'no'],
[](#cb153-4)  [true, 'yes'],
[](#cb153-5)]);
[](#cb153-6)
[](#cb153-7)// We create a modified version of map0:
[](#cb153-8)const map1 = map0.set(true, 'maybe');
[](#cb153-9)
[](#cb153-10)// The modified version is different from the original:
[](#cb153-11)assert.ok(map1 !== map0);
[](#cb153-12)assert.equal(map1.equals(map0), false); // (A)
[](#cb153-13)
[](#cb153-14)// We undo the change we just made:
[](#cb153-15)const map2 = map1.set(true, 'yes');
[](#cb153-16)
[](#cb153-17)// map2 is a different object than map0,
[](#cb153-18)// but it has the same content
[](#cb153-19)assert.ok(map2 !== map0);
[](#cb153-20)assert.equal(map2.equals(map0), true); // (B)
```

Notes:

*   Instead of modifying the receiver, “destructive” operations such as `.set()` return modified copies.
*   To check if two data structures have the same content, we use the built-in `.equals()` method (line A and line B).

### 8.5.2 Immer

In its repository, [the library Immer](https://immerjs.github.io/immer/) is described as:

> Create the next immutable state by mutating the current one.

Immer helps with non-destructively updating (potentially nested) plain objects, Arrays, Sets, and Maps. That is, there are no custom data structures involved.

This is what using Immer looks like:

```
[](#cb154-1)import {produce} from 'immer/dist/immer.module.js';
[](#cb154-2)
[](#cb154-3)const people = [
[](#cb154-4)  {name: 'Jane', work: {employer: 'Acme'}},
[](#cb154-5)];
[](#cb154-6)
[](#cb154-7)const modifiedPeople = produce(people, (draft) => {
[](#cb154-8)  draft[0].work.employer = 'Cyberdyne';
[](#cb154-9)  draft.push({name: 'John', work: {employer: 'Spectre'}});
[](#cb154-10)});
[](#cb154-11)
[](#cb154-12)assert.deepEqual(modifiedPeople, [
[](#cb154-13)  {name: 'Jane', work: {employer: 'Cyberdyne'}},
[](#cb154-14)  {name: 'John', work: {employer: 'Spectre'}},
[](#cb154-15)]);
[](#cb154-16)assert.deepEqual(people, [
[](#cb154-17)  {name: 'Jane', work: {employer: 'Acme'}},
[](#cb154-18)]);
```

The original data is stored in `people`. `produce()` provides us with a variable `draft`. We pretend that this variable is `people` and use operations with which we would normally make destructive changes. Immer intercepts these operations. Instead of mutating `draft`, it non-destructively changes `people`. The result is referenced by `modifiedPeople`. As a bonus, it is deeply immutable.

`assert.deepEqual()` works because Immer returns plain objects and Arrays.

# 9 Property attributes: an introduction

* * *

*   9.1 [The structure of objects](#ch010.xhtml_the-structure-of-objects)
    *   9.1.1 [Internal slots](#ch010.xhtml_internal-slots)
    *   9.1.2 [Property keys](#ch010.xhtml_property-keys)
    *   9.1.3 [Property attributes](#ch010.xhtml_property-attributes)
*   9.2 [Property descriptors](#ch010.xhtml_property-descriptors)
*   9.3 [Retrieving descriptors for properties](#ch010.xhtml_retrieving-descriptors-for-properties)
    *   9.3.1 [`Object.getOwnPropertyDescriptor()`: retrieving a descriptor for a single property](#ch010.xhtml_object.getownpropertydescriptor-retrieving-a-descriptor-for-a-single-property)
    *   9.3.2 [`Object.getOwnPropertyDescriptors()`: retrieving descriptors for all properties of an object](#ch010.xhtml_object.getownpropertydescriptors-retrieving-descriptors-for-all-properties-of-an-object)
*   9.4 [Defining properties via descriptors](#ch010.xhtml_defining-properties-via-descriptors)
    *   9.4.1 [`Object.defineProperty()`: defining single properties via descriptors](#ch010.xhtml_object.defineproperty-defining-single-properties-via-descriptors)
    *   9.4.2 [`Object.defineProperties()`: defining multiple properties via descriptors](#ch010.xhtml_object.defineproperties-defining-multiple-properties-via-descriptors)
*   9.5 [`Object.create()`: Creating objects via descriptors](#ch010.xhtml_object.create-creating-objects-via-descriptors)
*   9.6 [Use cases for `Object.getOwnPropertyDescriptors()`](#ch010.xhtml_use-cases-for-object.getownpropertydescriptors)
    *   9.6.1 [Use case: copying properties into an object](#ch010.xhtml_use-case-copying-properties-into-an-object)
    *   9.6.2 [Use case for `Object.getOwnPropertyDescriptors()`: cloning objects](#ch010.xhtml_use-case-for-object.getownpropertydescriptors-cloning-objects)
*   9.7 [Omitting descriptor properties](#ch010.xhtml_omitting-descriptor-properties)
    *   9.7.1 [Omitting descriptor properties when creating properties](#ch010.xhtml_omitting-descriptor-properties-when-creating-properties)
    *   9.7.2 [Omitting descriptor properties when changing properties](#ch010.xhtml_omitting-descriptor-properties-when-changing-properties)
*   9.8 [What property attributes do built-in constructs use?](#ch010.xhtml_what-property-attributes-do-built-in-constructs-use)
    *   9.8.1 [Own properties created via assignment](#ch010.xhtml_own-properties-created-via-assignment)
    *   9.8.2 [Own properties created via object literals](#ch010.xhtml_own-properties-created-via-object-literals)
    *   9.8.3 [The own property `.length` of Arrays](#ch010.xhtml_the-own-property-.length-of-arrays)
    *   9.8.4 [Prototype properties of built-in classes](#ch010.xhtml_prototype-properties-of-built-in-classes)
    *   9.8.5 [Prototype properties and instance properties of user-defined classes](#ch010.xhtml_prototype-properties-and-instance-properties-of-user-defined-classes)
*   9.9 [API: property descriptors](#ch010.xhtml_api-property-descriptors)
*   9.10 [Further reading](#ch010.xhtml_further-reading-1)

* * *

In this chapter, we take a closer look at how the ECMAScript specification sees JavaScript objects. In particular, properties are not atomic in the spec, but composed of multiple *attributes* (think fields in a record). Even the value of a data property is stored in an attribute!

## 9.1 The structure of objects

[In the ECMAScript specification](https://tc39.es/ecma262/#sec-object-type), an object consists of:

*   *Internal slots*, which are storage locations that are not accessible from JavaScript, only from operations in the specification.
*   A collection of *properties*. Each property associates a *key* with *attributes* (think fields in a record).

### 9.1.1 Internal slots

[The specification](https://tc39.es/ecma262/#sec-object-internal-methods-and-internal-slots) describes internal slots as follows. I added bullet points and emphasized one part:

*   Internal slots correspond to internal state that is associated with objects and used by various ECMAScript specification algorithms.
*   Internal slots are not object properties and they are not inherited.
*   Depending upon the specific internal slot specification, such state may consist of:
    *   values of any ECMAScript language type or
    *   of specific ECMAScript specification type values.
*   Unless explicitly specified otherwise, internal slots are allocated as part of the process of creating an object and may not be dynamically added to an object.
*   Unless specified otherwise, the initial value of an internal slot is the value `undefined`.
*   Various algorithms within this specification create objects that have internal slots. However, **the ECMAScript language provides no direct way to associate internal slots with an object**.
*   Internal methods and internal slots are identified within this specification using names enclosed in double square brackets `[[ ]]`.

There are two kinds of internal slots:

*   Method slots for manipulating objects (getting properties, setting properties, etc.)
*   Data slots that store values.

Ordinary objects have the following data slots:

*   `.[[Prototype]]: null | object`
    *   Stores the prototype of an object.
    *   Can be accessed indirectly via `Object.getPrototypeOf()` and `Object.setPrototypeOf()`.
*   `.[[Extensible]]: boolean`
    *   Indicates if it is possible to add properties to an object.
    *   Can be set to `false` via `Object.preventExtensions()`.
*   `.[[PrivateFieldValues]]: EntryList`
    *   Is used to manage [private class fields](https://2ality.com/2019/07/private-class-fields.html).

### 9.1.2 Property keys

The key of a property is either:

*   A string
*   A symbol

### 9.1.3 Property attributes

There are two kinds of properties and they are characterized by their attributes:

*   A *data property* stores data. Its attribute `value` holds any JavaScript value.
*   An *accessor property* consists of a getter function and/or a setter function. The former is stored in the attribute `get`, the latter in the attribute `set`.

Additionally, there are attributes that both kinds of properties have. The following table lists all attributes and their default values.

| Kind of property | Name and type of attribute | Default value |
| --- | --- | --- |
| Data property | `value: any` | `undefined` |
|  | `writable: boolean` | `false` |
| Accessor property | `get: (this: any) => any` | `undefined` |
|  | `set: (this: any, v: any) => void` | `undefined` |
| All properties | `configurable: boolean` | `false` |
|  | `enumerable: boolean` | `false` |

We have already encountered the attributes `value`, `get`, and `set`. The other attributes work as follows:

*   `writable` determines if the value of a data property can be changed.
*   `configurable` determines if the attributes of a property can be changed. If it is `false`, then:
    *   We cannot delete the property.
    *   We cannot change a property from a data property to an accessor property or vice versa.
    *   We cannot change any attribute other than `value`.
    *   However, one more attribute change is allowed: We can change `writable` from `true` to `false`. The rationale behind this anomaly is [historical](https://stackoverflow.com/questions/9829817/why-can-i-set-enumerability-and-writability-of-unconfigurable-property-descrip/9843191#9843191): Property `.length` of Arrays has always been writable and non-configurable. Allowing its `writable` attribute to be changed enables us to freeze Arrays.
*   `enumerable` influences some operations (such as `Object.keys()`). If it is `false`, then those operations ignore the property. Most properties are enumerable (e.g. those created via assignment or object literals), which is why you’ll rarely notice this attribute in practice. If you are still interested in how it works, see [§12 “Enumerability of properties”](#ch013.xhtml_ch_enumerability).

#### 9.1.3.1 Pitfall: Inherited non-writable properties prevent creating own properties via assignment

If an inherited property is non-writable, we can’t use assignment to create an own property with the same key:

```
[](#cb155-1)const proto = {
[](#cb155-2)  prop: 1,
[](#cb155-3)};
[](#cb155-4)// Make proto.prop non-writable:
[](#cb155-5)Object.defineProperty(
[](#cb155-6)  proto, 'prop', {writable: false});
[](#cb155-7)
[](#cb155-8)const obj = Object.create(proto);
[](#cb155-9)
[](#cb155-10)assert.throws(
[](#cb155-11)  () => obj.prop = 2,
[](#cb155-12)  /^TypeError: Cannot assign to read only property 'prop'/);
```

For more information, see [§11.3.4 “Inherited read-only properties prevent creating own properties via assignment”](#ch012.xhtml_inherited-properties-prevent-assignment).

## 9.2 Property descriptors

A *property descriptor* encodes the attributes of a property as a JavaScript object. Their TypeScript interfaces look as follows.

```
[](#cb156-1)interface DataPropertyDescriptor {
[](#cb156-2)  value?: any;
[](#cb156-3)  writable?: boolean;
[](#cb156-4)  configurable?: boolean;
[](#cb156-5)  enumerable?: boolean;
[](#cb156-6)}
[](#cb156-7)interface AccessorPropertyDescriptor {
[](#cb156-8)  get?: (this: any) => any;
[](#cb156-9)  set?: (this: any, v: any) => void;
[](#cb156-10)  configurable?: boolean;
[](#cb156-11)  enumerable?: boolean;
[](#cb156-12)}
[](#cb156-13)type PropertyDescriptor = DataPropertyDescriptor | AccessorPropertyDescriptor;
```

The question marks indicate that all properties are optional. [§9.7 “Omitting descriptor properties”](#ch010.xhtml_omitting-descriptor-properties) describes what happens if they are omitted.

## 9.3 Retrieving descriptors for properties

### 9.3.1 `Object.getOwnPropertyDescriptor()`: retrieving a descriptor for a single property

Consider the following object:

```
[](#cb157-1)const legoBrick = {
[](#cb157-2)  kind: 'Plate 1x3',
[](#cb157-3)  color: 'yellow',
[](#cb157-4)  get description() {
[](#cb157-5)    return `${this.kind} (${this.color})`;
[](#cb157-6)  },
[](#cb157-7)};
```

Let’s first get a descriptor for the data property `.color`:

```
[](#cb158-1)assert.deepEqual(
[](#cb158-2)  Object.getOwnPropertyDescriptor(legoBrick, 'color'),
[](#cb158-3)  {
[](#cb158-4)    value: 'yellow',
[](#cb158-5)    writable: true,
[](#cb158-6)    enumerable: true,
[](#cb158-7)    configurable: true,
[](#cb158-8)  });
```

This is what the descriptor for the accessor property `.description` looks like:

```
[](#cb159-1)const desc = Object.getOwnPropertyDescriptor.bind(Object);
[](#cb159-2)assert.deepEqual(
[](#cb159-3)  Object.getOwnPropertyDescriptor(legoBrick, 'description'),
[](#cb159-4)  {
[](#cb159-5)    get: desc(legoBrick, 'description').get, // (A)
[](#cb159-6)    set: undefined,
[](#cb159-7)    enumerable: true,
[](#cb159-8)    configurable: true
[](#cb159-9)  });
```

Using the utility function `desc()` in line A ensures that `.deepEqual()` works.

### 9.3.2 `Object.getOwnPropertyDescriptors()`: retrieving descriptors for all properties of an object

```
[](#cb160-1)const legoBrick = {
[](#cb160-2)  kind: 'Plate 1x3',
[](#cb160-3)  color: 'yellow',
[](#cb160-4)  get description() {
[](#cb160-5)    return `${this.kind} (${this.color})`;
[](#cb160-6)  },
[](#cb160-7)};
[](#cb160-8)
[](#cb160-9)const desc = Object.getOwnPropertyDescriptor.bind(Object);
[](#cb160-10)assert.deepEqual(
[](#cb160-11)  Object.getOwnPropertyDescriptors(legoBrick),
[](#cb160-12)  {
[](#cb160-13)    kind: {
[](#cb160-14)      value: 'Plate 1x3',
[](#cb160-15)      writable: true,
[](#cb160-16)      enumerable: true,
[](#cb160-17)      configurable: true,
[](#cb160-18)    },
[](#cb160-19)    color: {
[](#cb160-20)      value: 'yellow',
[](#cb160-21)      writable: true,
[](#cb160-22)      enumerable: true,
[](#cb160-23)      configurable: true,
[](#cb160-24)    },
[](#cb160-25)    description: {
[](#cb160-26)      get: desc(legoBrick, 'description').get, // (A)
[](#cb160-27)      set: undefined,
[](#cb160-28)      enumerable: true,
[](#cb160-29)      configurable: true,
[](#cb160-30)    },
[](#cb160-31)  });
```

Using the helper function `desc()` in line A ensures that `.deepEqual()` works.

## 9.4 Defining properties via descriptors

If we define a property with the key `k` via a property descriptor `propDesc`, then what happens depends:

*   If there is no property with key `k`, a new own property is created that has the attributes specified by `propDesc`.
*   If there is a property with key `k`, defining changes the property’s attributes so that they match `propDesc`.

### 9.4.1 `Object.defineProperty()`: defining single properties via descriptors

First, let us create a new property via a descriptor:

```
[](#cb161-1)const car = {};
[](#cb161-2)
[](#cb161-3)Object.defineProperty(car, 'color', {
[](#cb161-4)  value: 'blue',
[](#cb161-5)  writable: true,
[](#cb161-6)  enumerable: true,
[](#cb161-7)  configurable: true,
[](#cb161-8)});
[](#cb161-9)
[](#cb161-10)assert.deepEqual(
[](#cb161-11)  car,
[](#cb161-12)  {
[](#cb161-13)    color: 'blue',
[](#cb161-14)  });
```

Next, we change the kind of a property via a descriptor; we turn a data property into a getter:

```
[](#cb162-1)const car = {
[](#cb162-2)  color: 'blue',
[](#cb162-3)};
[](#cb162-4)
[](#cb162-5)let readCount = 0;
[](#cb162-6)Object.defineProperty(car, 'color', {
[](#cb162-7)  get() {
[](#cb162-8)    readCount++;
[](#cb162-9)    return 'red';
[](#cb162-10)  },
[](#cb162-11)});
[](#cb162-12)
[](#cb162-13)assert.equal(car.color, 'red');
[](#cb162-14)assert.equal(readCount, 1);
```

Lastly, we change the value of a data property via a descriptor:

```
[](#cb163-1)const car = {
[](#cb163-2)  color: 'blue',
[](#cb163-3)};
[](#cb163-4)
[](#cb163-5)// Use the same attributes as assignment:
[](#cb163-6)Object.defineProperty(
[](#cb163-7)  car, 'color', {
[](#cb163-8)    value: 'green',
[](#cb163-9)    writable: true,
[](#cb163-10)    enumerable: true,
[](#cb163-11)    configurable: true,
[](#cb163-12)  });
[](#cb163-13)
[](#cb163-14)assert.deepEqual(
[](#cb163-15)  car,
[](#cb163-16)  {
[](#cb163-17)    color: 'green',
[](#cb163-18)  });
```

We have used the same property attributes as assignment.

### 9.4.2 `Object.defineProperties()`: defining multiple properties via descriptors

`Object.defineProperties()` is the multi-property version of ``Object.defineProperty()`:

```
[](#cb164-1)const legoBrick1 = {};
[](#cb164-2)Object.defineProperties(
[](#cb164-3)  legoBrick1,
[](#cb164-4)  {
[](#cb164-5)    kind: {
[](#cb164-6)      value: 'Plate 1x3',
[](#cb164-7)      writable: true,
[](#cb164-8)      enumerable: true,
[](#cb164-9)      configurable: true,
[](#cb164-10)    },
[](#cb164-11)    color: {
[](#cb164-12)      value: 'yellow',
[](#cb164-13)      writable: true,
[](#cb164-14)      enumerable: true,
[](#cb164-15)      configurable: true,
[](#cb164-16)    },
[](#cb164-17)    description: {
[](#cb164-18)      get: function () {
[](#cb164-19)        return `${this.kind} (${this.color})`;
[](#cb164-20)      },
[](#cb164-21)      enumerable: true,
[](#cb164-22)      configurable: true,
[](#cb164-23)    },
[](#cb164-24)  });
[](#cb164-25)
[](#cb164-26)assert.deepEqual(
[](#cb164-27)  legoBrick1,
[](#cb164-28)  {
[](#cb164-29)    kind: 'Plate 1x3',
[](#cb164-30)    color: 'yellow',
[](#cb164-31)    get description() {
[](#cb164-32)      return `${this.kind} (${this.color})`;
[](#cb164-33)    },
[](#cb164-34)  });
```

## 9.5 `Object.create()`: Creating objects via descriptors

`Object.create()` creates a new object. Its first argument specifies the prototype of that object. Its optional second argument specifies descriptors for the properties of that object. In the next example, we create the same object as in the previous example.

```
[](#cb165-1)const legoBrick2 = Object.create(
[](#cb165-2)  Object.prototype,
[](#cb165-3)  {
[](#cb165-4)    kind: {
[](#cb165-5)      value: 'Plate 1x3',
[](#cb165-6)      writable: true,
[](#cb165-7)      enumerable: true,
[](#cb165-8)      configurable: true,
[](#cb165-9)    },
[](#cb165-10)    color: {
[](#cb165-11)      value: 'yellow',
[](#cb165-12)      writable: true,
[](#cb165-13)      enumerable: true,
[](#cb165-14)      configurable: true,
[](#cb165-15)    },
[](#cb165-16)    description: {
[](#cb165-17)      get: function () {
[](#cb165-18)        return `${this.kind} (${this.color})`;
[](#cb165-19)      },
[](#cb165-20)      enumerable: true,
[](#cb165-21)      configurable: true,
[](#cb165-22)    },
[](#cb165-23)  });
[](#cb165-24)
[](#cb165-25)// Did we really create the same object?
[](#cb165-26)assert.deepEqual(legoBrick1, legoBrick2); // Yes!
```

## 9.6 Use cases for `Object.getOwnPropertyDescriptors()`

`Object.getOwnPropertyDescriptors()` helps us with two use cases, if we combine it with `Object.defineProperties()` or `Object.create()`.

### 9.6.1 Use case: copying properties into an object

Since ES6, JavaScript already has had a tool method for copying properties: `Object.assign()`. However, this method uses simple get and set operations to copy a property whose key is `key`:

```
[](#cb166-1)target[key] = source[key];
```

That means that it only creates a faithful copy of a property if:

*   Its attribute `writable` is `true` and its attribute `enumerable` is `true` (because that’s how assignment creates properties).
*   It is a data property.

The following example illustrates this limitation. Object `source` has a setter whose key is `data`.

```
[](#cb167-1)const source = {
[](#cb167-2)  set data(value) {
[](#cb167-3)    this._data = value;
[](#cb167-4)  }
[](#cb167-5)};
[](#cb167-6)
[](#cb167-7)// Because there is only a setter, property `data` exists,
[](#cb167-8)// but has the value `undefined`.
[](#cb167-9)assert.equal('data' in source, true);
[](#cb167-10)assert.equal(source.data, undefined);
```

If we use `Object.assign()` to copy property `data`, then the accessor property `data` is converted to a data property:

```
[](#cb168-1)const target1 = {};
[](#cb168-2)Object.assign(target1, source);
[](#cb168-3)
[](#cb168-4)assert.deepEqual(
[](#cb168-5)  Object.getOwnPropertyDescriptor(target1, 'data'),
[](#cb168-6)  {
[](#cb168-7)    value: undefined,
[](#cb168-8)    writable: true,
[](#cb168-9)    enumerable: true,
[](#cb168-10)    configurable: true,
[](#cb168-11)  });
[](#cb168-12)
[](#cb168-13)// For comparison, the original:
[](#cb168-14)const desc = Object.getOwnPropertyDescriptor.bind(Object);
[](#cb168-15)assert.deepEqual(
[](#cb168-16)  Object.getOwnPropertyDescriptor(source, 'data'),
[](#cb168-17)  {
[](#cb168-18)    get: undefined,
[](#cb168-19)    set: desc(source, 'data').set,
[](#cb168-20)    enumerable: true,
[](#cb168-21)    configurable: true,
[](#cb168-22)  });
```

Fortunately, using `Object.getOwnPropertyDescriptors()` together with `Object.defineProperties()` does faithfully copy the property `data`:

```
[](#cb169-1)const target2 = {};
[](#cb169-2)Object.defineProperties(
[](#cb169-3)  target2, Object.getOwnPropertyDescriptors(source));
[](#cb169-4)
[](#cb169-5)assert.deepEqual(
[](#cb169-6)  Object.getOwnPropertyDescriptor(target2, 'data'),
[](#cb169-7)  {
[](#cb169-8)    get: undefined,
[](#cb169-9)    set: desc(source, 'data').set,
[](#cb169-10)    enumerable: true,
[](#cb169-11)    configurable: true,
[](#cb169-12)  });
```

#### 9.6.1.1 Pitfall: copying methods that use `super`

A method that uses `super` is firmly connected with its *home object* (the object it is stored in). There is currently no way to copy or move such a method to a different object.

### 9.6.2 Use case for `Object.getOwnPropertyDescriptors()`: cloning objects

Shallow cloning is similar to copying properties, which is why `Object.getOwnPropertyDescriptors()` is a good choice here, too.

To create the clone, we use `Object.create()`:

```
[](#cb170-1)const original = {
[](#cb170-2)  set data(value) {
[](#cb170-3)    this._data = value;
[](#cb170-4)  }
[](#cb170-5)};
[](#cb170-6)
[](#cb170-7)const clone = Object.create(
[](#cb170-8)  Object.getPrototypeOf(original),
[](#cb170-9)  Object.getOwnPropertyDescriptors(original));
[](#cb170-10)
[](#cb170-11)assert.deepEqual(original, clone);
```

For more information on this topic, see [§6 “Copying objects and Arrays”](#ch007.xhtml_ch_copying-objects-and-arrays).

## 9.7 Omitting descriptor properties

All properties of descriptors are optional. What happens when you omit a property depends on the operation.

### 9.7.1 Omitting descriptor properties when creating properties

When we create a new property via a descriptor, then omitting attributes means that their default values are used:

```
[](#cb171-1)const car = {};
[](#cb171-2)Object.defineProperty(
[](#cb171-3)  car, 'color', {
[](#cb171-4)    value: 'red',
[](#cb171-5)  });
[](#cb171-6)assert.deepEqual(
[](#cb171-7)  Object.getOwnPropertyDescriptor(car, 'color'),
[](#cb171-8)  {
[](#cb171-9)    value: 'red',
[](#cb171-10)    writable: false,
[](#cb171-11)    enumerable: false,
[](#cb171-12)    configurable: false,
[](#cb171-13)  });
```

### 9.7.2 Omitting descriptor properties when changing properties

If instead, we change an existing property, then omitting descriptor properties means that the corresponding attributes are not touched:

```
[](#cb172-1)const car = {
[](#cb172-2)  color: 'yellow',
[](#cb172-3)};
[](#cb172-4)assert.deepEqual(
[](#cb172-5)  Object.getOwnPropertyDescriptor(car, 'color'),
[](#cb172-6)  {
[](#cb172-7)    value: 'yellow',
[](#cb172-8)    writable: true,
[](#cb172-9)    enumerable: true,
[](#cb172-10)    configurable: true,
[](#cb172-11)  });
[](#cb172-12)Object.defineProperty(
[](#cb172-13)  car, 'color', {
[](#cb172-14)    value: 'pink',
[](#cb172-15)  });
[](#cb172-16)assert.deepEqual(
[](#cb172-17)  Object.getOwnPropertyDescriptor(car, 'color'),
[](#cb172-18)  {
[](#cb172-19)    value: 'pink',
[](#cb172-20)    writable: true,
[](#cb172-21)    enumerable: true,
[](#cb172-22)    configurable: true,
[](#cb172-23)  });
```

## 9.8 What property attributes do built-in constructs use?

The general rule (with few exceptions) for property attributes is:

*   Properties of objects at the beginning of a prototype chain are usually writable, enumerable, and configurable.

*   As described in [the chapter on enumerability](#ch013.xhtml_ch_enumerability), most inherited properties are non-enumerable, to hide them from legacy constructs such as `for-in` loops. Inherited properties are usually writable and configurable.

### 9.8.1 Own properties created via assignment

```
[](#cb173-1)const obj = {};
[](#cb173-2)obj.prop = 3;
[](#cb173-3)
[](#cb173-4)assert.deepEqual(
[](#cb173-5)  Object.getOwnPropertyDescriptors(obj),
[](#cb173-6)  {
[](#cb173-7)    prop: {
[](#cb173-8)      value: 3,
[](#cb173-9)      writable: true,
[](#cb173-10)      enumerable: true,
[](#cb173-11)      configurable: true,
[](#cb173-12)    }
[](#cb173-13)  });
```

### 9.8.2 Own properties created via object literals

```
[](#cb174-1)const obj = { prop: 'yes' };
[](#cb174-2)
[](#cb174-3)assert.deepEqual(
[](#cb174-4)  Object.getOwnPropertyDescriptors(obj),
[](#cb174-5)  {
[](#cb174-6)    prop: {
[](#cb174-7)      value: 'yes',
[](#cb174-8)      writable: true,
[](#cb174-9)      enumerable: true,
[](#cb174-10)      configurable: true
[](#cb174-11)    }
[](#cb174-12)  });
```

### 9.8.3 The own property `.length` of Arrays

The own property `.length` of Arrays is non-enumerable, so that it isn’t copied by `Object.assign()`, spreading, and similar operations. It is also non-configurable:

```
> Object.getOwnPropertyDescriptor([], 'length')
{ value: 0, writable: true, enumerable: false, configurable: false }
> Object.getOwnPropertyDescriptor('abc', 'length')
{ value: 3, writable: false, enumerable: false, configurable: false }
```

`.length` is a special data property, in that it is influenced by (and influences) other own properties (specifically, index properties).

### 9.8.4 Prototype properties of built-in classes

```
[](#cb176-1)assert.deepEqual(
[](#cb176-2)  Object.getOwnPropertyDescriptor(Array.prototype, 'map'),
[](#cb176-3)  {
[](#cb176-4)    value: Array.prototype.map,
[](#cb176-5)    writable: true,
[](#cb176-6)    enumerable: false,
[](#cb176-7)    configurable: true
[](#cb176-8)  });
```

### 9.8.5 Prototype properties and instance properties of user-defined classes

```
[](#cb177-1)class DataContainer {
[](#cb177-2)  accessCount = 0;
[](#cb177-3)  constructor(data) {
[](#cb177-4)    this.data = data;
[](#cb177-5)  }
[](#cb177-6)  getData() {
[](#cb177-7)    this.accessCount++;
[](#cb177-8)    return this.data;
[](#cb177-9)  }
[](#cb177-10)}
[](#cb177-11)assert.deepEqual(
[](#cb177-12)  Object.getOwnPropertyDescriptors(DataContainer.prototype),
[](#cb177-13)  {
[](#cb177-14)    constructor: {
[](#cb177-15)      value: DataContainer,
[](#cb177-16)      writable: true,
[](#cb177-17)      enumerable: false,
[](#cb177-18)      configurable: true,
[](#cb177-19)    },
[](#cb177-20)    getData: {
[](#cb177-21)      value: DataContainer.prototype.getData,
[](#cb177-22)      writable: true,
[](#cb177-23)      enumerable: false,
[](#cb177-24)      configurable: true,
[](#cb177-25)    }
[](#cb177-26)  });
```

Note that all own properties of instances of `DataContainer` are writable, enumerable, and configurable:

```
[](#cb178-1)const dc = new DataContainer('abc')
[](#cb178-2)assert.deepEqual(
[](#cb178-3)  Object.getOwnPropertyDescriptors(dc),
[](#cb178-4)  {
[](#cb178-5)    accessCount: {
[](#cb178-6)      value: 0,
[](#cb178-7)      writable: true,
[](#cb178-8)      enumerable: true,
[](#cb178-9)      configurable: true,
[](#cb178-10)    },
[](#cb178-11)    data: {
[](#cb178-12)      value: 'abc',
[](#cb178-13)      writable: true,
[](#cb178-14)      enumerable: true,
[](#cb178-15)      configurable: true,
[](#cb178-16)    }
[](#cb178-17)  });
```

## 9.9 API: property descriptors

The following tool methods use property descriptors:

*   `Object.defineProperty(obj: object, key: string|symbol, propDesc: PropertyDescriptor): object` ^([ES5])

    Creates or changes a property on `obj` whose key is `key` and whose attributes are specified via `propDesc`. Returns the modified object.

    ```
    [](#cb179-1)const obj = {};
    [](#cb179-2)const result = Object.defineProperty(
    [](#cb179-3)  obj, 'happy', {
    [](#cb179-4)    value: 'yes',
    [](#cb179-5)    writable: true,
    [](#cb179-6)    enumerable: true,
    [](#cb179-7)    configurable: true,
    [](#cb179-8)  });
    [](#cb179-9)
    [](#cb179-10)// obj was returned and modified:
    [](#cb179-11)assert.equal(result, obj);
    [](#cb179-12)assert.deepEqual(obj, {
    [](#cb179-13)  happy: 'yes',
    [](#cb179-14)});
    ```

*   `Object.defineProperties(obj: object, properties: {[k: string|symbol]: PropertyDescriptor}): object` ^([ES5])

    The batch version of `Object.defineProperty()`. Each property `p` of the object `properties` specifies one property that is to be added to `obj`: The key of `p` specifies the key of the property, the value of `p` is a descriptor that specifies the attributes of the property.

    ```
    [](#cb180-1)const address1 = Object.defineProperties({}, {
    [](#cb180-2)  street: { value: 'Evergreen Terrace', enumerable: true },
    [](#cb180-3)  number: { value: 742, enumerable: true },
    [](#cb180-4)});
    ```

*   `Object.create(proto: null|object, properties?: {[k: string|symbol]: PropertyDescriptor}): object` ^([ES5])

    First, creates an object whose prototype is `proto`. Then, if the optional parameter `properties` has been provided, adds properties to it – in the same manner as `Object.defineProperties()`. Finally, returns the result. For example, the following code snippet produces the same result as the previous snippet:

    ```
    [](#cb181-1)const address2 = Object.create(Object.prototype, {
    [](#cb181-2)  street: { value: 'Evergreen Terrace', enumerable: true },
    [](#cb181-3)  number: { value: 742, enumerable: true },
    [](#cb181-4)});
    [](#cb181-5)assert.deepEqual(address1, address2);
    ```

*   `Object.getOwnPropertyDescriptor(obj: object, key: string|symbol): undefined|PropertyDescriptor` ^([ES5])

    Returns the descriptor of the own (non-inherited) property of `obj` whose key is `key`. If there is no such property, `undefined` is returned.

    ```
    [](#cb182-1)assert.deepEqual(
    [](#cb182-2)  Object.getOwnPropertyDescriptor(Object.prototype, 'toString'),
    [](#cb182-3)  {
    [](#cb182-4)    value: {}.toString,
    [](#cb182-5)    writable: true,
    [](#cb182-6)    enumerable: false,
    [](#cb182-7)    configurable: true,
    [](#cb182-8)  });
    [](#cb182-9)assert.equal(
    [](#cb182-10)  Object.getOwnPropertyDescriptor({}, 'toString'),
    [](#cb182-11)  undefined);
    ```

*   `Object.getOwnPropertyDescriptors(obj: object): {[k: string|symbol]: PropertyDescriptor}` ^([ES2017])

    Returns an object where each property key `'k'` of `obj` is mapped to the property descriptor for `obj.k`. The result can be used as input for `Object.defineProperties()` and `Object.create()`.

    ```
    [](#cb183-1)const propertyKey = Symbol('propertyKey');
    [](#cb183-2)const obj = {
    [](#cb183-3)  [propertyKey]: 'abc',
    [](#cb183-4)  get count() { return 123 },
    [](#cb183-5)};
    [](#cb183-6)
    [](#cb183-7)const desc = Object.getOwnPropertyDescriptor.bind(Object);
    [](#cb183-8)assert.deepEqual(
    [](#cb183-9)  Object.getOwnPropertyDescriptors(obj),
    [](#cb183-10)  {
    [](#cb183-11)    [propertyKey]: {
    [](#cb183-12)      value: 'abc',
    [](#cb183-13)      writable: true,
    [](#cb183-14)      enumerable: true,
    [](#cb183-15)      configurable: true
    [](#cb183-16)    },
    [](#cb183-17)    count: {
    [](#cb183-18)      get: desc(obj, 'count').get, // (A)
    [](#cb183-19)      set: undefined,
    [](#cb183-20)      enumerable: true,
    [](#cb183-21)      configurable: true
    [](#cb183-22)    }
    [](#cb183-23)  });
    ```

    Using `desc()` in line A is a work-around so that `.deepEqual()` works.

## 9.10 Further reading

The next three chapters provide more details on property attributes:

*   [§10 “Protecting objects from being changed”](#ch011.xhtml_ch_protecting-objects)
*   [§11 “Properties: assignment vs. definition”](#ch012.xhtml_ch_property-assignment-vs-definition)
*   [§12 “Enumerability of properties”](#ch013.xhtml_ch_enumerability)

# 10 Protecting objects from being changed

* * *

*   10.1 [Levels of protection: preventing extensions, sealing, freezing](#ch011.xhtml_levels-of-protection-preventing-extensions-sealing-freezing)
*   10.2 [Preventing extensions](#ch011.xhtml_preventing-extensions)
    *   10.2.1 [Checking whether an object is extensible](#ch011.xhtml_checking-whether-an-object-is-extensible)
*   10.3 [Sealing](#ch011.xhtml_sealing)
    *   10.3.1 [Checking whether an object is sealed](#ch011.xhtml_checking-whether-an-object-is-sealed)
*   10.4 [Freezing](#ch011.xhtml_freezing)
    *   10.4.1 [Checking whether an object is frozen](#ch011.xhtml_checking-whether-an-object-is-frozen)
    *   10.4.2 [Freezing is shallow](#ch011.xhtml_freezing-is-shallow)
    *   10.4.3 [Implementing deep freezing](#ch011.xhtml_implementing-deep-freezing)
*   10.5 [Further reading](#ch011.xhtml_further-reading-2)

* * *

In this chapter, we’ll look at how objects can be protected from being changed. Examples include: Preventing properties being added and preventing properties being changed.

![](media/file0.svg)  **Required knowledge: property attributes**

For this chapter, you should be familiar with property attributes. If you aren’t, check out [§9 “Property attributes: an introduction”](#ch010.xhtml_ch_property-attributes-intro).

## 10.1 Levels of protection: preventing extensions, sealing, freezing

JavaScript has three levels of protecting objects:

*   *Preventing extensions* makes it impossible to add new properties to an object. We can still delete and change properties, though.
    *   Method: `Object.preventExtensions(obj)`
*   *Sealing* prevents extensions and makes all properties *unconfigurable* (roughly: we can’t change how a property works anymore).
    *   Method: `Object.seal(obj)`
*   *Freezing* seals an object after making all of its properties non-writable. That is, the object is not extensible, all properties are read-only and there is no way to change that.
    *   Method: `Object.freeze(obj)`

## 10.2 Preventing extensions

```
[](#cb184-1)Object.preventExtensions<T>(obj: T): T
```

This method works as follows:

*   If `obj` is not an object, it returns it.
*   Otherwise, it changes `obj` so that we can’t add properties anymore and returns it.
*   The type parameter `<T>` expresses that the result has the same type as the parameter.

Let’s use `Object.preventExtensions()` in an example:

```
[](#cb185-1)const obj = { first: 'Jane' };
[](#cb185-2)Object.preventExtensions(obj);
[](#cb185-3)assert.throws(
[](#cb185-4)  () => obj.last = 'Doe',
[](#cb185-5)  /^TypeError: Cannot add property last, object is not extensible$/);
```

We can still delete properties, though:

```
[](#cb186-1)assert.deepEquals(
[](#cb186-2)  Object.keys(obj), ['first']);
[](#cb186-3)delete obj.first;
[](#cb186-4)assert.deepEquals(
[](#cb186-5)  Object.keys(obj), []);
```

### 10.2.1 Checking whether an object is extensible

```
[](#cb187-1)Object.isExtensible(obj: any): boolean
```

Checks whether `obj` is extensible – for example:

```
> const obj = {};
> Object.isExtensible(obj)
true
> Object.preventExtensions(obj)
{}
> Object.isExtensible(obj)
false
```

## 10.3 Sealing

```
[](#cb189-1)Object.seal<T>(obj: T): T
```

Description of this method:

*   If `obj` isn’t an object, it returns it.
*   Otherwise, it prevents extensions of `obj`, makes all of its properties *unconfigurable*, and returns it. The properties being unconfigurable means that they can’t be changed, anymore (except for their values): Read-only properties stay read-only, enumerable properties stay enumerable, etc.

The following example demonstrates that sealing makes the object non-extensible and its properties unconfigurable.

```
[](#cb190-1)const obj = {
[](#cb190-2)  first: 'Jane',
[](#cb190-3)  last: 'Doe',
[](#cb190-4)};
[](#cb190-5)
[](#cb190-6)// Before sealing
[](#cb190-7)assert.equal(Object.isExtensible(obj), true);
[](#cb190-8)assert.deepEqual(
[](#cb190-9)  Object.getOwnPropertyDescriptors(obj),
[](#cb190-10)  {
[](#cb190-11)    first: {
[](#cb190-12)      value: 'Jane',
[](#cb190-13)      writable: true,
[](#cb190-14)      enumerable: true,
[](#cb190-15)      configurable: true
[](#cb190-16)    },
[](#cb190-17)    last: {
[](#cb190-18)      value: 'Doe',
[](#cb190-19)      writable: true,
[](#cb190-20)      enumerable: true,
[](#cb190-21)      configurable: true
[](#cb190-22)    }
[](#cb190-23)  });
[](#cb190-24)
[](#cb190-25)Object.seal(obj);
[](#cb190-26)
[](#cb190-27)// After sealing
[](#cb190-28)assert.equal(Object.isExtensible(obj), false);
[](#cb190-29)assert.deepEqual(
[](#cb190-30)  Object.getOwnPropertyDescriptors(obj),
[](#cb190-31)  {
[](#cb190-32)    first: {
[](#cb190-33)      value: 'Jane',
[](#cb190-34)      writable: true,
[](#cb190-35)      enumerable: true,
[](#cb190-36)      configurable: false
[](#cb190-37)    },
[](#cb190-38)    last: {
[](#cb190-39)      value: 'Doe',
[](#cb190-40)      writable: true,
[](#cb190-41)      enumerable: true,
[](#cb190-42)      configurable: false
[](#cb190-43)    }
[](#cb190-44)  });
```

We can still change the the value of property `.first`:

```
[](#cb191-1)obj.first = 'John';
[](#cb191-2)assert.deepEqual(
[](#cb191-3)  obj, {first: 'John', last: 'Doe'});
```

But we can’t change its attributes:

```
[](#cb192-1)assert.throws(
[](#cb192-2)  () => Object.defineProperty(obj, 'first', { enumerable: false }),
[](#cb192-3)  /^TypeError: Cannot redefine property: first$/);
```

### 10.3.1 Checking whether an object is sealed

```
[](#cb193-1)Object.isSealed(obj: any): boolean
```

Checks whether `obj` is sealed – for example:

```
> const obj = {};
> Object.isSealed(obj)
false
> Object.seal(obj)
{}
> Object.isSealed(obj)
true
```

## 10.4 Freezing

```
[](#cb195-1)Object.freeze<T>(obj: T): T;
```

*   This method immediately returns `obj` if it isn’t an object.
*   Otherwise, it makes all properties non-writable, seals `obj`, and returns it. That is, `obj` is not extensible, all properties are read-only and there is no way to change that.

```
[](#cb196-1)const point = { x: 17, y: -5 };
[](#cb196-2)Object.freeze(point);
[](#cb196-3)
[](#cb196-4)assert.throws(
[](#cb196-5)  () => point.x = 2,
[](#cb196-6)  /^TypeError: Cannot assign to read only property 'x'/);
[](#cb196-7)
[](#cb196-8)assert.throws(
[](#cb196-9)  () => Object.defineProperty(point, 'x', {enumerable: false}),
[](#cb196-10)  /^TypeError: Cannot redefine property: x$/);
[](#cb196-11)
[](#cb196-12)assert.throws(
[](#cb196-13)  () => point.z = 4,
[](#cb196-14)  /^TypeError: Cannot add property z, object is not extensible$/);
```

### 10.4.1 Checking whether an object is frozen

```
[](#cb197-1)Object.isFrozen(obj: any): boolean
```

Checks whether `obj` is frozen – for example:

```
> const point = { x: 17, y: -5 };
> Object.isFrozen(point)
false
> Object.freeze(point)
{ x: 17, y: -5 }
> Object.isFrozen(point)
true
```

### 10.4.2 Freezing is shallow

`Object.freeze(obj)` only freezes `obj` and its properties. It does not freeze the values of those properties – for example:

```
[](#cb199-1)const teacher = {
[](#cb199-2)  name: 'Edna Krabappel',
[](#cb199-3)  students: ['Bart'],
[](#cb199-4)};
[](#cb199-5)Object.freeze(teacher);
[](#cb199-6)
[](#cb199-7)// We can’t change own properties:
[](#cb199-8)assert.throws(
[](#cb199-9)  () => teacher.name = 'Elizabeth Hoover',
[](#cb199-10)  /^TypeError: Cannot assign to read only property 'name'/);
[](#cb199-11)
[](#cb199-12)// Alas, we can still change values of own properties:
[](#cb199-13)teacher.students.push('Lisa');
[](#cb199-14)assert.deepEqual(
[](#cb199-15)  teacher, {
[](#cb199-16)    name: 'Edna Krabappel',
[](#cb199-17)    students: ['Bart', 'Lisa'],
[](#cb199-18)  });
```

### 10.4.3 Implementing deep freezing

If we want deep freezing, we need to implement it ourselves:

```
[](#cb200-1)function deepFreeze(value) {
[](#cb200-2)  if (Array.isArray(value)) {
[](#cb200-3)    for (const element of value) {
[](#cb200-4)      deepFreeze(element);
[](#cb200-5)    }
[](#cb200-6)    Object.freeze(value);
[](#cb200-7)  } else if (typeof value === 'object' && value !== null) {
[](#cb200-8)    for (const v of Object.values(value)) {
[](#cb200-9)      deepFreeze(v);
[](#cb200-10)    }
[](#cb200-11)    Object.freeze(value);
[](#cb200-12)  } else {
[](#cb200-13)    // Nothing to do: primitive values are already immutable
[](#cb200-14)  } 
[](#cb200-15)  return value;
[](#cb200-16)}
```

Revisiting the example from the previous section, we can check if `deepFreeze()` really freezes deeply:

```
[](#cb201-1)const teacher = {
[](#cb201-2)  name: 'Edna Krabappel',
[](#cb201-3)  students: ['Bart'],
[](#cb201-4)};
[](#cb201-5)deepFreeze(teacher);
[](#cb201-6)
[](#cb201-7)assert.throws(
[](#cb201-8)  () => teacher.students.push('Lisa'),
[](#cb201-9)  /^TypeError: Cannot add property 1, object is not extensible$/);
```

## 10.5 Further reading

*   More information on patterns for preventing data structures from being changed: [§15 “Immutable wrappers for collections”](#ch016.xhtml_ch_immutable-collection-wrappers)

# 11 Properties: assignment vs. definition

* * *

*   11.1 [Assignment vs. definition](#ch012.xhtml_assignment-vs.-definition)
    *   11.1.1 [Assignment](#ch012.xhtml_assignment)
    *   11.1.2 [Definition](#ch012.xhtml_definition)
*   11.2 [Assignment and definition in theory (optional)](#ch012.xhtml_assignment-and-definition-in-theory-optional)
    *   11.2.1 [Assigning to a property](#ch012.xhtml_assigning-to-a-property)
    *   11.2.2 [Defining a property](#ch012.xhtml_defining-a-property)
*   11.3 [Definition and assignment in practice](#ch012.xhtml_definition-and-assignment-in-practice)
    *   11.3.1 [Only definition allows us to create a property with arbitrary attributes](#ch012.xhtml_only-definition-allows-us-to-create-a-property-with-arbitrary-attributes)
    *   11.3.2 [The assignment operator does not change properties in prototypes](#ch012.xhtml_the-assignment-operator-does-not-change-properties-in-prototypes)
    *   11.3.3 [Assignment calls setters, definition doesn’t](#ch012.xhtml_setters-and-assignment-vs-definition)
    *   11.3.4 [Inherited read-only properties prevent creating own properties via assignment](#ch012.xhtml_inherited-properties-prevent-assignment)
*   11.4 [Which language constructs use definition, which assignment?](#ch012.xhtml_which-language-constructs-use-definition-which-assignment)
    *   11.4.1 [The properties of an object literal are added via definition](#ch012.xhtml_the-properties-of-an-object-literal-are-added-via-definition)
    *   11.4.2 [The assignment operator `=` always uses assignment](#ch012.xhtml_the-assignment-operator-always-uses-assignment)
    *   11.4.3 [Public class fields are added via definition](#ch012.xhtml_public-class-fields-are-added-via-definition)
*   11.5 [Further reading and sources of this chapter](#ch012.xhtml_further-reading-and-sources-of-this-chapter-2)

* * *

There are two ways of creating or changing a property `prop` of an object `obj`:

*   *Assigning*: `obj.prop = true`
*   *Defining*: `Object.defineProperty(obj, '', {value: true})`

This chapter explains how they work.

![](media/file0.svg)  **Required knowledge: property attributes and property descriptors**

For this chapter, you should be familiar with property attributes and property descriptors. If you aren’t, check out [§9 “Property attributes: an introduction”](#ch010.xhtml_ch_property-attributes-intro).

## 11.1 Assignment vs. definition

### 11.1.1 Assignment

We use the assignment operator `=` to assign a value `value` to a property `.prop` of an object `obj`:

```
[](#cb202-1)obj.prop = value
```

This operator works differently depending on what `.prop` looks like:

*   Changing properties: If there is an own data property `.prop`, assignment changes its value to `value`.

*   Invoking setters: If there is an own or inherited setter for `.prop`, assignment invokes that setter.

*   Creating properties: If there is no own data property `.prop` and no own or inherited setter for it, assignment creates a new own data property.

That is, the main purpose of assignment is making changes. That’s why it supports setters.

### 11.1.2 Definition

To define a property with the key `propKey` of an object `obj`, we use an operation such as the following method:

```
[](#cb203-1)Object.defineProperty(obj, propKey, propDesc)
```

This method works differently depending on what the property looks like:

*   Changing properties: If an own property with key `propKey` exists, defining changes its property attributes as specified by the property descriptor `propDesc` (if possible).
*   Creating properties: Otherwise, defining creates an own property with the attributes specified by `propDesc` (if possible).

That is, the main purpose of definition is to create an own property (even if there is an inherited setter, which it ignores) and to change property attributes.

## 11.2 Assignment and definition in theory (optional)

![](media/file2.svg)  **Property descriptors in the ECMAScript specification**

In specification operations, property descriptors are not JavaScript objects but [*Records*](https://tc39.es/ecma262/#sec-list-and-record-specification-type), a spec-internal data structure that has *fields*. The keys of fields are written in double brackets. For example, `Desc.[[Configurable]]` accesses the field `.[[Configurable]]` of `Desc`. These records are translated to and from JavaScript objects when interacting with the outside world.

### 11.2.1 Assigning to a property

The actual work of assigning to a property is handled via [the following operation](https://tc39.es/ecma262/#sec-ordinarysetwithowndescriptor) in the ECMAScript specification:

```
OrdinarySetWithOwnDescriptor(O, P, V, Receiver, ownDesc)
```

These are the parameters:

*   `O` is the object that is currently being visited.
*   `P` is the key of the property that we are assigning to.
*   `V` is the value we are assigning.
*   `Receiver` is the object where the assignment started.
*   `ownDesc` is the descriptor of `O[P]` or `null` if that property doesn’t exist.

The return value is a boolean that indicates whether or not the operation succeeded. As explained [later in this chapter](#ch012.xhtml_control-flow-of-assignment), strict-mode assignment throws a `TypeError` if `OrdinarySetWithOwnDescriptor()` fails.

This is a high-level summary of the algorithm:

*   It traverses the prototype chain of `Receiver` until it finds a property whose key is `P`. The traversal is done by calling `OrdinarySetWithOwnDescriptor()` recursively. During recursion, `O` changes and points to the object that is currently being visited, but `Receiver` stays the same.
*   Depending on what the traversal finds, an own property is created in `Receiver` (where recursion started) or something else happens.

In more detail, this algorithm works as follows:

*   If `ownDesc` is `undefined`, then we haven’t yet found a property with key `P`:
    *   If `O` has a prototype `parent`, then we return `parent.[[Set]](P, V, Receiver)`. This continues our search. The method call usually ends up invoking `OrdinarySetWithOwnDescriptor()` recursively.

    *   Otherwise, our search for `P` has failed and we set `ownDesc` as follows:

        ```
        {
          [[Value]]: undefined, [[Writable]]: true,
          [[Enumerable]]: true, [[Configurable]]: true
        }
        ```

        With this `ownDesc`, the next `if` statement will create an own property in `Receiver`.

*   If `ownDesc` specifies a data property, then we have found a property:
    *   If `ownDesc.[[Writable]]` is `false`, return `false`. This means that any non-writable property `P` (own or inherited!) prevents assignment.
    *   Let `existingDescriptor` be `Receiver.[[GetOwnProperty]](P)`. That is, retrieve the descriptor of the property where the assignment started. We now have:
        *   The current object `O` and the current property descriptor `ownDesc` on one hand.
        *   The original object `Receiver` and the original property descriptor `existingDescriptor` on the other hand.
    *   If `existingDescriptor` is not `undefined`:
        *   (If we get here, then we are still at the beginning of the prototype chain – we only recurse if `Receiver` does not have a property `P`.)
        *   The following two `if` conditions should never be `true` because `ownDesc` and `existingDesc` should be equal:
            *   If `existingDescriptor` specifies an accessor, return `false`.
            *   If `existingDescriptor.[[Writable]]` is `false`, return `false`.
        *   Return `Receiver.[[DefineOwnProperty]](P, { [[Value]]: V })`. This internal method performs definition, which we use to change the value of property `Receiver[P]`. The definition algorithm is described in the next subsection.
    *   Else:
        *   (If we get here, then `Receiver` does not have an own property with key `P`.)
        *   Return `CreateDataProperty(Receiver, P, V)`. ([This operation](https://tc39.es/ecma262/#sec-createdataproperty) creates an own data property in its first argument.)
*   (If we get here, then `ownDesc` describes an accessor property that is own or inherited.)
*   Let `setter` be `ownDesc.[[Set]]`.
*   If `setter` is `undefined`, return `false`.
*   Perform `Call(setter, Receiver, «V»)`. [`Call()`](https://tc39.es/ecma262/#sec-call) invokes the function object `setter` with `this` set to `Receiver` and the single parameter `V` (French quotes `«»` are used for lists in the specification).
*   Return `true`.

#### 11.2.1.1 How do we get from an assignment to `OrdinarySetWithOwnDescriptor()`?

Evaluating an assignment without destructuring involves the following steps:

*   In the spec, evaluation starts in [the section on the runtime semantics of `AssignmentExpression`](https://tc39.es/ecma262/#sec-assignment-operators-runtime-semantics-evaluation). This section handles providing names for anonymous functions, destructuring, and more.
*   If there is no destructuring pattern, then [`PutValue()`](https://tc39.es/ecma262/#sec-putvalue) is used to make the assignment.
*   For property assignments, `PutValue()` invokes the internal method `.[[Set]]()`.
*   For ordinary objects, [`.[[Set]]()`](https://tc39.es/ecma262/#sec-ordinary-object-internal-methods-and-internal-slots-set-p-v-receiver) calls `OrdinarySet()` (which calls `OrdinarySetWithOwnDescriptor()`) and returns the result.

Notably, `PutValue()` throws a `TypeError` in strict mode if the result of `.[[Set]]()` is `false`.

### 11.2.2 Defining a property

The actual work of defining a property is handled via [the following operation](https://tc39.es/ecma262/#sec-validateandapplypropertydescriptor) in the ECMAScript specification:

```
ValidateAndApplyPropertyDescriptor(O, P, extensible, Desc, current)
```

The parameters are:

*   The object `O` where we want to define a property. There is a special validation-only mode where `O` is `undefined`. We are ignoring this mode here.
*   The property key `P` of the property we want to define.
*   `extensible` indicates if `O` is extensible.
*   `Desc` is a property descriptor specifying the attributes we want the property to have.
*   `current` contains the property descriptor of an own property `O[P]` if it exists. Otherwise, `current` is `undefined`.

The result of the operation is a boolean that indicates if it succeeded. Failure can have different consequences. Some callers ignore the result. Others, such as `Object.defineProperty()`, throw an exception if the result is `false`.

This is a summary of the algorithm:

*   If `current` is `undefined`, then property `P` does not currently exist and must be created.

    *   If `extensible` is `false`, return `false` indicating that the property could not be added.
    *   Otherwise, check `Desc` and create either a data property or an accessor property.
    *   Return `true`.
*   If `Desc` doesn’t have any fields, return `true` indicating that the operation succeeded (because no changes had to be made).

*   If `current.[[Configurable]]` is `false`:

    *   (`Desc` is not allowed to change attributes other than `value`.)
    *   If `Desc.[[Configurable]]` exists, it must have the same value as `current.[[Configurable]]`. If not, return `false`.
    *   Same check: `Desc.[[Enumerable]]`
*   Next, we *validate* the property descriptor `Desc`: Can the attributes described by `current` be changed to the values specified by `Desc`? If not, return `false`. If yes, go on.

    *   If the descriptor is *generic* (with no attributes specific to data properties or accessor properties), then validation is successful and we can move on.
    *   Else if one descriptor specifies a data property and the other an accessor property:
        *   The current property must be configurable (otherwise its attributes can’t be changed as necessary). If not, `false` is returned.
        *   Change the current property from a data property to an accessor property or vice versa. When doing so, the values of `.[[Configurable]]` and `.[[Enumerable]]` are preserved, all other attributes get [default values](#ch010.xhtml_property-attributes) (`undefined` for object-valued attributes, `false` for boolean-valued attributes).
    *   Else if both descriptors specify data properties:
        *   If both `current.[[Configurable]]` and `current.[[Writable]]` are `false`, then no changes are allowed and `Desc` and `current` must specify the same attributes:
            *   (Due to `current.[[Configurable]]` being `false`, `Desc.[[Configurable]]` and `Desc.[[Enumerable]]` were already checked previously and have the correct values.)
            *   If `Desc.[[Writable]]` exists and is `true`, then return `false`.
            *   If `Desc.[[Value]]` exists and does not have the same value as `current.[[Value]]`, then return `false`.
            *   There is nothing more to do. Return `true` indicating that the algorithm succeeded.
            *   (Note that normally, we can’t change any attributes of a non-configurable property other than its value. The one exception to this rule is that we can always go from writable to non-writable. This algorithm handles this exception correctly.)
    *   Else (both descriptors specify accessor properties):
        *   If `current.[[Configurable]]` is `false`, then no changes are allowed and `Desc` and `current` must specify the same attributes:
            *   (Due to `current.[[Configurable]]` being `false`, `Desc.[[Configurable]]` and `Desc.[[Enumerable]]` were already checked previously and have the correct values.)
            *   If `Desc.[[Set]]` exists, it must have the same value as `current.[[Set]]`. If not, return `false`.
            *   Same check: `Desc.[[Get]]`
            *   There is nothing more to do. Return `true` indicating that the algorithm succeeded.
*   Set the attributes of the property with key `P` to the values specified by `Desc`. Due to validation, we can be sure that all of the changes are allowed.

*   Return `true`.

## 11.3 Definition and assignment in practice

This section describes some consequences of how property definition and assignment work.

### 11.3.1 Only definition allows us to create a property with arbitrary attributes

If we create an own property via assignment, it always creates properties whose attributes `writable`, `enumerable`, and `configurable` are all `true`.

```
[](#cb207-1)const obj = {};
[](#cb207-2)obj.dataProp = 'abc';
[](#cb207-3)assert.deepEqual(
[](#cb207-4)  Object.getOwnPropertyDescriptor(obj, 'dataProp'),
[](#cb207-5)  {
[](#cb207-6)    value: 'abc',
[](#cb207-7)    writable: true,
[](#cb207-8)    enumerable: true,
[](#cb207-9)    configurable: true,
[](#cb207-10)  });
```

Therefore, if we want to specify arbitrary attributes, we must use definition.

And while we can create getters and setters inside object literals, we can’t add them later via assignment. Here, too, we need definition.

### 11.3.2 The assignment operator does not change properties in prototypes

Let us consider the following setup, where `obj` inherits the property `prop` from `proto`.

```
[](#cb208-1)const proto = { prop: 'a' };
[](#cb208-2)const obj = Object.create(proto);
```

We can’t (destructively) change `proto.prop` by assigning to `obj.prop`. Doing so creates a new own property:

```
[](#cb209-1)assert.deepEqual(
[](#cb209-2)  Object.keys(obj), []);
[](#cb209-3)
[](#cb209-4)obj.prop = 'b';
[](#cb209-5)
[](#cb209-6)// The assignment worked:
[](#cb209-7)assert.equal(obj.prop, 'b');
[](#cb209-8)
[](#cb209-9)// But we created an own property and overrode proto.prop,
[](#cb209-10)// we did not change it:
[](#cb209-11)assert.deepEqual(
[](#cb209-12)  Object.keys(obj), ['prop']);
[](#cb209-13)assert.equal(proto.prop, 'a');
```

The rationale for this behavior is as follows: Prototypes can have properties whose values are shared by all of their descendants. If we want to change such a property in only one descendant, we must do so non-destructively, via overriding. Then the change does not affect the other descendants.

### 11.3.3 Assignment calls setters, definition doesn’t

What is the difference between defining the property `.prop` of `obj` versus assigning to it?

If we define, then our intention is to either create or change an own (non-inherited) property of `obj`. Therefore, definition ignores the inherited setter for `.prop` in the following example:

```
[](#cb210-1)let setterWasCalled = false;
[](#cb210-2)const proto = {
[](#cb210-3)  get prop() {
[](#cb210-4)    return 'protoGetter';
[](#cb210-5)  },
[](#cb210-6)  set prop(x) {
[](#cb210-7)    setterWasCalled = true;
[](#cb210-8)  },
[](#cb210-9)};
[](#cb210-10)const obj = Object.create(proto);
[](#cb210-11)
[](#cb210-12)assert.equal(obj.prop, 'protoGetter');
[](#cb210-13)
[](#cb210-14)// Defining obj.prop:
[](#cb210-15)Object.defineProperty(
[](#cb210-16)  obj, 'prop', { value: 'objData' });
[](#cb210-17)assert.equal(setterWasCalled, false);
[](#cb210-18)
[](#cb210-19)// We have overridden the getter:
[](#cb210-20)assert.equal(obj.prop, 'objData');
```

If, instead, we assign to `.prop`, then our intention is often to change something that already exists and that change should be handled by the setter:

```
[](#cb211-1)let setterWasCalled = false;
[](#cb211-2)const proto = {
[](#cb211-3)  get prop() {
[](#cb211-4)    return 'protoGetter';
[](#cb211-5)  },
[](#cb211-6)  set prop(x) {
[](#cb211-7)    setterWasCalled = true;
[](#cb211-8)  },
[](#cb211-9)};
[](#cb211-10)const obj = Object.create(proto);
[](#cb211-11)
[](#cb211-12)assert.equal(obj.prop, 'protoGetter');
[](#cb211-13)
[](#cb211-14)// Assigning to obj.prop:
[](#cb211-15)obj.prop = 'objData';
[](#cb211-16)assert.equal(setterWasCalled, true);
[](#cb211-17)
[](#cb211-18)// The getter still active:
[](#cb211-19)assert.equal(obj.prop, 'protoGetter');
```

### 11.3.4 Inherited read-only properties prevent creating own properties via assignment

What happens if `.prop` is read-only in a prototype?

```
[](#cb212-1)const proto = Object.defineProperty(
[](#cb212-2)  {}, 'prop', {
[](#cb212-3)    value: 'protoValue',
[](#cb212-4)    writable: false,
[](#cb212-5)  });
```

In any object that inherits the read-only `.prop` from `proto`, we can’t use assignment to create an own property with the same key – for example:

```
[](#cb213-1)const obj = Object.create(proto);
[](#cb213-2)assert.throws(
[](#cb213-3)  () => obj.prop = 'objValue',
[](#cb213-4)  /^TypeError: Cannot assign to read only property 'prop'/);
```

Why can’t we assign? The rationale is that overriding an inherited property by creating an own property can be seen as [non-destructively changing](#ch008.xhtml_ch_updating-destructively-and-nondestructively) the inherited property. Arguably, if a property is non-writable, we shouldn’t be able to do that.

However, defining `.prop` still works and lets us override:

```
[](#cb214-1)Object.defineProperty(
[](#cb214-2)  obj, 'prop', { value: 'objValue' });
[](#cb214-3)assert.equal(obj.prop, 'objValue');
```

Accessor properties that don’t have a setter are also considered to be read-only:

```
[](#cb215-1)const proto = {
[](#cb215-2)  get prop() {
[](#cb215-3)    return 'protoValue';
[](#cb215-4)  }
[](#cb215-5)};
[](#cb215-6)const obj = Object.create(proto);
[](#cb215-7)assert.throws(
[](#cb215-8)  () => obj.prop = 'objValue',
[](#cb215-9)  /^TypeError: Cannot set property prop of #<Object> which has only a getter$/);
```

![](media/file5.svg)  **The “override mistake”: pros and cons**

The fact that read-only properties prevent assignment earlier in the prototype chain, has been given the name *override mistake*:

*   It was introduced in ECMAScript 5.1.
*   On one hand, this behavior is consistent with how prototypal inheritance and setters work. (So, arguably, it is *not* a mistake.)
*   On the other hand, with the behavior, deep-freezing the global object causes unwanted side-effects.
*   There was an attempt to change the behavior, but that broke the library Lodash and was abandoned ([pull request on GitHub](https://github.com/tc39/ecma262/pull/1320#issuecomment-443485524)).
*   Background knowledge:
    *   [Pull request on GitHub](https://github.com/tc39/ecma262/pull/1307)
    *   [Wiki page on ECMAScript.org](http://wiki.ecmascript.org/doku.php?id=strawman:fixing_override_mistake) ([archived](https://web.archive.org/web/20141230041441/http://wiki.ecmascript.org/doku.php?id=strawman:fixing_override_mistake))

## 11.4 Which language constructs use definition, which assignment?

In this section, we examine where the language uses definition and where it uses assignment. We detect which operation is used by tracking whether or not inherited setters are called. See [§11.3.3 “Assignment calls setters, definition doesn’t”](#ch012.xhtml_setters-and-assignment-vs-definition) for more information.

### 11.4.1 The properties of an object literal are added via definition

When we create properties via an object literal, JavaScript always uses definition (and therefore never calls inherited setters):

```
[](#cb216-1)let lastSetterArgument;
[](#cb216-2)const proto = {
[](#cb216-3)  set prop(x) {
[](#cb216-4)    lastSetterArgument = x;
[](#cb216-5)  },
[](#cb216-6)};
[](#cb216-7)const obj = {
[](#cb216-8)  __proto__: proto,
[](#cb216-9)  prop: 'abc',
[](#cb216-10)};
[](#cb216-11)assert.equal(lastSetterArgument, undefined);
```

### 11.4.2 The assignment operator `=` always uses assignment

The assignment operator `=` always uses assignment to create or change properties.

```
[](#cb217-1)let lastSetterArgument;
[](#cb217-2)const proto = {
[](#cb217-3)  set prop(x) {
[](#cb217-4)    lastSetterArgument = x;
[](#cb217-5)  },
[](#cb217-6)};
[](#cb217-7)const obj = Object.create(proto);
[](#cb217-8)
[](#cb217-9)// Normal assignment:
[](#cb217-10)obj.prop = 'abc';
[](#cb217-11)assert.equal(lastSetterArgument, 'abc');
[](#cb217-12)
[](#cb217-13)// Assigning via destructuring:
[](#cb217-14)[obj.prop] = ['def'];
[](#cb217-15)assert.equal(lastSetterArgument, 'def');
```

### 11.4.3 Public class fields are added via definition

Alas, even though public class fields have the same syntax as assignment, they do *not* use assignment to create properties, they use definition (like properties in object literals):

```
[](#cb218-1)let lastSetterArgument1;
[](#cb218-2)let lastSetterArgument2;
[](#cb218-3)class A {
[](#cb218-4)  set prop1(x) {
[](#cb218-5)    lastSetterArgument1 = x;
[](#cb218-6)  }
[](#cb218-7)  set prop2(x) {
[](#cb218-8)    lastSetterArgument2 = x;
[](#cb218-9)  }
[](#cb218-10)}
[](#cb218-11)class B extends A {
[](#cb218-12)  prop1 = 'one';
[](#cb218-13)  constructor() {
[](#cb218-14)    super();
[](#cb218-15)    this.prop2 = 'two';
[](#cb218-16)  }
[](#cb218-17)}
[](#cb218-18)new B();
[](#cb218-19)
[](#cb218-20)// The public class field uses definition:
[](#cb218-21)assert.equal(lastSetterArgument1, undefined);
[](#cb218-22)// Inside the constructor, we trigger assignment:
[](#cb218-23)assert.equal(lastSetterArgument2, 'two');
```

## 11.5 Further reading and sources of this chapter

*   [Section “Prototype chains”](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html#prototype-chains) in “JavaScript for impatient programmers”

*   [Email by Allen Wirfs-Brock to the es-discuss mailing list](https://mail.mozilla.org/pipermail/es-discuss/2012-July/024227.html): “The distinction between assignment and definition […] was not very important when all ES had was data properties and there was no way for ES code to manipulate property attributes.” [That changed with ECMAScript 5.]

# 12 Enumerability of properties

* * *

*   12.1 [How enumerability affects property-iterating constructs](#ch013.xhtml_how-enumerability-affects-property-iterating-constructs)
    *   12.1.1 [Operations that only consider enumerable properties](#ch013.xhtml_operations-that-only-consider-enumerable-properties)
    *   12.1.2 [Operations that consider both enumerable and non-enumerable properties](#ch013.xhtml_operations-that-consider-both-enumerable-and-non-enumerable-properties)
    *   12.1.3 [Naming rules for introspective operations](#ch013.xhtml_naming-rules-for-introspective-operations)
*   12.2 [The enumerability of pre-defined and created properties](#ch013.xhtml_the-enumerability-of-pre-defined-and-created-properties)
*   12.3 [Use cases for enumerability](#ch013.xhtml_use-cases-for-enumerability)
    *   12.3.1 [Use case: Hiding properties from the `for-in` loop](#ch013.xhtml_for-in-loop)
    *   12.3.2 [Use case: Marking properties as not to be copied](#ch013.xhtml_use-case-marking-properties-as-not-to-be-copied)
    *   12.3.3 [Marking properties as private](#ch013.xhtml_marking-properties-as-private)
    *   12.3.4 [Hiding own properties from `JSON.stringify()`](#ch013.xhtml_hiding-own-properties-from-json.stringify)
*   12.4 [Conclusion](#ch013.xhtml_conclusion)

* * *

Enumerability is an *attribute* of object properties. In this chapter, we take a closer look at how it is used and how it influences operations such as `Object.keys()` and `Object.assign()`.

![](media/file0.svg)  **Required knowledge: property attributes**

For this chapter, you should be familiar with property attributes. If you aren’t, check out [§9 “Property attributes: an introduction”](#ch010.xhtml_ch_property-attributes-intro).

## 12.1 How enumerability affects property-iterating constructs

To demonstrate how various operations are affected by enumerability, we use the following object `obj` whose prototype is `proto`.

```
[](#cb219-1)const protoEnumSymbolKey = Symbol('protoEnumSymbolKey');
[](#cb219-2)const protoNonEnumSymbolKey = Symbol('protoNonEnumSymbolKey');
[](#cb219-3)const proto = Object.defineProperties({}, {
[](#cb219-4)  protoEnumStringKey: {
[](#cb219-5)    value: 'protoEnumStringKeyValue',
[](#cb219-6)    enumerable: true,
[](#cb219-7)  },
[](#cb219-8)  [protoEnumSymbolKey]: {
[](#cb219-9)    value: 'protoEnumSymbolKeyValue',
[](#cb219-10)    enumerable: true,
[](#cb219-11)  },
[](#cb219-12)  protoNonEnumStringKey: {
[](#cb219-13)    value: 'protoNonEnumStringKeyValue',
[](#cb219-14)    enumerable: false,
[](#cb219-15)  },
[](#cb219-16)  [protoNonEnumSymbolKey]: {
[](#cb219-17)    value: 'protoNonEnumSymbolKeyValue',
[](#cb219-18)    enumerable: false,
[](#cb219-19)  },
[](#cb219-20)});
[](#cb219-21)
[](#cb219-22)const objEnumSymbolKey = Symbol('objEnumSymbolKey');
[](#cb219-23)const objNonEnumSymbolKey = Symbol('objNonEnumSymbolKey');
[](#cb219-24)const obj = Object.create(proto, {
[](#cb219-25)  objEnumStringKey: {
[](#cb219-26)    value: 'objEnumStringKeyValue',
[](#cb219-27)    enumerable: true,
[](#cb219-28)  },
[](#cb219-29)  [objEnumSymbolKey]: {
[](#cb219-30)    value: 'objEnumSymbolKeyValue',
[](#cb219-31)    enumerable: true,
[](#cb219-32)  },
[](#cb219-33)  objNonEnumStringKey: {
[](#cb219-34)    value: 'objNonEnumStringKeyValue',
[](#cb219-35)    enumerable: false,
[](#cb219-36)  },
[](#cb219-37)  [objNonEnumSymbolKey]: {
[](#cb219-38)    value: 'objNonEnumSymbolKeyValue',
[](#cb219-39)    enumerable: false,
[](#cb219-40)  },
[](#cb219-41)});
```

### 12.1.1 Operations that only consider enumerable properties

Table 2: Operations that ignore non-enumerable properties.

| Operation |  | String keys | Symbol keys | Inherited |
| --- | --- | --- | --- | --- |
| `Object.keys()` | ES5 | `✔` | `✘` | `✘` |
| `Object.values()` | ES2017 | `✔` | `✘` | `✘` |
| `Object.entries()` | ES2017 | `✔` | `✘` | `✘` |
| Spreading `{...x}` | ES2018 | `✔` | `✔` | `✘` |
| `Object.assign()` | ES6 | `✔` | `✔` | `✘` |
| `JSON.stringify()` | ES5 | `✔` | `✘` | `✘` |
| `for-in` | ES1 | `✔` | `✘` | `✔` |

The following operations (summarized in tbl. [2](#ch013.xhtml_tbl:operations-ignoring-non-enumerable-properties)) only consider enumerable properties:

*   `Object.keys()` ^([ES5]) returns the keys of enumerable own string-keyed properties.

    ```
    > Object.keys(obj)
    [ 'objEnumStringKey' ]
    ```

*   `Object.values()` ^([ES2017]) returns the values of enumerable own string-keyed properties.

    ```
    > Object.values(obj)
    [ 'objEnumStringKeyValue' ]
    ```

*   `Object.entries()` ^([ES2017]) returns key-value pairs for enumerable own string-keyed properties. (Note that `Object.fromEntries()` does accept symbols as keys, but only creates enumerable properties.)

    ```
    > Object.entries(obj)
    [ [ 'objEnumStringKey', 'objEnumStringKeyValue' ] ]
    ```

*   Spreading into object literals ^([ES2018]) only considers own enumerable properties (with string keys or symbol keys).

    ```
    > const copy = {...obj};
    > Reflect.ownKeys(copy)
    [ 'objEnumStringKey', objEnumSymbolKey ]
    ```

*   `Object.assign()` ^([ES6]) only copies enumerable own properties (with either string keys or symbol keys).

    ```
    > const copy = Object.assign({}, obj);
    > Reflect.ownKeys(copy)
    [ 'objEnumStringKey', objEnumSymbolKey ]
    ```

*   `JSON.stringify()` ^([ES5]) only stringifies enumerable own properties with string keys.

    ```
    > JSON.stringify(obj)
    '{"objEnumStringKey":"objEnumStringKeyValue"}'
    ```

*   `for-in` loop ^([ES1]) traverses the keys of own and inherited enumerable string-keyed properties.

    ```
    [](#cb226-1)const propKeys = [];
    [](#cb226-2)for (const propKey in obj) {
    [](#cb226-3)  propKeys.push(propKey);
    [](#cb226-4)}
    [](#cb226-5)assert.deepEqual(
    [](#cb226-6)  propKeys, ['objEnumStringKey', 'protoEnumStringKey']);
    ```

`for-in` is the only built-in operation where enumerability matters for inherited properties. All other operations only work with own properties.

### 12.1.2 Operations that consider both enumerable and non-enumerable properties

Table 3: Operations that consider both enumerable and non-enumerable properties.

| Operation |  | Str. keys | Sym. keys | Inherited |
| --- | --- | --- | --- | --- |
| `Object.getOwnPropertyNames()` | ES5 | `✔` | `✘` | `✘` |
| `Object.getOwnPropertySymbols()` | ES6 | `✘` | `✔` | `✘` |
| `Reflect.ownKeys()` | ES6 | `✔` | `✔` | `✘` |
| `Object.getOwnPropertyDescriptors()` | ES2017 | `✔` | `✔` | `✘` |

The following operations (summarized in tbl. [3](#ch013.xhtml_tbl:operations-considering-enumerable-and-nonenumerable-properties)) consider both enumerable and non-enumerable properties:

*   `Object.getOwnPropertyNames()` ^([ES5]) lists the keys of all own string-keyed properties.

    ```
    > Object.getOwnPropertyNames(obj)
    [ 'objEnumStringKey', 'objNonEnumStringKey' ]
    ```

*   `Object.getOwnPropertySymbols()` ^([ES6]) lists the keys of all own symbol-keyed properties.

    ```
    > Object.getOwnPropertySymbols(obj)
    [ objEnumSymbolKey, objNonEnumSymbolKey ]
    ```

*   `Reflect.ownKeys()` ^([ES6]) lists the keys of all own properties.

    ```
    > Reflect.ownKeys(obj)
    [
      'objEnumStringKey',
      'objNonEnumStringKey',
      objEnumSymbolKey,
      objNonEnumSymbolKey
    ]
    ```

*   `Object.getOwnPropertyDescriptors()` ^([ES2017]) lists the property descriptors of all own properties.

    ```
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

### 12.1.3 Naming rules for introspective operations

*Introspection* enables a program to examine the structure of values at runtime. It is *metaprogramming*: Normal programming is about writing programs; metaprogramming is about examining and/or changing programs.

In JavaScript, common introspective operations have short names, while rarely used operations have long names. Ignoring non-enumerable properties is the norm, which is why operations that do that have short names and operations that don’t, long names:

*   `Object.keys()` ignores non-enumerable properties.
*   `Object.getOwnPropertyNames()` lists the string keys of all own properties.

However, `Reflect` methods (such as `Reflect.ownKeys()`) deviate from this rule because `Reflect` provides operations that are more “meta” and related to Proxies.

Additionally, the following distinction is made (since ES6, which introduced symbols):

*   *Property keys* are either strings or symbols.
*   *Property names* are property keys that are strings.
*   *Property symbols* are property keys that are symbols.

Therefore, a better name for `Object.keys()` would now be `Object.names()`.

## 12.2 The enumerability of pre-defined and created properties

In this section, we’ll abbreviate `Object.getOwnPropertyDescriptor()` like this:

```
[](#cb231-1)const desc = Object.getOwnPropertyDescriptor.bind(Object);
```

Most data properties are created with the following attributes:

```
[](#cb232-1){
[](#cb232-2)  writable: true,
[](#cb232-3)  enumerable: false,
[](#cb232-4)  configurable: true,
[](#cb232-5)}
```

That includes:

*   Assignment
*   Object literals
*   Public class fields
*   `Object.fromEntries()`

The most important non-enumerable properties are:

*   Prototype properties of built-in classes

    ```
    > desc(Object.prototype, 'toString').enumerable
    false
    ```

*   Prototype properties created via user-defined classes

    ```
    > desc(class {foo() {}}.prototype, 'foo').enumerable
    false
    ```

*   Property `.length` of Arrays:

    ```
    > Object.getOwnPropertyDescriptor([], 'length')
    { value: 0, writable: true, enumerable: false, configurable: false }
    ```

*   Property `.length` of strings (note that all properties of primitive values are read-only):

    ```
    > Object.getOwnPropertyDescriptor('', 'length')
    { value: 0, writable: false, enumerable: false, configurable: false }
    ```

We’ll look at the use cases for enumerability next, which will tell us why some properties are enumerable and others aren’t.

## 12.3 Use cases for enumerability

Enumerability is an inconsistent feature. It does have use cases, but there is always some kind of caveat. In this section, we look at the use cases and the caveats.

### 12.3.1 Use case: Hiding properties from the `for-in` loop

The `for-in` loop traverses *all* enumerable string-keyed properties of an object, own and inherited ones. Therefore, the attribute `enumerable` is used to hide properties that should not be traversed. That was the reason for introducing enumerability in ECMAScript 1.

In general, it is best to avoid `for-in`. The next two subsections explain why. The following function will help us demonstrate how `for-in` works.

```
[](#cb237-1)function listPropertiesViaForIn(obj) {
[](#cb237-2)  const result = [];
[](#cb237-3)  for (const key in obj) {
[](#cb237-4)    result.push(key);
[](#cb237-5)  }
[](#cb237-6)  return result;
[](#cb237-7)}
```

#### 12.3.1.1 The caveats of using `for-in` for objects

`for-in` iterates over all properties, including inherited ones:

```
[](#cb238-1)const proto = {enumerableProtoProp: 1};
[](#cb238-2)const obj = {
[](#cb238-3)  __proto__: proto,
[](#cb238-4)  enumerableObjProp: 2,
[](#cb238-5)};
[](#cb238-6)assert.deepEqual(
[](#cb238-7)  listPropertiesViaForIn(obj),
[](#cb238-8)  ['enumerableObjProp', 'enumerableProtoProp']);
```

With normal plain objects, `for-in` doesn’t see inherited methods such as `Object.prototype.toString()` because they are all non-enumerable:

```
[](#cb239-1)const obj = {};
[](#cb239-2)assert.deepEqual(
[](#cb239-3)  listPropertiesViaForIn(obj),
[](#cb239-4)  []);
```

In user-defined classes, all inherited properties are also non-enumerable and therefore ignored:

```
[](#cb240-1)class Person {
[](#cb240-2)  constructor(first, last) {
[](#cb240-3)    this.first = first;
[](#cb240-4)    this.last = last;
[](#cb240-5)  }
[](#cb240-6)  getName() {
[](#cb240-7)    return this.first + ' ' + this.last;
[](#cb240-8)  }
[](#cb240-9)}
[](#cb240-10)const jane = new Person('Jane', 'Doe');
[](#cb240-11)assert.deepEqual(
[](#cb240-12)  listPropertiesViaForIn(jane),
[](#cb240-13)  ['first', 'last']);
```

**Conclusion:** In objects, `for-in` considers inherited properties and we usually want to ignore those. Then it is better to combine a `for-of` loop with `Object.keys()`, `Object.entries()`, etc.

#### 12.3.1.2 The caveats of using `for-in` for Arrays

The own property `.length` is non-enumerable in Arrays and strings and therefore ignored by `for-in`:

```
> listPropertiesViaForIn(['a', 'b'])
[ '0', '1' ]
> listPropertiesViaForIn('ab')
[ '0', '1' ]
```

However, it is generally not safe to use `for-in` to iterate over the indices of an Array because it considers both inherited and own properties that are not indices. The following example demonstrate what happens if an Array has an own non-index property:

```
[](#cb242-1)const arr1 = ['a', 'b'];
[](#cb242-2)assert.deepEqual(
[](#cb242-3)  listPropertiesViaForIn(arr1),
[](#cb242-4)  ['0', '1']);
[](#cb242-5)
[](#cb242-6)const arr2 = ['a', 'b'];
[](#cb242-7)arr2.nonIndexProp = 'yes';
[](#cb242-8)assert.deepEqual(
[](#cb242-9)  listPropertiesViaForIn(arr2),
[](#cb242-10)  ['0', '1', 'nonIndexProp']);
```

**Conclusion:** `for-in` should not be used for iterating over the indices of an Array because it considers both index properties and non-index properties:

*   If you are interested in the keys of an Array, use the Array method `.keys()`:

    ```
    > [...['a', 'b', 'c'].keys()]
    [ 0, 1, 2 ]
    ```

*   If you want to iterate over the elements of an Array, use a `for-of` loop, which has the added benefit of also working with other iterable data structures.

### 12.3.2 Use case: Marking properties as not to be copied

By making properties non-enumerable, we can hide them from some copying operations. Let us first examine two historical copying operations before moving on to more modern copying operations.

#### 12.3.2.1 Historical copying operation: Prototype’s `Object.extend()`

[Prototype](https://en.wikipedia.org/wiki/Prototype_JavaScript_Framework) is a JavaScript framework that was created by Sam Stephenson in February 2005 as part of the foundation for Ajax support in Ruby on Rails.

[Prototype’s `Object.extend(destination, source)`](http://api.prototypejs.org/language/Object/extend/) copies all enumerable own and inherited properties of `source` into own properties of `destination`. [It is implemented](https://github.com/prototypejs/prototype/blob/5fddd3e/src/prototype/lang/object.js#L88) as follows:

```
[](#cb244-1)function extend(destination, source) {
[](#cb244-2)  for (var property in source)
[](#cb244-3)    destination[property] = source[property];
[](#cb244-4)  return destination;
[](#cb244-5)}
```

If we use `Object.extend()` with an object, we can see that it copies inherited properties into own properties and ignores non-enumerable properties (it also ignores symbol-keyed properties). All of this is due to how `for-in` works.

```
[](#cb245-1)const proto = Object.defineProperties({}, {
[](#cb245-2)  enumProtoProp: {
[](#cb245-3)    value: 1,
[](#cb245-4)    enumerable: true,
[](#cb245-5)  },
[](#cb245-6)  nonEnumProtoProp: {
[](#cb245-7)    value: 2,
[](#cb245-8)    enumerable: false,
[](#cb245-9)  },
[](#cb245-10)});
[](#cb245-11)const obj = Object.create(proto, {
[](#cb245-12)  enumObjProp: {
[](#cb245-13)    value: 3,
[](#cb245-14)    enumerable: true,
[](#cb245-15)  },
[](#cb245-16)  nonEnumObjProp: {
[](#cb245-17)    value: 4,
[](#cb245-18)    enumerable: false,
[](#cb245-19)  },
[](#cb245-20)});
[](#cb245-21)
[](#cb245-22)assert.deepEqual(
[](#cb245-23)  extend({}, obj),
[](#cb245-24)  {enumObjProp: 3, enumProtoProp: 1});
```

#### 12.3.2.2 Historical copying operation: jQuery’s `$.extend()`

[jQuery’s `$.extend(target, source1, source2, ···)`](https://api.jquery.com/jquery.extend/) works similar to `Object.extend()`:

*   It copies all enumerable own and inherited properties of `source1` into own properties of `target`.
*   Then it does the same with `source2`.
*   Etc.

#### 12.3.2.3 The downsides of enumerability-driven copying

Basing copying on enumerability has several downsides:

*   While enumerability is useful for hiding inherited properties, it is mainly used in this manner because we usually only want to copy own properties into own properties. The same effect can be better achieved by ignoring inherited properties.

*   Which properties to copy often depends on the task at hand; it rarely makes sense to have a single flag for all use cases. A better choice is to provide a copying operation with a *predicate* (a callback that returns a boolean) that tells it when to ignore properties.

*   Enumerability conveniently hides the own property `.length` of Arrays when copying. But that is an incredibly rare exceptional case: a magic property that both influences sibling properties and is influenced by them. If we implement this kind of magic ourselves, we will use (inherited) getters and/or setters, not (own) data properties.

#### 12.3.2.4 `Object.assign()` ^([ES5])

In ES6, [`Object.assign(target, source_1, source_2, ···)`](https://exploringjs.com/impatient-js/ch_single-objects.html#object.assign) can be used to merge the sources into the target. All own enumerable properties of the sources are considered (with either string keys or symbol keys). `Object.assign()` uses a “get” operation to read a value from a source and a “set” operation to write a value to the target.

With regard to enumerability, `Object.assign()` continues the tradition of `Object.extend()` and `$.extend()`. [Quoting Yehuda Katz](https://mail.mozilla.org/pipermail/es-discuss/2012-October/025934.html):

> `Object.assign` would pave the cowpath of all of the `extend()` APIs already in circulation. We thought the precedent of not copying enumerable methods in those cases was enough reason for `Object.assign` to have this behavior.

In other words: `Object.assign()` was created with an upgrade path from `$.extend()` (and similar) in mind. Its approach is cleaner than `$.extend`’s because it ignores inherited properties.

#### 12.3.2.5 A rare example of non-enumerability being useful when copying

Cases where non-enumerability helps are few. One rare example is [a recent issue that the liberary `fs-extra` had](https://github.com/jprichardson/node-fs-extra/issues/577):

*   The built-in Node.js module `fs` has a property `.promises` that contains an object with a Promise-based version of the `fs` API. At the time of the issue, reading `.promise` led to the following warning being logged to the console:

    ```
    ExperimentalWarning: The fs.promises API is experimental
    ```

*   In addition to providing its own functionality, `fs-extra` also re-exports everything that’s in `fs`. For CommonJS modules, that means copying all properties of `fs` into the `module.exports` of `fs-extra` ([via `Object.assign()`](https://github.com/jprichardson/node-fs-extra/blob/master/lib/index.js)). And when `fs-extra` did that, it triggered the warning. That was confusing because it happened every time `fs-extra` was loaded.

*   [A quick fix](https://github.com/nodejs/node/pull/20504) was to make property `fs.promises` non-enumerable. Afterwards, `fs-extra` ignored it.

### 12.3.3 Marking properties as private

If we make a property non-enumerable, it can’t by seen by `Object.keys()`, the `for-in` loop, etc., anymore. With regard to those mechanisms, the property is private.

However, there are several problems with this approach:

*   When copying an object, we normally want to copy private properties. That clashes with making properties non-enumerable that shouldn’t be copied (see previous section).
*   The property isn’t really private. Getting, setting and several other mechanisms make no distinction between enumerable and non-enumerable properties.
*   When working with code either as source or interactively, we can’t immediately see whether a property is enumerable or not. A naming convention (such as prefixing property names with an underscore) is easier to discover.
*   We can’t use enumerability to distinguish between public and private methods because methods in prototypes are non-enumerable by default.

### 12.3.4 Hiding own properties from `JSON.stringify()`

`JSON.stringify()` does not include properties in its output that are non-enumerable. We can therefore use enumerability to determine which own properties should be exported to JSON. This use case is similar to the previous one, marking properties as private. But it is also different because this is more about exporting and slightly different considerations apply. For example: Can an object be completely reconstructed from JSON?

As an alternative to enumerability, an object can implement the method `.toJSON()` and `JSON.stringify()` stringifies whatever that method returns, instead of the object itself. The next example demonstrates how that works.

```
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

I find `toJSON()` cleaner than enumerability. It also gives us more freedom w.r.t. what the storage format should look like.

## 12.4 Conclusion

We have seen that almost all applications for non-enumerability are work-arounds that now have other and better solutions.

For our own code, we can usually pretend that enumerability doesn’t exist:

*   Creating properties via object literals and assignment always creates enumerable properties.
*   Prototype properties created via classes are always non-enumerable.

That is, we automatically follow best practices.

# 13 Techniques for instantiating classes

* * *

*   13.1 [The problem: initializing a property asynchronously](#ch014.xhtml_the-problem-initializing-a-property-asynchronously)
*   13.2 [Solution: Promise-based constructor](#ch014.xhtml_solution-promise-based-constructor)
    *   13.2.1 [Using an immediately-invoked asynchronous arrow function](#ch014.xhtml_using-an-immediately-invoked-asynchronous-arrow-function)
*   13.3 [Solution: static factory method](#ch014.xhtml_solution-static-factory-method)
    *   13.3.1 [Improvement: private constructor via secret token](#ch014.xhtml_improvement-private-constructor-via-secret-token)
    *   13.3.2 [Improvement: constructor throws, factory method borrows the class prototype](#ch014.xhtml_improvement-constructor-throws-factory-method-borrows-the-class-prototype)
    *   13.3.3 [Improvement: instances are inactive by default, activated by factory method](#ch014.xhtml_improvement-instances-are-inactive-by-default-activated-by-factory-method)
    *   13.3.4 [Variant: separate factory function](#ch014.xhtml_variant-separate-factory-function)
*   13.4 [Subclassing a Promise-based constructor (optional)](#ch014.xhtml_subclassing-a-promise-based-constructor-optional)
*   13.5 [Conclusion](#ch014.xhtml_conclusion-1)
*   13.6 [Further reading](#ch014.xhtml_further-reading-3)

* * *

In this chapter, we examine several approaches for creating instances of classes: Constructors, factory functions, etc. We do so by solving one concrete problem several times. The focus of this chapter is on classes, which is why alternatives to classes are ignored.

## 13.1 The problem: initializing a property asynchronously

The following container class is supposed to receive the contents of its property `.data` asynchronously. This is our first attempt:

```
[](#cb248-1)class DataContainer {
[](#cb248-2)  #data; // (A)
[](#cb248-3)  constructor() {
[](#cb248-4)    Promise.resolve('downloaded')
[](#cb248-5)      .then(data => this.#data = data); // (B)
[](#cb248-6)  }
[](#cb248-7)  getData() {
[](#cb248-8)    return 'DATA: '+this.#data; // (C)
[](#cb248-9)  }
[](#cb248-10)}
```

Key issue of this code: Property `.data` is initially `undefined`.

```
[](#cb249-1)const dc = new DataContainer();
[](#cb249-2)assert.equal(dc.getData(), 'DATA: undefined');
[](#cb249-3)setTimeout(() => assert.equal(
[](#cb249-4)  dc.getData(), 'DATA: downloaded'), 0);
```

In line A, we declare the [private field](https://2ality.com/2019/07/private-class-fields.html) `.#data` that we use in line B and line C.

The Promise inside the constructor of `DataContainer` is settled asynchronously, which is why we can only see the final value of `.data` if we finish the current task and start a new one, via `setTimeout()`. In other words, the instance of `DataContainer` is not completely initialized, yet, when we first see it.

## 13.2 Solution: Promise-based constructor

What if we delay access to the instance of `DataContainer` until it is fully initialized? We can achieve that by returning a Promise from the constructor. By default, a constructor returns a new instance of the class that it is part of. We can override that if we explicitly return an object:

```
[](#cb250-1)class DataContainer {
[](#cb250-2)  #data;
[](#cb250-3)  constructor() {
[](#cb250-4)    return Promise.resolve('downloaded')
[](#cb250-5)      .then(data => {
[](#cb250-6)        this.#data = data;
[](#cb250-7)        return this; // (A)
[](#cb250-8)      });
[](#cb250-9)  }
[](#cb250-10)  getData() {
[](#cb250-11)    return 'DATA: '+this.#data;
[](#cb250-12)  }
[](#cb250-13)}
[](#cb250-14)new DataContainer()
[](#cb250-15)  .then(dc => assert.equal( // (B)
[](#cb250-16)    dc.getData(), 'DATA: downloaded'));
```

Now we have to wait until we can access our instance (line B). It is passed on to us after the data is “downloaded” (line A). There are two possible sources of errors in this code:

*   The download may fail and produce a rejection.
*   An exception may be thrown in the body of the first `.then()` callback.

In either case, the errors become rejections of the Promise that is returned from the constructor.

Pros and cons:

*   A benefit of this approach is that we can only access the instance once it is fully initialized. And there is no other way of creating instances of `DataContainer`.
*   A disadvantage is that it may be surprising to have a constructor return a Promise instead of an instance.

### 13.2.1 Using an immediately-invoked asynchronous arrow function

Instead of using the Promise API directly to create the Promise that is returned from the constructor, we can also use an asynchronous arrow function that [we invoke immediately](https://exploringjs.com/impatient-js/ch_async-functions.html#immediately-invoked-async-arrow-functions):

```
[](#cb251-1)constructor() {
[](#cb251-2)  return (async () => {
[](#cb251-3)    this.#data = await Promise.resolve('downloaded');
[](#cb251-4)    return this;
[](#cb251-5)  })();
[](#cb251-6)}
```

## 13.3 Solution: static factory method

A *static factory method* of a class `C` creates instances of `C` and is an alternative to using `new C()`. Common names for static factory methods in JavaScript:

*   `.create()`: Creates a new instance. Example: `Object.create()`
*   `.from()`: Creates a new instance based on a different object, by copying and/or converting it. Example: `Array.from()`
*   `.of()`: Creates a new instance by assembling values specified via arguments. Example: `Array.of()`

In the following example, `DataContainer.create()` is a static factory method. It returns Promises for instances of `DataContainer`:

```
[](#cb252-1)class DataContainer {
[](#cb252-2)  #data;
[](#cb252-3)  static async create() {
[](#cb252-4)    const data = await Promise.resolve('downloaded');
[](#cb252-5)    return new this(data);
[](#cb252-6)  }
[](#cb252-7)  constructor(data) {
[](#cb252-8)    this.#data = data;
[](#cb252-9)  }
[](#cb252-10)  getData() {
[](#cb252-11)    return 'DATA: '+this.#data;
[](#cb252-12)  }
[](#cb252-13)}
[](#cb252-14)DataContainer.create()
[](#cb252-15)  .then(dc => assert.equal(
[](#cb252-16)    dc.getData(), 'DATA: downloaded'));
```

This time, all asynchronous functionality is contained in `.create()`, which enables the rest of the class to be completely synchronous and therefore simpler.

Pros and cons:

*   A benefit of this approach is that the constructor becomes simple.
*   A disadvantage of this approach is that it’s now possible to create instances that are incorrectly set up, via `new DataContainer()`.

### 13.3.1 Improvement: private constructor via secret token

If we want to ensure that instances are always correctly set up, we must ensure that only `DataContainer.create()` can invoke the constructor of `DataContainer`. We can achieve that via a secret token:

```
[](#cb253-1)const secretToken = Symbol('secretToken');
[](#cb253-2)class DataContainer {
[](#cb253-3)  #data;
[](#cb253-4)  static async create() {
[](#cb253-5)    const data = await Promise.resolve('downloaded');
[](#cb253-6)    return new this(secretToken, data);
[](#cb253-7)  }
[](#cb253-8)  constructor(token, data) {
[](#cb253-9)    if (token !== secretToken) {
[](#cb253-10)      throw new Error('Constructor is private');
[](#cb253-11)    }
[](#cb253-12)    this.#data = data;
[](#cb253-13)  }
[](#cb253-14)  getData() {
[](#cb253-15)    return 'DATA: '+this.#data;
[](#cb253-16)  }
[](#cb253-17)}
[](#cb253-18)DataContainer.create()
[](#cb253-19)  .then(dc => assert.equal(
[](#cb253-20)    dc.getData(), 'DATA: downloaded'));
```

If `secretToken` and `DataContainer` reside in the same module and only the latter is exported, then outside parties don’t have access to `secretToken` and therefore can’t create instances of `DataContainer`.

Pros and cons:

*   Benefit: safe and straightforward.
*   Disadvantage: slightly verbose.

### 13.3.2 Improvement: constructor throws, factory method borrows the class prototype

The following variant of our solution disables the constructor of `DataContainer` and uses a trick to create instances of it another way (line A):

```
[](#cb254-1)class DataContainer {
[](#cb254-2)  static async create() {
[](#cb254-3)    const data = await Promise.resolve('downloaded');
[](#cb254-4)    return Object.create(this.prototype)._init(data); // (A)
[](#cb254-5)  }
[](#cb254-6)  constructor() {
[](#cb254-7)    throw new Error('Constructor is private');
[](#cb254-8)  }
[](#cb254-9)  _init(data) {
[](#cb254-10)    this._data = data;
[](#cb254-11)    return this;
[](#cb254-12)  }
[](#cb254-13)  getData() {
[](#cb254-14)    return 'DATA: '+this._data;
[](#cb254-15)  }
[](#cb254-16)}
[](#cb254-17)DataContainer.create()
[](#cb254-18)  .then(dc => {
[](#cb254-19)    assert.equal(dc instanceof DataContainer, true); // (B)
[](#cb254-20)    assert.equal(
[](#cb254-21)      dc.getData(), 'DATA: downloaded');
[](#cb254-22)  });
```

Internally, an instance of `DataContainer` is any object whose prototype is `DataContainer.prototype`. That’s why we can create instances via `Object.create()` (line A) and that’s why `instanceof` works in line B.

Pros and cons:

*   Benefit: elegant; `instanceof` works.
*   Disadvantages:
    *   Creating instances is not completely prevented. To be fair, though, the work-around via `Object.create()` can also be used for our previous solutions.
    *   We can’t use [private fields](https://2ality.com/2019/07/private-class-fields.html) and [private methods](https://2ality.com/2019/07/private-methods-accessors-in-classes.html) in `DataContainer`, because those are only set up correctly for instances that were created via the constructor.

### 13.3.3 Improvement: instances are inactive by default, activated by factory method

Another, more verbose variant is that, by default, instances are switched off via the flag `.#active`. The initialization method `.#init()` that switches them on cannot be accessed externally, but `Data.container()` can invoke it:

```
[](#cb255-1)class DataContainer {
[](#cb255-2)  #data;
[](#cb255-3)  static async create() {
[](#cb255-4)    const data = await Promise.resolve('downloaded');
[](#cb255-5)    return new this().#init(data);
[](#cb255-6)  }
[](#cb255-7)
[](#cb255-8)  #active = false;
[](#cb255-9)  constructor() {
[](#cb255-10)  }
[](#cb255-11)  #init(data) {
[](#cb255-12)    this.#active = true;
[](#cb255-13)    this.#data = data;
[](#cb255-14)    return this;
[](#cb255-15)  }
[](#cb255-16)  getData() {
[](#cb255-17)    this.#check();
[](#cb255-18)    return 'DATA: '+this.#data;
[](#cb255-19)  }
[](#cb255-20)  #check() {
[](#cb255-21)    if (!this.#active) {
[](#cb255-22)      throw new Error('Not created by factory');
[](#cb255-23)    }
[](#cb255-24)  }
[](#cb255-25)}
[](#cb255-26)DataContainer.create()
[](#cb255-27)  .then(dc => assert.equal(
[](#cb255-28)    dc.getData(), 'DATA: downloaded'));
```

The flag `.#active` is enforced via the private method `.#check()` which must be invoked at the beginning of every method.

The major downside of this solution is its verbosity. There is also a risk of forgetting to invoke `.#check()` in each method.

### 13.3.4 Variant: separate factory function

For completeness sake, I’ll show another variant: Instead of using a static method as a factory you can also use a separate stand-alone function.

```
[](#cb256-1)const secretToken = Symbol('secretToken');
[](#cb256-2)class DataContainer {
[](#cb256-3)  #data;
[](#cb256-4)  constructor(token, data) {
[](#cb256-5)    if (token !== secretToken) {
[](#cb256-6)      throw new Error('Constructor is private');
[](#cb256-7)    }
[](#cb256-8)    this.#data = data;
[](#cb256-9)  }
[](#cb256-10)  getData() {
[](#cb256-11)    return 'DATA: '+this.#data;
[](#cb256-12)  }
[](#cb256-13)}
[](#cb256-14)
[](#cb256-15)async function createDataContainer() {
[](#cb256-16)  const data = await Promise.resolve('downloaded');
[](#cb256-17)  return new DataContainer(secretToken, data);
[](#cb256-18)}
[](#cb256-19)
[](#cb256-20)createDataContainer()
[](#cb256-21)  .then(dc => assert.equal(
[](#cb256-22)    dc.getData(), 'DATA: downloaded'));
```

Stand-alone functions as factories are occasionally useful, but in this case, I prefer a static method:

*   The stand-alone function can’t access private members of `DataContainer`.
*   I prefer the way `DataContainer.create()` looks.

## 13.4 Subclassing a Promise-based constructor (optional)

In general, subclassing is something to use sparingly.

With a separate factory function, it is relatively easy to extend `DataContainer`.

Alas, extending the class with the Promise-based constructor leads to severe limitations. In the following example, we subclass `DataContainer`. The subclass `SubDataContainer` has its own private field `.#moreData` that it initializes asynchronously by hooking into the Promise returned by the constructor of its superclass.

```
[](#cb257-1)class DataContainer {
[](#cb257-2)  #data;
[](#cb257-3)  constructor() {
[](#cb257-4)    return Promise.resolve('downloaded')
[](#cb257-5)      .then(data => {
[](#cb257-6)        this.#data = data;
[](#cb257-7)        return this; // (A)
[](#cb257-8)      });
[](#cb257-9)  }
[](#cb257-10)  getData() {
[](#cb257-11)    return 'DATA: '+this.#data;
[](#cb257-12)  }
[](#cb257-13)}
[](#cb257-14)
[](#cb257-15)class SubDataContainer extends DataContainer {
[](#cb257-16)  #moreData;
[](#cb257-17)  constructor() {
[](#cb257-18)    super();
[](#cb257-19)    const promise = this;
[](#cb257-20)    return promise
[](#cb257-21)      .then(_this => {
[](#cb257-22)        return Promise.resolve('more')
[](#cb257-23)          .then(moreData => {
[](#cb257-24)            _this.#moreData = moreData;
[](#cb257-25)            return _this;
[](#cb257-26)          });
[](#cb257-27)      });
[](#cb257-28)  }
[](#cb257-29)  getData() {
[](#cb257-30)    return super.getData() + ', ' + this.#moreData;
[](#cb257-31)  }
[](#cb257-32)}
```

Alas, we can’t instantiate this class:

```
[](#cb258-1)assert.rejects(
[](#cb258-2)  () => new SubDataContainer(),
[](#cb258-3)  {
[](#cb258-4)    name: 'TypeError',
[](#cb258-5)    message: 'Cannot write private member #moreData ' +
[](#cb258-6)      'to an object whose class did not declare it',
[](#cb258-7)  }
[](#cb258-8));
```

Why the failure? A constructor always adds its private fields to its `this`. However, here, `this` in the subconstructor is the Promise returned by the superconstructor (and not the instance of `SubDataContainer` delivered via the Promise).

However, this approach still works if `SubDataContainer` does not have any private fields.

## 13.5 Conclusion

For the scenario examined in this chapter, I prefer either a Promise-based constructor or a static factory method plus a private constructor via a secret token.

However, the other techniques presented here can still be useful in other scenarios.

## 13.6 Further reading

*   Asynchronous programming:
    *   [Chapter “Promises for asynchronous programming”](https://exploringjs.com/impatient-js/ch_promises.html) in “JavaScript for impatient programmers”
    *   [Chapter “Async functions”](https://exploringjs.com/impatient-js/ch_async-functions.html) in “JavaScript for impatient programmers”
    *   [Section “Immediately invoked async arrow functions”](https://exploringjs.com/impatient-js/ch_async-functions.html#immediately-invoked-async-arrow-functions) in “JavaScript for impatient programmers”
*   OOP:
    *   [Chapter “Prototype chains and classes”](https://exploringjs.com/impatient-js/ch_proto-chains-classes.html) in “JavaScript for impatient programmers”
    *   [Blog post “ES proposal: private class fields”](https://2ality.com/2019/07/private-class-fields.html)
    *   [Blog post “ES proposal: private methods and accessors in JavaScript classes”](https://2ality.com/2019/07/private-methods-accessors-in-classes.html)

# 14 Copying instances of classes: `.clone()` vs. copy constructors

* * *

*   14.1 [`.clone()` methods](#ch015.xhtml_clone-methods)
*   14.2 [Static factory methods](#ch015.xhtml_static-factory-methods)
*   14.3 [Acknowledgements](#ch015.xhtml_acknowledgements)

* * *

In this chapter, we look at two techniques for implementing copying for class instances:

*   `.clone()` methods
*   So-called *copy constructors*, constructors that receive another instance of the current class and use it to initialize the current instance.

## 14.1 `.clone()` methods

This technique introduces one method `.clone()` per class whose instances are to be copied. It returns a deep copy of `this`. The following example shows three classes that can be cloned.

```
[](#cb259-1)class Point {
[](#cb259-2)  constructor(x, y) {
[](#cb259-3)    this.x = x;
[](#cb259-4)    this.y = y;
[](#cb259-5)  }
[](#cb259-6)  clone() {
[](#cb259-7)    return new Point(this.x, this.y);
[](#cb259-8)  }
[](#cb259-9)}
[](#cb259-10)class Color {
[](#cb259-11)  constructor(name) {
[](#cb259-12)    this.name = name;
[](#cb259-13)  }
[](#cb259-14)  clone() {
[](#cb259-15)    return new Color(this.name);
[](#cb259-16)  }
[](#cb259-17)}
[](#cb259-18)class ColorPoint extends Point {
[](#cb259-19)  constructor(x, y, color) {
[](#cb259-20)    super(x, y);
[](#cb259-21)    this.color = color;
[](#cb259-22)  }
[](#cb259-23)  clone() {
[](#cb259-24)    return new ColorPoint(
[](#cb259-25)      this.x, this.y, this.color.clone()); // (A)
[](#cb259-26)  }
[](#cb259-27)}
```

Line A demonstrates an important aspect of this technique: compound instance property values must also be cloned, recursively.

## 14.2 Static factory methods

A *copy constructor* is a constructor that uses another instance of the current class to set up the current instance. Copy constructors are popular in static languages such as C++ and Java, where you can provide multiple versions of a constructor via *static overloading*. Here, *static* means that the choice which version to use, is made at compile time.

In JavaScript, we must make that decision at runtime and that leads to inelegant code:

```
[](#cb260-1)class Point {
[](#cb260-2)  constructor(...args) {
[](#cb260-3)    if (args[0] instanceof Point) {
[](#cb260-4)      // Copy constructor
[](#cb260-5)      const [other] = args;
[](#cb260-6)      this.x = other.x;
[](#cb260-7)      this.y = other.y;
[](#cb260-8)    } else {
[](#cb260-9)      const [x, y] = args;
[](#cb260-10)      this.x = x;
[](#cb260-11)      this.y = y;
[](#cb260-12)    }
[](#cb260-13)  }
[](#cb260-14)}
```

This is how you’d use this class:

```
[](#cb261-1)const original = new Point(-1, 4);
[](#cb261-2)const copy = new Point(original);
[](#cb261-3)assert.deepEqual(copy, original);
```

*Static factory methods* are an alternative to constructors and work better in this case because we can directly invoke the desired functionality. (Here, *static* means that these factory methods are class methods.)

In the following example, the three classes `Point`, `Color` and `ColorPoint` each have a static factory method `.from()`:

```
[](#cb262-1)class Point {
[](#cb262-2)  constructor(x, y) {
[](#cb262-3)    this.x = x;
[](#cb262-4)    this.y = y;
[](#cb262-5)  }
[](#cb262-6)  static from(other) {
[](#cb262-7)    return new Point(other.x, other.y);
[](#cb262-8)  }
[](#cb262-9)}
[](#cb262-10)class Color {
[](#cb262-11)  constructor(name) {
[](#cb262-12)    this.name = name;
[](#cb262-13)  }
[](#cb262-14)  static from(other) {
[](#cb262-15)    return new Color(other.name);
[](#cb262-16)  }
[](#cb262-17)}
[](#cb262-18)class ColorPoint extends Point {
[](#cb262-19)  constructor(x, y, color) {
[](#cb262-20)    super(x, y);
[](#cb262-21)    this.color = color;
[](#cb262-22)  }
[](#cb262-23)  static from(other) {
[](#cb262-24)    return new ColorPoint(
[](#cb262-25)      other.x, other.y, Color.from(other.color)); // (A)
[](#cb262-26)  }
[](#cb262-27)}
```

In line A, we once again copy recursively.

This is how `ColorPoint.from()` works:

```
[](#cb263-1)const original = new ColorPoint(-1, 4, new Color('red'));
[](#cb263-2)const copy = ColorPoint.from(original);
[](#cb263-3)assert.deepEqual(copy, original);
```

## 14.3 Acknowledgements

*   [Ron Korvig](https://github.com/ronkorving) reminded me to use static factory methods and not overloaded constructors for deep-copying in JavaScript.

# 15 Immutable wrappers for collections

* * *

*   15.1 [Wrapping objects](#ch016.xhtml_wrapping-objects)
    *   15.1.1 [Making collections immutable via wrapping](#ch016.xhtml_making-collections-immutable-via-wrapping)
*   15.2 [An immutable wrapper for Maps](#ch016.xhtml_an-immutable-wrapper-for-maps)
*   15.3 [An immutable wrapper for Arrays](#ch016.xhtml_an-immutable-wrapper-for-arrays)

* * *

An immutable wrapper for a collection makes that collection immutable by wrapping it in a new object. In this chapter, we examine how that works and why it is useful.

## 15.1 Wrapping objects

If there is an object whose interface we’d like to reduce, we can take the following approach:

*   Create a new object that stores the original in a private field. The new object is said to *wrap* the original object. The new object is called *wrapper*, the original object *wrapped object*.
*   The wrapper only forwards some of the method calls it receives to the wrapped object.

This is what wrapping looks like:

```
[](#cb264-1)class Wrapper {
[](#cb264-2)  #wrapped;
[](#cb264-3)  constructor(wrapped) {
[](#cb264-4)    this.#wrapped = wrapped;
[](#cb264-5)  }
[](#cb264-6)  allowedMethod1(...args) {
[](#cb264-7)    return this.#wrapped.allowedMethod1(...args);
[](#cb264-8)  }
[](#cb264-9)  allowedMethod2(...args) {
[](#cb264-10)    return this.#wrapped.allowedMethod2(...args);
[](#cb264-11)  }
[](#cb264-12)}
```

Related software design patterns:

*   Wrapping is related to [the Gang of Four design pattern *Facade*](https://en.wikipedia.org/wiki/Facade_pattern).
*   We used [*forwarding*](https://en.wikipedia.org/wiki/Forwarding_(object-oriented_programming)) to implement [*delegation*](https://en.wikipedia.org/wiki/Delegation_pattern). Delegation means that one object lets another object (the *delegate*) handle some of its work. It is an alternative to inheritance for sharing code.

### 15.1.1 Making collections immutable via wrapping

To make a collection immutable, we can use wrapping and remove all destructive operations from its interface.

One important use case for this technique is an object that has an internal mutable data structure that it wants to export safely without copying it. The export being “live” may also be a goal. The object can achieve its goals by wrapping the internal data structure and making it immutable.

The next two sections showcase immutable wrappers for Maps and Arrays. They both have the following limitations:

*   They are sketches. More work is needed to make them suitable for practical use: Better checks, support for more methods, etc.
*   They work shallowly: Each one makes the wrapped object immutable, but not the data it returns. This could be fixed by wrapping some of the results that are returned by methods.

## 15.2 An immutable wrapper for Maps

Class `ImmutableMapWrapper` produces wrappers for Maps:

```
[](#cb265-1)class ImmutableMapWrapper {
[](#cb265-2)  static _setUpPrototype() {
[](#cb265-3)    // Only forward non-destructive methods to the wrapped Map:
[](#cb265-4)    for (const methodName of ['get', 'has', 'keys', 'size']) {
[](#cb265-5)      ImmutableMapWrapper.prototype[methodName] = function (...args) {
[](#cb265-6)        return this.#wrappedMap[methodName](...args);
[](#cb265-7)      }
[](#cb265-8)    }
[](#cb265-9)  }
[](#cb265-10)
[](#cb265-11)  #wrappedMap;
[](#cb265-12)  constructor(wrappedMap) {
[](#cb265-13)    this.#wrappedMap = wrappedMap;
[](#cb265-14)  }
[](#cb265-15)}
[](#cb265-16)ImmutableMapWrapper._setUpPrototype();
```

The setup of the prototype has to be performed by a static method, because we only have access to the private field `.#wrappedMap` from inside the class.

This is `ImmutableMapWrapper` in action:

```
[](#cb266-1)const map = new Map([[false, 'no'], [true, 'yes']]);
[](#cb266-2)const wrapped = new ImmutableMapWrapper(map);
[](#cb266-3)
[](#cb266-4)// Non-destructive operations work as usual:
[](#cb266-5)assert.equal(
[](#cb266-6)  wrapped.get(true), 'yes');
[](#cb266-7)assert.equal(
[](#cb266-8)  wrapped.has(false), true);
[](#cb266-9)assert.deepEqual(
[](#cb266-10)  [...wrapped.keys()], [false, true]);
[](#cb266-11)
[](#cb266-12)// Destructive operations are not available:
[](#cb266-13)assert.throws(
[](#cb266-14)  () => wrapped.set(false, 'never!'),
[](#cb266-15)  /^TypeError: wrapped.set is not a function$/);
[](#cb266-16)assert.throws(
[](#cb266-17)  () => wrapped.clear(),
[](#cb266-18)  /^TypeError: wrapped.clear is not a function$/);
```

## 15.3 An immutable wrapper for Arrays

For an Array `arr`, normal wrapping is not enough because we need to intercept not just method calls, but also property accesses such as `arr[1] = true`. [JavaScript proxies](https://exploringjs.com/es6/ch_proxies.html) enable us to do this:

```
[](#cb267-1)const RE_INDEX_PROP_KEY = /^[0-9]+$/;
[](#cb267-2)const ALLOWED_PROPERTIES = new Set([
[](#cb267-3)  'length', 'constructor', 'slice', 'concat']);
[](#cb267-4)
[](#cb267-5)function wrapArrayImmutably(arr) {
[](#cb267-6)  const handler = {
[](#cb267-7)    get(target, propKey, receiver) {
[](#cb267-8)      // We assume that propKey is a string (not a symbol)
[](#cb267-9)      if (RE_INDEX_PROP_KEY.test(propKey) // simplified check!
[](#cb267-10)        || ALLOWED_PROPERTIES.has(propKey)) {
[](#cb267-11)          return Reflect.get(target, propKey, receiver);
[](#cb267-12)      }
[](#cb267-13)      throw new TypeError(`Property "${propKey}" can’t be accessed`);
[](#cb267-14)    },
[](#cb267-15)    set(target, propKey, value, receiver) {
[](#cb267-16)      throw new TypeError('Setting is not allowed');
[](#cb267-17)    },
[](#cb267-18)    deleteProperty(target, propKey) {
[](#cb267-19)      throw new TypeError('Deleting is not allowed');
[](#cb267-20)    },
[](#cb267-21)  };
[](#cb267-22)  return new Proxy(arr, handler);
[](#cb267-23)}
```

Let’s wrap an Array:

```
[](#cb268-1)const arr = ['a', 'b', 'c'];
[](#cb268-2)const wrapped = wrapArrayImmutably(arr);
[](#cb268-3)
[](#cb268-4)// Non-destructive operations are allowed:
[](#cb268-5)assert.deepEqual(
[](#cb268-6)  wrapped.slice(1), ['b', 'c']);
[](#cb268-7)assert.equal(
[](#cb268-8)  wrapped[1], 'b');
[](#cb268-9)
[](#cb268-10)// Destructive operations are not allowed:
[](#cb268-11)assert.throws(
[](#cb268-12)  () => wrapped[1] = 'x',
[](#cb268-13)  /^TypeError: Setting is not allowed$/);
[](#cb268-14)assert.throws(
[](#cb268-15)  () => wrapped.shift(),
[](#cb268-16)  /^TypeError: Property "shift" can’t be accessed$/);
```

# 16 Regular expressions: lookaround assertions by example

* * *

*   16.1 [Cheat sheet: lookaround assertions](#ch017.xhtml_cheat-sheet-lookaround-assertions)
*   16.2 [Warnings for this chapter](#ch017.xhtml_warnings-for-this-chapter)
*   16.3 [Example: Specifying what comes before or after a match (positive lookaround)](#ch017.xhtml_example-specifying-what-comes-before-or-after-a-match-positive-lookaround)
*   16.4 [Example: Specifying what does not come before or after a match (negative lookaround)](#ch017.xhtml_example-specifying-what-does-not-come-before-or-after-a-match-negative-lookaround)
    *   16.4.1 [There are no simple alternatives to negative lookaround assertions](#ch017.xhtml_there-are-no-simple-alternatives-to-negative-lookaround-assertions)
*   16.5 [Interlude: pointing lookaround assertions inward](#ch017.xhtml_interlude-pointing-lookaround-assertions-inward)
*   16.6 [Example: match strings not starting with `'abc'`](#ch017.xhtml_example-match-strings-not-starting-with-abc)
*   16.7 [Example: match substrings that do not contain `'.mjs'`](#ch017.xhtml_example-match-substrings-that-do-not-contain-.mjs)
*   16.8 [Example: skipping lines with comments](#ch017.xhtml_example-skipping-lines-with-comments)
*   16.9 [Example: smart quotes](#ch017.xhtml_example-smart-quotes)
    *   16.9.1 [Supporting escaping via backslashes](#ch017.xhtml_supporting-escaping-via-backslashes)
*   16.10 [Acknowledgements](#ch017.xhtml_acknowledgements-1)
*   16.11 [Further reading](#ch017.xhtml_further-reading-4)

* * *

In this chapter we use examples to explore lookaround assertions in regular expressions. A lookaround assertion is non-capturing and must match (or not match) what comes before (or after) the current location in the input string.

## 16.1 Cheat sheet: lookaround assertions

Table 4: Overview of available lookaround assertions.

| Pattern | Name |  |
| --- | --- | --- |
| `(?=«pattern»)` | Positive lookahead | ES3 |
| `(?!«pattern»)` | Negative lookahead | ES3 |
| `(?<=«pattern»)` | Positive lookbehind | ES2018 |
| `(?<!«pattern»)` | Negative lookbehind | ES2018 |

There are four lookaround assertions (tbl. [4](#ch017.xhtml_tbl:lookaround-assertions-overview))

*   Lookahead assertions (ECMAScript 3):
    *   Positive lookahead: `(?=«pattern»)` matches if `pattern` matches what comes after the current location in the input string.
    *   Negative lookahead: `(?!«pattern»)` matches if `pattern` does not match what comes after the current location in the input string.
*   Lookbehind assertions (ECMAScript 2018):
    *   Positive lookbehind: `(?<=«pattern»)` matches if `pattern` matches what comes before the current location in the input string.
    *   Negative lookbehind: `(?<!«pattern»)` matches if `pattern` does not match what comes before the current location in the input string.

## 16.2 Warnings for this chapter

*   The examples show what can be achieved via lookaround assertions. However, regular expression aren’t always the best solution. Another technique, such as proper parsing, may be a better choice.

*   Lookbehind assertions are a relatively new feature that may not be supported by all JavaScript engines you are targeting.

*   Lookaround assertions may affect performance negatively, especially if their patterns match long strings.

## 16.3 Example: Specifying what comes before or after a match (positive lookaround)

In the following interaction, we extract quoted words:

```
> 'how "are" "you" doing'.match(/(?<=")[a-z]+(?=")/g)
[ 'are', 'you' ]
```

Two lookaround assertions help us here:

*   `(?<=")` “must be preceded by a quote”
*   `(?=")` “must be followed by a quote”

Lookaround assertions are especially convenient for `.match()` in `/g` mode, which returns whole matches (capture group 0). Whatever the pattern of a lookaround assertion matches is not captured. Without lookaround assertions, the quotes show up in the result:

```
> 'how "are" "you" doing'.match(/"([a-z]+)"/g)
[ '"are"', '"you"' ]
```

## 16.4 Example: Specifying what does not come before or after a match (negative lookaround)

How can we achieve the opposite of what we did in the previous section and extract all unquoted words from a string?

*   Input: `'how "are" "you" doing'`
*   Output: `['how', 'doing']`

Our first attempt is to simply convert positive lookaround assertions to negative lookaround assertions. Alas, that fails:

```
> 'how "are" "you" doing'.match(/(?<!")[a-z]+(?!")/g)
[ 'how', 'r', 'o', 'doing' ]
```

The problem is that we extract sequences of characters that are not bracketed by quotes. That means that in the string `'"are"'`, the “r” in the middle is considered unquoted, because it is preceded by an “a” and followed by an “e”.

We can fix this by stating that prefix and suffix must be neither quote nor letter:

```
> 'how "are" "you" doing'.match(/(?<!["a-z])[a-z]+(?!["a-z])/g)
[ 'how', 'doing' ]
```

Another solution is to demand via `\b` that the sequence of characters `[a-z]+` start and end at word boundaries:

```
> 'how "are" "you" doing'.match(/(?<!")\b[a-z]+\b(?!")/g)
[ 'how', 'doing' ]
```

One thing that is nice about negative lookbehind and negative lookahead is that they also work at the beginning or end, respectively, of a string – as demonstrated in the example.

### 16.4.1 There are no simple alternatives to negative lookaround assertions

Negative lookaround assertions are a powerful tool and usually impossible to emulate via other regular expression means.

If we don’t want to use them, we normally have to take a completely different approach. For example, in this case, we could split the string into (quoted and unquoted) words and then filter those:

```
[](#cb274-1)const str = 'how "are" "you" doing';
[](#cb274-2)
[](#cb274-3)const allWords = str.match(/"?[a-z]+"?/g);
[](#cb274-4)const unquotedWords = allWords.filter(
[](#cb274-5)  w => !w.startsWith('"') || !w.endsWith('"'));
[](#cb274-6)assert.deepEqual(unquotedWords, ['how', 'doing']);
```

Benefits of this approach:

*   It works on older engines.
*   It is easy to understand.

## 16.5 Interlude: pointing lookaround assertions inward

All of the examples we have seen so far have in common that the lookaround assertions dictate what must come before or after the match but without including those characters in the match.

The regular expressions shown in the remainder of this chapter are different: Their lookaround assertions point inward and restrict what’s inside the match.

## 16.6 Example: match strings not starting with `'abc'`

Let‘s assume we want to match all strings that do not start with `'abc'`. Our first attempt could be the regular expression `/^(?!abc)/`.

That works well for `.test()`:

```
> /^(?!abc)/.test('xyz')
true
```

However, `.exec()` gives us an empty string:

```
> /^(?!abc)/.exec('xyz')
{ 0: '', index: 0, input: 'xyz', groups: undefined }
```

The problem is that assertions such as lookaround assertions don’t expand the matched text. That is, they don’t capture input characters, they only make demands about the current location in the input.

Therefore, the solution is to add a pattern that does capture input characters:

```
> /^(?!abc).*$/.exec('xyz')
{ 0: 'xyz', index: 0, input: 'xyz', groups: undefined }
```

As desired, this new regular expression rejects strings that are prefixed with `'abc'`:

```
> /^(?!abc).*$/.exec('abc')
null
> /^(?!abc).*$/.exec('abcd')
null
```

And it accepts strings that don’t have the full prefix:

```
> /^(?!abc).*$/.exec('ab')
{ 0: 'ab', index: 0, input: 'ab', groups: undefined }
```

## 16.7 Example: match substrings that do not contain `'.mjs'`

In the following example, we want to find

```
import ··· from '«module-specifier»';
```

where `module-specifier` does not end with `'.mjs'`.

```
[](#cb281-1)const code = `
[](#cb281-2)import {transform} from './util';
[](#cb281-3)import {Person} from './person.mjs';
[](#cb281-4)import {zip} from 'lodash';
[](#cb281-5)`.trim();
[](#cb281-6)assert.deepEqual(
[](#cb281-7)  code.match(/^import .*? from '[^']+(?<!\.mjs)';$/umg),
[](#cb281-8)  [
[](#cb281-9)    "import {transform} from './util';",
[](#cb281-10)    "import {zip} from 'lodash';",
[](#cb281-11)  ]);
```

Here, the lookbehind assertion `(?<!\.mjs)` acts as a *guard* and prevents that the regular expression matches strings that contain `'.mjs`’ at this location.

## 16.8 Example: skipping lines with comments

Scenario: We want to parse lines with settings, while skipping comments. For example:

```
[](#cb282-1)const RE_SETTING = /^(?!#)([^:]*):(.*)$/
[](#cb282-2)
[](#cb282-3)const lines = [
[](#cb282-4)  'indent: 2', // setting
[](#cb282-5)  '# Trim trailing whitespace:', // comment
[](#cb282-6)  'whitespace: trim', // setting
[](#cb282-7)];
[](#cb282-8)for (const line of lines) {
[](#cb282-9)  const match = RE_SETTING.exec(line);
[](#cb282-10)  if (match) {
[](#cb282-11)    const key = JSON.stringify(match[1]);
[](#cb282-12)    const value = JSON.stringify(match[2]);
[](#cb282-13)    console.log(`KEY: ${key} VALUE: ${value}`);
[](#cb282-14)  }
[](#cb282-15)}
[](#cb282-16)
[](#cb282-17)// Output:
[](#cb282-18)// 'KEY: "indent" VALUE: " 2"'
[](#cb282-19)// 'KEY: "whitespace" VALUE: " trim"'
```

How did we arrive at the regular expression `RE_SETTING`?

We started with the following regular expression for settings:

```
[](#cb283-1)/^([^:]*):(.*)$/
```

Intuitively, it is a sequence of the following parts:

*   Start of the line
*   Non-colons (zero or more)
*   A single colon
*   Any characters (zero or more)
*   The end of line

This regular expression does reject *some* comments:

```
> /^([^:]*):(.*)$/.test('# Comment')
false
```

But it accepts others (that have colons in them):

```
> /^([^:]*):(.*)$/.test('# Comment:')
true
```

We can fix that by prefixing `(?!#)` as a guard. Intuitively, it means: ”The current location in the input string must not be followed by the character `#`.”

The new regular expression works as desired:

```
> /^(?!#)([^:]*):(.*)$/.test('# Comment:')
false
```

## 16.9 Example: smart quotes

Let’s assume we want to convert pairs of straight double quotes to curly quotes:

*   Input: `` `"yes" and "no"` ``
*   Output: `` `“yes” and “no”` ``

This is our first attempt:

```
> `The words "must" and "should".`.replace(/"(.*)"/g, '“$1”')
'The words “must" and "should”.'
```

Only the first quote and the last quote is curly. The problem here is that the `*` quantifier matches [*greedily*](https://exploringjs.com/impatient-js/ch_regexps.html#quantifiers) (as much as possible).

If we put a question mark after the `*`, it matches *reluctantly*:

```
> `The words "must" and "should".`.replace(/"(.*?)"/g, '“$1”')
'The words “must” and “should”.'
```

### 16.9.1 Supporting escaping via backslashes

What if we want to allow the escaping of quotes via backslashes? We can do that by using the guard `(?<!\\)` before the quotes:

```
> const regExp = /(?<!\\)"(.*?)(?<!\\)"/g;
> String.raw`\"straight\" and "curly"`.replace(regExp, '“$1”')
'\\"straight\\" and “curly”'
```

As a post-processing step, we would still need to do:

```
[](#cb290-1).replace(/\\"/g, `"`)
```

However, this regular expression can fail when there is a backslash-escaped backslash:

```
> String.raw`Backslash: "\\"`.replace(/(?<!\\)"(.*?)(?<!\\)"/g, '“$1”')
'Backslash: "\\\\"'
```

The second backslash prevented the quotes from becoming curly.

We can fix that if we make our guard more sophisticated (`?:` makes the group non-capturing):

```
[](#cb292-1)(?<=[^\\](?:\\\\)*)
```

The new guard allows pairs of backslashes before quotes:

```
> const regExp = /(?<=[^\\](?:\\\\)*)"(.*?)(?<=[^\\](?:\\\\)*)"/g;
> String.raw`Backslash: "\\"`.replace(regExp, '“$1”')
'Backslash: “\\\\”'
```

One issue remains. This guard prevents the first quote from being matched if it appears at the beginning of a string:

```
> const regExp = /(?<=[^\\](?:\\\\)*)"(.*?)(?<=[^\\](?:\\\\)*)"/g;
> `"abc"`.replace(regExp, '“$1”')
'"abc"'
```

We can fix that by changing the first guard to: `(?<=[^\\](?:\\\\)*|^)`

```
> const regExp = /(?<=[^\\](?:\\\\)*|^)"(.*?)(?<=[^\\](?:\\\\)*)"/g;
> `"abc"`.replace(regExp, '“$1”')
'“abc”'
```

## 16.10 Acknowledgements

*   The first regular expression that handles escaped backslashes in front of quotes [was proposed by `@jonasraoni` on Twitter](https://twitter.com/jonasraoni/status/992506010454683650).

## 16.11 Further reading

*   [Chapter “Regular expressions (`RegExp`)”](https://exploringjs.com/impatient-js/ch_regexps.html) in “JavaScript for impatient programmers”

# 17 Composing regular expressions via `re-template-tag`

* * *

*   17.1 [The basics](#ch018.xhtml_the-basics)
*   17.2 [A tour of the features](#ch018.xhtml_a-tour-of-the-features)
    *   17.2.1 [Main features](#ch018.xhtml_main-features)
    *   17.2.2 [Details and advanced features](#ch018.xhtml_details-and-advanced-features)
*   17.3 [Why is this useful?](#ch018.xhtml_why-is-this-useful)
*   17.4 [`re` and named capture groups](#ch018.xhtml_re-and-named-capture-groups)

* * *

My small library [`re-template-tag`](https://github.com/rauschma/re-template-tag) provides a template tag function for composing regular expressions. This chapter explains how it works. The intent is to introduce the ideas behind the library (more than the library itself).

## 17.1 The basics

The library implements the template tag `re` for regular expressions.

Installation:

```
npm install re-template-tag
```

Importing:

```
[](#cb297-1)import {re} from 're-template-tag';
```

Use: The following two expressions produce the same regular expression.

```
[](#cb298-1)assert.deepEqual(
[](#cb298-2)  re`/abc/gu`,
[](#cb298-3)  /abc/gu);
```

## 17.2 A tour of the features

[The unit tests](https://github.com/rauschma/re-template-tag/blob/master/test/index_test.js) are a good tour of the features of re-template-tag.

### 17.2.1 Main features

You can use `re` to assemble a regular expression from fragments:

```
[](#cb299-1)const RE_YEAR = /([0-9]{4})/;
[](#cb299-2)const RE_MONTH = /([0-9]{2})/;
[](#cb299-3)const RE_DAY = /([0-9]{2})/;
[](#cb299-4)const RE_DATE = re`/^${RE_YEAR}-${RE_MONTH}-${RE_DAY}$/u`;
[](#cb299-5)assert.equal(RE_DATE.source, '^([0-9]{4})-([0-9]{2})-([0-9]{2})$');
```

Any strings you insert are escaped properly:

```
[](#cb300-1)assert.equal(re`/-${'.'}-/u`.source, '-\\.-');
```

Flag-less mode:

```
[](#cb301-1)const regexp = re`abc`;
[](#cb301-2)assert.ok(regexp instanceof RegExp);
[](#cb301-3)assert.equal(regexp.source, 'abc');
[](#cb301-4)assert.equal(regexp.flags, '');
```

### 17.2.2 Details and advanced features

You can use the backslash as you would inside regular expression literals:

```
[](#cb302-1)assert.equal(re`/\./u`.source, '\\.');
```

Regular expression flags (such as `/u` in the previous example) can also be computed:

```
[](#cb303-1)const regexp = re`/abc/${'g'+'u'}`;
[](#cb303-2)assert.ok(regexp instanceof RegExp);
[](#cb303-3)assert.equal(regexp.source, 'abc');
[](#cb303-4)assert.equal(regexp.flags, 'gu');
```

## 17.3 Why is this useful?

*   You can compose regular expressions from fragments and document the fragments via comments. That makes regular expressions easier to understand.
*   You can define constants for regular expression fragments and reuse them.
*   You can define plain text constants via strings and insert them into regular expressions and they are escaped as necessary.

## 17.4 `re` and named capture groups

`re` profits from [named capture groups](https://exploringjs.com/impatient-js/ch_regexps.html#named-capture-groups) because they make the fragments more independent.

Without named groups:

```
[](#cb304-1)const RE_YEAR = /([0-9]{4})/;
[](#cb304-2)const RE_MONTH = /([0-9]{2})/;
[](#cb304-3)const RE_DAY = /([0-9]{2})/;
[](#cb304-4)const RE_DATE = re`/^${RE_YEAR}-${RE_MONTH}-${RE_DAY}$/u`;
[](#cb304-5)
[](#cb304-6)const match = RE_DATE.exec('2017-01-27');
[](#cb304-7)assert.equal(match[1], '2017');
```

With named groups:

```
[](#cb305-1)const RE_YEAR = re`(?<year>[0-9]{4})`;
[](#cb305-2)const RE_MONTH = re`(?<month>[0-9]{2})`;
[](#cb305-3)const RE_DAY = re`(?<day>[0-9]{2})`;
[](#cb305-4)const RE_DATE = re`/${RE_YEAR}-${RE_MONTH}-${RE_DAY}/u`;
[](#cb305-5)
[](#cb305-6)const match = RE_DATE.exec('2017-01-27');
[](#cb305-7)assert.equal(match.groups.year, '2017');
```

# 18 Exploring Promises by implementing them

* * *

*   18.1 [Refresher: states of Promises](#ch019.xhtml_refresher-states-of-promises)
*   18.2 [Version 1: Stand-alone Promise](#ch019.xhtml_version-1-stand-alone-promise)
    *   18.2.1 [Method `.then()`](#ch019.xhtml_method-.then)
    *   18.2.2 [Method `.resolve()`](#ch019.xhtml_method-.resolve)
*   18.3 [Version 2: Chaining `.then()` calls](#ch019.xhtml_version-2-chaining-.then-calls)
*   18.4 [Convenience method `.catch()`](#ch019.xhtml_convenience-method-.catch)
*   18.5 [Omitting reactions](#ch019.xhtml_omitting-reactions)
*   18.6 [The implementation](#ch019.xhtml_the-implementation)
*   18.7 [Version 3: Flattening Promises returned from `.then()` callbacks](#ch019.xhtml_version-3-flattening-promises-returned-from-.then-callbacks)
    *   18.7.1 [Returning Promises from a callback of `.then()`](#ch019.xhtml_returning-promises-from-a-callback-of-.then)
    *   18.7.2 [Flattening makes Promise states more complicated](#ch019.xhtml_flattening-makes-promise-states-more-complicated)
    *   18.7.3 [Implementing Promise-flattening](#ch019.xhtml_implementing-promise-flattening)
*   18.8 [Version 4: Exceptions thrown in reaction callbacks](#ch019.xhtml_version-4-exceptions-thrown-in-reaction-callbacks)
*   18.9 [Version 5: Revealing constructor pattern](#ch019.xhtml_version-5-revealing-constructor-pattern)

* * *

![](media/file1.svg)  **Required knowledge: Promises**

For this chapter, you should be roughly familiar with Promises, but much relevant knowledge is also reviewed here. If necessary, you can read [the chapter on Promises in “JavaScript for impatient programmers”](https://exploringjs.com/impatient-js/ch_promises.html).

In this chapter, we will approach Promises from a different angle: Instead of using this API, we will create a simple implementation of it. This different angle once helped me greatly with making sense of Promises.

The Promise implementation is the class `ToyPromise`. In order to be easier to understand, it doesn’t completely match the API. But it is close enough to still give us much insight into how Promises work.

![](media/file1.svg)  **Repository with code**

`ToyPromise` is available on GitHub, in the repository [`toy-promise`](https://github.com/rauschma/toy-promise).

## 18.1 Refresher: states of Promises

![](media/file9.svg)

Figure 2: The states of a Promise (simplified version): A Promise is initially pending. If we resolve it, it becomes fulfilled. If we reject it, it becomes rejected.

We start with a simplified version of how Promise states work (fig. [2](#ch019.xhtml_fig:promise-states-simple)):

*   A Promise is initially *pending*.
*   If a Promise is *resolved* with a value `v`, it becomes *fulfilled* (later, we’ll see that resolving can also reject). `v` is now the *fulfillment value* of the Promise.
*   If a Promise is *rejected* with an error `e`, it becomes *rejected*. `e` is now the *rejection value* of the Promise.

## 18.2 Version 1: Stand-alone Promise

Our first implementation is a stand-alone Promise with minimal functionality:

*   We can create a Promise.
*   We can resolve or reject a Promise and we can only do it once.
*   We can register *reactions* (callbacks) via `.then()`. Registering must do the right thing independently of whether the Promise has already been settled or not.
*   `.then()` does not support chaining, yet – it does not return anything.

`ToyPromise1` is a class with three prototype methods:

*   `ToyPromise1.prototype.resolve(value)`
*   `ToyPromise1.prototype.reject(reason)`
*   `ToyPromise1.prototype.then(onFulfilled, onRejected)`

That is, `resolve` and `reject` are methods (and not functions handed to a callback parameter of the constructor).

This is how this first implementation is used:

```
[](#cb306-1)// .resolve() before .then()
[](#cb306-2)const tp1 = new ToyPromise1();
[](#cb306-3)tp1.resolve('abc');
[](#cb306-4)tp1.then((value) => {
[](#cb306-5)  assert.equal(value, 'abc');
[](#cb306-6)});
```

```
[](#cb307-1)// .then() before .resolve()
[](#cb307-2)const tp2 = new ToyPromise1();
[](#cb307-3)tp2.then((value) => {
[](#cb307-4)  assert.equal(value, 'def');
[](#cb307-5)});
[](#cb307-6)tp2.resolve('def');
```

Fig. [3](#ch019.xhtml_fig:promise-impl1-simple) illustrates how our first `ToyPromise` works.

![](media/file0.svg)  **The diagrams of the data flow in Promises are optional**

The motivation for the diagrams is to have a visual explanation for how Promises work. But they are optional. If you find them confusing, you can ignore them and focus on the code.

![](media/file10.svg)

Figure 3: `ToyPromise1`: If a Promise is resolved, the provided value is passed on to the *fulfillment reactions* (first arguments of `.then()`). If a Promise is rejected, the provided value is passed on to the *rejection reactions* (second arguments of `.then()`).

### 18.2.1 Method `.then()`

Let’s examine `.then()` first. It has to handle two cases:

*   If the Promise is still pending, it queues invocations of `onFulfilled` and `onRejected`. They are to be used later, when the Promise is settled.
*   If the Promise is already fulfilled or rejected, `onFulfilled` or `onRejected` can be invoked right away.

```
[](#cb308-1)then(onFulfilled, onRejected) {
[](#cb308-2)  const fulfillmentTask = () => {
[](#cb308-3)    if (typeof onFulfilled === 'function') {
[](#cb308-4)      onFulfilled(this._promiseResult);
[](#cb308-5)    }
[](#cb308-6)  };
[](#cb308-7)  const rejectionTask = () => {
[](#cb308-8)    if (typeof onRejected === 'function') {
[](#cb308-9)      onRejected(this._promiseResult);
[](#cb308-10)    }
[](#cb308-11)  };
[](#cb308-12)  switch (this._promiseState) {
[](#cb308-13)    case 'pending':
[](#cb308-14)      this._fulfillmentTasks.push(fulfillmentTask);
[](#cb308-15)      this._rejectionTasks.push(rejectionTask);
[](#cb308-16)      break;
[](#cb308-17)    case 'fulfilled':
[](#cb308-18)      addToTaskQueue(fulfillmentTask);
[](#cb308-19)      break;
[](#cb308-20)    case 'rejected':
[](#cb308-21)      addToTaskQueue(rejectionTask);
[](#cb308-22)      break;
[](#cb308-23)    default:
[](#cb308-24)      throw new Error();
[](#cb308-25)  }
[](#cb308-26)}
```

The previous code snippet uses the following helper function:

```
[](#cb309-1)function addToTaskQueue(task) {
[](#cb309-2)  setTimeout(task, 0);
[](#cb309-3)}
```

Promises must always settle asynchronously. That’s why we don’t directly execute tasks, we add them to the task queue of the event loop (of browsers, Node.js, etc.). Note that the real Promise API doesn’t use normal tasks (like `setTimeout()`), it uses [*microtasks*](https://jakearchibald.com/2015/tasks-microtasks-queues-and-schedules/), which are tightly coupled with the current normal task and always execute directly after it.

### 18.2.2 Method `.resolve()`

`.resolve()` works as follows: If the Promise is already settled, it does nothing (ensuring that a Promise can only be settled once). Otherwise, the state of the Promise changes to `'fulfilled'` and the result is cached in `this.promiseResult`. Next, all fulfillment reactions that have been enqueued so far, are invoked.

```
[](#cb310-1)resolve(value) {
[](#cb310-2)  if (this._promiseState !== 'pending') return this;
[](#cb310-3)  this._promiseState = 'fulfilled';
[](#cb310-4)  this._promiseResult = value;
[](#cb310-5)  this._clearAndEnqueueTasks(this._fulfillmentTasks);
[](#cb310-6)  return this; // enable chaining
[](#cb310-7)}
```

```
[](#cb311-1)_clearAndEnqueueTasks(tasks) {
[](#cb311-2)  this._fulfillmentTasks = undefined;
[](#cb311-3)  this._rejectionTasks = undefined;
[](#cb311-4)  tasks.map(addToTaskQueue);
[](#cb311-5)}
```

`reject()` is similar to `resolve()`.

## 18.3 Version 2: Chaining `.then()` calls

![](media/file11.svg)

Figure 4: `ToyPromise2` chains `.then()` calls: `.then()` now returns a Promise that is resolved by whatever value is returned by the fulfillment reaction or the rejection reaction.

The next feature we implement is chaining (fig. [4](#ch019.xhtml_fig:promise-impl2-chaining)): A value that we return from a fulfillment reaction or a rejection reaction can be handled by a fulfilment reaction in a following `.then()` call. (In the next version, chaining will become much more useful, due to special support for returning Promises.)

In the following example:

*   First `.then()`: We return a value in a fulfillment reaction.
*   Second `.then()`: We receive that value via a fulfillment reaction.

```
[](#cb312-1)new ToyPromise2()
[](#cb312-2)  .resolve('result1')
[](#cb312-3)  .then(x => {
[](#cb312-4)    assert.equal(x, 'result1');
[](#cb312-5)    return 'result2';
[](#cb312-6)  })
[](#cb312-7)  .then(x => {
[](#cb312-8)    assert.equal(x, 'result2');
[](#cb312-9)  });
```

In the following example:

*   First `.then()`: We return a value in a rejection reaction.
*   Second `.then()`: We receive that value via a fulfillment reaction.

```
[](#cb313-1)new ToyPromise2()
[](#cb313-2)  .reject('error1')
[](#cb313-3)  .then(null,
[](#cb313-4)    x => {
[](#cb313-5)      assert.equal(x, 'error1');
[](#cb313-6)      return 'result2';
[](#cb313-7)    })
[](#cb313-8)  .then(x => {
[](#cb313-9)    assert.equal(x, 'result2');
[](#cb313-10)  });
```

## 18.4 Convenience method `.catch()`

The new version introduces a convenience method `.catch()` that makes it easier to only provide a rejection reaction. Note that only providing a fulfillment reaction is already easy – we simply omit the second parameter of `.then()` (see previous example).

The previous example looks nicer if we use it (line A):

```
[](#cb314-1)new ToyPromise2()
[](#cb314-2)  .reject('error1')
[](#cb314-3)  .catch(x => { // (A)
[](#cb314-4)    assert.equal(x, 'error1');
[](#cb314-5)    return 'result2';
[](#cb314-6)  })
[](#cb314-7)  .then(x => {
[](#cb314-8)    assert.equal(x, 'result2');
[](#cb314-9)  });
```

The following two method invocations are equivalent:

```
[](#cb315-1).catch(rejectionReaction)
[](#cb315-2).then(null, rejectionReaction)
```

This is how `.catch()` is implemented:

```
[](#cb316-1)catch(onRejected) { // [new]
[](#cb316-2)  return this.then(null, onRejected);
[](#cb316-3)}
```

## 18.5 Omitting reactions

The new version also forwards fulfillments if we omit a fulfillment reaction and it forwards rejections if we omit a rejection reaction. Why is that useful?

The following example demonstrates passing on rejections:

```
[](#cb317-1)someAsyncFunction()
[](#cb317-2)  .then(fulfillmentReaction1)
[](#cb317-3)  .then(fulfillmentReaction2)
[](#cb317-4)  .catch(rejectionReaction);
```

`rejectionReaction` can now handle the rejections of `someAsyncFunction()`, `fulfillmentReaction1`, and `fulfillmentReaction2`.

The following example demonstrates passing on fulfillments:

```
[](#cb318-1)someAsyncFunction()
[](#cb318-2)  .catch(rejectionReaction)
[](#cb318-3)  .then(fulfillmentReaction);
```

If `someAsyncFunction()` rejects its Promise, `rejectionReaction` can fix whatever is wrong and return a fulfillment value that is then handled by `fulfillmentReaction`.

If `someAsyncFunction()` fulfills its Promise, `fulfillmentReaction` can also handle it because the `.catch()` is skipped.

## 18.6 The implementation

How is all of this handled under the hood?

*   `.then()` returns a Promise that is resolved with what either `onFulfilled` or `onRejected` return.
*   If `onFulfilled` or `onRejected` are missing, whatever they would have received is passed on to the Promise returned by `.then()`.

Only `.then()` changes:

```
[](#cb319-1)then(onFulfilled, onRejected) {
[](#cb319-2)  const resultPromise = new ToyPromise2(); // [new]
[](#cb319-3)
[](#cb319-4)  const fulfillmentTask = () => {
[](#cb319-5)    if (typeof onFulfilled === 'function') {
[](#cb319-6)      const returned = onFulfilled(this._promiseResult);
[](#cb319-7)      resultPromise.resolve(returned); // [new]
[](#cb319-8)    } else { // [new]
[](#cb319-9)      // `onFulfilled` is missing
[](#cb319-10)      // => we must pass on the fulfillment value
[](#cb319-11)      resultPromise.resolve(this._promiseResult);
[](#cb319-12)    } 
[](#cb319-13)  };
[](#cb319-14)
[](#cb319-15)  const rejectionTask = () => {
[](#cb319-16)    if (typeof onRejected === 'function') {
[](#cb319-17)      const returned = onRejected(this._promiseResult);
[](#cb319-18)      resultPromise.resolve(returned); // [new]
[](#cb319-19)    } else { // [new]
[](#cb319-20)      // `onRejected` is missing
[](#cb319-21)      // => we must pass on the rejection value
[](#cb319-22)      resultPromise.reject(this._promiseResult);
[](#cb319-23)    }
[](#cb319-24)  };
[](#cb319-25)
[](#cb319-26)  ···
[](#cb319-27)
[](#cb319-28)  return resultPromise; // [new]
[](#cb319-29)}
```

`.then()` creates and returns a new Promise (first line and last line of the method). Additionally:

*   `fulfillmentTask` works differently. This is what now happens after fulfillment:
    *   If `onFullfilled` was provided, it is called and its result is used to resolve `resultPromise`.
    *   If `onFulfilled` is missing, we use the fulfillment value of the current Promise to resolve `resultPromise`.
*   `rejectionTask` works differently. This is what now happens after rejection:
    *   If `onRejected` was provided, it is called and its result is used to *resolve* `resultPromise`. Note that `resultPromise` is not rejected: We are assuming that `onRejected()` fixed whatever problem there was.
    *   If `onRejected` is missing, we use the rejection value of the current Promise to reject `resultPromise`.

## 18.7 Version 3: Flattening Promises returned from `.then()` callbacks

### 18.7.1 Returning Promises from a callback of `.then()`

Promise-flattening is mostly about making chaining more convenient: If we want to pass on a value from one `.then()` callback to the next one, we return it in the former. After that, `.then()` puts it into the Promise that it has already returned.

This approach becomes inconvenient if we return a Promise from a `.then()` callback. For example, the result of a Promise-based function (line A):

```
[](#cb320-1)asyncFunc1()
[](#cb320-2).then((result1) => {
[](#cb320-3)  assert.equal(result1, 'Result of asyncFunc1()');
[](#cb320-4)  return asyncFunc2(); // (A)
[](#cb320-5)})
[](#cb320-6).then((result2Promise) => {
[](#cb320-7)  result2Promise
[](#cb320-8)  .then((result2) => { // (B)
[](#cb320-9)    assert.equal(
[](#cb320-10)      result2, 'Result of asyncFunc2()');
[](#cb320-11)  });
[](#cb320-12)});
```

This time, putting the value returned in line A into the Promise returned by `.then()` forces us to unwrap that Promise in line B. It would be nice if instead, the Promise returned in line A replaced the Promise returned by `.then()`. How exactly that could be done is not immediately clear, but if it worked, it would let us write our code like this:

```
[](#cb321-1)asyncFunc1()
[](#cb321-2).then((result1) => {
[](#cb321-3)  assert.equal(result1, 'Result of asyncFunc1()');
[](#cb321-4)  return asyncFunc2(); // (A)
[](#cb321-5)})
[](#cb321-6).then((result2) => {
[](#cb321-7)  // result2 is the fulfillment value, not the Promise
[](#cb321-8)  assert.equal(
[](#cb321-9)    result2, 'Result of asyncFunc2()');
[](#cb321-10)});
```

In line A, we returned a Promise. Thanks to Promise-flattening, `result2` is the fulfillment value of that Promise, not the Promise itself.

### 18.7.2 Flattening makes Promise states more complicated

![](media/file5.svg)  **Flattening Promises in the ECMAScript specification**

In the ECMAScript specification, the details of flattening Promises are described in [section “Promise Objects”](https://tc39.es/ecma262/#sec-promise-objects).

How does the Promise API handle flattening?

If a Promise P is resolved with a Promise Q, then P does not wrap Q, P “becomes” Q: State and settlement value of P are now always the same as Q’s. That helps us with `.then()` because `.then()` resolves the Promise it returns with the value returned by one of its callbacks.

How does P become Q? By *locking in* on Q: P becomes externally unresolvable and a settlement of Q triggers a settlement of P. Lock-in is an additional invisible Promise state that makes states more complicated.

The Promise API has one additional feature: Q doesn’t have to be a Promise, only a so-called *thenable*. A thenable is an object with a method `.then()`. The reason for this added flexibility is to enable different Promise implementations to work together (which mattered when Promises were first added to the language).

Fig. [5](#ch019.xhtml_fig:promise-states-all) visualizes the new states.

![](media/file12.svg)

Figure 5: All states of a Promise: Promise-flattening introduces the invisible pseudo-state “locked-in”. That state is reached if a Promise P is resolved with a thenable Q. Afterwards, state and settlement value of P is always the same as those of Q.

Note that the concept of *resolving* has also become more complicated. Resolving a Promise now only means that it can’t be settled directly, anymore:

*   Resolving may reject a Promise: We can resolve a Promise with a rejected Promise.
*   Resolving may not even settle a Promise: We can resolve a Promise with another one that is always pending.

The ECMAScript specification puts it this way: “An unresolved Promise is always in the pending state. A resolved Promise may be pending, fulfilled, or rejected.”

### 18.7.3 Implementing Promise-flattening

Fig. [6](#ch019.xhtml_fig:promise-impl3-flattening) shows how `ToyPromise3` handles flattening.

![](media/file13.svg)

Figure 6: `ToyPromise3` flattens resolved Promises: If the first Promise is resolved with a thenable `x1`, it locks in on `x1` and is settled with the settlement value of `x1`. If the first Promise is resolved with a non-thenable value, everything works as it did before.

We detect thenables via this function:

```
[](#cb322-1)function isThenable(value) { // [new]
[](#cb322-2)  return typeof value === 'object' && value !== null
[](#cb322-3)    && typeof value.then === 'function';
[](#cb322-4)}
```

To implement lock-in, we introduce a new boolean flag `._alreadyResolved`. Setting it to `true` deactivates `.resolve()` and `.reject()` – for example:

```
[](#cb323-1)resolve(value) { // [new]
[](#cb323-2)  if (this._alreadyResolved) return this;
[](#cb323-3)  this._alreadyResolved = true;
[](#cb323-4)
[](#cb323-5)  if (isThenable(value)) {
[](#cb323-6)    // Forward fulfillments and rejections from `value` to `this`.
[](#cb323-7)    // The callbacks are always executed asynchronously
[](#cb323-8)    value.then(
[](#cb323-9)      (result) => this._doFulfill(result),
[](#cb323-10)      (error) => this._doReject(error));
[](#cb323-11)  } else {
[](#cb323-12)    this._doFulfill(value);
[](#cb323-13)  }
[](#cb323-14)
[](#cb323-15)  return this; // enable chaining
[](#cb323-16)}
```

If `value` is a thenable then we lock the current Promise in on it:

*   If `value` is fulfilled with a result, the current Promise is also fulfilled with that result.
*   If `value` is rejected with an error, the current Promise is also rejected with that error.

The settling is performed via the private methods `._doFulfill()` and `._doReject()`, to get around the protection via `._alreadyResolved`.

`._doFulfill()` is relatively simple:

```
[](#cb324-1)_doFulfill(value) { // [new]
[](#cb324-2)  assert.ok(!isThenable(value));
[](#cb324-3)  this._promiseState = 'fulfilled';
[](#cb324-4)  this._promiseResult = value;
[](#cb324-5)  this._clearAndEnqueueTasks(this._fulfillmentTasks);
[](#cb324-6)}
```

`.reject()` is not shown here. Its only new functionality is that it now also obeys `._alreadyResolved`.

## 18.8 Version 4: Exceptions thrown in reaction callbacks

![](media/file14.svg)

Figure 7: `ToyPromise4` converts exceptions in Promise reactions to rejections of the Promise returned by `.then()`.

As our final feature, we’d like our Promises to handle exceptions in user code as rejections (fig. [7](#ch019.xhtml_fig:promise-impl4-exceptions)). In this chapter, “user code” means the two callback parameters of .`then()`.

```
[](#cb325-1)new ToyPromise4()
[](#cb325-2)  .resolve('a')
[](#cb325-3)  .then((value) => {
[](#cb325-4)    assert.equal(value, 'a');
[](#cb325-5)    throw 'b'; // triggers a rejection
[](#cb325-6)  })
[](#cb325-7)  .catch((error) => {
[](#cb325-8)    assert.equal(error, 'b');
[](#cb325-9)  })
```

`.then()` now runs the Promise reactions `onFulfilled` and `onRejected` safely, via the helper method `._runReactionSafely()` – for example:

```
[](#cb326-1)  const fulfillmentTask = () => {
[](#cb326-2)    if (typeof onFulfilled === 'function') {
[](#cb326-3)      this._runReactionSafely(resultPromise, onFulfilled); // [new]
[](#cb326-4)    } else {
[](#cb326-5)      // `onFulfilled` is missing
[](#cb326-6)      // => we must pass on the fulfillment value
[](#cb326-7)      resultPromise.resolve(this._promiseResult);
[](#cb326-8)    } 
[](#cb326-9)  };
```

`._runReactionSafely()` is implemented as follows:

```
[](#cb327-1)_runReactionSafely(resultPromise, reaction) { // [new]
[](#cb327-2)  try {
[](#cb327-3)    const returned = reaction(this._promiseResult);
[](#cb327-4)    resultPromise.resolve(returned);
[](#cb327-5)  } catch (e) {
[](#cb327-6)    resultPromise.reject(e);
[](#cb327-7)  }
[](#cb327-8)}
```

## 18.9 Version 5: Revealing constructor pattern

We are skipping one last step: If we wanted to turn `ToyPromise` into an actual Promise implementation, we’d still need to implement [the revealing constructor pattern](https://blog.domenic.me/the-revealing-constructor-pattern/): JavaScript Promises are not resolved and rejected via methods, but via functions that are handed to the *executor*, the callback parameter of the constructor.

```
[](#cb328-1)const promise = new Promise(
[](#cb328-2)  (resolve, reject) => { // executor
[](#cb328-3)    // ···
[](#cb328-4)  });
```

If the executor throws an exception, then `promise` is rejected.

# 19 The property `.name` of functions

* * *

*   19.1 [Names of functions](#ch020.xhtml_names-of-functions)
    *   19.1.1 [Function names are used in stack traces](#ch020.xhtml_function-names-are-used-in-stack-traces)
*   19.2 [Constructs that provide names for functions](#ch020.xhtml_constructs-that-provide-names-for-functions)
    *   19.2.1 [Function declarations](#ch020.xhtml_function-declarations)
    *   19.2.2 [Variable declarations and anonymous functions](#ch020.xhtml_variable-declarations-and-anonymous-functions)
    *   19.2.3 [Assignments and anonymous functions](#ch020.xhtml_assignments-and-anonymous-functions)
    *   19.2.4 [Default values and anonymous functions](#ch020.xhtml_default-values-and-anonymous-functions)
    *   19.2.5 [Named function expressions](#ch020.xhtml_named-function-expressions)
    *   19.2.6 [Methods in object literals](#ch020.xhtml_methods-in-object-literals)
    *   19.2.7 [Methods in class definitions](#ch020.xhtml_methods-in-class-definitions)
    *   19.2.8 [Names of classes](#ch020.xhtml_names-of-classes)
    *   19.2.9 [Default exports and anonymous constructs](#ch020.xhtml_default-exports-and-anonymous-constructs)
    *   19.2.10 [Other programming constructs](#ch020.xhtml_other-programming-constructs)
*   19.3 [Things to look out for with names of functions](#ch020.xhtml_things-to-look-out-for-with-names-of-functions)
    *   19.3.1 [The name of a function is always assigned at creation](#ch020.xhtml_the-name-of-a-function-is-always-assigned-at-creation)
    *   19.3.2 [Caveat: minification](#ch020.xhtml_caveat-minification)
*   19.4 [Changing the names of functions](#ch020.xhtml_changing-the-names-of-functions)
*   19.5 [The function property `.name` in the ECMAScript specification](#ch020.xhtml_the-function-property-.name-in-the-ecmascript-specification)

* * *

In this chapter, we look at the names of functions:

*   All functions have the property `.name`
*   This property is useful for debugging (its value shows up in stack traces) and some metaprogramming tasks (picking a function by name etc.).

## 19.1 Names of functions

The property `.name` of a function contains the function’s name:

```
[](#cb329-1)function myBeautifulFunction() {}
[](#cb329-2)assert.equal(myBeautifulFunction.name, 'myBeautifulFunction');
```

Prior to ECMAScript 6, this property was already supported by most engines. With ES6, it became part of the language standard.

The language has become surprisingly good at finding names for functions, even when they are initially anonymous (e.g., arrow functions).

### 19.1.1 Function names are used in stack traces

One benefit of function names is that they show up in stack traces. In the following example, the argument of `callFunc()` doesn’t get a name, which is why there is no function name in the second line of the stack trace.

```
[](#cb330-1)function callFunc(func) {
[](#cb330-2)  return func();
[](#cb330-3)}
[](#cb330-4)
[](#cb330-5)function func1() {
[](#cb330-6)  throw new Error('Problem');
[](#cb330-7)}
[](#cb330-8)
[](#cb330-9)function func2() {
[](#cb330-10)  // The following arrow function doesn’t have a name
[](#cb330-11)  callFunc(() => func1());
[](#cb330-12)}
[](#cb330-13)
[](#cb330-14)function func3() {
[](#cb330-15)  func2();
[](#cb330-16)}
[](#cb330-17)
[](#cb330-18)try {
[](#cb330-19)  func3();
[](#cb330-20)} catch (err) {
[](#cb330-21)assert.equal(err.stack, `
[](#cb330-22)Error: Problem
[](#cb330-23) at func1 (ch_function-names.mjs:6:9)
[](#cb330-24) at ch_function-names.mjs:11:18
[](#cb330-25) at callFunc (ch_function-names.mjs:2:10)
[](#cb330-26) at func2 (ch_function-names.mjs:11:3)
[](#cb330-27) at func3 (ch_function-names.mjs:15:3)
[](#cb330-28) at ch_function-names.mjs:19:3
[](#cb330-29)`.trim());
[](#cb330-30)
[](#cb330-31)}
```

## 19.2 Constructs that provide names for functions

The following sections describe how `.name` is set up automatically by various programming constructs.

### 19.2.1 Function declarations

Function declarations have had a `.name` for a long time – for example:

```
[](#cb331-1)function funcDecl() {}
[](#cb331-2)assert.equal(funcDecl.name, 'funcDecl');
```

### 19.2.2 Variable declarations and anonymous functions

A function created by an anonymous function expression picks up a name if it is the initialization value of a variable declaration:

```
[](#cb332-1)let letFunc = function () {};
[](#cb332-2)assert.equal(letFunc.name, 'letFunc');
[](#cb332-3)
[](#cb332-4)const constFunc = function () {};
[](#cb332-5)assert.equal(constFunc.name, 'constFunc');
[](#cb332-6)
[](#cb332-7)var varFunc = function () {};
[](#cb332-8)assert.equal(varFunc.name, 'varFunc');
```

![](media/file0.svg)  **Arrow functions also get names**

With regard to names, arrow functions are like anonymous function expressions:

```
[](#cb333-1)const arrowFunc = () => {};
[](#cb333-2)assert.equal(arrowFunc.name, 'arrowFunc');
```

From now on, whenever you see an anonymous function expression, you can assume that an arrow function works the same way.

### 19.2.3 Assignments and anonymous functions

Even with a normal assignment, `.name` is set up properly:

```
[](#cb334-1)let assignedFunc;
[](#cb334-2)assignedFunc = function () {};
[](#cb334-3)assert.equal(assignedFunc.name, 'assignedFunc');
```

### 19.2.4 Default values and anonymous functions

If a function is a default value, it gets its name from its variable or parameter:

```
[](#cb335-1)const [arrayDestructured = function () {}] = [];
[](#cb335-2)assert.equal(arrayDestructured.name, 'arrayDestructured');
[](#cb335-3)
[](#cb335-4)const {prop: objectDestructured = function () {}} = {};
[](#cb335-5)assert.equal(objectDestructured.name, 'objectDestructured');
[](#cb335-6)
[](#cb335-7)function createParamDefault(paramDefault = function () {}) {
[](#cb335-8)  return paramDefault;
[](#cb335-9)}
[](#cb335-10)assert.equal(createParamDefault().name, 'paramDefault');
```

### 19.2.5 Named function expressions

The name of a named function expression is used to set up the `.name` property:

```
[](#cb336-1)const varName = function funcName() {};
[](#cb336-2)assert.equal(varName.name, 'funcName');
```

Because it comes first, the function expression’s name `funcName` takes precedence over other names (in this case, the name `varName` of the variable). However, the name of a function expression is still only a variable inside the function expression:

```
[](#cb337-1)const varName = function funcName() {
[](#cb337-2)  assert.equal(funcName.name, 'funcName');
[](#cb337-3)};
[](#cb337-4)varName();
[](#cb337-5)assert.throws(
[](#cb337-6)  () => funcName,
[](#cb337-7)  /^ReferenceError: funcName is not defined$/
[](#cb337-8));
```

### 19.2.6 Methods in object literals

If a function is the value of a property, it gets its name from that property. It doesn’t matter if that happens via a method definition (line A), a traditional property definition (line B), a property definition with a computed property key (line C) or a property value shorthand (line D).

```
[](#cb338-1)function shortHand() {}
[](#cb338-2)const obj = {
[](#cb338-3)  methodDef() {}, // (A)
[](#cb338-4)  propDef: function () {}, // (B)
[](#cb338-5)  ['computed' + 'Key']: function () {}, // (C)
[](#cb338-6)  shortHand, // (D)
[](#cb338-7)};
[](#cb338-8)assert.equal(obj.methodDef.name, 'methodDef');
[](#cb338-9)assert.equal(obj.propDef.name, 'propDef');
[](#cb338-10)assert.equal(obj.computedKey.name, 'computedKey');
[](#cb338-11)assert.equal(obj.shortHand.name, 'shortHand');
```

The names of getters are prefixed with `'get'`, the names of setters are prefixed with `'set'`:

```
[](#cb339-1)const obj = {
[](#cb339-2)  get myGetter() {},
[](#cb339-3)  set mySetter(value) {},
[](#cb339-4)};
[](#cb339-5)const getter = Object.getOwnPropertyDescriptor(obj, 'myGetter').get;
[](#cb339-6)assert.equal(getter.name, 'get myGetter');
[](#cb339-7)
[](#cb339-8)const setter = Object.getOwnPropertyDescriptor(obj, 'mySetter').set;
[](#cb339-9)assert.equal(setter.name, 'set mySetter');
```

### 19.2.7 Methods in class definitions

The naming of methods in class definitions is similar to object literals. For example, here is a class declaration (naming works the same in class expressions):

```
[](#cb340-1)class ClassDecl {
[](#cb340-2)  methodDef() {}
[](#cb340-3)  ['computed' + 'Key']() {} // computed property key
[](#cb340-4)
[](#cb340-5)  static staticMethod() {}
[](#cb340-6)}
[](#cb340-7)assert.equal(ClassDecl.prototype.methodDef.name, 'methodDef');
[](#cb340-8)assert.equal(new ClassDecl().methodDef.name, 'methodDef');
[](#cb340-9)
[](#cb340-10)assert.equal(ClassDecl.prototype.computedKey.name, 'computedKey');
[](#cb340-11)
[](#cb340-12)assert.equal(ClassDecl.staticMethod.name, 'staticMethod');
```

Getters and setters again have the name prefixes `'get'` and `'set'`, respectively:

```
[](#cb341-1)class ClassDecl {
[](#cb341-2)  get myGetter() {}
[](#cb341-3)  set mySetter(value) {}
[](#cb341-4)}
[](#cb341-5)const getter = Object.getOwnPropertyDescriptor(
[](#cb341-6)  ClassDecl.prototype, 'myGetter').get;
[](#cb341-7)assert.equal(getter.name, 'get myGetter');
[](#cb341-8)
[](#cb341-9)const setter = Object.getOwnPropertyDescriptor(
[](#cb341-10)  ClassDecl.prototype, 'mySetter').set;
[](#cb341-11)assert.equal(setter.name, 'set mySetter');
```

#### 19.2.7.1 Methods whose keys are symbols

The key of a method can be a symbol. The `.name` property of such a method is still a string:

*   If the symbol has a description, the method’s name is the description in square brackets.
*   Otherwise, the method’s name is the empty string (`''`).

```
[](#cb342-1)const keyWithDesc = Symbol('keyWithDesc');
[](#cb342-2)const keyWithoutDesc = Symbol();
[](#cb342-3)
[](#cb342-4)const obj = {
[](#cb342-5)  [keyWithDesc]() {},
[](#cb342-6)  [keyWithoutDesc]() {},
[](#cb342-7)};
[](#cb342-8)assert.equal(obj[keyWithDesc].name, '[keyWithDesc]');
[](#cb342-9)assert.equal(obj[keyWithoutDesc].name, '');
```

### 19.2.8 Names of classes

Under the hood, classes are functions. Property `.name` of such functions is also set up correctly:

```
[](#cb343-1)class ClassDecl {}
[](#cb343-2)assert.equal(ClassDecl.name, 'ClassDecl');
[](#cb343-3)
[](#cb343-4)const AnonClassExpr = class {};
[](#cb343-5)assert.equal(AnonClassExpr.name, 'AnonClassExpr');
[](#cb343-6)
[](#cb343-7)const NamedClassExpr = class ClassName {};
[](#cb343-8)assert.equal(NamedClassExpr.name, 'ClassName');
```

### 19.2.9 Default exports and anonymous constructs

All of the following statements set `.name` to `'default'`:

```
[](#cb344-1)// Anonymous function expressions
[](#cb344-2)export default function () {}
[](#cb344-3)export default (function () {});
[](#cb344-4)
[](#cb344-5)// Anonymous class expressions
[](#cb344-6)export default class {}
[](#cb344-7)export default (class {});
[](#cb344-8)
[](#cb344-9)// Arrow functions
[](#cb344-10)export default () => {};
```

### 19.2.10 Other programming constructs

*   Generator functions and generator methods get their names the same way that normal functions and methods do. There are no asterisks in their names:

    ```
    [](#cb345-1)function* genFuncDecl() {}
    [](#cb345-2)assert.equal(genFuncDecl.name, 'genFuncDecl');
    ```

*   `new Function()` produces functions whose `.name` is `'anonymous'`. [A webkit bug](https://bugs.webkit.org/show_bug.cgi?id=7726) describes why that is necessary on the web.

    ```
    [](#cb346-1)assert.equal(new Function().name, 'anonymous');
    ```

*   `func.bind()` produces a function whose `.name` is `'bound '+func.name`:

    ```
    [](#cb347-1)function func(x) {
    [](#cb347-2)  return x
    [](#cb347-3)}
    [](#cb347-4)const bound = func.bind(undefined, 123);
    [](#cb347-5)assert.equal(bound.name, 'bound func');
    ```

## 19.3 Things to look out for with names of functions

### 19.3.1 The name of a function is always assigned at creation

A function only gets a name if one of the previously mentioned patterns is used during its creation. Using one of the patterns later doesn’t change anything – for example:

```
[](#cb348-1)function functionFactory() {
[](#cb348-2)  return function () {}; // (A)
[](#cb348-3)}
[](#cb348-4)const func = functionFactory(); // (B)
[](#cb348-5)assert.equal(func.name, ''); // anonymous
```

Function `func` is created in line A, where it also receives its non-name, the empty string `''`. Using an assignment in line B doesn’t update the initial name. Missing function names could conceivably be updated later, but doing so would impact performance negatively.

### 19.3.2 Caveat: minification

Function names are subject to minification, which means that they will usually change in minified code. Depending on what we want to do, we may have to manage function names via strings (which are not minified) or we may have to tell our minifier what names not to minify.

## 19.4 Changing the names of functions

![](media/file0.svg)  **More information on property attributes**

`Object.getOwnPropertyDescriptor()` and `Object.defineProperty()` work with property attributes. For more information on those, see [§9 “Property attributes: an introduction”](#ch010.xhtml_ch_property-attributes-intro).

These are the attributes of property `.name`:

```
[](#cb349-1)const func = function () {};
[](#cb349-2)assert.deepEqual(
[](#cb349-3)  Object.getOwnPropertyDescriptor(func, 'name'),
[](#cb349-4)  {
[](#cb349-5)    value: 'func',
[](#cb349-6)    writable: false,
[](#cb349-7)    enumerable: false,
[](#cb349-8)    configurable: true,
[](#cb349-9)  });
```

The property not being writable means that we can’t change its value via assignment:

```
[](#cb350-1)assert.throws(
[](#cb350-2)  () => func.name = 'differentName',
[](#cb350-3)  /^TypeError: Cannot assign to read only property 'name'/
[](#cb350-4));
```

The property is, however, configurable, which means that we can change it by re-defining it:

```
[](#cb351-1)Object.defineProperty(
[](#cb351-2)  func, 'name', {
[](#cb351-3)    value: 'differentName',
[](#cb351-4)  });
[](#cb351-5)assert.equal(func.name, 'differentName');
```

## 19.5 The function property `.name` in the ECMAScript specification

*   The spec operation [`SetFunctionName()`](https://tc39.es/ecma262/#sec-setfunctionname) sets up the property `.name`. Search for its name in the spec to find out where that happens. The third parameter specifies a name prefix:
    *   [Getters and setters](https://tc39.es/ecma262/#sec-method-definitions-runtime-semantics-propertydefinitionevaluation) prefix `'get'` and `'set'`.
    *   [`Function.prototype.bind()`](https://tc39.es/ecma262/#sec-function.prototype.bind) prefixes `'bound'`.
*   Anonymous function expressions initially not having a property `.name` can be seen by looking at how functions are created in the spec:
    *   The names of named function expressions are set up via `SetFunctionName()`. That operation is not invoked when [creating anonymous function expressions](https://tc39.es/ecma262/#sec-function-definitions-runtime-semantics-evaluation).
    *   The names of function declarations are set up [elsewhere](https://tc39.es/ecma262/#sec-function-definitions-runtime-semantics-instantiatefunctionobject), when entering a scope (early activation).
    *   Additionally, the spec [explicitly states](https://tc39.es/ecma262/#sec-function-instances-name): “Anonymous functions objects that do not have a contextual name associated with them by this specification do not have a `"name"` own property but inherit the `"name"` property of `%Function.prototype%`.”
*   [When an arrow function is created](https://tc39.es/ecma262/#sec-arrow-function-definitions-runtime-semantics-evaluation), no name is set up, either (`SetFunctionName()` is not invoked).

Most JavaScript engines diverge from the spec and do create own properties `.name` for anonymous functions:

```
> Reflect.ownKeys(() => {})
[ 'length', 'name' ]
```