![](media/cover-epub.jpg)

![cover image](media/cover-epub.jpg)

# JavaScript for impatient programmers

Dr. Axel Rauschmayer

2019

# JavaScript for impatient programmers

1.  [JavaScript for impatient programmers](#ch001.xhtml_javascript-for-impatient-programmers)
2.  [1 About this book (ES2019 edition)](#ch002.xhtml_ch_about-book)
    1.  [1.1 About the content](#ch002.xhtml_about-the-content)
    2.  [1.2 Previewing and buying this book](#ch002.xhtml_previewing-and-buying-this-book)
    3.  [1.3 About the author](#ch002.xhtml_about-the-author)
    4.  [1.4 Acknowledgements](#ch002.xhtml_acknowledgements)
3.  [2 FAQ: Book and supplementary material](#ch003.xhtml_ch_faq-book)
    1.  [2.1 How to read this book](#ch003.xhtml_how-to-read-this-book)
    2.  [2.2 I own a digital edition](#ch003.xhtml_i-own-a-digital-edition)
    3.  [2.3 I own the print edition](#ch003.xhtml_i-own-the-print-edition)
    4.  [2.4 Notations and conventions](#ch003.xhtml_notations-and-conventions)
4.  [3 Why JavaScript? (bonus)](#ch004.xhtml_ch_why-js)
    1.  [3.1 The cons of JavaScript](#ch004.xhtml_the-cons-of-javascript)
    2.  [3.2 The pros of JavaScript](#ch004.xhtml_the-pros-of-javascript)
    3.  [3.3 Pro and con of JavaScript: innovation](#ch004.xhtml_pro-and-con-of-javascript-innovation)
5.  [4 The nature of JavaScript (bonus)](#ch005.xhtml_ch_nature)
    1.  [4.1 JavaScript’s influences](#ch005.xhtml_javascripts-influences)
    2.  [4.2 The nature of JavaScript](#ch005.xhtml_the-nature-of-javascript)
    3.  [4.3 Tips for getting started with JavaScript](#ch005.xhtml_tips-for-getting-started-with-javascript)
6.  [5 History and evolution of JavaScript](#ch006.xhtml_ch_history)
    1.  [5.1 How JavaScript was created](#ch006.xhtml_how-javascript-was-created)
    2.  [5.2 Standardizing JavaScript](#ch006.xhtml_standardizing-javascript)
    3.  [5.3 Timeline of ECMAScript versions](#ch006.xhtml_timeline-of-ecmascript-versions)
    4.  [5.4 Ecma Technical Committee 39 (TC39)](#ch006.xhtml_tc39)
    5.  [5.5 The TC39 process](#ch006.xhtml_tc39-process)
    6.  [5.6 FAQ: TC39 process](#ch006.xhtml_tc39-process-faq)
    7.  [5.7 Evolving JavaScript: Don’t break the web](#ch006.xhtml_backward-compatibility)
7.  [6 FAQ: JavaScript](#ch007.xhtml_ch_faq-language)
    1.  [6.1 What are good references for JavaScript?](#ch007.xhtml_what-are-good-references-for-javascript)
    2.  [6.2 How do I find out what JavaScript features are supported where?](#ch007.xhtml_how-do-i-find-out-what-javascript-features-are-supported-where)
    3.  [6.3 Where can I look up what features are planned for JavaScript?](#ch007.xhtml_where-can-i-look-up-what-features-are-planned-for-javascript)
    4.  [6.4 Why does JavaScript fail silently so often?](#ch007.xhtml_why-does-javascript-fail-silently-so-often)
    5.  [6.5 Why can’t we clean up JavaScript, by removing quirks and outdated features?](#ch007.xhtml_why-cant-we-clean-up-javascript-by-removing-quirks-and-outdated-features)
    6.  [6.6 How can I quickly try out a piece of JavaScript code?](#ch007.xhtml_how-can-i-quickly-try-out-a-piece-of-javascript-code)
8.  [7 The big picture](#ch008.xhtml_ch_big-picture)
    1.  [7.1 What are you learning in this book?](#ch008.xhtml_what-are-you-learning-in-this-book)
    2.  [7.2 The structure of browsers and Node.js](#ch008.xhtml_the-structure-of-browsers-and-node.js)
    3.  [7.3 JavaScript references](#ch008.xhtml_javascript-references)
    4.  [7.4 Further reading](#ch008.xhtml_further-reading)
9.  [8 Syntax](#ch009.xhtml_ch_syntax)
    1.  [8.1 An overview of JavaScript’s syntax](#ch009.xhtml_an-overview-of-javascripts-syntax)
    2.  [8.2 (Advanced)](#ch009.xhtml_advanced)
    3.  [8.3 Identifiers](#ch009.xhtml_identifiers)
    4.  [8.4 Statement vs. expression](#ch009.xhtml_statement-vs-expression)
    5.  [8.5 Ambiguous syntax](#ch009.xhtml_ambiguous-syntax)
    6.  [8.6 Semicolons](#ch009.xhtml_semicolons)
    7.  [8.7 Automatic semicolon insertion (ASI)](#ch009.xhtml_automatic-semicolon-insertion-asi)
    8.  [8.8 Semicolons: best practices](#ch009.xhtml_semicolons-best-practices)
    9.  [8.9 Strict mode vs. sloppy mode](#ch009.xhtml_strict-mode)
10.  [9 Consoles: interactive JavaScript command lines](#ch010.xhtml_ch_console)
    1.  [9.1 Trying out JavaScript code](#ch010.xhtml_trying-out-code)
    2.  [9.2 The `console.*` API: printing data and more](#ch010.xhtml_the-console.-api-printing-data-and-more)
11.  [10 Assertion API](#ch011.xhtml_ch_assertion-api)
    1.  [10.1 Assertions in software development](#ch011.xhtml_assertions-in-software-development)
    2.  [10.2 How assertions are used in this book](#ch011.xhtml_how-assertions-are-used-in-this-book)
    3.  [10.3 Normal comparison vs. deep comparison](#ch011.xhtml_normal-comparison-vs.-deep-comparison)
    4.  [10.4 Quick reference: module `assert`](#ch011.xhtml_quick-reference-module-assert)
12.  [11 Getting started with quizzes and exercises](#ch012.xhtml_ch_quizzes-exercises)
    1.  [11.1 Quizzes](#ch012.xhtml_quizzes)
    2.  [11.2 Exercises](#ch012.xhtml_exercises)
    3.  [11.3 Unit tests in JavaScript](#ch012.xhtml_unit-tests-in-javascript)
13.  [12 Variables and assignment](#ch013.xhtml_ch_variables-assignment)
    1.  [12.1 `let`](#ch013.xhtml_let)
    2.  [12.2 `const`](#ch013.xhtml_const)
    3.  [12.3 Deciding between `const` and `let`](#ch013.xhtml_deciding-between-const-and-let)
    4.  [12.4 The scope of a variable](#ch013.xhtml_the-scope-of-a-variable)
    5.  [12.5 (Advanced)](#ch013.xhtml_advanced-1)
    6.  [12.6 Terminology: static vs. dynamic](#ch013.xhtml_terminology-static-vs.-dynamic)
    7.  [12.7 Global variables and the global object](#ch013.xhtml_global-variables-and-the-global-object)
    8.  [12.8 Declarations: scope and activation](#ch013.xhtml_declarations-scope-activation)
    9.  [12.9 Closures](#ch013.xhtml_closures)
    10.  [12.10 Further reading](#ch013.xhtml_further-reading-1)
14.  [13 Values](#ch014.xhtml_ch_values)
    1.  [13.1 What’s a type?](#ch014.xhtml_whats-a-type)
    2.  [13.2 JavaScript’s type hierarchy](#ch014.xhtml_javascripts-type-hierarchy)
    3.  [13.3 The types of the language specification](#ch014.xhtml_the-types-of-the-language-specification)
    4.  [13.4 Primitive values vs. objects](#ch014.xhtml_primitive-values-vs.-objects)
    5.  [13.5 The operators `typeof` and `instanceof`: what’s the type of a value?](#ch014.xhtml_the-operators-typeof-and-instanceof-whats-the-type-of-a-value)
    6.  [13.6 Classes and constructor functions](#ch014.xhtml_classes-and-constructor-functions)
    7.  [13.7 Converting between types](#ch014.xhtml_converting-between-types)
15.  [14 Operators](#ch015.xhtml_ch_operators)
    1.  [14.1 Making sense of operators](#ch015.xhtml_making-sense-of-operators)
    2.  [14.2 The plus operator (`+`)](#ch015.xhtml_the-plus-operator)
    3.  [14.3 Assignment operators](#ch015.xhtml_assignment-operators)
    4.  [14.4 Equality: `==` vs. `===`](#ch015.xhtml_equality-vs.)
    5.  [14.5 Ordering operators](#ch015.xhtml_ordering-operators)
    6.  [14.6 Various other operators](#ch015.xhtml_various-other-operators)
16.  [15 The non-values `undefined` and `null`](#ch016.xhtml_ch_undefined-null)
    1.  [15.1 `undefined` vs. `null`](#ch016.xhtml_undefined-vs.-null)
    2.  [15.2 Occurrences of `undefined` and `null`](#ch016.xhtml_occurrences-of-undefined-and-null)
    3.  [15.3 Checking for `undefined` or `null`](#ch016.xhtml_checking-for-undefined-or-null)
    4.  [15.4 `undefined` and `null` don’t have properties](#ch016.xhtml_undefined-and-null-dont-have-properties)
    5.  [15.5 The history of `undefined` and `null`](#ch016.xhtml_the-history-of-undefined-and-null)
17.  [16 Booleans](#ch017.xhtml_ch_booleans)
    1.  [16.1 Converting to boolean](#ch017.xhtml_converting-to-boolean)
    2.  [16.2 Falsy and truthy values](#ch017.xhtml_falsiness-truthiness)
    3.  [16.3 Truthiness-based existence checks](#ch017.xhtml_truthiness-existence-checks)
    4.  [16.4 Conditional operator (`? :`)](#ch017.xhtml_conditional-operator)
    5.  [16.5 Binary logical operators: And (`x && y`), Or (`x || y`)](#ch017.xhtml_binary-logical-operators-and-x-y-or-x-y)
    6.  [16.6 Logical Not (`!`)](#ch017.xhtml_logical-not)
18.  [17 Numbers](#ch018.xhtml_ch_numbers)
    1.  [17.1 JavaScript only has floating point numbers](#ch018.xhtml_javascript-only-has-floating-point-numbers)
    2.  [17.2 Number literals](#ch018.xhtml_number-literals)
    3.  [17.3 Arithmetic operators](#ch018.xhtml_arithmetic-operators)
    4.  [17.4 Converting to number](#ch018.xhtml_converting-to-number)
    5.  [17.5 Error values](#ch018.xhtml_error-values)
    6.  [17.6 Error value: `NaN`](#ch018.xhtml_nan)
    7.  [17.7 Error value: `Infinity`](#ch018.xhtml_error-value-infinity)
    8.  [17.8 The precision of numbers: careful with decimal fractions](#ch018.xhtml_the-precision-of-numbers-careful-with-decimal-fractions)
    9.  [17.9 (Advanced)](#ch018.xhtml_advanced-2)
    10.  [17.10 Background: floating point precision](#ch018.xhtml_background-floating-point-precision)
    11.  [17.11 Integers in JavaScript](#ch018.xhtml_integers-in-javascript)
    12.  [17.12 Bitwise operators](#ch018.xhtml_bitwise-operators)
    13.  [17.13 Quick reference: numbers](#ch018.xhtml_quick-reference-numbers)
19.  [18 `Math`](#ch019.xhtml_ch_math)
    1.  [18.1 Data properties](#ch019.xhtml_data-properties)
    2.  [18.2 Exponents, roots, logarithms](#ch019.xhtml_exponents-roots-logarithms)
    3.  [18.3 Rounding](#ch019.xhtml_math-rounding)
    4.  [18.4 Trigonometric Functions](#ch019.xhtml_trigonometric-functions)
    5.  [18.5 Various other functions](#ch019.xhtml_various-other-functions)
    6.  [18.6 Sources](#ch019.xhtml_sources-1)
20.  [19 Unicode – a brief introduction (advanced)](#ch020.xhtml_ch_unicode)
    1.  [19.1 Code points vs. code units](#ch020.xhtml_code-points-vs.-code-units)
    2.  [19.2 Encodings used in web development: UTF-16 and UTF-8](#ch020.xhtml_encodings-used-in-web-development-utf-16-and-utf-8)
    3.  [19.3 Grapheme clusters – the real characters](#ch020.xhtml_grapheme-clusters-the-real-characters)
21.  [20 Strings](#ch021.xhtml_ch_strings)
    1.  [20.1 Plain string literals](#ch021.xhtml_plain-string-literals)
    2.  [20.2 Accessing characters and code points](#ch021.xhtml_accessing-characters-and-code-points)
    3.  [20.3 String concatenation via `+`](#ch021.xhtml_string-concatenation-via)
    4.  [20.4 Converting to string](#ch021.xhtml_converting-to-string)
    5.  [20.5 Comparing strings](#ch021.xhtml_comparing-strings)
    6.  [20.6 Atoms of text: Unicode characters, JavaScript characters, grapheme clusters](#ch021.xhtml_atoms-of-text)
    7.  [20.7 Quick reference: Strings](#ch021.xhtml_quickref-strings)
22.  [21 Using template literals and tagged templates](#ch022.xhtml_ch_template-literals)
    1.  [21.1 Disambiguation: “template”](#ch022.xhtml_disambiguation-template)
    2.  [21.2 Template literals](#ch022.xhtml_template-literals)
    3.  [21.3 Tagged templates](#ch022.xhtml_tagged-templates)
    4.  [21.4 Raw string literals](#ch022.xhtml_raw-string-literals)
    5.  [21.5 (Advanced)](#ch022.xhtml_advanced-3)
    6.  [21.6 Multiline template literals and indentation](#ch022.xhtml_multiline-template-literals-and-indentation)
    7.  [21.7 Simple templating via template literals](#ch022.xhtml_simple-templating-via-template-literals)
23.  [22 Symbols](#ch023.xhtml_ch_symbols)
    1.  [22.1 Use cases for symbols](#ch023.xhtml_use-cases-for-symbols)
    2.  [22.2 Publicly known symbols](#ch023.xhtml_publicly-known-symbols)
    3.  [22.3 Converting symbols](#ch023.xhtml_converting-symbols)
24.  [23 Control flow statements](#ch024.xhtml_ch_control-flow)
    1.  [23.1 Conditions of control flow statements](#ch024.xhtml_conditions-of-control-flow-statements)
    2.  [23.2 Controlling loops: `break` and `continue`](#ch024.xhtml_controlling-loops-break-and-continue)
    3.  [23.3 `if` statements](#ch024.xhtml_if)
    4.  [23.4 `switch` statements](#ch024.xhtml_switch)
    5.  [23.5 `while` loops](#ch024.xhtml_while)
    6.  [23.6 `do-while` loops](#ch024.xhtml_do-while)
    7.  [23.7 `for` loops](#ch024.xhtml_for)
    8.  [23.8 `for-of` loops](#ch024.xhtml_for-of)
    9.  [23.9 `for-await-of` loops](#ch024.xhtml_for-await-of-loops)
    10.  [23.10 `for-in` loops (avoid)](#ch024.xhtml_for-in)
25.  [24 Exception handling](#ch025.xhtml_ch_exception-handling)
    1.  [24.1 Motivation: throwing and catching exceptions](#ch025.xhtml_motivation-throwing-and-catching-exceptions)
    2.  [24.2 `throw`](#ch025.xhtml_throw)
    3.  [24.3 The `try` statement](#ch025.xhtml_the-try-statement)
    4.  [24.4 Error classes](#ch025.xhtml_error-classes)
26.  [25 Callable values](#ch026.xhtml_ch_callables)
    1.  [25.1 Kinds of functions](#ch026.xhtml_kinds-of-functions)
    2.  [25.2 Ordinary functions](#ch026.xhtml_ordinary-functions)
    3.  [25.3 Specialized functions](#ch026.xhtml_specialized-functions)
    4.  [25.4 More kinds of functions and methods](#ch026.xhtml_more-kinds-of-functions-and-methods)
    5.  [25.5 Returning values from functions and methods](#ch026.xhtml_returning-values-from-functions-and-methods)
    6.  [25.6 Parameter handling](#ch026.xhtml_parameter-handling)
    7.  [25.7 Dynamically evaluating code: `eval()`, `new Function()` (advanced)](#ch026.xhtml_dynamically-evaluating-code-eval-new-function-advanced)
27.  [26 Environments: under the hood of variables (bonus)](#ch027.xhtml_ch_environments)
    1.  [26.1 Environment: data structure for managing variables](#ch027.xhtml_environment-data-structure-for-managing-variables)
    2.  [26.2 Recursion via environments](#ch027.xhtml_recursion-via-environments)
    3.  [26.3 Nested scopes via environments](#ch027.xhtml_nested-scopes-via-environments)
    4.  [26.4 Closures and environments](#ch027.xhtml_closures-environments)
28.  [27 Modules](#ch028.xhtml_ch_modules)
    1.  [27.1 Overview: syntax of ECMAScript modules](#ch028.xhtml_overview-syntax-of-ecmascript-modules)
    2.  [27.2 JavaScript source code formats](#ch028.xhtml_javascript-source-code-formats)
    3.  [27.3 Before we had modules, we had scripts](#ch028.xhtml_scripts)
    4.  [27.4 Module systems created prior to ES6](#ch028.xhtml_module-systems-created-prior-to-es6)
    5.  [27.5 ECMAScript modules](#ch028.xhtml_ecmascript-modules)
    6.  [27.6 Named exports and imports](#ch028.xhtml_named-exports-and-imports)
    7.  [27.7 Default exports and imports](#ch028.xhtml_default-exports-and-imports)
    8.  [27.8 More details on exporting and importing](#ch028.xhtml_more-details-on-exporting-and-importing)
    9.  [27.9 npm packages](#ch028.xhtml_npm-packages)
    10.  [27.10 Naming modules](#ch028.xhtml_naming-modules)
    11.  [27.11 Module specifiers](#ch028.xhtml_module-specifiers)
    12.  [27.12 Loading modules dynamically via `import()`](#ch028.xhtml_loading-modules-dynamically-via-import)
    13.  [27.13 Preview: `import.meta.url`](#ch028.xhtml_preview-import.meta.url)
    14.  [27.14 Polyfills: emulating native web platform features (advanced)](#ch028.xhtml_polyfills)
29.  [28 Single objects](#ch029.xhtml_ch_single-objects)
    1.  [28.1 What is an object?](#ch029.xhtml_what-is-an-object)
    2.  [28.2 Objects as records](#ch029.xhtml_objects-as-records)
    3.  [28.3 Spreading into object literals (`...`)](#ch029.xhtml_spreading-into-object-literals)
    4.  [28.4 Methods](#ch029.xhtml_methods)
    5.  [28.5 Objects as dictionaries (advanced)](#ch029.xhtml_objects-as-dictionaries-advanced)
    6.  [28.6 Standard methods (advanced)](#ch029.xhtml_standard-methods-advanced)
    7.  [28.7 Advanced topics](#ch029.xhtml_advanced-topics)
30.  [29 Prototype chains and classes](#ch030.xhtml_ch_proto-chains-classes)
    1.  [29.1 Prototype chains](#ch030.xhtml_prototype-chains)
    2.  [29.2 Classes](#ch030.xhtml_classes)
    3.  [29.3 Private data for classes](#ch030.xhtml_private-data-for-classes)
    4.  [29.4 Subclassing](#ch030.xhtml_subclassing)
    5.  [29.5 FAQ: objects](#ch030.xhtml_faq-objects)
31.  [30 Synchronous iteration](#ch031.xhtml_ch_sync-iteration)
    1.  [30.1 What is synchronous iteration about?](#ch031.xhtml_what-is-synchronous-iteration-about)
    2.  [30.2 Core iteration constructs: iterables and iterators](#ch031.xhtml_iterable-iterator-iteratorresult)
    3.  [30.3 Iterating manually](#ch031.xhtml_iterating-manually)
    4.  [30.4 Iteration in practice](#ch031.xhtml_iteration-in-practice)
    5.  [30.5 Quick reference: synchronous iteration](#ch031.xhtml_quick-reference-synchronous-iteration)
32.  [31 Arrays (`Array`)](#ch032.xhtml_ch_arrays)
    1.  [31.1 The two roles of Arrays in JavaScript](#ch032.xhtml_the-two-roles-of-arrays-in-javascript)
    2.  [31.2 Basic Array operations](#ch032.xhtml_basic-array-operations)
    3.  [31.3 `for-of` and Arrays](#ch032.xhtml_for-of-and-arrays)
    4.  [31.4 Array-like objects](#ch032.xhtml_array-like-objects)
    5.  [31.5 Converting iterable and Array-like values to Arrays](#ch032.xhtml_converting-iterable-and-array-like-values-to-arrays)
    6.  [31.6 Creating and filling Arrays with arbitrary lengths](#ch032.xhtml_filling-arrays)
    7.  [31.7 Multidimensional Arrays](#ch032.xhtml_multidimensional-arrays)
    8.  [31.8 More Array features (advanced)](#ch032.xhtml_more-array-features-advanced)
    9.  [31.9 Adding and removing elements (destructively and non-destructively)](#ch032.xhtml_adding-and-removing-elements-destructively-and-non-destructively)
    10.  [31.10 Methods: iteration and transformation (`.find()`, `.map()`, `.filter()`, etc.)](#ch032.xhtml_methods-iteration-and-transformation-.find-.map-.filter-etc.)
    11.  [31.11 `.sort()`: sorting Arrays](#ch032.xhtml_sort-sorting-arrays)
    12.  [31.12 Quick reference: `Array<T>`](#ch032.xhtml_quickref-arrays)
33.  [32 Typed Arrays: handling binary data (Advanced)](#ch033.xhtml_ch_typed-arrays)
    1.  [32.1 The basics of the API](#ch033.xhtml_the-basics-of-the-api)
    2.  [32.2 Element types](#ch033.xhtml_element-types)
    3.  [32.3 More information on Typed Arrays](#ch033.xhtml_more-information-on-typed-arrays)
    4.  [32.4 Quick references: indices vs. offsets](#ch033.xhtml_typed-arrays-indices-offsets)
    5.  [32.5 Quick reference: ArrayBuffers](#ch033.xhtml_quick-reference-arraybuffers)
    6.  [32.6 Quick reference: Typed Arrays](#ch033.xhtml_quick-reference-typed-arrays)
    7.  [32.7 Quick reference: DataViews](#ch033.xhtml_quick-reference-dataviews)
34.  [33 Maps (`Map`)](#ch034.xhtml_ch_maps)
    1.  [33.1 Using Maps](#ch034.xhtml_using-maps)
    2.  [33.2 Example: Counting characters](#ch034.xhtml_example-counting-characters)
    3.  [33.3 A few more details about the keys of Maps (advanced)](#ch034.xhtml_a-few-more-details-about-the-keys-of-maps-advanced)
    4.  [33.4 Missing Map operations](#ch034.xhtml_missing-map-operations)
    5.  [33.5 Quick reference: `Map<K,V>`](#ch034.xhtml_quickref-maps)
    6.  [33.6 FAQ: Maps](#ch034.xhtml_faq-maps)
35.  [34 WeakMaps (`WeakMap`)](#ch035.xhtml_ch_weakmaps)
    1.  [34.1 WeakMaps are black boxes](#ch035.xhtml_weakmaps-as-black-boxes)
    2.  [34.2 The keys of a WeakMap are *weakly held*](#ch035.xhtml_weakmap-keys-are-weakly-held)
    3.  [34.3 Examples](#ch035.xhtml_examples)
    4.  [34.4 WeakMap API](#ch035.xhtml_weakmap-api)
36.  [35 Sets (`Set`)](#ch036.xhtml_ch_sets)
    1.  [35.1 Using Sets](#ch036.xhtml_using-sets)
    2.  [35.2 Examples of using Sets](#ch036.xhtml_examples-of-using-sets)
    3.  [35.3 What Set elements are considered equal?](#ch036.xhtml_what-set-elements-are-considered-equal)
    4.  [35.4 Missing Set operations](#ch036.xhtml_missing-set-operations)
    5.  [35.5 Quick reference: `Set<T>`](#ch036.xhtml_quickref-sets)
    6.  [35.6 FAQ: Sets](#ch036.xhtml_faq-sets)
37.  [36 WeakSets (`WeakSet`)](#ch037.xhtml_ch_weaksets)
    1.  [36.1 Example: Marking objects as safe to use with a method](#ch037.xhtml_example-marking-objects-as-safe-to-use-with-a-method)
    2.  [36.2 WeakSet API](#ch037.xhtml_weakset-api)
38.  [37 Destructuring](#ch038.xhtml_ch_destructuring)
    1.  [37.1 A first taste of destructuring](#ch038.xhtml_a-first-taste-of-destructuring)
    2.  [37.2 Constructing vs. extracting](#ch038.xhtml_constructing-vs.-extracting)
    3.  [37.3 Where can we destructure?](#ch038.xhtml_where-can-we-destructure)
    4.  [37.4 Object-destructuring](#ch038.xhtml_object-destructuring)
    5.  [37.5 Array-destructuring](#ch038.xhtml_array-destructuring)
    6.  [37.6 Examples of destructuring](#ch038.xhtml_examples-of-destructuring)
    7.  [37.7 What happens if a pattern part does not match anything?](#ch038.xhtml_what-happens-if-a-pattern-part-does-not-match-anything)
    8.  [37.8 What values can’t be destructured?](#ch038.xhtml_what-values-cant-be-destructured)
    9.  [37.9 (Advanced)](#ch038.xhtml_advanced-4)
    10.  [37.10 Default values](#ch038.xhtml_default-values)
    11.  [37.11 Parameter definitions are similar to destructuring](#ch038.xhtml_parameter-definitions-are-similar-to-destructuring)
    12.  [37.12 Nested destructuring](#ch038.xhtml_nested-destructuring)
39.  [38 Synchronous generators (advanced)](#ch039.xhtml_ch_sync-generators)
    1.  [38.1 What are synchronous generators?](#ch039.xhtml_what-are-synchronous-generators)
    2.  [38.2 Calling generators from generators (advanced)](#ch039.xhtml_calling-generators-from-generators-advanced)
    3.  [38.3 Background: external iteration vs. internal iteration](#ch039.xhtml_external-iteration-internal-iteration)
    4.  [38.4 Use case for generators: reusing traversals](#ch039.xhtml_reusing-traversals)
    5.  [38.5 Advanced features of generators](#ch039.xhtml_advanced-features-of-generators)
40.  [39 Asynchronous programming in JavaScript](#ch040.xhtml_ch_async-js)
    1.  [39.1 A roadmap for asynchronous programming in JavaScript](#ch040.xhtml_a-roadmap-for-asynchronous-programming-in-javascript)
    2.  [39.2 The call stack](#ch040.xhtml_the-call-stack)
    3.  [39.3 The event loop](#ch040.xhtml_the-event-loop)
    4.  [39.4 How to avoid blocking the JavaScript process](#ch040.xhtml_how-to-avoid-blocking-the-javascript-process)
    5.  [39.5 Patterns for delivering asynchronous results](#ch040.xhtml_patterns-for-delivering-asynchronous-results)
    6.  [39.6 Asynchronous code: the downsides](#ch040.xhtml_asynchronous-code-the-downsides)
    7.  [39.7 Resources](#ch040.xhtml_resources)
41.  [40 Promises for asynchronous programming](#ch041.xhtml_ch_promises)
    1.  [40.1 The basics of using Promises](#ch041.xhtml_the-basics-of-using-promises)
    2.  [40.2 Examples](#ch041.xhtml_examples-1)
    3.  [40.3 Error handling: don’t mix rejections and exceptions](#ch041.xhtml_error-handling-dont-mix-rejections-and-exceptions)
    4.  [40.4 Promise-based functions start synchronously, settle asynchronously](#ch041.xhtml_promise-based-functions-start-synchronously-settle-asynchronously)
    5.  [40.5 `Promise.all()`: concurrency and Arrays of Promises](#ch041.xhtml_promise.all-concurrency-and-arrays-of-promises)
    6.  [40.6 Tips for chaining Promises](#ch041.xhtml_tips-for-chaining-promises)
    7.  [40.7 Advanced topics](#ch041.xhtml_advanced-topics-1)
42.  [41 Async functions](#ch042.xhtml_ch_async-functions)
    1.  [41.1 Async functions: the basics](#ch042.xhtml_async-functions-the-basics)
    2.  [41.2 Returning from async functions](#ch042.xhtml_returning-from-async-functions)
    3.  [41.3 `await`: working with Promises](#ch042.xhtml_await-working-with-promises)
    4.  [41.4 (Advanced)](#ch042.xhtml_advanced-5)
    5.  [41.5 Immediately invoked async arrow functions](#ch042.xhtml_immediately-invoked-async-arrow-functions)
    6.  [41.6 Concurrency and `await`](#ch042.xhtml_concurrency-and-await)
    7.  [41.7 Tips for using async functions](#ch042.xhtml_tips-for-using-async-functions)
43.  [42 Asynchronous iteration](#ch043.xhtml_ch_async-iteration)
    1.  [42.1 Basic asynchronous iteration](#ch043.xhtml_basic-asynchronous-iteration)
    2.  [42.2 Asynchronous generators](#ch043.xhtml_async-generators)
    3.  [42.3 Async iteration over Node.js streams](#ch043.xhtml_async-iteration-over-node.js-streams)
44.  [43 Regular expressions (`RegExp`)](#ch044.xhtml_ch_regexps)
    1.  [43.1 Creating regular expressions](#ch044.xhtml_creating-regular-expressions)
    2.  [43.2 Syntax](#ch044.xhtml_syntax)
    3.  [43.3 Flags](#ch044.xhtml_reg-exp-flags)
    4.  [43.4 Properties of regular expression objects](#ch044.xhtml_properties-of-regular-expression-objects)
    5.  [43.5 Methods for working with regular expressions](#ch044.xhtml_methods-for-working-with-regular-expressions)
    6.  [43.6 Flag `/g` and its pitfalls](#ch044.xhtml_regexp-flag-g)
    7.  [43.7 Techniques for working with regular expressions](#ch044.xhtml_techniques-for-working-with-regular-expressions)
45.  [44 Dates (`Date`)](#ch045.xhtml_ch_dates)
    1.  [44.1 Best practice: avoid the built-in `Date`](#ch045.xhtml_date-libraries)
    2.  [44.2 Time standards](#ch045.xhtml_time-standards)
    3.  [44.3 Background: date time formats (ISO)](#ch045.xhtml_date-time-formats)
    4.  [44.4 Time values](#ch045.xhtml_time-values)
    5.  [44.5 Creating Dates](#ch045.xhtml_creating-dates)
    6.  [44.6 Getters and setters](#ch045.xhtml_getters-and-setters)
    7.  [44.7 Converting Dates to strings](#ch045.xhtml_converting-dates-to-strings)
46.  [45 Creating and parsing JSON (`JSON`)](#ch046.xhtml_ch_json)
    1.  [45.1 The discovery and standardization of JSON](#ch046.xhtml_the-discovery-and-standardization-of-json)
    2.  [45.2 JSON syntax](#ch046.xhtml_json-syntax)
    3.  [45.3 Using the `JSON` API](#ch046.xhtml_using-the-json-api)
    4.  [45.4 Customizing stringification and parsing (advanced)](#ch046.xhtml_json-replacers-revivers)
    5.  [45.5 FAQ](#ch046.xhtml_faq)
47.  [46 Next steps: overview of web development (bonus)](#ch047.xhtml_ch_next-steps)
    1.  [46.1 Tips against feeling overwhelmed](#ch047.xhtml_tips-against-feeling-overwhelmed)
    2.  [46.2 Things worth learning for web development](#ch047.xhtml_things-worth-learning-for-web-development)
    3.  [46.3 Example: tool-based JavaScript workflow](#ch047.xhtml_example-tool-based-javascript-workflow)
    4.  [46.4 An overview of JavaScript tools](#ch047.xhtml_overview-of-js-tools)
    5.  [46.5 Tools not related to JavaScript](#ch047.xhtml_tools-not-related-to-javascript)
48.  [47 Index](#ch048.xhtml_ch_index)

# JavaScript for impatient programmers

# 1 About this book (ES2019 edition)

* * *

*   1.1 [About the content](#ch002.xhtml_about-the-content)
    *   1.1.1 [What’s in this book?](#ch002.xhtml_whats-in-this-book)
    *   1.1.2 [What is not covered by this book?](#ch002.xhtml_what-is-not-covered-by-this-book)
    *   1.1.3 [Isn’t this book too long for impatient people?](#ch002.xhtml_isnt-this-book-too-long-for-impatient-people)
*   1.2 [Previewing and buying this book](#ch002.xhtml_previewing-and-buying-this-book)
    *   1.2.1 [How can I preview the book, the exercises, and the quizzes?](#ch002.xhtml_how-can-i-preview-the-book-the-exercises-and-the-quizzes)
    *   1.2.2 [How can I buy a digital edition of this book?](#ch002.xhtml_how-can-i-buy-a-digital-edition-of-this-book)
    *   1.2.3 [How can I buy the print edition of this book?](#ch002.xhtml_how-can-i-buy-the-print-edition-of-this-book)
*   1.3 [About the author](#ch002.xhtml_about-the-author)
*   1.4 [Acknowledgements](#ch002.xhtml_acknowledgements)

* * *

## 1.1 About the content

### 1.1.1 What’s in this book?

This book makes JavaScript less challenging to learn for newcomers by offering a modern view that is as consistent as possible.

Highlights:

*   Get started quickly by initially focusing on modern features.
*   Test-driven exercises and quizzes available for most chapters.
*   Covers all essential features of JavaScript, up to and including ES2019.
*   Optional advanced sections let you dig deeper.

No prior knowledge of JavaScript is required, but you should know how to program.

### 1.1.2 What is not covered by this book?

*   Some advanced language features are not explained, but references to appropriate material are provided – for example, to my other JavaScript books at [`ExploringJS.com`](https://exploringjs.com/), which are free to read online.
*   This book deliberately focuses on the language. Browser-only features, etc. are not described.

### 1.1.3 Isn’t this book too long for impatient people?

There are several ways in which you can read this book. One of them involves skipping much of the content in order to get started quickly. For details, see [§2.1.1 “In which order should I read the content in this book?”](#ch003.xhtml_order-of-reading).

## 1.2 Previewing and buying this book

### 1.2.1 How can I preview the book, the exercises, and the quizzes?

Go to [the homepage of this book](https://exploringjs.com/impatient-js/):

*   All essential chapters of this book can be read online.
*   The first half of the test-driven exercises can be downloaded.
*   The first half of the quizzes can be tried online.

### 1.2.2 How can I buy a digital edition of this book?

There are two digital editions of *JavaScript for impatient programmers*:

*   Ebooks: PDF, EPUB, MOBI, HTML (all without DRM)
*   Ebooks plus exercises and quizzes

[The home page of this book](https://exploringjs.com/impatient-js/#buy) describes how you can buy them.

### 1.2.3 How can I buy the print edition of this book?

The print edition of *JavaScript for impatient programmers* is available on Amazon.

## 1.3 About the author

Dr. Axel Rauschmayer specializes in JavaScript and web development. He has been developing web applications since 1995\. In 1999, he was technical manager at a German internet startup that later expanded internationally. In 2006, he held his first talk on Ajax. In 2010, he received a PhD in Informatics from the University of Munich.

Since 2011, he has been blogging about web development at 2ality.com and has written several books on JavaScript. He has held trainings and talks for companies such as eBay, Bank of America, and O’Reilly Media.

He lives in Munich, Germany.

## 1.4 Acknowledgements

*   Cover by [Fran Caye](http://francaye.net)
*   Parts of this book were edited by [Adaobi Obi Tulton](http://www.serendipity23editorial.com).
*   Thanks for answering questions, discussing language topics, etc.:
    *   Allen Wirfs-Brock ([`@awbjs`](https://twitter.com/awbjs))
    *   Benedikt Meurer ([`@bmeurer`](https://twitter.com/bmeurer))
    *   Brian Terlson ([`@bterlson`](https://twitter.com/bterlson))
    *   Daniel Ehrenberg ([`@littledan`](https://twitter.com/littledan))
    *   Jordan Harband ([`@ljharb`](https://twitter.com/ljharb))
    *   Mathias Bynens ([`@mathias`](https://twitter.com/mathias))
    *   Myles Borins ([`@MylesBorins`](https://twitter.com/MylesBorins))
    *   Rob Palmer ([`@robpalmer2`](https://twitter.com/robpalmer2))
    *   Šime Vidas ([`@simevidas`](https://twitter.com/simevidas))
    *   And many others
*   Thanks for reviewing:
    *   Johannes Weber ([`@jowe`](https://twitter.com/jowe))

[Generated: 2019-08-31 17:39]

# 2 FAQ: Book and supplementary material

* * *

*   2.1 [How to read this book](#ch003.xhtml_how-to-read-this-book)
    *   2.1.1 [In which order should I read the content in this book?](#ch003.xhtml_order-of-reading)
    *   2.1.2 [Why are some chapters and sections marked with “(advanced)”?](#ch003.xhtml_why-are-some-chapters-and-sections-marked-with-advanced)
    *   2.1.3 [Why are some chapters marked with “(bonus)”?](#ch003.xhtml_why-are-some-chapters-marked-with-bonus)
*   2.2 [I own a digital edition](#ch003.xhtml_i-own-a-digital-edition)
    *   2.2.1 [How do I submit feedback and corrections?](#ch003.xhtml_how-do-i-submit-feedback-and-corrections)
    *   2.2.2 [How do I get updates for the downloads I bought at Payhip?](#ch003.xhtml_how-do-i-get-updates-for-the-downloads-i-bought-at-payhip)
    *   2.2.3 [Can I upgrade from package “Ebooks” to package “Ebooks + exercises + quizzes”?](#ch003.xhtml_can-i-upgrade-from-package-ebooks-to-package-ebooks-exercises-quizzes)
*   2.3 [I own the print edition](#ch003.xhtml_i-own-the-print-edition)
    *   2.3.1 [Can I get a discount for a digital edition?](#ch003.xhtml_can-i-get-a-discount-for-a-digital-edition)
    *   2.3.2 [Can I submit an error or see submitted errors?](#ch003.xhtml_can-i-submit-an-error-or-see-submitted-errors)
    *   2.3.3 [Is there an online list with the URLs in this book?](#ch003.xhtml_is-there-an-online-list-with-the-urls-in-this-book)
*   2.4 [Notations and conventions](#ch003.xhtml_notations-and-conventions)
    *   2.4.1 [What is a type signature? Why am I seeing static types in this book?](#ch003.xhtml_what-is-a-type-signature-why-am-i-seeing-static-types-in-this-book)
    *   2.4.2 [What do the notes with icons mean?](#ch003.xhtml_what-do-the-notes-with-icons-mean)

* * *

This chapter answers questions you may have and gives tips for reading this book.

## 2.1 How to read this book

### 2.1.1 In which order should I read the content in this book?

This book is three books in one:

*   You can use it to get started with JavaScript as quickly as possible. This “mode” is for impatient people:
    *   Start reading with [§7 “The big picture”](#ch008.xhtml_ch_big-picture).
    *   Skip all chapters and sections marked as “advanced”, and all quick references.
*   It gives you a comprehensive look at current JavaScript. In this “mode”, you read everything and don’t skip advanced content and quick references.
*   It serves as a reference. If there is a topic that you are interested in, you can find information on it via the table of contents or via the index. Due to basic and advanced content being mixed, everything you need is usually in a single location.

[The quizzes and exercises](#ch012.xhtml_ch_quizzes-exercises) play an important part in helping you practice and retain what you have learned.

### 2.1.2 Why are some chapters and sections marked with “(advanced)”?

Several chapters and sections are marked with “(advanced)”. The idea is that you can initially skip them. That is, you can get a quick working knowledge of JavaScript by only reading the basic (non-advanced) content.

As your knowledge evolves, you can later come back to some or all of the advanced content.

### 2.1.3 Why are some chapters marked with “(bonus)”?

The bonus chapters are only available in the paid versions of this book (print and ebook). They are listed in [the full table of contents](https://exploringjs.com/impatient-js/downloads/complete-toc.html).

## 2.2 I own a digital edition

### 2.2.1 How do I submit feedback and corrections?

The HTML version of this book (online, or ad-free archive in the paid version) has a link at the end of each chapter that enables you to give feedback.

### 2.2.2 How do I get updates for the downloads I bought at Payhip?

*   The receipt email for the purchase includes a link. You’ll always be able to download the latest version of the files at that location.

*   If you opted into emails while buying, you’ll get an email whenever there is new content. To opt in later, you must contact Payhip (see bottom of `payhip.com`).

### 2.2.3 Can I upgrade from package “Ebooks” to package “Ebooks + exercises + quizzes”?

Yes. The instructions for doing so are [on the homepage of this book](https://exploringjs.com/impatient-js/#upgrades).

## 2.3 I own the print edition

### 2.3.1 Can I get a discount for a digital edition?

If you bought the print edition, you can get a discount for a digital edition. [The homepage of the print edition](https://exploringjs.com/impatient-js/es2019/) explains how.

Alas, the reverse is not possible: you cannot get a discount for the print edition if you bought a digital edition.

### 2.3.2 Can I submit an error or see submitted errors?

On [the homepage of the print edition](https://exploringjs.com/impatient-js/es2019/), you can submit errors and see submitted errors.

### 2.3.3 Is there an online list with the URLs in this book?

[The homepage of the print edition](https://exploringjs.com/impatient-js/es2019/) has a list with all the URLs that you see in the footnotes of the print edition.

## 2.4 Notations and conventions

### 2.4.1 What is a type signature? Why am I seeing static types in this book?

For example, you may see:

```
[](#cb1-1)Number.isFinite(num: number): boolean
```

That is called the *type signature* of `Number.isFinite()`. This notation, especially the static types `number` of `num` and `boolean` of the result, are not real JavaScript. The notation is borrowed from the compile-to-JavaScript language TypeScript (which is mostly just JavaScript plus static typing).

Why is this notation being used? It helps give you a quick idea of how a function works. The notation is explained in detail in [a 2ality blog post](https://2ality.com/2018/04/type-notation-typescript.html), but is usually relatively intuitive.

### 2.4.2 What do the notes with icons mean?

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

# 3 Why JavaScript? (bonus)

* * *

*   3.1 [The cons of JavaScript](#ch004.xhtml_the-cons-of-javascript)
*   3.2 [The pros of JavaScript](#ch004.xhtml_the-pros-of-javascript)
    *   3.2.1 [Community](#ch004.xhtml_community)
    *   3.2.2 [Practically useful](#ch004.xhtml_practically-useful)
    *   3.2.3 [Language](#ch004.xhtml_language)
*   3.3 [Pro and con of JavaScript: innovation](#ch004.xhtml_pro-and-con-of-javascript-innovation)

* * *

In this chapter, we examine the pros and cons of JavaScript.

![](media/file0.svg)  **“ECMAScript 6” and “ES6” refer to versions of JavaScript**

ECMAScript is the name of the language standard; the number refers to the version of that standard. For more information, consult [§5.2 “Standardizing JavaScript”](#ch006.xhtml_standardizing-javascript).

## 3.1 The cons of JavaScript

Among programmers, JavaScript isn’t always well liked. One reason is that it has a fair amount of quirks. Some of them are just unusual ways of doing something. Others are considered bugs. Either way, learning *why* JavaScript does something the way it does, helps with dealing with the quirks and with accepting JavaScript (maybe even liking it). Hopefully, this book can be of assistance here.

Additionally, many traditional quirks have been eliminated now. For example:

*   Traditionally, JavaScript variables weren’t block-scoped. ES6 introduced `let` and `const`, which let you declare block-scoped variables.
*   Prior to ES6, implementing object factories and inheritance via `function` and `.prototype` was clumsy. ES6 introduced classes, which provide more convenient syntax for these mechanisms.
*   Traditionally, JavaScript did not have built-in modules. ES6 added them to the language.

Lastly, JavaScript’s standard library is limited, but:

*   There are [plans](https://github.com/tc39/proposal-javascript-standard-library) for adding more functionality.
*   Many libraries are easily available via [the npm software registry](https://www.npmjs.com).

## 3.2 The pros of JavaScript

On the plus side, JavaScript offers many benefits.

### 3.2.1 Community

JavaScript’s popularity means that it’s well supported and well documented. Whenever you create something in JavaScript, you can rely on many people being (potentially) interested. And there is a large pool of JavaScript programmers from which you can hire, if you need to.

No single party controls JavaScript – it is evolved by [TC39](#ch006.xhtml_tc39), a committee comprising many organizations. The language is evolved via an open process that encourages feedback from the public.

### 3.2.2 Practically useful

With JavaScript, you can write apps for many client platforms. These are a few example technologies:

*   [*Progressive Web Apps*](https://developers.google.com/web/progressive-web-apps/) can be installed natively on Android and many desktop operating systems.
*   [*Electron*](https://electronjs.org) lets you build cross-platform desktop apps.
*   [*React Native*](https://facebook.github.io/react-native/) lets you write apps for iOS and Android that have native user interfaces.
*   [*Node.js*](https://nodejs.org/) provides extensive support for writing shell scripts (in addition to being a platform for web servers).

JavaScript is supported by many server platforms and services – for example:

*   Node.js (many of the following services are based on Node.js or support its APIs)
*   ZEIT Now
*   Microsoft Azure Functions
*   AWS Lambda
*   Google Cloud Functions

There are many data technologies available for JavaScript: many databases support it and intermediate layers (such as GraphQL) exist. Additionally, [the standard data format *JSON* (*JavaScript Object Notation*)](#ch046.xhtml_ch_json) is based on JavaScript and supported by its standard library.

Lastly, many, if not most, tools for JavaScript are written in JavaScript. That includes IDEs, build tools, and more. As a consequence, you install them the same way you install your libraries and you can customize them in JavaScript.

### 3.2.3 Language

*   Many libraries are available, via the de-facto standard in the JavaScript universe, [the npm software registry](https://www.npmjs.com).
*   If you are unhappy with “plain” JavaScript, it is relatively easy to add more features:
    *   You can compile future and modern language features to current and past versions of JavaScript, via [Babel](https://babeljs.io).
    *   You can add static typing, via [TypeScript](https://www.typescriptlang.org) and [Flow](https://flow.org).
    *   You can work with ReasonML, which is, roughly, OCaml with JavaScript syntax. It can be compiled to JavaScript or native code.
*   The language is flexible: it is dynamic and supports both object-oriented programming and functional programming.
*   JavaScript has become suprisingly fast for such a dynamic language.
    *   Whenever it isn’t fast enough, you can switch to [WebAssembly](#ch047.xhtml_web-assembly), a universal virtual machine built into most JavaScript engines. It can run static code at nearly native speeds.

## 3.3 Pro and con of JavaScript: innovation

There is much innovation in the JavaScript ecosystem: new approaches to implementing user interfaces, new ways of optimizing the delivery of software, and more. The upside is that you will constantly learn new things. The downside is that the constant change can be exhausting at times. Thankfully, things have somewhat slowed down, recently: all of ES6 (which was a considerable modernization of the language) is becoming established, as are certain tools and workflows.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 4 The nature of JavaScript (bonus)

* * *

*   4.1 [JavaScript’s influences](#ch005.xhtml_javascripts-influences)
*   4.2 [The nature of JavaScript](#ch005.xhtml_the-nature-of-javascript)
    *   4.2.1 [JavaScript often fails silently](#ch005.xhtml_silent-failures-in-js)
*   4.3 [Tips for getting started with JavaScript](#ch005.xhtml_tips-for-getting-started-with-javascript)

* * *

## 4.1 JavaScript’s influences

When JavaScript was created in 1995, it was influenced by several programming languages:

*   JavaScript’s syntax is largely based on Java.
*   Self inspired JavaScript’s prototypal inheritance.
*   Closures and environments were borrowed from Scheme.
*   AWK influenced JavaScript’s functions (including the keyword `function`).
*   JavaScript’s strings, Arrays, and regular expressions take cues from Perl.
*   HyperTalk inspired event handling via `onclick` in web browsers.

With ECMAScript 6, new influences came to JavaScript:

*   Generators were borrowed from Python.
*   The syntax of arrow functions came from CoffeeScript.
*   C++ contributed the keyword `const`.
*   Destructuring was inspired by Lisp’s *destructuring bind*.
*   Template literals came from the E language (where they are called *quasi literals*).

## 4.2 The nature of JavaScript

These are a few traits of the language:

*   Its syntax is part of the C family of languages (curly braces, etc.).

*   It is a dynamic language: most objects can be changed in various ways at runtime, objects can be created directly, etc.

*   It is a dynamically typed language: variables don’t have fixed static types and you can assign any value to a given (mutable) variable.

*   It has functional programming features: first-class functions, closures, partial application via `bind()`, etc.

*   It has object-oriented features: mutable state, objects, inheritance, classes, etc.

*   It often fails silently: see the next subsection for details.

*   It is deployed as source code. But that source code is often *minified* (rewritten to require less storage). And there are [plans for a binary source code format](https://github.com/tc39/proposal-binary-ast).

*   JavaScript is part of the web platform – it is the language built into web browsers. But it is also used elsewhere – for example, in Node.js, for server things, and shell scripting.

*   JavaScript engines often optimize less-efficient language mechanisms under the hood. For example, in principle, JavaScript Arrays are dictionaries. But under the hood, engines store Arrays contiguously if they have contiguous indices.

### 4.2.1 JavaScript often fails silently

JavaScript often fails silently. Let’s look at two examples.

First example: If the operands of an operator don’t have the appropriate types, they are converted as necessary.

```
> '3' * '5'
15
```

Second example: If an arithmetic computation fails, you get an error value, not an exception.

```
> 1 / 0
Infinity
```

The reason for the silent failures is historical: JavaScript did not have exceptions until ECMAScript 3\. Since then, its designers have tried to avoid silent failures.

## 4.3 Tips for getting started with JavaScript

These are a few tips to help you get started with JavaScript:

*   Take your time to really get to know this language. The conventional C-style syntax hides that this is a very unconventional language. Learn especially the quirks and the rationales behind them. Then you will understand and appreciate the language better.
    *   In addition to details, this book also teaches simple rules of thumb to be safe – for example, “Always use `===` to determine if two values are equal, never `==`.”
*   Language tools make it easier to work with JavaScript. For example:
    *   You can statically type JavaScript via [TypeScript](https://www.typescriptlang.org) or [Flow](https://flow.org).
    *   You can check for problems and anti-patterns via linters such as [ESLint](https://eslint.org).
    *   You can format your code automatically via code formatters such as [Prettier](https://prettier.io).
*   Get in contact with the community:
    *   Twitter is popular among JavaScript programmers. As a mode of communication that sits between the spoken and the written word, it is well suited for exchanging knowledge.
    *   Many cities have regular free meetups where people come together to learn topics related to JavaScript.
    *   JavaScript conferences are another convenient way of meeting other JavaScript programmers.
*   Read books and blogs. Much material is free online!

# 5 History and evolution of JavaScript

* * *

*   5.1 [How JavaScript was created](#ch006.xhtml_how-javascript-was-created)
*   5.2 [Standardizing JavaScript](#ch006.xhtml_standardizing-javascript)
*   5.3 [Timeline of ECMAScript versions](#ch006.xhtml_timeline-of-ecmascript-versions)
*   5.4 [Ecma Technical Committee 39 (TC39)](#ch006.xhtml_tc39)
*   5.5 [The TC39 process](#ch006.xhtml_tc39-process)
    *   5.5.1 [Tip: Think in individual features and stages, not ECMAScript versions](#ch006.xhtml_tip-think-in-individual-features-and-stages-not-ecmascript-versions)
*   5.6 [FAQ: TC39 process](#ch006.xhtml_tc39-process-faq)
    *   5.6.1 [How is [my favorite proposed feature] doing?](#ch006.xhtml_how-is-my-favorite-proposed-feature-doing)
    *   5.6.2 [Is there an official list of ECMAScript features?](#ch006.xhtml_is-there-an-official-list-of-ecmascript-features)
*   5.7 [Evolving JavaScript: Don’t break the web](#ch006.xhtml_backward-compatibility)

* * *

## 5.1 How JavaScript was created

JavaScript was created in May 1995 in 10 days, by Brendan Eich. Eich worked at Netscape and implemented JavaScript for their web browser, *Netscape Navigator*.

The idea was that major interactive parts of the client-side web were to be implemented in Java. JavaScript was supposed to be a glue language for those parts and to also make HTML slightly more interactive. Given its role of assisting Java, JavaScript had to look like Java. That ruled out existing solutions such as Perl, Python, TCL, and others.

Initially, JavaScript’s name changed several times:

*   Its code name was *Mocha*.
*   In the Netscape Navigator 2.0 betas (September 1995), it was called *LiveScript*.
*   In Netscape Navigator 2.0 beta 3 (December 1995), it got its final name, *JavaScript*.

## 5.2 Standardizing JavaScript

There are two standards for JavaScript:

*   ECMA-262 is hosted by Ecma International. It is the primary standard.
*   ISO/IEC 16262 is hosted by the International Organization for Standardization (ISO) and the International Electrotechnical Commission (IEC). This is a secondary standard.

The language described by these standards is called *ECMAScript*, not *JavaScript*. A different name was chosen because Sun (now Oracle) had a trademark for the latter name. The “ECMA” in “ECMAScript” comes from the organization that hosts the primary standard.

The original name of that organization was *ECMA*, an acronym for *European Computer Manufacturers Association*. It was later changed to *Ecma International* (with “Ecma” being a proper name, not an acronym) because the organization’s activities had expanded beyond Europe. The initial all-caps acronym explains the spelling of ECMAScript.

In principle, JavaScript and ECMAScript mean the same thing. Sometimes the following distinction is made:

*   The term *JavaScript* refers to the language and its implementations.
*   The term *ECMAScript* refers to the language standard and language versions.

Therefore, *ECMAScript 6* is a version of the language (its 6th edition).

## 5.3 Timeline of ECMAScript versions

This is a brief timeline of ECMAScript versions:

*   ECMAScript 1 (June 1997): First version of the standard.
*   ECMAScript 2 (June 1998): Small update to keep ECMA-262 in sync with the ISO standard.
*   ECMAScript 3 (December 1999): Adds many core features – “[…] regular expressions, better string handling, new control statements [do-while, switch], try/catch exception handling, […]”
*   ECMAScript 4 (abandoned in July 2008): Would have been a massive upgrade (with static typing, modules, namespaces, and more), but ended up being too ambitious and dividing the language’s stewards.
*   ECMAScript 5 (December 2009): Brought minor improvements – a few standard library features and [*strict mode*](#ch009.xhtml_strict-mode).
*   ECMAScript 5.1 (June 2011): Another small update to keep Ecma and ISO standards in sync.
*   ECMAScript 6 (June 2015): A large update that fulfilled many of the promises of ECMAScript 4\. This version is the first one whose official name – *ECMAScript 2015* – is based on the year of publication.
*   ECMAScript 2016 (June 2016): First yearly release. The shorter release life cycle resulted in fewer new features compared to the large ES6.
*   ECMAScript 2017 (June 2017). Second yearly release.
*   Subsequent ECMAScript versions (ES2018, etc.) are always ratified in June.

## 5.4 Ecma Technical Committee 39 (TC39)

TC39 is the committee that evolves JavaScript. Its member are, strictly speaking, companies: Adobe, Apple, Facebook, Google, Microsoft, Mozilla, Opera, Twitter, and others. That is, companies that are usually fierce competitors are working together for the good of the language.

Every two months, TC39 has meetings that member-appointed delegates and invited experts attend. The minutes of those meetings are public in [a GitHub repository](https://github.com/tc39/tc39-notes/).

## 5.5 The TC39 process

With ECMAScript 6, two issues with the release process used at that time became obvious:

*   If too much time passes between releases then features that are ready early, have to wait a long time until they can be released. And features that are ready late, risk being rushed to make the deadline.

*   Features were often designed long before they were implemented and used. Design deficiencies related to implementation and use were therefore discovered too late.

In response to these issues, TC39 instituted the new *TC39 process*:

*   ECMAScript features are designed independently and go through stages, starting at 0 (“strawman”), ending at 4 (“finished”).
*   Especially the later stages require prototype implementations and real-world testing, leading to feedback loops between designs and implementations.
*   ECMAScript versions are released once per year and include all features that have reached stage 4 prior to a release deadline.

The result: smaller, incremental releases, whose features have already been field-tested. Fig. [1](#ch006.xhtml_fig:tc39-process-stages) illustrates the TC39 process.

![](media/file8.svg)

Figure 1: Each ECMAScript feature proposal goes through stages that are numbered from 0 to 4\. *Champions* are TC39 members that support the authors of a feature. Test 262 is a suite of tests that checks JavaScript engines for compliance with the language specification.

ES2016 was the first ECMAScript version that was designed according to the TC39 process.

### 5.5.1 Tip: Think in individual features and stages, not ECMAScript versions

Up to and including ES6, it was most common to think about JavaScript in terms of ECMAScript versions – for example, “Does this browser support ES6 yet?”

Starting with ES2016, it’s better to think in individual features: once a feature reaches stage 4, you can safely use it (if it’s supported by the JavaScript engines you are targeting). You don’t have to wait until the next ECMAScript release.

## 5.6 FAQ: TC39 process

### 5.6.1 How is [my favorite proposed feature] doing?

If you are wondering what stages various proposed features are in, consult [the GitHub repository `proposals`](https://github.com/tc39/proposals).

### 5.6.2 Is there an official list of ECMAScript features?

Yes, the TC39 repo lists [finished proposals](https://github.com/tc39/proposals/blob/master/finished-proposals.md) and mentions in which ECMAScript versions they were introduced.

## 5.7 Evolving JavaScript: Don’t break the web

One idea that occasionally comes up is to clean up JavaScript by removing old features and quirks. While the appeal of that idea is obvious, it has significant downsides.

Let’s assume we create a new version of JavaScript that is not backward compatible and fix all of its flaws. As a result, we’d encounter the following problems:

*   JavaScript engines become bloated: they need to support both the old and the new version. The same is true for tools such as IDEs and build tools.
*   Programmers need to know, and be continually conscious of, the differences between the versions.
*   You can either migrate all of an existing code base to the new version (which can be a lot of work). Or you can mix versions and refactoring becomes harder because you can’t move code between versions without changing it.
*   You somehow have to specify per piece of code – be it a file or code embedded in a web page – what version it is written in. Every conceivable solution has pros and cons. For example, [*strict mode*](#ch009.xhtml_strict-mode) is a slightly cleaner version of ES5\. One of the reasons why it wasn’t as popular as it should have been: it was a hassle to opt in via a directive at the beginning of a file or a function.

So what is the solution? Can we have our cake and eat it? The approach that was chosen for ES6 is called “One JavaScript”:

*   New versions are always completely backward compatible (but there may occasionally be minor, hardly noticeable clean-ups).
*   Old features aren’t removed or fixed. Instead, better versions of them are introduced. One example is declaring variables via `let` – which is an improved version of `var`.
*   If aspects of the language are changed, it is done inside new syntactic constructs. That is, you opt in implicitly. For example, `yield` is only a keyword inside generators (which were introduced in ES6). And all code inside modules and classes (both introduced in ES6) is implicitly in strict mode.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 6 FAQ: JavaScript

* * *

*   6.1 [What are good references for JavaScript?](#ch007.xhtml_what-are-good-references-for-javascript)
*   6.2 [How do I find out what JavaScript features are supported where?](#ch007.xhtml_how-do-i-find-out-what-javascript-features-are-supported-where)
*   6.3 [Where can I look up what features are planned for JavaScript?](#ch007.xhtml_where-can-i-look-up-what-features-are-planned-for-javascript)
*   6.4 [Why does JavaScript fail silently so often?](#ch007.xhtml_why-does-javascript-fail-silently-so-often)
*   6.5 [Why can’t we clean up JavaScript, by removing quirks and outdated features?](#ch007.xhtml_why-cant-we-clean-up-javascript-by-removing-quirks-and-outdated-features)
*   6.6 [How can I quickly try out a piece of JavaScript code?](#ch007.xhtml_how-can-i-quickly-try-out-a-piece-of-javascript-code)

* * *

## 6.1 What are good references for JavaScript?

Please consult [§7.3 “JavaScript references”](#ch008.xhtml_javascript-references).

## 6.2 How do I find out what JavaScript features are supported where?

This book usually mentions if a feature is part of ECMAScript 5 (as required by older browsers) or a newer version. For more detailed information (including pre-ES5 versions), there are several good compatibility tables available online:

*   [ECMAScript compatibility tables for various engines](http://kangax.github.io/compat-table/es5/) (by [kangax](https://twitter.com/kangax), [webbedspace](https://twitter.com/webbedspace), [zloirock](https://twitter.com/zloirock))
*   [Node.js compatibility tables](https://node.green) (by [William Kapke](https://twitter.com/williamkapke))
*   Mozilla’s [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript) have tables for each feature that describe relevant ECMAScript versions and browser support.
*   [“Can I use…”](https://caniuse.com/) documents what features (including JavaScript language features) are supported by web browsers.

## 6.3 Where can I look up what features are planned for JavaScript?

Please consult the following sources:

*   [§5.5 “The TC39 process”](#ch006.xhtml_tc39-process) describes how upcoming features are planned.
*   [§5.6 “FAQ: TC39 process”](#ch006.xhtml_tc39-process-faq) answers various questions regarding upcoming features.

## 6.4 Why does JavaScript fail silently so often?

JavaScript often fails silently. Let’s look at two examples.

First example: If the operands of an operator don’t have the appropriate types, they are converted as necessary.

```
> '3' * '5'
15
```

Second example: If an arithmetic computation fails, you get an error value, not an exception.

```
> 1 / 0
Infinity
```

The reason for the silent failures is historical: JavaScript did not have exceptions until ECMAScript 3\. Since then, its designers have tried to avoid silent failures.

## 6.5 Why can’t we clean up JavaScript, by removing quirks and outdated features?

This question is answered in [§5.7 “Evolving JavaScript: Don’t break the web”](#ch006.xhtml_backward-compatibility).

## 6.6 How can I quickly try out a piece of JavaScript code?

[§9.1 “Trying out JavaScript code”](#ch010.xhtml_trying-out-code) explains how to do that.

# 7 The big picture

* * *

*   7.1 [What are you learning in this book?](#ch008.xhtml_what-are-you-learning-in-this-book)
*   7.2 [The structure of browsers and Node.js](#ch008.xhtml_the-structure-of-browsers-and-node.js)
*   7.3 [JavaScript references](#ch008.xhtml_javascript-references)
*   7.4 [Further reading](#ch008.xhtml_further-reading)

* * *

In this chapter, I’d like to paint the big picture: what are you learning in this book, and how does it fit into the overall landscape of web development?

## 7.1 What are you learning in this book?

This book teaches the JavaScript language. It focuses on just the language, but offers occasional glimpses at two platforms where JavaScript can be used:

*   Web browser
*   Node.js

Node.js is important for web development in three ways:

*   You can use it to write server-side software in JavaScript.
*   You can also use it to write software for the command line (think Unix shell, Windows PowerShell, etc.). Many JavaScript-related tools are based on (and executed via) Node.js.
*   Node’s software registry, npm, has become the dominant way of installing tools (such as compilers and build tools) and libraries – even for client-side development.

## 7.2 The structure of browsers and Node.js

![](media/file9.svg)

Figure 2: The structure of the two JavaScript platforms *web browser* and *Node.js*. The APIs “standard library” and “platform API” are hosted on top of a foundational layer with a JavaScript engine and a platform-specific “core”.

The structures of the two JavaScript platforms *web browser* and *Node.js* are similar (fig. [2](#ch008.xhtml_fig:javascript-platforms)):

*   The foundational layer consists of the JavaScript engine and platform-specific “core” functionality.
*   Two APIs are hosted on top of this foundation:
    *   The JavaScript standard library is part of JavaScript proper and runs on top of the engine.
    *   The platform API are also available from JavaScript – it provides access to platform-specific functionality. For example:
        *   In browsers, you need to use the platform-specific API if you want to do anything related to the user interface: react to mouse clicks, play sounds, etc.
        *   In Node.js, the platform-specific API lets you read and write files, download data via HTTP, etc.

## 7.3 JavaScript references

When you have a question about a JavaScript, a web search usually helps. I can recommend the following online sources:

*   [MDN web docs](https://developer.mozilla.org/en-US/): cover various web technologies such as CSS, HTML, JavaScript, and more. An excellent reference.
*   [Node.js Docs](https://nodejs.org/en/docs/): document the Node.js API.
*   [ExploringJS.com](https://exploringjs.com): My other books on JavaScript go into greater detail than this book and are free to read online. You can look up features by ECMAScript version:
    *   ES1–ES5: [*Speaking JavaScript*](http://speakingjs.com/)
    *   ES6: [*Exploring ES6*](https://exploringjs.com/es6.html)
    *   ES2016–ES2017: [*Exploring ES2016 and ES2017*](https://exploringjs.com/es2016-es2017.html)
    *   Etc.

## 7.4 Further reading

*   [§46 “Next steps: overview of web development”](#ch047.xhtml_ch_next-steps) provides a more comprehensive look at web development.

# 8 Syntax

* * *

*   8.1 [An overview of JavaScript’s syntax](#ch009.xhtml_an-overview-of-javascripts-syntax)
    *   8.1.1 [Basic syntax](#ch009.xhtml_basic-syntax)
    *   8.1.2 [Modules](#ch009.xhtml_modules)
    *   8.1.3 [Legal variable and property names](#ch009.xhtml_legal-variable-and-property-names)
    *   8.1.4 [Casing styles](#ch009.xhtml_casing-styles)
    *   8.1.5 [Capitalization of names](#ch009.xhtml_capitalization-of-names)
    *   8.1.6 [More naming conventions](#ch009.xhtml_more-naming-conventions)
    *   8.1.7 [Where to put semicolons?](#ch009.xhtml_where-to-put-semicolons)
*   8.2 [(Advanced)](#ch009.xhtml_advanced)
*   8.3 [Identifiers](#ch009.xhtml_identifiers)
    *   8.3.1 [Valid identifiers (variable names, etc.)](#ch009.xhtml_valid-identifiers-variable-names-etc.)
    *   8.3.2 [Reserved words](#ch009.xhtml_reserved-words)
*   8.4 [Statement vs. expression](#ch009.xhtml_statement-vs-expression)
    *   8.4.1 [Statements](#ch009.xhtml_statements)
    *   8.4.2 [Expressions](#ch009.xhtml_expressions)
    *   8.4.3 [What is allowed where?](#ch009.xhtml_what-is-allowed-where)
*   8.5 [Ambiguous syntax](#ch009.xhtml_ambiguous-syntax)
    *   8.5.1 [Same syntax: function declaration and function expression](#ch009.xhtml_same-syntax-function-declaration-and-function-expression)
    *   8.5.2 [Same syntax: object literal and block](#ch009.xhtml_same-syntax-object-literal-and-block)
    *   8.5.3 [Disambiguation](#ch009.xhtml_disambiguation)
*   8.6 [Semicolons](#ch009.xhtml_semicolons)
    *   8.6.1 [Rule of thumb for semicolons](#ch009.xhtml_rule-of-thumb-for-semicolons)
    *   8.6.2 [Semicolons: control statements](#ch009.xhtml_semicolons-control-statements)
*   8.7 [Automatic semicolon insertion (ASI)](#ch009.xhtml_automatic-semicolon-insertion-asi)
    *   8.7.1 [ASI triggered unexpectedly](#ch009.xhtml_asi-triggered-unexpectedly)
    *   8.7.2 [ASI unexpectedly not triggered](#ch009.xhtml_asi-unexpectedly-not-triggered)
*   8.8 [Semicolons: best practices](#ch009.xhtml_semicolons-best-practices)
*   8.9 [Strict mode vs. sloppy mode](#ch009.xhtml_strict-mode)
    *   8.9.1 [Switching on strict mode](#ch009.xhtml_switching-on-strict-mode)
    *   8.9.2 [Improvements in strict mode](#ch009.xhtml_improvements-in-strict-mode)

* * *

## 8.1 An overview of JavaScript’s syntax

### 8.1.1 Basic syntax

Comments:

```
[](#cb6-1)// single-line comment
[](#cb6-2)
[](#cb6-3)/*
[](#cb6-4)Comment with
[](#cb6-5)multiple lines
[](#cb6-6)*/
```

*Primitive* (atomic) values:

```
[](#cb7-1)// Booleans
[](#cb7-2)true
[](#cb7-3)false
[](#cb7-4)
[](#cb7-5)// Numbers (JavaScript only has a single type for numbers)
[](#cb7-6)-123
[](#cb7-7)1.141
[](#cb7-8)
[](#cb7-9)// Strings (JavaScript has no type for characters)
[](#cb7-10)'abc'
[](#cb7-11)"abc"
```

An *assertion* describes what the result of a computation is expected to look like and throws an exception if those expectations aren’t correct. For example, the following assertion states that the result of the computation 7 plus 1 must be 8:

```
[](#cb8-1)assert.equal(7 + 1, 8);
```

`assert.equal()` is a method call (the object is `assert`, the method is `.equal()`) with two arguments: the actual result and the expected result. It is part of a Node.js assertion API that is explained [later in this book](#ch011.xhtml_ch_assertion-api).

Logging to [the console](#ch010.xhtml_browser-consoles) of a browser or Node.js:

```
[](#cb9-1)// Printing a value to standard out (another method call)
[](#cb9-2)console.log('Hello!');
[](#cb9-3)
[](#cb9-4)// Printing error information to standard error
[](#cb9-5)console.error('Something went wrong!');
```

Operators:

```
[](#cb10-1)// Operators for booleans
[](#cb10-2)assert.equal(true && false, false); // And
[](#cb10-3)assert.equal(true || false, true); // Or
[](#cb10-4)
[](#cb10-5)// Operators for numbers
[](#cb10-6)assert.equal(3 + 4, 7);
[](#cb10-7)assert.equal(5 - 1, 4);
[](#cb10-8)assert.equal(3 * 4, 12);
[](#cb10-9)assert.equal(9 / 3, 3);
[](#cb10-10)
[](#cb10-11)// Operators for strings
[](#cb10-12)assert.equal('a' + 'b', 'ab');
[](#cb10-13)assert.equal('I see ' + 3 + ' monkeys', 'I see 3 monkeys');
[](#cb10-14)
[](#cb10-15)// Comparison operators
[](#cb10-16)assert.equal(3 < 4, true);
[](#cb10-17)assert.equal(3 <= 4, true);
[](#cb10-18)assert.equal('abc' === 'abc', true);
[](#cb10-19)assert.equal('abc' !== 'def', true);
```

Declaring variables:

```
[](#cb11-1)let x; // declaring x (mutable)
[](#cb11-2)x = 3 * 5; // assign a value to x
[](#cb11-3)
[](#cb11-4)let y = 3 * 5; // declaring and assigning
[](#cb11-5)
[](#cb11-6)const z = 8; // declaring z (immutable)
```

Control flow statements:

```
[](#cb12-1)// Conditional statement
[](#cb12-2)if (x < 0) { // is x less than zero?
[](#cb12-3)  x = -x;
[](#cb12-4)}
```

Ordinary function declarations:

```
[](#cb13-1)// add1() has the parameters a and b
[](#cb13-2)function add1(a, b) {
[](#cb13-3)  return a + b;
[](#cb13-4)}
[](#cb13-5)// Calling function add1()
[](#cb13-6)assert.equal(add1(5, 2), 7);
```

Arrow function expressions (used especially as arguments of function calls and method calls):

```
[](#cb14-1)const add2 = (a, b) => { return a + b };
[](#cb14-2)// Calling function add2()
[](#cb14-3)assert.equal(add2(5, 2), 7);
[](#cb14-4)
[](#cb14-5)// Equivalent to add2:
[](#cb14-6)const add3 = (a, b) => a + b;
```

The previous code contains the following two arrow functions (the terms *expression* and *statement* are explained [later in this chapter](#ch009.xhtml_statement-vs-expression)):

```
[](#cb15-1)// An arrow function whose body is a code block
[](#cb15-2)(a, b) => { return a + b }
[](#cb15-3)
[](#cb15-4)// An arrow function whose body is an expression
[](#cb15-5)(a, b) => a + b
```

Objects:

```
[](#cb16-1)// Creating a plain object via an object literal
[](#cb16-2)const obj = {
[](#cb16-3)  first: 'Jane', // property
[](#cb16-4)  last: 'Doe', // property
[](#cb16-5)  getFullName() { // property (method)
[](#cb16-6)    return this.first + ' ' + this.last;
[](#cb16-7)  },
[](#cb16-8)};
[](#cb16-9)
[](#cb16-10)// Getting a property value
[](#cb16-11)assert.equal(obj.first, 'Jane');
[](#cb16-12)// Setting a property value
[](#cb16-13)obj.first = 'Janey';
[](#cb16-14)
[](#cb16-15)// Calling the method
[](#cb16-16)assert.equal(obj.getFullName(), 'Janey Doe');
```

Arrays (Arrays are also objects):

```
[](#cb17-1)// Creating an Array via an Array literal
[](#cb17-2)const arr = ['a', 'b', 'c'];
[](#cb17-3)
[](#cb17-4)// Getting an Array element
[](#cb17-5)assert.equal(arr[1], 'b');
[](#cb17-6)// Setting an Array element
[](#cb17-7)arr[1] = 'β';
```

### 8.1.2 Modules

Each module is a single file. Consider, for example, the following two files with modules in them:

```
file-tools.mjs
main.mjs
```

The module in `file-tools.mjs` exports its function `isTextFilePath()`:

```
[](#cb19-1)export function isTextFilePath(filePath) {
[](#cb19-2)  return filePath.endsWith('.txt');
[](#cb19-3)}
```

The module in `main.mjs` imports the whole module `path` and the function `isTextFilePath()`:

```
[](#cb20-1)// Import whole module as namespace object `path`
[](#cb20-2)import * as path from 'path';
[](#cb20-3)// Import a single export of module file-tools.mjs
[](#cb20-4)import {isTextFilePath} from './file-tools.mjs';
```

### 8.1.3 Legal variable and property names

The grammatical category of variable names and property names is called *identifier*.

Identifiers are allowed to have the following characters:

*   Unicode letters: `A`–`Z`, `a`–`z` (etc.)
*   `$`, `_`
*   Unicode digits: `0`–`9` (etc.)
    *   Variable names can’t start with a digit

Some words have special meaning in JavaScript and are called *reserved*. Examples include: `if`, `true`, `const`.

Reserved words can’t be used as variable names:

```
[](#cb21-1)const if = 123;
[](#cb21-2)  // SyntaxError: Unexpected token if
```

But they are allowed as names of properties:

```
> const obj = { if: 123 };
> obj.if
123
```

### 8.1.4 Casing styles

Common casing styles for concatenating words are:

*   Camel case: `threeConcatenatedWords`
*   Underscore case (also called *snake case*): `three_concatenated_words`
*   Dash case (also called *kebab case*): `three-concatenated-words`

### 8.1.5 Capitalization of names

In general, JavaScript uses camel case, except for constants.

Lowercase:

*   Functions, variables: `myFunction`
*   Methods: `obj.myMethod`
*   CSS:
    *   CSS entity: `special-class`
    *   Corresponding JavaScript variable: `specialClass`

Uppercase:

*   Classes: `MyClass`
*   Constants: `MY_CONSTANT`
    *   Constants are also often written in camel case: `myConstant`

### 8.1.6 More naming conventions

The following naming conventions are popular in JavaScript.

If the name of a parameter starts with an underscore (or is an underscore) it means that this parameter is not used – for example:

```
[](#cb23-1)arr.map((_x, i) => i)
```

If the name of a property of an object starts with an underscore then that property is considered private:

```
[](#cb24-1)class ValueWrapper {
[](#cb24-2)  constructor(value) {
[](#cb24-3)    this._value = value;
[](#cb24-4)  }
[](#cb24-5)}
```

### 8.1.7 Where to put semicolons?

At the end of a statement:

```
[](#cb25-1)const x = 123;
[](#cb25-2)func();
```

But not if that statement ends with a curly brace:

```
[](#cb26-1)while (false) {
[](#cb26-2)  // ···
[](#cb26-3)} // no semicolon
[](#cb26-4)
[](#cb26-5)function func() {
[](#cb26-6)  // ···
[](#cb26-7)} // no semicolon
```

However, adding a semicolon after such a statement is not a syntax error – it is interpreted as an empty statement:

```
[](#cb27-1)// Function declaration followed by empty statement:
[](#cb27-2)function func() {
[](#cb27-3)  // ···
[](#cb27-4)};
```

![](media/file7.svg)  **Quiz: basic**

See [quiz app](#ch012.xhtml_quizzes).

## 8.2 (Advanced)

All remaining sections of this chapter are advanced.

## 8.3 Identifiers

### 8.3.1 Valid identifiers (variable names, etc.)

First character:

*   Unicode letter (including accented characters such as `é` and `ü` and characters from non-latin alphabets, such as `α`)
*   `$`
*   `_`

Subsequent characters:

*   Legal first characters
*   Unicode digits (including Eastern Arabic numerals)
*   Some other Unicode marks and punctuations

Examples:

```
[](#cb28-1)const ε = 0.0001;
[](#cb28-2)const строка = '';
[](#cb28-3)let _tmp = 0;
[](#cb28-4)const $foo2 = true;
```

### 8.3.2 Reserved words

Reserved words can’t be variable names, but they can be property names.

All JavaScript *keywords* are reserved words:

> `await` `break` `case` `catch` `class` `const` `continue` `debugger` `default` `delete` `do` `else` `export` `extends` `finally` `for` `function` `if` `import` `in` `instanceof` `let` `new` `return` `static` `super` `switch` `this` `throw` `try` `typeof` `var` `void` `while` `with` `yield`

The following tokens are also keywords, but currently not used in the language:

> `enum` `implements` `package` `protected` `interface` `private` `public`

The following literals are reserved words:

> `true` `false` `null`

Technically, these words are not reserved, but you should avoid them, too, because they effectively are keywords:

> `Infinity` `NaN` `undefined` `async`

You shouldn’t use the names of global variables (`String`, `Math`, etc.) for your own variables and parameters, either.

## 8.4 Statement vs. expression

In this section, we explore how JavaScript distinguishes two kinds of syntactic constructs: *statements* and *expressions*. Afterward, we’ll see that that can cause problems because the same syntax can mean different things, depending on where it is used.

![](media/file5.svg)  **We pretend there are only statements and expressions**

For the sake of simplicity, we pretend that there are only statements and expressions in JavaScript.

### 8.4.1 Statements

A *statement* is a piece of code that can be executed and performs some kind of action. For example, `if` is a statement:

```
[](#cb29-1)let myStr;
[](#cb29-2)if (myBool) {
[](#cb29-3)  myStr = 'Yes';
[](#cb29-4)} else {
[](#cb29-5)  myStr = 'No';
[](#cb29-6)}
```

One more example of a statement: a function declaration.

```
[](#cb30-1)function twice(x) {
[](#cb30-2)  return x + x;
[](#cb30-3)}
```

### 8.4.2 Expressions

An *expression* is a piece of code that can be *evaluated* to produce a value. For example, the code between the parentheses is an expression:

```
[](#cb31-1)let myStr = (myBool ? 'Yes' : 'No');
```

The operator `_?_:_` used between the parentheses is called the *ternary operator*. It is the expression version of the `if` statement.

Let’s look at more examples of expressions. We enter expressions and the REPL evaluates them for us:

```
> 'ab' + 'cd'
'abcd'
> Number('123')
123
> true || false
true
```

### 8.4.3 What is allowed where?

The current location within JavaScript source code determines which kind of syntactic constructs you are allowed to use:

*   The body of a function must be a sequence of statements:

    ```
    [](#cb33-1)function max(x, y) {
    [](#cb33-2)  if (x > y) {
    [](#cb33-3)    return x;
    [](#cb33-4)  } else {
    [](#cb33-5)    return y;
    [](#cb33-6)  }
    [](#cb33-7)}
    ```

*   The arguments of a function call or a method call must be expressions:

    ```
    [](#cb34-1)console.log('ab' + 'cd', Number('123'));
    ```

However, expressions can be used as statements. Then they are called *expression statements*. The opposite is not true: when the context requires an expression, you can’t use a statement.

The following code demonstrates that any expression `bar()` can be either expression or statement – it depends on the context:

```
[](#cb35-1)function f() {
[](#cb35-2)  console.log(bar()); // bar() is expression
[](#cb35-3)  bar(); // bar(); is (expression) statement 
[](#cb35-4)}
```

## 8.5 Ambiguous syntax

JavaScript has several programming constructs that are syntactically ambiguous: the same syntax is interpreted differently, depending on whether it is used in statement context or in expression context. This section explores the phenomenon and the pitfalls it causes.

### 8.5.1 Same syntax: function declaration and function expression

A *function declaration* is a statement:

```
[](#cb36-1)function id(x) {
[](#cb36-2)  return x;
[](#cb36-3)}
```

A *function expression* is an expression (right-hand side of `=`):

```
[](#cb37-1)const id = function me(x) {
[](#cb37-2)  return x;
[](#cb37-3)};
```

### 8.5.2 Same syntax: object literal and block

In the following code, `{}` is an *object literal*: an expression that creates an empty object.

```
[](#cb38-1)const obj = {};
```

This is an empty code block (a statement):

```
[](#cb39-1){
[](#cb39-2)}
```

### 8.5.3 Disambiguation

The ambiguities are only a problem in statement context: If the JavaScript parser encounters ambiguous syntax, it doesn’t know if it’s a plain statement or an expression statement. For example:

*   If a statement starts with `function`: Is it a function declaration or a function expression?
*   If a statement starts with `{`: Is it an object literal or a code block?

To resolve the ambiguity, statements starting with `function` or `{` are never interpreted as expressions. If you want an expression statement to start with either one of these tokens, you must wrap it in parentheses:

```
[](#cb40-1)(function (x) { console.log(x) })('abc');
[](#cb40-2)
[](#cb40-3)// Output:
[](#cb40-4)// 'abc'
```

In this code:

1.  We first create a function via a function expression:

    ```
    [](#cb41-1)function (x) { console.log(x) }
    ```

2.  Then we invoke that function: `('abc')`

The code fragment shown in (1) is only interpreted as an expression because we wrap it in parentheses. If we didn’t, we would get a syntax error because then JavaScript expects a function declaration and complains about the missing function name. Additionally, you can’t put a function call immediately after a function declaration.

Later in this book, we’ll see more examples of pitfalls caused by syntactic ambiguity:

*   [Assigning via object destructuring](#ch038.xhtml_assigning-via-object-destructuring)
*   [Returning an object literal from an arrow function](#ch026.xhtml_returning-object-literal-from-arrow-function)

## 8.6 Semicolons

### 8.6.1 Rule of thumb for semicolons

Each statement is terminated by a semicolon:

```
[](#cb42-1)const x = 3;
[](#cb42-2)someFunction('abc');
[](#cb42-3)i++;
```

except statements ending with blocks:

```
[](#cb43-1)function foo() {
[](#cb43-2)  // ···
[](#cb43-3)}
[](#cb43-4)if (y > 0) {
[](#cb43-5)  // ···
[](#cb43-6)}
```

The following case is slightly tricky:

```
[](#cb44-1)const func = () => {}; // semicolon!
```

The whole `const` declaration (a statement) ends with a semicolon, but inside it, there is an arrow function expression. That is, it’s not the statement per se that ends with a curly brace; it’s the embedded arrow function expression. That’s why there is a semicolon at the end.

### 8.6.2 Semicolons: control statements

The body of a control statement is itself a statement. For example, this is the syntax of the `while` loop:

```
[](#cb45-1)while (condition)
[](#cb45-2)  statement
```

The body can be a single statement:

```
[](#cb46-1)while (a > 0) a--;
```

But blocks are also statements and therefore legal bodies of control statements:

```
[](#cb47-1)while (a > 0) {
[](#cb47-2)  a--;
[](#cb47-3)}
```

If you want a loop to have an empty body, your first option is an empty statement (which is just a semicolon):

```
[](#cb48-1)while (processNextItem() > 0);
```

Your second option is an empty block:

```
[](#cb49-1)while (processNextItem() > 0) {}
```

## 8.7 Automatic semicolon insertion (ASI)

While I recommend to always write semicolons, most of them are optional in JavaScript. The mechanism that makes this possible is called *automatic semicolon insertion* (ASI). In a way, it corrects syntax errors.

ASI works as follows. Parsing of a statement continues until there is either:

*   A semicolon
*   A line terminator followed by an illegal token

In other words, ASI can be seen as inserting semicolons at line breaks. The next subsections cover the pitfalls of ASI.

### 8.7.1 ASI triggered unexpectedly

The good news about ASI is that – if you don’t rely on it and always write semicolons – there is only one pitfall that you need to be aware of. It is that JavaScript forbids line breaks after some tokens. If you do insert a line break, a semicolon will be inserted, too.

The token where this is most practically relevant is `return`. Consider, for example, the following code:

```
[](#cb50-1)return
[](#cb50-2){
[](#cb50-3)  first: 'jane'
[](#cb50-4)};
```

This code is parsed as:

```
[](#cb51-1)return;
[](#cb51-2){
[](#cb51-3)  first: 'jane';
[](#cb51-4)}
[](#cb51-5);
```

That is:

*   Return statement without operand: `return;`
*   Start of code block: `{`
*   Expression statement `'jane';` with [label](#ch024.xhtml_labels) `first:`
*   End of code block: `}`
*   Empty statement: `;`

Why does JavaScript do this? It protects against accidentally returning a value in a line after a `return`.

### 8.7.2 ASI unexpectedly not triggered

In some cases, ASI is *not* triggered when you think it should be. That makes life more complicated for people who don’t like semicolons because they need to be aware of those cases. The following are three examples. There are more.

**Example 1:** Unintended function call.

```
[](#cb52-1)a = b + c
[](#cb52-2)(d + e).print()
```

Parsed as:

```
[](#cb53-1)a = b + c(d + e).print();
```

**Example 2:** Unintended division.

```
[](#cb54-1)a = b
[](#cb54-2)/hi/g.exec(c).map(d)
```

Parsed as:

```
[](#cb55-1)a = b / hi / g.exec(c).map(d);
```

**Example 3:** Unintended property access.

```
[](#cb56-1)someFunction()
[](#cb56-2)['ul', 'ol'].map(x => x + x)
```

Executed as:

```
[](#cb57-1)const propKey = ('ul','ol'); // comma operator
[](#cb57-2)assert.equal(propKey, 'ol');
[](#cb57-3)
[](#cb57-4)someFunction()[propKey].map(x => x + x);
```

## 8.8 Semicolons: best practices

I recommend that you always write semicolons:

*   I like the visual structure it gives code – you clearly see when a statement ends.
*   There are less rules to keep in mind.
*   The majority of JavaScript programmers use semicolons.

However, there are also many people who don’t like the added visual clutter of semicolons. If you are one of them: Code without them *is* legal. I recommend that you use tools to help you avoid mistakes. The following are two examples:

*   The automatic code formatter [Prettier](https://prettier.io) can be configured to not use semicolons. It then automatically fixes problems. For example, if it encounters a line that starts with a square bracket, it prefixes that line with a semicolon.
*   The static checker [ESLint](https://eslint.org) has [a rule](https://eslint.org/docs/rules/semi) that you tell your preferred style (always semicolons or as few semicolons as possible) and that warns you about critical issues.

## 8.9 Strict mode vs. sloppy mode

Starting with ECMAScript 5, JavaScript has two *modes* in which JavaScript can be executed:

*   Normal “sloppy” mode is the default in scripts (code fragments that are a precursor to modules and supported by browsers).
*   Strict mode is the default in modules and classes, and can be switched on in scripts (how, is explained later). In this mode, several pitfalls of normal mode are removed and more exceptions are thrown.

You’ll rarely encounter sloppy mode in modern JavaScript code, which is almost always located in modules. In this book, I assume that strict mode is always switched on.

### 8.9.1 Switching on strict mode

In script files and CommonJS modules, you switch on strict mode for a complete file, by putting the following code in the first line:

```
[](#cb58-1)'use strict';
```

The neat thing about this “directive” is that ECMAScript versions before 5 simply ignore it: it’s an expression statement that does nothing.

You can also switch on strict mode for just a single function:

```
[](#cb59-1)function functionInStrictMode() {
[](#cb59-2)  'use strict';
[](#cb59-3)}
```

### 8.9.2 Improvements in strict mode

Let’s look at three things that strict mode does better than sloppy mode. Just in this one section, all code fragments are executed in sloppy mode.

#### 8.9.2.1 Sloppy mode pitfall: changing an undeclared variable creates a global variable

In non-strict mode, changing an undeclared variable creates a global variable.

```
[](#cb60-1)function sloppyFunc() {
[](#cb60-2)  undeclaredVar1 = 123;
[](#cb60-3)}
[](#cb60-4)sloppyFunc();
[](#cb60-5)// Created global variable `undeclaredVar1`:
[](#cb60-6)assert.equal(undeclaredVar1, 123);
```

Strict mode does it better and throws a `ReferenceError`. That makes it easier to detect typos.

```
[](#cb61-1)function strictFunc() {
[](#cb61-2)  'use strict';
[](#cb61-3)  undeclaredVar2 = 123;
[](#cb61-4)}
[](#cb61-5)assert.throws(
[](#cb61-6)  () => strictFunc(),
[](#cb61-7)  {
[](#cb61-8)    name: 'ReferenceError',
[](#cb61-9)    message: 'undeclaredVar2 is not defined',
[](#cb61-10)  });
```

The `assert.throws()` states that its first argument, a function, throws a `ReferenceError` when it is called.

#### 8.9.2.2 Function declarations are block-scoped in strict mode, function-scoped in sloppy mode

In strict mode, a variable created via a function declaration only exists within the innermost enclosing block:

```
[](#cb62-1)function strictFunc() {
[](#cb62-2)  'use strict';
[](#cb62-3)  {
[](#cb62-4)    function foo() { return 123 }
[](#cb62-5)  }
[](#cb62-6)  return foo(); // ReferenceError
[](#cb62-7)}
[](#cb62-8)assert.throws(
[](#cb62-9)  () => strictFunc(),
[](#cb62-10)  {
[](#cb62-11)    name: 'ReferenceError',
[](#cb62-12)    message: 'foo is not defined',
[](#cb62-13)  });
```

In sloppy mode, function declarations are function-scoped:

```
[](#cb63-1)function sloppyFunc() {
[](#cb63-2)  {
[](#cb63-3)    function foo() { return 123 }
[](#cb63-4)  }
[](#cb63-5)  return foo(); // works
[](#cb63-6)}
[](#cb63-7)assert.equal(sloppyFunc(), 123);
```

#### 8.9.2.3 Sloppy mode doesn’t throw exceptions when changing immutable data

In strict mode, you get an exception if you try to change immutable data:

```
[](#cb64-1)function strictFunc() {
[](#cb64-2)  'use strict';
[](#cb64-3)  true.prop = 1; // TypeError
[](#cb64-4)}
[](#cb64-5)assert.throws(
[](#cb64-6)  () => strictFunc(),
[](#cb64-7)  {
[](#cb64-8)    name: 'TypeError',
[](#cb64-9)    message: "Cannot create property 'prop' on boolean 'true'",
[](#cb64-10)  });
```

In sloppy mode, the assignment fails silently:

```
[](#cb65-1)function sloppyFunc() {
[](#cb65-2)  true.prop = 1; // fails silently
[](#cb65-3)  return true.prop;
[](#cb65-4)}
[](#cb65-5)assert.equal(sloppyFunc(), undefined);
```

![](media/file1.svg)  **Further reading: sloppy mode**

For more information on how sloppy mode differs from strict mode, see [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode).

![](media/file7.svg)  **Quiz: advanced**

See [quiz app](#ch012.xhtml_quizzes).

# 9 Consoles: interactive JavaScript command lines

* * *

*   9.1 [Trying out JavaScript code](#ch010.xhtml_trying-out-code)
    *   9.1.1 [Browser consoles](#ch010.xhtml_browser-consoles)
    *   9.1.2 [The Node.js REPL](#ch010.xhtml_the-node.js-repl)
    *   9.1.3 [Other options](#ch010.xhtml_other-options)
*   9.2 [The `console.*` API: printing data and more](#ch010.xhtml_the-console.-api-printing-data-and-more)
    *   9.2.1 [Printing values: `console.log()` (stdout)](#ch010.xhtml_printing-values-console.log-stdout)
    *   9.2.2 [Printing error information: `console.error()` (stderr)](#ch010.xhtml_printing-error-information-console.error-stderr)
    *   9.2.3 [Printing nested objects via `JSON.stringify()`](#ch010.xhtml_printing-nested-objects-via-json.stringify)

* * *

## 9.1 Trying out JavaScript code

You have many options for quickly running pieces of JavaScript code. The following subsections describe a few of them.

### 9.1.1 Browser consoles

Web browsers have so-called *consoles*: interactive command lines to which you can print text via `console.log()` and where you can run pieces of code. How to open the console differs from browser to browser. Fig. [3](#ch010.xhtml_fig:chrome-console) shows the console of Google Chrome.

To find out how to open the console in your web browser, you can do a web search for “console «name-of-your-browser»”. These are pages for a few commonly used web browsers:

*   [Apple Safari](https://developer.apple.com/safari/tools/)
*   [Google Chrome](https://developers.google.com/web/tools/chrome-devtools/console/)
*   [Microsoft Edge](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide/console)
*   [Mozilla Firefox](https://developer.mozilla.org/en-US/docs/Tools/Web_Console/Opening_the_Web_Console)

![](media/file10.png)

Figure 3: The console of the web browser “Google Chrome” is open (in the bottom half of window) while visiting a web page.

### 9.1.2 The Node.js REPL

*REPL* stands for *read-eval-print loop* and basically means *command line*. To use it, you must first start Node.js from an operating system command line, via the command `node`. Then an interaction with it looks as depicted in fig. [4](#ch010.xhtml_fig:nodejs-repl): The text after `>` is input from the user; everything else is output from Node.js.

![](media/file11.png)

Figure 4: Starting and using the Node.js REPL (interactive command line).

![](media/file0.svg)  **Reading: REPL interactions**

I occasionally demonstrate JavaScript via REPL interactions. Then I also use greater-than symbols (`>`) to mark input – for example:

```
> 3 + 5
8
```

### 9.1.3 Other options

Other options include:

*   There are many web apps that let you experiment with JavaScript in web browsers – for example, [Babel’s REPL](https://babeljs.io/repl).

*   There are also native apps and IDE plugins for running JavaScript.

![](media/file4.svg)  **Consoles often run in non-strict mode**

In modern JavaScript, most code (e.g., modules) is executed in [strict mode](#ch009.xhtml_strict-mode). However, consoles often run in non-strict mode. Therefore, you may occasionally get slightly different results when using a console to execute code from this book.

## 9.2 The `console.*` API: printing data and more

In browsers, the console is something you can bring up that is normally hidden. For Node.js, the console is the terminal that Node.js is currently running in.

The full `console.*` API is documented [on MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/console) and [on the Node.js website](https://nodejs.org/api/console.html). It is not part of the JavaScript language standard, but much functionality is supported by both browsers and Node.js.

In this chapter, we only look at the following two methods for printing data (“printing” means displaying in the console):

*   `console.log()`
*   `console.error()`

### 9.2.1 Printing values: `console.log()` (stdout)

There are two variants of this operation:

```
[](#cb67-1)console.log(...values: any[]): void
[](#cb67-2)console.log(pattern: string, ...values: any[]): void
```

#### 9.2.1.1 Printing multiple values

The first variant prints (text representations of) values on the console:

```
[](#cb68-1)console.log('abc', 123, true);
[](#cb68-2)// Output:
[](#cb68-3)// abc 123 true
```

At the end, `console.log()` always prints a newline. Therefore, if you call it with zero arguments, it just prints a newline.

#### 9.2.1.2 Printing a string with substitutions

The second variant performs string substitution:

```
[](#cb69-1)console.log('Test: %s %j', 123, 'abc');
[](#cb69-2)// Output:
[](#cb69-3)// Test: 123 "abc"
```

These are some of the directives you can use for substitutions:

*   `%s` converts the corresponding value to a string and inserts it.

    ```
    [](#cb70-1)console.log('%s %s', 'abc', 123);
    [](#cb70-2)// Output:
    [](#cb70-3)// abc 123
    ```

*   `%o` inserts a string representation of an object.

    ```
    [](#cb71-1)console.log('%o', {foo: 123, bar: 'abc'});
    [](#cb71-2)// Output:
    [](#cb71-3)// { foo: 123, bar: 'abc' }
    ```

*   `%j` converts a value to a JSON string and inserts it.

    ```
    [](#cb72-1)console.log('%j', {foo: 123, bar: 'abc'});
    [](#cb72-2)// Output:
    [](#cb72-3)// {"foo":123,"bar":"abc"}
    ```

*   `%%` inserts a single `%`.

    ```
    [](#cb73-1)console.log('%s%%', 99);
    [](#cb73-2)// Output:
    [](#cb73-3)// 99%
    ```

### 9.2.2 Printing error information: `console.error()` (stderr)

`console.error()` works the same as `console.log()`, but what it logs is considered error information. For Node.js, that means that the output goes to stderr instead of stdout on Unix.

### 9.2.3 Printing nested objects via `JSON.stringify()`

[`JSON.stringify()`](#ch046.xhtml_JSON.stringify) is occasionally useful for printing nested objects:

```
[](#cb74-1)console.log(JSON.stringify({first: 'Jane', last: 'Doe'}, null, 2));
```

Output:

```
{
  "first": "Jane",
  "last": "Doe"
}
```

# 10 Assertion API

* * *

*   10.1 [Assertions in software development](#ch011.xhtml_assertions-in-software-development)
*   10.2 [How assertions are used in this book](#ch011.xhtml_how-assertions-are-used-in-this-book)
    *   10.2.1 [Documenting results in code examples via assertions](#ch011.xhtml_documenting-results-in-code-examples-via-assertions)
    *   10.2.2 [Implementing test-driven exercises via assertions](#ch011.xhtml_implementing-test-driven-exercises-via-assertions)
*   10.3 [Normal comparison vs. deep comparison](#ch011.xhtml_normal-comparison-vs.-deep-comparison)
*   10.4 [Quick reference: module `assert`](#ch011.xhtml_quick-reference-module-assert)
    *   10.4.1 [Normal equality](#ch011.xhtml_normal-equality)
    *   10.4.2 [Deep equality](#ch011.xhtml_deep-equality)
    *   10.4.3 [Expecting exceptions](#ch011.xhtml_expecting-exceptions)
    *   10.4.4 [Another tool function](#ch011.xhtml_another-tool-function)

* * *

## 10.1 Assertions in software development

In software development, *assertions* state facts about values or pieces of code that must be true. If they aren’t, an exception is thrown. Node.js supports assertions via its built-in module `assert` – for example:

```
[](#cb76-1)import {strict as assert} from 'assert';
[](#cb76-2)assert.equal(3 + 5, 8);
```

This assertion states that the expected result of 3 plus 5 is 8\. The import statement uses [the recommended `strict` version](https://nodejs.org/api/assert.html#assert_strict_mode) of `assert`.

## 10.2 How assertions are used in this book

In this book, assertions are used in two ways: to document results in code examples and to implement test-driven exercises.

### 10.2.1 Documenting results in code examples via assertions

In code examples, assertions express expected results. Take, for example, the following function:

```
[](#cb77-1)function id(x) {
[](#cb77-2)  return x;
[](#cb77-3)}
```

`id()` returns its parameter. We can show it in action via an assertion:

```
[](#cb78-1)assert.equal(id('abc'), 'abc');
```

In the examples, I usually omit the statement for importing `assert`.

The motivation behind using assertions is:

*   You can specify precisely what is expected.
*   Code examples can be tested automatically, which ensures that they really work.

### 10.2.2 Implementing test-driven exercises via assertions

The exercises for this book are test-driven, via the test framework AVA. Checks inside the tests are made via methods of `assert`.

The following is an example of such a test:

```
[](#cb79-1)// For the exercise, you must implement the function hello().
[](#cb79-2)// The test checks if you have done it properly.
[](#cb79-3)test('First exercise', t => {
[](#cb79-4)  assert.equal(hello('world'), 'Hello world!');
[](#cb79-5)  assert.equal(hello('Jane'), 'Hello Jane!');
[](#cb79-6)  assert.equal(hello('John'), 'Hello John!');
[](#cb79-7)  assert.equal(hello(''), 'Hello !');
[](#cb79-8)});
```

For more information, consult [§11 “Getting started with quizzes and exercises”](#ch012.xhtml_ch_quizzes-exercises).

## 10.3 Normal comparison vs. deep comparison

The strict `equal()` uses `===` to compare values. Therefore, an object is only equal to itself – even if another object has the same content (because `===` does not compare the contents of objects, only their identities):

```
[](#cb80-1)assert.notEqual({foo: 1}, {foo: 1});
```

`deepEqual()` is a better choice for comparing objects:

```
[](#cb81-1)assert.deepEqual({foo: 1}, {foo: 1});
```

This method works for Arrays, too:

```
[](#cb82-1)assert.notEqual(['a', 'b', 'c'], ['a', 'b', 'c']);
[](#cb82-2)assert.deepEqual(['a', 'b', 'c'], ['a', 'b', 'c']);
```

## 10.4 Quick reference: module `assert`

For the full documentation, see [the Node.js docs](https://nodejs.org/api/assert.html).

### 10.4.1 Normal equality

*   `function equal(actual: any, expected: any, message?: string): void`

    `actual === expected` must be `true`. If not, an `AssertionError` is thrown.

    ```
    [](#cb83-1)assert.equal(3+3, 6);
    ```

*   `function notEqual(actual: any, expected: any, message?: string): void`

    `actual !== expected` must be `true`. If not, an `AssertionError` is thrown.

    ```
    [](#cb84-1)assert.notEqual(3+3, 22);
    ```

The optional last parameter `message` can be used to explain what is asserted. If the assertion fails, the message is used to set up the `AssertionError` that is thrown.

```
[](#cb85-1)let e;
[](#cb85-2)try {
[](#cb85-3)  const x = 3;
[](#cb85-4)  assert.equal(x, 8, 'x must be equal to 8')
[](#cb85-5)} catch (err) {
[](#cb85-6)  assert.equal(
[](#cb85-7)    String(err),
[](#cb85-8)    'AssertionError [ERR_ASSERTION]: x must be equal to 8');
[](#cb85-9)}
```

### 10.4.2 Deep equality

*   `function deepEqual(actual: any, expected: any, message?: string): void`

    `actual` must be deeply equal to `expected`. If not, an `AssertionError` is thrown.

    ```
    [](#cb86-1)assert.deepEqual([1,2,3], [1,2,3]);
    [](#cb86-2)assert.deepEqual([], []);
    [](#cb86-3)
    [](#cb86-4)// To .equal(), an object is only equal to itself:
    [](#cb86-5)assert.notEqual([], []);
    ```

*   `function notDeepEqual(actual: any, expected: any, message?: string): void`

    `actual` must not be deeply equal to `expected`. If it is, an `AssertionError` is thrown.

    ```
    [](#cb87-1)assert.notDeepEqual([1,2,3], [1,2]);
    ```

### 10.4.3 Expecting exceptions

If you want to (or expect to) receive an exception, you need `throws()`: This function calls its first parameter, the function `block`, and only succeeds if it throws an exception. Additional parameters can be used to specify what that exception must look like.

*   `function throws(block: Function, message?: string): void`

    ```
    [](#cb88-1)assert.throws(
    [](#cb88-2)  () => {
    [](#cb88-3)    null.prop;
    [](#cb88-4)  }
    [](#cb88-5));
    ```

*   `function throws(block: Function, error: Function, message?: string): void`

    ```
    [](#cb89-1)assert.throws(
    [](#cb89-2)  () => {
    [](#cb89-3)    null.prop;
    [](#cb89-4)  },
    [](#cb89-5)  TypeError
    [](#cb89-6));
    ```

*   `function throws(block: Function, error: RegExp, message?: string): void`

    ```
    [](#cb90-1)assert.throws(
    [](#cb90-2)  () => {
    [](#cb90-3)    null.prop;
    [](#cb90-4)  },
    [](#cb90-5)  /^TypeError: Cannot read property 'prop' of null$/
    [](#cb90-6));
    ```

*   `function throws(block: Function, error: Object, message?: string): void`

    ```
    [](#cb91-1)assert.throws(
    [](#cb91-2)  () => {
    [](#cb91-3)    null.prop;
    [](#cb91-4)  },
    [](#cb91-5)  {
    [](#cb91-6)    name: 'TypeError',
    [](#cb91-7)    message: `Cannot read property 'prop' of null`,
    [](#cb91-8)  }
    [](#cb91-9));
    ```

### 10.4.4 Another tool function

*   `function fail(message: string | Error): never`

    Always throws an `AssertionError` when it is called. That is occasionally useful for unit testing.

    ```
    [](#cb92-1)try {
    [](#cb92-2)  functionThatShouldThrow();
    [](#cb92-3)  assert.fail();
    [](#cb92-4)} catch (_) {
    [](#cb92-5)  // Success
    [](#cb92-6)}
    ```

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 11 Getting started with quizzes and exercises

* * *

*   11.1 [Quizzes](#ch012.xhtml_quizzes)
*   11.2 [Exercises](#ch012.xhtml_exercises)
    *   11.2.1 [Installing the exercises](#ch012.xhtml_installing-the-exercises)
    *   11.2.2 [Running exercises](#ch012.xhtml_running-exercises)
*   11.3 [Unit tests in JavaScript](#ch012.xhtml_unit-tests-in-javascript)
    *   11.3.1 [A typical test](#ch012.xhtml_a-typical-test)
    *   11.3.2 [Asynchronous tests in AVA](#ch012.xhtml_async-tests-ava)

* * *

Throughout most chapters, there are quizzes and exercises. These are a paid feature, but a comprehensive preview is available. This chapter explains how to get started with them.

## 11.1 Quizzes

Installation:

*   Download and unzip `impatient-js-quiz.zip`

Running the quiz app:

*   Open `impatient-js-quiz/index.html` in a web browser
*   You’ll see a TOC of all the quizzes.

## 11.2 Exercises

### 11.2.1 Installing the exercises

To install the exercises:

*   Download and unzip `impatient-js-code.zip`
*   Follow the instructions in `README.txt`

### 11.2.2 Running exercises

*   Exercises are referred to by path in this book.
    *   For example: `exercises/quizzes-exercises/first_module_test.mjs`
*   Within each file:
    *   The first line contains the command for running the exercise.
    *   The following lines describe what you have to do.

## 11.3 Unit tests in JavaScript

All exercises in this book are tests that are run via the test framework [AVA](https://github.com/avajs/ava). This section gives a brief introduction.

### 11.3.1 A typical test

Typical test code is split into two parts:

*   Part 1: the code to be tested.
*   Part 2: the tests for the code.

Take, for example, the following two files:

*   `id.mjs` (code to be tested)
*   `id_test.mjs` (tests)

#### 11.3.1.1 Part 1: the code

The code itself resides in `id.mjs`:

```
[](#cb93-1)export function id(x) {
[](#cb93-2)  return x;
[](#cb93-3)}
```

The key thing here is: everything you want to test must be exported. Otherwise, the test code can’t access it.

#### 11.3.1.2 Part 2: the tests

![](media/file0.svg)  **Don’t worry about the exact details of tests**

You don’t need to worry about the exact details of tests: They are always implemented for you. Therefore, you only need to read them, but not write them.

The tests for the code reside in `id_test.mjs`:

```
[](#cb94-1)// npm t demos/quizzes-exercises/id_test.mjs
[](#cb94-2)
[](#cb94-3)import test from 'ava'; // (A)
[](#cb94-4)import {strict as assert} from 'assert'; // (B)
[](#cb94-5)import {id} from './id.mjs'; // (C)
[](#cb94-6)
[](#cb94-7)test('My test', t => { // (D)
[](#cb94-8)  assert.equal(id('abc'), 'abc'); // (E)
[](#cb94-9)});
```

The core of this test file is line E – [an assertion](#ch011.xhtml_ch_assertion-api): `assert.equal()` specifies that the expected result of `id('abc')` is `'abc'`.

As for the other lines:

*   The comment at the very beginning shows the shell command for running the test.
*   Line A: We import the test framework.
*   Line B: We import the assertion library. AVA has built-in assertions, but module `assert` lets us remain compatible with plain Node.js.
*   Line C: We import the function to test.
*   Line D: We define a test. This is done by calling the function `test()`:
    *   First parameter: the name of the test.
    *   Second parameter: the test code, which is provided via an arrow function. The parameter `t` gives us access to AVA’s testing API (assertions, etc.).

To run the test, we execute the following in a command line:

```
npm t demos/quizzes-exercises/id_test.mjs
```

The `t` is an abbreviation for `test`. That is, the long version of this command is:

```
npm test demos/quizzes-exercises/id_test.mjs
```

![](media/file6.svg)  **Exercise: Your first exercise**

The following exercise gives you a first taste of what exercises are like:

*   `exercises/quizzes-exercises/first_module_test.mjs`

### 11.3.2 Asynchronous tests in AVA

![](media/file0.svg)  **Reading**

You can postpone reading this section until you get to the chapters on asynchronous programming.

Writing tests for asynchronous code requires extra work: The test receives its results later and has to signal to AVA that it isn’t finished yet when it returns. The following subsections examine three ways of doing so.

#### 11.3.2.1 Asynchronicity via callbacks

If we call `test.cb()` instead of `test()`, AVA switches to callback-based asynchronicity. When we are done with our asynchronous work, we have to call `t.end()`:

```
[](#cb97-1)test.cb('divideCallback', t => {
[](#cb97-2)  divideCallback(8, 4, (error, result) => {
[](#cb97-3)    if (error) {
[](#cb97-4)      t.end(error);
[](#cb97-5)    } else {
[](#cb97-6)      assert.strictEqual(result, 2);
[](#cb97-7)      t.end();
[](#cb97-8)    }
[](#cb97-9)  });
[](#cb97-10)});
```

#### 11.3.2.2 Asynchronicity via Promises

If a test returns a Promise, AVA switches to Promise-based asynchronicity. A test is considered successful if the Promise is fulfilled and failed if the Promise is rejected.

```
[](#cb98-1)test('dividePromise 1', t => {
[](#cb98-2)  return dividePromise(8, 4)
[](#cb98-3)  .then(result => {
[](#cb98-4)    assert.strictEqual(result, 2);
[](#cb98-5)  });
[](#cb98-6)});
```

#### 11.3.2.3 Async functions as test “bodies”

Async functions always return Promises. Therefore, an async function is a convenient way of implementing an asynchronous test. The following code is equivalent to the previous example.

```
[](#cb99-1)test('dividePromise 2', async t => {
[](#cb99-2)  const result = await dividePromise(8, 4);
[](#cb99-3)  assert.strictEqual(result, 2);
[](#cb99-4)  // No explicit return necessary!
[](#cb99-5)});
```

You don’t need to explicitly return anything: The implicitly returned `undefined` is used to fulfill the Promise returned by this async function. And if the test code throws an exception, then the async function takes care of rejecting the returned Promise.

# 12 Variables and assignment

* * *

*   12.1 [`let`](#ch013.xhtml_let)
*   12.2 [`const`](#ch013.xhtml_const)
    *   12.2.1 [`const` and immutability](#ch013.xhtml_const-and-immutability)
    *   12.2.2 [`const` and loops](#ch013.xhtml_const-and-loops)
*   12.3 [Deciding between `const` and `let`](#ch013.xhtml_deciding-between-const-and-let)
*   12.4 [The scope of a variable](#ch013.xhtml_the-scope-of-a-variable)
    *   12.4.1 [Shadowing variables](#ch013.xhtml_shadowing-variables)
*   12.5 [(Advanced)](#ch013.xhtml_advanced-1)
*   12.6 [Terminology: static vs. dynamic](#ch013.xhtml_terminology-static-vs.-dynamic)
    *   12.6.1 [Static phenomenon: scopes of variables](#ch013.xhtml_static-phenomenon-scopes-of-variables)
    *   12.6.2 [Dynamic phenomenon: function calls](#ch013.xhtml_dynamic-phenomenon-function-calls)
*   12.7 [Global variables and the global object](#ch013.xhtml_global-variables-and-the-global-object)
    *   12.7.1 [`globalThis`](#ch013.xhtml_globalthis)
*   12.8 [Declarations: scope and activation](#ch013.xhtml_declarations-scope-activation)
    *   12.8.1 [`const` and `let`: temporal dead zone](#ch013.xhtml_const-and-let-temporal-dead-zone)
    *   12.8.2 [Function declarations and early activation](#ch013.xhtml_function-declarations-and-early-activation)
    *   12.8.3 [Class declarations are not activated early](#ch013.xhtml_class-declarations-are-not-activated-early)
    *   12.8.4 [`var`: hoisting (partial early activation)](#ch013.xhtml_var-hoisting-partial-early-activation)
*   12.9 [Closures](#ch013.xhtml_closures)
    *   12.9.1 [Bound variables vs. free variables](#ch013.xhtml_bound-variables-vs.-free-variables)
    *   12.9.2 [What is a closure?](#ch013.xhtml_what-is-a-closure)
    *   12.9.3 [Example: A factory for incrementors](#ch013.xhtml_example-a-factory-for-incrementors)
    *   12.9.4 [Use cases for closures](#ch013.xhtml_use-cases-for-closures)
*   12.10 [Further reading](#ch013.xhtml_further-reading-1)

* * *

These are JavaScript’s main ways of declaring variables:

*   `let` declares mutable variables.
*   `const` declares *constants* (immutable variables).

Before ES6, there was also `var`. But it has several quirks, so it’s best to avoid it in modern JavaScript. You can read more about it in [*Speaking JavaScript*](http://speakingjs.com/es5/ch16.html).

## 12.1 `let`

Variables declared via `let` are mutable:

```
[](#cb100-1)let i;
[](#cb100-2)i = 0;
[](#cb100-3)i = i + 1;
[](#cb100-4)assert.equal(i, 1);
```

You can also declare and assign at the same time:

```
[](#cb101-1)let i = 0;
```

## 12.2 `const`

Variables declared via `const` are immutable. You must always initialize immediately:

```
[](#cb102-1)const i = 0; // must initialize
[](#cb102-2)
[](#cb102-3)assert.throws(
[](#cb102-4)  () => { i = i + 1 },
[](#cb102-5)  {
[](#cb102-6)    name: 'TypeError',
[](#cb102-7)    message: 'Assignment to constant variable.',
[](#cb102-8)  }
[](#cb102-9));
```

### 12.2.1 `const` and immutability

In JavaScript, `const` only means that the *binding* (the association between variable name and variable value) is immutable. The value itself may be mutable, like `obj` in the following example.

```
[](#cb103-1)const obj = { prop: 0 };
[](#cb103-2)
[](#cb103-3)// Allowed: changing properties of `obj`
[](#cb103-4)obj.prop = obj.prop + 1;
[](#cb103-5)assert.equal(obj.prop, 1);
[](#cb103-6)
[](#cb103-7)// Not allowed: assigning to `obj`
[](#cb103-8)assert.throws(
[](#cb103-9)  () => { obj = {} },
[](#cb103-10)  {
[](#cb103-11)    name: 'TypeError',
[](#cb103-12)    message: 'Assignment to constant variable.',
[](#cb103-13)  }
[](#cb103-14));
```

### 12.2.2 `const` and loops

You can use `const` with `for-of` loops, where a fresh binding is created for each iteration:

```
[](#cb104-1)const arr = ['hello', 'world'];
[](#cb104-2)for (const elem of arr) {
[](#cb104-3)  console.log(elem);
[](#cb104-4)}
[](#cb104-5)// Output:
[](#cb104-6)// 'hello'
[](#cb104-7)// 'world'
```

In plain `for` loops, you must use `let`, however:

```
[](#cb105-1)const arr = ['hello', 'world'];
[](#cb105-2)for (let i=0; i<arr.length; i++) {
[](#cb105-3)  const elem = arr[i];
[](#cb105-4)  console.log(elem);
[](#cb105-5)}
```

## 12.3 Deciding between `const` and `let`

I recommend the following rules to decide between `const` and `let`:

*   `const` indicates an immutable binding and that a variable never changes its value. Prefer it.
*   `let` indicates that the value of a variable changes. Use it only when you can’t use `const`.

![](media/file6.svg)  **Exercise: `const`**

`exercises/variables-assignment/const_exrc.mjs`

## 12.4 The scope of a variable

The *scope* of a variable is the region of a program where it can be accessed. Consider the following code.

```
[](#cb106-1){ // // Scope A. Accessible: x
[](#cb106-2)  const x = 0;
[](#cb106-3)  assert.equal(x, 0);
[](#cb106-4)  { // Scope B. Accessible: x, y
[](#cb106-5)    const y = 1;
[](#cb106-6)    assert.equal(x, 0);
[](#cb106-7)    assert.equal(y, 1);
[](#cb106-8)    { // Scope C. Accessible: x, y, z
[](#cb106-9)      const z = 2;
[](#cb106-10)      assert.equal(x, 0);
[](#cb106-11)      assert.equal(y, 1);
[](#cb106-12)      assert.equal(z, 2);
[](#cb106-13)    }
[](#cb106-14)  }
[](#cb106-15)}
[](#cb106-16)// Outside. Not accessible: x, y, z
[](#cb106-17)assert.throws(
[](#cb106-18)  () => console.log(x),
[](#cb106-19)  {
[](#cb106-20)    name: 'ReferenceError',
[](#cb106-21)    message: 'x is not defined',
[](#cb106-22)  }
[](#cb106-23));
```

*   Scope A is the *(direct) scope* of `x`.
*   Scopes B and C are *inner scopes* of scope A.
*   Scope A is an *outer scope* of scope B and scope C.

Each variable is accessible in its direct scope and all scopes nested within that scope.

The variables declared via `const` and `let` are called *block-scoped* because their scopes are always the innermost surrounding blocks.

### 12.4.1 Shadowing variables

You can’t declare the same variable twice at the same level:

```
[](#cb107-1)assert.throws(
[](#cb107-2)  () => {
[](#cb107-3)    eval('let x = 1; let x = 2;');
[](#cb107-4)  },
[](#cb107-5)  {
[](#cb107-6)    name: 'SyntaxError',
[](#cb107-7)    message: "Identifier 'x' has already been declared",
[](#cb107-8)  });
```

![](media/file5.svg)  **Why `eval()`?**

[`eval()`](#ch026.xhtml_eval) delays parsing (and therefore the `SyntaxError`), until the callback of `assert.throws()` is executed. If we didn’t use it, we’d already get an error when this code is parsed and `assert.throws()` wouldn’t even be executed.

You can, however, nest a block and use the same variable name `x` that you used outside the block:

```
[](#cb108-1)const x = 1;
[](#cb108-2)assert.equal(x, 1);
[](#cb108-3){
[](#cb108-4)  const x = 2;
[](#cb108-5)  assert.equal(x, 2);
[](#cb108-6)}
[](#cb108-7)assert.equal(x, 1);
```

Inside the block, the inner `x` is the only accessible variable with that name. The inner `x` is said to *shadow* the outer `x`. Once you leave the block, you can access the old value again.

![](media/file7.svg)  **Quiz: basic**

See [quiz app](#ch012.xhtml_quizzes).

## 12.5 (Advanced)

All remaining sections are advanced.

## 12.6 Terminology: static vs. dynamic

These two adjectives describe phenomena in programming languages:

*   *Static* means that something is related to source code and can be determined without executing code.
*   *Dynamic* means at runtime.

Let’s look at examples for these two terms.

### 12.6.1 Static phenomenon: scopes of variables

Variable scopes are a static phenomenon. Consider the following code:

```
[](#cb109-1)function f() {
[](#cb109-2)  const x = 3;
[](#cb109-3)  // ···
[](#cb109-4)}
```

`x` is *statically* (or *lexically*) *scoped*. That is, its scope is fixed and doesn’t change at runtime.

Variable scopes form a static tree (via static nesting).

### 12.6.2 Dynamic phenomenon: function calls

Function calls are a dynamic phenomenon. Consider the following code:

```
[](#cb110-1)function g(x) {}
[](#cb110-2)function h(y) {
[](#cb110-3)  if (Math.random()) g(y); // (A)
[](#cb110-4)}
```

Whether or not the function call in line A happens, can only be decided at runtime.

Function calls form a dynamic tree (via dynamic calls).

## 12.7 Global variables and the global object

JavaScript’s variable scopes are nested. They form a tree:

*   The outermost scope is the root of the tree.
*   The scopes directly contained in that scope are the children of the root.
*   And so on.

The root is also called the *global scope*. In web browsers, the only location where one is directly in that scope is at the top level of a script. The variables of the global scope are called *global variables* and accessible everywhere. There are two kinds of global variables:

*   *Global declarative variables* are normal variables.
    *   They can only be created while at the top level of a script, via `const`, `let, and class declarations.
*   *Global object variables* are stored in properties of the so-called *global object*.
    *   They are created in the top level of a script, via `var` and function declarations.
    *   The global object can be accessed via the global variable `globalThis`. It can be used to create, read, and delete global object variables.
    *   Other than that, global object variables work like normal variables.

The following HTML fragment demonstrates `globalThis` and the two kinds of global variables.

```
[](#cb111-1)<script>
[](#cb111-2)  const declarativeVariable = 'd';
[](#cb111-3)  var objectVariable = 'o';
[](#cb111-4)</script>
[](#cb111-5)<script>
[](#cb111-6)  // All scripts share the same top-level scope:
[](#cb111-7)  console.log(declarativeVariable); // 'd'
[](#cb111-8)  console.log(objectVariable); // 'o'
[](#cb111-9) 
[](#cb111-10)  // Not all declarations create properties of the global object:
[](#cb111-11)  console.log(globalThis.declarativeVariable); // undefined
[](#cb111-12)  console.log(globalThis.objectVariable); // 'o'
[](#cb111-13)</script>
```

Each ECMAScript module has its own scope. Therefore, variables that exist at the top level of a module are not global. Fig. [5](#ch013.xhtml_fig:global-scope) illustrates how the various scopes are related.

![](media/file12.svg)

Figure 5: The global scope is JavaScript’s outermost scope. It has two kinds of variables: *object variables* (managed via the *global object*) and normal *declarative variables*. Each ECMAScript module has its own scope which is contained in the global scope.

### 12.7.1 `globalThis`

![](media/file4.svg)  **`globalThis` is new**

`globalThis` is a new feature. Be sure that the JavaScript engines you are targeting support it. If they don’t, switch to one of the alternatives mentioned below.

The global variable `globalThis` is the new standard way of accessing the global object. It got its name from the fact that it has the same value as `this` in global scope.

![](media/file5.svg)  **`globalThis` does not always directly point to the global object**

For example, in browsers, [there is an indirection](https://2ality.com/2019/08/global-this.html#window-proxy). That indirection is normally not noticable, but it is there and can be observed.

#### 12.7.1.1 Alternatives to `globalThis`

Older ways of accessing the global object depend on the platform:

*   Global variable `window`: is the classic way of referring to the global object. But it doesn’t work in Node.js and in Web Workers.
*   Global variable `self`: is available in Web Workers and browsers in general. But it isn’t supported by Node.js.
*   Global variable `global`: is only available in Node.js.

#### 12.7.1.2 Use cases for `globalThis`

The global object is now considered a mistake that JavaScript can’t get rid of, due to backward compatibility. It affects performance negatively and is generally confusing.

ECMAScript 6 introduced several features that make it easier to avoid the global object – for example:

*   `const`, `let`, and class declarations don’t create global object properties when used in global scope.
*   Each ECMAScript module has its own local scope.

It is usually better to access global object variables via variables and not via properties of `globalThis`. The former has always worked the same on all JavaScript platforms.

Tutorials on the web occasionally access global variables `globVar` via `window.globVar`. But the prefix “`window.`” is not necessary and I recommend to omit it:

```
[](#cb112-1)window.encodeURIComponent(str); // no
[](#cb112-2)encodeURIComponent(str); // yes
```

Therefore, there are relatively few use cases for `globalThis` – for example:

*   [*Polyfills*](#ch028.xhtml_polyfills) that add new features to old JavaScript engines.
*   Feature detection, to find out what features a JavaScript engine supports.

## 12.8 Declarations: scope and activation

These are two key aspects of declarations:

*   Scope: Where can a declared entity be seen? This is a static trait.
*   Activation: When can I access an entity? This is a dynamic trait. Some entities can be accessed as soon as we enter their scopes. For others, we have to wait until execution reaches their declarations.

Tbl. [1](#ch013.xhtml_tbl:aspects-of-declarations) summarizes how various declarations handle these aspects.

Table 1: Aspects of declarations. “Duplicates” describes if a declaration can be used twice with the same name (per scope). “Global prop.” describes if a declaration adds a property to the global object, when it is executed in the global scope of a script. *TDZ* means *temporal dead zone* (which is explained later). (*) Function declarations are normally block-scoped, but function-scoped in [sloppy mode](#ch009.xhtml_strict-mode).

|  | Scope | Activation | Duplicates | Global prop. |
| --- | --- | --- | --- | --- |
| `const` | Block | decl. (TDZ) | `✘` | `✘` |
| `let` | Block | decl. (TDZ) | `✘` | `✘` |
| `function` | Block (*) | start | `✔` | `✔` |
| `class` | Block | decl. (TDZ) | `✘` | `✘` |
| `import` | Module | same as export | `✘` | `✘` |
| `var` | Function | start, partially | `✔` | `✔` |

`import` is described in [§27.5 “ECMAScript modules”](#ch028.xhtml_ecmascript-modules). The following sections describe the other constructs in more detail.

### 12.8.1 `const` and `let`: temporal dead zone

For JavaScript, TC39 needed to decide what happens if you access a constant in its direct scope, before its declaration:

```
[](#cb113-1){
[](#cb113-2)  console.log(x); // What happens here?
[](#cb113-3)  const x;
[](#cb113-4)}
```

Some possible approaches are:

1.  The name is resolved in the scope surrounding the current scope.
2.  You get `undefined`.
3.  There is an error.

Approach 1 was rejected because there is no precedent in the language for this approach. It would therefore not be intuitive to JavaScript programmers.

Approach 2 was rejected because then `x` wouldn’t be a constant – it would have different values before and after its declaration.

`let` uses the same approach 3 as `const`, so that both work similarly and it’s easy to switch between them.

The time between entering the scope of a variable and executing its declaration is called the *temporal dead zone* (TDZ) of that variable:

*   During this time, the variable is considered to be uninitialized (as if that were a special value it has).
*   If you access an uninitialized variable, you get a `ReferenceError`.
*   Once you reach a variable declaration, the variable is set to either the value of the initializer (specified via the assignment symbol) or `undefined` – if there is no initializer.

The following code illustrates the temporal dead zone:

```
[](#cb114-1)if (true) { // entering scope of `tmp`, TDZ starts
[](#cb114-2)  // `tmp` is uninitialized:
[](#cb114-3)  assert.throws(() => (tmp = 'abc'), ReferenceError);
[](#cb114-4)  assert.throws(() => console.log(tmp), ReferenceError);
[](#cb114-5)
[](#cb114-6)  let tmp; // TDZ ends
[](#cb114-7)  assert.equal(tmp, undefined);
[](#cb114-8)}
```

The next example shows that the temporal dead zone is truly *temporal* (related to time):

```
[](#cb115-1)if (true) { // entering scope of `myVar`, TDZ starts
[](#cb115-2)  const func = () => {
[](#cb115-3)    console.log(myVar); // executed later
[](#cb115-4)  };
[](#cb115-5)
[](#cb115-6)  // We are within the TDZ:
[](#cb115-7)  // Accessing `myVar` causes `ReferenceError`
[](#cb115-8)
[](#cb115-9)  let myVar = 3; // TDZ ends
[](#cb115-10)  func(); // OK, called outside TDZ
[](#cb115-11)}
```

Even though `func()` is located before the declaration of `myVar` and uses that variable, we can call `func()`. But we have to wait until the temporal dead zone of `myVar` is over.

### 12.8.2 Function declarations and early activation

![](media/file0.svg)  **More information on functions**

In this section, we are using functions – before we had a chance to learn them properly. Hopefully, everything still makes sense. Whenever it doesn’t, please see [§25 “Callable values”](#ch026.xhtml_ch_callables).

A function declaration is always executed when entering its scope, regardless of where it is located within that scope. That enables you to call a function `foo()` before it is declared:

```
[](#cb116-1)assert.equal(foo(), 123); // OK
[](#cb116-2)function foo() { return 123; }
```

The early activation of `foo()` means that the previous code is equivalent to:

```
[](#cb117-1)function foo() { return 123; }
[](#cb117-2)assert.equal(foo(), 123);
```

If you declare a function via `const` or `let`, then it is not activated early. In the following example, you can only use `bar()` after its declaration.

```
[](#cb118-1)assert.throws(
[](#cb118-2)  () => bar(), // before declaration
[](#cb118-3)  ReferenceError);
[](#cb118-4)
[](#cb118-5)const bar = () => { return 123; };
[](#cb118-6)
[](#cb118-7)assert.equal(bar(), 123); // after declaration 
```

#### 12.8.2.1 Calling ahead without early activation

Even if a function `g()` is not activated early, it can be called by a preceding function `f()` (in the same scope) if we adhere to the following rule: `f()` must be invoked after the declaration of `g()`.

```
[](#cb119-1)const f = () => g();
[](#cb119-2)const g = () => 123;
[](#cb119-3)
[](#cb119-4)// We call f() after g() was declared:
[](#cb119-5)assert.equal(f(), 123);
```

The functions of a module are usually invoked after its complete body is executed. Therefore, in modules, you rarely need to worry about the order of functions.

Lastly, note how early activation automatically keeps the aforementioned rule: when entering a scope, all function declarations are executed first, before any calls are made.

#### 12.8.2.2 A pitfall of early activation

If you rely on early activation to call a function before its declaration, then you need to be careful that it doesn’t access data that isn’t activated early.

```
[](#cb120-1)funcDecl();
[](#cb120-2)
[](#cb120-3)const MY_STR = 'abc';
[](#cb120-4)function funcDecl() {
[](#cb120-5)  assert.throws(
[](#cb120-6)    () => MY_STR,
[](#cb120-7)    ReferenceError);
[](#cb120-8)}
```

The problem goes away if you make the call to `funcDecl()` after the declaration of `MY_STR`.

#### 12.8.2.3 The pros and cons of early activation

We have seen that early activation has a pitfall and that you can get most of its benefits without using it. Therefore, it is better to avoid early activation. But I don’t feel strongly about this and, as mentioned before, often use function declarations because I like their syntax.

### 12.8.3 Class declarations are not activated early

Even though they are similar to function declarations in some ways, [class declarations](#ch030.xhtml_classes) are not activated early:

```
[](#cb121-1)assert.throws(
[](#cb121-2)  () => new MyClass(),
[](#cb121-3)  ReferenceError);
[](#cb121-4)
[](#cb121-5)class MyClass {}
[](#cb121-6)
[](#cb121-7)assert.equal(new MyClass() instanceof MyClass, true);
```

Why is that? Consider the following class declaration:

```
[](#cb122-1)class MyClass extends Object {}
```

The operand of `extends` is an expression. Therefore, you can do things like this:

```
[](#cb123-1)const identity = x => x;
[](#cb123-2)class MyClass extends identity(Object) {}
```

Evaluating such an expression must be done at the location where it is mentioned. Anything else would be confusing. That explains why class declarations are not activated early.

### 12.8.4 `var`: hoisting (partial early activation)

`var` is an older way of declaring variables that predates `const` and `let` (which are preferred now). Consider the following `var` declaration.

```
[](#cb124-1)var x = 123;
```

This declaration has two parts:

*   Declaration `var x`: The scope of a `var`-declared variable is the innermost surrounding function and not the innermost surrounding block, as for most other declarations. Such a variable is already active at the beginning of its scope and initialized with `undefined`.
*   Assignment `x = 123`: The assignment is always executed in place.

The following code demonstrates the effects of `var`:

```
[](#cb125-1)function f() {
[](#cb125-2)  // Partial early activation:
[](#cb125-3)  assert.equal(x, undefined);
[](#cb125-4)  if (true) {
[](#cb125-5)    var x = 123;
[](#cb125-6)    // The assignment is executed in place:
[](#cb125-7)    assert.equal(x, 123);
[](#cb125-8)  }
[](#cb125-9)  // Scope is function, not block:
[](#cb125-10)  assert.equal(x, 123);
[](#cb125-11)}
```

## 12.9 Closures

Before we can explore closures, we need to learn about bound variables and free variables.

### 12.9.1 Bound variables vs. free variables

Per scope, there is a set of variables that are mentioned. Among these variables we distinguish:

*   *Bound variables* are declared within the scope. They are parameters and local variables.
*   *Free variables* are declared externally. They are also called *non-local variables*.

Consider the following code:

```
[](#cb126-1)function func(x) {
[](#cb126-2)  const y = 123;
[](#cb126-3)  console.log(z);
[](#cb126-4)}
```

In the body of `func()`, `x` and `y` are bound variables. `z` is a free variable.

### 12.9.2 What is a closure?

What is a closure then?

> A *closure* is a function plus a connection to the variables that exist at its “birth place”.

What is the point of keeping this connection? It provides the values for the free variables of the function – for example:

```
[](#cb127-1)function funcFactory(value) {
[](#cb127-2)  return () => {
[](#cb127-3)    return value;
[](#cb127-4)  };
[](#cb127-5)}
[](#cb127-6)
[](#cb127-7)const func = funcFactory('abc');
[](#cb127-8)assert.equal(func(), 'abc'); // (A)
```

`funcFactory` returns a closure that is assigned to `func`. Because `func` has the connection to the variables at its birth place, it can still access the free variable `value` when it is called in line A (even though it “escaped” its scope).

![](media/file2.svg)  **All functions in JavaScript are closures**

Static scoping is supported via closures in JavaScript. Therefore, every function is a closure.

### 12.9.3 Example: A factory for incrementors

The following function returns *incrementors* (a name that I just made up). An incrementor is a function that internally stores a number. When it is called, it updates that number by adding the argument to it and returns the new value.

```
[](#cb128-1)function createInc(startValue) {
[](#cb128-2)  return (step) => { // (A)
[](#cb128-3)    startValue += step;
[](#cb128-4)    return startValue;
[](#cb128-5)  };
[](#cb128-6)}
[](#cb128-7)const inc = createInc(5);
[](#cb128-8)assert.equal(inc(2), 7);
```

We can see that the function created in line A keeps its internal number in the free variable `startValue`. This time, we don’t just read from the birth scope, we use it to store data that we change and that persists across function calls.

We can create more storage slots in the birth scope, via local variables:

```
[](#cb129-1)function createInc(startValue) {
[](#cb129-2)  let index = -1;
[](#cb129-3)  return (step) => {
[](#cb129-4)    startValue += step;
[](#cb129-5)    index++;
[](#cb129-6)    return [index, startValue];
[](#cb129-7)  };
[](#cb129-8)}
[](#cb129-9)const inc = createInc(5);
[](#cb129-10)assert.deepEqual(inc(2), [0, 7]);
[](#cb129-11)assert.deepEqual(inc(2), [1, 9]);
[](#cb129-12)assert.deepEqual(inc(2), [2, 11]);
```

### 12.9.4 Use cases for closures

What are closures good for?

*   For starters, they are simply an implementation of static scoping. As such, they provide context data for callbacks.

*   They can also be used by functions to store state that persists across function calls. `createInc()` is an example of that.

*   And they can provide private data for objects (produced via literals or classes). The details of how that works are explained in [*Exploring ES6*](https://exploringjs.com/es6/ch_classes.html#_private-data-via-constructor-environments).

![](media/file7.svg)  **Quiz: advanced**

See [quiz app](#ch012.xhtml_quizzes).

## 12.10 Further reading

For more information on how variables are handled under the hood (as described in the ECMAScript specification), consult [§26.4 “Closures and environments”](#ch027.xhtml_closures-environments).

# 13 Values

* * *

*   13.1 [What’s a type?](#ch014.xhtml_whats-a-type)
*   13.2 [JavaScript’s type hierarchy](#ch014.xhtml_javascripts-type-hierarchy)
*   13.3 [The types of the language specification](#ch014.xhtml_the-types-of-the-language-specification)
*   13.4 [Primitive values vs. objects](#ch014.xhtml_primitive-values-vs.-objects)
    *   13.4.1 [Primitive values (short: primitives)](#ch014.xhtml_primitive-values-short-primitives)
    *   13.4.2 [Objects](#ch014.xhtml_objects)
*   13.5 [The operators `typeof` and `instanceof`: what’s the type of a value?](#ch014.xhtml_the-operators-typeof-and-instanceof-whats-the-type-of-a-value)
    *   13.5.1 [`typeof`](#ch014.xhtml_typeof)
    *   13.5.2 [`instanceof`](#ch014.xhtml_instanceof)
*   13.6 [Classes and constructor functions](#ch014.xhtml_classes-and-constructor-functions)
    *   13.6.1 [Constructor functions associated with primitive types](#ch014.xhtml_constructor-functions-associated-with-primitive-types)
*   13.7 [Converting between types](#ch014.xhtml_converting-between-types)
    *   13.7.1 [Explicit conversion between types](#ch014.xhtml_explicit-conversion-between-types)
    *   13.7.2 [Coercion (automatic conversion between types)](#ch014.xhtml_coercion-automatic-conversion-between-types)

* * *

In this chapter, we’ll examine what kinds of values JavaScript has.

![](media/file0.svg)  **Supporting tool: `===`**

In this chapter, we’ll occasionally use the strict equality operator. `a === b` evaluates to `true` if `a` and `b` are equal. What exactly that means is explained in [§14.4.2 “Strict equality (`===` and `!==`)”](#ch015.xhtml_strict-equality).

## 13.1 What’s a type?

For this chapter, I consider types to be sets of values – for example, the type `boolean` is the set { `false`, `true` }.

## 13.2 JavaScript’s type hierarchy

![](media/file13.svg)

Figure 6: A partial hierarchy of JavaScript’s types. Missing are the classes for errors, the classes associated with primitive types, and more. The diagram hints at the fact that not all objects are instances of `Object`.

Fig. [6](#ch014.xhtml_fig:type_hierarchy) shows JavaScript’s type hierarchy. What do we learn from that diagram?

*   JavaScript distinguishes two kinds of values: primitive values and objects. We’ll see soon what the difference is.
*   The diagram differentiates objects and instances of class `Object`. Each instance of `Object` is also an object, but not vice versa. However, virtually all objects that you’ll encounter in practice are instances of `Object` – for example, objects created via object literals. More details on this topic are explained in [§29.4.3.4 “Objects that aren’t instances of `Object`”](#ch030.xhtml_non-instances-of-object).

## 13.3 The types of the language specification

The ECMAScript specification only knows a total of seven types. The names of those types are (I’m using TypeScript’s names, not the spec’s names):

*   `undefined` with the only element `undefined`
*   `null` with the only element `null`
*   `boolean` with the elements `false` and `true`
*   `number` the type of all numbers (e.g., `-123`, `3.141`)
*   `string` the type of all strings (e.g., `'abc'`)
*   `symbol` the type of all symbols (e.g., `Symbol('My Symbol')`)
*   `object` the type of all objects (different from `Object`, the type of all instances of class `Object` and its subclasses)

## 13.4 Primitive values vs. objects

The specification makes an important distinction between values:

*   *Primitive values* are the elements of the types `undefined`, `null`, `boolean`, `number`, `string`, `symbol`.
*   All other values are *objects*.

In contrast to Java (that inspired JavaScript here), primitive values are not second-class citizens. The difference between them and objects is more subtle. In a nutshell:

*   Primitive values: are atomic building blocks of data in JavaScript.
    *   They are *passed by value*: when primitive values are assigned to variables or passed to functions, their contents are copied.
    *   They are *compared by value*: when comparing two primitive values, their contents are compared.
*   Objects: are compound pieces of data.
    *   They are *passed by identity* (my term): when objects are assigned to variables or passed to functions, their *identities* (think pointers) are copied.
    *   They are *compared by identity* (my term): when comparing two objects, their identities are compared.

Other than that, primitive values and objects are quite similar: they both have *properties* (key-value entries) and can be used in the same locations.

Next, we’ll look at primitive values and objects in more depth.

### 13.4.1 Primitive values (short: primitives)

#### 13.4.1.1 Primitives are immutable

You can’t change, add, or remove properties of primitives:

```
[](#cb130-1)let str = 'abc';
[](#cb130-2)assert.equal(str.length, 3);
[](#cb130-3)assert.throws(
[](#cb130-4)  () => { str.length = 1 },
[](#cb130-5)  /^TypeError: Cannot assign to read only property 'length'/
[](#cb130-6));
```

#### 13.4.1.2 Primitives are *passed by value*

Primitives are *passed by value*: variables (including parameters) store the contents of the primitives. When assigning a primitive value to a variable or passing it as an argument to a function, its content is copied.

```
[](#cb131-1)let x = 123;
[](#cb131-2)let y = x;
[](#cb131-3)assert.equal(y, 123);
```

#### 13.4.1.3 Primitives are *compared by value*

Primitives are *compared by value*: when comparing two primitive values, we compare their contents.

```
[](#cb132-1)assert.equal(123 === 123, true);
[](#cb132-2)assert.equal('abc' === 'abc', true);
```

To see what’s so special about this way of comparing, read on and find out how objects are compared.

### 13.4.2 Objects

Objects are covered in detail in [§28 “Single objects”](#ch029.xhtml_ch_single-objects) and the following chapter. Here, we mainly focus on how they differ from primitive values.

Let’s first explore two common ways of creating objects:

*   Object literal:

    ```
    [](#cb133-1)const obj = {
    [](#cb133-2)  first: 'Jane',
    [](#cb133-3)  last: 'Doe',
    [](#cb133-4)};
    ```

    The object literal starts and ends with curly braces `{}`. It creates an object with two properties. The first property has the key `'first'` (a string) and the value `'Jane'`. The second property has the key `'last'` and the value `'Doe'`. For more information on object literals, consult [§28.2.1 “Object literals: properties”](#ch029.xhtml_object-literals).

*   Array literal:

    ```
    [](#cb134-1)const arr = ['foo', 'bar'];
    ```

    The Array literal starts and ends with square brackets `[]`. It creates an Array with two *elements*: `'foo'` and `'bar'`. For more information on Array literals, consult [§31.2.1 “Creating, reading, writing Arrays”](#ch032.xhtml_array-literals).

#### 13.4.2.1 Objects are mutable by default

By default, you can freely change, add, and remove the properties of objects:

```
[](#cb135-1)const obj = {};
[](#cb135-2)
[](#cb135-3)obj.foo = 'abc'; // add a property
[](#cb135-4)assert.equal(obj.foo, 'abc');
[](#cb135-5)
[](#cb135-6)obj.foo = 'def'; // change a property
[](#cb135-7)assert.equal(obj.foo, 'def');
```

#### 13.4.2.2 Objects are *passed by identity*

Objects are *passed by identity* (my term): variables (including parameters) store the *identities* of objects.

The identity of an object is like a pointer (or a transparent reference) to the object’s actual data on the *heap* (think shared main memory of a JavaScript engine).

When assigning an object to a variable or passing it as an argument to a function, its identity is copied. Each object literal creates a fresh object on the heap and returns its identity.

```
[](#cb136-1)const a = {}; // fresh empty object
[](#cb136-2)// Pass the identity in `a` to `b`:
[](#cb136-3)const b = a;
[](#cb136-4)
[](#cb136-5)// Now `a` and `b` point to the same object
[](#cb136-6)// (they “share” that object):
[](#cb136-7)assert.equal(a === b, true);
[](#cb136-8)
[](#cb136-9)// Changing `a` also changes `b`:
[](#cb136-10)a.foo = 123;
[](#cb136-11)assert.equal(b.foo, 123);
```

JavaScript uses *garbage collection* to automatically manage memory:

```
[](#cb137-1)let obj = { prop: 'value' };
[](#cb137-2)obj = {};
```

Now the old value `{ prop: 'value' }` of `obj` is *garbage* (not used anymore). JavaScript will automatically *garbage-collect* it (remove it from memory), at some point in time (possibly never if there is enough free memory).

![](media/file5.svg)  **Details: passing by identity**

“Passing by identity” means that the identity of an object (a transparent reference) is passed by value. This approach is also called [“passing by sharing”](https://en.wikipedia.org/wiki/Evaluation_strategy#Call_by_sharing).

#### 13.4.2.3 Objects are *compared by identity*

Objects are *compared by identity* (my term): two variables are only equal if they contain the same object identity. They are not equal if they refer to different objects with the same content.

```
[](#cb138-1)const obj = {}; // fresh empty object
[](#cb138-2)assert.equal(obj === obj, true); // same identity
[](#cb138-3)assert.equal({} === {}, false); // different identities, same content
```

## 13.5 The operators `typeof` and `instanceof`: what’s the type of a value?

The two operators `typeof` and `instanceof` let you determine what type a given value `x` has:

```
[](#cb139-1)if (typeof x === 'string') ···
[](#cb139-2)if (x instanceof Array) ···
```

How do they differ?

*   `typeof` distinguishes the 7 types of the specification (minus one omission, plus one addition).
*   `instanceof` tests which class created a given value.

![](media/file2.svg)  **Rule of thumb: `typeof` is for primitive values; `instanceof` is for objects**

### 13.5.1 `typeof`

Table 2: The results of the `typeof` operator.

| `x` | `typeof x` |
| --- | --- |
| `undefined` | `'undefined'` |
| `null` | `'object'` |
| Boolean | `'boolean'` |
| Number | `'number'` |
| String | `'string'` |
| Symbol | `'symbol'` |
| Function | `'function'` |
| All other objects | `'object'` |

Tbl. [2](#ch014.xhtml_tbl:typeof-results) lists all results of `typeof`. They roughly correspond to the 7 types of the language specification. Alas, there are two differences, and they are language quirks:

*   `typeof null` returns `'object'` and not `'null'`. That’s a bug. Unfortunately, it can’t be fixed. TC39 tried to do that, but it broke too much code on the web.
*   `typeof` of a function should be `'object'` (functions are objects). Introducing a separate category for functions is confusing.

![](media/file6.svg)  **Exercises: Two exercises on `typeof`**

*   `exercises/values/typeof_exrc.mjs`

*   Bonus: `exercises/values/is_object_test.mjs`

### 13.5.2 `instanceof`

This operator answers the question: has a value `x` been created by a class `C`?

```
[](#cb140-1)x instanceof C
```

For example:

```
> (function() {}) instanceof Function
true
> ({}) instanceof Object
true
> [] instanceof Array
true
```

Primitive values are not instances of anything:

```
> 123 instanceof Number
false
> '' instanceof String
false
> '' instanceof Object
false
```

![](media/file6.svg)  **Exercise: `instanceof`**

`exercises/values/instanceof_exrc.mjs`

## 13.6 Classes and constructor functions

JavaScript’s original factories for objects are *constructor functions*: ordinary functions that return “instances” of themselves if you invoke them via the `new` operator.

ES6 introduced *classes*, which are mainly better syntax for constructor functions.

In this book, I’m using the terms *constructor function* and *class* interchangeably.

Classes can be seen as partitioning the single type `object` of the specification into subtypes – they give us more types than the limited 7 ones of the specification. Each class is the type of the objects that were created by it.

### 13.6.1 Constructor functions associated with primitive types

Each primitive type (except for the spec-internal types for `undefined` and `null`) has an associated *constructor function* (think class):

*   The constructor function `Boolean` is associated with booleans.
*   The constructor function `Number` is associated with numbers.
*   The constructor function `String` is associated with strings.
*   The constructor function `Symbol` is associated with symbols.

Each of these functions plays several roles – for example, `Number`:

*   You can use it as a function and convert values to numbers:

    ```
    [](#cb143-1)assert.equal(Number('123'), 123);
    ```

*   `Number.prototype` provides the properties for numbers – for example, method `.toString()`:

    ```
    [](#cb144-1)assert.equal((123).toString, Number.prototype.toString);
    ```

*   `Number` is a namespace/container object for tool functions for numbers – for example:

    ```
    [](#cb145-1)assert.equal(Number.isInteger(123), true);
    ```

*   Lastly, you can also use `Number` as a class and create number objects. These objects are different from real numbers and should be avoided.

    ```
    [](#cb146-1)assert.notEqual(new Number(123), 123);
    [](#cb146-2)assert.equal(new Number(123).valueOf(), 123);
    ```

#### 13.6.1.1 Wrapping primitive values

The constructor functions related to primitive types are also called *wrapper types* because they provide the canonical way of converting primitive values to objects. In the process, primitive values are “wrapped” in objects.

```
[](#cb147-1)const prim = true;
[](#cb147-2)assert.equal(typeof prim, 'boolean');
[](#cb147-3)assert.equal(prim instanceof Boolean, false);
[](#cb147-4)
[](#cb147-5)const wrapped = Object(prim);
[](#cb147-6)assert.equal(typeof wrapped, 'object');
[](#cb147-7)assert.equal(wrapped instanceof Boolean, true);
[](#cb147-8)
[](#cb147-9)assert.equal(wrapped.valueOf(), prim); // unwrap
```

Wrapping rarely matters in practice, but it is used internally in the language specification, to give primitives properties.

## 13.7 Converting between types

There are two ways in which values are converted to other types in JavaScript:

*   Explicit conversion: via functions such as `String()`.
*   *Coercion* (automatic conversion): happens when an operation receives operands/parameters that it can’t work with.

### 13.7.1 Explicit conversion between types

The function associated with a primitive type explicitly converts values to that type:

```
> Boolean(0)
false
> Number('123')
123
> String(123)
'123'
```

You can also use `Object()` to convert values to objects:

```
> typeof Object(123)
'object'
```

### 13.7.2 Coercion (automatic conversion between types)

For many operations, JavaScript automatically converts the operands/parameters if their types don’t fit. This kind of automatic conversion is called *coercion*.

For example, the multiplication operator coerces its operands to numbers:

```
> '7' * '3'
21
```

Many built-in functions coerce, too. For example, `parseInt()` coerces its parameter to string (parsing stops at the first character that is not a digit):

```
> parseInt(123.45)
123
```

![](media/file6.svg)  **Exercise: Converting values to primitives**

`exercises/values/conversion_exrc.mjs`

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 14 Operators

* * *

*   14.1 [Making sense of operators](#ch015.xhtml_making-sense-of-operators)
    *   14.1.1 [Operators coerce their operands to appropriate types](#ch015.xhtml_operators-coerce-their-operands-to-appropriate-types)
    *   14.1.2 [Most operators only work with primitive values](#ch015.xhtml_most-operators-only-work-with-primitive-values)
*   14.2 [The plus operator (`+`)](#ch015.xhtml_the-plus-operator)
*   14.3 [Assignment operators](#ch015.xhtml_assignment-operators)
    *   14.3.1 [The plain assignment operator](#ch015.xhtml_the-plain-assignment-operator)
    *   14.3.2 [Compound assignment operators](#ch015.xhtml_compound-assignment-operators)
    *   14.3.3 [A list of all compound assignment operators](#ch015.xhtml_a-list-of-all-compound-assignment-operators)
*   14.4 [Equality: `==` vs. `===`](#ch015.xhtml_equality-vs.)
    *   14.4.1 [Loose equality (`==` and `!=`)](#ch015.xhtml_loose-equality-and)
    *   14.4.2 [Strict equality (`===` and `!==`)](#ch015.xhtml_strict-equality)
    *   14.4.3 [Recommendation: always use strict equality](#ch015.xhtml_recommendation-always-use-strict-equality)
    *   14.4.4 [Even stricter than `===`: `Object.is()`](#ch015.xhtml_Object.is)
*   14.5 [Ordering operators](#ch015.xhtml_ordering-operators)
*   14.6 [Various other operators](#ch015.xhtml_various-other-operators)
    *   14.6.1 [Comma operator](#ch015.xhtml_comma-operator)
    *   14.6.2 [`void` operator](#ch015.xhtml_void-operator)

* * *

## 14.1 Making sense of operators

JavaScript’s operators may seem quirky. With the following two rules, they are easier to understand:

*   Operators coerce their operands to appropriate types
*   Most operators only work with primitive values

### 14.1.1 Operators coerce their operands to appropriate types

If an operator gets operands that don’t have the proper types, it rarely throws an exception. Instead, it *coerces* (automatically converts) the operands so that it can work with them. Let’s look at two examples.

First, the multiplication operator can only work with numbers. Therefore, it converts strings to numbers before computing its result.

```
> '7' * '3'
21
```

Second, the square brackets operator (`[ ]`) for accessing the properties of an object can only handle strings and symbols. All other values are coerced to string:

```
[](#cb153-1)const obj = {};
[](#cb153-2)obj['true'] = 123;
[](#cb153-3)
[](#cb153-4)// Coerce true to the string 'true'
[](#cb153-5)assert.equal(obj[true], 123);
```

### 14.1.2 Most operators only work with primitive values

As mentioned before, most operators only work with primitive values. If an operand is an object, it is usually coerced to a primitive value – for example:

```
> [1,2,3] + [4,5,6]
'1,2,34,5,6'
```

Why? The plus operator first coerces its operands to primitive values:

```
> String([1,2,3])
'1,2,3'
> String([4,5,6])
'4,5,6'
```

Next, it concatenates the two strings:

```
> '1,2,3' + '4,5,6'
'1,2,34,5,6'
```

## 14.2 The plus operator (`+`)

The plus operator works as follows in JavaScript:

*   First, it converts both operands to primitive values. Then it switches to one of two modes:
    *   String mode: If one of the two primitive values is a string, then it converts the other one to a string, concatenates both strings, and returns the result.
    *   Number mode: Otherwise, It converts both operands to numbers, adds them, and returns the result.

String mode lets us use `+` to assemble strings:

```
> 'There are ' + 3 + ' items'
'There are 3 items'
```

Number mode means that if neither operand is a string (or an object that becomes a string) then everything is coerced to numbers:

```
> 4 + true
5
```

`Number(true)` is `1`.

## 14.3 Assignment operators

### 14.3.1 The plain assignment operator

The plain assignment operator is used to change storage locations:

```
[](#cb159-1)x = value; // assign to a previously declared variable
[](#cb159-2)obj.propKey = value; // assign to a property
[](#cb159-3)arr[index] = value; // assign to an Array element
```

Initializers in variable declarations can also be viewed as a form of assignment:

```
[](#cb160-1)const x = value;
[](#cb160-2)let y = value;
```

### 14.3.2 Compound assignment operators

Given an operator `op`, the following two ways of assigning are equivalent:

```
myvar op= value
myvar = myvar op value
```

If, for example, `op` is `+`, then we get the operator `+=` that works as follows.

```
[](#cb162-1)let str = '';
[](#cb162-2)str += '<b>';
[](#cb162-3)str += 'Hello!';
[](#cb162-4)str += '</b>';
[](#cb162-5)
[](#cb162-6)assert.equal(str, '<b>Hello!</b>');
```

### 14.3.3 A list of all compound assignment operators

*   Arithmetic operators:

    ```
    += -= *= /= %= **=
    ```

    `+=` also works for string concatenation

*   Bitwise operators:

    ```
    <<= >>= >>>= &= ^= |=
    ```

## 14.4 Equality: `==` vs. `===`

JavaScript has two kinds of equality operators: loose equality (`==`) and strict equality (`===`). The recommendation is to always use the latter.

![](media/file5.svg)  **Other names for `==` and `===`**

*   `==` is also called *double equals*. Its official name in the language specification is [*abstract equality comparison*](https://tc39.github.io/ecma262/#sec-abstract-equality-comparison).
*   `===` is also called *triple equals*.

### 14.4.1 Loose equality (`==` and `!=`)

Loose equality is one of JavaScript’s quirks. It often coerces operands. Some of those coercions make sense:

```
> '123' == 123
true
> false == 0
true
```

Others less so:

```
> '' == 0
true
```

Objects are coerced to primitives if (and only if!) the other operand is primitive:

```
> [1, 2, 3] == '1,2,3'
true
> ['1', '2', '3'] == '1,2,3'
true
```

If both operands are objects, they are only equal if they are the same object:

```
> [1, 2, 3] == ['1', '2', '3']
false
> [1, 2, 3] == [1, 2, 3]
false

> const arr = [1, 2, 3];
> arr == arr
true
```

Lastly, `==` considers `undefined` and `null` to be equal:

```
> undefined == null
true
```

### 14.4.2 Strict equality (`===` and `!==`)

Strict equality never coerces. Two values are only equal if they have the same type. Let’s revisit our previous interaction with the `==` operator and see what the `===` operator does:

```
> false === 0
false
> '123' === 123
false
```

An object is only equal to another value if that value is the same object:

```
> [1, 2, 3] === '1,2,3'
false
> ['1', '2', '3'] === '1,2,3'
false

> [1, 2, 3] === ['1', '2', '3']
false
> [1, 2, 3] === [1, 2, 3]
false

> const arr = [1, 2, 3];
> arr === arr
true
```

The `===` operator does not consider `undefined` and `null` to be equal:

```
> undefined === null
false
```

### 14.4.3 Recommendation: always use strict equality

I recommend to always use `===`. It makes your code easier to understand and spares you from having to think about the quirks of `==`.

Let’s look at two use cases for `==` and what I recommend to do instead.

#### 14.4.3.1 Use case for `==`: comparing with a number or a string

`==` lets you check if a value `x` is a number or that number as a string – with a single comparison:

```
[](#cb173-1)if (x == 123) {
[](#cb173-2)  // x is either 123 or '123'
[](#cb173-3)}
```

I prefer either of the following two alternatives:

```
[](#cb174-1)if (x === 123 || x === '123') ···
[](#cb174-2)if (Number(x) === 123) ···
```

You can also convert `x` to a number when you first encounter it.

#### 14.4.3.2 Use case for `==`: comparing with `undefined` or `null`

Another use case for `==` is to check if a value `x` is either `undefined` or `null`:

```
[](#cb175-1)if (x == null) {
[](#cb175-2)  // x is either null or undefined
[](#cb175-3)}
```

The problem with this code is that you can’t be sure if someone meant to write it that way or if they made a typo and meant `=== null`.

I prefer either of the following two alternatives:

```
[](#cb176-1)if (x === undefined || x === null) ···
[](#cb176-2)if (!x) ···
```

A downside of the second alternative is that it accepts values other than `undefined` and `null`, but it is a well-established pattern in JavaScript (to be explained in detail in [§16.3 “Truthiness-based existence checks”](#ch017.xhtml_truthiness-existence-checks)).

The following three conditions are also roughly equivalent:

```
[](#cb177-1)if (x != null) ···
[](#cb177-2)if (x !== undefined && x !== null) ···
[](#cb177-3)if (x) ···
```

### 14.4.4 Even stricter than `===`: `Object.is()`

Method `Object.is()` compares two values:

```
> Object.is(123, 123)
true
> Object.is(123, '123')
false
```

It is even stricter than `===`. For example, it considers `NaN`, [the error value for computations involving numbers](#ch018.xhtml_nan), to be equal to itself:

```
> Object.is(NaN, NaN)
true
> NaN === NaN
false
```

That is occasionally useful. For example, you can use it to implement an improved version of the Array method `.indexOf()`:

```
[](#cb180-1)const myIndexOf = (arr, elem) => {
[](#cb180-2)  return arr.findIndex(x => Object.is(x, elem));
[](#cb180-3)};
```

`myIndexOf()` finds `NaN` in an Array, while `.indexOf()` doesn’t:

```
> myIndexOf([0,NaN,2], NaN)
1
> [0,NaN,2].indexOf(NaN)
-1
```

The result `-1` means that `.indexOf()` couldn’t find its argument in the Array.

## 14.5 Ordering operators

Table 3: JavaScript’s ordering operators.

| Operator | name |
| --- | --- |
| `<` | less than |
| `<=` | Less than or equal |
| `>` | Greater than |
| `>=` | Greater than or equal |

JavaScript’s ordering operators (tbl. [3](#ch015.xhtml_tbl:ordering_operators)) work for both numbers and strings:

```
> 5 >= 2
true
> 'bar' < 'foo'
true
```

`<=` and `>=` are based on strict equality.

![](media/file4.svg)  **The ordering operators don’t work well for human languages**

The ordering operators don’t work well for comparing text in a human language, e.g., when capitalization or accents are involved. The details are explained in [§20.5 “Comparing strings”](#ch021.xhtml_comparing-strings).

## 14.6 Various other operators

Operators for booleans, strings, numbers, objects: are covered elsewhere in this book.

The next two subsections discuss two operators that are rarely used.

### 14.6.1 Comma operator

The comma operator has two operands, evaluates both of them and returns the second one:

```
> 'a', 'b'
'b'
```

For more information on this operator, see [*Speaking JavaScript*](http://speakingjs.com/es5/ch09.html#comma_operator).

### 14.6.2 `void` operator

The `void` operator evaluates its operand and returns `undefined`:

```
> void (3 + 2)
undefined
```

For more information on this operator, see [*Speaking JavaScript*](http://speakingjs.com/es5/ch09.html#void_operator).

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 15 The non-values `undefined` and `null`

* * *

*   15.1 [`undefined` vs. `null`](#ch016.xhtml_undefined-vs.-null)
*   15.2 [Occurrences of `undefined` and `null`](#ch016.xhtml_occurrences-of-undefined-and-null)
    *   15.2.1 [Occurrences of `undefined`](#ch016.xhtml_occurrences-of-undefined)
    *   15.2.2 [Occurrences of `null`](#ch016.xhtml_occurrences-of-null)
*   15.3 [Checking for `undefined` or `null`](#ch016.xhtml_checking-for-undefined-or-null)
*   15.4 [`undefined` and `null` don’t have properties](#ch016.xhtml_undefined-and-null-dont-have-properties)
*   15.5 [The history of `undefined` and `null`](#ch016.xhtml_the-history-of-undefined-and-null)

* * *

Many programming languages have one “non-value” called `null`. It indicates that a variable does not currently point to an object – for example, when it hasn’t been initialized yet.

In contrast, JavaScript has two of them: `undefined` and `null`.

## 15.1 `undefined` vs. `null`

Both values are very similar and often used interchangeably. How they differ is therefore subtle. The language itself makes the following distinction:

*   `undefined` means “not initialized” (e.g., a variable) or “not existing” (e.g., a property of an object).
*   `null` means “the intentional absence of any object value” (a quote from [the language specification](https://tc39.github.io/ecma262/#sec-null-value)).

Programmers may make the following distinction:

*   `undefined` is the non-value used by the language (when something is uninitialized, etc.).
*   `null` means “explicitly switched off”. That is, it helps implement a type that comprises both meaningful values and a meta-value that stands for “no meaningful value”. Such a type is called [*option type* or *maybe type*](https://en.wikipedia.org/wiki/Option_type) in functional programming.

## 15.2 Occurrences of `undefined` and `null`

The following subsections describe where `undefined` and `null` appear in the language. We’ll encounter several mechanisms that are explained in more detail later in this book.

### 15.2.1 Occurrences of `undefined`

Uninitialized variable `myVar`:

```
[](#cb185-1)let myVar;
[](#cb185-2)assert.equal(myVar, undefined);
```

Parameter `x` is not provided:

```
[](#cb186-1)function func(x) {
[](#cb186-2)  return x;
[](#cb186-3)}
[](#cb186-4)assert.equal(func(), undefined);
```

Property `.unknownProp` is missing:

```
[](#cb187-1)const obj = {};
[](#cb187-2)assert.equal(obj.unknownProp, undefined);
```

If you don’t explicitly specify the result of a function via a `return` statement, JavaScript returns `undefined` for you:

```
[](#cb188-1)function func() {}
[](#cb188-2)assert.equal(func(), undefined);
```

### 15.2.2 Occurrences of `null`

The prototype of an object is either an object or, at the end of a chain of prototypes, `null`. `Object.prototype` does not have a prototype:

```
> Object.getPrototypeOf(Object.prototype)
null
```

If you match a regular expression (such as `/a/`) against a string (such as `'x'`), you either get an object with matching data (if matching was successful) or `null` (if matching failed):

```
> /a/.exec('x')
null
```

The [JSON data format](#ch046.xhtml_ch_json) does not support `undefined`, only `null`:

```
> JSON.stringify({a: undefined, b: null})
'{"b":null}'
```

## 15.3 Checking for `undefined` or `null`

Checking for either:

```
[](#cb192-1)if (x === null) ···
[](#cb192-2)if (x === undefined) ···
```

Does `x` have a value?

```
[](#cb193-1)if (x !== undefined && x !== null) {
[](#cb193-2)  // ···
[](#cb193-3)}
[](#cb193-4)if (x) { // truthy?
[](#cb193-5)  // x is neither: undefined, null, false, 0, NaN, ''
[](#cb193-6)}
```

Is `x` either `undefined` or `null`?

```
[](#cb194-1)if (x === undefined || x === null) {
[](#cb194-2)  // ···
[](#cb194-3)}
[](#cb194-4)if (!x) { // falsy?
[](#cb194-5)  // x is: undefined, null, false, 0, NaN, ''
[](#cb194-6)}
```

*Truthy* means “is `true` if coerced to boolean”. *Falsy* means “is `false` if coerced to boolean”. Both concepts are explained properly in [§16.2 “Falsy and truthy values”](#ch017.xhtml_falsiness-truthiness).

## 15.4 `undefined` and `null` don’t have properties

`undefined` and `null` are the two only JavaScript values where you get an exception if you try to read a property. To explore this phenomenon, let’s use the following function, which reads (“gets”) property `.foo` and returns the result.

```
[](#cb195-1)function getFoo(x) {
[](#cb195-2)  return x.foo;
[](#cb195-3)}
```

If we apply `getFoo()` to various values, we can see that it only fails for `undefined` and `null`:

```
> getFoo(undefined)
TypeError: Cannot read property 'foo' of undefined
> getFoo(null)
TypeError: Cannot read property 'foo' of null

> getFoo(true)
undefined
> getFoo({})
undefined
```

## 15.5 The history of `undefined` and `null`

In Java (which inspired many aspects of JavaScript), initialization values depend on the static type of a variable:

*   Variables with object types are initialized with `null`.
*   Each primitive type has its own initialization value. For example, `int` variables are initialized with `0`.

In JavaScript, each variable can hold both object values and primitive values. Therefore, if `null` means “not an object”, JavaScript also needs an initialization value that means “neither an object nor a primitive value”. That initialization value is `undefined`.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 16 Booleans

* * *

*   16.1 [Converting to boolean](#ch017.xhtml_converting-to-boolean)
*   16.2 [Falsy and truthy values](#ch017.xhtml_falsiness-truthiness)
    *   16.2.1 [Checking for truthiness or falsiness](#ch017.xhtml_checking-for-truthiness-or-falsiness)
*   16.3 [Truthiness-based existence checks](#ch017.xhtml_truthiness-existence-checks)
    *   16.3.1 [Pitfall: truthiness-based existence checks are imprecise](#ch017.xhtml_pitfall-truthiness-based-existence-checks-are-imprecise)
    *   16.3.2 [Use case: was a parameter provided?](#ch017.xhtml_use-case-was-a-parameter-provided)
    *   16.3.3 [Use case: does a property exist?](#ch017.xhtml_use-case-does-a-property-exist)
*   16.4 [Conditional operator (`? :`)](#ch017.xhtml_conditional-operator)
*   16.5 [Binary logical operators: And (`x && y`), Or (`x || y`)](#ch017.xhtml_binary-logical-operators-and-x-y-or-x-y)
    *   16.5.1 [Logical And (`x && y`)](#ch017.xhtml_logical-and-x-y)
    *   16.5.2 [Logical Or (`||`)](#ch017.xhtml_logical-or)
    *   16.5.3 [Default values via logical Or (`||`)](#ch017.xhtml_default-values-via-logical-or)
*   16.6 [Logical Not (`!`)](#ch017.xhtml_logical-not)

* * *

The primitive type *boolean* comprises two values – `false` and `true`:

```
> typeof false
'boolean'
> typeof true
'boolean'
```

## 16.1 Converting to boolean

![](media/file5.svg)  **The meaning of “converting to [type]”**

“Converting to [type]” is short for “Converting arbitrary values to values of type [type]”.

These are three ways in which you can convert an arbitrary value `x` to a boolean.

*   `Boolean(x)`
    Most descriptive; recommended.

*   `x ? true : false`
    Uses the conditional operator (explained [later in this chapter](#ch017.xhtml_conditional-operator)).

*   `!!x`
    Uses [the logical Not operator (`!`)](#ch017.xhtml_logical-not). This operator coerces its operand to boolean. It is applied a second time to get a non-negated result.

Tbl. [4](#ch017.xhtml_tbl:converting_to_boolean) describes how various values are converted to boolean.

Table 4: Converting values to booleans.

| `x` | `Boolean(x)` |
| --- | --- |
| `undefined` | `false` |
| `null` | `false` |
| boolean value | `x` (no change) |
| number value | `0` `→` `false`, `NaN` `→` `false` |
|  | other numbers `→` `true` |
| string value | `''` `→` `false` |
|  | other strings `→` `true` |
| object value | always `true` |

## 16.2 Falsy and truthy values

When checking the condition of an `if` statement, a `while` loop, or a `do-while` loop, JavaScript works differently than you may expect. Take, for example, the following condition:

```
[](#cb198-1)if (value) {}
```

In many programming languages, this condition is equivalent to:

```
[](#cb199-1)if (value === true) {}
```

However, in JavaScript, it is equivalent to:

```
[](#cb200-1)if (Boolean(value) === true) {}
```

That is, JavaScript checks if `value` is `true` when converted to boolean. This kind of check is so common that the following names were introduced:

*   A value is called *truthy* if it is `true` when converted to boolean.
*   A value is called *falsy* if it is `false` when converted to boolean.

Each value is either truthy or falsy. Consulting tbl. [4](#ch017.xhtml_tbl:converting_to_boolean), we can make an exhaustive list of falsy values:

*   `undefined`, `null`
*   `false`
*   `0`, `NaN`
*   `''`

All other values (including all objects) are truthy:

```
> Boolean('abc')
true
> Boolean([])
true
> Boolean({})
true
```

### 16.2.1 Checking for truthiness or falsiness

```
[](#cb202-1)if (x) {
[](#cb202-2)  // x is truthy
[](#cb202-3)}
[](#cb202-4)
[](#cb202-5)if (!x) {
[](#cb202-6)  // x is falsy
[](#cb202-7)}
[](#cb202-8)
[](#cb202-9)if (x) {
[](#cb202-10)  // x is truthy
[](#cb202-11)} else {
[](#cb202-12)  // x is falsy
[](#cb202-13)}
[](#cb202-14)
[](#cb202-15)const result = x ? 'truthy' : 'falsy';
```

The conditional operator that is used in the last line, is explained [later in this chapter](#ch017.xhtml_conditional-operator).

![](media/file6.svg)  **Exercise: Truthiness**

`exercises/booleans/truthiness_exrc.mjs`

## 16.3 Truthiness-based existence checks

In JavaScript, if you read something that doesn’t exist (e.g., a missing parameter or a missing property), you usually get `undefined` as a result. In these cases, an existence check amounts to comparing a value with `undefined`. For example, the following code checks if object `obj` has the property `.prop`:

```
[](#cb203-1)if (obj.prop !== undefined) {
[](#cb203-2)  // obj has property .prop
[](#cb203-3)}
```

Due to `undefined` being falsy, we can shorten this check to:

```
[](#cb204-1)if (obj.prop) {
[](#cb204-2)  // obj has property .prop
[](#cb204-3)}
```

### 16.3.1 Pitfall: truthiness-based existence checks are imprecise

Truthiness-based existence checks have one pitfall: they are not very precise. Consider this previous example:

```
[](#cb205-1)if (obj.prop) {
[](#cb205-2)  // obj has property .prop
[](#cb205-3)}
```

The body of the `if` statement is skipped if:

*   `obj.prop` is missing (in which case, JavaScript returns `undefined`).

However, it is also skipped if:

*   `obj.prop` is `undefined`.
*   `obj.prop` is any other falsy value (`null`, `0`, `''`, etc.).

In practice, this rarely causes problems, but you have to be aware of this pitfall.

### 16.3.2 Use case: was a parameter provided?

A truthiness check is often used to determine if the caller of a function provided a parameter:

```
[](#cb206-1)function func(x) {
[](#cb206-2)  if (!x) {
[](#cb206-3)    throw new Error('Missing parameter x');
[](#cb206-4)  }
[](#cb206-5)  // ···
[](#cb206-6)}
```

On the plus side, this pattern is established and short. It correctly throws errors for `undefined` and `null`.

On the minus side, there is the previously mentioned pitfall: the code also throws errors for all other falsy values.

An alternative is to check for `undefined`:

```
[](#cb207-1)if (x === undefined) {
[](#cb207-2)  throw new Error('Missing parameter x');
[](#cb207-3)}
```

### 16.3.3 Use case: does a property exist?

Truthiness checks are also often used to determine if a property exists:

```
[](#cb208-1)function readFile(fileDesc) {
[](#cb208-2)  if (!fileDesc.path) {
[](#cb208-3)    throw new Error('Missing property: .path');
[](#cb208-4)  }
[](#cb208-5)  // ···
[](#cb208-6)}
[](#cb208-7)readFile({ path: 'foo.txt' }); // no error
```

This pattern is also established and has the usual caveat: it not only throws if the property is missing, but also if it exists and has any of the falsy values.

If you truly want to check if the property exists, you have to use [the `in` operator](#ch029.xhtml_in-operator):

```
[](#cb209-1)if (! ('path' in fileDesc)) {
[](#cb209-2)  throw new Error('Missing property: .path');
[](#cb209-3)}
```

## 16.4 Conditional operator (`? :`)

The conditional operator is the expression version of the `if` statement. Its syntax is:

```
«condition» ? «thenExpression» : «elseExpression»
```

It is evaluated as follows:

*   If `condition` is truthy, evaluate and return `thenExpression`.
*   Otherwise, evaluate and return `elseExpression`.

The conditional operator is also called *ternary operator* because it has three operands.

Examples:

```
> true ? 'yes' : 'no'
'yes'
> false ? 'yes' : 'no'
'no'
> '' ? 'yes' : 'no'
'no'
```

The following code demonstrates that whichever of the two branches “then” and “else” is chosen via the condition, only that branch is evaluated. The other branch isn’t.

```
[](#cb212-1)const x = (true ? console.log('then') : console.log('else'));
[](#cb212-2)
[](#cb212-3)// Output:
[](#cb212-4)// 'then'
```

## 16.5 Binary logical operators: And (`x && y`), Or (`x || y`)

The operators `&&` and `||` are *value-preserving* and *short-circuiting*. What does that mean?

*Value-preservation* means that operands are interpreted as booleans but returned unchanged:

```
> 12 || 'hello'
12
> 0 || 'hello'
'hello'
```

*Short-circuiting* means if the first operand already determines the result, then the second operand is not evaluated. The only other operator that delays evaluating its operands is the conditional operator. Usually, all operands are evaluated before performing an operation.

For example, logical And (`&&`) does not evaluate its second operand if the first one is falsy:

```
[](#cb214-1)const x = false && console.log('hello');
[](#cb214-2)// No output
```

If the first operand is truthy, `console.log()` is executed:

```
[](#cb215-1)const x = true && console.log('hello');
[](#cb215-2)
[](#cb215-3)// Output:
[](#cb215-4)// 'hello'
```

### 16.5.1 Logical And (`x && y`)

The expression `a && b` (“`a` And `b`”) is evaluated as follows:

1.  Evaluate `a`.
2.  Is the result falsy? Return it.
3.  Otherwise, evaluate `b` and return the result.

In other words, the following two expressions are roughly equivalent:

```
[](#cb216-1)a && b
[](#cb216-2)!a ? a : b
```

Examples:

```
> false && true
false
> false && 'abc'
false

> true && false
false
> true && 'abc'
'abc'

> '' && 'abc'
''
```

### 16.5.2 Logical Or (`||`)

The expression `a || b` (“`a` Or `b`”) is evaluated as follows:

1.  Evaluate `a`.
2.  Is the result truthy? Return it.
3.  Otherwise, evaluate `b` and return the result.

In other words, the following two expressions are roughly equivalent:

```
[](#cb218-1)a || b
[](#cb218-2)a ? a : b
```

Examples:

```
> true || false
true
> true || 'abc'
true

> false || true
true
> false || 'abc'
'abc'

> 'abc' || 'def'
'abc'
```

### 16.5.3 Default values via logical Or (`||`)

Sometimes you receive a value and only want to use it if it isn’t either `null` or `undefined`. Otherwise, you’d like to use a default value, as a fallback. You can do that via the `||` operator:

```
[](#cb220-1)const valueToUse = valueReceived || defaultValue;
```

The following code shows a real-world example:

```
[](#cb221-1)function countMatches(regex, str) {
[](#cb221-2)  const matchResult = str.match(regex); // null or Array
[](#cb221-3)  return (matchResult || []).length;
[](#cb221-4)}
```

If there are one or more matches for `regex` inside `str` then `.match()` returns an Array. If there are no matches, it unfortunately returns `null` (and not the empty Array). We fix that via the `||` operator.

![](media/file6.svg)  **Exercise: Default values via the Or operator (`||`)**

`exercises/booleans/default_via_or_exrc.mjs`

## 16.6 Logical Not (`!`)

The expression `!x` (“Not `x`”) is evaluated as follows:

1.  Evaluate `x`.
2.  Is it truthy? Return `false`.
3.  Otherwise, return `true`.

Examples:

```
> !false
true
> !true
false

> !0
true
> !123
false

> !''
true
> !'abc'
false
```

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 17 Numbers

* * *

*   17.1 [JavaScript only has floating point numbers](#ch018.xhtml_javascript-only-has-floating-point-numbers)
*   17.2 [Number literals](#ch018.xhtml_number-literals)
    *   17.2.1 [Integer literals](#ch018.xhtml_integer-literals)
    *   17.2.2 [Floating point literals](#ch018.xhtml_floating-point-literals)
    *   17.2.3 [Syntactic pitfall: properties of integer literals](#ch018.xhtml_syntactic-pitfall-properties-of-integer-literals)
*   17.3 [Arithmetic operators](#ch018.xhtml_arithmetic-operators)
    *   17.3.1 [Binary arithmetic operators](#ch018.xhtml_binary-arithmetic-operators)
    *   17.3.2 [Unary plus (`+`) and negation (`-`)](#ch018.xhtml_unary-plus-and-negation--)
    *   17.3.3 [Incrementing (`++`) and decrementing (`--`)](#ch018.xhtml_incrementing-and-decrementing---)
*   17.4 [Converting to number](#ch018.xhtml_converting-to-number)
*   17.5 [Error values](#ch018.xhtml_error-values)
*   17.6 [Error value: `NaN`](#ch018.xhtml_nan)
    *   17.6.1 [Checking for `NaN`](#ch018.xhtml_checking-for-nan)
    *   17.6.2 [Finding `NaN` in Arrays](#ch018.xhtml_finding-nan-in-arrays)
*   17.7 [Error value: `Infinity`](#ch018.xhtml_error-value-infinity)
    *   17.7.1 [`Infinity` as a default value](#ch018.xhtml_infinity-as-a-default-value)
    *   17.7.2 [Checking for `Infinity`](#ch018.xhtml_checking-for-infinity)
*   17.8 [The precision of numbers: careful with decimal fractions](#ch018.xhtml_the-precision-of-numbers-careful-with-decimal-fractions)
*   17.9 [(Advanced)](#ch018.xhtml_advanced-2)
*   17.10 [Background: floating point precision](#ch018.xhtml_background-floating-point-precision)
    *   17.10.1 [A simplified representation of floating point numbers](#ch018.xhtml_a-simplified-representation-of-floating-point-numbers)
*   17.11 [Integers in JavaScript](#ch018.xhtml_integers-in-javascript)
    *   17.11.1 [Converting to integer](#ch018.xhtml_converting-to-integer)
    *   17.11.2 [Ranges of integers in JavaScript](#ch018.xhtml_ranges-of-integers-in-javascript)
    *   17.11.3 [Safe integers](#ch018.xhtml_safe-integers)
*   17.12 [Bitwise operators](#ch018.xhtml_bitwise-operators)
    *   17.12.1 [Internally, bitwise operators work with 32-bit integers](#ch018.xhtml_internally-bitwise-operators-work-with-32-bit-integers)
    *   17.12.2 [Binary bitwise operators](#ch018.xhtml_binary-bitwise-operators)
    *   17.12.3 [Bitwise Not](#ch018.xhtml_bitwise-not)
    *   17.12.4 [Bitwise shift operators](#ch018.xhtml_bitwise-shift-operators)
    *   17.12.5 [`b32()`: displaying unsigned 32-bit integers in binary notation](#ch018.xhtml_b32)
*   17.13 [Quick reference: numbers](#ch018.xhtml_quick-reference-numbers)
    *   17.13.1 [Global functions for numbers](#ch018.xhtml_global-functions-for-numbers)
    *   17.13.2 [Static properties of `Number`](#ch018.xhtml_static-properties-of-number)
    *   17.13.3 [Static methods of `Number`](#ch018.xhtml_static-methods-of-number)
    *   17.13.4 [Methods of `Number.prototype`](#ch018.xhtml_methods-of-number.prototype)
    *   17.13.5 [Sources](#ch018.xhtml_sources)

* * *

This chapter covers JavaScript’s single type for numbers, `number`.

## 17.1 JavaScript only has floating point numbers

You can express both integers and floating point numbers in JavaScript:

```
[](#cb223-1)98
[](#cb223-2)123.45
```

However, there is only a single type for all numbers: they are all *doubles*, 64-bit floating point numbers implemented according to the IEEE Standard for Floating-Point Arithmetic (IEEE 754).

Integers are simply floating point numbers without a decimal fraction:

```
> 98 === 98.0
true
```

Note that, under the hood, most JavaScript engines are often able to use real integers, with all associated performance and storage size benefits.

## 17.2 Number literals

Let’s examine literals for numbers.

### 17.2.1 Integer literals

Several *integer literals* let you express integers with various bases:

```
[](#cb225-1)// Binary (base 2)
[](#cb225-2)assert.equal(0b11, 3);
[](#cb225-3)
[](#cb225-4)// Octal (base 8)
[](#cb225-5)assert.equal(0o10, 8);
[](#cb225-6)
[](#cb225-7)// Decimal (base 10):
[](#cb225-8)assert.equal(35, 35);
[](#cb225-9)
[](#cb225-10)// Hexadecimal (base 16)
[](#cb225-11)assert.equal(0xE7, 231);
```

### 17.2.2 Floating point literals

Floating point numbers can only be expressed in base 10.

Fractions:

```
> 35.0
35
```

Exponent: `eN` means ×10^N

```
> 3e2
300
> 3e-2
0.03
> 0.3e2
30
```

### 17.2.3 Syntactic pitfall: properties of integer literals

Accessing a property of an integer literal entails a pitfall: If the integer literal is immediately followed by a dot, then that dot is interpreted as a decimal dot:

```
7.toString(); // syntax error
```

There are four ways to work around this pitfall:

```
[](#cb229-1)7.0.toString()
[](#cb229-2)(7).toString()
[](#cb229-3)7..toString()
[](#cb229-4)7 .toString()  // space before dot
```

## 17.3 Arithmetic operators

### 17.3.1 Binary arithmetic operators

Tbl. [5](#ch018.xhtml_tbl:binary-arithmetic-operators) lists JavaScript’s binary arithmetic operators.

Table 5: Binary arithmetic operators.

| Operator | Name |  | Example |
| --- | --- | --- | --- |
| `n + m` | Addition | ES1 | `3 + 4` `→` `7` |
| `n - m` | Subtraction | ES1 | `9 - 1` `→` `8` |
| `n * m` | Multiplication | ES1 | `3 * 2.25` `→` `6.75` |
| `n / m` | Division | ES1 | `5.625 / 5` `→` `1.125` |
| `n % m` | Remainder | ES1 | `8 % 5` `→` `3` |
|  |  |  | `-8 % 5` `→` `-3` |
| `n ** m` | Exponentiation | ES2016 | `4 ** 2` `→` `16` |

#### 17.3.1.1 `%` is a remainder operator

`%` is a remainder operator, not a modulo operator. Its result has the sign of the first operand:

```
> 5 % 3
2
> -5 % 3
-2
```

For more information on the difference between remainder and modulo, see the blog post [“Remainder operator vs. modulo operator (with JavaScript code)”](https://2ality.com/2019/08/remainder-vs-modulo.html) on 2ality.

### 17.3.2 Unary plus (`+`) and negation (`-`)

Tbl. [6](#ch018.xhtml_tbl:unary-plus-negation) summarizes the two operators *unary plus* (`+`) and *negation* (`-`).

Table 6: The operators unary plus (`+`) and negation (`-`).

| Operator | Name |  | Example |
| --- | --- | --- | --- |
| `+n` | Unary plus | ES1 | `+(-7)` `→` `-7` |
| `-n` | Unary negation | ES1 | `-(-7)` `→` `7` |

Both operators coerce their operands to numbers:

```
> +'5'
5
> +'-12'
-12
> -'9'
-9
```

Thus, unary plus lets us convert arbitrary values to numbers.

### 17.3.3 Incrementing (`++`) and decrementing (`--`)

The incrementation operator `++` exists in a prefix version and a suffix version. In both versions, it destructively adds one to its operand. Therefore, its operand must be a storage location that can be changed.

The decrementation operator `--` works the same, but subtracts one from its operand. The next two examples explain the difference between the prefix and the suffix version.

Tbl. [7](#ch018.xhtml_tbl:incrementing-decrementing) summarizes the incrementation and decrementation operators.

Table 7: Incrementation operators and decrementation operators.

| Operator | Name |  | Example |
| --- | --- | --- | --- |
| `v++` | Increment | ES1 | `let v=0; [v++, v]` `→` `[0, 1]` |
| `++v` | Increment | ES1 | `let v=0; [++v, v]` `→` `[1, 1]` |
| `v--` | Decrement | ES1 | `let v=1; [v--, v]` `→` `[1, 0]` |
| `--v` | Decrement | ES1 | `let v=1; [--v, v]` `→` `[0, 0]` |

Next, we’ll look at examples of these operators in use.

Prefix `++` and prefix `--` change their operands and then return them.

```
[](#cb232-1)let foo = 3;
[](#cb232-2)assert.equal(++foo, 4);
[](#cb232-3)assert.equal(foo, 4);
[](#cb232-4)
[](#cb232-5)let bar = 3;
[](#cb232-6)assert.equal(--bar, 2);
[](#cb232-7)assert.equal(bar, 2);
```

Suffix `++` and suffix `--` return their operands and then change them.

```
[](#cb233-1)let foo = 3;
[](#cb233-2)assert.equal(foo++, 3);
[](#cb233-3)assert.equal(foo, 4);
[](#cb233-4)
[](#cb233-5)let bar = 3;
[](#cb233-6)assert.equal(bar--, 3);
[](#cb233-7)assert.equal(bar, 2);
```

#### 17.3.3.1 Operands: not just variables

You can also apply these operators to property values:

```
[](#cb234-1)const obj = { a: 1 };
[](#cb234-2)++obj.a;
[](#cb234-3)assert.equal(obj.a, 2);
```

And to Array elements:

```
[](#cb235-1)const arr = [ 4 ];
[](#cb235-2)arr[0]++;
[](#cb235-3)assert.deepEqual(arr, [5]);
```

![](media/file6.svg)  **Exercise: Number operators**

`exercises/numbers-math/is_odd_test.mjs`

## 17.4 Converting to number

These are three ways of converting values to numbers:

*   `Number(value)`
*   `+value`
*   `parseFloat(value)` (avoid; different than the other two!)

Recommendation: use the descriptive `Number()`. Tbl. [8](#ch018.xhtml_tbl:converting-values-to-numbers) summarizes how it works.

Table 8: Converting values to numbers.

| `x` | `Number(x)` |
| --- | --- |
| `undefined` | `NaN` |
| `null` | `0` |
| boolean | `false` `→` `0`, `true` `→` `1` |
| number | `x` (no change) |
| string | `''` `→` `0` |
|  | other `→` parsed number, ignoring leading/trailing whitespace |
| object | configurable (e.g. via `.valueOf()`) |

Examples:

```
[](#cb236-1)assert.equal(Number(123.45), 123.45);
[](#cb236-2)
[](#cb236-3)assert.equal(Number(''), 0);
[](#cb236-4)assert.equal(Number('\n 123.45 \t'), 123.45);
[](#cb236-5)assert.equal(Number('xyz'), NaN);
```

How objects are converted to numbers can be configured – for example, by overriding `.valueOf()`:

```
> Number({ valueOf() { return 123 } })
123
```

![](media/file6.svg)  **Exercise: Converting to number**

`exercises/numbers-math/parse_number_test.mjs`

## 17.5 Error values

Two number values are returned when errors happen:

*   `NaN`
*   `Infinity`

## 17.6 Error value: `NaN`

`NaN` is an abbreviation of “not a number”. Ironically, JavaScript considers it to be a number:

```
> typeof NaN
'number'
```

When is `NaN` returned?

`NaN` is returned if a number can’t be parsed:

```
> Number('$$$')
NaN
> Number(undefined)
NaN
```

`NaN` is returned if an operation can’t be performed:

```
> Math.log(-1)
NaN
> Math.sqrt(-1)
NaN
```

`NaN` is returned if an operand or argument is `NaN` (to propagate errors):

```
> NaN - 3
NaN
> 7 ** NaN
NaN
```

### 17.6.1 Checking for `NaN`

`NaN` is the only JavaScript value that is not strictly equal to itself:

```
[](#cb242-1)const n = NaN;
[](#cb242-2)assert.equal(n === n, false);
```

These are several ways of checking if a value `x` is `NaN`:

```
[](#cb243-1)const x = NaN;
[](#cb243-2)
[](#cb243-3)assert.equal(Number.isNaN(x), true); // preferred
[](#cb243-4)assert.equal(Object.is(x, NaN), true);
[](#cb243-5)assert.equal(x !== x, true);
```

In the last line, we use the comparison quirk to detect `NaN`.

### 17.6.2 Finding `NaN` in Arrays

Some Array methods can’t find `NaN`:

```
> [NaN].indexOf(NaN)
-1
```

Others can:

```
> [NaN].includes(NaN)
true
> [NaN].findIndex(x => Number.isNaN(x))
0
> [NaN].find(x => Number.isNaN(x))
NaN
```

Alas, there is no simple rule of thumb. You have to check for each method how it handles `NaN`.

## 17.7 Error value: `Infinity`

When is the error value `Infinity` returned?

Infinity is returned if a number is too large:

```
> Math.pow(2, 1023)
8.98846567431158e+307
> Math.pow(2, 1024)
Infinity
```

Infinity is returned if there is a division by zero:

```
> 5 / 0
Infinity
> -5 / 0
-Infinity
```

### 17.7.1 `Infinity` as a default value

`Infinity` is larger than all other numbers (except `NaN`), making it a good default value:

```
[](#cb248-1)function findMinimum(numbers) {
[](#cb248-2)  let min = Infinity;
[](#cb248-3)  for (const n of numbers) {
[](#cb248-4)    if (n < min) min = n;
[](#cb248-5)  }
[](#cb248-6)  return min;
[](#cb248-7)}
[](#cb248-8)
[](#cb248-9)assert.equal(findMinimum([5, -1, 2]), -1);
[](#cb248-10)assert.equal(findMinimum([]), Infinity);
```

### 17.7.2 Checking for `Infinity`

These are two common ways of checking if a value `x` is `Infinity`:

```
[](#cb249-1)const x = Infinity;
[](#cb249-2)
[](#cb249-3)assert.equal(x === Infinity, true);
[](#cb249-4)assert.equal(Number.isFinite(x), false);
```

![](media/file6.svg)  **Exercise: Comparing numbers**

`exercises/numbers-math/find_max_test.mjs`

## 17.8 The precision of numbers: careful with decimal fractions

Internally, JavaScript floating point numbers are represented with base 2 (according to the IEEE 754 standard). That means that decimal fractions (base 10) can’t always be represented precisely:

```
> 0.1 + 0.2
0.30000000000000004
> 1.3 * 3
3.9000000000000004
> 1.4 * 100000000000000
139999999999999.98
```

You therefore need to take rounding errors into consideration when performing arithmetic in JavaScript.

Read on for an explanation of this phenomenon.

![](media/file7.svg)  **Quiz: basic**

See [quiz app](#ch012.xhtml_quizzes).

## 17.9 (Advanced)

All remaining sections of this chapter are advanced.

## 17.10 Background: floating point precision

In JavaScript, computations with numbers don’t always produce correct results – for example:

```
> 0.1 + 0.2
0.30000000000000004
```

To understand why, we need to explore how JavaScript represents floating point numbers internally. It uses three integers to do so, which take up a total of 64 bits of storage (double precision):

| Component | Size | Integer range |
| --- | --- | --- |
| Sign | 1 bit | [0, 1] |
| Fraction | 52 bits | [0, 2^(52)−1] |
| Exponent | 11 bits | [−1023, 1024] |

The floating point number represented by these integers is computed as follows:

> (–1)^(sign) × 0b1.fraction × 2^(exponent)

This representation can’t encode a zero because its second component (involving the fraction) always has a leading 1\. Therefore, a zero is encoded via the special exponent −1023 and a fraction 0.

### 17.10.1 A simplified representation of floating point numbers

To make further discussions easier, we simplify the previous representation:

*   Instead of base 2 (binary), we use base 10 (decimal) because that’s what most people are more familiar with.
*   The *fraction* is a natural number that is interpreted as a fraction (digits after a point). We switch to a *mantissa*, an integer that is interpreted as itself. As a consequence, the exponent is used differently, but its fundamental role doesn’t change.
*   As the mantissa is an integer (with its own sign), we don’t need a separate sign, anymore.

The new representation works like this:

> mantissa × 10^(exponent)

Let’s try out this representation for a few floating point numbers.

*   For the integer −123, we mainly need the mantissa:

    ```
    > -123 * (10 ** 0)
    -123
    ```

*   For the number 1.5, we imagine there being a point after the mantissa. We use a negative exponent to move that point one digit to the left:

    ```
    > 15 * (10 ** -1)
    1.5
    ```

*   For the number 0.25, we move the point two digits to the left:

    ```
    > 25 * (10 ** -2)
    0.25
    ```

Representations with negative exponents can also be written as fractions with positive exponents in the denominators:

```
> 15 * (10 ** -1) === 15 / (10 ** 1)
true
> 25 * (10 ** -2) === 25 / (10 ** 2)
true
```

These fractions help with understanding why there are numbers that our encoding cannot represent:

*   `1/10` can be represented. It already has the required format: a power of 10 in the denominator.

*   `1/2` can be represented as `5/10`. We turned the 2 in the denominator into a power of 10 by multiplying the numerator and denominator by 5.

*   `1/4` can be represented as `25/100`. We turned the 4 in the denominator into a power of 10 by multiplying the numerator and denominator by 25.

*   `1/3` cannot be represented. There is no way to turn the denominator into a power of 10\. (The prime factors of 10 are 2 and 5\. Therefore, any denominator that only has these prime factors can be converted to a power of 10, by multiplying both the numerator and denominator by enough twos and fives. If a denominator has a different prime factor, then there’s nothing we can do.)

To conclude our excursion, we switch back to base 2:

*   `0.5 = 1/2` can be represented with base 2 because the denominator is already a power of 2.
*   `0.25 = 1/4` can be represented with base 2 because the denominator is already a power of 2.
*   `0.1 = 1/10` cannot be represented because the denominator cannot be converted to a power of 2.
*   `0.2 = 2/10` cannot be represented because the denominator cannot be converted to a power of 2.

Now we can see why `0.1 + 0.2` doesn’t produce a correct result: internally, neither of the two operands can be represented precisely.

The only way to compute precisely with decimal fractions is by internally switching to base 10\. For many programming languages, base 2 is the default and base 10 an option. For example, Java has the class [`BigDecimal`](https://docs.oracle.com/javase/8/docs/api/java/math/BigDecimal.html) and Python has the module [`decimal`](https://docs.python.org/3/library/decimal.html). There are tentative plans to add something similar to JavaScript: [the ECMAScript proposal “Decimal”](https://github.com/tc39/proposals/blob/master/stage-0-proposals.md) is currently at stage 0.

## 17.11 Integers in JavaScript

JavaScript doesn’t have a special type for integers. Instead, they are simply normal (floating point) numbers without a decimal fraction:

```
> 1 === 1.0
true
> Number.isInteger(1.0)
true
```

In this section, we’ll look at a few tools for working with these pseudo-integers.

### 17.11.1 Converting to integer

The recommended way of converting numbers to integers is to use one of the rounding methods of the `Math` object:

*   `Math.floor(n)`: returns the largest integer `i` ≤ `n`

    ```
    > Math.floor(2.1)
    2
    > Math.floor(2.9)
    2
    ```

*   `Math.ceil(n)`: returns the smallest integer `i` ≥ `n`

    ```
    > Math.ceil(2.1)
    3
    > Math.ceil(2.9)
    3
    ```

*   `Math.round(n)`: returns the integer that is “closest” to `n` with `__.5` being rounded up – for example:

    ```
    > Math.round(2.4)
    2
    > Math.round(2.5)
    3
    ```

*   `Math.trunc(n)`: removes any decimal fraction (after the point) that `n` has, therefore turning it into an integer.

    ```
    > Math.trunc(2.1)
    2
    > Math.trunc(2.9)
    2
    ```

For more information on rounding, consult [§18.3 “Rounding”](#ch019.xhtml_math-rounding).

### 17.11.2 Ranges of integers in JavaScript

These are important ranges of integers in JavaScript:

*   **Safe integers:** can be represented “safely” by JavaScript (more on what that means in the next subsection)
    *   Precision: 53 bits plus sign
    *   Range: (−2^(53), 2^(53))
*   **Array indices**
    *   Precision: 32 bits, unsigned
    *   Range: [0, 2^(32)−1) (excluding the maximum length)
    *   Typed Arrays have a larger range of 53 bits (safe and unsigned)
*   **Bitwise operators** (bitwise Or, etc.)
    *   Precision: 32 bits
    *   Range of unsigned right shift (`>>>`): unsigned, [0, 2^(32))
    *   Range of all other bitwise operators: signed, [−2^(31), 2^(31))

### 17.11.3 Safe integers

This is the range of integers that are *safe* in JavaScript (53 bits plus a sign):

> [–2^(53)–1, 2^(53)–1]

An integer is *safe* if it is represented by exactly one JavaScript number. Given that JavaScript numbers are encoded as a fraction multiplied by 2 to the power of an exponent, higher integers can also be represented, but then there are gaps between them.

For example (18014398509481984 is 2^(54)):

```
> 18014398509481984
18014398509481984
> 18014398509481985
18014398509481984
> 18014398509481986
18014398509481984
> 18014398509481987
18014398509481988
```

The following properties of `Number` help determine if an integer is safe:

```
[](#cb262-1)assert.equal(Number.MAX_SAFE_INTEGER, (2 ** 53) - 1);
[](#cb262-2)assert.equal(Number.MIN_SAFE_INTEGER, -Number.MAX_SAFE_INTEGER);
[](#cb262-3)
[](#cb262-4)assert.equal(Number.isSafeInteger(5), true);
[](#cb262-5)assert.equal(Number.isSafeInteger('5'), false);
[](#cb262-6)assert.equal(Number.isSafeInteger(5.1), false);
[](#cb262-7)assert.equal(Number.isSafeInteger(Number.MAX_SAFE_INTEGER), true);
[](#cb262-8)assert.equal(Number.isSafeInteger(Number.MAX_SAFE_INTEGER+1), false);
```

![](media/file6.svg)  **Exercise: Detecting safe integers**

`exercises/numbers-math/is_safe_integer_test.mjs`

#### 17.11.3.1 Safe computations

Let’s look at computations involving unsafe integers.

The following result is incorrect and unsafe, even though both of its operands are safe:

```
> 9007199254740990 + 3
9007199254740992
```

The following result is safe, but incorrect. The first operand is unsafe; the second operand is safe:

```
> 9007199254740995 - 10
9007199254740986
```

Therefore, the result of an expression `a op b` is correct if and only if:

```
[](#cb265-1)isSafeInteger(a) && isSafeInteger(b) && isSafeInteger(a op b)
```

That is, both operands and the result must be safe.

## 17.12 Bitwise operators

### 17.12.1 Internally, bitwise operators work with 32-bit integers

Internally, JavaScript’s bitwise operators work with 32-bit integers. They produce their results in the following steps:

*   Input (JavaScript numbers): The 1–2 operands are first converted to JavaScript numbers (64-bit floating point numbers) and then to 32-bit integers.
*   Computation (32-bit integers): The actual operation processes 32-bit integers and produces a 32-bit integer.
*   Output (JavaScript number): Before returning the result, it is converted back to a JavaScript number.

#### 17.12.1.1 The types of operands and results

For each bitwise operator, this book mentions the types of its operands and its result. Each type is always one of the following two:

| Type | Description | Size | Range |
| --- | --- | --- | --- |
| Int32 | signed 32-bit integer | 32 bits incl. sign | [−2^(31), 2^(31)) |
| Uint32 | unsigned 32-bit integer | 32 bits | [0, 2^(32)) |

Considering the previously mentioned steps, I recommend to pretend that bitwise operators internally work with unsigned 32-bit integers (step “computation”) and that Int32 and Uint32 only affect how JavaScript numbers are converted to and from integers (steps “input” and “output”).

#### 17.12.1.2 Displaying JavaScript numbers as unsigned 32-bit integers

While exploring the bitwise operators, it occasionally helps to display JavaScript numbers as unsigned 32-bit integers in binary notation. That’s what `b32()` does (whose implementation is shown later):

```
[](#cb266-1)assert.equal(
[](#cb266-2)  b32(-1),
[](#cb266-3)  '11111111111111111111111111111111');
[](#cb266-4)assert.equal(
[](#cb266-5)  b32(1),
[](#cb266-6)  '00000000000000000000000000000001');
[](#cb266-7)assert.equal(
[](#cb266-8)  b32(2 ** 31),
[](#cb266-9)  '10000000000000000000000000000000');
```

### 17.12.2 Binary bitwise operators

Table 9: Binary bitwise operators.

| Operation | Name | Type signature |  |
| --- | --- | --- | --- |
| `num1 & num2` | Bitwise And | Int32 × Int32 `→` Int32 | ES1 |
| `num1 ¦ num2` | Bitwise Or | Int32 × Int32 `→` Int32 | ES1 |
| `num1 ^ num2` | Bitwise Xor | Int32 × Int32 `→` Int32 | ES1 |

The binary bitwise operators (tbl. [9](#ch018.xhtml_tbl:binary-bitwise-operators)) combine the bits of their operands to produce their results:

```
> (0b1010 & 0b0011).toString(2).padStart(4, '0')
'0010'
> (0b1010 | 0b0011).toString(2).padStart(4, '0')
'1011'
> (0b1010 ^ 0b0011).toString(2).padStart(4, '0')
'1001'
```

### 17.12.3 Bitwise Not

Table 10: The bitwise Not operator.

| Operation | Name | Type signature |  |
| --- | --- | --- | --- |
| `~num` | Bitwise Not, ones’ complement | Int32 `→` Int32 | ES1 |

The bitwise Not operator (tbl. [10](#ch018.xhtml_tbl:bitwise-not)) inverts each binary digit of its operand:

```
> b32(~0b100)
'11111111111111111111111111111011'
```

### 17.12.4 Bitwise shift operators

Table 11: Bitwise shift operators.

| Operation | Name | Type signature |  |
| --- | --- | --- | --- |
| `num << count` | Left shift | Int32 × Uint32 `→` Int32 | ES1 |
| `num >> count` | Signed right shift | Int32 × Uint32 `→` Int32 | ES1 |
| `num >>> count` | Unsigned right shift | Uint32 × Uint32 `→` Uint32 | ES1 |

The shift operators (tbl. [11](#ch018.xhtml_tbl:bitwise-shift-operators-short)) move binary digits to the left or to the right:

```
> (0b10 << 1).toString(2)
'100'
```

`>>` preserves highest bit, `>>>` doesn’t:

```
> b32(0b10000000000000000000000000000010 >> 1)
'11000000000000000000000000000001'
> b32(0b10000000000000000000000000000010 >>> 1)
'01000000000000000000000000000001'
```

### 17.12.5 `b32()`: displaying unsigned 32-bit integers in binary notation

We have now used `b32()` a few times. The following code is an implementation of it:

```
[](#cb271-1)/**
[](#cb271-2) * Return a string representing n as a 32-bit unsigned integer,
[](#cb271-3) * in binary notation.
[](#cb271-4) */
[](#cb271-5)function b32(n) {
[](#cb271-6)  // >>> ensures highest bit isn’t interpreted as a sign
[](#cb271-7)  return (n >>> 0).toString(2).padStart(32, '0');
[](#cb271-8)}
[](#cb271-9)assert.equal(
[](#cb271-10)  b32(6),
[](#cb271-11)  '00000000000000000000000000000110');
```

`n >>> 0` means that we are shifting `n` zero bits to the right. Therefore, in principle, the `>>>` operator does nothing, but it still coerces `n` to an unsigned 32-bit integer:

```
> 12 >>> 0
12
> -12 >>> 0
4294967284
> (2**32 + 1) >>> 0
1
```

## 17.13 Quick reference: numbers

### 17.13.1 Global functions for numbers

JavaScript has the following four global functions for numbers:

*   `isFinite()`
*   `isNaN()`
*   `parseFloat()`
*   `parseInt()`

However, it is better to use the corresponding methods of `Number` (`Number.isFinite()`, etc.), which have fewer pitfalls. They were introduced with ES6 and are discussed below.

### 17.13.2 Static properties of `Number`

*   `.EPSILON: number` ^([ES6])

    The difference between 1 and the next representable floating point number. In general, [a machine epsilon](https://en.wikipedia.org/wiki/Machine_epsilon) provides an upper bound for rounding errors in floating point arithmetic.

    *   Approximately: 2.2204460492503130808472633361816 × 10^(-16)
*   `.MAX_SAFE_INTEGER: number` ^([ES6])

    The largest integer that JavaScript can represent unambiguously (2^(53)−1).

*   `.MAX_VALUE: number` ^([ES1])

    The largest positive finite JavaScript number.

    *   Approximately: 1.7976931348623157 × 10^(308)
*   `.MIN_SAFE_INTEGER: number` ^([ES6])

    The smallest integer that JavaScript can represent unambiguously (−2^(53)+1).

*   `.MIN_VALUE: number` ^([ES1])

    The smallest positive JavaScript number. Approximately 5 × 10^(−324).

*   `.NaN: number` ^([ES1])

    The same as the global variable `NaN`.

*   `.NEGATIVE_INFINITY: number` ^([ES1])

    The same as `-Number.POSITIVE_INFINITY`.

*   `.POSITIVE_INFINITY: number` ^([ES1])

    The same as the global variable `Infinity`.

### 17.13.3 Static methods of `Number`

*   `.isFinite(num: number): boolean` ^([ES6])

    Returns `true` if `num` is an actual number (neither `Infinity` nor `-Infinity` nor `NaN`).

    ```
    > Number.isFinite(Infinity)
    false
    > Number.isFinite(-Infinity)
    false
    > Number.isFinite(NaN)
    false
    > Number.isFinite(123)
    true
    ```

*   `.isInteger(num: number): boolean` ^([ES6])

    Returns `true` if `num` is a number and does not have a decimal fraction.

    ```
    > Number.isInteger(-17)
    true
    > Number.isInteger(33)
    true
    > Number.isInteger(33.1)
    false
    > Number.isInteger('33')
    false
    > Number.isInteger(NaN)
    false
    > Number.isInteger(Infinity)
    false
    ```

*   `.isNaN(num: number): boolean` ^([ES6])

    Returns `true` if `num` is the value `NaN`:

    ```
    > Number.isNaN(NaN)
    true
    > Number.isNaN(123)
    false
    > Number.isNaN('abc')
    false
    ```

*   `.isSafeInteger(num: number): boolean` ^([ES6])

    Returns `true` if `num` is a number and unambiguously represents an integer.

*   `.parseFloat(str: string): number` ^([ES6])

    Coerces its parameter to string and parses it as a floating point number. For converting strings to numbers, `Number()` (which ignores leading and trailing whitespace) is usually a better choice than `Number.parseFloat()` (which ignores leading whitespace and illegal trailing characters and can hide problems).

    ```
    > Number.parseFloat(' 123.4#')
    123.4
    > Number(' 123.4#')
    NaN
    ```

*   `.parseInt(str: string, radix=10): number` ^([ES6])

    Coerces its parameter to string and parses it as an integer, ignoring leading whitespace and illegal trailing characters:

    ```
    > Number.parseInt('  123#')
    123
    ```

    The parameter `radix` specifies the base of the number to be parsed:

    ```
    > Number.parseInt('101', 2)
    5
    > Number.parseInt('FF', 16)
    255
    ```

    Do not use this method to convert numbers to integers: coercing to string is inefficient. And stopping before the first non-digit is not a good algorithm for removing the fraction of a number. Here is an example where it goes wrong:

    ```
    > Number.parseInt(1e21, 10) // wrong
    1
    ```

    It is better to use one of the rounding functions of `Math` to convert a number to an integer:

    ```
    > Math.trunc(1e21) // correct
    1e+21
    ```

### 17.13.4 Methods of `Number.prototype`

(`Number.prototype` is where the methods of numbers are stored.)

*   `.toExponential(fractionDigits?: number): string` ^([ES3])

    Returns a string that represents the number via exponential notation. With `fractionDigits`, you can specify, how many digits should be shown of the number that is multiplied with the exponent (the default is to show as many digits as necessary).

    Example: number too small to get a positive exponent via `.toString()`.

    ```
    > 1234..toString()
    '1234'

    > 1234..toExponential() // 3 fraction digits
    '1.234e+3'
    > 1234..toExponential(5)
    '1.23400e+3'
    > 1234..toExponential(1)
    '1.2e+3'
    ```

    Example: fraction not small enough to get a negative exponent via `.toString()`.

    ```
    > 0.003.toString()
    '0.003'
    > 0.003.toExponential()
    '3e-3'
    ```

*   `.toFixed(fractionDigits=0): string` ^([ES3])

    Returns an exponent-free representation of the number, rounded to `fractionDigits` digits.

    ```
    > 0.00000012.toString() // with exponent
    '1.2e-7'

    > 0.00000012.toFixed(10) // no exponent
    '0.0000001200'
    > 0.00000012.toFixed()
    '0'
    ```

    If the number is 10^(21) or greater, even `.toFixed()` uses an exponent:

    ```
    > (10 ** 21).toFixed()
    '1e+21'
    ```

*   `.toPrecision(precision?: number): string` ^([ES3])

    Works like `.toString()`, but `precision` specifies how many digits should be shown. If `precision` is missing, `.toString()` is used.

    ```
    > 1234..toPrecision(3)  // requires exponential notation
    '1.23e+3'

    > 1234..toPrecision(4)
    '1234'

    > 1234..toPrecision(5)
    '1234.0'

    > 1.234.toPrecision(3)
    '1.23'
    ```

*   `.toString(radix=10): string` ^([ES1])

    Returns a string representation of the number.

    By default, you get a base 10 numeral as a result:

    ```
    > 123.456.toString()
    '123.456'
    ```

    If you want the numeral to have a different base, you can specify it via `radix`:

    ```
    > 4..toString(2) // binary (base 2)
    '100'
    > 4.5.toString(2)
    '100.1'

    > 255..toString(16) // hexadecimal (base 16)
    'ff'
    > 255.66796875.toString(16)
    'ff.ab'

    > 1234567890..toString(36)
    'kf12oi'
    ```

    `parseInt()` provides the inverse operation: it converts a string that contains an integer (no fraction!) numeral with a given base, to a number.

    ```
    > parseInt('kf12oi', 36)
    1234567890
    ```

### 17.13.5 Sources

*   Wikipedia
*   [TypeScript’s built-in typings](https://github.com/Microsoft/TypeScript/blob/master/lib/)
*   [MDN web docs for JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
*   [ECMAScript language specification](https://tc39.github.io/ecma262/)

![](media/file7.svg)  **Quiz: advanced**

See [quiz app](#ch012.xhtml_quizzes).

# 18 `Math`

* * *

*   18.1 [Data properties](#ch019.xhtml_data-properties)
*   18.2 [Exponents, roots, logarithms](#ch019.xhtml_exponents-roots-logarithms)
*   18.3 [Rounding](#ch019.xhtml_math-rounding)
*   18.4 [Trigonometric Functions](#ch019.xhtml_trigonometric-functions)
*   18.5 [Various other functions](#ch019.xhtml_various-other-functions)
*   18.6 [Sources](#ch019.xhtml_sources-1)

* * *

`Math` is an object with data properties and methods for processing numbers. You can see it as a poor man’s module: It was created long before JavaScript had modules.

## 18.1 Data properties

*   `Math.E: number` ^([ES1])

    Euler’s number, base of the natural logarithms, approximately 2.7182818284590452354.

*   `Math.LN10: number` ^([ES1])

    The natural logarithm of 10, approximately 2.302585092994046.

*   `Math.LN2: number` ^([ES1])

    The natural logarithm of 2, approximately 0.6931471805599453.

*   `Math.LOG10E: number` ^([ES1])

    The logarithm of *e* to base 10, approximately 0.4342944819032518.

*   `Math.LOG2E: number` ^([ES1])

    The logarithm of *e* to base 2, approximately 1.4426950408889634.

*   `Math.PI: number` ^([ES1])

    The mathematical constant π, ratio of a circle’s circumference to its diameter, approximately 3.1415926535897932.

*   `Math.SQRT1_2: number` ^([ES1])

    The square root of 1/2, approximately 0.7071067811865476.

*   `Math.SQRT2: number` ^([ES1])

    The square root of 2, approximately 1.4142135623730951.

## 18.2 Exponents, roots, logarithms

*   `Math.cbrt(x: number): number` ^([ES6])

    Returns the cube root of `x`.

    ```
    > Math.cbrt(8)
    2
    ```

*   `Math.exp(x: number): number` ^([ES1])

    Returns *e*^(`x`) (*e* being Euler’s number). The inverse of `Math.log()`.

    ```
    > Math.exp(0)
    1
    > Math.exp(1) === Math.E
    true
    ```

*   `Math.expm1(x: number): number` ^([ES6])

    Returns `Math.exp(x)-1`. The inverse of `Math.log1p()`. Very small numbers (fractions close to 0) are represented with a higher precision. Therefore, this function returns more precise values whenever `.exp()` returns values close to 1.

*   `Math.log(x: number): number` ^([ES1])

    Returns the natural logarithm of `x` (to base *e*, Euler’s number). The inverse of `Math.exp()`.

    ```
    > Math.log(1)
    0
    > Math.log(Math.E)
    1
    > Math.log(Math.E ** 2)
    2
    ```

*   `Math.log1p(x: number): number` ^([ES6])

    Returns `Math.log(1 + x)`. The inverse of `Math.expm1()`. Very small numbers (fractions close to 0) are represented with a higher precision. Therefore, you can provide this function with a more precise argument whenever the argument for `.log()` is close to 1.

*   `Math.log10(x: number): number` ^([ES6])

    Returns the logarithm of `x` to base 10\. The inverse of `10 ** x`.

    ```
    > Math.log10(1)
    0
    > Math.log10(10)
    1
    > Math.log10(100)
    2
    ```

*   `Math.log2(x: number): number` ^([ES6])

    Returns the logarithm of `x` to base 2\. The inverse of `2 ** x`.

    ```
    > Math.log2(1)
    0
    > Math.log2(2)
    1
    > Math.log2(4)
    2
    ```

*   `Math.pow(x: number, y: number): number` ^([ES1])

    Returns `x`^(`y`), `x` to the power of `y`. The same as `x ** y`.

    ```
    > Math.pow(2, 3)
    8
    > Math.pow(25, 0.5)
    5
    ```

*   `Math.sqrt(x: number): number` ^([ES1])

    Returns the square root of `x`. The inverse of `x ** 2`.

    ```
    > Math.sqrt(9)
    3
    ```

## 18.3 Rounding

Rounding means converting an arbitrary number to an integer (a number without a decimal fraction). The following functions implement different approaches to rounding.

*   `Math.ceil(x: number): number` ^([ES1])

    Returns the smallest (closest to −∞) integer `i` with `x` ≤ `i`.

    ```
    > Math.ceil(2.1)
    3
    > Math.ceil(2.9)
    3
    ```

*   `Math.floor(x: number): number` ^([ES1])

    Returns the largest (closest to +∞) integer `i` with `i` ≤ `x`.

    ```
    > Math.floor(2.1)
    2
    > Math.floor(2.9)
    2
    ```

*   `Math.round(x: number): number` ^([ES1])

    Returns the integer that is closest to `x`. If the decimal fraction of `x` is `.5` then `.round()` rounds up (to the integer closer to positive infinity):

    ```
    > Math.round(2.4)
    2
    > Math.round(2.5)
    3
    ```

*   `Math.trunc(x: number): number` ^([ES6])

    Removes the decimal fraction of `x` and returns the resulting integer.

    ```
    > Math.trunc(2.1)
    2
    > Math.trunc(2.9)
    2
    ```

Tbl. [12](#ch019.xhtml_tbl:math-rounding-functions) shows the results of the rounding functions for a few representative inputs.

Table 12: Rounding functions of `Math`. Note how things change with negative numbers because “larger” always means “closer to positive infinity”.

|  | `-2.9` | `-2.5` | `-2.1` | `2.1` | `2.5` | `2.9` |
| --- | --- | --- | --- | --- | --- | --- |
| `Math.floor` | `-3` | `-3` | `-3` | `2` | `2` | `2` |
| `Math.ceil` | `-2` | `-2` | `-2` | `3` | `3` | `3` |
| `Math.round` | `-3` | `-2` | `-2` | `2` | `3` | `3` |
| `Math.trunc` | `-2` | `-2` | `-2` | `2` | `2` | `2` |

## 18.4 Trigonometric Functions

All angles are specified in radians. Use the following two functions to convert between degrees and radians.

```
[](#cb300-1)function degreesToRadians(degrees) {
[](#cb300-2)  return degrees / 180 * Math.PI;
[](#cb300-3)}
[](#cb300-4)assert.equal(degreesToRadians(90), Math.PI/2);
[](#cb300-5)
[](#cb300-6)function radiansToDegrees(radians) {
[](#cb300-7)  return radians / Math.PI * 180;
[](#cb300-8)}
[](#cb300-9)assert.equal(radiansToDegrees(Math.PI), 180);
```

*   `Math.acos(x: number): number` ^([ES1])

    Returns the arc cosine (inverse cosine) of `x`.

    ```
    > Math.acos(0)
    1.5707963267948966
    > Math.acos(1)
    0
    ```

*   `Math.acosh(x: number): number` ^([ES6])

    Returns the inverse hyperbolic cosine of `x`.

*   `Math.asin(x: number): number` ^([ES1])

    Returns the arc sine (inverse sine) of `x`.

    ```
    > Math.asin(0)
    0
    > Math.asin(1)
    1.5707963267948966
    ```

*   `Math.asinh(x: number): number` ^([ES6])

    Returns the inverse hyperbolic sine of `x`.

*   `Math.atan(x: number): number` ^([ES1])

    Returns the arc tangent (inverse tangent) of `x`.

*   `Math.atanh(x: number): number` ^([ES6])

    Returns the inverse hyperbolic tangent of `x`.

*   `Math.atan2(y: number, x: number): number` ^([ES1])

    Returns the arc tangent of the quotient y/x.

*   `Math.cos(x: number): number` ^([ES1])

    Returns the cosine of `x`.

    ```
    > Math.cos(0)
    1
    > Math.cos(Math.PI)
    -1
    ```

*   `Math.cosh(x: number): number` ^([ES6])

    Returns the hyperbolic cosine of `x`.

*   `Math.hypot(...values: number[]): number` ^([ES6])

    Returns the square root of the sum of the squares of `values` (Pythagoras’ theorem):

    ```
    > Math.hypot(3, 4)
    5
    ```

*   `Math.sin(x: number): number` ^([ES1])

    Returns the sine of `x`.

    ```
    > Math.sin(0)
    0
    > Math.sin(Math.PI / 2)
    1
    ```

*   `Math.sinh(x: number): number` ^([ES6])

    Returns the hyperbolic sine of `x`.

*   `Math.tan(x: number): number` ^([ES1])

    Returns the tangent of `x`.

    ```
    > Math.tan(0)
    0
    > Math.tan(1)
    1.5574077246549023
    ```

*   `Math.tanh(x: number): number;` ^([ES6])

    Returns the hyperbolic tangent of `x`.

## 18.5 Various other functions

*   `Math.abs(x: number): number` ^([ES1])

    Returns the absolute value of `x`.

    ```
    > Math.abs(3)
    3
    > Math.abs(-3)
    3
    > Math.abs(0)
    0
    ```

*   `Math.clz32(x: number): number` ^([ES6])

    Counts the leading zero bits in the 32-bit integer `x`. Used in DSP algorithms.

    ```
    > Math.clz32(0b01000000000000000000000000000000)
    1
    > Math.clz32(0b00100000000000000000000000000000)
    2
    > Math.clz32(2)
    30
    > Math.clz32(1)
    31
    ```

*   `Math.max(...values: number[]): number` ^([ES1])

    Converts `values` to numbers and returns the largest one.

    ```
    > Math.max(3, -5, 24)
    24
    ```

*   `Math.min(...values: number[]): number` ^([ES1])

    Converts `values` to numbers and returns the smallest one.

    ```
    > Math.min(3, -5, 24)
    -5
    ```

*   `Math.random(): number` ^([ES1])

    Returns a pseudo-random number `n` where 0 ≤ `n` < 1.

    Computing a random integer `i` where 0 ≤ `i` < `max`:

    ```
    [](#cb311-1)function getRandomInteger(max) {
    [](#cb311-2)  return Math.floor(Math.random() * max);
    [](#cb311-3)}
    ```

*   `Math.sign(x: number): number` ^([ES6])

    Returns the sign of a number:

    ```
    > Math.sign(-8)
    -1
    > Math.sign(0)
    0
    > Math.sign(3)
    1
    ```

## 18.6 Sources

*   Wikipedia
*   [TypeScript’s built-in typings](https://github.com/Microsoft/TypeScript/blob/master/lib/)
*   [MDN web docs for JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
*   [ECMAScript language specification](https://tc39.github.io/ecma262/)

# 19 Unicode – a brief introduction (advanced)

* * *

*   19.1 [Code points vs. code units](#ch020.xhtml_code-points-vs.-code-units)
    *   19.1.1 [Code points](#ch020.xhtml_code-points)
    *   19.1.2 [Encoding Unicode code points: UTF-32, UTF-16, UTF-8](#ch020.xhtml_encoding-unicode-code-points-utf-32-utf-16-utf-8)
*   19.2 [Encodings used in web development: UTF-16 and UTF-8](#ch020.xhtml_encodings-used-in-web-development-utf-16-and-utf-8)
    *   19.2.1 [Source code internally: UTF-16](#ch020.xhtml_source-code-internally-utf-16)
    *   19.2.2 [Strings: UTF-16](#ch020.xhtml_strings-utf-16)
    *   19.2.3 [Source code in files: UTF-8](#ch020.xhtml_source-code-in-files-utf-8)
*   19.3 [Grapheme clusters – the real characters](#ch020.xhtml_grapheme-clusters-the-real-characters)

* * *

Unicode is a standard for representing and managing text in most of the world’s writing systems. Virtually all modern software that works with text, supports Unicode. The standard is maintained by the Unicode Consortium. A new version of the standard is published every year (with new emojis, etc.). Unicode version 1.0.0 was published in October 1991.

## 19.1 Code points vs. code units

Two concepts are crucial for understanding Unicode:

*   *Code points* are numbers that represent Unicode characters.
*   *Code units* are numbers that encode code points, to store or transmit Unicode text. One or more code units encode a single code point. Each code unit has the same size, which depends on the *encoding format* that is used. The most popular format, UTF-8, has 8-bit code units.

### 19.1.1 Code points

The first version of Unicode had 16-bit code points. Since then, the number of characters has grown considerably and the size of code points was extended to 21 bits. These 21 bits are partitioned in 17 planes, with 16 bits each:

*   Plane 0: **Basic Multilingual Plane (BMP)**, 0x0000–0xFFFF
    *   Contains characters for almost all modern languages (Latin characters, Asian characters, etc.) and many symbols.
*   Plane 1: Supplementary Multilingual Plane (SMP), 0x10000–0x1FFFF
    *   Supports historic writing systems (e.g., Egyptian hieroglyphs and cuneiform) and additional modern writing systems.
    *   Supports emojis and many other symbols.
*   Plane 2: Supplementary Ideographic Plane (SIP), 0x20000–0x2FFFF
    *   Contains additional CJK (Chinese, Japanese, Korean) ideographs.
*   Plane 3–13: Unassigned
*   Plane 14: Supplementary Special-Purpose Plane (SSP), 0xE0000–0xEFFFF
    *   Contains non-graphical characters such as tag characters and glyph variation selectors.
*   Plane 15–16: Supplementary Private Use Area (S PUA A/B), 0x0F0000–0x10FFFF
    *   Available for character assignment by parties outside the ISO and the Unicode Consortium. Not standardized.

Planes 1-16 are called supplementary planes or **astral planes**.

Let’s check the code points of a few characters:

```
> 'A'.codePointAt(0).toString(16)
'41'
> 'ü'.codePointAt(0).toString(16)
'fc'
> 'π'.codePointAt(0).toString(16)
'3c0'
> '🙂'.codePointAt(0).toString(16)
'1f642'
```

The hexadecimal numbers of the code points tell us that the first three characters reside in plane 0 (within 16 bits), while the emoji resides in plane 1.

### 19.1.2 Encoding Unicode code points: UTF-32, UTF-16, UTF-8

The main ways of encoding code points are three *Unicode Transformation Formats* (UTFs): UTF-32, UTF-16, UTF-8\. The number at the end of each format indicates the size (in bits) of its code units.

#### 19.1.2.1 UTF-32 (Unicode Transformation Format 32)

UTF-32 uses 32 bits to store code units, resulting in one code unit per code point. This format is the only one with *fixed-length encoding*; all others use a varying number of code units to encode a single code point.

#### 19.1.2.2 UTF-16 (Unicode Transformation Format 16)

UTF-16 uses 16-bit code units. It encodes code points as follows:

*   The BMP (first 16 bits of Unicode) is stored in single code units.

*   Astral planes: The BMP comprises 0x10_000 code points. Given that Unicode has a total of 0x110_000 code points, we still need to encode the remaining 0x100_000 code points (20 bits). The BMP has two ranges of unassigned code points that provide the necessary storage:

    *   Most significant 10 bits (*leading surrogate*): 0xD800-0xDBFF
    *   Least significant 10 bits (*trailing surrogate*): 0xDC00-0xDFFF

In other words, the two hexadecimal digits at the end contribute 8 bits. But we can only use those 8 bits if a BMP starts with one of the following 2-digit pairs:

*   D8, D9, DA, DB
*   DC, DD, DE, DF

Per surrogate, we have a choice between 4 pairs, which is where the remaining 2 bits come from.

As a consequence, each UTF-16 code unit is always either a leading surrogate, a trailing surrogate, or encodes a BMP code point.

These are two examples of UTF-16-encoded code points:

*   Code point 0x03C0 (π) is in the BMP and can therefore be represented by a single UTF-16 code unit: 0x03C0.
*   Code point 0x1F642 (`🙂`) is in an astral plane and represented by two code units: 0xD83D and 0xDE42.

#### 19.1.2.3 UTF-8 (Unicode Transformation Format 8)

UTF-8 has 8-bit code units. It uses 1–4 code units to encode a code point:

| Code points | Code units |
| --- | --- |
| 0000–007F | 0bbbbbbb (7 bits) |
| 0080–07FF | 110bbbbb, 10bbbbbb (5+6 bits) |
| 0800–FFFF | 1110bbbb, 10bbbbbb, 10bbbbbb (4+6+6 bits) |
| 10000–1FFFFF | 11110bbb, 10bbbbbb, 10bbbbbb, 10bbbbbb (3+6+6+6 bits) |

Notes:

*   The bit prefix of each code unit tells us:
    *   Is it first in a series of code units? If yes, how many code units will follow?
    *   Is it second or later in a series of code units?
*   The character mappings in the 0000–007F range are the same as ASCII, which leads to a degree of backward compatibility with older software.

Three examples:

| Character | Code point | Code units |
| --- | --- | --- |
| A | 0x0041 | 01000001 |
| π | 0x03C0 | 11001111, 10000000 |
| `🙂` | 0x1F642 | 11110000, 10011111, 10011001, 10000010 |

## 19.2 Encodings used in web development: UTF-16 and UTF-8

The Unicode encoding formats that are used in web development are: UTF-16 and UTF-8.

### 19.2.1 Source code internally: UTF-16

The ECMAScript specification internally represents source code as UTF-16.

### 19.2.2 Strings: UTF-16

The characters in JavaScript strings are based on UTF-16 code units:

```
> const smiley = '🙂';
> smiley.length
2
> smiley === '\uD83D\uDE42' // code units
true
```

For more information on Unicode and strings, consult [§20.6 “Atoms of text: Unicode characters, JavaScript characters, grapheme clusters”](#ch021.xhtml_atoms-of-text).

### 19.2.3 Source code in files: UTF-8

HTML and JavaScript are almost always encoded as UTF-8 these days.

For example, this is how HTML files usually start now:

```
[](#cb315-1)<!doctype html>
[](#cb315-2)<html>
[](#cb315-3)<head>
[](#cb315-4)  <meta charset="UTF-8">
[](#cb315-5)···
```

For HTML modules loaded in web browsers, the [standard encoding](https://html.spec.whatwg.org/multipage/webappapis.html#fetch-a-single-module-script) is also UTF-8.

## 19.3 Grapheme clusters – the real characters

The concept of a character becomes remarkably complex once you consider many of the world’s writing systems.

On one hand, there are Unicode characters, as represented by code points.

On the other hand, there are *grapheme clusters*. A grapheme cluster corresponds most closely to a symbol displayed on screen or paper. It is defined as “a horizontally segmentable unit of text”. Therefore, [official Unicode documents](https://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries) also call it a *user-perceived character*. One or more code point characters are needed to encode a grapheme cluster.

For example, the Devanagari *kshi* is encoded by 4 code points. We use spreading (`...`) to split a string into an Array with code point characters (for details, consult [§20.6.1 “Working with code points”](#ch021.xhtml_working-with-code-points)):

> ![Splitting the grapheme cluster for the Devanagari _kshi_ into code point characters.](media/file14.png)

Flag emojis are also grapheme clusters and composed of two code point characters – for example, the flag of Japan:

> ![Splitting a flag emoji into code point characters.](media/file15.png)

![](media/file1.svg)  **More information on grapheme clusters**

For more information, consult [“Let’s Stop Ascribing Meaning to Code Points”](https://manishearth.github.io/blog/2017/01/14/stop-ascribing-meaning-to-unicode-code-points/) by Manish Goregaokar.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 20 Strings

* * *

*   20.1 [Plain string literals](#ch021.xhtml_plain-string-literals)
    *   20.1.1 [Escaping](#ch021.xhtml_escaping)
*   20.2 [Accessing characters and code points](#ch021.xhtml_accessing-characters-and-code-points)
    *   20.2.1 [Accessing JavaScript characters](#ch021.xhtml_accessing-javascript-characters)
    *   20.2.2 [Accessing Unicode code point characters via `for-of` and spreading](#ch021.xhtml_accessing-unicode-code-point-characters-via-for-of-and-spreading)
*   20.3 [String concatenation via `+`](#ch021.xhtml_string-concatenation-via)
*   20.4 [Converting to string](#ch021.xhtml_converting-to-string)
    *   20.4.1 [Stringifying objects](#ch021.xhtml_stringifying-objects)
    *   20.4.2 [Customizing the stringification of objects](#ch021.xhtml_customizing-the-stringification-of-objects)
    *   20.4.3 [An alternate way of stringifying values](#ch021.xhtml_an-alternate-way-of-stringifying-values)
*   20.5 [Comparing strings](#ch021.xhtml_comparing-strings)
*   20.6 [Atoms of text: Unicode characters, JavaScript characters, grapheme clusters](#ch021.xhtml_atoms-of-text)
    *   20.6.1 [Working with code points](#ch021.xhtml_working-with-code-points)
    *   20.6.2 [Working with code units (char codes)](#ch021.xhtml_working-with-code-units-char-codes)
    *   20.6.3 [Caveat: grapheme clusters](#ch021.xhtml_caveat-grapheme-clusters)
*   20.7 [Quick reference: Strings](#ch021.xhtml_quickref-strings)
    *   20.7.1 [Converting to string](#ch021.xhtml_converting-to-string-1)
    *   20.7.2 [Numeric values of characters](#ch021.xhtml_numeric-values-of-characters)
    *   20.7.3 [String operators](#ch021.xhtml_string-operators)
    *   20.7.4 [`String.prototype`: finding and matching](#ch021.xhtml_string.prototype-finding-and-matching)
    *   20.7.5 [`String.prototype`: extracting](#ch021.xhtml_string-api-extracting)
    *   20.7.6 [`String.prototype`: combining](#ch021.xhtml_string.prototype-combining)
    *   20.7.7 [`String.prototype`: transforming](#ch021.xhtml_string.prototype-transforming)
    *   20.7.8 [Sources](#ch021.xhtml_sources-2)

* * *

Strings are primitive values in JavaScript and immutable. That is, string-related operations always produce new strings and never change existing strings.

## 20.1 Plain string literals

Plain string literals are delimited by either single quotes or double quotes:

```
[](#cb316-1)const str1 = 'abc';
[](#cb316-2)const str2 = "abc";
[](#cb316-3)assert.equal(str1, str2);
```

Single quotes are used more often because it makes it easier to mention HTML, where double quotes are preferred.

[The next chapter](#ch022.xhtml_ch_template-literals) covers *template literals*, which give you:

*   String interpolation
*   Multiple lines
*   Raw string literals (backslash has no special meaning)

### 20.1.1 Escaping

The backslash lets you create special characters:

*   Unix line break: `'\n'`
*   Windows line break: `'\r\n'`
*   Tab: `'\t'`
*   Backslash: `'\\'`

The backslash also lets you use the delimiter of a string literal inside that literal:

```
[](#cb317-1)assert.equal(
[](#cb317-2)  'She said: "Let\'s go!"',
[](#cb317-3)  "She said: \"Let's go!\"");
```

## 20.2 Accessing characters and code points

### 20.2.1 Accessing JavaScript characters

JavaScript has no extra data type for characters – characters are always represented as strings.

```
[](#cb318-1)const str = 'abc';
[](#cb318-2)
[](#cb318-3)// Reading a character at a given index
[](#cb318-4)assert.equal(str[1], 'b');
[](#cb318-5)
[](#cb318-6)// Counting the characters in a string:
[](#cb318-7)assert.equal(str.length, 3);
```

### 20.2.2 Accessing Unicode code point characters via `for-of` and spreading

Iterating over strings via `for-of` or spreading (`...`) visits Unicode code point characters. Each code point character is encoded by 1–2 JavaScript characters. For more information, see [§20.6 “Atoms of text: Unicode characters, JavaScript characters, grapheme clusters”](#ch021.xhtml_atoms-of-text).

This is how you iterate over the code point characters of a string via `for-of`:

```
[](#cb319-1)for (const ch of 'x🙂y') {
[](#cb319-2)  console.log(ch);
[](#cb319-3)}
[](#cb319-4)// Output:
[](#cb319-5)// 'x'
[](#cb319-6)// '🙂'
[](#cb319-7)// 'y'
```

And this is how you convert a string into an Array of code point characters via spreading:

```
[](#cb320-1)assert.deepEqual([...'x🙂y'], ['x', '🙂', 'y']);
```

## 20.3 String concatenation via `+`

If at least one operand is a string, the plus operator (`+`) converts any non-strings to strings and concatenates the result:

```
[](#cb321-1)assert.equal(3 + ' times ' + 4, '3 times 4');
```

The assignment operator `+=` is useful if you want to assemble a string, piece by piece:

```
[](#cb322-1)let str = ''; // must be `let`!
[](#cb322-2)str += 'Say it';
[](#cb322-3)str += ' one more';
[](#cb322-4)str += ' time';
[](#cb322-5)
[](#cb322-6)assert.equal(str, 'Say it one more time');
```

![](media/file5.svg)  **Concatenating via `+` is efficient**

Using `+` to assemble strings is quite efficient because most JavaScript engines internally optimize it.

![](media/file6.svg)  **Exercise: Concatenating strings**

`exercises/strings/concat_string_array_test.mjs`

## 20.4 Converting to string

These are three ways of converting a value `x` to a string:

*   `String(x)`
*   `''+x`
*   `x.toString()` (does not work for `undefined` and `null`)

Recommendation: use the descriptive and safe `String()`.

Examples:

```
[](#cb323-1)assert.equal(String(undefined), 'undefined');
[](#cb323-2)assert.equal(String(null), 'null');
[](#cb323-3)
[](#cb323-4)assert.equal(String(false), 'false');
[](#cb323-5)assert.equal(String(true), 'true');
[](#cb323-6)
[](#cb323-7)assert.equal(String(123.45), '123.45');
```

Pitfall for booleans: If you convert a boolean to a string via `String()`, you generally can’t convert it back via `Boolean()`:

```
> String(false)
'false'
> Boolean('false')
true
```

The only string for which `Boolean()` returns `false`, is the empty string.

### 20.4.1 Stringifying objects

Plain objects have a default string representation that is not very useful:

```
> String({a: 1})
'[object Object]'
```

Arrays have a better string representation, but it still hides much information:

```
> String(['a', 'b'])
'a,b'
> String(['a', ['b']])
'a,b'

> String([1, 2])
'1,2'
> String(['1', '2'])
'1,2'

> String([true])
'true'
> String(['true'])
'true'
> String(true)
'true'
```

Stringifying functions, returns their source code:

```
> String(function f() {return 4})
'function f() {return 4}'
```

### 20.4.2 Customizing the stringification of objects

You can override the built-in way of stringifying objects by implementing the method `toString()`:

```
[](#cb328-1)const obj = {
[](#cb328-2)  toString() {
[](#cb328-3)    return 'hello';
[](#cb328-4)  }
[](#cb328-5)};
[](#cb328-6)
[](#cb328-7)assert.equal(String(obj), 'hello');
```

### 20.4.3 An alternate way of stringifying values

The JSON data format is a text representation of JavaScript values. Therefore, [`JSON.stringify()`](#ch046.xhtml_JSON.stringify) can also be used to convert values to strings:

```
> JSON.stringify({a: 1})
'{"a":1}'
> JSON.stringify(['a', ['b']])
'["a",["b"]]'
```

The caveat is that JSON only supports `null`, booleans, numbers, strings, Arrays, and objects (which it always treats as if they were created by object literals).

Tip: The third parameter lets you switch on multiline output and specify how much to indent – for example:

```
[](#cb330-1)console.log(JSON.stringify({first: 'Jane', last: 'Doe'}, null, 2));
```

This statement produces the following output:

```
{
  "first": "Jane",
  "last": "Doe"
}
```

## 20.5 Comparing strings

Strings can be compared via the following operators:

```
< <= > >=
```

There is one important caveat to consider: These operators compare based on the numeric values of JavaScript characters. That means that the order that JavaScript uses for strings is different from the one used in dictionaries and phone books:

```
> 'A' < 'B' // ok
true
> 'a' < 'B' // not ok
false
> 'ä' < 'b' // not ok
false
```

Properly comparing text is beyond the scope of this book. It is supported via [the ECMAScript Internationalization API (`Intl`)](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Intl).

## 20.6 Atoms of text: Unicode characters, JavaScript characters, grapheme clusters

Quick recap of [§19 “Unicode – a brief introduction”](#ch020.xhtml_ch_unicode):

*   Unicode characters are represented by *code points* – numbers which have a range of 21 bits.
*   In JavaScript strings, Unicode is implemented via *code units* based on the encoding format UTF-16\. Each code unit is a 16-bit number. One to two of code units are needed to encode a single code point.
    *   Therefore, each JavaScript character is represented by a code unit. In the JavaScript standard library, code units are also called *char codes*. Which is what they are: numbers for JavaScript characters.
*   *Grapheme clusters* (*user-perceived characters*) are written symbols, as displayed on screen or paper. One or more Unicode characters are needed to encode a single grapheme cluster.

The following code demonstrates that a single Unicode character comprises one or two JavaScript characters. We count the latter via `.length`:

```
[](#cb334-1)// 3 Unicode characters, 3 JavaScript characters:
[](#cb334-2)assert.equal('abc'.length, 3);
[](#cb334-3)
[](#cb334-4)// 1 Unicode character, 2 JavaScript characters:
[](#cb334-5)assert.equal('🙂'.length, 2);
```

The following table summarizes the concepts we have just explored:

| Entity | Numeric representation | Size | Encoded via |
| --- | --- | --- | --- |
| Grapheme cluster |  |  | 1+ code points |
| Unicode character | Code point | 21 bits | 1–2 code units |
| JavaScript character | UTF-16 code unit | 16 bits | – |

### 20.6.1 Working with code points

Let’s explore JavaScript’s tools for working with code points.

A *code point escape* lets you specify a code point hexadecimally. It produces one or two JavaScript characters.

```
> '\u{1F642}'
'🙂'
```

`String.fromCodePoint()` converts a single code point to 1–2 JavaScript characters:

```
> String.fromCodePoint(0x1F642)
'🙂'
```

`.codePointAt()` converts 1–2 JavaScript characters to a single code point:

```
> '🙂'.codePointAt(0).toString(16)
'1f642'
```

You can *iterate* over a string, which visits Unicode characters (not JavaScript characters). Iteration is described [later in this book](#ch031.xhtml_ch_sync-iteration). One way of iterating is via a `for-of` loop:

```
[](#cb338-1)const str = '🙂a';
[](#cb338-2)assert.equal(str.length, 3);
[](#cb338-3)
[](#cb338-4)for (const codePointChar of str) {
[](#cb338-5)  console.log(codePointChar);
[](#cb338-6)}
[](#cb338-7)
[](#cb338-8)// Output:
[](#cb338-9)// '🙂'
[](#cb338-10)// 'a'
```

[*Spreading* (`...`) into Array literals](#ch032.xhtml_spreading-into-array-literals) is also based on iteration and visits Unicode characters:

```
> [...'🙂a']
[ '🙂', 'a' ]
```

That makes it a good tool for counting Unicode characters:

```
> [...'🙂a'].length
2
> '🙂a'.length
3
```

### 20.6.2 Working with code units (char codes)

Indices and lengths of strings are based on JavaScript characters (as represented by UTF-16 code units).

To specify a code unit hexadecimally, you can use a *code unit escape*:

```
> '\uD83D\uDE42'
'🙂'
```

And you can use `String.fromCharCode()`. *Char code* is the standard library’s name for *code unit*:

```
> String.fromCharCode(0xD83D) + String.fromCharCode(0xDE42)
'🙂'
```

To get the char code of a character, use `.charCodeAt()`:

```
> '🙂'.charCodeAt(0).toString(16)
'd83d'
```

### 20.6.3 Caveat: grapheme clusters

When working with text that may be written in any human language, it’s best to split at the boundaries of grapheme clusters, not at the boundaries of Unicode characters.

TC39 is working on [`Intl.Segmenter`](https://github.com/tc39/proposal-intl-segmenter), a proposal for the ECMAScript Internationalization API to support Unicode segmentation (along grapheme cluster boundaries, word boundaries, sentence boundaries, etc.).

Until that proposal becomes a standard, you can use one of several libraries that are available (do a web search for “JavaScript grapheme”).

## 20.7 Quick reference: Strings

Strings are immutable; none of the string methods ever modify their strings.

### 20.7.1 Converting to string

Tbl. [13](#ch021.xhtml_tbl:converting-to-string) describes how various values are converted to strings.

Table 13: Converting values to strings.

| `x` | `String(x)` |
| --- | --- |
| `undefined` | `'undefined'` |
| `null` | `'null'` |
| Boolean value | `false` `→` `'false'`, `true` `→` `'true'` |
| Number value | Example: `123` `→` `'123'` |
| String value | `x` (input, unchanged) |
| An object | Configurable via, e.g., `toString()` |

### 20.7.2 Numeric values of characters

*   **Char code:** represents a JavaScript character numerically. JavaScript’s name for *Unicode code unit*.
    *   Size: 16 bits, unsigned
    *   Convert number to character: `String.fromCharCode()` ^([ES1])
    *   Convert character to number: string method `.charCodeAt()` ^([ES1])
*   **Code point:** represents a Unicode character numerically.
    *   Size: 21 bits, unsigned (17 planes, 16 bits each)
    *   Convert number to character: `String.fromCodePoint()` ^([ES6])
    *   Convert character to number: string method `.codePointAt()` ^([ES6])

### 20.7.3 String operators

```
[](#cb344-1)// Access characters via []
[](#cb344-2)const str = 'abc';
[](#cb344-3)assert.equal(str[1], 'b');
[](#cb344-4)
[](#cb344-5)// Concatenate strings via +
[](#cb344-6)assert.equal('a' + 'b' + 'c', 'abc');
[](#cb344-7)assert.equal('take ' + 3 + ' oranges', 'take 3 oranges');
```

### 20.7.4 `String.prototype`: finding and matching

(`String.prototype` is where the methods of strings are stored.)

*   `.endsWith(searchString: string, endPos=this.length): boolean` ^([ES6])

    Returns `true` if the string would end with `searchString` if its length were `endPos`. Returns `false` otherwise.

    ```
    > 'foo.txt'.endsWith('.txt')
    true
    > 'abcde'.endsWith('cd', 4)
    true
    ```

*   `.includes(searchString: string, startPos=0): boolean` ^([ES6])

    Returns `true` if the string contains the `searchString` and `false` otherwise. The search starts at `startPos`.

    ```
    > 'abc'.includes('b')
    true
    > 'abc'.includes('b', 2)
    false
    ```

*   `.indexOf(searchString: string, minIndex=0): number` ^([ES1])

    Returns the lowest index at which `searchString` appears within the string or `-1, otherwise. Any returned index will be`minIndex` or higher.

    ```
    > 'abab'.indexOf('a')
    0
    > 'abab'.indexOf('a', 1)
    2
    > 'abab'.indexOf('c')
    -1
    ```

*   `.lastIndexOf(searchString: string, maxIndex=Infinity): number` ^([ES1])

    Returns the highest index at which `searchString` appears within the string or `-1, otherwise. Any returned index will be`maxIndex` or lower.

    ```
    > 'abab'.lastIndexOf('ab', 2)
    2
    > 'abab'.lastIndexOf('ab', 1)
    0
    > 'abab'.lastIndexOf('ab')
    2
    ```

*   [1 of 2] `.match(regExp: string | RegExp): RegExpMatchArray | null` ^([ES3])

    If `regExp` is a regular expression with flag `/g` not set, then `.match()` returns the first match for `regExp` within the string. Or `null` if there is no match. If `regExp` is a string, it is used to create a regular expression (think parameter of `new RegExp()`) before performing the previously mentioned steps.

    The result has the following type:

    ```
    [](#cb349-1)interface RegExpMatchArray extends Array<string> {
    [](#cb349-2)  index: number;
    [](#cb349-3)  input: string;
    [](#cb349-4)  groups: undefined | {
    [](#cb349-5)    [key: string]: string
    [](#cb349-6)  };
    [](#cb349-7)}
    ```

    Numbered capture groups become Array indices (which is why this type extends `Array`). [Named capture groups](#ch044.xhtml_named-capture-groups) (ES2018) become properties of `.groups`. In this mode, `.match()` works like `RegExp.prototype.exec()`.

    Examples:

    ```
    > 'ababb'.match(/a(b+)/)
    { 0: 'ab', 1: 'b', index: 0, input: 'ababb', groups: undefined }
    > 'ababb'.match(/a(?<foo>b+)/)
    { 0: 'ab', 1: 'b', index: 0, input: 'ababb', groups: { foo: 'b' } }
    > 'abab'.match(/x/)
    null
    ```

*   [2 of 2] `.match(regExp: RegExp): string[] | null` ^([ES3])

    If flag `/g` of `regExp` is set, `.match()` returns either an Array with all matches or `null` if there was no match.

    ```
    > 'ababb'.match(/a(b+)/g)
    [ 'ab', 'abb' ]
    > 'ababb'.match(/a(?<foo>b+)/g)
    [ 'ab', 'abb' ]
    > 'abab'.match(/x/g)
    null
    ```

*   `.search(regExp: string | RegExp): number` ^([ES3])

    Returns the index at which `regExp` occurs within the string. If `regExp` is a string, it is used to create a regular expression (think parameter of `new RegExp()`).

    ```
    > 'a2b'.search(/[0-9]/)
    1
    > 'a2b'.search('[0-9]')
    1
    ```

*   `.startsWith(searchString: string, startPos=0): boolean` ^([ES6])

    Returns `true` if `searchString` occurs in the string at index `startPos`. Returns `false` otherwise.

    ```
    > '.gitignore'.startsWith('.')
    true
    > 'abcde'.startsWith('bc', 1)
    true
    ```

### 20.7.5 `String.prototype`: extracting

*   `.slice(start=0, end=this.length): string` ^([ES3])

    Returns the substring of the string that starts at (including) index `start` and ends at (excluding) index `end`. If an index is negative, it is added to `.length` before it is used (`-1` becomes `this.length-1`, etc.).

    ```
    > 'abc'.slice(1, 3)
    'bc'
    > 'abc'.slice(1)
    'bc'
    > 'abc'.slice(-2)
    'bc'
    ```

*   `.split(separator: string | RegExp, limit?: number): string[]` ^([ES3])

    Splits the string into an Array of substrings – the strings that occur between the separators. The separator can be a string:

    ```
    > 'a | b | c'.split('|')
    [ 'a ', ' b ', ' c' ]
    ```

    It can also be a regular expression:

    ```
    > 'a : b : c'.split(/ *: */)
    [ 'a', 'b', 'c' ]
    > 'a : b : c'.split(/( *):( *)/)
    [ 'a', ' ', ' ', 'b', ' ', ' ', 'c' ]
    ```

    The last invocation demonstrates that captures made by groups in the regular expression become elements of the returned Array.

    **Warning: `.split('')` splits a string into JavaScript characters.** That doesn’t work well when dealing with astral Unicode characters (which are encoded as two JavaScript characters). For example, emojis are astral:

    ```
    > '🙂X🙂'.split('')
    [ '\uD83D', '\uDE42', 'X', '\uD83D', '\uDE42' ]
    ```

    Instead, it is better to use spreading:

    ```
    > [...'🙂X🙂']
    [ '🙂', 'X', '🙂' ]
    ```

*   `.substring(start: number, end=this.length): string` ^([ES1])

    Use `.slice()` instead of this method. `.substring()` wasn’t implemented consistently in older engines and doesn’t support negative indices.

### 20.7.6 `String.prototype`: combining

*   `.concat(...strings: string[]): string` ^([ES3])

    Returns the concatenation of the string and `strings`. `'a'.concat('b')` is equivalent to `'a'+'b'`. The latter is much more popular.

    ```
    > 'ab'.concat('cd', 'ef', 'gh')
    'abcdefgh'
    ```

*   `.padEnd(len: number, fillString=' '): string` ^([ES2017])

    Appends (fragments of) `fillString` to the string until it has the desired length `len`. If it already has or exceeds `len`, then it is returned without any changes.

    ```
    > '#'.padEnd(2)
    '# '
    > 'abc'.padEnd(2)
    'abc'
    > '#'.padEnd(5, 'abc')
    '#abca'
    ```

*   `.padStart(len: number, fillString=' '): string` ^([ES2017])

    Prepends (fragments of) `fillString` to the string until it has the desired length `len`. If it already has or exceeds `len`, then it is returned without any changes.

    ```
    > '#'.padStart(2)
    ' #'
    > 'abc'.padStart(2)
    'abc'
    > '#'.padStart(5, 'abc')
    'abca#'
    ```

*   `.repeat(count=0): string` ^([ES6])

    Returns the string, concatenated `count` times.

    ```
    > '*'.repeat()
    ''
    > '*'.repeat(3)
    '***'
    ```

### 20.7.7 `String.prototype`: transforming

*   `.normalize(form: 'NFC'|'NFD'|'NFKC'|'NFKD' = 'NFC'): string` ^([ES6])

    Normalizes the string according to [the Unicode Normalization Forms](https://unicode.org/reports/tr15/).

*   [1 of 2] `.replace(searchValue: string | RegExp, replaceValue: string): string` ^([ES3])

    Replace matches of `searchValue` with `replaceValue`. If `searchValue` is a string, only the first verbatim occurrence is replaced. If `searchValue` is a regular expression without flag `/g`, only the first match is replaced. If `searchValue` is a regular expression with `/g` then all matches are replaced.

    ```
    > 'x.x.'.replace('.', '#')
    'x#x.'
    > 'x.x.'.replace(/./, '#')
    '#.x.'
    > 'x.x.'.replace(/./g, '#')
    '####'
    ```

    Special characters in `replaceValue` are:

    *   `$$`: becomes `$`
    *   `$n`: becomes the capture of numbered group `n` (alas, `$0` stands for the string `'$0'`, it does not refer to the complete match)
    *   `$&`: becomes the complete match
    *   `` $` ``: becomes everything before the match
    *   `$'`: becomes everything after the match

    Examples:

    ```
    > 'a 2020-04 b'.replace(/([0-9]{4})-([0-9]{2})/, '|$2|')
    'a |04| b'
    > 'a 2020-04 b'.replace(/([0-9]{4})-([0-9]{2})/, '|$&|')
    'a |2020-04| b'
    > 'a 2020-04 b'.replace(/([0-9]{4})-([0-9]{2})/, '|$`|')
    'a |a | b'
    ```

    [Named capture groups](#ch044.xhtml_named-capture-groups) (ES2018) are supported, too:

    *   `$<name>` becomes the capture of named group `name`

    Example:

    ```
    [](#cb365-1)assert.equal(
    [](#cb365-2)  'a 2020-04 b'.replace(
    [](#cb365-3)    /(?<year>[0-9]{4})-(?<month>[0-9]{2})/, '|$<month>|'),
    [](#cb365-4)  'a |04| b');
    ```

*   [2 of 2] `.replace(searchValue: string | RegExp, replacer: (...args: any[]) => string): string` ^([ES3])

    If the second parameter is a function, occurrences are replaced with the strings it returns. Its parameters `args` are:

    *   `matched: string`. The complete match
    *   `g1: string|undefined`. The capture of numbered group 1
    *   `g2: string|undefined`. The capture of numbered group 2
    *   (Etc.)
    *   `offset: number`. Where was the match found in the input string?
    *   `input: string`. The whole input string

    ```
    [](#cb366-1)const regexp = /([0-9]{4})-([0-9]{2})/;
    [](#cb366-2)const replacer = (all, year, month) => '|' + all + '|';
    [](#cb366-3)assert.equal(
    [](#cb366-4)  'a 2020-04 b'.replace(regexp, replacer),
    [](#cb366-5)  'a |2020-04| b');
    ```

    [Named capture groups](#ch044.xhtml_named-capture-groups) (ES2018) are supported, too. If there are any, an argument is added at the end with an object whose properties contain the captures:

    ```
    [](#cb367-1)const regexp = /(?<year>[0-9]{4})-(?<month>[0-9]{2})/;
    [](#cb367-2)const replacer = (...args) => {
    [](#cb367-3)  const groups=args.pop();
    [](#cb367-4)  return '|' + groups.month + '|';
    [](#cb367-5)};
    [](#cb367-6)assert.equal(
    [](#cb367-7)  'a 2020-04 b'.replace(regexp, replacer),
    [](#cb367-8)  'a |04| b');
    ```

*   `.toUpperCase(): string` ^([ES1])

    Returns a copy of the string in which all lowercase alphabetic characters are converted to uppercase. How well that works for various alphabets, depends on the JavaScript engine.

    ```
    > '-a2b-'.toUpperCase()
    '-A2B-'
    > 'αβγ'.toUpperCase()
    'ΑΒΓ'
    ```

*   `.toLowerCase(): string` ^([ES1])

    Returns a copy of the string in which all uppercase alphabetic characters are converted to lowercase. How well that works for various alphabets, depends on the JavaScript engine.

    ```
    > '-A2B-'.toLowerCase()
    '-a2b-'
    > 'ΑΒΓ'.toLowerCase()
    'αβγ'
    ```

*   `.trim(): string` ^([ES5])

    Returns a copy of the string in which all leading and trailing whitespace (spaces, tabs, line terminators, etc.) is gone.

    ```
    > '\r\n#\t  '.trim()
    '#'
    > '  abc  '.trim()
    'abc'
    ```

*   `.trimEnd(): string` ^([ES2019])

    Similar to `.trim()` but only the end of the string is trimmed:

    ```
    > '  abc  '.trimEnd()
    '  abc'
    ```

*   `.trimStart(): string` ^([ES2019])

    Similar to `.trim()` but only the beginning of the string is trimmed:

    ```
    > '  abc  '.trimStart()
    'abc  '
    ```

### 20.7.8 Sources

*   [TypeScript’s built-in typings](https://github.com/Microsoft/TypeScript/blob/master/lib/)
*   [MDN web docs for JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
*   [ECMAScript language specification](https://tc39.github.io/ecma262/)

![](media/file6.svg)  **Exercise: Using string methods**

`exercises/strings/remove_extension_test.mjs`

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 21 Using template literals and tagged templates

* * *

*   21.1 [Disambiguation: “template”](#ch022.xhtml_disambiguation-template)
*   21.2 [Template literals](#ch022.xhtml_template-literals)
*   21.3 [Tagged templates](#ch022.xhtml_tagged-templates)
    *   21.3.1 [Cooked vs. raw template strings (advanced)](#ch022.xhtml_cooked-vs.-raw-template-strings-advanced)
    *   21.3.2 [Tag function library: lit-html](#ch022.xhtml_tag-function-library-lit-html)
    *   21.3.3 [Tag function library: re-template-tag](#ch022.xhtml_tag-function-library-re-template-tag)
    *   21.3.4 [Tag function library: graphql-tag](#ch022.xhtml_tag-function-library-graphql-tag)
*   21.4 [Raw string literals](#ch022.xhtml_raw-string-literals)
*   21.5 [(Advanced)](#ch022.xhtml_advanced-3)
*   21.6 [Multiline template literals and indentation](#ch022.xhtml_multiline-template-literals-and-indentation)
    *   21.6.1 [Fix: template tag for dedenting](#ch022.xhtml_fix-template-tag-for-dedenting)
    *   21.6.2 [Fix: `.trim()`](#ch022.xhtml_fix-.trim)
*   21.7 [Simple templating via template literals](#ch022.xhtml_simple-templating-via-template-literals)
    *   21.7.1 [A more complex example](#ch022.xhtml_a-more-complex-example)
    *   21.7.2 [Simple HTML-escaping](#ch022.xhtml_simple-html-escaping)

* * *

Before we dig into the two features *template literal* and *tagged template*, let’s first examine the multiple meanings of the term *template*.

## 21.1 Disambiguation: “template”

The following three things are significantly different despite all having *template* in their names and despite all of them looking similar:

*   A *text template* is a function from data to text. It is frequently used in web development and often defined via text files. For example, the following text defines a template for the library [Handlebars](https://handlebarsjs.com):

    ```
    [](#cb373-1)<div class="entry">
    [](#cb373-2)  <h1>{{title}}</h1>
    [](#cb373-3)  <div class="body">
    [](#cb373-4)    {{body}}
    [](#cb373-5)  </div>
    [](#cb373-6)</div>
    ```

    This template has two blanks to be filled in: `title` and `body`. It is used like this:

    ```
    [](#cb374-1)// First step: retrieve the template text, e.g. from a text file.
    [](#cb374-2)const tmplFunc = Handlebars.compile(TMPL_TEXT); // compile string
    [](#cb374-3)const data = {title: 'My page', body: 'Welcome to my page!'};
    [](#cb374-4)const html = tmplFunc(data);
    ```

*   A *template literal* is similar to a string literal, but has additional features – for example, interpolation. It is delimited by backticks:

    ```
    [](#cb375-1)const num = 5;
    [](#cb375-2)assert.equal(`Count: ${num}!`, 'Count: 5!');
    ```

*   Syntactically, a *tagged template* is a template literal that follows a function (or rather, an expression that evaluates to a function). That leads to the function being called. Its arguments are derived from the contents of the template literal.

    ```
    [](#cb376-1)const getArgs = (...args) => args;
    [](#cb376-2)assert.deepEqual(
    [](#cb376-3)  getArgs`Count: ${5}!`,
    [](#cb376-4)  [['Count: ', '!'], 5] );
    ```

    Note that `getArgs()` receives both the text of the literal and the data interpolated via `${}`.

## 21.2 Template literals

A template literal has two new features compared to a normal string literal.

First, it supports *string interpolation*: if you put a dynamically computed value inside a `${}`, it is converted to a string and inserted into the string returned by the literal.

```
[](#cb377-1)const MAX = 100;
[](#cb377-2)function doSomeWork(x) {
[](#cb377-3)  if (x > MAX) {
[](#cb377-4)    throw new Error(`At most ${MAX} allowed: ${x}!`);
[](#cb377-5)  }
[](#cb377-6)  // ···
[](#cb377-7)}
[](#cb377-8)assert.throws(
[](#cb377-9)  () => doSomeWork(101),
[](#cb377-10)  {message: 'At most 100 allowed: 101!'});
```

Second, template literals can span multiple lines:

```
[](#cb378-1)const str = `this is
[](#cb378-2)a text with
[](#cb378-3)multiple lines`;
```

Template literals always produce strings.

## 21.3 Tagged templates

The expression in line A is a *tagged template*. It is equivalent to invoking `tagFunc()` with the arguments listed in the Array in line B.

```
[](#cb379-1)function tagFunc(...args) {
[](#cb379-2)  return args;
[](#cb379-3)}
[](#cb379-4)
[](#cb379-5)const setting = 'dark mode';
[](#cb379-6)const value = true;
[](#cb379-7)
[](#cb379-8)assert.deepEqual(
[](#cb379-9)  tagFunc`Setting ${setting} is ${value}!`, // (A)
[](#cb379-10)  [['Setting ', ' is ', '!'], 'dark mode', true] // (B)
[](#cb379-11));
```

The function `tagFunc` before the first backtick is called a *tag function*. Its arguments are:

*   *Template strings* (first argument): an Array with the text fragments surrounding the interpolations `${}`.
    *   In the example: `['Setting ', ' is ', '!']`
*   *Substitutions* (remaining arguments): the interpolated values.
    *   In the example: `'dark mode'` and `true`

The static (fixed) parts of the literal (the template strings) are kept separate from the dynamic parts (the substitutions).

A tag function can return arbitrary values.

### 21.3.1 Cooked vs. raw template strings (advanced)

So far, we have only seen the *cooked interpretation* of template strings. But tag functions actually get two interpretations:

*   A *cooked interpretation* where backslashes have special meaning. For example, `\t` produces a tab character. This interpretation of the template strings is stored as an Array in the first argument.

*   A *raw interpretation* where backslashes do not have special meaning. For example, `\t` produces two characters – a backslash and a `t`. This interpretation of the template strings is stored in property `.raw` of the first argument (an Array).

The following tag function `cookedRaw` uses both interpretations:

```
[](#cb380-1)function cookedRaw(templateStrings, ...substitutions) {
[](#cb380-2)  return {
[](#cb380-3)    cooked: [...templateStrings], // copy just the Array elements
[](#cb380-4)    raw: templateStrings.raw,
[](#cb380-5)    substitutions,
[](#cb380-6)  };
[](#cb380-7)}
[](#cb380-8)assert.deepEqual(
[](#cb380-9)  cookedRaw`\tab${'subst'}\newline\\`,
[](#cb380-10)  {
[](#cb380-11)    cooked: ['\tab', '\newline\\'],
[](#cb380-12)    raw:    ['\\tab', '\\newline\\\\'],
[](#cb380-13)    substitutions: ['subst'],
[](#cb380-14)  });
```

The raw interpretation enables raw string literals via `String.raw` [(described later)](#ch022.xhtml_raw-string-literals) and similar applications.

Tagged templates are great for supporting small embedded languages (so-called *domain-specific languages*). We’ll continue with a few examples.

### 21.3.2 Tag function library: lit-html

[lit-html](https://github.com/Polymer/lit-html) is a templating library that is based on tagged templates and used by [the frontend framework Polymer](https://www.polymer-project.org/):

```
[](#cb381-1)import {html, render} from 'lit-html';
[](#cb381-2)
[](#cb381-3)const template = (items) => html`
[](#cb381-4) <ul>
[](#cb381-5)  ${
[](#cb381-6)      repeat(items,
[](#cb381-7)        (item) => item.id,
[](#cb381-8)        (item, index) => html`<li>${index}. ${item.name}</li>`
[](#cb381-9)      )
[](#cb381-10)    }
[](#cb381-11) </ul>
[](#cb381-12)`;
```

`repeat()` is a custom function for looping. Its 2nd parameter produces unique keys for the values returned by the 3rd parameter. Note the nested tagged template used by that parameter.

### 21.3.3 Tag function library: re-template-tag

[re-template-tag](https://github.com/rauschma/re-template-tag) is a simple library for composing regular expressions. Templates tagged with `re` produce regular expressions. The main benefit is that you can interpolate regular expressions and plain text via `${}` (line A):

```
[](#cb382-1)const RE_YEAR = re`(?<year>[0-9]{4})`;
[](#cb382-2)const RE_MONTH = re`(?<month>[0-9]{2})`;
[](#cb382-3)const RE_DAY = re`(?<day>[0-9]{2})`;
[](#cb382-4)const RE_DATE = re`/${RE_YEAR}-${RE_MONTH}-${RE_DAY}/u`; // (A)
[](#cb382-5)
[](#cb382-6)const match = RE_DATE.exec('2017-01-27');
[](#cb382-7)assert.equal(match.groups.year, '2017');
```

### 21.3.4 Tag function library: graphql-tag

[The library graphql-tag](https://github.com/apollographql/graphql-tag) lets you create GraphQL queries via tagged templates:

```
[](#cb383-1)import gql from 'graphql-tag';
[](#cb383-2)
[](#cb383-3)const query = gql`
[](#cb383-4) {
[](#cb383-5) user(id: 5) {
[](#cb383-6) firstName
[](#cb383-7) lastName
[](#cb383-8) }
[](#cb383-9) }
[](#cb383-10) `;
```

Additionally, there are plugins for pre-compiling such queries in Babel, TypeScript, etc.

## 21.4 Raw string literals

Raw string literals are implemented via the tag function `String.raw`. They are string literals where backslashes don’t do anything special (such as escaping characters, etc.):

```
[](#cb384-1)assert.equal(String.raw`\back`, '\\back');
```

This helps whenever data contains backslashes – for example, strings with regular expressions:

```
[](#cb385-1)const regex1 = /^\./;
[](#cb385-2)const regex2 = new RegExp('^\\.');
[](#cb385-3)const regex3 = new RegExp(String.raw`^\.`);
```

All three regular expressions are equivalent. With a normal string literal, you have to write the backslash twice, to escape it for that literal. With a raw string literal, you don’t have to do that.

Raw string literals are also useful for specifying Windows filename paths:

```
[](#cb386-1)const WIN_PATH = String.raw`C:\foo\bar`;
[](#cb386-2)assert.equal(WIN_PATH, 'C:\\foo\\bar');
```

## 21.5 (Advanced)

All remaining sections are advanced

## 21.6 Multiline template literals and indentation

If you put multiline text in template literals, two goals are in conflict: On one hand, the template literal should be indented to fit inside the source code. On the other hand, the lines of its content should start in the leftmost column.

For example:

```
[](#cb387-1)function div(text) {
[](#cb387-2)  return `
[](#cb387-3) <div>
[](#cb387-4)  ${text}
[](#cb387-5) </div>
[](#cb387-6) `;
[](#cb387-7)}
[](#cb387-8)console.log('Output:');
[](#cb387-9)console.log(
[](#cb387-10)  div('Hello!')
[](#cb387-11)  // Replace spaces with mid-dots:
[](#cb387-12)  .replace(/ /g, '·')
[](#cb387-13)  // Replace \n with #\n:
[](#cb387-14)  .replace(/\n/g, '#\n')
[](#cb387-15));
```

Due to the indentation, the template literal fits well into the source code. Alas, the output is also indented. And we don’t want the return at the beginning and the return plus two spaces at the end.

```
[](#cb388-1)Output:
[](#cb388-2)#
[](#cb388-3)····<div>#
[](#cb388-4)······Hello!#
[](#cb388-5)····</div>#
[](#cb388-6)··
```

There are two ways to fix this: via a tagged template or by trimming the result of the template literal.

### 21.6.1 Fix: template tag for dedenting

The first fix is to use a custom template tag that removes the unwanted whitespace. It uses the first line after the initial line break to determine in which column the text starts and shortens the indentation everywhere. It also removes the line break at the very beginning and the indentation at the very end. One such template tag is [`dedent` by Desmond Brand](https://github.com/dmnd/dedent):

```
[](#cb389-1)import dedent from 'dedent';
[](#cb389-2)function divDedented(text) {
[](#cb389-3)  return dedent`
[](#cb389-4) <div>
[](#cb389-5)  ${text}
[](#cb389-6) </div>
[](#cb389-7) `.replace(/\n/g, '#\n');
[](#cb389-8)}
[](#cb389-9)console.log('Output:');
[](#cb389-10)console.log(divDedented('Hello!'));
```

This time, the output is not indented:

```
[](#cb390-1)Output:
[](#cb390-2)<div>#
[](#cb390-3)  Hello!#
[](#cb390-4)</div>
```

### 21.6.2 Fix: `.trim()`

The second fix is quicker, but also dirtier:

```
[](#cb391-1)function divDedented(text) {
[](#cb391-2)  return `
[](#cb391-3)<div>
[](#cb391-4)  ${text}
[](#cb391-5)</div>
[](#cb391-6) `.trim().replace(/\n/g, '#\n');
[](#cb391-7)}
[](#cb391-8)console.log('Output:');
[](#cb391-9)console.log(divDedented('Hello!'));
```

The string method `.trim()` removes the superfluous whitespace at the beginning and at the end, but the content itself must start in the leftmost column. The advantage of this solution is that you don’t need a custom tag function. The downside is that it looks ugly.

The output is the same as with `dedent`:

```
[](#cb392-1)Output:
[](#cb392-2)<div>#
[](#cb392-3)  Hello!#
[](#cb392-4)</div>
```

## 21.7 Simple templating via template literals

While template literals look like text templates, it is not immediately obvious how to use them for (text) templating: A text template gets its data from an object, while a template literal gets its data from variables. The solution is to use a template literal in the body of a function whose parameter receives the templating data – for example:

```
[](#cb393-1)const tmpl = (data) => `Hello ${data.name}!`;
[](#cb393-2)assert.equal(tmpl({name: 'Jane'}), 'Hello Jane!');
```

### 21.7.1 A more complex example

As a more complex example, we’d like to take an Array of addresses and produce an HTML table. This is the Array:

```
[](#cb394-1)const addresses = [
[](#cb394-2)  { first: '<Jane>', last: 'Bond' },
[](#cb394-3)  { first: 'Lars', last: '<Croft>' },
[](#cb394-4)];
```

The function `tmpl()` that produces the HTML table looks as follows:

```
[](#cb395-1)const tmpl = (addrs) => `
[](#cb395-2)<table>
[](#cb395-3)  ${addrs.map(
[](#cb395-4)    (addr) => `
[](#cb395-5) <tr>
[](#cb395-6) <td>${escapeHtml(addr.first)}</td>
[](#cb395-7) <td>${escapeHtml(addr.last)}</td>
[](#cb395-8) </tr>
[](#cb395-9) `.trim()
[](#cb395-10)  ).join('')}
[](#cb395-11)</table>
[](#cb395-12)`.trim();
```

This code contains two templating functions:

*   The first one (line 1) takes `addrs`, an Array with addresses, and returns a string with a table.
*   The second one (line 4) takes `addr`, an object containing an address, and returns a string with a table row. Note the `.trim()` at the end, which removes unnecessary whitespace.

The first templating function produces its result by wrapping a table element around an Array that it joins into a string (line 10). That Array is produced by mapping the second templating function to each element of `addrs` (line 3). It therefore contains strings with table rows.

The helper function `escapeHtml()` is used to escape special HTML characters (line 6 and line 7). Its implementation is shown in the next subsection.

Let us call `tmpl()` with the addresses and log the result:

```
[](#cb396-1)console.log(tmpl(addresses));
```

The output is:

```
[](#cb397-1)<table>
[](#cb397-2)  <tr>
[](#cb397-3)        <td>&lt;Jane&gt;</td>
[](#cb397-4)        <td>Bond</td>
[](#cb397-5)      </tr><tr>
[](#cb397-6)        <td>Lars</td>
[](#cb397-7)        <td>&lt;Croft&gt;</td>
[](#cb397-8)      </tr>
[](#cb397-9)</table>
```

### 21.7.2 Simple HTML-escaping

The following function escapes plain text so that it is displayed verbatim in HTML:

```
[](#cb398-1)function escapeHtml(str) {
[](#cb398-2)  return str
[](#cb398-3)    .replace(/&/g, '&amp;') // first!
[](#cb398-4)    .replace(/>/g, '&gt;')
[](#cb398-5)    .replace(/</g, '&lt;')
[](#cb398-6)    .replace(/"/g, '&quot;')
[](#cb398-7)    .replace(/'/g, '&#39;')
[](#cb398-8)    .replace(/`/g, '&#96;')
[](#cb398-9)    ;
[](#cb398-10)}
[](#cb398-11)assert.equal(
[](#cb398-12)  escapeHtml('Rock & Roll'), 'Rock &amp; Roll');
[](#cb398-13)assert.equal(
[](#cb398-14)  escapeHtml('<blank>'), '&lt;blank&gt;');
```

![](media/file6.svg)  **Exercise: HTML templating**

Exercise with bonus challenge: `exercises/template-literals/templating_test.mjs`

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 22 Symbols

* * *

*   22.1 [Use cases for symbols](#ch023.xhtml_use-cases-for-symbols)
    *   22.1.1 [Symbols: values for constants](#ch023.xhtml_symbols-values-for-constants)
    *   22.1.2 [Symbols: unique property keys](#ch023.xhtml_symbols-unique-property-keys)
*   22.2 [Publicly known symbols](#ch023.xhtml_publicly-known-symbols)
*   22.3 [Converting symbols](#ch023.xhtml_converting-symbols)

* * *

Symbols are primitive values that are created via the factory function `Symbol()`:

```
[](#cb399-1)const mySymbol = Symbol('mySymbol');
```

The parameter is optional and provides a description, which is mainly useful for debugging.

On one hand, symbols are like objects in that each value created by `Symbol()` is unique and not compared by value:

```
> Symbol() === Symbol()
false
```

On the other hand, they also behave like primitive values. They have to be categorized via `typeof`:

```
[](#cb401-1)const sym = Symbol();
[](#cb401-2)assert.equal(typeof sym, 'symbol');
```

And they can be property keys in objects:

```
[](#cb402-1)const obj = {
[](#cb402-2)  [sym]: 123,
[](#cb402-3)};
```

## 22.1 Use cases for symbols

The main use cases for symbols, are:

*   Values for constants
*   Unique property keys

### 22.1.1 Symbols: values for constants

Let’s assume you want to create constants representing the colors red, orange, yellow, green, blue, and violet. One simple way of doing so would be to use strings:

```
[](#cb403-1)const COLOR_BLUE = 'Blue';
```

On the plus side, logging that constant produces helpful output. On the minus side, there is a risk of mistaking an unrelated value for a color because two strings with the same content are considered equal:

```
[](#cb404-1)const MOOD_BLUE = 'Blue';
[](#cb404-2)assert.equal(COLOR_BLUE, MOOD_BLUE);
```

We can fix that problem via symbols:

```
[](#cb405-1)const COLOR_BLUE = Symbol('Blue');
[](#cb405-2)const MOOD_BLUE = Symbol('Blue');
[](#cb405-3)
[](#cb405-4)assert.notEqual(COLOR_BLUE, MOOD_BLUE);
```

Let’s use symbol-valued constants to implement a function:

```
[](#cb406-1)const COLOR_RED    = Symbol('Red');
[](#cb406-2)const COLOR_ORANGE = Symbol('Orange');
[](#cb406-3)const COLOR_YELLOW = Symbol('Yellow');
[](#cb406-4)const COLOR_GREEN  = Symbol('Green');
[](#cb406-5)const COLOR_BLUE   = Symbol('Blue');
[](#cb406-6)const COLOR_VIOLET = Symbol('Violet');
[](#cb406-7)
[](#cb406-8)function getComplement(color) {
[](#cb406-9)  switch (color) {
[](#cb406-10)    case COLOR_RED:
[](#cb406-11)      return COLOR_GREEN;
[](#cb406-12)    case COLOR_ORANGE:
[](#cb406-13)      return COLOR_BLUE;
[](#cb406-14)    case COLOR_YELLOW:
[](#cb406-15)      return COLOR_VIOLET;
[](#cb406-16)    case COLOR_GREEN:
[](#cb406-17)      return COLOR_RED;
[](#cb406-18)    case COLOR_BLUE:
[](#cb406-19)      return COLOR_ORANGE;
[](#cb406-20)    case COLOR_VIOLET:
[](#cb406-21)      return COLOR_YELLOW;
[](#cb406-22)    default:
[](#cb406-23)      throw new Exception('Unknown color: '+color);
[](#cb406-24)  }
[](#cb406-25)}
[](#cb406-26)assert.equal(getComplement(COLOR_YELLOW), COLOR_VIOLET);
```

### 22.1.2 Symbols: unique property keys

The keys of properties (fields) in objects are used at two levels:

*   The program operates at a *base level*. The keys at that level reflect the problem that the program solves.

*   Libraries and ECMAScript operate at a *meta-level*. The keys at that level are used by services operating on base-level data and code. One such key is `'toString'`.

The following code demonstrates the difference:

```
[](#cb407-1)const pt = {
[](#cb407-2)  x: 7,
[](#cb407-3)  y: 4,
[](#cb407-4)  toString() {
[](#cb407-5)    return `(${this.x}, ${this.y})`;
[](#cb407-6)  },
[](#cb407-7)};
[](#cb407-8)assert.equal(String(pt), '(7, 4)');
```

Properties `.x` and `.y` exist at the base level. They hold the coordinates of the point represented by `pt` and are used to solve a problem – computing with points. Method `.toString()` exists at a meta-level. It is used by JavaScript to convert this object to a string.

Meta-level properties must never interfere with base-level properties. That is, their keys must never overlap. That is difficult when both language and libraries contribute to the meta-level. For example, it is now impossible to give new meta-level methods simple names, such as `toString` because they might clash with existing base-level names. Python’s solution to this problem is to prefix and suffix special names with two underscores: `__init__`, `__iter__`, `__hash__`, etc. However, even with this solution, libraries can’t have their own meta-level properties because those might be in conflict with future language properties.

Symbols, used as property keys, help us here: Each symbol is unique and a symbol key never clashes with any other string or symbol key.

#### 22.1.2.1 Example: a library with a meta-level method

As an example, let’s assume we are writing a library that treats objects differently if they implement a special method. This is what defining a property key for such a method and implementing it for an object would look like:

```
[](#cb408-1)const specialMethod = Symbol('specialMethod');
[](#cb408-2)const obj = {
[](#cb408-3)  _id: 'kf12oi',
[](#cb408-4)  [specialMethod]() { // (A)
[](#cb408-5)    return this._id;
[](#cb408-6)  }
[](#cb408-7)};
[](#cb408-8)assert.equal(obj[specialMethod](), 'kf12oi');
```

The square brackets in line A enable us to specify that the method must have the key `specialMethod`. More details are explained in [§28.5.2 “Computed property keys”](#ch029.xhtml_computed-property-keys).

## 22.2 Publicly known symbols

Symbols that play special roles within ECMAScript are called *publicly known symbols*. Examples include:

*   `Symbol.iterator`: makes an object *iterable*. It’s the key of a method that returns an iterator. For more information on this topic, see [§30 “Synchronous iteration”](#ch031.xhtml_ch_sync-iteration).

*   `Symbol.hasInstance`: customizes how `instanceof` works. If an object implements a method with that key, it can be used at the right-hand side of that operator. For example:

    ```
    [](#cb409-1)const PrimitiveNull = {
    [](#cb409-2)  [Symbol.hasInstance](x) {
    [](#cb409-3)    return x === null;
    [](#cb409-4)  }
    [](#cb409-5)};
    [](#cb409-6)assert.equal(null instanceof PrimitiveNull, true);
    ```

*   `Symbol.toStringTag`: influences the default `.toString()` method.

    ```
    > String({})
    '[object Object]'
    > String({ [Symbol.toStringTag]: 'is no money' })
    '[object is no money]'
    ```

    Note: It’s usually better to override `.toString()`.

![](media/file6.svg)  **Exercises: Publicly known symbols**

*   `Symbol.toStringTag`: `exercises/symbols/to_string_tag_test.mjs`
*   `Symbol.hasInstance`: `exercises/symbols/has_instance_test.mjs`

## 22.3 Converting symbols

What happens if we convert a symbol `sym` to another primitive type? Tbl. [14](#ch023.xhtml_tbl:converting-to-symbol) has the answers.

Table 14: The results of converting symbols to other primitive types.

| Convert to | Explicit conversion | Coercion (implicit conv.) |
| --- | --- | --- |
| boolean | `Boolean(sym)` `→` OK | `!sym` `→` OK |
| number | `Number(sym)` `→` `TypeError` | `sym*2` `→` `TypeError` |
| string | `String(sym)` `→` OK | `''+sym` `→` `TypeError` |
|  | `sym.toString()` `→` OK | `` `${sym}` `` `→` `TypeError` |

One key pitfall with symbols is how often exceptions are thrown when converting them to something else. What is the thinking behind that? First, conversion to number never makes sense and should be warned about. Second, converting a symbol to a string is indeed useful for diagnostic output. But it also makes sense to warn about accidentally turning a symbol into a string (which is a different kind of property key):

```
[](#cb411-1)const obj = {};
[](#cb411-2)const sym = Symbol();
[](#cb411-3)assert.throws(
[](#cb411-4)  () => { obj['__'+sym+'__'] = true },
[](#cb411-5)  { message: 'Cannot convert a Symbol value to a string' });
```

The downside is that the exceptions make working with symbols more complicated. You have to explicitly convert symbols when assembling strings via the plus operator:

```
> const mySymbol = Symbol('mySymbol');
> 'Symbol I used: ' + mySymbol
TypeError: Cannot convert a Symbol value to a string
> 'Symbol I used: ' + String(mySymbol)
'Symbol I used: Symbol(mySymbol)'
```

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 23 Control flow statements

* * *

*   23.1 [Conditions of control flow statements](#ch024.xhtml_conditions-of-control-flow-statements)
*   23.2 [Controlling loops: `break` and `continue`](#ch024.xhtml_controlling-loops-break-and-continue)
    *   23.2.1 [`break`](#ch024.xhtml_break)
    *   23.2.2 [`break` plus label: leaving any labeled statement](#ch024.xhtml_labels)
    *   23.2.3 [`continue`](#ch024.xhtml_continue)
*   23.3 [`if` statements](#ch024.xhtml_if)
    *   23.3.1 [The syntax of `if` statements](#ch024.xhtml_the-syntax-of-if-statements)
*   23.4 [`switch` statements](#ch024.xhtml_switch)
    *   23.4.1 [A first example of a `switch` statement](#ch024.xhtml_a-first-example-of-a-switch-statement)
    *   23.4.2 [Don’t forget to `return` or `break`!](#ch024.xhtml_dont-forget-to-return-or-break)
    *   23.4.3 [Empty case clauses](#ch024.xhtml_empty-case-clauses)
    *   23.4.4 [Checking for illegal values via a `default` clause](#ch024.xhtml_checking-for-illegal-values-via-a-default-clause)
*   23.5 [`while` loops](#ch024.xhtml_while)
    *   23.5.1 [Examples of `while` loops](#ch024.xhtml_examples-of-while-loops)
*   23.6 [`do-while` loops](#ch024.xhtml_do-while)
*   23.7 [`for` loops](#ch024.xhtml_for)
    *   23.7.1 [Examples of `for` loops](#ch024.xhtml_examples-of-for-loops)
*   23.8 [`for-of` loops](#ch024.xhtml_for-of)
    *   23.8.1 [`const`: `for-of` vs. `for`](#ch024.xhtml_const-for-of-vs.-for)
    *   23.8.2 [Iterating over iterables](#ch024.xhtml_iterating-over-iterables)
    *   23.8.3 [Iterating over [index, element] pairs of Arrays](#ch024.xhtml_for-of-iterating-index-element)
*   23.9 [`for-await-of` loops](#ch024.xhtml_for-await-of-loops)
*   23.10 [`for-in` loops (avoid)](#ch024.xhtml_for-in)

* * *

This chapter covers the following control flow statements:

*   `if` statement (ES1)
*   `switch` statement (ES3)
*   `while` loop (ES1)
*   `do-while` loop (ES3)
*   `for` loop (ES1)
*   `for-of` loop (ES6)
*   `for-await-of` loop (ES2018)
*   `for-in` loop (ES1)

Before we get to the actual control flow statements, let’s take a look at two operators for controlling loops.

## 23.1 Conditions of control flow statements

`if`, `while`, and `do-while` have conditions that are, in principle, boolean. However, a condition only has to be *truthy* (`true` if coerced to boolean) in order to be accepted. In other words, the following two control flow statements are equivalent:

```
[](#cb413-1)if (value) {}
[](#cb413-2)if (Boolean(value) === true) {}
```

This is a list of all *falsy* values:

*   `undefined`, `null`
*   `false`
*   `0`, `NaN`
*   `''`

All other values are truthy. For more information, see [§16.2 “Falsy and truthy values”](#ch017.xhtml_falsiness-truthiness).

## 23.2 Controlling loops: `break` and `continue`

The two operators `break` and `continue` can be used to control loops and other statements while you are inside them.

### 23.2.1 `break`

There are two versions of `break`: one with an operand and one without an operand. The latter version works inside the following statements: `while`, `do-while`, `for`, `for-of`, `for-await-of`, `for-in` and `switch`. It immediately leaves the current statement:

```
[](#cb414-1)for (const x of ['a', 'b', 'c']) {
[](#cb414-2)  console.log(x);
[](#cb414-3)  if (x === 'b') break;
[](#cb414-4)  console.log('---')
[](#cb414-5)}
[](#cb414-6)
[](#cb414-7)// Output:
[](#cb414-8)// 'a'
[](#cb414-9)// '---'
[](#cb414-10)// 'b'
```

### 23.2.2 `break` plus label: leaving any labeled statement

`break` with an operand works everywhere. Its operand is a *label*. Labels can be put in front of any statement, including blocks. `break foo` leaves the statement whose label is `foo`:

```
[](#cb415-1)foo: { // label
[](#cb415-2)  if (condition) break foo; // labeled break
[](#cb415-3)  // ···
[](#cb415-4)}
```

In the following example, we use break with a label to leave a loop differently when we succeeded (line A). Then we skip what comes directly after the loop, which is where we end up if we failed.

```
[](#cb416-1)function findSuffix(stringArray, suffix) {
[](#cb416-2)  let result;
[](#cb416-3)  search_block: {
[](#cb416-4)    for (const str of stringArray) {
[](#cb416-5)      if (str.endsWith(suffix)) {
[](#cb416-6)        // Success:
[](#cb416-7)        result = str;
[](#cb416-8)        break search_block; // (A)
[](#cb416-9)      }
[](#cb416-10)    } // for
[](#cb416-11)    // Failure:
[](#cb416-12)    result = '(Untitled)';
[](#cb416-13)  } // search_block
[](#cb416-14)
[](#cb416-15)  return { suffix, result };
[](#cb416-16)    // Same as: {suffix: suffix, result: result}
[](#cb416-17)}
[](#cb416-18)assert.deepEqual(
[](#cb416-19)  findSuffix(['foo.txt', 'bar.html'], '.html'),
[](#cb416-20)  { suffix: '.html', result: 'bar.html' }
[](#cb416-21));
[](#cb416-22)assert.deepEqual(
[](#cb416-23)  findSuffix(['foo.txt', 'bar.html'], '.mjs'),
[](#cb416-24)  { suffix: '.mjs', result: '(Untitled)' }
[](#cb416-25));
```

### 23.2.3 `continue`

`continue` only works inside `while`, `do-while`, `for`, `for-of`, `for-await-of`, and `for-in`. It immediately leaves the current loop iteration and continues with the next one – for example:

```
[](#cb417-1)const lines = [
[](#cb417-2)  'Normal line',
[](#cb417-3)  '# Comment',
[](#cb417-4)  'Another normal line',
[](#cb417-5)];
[](#cb417-6)for (const line of lines) {
[](#cb417-7)  if (line.startsWith('#')) continue;
[](#cb417-8)  console.log(line);
[](#cb417-9)}
[](#cb417-10)// Output:
[](#cb417-11)// 'Normal line'
[](#cb417-12)// 'Another normal line'
```

## 23.3 `if` statements

These are two simple `if` statements: one with just a “then” branch and one with both a “then” branch and an “else” branch:

```
[](#cb418-1)if (cond) {
[](#cb418-2)  // then branch
[](#cb418-3)}
[](#cb418-4)
[](#cb418-5)if (cond) {
[](#cb418-6)  // then branch
[](#cb418-7)} else {
[](#cb418-8)  // else branch
[](#cb418-9)}
```

Instead of the block, `else` can also be followed by another `if` statement:

```
[](#cb419-1)if (cond1) {
[](#cb419-2)  // ···
[](#cb419-3)} else if (cond2) {
[](#cb419-4)  // ···
[](#cb419-5)}
[](#cb419-6)
[](#cb419-7)if (cond1) {
[](#cb419-8)  // ···
[](#cb419-9)} else if (cond2) {
[](#cb419-10)  // ···
[](#cb419-11)} else {
[](#cb419-12)  // ···
[](#cb419-13)}
```

You can continue this chain with more `else if`s.

### 23.3.1 The syntax of `if` statements

The general syntax of `if` statements is:

```
[](#cb420-1)if (cond) «then_statement»
[](#cb420-2)else «else_statement»
```

So far, the `then_statement` has always been a block, but we can use any statement. That statement must be terminated with a semicolon:

```
[](#cb421-1)if (true) console.log('Yes'); else console.log('No');
```

That means that `else if` is not its own construct; it’s simply an `if` statement whose `else_statement` is another `if` statement.

## 23.4 `switch` statements

A `switch` statement looks as follows:

```
switch («switch_expression») {
  «switch_body»
}
```

The body of `switch` consists of zero or more case clauses:

```
case «case_expression»:
  «statements»
```

And, optionally, a default clause:

```
default:
  «statements»
```

A `switch` is executed as follows:

*   It evaluates the switch expression.
*   It jumps to the first case clause whose expression has the same result as the switch expression.
*   Otherwise, if there is no such clause, it jumps to the default clause.
*   Otherwise, if there is no default clause, it does nothing.

### 23.4.1 A first example of a `switch` statement

Let’s look at an example: The following function converts a number from 1–7 to the name of a weekday.

```
[](#cb425-1)function dayOfTheWeek(num) {
[](#cb425-2)  switch (num) {
[](#cb425-3)    case 1:
[](#cb425-4)      return 'Monday';
[](#cb425-5)    case 2:
[](#cb425-6)      return 'Tuesday';
[](#cb425-7)    case 3:
[](#cb425-8)      return 'Wednesday';
[](#cb425-9)    case 4:
[](#cb425-10)      return 'Thursday';
[](#cb425-11)    case 5:
[](#cb425-12)      return 'Friday';
[](#cb425-13)    case 6:
[](#cb425-14)      return 'Saturday';
[](#cb425-15)    case 7:
[](#cb425-16)      return 'Sunday';
[](#cb425-17)  }
[](#cb425-18)}
[](#cb425-19)assert.equal(dayOfTheWeek(5), 'Friday');
```

### 23.4.2 Don’t forget to `return` or `break`!

At the end of a case clause, execution continues with the next case clause, unless you `return` or `break` – for example:

```
[](#cb426-1)function englishToFrench(english) {
[](#cb426-2)  let french;
[](#cb426-3)  switch (english) {
[](#cb426-4)    case 'hello':
[](#cb426-5)      french = 'bonjour';
[](#cb426-6)    case 'goodbye':
[](#cb426-7)      french = 'au revoir';
[](#cb426-8)  }
[](#cb426-9)  return french;
[](#cb426-10)}
[](#cb426-11)// The result should be 'bonjour'!
[](#cb426-12)assert.equal(englishToFrench('hello'), 'au revoir');
```

That is, our implementation of `dayOfTheWeek()` only worked because we used `return`. We can fix `englishToFrench()` by using `break`:

```
[](#cb427-1)function englishToFrench(english) {
[](#cb427-2)  let french;
[](#cb427-3)  switch (english) {
[](#cb427-4)    case 'hello':
[](#cb427-5)      french = 'bonjour';
[](#cb427-6)      break;
[](#cb427-7)    case 'goodbye':
[](#cb427-8)      french = 'au revoir';
[](#cb427-9)      break;
[](#cb427-10)  }
[](#cb427-11)  return french;
[](#cb427-12)}
[](#cb427-13)assert.equal(englishToFrench('hello'), 'bonjour'); // ok
```

### 23.4.3 Empty case clauses

The statements of a case clause can be omitted, which effectively gives us multiple case expressions per case clause:

```
[](#cb428-1)function isWeekDay(name) {
[](#cb428-2)  switch (name) {
[](#cb428-3)    case 'Monday':
[](#cb428-4)    case 'Tuesday':
[](#cb428-5)    case 'Wednesday':
[](#cb428-6)    case 'Thursday':
[](#cb428-7)    case 'Friday':
[](#cb428-8)      return true;
[](#cb428-9)    case 'Saturday':
[](#cb428-10)    case 'Sunday':
[](#cb428-11)      return false;
[](#cb428-12)  }
[](#cb428-13)}
[](#cb428-14)assert.equal(isWeekDay('Wednesday'), true);
[](#cb428-15)assert.equal(isWeekDay('Sunday'), false);
```

### 23.4.4 Checking for illegal values via a `default` clause

A `default` clause is jumped to if the `switch` expression has no other match. That makes it useful for error checking:

```
[](#cb429-1)function isWeekDay(name) {
[](#cb429-2)  switch (name) {
[](#cb429-3)    case 'Monday':
[](#cb429-4)    case 'Tuesday':
[](#cb429-5)    case 'Wednesday':
[](#cb429-6)    case 'Thursday':
[](#cb429-7)    case 'Friday':
[](#cb429-8)      return true;
[](#cb429-9)    case 'Saturday':
[](#cb429-10)    case 'Sunday':
[](#cb429-11)      return false;
[](#cb429-12)    default:
[](#cb429-13)      throw new Error('Illegal value: '+name);
[](#cb429-14)  }
[](#cb429-15)}
[](#cb429-16)assert.throws(
[](#cb429-17)  () => isWeekDay('January'),
[](#cb429-18)  {message: 'Illegal value: January'});
```

![](media/file6.svg)  **Exercises: `switch`**

*   `exercises/control-flow/number_to_month_test.mjs`

*   Bonus: `exercises/control-flow/is_object_via_switch_test.mjs`

## 23.5 `while` loops

A `while` loop has the following syntax:

```
while («condition») {
  «statements»
}
```

Before each loop iteration, `while` evaluates `condition`:

*   If the result is falsy, the loop is finished.
*   If the result is truthy, the `while` body is executed one more time.

### 23.5.1 Examples of `while` loops

The following code uses a `while` loop. In each loop iteration, it removes the first element of `arr` via `.shift()` and logs it.

```
[](#cb431-1)const arr = ['a', 'b', 'c'];
[](#cb431-2)while (arr.length > 0) {
[](#cb431-3)  const elem = arr.shift(); // remove first element
[](#cb431-4)  console.log(elem);
[](#cb431-5)}
[](#cb431-6)// Output:
[](#cb431-7)// 'a'
[](#cb431-8)// 'b'
[](#cb431-9)// 'c'
```

If the condition always evaluates to `true`, then `while` is an infinite loop:

```
[](#cb432-1)while (true) {
[](#cb432-2)  if (Math.random() === 0) break;
[](#cb432-3)}
```

## 23.6 `do-while` loops

The `do-while` loop works much like `while`, but it checks its condition *after* each loop iteration, not before.

```
[](#cb433-1)let input;
[](#cb433-2)do {
[](#cb433-3)  input = prompt('Enter text:');
[](#cb433-4)  console.log(input);
[](#cb433-5)} while (input !== ':q');
```

[`prompt()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt) is a global function that is available in web browsers. It prompts the user to input text and returns it.

## 23.7 `for` loops

A `for` loop has the following syntax:

```
for («initialization»; «condition»; «post_iteration») {
  «statements»
}
```

The first line is the *head* of the loop and controls how often the *body* (the remainder of the loop) is executed. It has three parts and each of them is optional:

*   `initialization`: sets up variables, etc. for the loop. Variables declared here via `let` or `const` only exist inside the loop.
*   `condition`: This condition is checked before each loop iteration. If it is falsy, the loop stops.
*   `post_iteration`: This code is executed after each loop iteration.

A `for` loop is therefore roughly equivalent to the following `while` loop:

```
«initialization»
while («condition») {
  «statements»
  «post_iteration»
}
```

### 23.7.1 Examples of `for` loops

As an example, this is how to count from zero to two via a `for` loop:

```
[](#cb436-1)for (let i=0; i<3; i++) {
[](#cb436-2)  console.log(i);
[](#cb436-3)}
[](#cb436-4)
[](#cb436-5)// Output:
[](#cb436-6)// 0
[](#cb436-7)// 1
[](#cb436-8)// 2
```

This is how to log the contents of an Array via a `for` loop:

```
[](#cb437-1)const arr = ['a', 'b', 'c'];
[](#cb437-2)for (let i=0; i<arr.length; i++) {
[](#cb437-3)  console.log(arr[i]);
[](#cb437-4)}
[](#cb437-5)
[](#cb437-6)// Output:
[](#cb437-7)// 'a'
[](#cb437-8)// 'b'
[](#cb437-9)// 'c'
```

If you omit all three parts of the head, you get an infinite loop:

```
[](#cb438-1)for (;;) {
[](#cb438-2)  if (Math.random() === 0) break;
[](#cb438-3)}
```

## 23.8 `for-of` loops

A `for-of` loop iterates over an *iterable* – a data container that supports [the *iteration protocol*](#ch031.xhtml_ch_sync-iteration). Each iterated value is stored in a variable, as specified in the head:

```
for («iteration_variable» of «iterable») {
  «statements»
}
```

The iteration variable is usually created via a variable declaration:

```
[](#cb440-1)const iterable = ['hello', 'world'];
[](#cb440-2)for (const elem of iterable) {
[](#cb440-3)  console.log(elem);
[](#cb440-4)}
[](#cb440-5)// Output:
[](#cb440-6)// 'hello'
[](#cb440-7)// 'world'
```

But you can also use a (mutable) variable that already exists:

```
[](#cb441-1)const iterable = ['hello', 'world'];
[](#cb441-2)let elem;
[](#cb441-3)for (elem of iterable) {
[](#cb441-4)  console.log(elem);
[](#cb441-5)}
```

### 23.8.1 `const`: `for-of` vs. `for`

Note that in `for-of` loops you can use `const`. The iteration variable can still be different for each iteration (it just can’t change during the iteration). Think of it as a new `const` declaration being executed each time in a fresh scope.

In contrast, in `for` loops you must declare variables via `let` or `var` if their values change.

### 23.8.2 Iterating over iterables

As mentioned before, `for-of` works with any iterable object, not just with Arrays – for example, with Sets:

```
[](#cb442-1)const set = new Set(['hello', 'world']);
[](#cb442-2)for (const elem of set) {
[](#cb442-3)  console.log(elem);
[](#cb442-4)}
```

### 23.8.3 Iterating over [index, element] pairs of Arrays

Lastly, you can also use `for-of` to iterate over the [index, element] entries of Arrays:

```
[](#cb443-1)const arr = ['a', 'b', 'c'];
[](#cb443-2)for (const [index, elem] of arr.entries()) {
[](#cb443-3)  console.log(`${index} -> ${elem}`);
[](#cb443-4)}
[](#cb443-5)// Output:
[](#cb443-6)// '0 -> a'
[](#cb443-7)// '1 -> b'
[](#cb443-8)// '2 -> c'
```

With `[index, element]`, we are using [*destructuring*](#ch038.xhtml_ch_destructuring) to access Array elements.

![](media/file6.svg)  **Exercise: `for-of`**

`exercises/control-flow/array_to_string_test.mjs`

## 23.9 `for-await-of` loops

`for-await-of` is like `for-of`, but it works with asynchronous iterables instead of synchronous ones. And it can only be used inside async functions and async generators.

```
[](#cb444-1)for await (const item of asyncIterable) {
[](#cb444-2)  // ···
[](#cb444-3)}
```

`for-await-of` is described in detail [in the chapter on asynchronous iteration](#ch043.xhtml_for-await-of).

## 23.10 `for-in` loops (avoid)

![](media/file4.svg)  **Recommendation: don’t use `for-in` loops**

`for-in` has several pitfalls. Therefore, it is usually best to avoid it.

This is an example of using `for-in` properly, which involves boilerplate code (line A):

```
[](#cb445-1)function getOwnPropertyNames(obj) {
[](#cb445-2)  const result = [];
[](#cb445-3)  for (const key in obj) {
[](#cb445-4)    if ({}.hasOwnProperty.call(obj, key)) { // (A)
[](#cb445-5)      result.push(key);
[](#cb445-6)    }
[](#cb445-7)  }
[](#cb445-8)  return result;
[](#cb445-9)}
[](#cb445-10)assert.deepEqual(
[](#cb445-11)  getOwnPropertyNames({ a: 1, b:2 }),
[](#cb445-12)  ['a', 'b']);
[](#cb445-13)assert.deepEqual(
[](#cb445-14)  getOwnPropertyNames(['a', 'b']),
[](#cb445-15)  ['0', '1']); // strings!
```

We can implement the same functionality without `for-in`, which is almost always better:

```
[](#cb446-1)function getOwnPropertyNames(obj) {
[](#cb446-2)  const result = [];
[](#cb446-3)  for (const key of Object.keys(obj)) {
[](#cb446-4)    result.push(key);
[](#cb446-5)  }
[](#cb446-6)  return result;
[](#cb446-7)}
```

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 24 Exception handling

* * *

*   24.1 [Motivation: throwing and catching exceptions](#ch025.xhtml_motivation-throwing-and-catching-exceptions)
*   24.2 [`throw`](#ch025.xhtml_throw)
    *   24.2.1 [Options for creating error objects](#ch025.xhtml_options-for-creating-error-objects)
*   24.3 [The `try` statement](#ch025.xhtml_the-try-statement)
    *   24.3.1 [The `try` block](#ch025.xhtml_the-try-block)
    *   24.3.2 [The `catch` clause](#ch025.xhtml_the-catch-clause)
    *   24.3.3 [The `finally` clause](#ch025.xhtml_the-finally-clause)
*   24.4 [Error classes](#ch025.xhtml_error-classes)
    *   24.4.1 [Properties of error objects](#ch025.xhtml_properties-of-error-objects)

* * *

This chapter covers how JavaScript handles exceptions.

![](media/file5.svg)  **Why doesn’t JavaScript throw exceptions more often?**

JavaScript didn’t support exceptions until ES3\. That explains why they are used sparingly by the language and its standard library.

## 24.1 Motivation: throwing and catching exceptions

Consider the following code. It reads profiles stored in files into an Array with instances of class `Profile`:

```
[](#cb447-1)function readProfiles(filePaths) {
[](#cb447-2)  const profiles = [];
[](#cb447-3)  for (const filePath of filePaths) {
[](#cb447-4)    try {
[](#cb447-5)      const profile = readOneProfile(filePath);
[](#cb447-6)      profiles.push(profile);
[](#cb447-7)    } catch (err) { // (A)
[](#cb447-8)      console.log('Error in: '+filePath, err);
[](#cb447-9)    }
[](#cb447-10)  }
[](#cb447-11)}
[](#cb447-12)function readOneProfile(filePath) {
[](#cb447-13)  const profile = new Profile();
[](#cb447-14)  const file = openFile(filePath);
[](#cb447-15)  // ··· (Read the data in `file` into `profile`)
[](#cb447-16)  return profile;
[](#cb447-17)}
[](#cb447-18)function openFile(filePath) {
[](#cb447-19)  if (!fs.existsSync(filePath)) {
[](#cb447-20)    throw new Error('Could not find file '+filePath); // (B)
[](#cb447-21)  }
[](#cb447-22)  // ··· (Open the file whose path is `filePath`)
[](#cb447-23)}
```

Let’s examine what happens in line B: An error occurred, but the best place to handle the problem is not the current location, it’s line A. There, we can skip the current file and move on to the next one.

Therefore:

*   In line B, we use a `throw` statement to indicate that there was a problem.
*   In line A, we use a `try-catch` statement to handle the problem.

When we throw, the following constructs are active:

```
readProfiles(···)
  for (const filePath of filePaths)
    try
      readOneProfile(···)
        openFile(···)
          if (!fs.existsSync(filePath))
            throw
```

One by one, `throw` exits the nested constructs, until it encounters a `try` statement. Execution continues in the `catch` clause of that `try` statement.

## 24.2 `throw`

This is the syntax of the `throw` statement:

```
[](#cb449-1)throw «value»;
```

Any value can be thrown, but it’s best to throw an instance of `Error` or its subclasses.

```
[](#cb450-1)throw new Error('Problem!');
```

### 24.2.1 Options for creating error objects

*   Use class `Error`. That is less limiting in JavaScript than in a more static language because you can add your own properties to instances:

    ```
    [](#cb451-1)const err = new Error('Could not find the file');
    [](#cb451-2)err.filePath = filePath;
    [](#cb451-3)throw err;
    ```

*   Use one of JavaScript’s subclasses of `Error` (which are listed [later](#ch025.xhtml_error-classes)).

*   Subclass `Error` yourself.

    ```
    [](#cb452-1)class MyError extends Error {
    [](#cb452-2)}
    [](#cb452-3)function func() {
    [](#cb452-4)  throw new MyError('Problem!');
    [](#cb452-5)}
    [](#cb452-6)assert.throws(
    [](#cb452-7)  () => func(),
    [](#cb452-8)  MyError);
    ```

## 24.3 The `try` statement

The maximal version of the `try` statement looks as follows:

```
[](#cb453-1)try {
[](#cb453-2)  «try_statements»
[](#cb453-3)} catch (error) {
[](#cb453-4)  «catch_statements»
[](#cb453-5)} finally {
[](#cb453-6)  «finally_statements»
[](#cb453-7)}
```

You can combine these clauses as follows:

*   `try-catch`
*   `try-finally`
*   `try-catch-finally`

Since ECMAScript 2019, you can omit the `catch` parameter `(error)`, if you are not interested in the value that was thrown.

### 24.3.1 The `try` block

The `try` block can be considered the body of the statement. This is where we execute the regular code.

### 24.3.2 The `catch` clause

If an exception reaches the `try` block, then it is assigned to the parameter of the `catch` clause and the code in that clause is executed. Next, execution normally continues after the `try` statement. That may change if:

*   There is a `return`, `break`, or `throw` inside the `catch` block.
*   There is a `finally` clause (which is always executed before the `try` statement ends).

The following code demonstrates that the value that is thrown in line A is indeed caught in line B.

```
[](#cb454-1)const errorObject = new Error();
[](#cb454-2)function func() {
[](#cb454-3)  throw errorObject; // (A)
[](#cb454-4)}
[](#cb454-5)
[](#cb454-6)try {
[](#cb454-7)  func();
[](#cb454-8)} catch (err) { // (B)
[](#cb454-9)  assert.equal(err, errorObject);
[](#cb454-10)}
```

### 24.3.3 The `finally` clause

The code inside the `finally` clause is always executed at the end of a `try` statement – no matter what happens in the `try` block or the `catch` clause.

Let’s look at a common use case for `finally`: You have created a resource and want to always destroy it when you are done with it, no matter what happens while working with it. You’d implement that as follows:

```
[](#cb455-1)const resource = createResource();
[](#cb455-2)try {
[](#cb455-3)  // Work with `resource`. Errors may be thrown.
[](#cb455-4)} finally {
[](#cb455-5)  resource.destroy();
[](#cb455-6)}
```

#### 24.3.3.1 `finally` is always executed

The `finally` clause is always executed, even if an error is thrown (line A):

```
[](#cb456-1)let finallyWasExecuted = false;
[](#cb456-2)assert.throws(
[](#cb456-3)  () => {
[](#cb456-4)    try {
[](#cb456-5)      throw new Error(); // (A)
[](#cb456-6)    } finally {
[](#cb456-7)      finallyWasExecuted = true;
[](#cb456-8)    }
[](#cb456-9)  },
[](#cb456-10)  Error
[](#cb456-11));
[](#cb456-12)assert.equal(finallyWasExecuted, true);
```

And even if there is a `return` statement (line A):

```
[](#cb457-1)let finallyWasExecuted = false;
[](#cb457-2)function func() {
[](#cb457-3)  try {
[](#cb457-4)    return; // (A)
[](#cb457-5)  } finally {
[](#cb457-6)    finallyWasExecuted = true;
[](#cb457-7)  }
[](#cb457-8)}
[](#cb457-9)func();
[](#cb457-10)assert.equal(finallyWasExecuted, true);
```

## 24.4 Error classes

`Error` is the common superclass of all built-in error classes. It has the following subclasses (I’m quoting [the ECMAScript specification](https://tc39.github.io/ecma262/#sec-native-error-types-used-in-this-standard)):

*   `RangeError`: Indicates a value that is not in the set or range of allowable values.
*   `ReferenceError`: Indicate that an invalid reference value has been detected.
*   `SyntaxError`: Indicates that a parsing error has occurred.
*   `TypeError`: is used to indicate an unsuccessful operation when none of the other *NativeError* objects are an appropriate indication of the failure cause.
*   `URIError`: Indicates that one of the global URI handling functions was used in a way that is incompatible with its definition.

### 24.4.1 Properties of error objects

Consider `err`, an instance of `Error`:

```
[](#cb458-1)const err = new Error('Hello!');
[](#cb458-2)assert.equal(String(err), 'Error: Hello!');
```

Two properties of `err` are especially useful:

*   `.message`: contains just the error message.

    ```
    [](#cb459-1)assert.equal(err.message, 'Hello!');
    ```

*   `.stack`: contains a stack trace. It is supported by all mainstream browsers.

    ```
    [](#cb460-1)assert.equal(
    [](#cb460-2)err.stack,
    [](#cb460-3)`
    [](#cb460-4)Error: Hello!
    [](#cb460-5) at ch_exception-handling.mjs:1:13
    [](#cb460-6)`.trim());
    ```

![](media/file6.svg)  **Exercise: Exception handling**

`exercises/exception-handling/call_function_test.mjs`

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 25 Callable values

* * *

*   25.1 [Kinds of functions](#ch026.xhtml_kinds-of-functions)
*   25.2 [Ordinary functions](#ch026.xhtml_ordinary-functions)
    *   25.2.1 [Parts of a function declaration](#ch026.xhtml_parts-of-a-function-declaration)
    *   25.2.2 [Roles played by ordinary functions](#ch026.xhtml_roles-of-ordinary-functions)
    *   25.2.3 [Names of ordinary functions](#ch026.xhtml_names-of-ordinary-functions)
*   25.3 [Specialized functions](#ch026.xhtml_specialized-functions)
    *   25.3.1 [Specialized functions are still functions](#ch026.xhtml_specialized-functions-are-still-functions)
    *   25.3.2 [Recommendation: prefer specialized functions](#ch026.xhtml_recommendation-prefer-specialized-functions)
    *   25.3.3 [Arrow functions](#ch026.xhtml_arrow-functions)
*   25.4 [More kinds of functions and methods](#ch026.xhtml_more-kinds-of-functions-and-methods)
*   25.5 [Returning values from functions and methods](#ch026.xhtml_returning-values-from-functions-and-methods)
*   25.6 [Parameter handling](#ch026.xhtml_parameter-handling)
    *   25.6.1 [Terminology: parameters vs. arguments](#ch026.xhtml_terminology-parameters-vs.-arguments)
    *   25.6.2 [Terminology: callback](#ch026.xhtml_callback-function)
    *   25.6.3 [Too many or not enough arguments](#ch026.xhtml_too-many-or-not-enough-arguments)
    *   25.6.4 [Parameter default values](#ch026.xhtml_parameter-default-values)
    *   25.6.5 [Rest parameters](#ch026.xhtml_rest-parameters)
    *   25.6.6 [Named parameters](#ch026.xhtml_named-parameters)
    *   25.6.7 [Simulating named parameters](#ch026.xhtml_simulating-named-parameters)
    *   25.6.8 [Spreading (`...`) into function calls](#ch026.xhtml_spread-arguments)
*   25.7 [Dynamically evaluating code: `eval()`, `new Function()` (advanced)](#ch026.xhtml_dynamically-evaluating-code-eval-new-function-advanced)
    *   25.7.1 [`eval()`](#ch026.xhtml_eval)
    *   25.7.2 [`new Function()`](#ch026.xhtml_new-function)
    *   25.7.3 [Recommendations](#ch026.xhtml_recommendations)

* * *

## 25.1 Kinds of functions

JavaScript has two categories of functions:

*   An *ordinary function* can play several roles:
    *   Real function
    *   Method
    *   Constructor function
*   A *specialized function* can only play one of those roles – for example:
    *   An *arrow function* can only be a real function.
    *   A *method* can only be a method.
    *   A *class* can only be a constructor function.

The next two sections explain what all of those things mean.

## 25.2 Ordinary functions

The following code shows three ways of doing (roughly) the same thing: creating an ordinary function.

```
[](#cb461-1)// Function declaration (a statement)
[](#cb461-2)function ordinary1(a, b, c) {
[](#cb461-3)  // ···
[](#cb461-4)}
[](#cb461-5)
[](#cb461-6)// const plus anonymous function expression
[](#cb461-7)const ordinary2 = function (a, b, c) {
[](#cb461-8)  // ···
[](#cb461-9)};
[](#cb461-10)
[](#cb461-11)// const plus named function expression
[](#cb461-12)const ordinary3 = function myName(a, b, c) {
[](#cb461-13)  // `myName` is only accessible in here
[](#cb461-14)};
```

As we have seen in [§12.8 “Declarations: scope and activation”](#ch013.xhtml_declarations-scope-activation), function declarations are activated early, while variable declarations (e.g., via `const`) are not.

The syntax of function declarations and function expressions is very similar. The context determines which is which. For more information on this kind of syntactic ambiguity, consult [§8.5 “Ambiguous syntax”](#ch009.xhtml_ambiguous-syntax).

### 25.2.1 Parts of a function declaration

Let’s examine the parts of a function declaration via an example:

```
[](#cb462-1)function add(x, y) {
[](#cb462-2)  return x + y;
[](#cb462-3)}
```

*   `add` is the *name* of the function declaration.
*   `add(x, y)` is the *head* of the function declaration.
*   `x` and `y` are the *parameters*.
*   The curly braces (`{` and `}`) and everything between them are the *body* of the function declaration.
*   The `return` statement explicitly returns a value from the function.

### 25.2.2 Roles played by ordinary functions

Consider the following function declaration from the previous section:

```
[](#cb463-1)function add(x, y) {
[](#cb463-2)  return x + y;
[](#cb463-3)}
```

This function declaration creates an ordinary function whose name is `add`. As an ordinary function, `add()` can play three roles:

*   Real function: invoked via a function call.

    ```
    [](#cb464-1)assert.equal(add(2, 1), 3);
    ```

*   Method: stored in property, invoked via a method call.

    ```
    [](#cb465-1)const obj = { addAsMethod: add };
    [](#cb465-2)assert.equal(obj.addAsMethod(2, 4), 6); // (A)
    ```

    In line A, `obj` is called the *receiver* of the method call. It can be accessed via `this` inside the method.

*   Constructor function/class: invoked via `new`.

    ```
    [](#cb466-1)const inst = new add();
    [](#cb466-2)assert.equal(inst instanceof add, true);
    ```

    (As an aside, the names of classes normally start with capital letters.)

![](media/file5.svg)  **Ordinary function vs. real function**

In JavaScript, we distinguish:

*   The entity *ordinary function*
*   The role *real function*, as played by an ordinary function

In many other programming languages, the entity *function* only plays one role – *function*. Therefore, the same name *function* can be used for both.

### 25.2.3 Names of ordinary functions

The name of a function expression is only accessible inside the function, where the function can use it to refer to itself (e.g., for self-recursion):

```
[](#cb467-1)const func = function funcExpr() { return funcExpr };
[](#cb467-2)assert.equal(func(), func);
[](#cb467-3)
[](#cb467-4)// The name `funcExpr` only exists inside the function:
[](#cb467-5)assert.throws(() => funcExpr(), ReferenceError);
```

In contrast, the name of a function declaration is accessible inside the current scope:

```
[](#cb468-1)function funcDecl() { return funcDecl }
[](#cb468-2)
[](#cb468-3)// The name `funcDecl` exists in the current scope
[](#cb468-4)assert.equal(funcDecl(), funcDecl);
```

## 25.3 Specialized functions

Specialized functions are single-purpose versions of ordinary functions. Each one of them specializes in a single role:

*   The purpose of an *arrow function* is to be a real function:

    ```
    [](#cb469-1)const arrow = () => { return 123 };
    [](#cb469-2)assert.equal(arrow(), 123);
    ```

*   The purpose of a *method* is to be a method:

    ```
    [](#cb470-1)const obj = { method() { return 'abc' } };
    [](#cb470-2)assert.equal(obj.method(), 'abc');
    ```

*   The purpose of a *class* is to be a constructor function:

    ```
    [](#cb471-1)class MyClass { /* ··· */ }
    [](#cb471-2)const inst = new MyClass();
    ```

Apart from nicer syntax, each kind of specialized function also supports new features, making them better at their jobs than ordinary functions.

*   Arrow functions are explained later in this chapter.
*   Methods are explained [in the chapter on single objects](#ch029.xhtml_methods).
*   Classes are explained [in the chapter on classes](#ch030.xhtml_classes).

Tbl. [15](#ch026.xhtml_tbl:capabilities-of-functions) lists the capabilities of ordinary and specialized functions.

Table 15: Capabilities of four kinds of functions. [“Lexical `this`”](#ch026.xhtml_arrow-functins-lexical-this) means that `this` is defined by the surroundings of an arrow function, not by method calls.

|  | Function call | Method call | Constructor call |
| --- | --- | --- | --- |
| Ordinary function | (`this === undefined`) | `✔` | `✔` |
| Arrow function | `✔` | (lexical `this`) | `✘` |
| Method | (`this === undefined`) | `✔` | `✘` |
| Class | `✘` | `✘` | `✔` |

### 25.3.1 Specialized functions are still functions

It’s important to note that arrow functions, methods, and classes are still categorized as functions:

```
> (() => {}) instanceof Function
true
> ({ method() {} }.method) instanceof Function
true
> (class SomeClass {}) instanceof Function
true
```

### 25.3.2 Recommendation: prefer specialized functions

Normally, you should prefer specialized functions over ordinary functions, especially classes and methods. The choice between an arrow function and an ordinary function is less clear-cut, though:

*   On one hand, an ordinary function has `this` as an implicit parameter. That parameter is set to `undefined` during function calls – which is not what you want. An arrow function treats `this` like any other variable. For details, see [§28.4.6 “Avoiding the pitfalls of `this`”](#ch029.xhtml_avoiding-pitfalls-of-this).

*   On the other hand, I like the syntax of a function declaration (which produces an ordinary function). If you don’t use `this` inside it, it is mostly equivalent to `const` plus arrow function:

    ```
    [](#cb473-1)function funcDecl(x, y) {
    [](#cb473-2)  return x * y;
    [](#cb473-3)}
    [](#cb473-4)const arrowFunc = (x, y) => {
    [](#cb473-5)  return x * y;
    [](#cb473-6)};
    ```

### 25.3.3 Arrow functions

Arrow functions were added to JavaScript for two reasons:

1.  To provide a more concise way for creating functions.
2.  To make working with real functions easier: You can’t refer to the `this` of the surrounding scope inside an ordinary function.

Next, we’ll first look at the syntax of arrow functions and then how they help with `this`.

#### 25.3.3.1 The syntax of arrow functions

Let’s review the syntax of an anonymous function expression:

```
[](#cb474-1)const f = function (x, y, z) { return 123 };
```

The (roughly) equivalent arrow function looks as follows. Arrow functions are expressions.

```
[](#cb475-1)const f = (x, y, z) => { return 123 };
```

Here, the body of the arrow function is a block. But it can also be an expression. The following arrow function works exactly like the previous one.

```
[](#cb476-1)const f = (x, y, z) => 123;
```

If an arrow function has only a single parameter and that parameter is an identifier (not [a destructuring pattern](#ch038.xhtml_ch_destructuring)) then you can omit the parentheses around the parameter:

```
[](#cb477-1)const id = x => x;
```

That is convenient when passing arrow functions as parameters to other functions or methods:

```
> [1,2,3].map(x => x+1)
[ 2, 3, 4 ]
```

This previous example demonstrates one benefit of arrow functions – conciseness. If we perform the same task with a function expression, our code is more verbose:

```
[](#cb479-1)[1,2,3].map(function (x) { return x+1 });
```

#### 25.3.3.2 Arrow functions: lexical `this`

Ordinary functions can be both methods and real functions. Alas, the two roles are in conflict:

*   As each ordinary function can be a method, it has its own `this`.
*   The own `this` makes it impossible to access the `this` of the surrounding scope from inside an ordinary function. And that is inconvenient for real functions.

The following code demonstrates the issue:

```
[](#cb480-1)const person = {
[](#cb480-2)  name: 'Jill',
[](#cb480-3)  someMethod() {
[](#cb480-4)    const ordinaryFunc = function () {
[](#cb480-5)      assert.throws(
[](#cb480-6)        () => this.name, // (A)
[](#cb480-7)        /^TypeError: Cannot read property 'name' of undefined$/);
[](#cb480-8)    };
[](#cb480-9)    const arrowFunc = () => {
[](#cb480-10)      assert.equal(this.name, 'Jill'); // (B)
[](#cb480-11)    };
[](#cb480-12) 
[](#cb480-13)    ordinaryFunc();
[](#cb480-14)    arrowFunc();
[](#cb480-15)  },
[](#cb480-16)}
```

In this code, we can observe two ways of handling `this`:

*   Dynamic `this`: In line A, we try to access the `this` of `.someMethod()` from an ordinary function. There, it is *shadowed* by the function’s own `this`, which is `undefined` (as filled in by the function call). Given that ordinary functions receive their `this` via (dynamic) function or method calls, their `this` is called *dynamic*.

*   Lexical `this`: In line B, we again try to access the `this` of `.someMethod()`. This time, we succeed because the arrow function does not have its own `this`. `this` is resolved *lexically*, just like any other variable. That’s why the `this` of arrow functions is called *lexical*.

#### 25.3.3.3 Syntax pitfall: returning an object literal from an arrow function

If you want the expression body of an arrow function to be an object literal, you must put the literal in parentheses:

```
[](#cb481-1)const func1 = () => ({a: 1});
[](#cb481-2)assert.deepEqual(func1(), { a: 1 });
```

If you don’t, JavaScript thinks, the arrow function has a block body (that doesn’t return anything):

```
[](#cb482-1)const func2 = () => {a: 1};
[](#cb482-2)assert.deepEqual(func2(), undefined);
```

`{a: 1}` is interpreted as a block with [the label `a:`](#ch024.xhtml_labels) and the expression statement `1`. Without an explicit `return` statement, the block body returns `undefined`.

This pitfall is caused by [syntactic ambiguity](#ch009.xhtml_ambiguous-syntax): object literals and code blocks have the same syntax. We use the parentheses to tell JavaScript that the body is an expression (an object literal) and not a statement (a block).

For more information on shadowing `this`, consult [§28.4.5 “`this` pitfall: accidentally shadowing `this`”](#ch029.xhtml_shadowing-this).

## 25.4 More kinds of functions and methods

![](media/file0.svg)  **This section is a summary of upcoming content**

This section mainly serves as a reference for the current and upcoming chapters. Don’t worry if you don’t understand everything.

So far, all (real) functions and methods, that we have seen, were:

*   Single-result
*   Synchronous

Later chapters will cover other modes of programming:

*   *Iteration* treats objects as containers of data (so-called *iterables*) and provides a standardized way for retrieving what is inside them. If a function or a method returns an iterable, it returns multiple values.
*   *Asynchronous programming* deals with handling a long-running computation. You are notified when the computation is finished and can do something else in between. The standard pattern for asynchronously delivering single results is called *Promise*.

These modes can be combined – for example, there are synchronous iterables and asynchronous iterables.

Several new kinds of functions and methods help with some of the mode combinations:

*   *Async functions* help implement functions that return Promises. There are also *async methods*.
*   *Synchronous generator functions* help implement functions that return synchronous iterables. There are also *synchronous generator methods*.
*   *Asynchronous generator functions* help implement functions that return asynchronous iterables. There are also *asynchronous generator methods*.

That leaves us with 4 kinds (2 × 2) of functions and methods:

*   Synchronous vs. asynchronous
*   Generator vs. single-result

Tbl. [16](#ch026.xhtml_tbl:syntax-functions-methods) gives an overview of the syntax for creating these 4 kinds of functions and methods.

Table 16: Syntax for creating functions and methods. The last column specifies how many values are produced by an entity.

|  |  | **Result** | **Values** |
| --- | --- | --- | --- |
| **Sync function** | **Sync method** |  |  |
| `function f() {}` | `{ m() {} }` | value | 1 |
| `f = function () {}` |  |  |  |
| `f = () => {}` |  |  |  |
| **Sync generator function** | **Sync gen. method** |  |  |
| `function* f() {}` | `{ * m() {} }` | iterable | 0+ |
| `f = function* () {}` |  |  |  |
| **Async function** | **Async method** |  |  |
| `async function f() {}` | `{ async m() {} }` | Promise | 1 |
| `f = async function () {}` |  |  |  |
| `f = async () => {}` |  |  |  |
| **Async generator function** | **Async gen. method** |  |  |
| `async function* f() {}` | `{ async * m() {} }` | async iterable | 0+ |
| `f = async function* () {}` |  |  |  |

## 25.5 Returning values from functions and methods

(Everything mentioned in this section applies to both functions and methods.)

The `return` statement explicitly returns a value from a function:

```
[](#cb483-1)function func() {
[](#cb483-2)  return 123;
[](#cb483-3)}
[](#cb483-4)assert.equal(func(), 123);
```

Another example:

```
[](#cb484-1)function boolToYesNo(bool) {
[](#cb484-2)  if (bool) {
[](#cb484-3)    return 'Yes';
[](#cb484-4)  } else {
[](#cb484-5)    return 'No';
[](#cb484-6)  }
[](#cb484-7)}
[](#cb484-8)assert.equal(boolToYesNo(true), 'Yes');
[](#cb484-9)assert.equal(boolToYesNo(false), 'No');
```

If, at the end of a function, you haven’t returned anything explicitly, JavaScript returns `undefined` for you:

```
[](#cb485-1)function noReturn() {
[](#cb485-2)  // No explicit return
[](#cb485-3)}
[](#cb485-4)assert.equal(noReturn(), undefined);
```

## 25.6 Parameter handling

Once again, I am only mentioning functions in this section, but everything also applies to methods.

### 25.6.1 Terminology: parameters vs. arguments

The term *parameter* and the term *argument* basically mean the same thing. If you want to, you can make the following distinction:

*   *Parameters* are part of a function definition. They are also called *formal parameters* and *formal arguments*.

*   *Arguments* are part of a function call. They are also called *actual parameters* and *actual arguments*.

### 25.6.2 Terminology: callback

A *callback* or *callback function* is a function that is an argument of a function or method call.

The following is an example of a callback:

```
[](#cb486-1)const myArray = ['a', 'b'];
[](#cb486-2)const callback = (x) => console.log(x);
[](#cb486-3)myArray.forEach(callback);
[](#cb486-4)
[](#cb486-5)// Output:
[](#cb486-6)// 'a'
[](#cb486-7)// 'b'
```

![](media/file5.svg)  **JavaScript uses the term *callback* broadly**

In other programming languages, the term *callback* often has a narrower meaning: it refers to a pattern for delivering results asynchronously, via a function-valued parameter. In this meaning, the *callback* (or *continuation*) is invoked after a function has completely finished its computation.

Callbacks as an asynchronous pattern, are described [in the chapter on asynchronous programming](#ch040.xhtml_callback-pattern).

### 25.6.3 Too many or not enough arguments

JavaScript does not complain if a function call provides a different number of arguments than expected by the function definition:

*   Extra arguments are ignored.
*   Missing parameters are set to `undefined`.

For example:

```
[](#cb487-1)function foo(x, y) {
[](#cb487-2)  return [x, y];
[](#cb487-3)}
[](#cb487-4)
[](#cb487-5)// Too many arguments:
[](#cb487-6)assert.deepEqual(foo('a', 'b', 'c'), ['a', 'b']);
[](#cb487-7)
[](#cb487-8)// The expected number of arguments:
[](#cb487-9)assert.deepEqual(foo('a', 'b'), ['a', 'b']);
[](#cb487-10)
[](#cb487-11)// Not enough arguments:
[](#cb487-12)assert.deepEqual(foo('a'), ['a', undefined]);
```

### 25.6.4 Parameter default values

Parameter default values specify the value to use if a parameter has not been provided – for example:

```
[](#cb488-1)function f(x, y=0) {
[](#cb488-2)  return [x, y];
[](#cb488-3)}
[](#cb488-4)
[](#cb488-5)assert.deepEqual(f(1), [1, 0]);
[](#cb488-6)assert.deepEqual(f(), [undefined, 0]);
```

`undefined` also triggers the default value:

```
[](#cb489-1)assert.deepEqual(
[](#cb489-2)  f(undefined, undefined),
[](#cb489-3)  [undefined, 0]);
```

### 25.6.5 Rest parameters

A rest parameter is declared by prefixing an identifier with three dots (`...`). During a function or method call, it receives an Array with all remaining arguments. If there are no extra arguments at the end, it is an empty Array – for example:

```
[](#cb490-1)function f(x, ...y) {
[](#cb490-2)  return [x, y];
[](#cb490-3)}
[](#cb490-4)assert.deepEqual(
[](#cb490-5)  f('a', 'b', 'c'),
[](#cb490-6)  ['a', ['b', 'c']]);
[](#cb490-7)assert.deepEqual(
[](#cb490-8)  f(),
[](#cb490-9)  [undefined, []]);
```

#### 25.6.5.1 Enforcing a certain number of arguments via a rest parameter

You can use a rest parameter to enforce a certain number of arguments. Take, for example, the following function:

```
[](#cb491-1)function createPoint(x, y) {
[](#cb491-2)  return {x, y};
[](#cb491-3)    // same as {x: x, y: y}
[](#cb491-4)}
```

This is how we force callers to always provide two arguments:

```
[](#cb492-1)function createPoint(...args) {
[](#cb492-2)  if (args.length !== 2) {
[](#cb492-3)    throw new Error('Please provide exactly 2 arguments!');
[](#cb492-4)  }
[](#cb492-5)  const [x, y] = args; // (A)
[](#cb492-6)  return {x, y};
[](#cb492-7)}
```

In line A, we access the elements of `args` via [*destructuring*](#ch038.xhtml_ch_destructuring).

### 25.6.6 Named parameters

When someone calls a function, the arguments provided by the caller are assigned to the parameters received by the callee. Two common ways of performing the mapping are:

1.  Positional parameters: An argument is assigned to a parameter if they have the same position. A function call with only positional arguments looks as follows.

    ```
    [](#cb493-1)selectEntries(3, 20, 2)
    ```

2.  Named parameters: An argument is assigned to a parameter if they have the same name. JavaScript doesn’t have named parameters, but you can simulate them. For example, this is a function call with only (simulated) named arguments:

    ```
    [](#cb494-1)selectEntries({start: 3, end: 20, step: 2})
    ```

Named parameters have several benefits:

*   They lead to more self-explanatory code because each argument has a descriptive label. Just compare the two versions of `selectEntries()`: with the second one, it is much easier to see what happens.

*   The order of the arguments doesn’t matter (as long as the names are correct).

*   Handling more than one optional parameter is more convenient: callers can easily provide any subset of all optional parameters and don’t have to be aware of the ones they omit (with positional parameters, you have to fill in preceding optional parameters, with `undefined`).

### 25.6.7 Simulating named parameters

JavaScript doesn’t have real named parameters. The official way of simulating them is via object literals:

```
[](#cb495-1)function selectEntries({start=0, end=-1, step=1}) {
[](#cb495-2)  return {start, end, step};
[](#cb495-3)}
```

This function uses [*destructuring*](#ch038.xhtml_ch_destructuring) to access the properties of its single parameter. The pattern it uses is an abbreviation for the following pattern:

```
[](#cb496-1){start: start=0, end: end=-1, step: step=1}
```

This destructuring pattern works for empty object literals:

```
> selectEntries({})
{ start: 0, end: -1, step: 1 }
```

But it does not work if you call the function without any parameters:

```
> selectEntries()
TypeError: Cannot destructure property `start` of 'undefined' or 'null'.
```

You can fix this by providing a default value for the whole pattern. This default value works the same as default values for simpler parameter definitions: if the parameter is missing, the default is used.

```
[](#cb499-1)function selectEntries({start=0, end=-1, step=1} = {}) {
[](#cb499-2)  return {start, end, step};
[](#cb499-3)}
[](#cb499-4)assert.deepEqual(
[](#cb499-5)  selectEntries(),
[](#cb499-6)  { start: 0, end: -1, step: 1 });
```

### 25.6.8 Spreading (`...`) into function calls

If you put three dots (`...`) in front of the argument of a function call, then you *spread* it. That means that the argument must be [an *iterable* object](#ch031.xhtml_ch_sync-iteration) and the iterated values all become arguments. In other words, a single argument is expanded into multiple arguments – for example:

```
[](#cb500-1)function func(x, y) {
[](#cb500-2)  console.log(x);
[](#cb500-3)  console.log(y);
[](#cb500-4)}
[](#cb500-5)const someIterable = ['a', 'b'];
[](#cb500-6)func(...someIterable);
[](#cb500-7)  // same as func('a', 'b')
[](#cb500-8)
[](#cb500-9)// Output:
[](#cb500-10)// 'a'
[](#cb500-11)// 'b'
```

Spreading and rest parameters use the same syntax (`...`), but they serve opposite purposes:

*   Rest parameters are used when defining functions or methods. They collect arguments into Arrays.
*   Spread arguments are used when calling functions or methods. They turn iterable objects into arguments.

#### 25.6.8.1 Example: spreading into `Math.max()`

`Math.max()` returns the largest one of its zero or more arguments. Alas, it can’t be used for Arrays, but spreading gives us a way out:

```
> Math.max(-1, 5, 11, 3)
11
> Math.max(...[-1, 5, 11, 3])
11
> Math.max(-1, ...[-5, 11], 3)
11
```

#### 25.6.8.2 Example: spreading into `Array.prototype.push()`

Similarly, the Array method `.push()` destructively adds its zero or more parameters to the end of its Array. JavaScript has no method for destructively appending an Array to another one. Once again, we are saved by spreading:

```
[](#cb502-1)const arr1 = ['a', 'b'];
[](#cb502-2)const arr2 = ['c', 'd'];
[](#cb502-3)
[](#cb502-4)arr1.push(...arr2);
[](#cb502-5)assert.deepEqual(arr1, ['a', 'b', 'c', 'd']);
```

![](media/file6.svg)  **Exercises: Parameter handling**

*   Positional parameters: `exercises/callables/positional_parameters_test.mjs`
*   Named parameters: `exercises/callables/named_parameters_test.mjs`

## 25.7 Dynamically evaluating code: `eval()`, `new Function()` (advanced)

Next, we’ll look at two ways of evaluating code dynamically: `eval()` and `new Function()`.

### 25.7.1 `eval()`

Given a string `str` with JavaScript code, `eval(str)` evaluates that code and returns the result:

```
> eval('2 ** 4')
16
```

There are two ways of invoking `eval()`:

*   *Directly*, via a function call. Then the code in its argument is evaluated inside the current scope.
*   *Indirectly*, not via a function call. Then it evaluates its code in global scope.

“Not via a function call” means “anything that looks different than `eval(···)`”:

*   `eval.call(undefined, '···')`
*   `(0, eval)('···')` (uses the comma operator)
*   `globalThis.eval('···')`
*   `const e = eval; e('···')`
*   Etc.

The following code illustrates the difference:

```
[](#cb504-1)globalThis.myVariable = 'global';
[](#cb504-2)function func() {
[](#cb504-3)  const myVariable = 'local';
[](#cb504-4) 
[](#cb504-5)  // Direct eval
[](#cb504-6)  assert.equal(eval('myVariable'), 'local');
[](#cb504-7) 
[](#cb504-8)  // Indirect eval
[](#cb504-9)  assert.equal(eval.call(undefined, 'myVariable'), 'global');
[](#cb504-10)}
```

Evaluating code in global context is safer because the code has access to fewer internals.

### 25.7.2 `new Function()`

`new Function()` creates a function object and is invoked as follows:

```
[](#cb505-1)const func = new Function('«param_1»', ···, '«param_n»', '«func_body»');
```

The previous statement is equivalent to the next statement. Note that `«param_1»`, etc., are not inside string literals, anymore.

```
[](#cb506-1)const func = function («param_1», ···, «param_n») {
[](#cb506-2)  «func_body»
[](#cb506-3)};
```

In the next example, we create the same function twice, first via `new Function()`, then via a function expression:

```
[](#cb507-1)const times1 = new Function('a', 'b', 'return a * b');
[](#cb507-2)const times2 = function (a, b) { return a * b };
```

![](media/file4.svg)  **`new Function()` creates non-strict mode functions**

Functions created via `new Function()` are [sloppy](#ch009.xhtml_strict-mode).

### 25.7.3 Recommendations

Avoid dynamic evaluation of code as much as you can:

*   It’s a security risk because it may enable an attacker to execute arbitrary code with the privileges of your code.
*   It may be switched off – for example, in browsers, via [a Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP).

Very often, JavaScript is dynamic enough so that you don’t need `eval()` or similar. In the following example, what we are doing with `eval()` (line A) can be achieved just as well without it (line B).

```
[](#cb508-1)const obj = {a: 1, b: 2};
[](#cb508-2)const propKey = 'b';
[](#cb508-3)
[](#cb508-4)assert.equal(eval('obj.' + propKey), 2); // (A)
[](#cb508-5)assert.equal(obj[propKey], 2); // (B)
```

If you have to dynamically evaluate code:

*   Prefer `new Function()` over `eval()`: it always executes its code in global context and a function provides a clean interface to the evaluated code.
*   Prefer indirect `eval` over direct `eval`: evaluating code in global context is safer.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 26 Environments: under the hood of variables (bonus)

* * *

*   26.1 [Environment: data structure for managing variables](#ch027.xhtml_environment-data-structure-for-managing-variables)
*   26.2 [Recursion via environments](#ch027.xhtml_recursion-via-environments)
    *   26.2.1 [Executing the code](#ch027.xhtml_executing-the-code)
*   26.3 [Nested scopes via environments](#ch027.xhtml_nested-scopes-via-environments)
    *   26.3.1 [Executing the code](#ch027.xhtml_executing-the-code-1)
*   26.4 [Closures and environments](#ch027.xhtml_closures-environments)

* * *

In this chapter, we take a closer look at how the ECMAScript language specification handles variables.

## 26.1 Environment: data structure for managing variables

An environment is the data structure that the ECMAScript specification uses to manage variables. It is a dictionary whose keys are variable names and whose values are the values of those variables. Each scope has its associated environment. Environments must be able to support the following phenomena related to variables:

*   Recursion
*   Nested scopes
*   Closures

We’ll use examples to illustrate how that is done for each phenomenon.

## 26.2 Recursion via environments

We’ll tackle recursion first. Consider the following code:

```
[](#cb509-1)function f(x) {
[](#cb509-2)  return x * 2;
[](#cb509-3)}
[](#cb509-4)function g(y) {
[](#cb509-5)  const tmp = y + 1;
[](#cb509-6)  return f(tmp);
[](#cb509-7)}
[](#cb509-8)assert.equal(g(3), 8);
```

For each function call, you need fresh storage space for the variables (parameters and local variables) of the called function. This is managed via a stack of so-called *execution contexts*, which are references to environments (for the purpose of this chapter). Environments themselves are stored on the heap. That is necessary because they occasionally live on after execution has left their scopes (we’ll see that when exploring *closures*). Therefore, they themselves can’t be managed via a stack.

### 26.2.1 Executing the code

While executing the code, we make the following pauses:

```
[](#cb510-1)function f(x) {
[](#cb510-2)  // Pause 3
[](#cb510-3)  return x * 2;
[](#cb510-4)}
[](#cb510-5)function g(y) {
[](#cb510-6)  const tmp = y + 1;
[](#cb510-7)  // Pause 2
[](#cb510-8)  return f(tmp);
[](#cb510-9)}
[](#cb510-10)// Pause 1
[](#cb510-11)assert.equal(g(3), 8);
```

This is what happens:

*   Pause 1 – before calling `g()` (fig. [7](#ch027.xhtml_fig:env_recursion_1)).

*   Pause 2 – while executing `g()` (fig. [8](#ch027.xhtml_fig:env_recursion_2)).

*   Pause 3 – while executing `f()` (fig. [9](#ch027.xhtml_fig:env_recursion_3)).

*   Remaining steps: Every time there is a `return`, one execution context is removed from the stack.

![](media/file16.svg)

Figure 7: Recursion, pause 1 – before calling `g()`: The execution context stack has one entry, which points to the top-level environment. In that environment, there are two entries; one for `f()` and one for `g()`.

![](media/file17.svg)

Figure 8: Recursion, pause 2 – while executing `g()`: The top of the execution context stack points to the environment that was created for `g()`. That environment contains entries for the argument `y` and for the local variable `tmp`.

![](media/file18.svg)

Figure 9: Recursion, pause 3 – while executing `f()`: The top execution context now points to the environment for `f()`.

## 26.3 Nested scopes via environments

We use the following code to explore how nested scopes are implemented via environments.

```
[](#cb511-1)function f(x) {
[](#cb511-2)  function square() {
[](#cb511-3)    const result = x * x;
[](#cb511-4)    return result;
[](#cb511-5)  }
[](#cb511-6)  return square();
[](#cb511-7)}
[](#cb511-8)assert.equal(f(6), 36);
```

Here, we have three nested scopes: The top-level scope, the scope of `f()`, and the scope of `square()`. Observations:

*   The scopes are connected. An inner scope “inherits” all the variables of an outer scope (minus the ones it shadows).
*   Nesting scopes as a mechanism is independent of recursion. The latter is best managed by a stack of independent environments. The former is a relationship that each environment has with the environment “in which” it is created.

Therefore, the environment of each scope points to the environment of the surrounding scope via a field called `outer`. When we are looking up the value of a variable, we first search for its name in the current environment, then in the outer environment, then in the outer environment’s outer environment, etc. The whole chain of outer environments contains all variables that can currently be accessed (minus shadowed variables).

When you make a function call, you create a new environment. The outer environment of that environment is the environment in which the function was created. To help set up the field `outer` of environments created via function calls, each function has an internal property named `[[Scope]]` that points to its “birth environment”.

### 26.3.1 Executing the code

These are the pauses we are making while executing the code:

```
[](#cb512-1)function f(x) {
[](#cb512-2)  function square() {
[](#cb512-3)    const result = x * x;
[](#cb512-4)    // Pause 3
[](#cb512-5)    return result;
[](#cb512-6)  }
[](#cb512-7)  // Pause 2
[](#cb512-8)  return square();
[](#cb512-9)}
[](#cb512-10)// Pause 1
[](#cb512-11)assert.equal(f(6), 36);
```

This is what happens:

*   Pause 1 – before calling `f()` (fig. [10](#ch027.xhtml_fig:env_nested_1)).
*   Pause 2 – while executing `f()` (fig. [11](#ch027.xhtml_fig:env_nested_2)).
*   Pause 3 – while executing `square()` (fig. [12](#ch027.xhtml_fig:env_nested_3)).
*   After that, `return` statements pop execution entries off the stack.

![](media/file19.svg)

Figure 10: Nested scopes, pause 1 – before calling `f()`: The top-level environment has a single entry, for `f()`. The birth environment of `f()` is the top-level environment. Therefore, `f`’s `[[Scope]]` points to it.

![](media/file20.svg)

Figure 11: Nested scopes, pause 2 – while executing `f()`: There is now an environment for the function call `f(6)`. The outer environment of that environment is the birth environment of `f()` (the top-level environment at index 0). We can see that the field `outer` was set to the value of `f`’s `[[Scope]]`. Furthermore, the `[[Scope]]` of the new function `square()` is the environment that was just created.

![](media/file21.svg)

Figure 12: Nested scopes, pause 3 – while executing `square()`: The previous pattern was repeated: the `outer` of the most recent environment was set up via the `[[Scope]]` of the function that we just called. The chain of scopes created via `outer`, contains all variables that are active right now. For example, we can access `result`, `square`, and `f` if we want to. Environments reflect two aspects of variables. First, the chain of outer environments reflects the nested static scopes. Second, the stack of execution contexts reflects what function calls were made, dynamically.

## 26.4 Closures and environments

To see how environments are used to implement [closures](#ch013.xhtml_closures), we are using the following example:

```
[](#cb513-1)function add(x) {
[](#cb513-2)  return (y) => { // (A)
[](#cb513-3)    return x + y;
[](#cb513-4)  };
[](#cb513-5)}
[](#cb513-6)assert.equal(add(3)(1), 4); // (B)
```

What is going on here? `add()` is a function that returns a function. When we make the nested function call `add(3)(1)` in line B, the first parameter is for `add()`, the second parameter is for the function it returns. This works because the function created in line A does not lose the connection to its birth scope when it leaves that scope. The associated environment is kept alive by that connection and the function still has access to variable `x` in that environment (`x` is free inside the function).

This nested way of calling `add()` has an advantage: if you only make the first function call, you get a version of `add()` whose parameter `x` is already filled in:

```
[](#cb514-1)const plus2 = add(2);
[](#cb514-2)assert.equal(plus2(5), 7);
```

Converting a function with two parameters into two nested functions with one parameter each, is called *currying*. `add()` is a curried function.

Only filling in some of the parameters of a function is called *partial application* (the function has not been fully applied yet). [Method `.bind()` of functions](#ch029.xhtml_function-prototype-bind) performs partial application. In the previous example, we can see that partial application is simple if a function is curried.

#### 26.4.0.1 Executing the code

As we are executing the following code, we are making three pauses:

```
[](#cb515-1)function add(x) {
[](#cb515-2)  return (y) => {
[](#cb515-3)    // Pause 3: plus2(5)
[](#cb515-4)    return x + y;
[](#cb515-5)  }; // Pause 1: add(2)
[](#cb515-6)}
[](#cb515-7)const plus2 = add(2);
[](#cb515-8)// Pause 2
[](#cb515-9)assert.equal(plus2(5), 7);
```

This is what happens:

*   Pause 1 – during the execution of `add(2)` (fig. [13](#ch027.xhtml_fig:env_closure_2)).
*   Pause 2 – after the execution of `add(2)` (fig. [14](#ch027.xhtml_fig:env_closure_3)).
*   Pause 3 – while executing `plus2(5)` (fig. [15](#ch027.xhtml_fig:env_closure_4)).

![](media/file22.svg)

Figure 13: Closures, pause 1 – during the execution of `add(2)`: We can see that the function returned by `add()` already exists (see bottom right corner) and that it points to its birth environment via its internal property `[[Scope]]`. Note that `plus2` is still in its temporal dead zone and uninitialized.

![](media/file23.svg)

Figure 14: Closures, pause 2 – after the execution of `add(2)`: `plus2` now points to the function returned by `add(2)`. That function keeps its birth environment (the environment of `add(2)`) alive via its `[[Scope]]`.

![](media/file24.svg)

Figure 15: Closures, pause 3 – while executing `plus2(5)`: The `[[Scope]]` of `plus2` is used to set up the `outer` of the new environment. That’s how the current function gets access to `x`.

# 27 Modules

* * *

*   27.1 [Overview: syntax of ECMAScript modules](#ch028.xhtml_overview-syntax-of-ecmascript-modules)
    *   27.1.1 [Exporting](#ch028.xhtml_exporting)
    *   27.1.2 [Importing](#ch028.xhtml_importing)
*   27.2 [JavaScript source code formats](#ch028.xhtml_javascript-source-code-formats)
    *   27.2.1 [Code before built-in modules was written in ECMAScript 5](#ch028.xhtml_code-before-built-in-modules-was-written-in-ecmascript-5)
*   27.3 [Before we had modules, we had scripts](#ch028.xhtml_scripts)
*   27.4 [Module systems created prior to ES6](#ch028.xhtml_module-systems-created-prior-to-es6)
    *   27.4.1 [Server side: CommonJS modules](#ch028.xhtml_server-side-commonjs-modules)
    *   27.4.2 [Client side: AMD (Asynchronous Module Definition) modules](#ch028.xhtml_client-side-amd-asynchronous-module-definition-modules)
    *   27.4.3 [Characteristics of JavaScript modules](#ch028.xhtml_characteristics-of-javascript-modules)
*   27.5 [ECMAScript modules](#ch028.xhtml_ecmascript-modules)
    *   27.5.1 [ES modules: syntax, semantics, loader API](#ch028.xhtml_es-modules-syntax-semantics-loader-api)
*   27.6 [Named exports and imports](#ch028.xhtml_named-exports-and-imports)
    *   27.6.1 [Named exports](#ch028.xhtml_named-exports)
    *   27.6.2 [Named imports](#ch028.xhtml_named-imports)
    *   27.6.3 [Namespace imports](#ch028.xhtml_namespace-imports)
    *   27.6.4 [Named exporting styles: inline versus clause (advanced)](#ch028.xhtml_named-exporting-styles-inline-versus-clause-advanced)
*   27.7 [Default exports and imports](#ch028.xhtml_default-exports-and-imports)
    *   27.7.1 [The two styles of default-exporting](#ch028.xhtml_the-two-styles-of-default-exporting)
    *   27.7.2 [The default export as a named export (advanced)](#ch028.xhtml_the-default-export-as-a-named-export-advanced)
*   27.8 [More details on exporting and importing](#ch028.xhtml_more-details-on-exporting-and-importing)
    *   27.8.1 [Imports are read-only views on exports](#ch028.xhtml_imports-are-read-only-views-on-exports)
    *   27.8.2 [ESM’s transparent support for cyclic imports (advanced)](#ch028.xhtml_esms-transparent-support-for-cyclic-imports-advanced)
*   27.9 [npm packages](#ch028.xhtml_npm-packages)
    *   27.9.1 [Packages are installed inside a directory `node_modules/`](#ch028.xhtml_packages-are-installed-inside-a-directory-node_modules)
    *   27.9.2 [Why can npm be used to install frontend libraries?](#ch028.xhtml_why-can-npm-be-used-to-install-frontend-libraries)
*   27.10 [Naming modules](#ch028.xhtml_naming-modules)
*   27.11 [Module specifiers](#ch028.xhtml_module-specifiers)
    *   27.11.1 [Categories of module specifiers](#ch028.xhtml_categories-of-module-specifiers)
    *   27.11.2 [ES module specifiers in browsers](#ch028.xhtml_es-module-specifiers-in-browsers)
    *   27.11.3 [ES module specifiers on Node.js](#ch028.xhtml_es-module-specifiers-on-node.js)
*   27.12 [Loading modules dynamically via `import()`](#ch028.xhtml_loading-modules-dynamically-via-import)
    *   27.12.1 [Example: loading a module dynamically](#ch028.xhtml_example-loading-a-module-dynamically)
    *   27.12.2 [Use cases for `import()`](#ch028.xhtml_use-cases-for-import)
*   27.13 [Preview: `import.meta.url`](#ch028.xhtml_preview-import.meta.url)
    *   27.13.1 [`import.meta.url` and class `URL`](#ch028.xhtml_import.meta.url-and-class-url)
    *   27.13.2 [`import.meta.url` on Node.js](#ch028.xhtml_import.meta.url-on-node.js)
*   27.14 [Polyfills: emulating native web platform features (advanced)](#ch028.xhtml_polyfills)
    *   27.14.1 [Sources of this section](#ch028.xhtml_sources-of-this-section)

* * *

## 27.1 Overview: syntax of ECMAScript modules

### 27.1.1 Exporting

```
[](#cb516-1)// Named exports
[](#cb516-2)export function f() {}
[](#cb516-3)export const one = 1;
[](#cb516-4)export {foo, b as bar};
[](#cb516-5)
[](#cb516-6)// Default exports
[](#cb516-7)export default function f() {} // declaration with optional name
[](#cb516-8)// Replacement for `const` (there must be exactly one value)
[](#cb516-9)export default 123;
[](#cb516-10)
[](#cb516-11)// Re-exporting from another module
[](#cb516-12)export * from './some-module.mjs';
[](#cb516-13)export {foo, b as bar} from './some-module.mjs';
```

### 27.1.2 Importing

```
[](#cb517-1)// Named imports
[](#cb517-2)import {foo, bar as b} from './some-module.mjs';
[](#cb517-3)// Namespace import
[](#cb517-4)import * as someModule from './some-module.mjs';
[](#cb517-5)// Default import
[](#cb517-6)import someModule from './some-module.mjs';
[](#cb517-7)
[](#cb517-8)// Combinations:
[](#cb517-9)import someModule, * as someModule from './some-module.mjs';
[](#cb517-10)import someModule, {foo, bar as b} from './some-module.mjs';
[](#cb517-11)
[](#cb517-12)// Empty import (for modules with side effects)
[](#cb517-13)import './some-module.mjs';
```

## 27.2 JavaScript source code formats

The current landscape of JavaScript modules is quite diverse: ES6 brought built-in modules, but the source code formats that came before them, are still around, too. Understanding the latter helps understand the former, so let’s investigate. The next sections describe the following ways of delivering JavaScript source code:

*   *Scripts* are code fragments that browsers run in global scope. They are precursors of modules.
*   *CommonJS modules* are a module format that is mainly used on servers (e.g., via Node.js).
*   *AMD modules* are a module format that is mainly used in browsers.
*   *ECMAScript modules* are JavaScript’s built-in module format. It supersedes all previous formats.

Tbl. [17](#ch028.xhtml_tbl:source-code-formats) gives an overview of these code formats. Note that for CommonJS modules and ECMAScript modules, two filename extensions are commonly used. Which one is appropriate depends on how you want to use a file. Details are given later in this chapter.

Table 17: Ways of delivering JavaScript source code.

|  | Runs on | Loaded | Filename ext. |
| --- | --- | --- | --- |
| Script | browsers | async | `.js` |
| CommonJS module | servers | sync | `.js .cjs` |
| AMD module | browsers | async | `.js` |
| ECMAScript module | browsers and servers | async | `.js .mjs` |

### 27.2.1 Code before built-in modules was written in ECMAScript 5

Before we get to built-in modules (which were introduced with ES6), all code that you’ll see, will be written in ES5\. Among other things:

*   ES5 did not have `const` and `let`, only `var`.
*   ES5 did not have arrow functions, only function expressions.

## 27.3 Before we had modules, we had scripts

Initially, browsers only had *scripts* – pieces of code that were executed in global scope. As an example, consider an HTML file that loads script files via the following HTML:

```
[](#cb518-1)<script src="other-module1.js"></script>
[](#cb518-2)<script src="other-module2.js"></script>
[](#cb518-3)<script src="my-module.js"></script>
```

The main file is `my-module.js`, where we simulate a module:

```
[](#cb519-1)var myModule = (function () { // Open IIFE
[](#cb519-2)  // Imports (via global variables)
[](#cb519-3)  var importedFunc1 = otherModule1.importedFunc1;
[](#cb519-4)  var importedFunc2 = otherModule2.importedFunc2;
[](#cb519-5)
[](#cb519-6)  // Body
[](#cb519-7)  function internalFunc() {
[](#cb519-8)    // ···
[](#cb519-9)  }
[](#cb519-10)  function exportedFunc() {
[](#cb519-11)    importedFunc1();
[](#cb519-12)    importedFunc2();
[](#cb519-13)    internalFunc();
[](#cb519-14)  }
[](#cb519-15)
[](#cb519-16)  // Exports (assigned to global variable `myModule`)
[](#cb519-17)  return {
[](#cb519-18)    exportedFunc: exportedFunc,
[](#cb519-19)  };
[](#cb519-20)})(); // Close IIFE
```

`myModule` is a global variable that is assigned the result of immediately invoking a function expression. The function expression starts in the first line. It is invoked in the last line.

This way of wrapping a code fragment is called *immediately invoked function expression* (IIFE, coined by Ben Alman). What do we gain from an IIFE? `var` is not block-scoped (like `const` and `let`), it is function-scoped: the only way to create new scopes for `var`-declared variables is via functions or methods (with `const` and `let`, you can use either functions, methods, or blocks `{}`). Therefore, the IIFE in the example hides all of the following variables from global scope and minimizes name clashes: `importedFunc1`, `importedFunc2`, `internalFunc`, `exportedFunc`.

Note that we are using an IIFE in a particular manner: at the end, we pick what we want to export and return it via an object literal. That is called the *revealing module pattern* (coined by Christian Heilmann).

This way of simulating modules, has several issues:

*   Libraries in script files export and import functionality via global variables, which risks name clashes.
*   Dependencies are not stated explicitly, and there is no built-in way for a script to load the scripts it depends on. Therefore, the web page has to load not just the scripts that are needed by the page but also the dependencies of those scripts, the dependencies’ dependencies, etc. And it has to do so in the right order!

## 27.4 Module systems created prior to ES6

Prior to ECMAScript 6, JavaScript did not have built-in modules. Therefore, the flexible syntax of the language was used to implement custom module systems *within* the language. Two popular ones are:

*   CommonJS (targeting the server side)
*   AMD (Asynchronous Module Definition, targeting the client side)

### 27.4.1 Server side: CommonJS modules

The original CommonJS standard for modules was created for server and desktop platforms. It was the foundation of the original Node.js module system, where it achieved enormous popularity. Contributing to that popularity were the npm package manager for Node and tools that enabled using Node modules on the client side (browserify, webpack, and others).

From now on, *CommonJS module* means the Node.js version of this standard (which has a few additional features). This is an example of a CommonJS module:

```
[](#cb520-1)// Imports
[](#cb520-2)var importedFunc1 = require('./other-module1.js').importedFunc1;
[](#cb520-3)var importedFunc2 = require('./other-module2.js').importedFunc2;
[](#cb520-4)
[](#cb520-5)// Body
[](#cb520-6)function internalFunc() {
[](#cb520-7)  // ···
[](#cb520-8)}
[](#cb520-9)function exportedFunc() {
[](#cb520-10)  importedFunc1();
[](#cb520-11)  importedFunc2();
[](#cb520-12)  internalFunc();
[](#cb520-13)}
[](#cb520-14)
[](#cb520-15)// Exports
[](#cb520-16)module.exports = {
[](#cb520-17)  exportedFunc: exportedFunc,
[](#cb520-18)};
```

CommonJS can be characterized as follows:

*   Designed for servers.
*   Modules are meant to be loaded *synchronously* (the importer waits while the imported module is loaded and executed).
*   Compact syntax.

### 27.4.2 Client side: AMD (Asynchronous Module Definition) modules

The AMD module format was created to be easier to use in browsers than the CommonJS format. Its most popular implementation is [RequireJS](https://requirejs.org). The following is an example of an AMD module.

```
[](#cb521-1)define(['./other-module1.js', './other-module2.js'],
[](#cb521-2)  function (otherModule1, otherModule2) {
[](#cb521-3)    var importedFunc1 = otherModule1.importedFunc1;
[](#cb521-4)    var importedFunc2 = otherModule2.importedFunc2;
[](#cb521-5)
[](#cb521-6)    function internalFunc() {
[](#cb521-7)      // ···
[](#cb521-8)    }
[](#cb521-9)    function exportedFunc() {
[](#cb521-10)      importedFunc1();
[](#cb521-11)      importedFunc2();
[](#cb521-12)      internalFunc();
[](#cb521-13)    }
[](#cb521-14) 
[](#cb521-15)    return {
[](#cb521-16)      exportedFunc: exportedFunc,
[](#cb521-17)    };
[](#cb521-18)  });
```

AMD can be characterized as follows:

*   Designed for browsers.
*   Modules are meant to be loaded *asynchronously*. That’s a crucial requirement for browsers, where code can’t wait until a module has finished downloading. It has to be notified once the module is available.
*   The syntax is slightly more complicated.

On the plus side, AMD modules can be executed directly. In contrast, CommonJS modules must either be compiled before deployment or custom source code must be generated and evaluated dynamically [(think `eval()`)](#ch026.xhtml_eval). That isn’t always permitted on the web.

### 27.4.3 Characteristics of JavaScript modules

Looking at CommonJS and AMD, similarities between JavaScript module systems emerge:

*   There is one module per file.
*   Such a file is basically a piece of code that is executed:
    *   Local scope: The code is executed in a local “module scope”. Therefore, by default, all of the variables, functions, and classes declared in it are internal and not global.
    *   Exports: If you want any declared entity to be exported, you must explicitly mark it as an export.
    *   Imports: Each module can import exported entities from other modules. Those other modules are identified via *module specifiers* (usually paths, occasionally full URLs).
*   Modules are *singletons*: Even if a module is imported multiple times, only a single “instance” of it exists.
*   No global variables are used. Instead, module specifiers serve as global IDs.

## 27.5 ECMAScript modules

*ECMAScript modules* (*ES modules* or *ESM*) were introduced with ES6\. They continue the tradition of JavaScript modules and have all of their aforementioned characteristics. Additionally:

*   With CommonJS, ES modules share the compact syntax and support for cyclic dependencies.
*   With AMD, ES modules share being designed for asynchronous loading.

ES modules also have new benefits:

*   The syntax is even more compact than CommonJS’s.
*   Modules have *static* structures (which can’t be changed at runtime). That helps with static checking, optimized access of imports, dead code elimination, and more.
*   Support for cyclic imports is completely transparent.

This is an example of ES module syntax:

```
[](#cb522-1)import {importedFunc1} from './other-module1.mjs';
[](#cb522-2)import {importedFunc2} from './other-module2.mjs';
[](#cb522-3)
[](#cb522-4)function internalFunc() {
[](#cb522-5)  ···
[](#cb522-6)}
[](#cb522-7)
[](#cb522-8)export function exportedFunc() {
[](#cb522-9)  importedFunc1();
[](#cb522-10)  importedFunc2();
[](#cb522-11)  internalFunc();
[](#cb522-12)}
```

From now on, “module” means “ECMAScript module”.

### 27.5.1 ES modules: syntax, semantics, loader API

The full standard of ES modules comprises the following parts:

1.  Syntax (how code is written): What is a module? How are imports and exports declared? Etc.
2.  Semantics (how code is executed): How are variable bindings exported? How are imports connected with exports? Etc.
3.  A programmatic loader API for configuring module loading.

Parts 1 and 2 were introduced with ES6\. Work on part 3 is ongoing.

## 27.6 Named exports and imports

### 27.6.1 Named exports

Each module can have zero or more *named exports*.

As an example, consider the following two files:

```
lib/my-math.mjs
main.mjs
```

Module `my-math.mjs` has two named exports: `square` and `LIGHTSPEED`.

```
[](#cb524-1)// Not exported, private to module
[](#cb524-2)function times(a, b) {
[](#cb524-3)  return a * b;
[](#cb524-4)}
[](#cb524-5)export function square(x) {
[](#cb524-6)  return times(x, x);
[](#cb524-7)}
[](#cb524-8)export const LIGHTSPEED = 299792458;
```

To export something, we put the keyword `export` in front of a declaration. Entities that are not exported are private to a module and can’t be accessed from outside.

### 27.6.2 Named imports

Module `main.mjs` has a single named import, `square`:

```
[](#cb525-1)import {square} from './lib/my-math.mjs';
[](#cb525-2)assert.equal(square(3), 9);
```

It can also rename its import:

```
[](#cb526-1)import {square as sq} from './lib/my-math.mjs';
[](#cb526-2)assert.equal(sq(3), 9);
```

#### 27.6.2.1 Syntactic pitfall: named importing is not destructuring

Both named importing and destructuring look similar:

```
[](#cb527-1)import {foo} from './bar.mjs'; // import
[](#cb527-2)const {foo} = require('./bar.mjs'); // destructuring
```

But they are quite different:

*   Imports remain connected with their exports.

*   You can destructure again inside a destructuring pattern, but the `{}` in an import statement can’t be nested.

*   The syntax for renaming is different:

    ```
    [](#cb528-1)import {foo as f} from './bar.mjs'; // importing
    [](#cb528-2)const {foo: f} = require('./bar.mjs'); // destructuring
    ```

    Rationale: Destructuring is reminiscent of an object literal (including nesting), while importing evokes the idea of renaming.

![](media/file6.svg)  **Exercise: Named exports**

`exercises/modules/export_named_test.mjs`

### 27.6.3 Namespace imports

*Namespace imports* are an alternative to named imports. If we namespace-import a module, it becomes an object whose properties are the named exports. This is what `main.mjs` looks like if we use a namespace import:

```
[](#cb529-1)import * as myMath from './lib/my-math.mjs';
[](#cb529-2)assert.equal(myMath.square(3), 9);
[](#cb529-3)
[](#cb529-4)assert.deepEqual(
[](#cb529-5)  Object.keys(myMath), ['LIGHTSPEED', 'square']);
```

### 27.6.4 Named exporting styles: inline versus clause (advanced)

The named export style we have seen so far was *inline*: We exported entities by prefixing them with the keyword `export`.

But we can also use separate *export clauses*. For example, this is what `lib/my-math.mjs` looks like with an export clause:

```
[](#cb530-1)function times(a, b) {
[](#cb530-2)  return a * b;
[](#cb530-3)}
[](#cb530-4)function square(x) {
[](#cb530-5)  return times(x, x);
[](#cb530-6)}
[](#cb530-7)const LIGHTSPEED = 299792458;
[](#cb530-8)
[](#cb530-9)export { square, LIGHTSPEED }; // semicolon!
```

With an export clause, we can rename before exporting and use different names internally:

```
[](#cb531-1)function times(a, b) {
[](#cb531-2)  return a * b;
[](#cb531-3)}
[](#cb531-4)function sq(x) {
[](#cb531-5)  return times(x, x);
[](#cb531-6)}
[](#cb531-7)const LS = 299792458;
[](#cb531-8)
[](#cb531-9)export {
[](#cb531-10)  sq as square,
[](#cb531-11)  LS as LIGHTSPEED, // trailing comma is optional
[](#cb531-12)};
```

## 27.7 Default exports and imports

Each module can have at most one *default export*. The idea is that the module *is* the default-exported value.

![](media/file2.svg)  **Avoid mixing named exports and default exports**

A module can have both named exports and a default export, but it’s usually better to stick to one export style per module.

As an example for default exports, consider the following two files:

```
my-func.mjs
main.mjs
```

Module `my-func.mjs` has a default export:

```
[](#cb533-1)const GREETING = 'Hello!';
[](#cb533-2)export default function () {
[](#cb533-3)  return GREETING;
[](#cb533-4)}
```

Module `main.mjs` default-imports the exported function:

```
[](#cb534-1)import myFunc from './my-func.mjs';
[](#cb534-2)assert.equal(myFunc(), 'Hello!');
```

Note the syntactic difference: the curly braces around named imports indicate that we are reaching *into* the module, while a default import *is* the module.

![](media/file3.svg)  **What are use cases for default exports?**

The most common use case for a default export is a module that contains a single function or a single class.

### 27.7.1 The two styles of default-exporting

There are two styles of doing default exports.

First, you can label existing declarations with `export default`:

```
[](#cb535-1)export default function foo() {} // no semicolon!
[](#cb535-2)export default class Bar {} // no semicolon!
```

Second, you can directly default-export values. In that style, `export default` is itself much like a declaration.

```
[](#cb536-1)export default 'abc';
[](#cb536-2)export default foo();
[](#cb536-3)export default /^xyz$/;
[](#cb536-4)export default 5 * 7;
[](#cb536-5)export default { no: false, yes: true };
```

#### 27.7.1.1 Why are there two default export styles?

The reason is that `export default` can’t be used to label `const`: `const` may define multiple values, but `export default` needs exactly one value. Consider the following hypothetical code:

```
[](#cb537-1)// Not legal JavaScript!
[](#cb537-2)export default const foo = 1, bar = 2, baz = 3;
```

With this code, you don’t know which one of the three values is the default export.

![](media/file6.svg)  **Exercise: Default exports**

`exercises/modules/export_default_test.mjs`

### 27.7.2 The default export as a named export (advanced)

Internally, a default export is simply a named export whose name is `default`. As an example, consider the previous module `my-func.mjs` with a default export:

```
[](#cb538-1)const GREETING = 'Hello!';
[](#cb538-2)export default function () {
[](#cb538-3)  return GREETING;
[](#cb538-4)}
```

The following module `my-func2.mjs` is equivalent to that module:

```
[](#cb539-1)const GREETING = 'Hello!';
[](#cb539-2)function greet() {
[](#cb539-3)  return GREETING;
[](#cb539-4)}
[](#cb539-5)
[](#cb539-6)export {
[](#cb539-7)  greet as default,
[](#cb539-8)};
```

For importing, we can use a normal default import:

```
[](#cb540-1)import myFunc from './my-func2.mjs';
[](#cb540-2)assert.equal(myFunc(), 'Hello!');
```

Or we can use a named import:

```
[](#cb541-1)import {default as myFunc} from './my-func2.mjs';
[](#cb541-2)assert.equal(myFunc(), 'Hello!');
```

The default export is also available via property `.default` of namespace imports:

```
[](#cb542-1)import * as mf from './my-func2.mjs';
[](#cb542-2)assert.equal(mf.default(), 'Hello!');
```

![](media/file3.svg)  **Isn’t `default` illegal as a variable name?**

`default` can’t be a variable name, but it can be an export name and it can be a property name:

```
[](#cb543-1)const obj = {
[](#cb543-2)  default: 123,
[](#cb543-3)};
[](#cb543-4)assert.equal(obj.default, 123);
```

## 27.8 More details on exporting and importing

### 27.8.1 Imports are read-only views on exports

So far, we have used imports and exports intuitively, and everything seems to have worked as expected. But now it is time to take a closer look at how imports and exports are really related.

Consider the following two modules:

```
counter.mjs
main.mjs
```

`counter.mjs` exports a (mutable!) variable and a function:

```
[](#cb545-1)export let counter = 3;
[](#cb545-2)export function incCounter() {
[](#cb545-3)  counter++;
[](#cb545-4)}
```

`main.mjs` name-imports both exports. When we use `incCounter()`, we discover that the connection to `counter` is live – we can always access the live state of that variable:

```
[](#cb546-1)import { counter, incCounter } from './counter.mjs';
[](#cb546-2)
[](#cb546-3)// The imported value `counter` is live
[](#cb546-4)assert.equal(counter, 3);
[](#cb546-5)incCounter();
[](#cb546-6)assert.equal(counter, 4);
```

Note that while the connection is live and we can read `counter`, we cannot change this variable (e.g., via `counter++`).

There are two benefits to handling imports this way:

*   It is easier to split modules because previously shared variables can become exports.
*   This behavior is crucial for supporting transparent cyclic imports. Read on for more information.

### 27.8.2 ESM’s transparent support for cyclic imports (advanced)

ESM supports cyclic imports transparently. To understand how that is achieved, consider the following example: fig. [16](#ch028.xhtml_fig:module-imports) shows a directed graph of modules importing other modules. P importing M is the cycle in this case.

![](media/file25.svg)

Figure 16: A directed graph of modules importing modules: M imports N and O, N imports P and Q, etc.

After parsing, these modules are set up in two phases:

*   Instantiation: Every module is visited and its imports are connected to its exports. Before a parent can be instantiated, all of its children must be instantiated.
*   Evaluation: The bodies of the modules are executed. Once again, children are evaluated before parents.

This approach handles cyclic imports correctly, due to two features of ES modules:

*   Due to the static structure of ES modules, the exports are already known after parsing. That makes it possible to instantiate P before its child M: P can already look up M’s exports.

*   When P is evaluated, M hasn’t been evaluated, yet. However, entities in P can already mention imports from M. They just can’t use them, yet, because the imported values are filled in later. For example, a function in P can access an import from M. The only limitation is that we must wait until after the evaluation of M, before calling that function.

    Imports being filled in later is enabled by them being “live immutable views” on exports.

## 27.9 npm packages

The *npm software registry* is the dominant way of distributing JavaScript libraries and apps for Node.js and web browsers. It is managed via the *npm package manager* (short: *npm*). Software is distributed as so-called *packages*. A package is a directory containing arbitrary files and a file `package.json` at the top level that describes the package. For example, when npm creates an empty package inside a directory `foo/`, you get this `package.json`:

```
[](#cb547-1){
[](#cb547-2)  "name": "foo",
[](#cb547-3)  "version": "1.0.0",
[](#cb547-4)  "description": "",
[](#cb547-5)  "main": "index.js",
[](#cb547-6)  "scripts": {
[](#cb547-7)    "test": "echo \"Error: no test specified\" && exit 1"
[](#cb547-8)  },
[](#cb547-9)  "keywords": [],
[](#cb547-10)  "author": "",
[](#cb547-11)  "license": "ISC"
[](#cb547-12)}
```

Some of these properties contain simple metadata:

*   `name` specifies the name of this package. Once it is uploaded to the npm registry, it can be installed via `npm install foo`.
*   `version` is used for version management and follows [semantic versioning](https://semver.org), with three numbers:
    *   Major version: is incremented when incompatible API changes are made.
    *   Minor version: is incremented when functionality is added in a backward compatible manner.
    *   Patch version: is incremented when backward compatible changes are made.
*   `description`, `keywords`, `author` make it easier to find packages.
*   `license` clarifies how you can use this package.

Other properties enable advanced configuration:

*   `main`: specifies the module that “is” the package (explained later in this chapter).
*   `scripts`: are commands that you can execute via `npm run`. For example, the script `test` can be executed via `npm run test`.

For more information on `package.json`, consult [the npm documentation](https://docs.npmjs.com/files/package.json).

### 27.9.1 Packages are installed inside a directory `node_modules/`

npm always installs packages inside a directory `node_modules`. There are usually many of these directories. Which one npm uses, depends on the directory where one currently is. For example, if we are inside a directory `/tmp/a/b/`, npm tries to find a `node_modules` in the current directory, its parent directory, the parent directory of the parent, etc. In other words, it searches the following *chain* of locations:

*   `/tmp/a/b/node_modules`
*   `/tmp/a/node_modules`
*   `/tmp/node_modules`

When installing a package `foo`, npm uses the closest `node_modules`. If, for example, we are inside `/tmp/a/b/` and there is a `node_modules` in that directory, then npm puts the package inside the directory:

```
/tmp/a/b/node_modules/foo/
```

When importing a module, we can use a special module specifier to tell Node.js that we want to import it from an installed package. How exactly that works, is explained later. For now, consider the following example:

```
[](#cb549-1)// /home/jane/proj/main.mjs
[](#cb549-2)import * as theModule from 'the-package/the-module.mjs';
```

To find `the-module.mjs` (Node.js prefers the filename extension `.mjs` for ES modules), Node.js walks up the `node_module` chain and searches the following locations:

*   `/home/jane/proj/node_modules/the-package/the-module.mjs`
*   `/home/jane/node_modules/the-package/the-module.mjs`
*   `/home/node_modules/the-package/the-module.mjs`

### 27.9.2 Why can npm be used to install frontend libraries?

Finding installed modules in `node_modules` directories is only supported on Node.js. So why can we also use npm to install libraries for browsers?

That is enabled via [bundling tools](#ch047.xhtml_bundler), such as webpack, that compile and optimize code before it is deployed online. During this compilation process, the code in npm packages is adapted so that it works in browsers.

## 27.10 Naming modules

There are no established best practices for naming module files and the variables they are imported into.

In this chapter, I’m using the following naming style:

*   The names of module files are dash-cased and start with lowercase letters:

    ```
    ./my-module.mjs
    ./some-func.mjs
    ```

*   The names of namespace imports are lowercased and camel-cased:

    ```
    [](#cb551-1)import * as myModule from './my-module.mjs';
    ```

*   The names of default imports are lowercased and camel-cased:

    ```
    [](#cb552-1)import someFunc from './some-func.mjs';
    ```

What are the rationales behind this style?

*   npm doesn’t allow uppercase letters in package names ([source](https://docs.npmjs.com/files/package.json#name)). Thus, we avoid camel case, so that “local” files have names that are consistent with those of npm packages. Using only lowercase letters also minimizes conflicts between file systems that are case-sensitive and file systems that aren’t: the former distinguish files whose names have the same letters, but with different cases; the latter don’t.

*   There are clear rules for translating dash-cased file names to camel-cased JavaScript variable names. Due to how we name namespace imports, these rules work for both namespace imports and default imports.

I also like underscore-cased module file names because you can directly use these names for namespace imports (without any translation):

```
[](#cb553-1)import * as my_module from './my_module.mjs';
```

But that style does not work for default imports: I like underscore-casing for namespace objects, but it is not a good choice for functions, etc.

## 27.11 Module specifiers

*Module specifiers* are the strings that identify modules. They work slightly differently in browsers and Node.js. Before we can look at the differences, we need to learn about the different categories of module specifiers.

### 27.11.1 Categories of module specifiers

In ES modules, we distinguish the following categories of specifiers. These categories originated with CommonJS modules.

*   Relative path: starts with a dot. Examples:

    ```
    './some/other/module.mjs'
    '../../lib/counter.mjs'
    ```

*   Absolute path: starts with a slash. Example:

    ```
    '/home/jane/file-tools.mjs'
    ```

*   URL: includes a protocol (technically, paths are URLs, too). Examples:

    ```
    'https://example.com/some-module.mjs'
    'file:///home/john/tmp/main.mjs'
    ```

*   Bare path: does not start with a dot, a slash or a protocol, and consists of a single filename without an extension. Examples:

    ```
    'lodash'
    'the-package'
    ```

*   Deep import path: starts with a bare path and has at least one slash. Example:

    ```
    'the-package/dist/the-module.mjs'
    ```

### 27.11.2 ES module specifiers in browsers

Browsers handle module specifiers as follows:

*   Relative paths, absolute paths, and URLs work as expected. They all must point to real files (in contrast to CommonJS, which lets you omit filename extensions and more).
*   The file name extensions of modules don’t matter, as long as they are served with the content type `text/javascript`.
*   How bare paths will end up being handled is not yet clear. You will probably eventually be able to map them to other specifiers via lookup tables.

Note that [bundling tools](#ch047.xhtml_bundler) such as webpack, which combine modules into fewer files, are often less strict with specifiers than browsers. That’s because they operate at build/compile time (not at runtime) and can search for files by traversing the file system.

### 27.11.3 ES module specifiers on Node.js

![](media/file4.svg)  **Support for ES modules on Node.js is still new**

You may have to switch it on via a command line flag. See [the Node.js documentation](https://nodejs.org/api/esm.html) for details.

Node.js handles module specifiers as follows:

*   Relative paths are resolved as they are in web browsers – relative to the path of the current module.

*   Absolute paths are currently not supported. As a workaround, you can use URLs that start with `file:///`. You can create such URLs via [`url.pathToFileURL()`](#ch028.xhtml_converting-urls-paths).

*   Only `file:` is supported as a protocol for URL specifiers.

*   A bare path is interpreted as a package name and resolved relative to the closest `node_modules` directory. What module should be loaded, is determined by looking at property `"main"` of the package’s `package.json` (similarly to CommonJS).

*   Deep import paths are also resolved relatively to the closest `node_modules` directory. They contain file names, so it is always clear which module is meant.

All specifiers, except bare paths, must refer to actual files. That is, ESM does not support the following CommonJS features:

*   CommonJS automatically adds missing filename extensions.

*   CommonJS can import a directory `foo` if there is a `foo/package.json` with a `"main"` property.

*   CommonJS can import a directory `foo` if there is a module `foo/index.js`.

All built-in Node.js modules are available via bare paths and have named ESM exports – for example:

```
[](#cb559-1)import * as path from 'path';
[](#cb559-2)import {strict as assert} from 'assert';
[](#cb559-3)
[](#cb559-4)assert.equal(
[](#cb559-5)  path.join('a/b/c', '../d'), 'a/b/d');
```

#### 27.11.3.1 Filename extensions on Node.js

Node.js supports the following default filename extensions:

*   `.mjs` for ES modules
*   `.cjs` for CommonJS modules

The filename extension `.js` stands for either ESM or CommonJS. Which one it is is configured via the “closest” `package.json` (in the current directory, the parent directory, etc.). Using `package.json` in this manner is independent of packages.

In that `package.json`, there is a property `"type"`, which has two settings:

*   `"commonjs"` (the default): files with the extension `.js` or without an extension are interpreted as CommonJS modules.

*   `"module"`: files with the extension `.js` or without an extension are interpreted as ESM modules.

#### 27.11.3.2 Interpreting non-file source code as either CommonJS or ESM

Not all source code executed by Node.js comes from files. You can also send it code via stdin, `--eval`, and `--print`. The command line option `--input-type` lets you specify how such code is interpreted:

*   As CommonJS (the default): `--input-type=commonjs`
*   As ESM: `--input-type=module`

## 27.12 Loading modules dynamically via `import()`

So far, the only way to import a module has been via an `import` statement. That statement has several limitations:

*   You must use it at the top level of a module. That is, you can’t, for example, import something when you are inside a block.
*   The module specifier is always fixed. That is, you can’t change what you import depending on a condition. And you can’t assemble a specifier dynamically.

The `import()` operator changes that. Let’s look at an example of it being used.

### 27.12.1 Example: loading a module dynamically

Consider the following files:

```
lib/my-math.mjs
main1.mjs
main2.mjs
```

We have already seen module `my-math.mjs`:

```
[](#cb561-1)// Not exported, private to module
[](#cb561-2)function times(a, b) {
[](#cb561-3)  return a * b;
[](#cb561-4)}
[](#cb561-5)export function square(x) {
[](#cb561-6)  return times(x, x);
[](#cb561-7)}
[](#cb561-8)export const LIGHTSPEED = 299792458;
```

This is what using `import()` looks like in `main1.mjs`:

```
[](#cb562-1)const dir = './lib/';
[](#cb562-2)const moduleSpecifier = dir + 'my-math.mjs';
[](#cb562-3)
[](#cb562-4)function loadConstant() {
[](#cb562-5)  return import(moduleSpecifier)
[](#cb562-6)  .then(myMath => {
[](#cb562-7)    const result = myMath.LIGHTSPEED;
[](#cb562-8)    assert.equal(result, 299792458);
[](#cb562-9)    return result;
[](#cb562-10)  });
[](#cb562-11)}
```

Method `.then()` is part of *Promises*, a mechanism for handling asynchronous results, which is covered [later in this book](#ch041.xhtml_ch_promises).

Two things in this code weren’t possible before:

*   We are importing inside a function (not at the top level).
*   The module specifier comes from a variable.

Next, we’ll implement the exact same functionality in `main2.mjs` but via a so-called *async function*, which provides nicer syntax for Promises.

```
[](#cb563-1)const dir = './lib/';
[](#cb563-2)const moduleSpecifier = dir + 'my-math.mjs';
[](#cb563-3)
[](#cb563-4)async function loadConstant() {
[](#cb563-5)  const myMath = await import(moduleSpecifier);
[](#cb563-6)  const result = myMath.LIGHTSPEED;
[](#cb563-7)  assert.equal(result, 299792458);
[](#cb563-8)  return result;
[](#cb563-9)}
```

![](media/file3.svg)  **Why is `import()` an operator and not a function?**

Even though it works much like a function, `import()` is an operator: in order to resolve module specifiers relatively to the current module, it needs to know from which module it is invoked. A normal function cannot receive this information as implicitly as an operator can. It would need, for example, a parameter.

### 27.12.2 Use cases for `import()`

#### 27.12.2.1 Loading code on demand

Some functionality of web apps doesn’t have to be present when they start, it can be loaded on demand. Then `import()` helps because you can put such functionality into modules – for example:

```
[](#cb564-1)button.addEventListener('click', event => {
[](#cb564-2)  import('./dialogBox.mjs')
[](#cb564-3)    .then(dialogBox => {
[](#cb564-4)      dialogBox.open();
[](#cb564-5)    })
[](#cb564-6)    .catch(error => {
[](#cb564-7)      /* Error handling */
[](#cb564-8)    })
[](#cb564-9)});
```

#### 27.12.2.2 Conditional loading of modules

We may want to load a module depending on whether a condition is true. For example, a module with [a polyfill](#ch028.xhtml_polyfills) that makes a new feature available on legacy platforms:

```
[](#cb565-1)if (isLegacyPlatform()) {
[](#cb565-2)  import('./my-polyfill.mjs')
[](#cb565-3)    .then(···);
[](#cb565-4)}
```

#### 27.12.2.3 Computed module specifiers

For applications such as internationalization, it helps if you can dynamically compute module specifiers:

```
[](#cb566-1)import(`messages_${getLocale()}.mjs`)
[](#cb566-2)  .then(···);
```

## 27.13 Preview: `import.meta.url`

[“`import.meta`”](https://github.com/tc39/proposal-import-meta) is an ECMAScript feature proposed by Domenic Denicola. The object `import.meta` holds metadata for the current module.

Its most important property is `import.meta.url`, which contains a string with the URL of the current module file. For example:

```
'https://example.com/code/main.mjs'
```

### 27.13.1 `import.meta.url` and class `URL`

Class `URL` is available via a global variable in browsers and on Node.js. You can look up its full functionality in [the Node.js documentation](https://nodejs.org/api/url.html#url_class_url). When working with `import.meta.url`, its constructor is especially useful:

```
[](#cb568-1)new URL(input: string, base?: string|URL)
```

Parameter `input` contains the URL to be parsed. It can be relative if the second parameter, `base`, is provided.

In other words, this constructor lets us resolve a relative path against a base URL:

```
> new URL('other.mjs', 'https://example.com/code/main.mjs').href
'https://example.com/code/other.mjs'
> new URL('../other.mjs', 'https://example.com/code/main.mjs').href
'https://example.com/other.mjs'
```

This is how we get a `URL` instance that points to a file `data.txt` that sits next to the current module:

```
[](#cb570-1)const urlOfData = new URL('data.txt', import.meta.url);
```

### 27.13.2 `import.meta.url` on Node.js

On Node.js, `import.meta.url` is always a string with a `file:` URL – for example:

```
'file:///Users/rauschma/my-module.mjs'
```

#### 27.13.2.1 Example: reading a sibling file of a module

Many Node.js file system operations accept either strings with paths or instances of `URL`. That enables us to read a sibling file `data.txt` of the current module:

```
[](#cb572-1)import {promises as fs} from 'fs';
[](#cb572-2)
[](#cb572-3)async function main() {
[](#cb572-4)  const urlOfData = new URL('data.txt', import.meta.url);
[](#cb572-5)  const str = await fs.readFile(urlOfData, {encoding: 'UTF-8'});
[](#cb572-6)  assert.equal(str, 'This is textual data.\n');
[](#cb572-7)}
[](#cb572-8)main();
```

`main()` is an async function, as explained in [§41 “Async functions”](#ch042.xhtml_ch_async-functions).

[`fs.promises`](https://nodejs.org/api/fs.html#fs_fs_promises_api) contains a Promise-based version of the `fs` API, which can be used with async functions.

#### 27.13.2.2 Converting between `file:` URLs and paths

[The Node.js module `url`](https://nodejs.org/api/url.html) has two functions for converting between `file:` URLs and paths:

*   `fileURLToPath(url: URL|string): string`
    Converts a `file:` URL to a path.
*   `pathToFileURL(path: string): URL`
    Converts a path to a `file:` URL.

If you need a path that can be used in the local file system, then property `.pathname` of `URL` instances does not always work:

```
[](#cb573-1)assert.equal(
[](#cb573-2)  new URL('file:///tmp/with%20space.txt').pathname,
[](#cb573-3)  '/tmp/with%20space.txt');
```

Therefore, it is better to use `fileURLToPath()`:

```
[](#cb574-1)import * as url from 'url';
[](#cb574-2)assert.equal(
[](#cb574-3)  url.fileURLToPath('file:///tmp/with%20space.txt'),
[](#cb574-4)  '/tmp/with space.txt'); // result on Unix
```

Similarly, `pathToFileURL()` does more than just prepend `'file://'` to an absolute path.

## 27.14 Polyfills: emulating native web platform features (advanced)

![](media/file5.svg)  **Backends have polyfills, too**

This section is about frontend development and web browsers, but similar ideas apply to backend development.

*Polyfills* help with a conflict that we are facing when developing a web application in JavaScript:

*   On one hand, we want to use modern web platform features that make the app better and/or development easier.
*   On the other hand, the app should run on as many browsers as possible.

Given a web platform feature X:

*   A *polyfill* for X is a piece of code. If it is executed on a platform that already has built-in support for X, it does nothing. Otherwise, it makes the feature available on the platform. In the latter case, the polyfilled feature is (mostly) indistinguishable from a native implementation. In order to achieve that, the polyfill usually makes global changes. For example, it may modify global data or configure a global module loader. Polyfills are often packaged as modules.
    *   The term [*polyfill*](https://remysharp.com/2010/10/08/what-is-a-polyfill) was coined by Remy Sharp.
*   A *speculative polyfill* is a polyfill for a proposed web platform feature (that is not standardized, yet).
    *   Alternative term: *prollyfill*
*   A *replica* of X is a library that reproduces the API and functionality of X locally. Such a library exists independently of a native (and global) implementation of X.
    *   *Replica* is a new term introduced in this section. Alternative term: *ponyfill*
*   There is also the term *shim*, but it doesn’t have a universally agreed upon definition. It often means roughly the same as *polyfill*.

Every time our web applications starts, it must first execute all polyfills for features that may not be available everywhere. Afterwards, we can be sure that those features are available natively.

### 27.14.1 Sources of this section

*   [“What is a Polyfill?”](https://remysharp.com/2010/10/08/what-is-a-polyfill) by Remy Sharp
*   Inspiration for the term *replica*: [The Eiffel Tower in Las Vegas](https://en.wikipedia.org/wiki/Paris_Las_Vegas)
*   Useful clarification of “polyfill” and related terms: [“Polyfills and the evolution of the Web”](https://www.w3.org/2001/tag/doc/polyfills/). Edited by Andrew Betts.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 28 Single objects

* * *

*   28.1 [What is an object?](#ch029.xhtml_what-is-an-object)
    *   28.1.1 [Roles of objects: record vs. dictionary](#ch029.xhtml_roles-of-objects-record-vs.-dictionary)
*   28.2 [Objects as records](#ch029.xhtml_objects-as-records)
    *   28.2.1 [Object literals: properties](#ch029.xhtml_object-literals)
    *   28.2.2 [Object literals: property value shorthands](#ch029.xhtml_object-literals-property-value-shorthands)
    *   28.2.3 [Getting properties](#ch029.xhtml_getting-properties)
    *   28.2.4 [Setting properties](#ch029.xhtml_setting-properties)
    *   28.2.5 [Object literals: methods](#ch029.xhtml_object-literals-methods)
    *   28.2.6 [Object literals: accessors](#ch029.xhtml_object-literals-accessors)
*   28.3 [Spreading into object literals (`...`)](#ch029.xhtml_spreading-into-object-literals)
    *   28.3.1 [Use case for spreading: copying objects](#ch029.xhtml_use-case-for-spreading-copying-objects)
    *   28.3.2 [Use case for spreading: default values for missing properties](#ch029.xhtml_use-case-for-spreading-default-values-for-missing-properties)
    *   28.3.3 [Use case for spreading: non-destructively changing properties](#ch029.xhtml_use-case-for-spreading-non-destructively-changing-properties)
*   28.4 [Methods](#ch029.xhtml_methods)
    *   28.4.1 [Methods are properties whose values are functions](#ch029.xhtml_methods-are-properties-whose-values-are-functions)
    *   28.4.2 [`.call()`: specifying `this` via a parameter](#ch029.xhtml_call-specifying-this-via-a-parameter)
    *   28.4.3 [`.bind()`: pre-filling `this` and parameters of functions](#ch029.xhtml_function-prototype-bind)
    *   28.4.4 [`this` pitfall: extracting methods](#ch029.xhtml_extracting-methods)
    *   28.4.5 [`this` pitfall: accidentally shadowing `this`](#ch029.xhtml_shadowing-this)
    *   28.4.6 [Avoiding the pitfalls of `this`](#ch029.xhtml_avoiding-pitfalls-of-this)
    *   28.4.7 [The value of `this` in various contexts](#ch029.xhtml_the-value-of-this-in-various-contexts)
*   28.5 [Objects as dictionaries (advanced)](#ch029.xhtml_objects-as-dictionaries-advanced)
    *   28.5.1 [Arbitrary fixed strings as property keys](#ch029.xhtml_arbitrary-fixed-strings-as-property-keys)
    *   28.5.2 [Computed property keys](#ch029.xhtml_computed-property-keys)
    *   28.5.3 [The `in` operator: is there a property with a given key?](#ch029.xhtml_in-operator)
    *   28.5.4 [Deleting properties](#ch029.xhtml_deleting-properties)
    *   28.5.5 [Listing property keys](#ch029.xhtml_listing-property-keys)
    *   28.5.6 [Listing property values via `Object.values()`](#ch029.xhtml_listing-property-values-via-object.values)
    *   28.5.7 [Listing property entries via `Object.entries()`](#ch029.xhtml_Object.entries)
    *   28.5.8 [Properties are listed deterministically](#ch029.xhtml_order-of-properties)
    *   28.5.9 [Assembling objects via `Object.fromEntries()`](#ch029.xhtml_Object.fromEntries)
    *   28.5.10 [The pitfalls of using an object as a dictionary](#ch029.xhtml_the-pitfalls-of-using-an-object-as-a-dictionary)
*   28.6 [Standard methods (advanced)](#ch029.xhtml_standard-methods-advanced)
    *   28.6.1 [`.toString()`](#ch029.xhtml_tostring)
    *   28.6.2 [`.valueOf()`](#ch029.xhtml_valueof)
*   28.7 [Advanced topics](#ch029.xhtml_advanced-topics)
    *   28.7.1 [`Object.assign()`](#ch029.xhtml_object.assign)
    *   28.7.2 [Freezing objects](#ch029.xhtml_freezing-objects)
    *   28.7.3 [Property attributes and property descriptors](#ch029.xhtml_property-attributes)

* * *

In this book, JavaScript’s style of object-oriented programming (OOP) is introduced in four steps. This chapter covers step 1; [the next chapter](#ch030.xhtml_ch_proto-chains-classes) covers steps 2–4\. The steps are (fig. [17](#ch029.xhtml_fig:oop_steps1)):

1.  **Single objects (this chapter):** How do *objects*, JavaScript’s basic OOP building blocks, work in isolation?
2.  **Prototype chains (next chapter):** Each object has a chain of zero or more *prototype objects*. Prototypes are JavaScript’s core inheritance mechanism.
3.  **Classes (next chapter):** JavaScript’s *classes* are factories for objects. The relationship between a class and its instances is based on prototypal inheritance.
4.  **Subclassing (next chapter):** The relationship between a *subclass* and its *superclass* is also based on prototypal inheritance.

![](media/file26.svg)

Figure 17: This book introduces object-oriented programming in JavaScript in four steps.

## 28.1 What is an object?

In JavaScript:

*   An object is a set of *properties* (key-value entries).
*   A property key can only be a string or a symbol.

### 28.1.1 Roles of objects: record vs. dictionary

Objects play two roles in JavaScript:

*   Records: Objects-as-records have a fixed number of properties, whose keys are known at development time. Their values can have different types.

*   Dictionaries: Objects-as-dictionaries have a variable number of properties, whose keys are not known at development time. All of their values have the same type.

These roles influence how objects are explained in this chapter:

*   First, we’ll explore objects-as-records. Even though property keys are strings or symbols under the hood, they will appear as fixed identifiers to us, in this part of the chapter.
*   Later, we’ll explore objects-as-dictionaries. Note that [Maps](#ch034.xhtml_ch_maps) are usually better dictionaries than objects. However, some of the operations that we’ll encounter, can also be useful for objects-as-records.

## 28.2 Objects as records

Let’s first explore the role *record* of objects.

### 28.2.1 Object literals: properties

*Object literals* are one way of creating objects-as-records. They are a stand-out feature of JavaScript: you can directly create objects – no need for classes! This is an example:

```
[](#cb575-1)const jane = {
[](#cb575-2)  first: 'Jane',
[](#cb575-3)  last: 'Doe', // optional trailing comma
[](#cb575-4)};
```

In the example, we created an object via an object literal, which starts and ends with curly braces `{}`. Inside it, we defined two *properties* (key-value entries):

*   The first property has the key `first` and the value `'Jane'`.
*   The second property has the key `last` and the value `'Doe'`.

We will later see other ways of specifying property keys, but with this way of specifying them, they must follow the rules of JavaScript variable names. For example, you can use `first_name` as a property key, but not `first-name`). However, reserved words are allowed:

```
[](#cb576-1)const obj = {
[](#cb576-2)  if: true,
[](#cb576-3)  const: true,
[](#cb576-4)};
```

In order to check the effects of various operations on objects, we’ll occasionally use `Object.keys()` in this part of the chapter. It lists property keys:

```
> Object.keys({a:1, b:2})
[ 'a', 'b' ]
```

### 28.2.2 Object literals: property value shorthands

Whenever the value of a property is defined via a variable name and that name is the same as the key, you can omit the key.

```
[](#cb578-1)function createPoint(x, y) {
[](#cb578-2)  return {x, y};
[](#cb578-3)}
[](#cb578-4)assert.deepEqual(
[](#cb578-5)  createPoint(9, 2),
[](#cb578-6)  { x: 9, y: 2 }
[](#cb578-7));
```

### 28.2.3 Getting properties

This is how you *get* (read) a property (line A):

```
[](#cb579-1)const jane = {
[](#cb579-2)  first: 'Jane',
[](#cb579-3)  last: 'Doe',
[](#cb579-4)};
[](#cb579-5)
[](#cb579-6)// Get property .first
[](#cb579-7)assert.equal(jane.first, 'Jane'); // (A)
```

Getting an unknown property produces `undefined`:

```
[](#cb580-1)assert.equal(jane.unknownProperty, undefined);
```

### 28.2.4 Setting properties

This is how you *set* (write to) a property:

```
[](#cb581-1)const obj = {
[](#cb581-2)  prop: 1,
[](#cb581-3)};
[](#cb581-4)assert.equal(obj.prop, 1);
[](#cb581-5)obj.prop = 2; // (A)
[](#cb581-6)assert.equal(obj.prop, 2);
```

We just changed an existing property via setting. If we set an unknown property, we create a new entry:

```
[](#cb582-1)const obj = {}; // empty object
[](#cb582-2)assert.deepEqual(
[](#cb582-3)  Object.keys(obj), []);
[](#cb582-4)
[](#cb582-5)obj.unknownProperty = 'abc';
[](#cb582-6)assert.deepEqual(
[](#cb582-7)  Object.keys(obj), ['unknownProperty']);
```

### 28.2.5 Object literals: methods

The following code shows how to create the method `.says()` via an object literal:

```
[](#cb583-1)const jane = {
[](#cb583-2)  first: 'Jane', // data property
[](#cb583-3)  says(text) {   // method
[](#cb583-4)    return `${this.first} says “${text}”`; // (A)
[](#cb583-5)  }, // comma as separator (optional at end)
[](#cb583-6)};
[](#cb583-7)assert.equal(jane.says('hello'), 'Jane says “hello”');
```

During the method call `jane.says('hello')`, `jane` is called the *receiver* of the method call and assigned to the special variable `this`. That enables method `.says()` to access the sibling property `.first` in line A.

### 28.2.6 Object literals: accessors

There are two kinds of accessors in JavaScript:

*   A *getter* is a method-like entity that is invoked by getting a property.
*   A *setter* is a method-like entity that is invoked by setting a property.

#### 28.2.6.1 Getters

A getter is created by prefixing a method definition with the modifier `get`:

```
[](#cb584-1)const jane = {
[](#cb584-2)  first: 'Jane',
[](#cb584-3)  last: 'Doe',
[](#cb584-4)  get full() {
[](#cb584-5)    return `${this.first}  ${this.last}`;
[](#cb584-6)  },
[](#cb584-7)};
[](#cb584-8)
[](#cb584-9)assert.equal(jane.full, 'Jane Doe');
[](#cb584-10)jane.first = 'John';
[](#cb584-11)assert.equal(jane.full, 'John Doe');
```

#### 28.2.6.2 Setters

A setter is created by prefixing a method definition with the modifier `set`:

```
[](#cb585-1)const jane = {
[](#cb585-2)  first: 'Jane',
[](#cb585-3)  last: 'Doe',
[](#cb585-4)  set full(fullName) {
[](#cb585-5)    const parts = fullName.split(' ');
[](#cb585-6)    this.first = parts[0];
[](#cb585-7)    this.last = parts[1];
[](#cb585-8)  },
[](#cb585-9)};
[](#cb585-10)
[](#cb585-11)jane.full = 'Richard Roe';
[](#cb585-12)assert.equal(jane.first, 'Richard');
[](#cb585-13)assert.equal(jane.last, 'Roe');
```

![](media/file6.svg)  **Exercise: Creating an object via an object literal**

`exercises/single-objects/color_point_object_test.mjs`

## 28.3 Spreading into object literals (`...`)

[Inside a function call](#ch026.xhtml_spread-arguments), spreading (`...`) turns the iterated values of [an *iterable* object](#ch031.xhtml_ch_sync-iteration) into arguments.

Inside an object literal, a *spread property* adds the properties of another object to the current one:

```
> const obj = {foo: 1, bar: 2};
> {...obj, baz: 3}
{ foo: 1, bar: 2, baz: 3 }
```

If property keys clash, the property that is mentioned last “wins”:

```
> const obj = {foo: 1, bar: 2, baz: 3};
> {...obj, foo: true}
{ foo: true, bar: 2, baz: 3 }
> {foo: true, ...obj}
{ foo: 1, bar: 2, baz: 3 }
```

All values are spreadable, even `undefined` and `null`:

```
> {...undefined}
{}
> {...null}
{}
> {...123}
{}
> {...'abc'}
{ '0': 'a', '1': 'b', '2': 'c' }
> {...['a', 'b']}
{ '0': 'a', '1': 'b' }
```

Property `.length` of strings and of Arrays is hidden from this kind of operation (it is not *enumerable*; see [§28.7.3 “Property attributes and property descriptors”](#ch029.xhtml_property-attributes) for more information).

### 28.3.1 Use case for spreading: copying objects

You can use spreading to create a copy of an object `original`:

```
[](#cb589-1)const copy = {...original};
```

Caveat – copying is *shallow*: `copy` is a fresh object with duplicates of all properties (key-value entries) of `original`. But if property values are objects, then those are not copied themselves; they are shared between `original` and `copy`. Let’s look at an example:

```
[](#cb590-1)const original = { a: 1, b: {foo: true} };
[](#cb590-2)const copy = {...original};
```

The first level of `copy` is really a copy: If you change any properties at that level, it does not affect the original:

```
[](#cb591-1)copy.a = 2;
[](#cb591-2)assert.deepEqual(
[](#cb591-3)  original, { a: 1, b: {foo: true} }); // no change
```

However, deeper levels are not copied. For example, the value of `.b` is shared between original and copy. Changing `.b` in the copy also changes it in the original.

```
[](#cb592-1)copy.b.foo = false;
[](#cb592-2)assert.deepEqual(
[](#cb592-3)  original, { a: 1, b: {foo: false} });
```

![](media/file4.svg)  **JavaScript doesn’t have built-in support for deep copying**

*Deep copies* of objects (where all levels are copied) are notoriously difficult to do generically. Therefore, JavaScript does not have a built-in operation for them (for now). If you need such an operation, you have to implement it yourself.

### 28.3.2 Use case for spreading: default values for missing properties

If one of the inputs of your code is an object with data, you can make properties optional by specifying default values that are used if those properties are missing. One technique for doing so is via an object whose properties contain the default values. In the following example, that object is `DEFAULTS`:

```
[](#cb593-1)const DEFAULTS = {foo: 'a', bar: 'b'};
[](#cb593-2)const providedData = {foo: 1};
[](#cb593-3)
[](#cb593-4)const allData = {...DEFAULTS, ...providedData};
[](#cb593-5)assert.deepEqual(allData, {foo: 1, bar: 'b'});
```

The result, the object `allData`, is created by copying `DEFAULTS` and overriding its properties with those of `providedData`.

But you don’t need an object to specify the default values; you can also specify them inside the object literal, individually:

```
[](#cb594-1)const providedData = {foo: 1};
[](#cb594-2)
[](#cb594-3)const allData = {foo: 'a', bar: 'b', ...providedData};
[](#cb594-4)assert.deepEqual(allData, {foo: 1, bar: 'b'});
```

### 28.3.3 Use case for spreading: non-destructively changing properties

So far, we have encountered one way of changing a property `.foo` of an object: We *set* it (line A) and mutate the object. That is, this way of changing a property is *destructive*.

```
[](#cb595-1)const obj = {foo: 'a', bar: 'b'};
[](#cb595-2)obj.foo = 1; // (A)
[](#cb595-3)assert.deepEqual(obj, {foo: 1, bar: 'b'});
```

With spreading, we can change `.foo` *non-destructively* – we make a copy of `obj` where `.foo` has a different value:

```
[](#cb596-1)const obj = {foo: 'a', bar: 'b'};
[](#cb596-2)const updatedObj = {...obj, foo: 1};
[](#cb596-3)assert.deepEqual(updatedObj, {foo: 1, bar: 'b'});
```

![](media/file6.svg)  **Exercise: Non-destructively updating a property via spreading (fixed key)**

`exercises/single-objects/update_name_test.mjs`

## 28.4 Methods

### 28.4.1 Methods are properties whose values are functions

Let’s revisit the example that was used to introduce methods:

```
[](#cb597-1)const jane = {
[](#cb597-2)  first: 'Jane',
[](#cb597-3)  says(text) {
[](#cb597-4)    return `${this.first} says “${text}”`;
[](#cb597-5)  },
[](#cb597-6)};
```

Somewhat surprisingly, methods are functions:

```
[](#cb598-1)assert.equal(typeof jane.says, 'function');
```

Why is that? We learned [in the chapter on callable values](#ch026.xhtml_roles-of-ordinary-functions), that ordinary functions play several roles. *Method* is one of those roles. Therefore, under the hood, `jane` roughly looks as follows.

```
[](#cb599-1)const jane = {
[](#cb599-2)  first: 'Jane',
[](#cb599-3)  says: function (text) {
[](#cb599-4)    return `${this.first} says “${text}”`;
[](#cb599-5)  },
[](#cb599-6)};
```

### 28.4.2 `.call()`: specifying `this` via a parameter

Remember that each function `someFunc` is also an object and therefore has methods. One such method is `.call()` – it lets you call a function while specifying `this` via a parameter:

```
[](#cb600-1)someFunc.call(thisValue, arg1, arg2, arg3);
```

#### 28.4.2.1 Methods and `.call()`

If you make a method call, `this` is an implicit parameter that is filled in via the receiver of the call:

```
[](#cb601-1)const obj = {
[](#cb601-2)  method(x) {
[](#cb601-3)    assert.equal(this, obj); // implicit parameter
[](#cb601-4)    assert.equal(x, 'a');
[](#cb601-5)  },
[](#cb601-6)};
[](#cb601-7)
[](#cb601-8)obj.method('a'); // receiver is `obj`
```

The method call in the last line sets up `this` as follows:

```
[](#cb602-1)obj.method.call(obj, 'a');
```

As an aside, that means that there are actually two different dot operators:

1.  One for accessing properties: `obj.prop`
2.  One for making method calls: `obj.prop()`

They are different in that (2) is not just (1) followed by the function call operator `()`. Instead, (2) additionally specifies a value for `this`.

#### 28.4.2.2 Functions and `.call()`

If you function-call an ordinary function, its implicit parameter `this` is also provided – it is implicitly set to `undefined`:

```
[](#cb603-1)function func(x) {
[](#cb603-2)  assert.equal(this, undefined); // implicit parameter
[](#cb603-3)  assert.equal(x, 'a');
[](#cb603-4)}
[](#cb603-5)
[](#cb603-6)func('a');
```

The method call in the last line sets up `this` as follows:

```
[](#cb604-1)func.call(undefined, 'a');
```

`this` being set to `undefined` during a function call, indicates that it is a feature that is only needed during a method call.

Next, we’ll examine the pitfalls of using `this`. Before we can do that, we need one more tool: method `.bind()` of functions.

### 28.4.3 `.bind()`: pre-filling `this` and parameters of functions

`.bind()` is another method of function objects. This method is invoked as follows:

```
[](#cb605-1)const boundFunc = someFunc.bind(thisValue, arg1, arg2);
```

`.bind()` returns a new function `boundFunc()`. Calling that function invokes `someFunc()` with `this` set to `thisValue` and these parameters: `arg1`, `arg2`, followed by the parameters of `boundFunc()`.

That is, the following two function calls are equivalent:

```
[](#cb606-1)boundFunc('a', 'b')
[](#cb606-2)someFunc.call(thisValue, arg1, arg2, 'a', 'b')
```

#### 28.4.3.1 An alternative to `.bind()`

Another way of pre-filling `this` and parameters is via an arrow function:

```
[](#cb607-1)const boundFunc2 = (...args) =>
[](#cb607-2)  someFunc.call(thisValue, arg1, arg2, ...args);
```

#### 28.4.3.2 An implementation of `.bind()`

Considering the previous section, `.bind()` can be implemented as a real function as follows:

```
[](#cb608-1)function bind(func, thisValue, ...boundArgs) {
[](#cb608-2)  return (...args) =>
[](#cb608-3)    func.call(thisValue, ...boundArgs, ...args);
[](#cb608-4)}
```

#### 28.4.3.3 Example: binding a real function

Using `.bind()` for real functions is somewhat unintuitive because you have to provide a value for `this`. Given that it is `undefined` during function calls, it is usually set to `undefined` or `null`.

In the following example, we create `add8()`, a function that has one parameter, by binding the first parameter of `add()` to `8`.

```
[](#cb609-1)function add(x, y) {
[](#cb609-2)  return x + y;
[](#cb609-3)}
[](#cb609-4)
[](#cb609-5)const add8 = add.bind(undefined, 8);
[](#cb609-6)assert.equal(add8(1), 9);
```

#### 28.4.3.4 Example: binding a method

In the following code, we turn method `.says()` into the stand-alone function `func()`:

```
[](#cb610-1)const jane = {
[](#cb610-2)  first: 'Jane',
[](#cb610-3)  says(text) {
[](#cb610-4)    return `${this.first} says “${text}”`; // (A)
[](#cb610-5)  },
[](#cb610-6)};
[](#cb610-7)
[](#cb610-8)const func = jane.says.bind(jane, 'hello');
[](#cb610-9)assert.equal(func(), 'Jane says “hello”');
```

Setting `this` to `jane` via `.bind()` is crucial here. Otherwise, `func()` wouldn’t work properly because `this` is used in line A.

### 28.4.4 `this` pitfall: extracting methods

We now know quite a bit about functions and methods and are ready to take a look at the biggest pitfall involving methods and `this`: function-calling a method extracted from an object can fail if you are not careful.

In the following example, we fail when we extract method `jane.says()`, store it in the variable `func`, and function-call `func()`.

```
[](#cb611-1)const jane = {
[](#cb611-2)  first: 'Jane',
[](#cb611-3)  says(text) {
[](#cb611-4)    return `${this.first} says “${text}”`;
[](#cb611-5)  },
[](#cb611-6)};
[](#cb611-7)const func = jane.says; // extract the method
[](#cb611-8)assert.throws(
[](#cb611-9)  () => func('hello'), // (A)
[](#cb611-10)  {
[](#cb611-11)    name: 'TypeError',
[](#cb611-12)    message: "Cannot read property 'first' of undefined",
[](#cb611-13)  });
```

The function call in line A is equivalent to:

```
[](#cb612-1)assert.throws(
[](#cb612-2)  () => jane.says.call(undefined, 'hello'), // `this` is undefined!
[](#cb612-3)  {
[](#cb612-4)    name: 'TypeError',
[](#cb612-5)    message: "Cannot read property 'first' of undefined",
[](#cb612-6)  });
```

So how do we fix this? We need to use `.bind()` to extract method `.says()`:

```
[](#cb613-1)const func2 = jane.says.bind(jane);
[](#cb613-2)assert.equal(func2('hello'), 'Jane says “hello”');
```

The `.bind()` ensures that `this` is always `jane` when we call `func()`.

You can also use arrow functions to extract methods:

```
[](#cb614-1)const func3 = text => jane.says(text);
[](#cb614-2)assert.equal(func3('hello'), 'Jane says “hello”');
```

#### 28.4.4.1 Example: extracting a method

The following is a simplified version of code that you may see in actual web development:

```
[](#cb615-1)class ClickHandler {
[](#cb615-2)  constructor(id, elem) {
[](#cb615-3)    this.id = id;
[](#cb615-4)    elem.addEventListener('click', this.handleClick); // (A)
[](#cb615-5)  }
[](#cb615-6)  handleClick(event) {
[](#cb615-7)    alert('Clicked ' + this.id);
[](#cb615-8)  }
[](#cb615-9)}
```

In line A, we don’t extract the method `.handleClick()` properly. Instead, we should do:

```
[](#cb616-1)elem.addEventListener('click', this.handleClick.bind(this));
```

![](media/file6.svg)  **Exercise: Extracting a method**

`exercises/single-objects/method_extraction_exrc.mjs`

### 28.4.5 `this` pitfall: accidentally shadowing `this`

![](media/file2.svg)  **Accidentally shadowing `this` is only an issue with ordinary functions**

Arrow functions don’t shadow `this`.

Consider the following problem: when you are inside an ordinary function, you can’t access the `this` of the surrounding scope because the ordinary function has its own `this`. In other words, a variable in an inner scope hides a variable in an outer scope. That is called [*shadowing*](#ch013.xhtml_shadowing-variables). The following code is an example:

```
[](#cb617-1)const prefixer = {
[](#cb617-2)  prefix: '==> ',
[](#cb617-3)  prefixStringArray(stringArray) {
[](#cb617-4)    return stringArray.map(
[](#cb617-5)      function (x) {
[](#cb617-6)        return this.prefix + x; // (A)
[](#cb617-7)      });
[](#cb617-8)  },
[](#cb617-9)};
[](#cb617-10)assert.throws(
[](#cb617-11)  () => prefixer.prefixStringArray(['a', 'b']),
[](#cb617-12)  /^TypeError: Cannot read property 'prefix' of undefined$/);
```

In line A, we want to access the `this` of `.prefixStringArray()`. But we can’t since the surrounding ordinary function has its own `this` that *shadows* (blocks access to) the `this` of the method. The value of the former `this` is `undefined` due to the callback being function-called. That explains the error message.

The simplest way to fix this problem is via an arrow function, which doesn’t have its own `this` and therefore doesn’t shadow anything:

```
[](#cb618-1)const prefixer = {
[](#cb618-2)  prefix: '==> ',
[](#cb618-3)  prefixStringArray(stringArray) {
[](#cb618-4)    return stringArray.map(
[](#cb618-5)      (x) => {
[](#cb618-6)        return this.prefix + x;
[](#cb618-7)      });
[](#cb618-8)  },
[](#cb618-9)};
[](#cb618-10)assert.deepEqual(
[](#cb618-11)  prefixer.prefixStringArray(['a', 'b']),
[](#cb618-12)  ['==> a', '==> b']);
```

We can also store `this` in a different variable (line A), so that it doesn’t get shadowed:

```
[](#cb619-1)prefixStringArray(stringArray) {
[](#cb619-2)  const that = this; // (A)
[](#cb619-3)  return stringArray.map(
[](#cb619-4)    function (x) {
[](#cb619-5)      return that.prefix + x;
[](#cb619-6)    });
[](#cb619-7)},
```

Another option is to specify a fixed `this` for the callback via `.bind()` (line A):

```
[](#cb620-1)prefixStringArray(stringArray) {
[](#cb620-2)  return stringArray.map(
[](#cb620-3)    function (x) {
[](#cb620-4)      return this.prefix + x;
[](#cb620-5)    }.bind(this)); // (A)
[](#cb620-6)},
```

Lastly, `.map()` lets us specify a value for `this` (line A) that it uses when invoking the callback:

```
[](#cb621-1)prefixStringArray(stringArray) {
[](#cb621-2)  return stringArray.map(
[](#cb621-3)    function (x) {
[](#cb621-4)      return this.prefix + x;
[](#cb621-5)    },
[](#cb621-6)    this); // (A)
[](#cb621-7)},
```

### 28.4.6 Avoiding the pitfalls of `this`

We have seen two big `this`-related pitfalls:

1.  [Extracting methods](#ch029.xhtml_extracting-methods)
2.  [Accidentally shadowing `this`](#ch029.xhtml_shadowing-this)

One simple rule helps avoid the second pitfall:

> “Avoid the keyword `function`”: Never use ordinary functions, only arrow functions (for real functions) and method definitions.

Following this rule has two benefits:

*   It prevents the second pitfall because ordinary functions are never used as real functions.
*   `this` becomes easier to understand because it will only appear inside methods (never inside ordinary functions). That makes it clear that `this` is an OOP feature.

However, even though I don’t use (ordinary) function *expressions* anymore, I do like function *declarations* syntactically. You can use them safely if you don’t refer to `this` inside them. The static checking tool ESLint can warn you during development when you do this wrong via [a built-in rule](https://eslint.org/docs/rules/no-invalid-this).

Alas, there is no simple way around the first pitfall: whenever you extract a method, you have to be careful and do it properly – for example, by binding `this`.

### 28.4.7 The value of `this` in various contexts

What is the value of `this` in various contexts?

Inside a callable entity, the value of `this` depends on how the callable entity is invoked and what kind of callable entity it is:

*   Function call:
    *   Ordinary functions: `this === undefined` (in strict mode)
    *   Arrow functions: `this` is same as in surrounding scope (lexical `this`)
*   Method call: `this` is receiver of call
*   `new`: `this` refers to newly created instance

You can also access `this` in all common top-level scopes:

*   `<script>` element: `this === globalThis`
*   ECMAScript modules: `this === undefined`
*   CommonJS modules: `this === module.exports`

However, I like to pretend that you can’t access `this` in top-level scopes because top-level `this` is confusing and rarely useful.

## 28.5 Objects as dictionaries (advanced)

Objects work best as records. But before ES6, JavaScript did not have a data structure for dictionaries (ES6 brought [Maps](#ch034.xhtml_ch_maps)). Therefore, objects had to be used as dictionaries, which imposed a signficant constraint: keys had to be strings (symbols were also introduced with ES6).

We first look at features of objects that are related to dictionaries but also useful for objects-as-records. This section concludes with tips for actually using objects as dictionaries (spoiler: use Maps if you can).

### 28.5.1 Arbitrary fixed strings as property keys

So far, we have always used objects as records. Property keys were fixed tokens that had to be valid identifiers and internally became strings:

```
[](#cb622-1)const obj = {
[](#cb622-2)  mustBeAnIdentifier: 123,
[](#cb622-3)};
[](#cb622-4)
[](#cb622-5)// Get property
[](#cb622-6)assert.equal(obj.mustBeAnIdentifier, 123);
[](#cb622-7)
[](#cb622-8)// Set property
[](#cb622-9)obj.mustBeAnIdentifier = 'abc';
[](#cb622-10)assert.equal(obj.mustBeAnIdentifier, 'abc');
```

As a next step, we’ll go beyond this limitation for property keys: In this section, we’ll use arbitrary fixed strings as keys. In the next subsection, we’ll dynamically compute keys.

Two techniques allow us to use arbitrary strings as property keys.

First, when creating property keys via object literals, we can quote property keys (with single or double quotes):

```
[](#cb623-1)const obj = {
[](#cb623-2)  'Can be any string!': 123,
[](#cb623-3)};
```

Second, when getting or setting properties, we can use square brackets with strings inside them:

```
[](#cb624-1)// Get property
[](#cb624-2)assert.equal(obj['Can be any string!'], 123);
[](#cb624-3)
[](#cb624-4)// Set property
[](#cb624-5)obj['Can be any string!'] = 'abc';
[](#cb624-6)assert.equal(obj['Can be any string!'], 'abc');
```

You can also use these techniques for methods:

```
[](#cb625-1)const obj = {
[](#cb625-2)  'A nice method'() {
[](#cb625-3)    return 'Yes!';
[](#cb625-4)  },
[](#cb625-5)};
[](#cb625-6)
[](#cb625-7)assert.equal(obj['A nice method'](), 'Yes!');
```

### 28.5.2 Computed property keys

So far, property keys were always fixed strings inside object literals. In this section we learn how to dynamically compute property keys. That enables us to use either arbitrary strings or symbols.

The syntax of dynamically computed property keys in object literals is inspired by dynamically accessing properties. That is, we can use square brackets to wrap expressions:

```
[](#cb626-1)const obj = {
[](#cb626-2)  ['Hello world!']: true,
[](#cb626-3)  ['f'+'o'+'o']: 123,
[](#cb626-4)  [Symbol.toStringTag]: 'Goodbye', // (A)
[](#cb626-5)};
[](#cb626-6)
[](#cb626-7)assert.equal(obj['Hello world!'], true);
[](#cb626-8)assert.equal(obj.foo, 123);
[](#cb626-9)assert.equal(obj[Symbol.toStringTag], 'Goodbye');
```

The main use case for computed keys is having symbols as property keys (line A).

Note that the square brackets operator for getting and setting properties works with arbitrary expressions:

```
[](#cb627-1)assert.equal(obj['f'+'o'+'o'], 123);
[](#cb627-2)assert.equal(obj['==> foo'.slice(-3)], 123);
```

Methods can have computed property keys, too:

```
[](#cb628-1)const methodKey = Symbol();
[](#cb628-2)const obj = {
[](#cb628-3)  [methodKey]() {
[](#cb628-4)    return 'Yes!';
[](#cb628-5)  },
[](#cb628-6)};
[](#cb628-7)
[](#cb628-8)assert.equal(obj[methodKey](), 'Yes!');
```

For the remainder of this chapter, we’ll mostly use fixed property keys again (because they are syntactically more convenient). But all features are also available for arbitrary strings and symbols.

![](media/file6.svg)  **Exercise: Non-destructively updating a property via spreading (computed key)**

`exercises/single-objects/update_property_test.mjs`

### 28.5.3 The `in` operator: is there a property with a given key?

The `in` operator checks if an object has a property with a given key:

```
[](#cb629-1)const obj = {
[](#cb629-2)  foo: 'abc',
[](#cb629-3)  bar: false,
[](#cb629-4)};
[](#cb629-5)
[](#cb629-6)assert.equal('foo' in obj, true);
[](#cb629-7)assert.equal('unknownKey' in obj, false);
```

#### 28.5.3.1 Checking if a property exists via truthiness

You can also use a truthiness check to determine if a property exists:

```
[](#cb630-1)assert.equal(
[](#cb630-2)  obj.foo ? 'exists' : 'does not exist',
[](#cb630-3)  'exists');
[](#cb630-4)assert.equal(
[](#cb630-5)  obj.unknownKey ? 'exists' : 'does not exist',
[](#cb630-6)  'does not exist');
```

The previous checks work because `obj.foo` is truthy and because reading a missing property returns `undefined` (which is falsy).

There is, however, one important caveat: truthiness checks fail if the property exists, but has a falsy value (`undefined`, `null`, `false`, `0`, `""`, etc.):

```
[](#cb631-1)assert.equal(
[](#cb631-2)  obj.bar ? 'exists' : 'does not exist',
[](#cb631-3)  'does not exist'); // should be: 'exists'
```

### 28.5.4 Deleting properties

You can delete properties via the `delete` operator:

```
[](#cb632-1)const obj = {
[](#cb632-2)  foo: 123,
[](#cb632-3)};
[](#cb632-4)assert.deepEqual(Object.keys(obj), ['foo']);
[](#cb632-5)
[](#cb632-6)delete obj.foo;
[](#cb632-7)
[](#cb632-8)assert.deepEqual(Object.keys(obj), []);
```

### 28.5.5 Listing property keys

Table 18: Standard library methods for listing *own* (non-inherited) property keys. All of them return Arrays with strings and/or symbols.

|  | enumerable | non-e. | string | symbol |
| --- | --- | --- | --- | --- |
| `Object.keys()` | `✔` |  | `✔` |  |
| `Object.getOwnPropertyNames()` | `✔` | `✔` | `✔` |  |
| `Object.getOwnPropertySymbols()` | `✔` | `✔` |  | `✔` |
| `Reflect.ownKeys()` | `✔` | `✔` | `✔` | `✔` |

Each of the methods in tbl. [18](#ch029.xhtml_tbl:listing-property-keys) returns an Array with the own property keys of the parameter. In the names of the methods, you can see that the following distinction is made:

*   A *property key* can be either a string or a symbol.
*   A *property name* is a property key whose value is a string.
*   A *property symbol* is a property key whose value is a symbol.

The next section describes the term *enumerable* and demonstrates each of the methods.

#### 28.5.5.1 Enumerability

*Enumerability* is an [*attribute*](#ch029.xhtml_property-attributes) of a property. Non-enumerable properties are ignored by some operations – for example, by `Object.keys()` (see tbl. [18](#ch029.xhtml_tbl:listing-property-keys)) and by spread properties. By default, most properties are enumerable. The next example shows how to change that. It also demonstrates the various ways of listing property keys.

```
[](#cb633-1)const enumerableSymbolKey = Symbol('enumerableSymbolKey');
[](#cb633-2)const nonEnumSymbolKey = Symbol('nonEnumSymbolKey');
[](#cb633-3)
[](#cb633-4)// We create enumerable properties via an object literal
[](#cb633-5)const obj = {
[](#cb633-6)  enumerableStringKey: 1,
[](#cb633-7)  [enumerableSymbolKey]: 2,
[](#cb633-8)}
[](#cb633-9)
[](#cb633-10)// For non-enumerable properties, we need a more powerful tool
[](#cb633-11)Object.defineProperties(obj, {
[](#cb633-12)  nonEnumStringKey: {
[](#cb633-13)    value: 3,
[](#cb633-14)    enumerable: false,
[](#cb633-15)  },
[](#cb633-16)  [nonEnumSymbolKey]: {
[](#cb633-17)    value: 4,
[](#cb633-18)    enumerable: false,
[](#cb633-19)  },
[](#cb633-20)});
[](#cb633-21)
[](#cb633-22)assert.deepEqual(
[](#cb633-23)  Object.keys(obj),
[](#cb633-24)  [ 'enumerableStringKey' ]);
[](#cb633-25)assert.deepEqual(
[](#cb633-26)  Object.getOwnPropertyNames(obj),
[](#cb633-27)  [ 'enumerableStringKey', 'nonEnumStringKey' ]);
[](#cb633-28)assert.deepEqual(
[](#cb633-29)  Object.getOwnPropertySymbols(obj),
[](#cb633-30)  [ enumerableSymbolKey, nonEnumSymbolKey ]);
[](#cb633-31)assert.deepEqual(
[](#cb633-32)  Reflect.ownKeys(obj),
[](#cb633-33)  [
[](#cb633-34)    'enumerableStringKey', 'nonEnumStringKey',
[](#cb633-35)    enumerableSymbolKey, nonEnumSymbolKey,
[](#cb633-36)  ]);
```

`Object.defineProperties()` is explained [later in this chapter](#ch029.xhtml_property-attributes).

### 28.5.6 Listing property values via `Object.values()`

`Object.values()` lists the values of all enumerable properties of an object:

```
[](#cb634-1)const obj = {foo: 1, bar: 2};
[](#cb634-2)assert.deepEqual(
[](#cb634-3)  Object.values(obj),
[](#cb634-4)  [1, 2]);
```

### 28.5.7 Listing property entries via `Object.entries()`

`Object.entries()` lists key-value pairs of enumerable properties. Each pair is encoded as a two-element Array:

```
[](#cb635-1)const obj = {foo: 1, bar: 2};
[](#cb635-2)assert.deepEqual(
[](#cb635-3)  Object.entries(obj),
[](#cb635-4)  [
[](#cb635-5)    ['foo', 1],
[](#cb635-6)    ['bar', 2],
[](#cb635-7)  ]);
```

![](media/file6.svg)  **Exercise: `Object.entries()`**

`exercises/single-objects/find_key_test.mjs`

### 28.5.8 Properties are listed deterministically

Own (non-inherited) properties of objects are always listed in the following order:

1.  Properties with string keys that contain integer indices (that includes [Array indices](#ch032.xhtml_array-indices)):
    In ascending numeric order
2.  Remaining properties with string keys:
    In the order in which they were added
3.  Properties with symbol keys:
    In the order in which they were added

The following example demonstrates how property keys are sorted according to these rules:

```
> Object.keys({b:0,a:0, 10:0,2:0})
[ '2', '10', 'b', 'a' ]
```

![](media/file5.svg)  **The order of properties**

[The ECMAScript specification](https://tc39.github.io/ecma262/#sec-ordinaryownpropertykeys) describes in more detail how properties are ordered.

### 28.5.9 Assembling objects via `Object.fromEntries()`

Given an iterable over [key, value] pairs, `Object.fromEntries()` creates an object:

```
[](#cb637-1)assert.deepEqual(
[](#cb637-2)  Object.fromEntries([['foo',1], ['bar',2]]),
[](#cb637-3)  {
[](#cb637-4)    foo: 1,
[](#cb637-5)    bar: 2,
[](#cb637-6)  }
[](#cb637-7));
```

`Object.fromEntries()` does the opposite of [`Object.entries()`](#ch029.xhtml_Object.entries).

To demonstrate both, we’ll use them to implement two tool functions from the library [Underscore](https://underscorejs.org) in the next subsubsections.

#### 28.5.9.1 Example: `pick(object, ...keys)`

[`pick`](https://underscorejs.org/#pick) returns a copy of `object` that only has those properties whose keys are mentioned as arguments:

```
[](#cb638-1)const address = {
[](#cb638-2)  street: 'Evergreen Terrace',
[](#cb638-3)  number: '742',
[](#cb638-4)  city: 'Springfield',
[](#cb638-5)  state: 'NT',
[](#cb638-6)  zip: '49007',
[](#cb638-7)};
[](#cb638-8)assert.deepEqual(
[](#cb638-9)  pick(address, 'street', 'number'),
[](#cb638-10)  {
[](#cb638-11)    street: 'Evergreen Terrace',
[](#cb638-12)    number: '742',
[](#cb638-13)  }
[](#cb638-14));
```

We can implement `pick()` as follows:

```
[](#cb639-1)function pick(object, ...keys) {
[](#cb639-2)  const filteredEntries = Object.entries(object)
[](#cb639-3)    .filter(([key, _value]) => keys.includes(key));
[](#cb639-4)  return Object.fromEntries(filteredEntries);
[](#cb639-5)}
```

#### 28.5.9.2 Example: `invert(object)`

[`invert`](https://underscorejs.org/#invert) returns a copy of `object` where the keys and values of all properties are swapped:

```
[](#cb640-1)assert.deepEqual(
[](#cb640-2)  invert({a: 1, b: 2, c: 3}),
[](#cb640-3)  {1: 'a', 2: 'b', 3: 'c'}
[](#cb640-4));
```

We can implement `invert()` like this:

```
[](#cb641-1)function invert(object) {
[](#cb641-2)  const mappedEntries = Object.entries(object)
[](#cb641-3)    .map(([key, value]) => [value, key]);
[](#cb641-4)  return Object.fromEntries(mappedEntries);
[](#cb641-5)}
```

#### 28.5.9.3 A simple implementation of `Object.fromEntries()`

The following function is a simplified version of `Object.fromEntries()`:

```
[](#cb642-1)function fromEntries(iterable) {
[](#cb642-2)  const result = {};
[](#cb642-3)  for (const [key, value] of iterable) {
[](#cb642-4)    let coercedKey;
[](#cb642-5)    if (typeof key === 'string' || typeof key === 'symbol') {
[](#cb642-6)      coercedKey = key;
[](#cb642-7)    } else {
[](#cb642-8)      coercedKey = String(key);
[](#cb642-9)    }
[](#cb642-10)    result[coercedKey] = value;
[](#cb642-11)  }
[](#cb642-12)  return result;
[](#cb642-13)}
```

#### 28.5.9.4 A polyfill for `Object.fromEntries()`

[The npm package `object.fromentries`](https://github.com/es-shims/Object.fromEntries) is [a *polyfill*](#ch028.xhtml_polyfills) for `Object.entries()`: it installs its own implementation if that method doesn’t exist on the current platform.

![](media/file6.svg)  **Exercise: `Object.entries()` and `Object.fromEntries()`**

`exercises/single-objects/omit_properties_test.mjs`

### 28.5.10 The pitfalls of using an object as a dictionary

If you use plain objects (created via object literals) as dictionaries, you have to look out for two pitfalls.

The first pitfall is that the `in` operator also finds inherited properties:

```
[](#cb643-1)const dict = {};
[](#cb643-2)assert.equal('toString' in dict, true);
```

We want `dict` to be treated as empty, but the `in` operator detects the properties it inherits from its prototype, `Object.prototype`.

The second pitfall is that you can’t use the property key `__proto__` because it has special powers (it sets the prototype of the object):

```
[](#cb644-1)const dict = {};
[](#cb644-2)
[](#cb644-3)dict['__proto__'] = 123;
[](#cb644-4)// No property was added to dict:
[](#cb644-5)assert.deepEqual(Object.keys(dict), []);
```

So how do we avoid these pitfalls?

*   Whenever you can, use Maps. They are the best solution for dictionaries.
*   If you can’t, use a library for objects-as-dictionaries that does everything safely.
*   If you can’t, use an object without a prototype.

The following code demonstrates using objects without prototypes as dictionaries:

```
[](#cb645-1)const dict = Object.create(null); // no prototype
[](#cb645-2)
[](#cb645-3)assert.equal('toString' in dict, false); // (A)
[](#cb645-4)
[](#cb645-5)dict['__proto__'] = 123;
[](#cb645-6)assert.deepEqual(Object.keys(dict), ['__proto__']);
```

We avoided both pitfalls: First, a property without a prototype does not inherit any properties (line A). Second, in modern JavaScript, `__proto__` is implemented via `Object.prototype`. That means that it is switched off if `Object.prototype` is not in the prototype chain.

![](media/file6.svg)  **Exercise: Using an object as a dictionary**

`exercises/single-objects/simple_dict_test.mjs`

## 28.6 Standard methods (advanced)

`Object.prototype` defines several standard methods that can be overridden to configure how an object is treated by the language. Two important ones are:

*   `.toString()`
*   `.valueOf()`

### 28.6.1 `.toString()`

`.toString()` determines how objects are converted to strings:

```
> String({toString() { return 'Hello!' }})
'Hello!'
> String({})
'[object Object]'
```

### 28.6.2 `.valueOf()`

`.valueOf()` determines how objects are converted to numbers:

```
> Number({valueOf() { return 123 }})
123
> Number({})
NaN
```

## 28.7 Advanced topics

The following subsections give brief overviews of a few advanced topics.

### 28.7.1 `Object.assign()`

`Object.assign()` is a tool method:

```
[](#cb648-1)Object.assign(target, source_1, source_2, ···)
```

This expression assigns all properties of `source_1` to `target`, then all properties of `source_2`, etc. At the end, it returns `target` – for example:

```
[](#cb649-1)const target = { foo: 1 };
[](#cb649-2)
[](#cb649-3)const result = Object.assign(
[](#cb649-4)  target,
[](#cb649-5)  {bar: 2},
[](#cb649-6)  {baz: 3, bar: 4});
[](#cb649-7)
[](#cb649-8)assert.deepEqual(
[](#cb649-9)  result, { foo: 1, bar: 4, baz: 3 });
[](#cb649-10)// target was modified and returned:
[](#cb649-11)assert.equal(result, target);
```

The use cases for `Object.assign()` are similar to those for spread properties. In a way, it spreads destructively.

### 28.7.2 Freezing objects

`Object.freeze(obj)` makes `obj` completely immutable: You can’t change properties, add properties, or change its prototype – for example:

```
[](#cb650-1)const frozen = Object.freeze({ x: 2, y: 5 });
[](#cb650-2)assert.throws(
[](#cb650-3)  () => { frozen.x = 7 },
[](#cb650-4)  {
[](#cb650-5)    name: 'TypeError',
[](#cb650-6)    message: /^Cannot assign to read only property 'x'/,
[](#cb650-7)  });
```

There is one caveat: `Object.freeze(obj)` freezes shallowly. That is, only the properties of `obj` are frozen but not objects stored in properties.

### 28.7.3 Property attributes and property descriptors

Just as objects are composed of properties, properties are composed of *attributes*. The value of a property is only one of several attributes. Others include:

*   `writable`: Is it possible to change the value of the property?
*   `enumerable`: Is the property considered by `Object.keys()`, spreading, etc.?

When you are using one of the operations for handling property attributes, attributes are specified via *property descriptors*: objects where each property represents one attribute. For example, this is how you read the attributes of a property `obj.foo`:

```
[](#cb651-1)const obj = { foo: 123 };
[](#cb651-2)assert.deepEqual(
[](#cb651-3)  Object.getOwnPropertyDescriptor(obj, 'foo'),
[](#cb651-4)  {
[](#cb651-5)    value: 123,
[](#cb651-6)    writable: true,
[](#cb651-7)    enumerable: true,
[](#cb651-8)    configurable: true,
[](#cb651-9)  });
```

And this is how you set the attributes of a property `obj.bar`:

```
[](#cb652-1)const obj = {
[](#cb652-2)  foo: 1,
[](#cb652-3)  bar: 2,
[](#cb652-4)};
[](#cb652-5)
[](#cb652-6)assert.deepEqual(Object.keys(obj), ['foo', 'bar']);
[](#cb652-7)
[](#cb652-8)// Hide property `bar` from Object.keys()
[](#cb652-9)Object.defineProperty(obj, 'bar', {
[](#cb652-10)  enumerable: false,
[](#cb652-11)});
[](#cb652-12)
[](#cb652-13)assert.deepEqual(Object.keys(obj), ['foo']);
```

Enumerability is covered in greater detail [earlier in this chapter](#ch029.xhtml_enumerability). For more information on property attributes and property descriptors, consult [*Speaking JavaScript*](http://speakingjs.com/es5/ch17.html#property_attributes).

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 29 Prototype chains and classes

* * *

*   29.1 [Prototype chains](#ch030.xhtml_prototype-chains)
    *   29.1.1 [JavaScript’s operations: all properties vs. own properties](#ch030.xhtml_javascripts-operations-all-properties-vs.-own-properties)
    *   29.1.2 [Pitfall: only the first member of a prototype chain is mutated](#ch030.xhtml_pitfall-only-the-first-member-of-a-prototype-chain-is-mutated)
    *   29.1.3 [Tips for working with prototypes (advanced)](#ch030.xhtml_tips-for-working-with-prototypes-advanced)
    *   29.1.4 [Sharing data via prototypes](#ch030.xhtml_sharing-data-via-prototypes)
*   29.2 [Classes](#ch030.xhtml_classes)
    *   29.2.1 [A class for persons](#ch030.xhtml_a-class-for-persons)
    *   29.2.2 [Classes under the hood](#ch030.xhtml_classes-under-the-hood)
    *   29.2.3 [Class definitions: prototype properties](#ch030.xhtml_class-definitions-prototype-properties)
    *   29.2.4 [Class definitions: static properties](#ch030.xhtml_class-definitions-static-properties)
    *   29.2.5 [The `instanceof` operator](#ch030.xhtml_the-instanceof-operator)
    *   29.2.6 [Why I recommend classes](#ch030.xhtml_why-i-recommend-classes)
*   29.3 [Private data for classes](#ch030.xhtml_private-data-for-classes)
    *   29.3.1 [Private data: naming convention](#ch030.xhtml_private-data-naming-convention)
    *   29.3.2 [Private data: WeakMaps](#ch030.xhtml_private-data-weakmaps)
    *   29.3.3 [More techniques for private data](#ch030.xhtml_more-techniques-for-private-data)
*   29.4 [Subclassing](#ch030.xhtml_subclassing)
    *   29.4.1 [Subclasses under the hood (advanced)](#ch030.xhtml_subclasses-under-the-hood-advanced)
    *   29.4.2 [`instanceof` in more detail (advanced)](#ch030.xhtml_instanceof-operator)
    *   29.4.3 [Prototype chains of built-in objects (advanced)](#ch030.xhtml_prototype-chains-of-built-in-objects-advanced)
    *   29.4.4 [Dispatched vs. direct method calls (advanced)](#ch030.xhtml_dispatched-vs.-direct-method-calls-advanced)
    *   29.4.5 [Mixin classes (advanced)](#ch030.xhtml_mixin-classes-advanced)
*   29.5 [FAQ: objects](#ch030.xhtml_faq-objects)
    *   29.5.1 [Why do objects preserve the insertion order of properties?](#ch030.xhtml_why-do-objects-preserve-the-insertion-order-of-properties)

* * *

In this book, JavaScript’s style of object-oriented programming (OOP) is introduced in four steps. This chapter covers steps 2–4, [the previous chapter](#ch029.xhtml_ch_single-objects) covers step 1\. The steps are (fig. [18](#ch030.xhtml_fig:oop_steps2)):

1.  **Single objects (previous chapter):** How do *objects*, JavaScript’s basic OOP building blocks, work in isolation?
2.  **Prototype chains (this chapter):** Each object has a chain of zero or more *prototype objects*. Prototypes are JavaScript’s core inheritance mechanism.
3.  **Classes (this chapter):** JavaScript’s *classes* are factories for objects. The relationship between a class and its instances is based on prototypal inheritance.
4.  **Subclassing (this chapter):** The relationship between a *subclass* and its *superclass* is also based on prototypal inheritance.

![](media/file27.svg)

Figure 18: This book introduces object-oriented programming in JavaScript in four steps.

## 29.1 Prototype chains

Prototypes are JavaScript’s only inheritance mechanism: each object has a prototype that is either `null` or an object. In the latter case, the object inherits all of the prototype’s properties.

In an object literal, you can set the prototype via the special property `__proto__`:

```
[](#cb653-1)const proto = {
[](#cb653-2)  protoProp: 'a',
[](#cb653-3)};
[](#cb653-4)const obj = {
[](#cb653-5)  __proto__: proto,
[](#cb653-6)  objProp: 'b',
[](#cb653-7)};
[](#cb653-8)
[](#cb653-9)// obj inherits .protoProp:
[](#cb653-10)assert.equal(obj.protoProp, 'a');
[](#cb653-11)assert.equal('protoProp' in obj, true);
```

Given that a prototype object can have a prototype itself, we get a chain of objects – the so-called *prototype chain*. That means that inheritance gives us the impression that we are dealing with single objects, but we are actually dealing with chains of objects.

Fig. [19](#ch030.xhtml_fig:oo_proto_chain) shows what the prototype chain of `obj` looks like.

![](media/file28.svg)

Figure 19: `obj` starts a chain of objects that continues with `proto` and other objects.

Non-inherited properties are called *own properties*. `obj` has one own property, `.objProp`.

### 29.1.1 JavaScript’s operations: all properties vs. own properties

Some operations consider all properties (own and inherited) – for example, getting properties:

```
> const obj = { foo: 1 };
> typeof obj.foo // own
'number'
> typeof obj.toString // inherited
'function'
```

Other operations only consider own properties – for example, `Object.keys()`:

```
> Object.keys(obj)
[ 'foo' ]
```

Read on for another operation that also only considers own properties: setting properties.

### 29.1.2 Pitfall: only the first member of a prototype chain is mutated

One aspect of prototype chains that may be counter-intuitive is that setting *any* property via an object – even an inherited one – only changes that very object – never one of the prototypes.

Consider the following object `obj`:

```
[](#cb656-1)const proto = {
[](#cb656-2)  protoProp: 'a',
[](#cb656-3)};
[](#cb656-4)const obj = {
[](#cb656-5)  __proto__: proto,
[](#cb656-6)  objProp: 'b',
[](#cb656-7)};
```

In the next code snippet, we set the inherited property `obj.protoProp` (line A). That “changes” it by creating an own property: When reading `obj.protoProp`, the own property is found first and its value *overrides* the value of the inherited property.

```
[](#cb657-1)// In the beginning, obj has one own property
[](#cb657-2)assert.deepEqual(Object.keys(obj), ['objProp']);
[](#cb657-3)
[](#cb657-4)obj.protoProp = 'x'; // (A)
[](#cb657-5)
[](#cb657-6)// We created a new own property:
[](#cb657-7)assert.deepEqual(Object.keys(obj), ['objProp', 'protoProp']);
[](#cb657-8)
[](#cb657-9)// The inherited property itself is unchanged:
[](#cb657-10)assert.equal(proto.protoProp, 'a');
[](#cb657-11)
[](#cb657-12)// The own property overrides the inherited property:
[](#cb657-13)assert.equal(obj.protoProp, 'x');
```

The prototype chain of `obj` is depicted in fig. [20](#ch030.xhtml_fig:oo_overriding).

![](media/file29.svg)

Figure 20: The own property `.protoProp` of `obj` overrides the property inherited from `proto`.

### 29.1.3 Tips for working with prototypes (advanced)

#### 29.1.3.1 Best practice: avoid `__proto__`, except in object literals

I recommend to avoid the pseudo-property `__proto__`: As we will see [later](#ch030.xhtml_proto), not all objects have it.

However, `__proto__` in object literals is different. There, it is a built-in feature and always available.

The recommended ways of getting and setting prototypes are:

*   The best way to get a prototype is via the following method:

    ```
    [](#cb658-1)Object.getPrototypeOf(obj: Object) : Object
    ```

*   The best way to set a prototype is when creating an object – via `__proto__` in an object literal or via:

    ```
    [](#cb659-1)Object.create(proto: Object) : Object
    ```

    If you have to, you can use `Object.setPrototypeOf()` to change the prototype of an existing object. But that may affect performance negatively.

This is how these features are used:

```
[](#cb660-1)const proto1 = {};
[](#cb660-2)const proto2 = {};
[](#cb660-3)
[](#cb660-4)const obj = Object.create(proto1);
[](#cb660-5)assert.equal(Object.getPrototypeOf(obj), proto1);
[](#cb660-6)
[](#cb660-7)Object.setPrototypeOf(obj, proto2);
[](#cb660-8)assert.equal(Object.getPrototypeOf(obj), proto2);
```

#### 29.1.3.2 Check: is an object a prototype of another one?

So far, “`p` is a prototype of `o`” always meant “`p` is a *direct* prototype of `o`”. But it can also be used more loosely and mean that `p` is in the prototype chain of `o`. That looser relationship can be checked via:

```
[](#cb661-1)p.isPrototypeOf(o)
```

For example:

```
[](#cb662-1)const a = {};
[](#cb662-2)const b = {__proto__: a};
[](#cb662-3)const c = {__proto__: b};
[](#cb662-4)
[](#cb662-5)assert.equal(a.isPrototypeOf(b), true);
[](#cb662-6)assert.equal(a.isPrototypeOf(c), true);
[](#cb662-7)
[](#cb662-8)assert.equal(a.isPrototypeOf(a), false);
[](#cb662-9)assert.equal(c.isPrototypeOf(a), false);
```

### 29.1.4 Sharing data via prototypes

Consider the following code:

```
[](#cb663-1)const jane = {
[](#cb663-2)  name: 'Jane',
[](#cb663-3)  describe() {
[](#cb663-4)    return 'Person named '+this.name;
[](#cb663-5)  },
[](#cb663-6)};
[](#cb663-7)const tarzan = {
[](#cb663-8)  name: 'Tarzan',
[](#cb663-9)  describe() {
[](#cb663-10)    return 'Person named '+this.name;
[](#cb663-11)  },
[](#cb663-12)};
[](#cb663-13)
[](#cb663-14)assert.equal(jane.describe(), 'Person named Jane');
[](#cb663-15)assert.equal(tarzan.describe(), 'Person named Tarzan');
```

We have two objects that are very similar. Both have two properties whose names are `.name` and `.describe`. Additionally, method `.describe()` is the same. How can we avoid duplicating that method?

We can move it to an object `PersonProto` and make that object a prototype of both `jane` and `tarzan`:

```
[](#cb664-1)const PersonProto = {
[](#cb664-2)  describe() {
[](#cb664-3)    return 'Person named ' + this.name;
[](#cb664-4)  },
[](#cb664-5)};
[](#cb664-6)const jane = {
[](#cb664-7)  __proto__: PersonProto,
[](#cb664-8)  name: 'Jane',
[](#cb664-9)};
[](#cb664-10)const tarzan = {
[](#cb664-11)  __proto__: PersonProto,
[](#cb664-12)  name: 'Tarzan',
[](#cb664-13)};
```

The name of the prototype reflects that both `jane` and `tarzan` are persons.

![](media/file30.svg)

Figure 21: Objects `jane` and `tarzan` share method `.describe()`, via their common prototype `PersonProto`.

Fig. [21](#ch030.xhtml_fig:oo_person_shared) illustrates how the three objects are connected: The objects at the bottom now contain the properties that are specific to `jane` and `tarzan`. The object at the top contains the properties that are shared between them.

When you make the method call `jane.describe()`, `this` points to the receiver of that method call, `jane` (in the bottom-left corner of the diagram). That’s why the method still works. `tarzan.describe()` works similarly.

```
[](#cb665-1)assert.equal(jane.describe(), 'Person named Jane');
[](#cb665-2)assert.equal(tarzan.describe(), 'Person named Tarzan');
```

## 29.2 Classes

We are now ready to take on classes, which are basically a compact syntax for setting up prototype chains. Under the hood, JavaScript’s classes are unconventional. But that is something you rarely see when working with them. They should normally feel familiar to people who have used other object-oriented programming languages.

### 29.2.1 A class for persons

We have previously worked with `jane` and `tarzan`, single objects representing persons. Let’s use a *class declaration* to implement a factory for person objects:

```
[](#cb666-1)class Person {
[](#cb666-2)  constructor(name) {
[](#cb666-3)    this.name = name;
[](#cb666-4)  }
[](#cb666-5)  describe() {
[](#cb666-6)    return 'Person named '+this.name;
[](#cb666-7)  }
[](#cb666-8)}
```

`jane` and `tarzan` can now be created via `new Person()`:

```
[](#cb667-1)const jane = new Person('Jane');
[](#cb667-2)assert.equal(jane.name, 'Jane');
[](#cb667-3)assert.equal(jane.describe(), 'Person named Jane');
[](#cb667-4)
[](#cb667-5)const tarzan = new Person('Tarzan');
[](#cb667-6)assert.equal(tarzan.name, 'Tarzan');
[](#cb667-7)assert.equal(tarzan.describe(), 'Person named Tarzan');
```

Class `Person` has two methods:

*   The normal method `.describe()`
*   The special method `.constructor()` which is called directly after a new instance has been created and initializes that instance. It receives the arguments that are passed to the `new` operator (after the class name). If you don’t need any arguments to set up a new instance, you can omit the constructor.

#### 29.2.1.1 Class expressions

There are two kinds of *class definitions* (ways of defining classes):

*   *Class declarations*, which we have seen in the previous section.
*   *Class expressions*, which we’ll see next.

Class expressions can be anonymous and named:

```
[](#cb668-1)// Anonymous class expression
[](#cb668-2)const Person = class { ··· };
[](#cb668-3)
[](#cb668-4)// Named class expression
[](#cb668-5)const Person = class MyClass { ··· };
```

The name of a named class expression works similarly to [the name of a named function expression](#ch026.xhtml_names-of-ordinary-functions).

This was a first look at classes. We’ll explore more features soon, but first we need to learn the internals of classes.

### 29.2.2 Classes under the hood

There is a lot going on under the hood of classes. Let’s look at the diagram for `jane` (fig. [22](#ch030.xhtml_fig:oo_person_class)).

![](media/file31.svg)

Figure 22: The class `Person` has the property `.prototype` that points to an object that is the prototype of all instances of `Person`. `jane` is one such instance.

The main purpose of class `Person` is to set up the prototype chain on the right (`jane`, followed by `Person.prototype`). It is interesting to note that both constructs inside class `Person` (`.constructor` and `.describe()`) created properties for `Person.prototype`, not for `Person`.

The reason for this slightly odd approach is backward compatibility: prior to classes, *constructor functions* ([ordinary functions](#ch026.xhtml_roles-of-ordinary-functions), invoked via the `new` operator) were often used as factories for objects. Classes are mostly better syntax for constructor functions and therefore remain compatible with old code. That explains why classes are functions:

```
> typeof Person
'function'
```

In this book, I use the terms *constructor (function)* and *class* interchangeably.

It is easy to confuse `.__proto__` and `.prototype`. Hopefully, fig. [22](#ch030.xhtml_fig:oo_person_class) makes it clear how they differ:

*   `.__proto__` is a pseudo-property for accessing the prototype of an object.
*   `.prototype` is a normal property that is only special due to how the `new` operator uses it. The name is not ideal: `Person.prototype` does not point to the prototype of `Person`, it points to the prototype of all instances of `Person`.

#### 29.2.2.1 `Person.prototype.constructor` (advanced)

There is one detail in fig. [22](#ch030.xhtml_fig:oo_person_class) that we haven’t looked at, yet: `Person.prototype.constructor` points back to `Person`:

```
> Person.prototype.constructor === Person
true
```

This setup also exists due to backward compatibility. But it has two additional benefits.

First, each instance of a class inherits property `.constructor`. Therefore, given an instance, you can make “similar” objects using it:

```
[](#cb671-1)const jane = new Person('Jane');
[](#cb671-2)
[](#cb671-3)const cheeta = new jane.constructor('Cheeta');
[](#cb671-4)// cheeta is also an instance of Person
[](#cb671-5)// (the instanceof operator is explained later)
[](#cb671-6)assert.equal(cheeta instanceof Person, true);
```

Second, you can get the name of the class that created a given instance:

```
[](#cb672-1)const tarzan = new Person('Tarzan');
[](#cb672-2)
[](#cb672-3)assert.equal(tarzan.constructor.name, 'Person');
```

### 29.2.3 Class definitions: prototype properties

All constructs in the body of the following class declaration create properties of `Foo.prototype`.

```
[](#cb673-1)class Foo {
[](#cb673-2)  constructor(prop) {
[](#cb673-3)    this.prop = prop;
[](#cb673-4)  }
[](#cb673-5)  protoMethod() {
[](#cb673-6)    return 'protoMethod';
[](#cb673-7)  }
[](#cb673-8)  get protoGetter() {
[](#cb673-9)    return 'protoGetter';
[](#cb673-10)  }
[](#cb673-11)}
```

Let’s examine them in order:

*   `.constructor()` is called after creating a new instance of `Foo` to set up that instance.
*   `.protoMethod()` is a normal method. It is stored in `Foo.prototype`.
*   `.protoGetter` is a getter that is stored in `Foo.prototype`.

The following interaction uses class `Foo`:

```
> const foo = new Foo(123);
> foo.prop
123

> foo.protoMethod()
'protoMethod'
> foo.protoGetter
'protoGetter'
```

### 29.2.4 Class definitions: static properties

All constructs in the body of the following class declaration create so-called *static* properties – properties of `Bar` itself.

```
[](#cb675-1)class Bar {
[](#cb675-2)  static staticMethod() {
[](#cb675-3)    return 'staticMethod';
[](#cb675-4)  }
[](#cb675-5)  static get staticGetter() {
[](#cb675-6)    return 'staticGetter';
[](#cb675-7)  }
[](#cb675-8)}
```

The static method and the static getter are used as follows:

```
> Bar.staticMethod()
'staticMethod'
> Bar.staticGetter
'staticGetter'
```

### 29.2.5 The `instanceof` operator

The `instanceof` operator tells you if a value is an instance of a given class:

```
> new Person('Jane') instanceof Person
true
> ({}) instanceof Person
false
> ({}) instanceof Object
true
> [] instanceof Array
true
```

We’ll explore the `instanceof` operator in more detail [later](#ch030.xhtml_instanceof-operator), after we have looked at subclassing.

### 29.2.6 Why I recommend classes

I recommend using classes for the following reasons:

*   Classes are a common standard for object creation and inheritance that is now widely supported across frameworks (React, Angular, Ember, etc.). This is an improvement to how things were before, when almost every framework had its own inheritance library.

*   They help tools such as IDEs and type checkers with their work and enable new features there.

*   If you come from another language to JavaScript and are used to classes, then you can get started more quickly.

*   JavaScript engines optimize them. That is, code that uses classes is almost always faster than code that uses a custom inheritance library.

*   You can subclass built-in constructor functions such as `Error`.

That doesn’t mean that classes are perfect:

*   There is a risk of overdoing inheritance.

*   There is a risk of putting too much functionality in classes (when some of it is often better put in functions).

*   How they work superficially and under the hood is quite different. In other words, there is a disconnect between syntax and semantics. Two examples are:

    *   A method definition inside a class `C` creates a method in the object `C.prototype`.
    *   Classes are functions.

    The motivation for the disconnect is backward compatibility. Thankfully, the disconnect causes few problems in practice; you are usually OK if you go along with what classes pretend to be.

![](media/file6.svg)  **Exercise: Writing a class**

`exercises/proto-chains-classes/point_class_test.mjs`

## 29.3 Private data for classes

This section describes techniques for hiding some of the data of an object from the outside. We discuss them in the context of classes, but they also work for objects created directly, e.g., via object literals.

### 29.3.1 Private data: naming convention

The first technique makes a property private by prefixing its name with an underscore. This doesn’t protect the property in any way; it merely signals to the outside: “You don’t need to know about this property.”

In the following code, the properties `._counter` and `._action` are private.

```
[](#cb678-1)class Countdown {
[](#cb678-2)  constructor(counter, action) {
[](#cb678-3)    this._counter = counter;
[](#cb678-4)    this._action = action;
[](#cb678-5)  }
[](#cb678-6)  dec() {
[](#cb678-7)    this._counter--;
[](#cb678-8)    if (this._counter === 0) {
[](#cb678-9)      this._action();
[](#cb678-10)    }
[](#cb678-11)  }
[](#cb678-12)}
[](#cb678-13)
[](#cb678-14)// The two properties aren’t really private:
[](#cb678-15)assert.deepEqual(
[](#cb678-16)  Object.keys(new Countdown()),
[](#cb678-17)  ['_counter', '_action']);
```

With this technique, you don’t get any protection and private names can clash. On the plus side, it is easy to use.

### 29.3.2 Private data: WeakMaps

Another technique is to use WeakMaps. How exactly that works is explained [in the chapter on WeakMaps](#ch035.xhtml_private-data-in-weakmaps). This is a preview:

```
[](#cb679-1)const _counter = new WeakMap();
[](#cb679-2)const _action = new WeakMap();
[](#cb679-3)
[](#cb679-4)class Countdown {
[](#cb679-5)  constructor(counter, action) {
[](#cb679-6)    _counter.set(this, counter);
[](#cb679-7)    _action.set(this, action);
[](#cb679-8)  }
[](#cb679-9)  dec() {
[](#cb679-10)    let counter = _counter.get(this);
[](#cb679-11)    counter--;
[](#cb679-12)    _counter.set(this, counter);
[](#cb679-13)    if (counter === 0) {
[](#cb679-14)      _action.get(this)();
[](#cb679-15)    }
[](#cb679-16)  }
[](#cb679-17)}
[](#cb679-18)
[](#cb679-19)// The two pseudo-properties are truly private:
[](#cb679-20)assert.deepEqual(
[](#cb679-21)  Object.keys(new Countdown()),
[](#cb679-22)  []);
```

This technique offers you considerable protection from outside access and there can’t be any name clashes. But it is also more complicated to use.

### 29.3.3 More techniques for private data

This book explains the most important techniques for private data in classes. There will also probably soon be built-in support for it. Consult the ECMAScript proposal [“Class Public Instance Fields & Private Instance Fields”](https://github.com/tc39/proposal-class-fields) for details.

A few additional techniques are explained in [*Exploring ES6*](https://exploringjs.com/es6/ch_classes.html#sec_private-data-for-classes).

## 29.4 Subclassing

Classes can also subclass (“extend”) existing classes. As an example, the following class `Employee` subclasses `Person`:

```
[](#cb680-1)class Person {
[](#cb680-2)  constructor(name) {
[](#cb680-3)    this.name = name;
[](#cb680-4)  }
[](#cb680-5)  describe() {
[](#cb680-6)    return `Person named ${this.name}`;
[](#cb680-7)  }
[](#cb680-8)  static logNames(persons) {
[](#cb680-9)    for (const person of persons) {
[](#cb680-10)      console.log(person.name);
[](#cb680-11)    }
[](#cb680-12)  }
[](#cb680-13)}
[](#cb680-14)
[](#cb680-15)class Employee extends Person {
[](#cb680-16)  constructor(name, title) {
[](#cb680-17)    super(name);
[](#cb680-18)    this.title = title;
[](#cb680-19)  }
[](#cb680-20)  describe() {
[](#cb680-21)    return super.describe() +
[](#cb680-22)      ` (${this.title})`;
[](#cb680-23)  }
[](#cb680-24)}
[](#cb680-25)
[](#cb680-26)const jane = new Employee('Jane', 'CTO');
[](#cb680-27)assert.equal(
[](#cb680-28)  jane.describe(),
[](#cb680-29)  'Person named Jane (CTO)');
```

Two comments:

*   Inside a `.constructor()` method, you must call the super-constructor via `super()` before you can access `this`. That’s because `this` doesn’t exist before the super-constructor is called (this phenomenon is specific to classes).

*   Static methods are also inherited. For example, `Employee` inherits the static method `.logNames()`:

    ```
    > 'logNames' in Employee
    true
    ```

![](media/file6.svg)  **Exercise: Subclassing**

`exercises/proto-chains-classes/color_point_class_test.mjs`

### 29.4.1 Subclasses under the hood (advanced)

![](media/file32.svg)

Figure 23: These are the objects that make up class `Person` and its subclass, `Employee`. The left column is about classes. The right column is about the `Employee` instance `jane` and its prototype chain.

The classes `Person` and `Employee` from the previous section are made up of several objects (fig. [23](#ch030.xhtml_fig:oo_subclassing)). One key insight for understanding how these objects are related is that there are two prototype chains:

*   The instance prototype chain, on the right.
*   The class prototype chain, on the left.

#### 29.4.1.1 The instance prototype chain (right column)

The instance prototype chain starts with `jane` and continues with `Employee.prototype` and `Person.prototype`. In principle, the prototype chain ends at this point, but we get one more object: `Object.prototype`. This prototype provides services to virtually all objects, which is why it is included here, too:

```
> Object.getPrototypeOf(Person.prototype) === Object.prototype
true
```

#### 29.4.1.2 The class prototype chain (left column)

In the class prototype chain, `Employee` comes first, `Person` next. Afterward, the chain continues with `Function.prototype`, which is only there because `Person` is a function and functions need the services of `Function.prototype`.

```
> Object.getPrototypeOf(Person) === Function.prototype
true
```

### 29.4.2 `instanceof` in more detail (advanced)

We have not yet seen how `instanceof` really works. Given the expression:

```
[](#cb684-1)x instanceof C
```

How does `instanceof` determine if `x` is an instance of `C` (or a subclass of `C`)? It does so by checking if `C.prototype` is in the prototype chain of `x`. That is, the following expression is equivalent:

```
[](#cb685-1)C.prototype.isPrototypeOf(x)
```

If we go back to fig. [23](#ch030.xhtml_fig:oo_subclassing), we can confirm that the prototype chain does lead us to the following correct answers:

```
> jane instanceof Employee
true
> jane instanceof Person
true
> jane instanceof Object
true
```

### 29.4.3 Prototype chains of built-in objects (advanced)

Next, we’ll use our knowledge of subclassing to understand the prototype chains of a few built-in objects. The following tool function `p()` helps us with our explorations.

```
[](#cb687-1)const p = Object.getPrototypeOf.bind(Object);
```

We extracted method `.getPrototypeOf()` of `Object` and assigned it to `p`.

#### 29.4.3.1 The prototype chain of `{}`

Let’s start by examining plain objects:

```
> p({}) === Object.prototype
true
> p(p({})) === null
true
```

![](media/file33.svg)

Figure 24: The prototype chain of an object created via an object literal starts with that object, continues with `Object.prototype`, and ends with `null`.

Fig. [24](#ch030.xhtml_fig:proto_chain_object) shows a diagram for this prototype chain. We can see that `{}` really is an instance of `Object` – `Object.prototype` is in its prototype chain.

#### 29.4.3.2 The prototype chain of `[]`

What does the prototype chain of an Array look like?

```
> p([]) === Array.prototype
true
> p(p([])) === Object.prototype
true
> p(p(p([]))) === null
true
```

![](media/file34.svg)

Figure 25: The prototype chain of an Array has these members: the Array instance, `Array.prototype`, `Object.prototype`, `null`.

This prototype chain (visualized in fig. [25](#ch030.xhtml_fig:proto_chain_array)) tells us that an Array object is an instance of `Array`, which is a subclass of `Object`.

#### 29.4.3.3 The prototype chain of `function () {}`

Lastly, the prototype chain of an ordinary function tells us that all functions are objects:

```
> p(function () {}) === Function.prototype
true
> p(p(function () {})) === Object.prototype
true
```

#### 29.4.3.4 Objects that aren’t instances of `Object`

An object is only an instance of `Object` if `Object.prototype` is in its prototype chain. Most objects created via various literals are instances of `Object`:

```
> ({}) instanceof Object
true
> (() => {}) instanceof Object
true
> /abc/ug instanceof Object
true
```

Objects that don’t have prototypes are not instances of `Object`:

```
> ({ __proto__: null }) instanceof Object
false
```

`Object.prototype` ends most prototype chains. Its prototype is `null`, which means it isn’t an instance of `Object` either:

```
> Object.prototype instanceof Object
false
```

#### 29.4.3.5 How exactly does the pseudo-property `.__proto__` work?

The pseudo-property `.__proto__` is implemented by class `Object` via a getter and a setter. It could be implemented like this:

```
[](#cb694-1)class Object {
[](#cb694-2)  get __proto__() {
[](#cb694-3)    return Object.getPrototypeOf(this);
[](#cb694-4)  }
[](#cb694-5)  set __proto__(other) {
[](#cb694-6)    Object.setPrototypeOf(this, other);
[](#cb694-7)  }
[](#cb694-8)  // ···
[](#cb694-9)}
```

That means that you can switch `.__proto__` off by creating an object that doesn’t have `Object.prototype` in its prototype chain (see the previous section):

```
> '__proto__' in {}
true
> '__proto__' in { __proto__: null }
false
```

### 29.4.4 Dispatched vs. direct method calls (advanced)

Let’s examine how method calls work with classes. We are revisiting `jane` from earlier:

```
[](#cb696-1)class Person {
[](#cb696-2)  constructor(name) {
[](#cb696-3)    this.name = name;
[](#cb696-4)  }
[](#cb696-5)  describe() {
[](#cb696-6)    return 'Person named '+this.name;
[](#cb696-7)  }
[](#cb696-8)}
[](#cb696-9)const jane = new Person('Jane');
```

Fig. [26](#ch030.xhtml_fig:jane_proto_chain) has a diagram with `jane`’s prototype chain.

![](media/file35.svg)

Figure 26: The prototype chain of `jane` starts with `jane` and continues with `Person.prototype`.

Normal method calls are *dispatched* – the method call `jane.describe()` happens in two steps:

*   Dispatch: In the prototype chain of `jane`, find the first property whose key is `'describe'` and retrieve its value.

    ```
    [](#cb697-1)const func = jane.describe;
    ```

*   Call: Call the value, while setting `this` to `jane`.

    ```
    [](#cb698-1)func.call(jane);
    ```

This way of dynamically looking for a method and invoking it is called *dynamic dispatch*.

You can make the same method call *directly*, without dispatching:

```
[](#cb699-1)Person.prototype.describe.call(jane)
```

This time, we directly point to the method via `Person.prototype.describe` and don’t search for it in the prototype chain. We also specify `this` differently via `.call()`.

Note that `this` always points to the beginning of a prototype chain. That enables `.describe()` to access `.name`.

#### 29.4.4.1 Borrowing methods

Direct method calls become useful when you are working with methods of `Object.prototype`. For example, `Object.prototype.hasOwnProperty(k)` checks if `this` has a non-inherited property whose key is `k`:

```
> const obj = { foo: 123 };
> obj.hasOwnProperty('foo')
true
> obj.hasOwnProperty('bar')
false
```

However, in the prototype chain of an object, there may be another property with the key `'hasOwnProperty'` that overrides the method in `Object.prototype`. Then a dispatched method call doesn’t work:

```
> const obj = { hasOwnProperty: true };
> obj.hasOwnProperty('bar')
TypeError: obj.hasOwnProperty is not a function
```

The workaround is to use a direct method call:

```
> Object.prototype.hasOwnProperty.call(obj, 'bar')
false
> Object.prototype.hasOwnProperty.call(obj, 'hasOwnProperty')
true
```

This kind of direct method call is often abbreviated as follows:

```
> ({}).hasOwnProperty.call(obj, 'bar')
false
> ({}).hasOwnProperty.call(obj, 'hasOwnProperty')
true
```

This pattern may seem inefficient, but most engines optimize this pattern, so performance should not be an issue.

### 29.4.5 Mixin classes (advanced)

JavaScript’s class system only supports *single inheritance*. That is, each class can have at most one superclass. One way around this limitation is via a technique called *mixin classes* (short: *mixins*).

The idea is as follows: Let’s say we want a class `C` to inherit from two superclasses `S1` and `S2`. That would be *multiple inheritance*, which JavaScript doesn’t support.

Our workaround is to turn `S1` and `S2` into *mixins*, factories for subclasses:

```
[](#cb704-1)const S1 = (Sup) => class extends Sup { /*···*/ };
[](#cb704-2)const S2 = (Sup) => class extends Sup { /*···*/ };
```

Each of these two functions returns a class that extends a given superclass `Sup`. We create class `C` as follows:

```
[](#cb705-1)class C extends S2(S1(Object)) {
[](#cb705-2)  /*···*/
[](#cb705-3)}
```

We now have a class `C` that extends a class `S2` that extends a class `S1` that extends `Object` (which most classes do implicitly).

#### 29.4.5.1 Example: a mixin for brand management

We implement a mixin `Branded` that has helper methods for setting and getting the brand of an object:

```
[](#cb706-1)const Branded = (Sup) => class extends Sup {
[](#cb706-2)  setBrand(brand) {
[](#cb706-3)    this._brand = brand;
[](#cb706-4)    return this;
[](#cb706-5)  }
[](#cb706-6)  getBrand() {
[](#cb706-7)    return this._brand;
[](#cb706-8)  }
[](#cb706-9)};
```

We use this mixin to implement brand management for a class `Car`:

```
[](#cb707-1)class Car extends Branded(Object) {
[](#cb707-2)  constructor(model) {
[](#cb707-3)    super();
[](#cb707-4)    this._model = model;
[](#cb707-5)  }
[](#cb707-6)  toString() {
[](#cb707-7)    return `${this.getBrand()}  ${this._model}`;
[](#cb707-8)  }
[](#cb707-9)}
```

The following code confirms that the mixin worked: `Car` has method `.setBrand()` of `Branded`.

```
[](#cb708-1)const modelT = new Car('Model T').setBrand('Ford');
[](#cb708-2)assert.equal(modelT.toString(), 'Ford Model T');
```

#### 29.4.5.2 The benefits of mixins

Mixins free us from the constraints of single inheritance:

*   The same class can extend a single superclass and zero or more mixins.
*   The same mixin can be used by multiple classes.

## 29.5 FAQ: objects

### 29.5.1 Why do objects preserve the insertion order of properties?

In principle, objects are unordered. The main reason for ordering properties is so that operations that list entries, keys, or values are deterministic. That helps, e.g., with testing.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 30 Synchronous iteration

* * *

*   30.1 [What is synchronous iteration about?](#ch031.xhtml_what-is-synchronous-iteration-about)
*   30.2 [Core iteration constructs: iterables and iterators](#ch031.xhtml_iterable-iterator-iteratorresult)
*   30.3 [Iterating manually](#ch031.xhtml_iterating-manually)
    *   30.3.1 [Iterating over an iterable via `while`](#ch031.xhtml_iterating-over-an-iterable-via-while)
*   30.4 [Iteration in practice](#ch031.xhtml_iteration-in-practice)
    *   30.4.1 [Iterating over Arrays](#ch031.xhtml_iterating-over-arrays)
    *   30.4.2 [Iterating over Sets](#ch031.xhtml_iterating-over-sets)
*   30.5 [Quick reference: synchronous iteration](#ch031.xhtml_quick-reference-synchronous-iteration)
    *   30.5.1 [Iterable data sources](#ch031.xhtml_iterable-data-sources)
    *   30.5.2 [Iterating constructs](#ch031.xhtml_iterating-constructs)

* * *

## 30.1 What is synchronous iteration about?

Synchronous iteration is a *protocol* (interfaces plus rules for using them) that connects two groups of entities in JavaScript:

*   **Data sources:** On one hand, data comes in all shapes and sizes. In JavaScript’s standard library, you have the linear data structure Array, the ordered collection Set (elements are ordered by time of addition), the ordered dictionary Map (entries are ordered by time of addition), and more. In libraries, you may find tree-shaped data structures and more.

*   **Data consumers:** On the other hand, you have a whole class of constructs and algorithms that only need to access their input *sequentially*: one value at a time, until all values were visited. Examples include the `for-of` loop and spreading into function calls (via `...`).

The iteration protocol connects these two groups via the interface `Iterable`: data sources deliver their contents sequentially “through it”; data consumers get their input via it.

![](media/file36.svg)

Figure 27: Data consumers such as the `for-of` loop use the interface `Iterable`. Data sources such as `Arrays` implement that interface.

Fig. [27](#ch031.xhtml_fig:iterable-implementers-clients) illustrates how iteration works: data consumers use the interface `Iterable`; data sources implement it.

![](media/file5.svg)  **The JavaScript way of implementing interfaces**

In JavaScript, an object *implements* an interface if it has all the methods that it describes. The interfaces mentioned in this chapter only exist in the ECMAScript specification.

Both sources and consumers of data profit from this arrangement:

*   If you develop a new data structure, you only need to implement `Iterable` and a raft of tools can immediately be applied to it.

*   If you write code that uses iteration, it automatically works with many sources of data.

## 30.2 Core iteration constructs: iterables and iterators

Two roles (described by interfaces) form the core of iteration (fig. [28](#ch031.xhtml_fig:iteration-protocol)):

*   An *iterable* is an object whose contents can be traversed sequentially.
*   An *iterator* is the pointer used for the traversal.

![](media/file37.svg)

Figure 28: Iteration has two main interfaces: `Iterable` and `Iterator`. The former has a method that returns the latter.

These are type definitions (in TypeScript’s notation) for the interfaces of the iteration protocol:

```
[](#cb709-1)interface Iterable<T> {
[](#cb709-2)  [Symbol.iterator]() : Iterator<T>;
[](#cb709-3)}
[](#cb709-4)
[](#cb709-5)interface Iterator<T> {
[](#cb709-6)  next() : IteratorResult<T>;
[](#cb709-7)}
[](#cb709-8)
[](#cb709-9)interface IteratorResult<T> {
[](#cb709-10)  value: T;
[](#cb709-11)  done: boolean;
[](#cb709-12)}
```

The interfaces are used as follows:

*   You ask an `Iterable` for an iterator via the method whose key is `Symbol.iterator`.
*   The `Iterator` returns the iterated values via its method `.next()`.
*   The values are not returned directly, but wrapped in objects with two properties:
    *   `.value` is the iterated value.
    *   `.done` indicates if the end of the iteration has been reached yet. It is `true` after the last iterated value and `false` beforehand.

## 30.3 Iterating manually

This is an example of using the iteration protocol:

```
[](#cb710-1)const iterable = ['a', 'b'];
[](#cb710-2)
[](#cb710-3)// The iterable is a factory for iterators:
[](#cb710-4)const iterator = iterable[Symbol.iterator]();
[](#cb710-5)
[](#cb710-6)// Call .next() until .done is true:
[](#cb710-7)assert.deepEqual(
[](#cb710-8)  iterator.next(), { value: 'a', done: false });
[](#cb710-9)assert.deepEqual(
[](#cb710-10)  iterator.next(), { value: 'b', done: false });
[](#cb710-11)assert.deepEqual(
[](#cb710-12)  iterator.next(), { value: undefined, done: true });
```

### 30.3.1 Iterating over an iterable via `while`

The following code demonstrates how to use a `while` loop to iterate over an iterable:

```
[](#cb711-1)function logAll(iterable) {
[](#cb711-2)  const iterator = iterable[Symbol.iterator]();
[](#cb711-3)  while (true) {
[](#cb711-4)    const {value, done} = iterator.next();
[](#cb711-5)    if (done) break;
[](#cb711-6)    console.log(value);
[](#cb711-7)  }
[](#cb711-8)}
[](#cb711-9)
[](#cb711-10)logAll(['a', 'b']);
[](#cb711-11)// Output:
[](#cb711-12)// 'a'
[](#cb711-13)// 'b'
```

![](media/file6.svg)  **Exercise: Using sync iteration manually**

`exercises/sync-iteration-use/sync_iteration_manually_exrc.mjs`

## 30.4 Iteration in practice

We have seen how to use the iteration protocol manually, and it is relatively cumbersome. But the protocol is not meant to be used directly – it is meant to be used via higher-level language constructs built on top of it. This section shows what that looks like.

### 30.4.1 Iterating over Arrays

JavaScript’s Arrays are iterable. That enables us to use the `for-of` loop:

```
[](#cb712-1)const myArray = ['a', 'b', 'c'];
[](#cb712-2)
[](#cb712-3)for (const x of myArray) {
[](#cb712-4)  console.log(x);
[](#cb712-5)}
[](#cb712-6)// Output:
[](#cb712-7)// 'a'
[](#cb712-8)// 'b'
[](#cb712-9)// 'c'
```

Destructuring via Array patterns (explained later) also uses iteration under the hood:

```
[](#cb713-1)const [first, second] = myArray;
[](#cb713-2)assert.equal(first, 'a');
[](#cb713-3)assert.equal(second, 'b');
```

### 30.4.2 Iterating over Sets

JavaScript’s Set data structure is iterable. That means `for-of` works:

```
[](#cb714-1)const mySet = new Set().add('a').add('b').add('c');
[](#cb714-2)
[](#cb714-3)for (const x of mySet) {
[](#cb714-4)  console.log(x);
[](#cb714-5)}
[](#cb714-6)// Output:
[](#cb714-7)// 'a'
[](#cb714-8)// 'b'
[](#cb714-9)// 'c'
```

As does Array-destructuring:

```
[](#cb715-1)const [first, second] = mySet;
[](#cb715-2)assert.equal(first, 'a');
[](#cb715-3)assert.equal(second, 'b');
```

## 30.5 Quick reference: synchronous iteration

### 30.5.1 Iterable data sources

The following built-in data sources are iterable:

*   Arrays
*   Strings
*   Maps
*   Sets
*   (Browsers: DOM data structures)

To iterate over the properties of objects, you need helpers such as `Object.keys()` and `Object.entries()`. That is necessary because properties exist at a different level that is independent of the level of data structures.

### 30.5.2 Iterating constructs

The following constructs are based on iteration:

*   Destructuring via an Array pattern:

    ```
    [](#cb716-1)const [x,y] = iterable;
    ```

*   The `for-of` loop:

    ```
    [](#cb717-1)for (const x of iterable) { /*···*/ }
    ```

*   `Array.from()`:

    ```
    [](#cb718-1)const arr = Array.from(iterable);
    ```

*   Spreading (via `...`) into function calls and Array literals:

    ```
    [](#cb719-1)func(...iterable);
    [](#cb719-2)const arr = [...iterable];
    ```

*   `new Map()` and `new Set()`:

    ```
    [](#cb720-1)const m = new Map(iterableOverKeyValuePairs);
    [](#cb720-2)const s = new Set(iterableOverElements);
    ```

*   `Promise.all()` and `Promise.race()`:

    ```
    [](#cb721-1)const promise1 = Promise.all(iterableOverPromises);
    [](#cb721-2)const promise2 = Promise.race(iterableOverPromises);
    ```

*   `yield*`:

    ```
    [](#cb722-1)function* generatorFunction() {
    [](#cb722-2)  yield* iterable;
    [](#cb722-3)}
    ```

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 31 Arrays (`Array`)

* * *

*   31.1 [The two roles of Arrays in JavaScript](#ch032.xhtml_the-two-roles-of-arrays-in-javascript)
*   31.2 [Basic Array operations](#ch032.xhtml_basic-array-operations)
    *   31.2.1 [Creating, reading, writing Arrays](#ch032.xhtml_array-literals)
    *   31.2.2 [The `.length` of an Array](#ch032.xhtml_the-.length-of-an-array)
    *   31.2.3 [Clearing an Array](#ch032.xhtml_clearing-an-array)
    *   31.2.4 [Spreading into Array literals](#ch032.xhtml_spreading-into-array-literals)
    *   31.2.5 [Arrays: listing indices and entries](#ch032.xhtml_arrays-listing-indices-and-entries)
    *   31.2.6 [Is a value an Array?](#ch032.xhtml_is-a-value-an-array)
*   31.3 [`for-of` and Arrays](#ch032.xhtml_for-of-and-arrays)
    *   31.3.1 [`for-of`: iterating over elements](#ch032.xhtml_for-of-iterating-over-elements)
    *   31.3.2 [`for-of`: iterating over [index, element] pairs](#ch032.xhtml_for-of-iterating-over-index-element-pairs)
*   31.4 [Array-like objects](#ch032.xhtml_array-like-objects)
*   31.5 [Converting iterable and Array-like values to Arrays](#ch032.xhtml_converting-iterable-and-array-like-values-to-arrays)
    *   31.5.1 [Converting iterables to Arrays via spreading (`...`)](#ch032.xhtml_converting-iterables-to-arrays-via-spreading-...)
    *   31.5.2 [Converting iterables and Array-like objects to Arrays via `Array.from()` (advanced)](#ch032.xhtml_converting-iterables-and-array-like-objects-to-arrays-via-array.from-advanced)
*   31.6 [Creating and filling Arrays with arbitrary lengths](#ch032.xhtml_filling-arrays)
    *   31.6.1 [Do you need to create an empty Array that you’ll fill completely later on?](#ch032.xhtml_do-you-need-to-create-an-empty-array-that-youll-fill-completely-later-on)
    *   31.6.2 [Do you need to create an Array filled with a primitive value?](#ch032.xhtml_do-you-need-to-create-an-array-filled-with-a-primitive-value)
    *   31.6.3 [Do you need to create an Array filled with objects?](#ch032.xhtml_creating-arrays-filled-with-objects)
    *   31.6.4 [Do you need to create a range of integers?](#ch032.xhtml_create-range-of-integers)
    *   31.6.5 [Use a Typed Array if the elements are all integers or all floats](#ch032.xhtml_use-a-typed-array-if-the-elements-are-all-integers-or-all-floats)
*   31.7 [Multidimensional Arrays](#ch032.xhtml_multidimensional-arrays)
*   31.8 [More Array features (advanced)](#ch032.xhtml_more-array-features-advanced)
    *   31.8.1 [Array indices are (slightly special) property keys](#ch032.xhtml_array-indices)
    *   31.8.2 [Arrays are dictionaries and can have holes](#ch032.xhtml_array-holes)
*   31.9 [Adding and removing elements (destructively and non-destructively)](#ch032.xhtml_adding-and-removing-elements-destructively-and-non-destructively)
    *   31.9.1 [Prepending elements and Arrays](#ch032.xhtml_prepending-elements-and-arrays)
    *   31.9.2 [Appending elements and Arrays](#ch032.xhtml_appending-elements-and-arrays)
    *   31.9.3 [Removing elements](#ch032.xhtml_removing-elements)
*   31.10 [Methods: iteration and transformation (`.find()`, `.map()`, `.filter()`, etc.)](#ch032.xhtml_methods-iteration-and-transformation-.find-.map-.filter-etc.)
    *   31.10.1 [Callbacks for iteration and transformation methods](#ch032.xhtml_callbacks-for-iteration-and-transformation-methods)
    *   31.10.2 [Searching elements: `.find()`, `.findIndex()`](#ch032.xhtml_searching-elements-.find-.findindex)
    *   31.10.3 [`.map()`: copy while giving elements new values](#ch032.xhtml_map-copy-while-giving-elements-new-values)
    *   31.10.4 [`.flatMap()`: mapping to zero or more values](#ch032.xhtml_flatmap-mapping-to-zero-or-more-values)
    *   31.10.5 [`.filter()`: only keep some of the elements](#ch032.xhtml_filter-only-keep-some-of-the-elements)
    *   31.10.6 [`.reduce()`: deriving a value from an Array (advanced)](#ch032.xhtml_Array.prototype.reduce)
*   31.11 [`.sort()`: sorting Arrays](#ch032.xhtml_sort-sorting-arrays)
    *   31.11.1 [Customizing the sort order](#ch032.xhtml_customizing-the-sort-order)
    *   31.11.2 [Sorting numbers](#ch032.xhtml_sorting-numbers)
    *   31.11.3 [Sorting objects](#ch032.xhtml_sorting-objects)
*   31.12 [Quick reference: `Array<T>`](#ch032.xhtml_quickref-arrays)
    *   31.12.1 [`new Array()`](#ch032.xhtml_new-array)
    *   31.12.2 [Static methods of `Array`](#ch032.xhtml_static-methods-of-array)
    *   31.12.3 [Methods of `Array<T>.prototype`](#ch032.xhtml_quickref-array-prototype)
    *   31.12.4 [Sources](#ch032.xhtml_sources-3)

* * *

## 31.1 The two roles of Arrays in JavaScript

Arrays play two roles in JavaScript:

*   Tuples: Arrays-as-tuples have a fixed number of indexed elements. Each of those elements can have a different type.
*   Sequences: Arrays-as-sequences have a variable number of indexed elements. Each of those elements has the same type.

In practice, these two roles are often mixed.

Notably, Arrays-as-sequences are so flexible that you can use them as (traditional) arrays, stacks, and queues (see exercise later in this chapter).

## 31.2 Basic Array operations

### 31.2.1 Creating, reading, writing Arrays

The best way to create an Array is via an *Array literal*:

```
[](#cb723-1)const arr = ['a', 'b', 'c'];
```

The Array literal starts and ends with square brackets `[]`. It creates an Array with three *elements*: `'a'`, `'b'`, and `'c'`.

To read an Array element, you put an index in square brackets (indices start at zero):

```
[](#cb724-1)assert.equal(arr[0], 'a');
```

To change an Array element, you assign to an Array with an index:

```
[](#cb725-1)arr[0] = 'x';
[](#cb725-2)assert.deepEqual(arr, ['x', 'b', 'c']);
```

The range of Array indices is 32 bits (excluding the maximum length): [0, 2^(32)−1)

### 31.2.2 The `.length` of an Array

Every Array has a property `.length` that can be used to both read and change(!) the number of elements in an Array.

The length of an Array is always the highest index plus one:

```
> const arr = ['a', 'b'];
> arr.length
2
```

If you write to the Array at the index of the length, you append an element:

```
> arr[arr.length] = 'c';
> arr
[ 'a', 'b', 'c' ]
> arr.length
3
```

Another way of (destructively) appending an element is via the Array method `.push()`:

```
> arr.push('d');
> arr
[ 'a', 'b', 'c', 'd' ]
```

If you set `.length`, you are pruning the Array by removing elements:

```
> arr.length = 1;
> arr
[ 'a' ]
```

### 31.2.3 Clearing an Array

To clear (empty) an Array, you can either set its `.length` to zero:

```
[](#cb730-1)const arr = ['a', 'b', 'c'];
[](#cb730-2)arr.length = 0;
[](#cb730-3)assert.deepEqual(arr, []);
```

or you can assign a new empty Array to the variable storing the Array:

```
[](#cb731-1)let arr = ['a', 'b', 'c'];
[](#cb731-2)arr = [];
[](#cb731-3)assert.deepEqual(arr, []);
```

The latter approach has the advantage of not affecting other locations that point to the same Array. If, however, you do want to reset a shared Array for everyone, then you need the former approach.

![](media/file6.svg)  **Exercise: Removing empty lines via `.push()`**

`exercises/arrays/remove_empty_lines_push_test.mjs`

### 31.2.4 Spreading into Array literals

Inside an Array literal, a *spread element* consists of three dots (`...`) followed by an expression. It results in the expression being evaluated and then iterated over. Each iterated value becomes an additional Array element – for example:

```
> const iterable = ['b', 'c'];
> ['a', ...iterable, 'd']
[ 'a', 'b', 'c', 'd' ]
```

That means that we can use spreading to create a copy of an Array:

```
[](#cb733-1)const original = ['a', 'b', 'c'];
[](#cb733-2)const copy = [...original];
```

Spreading is also convenient for concatenating Arrays (and other iterables) into Arrays:

```
[](#cb734-1)const arr1 = ['a', 'b'];
[](#cb734-2)const arr2 = ['c', 'd'];
[](#cb734-3)
[](#cb734-4)const concatenated = [...arr1, ...arr2, 'e'];
[](#cb734-5)assert.deepEqual(
[](#cb734-6)  concatenated,
[](#cb734-7)  ['a', 'b', 'c', 'd', 'e']);
```

Due to spreading using iteration, it only works if the value is iterable:

```
> [...'abc'] // strings are iterable
[ 'a', 'b', 'c' ]
> [...123]
TypeError: number 123 is not iterable
> [...undefined]
TypeError: undefined is not iterable
```

![](media/file4.svg)  **Spreading into Array literals is shallow**

Similar to [spreading into object literals](#ch029.xhtml_spreading-into-object-literals), spreading into Array literals creates *shallow* copies. That is, nested Arrays are not copied.

### 31.2.5 Arrays: listing indices and entries

Method `.keys()` lists the indices of an Array:

```
[](#cb736-1)const arr = ['a', 'b'];
[](#cb736-2)assert.deepEqual(
[](#cb736-3)  [...arr.keys()], // (A)
[](#cb736-4)  [0, 1]);
```

`.keys()` returns an iterable. In line A, we spread to obtain an Array.

Listing Array indices is different from listing properties. The former produces numbers; the latter produces stringified numbers (in addition to non-index property keys):

```
[](#cb737-1)const arr = ['a', 'b'];
[](#cb737-2)arr.prop = true;
[](#cb737-3)
[](#cb737-4)assert.deepEqual(
[](#cb737-5)  Object.keys(arr),
[](#cb737-6)  ['0', '1', 'prop']);
```

Method `.entries()` lists the contents of an Array as [index, element] pairs:

```
[](#cb738-1)const arr = ['a', 'b'];
[](#cb738-2)assert.deepEqual(
[](#cb738-3)  [...arr.entries()],
[](#cb738-4)  [[0, 'a'], [1, 'b']]);
```

### 31.2.6 Is a value an Array?

Following are two ways of checking if a value is an Array:

```
> [] instanceof Array
true
> Array.isArray([])
true
```

`instanceof` is usually fine. You need `Array.isArray()` if a value may come from another *realm*. Roughly, a realm is an instance of JavaScript’s global scope. Some realms are isolated from each other (e.g., [Web Workers](#ch040.xhtml_web-workers) in browsers), but there are also realms between which you can move data – for example, same-origin iframes in browsers. `x instanceof Array` checks the prototype chain of `x` and therefore returns `false` if `x` is an Array from another realm.

`typeof` categorizes Arrays as objects:

```
> typeof []
'object'
```

## 31.3 `for-of` and Arrays

We have already encountered the `for-of` loop. This section briefly recaps how to use it for Arrays.

### 31.3.1 `for-of`: iterating over elements

The following `for-of` loop iterates over the elements of an Array.

```
[](#cb741-1)for (const element of ['a', 'b']) {
[](#cb741-2)  console.log(element);
[](#cb741-3)}
[](#cb741-4)// Output:
[](#cb741-5)// 'a'
[](#cb741-6)// 'b'
```

### 31.3.2 `for-of`: iterating over [index, element] pairs

The following `for-of` loop iterates over [index, element] pairs. Destructuring (described [later](#ch038.xhtml_ch_destructuring)), gives us convenient syntax for setting up `index` and `element` in the head of `for-of`.

```
[](#cb742-1)for (const [index, element] of ['a', 'b'].entries()) {
[](#cb742-2)  console.log(index, element);
[](#cb742-3)}
[](#cb742-4)// Output:
[](#cb742-5)// 0, 'a'
[](#cb742-6)// 1, 'b'
```

## 31.4 Array-like objects

Some operations that work with Arrays require only the bare minimum: values must only be *Array-like*. An Array-like value is an object with the following properties:

*   `.length`: holds the length of the Array-like object.
*   `[0]`: holds the element at index 0 (etc.). Note that if you use numbers as property names, they are always coerced to strings. Therefore, `[0]` retrieves the value of the property whose key is `'0'`.

For example, `Array.from()` accepts Array-like objects and converts them to Arrays:

```
[](#cb743-1)// If you omit .length, it is interpreted as 0
[](#cb743-2)assert.deepEqual(
[](#cb743-3)  Array.from({}),
[](#cb743-4)  []);
[](#cb743-5)
[](#cb743-6)assert.deepEqual(
[](#cb743-7)  Array.from({length:2, 0:'a', 1:'b'}),
[](#cb743-8)  [ 'a', 'b' ]);
```

The TypeScript interface for Array-like objects is:

```
[](#cb744-1)interface ArrayLike<T> {
[](#cb744-2)  length: number;
[](#cb744-3)  [n: number]: T;
[](#cb744-4)}
```

![](media/file5.svg)  **Array-like objects are relatively rare in modern JavaScript**

Array-like objects used to be common before ES6; now you don’t see them very often.

## 31.5 Converting iterable and Array-like values to Arrays

There are two common ways of converting iterable and Array-like values to Arrays: spreading and `Array.from()`.

### 31.5.1 Converting iterables to Arrays via spreading (`...`)

Inside an Array literal, spreading via `...` converts any iterable object into a series of Array elements. For example:

```
[](#cb745-1)// Get an Array-like collection from a web browser’s DOM
[](#cb745-2)const domCollection = document.querySelectorAll('a');
[](#cb745-3)
[](#cb745-4)// Alas, the collection is missing many Array methods
[](#cb745-5)assert.equal('map' in domCollection, false);
[](#cb745-6)
[](#cb745-7)// Solution: convert it to an Array
[](#cb745-8)const arr = [...domCollection];
[](#cb745-9)assert.deepEqual(
[](#cb745-10)  arr.map(x => x.href),
[](#cb745-11)  ['https://2ality.com', 'https://exploringjs.com']);
```

The conversion works because the DOM collection is iterable.

### 31.5.2 Converting iterables and Array-like objects to Arrays via `Array.from()` (advanced)

`Array.from()` can be used in two modes.

#### 31.5.2.1 Mode 1 of `Array.from()`: converting

The first mode has the following type signature:

```
[](#cb746-1).from<T>(iterable: Iterable<T> | ArrayLike<T>): T[]
```

Interface `Iterable` is shown [in the chapter on synchronous iteration](#ch031.xhtml_iterable-iterator-iteratorresult). Interface `ArrayLike` appeared [earlier in this chapter](#ch032.xhtml_array-like-objects).

With a single parameter, `Array.from()` converts anything iterable or Array-like to an Array:

```
> Array.from(new Set(['a', 'b']))
[ 'a', 'b' ]
> Array.from({length: 2, 0:'a', 1:'b'})
[ 'a', 'b' ]
```

#### 31.5.2.2 Mode 2 of `Array.from()`: converting and mapping

The second mode of `Array.from()` involves two parameters:

```
[](#cb748-1).from<T, U>(
[](#cb748-2)  iterable: Iterable<T> | ArrayLike<T>,
[](#cb748-3)  mapFunc: (v: T, i: number) => U,
[](#cb748-4)  thisArg?: any)
[](#cb748-5)  : U[]
```

In this mode, `Array.from()` does several things:

*   It iterates over `iterable`.
*   It calls `mapFunc` with each iterated value. The optional parameter `thisArg` specifies a `this` for `mapFunc`.
*   It applies `mapFunc` to each iterated value.
*   It collects the results in a new Array and returns it.

In other words: we are going from an iterable with elements of type `T` to an Array with elements of type `U`.

This is an example:

```
> Array.from(new Set(['a', 'b']), x => x + x)
[ 'aa', 'bb' ]
```

## 31.6 Creating and filling Arrays with arbitrary lengths

The best way of creating an Array is via an Array literal. However, you can’t always use one: The Array may be too large, you may not know its length during development, or you may want to keep its length flexible. Then I recommend the following techniques for creating, and possibly filling, Arrays.

### 31.6.1 Do you need to create an empty Array that you’ll fill completely later on?

```
> new Array(3)
[ , , ,]
```

Note that the result has three [*holes* (empty slots)](#ch032.xhtml_array-holes) – the last comma in an Array literal is always ignored.

### 31.6.2 Do you need to create an Array filled with a primitive value?

```
> new Array(3).fill(0)
[0, 0, 0]
```

Caveat: If you use `.fill()` with an object, then each Array element will refer to this object (sharing it).

```
[](#cb752-1)const arr = new Array(3).fill({});
[](#cb752-2)arr[0].prop = true;
[](#cb752-3)assert.deepEqual(
[](#cb752-4)  arr, [
[](#cb752-5)    {prop: true},
[](#cb752-6)    {prop: true},
[](#cb752-7)    {prop: true},
[](#cb752-8)  ]);
```

The next subsection explains how to fix this.

### 31.6.3 Do you need to create an Array filled with objects?

```
> Array.from({length: 3}, () => ({}))
[{}, {}, {}]
```

### 31.6.4 Do you need to create a range of integers?

```
[](#cb754-1)function createRange(start, end) {
[](#cb754-2)  return Array.from({length: end-start}, (_, i) => i+start);
[](#cb754-3)}
[](#cb754-4)assert.deepEqual(
[](#cb754-5)  createRange(2, 5),
[](#cb754-6)  [2, 3, 4]);
```

Here is an alternative, slightly hacky technique for creating integer ranges that start at zero:

```
[](#cb755-1)/** Returns an iterable */
[](#cb755-2)function createRange(end) {
[](#cb755-3)  return new Array(end).keys();
[](#cb755-4)}
[](#cb755-5)assert.deepEqual(
[](#cb755-6)  [...createRange(4)],
[](#cb755-7)  [0, 1, 2, 3]);
```

This works because `.keys()` treats [*holes*](#ch032.xhtml_array-holes) like `undefined` elements and lists their indices.

### 31.6.5 Use a Typed Array if the elements are all integers or all floats

If you are dealing with Arrays of integers or floats, consider [*Typed Arrays*](#ch033.xhtml_ch_typed-arrays), which were created for this purpose.

## 31.7 Multidimensional Arrays

JavaScript does not have real multidimensional Arrays; you need to resort to Arrays whose elements are Arrays:

```
[](#cb756-1)function initMultiArray(...dimensions) {
[](#cb756-2)  function initMultiArrayRec(dimIndex) {
[](#cb756-3)    if (dimIndex >= dimensions.length) {
[](#cb756-4)      return 0;
[](#cb756-5)    } else {
[](#cb756-6)      const dim = dimensions[dimIndex];
[](#cb756-7)      const arr = [];
[](#cb756-8)      for (let i=0; i<dim; i++) {
[](#cb756-9)        arr.push(initMultiArrayRec(dimIndex+1));
[](#cb756-10)      }
[](#cb756-11)      return arr;
[](#cb756-12)    }
[](#cb756-13)  }
[](#cb756-14)  return initMultiArrayRec(0);
[](#cb756-15)}
[](#cb756-16)
[](#cb756-17)const arr = initMultiArray(4, 3, 2);
[](#cb756-18)arr[3][2][1] = 'X'; // last in each dimension
[](#cb756-19)assert.deepEqual(arr, [
[](#cb756-20)  [ [ 0, 0 ], [ 0, 0 ], [ 0, 0 ] ],
[](#cb756-21)  [ [ 0, 0 ], [ 0, 0 ], [ 0, 0 ] ],
[](#cb756-22)  [ [ 0, 0 ], [ 0, 0 ], [ 0, 0 ] ],
[](#cb756-23)  [ [ 0, 0 ], [ 0, 0 ], [ 0, 'X' ] ],
[](#cb756-24)]);
```

## 31.8 More Array features (advanced)

In this section, we look at phenomena you don’t encounter often when working with Arrays.

### 31.8.1 Array indices are (slightly special) property keys

You’d think that Array elements are special because you are accessing them via numbers. But the square brackets operator `[]` for doing so is the same operator that is used for accessing properties. It coerces any value (that is not a symbol) to a string. Therefore, Array elements are (almost) normal properties (line A) and it doesn’t matter if you use numbers or strings as indices (lines B and C):

```
[](#cb757-1)const arr = ['a', 'b'];
[](#cb757-2)arr.prop = 123;
[](#cb757-3)assert.deepEqual(
[](#cb757-4)  Object.keys(arr),
[](#cb757-5)  ['0', '1', 'prop']); // (A)
[](#cb757-6)
[](#cb757-7)assert.equal(arr[0], 'a');  // (B)
[](#cb757-8)assert.equal(arr['0'], 'a'); // (C)
```

To make matters even more confusing, this is only how the language specification defines things (the theory of JavaScript, if you will). Most JavaScript engines optimize under the hood and do use actual integers to access Array elements (the practice of JavaScript, if you will).

Property keys (strings!) that are used for Array elements are called [*indices*](https://tc39.github.io/ecma262/#integer-index). A string `str` is an index if converting it to a 32-bit unsigned integer and back results in the original value. Written as a formula:

```
ToString(ToUint32(str)) === str
```

#### 31.8.1.1 Listing indices

When listing property keys, [indices are treated specially](#ch029.xhtml_order-of-properties) – they always come first and are sorted like numbers (`'2'` comes before `'10'`):

```
[](#cb759-1)const arr = [];
[](#cb759-2)arr.prop = true;
[](#cb759-3)arr[1] = 'b';
[](#cb759-4)arr[0] = 'a';
[](#cb759-5)
[](#cb759-6)assert.deepEqual(
[](#cb759-7)  Object.keys(arr),
[](#cb759-8)  ['0', '1', 'prop']);
```

Note that `.length`, `.entries()` and `.keys()` treat Array indices as numbers and ignore non-index properties:

```
[](#cb760-1)assert.equal(arr.length, 2);
[](#cb760-2)assert.deepEqual(
[](#cb760-3)  [...arr.keys()], [0, 1]);
[](#cb760-4)assert.deepEqual(
[](#cb760-5)  [...arr.entries()], [[0, 'a'], [1, 'b']]);
```

We used a spread element (`...`) to convert the iterables returned by `.keys()` and `.entries()` to Arrays.

### 31.8.2 Arrays are dictionaries and can have holes

We distinguish two kinds of Arrays in JavaScript:

*   An Array `arr` is *dense* if all indices `i`, with 0 ≤ `i` < `arr.length`, exist. That is, the indices form a contiguous range.
*   An Array is *sparse* if the range of indices has *holes* in it. That is, some indices are missing.

Arrays can be sparse in JavaScript because Arrays are actually dictionaries from indices to values.

![](media/file2.svg)  **Recommendation: avoid holes**

So far, we have only seen dense Arrays and it’s indeed recommended to avoid holes: They make your code more complicated and are not handled consistently by Array methods. Additionally, JavaScript engines optimize dense Arrays, making them faster.

#### 31.8.2.1 Creating holes

You can create holes by skipping indices when assigning elements:

```
[](#cb761-1)const arr = [];
[](#cb761-2)arr[0] = 'a';
[](#cb761-3)arr[2] = 'c';
[](#cb761-4)
[](#cb761-5)assert.deepEqual(Object.keys(arr), ['0', '2']); // (A)
[](#cb761-6)
[](#cb761-7)assert.equal(0 in arr, true); // element
[](#cb761-8)assert.equal(1 in arr, false); // hole
```

In line A, we are using `Object.keys()` because `arr.keys()` treats holes as if they were `undefined` elements and does not reveal them.

Another way of creating holes is to skip elements in Array literals:

```
[](#cb762-1)const arr = ['a', , 'c'];
[](#cb762-2)
[](#cb762-3)assert.deepEqual(Object.keys(arr), ['0', '2']);
```

You can also delete Array elements:

```
[](#cb763-1)const arr = ['a', 'b', 'c'];
[](#cb763-2)assert.deepEqual(Object.keys(arr), ['0', '1', '2']);
[](#cb763-3)delete arr[1];
[](#cb763-4)assert.deepEqual(Object.keys(arr), ['0', '2']);
```

#### 31.8.2.2 How do Array operations treat holes?

Alas, there are many different ways in which Array operations treat holes.

Some Array operations remove holes:

```
> ['a',,'b'].filter(x => true)
[ 'a', 'b' ]
```

Some Array operations ignore holes:

```
> ['a', ,'a'].every(x => x === 'a')
true
```

Some Array operations ignore but preserve holes:

```
> ['a',,'b'].map(x => 'c')
[ 'c', , 'c' ]
```

Some Array operations treat holes as `undefined` elements:

```
> Array.from(['a',,'b'], x => x)
[ 'a', undefined, 'b' ]
> [...['a',,'b'].entries()]
[[0, 'a'], [1, undefined], [2, 'b']]
```

`Object.keys()` works differently than `.keys()` (strings vs. numbers, holes don’t have keys):

```
> [...['a',,'b'].keys()]
[ 0, 1, 2 ]
> Object.keys(['a',,'b'])
[ '0', '2' ]
```

There is no rule to remember here. If it ever matters how an Array operation treats holes, the best approach is to do a quick test in a console.

## 31.9 Adding and removing elements (destructively and non-destructively)

JavaScript’s `Array` is quite flexible and more like a combination of array, stack, and queue. This section explores ways of adding and removing Array elements. Most operations can be performed both *destructively* (modifying the Array) and *non-destructively* (producing a modified copy).

### 31.9.1 Prepending elements and Arrays

In the following code, we destructively prepend single elements to `arr1` and an Array to `arr2`:

```
[](#cb769-1)const arr1 = ['a', 'b'];
[](#cb769-2)arr1.unshift('x', 'y'); // prepend single elements
[](#cb769-3)assert.deepEqual(arr1, ['x', 'y', 'a', 'b']);
[](#cb769-4)
[](#cb769-5)const arr2 = ['a', 'b'];
[](#cb769-6)arr2.unshift(...['x', 'y']); // prepend Array
[](#cb769-7)assert.deepEqual(arr2, ['x', 'y', 'a', 'b']);
```

Spreading lets us unshift an Array into `arr2`.

Non-destructive prepending is done via spread elements:

```
[](#cb770-1)const arr1 = ['a', 'b'];
[](#cb770-2)assert.deepEqual(
[](#cb770-3)  ['x', 'y', ...arr1], // prepend single elements
[](#cb770-4)  ['x', 'y', 'a', 'b']);
[](#cb770-5)assert.deepEqual(arr1, ['a', 'b']); // unchanged!
[](#cb770-6)
[](#cb770-7)const arr2 = ['a', 'b'];
[](#cb770-8)assert.deepEqual(
[](#cb770-9)  [...['x', 'y'], ...arr2], // prepend Array
[](#cb770-10)  ['x', 'y', 'a', 'b']);
[](#cb770-11)assert.deepEqual(arr2, ['a', 'b']); // unchanged!
```

### 31.9.2 Appending elements and Arrays

In the following code, we destructively append single elements to `arr1` and an Array to `arr2`:

```
[](#cb771-1)const arr1 = ['a', 'b'];
[](#cb771-2)arr1.push('x', 'y'); // append single elements
[](#cb771-3)assert.deepEqual(arr1, ['a', 'b', 'x', 'y']);
[](#cb771-4)
[](#cb771-5)const arr2 = ['a', 'b'];
[](#cb771-6)arr2.push(...['x', 'y']); // append Array
[](#cb771-7)assert.deepEqual(arr2, ['a', 'b', 'x', 'y']);
```

Spreading lets us push an Array into `arr2`.

Non-destructive appending is done via spread elements:

```
[](#cb772-1)const arr1 = ['a', 'b'];
[](#cb772-2)assert.deepEqual(
[](#cb772-3)  [...arr1, 'x', 'y'], // append single elements
[](#cb772-4)  ['a', 'b', 'x', 'y']);
[](#cb772-5)assert.deepEqual(arr1, ['a', 'b']); // unchanged!
[](#cb772-6)
[](#cb772-7)const arr2 = ['a', 'b'];
[](#cb772-8)assert.deepEqual(
[](#cb772-9)  [...arr2, ...['x', 'y']], // append Array
[](#cb772-10)  ['a', 'b', 'x', 'y']);
[](#cb772-11)assert.deepEqual(arr2, ['a', 'b']); // unchanged!
```

### 31.9.3 Removing elements

These are three destructive ways of removing Array elements:

```
[](#cb773-1)// Destructively remove first element:
[](#cb773-2)const arr1 = ['a', 'b', 'c'];
[](#cb773-3)assert.equal(arr1.shift(), 'a');
[](#cb773-4)assert.deepEqual(arr1, ['b', 'c']);
[](#cb773-5)
[](#cb773-6)// Destructively remove last element:
[](#cb773-7)const arr2 = ['a', 'b', 'c'];
[](#cb773-8)assert.equal(arr2.pop(), 'c');
[](#cb773-9)assert.deepEqual(arr2, ['a', 'b']);
[](#cb773-10)
[](#cb773-11)// Remove one or more elements anywhere:
[](#cb773-12)const arr3 = ['a', 'b', 'c', 'd'];
[](#cb773-13)assert.deepEqual(arr3.splice(1, 2), ['b', 'c']);
[](#cb773-14)assert.deepEqual(arr3, ['a', 'd']);
```

`.splice()` is covered in more detail in [the quick reference at the end of this chapter](#ch032.xhtml_quickref-array-prototype).

Destructuring via a rest element lets you non-destructively remove elements from the beginning of an Array (destructuring is covered [later](#ch038.xhtml_ch_destructuring)).

```
[](#cb774-1)const arr1 = ['a', 'b', 'c'];
[](#cb774-2)// Ignore first element, extract remaining elements
[](#cb774-3)const [, ...arr2] = arr1;
[](#cb774-4)
[](#cb774-5)assert.deepEqual(arr2, ['b', 'c']);
[](#cb774-6)assert.deepEqual(arr1, ['a', 'b', 'c']); // unchanged!
```

Alas, a rest element must come last in an Array. Therefore, you can only use it to extract suffixes.

![](media/file6.svg)  **Exercise: Implementing a queue via an Array**

`exercises/arrays/queue_via_array_test.mjs`

## 31.10 Methods: iteration and transformation (`.find()`, `.map()`, `.filter()`, etc.)

In this section, we take a look at Array methods for iterating over Arrays and for transforming Arrays.

### 31.10.1 Callbacks for iteration and transformation methods

All iteration and transformation methods use callbacks. The former feed all iterated values to their callbacks; the latter ask their callbacks how to transform Arrays.

These callbacks have type signatures that look as follows:

```
[](#cb775-1)callback: (value: T, index: number, array: Array<T>) => boolean
```

That is, the callback gets three parameters (it is free to ignore any of them):

*   `value` is the most important one. This parameter holds the iterated value that is currently being processed.
*   `index` can additionally tell the callback what the index of the iterated value is.
*   `array` points to the current Array (the receiver of the method call). Some algorithms need to refer to the whole Array – e.g., to search it for answers. This parameter lets you write reusable callbacks for such algorithms.

What the callback is expected to return depends on the method it is passed to. Possibilities include:

*   `.map()` fills its result with the values returned by its callback:

    ```
    > ['a', 'b', 'c'].map(x => x + x)
    [ 'aa', 'bb', 'cc' ]
    ```

*   `.find()` returns the first Array element for which its callback returns `true`:

    ```
    > ['a', 'bb', 'ccc'].find(str => str.length >= 2)
    'bb'
    ```

Both of these methods are described in more detail later.

### 31.10.2 Searching elements: `.find()`, `.findIndex()`

`.find()` returns the first element for which its callback returns a truthy value (and `undefined` if it can’t find anything):

```
> [6, -5, 8].find(x => x < 0)
-5
> [6, 5, 8].find(x => x < 0)
undefined
```

`.findIndex()` returns the index of the first element for which its callback returns a truthy value (and `-1` if it can’t find anything):

```
> [6, -5, 8].findIndex(x => x < 0)
1
> [6, 5, 8].findIndex(x => x < 0)
-1
```

`.findIndex()` can be implemented as follows:

```
[](#cb780-1)function findIndex(arr, callback) {
[](#cb780-2)  for (const [i, x] of arr.entries()) {
[](#cb780-3)    if (callback(x, i, arr)) {
[](#cb780-4)      return i;
[](#cb780-5)    }
[](#cb780-6)  }
[](#cb780-7)  return -1;
[](#cb780-8)}
```

### 31.10.3 `.map()`: copy while giving elements new values

`.map()` returns a modified copy of the receiver. The elements of the copy are the results of applying `map`’s callback to the elements of the receiver.

All of this is easier to understand via examples:

```
> [1, 2, 3].map(x => x * 3)
[ 3, 6, 9 ]
> ['how', 'are', 'you'].map(str => str.toUpperCase())
[ 'HOW', 'ARE', 'YOU' ]
> [true, true, true].map((_x, index) => index)
[ 0, 1, 2 ]
```

`.map()` can be implemented as follows:

```
[](#cb782-1)function map(arr, mapFunc) {
[](#cb782-2)  const result = [];
[](#cb782-3)  for (const [i, x] of arr.entries()) {
[](#cb782-4)    result.push(mapFunc(x, i, arr));
[](#cb782-5)  }
[](#cb782-6)  return result;
[](#cb782-7)}
```

![](media/file6.svg)  **Exercise: Numbering lines via `.map()`**

`exercises/arrays/number_lines_test.mjs`

### 31.10.4 `.flatMap()`: mapping to zero or more values

The type signature of `Array<T>.prototype.flatMap()` is:

```
[](#cb783-1).flatMap<U>(
[](#cb783-2)  callback: (value: T, index: number, array: T[]) => U|Array<U>,
[](#cb783-3)  thisValue?: any
[](#cb783-4)): U[]
```

Both `.map()` and `.flatMap()` take a function `callback` as a parameter that controls how an input Array is translated to an output Array:

*   With `.map()`, each input Array element is translated to exactly one output element. That is, `callback` returns a single value.
*   With `.flatMap()`, each input Array element is translated to zero or more output elements. That is, `callback` returns an Array of values (it can also return non-Array values, but that is rare).

This is `.flatMap()` in action:

```
> ['a', 'b', 'c'].flatMap(x => [x,x])
[ 'a', 'a', 'b', 'b', 'c', 'c' ]
> ['a', 'b', 'c'].flatMap(x => [x])
[ 'a', 'b', 'c' ]
> ['a', 'b', 'c'].flatMap(x => [])
[]
```

#### 31.10.4.1 A simple implementation

You could implement `.flatMap()` as follows. Note: This implementation is simpler than the built-in version, which, for example, performs more checks.

```
[](#cb785-1)function flatMap(arr, mapFunc) {
[](#cb785-2)  const result = [];
[](#cb785-3)  for (const [index, elem] of arr.entries()) {
[](#cb785-4)    const x = mapFunc(elem, index, arr);
[](#cb785-5)    // We allow mapFunc() to return non-Arrays
[](#cb785-6)    if (Array.isArray(x)) {
[](#cb785-7)      result.push(...x);
[](#cb785-8)    } else {
[](#cb785-9)      result.push(x);
[](#cb785-10)    }
[](#cb785-11)  }
[](#cb785-12)  return result;
[](#cb785-13)}
```

What is `.flatMap()` good for? Let’s look at use cases!

#### 31.10.4.2 Use case: filtering and mapping at the same time

The result of the Array method `.map()` always has the same length as the Array it is invoked on. That is, its callback can’t skip Array elements it isn’t interested in. The ability of `.flatMap()` to do so is useful in the next example.

We will use the following function `processArray()` to create an Array that we’ll then filter and map via `.flatMap()`:

```
[](#cb786-1)function processArray(arr, callback) {
[](#cb786-2)  return arr.map(x => {
[](#cb786-3)    try {
[](#cb786-4)      return { value: callback(x) };
[](#cb786-5)    } catch (e) {
[](#cb786-6)      return { error: e };
[](#cb786-7)    }
[](#cb786-8)  });
[](#cb786-9)}
```

Next, we create an Array `results` via `processArray()`:

```
[](#cb787-1)const results = processArray([1, -5, 6], throwIfNegative);
[](#cb787-2)assert.deepEqual(results, [
[](#cb787-3)  { value: 1 },
[](#cb787-4)  { error: new Error('Illegal value: -5') },
[](#cb787-5)  { value: 6 },
[](#cb787-6)]);
[](#cb787-7)
[](#cb787-8)function throwIfNegative(value) {
[](#cb787-9)  if (value < 0) {
[](#cb787-10)    throw new Error('Illegal value: '+value);
[](#cb787-11)  }
[](#cb787-12)  return value;
[](#cb787-13)}
```

We can now use `.flatMap()` to extract just the values or just the errors from `results`:

```
[](#cb788-1)const values = results.flatMap(
[](#cb788-2)  result => result.value ? [result.value] : []);
[](#cb788-3)assert.deepEqual(values, [1, 6]);
[](#cb788-4) 
[](#cb788-5)const errors = results.flatMap(
[](#cb788-6)  result => result.error ? [result.error] : []);
[](#cb788-7)assert.deepEqual(errors, [new Error('Illegal value: -5')]);
```

#### 31.10.4.3 Use case: mapping to multiple values

The Array method `.map()` maps each input Array element to one output element. But what if we want to map it to multiple output elements?

That becomes necessary in the following example:

```
> stringsToCodePoints(['many', 'a', 'moon'])
['m', 'a', 'n', 'y', 'a', 'm', 'o', 'o', 'n']
```

We want to convert an Array of strings to an Array of Unicode characters (code points). The following function achieves that via `.flatMap()`:

```
[](#cb790-1)function stringsToCodePoints(strs) {
[](#cb790-2)  return strs.flatMap(str => [...str]);
[](#cb790-3)}
```

![](media/file6.svg)  **Exercises: `.flatMap()`**

*   `exercises/arrays/convert_to_numbers_test.mjs`

*   `exercises/arrays/replace_objects_test.mjs`

### 31.10.5 `.filter()`: only keep some of the elements

The Array method `.filter()` returns an Array collecting all elements for which the callback returns a truthy value.

For example:

```
> [-1, 2, 5, -7, 6].filter(x => x >= 0)
[ 2, 5, 6 ]
> ['a', 'b', 'c', 'd'].filter((_x,i) => (i%2)===0)
[ 'a', 'c' ]
```

`.filter()` can be implemented as follows:

```
[](#cb792-1)function filter(arr, filterFunc) {
[](#cb792-2)  const result = [];
[](#cb792-3)  for (const [i, x] of arr.entries()) {
[](#cb792-4)    if (filterFunc(x, i, arr)) {
[](#cb792-5)      result.push(x);
[](#cb792-6)    }
[](#cb792-7)  }
[](#cb792-8)  return result;
[](#cb792-9)}
```

![](media/file6.svg)  **Exercise: Removing empty lines via `.filter()`**

`exercises/arrays/remove_empty_lines_filter_test.mjs`

### 31.10.6 `.reduce()`: deriving a value from an Array (advanced)

Method `.reduce()` is a powerful tool for computing a “summary” of an Array `arr`. A summary can be any kind of value:

*   A number. For example, the sum of all elements of `arr`.
*   An Array. For example, a copy of `arr`, where each element is twice the original element.
*   Etc.

`reduce` is also known as `foldl` (“fold left”) in functional programming and popular there. One caveat is that it can make code difficult to understand.

`.reduce()` has the following type signature (inside an `Array<T>`):

```
[](#cb793-1).reduce<U>(
[](#cb793-2)  callback: (accumulator: U, element: T, index: number, array: T[]) => U,
[](#cb793-3)  init?: U)
[](#cb793-4)  : U
```

`T` is the type of the Array elements, `U` is the type of the summary. The two may or may not be different. `accumulator` is just another name for “summary”.

To compute the summary of an Array `arr`, `.reduce()` feeds all Array elements to its callback one at a time:

```
[](#cb794-1)const accumulator_0 = callback(init, arr[0]);
[](#cb794-2)const accumulator_1 = callback(accumulator_0, arr[1]);
[](#cb794-3)const accumulator_2 = callback(accumulator_1, arr[2]);
[](#cb794-4)// Etc.
```

`callback` combines the previously computed summary (stored in its parameter `accumulator`) with the current Array element and returns the next `accumulator`. The result of `.reduce()` is the final accumulator – the last result of `callback` after it has visited all elements.

In other words: `callback` does most of the work; `.reduce()` just invokes it in a useful manner.

You could say that the callback folds Array elements into the accumulator. That’s why this operation is called “fold” in functional programming.

#### 31.10.6.1 A first example

Let’s look at an example of `.reduce()` in action: function `addAll()` computes the sum of all numbers in an Array `arr`.

```
[](#cb795-1)function addAll(arr) {
[](#cb795-2)  const startSum = 0;
[](#cb795-3)  const callback = (sum, element) => sum + element;
[](#cb795-4)  return arr.reduce(callback, startSum);
[](#cb795-5)}
[](#cb795-6)assert.equal(addAll([1,  2, 3]), 6); // (A)
[](#cb795-7)assert.equal(addAll([7, -4, 2]), 5);
```

In this case, the accumulator holds the sum of all Array elements that `callback` has already visited.

How was the result `6` derived from the Array in line A? Via the following invocations of `callback`:

```
callback(0, 1) --> 1
callback(1, 2) --> 3
callback(3, 3) --> 6
```

Notes:

*   The first parameters are the current accumulators (starting with parameter `init` of `.reduce()`).
*   The second parameters are the current Array elements.
*   The results are the next accumulators.
*   The last result of `callback` is also the result of `.reduce()`.

Alternatively, we could have implemented `addAll()` via a `for-of` loop:

```
[](#cb797-1)function addAll(arr) {
[](#cb797-2)  let sum = 0;
[](#cb797-3)  for (const element of arr) {
[](#cb797-4)    sum = sum + element;
[](#cb797-5)  }
[](#cb797-6)  return sum;
[](#cb797-7)}
```

It’s hard to say which of the two implementations is “better”: the one based on `.reduce()` is a little more concise, while the one based on `for-of` may be a little easier to understand – especially if you are not familiar with functional programming.

#### 31.10.6.2 Example: finding indices via `.reduce()`

The following function is an implementation of the Array method `.indexOf()`. It returns the first index at which the given `searchValue` appears inside the Array `arr`:

```
[](#cb798-1)const NOT_FOUND = -1;
[](#cb798-2)function indexOf(arr, searchValue) {
[](#cb798-3)  return arr.reduce(
[](#cb798-4)    (result, elem, index) => {
[](#cb798-5)      if (result !== NOT_FOUND) {
[](#cb798-6)        // We have already found something: don’t change anything
[](#cb798-7)        return result;
[](#cb798-8)      } else if (elem === searchValue) {
[](#cb798-9)        return index;
[](#cb798-10)      } else {
[](#cb798-11)        return NOT_FOUND;
[](#cb798-12)      }
[](#cb798-13)    },
[](#cb798-14)    NOT_FOUND);
[](#cb798-15)}
[](#cb798-16)assert.equal(indexOf(['a', 'b', 'c'], 'b'), 1);
[](#cb798-17)assert.equal(indexOf(['a', 'b', 'c'], 'x'), -1);
```

One limitation of `.reduce()` is that you can’t finish early (in a `for-of` loop, you can `break`). Here, we always immediately return the result once we have found it.

#### 31.10.6.3 Example: doubling Array elements

Function `double(arr)` returns a copy of `inArr` whose elements are all multiplied by 2:

```
[](#cb799-1)function double(inArr) {
[](#cb799-2)  return inArr.reduce(
[](#cb799-3)    (outArr, element) => {
[](#cb799-4)      outArr.push(element * 2);
[](#cb799-5)      return outArr;
[](#cb799-6)    },
[](#cb799-7)    []);
[](#cb799-8)}
[](#cb799-9)assert.deepEqual(
[](#cb799-10)  double([1, 2, 3]),
[](#cb799-11)  [2, 4, 6]);
```

We modify the initial value `[]` by pushing into it. A non-destructive, more functional version of `double()` looks as follows:

```
[](#cb800-1)function double(inArr) {
[](#cb800-2)  return inArr.reduce(
[](#cb800-3)    // Don’t change `outArr`, return a fresh Array
[](#cb800-4)    (outArr, element) => [...outArr, element * 2],
[](#cb800-5)    []);
[](#cb800-6)}
[](#cb800-7)assert.deepEqual(
[](#cb800-8)  double([1, 2, 3]),
[](#cb800-9)  [2, 4, 6]);
```

This version is more elegant but also slower and uses more memory.

![](media/file6.svg)  **Exercises: `.reduce()`**

*   `map()` via `.reduce()`: `exercises/arrays/map_via_reduce_test.mjs`
*   `filter()` via `.reduce()`: `exercises/arrays/filter_via_reduce_test.mjs`
*   `countMatches()` via `.reduce()`: `exercises/arrays/count_matches_via_reduce_test.mjs`

## 31.11 `.sort()`: sorting Arrays

`.sort()` has the following type definition:

```
[](#cb801-1)sort(compareFunc?: (a: T, b: T) => number): this
```

By default, `.sort()` sorts string representations of the elements. These representations are compared via `<`. This operator compares *lexicographically* (the first characters are most significant). You can see that when sorting numbers:

```
> [200, 3, 10].sort()
[ 10, 200, 3 ]
```

When sorting human-language strings, you need to be aware that they are compared according to their code unit values (char codes):

```
> ['pie', 'cookie', 'éclair', 'Pie', 'Cookie', 'Éclair'].sort()
[ 'Cookie', 'Pie', 'cookie', 'pie', 'Éclair', 'éclair' ]
```

As you can see, all unaccented uppercase letters come before all unaccented lowercase letters, which come before all accented letters. Use `Intl`, [the JavaScript internationalization API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl), if you want proper sorting for human languages.

Note that `.sort()` sorts *in place*; it changes and returns its receiver:

```
> const arr = ['a', 'c', 'b'];
> arr.sort() === arr
true
> arr
[ 'a', 'b', 'c' ]
```

### 31.11.1 Customizing the sort order

You can customize the sort order via the parameter `compareFunc`, which must return a number that is:

*   negative if `a < b`
*   zero if `a === b`
*   positive if `a > b`

![](media/file2.svg)  **Tip for remembering these rules**

A negative number is *less than* zero (etc.).

### 31.11.2 Sorting numbers

You can use this helper function to sort numbers:

```
[](#cb805-1)function compareNumbers(a, b) {
[](#cb805-2)  if (a < b) {
[](#cb805-3)    return -1;
[](#cb805-4)  } else if (a === b) {
[](#cb805-5)    return 0;
[](#cb805-6)  } else {
[](#cb805-7)    return 1;
[](#cb805-8)  }
[](#cb805-9)}
[](#cb805-10)assert.deepEqual(
[](#cb805-11)  [200, 3, 10].sort(compareNumbers),
[](#cb805-12)  [3, 10, 200]);
```

The following is a quick and dirty alternative.

```
> [200, 3, 10].sort((a,b) => a - b)
[ 3, 10, 200 ]
```

The downsides of this approach are:

*   It is cryptic.
*   There is a risk of numeric overflow or underflow, if `a-b` becomes a large positive or negative number.

### 31.11.3 Sorting objects

You also need to use a compare function if you want to sort objects. As an example, the following code shows how to sort objects by age.

```
[](#cb807-1)const arr = [ {age: 200}, {age: 3}, {age: 10} ];
[](#cb807-2)assert.deepEqual(
[](#cb807-3)  arr.sort((obj1, obj2) => obj1.age - obj2.age),
[](#cb807-4)  [{ age: 3 }, { age: 10 }, { age: 200 }] );
```

![](media/file6.svg)  **Exercise: Sorting objects by name**

`exercises/arrays/sort_objects_test.mjs`

## 31.12 Quick reference: `Array<T>`

Legend:

*   `R`: method does not change the Array (non-destructive).
*   `W`: method changes the Array (destructive).

### 31.12.1 `new Array()`

`new Array(n)` creates an Array of length `n` that contains `n` holes:

```
[](#cb808-1)// Trailing commas are always ignored.
[](#cb808-2)// Therefore: number of commas = number of holes
[](#cb808-3)assert.deepEqual(new Array(3), [,,,]);
```

`new Array()` creates an empty Array. However, I recommend to always use `[]` instead.

### 31.12.2 Static methods of `Array`

*   `Array.from<T>(iterable: Iterable<T> | ArrayLike<T>): T[]` ^([ES6])

*   `Array.from<T,U>(iterable: Iterable<T> | ArrayLike<T>, mapFunc: (v: T, k: number) => U, thisArg?: any): U[]` ^([ES6])

    Converts an iterable or [an Array-like object](#ch032.xhtml_array-like-objects) to an Array. Optionally, the input values can be translated via `mapFunc` before they are added to the output Array.

    Examples:

    ```
    > Array.from(new Set(['a', 'b'])) // iterable
    [ 'a', 'b' ]
    > Array.from({length: 2, 0:'a', 1:'b'}) // Array-like object
    [ 'a', 'b' ]
    ```

*   `Array.of<T>(...items: T[]): T[]` ^([ES6])

    This static method is mainly useful for subclasses of `Array`, where it serves as a custom Array literal:

    ```
    [](#cb810-1)class MyArray extends Array {}
    [](#cb810-2)
    [](#cb810-3)assert.equal(
    [](#cb810-4)  MyArray.of('a', 'b') instanceof MyArray, true);
    ```

### 31.12.3 Methods of `Array<T>.prototype`

*   `.concat(...items: Array<T[] | T>): T[]` ^([R, ES3])

    Returns a new Array that is the concatenation of the receiver and all `items`. Non-Array parameters (such as `'b'` in the following example) are treated as if they were Arrays with single elements.

    ```
    > ['a'].concat('b', ['c', 'd'])
    [ 'a', 'b', 'c', 'd' ]
    ```

*   `.copyWithin(target: number, start: number, end=this.length): this` ^([W, ES6])

    Copies the elements whose indices range from (including) `start` to (excluding) `end` to indices starting with `target`. Overlapping is handled correctly.

    ```
    > ['a', 'b', 'c', 'd'].copyWithin(0, 2, 4)
    [ 'c', 'd', 'c', 'd' ]
    ```

    If `start` or `end` is negative, then `.length` is added to it.

*   `.entries(): Iterable<[number, T]>` ^([R, ES6])

    Returns an iterable over [index, element] pairs.

    ```
    > Array.from(['a', 'b'].entries())
    [ [ 0, 'a' ], [ 1, 'b' ] ]
    ```

*   `.every(callback: (value: T, index: number, array: Array<T>) => boolean, thisArg?: any): boolean` ^([R, ES5])

    Returns `true` if `callback` returns a truthy value for every element. Otherwise, it returns `false`. It stops as soon as it receives a falsy value. This method corresponds to universal quantification (“for all”, `∀`) in mathematics.

    ```
    > [1, 2, 3].every(x => x > 0)
    true
    > [1, -2, 3].every(x => x > 0)
    false
    ```

    Related method: `.some()` (“exists”).

*   `.fill(value: T, start=0, end=this.length): this` ^([W, ES6])

    Assigns `value` to every index between (including) `start` and (excluding) `end`.

    ```
    > [0, 1, 2].fill('a')
    [ 'a', 'a', 'a' ]
    ```

    Caveat: Don’t use this method to fill an Array with an object `obj`; then each element will refer to `obj` (sharing it). In this case, it’s better to [use `Array.from()`](#ch032.xhtml_filling-arrays).

*   `.filter(callback: (value: T, index: number, array: Array<T>) => any, thisArg?: any): T[]` ^([R, ES5])

    Returns an Array with only those elements for which `callback` returns a truthy value.

    ```
    > [1, -2, 3].filter(x => x > 0)
    [ 1, 3 ]
    ```

*   `.find(predicate: (value: T, index: number, obj: T[]) => boolean, thisArg?: any): T | undefined` ^([R, ES6])

    The result is the first element for which `predicate` returns a truthy value. If there is no such element, the result is `undefined`.

    ```
    > [1, -2, 3].find(x => x < 0)
    -2
    > [1, 2, 3].find(x => x < 0)
    undefined
    ```

*   `.findIndex(predicate: (value: T, index: number, obj: T[]) => boolean, thisArg?: any): number` ^([R, ES6])

    The result is the index of the first element for which `predicate` returns a truthy value. If there is no such element, the result is `-1`.

    ```
    > [1, -2, 3].findIndex(x => x < 0)
    1
    > [1, 2, 3].findIndex(x => x < 0)
    -1
    ```

*   `.flat(depth = 1): any[]` ^([R, ES2019])

    “Flattens” an Array: It descends into the Arrays that are nested inside the input Array and creates a copy where all values it finds at level `depth` or lower are moved to the top level.

    ```
    > [ 1,2, [3,4], [[5,6]] ].flat(0) // no change
    [ 1, 2, [3,4], [[5,6]] ]

    > [ 1,2, [3,4], [[5,6]] ].flat(1)
    [1, 2, 3, 4, [5,6]]

    > [ 1,2, [3,4], [[5,6]] ].flat(2)
    [1, 2, 3, 4, 5, 6]
    ```

*   `.flatMap<U>(callback: (value: T, index: number, array: T[]) => U|Array<U>, thisValue?: any): U[]` ^([R, ES2019])

    The result is produced by invoking `callback()` for each element of the original Array and concatenating the Arrays it returns.

    ```
    > ['a', 'b', 'c'].flatMap(x => [x,x])
    [ 'a', 'a', 'b', 'b', 'c', 'c' ]
    > ['a', 'b', 'c'].flatMap(x => [x])
    [ 'a', 'b', 'c' ]
    > ['a', 'b', 'c'].flatMap(x => [])
    []
    ```

*   `.forEach(callback: (value: T, index: number, array: Array<T>) => void, thisArg?: any): void` ^([R, ES5])

    Calls `callback` for each element.

    ```
    [](#cb821-1)['a', 'b'].forEach((x, i) => console.log(x, i))
    [](#cb821-2)
    [](#cb821-3)// Output:
    [](#cb821-4)// 'a', 0
    [](#cb821-5)// 'b', 1
    ```

    A `for-of` loop is usually a better choice: it’s faster, supports `break` and can iterate over arbitrary iterables.

*   `.includes(searchElement: T, fromIndex=0): boolean` ^([R, ES2016])

    Returns `true` if the receiver has an element whose value is `searchElement` and `false`, otherwise. Searching starts at index `fromIndex`.

    ```
    > [0, 1, 2].includes(1)
    true
    > [0, 1, 2].includes(5)
    false
    ```

*   `.indexOf(searchElement: T, fromIndex=0): number` ^([R, ES5])

    Returns the index of the first element that is strictly equal to `searchElement`. Returns `-1` if there is no such element. Starts searching at index `fromIndex`, visiting higher indices next.

    ```
    > ['a', 'b', 'a'].indexOf('a')
    0
    > ['a', 'b', 'a'].indexOf('a', 1)
    2
    > ['a', 'b', 'a'].indexOf('c')
    -1
    ```

*   `.join(separator = ','): string` ^([R, ES1])

    Creates a string by concatenating string representations of all elements, separating them with `separator`.

    ```
    > ['a', 'b', 'c'].join('##')
    'a##b##c'
    > ['a', 'b', 'c'].join()
    'a,b,c'
    ```

*   `.keys(): Iterable<number>` ^([R, ES6])

    Returns an iterable over the keys of the receiver.

    ```
    > [...['a', 'b'].keys()]
    [ 0, 1 ]
    ```

*   `.lastIndexOf(searchElement: T, fromIndex=this.length-1): number` ^([R, ES5])

    Returns the index of the last element that is strictly equal to `searchElement`. Returns `-1` if there is no such element. Starts searching at index `fromIndex`, visiting lower indices next.

    ```
    > ['a', 'b', 'a'].lastIndexOf('a')
    2
    > ['a', 'b', 'a'].lastIndexOf('a', 1)
    0
    > ['a', 'b', 'a'].lastIndexOf('c')
    -1
    ```

*   `.map<U>(mapFunc: (value: T, index: number, array: Array<T>) => U, thisArg?: any): U[]` ^([R, ES5])

    Returns a new Array, in which every element is the result of `mapFunc` being applied to the corresponding element of the receiver.

    ```
    > [1, 2, 3].map(x => x * 2)
    [ 2, 4, 6 ]
    > ['a', 'b', 'c'].map((x, i) => i)
    [ 0, 1, 2 ]
    ```

*   `.pop(): T | undefined` ^([W, ES3])

    Removes and returns the last element of the receiver. That is, it treats the end of the receiver as a stack. The opposite of `.push()`.

    ```
    > const arr = ['a', 'b', 'c'];
    > arr.pop()
    'c'
    > arr
    [ 'a', 'b' ]
    ```

*   `.push(...items: T[]): number` ^([W, ES3])

    Adds zero or more `items` to the end of the receiver. That is, it treats the end of the receiver as a stack. The return value is the length of the receiver after the change. The opposite of `.pop()`.

    ```
    > const arr = ['a', 'b'];
    > arr.push('c', 'd')
    4
    > arr
    [ 'a', 'b', 'c', 'd' ]
    ```

*   `.reduce<U>(callback: (accumulator: U, element: T, index: number, array: T[]) => U, init?: U): U` ^([R, ES5])

    This method produces a summary of the receiver: it feeds all Array elements to `callback`, which combines a current summary (in parameter `accumulator`) with the current Array element and returns the next `accumulator`:

    ```
    [](#cb830-1)const accumulator_0 = callback(init, arr[0]);
    [](#cb830-2)const accumulator_1 = callback(accumulator_0, arr[1]);
    [](#cb830-3)const accumulator_2 = callback(accumulator_1, arr[2]);
    [](#cb830-4)// Etc.
    ```

    The result of `.reduce()` is the last result of `callback` after it has visited all Array elements.

    ```
    > [1, 2, 3].reduce((accu, x) => accu + x, 0)
    6
    > [1, 2, 3].reduce((accu, x) => accu + String(x), '')
    '123'
    ```

    If no `init` is provided, the Array element at index 0 is used and the element at index 1 is visited first. Therefore, the Array must have at least length 1.

*   `.reduceRight<U>(callback: (accumulator: U, element: T, index: number, array: T[]) => U, init?: U): U` ^([R, ES5])

    Works like `.reduce()`, but visits the Array elements backward, starting with the last element.

    ```
    > [1, 2, 3].reduceRight((accu, x) => accu + String(x), '')
    '321'
    ```

*   `.reverse(): this` ^([W, ES1])

    Rearranges the elements of the receiver so that they are in reverse order and then returns the receiver.

    ```
    > const arr = ['a', 'b', 'c'];
    > arr.reverse()
    [ 'c', 'b', 'a' ]
    > arr
    [ 'c', 'b', 'a' ]
    ```

*   `.shift(): T | undefined` ^([W, ES3])

    Removes and returns the first element of the receiver. The opposite of `.unshift()`.

    ```
    > const arr = ['a', 'b', 'c'];
    > arr.shift()
    'a'
    > arr
    [ 'b', 'c' ]
    ```

*   `.slice(start=0, end=this.length): T[]` ^([R, ES3])

    Returns a new Array containing the elements of the receiver whose indices are between (including) `start` and (excluding) `end`.

    ```
    > ['a', 'b', 'c', 'd'].slice(1, 3)
    [ 'b', 'c' ]
    > ['a', 'b'].slice() // shallow copy
    [ 'a', 'b' ]
    ```

    Negative indices are allowed and added to `.length`:

    ```
    > ['a', 'b', 'c'].slice(-2)
    [ 'b', 'c' ]
    ```

*   `.some(callback: (value: T, index: number, array: Array<T>) => boolean, thisArg?: any): boolean` ^([R, ES5])

    Returns `true` if `callback` returns a truthy value for at least one element. Otherwise, it returns `false`. It stops as soon as it receives a truthy value. This method corresponds to existential quantification (“exists”, `∃`) in mathematics.

    ```
    > [1, 2, 3].some(x => x < 0)
    false
    > [1, -2, 3].some(x => x < 0)
    true
    ```

    Related method: `.every()` (“for all”).

*   `.sort(compareFunc?: (a: T, b: T) => number): this` ^([W, ES1])

    Sorts the receiver and returns it. By default, it sorts string representations of the elements. It does so lexicographically and according to the code unit values (char codes) of the characters:

    ```
    > ['pie', 'cookie', 'éclair', 'Pie', 'Cookie', 'Éclair'].sort()
    [ 'Cookie', 'Pie', 'cookie', 'pie', 'Éclair', 'éclair' ]
    > [200, 3, 10].sort()
    [ 10, 200, 3 ]
    ```

    You can customize the sort order via `compareFunc`, which returns a number that is:

    *   negative if `a < b`
    *   zero if `a === b`
    *   positive if `a > b`

    Trick for sorting numbers (with a risk of numeric overflow or underflow):

    ```
    > [200, 3, 10].sort((a, b) => a - b)
    [ 3, 10, 200 ]
    ```

    ![](media/file5.svg)  **`.sort()` is stable**

    Since ECMAScript 2019, sorting is guaranteed to be stable: if elements are considered equal by sorting, then sorting does not change the order of those elements (relative to each other).

*   `.splice(start: number, deleteCount=this.length-start, ...items: T[]): T[]` ^([W, ES3])

    At index `start`, it removes `deleteCount` elements and inserts the `items`. It returns the deleted elements.

    ```
    > const arr = ['a', 'b', 'c', 'd'];
    > arr.splice(1, 2, 'x', 'y')
    [ 'b', 'c' ]
    > arr
    [ 'a', 'x', 'y', 'd' ]
    ```

    `start` can be negative and is added to `.length` if it is:

    ```
    > ['a', 'b', 'c'].splice(-2, 2)
    [ 'b', 'c' ]
    ```

*   `.toString(): string` ^([R, ES1])

    Converts all elements to strings via `String()`, concatenates them while separating them with commas, and returns the result.

    ```
    > [1, 2, 3].toString()
    '1,2,3'
    > ['1', '2', '3'].toString()
    '1,2,3'
    > [].toString()
    ''
    ```

*   `.unshift(...items: T[]): number` ^([W, ES3])

    Inserts the `items` at the beginning of the receiver and returns its length after this modification.

    ```
    > const arr = ['c', 'd'];
    > arr.unshift('e', 'f')
    4
    > arr
    [ 'e', 'f', 'c', 'd' ]
    ```

*   `.values(): Iterable<T>` ^([R, ES6])

    Returns an iterable over the values of the receiver.

    ```
    > [...['a', 'b'].values()]
    [ 'a', 'b' ]
    ```

### 31.12.4 Sources

*   [TypeScript’s built-in typings](https://github.com/Microsoft/TypeScript/blob/master/lib/)
*   [MDN web docs for JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
*   [ECMAScript language specification](https://tc39.github.io/ecma262/)

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 32 Typed Arrays: handling binary data (Advanced)

* * *

*   32.1 [The basics of the API](#ch033.xhtml_the-basics-of-the-api)
    *   32.1.1 [Use cases for Typed Arrays](#ch033.xhtml_use-cases-for-typed-arrays)
    *   32.1.2 [The core classes: `ArrayBuffer`, Typed Arrays, `DataView`](#ch033.xhtml_the-core-classes-arraybuffer-typed-arrays-dataview)
    *   32.1.3 [Using Typed Arrays](#ch033.xhtml_using-typed-arrays)
    *   32.1.4 [Using DataViews](#ch033.xhtml_using-dataviews)
*   32.2 [Element types](#ch033.xhtml_element-types)
    *   32.2.1 [Handling overflow and underflow](#ch033.xhtml_handling-overflow-underflow)
    *   32.2.2 [Endianness](#ch033.xhtml_endianness)
*   32.3 [More information on Typed Arrays](#ch033.xhtml_more-information-on-typed-arrays)
    *   32.3.1 [The static method `«ElementType»Array.from()`](#ch033.xhtml_the-static-method-elementtypearray.from)
    *   32.3.2 [Typed Arrays are iterable](#ch033.xhtml_typed-arrays-are-iterable)
    *   32.3.3 [Typed Arrays vs. normal Arrays](#ch033.xhtml_typed-arrays-vs.-normal-arrays)
    *   32.3.4 [Converting Typed Arrays to and from normal Arrays](#ch033.xhtml_converting-typed-arrays-to-and-from-normal-arrays)
    *   32.3.5 [Concatenating Typed Arrays](#ch033.xhtml_concatenating-typed-arrays)
*   32.4 [Quick references: indices vs. offsets](#ch033.xhtml_typed-arrays-indices-offsets)
*   32.5 [Quick reference: ArrayBuffers](#ch033.xhtml_quick-reference-arraybuffers)
    *   32.5.1 [`new ArrayBuffer()`](#ch033.xhtml_new-arraybuffer)
    *   32.5.2 [Static methods of `ArrayBuffer`](#ch033.xhtml_static-methods-of-arraybuffer)
    *   32.5.3 [Properties of `ArrayBuffer.prototype`](#ch033.xhtml_properties-of-arraybuffer.prototype)
*   32.6 [Quick reference: Typed Arrays](#ch033.xhtml_quick-reference-typed-arrays)
    *   32.6.1 [Static methods of `TypedArray<T>`](#ch033.xhtml_static-methods-of-typedarrayt)
    *   32.6.2 [Properties of `TypedArray<T>.prototype`](#ch033.xhtml_properties-of-typedarrayt.prototype)
    *   32.6.3 [`new «ElementType»Array()`](#ch033.xhtml_new-elementtypearray)
    *   32.6.4 [Static properties of `«ElementType»Array`](#ch033.xhtml_static-properties-of-elementtypearray)
    *   32.6.5 [Properties of `«ElementType»Array.prototype`](#ch033.xhtml_properties-of-elementtypearray.prototype)
*   32.7 [Quick reference: DataViews](#ch033.xhtml_quick-reference-dataviews)
    *   32.7.1 [`new DataView()`](#ch033.xhtml_new-dataview)
    *   32.7.2 [Properties of `DataView.prototype`](#ch033.xhtml_properties-of-dataview.prototype)

* * *

## 32.1 The basics of the API

Much data on the web is text: JSON files, HTML files, CSS files, JavaScript code, etc. JavaScript handles such data well via its built-in strings.

However, before 2011, it did not handle binary data well. [The Typed Array Specification 1.0](https://www.khronos.org/registry/typedarray/specs/1.0/) was introduced on February 8, 2011 and provides tools for working with binary data. With ECMAScript 6, Typed Arrays were added to the core language and gained methods that were previously only available for normal Arrays (`.map()`, `.filter()`, etc.).

### 32.1.1 Use cases for Typed Arrays

The main uses cases for Typed Arrays, are:

*   Processing binary data: managing image data, manipulating binary files, handling binary network protocols, etc.
*   Interacting with native APIs: Native APIs often receive and return data in a binary format, which you could neither store nor manipulate well in pre-ES6 JavaScript. That meant that whenever you were communicating with such an API, data had to be converted from JavaScript to binary and back for every call. Typed Arrays eliminate this bottleneck. One example of communicating with native APIs is WebGL, for which Typed Arrays were initially created. Section [“History of Typed Arrays”](http://www.html5rocks.com/en/tutorials/webgl/typed_arrays/#toc-history) of the article [“Typed Arrays: Binary Data in the Browser”](http://www.html5rocks.com/en/tutorials/webgl/typed_arrays/#toc-history) (by Ilmari Heikkinen for HTML5 Rocks) has more information.

### 32.1.2 The core classes: `ArrayBuffer`, Typed Arrays, `DataView`

The Typed Array API stores binary data in instances of `ArrayBuffer`:

```
[](#cb845-1)const buf = new ArrayBuffer(4); // length in bytes
[](#cb845-2)  // buf is initialized with zeros
```

An ArrayBuffer itself is a black box: if you want to access its data, you must wrap it in another object – a *view object*. Two kinds of view objects are available:

*   Typed Arrays: let you access the data as an indexed sequence of elements that all have the same type. Examples include:
    *   `Uint8Array`: Elements are unsigned 8-bit integers. *Unsigned* means that their ranges start at zero.
    *   `Int16Array`: Elements are signed 16-bit integers. *Signed* means that they have a sign and can be negative, zero, or positive.
    *   `Float32Array`: Elements are 32-bit floating point numbers.
*   DataViews: let you interpret the data as various types (`Uint8`, `Int16`, `Float32`, etc.) that you can read and write at any byte offset.

Fig. [29](#ch033.xhtml_fig:typed_arrays_class_diagram) shows a class diagram of the API.

![](media/file38.jpg)

Figure 29: The classes of the Typed Array API.

### 32.1.3 Using Typed Arrays

Typed Arrays are used much like normal Arrays with a few notable differences:

*   Typed Arrays store their data in ArrayBuffers.
*   All elements are initialized with zeros.
*   All elements have the same type. Writing values to a Typed Array coerces them to that type. Reading values produces normal numbers.
*   The length of a Typed Array is immutable; it can’t be changed.
*   Typed Arrays can’t have holes.

#### 32.1.3.1 Creating Typed Arrays

The following code shows three different ways of creating the same Typed Array:

```
[](#cb846-1)// Argument: Typed Array or Array-like object
[](#cb846-2)const ta1 = new Uint8Array([0, 1, 2]);
[](#cb846-3)
[](#cb846-4)const ta2 = Uint8Array.of(0, 1, 2);
[](#cb846-5)
[](#cb846-6)const ta3 = new Uint8Array(3); // length of Typed Array
[](#cb846-7)ta3[0] = 0;
[](#cb846-8)ta3[1] = 1;
[](#cb846-9)ta3[2] = 2;
[](#cb846-10)
[](#cb846-11)assert.deepEqual(ta1, ta2);
[](#cb846-12)assert.deepEqual(ta1, ta3);
```

#### 32.1.3.2 The wrapped ArrayBuffer

```
[](#cb847-1)const typedArray = new Int16Array(2); // 2 elements
[](#cb847-2)assert.equal(typedArray.length, 2);
[](#cb847-3)
[](#cb847-4)assert.deepEqual(
[](#cb847-5)  typedArray.buffer, new ArrayBuffer(4)); // 4 bytes
```

#### 32.1.3.3 Getting and setting elements

```
[](#cb848-1)const typedArray = new Int16Array(2);
[](#cb848-2)
[](#cb848-3)assert.equal(typedArray[1], 0); // initialized with 0
[](#cb848-4)typedArray[1] = 72;
[](#cb848-5)assert.equal(typedArray[1], 72);
```

### 32.1.4 Using DataViews

This is how DataViews are used:

```
[](#cb849-1)const dataView = new DataView(new ArrayBuffer(4));
[](#cb849-2)assert.equal(dataView.getInt16(0), 0);
[](#cb849-3)assert.equal(dataView.getUint8(0), 0);
[](#cb849-4)dataView.setUint8(0, 5);
```

## 32.2 Element types

Table 19: Element types supported by the Typed Array API.

| Element | Typed Array | Bytes | Description |  |
| --- | --- | --- | --- | --- |
| `Int8` | `Int8Array` | 1 | 8-bit signed integer | ES6 |
| `Uint8` | `Uint8Array` | 1 | 8-bit unsigned integer | ES6 |
| `Uint8C` | `Uint8ClampedArray` | 1 | 8-bit unsigned integer | ES6 |
|  |  |  | (clamped conversion) | ES6 |
| `Int16` | `Int16Array` | 2 | 16-bit signed integer | ES6 |
| `Uint16` | `Uint16Array` | 2 | 16-bit unsigned integer | ES6 |
| `Int32` | `Int32Array` | 4 | 32-bit signed integer | ES6 |
| `Uint32` | `Uint32Array` | 4 | 32-bit unsigned integer | ES6 |
| `Float32` | `Float32Array` | 4 | 32-bit floating point | ES6 |
| `Float64` | `Float64Array` | 8 | 64-bit floating point | ES6 |

Tbl. [19](#ch033.xhtml_tbl:typed-array-element-types) lists the available element types. These types (e.g., `Int32`) show up in two locations:

*   They are the types of the elements of Typed Arrays. For example, all elements of a `Int32Array` have the type `Int32`. The element type is the only aspect of Typed Arrays that differs.
*   They are the lenses through which an ArrayBuffer accesses its DataView when you use methods such as `.getInt32()` and `.setInt32()`.

The element type `Uint8C` is special: it is not supported by `DataView` and only exists to enable `Uint8ClampedArray`. This Typed Array is used by the `canvas` element (where it replaces `CanvasPixelArray`) and should otherwise be avoided. The only difference between `Uint8C` and `Uint8` is how overflow and underflow are handled (as explained in the next subsection).

### 32.2.1 Handling overflow and underflow

Normally, when a value is out of the range of the element type, modulo arithmetic is used to convert it to a value within range. For signed and unsigned integers that means that:

*   The highest value plus one is converted to the lowest value (0 for unsigned integers).
*   The lowest value minus one is converted to the highest value.

The following function helps illustrate how conversion works:

```
[](#cb850-1)function setAndGet(typedArray, value) {
[](#cb850-2)  typedArray[0] = value;
[](#cb850-3)  return typedArray[0];
[](#cb850-4)}
```

Modulo conversion for unsigned 8-bit integers:

```
[](#cb851-1)const uint8 = new Uint8Array(1);
[](#cb851-2)
[](#cb851-3)// Highest value of range
[](#cb851-4)assert.equal(setAndGet(uint8, 255), 255);
[](#cb851-5)// Overflow
[](#cb851-6)assert.equal(setAndGet(uint8, 256), 0);
[](#cb851-7)
[](#cb851-8)// Lowest value of range
[](#cb851-9)assert.equal(setAndGet(uint8, 0), 0);
[](#cb851-10)// Underflow
[](#cb851-11)assert.equal(setAndGet(uint8, -1), 255);
```

Modulo conversion for signed 8-bit integers:

```
[](#cb852-1)const int8 = new Int8Array(1);
[](#cb852-2)
[](#cb852-3)// Highest value of range
[](#cb852-4)assert.equal(setAndGet(int8, 127), 127);
[](#cb852-5)// Overflow
[](#cb852-6)assert.equal(setAndGet(int8, 128), -128);
[](#cb852-7)
[](#cb852-8)// Lowest value of range
[](#cb852-9)assert.equal(setAndGet(int8, -128), -128);
[](#cb852-10)// Underflow
[](#cb852-11)assert.equal(setAndGet(int8, -129), 127);
```

Clamped conversion is different:

*   All underflowing values are converted to the lowest value.
*   All overflowing values are converted to the highest value.

```
[](#cb853-1)const uint8c = new Uint8ClampedArray(1);
[](#cb853-2)
[](#cb853-3)// Highest value of range
[](#cb853-4)assert.equal(setAndGet(uint8c, 255), 255);
[](#cb853-5)// Overflow
[](#cb853-6)assert.equal(setAndGet(uint8c, 256), 255);
[](#cb853-7)
[](#cb853-8)// Lowest value of range
[](#cb853-9)assert.equal(setAndGet(uint8c, 0), 0);
[](#cb853-10)// Underflow
[](#cb853-11)assert.equal(setAndGet(uint8c, -1), 0);
```

### 32.2.2 Endianness

Whenever a type (such as `Uint16`) is stored as a sequence of multiple bytes, *endianness* matters:

*   Big endian: the most significant byte comes first. For example, the `Uint16` value 0x4321 is stored as two bytes – first 0x43, then 0x21\.
*   Little endian: the least significant byte comes first. For example, the `Uint16` value 0x4321 is stored as two bytes – first 0x21, then 0x43\.

Endianness tends to be fixed per CPU architecture and consistent across native APIs. Typed Arrays are used to communicate with those APIs, which is why their endianness follows the endianness of the platform and can’t be changed.

On the other hand, the endianness of protocols and binary files varies, but is fixed per format, across platforms. Therefore, we must be able to access data with either endianness. DataViews serve this use case and let you specify endianness when you get or set a value.

[Quoting Wikipedia on Endianness](https://en.wikipedia.org/wiki/Endianness):

*   Big-endian representation is the most common convention in data networking; fields in the protocols of the Internet protocol suite, such as IPv4, IPv6, TCP, and UDP, are transmitted in big-endian order. For this reason, big-endian byte order is also referred to as network byte order.
*   Little-endian storage is popular for microprocessors in part due to significant historical influence on microprocessor designs by Intel Corporation.

Other orderings are also possible. Those are generically called *middle-endian* or *mixed-endian*.

## 32.3 More information on Typed Arrays

In this section, `«ElementType»Array` stands for `Int8Array`, `Uint8Array`, etc. `ElementType` is `Int8`, `Uint8`, etc.

### 32.3.1 The static method `«ElementType»Array.from()`

This method has the type signature:

```
[](#cb854-1).from<S>(
[](#cb854-2)  source: Iterable<S>|ArrayLike<S>,
[](#cb854-3)  mapfn?: S => ElementType, thisArg?: any)
[](#cb854-4)  : «ElementType»Array
```

`.from()` converts `source` into an instance of `this` (a Typed Array).

For example, normal Arrays are iterable and can be converted with this method:

```
[](#cb855-1)assert.deepEqual(
[](#cb855-2)  Uint16Array.from([0, 1, 2]),
[](#cb855-3)  Uint16Array.of(0, 1, 2));
```

Typed Arrays are also iterable:

```
[](#cb856-1)assert.deepEqual(
[](#cb856-2)  Uint16Array.from(Uint8Array.of(0, 1, 2)),
[](#cb856-3)  Uint16Array.of(0, 1, 2));
```

`source` can also be [an *Array-like object*](#ch032.xhtml_array-like-objects):

```
[](#cb857-1)assert.deepEqual(
[](#cb857-2)  Uint16Array.from({0:0, 1:1, 2:2, length: 3}),
[](#cb857-3)  Uint16Array.of(0, 1, 2));
```

The optional `mapfn` lets you transform the elements of `source` before they become elements of the result. Why perform the two steps *mapping* and *conversion* in one go? Compared to mapping separately via `.map()`, there are two advantages:

1.  No intermediate Array or Typed Array is needed.
2.  When converting between Typed Arrays with different precisions, less can go wrong.

Read on for an explanation of the second advantage.

#### 32.3.1.1 Pitfall: mapping while converting between Typed Array types

The static method `.from()` can optionally both map and convert between Typed Array types. Less can go wrong if you use that method.

To see why that is, let us first convert a Typed Array to a Typed Array with a higher precision. If we use `.from()` to map, the result is automatically correct. Otherwise, you must first convert and then map.

```
[](#cb858-1)const typedArray = Int8Array.of(127, 126, 125);
[](#cb858-2)assert.deepEqual(
[](#cb858-3)  Int16Array.from(typedArray, x => x * 2),
[](#cb858-4)  Int16Array.of(254, 252, 250));
[](#cb858-5)
[](#cb858-6)assert.deepEqual(
[](#cb858-7)  Int16Array.from(typedArray).map(x => x * 2),
[](#cb858-8)  Int16Array.of(254, 252, 250)); // OK
[](#cb858-9)assert.deepEqual(
[](#cb858-10)  Int16Array.from(typedArray.map(x => x * 2)),
[](#cb858-11)  Int16Array.of(-2, -4, -6)); // wrong
```

If we go from a Typed Array to a Typed Array with a lower precision, mapping via `.from()` produces the correct result. Otherwise, we must first map and then convert.

```
[](#cb859-1)assert.deepEqual(
[](#cb859-2)  Int8Array.from(Int16Array.of(254, 252, 250), x => x / 2),
[](#cb859-3)  Int8Array.of(127, 126, 125));
[](#cb859-4)
[](#cb859-5)assert.deepEqual(
[](#cb859-6)  Int8Array.from(Int16Array.of(254, 252, 250).map(x => x / 2)),
[](#cb859-7)  Int8Array.of(127, 126, 125)); // OK
[](#cb859-8)assert.deepEqual(
[](#cb859-9)  Int8Array.from(Int16Array.of(254, 252, 250)).map(x => x / 2),
[](#cb859-10)  Int8Array.of(-1, -2, -3)); // wrong
```

The problem is that if we map via `.map()`, then input type and output type are the same. In contrast, `.from()` goes from an arbitrary input type to an output type that you specify via its receiver.

### 32.3.2 Typed Arrays are iterable

Typed Arrays are [iterable](#ch031.xhtml_ch_sync-iteration). That means that you can use the `for-of` loop and other iteration-based mechanisms:

```
[](#cb860-1)const ui8 = Uint8Array.of(0, 1, 2);
[](#cb860-2)for (const byte of ui8) {
[](#cb860-3)  console.log(byte);
[](#cb860-4)}
[](#cb860-5)// Output:
[](#cb860-6)// 0
[](#cb860-7)// 1
[](#cb860-8)// 2
```

ArrayBuffers and DataViews are not iterable.

### 32.3.3 Typed Arrays vs. normal Arrays

Typed Arrays are much like normal Arrays: they have a `.length`, elements can be accessed via the bracket operator `[]`, and they have most of the standard Array methods. They differ from normal Arrays in the following ways:

*   Typed Arrays have buffers. The elements of a Typed Array `ta` are not stored in `ta`, they are stored in an associated ArrayBuffer that can be accessed via `ta.buffer`:

    ```
    [](#cb861-1)const ta = new Uint16Array(2); // 2 elements
    [](#cb861-2)assert.deepEqual(
    [](#cb861-3)  ta.buffer, new ArrayBuffer(4)); // 4 bytes
    ```

*   Typed Arrays are initialized with zeros:

    *   `new Array(4)` creates a normal Array without any elements. It only has four *holes* (indices less than the `.length` that have no associated elements).
    *   `new Uint8Array(4)` creates a Typed Array whose four elements are all 0.

    ```
    [](#cb862-1)assert.deepEqual(new Uint8Array(4), Uint8Array.of(0, 0, 0, 0));
    ```

*   All of the elements of a Typed Array have the same type:

    *   Setting elements converts values to that type.

        ```
        [](#cb863-1)const ta = new Uint8Array(1);
        [](#cb863-2)
        [](#cb863-3)ta[0] = 257;
        [](#cb863-4)assert.equal(ta[0], 1); // 257 % 256 (overflow)
        [](#cb863-5)
        [](#cb863-6)ta[0] = '2';
        [](#cb863-7)assert.equal(ta[0], 2);
        ```

    *   Getting elements returns numbers.

        ```
        [](#cb864-1)const ta = new Uint8Array(1);
        [](#cb864-2)assert.equal(ta[0], 0);
        [](#cb864-3)assert.equal(typeof ta[0], 'number');
        ```

*   The `.length` of a Typed Array is derived from its ArrayBuffer and never changes (unless you switch to a different ArrayBuffer).

*   Normal Arrays can have holes; Typed Arrays can’t.

### 32.3.4 Converting Typed Arrays to and from normal Arrays

To convert a normal Array to a Typed Array, you pass it to a Typed Array constructor (which accepts Array-like objects and Typed Arrays) or to `«ElementType»Array.from()` (which accepts iterables and Array-like objects). For example:

```
[](#cb865-1)const ta1 = new Uint8Array([0, 1, 2]);
[](#cb865-2)const ta2 = Uint8Array.from([0, 1, 2]);
[](#cb865-3)assert.deepEqual(ta1, ta2);
```

To convert a Typed Array to a normal Array, you can use spreading or `Array.from()` (because Typed Arrays are iterable):

```
[](#cb866-1)assert.deepEqual(
[](#cb866-2)  [...Uint8Array.of(0, 1, 2)], [0, 1, 2] );
[](#cb866-3)assert.deepEqual(
[](#cb866-4)  Array.from(Uint8Array.of(0, 1, 2)), [0, 1, 2] );
```

### 32.3.5 Concatenating Typed Arrays

Typed Arrays don’t have a method `.concat()`, like normal Arrays do. The workaround is to use their overloaded method `.set()`:

```
[](#cb867-1).set(typedArray: TypedArray, offset=0): void
[](#cb867-2).set(arrayLike: ArrayLike<number>, offset=0): void
```

It copies the existing `typedArray` or `arrayLike` into the receiver, at index `offset`. `TypedArray` is a fictitious abstract superclass of all concrete Typed Array classes.

The following function uses that method to copy zero or more Typed Arrays (or Array-like objects) into an instance of `resultConstructor`:

```
[](#cb868-1)function concatenate(resultConstructor, ...arrays) {
[](#cb868-2)  let totalLength = 0;
[](#cb868-3)  for (const arr of arrays) {
[](#cb868-4)    totalLength += arr.length;
[](#cb868-5)  }
[](#cb868-6)  const result = new resultConstructor(totalLength);
[](#cb868-7)  let offset = 0;
[](#cb868-8)  for (const arr of arrays) {
[](#cb868-9)    result.set(arr, offset);
[](#cb868-10)    offset += arr.length;
[](#cb868-11)  }
[](#cb868-12)  return result;
[](#cb868-13)}
[](#cb868-14)assert.deepEqual(
[](#cb868-15)  concatenate(Uint8Array, Uint8Array.of(1, 2), [3, 4]),
[](#cb868-16)  Uint8Array.of(1, 2, 3, 4));
```

## 32.4 Quick references: indices vs. offsets

In preparation for the quick references on ArrayBuffers, Typed Arrays, and DataViews, we need learn the differences between indices and offsets:

*   Indices for the bracket operator `[ ]`: You can only use non-negative indices (starting at 0).

    In normal Arrays, writing to negative indices creates properties:

    ```
    [](#cb869-1)const arr = [6, 7];
    [](#cb869-2)arr[-1] = 5;
    [](#cb869-3)assert.deepEqual(
    [](#cb869-4)  Object.keys(arr), ['0', '1', '-1']);
    ```

    In Typed Arrays, writing to negative indices is ignored:

    ```
    [](#cb870-1)const tarr = Uint8Array.of(6, 7);
    [](#cb870-2)tarr[-1] = 5;
    [](#cb870-3)assert.deepEqual(
    [](#cb870-4)  Object.keys(tarr), ['0', '1']);
    ```

*   Indices for methods of ArrayBuffers, Typed Arrays, and DataViews: Every index can be negative. If it is, it is added to the length of the entity to produce the actual index. Therefore, `-1` refers to the last element, `-2` to the second-last, etc. Methods of normal Arrays work the same way.

    ```
    [](#cb871-1)const ui8 = Uint8Array.of(0, 1, 2);
    [](#cb871-2)assert.deepEqual(ui8.slice(-1), Uint8Array.of(2));
    ```

*   Offsets passed to methods of Typed Arrays and DataViews: must be non-negative – for example:

    ```
    [](#cb872-1)const dataView = new DataView(new ArrayBuffer(4));
    [](#cb872-2)assert.throws(
    [](#cb872-3)  () => dataView.getUint8(-1),
    [](#cb872-4)  {
    [](#cb872-5)    name: 'RangeError',
    [](#cb872-6)    message: 'Offset is outside the bounds of the DataView',
    [](#cb872-7)  });
    ```

Whether a parameter is an index or an offset can only be determined by looking at documentation; there is no simple rule.

## 32.5 Quick reference: ArrayBuffers

ArrayBuffers store binary data, which is meant to be accessed via Typed Arrays and DataViews.

### 32.5.1 `new ArrayBuffer()`

The type signature of the constructor is:

```
[](#cb873-1)new ArrayBuffer(length: number)
```

Invoking this constructor via `new` creates an instance whose capacity is `length` bytes. Each of those bytes is initially 0.

You can’t change the length of an ArrayBuffer; you can only create a new one with a different length.

### 32.5.2 Static methods of `ArrayBuffer`

*   `ArrayBuffer.isView(arg: any)`

    Returns `true` if `arg` is an object and a *view* for an ArrayBuffer (i.e., if it is a Typed Array or a DataView).

### 32.5.3 Properties of `ArrayBuffer.prototype`

*   `get .byteLength(): number`

    Returns the capacity of this ArrayBuffer in bytes.

*   `.slice(startIndex: number, endIndex=this.byteLength)`

    Creates a new ArrayBuffer that contains the bytes of this ArrayBuffer whose indices are greater than or equal to `startIndex` and less than `endIndex`. `start` and `endIndex` can be negative (see [§32.4 “Quick references: indices vs. offsets”](#ch033.xhtml_typed-arrays-indices-offsets)).

## 32.6 Quick reference: Typed Arrays

The properties of the various Typed Array objects are introduced in two steps:

1.  `TypedArray`: First, we look at the abstract superclass of all Typed Array classes (which was shown in the class diagram [at the beginning of this chapter](#ch033.xhtml_fig:typed_arrays_class_diagram)). I’m calling that superclass `TypedArray`, but it is not directly accessible from JavaScript. `TypedArray.prototype` houses all methods of Typed Arrays.
2.  `«ElementType»Array`: The concrete Typed Array classes are called `Uint8Array`, `Int16Array`, `Float32Array`, etc. These are the classes that you use via `new`, `.of`, and `.from()`.

### 32.6.1 Static methods of `TypedArray<T>`

Both static `TypedArray` methods are inherited by its subclasses (`Uint8Array`, etc.). `TypedArray` is abstract. Therefore, you always use these methods via the subclasses, which are concrete and can have direct instances.

*   `.from<S>(source: Iterable<S>|ArrayLike<S>, mapfn?: S => T, thisArg?: any) : instanceof this`

    Converts an iterable (including Arrays and Typed Arrays) or [an Array-like object](#ch032.xhtml_array-like-objects) to an instance of `this` (`instanceof this` is my invention to express that fact).

    ```
    [](#cb874-1)assert.deepEqual(
    [](#cb874-2)  Uint16Array.from([0, 1, 2]),
    [](#cb874-3)  Uint16Array.of(0, 1, 2));
    ```

    The optional `mapfn` lets you transform the elements of `source` before they become elements of the result.

    ```
    [](#cb875-1)assert.deepEqual(
    [](#cb875-2)  Int16Array.from(Int8Array.of(127, 126, 125), x => x * 2),
    [](#cb875-3)  Int16Array.of(254, 252, 250));
    ```

*   `.of(...items: number[]): instanceof this`

    Creates a new instance of `this` whose elements are `items` (coerced to the element type).

    ```
    [](#cb876-1)assert.deepEqual(
    [](#cb876-2)  Int16Array.of(-1234, 5, 67),
    [](#cb876-3)  new Int16Array([-1234, 5, 67]) );
    ```

### 32.6.2 Properties of `TypedArray<T>.prototype`

Indices accepted by Typed Array methods can be negative (they work like traditional Array methods that way). Offsets must be non-negative. For details, see [§32.4 “Quick references: indices vs. offsets”](#ch033.xhtml_typed-arrays-indices-offsets).

#### 32.6.2.1 Properties specific to Typed Arrays

The following properties are specific to Typed Arrays; normal Arrays don’t have them:

*   `get .buffer(): ArrayBuffer`

    Returns the buffer backing this Typed Array.

*   `get .length(): number`

    Returns the length in elements of this Typed Array’s buffer.

*   `get .byteLength(): number`

    Returns the size in bytes of this Typed Array’s buffer.

*   `get .byteOffset(): number`

    Returns the offset where this Typed Array “starts” inside its ArrayBuffer.

*   `.set(typedArray: TypedArray, offset=0): void`

*   `.set(arrayLike: ArrayLike<number>, offset=0): void`

    Copies all elements of the first parameter to this Typed Array. The element at index 0 of the parameter is written to index `offset` of this Typed Array (etc.). For more information on Array-like objects, consult [§31.4 “Array-like objects”](#ch032.xhtml_array-like-objects).

*   `.subarray(startIndex=0, endIndex=this.length): TypedArray<T>`

    Returns a new Typed Array that has the same buffer as this Typed Array, but a (generally) smaller range. If `startIndex` is non-negative then the first element of the resulting Typed Array is `this[startIndex]`, the second `this[startIndex+1]` (etc.). If `startIndex` in negative, it is converted appropriately.

#### 32.6.2.2 Array methods

The following methods are basically the same as the methods of normal Arrays:

*   `.copyWithin(target: number, start: number, end=this.length): this` ^([W, ES6])
*   `.entries(): Iterable<[number, T]>` ^([R, ES6])
*   `.every(callback: (value: T, index: number, array: TypedArray<T>) => boolean, thisArg?: any): boolean` ^([R, ES5])
*   `.fill(value: T, start=0, end=this.length): this` ^([W, ES6])
*   `.filter(callback: (value: T, index: number, array: TypedArray<T>) => any, thisArg?: any): T[]` ^([R, ES5])
*   `.find(predicate: (value: T, index: number, obj: T[]) => boolean, thisArg?: any): T | undefined` ^([R, ES6])
*   `.findIndex(predicate: (value: T, index: number, obj: T[]) => boolean, thisArg?: any): number` ^([R, ES6])
*   `.forEach(callback: (value: T, index: number, array: TypedArray<T>) => void, thisArg?: any): void` ^([R, ES5])
*   `.includes(searchElement: T, fromIndex=0): boolean` ^([R, ES2016])
*   `.indexOf(searchElement: T, fromIndex=0): number` ^([R, ES5])
*   `.join(separator = ','): string` ^([R, ES1])
*   `.keys(): Iterable<number>` ^([R, ES6])
*   `.lastIndexOf(searchElement: T, fromIndex=this.length-1): number` ^([R, ES5])
*   `.map<U>(mapFunc: (value: T, index: number, array: TypedArray<T>) => U, thisArg?: any): U[]` ^([R, ES5])
*   `.reduce<U>(callback: (accumulator: U, element: T, index: number, array: T[]) => U, init?: U): U` ^([R, ES5])
*   `.reduceRight<U>(callback: (accumulator: U, element: T, index: number, array: T[]) => U, init?: U): U` ^([R, ES5])
*   `.reverse(): this` ^([W, ES1])
*   `.slice(start=0, end=this.length): T[]` ^([R, ES3])
*   `.some(callback: (value: T, index: number, array: TypedArray<T>) => boolean, thisArg?: any): boolean` ^([R, ES5])
*   `.sort(compareFunc?: (a: T, b: T) => number): this` ^([W, ES1])
*   `.toString(): string` ^([R, ES1])
*   `.values(): Iterable<number>` ^([R, ES6])

For details on how these methods work, please consult [§31.12.3 “Methods of `Array<T>.prototype`”](#ch032.xhtml_quickref-array-prototype).

### 32.6.3 `new «ElementType»Array()`

Each Typed Array constructor has a name that follows the pattern `«ElementType»Array`, where `«ElementType»` is one of the element types in the table at the beginning. That means that there are nine constructors for Typed Arrays:

*   `Float32Array`, `Float64Array`
*   `Int8Array`, `Int16Array`, `Int32Array`
*   `Uint8Array`, `Uint8ClampedArray`, `Uint16Array`, `Uint32Array`

Each constructor has four *overloaded* versions – it behaves differently depending on how many arguments it receives and what their types are:

*   `new «ElementType»Array(buffer: ArrayBuffer, byteOffset=0, length=0)`

    Creates a new `«ElementType»Array` whose buffer is `buffer`. It starts accessing the buffer at the given `byteOffset` and will have the given `length`. Note that `length` counts elements of the Typed Array (with 1–8 bytes each), not bytes.

*   `new «ElementType»Array(length=0)`

    Creates a new `«ElementType»Array` with the given `length` and the appropriate buffer. The buffer’s size in bytes is:

    ```
    [](#cb877-1)length * «ElementType»Array.BYTES_PER_ELEMENT
    ```

*   `new «ElementType»Array(source: TypedArray)`

    Creates a new instance of `«ElementType»Array` whose elements have the same values as the elements of `source`, but coerced to `ElementType`.

*   `new «ElementType»Array(source: ArrayLike<number>)`

    Creates a new instance of `«ElementType»Array` whose elements have the same values as the elements of `source`, but coerced to `ElementType`. For more information on Array-like objects, consult [§31.4 “Array-like objects”](#ch032.xhtml_array-like-objects).

### 32.6.4 Static properties of `«ElementType»Array`

*   `«ElementType»Array.BYTES_PER_ELEMENT: number`

    Counts how many bytes are needed to store a single element:

    ```
    > Uint8Array.BYTES_PER_ELEMENT
    1
    > Int16Array.BYTES_PER_ELEMENT
    2
    > Float64Array.BYTES_PER_ELEMENT
    8
    ```

### 32.6.5 Properties of `«ElementType»Array.prototype`

*   `.BYTES_PER_ELEMENT: number`

    The same as `«ElementType»Array.BYTES_PER_ELEMENT`.

## 32.7 Quick reference: DataViews

### 32.7.1 `new DataView()`

*   `new DataView(buffer: ArrayBuffer, byteOffset=0, byteLength=buffer.byteLength-byteOffset)`

    Creates a new DataView whose data is stored in the ArrayBuffer `buffer`. By default, the new DataView can access all of `buffer`. The last two parameters allow you to change that.

### 32.7.2 Properties of `DataView.prototype`

In the remainder of this section, `«ElementType»` refers to either:

*   `Float32`, `Float64`
*   `Int8`, `Int16`, `Int32`
*   `Uint8`, `Uint16`, `Uint32`

These are the properties of `DataView.prototype`:

*   `get .buffer()`

    Returns the ArrayBuffer of this DataView.

*   `get .byteLength()`

    Returns how many bytes can be accessed by this DataView.

*   `get .byteOffset()`

    Returns at which offset this DataView starts accessing the bytes in its buffer.

*   `.get«ElementType»(byteOffset: number, littleEndian=false)`

    Reads a value from the buffer of this DataView.

*   `.set«ElementType»(byteOffset: number, value: number, littleEndian=false)`

    Writes `value` to the buffer of this DataView.

# 33 Maps (`Map`)

* * *

*   33.1 [Using Maps](#ch034.xhtml_using-maps)
    *   33.1.1 [Creating Maps](#ch034.xhtml_creating-maps)
    *   33.1.2 [Copying Maps](#ch034.xhtml_copying-maps)
    *   33.1.3 [Working with single entries](#ch034.xhtml_working-with-single-entries)
    *   33.1.4 [Determining the size of a Map and clearing it](#ch034.xhtml_determining-the-size-of-a-map-and-clearing-it)
    *   33.1.5 [Getting the keys and values of a Map](#ch034.xhtml_getting-the-keys-and-values-of-a-map)
    *   33.1.6 [Getting the entries of a Map](#ch034.xhtml_getting-the-entries-of-a-map)
    *   33.1.7 [Listed in insertion order: entries, keys, values](#ch034.xhtml_listed-in-insertion-order-entries-keys-values)
    *   33.1.8 [Converting between Maps and Objects](#ch034.xhtml_converting-maps-objects)
*   33.2 [Example: Counting characters](#ch034.xhtml_example-counting-characters)
*   33.3 [A few more details about the keys of Maps (advanced)](#ch034.xhtml_a-few-more-details-about-the-keys-of-maps-advanced)
    *   33.3.1 [What keys are considered equal?](#ch034.xhtml_what-keys-are-considered-equal)
*   33.4 [Missing Map operations](#ch034.xhtml_missing-map-operations)
    *   33.4.1 [Mapping and filtering Maps](#ch034.xhtml_mapping-and-filtering-maps)
    *   33.4.2 [Combining Maps](#ch034.xhtml_combining-maps)
*   33.5 [Quick reference: `Map<K,V>`](#ch034.xhtml_quickref-maps)
    *   33.5.1 [Constructor](#ch034.xhtml_constructor)
    *   33.5.2 [`Map<K,V>.prototype`: handling single entries](#ch034.xhtml_mapkv.prototype-handling-single-entries)
    *   33.5.3 [`Map<K,V>.prototype`: handling all entries](#ch034.xhtml_mapkv.prototype-handling-all-entries)
    *   33.5.4 [`Map<K,V>.prototype`: iterating and looping](#ch034.xhtml_mapkv.prototype-iterating-and-looping)
    *   33.5.5 [Sources of this section](#ch034.xhtml_sources-of-this-section-1)
*   33.6 [FAQ: Maps](#ch034.xhtml_faq-maps)
    *   33.6.1 [When should I use a Map, and when should I use an object?](#ch034.xhtml_when-should-i-use-a-map-and-when-should-i-use-an-object)
    *   33.6.2 [When would I use an object as a key in a Map?](#ch034.xhtml_when-would-i-use-an-object-as-a-key-in-a-map)
    *   33.6.3 [Why do Maps preserve the insertion order of entries?](#ch034.xhtml_why-do-maps-preserve-the-insertion-order-of-entries)
    *   33.6.4 [Why do Maps have a `.size`, while Arrays have a `.length`?](#ch034.xhtml_collection-size-vs-length)

* * *

Before ES6, JavaScript didn’t have a data structure for dictionaries and (ab)used objects as dictionaries from strings to arbitrary values. ES6 brought Maps, which are dictionaries from arbitrary values to arbitrary values.

## 33.1 Using Maps

An instance of `Map` maps keys to values. A single key-value mapping is called an *entry*.

### 33.1.1 Creating Maps

There are three common ways of creating Maps.

First, you can use the constructor without any parameters to create an empty Map:

```
[](#cb879-1)const emptyMap = new Map();
[](#cb879-2)assert.equal(emptyMap.size, 0);
```

Second, you can pass an iterable (e.g., an Array) over key-value “pairs” (Arrays with two elements) to the constructor:

```
[](#cb880-1)const map = new Map([
[](#cb880-2)  [1, 'one'],
[](#cb880-3)  [2, 'two'],
[](#cb880-4)  [3, 'three'], // trailing comma is ignored
[](#cb880-5)]);
```

Third, the `.set()` method adds entries to a Map and is chainable:

```
[](#cb881-1)const map = new Map()
[](#cb881-2)  .set(1, 'one')
[](#cb881-3)  .set(2, 'two')
[](#cb881-4)  .set(3, 'three');
```

### 33.1.2 Copying Maps

As we’ll see later, Maps are also iterables over key-value pairs. Therefore, you can use the constructor to create a copy of a Map. That copy is *shallow*: keys and values are the same; they are not duplicated.

```
[](#cb882-1)const original = new Map()
[](#cb882-2)  .set(false, 'no')
[](#cb882-3)  .set(true, 'yes');
[](#cb882-4)
[](#cb882-5)const copy = new Map(original);
[](#cb882-6)assert.deepEqual(original, copy);
```

### 33.1.3 Working with single entries

`.set()` and `.get()` are for writing and reading values (given keys).

```
[](#cb883-1)const map = new Map();
[](#cb883-2)
[](#cb883-3)map.set('foo', 123);
[](#cb883-4)
[](#cb883-5)assert.equal(map.get('foo'), 123);
[](#cb883-6)// Unknown key:
[](#cb883-7)assert.equal(map.get('bar'), undefined);
[](#cb883-8)// Use the default value '' if an entry is missing:
[](#cb883-9)assert.equal(map.get('bar') || '', '');
```

`.has()` checks if a Map has an entry with a given key. `.delete()` removes entries.

```
[](#cb884-1)const map = new Map([['foo', 123]]);
[](#cb884-2)
[](#cb884-3)assert.equal(map.has('foo'), true);
[](#cb884-4)assert.equal(map.delete('foo'), true)
[](#cb884-5)assert.equal(map.has('foo'), false)
```

### 33.1.4 Determining the size of a Map and clearing it

`.size` contains the number of entries in a Map. `.clear()` removes all entries of a Map.

```
[](#cb885-1)const map = new Map()
[](#cb885-2)  .set('foo', true)
[](#cb885-3)  .set('bar', false)
[](#cb885-4);
[](#cb885-5)
[](#cb885-6)assert.equal(map.size, 2)
[](#cb885-7)map.clear();
[](#cb885-8)assert.equal(map.size, 0)
```

### 33.1.5 Getting the keys and values of a Map

`.keys()` returns an iterable over the keys of a Map:

```
[](#cb886-1)const map = new Map()
[](#cb886-2)  .set(false, 'no')
[](#cb886-3)  .set(true, 'yes')
[](#cb886-4);
[](#cb886-5)
[](#cb886-6)for (const key of map.keys()) {
[](#cb886-7)  console.log(key);
[](#cb886-8)}
[](#cb886-9)// Output:
[](#cb886-10)// false
[](#cb886-11)// true
```

We can use [spreading (`...`)](#ch032.xhtml_spreading-into-array-literals) to convert the iterable returned by `.keys()` to an Array:

```
[](#cb887-1)assert.deepEqual(
[](#cb887-2)  [...map.keys()], 
[](#cb887-3)  [false, true]);
```

`.values()` works like `.keys()`, but for values instead of keys.

### 33.1.6 Getting the entries of a Map

`.entries()` returns an iterable over the entries of a Map:

```
[](#cb888-1)const map = new Map()
[](#cb888-2)  .set(false, 'no')
[](#cb888-3)  .set(true, 'yes')
[](#cb888-4);
[](#cb888-5)
[](#cb888-6)for (const entry of map.entries()) {
[](#cb888-7)  console.log(entry);
[](#cb888-8)}
[](#cb888-9)// Output:
[](#cb888-10)// [false, 'no']
[](#cb888-11)// [true, 'yes']
```

[Spreading (`...`)](#ch032.xhtml_spreading-into-array-literals) converts the iterable returned by `.entries()` to an Array:

```
[](#cb889-1)assert.deepEqual(
[](#cb889-2)  [...map.entries()], 
[](#cb889-3)  [[false, 'no'], [true, 'yes']]);
```

Map instances are also iterables over entries. In the following code, we use [destructuring](#ch038.xhtml_ch_destructuring) to access the keys and values of `map`:

```
[](#cb890-1)for (const [key, value] of map) {
[](#cb890-2)  console.log(key, value);
[](#cb890-3)}
[](#cb890-4)// Output:
[](#cb890-5)// false, 'no'
[](#cb890-6)// true, 'yes'
```

### 33.1.7 Listed in insertion order: entries, keys, values

Maps record in which order entries were created and honor that order when listing entries, keys, or values:

```
[](#cb891-1)const map1 = new Map([
[](#cb891-2)  ['a', 1],
[](#cb891-3)  ['b', 2],
[](#cb891-4)]);
[](#cb891-5)assert.deepEqual(
[](#cb891-6)  [...map1.keys()], ['a', 'b']);
[](#cb891-7)
[](#cb891-8)const map2 = new Map([
[](#cb891-9)  ['b', 2],
[](#cb891-10)  ['a', 1],
[](#cb891-11)]);
[](#cb891-12)assert.deepEqual(
[](#cb891-13)  [...map2.keys()], ['b', 'a']);
```

### 33.1.8 Converting between Maps and Objects

As long as a Map only uses strings and symbols as keys, you can convert it to an object (via [`Object.fromEntries()`](#ch029.xhtml_Object.fromEntries)):

```
[](#cb892-1)const map = new Map([
[](#cb892-2)  ['a', 1],
[](#cb892-3)  ['b', 2],
[](#cb892-4)]);
[](#cb892-5)const obj = Object.fromEntries(map);
[](#cb892-6)assert.deepEqual(
[](#cb892-7)  obj, {a: 1, b: 2});
```

You can also convert an object to a Map with string or symbol keys (via [`Object.entries()`](#ch029.xhtml_Object.entries)):

```
[](#cb893-1)const obj = {
[](#cb893-2)  a: 1,
[](#cb893-3)  b: 2,
[](#cb893-4)};
[](#cb893-5)const map = new Map(Object.entries(obj));
[](#cb893-6)assert.deepEqual(
[](#cb893-7)  map, new Map([['a', 1], ['b', 2]]));
```

## 33.2 Example: Counting characters

`countChars()` returns a Map that maps characters to numbers of occurrences.

```
[](#cb894-1)function countChars(chars) {
[](#cb894-2)  const charCounts = new Map();
[](#cb894-3)  for (let ch of chars) {
[](#cb894-4)    ch = ch.toLowerCase();
[](#cb894-5)    const prevCount = charCounts.get(ch) || 0;
[](#cb894-6)    charCounts.set(ch, prevCount+1);
[](#cb894-7)  }
[](#cb894-8)  return charCounts;
[](#cb894-9)}
[](#cb894-10)
[](#cb894-11)const result = countChars('AaBccc');
[](#cb894-12)assert.deepEqual(
[](#cb894-13)  [...result],
[](#cb894-14)  [
[](#cb894-15)    ['a', 2],
[](#cb894-16)    ['b', 1],
[](#cb894-17)    ['c', 3],
[](#cb894-18)  ]
[](#cb894-19));
```

## 33.3 A few more details about the keys of Maps (advanced)

Any value can be a key, even an object:

```
[](#cb895-1)const map = new Map();
[](#cb895-2)
[](#cb895-3)const KEY1 = {};
[](#cb895-4)const KEY2 = {};
[](#cb895-5)
[](#cb895-6)map.set(KEY1, 'hello');
[](#cb895-7)map.set(KEY2, 'world');
[](#cb895-8)
[](#cb895-9)assert.equal(map.get(KEY1), 'hello');
[](#cb895-10)assert.equal(map.get(KEY2), 'world');
```

### 33.3.1 What keys are considered equal?

Most Map operations need to check whether a value is equal to one of the keys. They do so via the internal operation [SameValueZero](http://www.ecma-international.org/ecma-262/6.0/#sec-samevaluezero), which works like `===` but considers `NaN` to be equal to itself.

As a consequence, you can use `NaN` as a key in Maps, just like any other value:

```
> const map = new Map();

> map.set(NaN, 123);
> map.get(NaN)
123
```

Different objects are always considered to be different. That is something that can’t be changed (yet – configuring key equality is on TC39’s long-term roadmap).

```
> new Map().set({}, 1).set({}, 2).size
2
```

## 33.4 Missing Map operations

### 33.4.1 Mapping and filtering Maps

You can `.map()` and `.filter()` an Array, but there are no such operations for a Map. The solution is:

1.  Convert the Map into an Array of [key, value] pairs.
2.  Map or filter the Array.
3.  Convert the result back to a Map.

I’ll use the following Map to demonstrate how that works.

```
[](#cb898-1)const originalMap = new Map()
[](#cb898-2).set(1, 'a')
[](#cb898-3).set(2, 'b')
[](#cb898-4).set(3, 'c');
```

Mapping `originalMap`:

```
[](#cb899-1)const mappedMap = new Map( // step 3
[](#cb899-2)  [...originalMap] // step 1
[](#cb899-3)  .map(([k, v]) => [k * 2, '_' + v]) // step 2
[](#cb899-4));
[](#cb899-5)assert.deepEqual([...mappedMap],
[](#cb899-6)  [[2,'_a'], [4,'_b'], [6,'_c']]);
```

Filtering `originalMap`:

```
[](#cb900-1)const filteredMap = new Map( // step 3
[](#cb900-2)  [...originalMap] // step 1
[](#cb900-3)  .filter(([k, v]) => k < 3) // step 2
[](#cb900-4));
[](#cb900-5)assert.deepEqual([...filteredMap],
[](#cb900-6)  [[1,'a'], [2,'b']]);
```

Step 1 is performed by spreading (`...`) in the Array literal.

### 33.4.2 Combining Maps

There are no methods for combining Maps, which is why we must use a workaround that is similar to the one from the previous section.

Let’s combine the following two Maps:

```
[](#cb901-1)const map1 = new Map()
[](#cb901-2)  .set(1, '1a')
[](#cb901-3)  .set(2, '1b')
[](#cb901-4)  .set(3, '1c')
[](#cb901-5);
[](#cb901-6)
[](#cb901-7)const map2 = new Map()
[](#cb901-8)  .set(2, '2b')
[](#cb901-9)  .set(3, '2c')
[](#cb901-10)  .set(4, '2d')
[](#cb901-11);
```

To combine `map1` and `map2`, we turn them into Arrays via spreading (`...`) and concatenate those Arrays. Afterward, we convert the result back to a Map. All of that is done in line A.

```
[](#cb902-1)const combinedMap = new Map([...map1, ...map2]); // (A)
[](#cb902-2)assert.deepEqual(
[](#cb902-3)  [...combinedMap], // convert to Array for comparison
[](#cb902-4)  [ [ 1, '1a' ],
[](#cb902-5)    [ 2, '2b' ],
[](#cb902-6)    [ 3, '2c' ],
[](#cb902-7)    [ 4, '2d' ] ]
[](#cb902-8));
```

![](media/file6.svg)  **Exercise: Combining two Maps**

`exercises/maps/combine_maps_test.mjs`

## 33.5 Quick reference: `Map<K,V>`

Note: For the sake of conciseness, I’m pretending that all keys have the same type `K` and that all values have the same type `V`.

### 33.5.1 Constructor

*   `new Map<K, V>(entries?: Iterable<[K, V]>)` ^([ES6])

    If you don’t provide the parameter `entries`, then an empty Map is created. If you do provide an iterable over [key, value] pairs, then those pairs are added as entries to the Map. For example:

    ```
    [](#cb903-1)const map = new Map([
    [](#cb903-2)  [ 1, 'one' ],
    [](#cb903-3)  [ 2, 'two' ],
    [](#cb903-4)  [ 3, 'three' ], // trailing comma is ignored
    [](#cb903-5)]);
    ```

### 33.5.2 `Map<K,V>.prototype`: handling single entries

*   `.get(key: K): V` ^([ES6])

    Returns the `value` that `key` is mapped to in this Map. If there is no key `key` in this Map, `undefined` is returned.

    ```
    [](#cb904-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb904-2)assert.equal(map.get(1), 'one');
    [](#cb904-3)assert.equal(map.get(5), undefined);
    ```

*   `.set(key: K, value: V): this` ^([ES6])

    Maps the given key to the given value. If there is already an entry whose key is `key`, it is updated. Otherwise, a new entry is created. This method returns `this`, which means that you can chain it.

    ```
    [](#cb905-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb905-2)map.set(1, 'ONE!')
    [](#cb905-3)   .set(3, 'THREE!');
    [](#cb905-4)assert.deepEqual(
    [](#cb905-5)  [...map.entries()],
    [](#cb905-6)  [[1, 'ONE!'], [2, 'two'], [3, 'THREE!']]);
    ```

*   `.has(key: K): boolean` ^([ES6])

    Returns whether the given key exists in this Map.

    ```
    [](#cb906-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb906-2)assert.equal(map.has(1), true); // key exists
    [](#cb906-3)assert.equal(map.has(5), false); // key does not exist
    ```

*   `.delete(key: K): boolean` ^([ES6])

    If there is an entry whose key is `key`, it is removed and `true` is returned. Otherwise, nothing happens and `false` is returned.

    ```
    [](#cb907-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb907-2)assert.equal(map.delete(1), true);
    [](#cb907-3)assert.equal(map.delete(5), false); // nothing happens
    [](#cb907-4)assert.deepEqual(
    [](#cb907-5)  [...map.entries()],
    [](#cb907-6)  [[2, 'two']]);
    ```

### 33.5.3 `Map<K,V>.prototype`: handling all entries

*   `get .size: number` ^([ES6])

    Returns how many entries this Map has.

    ```
    [](#cb908-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb908-2)assert.equal(map.size, 2);
    ```

*   `.clear(): void` ^([ES6])

    Removes all entries from this Map.

    ```
    [](#cb909-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb909-2)assert.equal(map.size, 2);
    [](#cb909-3)map.clear();
    [](#cb909-4)assert.equal(map.size, 0);
    ```

### 33.5.4 `Map<K,V>.prototype`: iterating and looping

Both iterating and looping happen in the order in which entries were added to a Map.

*   `.entries(): Iterable<[K,V]>` ^([ES6])

    Returns an iterable with one [key, value] pair for each entry in this Map. The pairs are Arrays of length 2.

    ```
    [](#cb910-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb910-2)for (const entry of map.entries()) {
    [](#cb910-3)  console.log(entry);
    [](#cb910-4)}
    [](#cb910-5)// Output:
    [](#cb910-6)// [1, 'one']
    [](#cb910-7)// [2, 'two']
    ```

*   `.forEach(callback: (value: V, key: K, theMap: Map<K,V>) => void, thisArg?: any): void` ^([ES6])

    The first parameter is a callback that is invoked once for each entry in this Map. If `thisArg` is provided, `this` is set to it for each invocation. Otherwise, `this` is set to `undefined`.

    ```
    [](#cb911-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb911-2)map.forEach((value, key) => console.log(value, key));
    [](#cb911-3)// Output:
    [](#cb911-4)// 'one', 1
    [](#cb911-5)// 'two', 2
    ```

*   `.keys(): Iterable<K>` ^([ES6])

    Returns an iterable over all keys in this Map.

    ```
    [](#cb912-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb912-2)for (const key of map.keys()) {
    [](#cb912-3)  console.log(key);
    [](#cb912-4)}
    [](#cb912-5)// Output:
    [](#cb912-6)// 1
    [](#cb912-7)// 2
    ```

*   `.values(): Iterable<V>` ^([ES6])

    Returns an iterable over all values in this Map.

    ```
    [](#cb913-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb913-2)for (const value of map.values()) {
    [](#cb913-3)  console.log(value);
    [](#cb913-4)}
    [](#cb913-5)// Output:
    [](#cb913-6)// 'one'
    [](#cb913-7)// 'two'
    ```

*   `[Symbol.iterator](): Iterable<[K,V]>` ^([ES6])

    The default way of iterating over Maps. Same as `.entries()`.

    ```
    [](#cb914-1)const map = new Map([[1, 'one'], [2, 'two']]);
    [](#cb914-2)for (const [key, value] of map) {
    [](#cb914-3)  console.log(key, value);
    [](#cb914-4)}
    [](#cb914-5)// Output:
    [](#cb914-6)// 1, 'one'
    [](#cb914-7)// 2, 'two'
    ```

### 33.5.5 Sources of this section

*   [TypeScript’s built-in typings](https://github.com/Microsoft/TypeScript/blob/master/lib/)

## 33.6 FAQ: Maps

### 33.6.1 When should I use a Map, and when should I use an object?

If you need a dictionary-like data structure with keys that are neither strings nor symbols, you have no choice: you must use a Map.

If, however, your keys are either strings or symbols, you must decide whether or not to use an object. A rough general guideline is:

*   Is there a fixed set of keys (known at development time)?

    Then use an object `obj` and access the values via fixed keys:

    ```
    [](#cb915-1)const value = obj.key;
    ```

*   Can the set of keys change at runtime?

    Then use a Map `map` and access the values via keys stored in variables:

    ```
    [](#cb916-1)const theKey = 123;
    [](#cb916-2)map.get(theKey);
    ```

### 33.6.2 When would I use an object as a key in a Map?

You normally want Map keys to be compared by value (two keys are considered equal if they have the same content). That excludes objects. However, there is one use case for objects as keys: externally attaching data to objects. But that use case is served better by WeakMaps, where entries don’t prevent keys from being garbage-collected (for details, consult [the next chapter](#ch035.xhtml_ch_weakmaps)).

### 33.6.3 Why do Maps preserve the insertion order of entries?

In principle, Maps are unordered. The main reason for ordering entries is so that operations that list entries, keys, or values are deterministic. That helps, for example, with testing.

### 33.6.4 Why do Maps have a `.size`, while Arrays have a `.length`?

In JavaScript, indexable sequences (such as Arrays and strings) have a `.length`, while unindexed collections (such as Maps and Sets) have a `.size`:

*   `.length` is based on indices; it is always the highest index plus one.
*   `.size` counts the number of elements in a collection.

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 34 WeakMaps (`WeakMap`)

* * *

*   34.1 [WeakMaps are black boxes](#ch035.xhtml_weakmaps-as-black-boxes)
*   34.2 [The keys of a WeakMap are *weakly held*](#ch035.xhtml_weakmap-keys-are-weakly-held)
    *   34.2.1 [All WeakMap keys must be objects](#ch035.xhtml_all-weakmap-keys-must-be-objects)
    *   34.2.2 [Use case: attaching values to objects](#ch035.xhtml_use-case-attaching-values-to-objects)
*   34.3 [Examples](#ch035.xhtml_examples)
    *   34.3.1 [Caching computed results via WeakMaps](#ch035.xhtml_caching-computed-results-via-weakmaps)
    *   34.3.2 [Keeping private data in WeakMaps](#ch035.xhtml_private-data-in-weakmaps)
*   34.4 [WeakMap API](#ch035.xhtml_weakmap-api)

* * *

WeakMaps are similar to Maps, with the following differences:

*   They are black boxes, where a value can only be accessed if you have both the WeakMap and the key.
*   The keys of a WeakMap are *weakly held*: if an object is a key in a WeakMap, it can still be garbage-collected. That lets us use WeakMaps to attach data to objects.

The next two sections examine in more detail what that means.

## 34.1 WeakMaps are black boxes

It is impossible to inspect what’s inside a WeakMap:

*   For example, you can’t iterate or loop over keys, values or entries. And you can’t compute the size.
*   Additionally, you can’t clear a WeakMap either – you have to create a fresh instance.

These restrictions enable a security property. Quoting [Mark Miller](https://github.com/tc39/tc39-notes/blob/master/meetings/2014-11/nov-19.md#412-should-weakmapweakset-have-a-clear-method-markm):

> The mapping from weakmap/key pair value can only be observed or affected by someone who has both the weakmap and the key. With `clear()`, someone with only the WeakMap would’ve been able to affect the WeakMap-and-key-to-value mapping.

## 34.2 The keys of a WeakMap are *weakly held*

The keys of a WeakMap are said to be *weakly held*: Normally if one object refers to another one, then the latter object can’t be garbage-collected as long as the former exists. With a WeakMap, that is different: If an object is a key and not referred to elsewhere, it can be garbage-collected while the WeakMap still exists. That also leads to the corresponding entry being removed (but there is no way to observe that).

### 34.2.1 All WeakMap keys must be objects

All WeakMap keys must be objects. You get an error if you use a primitive value:

```
> const wm = new WeakMap();
> wm.set(123, 'test')
TypeError: Invalid value used as weak map key
```

With primitive values as keys, WeakMaps wouldn’t be black boxes anymore. But given that primitive values are never garbage-collected, you don’t profit from weakly held keys anyway, and can just as well use a normal Map.

### 34.2.2 Use case: attaching values to objects

This is the main use case for WeakMaps: you can use them to externally attach values to objects – for example:

```
[](#cb918-1)const wm = new WeakMap();
[](#cb918-2){
[](#cb918-3)  const obj = {};
[](#cb918-4)  wm.set(obj, 'attachedValue'); // (A)
[](#cb918-5)}
[](#cb918-6)// (B)
```

In line A, we attach a value to `obj`. In line B, `obj` can already be garbage-collected, even though `wm` still exists. This technique of attaching a value to an object is equivalent to a property of that object being stored externally. If `wm` were a property, the previous code would look as follows:

```
[](#cb919-1){
[](#cb919-2)  const obj = {};
[](#cb919-3)  obj.wm = 'attachedValue';
[](#cb919-4)}
```

## 34.3 Examples

### 34.3.1 Caching computed results via WeakMaps

With WeakMaps, you can associate previously computed results with objects without having to worry about memory management. The following function `countOwnKeys()` is an example: it caches previous results in the WeakMap `cache`.

```
[](#cb920-1)const cache = new WeakMap();
[](#cb920-2)function countOwnKeys(obj) {
[](#cb920-3)  if (cache.has(obj)) {
[](#cb920-4)    return [cache.get(obj), 'cached'];
[](#cb920-5)  } else {
[](#cb920-6)    const count = Object.keys(obj).length;
[](#cb920-7)    cache.set(obj, count);
[](#cb920-8)    return [count, 'computed'];
[](#cb920-9)  }
[](#cb920-10)}
```

If we use this function with an object `obj`, you can see that the result is only computed for the first invocation, while a cached value is used for the second invocation:

```
> const obj = { foo: 1, bar: 2};
> countOwnKeys(obj)
[2, 'computed']
> countOwnKeys(obj)
[2, 'cached']
```

### 34.3.2 Keeping private data in WeakMaps

In the following code, the WeakMaps `_counter` and `_action` are used to store the values of virtual properties of instances of `Countdown`:

```
[](#cb922-1)const _counter = new WeakMap();
[](#cb922-2)const _action = new WeakMap();
[](#cb922-3)
[](#cb922-4)class Countdown {
[](#cb922-5)  constructor(counter, action) {
[](#cb922-6)    _counter.set(this, counter);
[](#cb922-7)    _action.set(this, action);
[](#cb922-8)  }
[](#cb922-9)  dec() {
[](#cb922-10)    let counter = _counter.get(this);
[](#cb922-11)    counter--;
[](#cb922-12)    _counter.set(this, counter);
[](#cb922-13)    if (counter === 0) {
[](#cb922-14)      _action.get(this)();
[](#cb922-15)    }
[](#cb922-16)  }
[](#cb922-17)}
[](#cb922-18)
[](#cb922-19)// The two pseudo-properties are truly private:
[](#cb922-20)assert.deepEqual(
[](#cb922-21)  Object.keys(new Countdown()),
[](#cb922-22)  []);
```

This is how `Countdown` is used:

```
[](#cb923-1)let invoked = false;
[](#cb923-2)
[](#cb923-3)const cd = new Countdown(3, () => invoked = true);
[](#cb923-4)
[](#cb923-5)cd.dec(); assert.equal(invoked, false);
[](#cb923-6)cd.dec(); assert.equal(invoked, false);
[](#cb923-7)cd.dec(); assert.equal(invoked, true);
```

![](media/file6.svg)  **Exercise: WeakMaps for private data**

`exercises/weakmaps/weakmaps_private_data_test.mjs`

## 34.4 WeakMap API

The constructor and the four methods of `WeakMap` work the same as [their `Map` equivalents](#ch034.xhtml_quickref-maps):

*   `new WeakMap<K, V>(entries?: Iterable<[K, V]>)` ^([ES6])
*   `.delete(key: K) : boolean` ^([ES6])
*   `.get(key: K) : V` ^([ES6])
*   `.has(key: K) : boolean` ^([ES6])
*   `.set(key: K, value: V) : this` ^([ES6])

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 35 Sets (`Set`)

* * *

*   35.1 [Using Sets](#ch036.xhtml_using-sets)
    *   35.1.1 [Creating Sets](#ch036.xhtml_creating-sets)
    *   35.1.2 [Adding, removing, checking membership](#ch036.xhtml_adding-removing-checking-membership)
    *   35.1.3 [Determining the size of a Set and clearing it](#ch036.xhtml_determining-the-size-of-a-set-and-clearing-it)
    *   35.1.4 [Iterating over Sets](#ch036.xhtml_iterating-over-sets-1)
*   35.2 [Examples of using Sets](#ch036.xhtml_examples-of-using-sets)
    *   35.2.1 [Removing duplicates from an Array](#ch036.xhtml_removing-duplicates-from-an-array)
    *   35.2.2 [Creating a set of Unicode characters (code points)](#ch036.xhtml_creating-a-set-of-unicode-characters-code-points)
*   35.3 [What Set elements are considered equal?](#ch036.xhtml_what-set-elements-are-considered-equal)
*   35.4 [Missing Set operations](#ch036.xhtml_missing-set-operations)
    *   35.4.1 [Union (`a` ∪ `b`)](#ch036.xhtml_union-a-b)
    *   35.4.2 [Intersection (`a` ∩ `b`)](#ch036.xhtml_intersection-a-b)
    *   35.4.3 [Difference (`a` \ `b`)](#ch036.xhtml_difference-a-b)
    *   35.4.4 [Mapping over Sets](#ch036.xhtml_mapping-over-sets)
    *   35.4.5 [Filtering Sets](#ch036.xhtml_filtering-sets)
*   35.5 [Quick reference: `Set<T>`](#ch036.xhtml_quickref-sets)
    *   35.5.1 [Constructor](#ch036.xhtml_constructor-1)
    *   35.5.2 [`Set<T>.prototype`: single Set elements](#ch036.xhtml_sett.prototype-single-set-elements)
    *   35.5.3 [`Set<T>.prototype`: all Set elements](#ch036.xhtml_sett.prototype-all-set-elements)
    *   35.5.4 [`Set<T>.prototype`: iterating and looping](#ch036.xhtml_sett.prototype-iterating-and-looping)
    *   35.5.5 [Symmetry with `Map`](#ch036.xhtml_symmetry-with-map)
*   35.6 [FAQ: Sets](#ch036.xhtml_faq-sets)
    *   35.6.1 [Why do Sets have a `.size`, while Arrays have a `.length`?](#ch036.xhtml_why-do-sets-have-a-.size-while-arrays-have-a-.length)

* * *

Before ES6, JavaScript didn’t have a data structure for sets. Instead, two workarounds were used:

*   The keys of an object were used as a set of strings.
*   Arrays were used as sets of arbitrary values. The downside is that checking *membership* (if an Array contains a value) is slower.

Since ES6, JavaScript has the data structure `Set`, which can contain arbitrary values and performs membership checks quickly.

## 35.1 Using Sets

### 35.1.1 Creating Sets

There are three common ways of creating Sets.

First, you can use the constructor without any parameters to create an empty Set:

```
[](#cb924-1)const emptySet = new Set();
[](#cb924-2)assert.equal(emptySet.size, 0);
```

Second, you can pass an iterable (e.g., an Array) to the constructor. The iterated values become elements of the new Set:

```
[](#cb925-1)const set = new Set(['red', 'green', 'blue']);
```

Third, the `.add()` method adds elements to a Set and is chainable:

```
[](#cb926-1)const set = new Set()
[](#cb926-2).add('red')
[](#cb926-3).add('green')
[](#cb926-4).add('blue');
```

### 35.1.2 Adding, removing, checking membership

`.add()` adds an element to a Set.

```
[](#cb927-1)const set = new Set();
[](#cb927-2)set.add('red');
```

`.has()` checks if an element is a member of a Set.

```
[](#cb928-1)assert.equal(set.has('red'), true);
```

`.delete()` removes an element from a Set.

```
[](#cb929-1)assert.equal(set.delete('red'), true); // there was a deletion
[](#cb929-2)assert.equal(set.has('red'), false);
```

### 35.1.3 Determining the size of a Set and clearing it

`.size` contains the number of elements in a Set.

```
[](#cb930-1)const set = new Set()
[](#cb930-2)  .add('foo')
[](#cb930-3)  .add('bar');
[](#cb930-4)assert.equal(set.size, 2)
```

`.clear()` removes all elements of a Set.

```
[](#cb931-1)set.clear();
[](#cb931-2)assert.equal(set.size, 0)
```

### 35.1.4 Iterating over Sets

Sets are iterable and the `for-of` loop works as you’d expect:

```
[](#cb932-1)const set = new Set(['red', 'green', 'blue']);
[](#cb932-2)for (const x of set) {
[](#cb932-3)  console.log(x);
[](#cb932-4)}
[](#cb932-5)// Output:
[](#cb932-6)// 'red'
[](#cb932-7)// 'green'
[](#cb932-8)// 'blue'
```

As you can see, Sets preserve *insertion order*. That is, elements are always iterated over in the order in which they were added.

Given that Sets are iterable, you can use [spreading (`...`)](#ch032.xhtml_spreading-into-array-literals) to convert them to Arrays:

```
[](#cb933-1)const set = new Set(['red', 'green', 'blue']);
[](#cb933-2)const arr = [...set]; // ['red', 'green', 'blue']
```

## 35.2 Examples of using Sets

### 35.2.1 Removing duplicates from an Array

Converting an Array to a Set and back, removes duplicates from the Array:

```
[](#cb934-1)assert.deepEqual(
[](#cb934-2)  [...new Set([1, 2, 1, 2, 3, 3, 3])],
[](#cb934-3)  [1, 2, 3]);
```

### 35.2.2 Creating a set of Unicode characters (code points)

Strings are iterable and can therefore be used as parameters for `new Set()`:

```
[](#cb935-1)assert.deepEqual(
[](#cb935-2)  new Set('abc'),
[](#cb935-3)  new Set(['a', 'b', 'c']));
```

## 35.3 What Set elements are considered equal?

As with Map keys, Set elements are compared similarly to `===`, with the exception of `NaN` being equal to itself.

```
> const set = new Set([NaN, NaN, NaN]);
> set.size
1
> set.has(NaN)
true
```

As with `===`, two different objects are never considered equal (and there is no way to change that at the moment):

```
> const set = new Set();

> set.add({});
> set.size
1

> set.add({});
> set.size
2
```

## 35.4 Missing Set operations

Sets are missing several common operations. Such an operation can usually be implemented by:

*   Converting the input Sets to Arrays by [spreading into Array literals](#ch032.xhtml_spreading-into-array-literals).
*   Performing the operation on Arrays.
*   Converting the result to a Set and returning it.

### 35.4.1 Union (`a` ∪ `b`)

Computing the union of two Sets `a` and `b` means creating a Set that contains the elements of both `a` and `b`.

```
[](#cb938-1)const a = new Set([1,2,3]);
[](#cb938-2)const b = new Set([4,3,2]);
[](#cb938-3)// Use spreading to concatenate two iterables
[](#cb938-4)const union = new Set([...a, ...b]);
[](#cb938-5)
[](#cb938-6)assert.deepEqual([...union], [1, 2, 3, 4]);
```

### 35.4.2 Intersection (`a` ∩ `b`)

Computing the intersection of two Sets `a` and `b` means creating a Set that contains those elements of `a` that are also in `b`.

```
[](#cb939-1)const a = new Set([1,2,3]);
[](#cb939-2)const b = new Set([4,3,2]);
[](#cb939-3)const intersection = new Set(
[](#cb939-4)  [...a].filter(x => b.has(x)));
[](#cb939-5)
[](#cb939-6)assert.deepEqual([...intersection], [2, 3]);
```

### 35.4.3 Difference (`a` \ `b`)

Computing the difference between two Sets `a` and `b` means creating a Set that contains those elements of `a` that are not in `b`. This operation is also sometimes called *minus* (−).

```
[](#cb940-1)const a = new Set([1,2,3]);
[](#cb940-2)const b = new Set([4,3,2]);
[](#cb940-3)const difference = new Set(
[](#cb940-4)  [...a].filter(x => !b.has(x)));
[](#cb940-5)
[](#cb940-6)assert.deepEqual([...difference], [1]);
```

### 35.4.4 Mapping over Sets

Sets don’t have a method `.map()`. But we can borrow the one that Arrays have:

```
[](#cb941-1)const set = new Set([1, 2, 3]);
[](#cb941-2)const mappedSet = new Set([...set].map(x => x * 2));
[](#cb941-3)
[](#cb941-4)// Convert mappedSet to an Array to check what’s inside it
[](#cb941-5)assert.deepEqual([...mappedSet], [2, 4, 6]);
```

### 35.4.5 Filtering Sets

We can’t directly `.filter()` Sets, so we need to use the corresponding Array method:

```
[](#cb942-1)const set = new Set([1, 2, 3, 4, 5]);
[](#cb942-2)const filteredSet = new Set([...set].filter(x => (x % 2) === 0));
[](#cb942-3)
[](#cb942-4)assert.deepEqual([...filteredSet], [2, 4]);
```

## 35.5 Quick reference: `Set<T>`

### 35.5.1 Constructor

*   `new Set<T>(values?: Iterable<T>)` ^([ES6])

    If you don’t provide the parameter `values`, then an empty Set is created. If you do, then the iterated values are added as elements to the Set. For example:

    ```
    [](#cb943-1)const set = new Set(['red', 'green', 'blue']);
    ```

### 35.5.2 `Set<T>.prototype`: single Set elements

*   `.add(value: T): this` ^([ES6])

    Adds `value` to this Set. This method returns `this`, which means that it can be chained.

    ```
    [](#cb944-1)const set = new Set(['red']);
    [](#cb944-2)set.add('green').add('blue');
    [](#cb944-3)assert.deepEqual([...set], ['red', 'green', 'blue']);
    ```

*   `.delete(value: T): boolean` ^([ES6])

    Removes `value` from this Set. Returns `true` if something was deleted and `false`, otherwise.

    ```
    [](#cb945-1)const set = new Set(['red', 'green', 'blue']);
    [](#cb945-2)assert.equal(set.delete('red'), true); // there was a deletion
    [](#cb945-3)assert.deepEqual([...set], ['green', 'blue']);
    ```

*   `.has(value: T): boolean` ^([ES6])

    Checks whether `value` is in this Set.

    ```
    [](#cb946-1)const set = new Set(['red', 'green']);
    [](#cb946-2)assert.equal(set.has('red'), true);
    [](#cb946-3)assert.equal(set.has('blue'), false);
    ```

### 35.5.3 `Set<T>.prototype`: all Set elements

*   `get .size: number` ^([ES6])

    Returns how many elements there are in this Set.

    ```
    [](#cb947-1)const set = new Set(['red', 'green', 'blue']);
    [](#cb947-2)assert.equal(set.size, 3);
    ```

*   `.clear(): void` ^([ES6])

    Removes all elements from this Set.

    ```
    [](#cb948-1)const set = new Set(['red', 'green', 'blue']);
    [](#cb948-2)assert.equal(set.size, 3);
    [](#cb948-3)set.clear();
    [](#cb948-4)assert.equal(set.size, 0);
    ```

### 35.5.4 `Set<T>.prototype`: iterating and looping

*   `.values(): Iterable<T>` ^([ES6])

    Returns an iterable over all elements of this Set.

    ```
    [](#cb949-1)const set = new Set(['red', 'green']);
    [](#cb949-2)for (const x of set.values()) {
    [](#cb949-3)  console.log(x);
    [](#cb949-4)}
    [](#cb949-5)// Output:
    [](#cb949-6)// 'red'
    [](#cb949-7)// 'green'
    ```

*   `[Symbol.iterator](): Iterable<T>` ^([ES6])

    Default way of iterating over Sets. Same as `.values()`.

    ```
    [](#cb950-1)const set = new Set(['red', 'green']);
    [](#cb950-2)for (const x of set) {
    [](#cb950-3)  console.log(x);
    [](#cb950-4)}
    [](#cb950-5)// Output:
    [](#cb950-6)// 'red'
    [](#cb950-7)// 'green'
    ```

*   `.forEach(callback: (value: T, key: T, theSet: Set<T>) => void, thisArg?: any): void` ^([ES6])

    Feeds each element of this Set to `callback()`. `value` and `key` both contain the current element. This redundancy was introduced so that this `callback` has the same type signature as the `callback` of `Map.prototype.forEach()`.

    You can specify the `this` of `callback` via `thisArg`. If you omit it, `this` is `undefined`.

    ```
    [](#cb951-1)const set = new Set(['red', 'green']);
    [](#cb951-2)set.forEach(x => console.log(x));
    [](#cb951-3)// Output:
    [](#cb951-4)// 'red'
    [](#cb951-5)// 'green'
    ```

### 35.5.5 Symmetry with `Map`

The following two methods mainly exist so that Sets and Maps have similar interfaces. Each Set element is handled as if it were a Map entry whose key and value are both the element.

*   `Set.prototype.entries(): Iterable<[T,T]>` ^([ES6])
*   `Set.prototype.keys(): Iterable<T>` ^([ES6])

`.entries()` enables you to convert a Set to a Map:

```
[](#cb952-1)const set = new Set(['a', 'b', 'c']);
[](#cb952-2)const map = new Map(set.entries());
[](#cb952-3)assert.deepEqual(
[](#cb952-4)  [...map.entries()],
[](#cb952-5)  [['a','a'], ['b','b'], ['c','c']]);
```

## 35.6 FAQ: Sets

### 35.6.1 Why do Sets have a `.size`, while Arrays have a `.length`?

The answer to this question is given in [§33.6.4 “Why do Maps have a `.size`, while Arrays have a `.length`?”](#ch034.xhtml_collection-size-vs-length).

![](media/file7.svg)  **Quiz**

See [quiz app](#ch012.xhtml_quizzes).

# 36 WeakSets (`WeakSet`)

* * *

*   36.1 [Example: Marking objects as safe to use with a method](#ch037.xhtml_example-marking-objects-as-safe-to-use-with-a-method)
*   36.2 [WeakSet API](#ch037.xhtml_weakset-api)

* * *

WeakSets are similar to Sets, with the following differences:

*   They can hold objects without preventing those objects from being garbage-collected.

*   They are black boxes: we only get any data out of a WeakSet if we have both the WeakSet and a value. The only methods that are supported are `.add()`, `.delete()`, `.has()`. Consult the section on [WeakMaps as black boxes](#ch035.xhtml_weakmaps-as-black-boxes) for an explanation of why WeakSets don’t allow iteration, looping, and clearing.

Given that we can’t iterate over their elements, there are not that many use cases for WeakSets. They do enable us to mark objects.

## 36.1 Example: Marking objects as safe to use with a method

[Domenic Denicola shows](https://mail.mozilla.org/pipermail/es-discuss/2015-June/043027.html) how a class `Foo` can ensure that its methods are only applied to instances that were created by it:

```
[](#cb953-1)const foos = new WeakSet();
[](#cb953-2)
[](#cb953-3)class Foo {
[](#cb953-4)  constructor() {
[](#cb953-5)    foos.add(this);
[](#cb953-6)  }
[](#cb953-7)
[](#cb953-8)  method() {
[](#cb953-9)    if (!foos.has(this)) {
[](#cb953-10)      throw new TypeError('Incompatible object!');
[](#cb953-11)    }
[](#cb953-12)  }
[](#cb953-13)}
[](#cb953-14)
[](#cb953-15)const foo = new Foo();
[](#cb953-16)foo.method(); // works
[](#cb953-17)
[](#cb953-18)assert.throws(
[](#cb953-19)  () => {
[](#cb953-20)    const obj = {};
[](#cb953-21)    Foo.prototype.method.call(obj); // throws an exception
[](#cb953-22)  },
[](#cb953-23)  TypeError
[](#cb953-24));
```

## 36.2 WeakSet API

The constructor and the three methods of `WeakSet` work the same as [their `Set` equivalents](#ch036.xhtml_quickref-sets):

*   `new WeakSet<T>(values?: Iterable<T>)` ^([ES6])
*   `.add(value: T): this` ^([ES6])
*   `.delete(value: T): boolean` ^([ES6])
*   `.has(value: T): boolean` ^([ES6])

# 37 Destructuring

* * *

*   37.1 [A first taste of destructuring](#ch038.xhtml_a-first-taste-of-destructuring)
*   37.2 [Constructing vs. extracting](#ch038.xhtml_constructing-vs.-extracting)
*   37.3 [Where can we destructure?](#ch038.xhtml_where-can-we-destructure)
*   37.4 [Object-destructuring](#ch038.xhtml_object-destructuring)
    *   37.4.1 [Property value shorthands](#ch038.xhtml_property-value-shorthands)
    *   37.4.2 [Rest properties](#ch038.xhtml_rest-properties)
    *   37.4.3 [Syntax pitfall: assigning via object destructuring](#ch038.xhtml_assigning-via-object-destructuring)
*   37.5 [Array-destructuring](#ch038.xhtml_array-destructuring)
    *   37.5.1 [Array-destructuring works with any iterable](#ch038.xhtml_array-destructuring-works-with-any-iterable)
    *   37.5.2 [Rest elements](#ch038.xhtml_rest-elements)
*   37.6 [Examples of destructuring](#ch038.xhtml_examples-of-destructuring)
    *   37.6.1 [Array-destructuring: swapping variable values](#ch038.xhtml_array-destructuring-swapping-variable-values)
    *   37.6.2 [Array-destructuring: operations that return Arrays](#ch038.xhtml_array-destructuring-operations-that-return-arrays)
    *   37.6.3 [Object-destructuring: multiple return values](#ch038.xhtml_object-destructuring-multiple-return-values)
*   37.7 [What happens if a pattern part does not match anything?](#ch038.xhtml_what-happens-if-a-pattern-part-does-not-match-anything)
    *   37.7.1 [Object-destructuring and missing properties](#ch038.xhtml_object-destructuring-and-missing-properties)
    *   37.7.2 [Array-destructuring and missing elements](#ch038.xhtml_array-destructuring-and-missing-elements)
*   37.8 [What values can’t be destructured?](#ch038.xhtml_what-values-cant-be-destructured)
    *   37.8.1 [You can’t object-destructure `undefined` and `null`](#ch038.xhtml_you-cant-object-destructure-undefined-and-null)
    *   37.8.2 [You can’t Array-destructure non-iterable values](#ch038.xhtml_you-cant-array-destructure-non-iterable-values)
*   37.9 [(Advanced)](#ch038.xhtml_advanced-4)
*   37.10 [Default values](#ch038.xhtml_default-values)
    *   37.10.1 [Default values in Array-destructuring](#ch038.xhtml_default-values-in-array-destructuring)
    *   37.10.2 [Default values in object-destructuring](#ch038.xhtml_default-values-in-object-destructuring)
*   37.11 [Parameter definitions are similar to destructuring](#ch038.xhtml_parameter-definitions-are-similar-to-destructuring)
*   37.12 [Nested destructuring](#ch038.xhtml_nested-destructuring)

* * *

## 37.1 A first taste of destructuring

With normal assignment, you extract one piece of data at a time – for example:

```
[](#cb954-1)const arr = ['a', 'b', 'c'];
[](#cb954-2)const x = arr[0]; // extract
[](#cb954-3)const y = arr[1]; // extract
```

With destructuring, you can extract multiple pieces of data at the same time via patterns in locations that receive data. The left-hand side of `=` in the previous code is one such location. In the following code, the square brackets in line A are a destructuring pattern:

```
[](#cb955-1)const arr = ['a', 'b', 'c'];
[](#cb955-2)const [x, y] = arr; // (A)
[](#cb955-3)assert.equal(x, 'a');
[](#cb955-4)assert.equal(y, 'b');
```

This code does the same as the previous code.

Note that the pattern is “smaller” than the data: we are only extracting what we need.

## 37.2 Constructing vs. extracting

In order to understand what destructuring is, consider that JavaScript has two kinds of operations that are opposites:

*   You can *construct* compound data, for example, by setting properties and via object literals.
*   You can *extract* data out of compound data, for example, by getting properties.

Constructing data looks as follows:

```
[](#cb956-1)// Constructing: one property at a time
[](#cb956-2)const jane1 = {};
[](#cb956-3)jane1.first = 'Jane';
[](#cb956-4)jane1.last = 'Doe';
[](#cb956-5)
[](#cb956-6)// Constructing: multiple properties
[](#cb956-7)const jane2 = {
[](#cb956-8)  first: 'Jane',
[](#cb956-9)  last: 'Doe',
[](#cb956-10)};
[](#cb956-11)
[](#cb956-12)assert.deepEqual(jane1, jane2);
```

Extracting data looks as follows:

```
[](#cb957-1)const jane = {
[](#cb957-2)  first: 'Jane',
[](#cb957-3)  last: 'Doe',
[](#cb957-4)};
[](#cb957-5)
[](#cb957-6)// Extracting: one property at a time
[](#cb957-7)const f1 = jane.first;
[](#cb957-8)const l1 = jane.last;
[](#cb957-9)assert.equal(f1, 'Jane');
[](#cb957-10)assert.equal(l1, 'Doe');
[](#cb957-11)
[](#cb957-12)// Extracting: multiple properties (NEW!)
[](#cb957-13)const {first: f2, last: l2} = jane; // (A)
[](#cb957-14)assert.equal(f2, 'Jane');
[](#cb957-15)assert.equal(l2, 'Doe');
```

The operation in line A is new: we declare two variables `f2` and `l2` and initialize them via *destructuring* (multivalue extraction).

The following part of line A is a *destructuring pattern*:

```
[](#cb958-1){first: f2, last: l2}
```

Destructuring patterns are syntactically similar to the literals that are used for multivalue construction. But they appear where data is received (e.g., at the left-hand side of assignments), not where data is created (e.g., at the right-hand side of assignments).

## 37.3 Where can we destructure?

Destructuring patterns can be used at “data sink locations” such as:

*   Variable declarations:

    ```
    [](#cb959-1)const [a] = ['x'];
    [](#cb959-2)assert.equal(a, 'x');
    [](#cb959-3)
    [](#cb959-4)let [b] = ['y'];
    [](#cb959-5)assert.equal(b, 'y');
    ```

*   Assignments:

    ```
    [](#cb960-1)let b;
    [](#cb960-2)[b] = ['z'];
    [](#cb960-3)assert.equal(b, 'z');
    ```

*   Parameter definitions:

    ```
    [](#cb961-1)const f = ([x]) => x;
    [](#cb961-2)assert.equal(f(['a']), 'a');
    ```

Note that variable declarations include `const` and `let` declarations in `for-of` loops:

```
[](#cb962-1)const arr = ['a', 'b'];
[](#cb962-2)for (const [index, element] of arr.entries()) {
[](#cb962-3)    console.log(index, element);
[](#cb962-4)}
[](#cb962-5)// Output:
[](#cb962-6)// 0, 'a'
[](#cb962-7)// 1, 'b'
```

In the next two sections, we’ll look deeper into the two kinds of destructuring: object-destructuring and Array-destructuring.

## 37.4 Object-destructuring

*Object-destructuring* lets you batch-extract values of properties via patterns that look like object literals:

```
[](#cb963-1)const address = {
[](#cb963-2)  street: 'Evergreen Terrace',
[](#cb963-3)  number: '742',
[](#cb963-4)  city: 'Springfield',
[](#cb963-5)  state: 'NT',
[](#cb963-6)  zip: '49007',
[](#cb963-7)};
[](#cb963-8)
[](#cb963-9)const { street: s, city: c } = address;
[](#cb963-10)assert.equal(s, 'Evergreen Terrace');
[](#cb963-11)assert.equal(c, 'Springfield');
```

You can think of the pattern as a transparent sheet that you place over the data: the pattern key `'street'` has a match in the data. Therefore, the data value `'Evergreen Terrace'` is assigned to the pattern variable `s`.

You can also object-destructure primitive values:

```
[](#cb964-1)const {length: len} = 'abc';
[](#cb964-2)assert.equal(len, 3);
```

And you can object-destructure Arrays:

```
[](#cb965-1)const {0:x, 2:y} = ['a', 'b', 'c'];
[](#cb965-2)assert.equal(x, 'a');
[](#cb965-3)assert.equal(y, 'c');
```

Why does that work? [Array indices are also properties](#ch032.xhtml_array-indices).

### 37.4.1 Property value shorthands

Object literals support property value shorthands and so do object patterns:

```
[](#cb966-1)const { street, city } = address;
[](#cb966-2)assert.equal(street, 'Evergreen Terrace');
[](#cb966-3)assert.equal(city, 'Springfield');
```

![](media/file6.svg)  **Exercise: Object-destructuring**

`exercises/destructuring/object_destructuring_exrc.mjs`

### 37.4.2 Rest properties

In object literals, you can have spread properties. In object patterns, you can have rest properties (which must come last):

```
[](#cb967-1)const obj = { a: 1, b: 2, c: 3 };
[](#cb967-2)const { a: propValue, ...remaining } = obj; // (A)
[](#cb967-3)
[](#cb967-4)assert.equal(propValue, 1);
[](#cb967-5)assert.deepEqual(remaining, {b:2, c:3});
```

A rest property variable, such as `remaining` (line A), is assigned an object with all data properties whose keys are not mentioned in the pattern.

`remaining` can also be viewed as the result of non-destructively removing property `a` from `obj`.

### 37.4.3 Syntax pitfall: assigning via object destructuring

If we object-destructure in an assignment, we are facing a pitfall caused by [syntactic ambiguity](#ch009.xhtml_ambiguous-syntax) – you can’t start a statement with a curly brace because then JavaScript thinks you are starting a block:

```
[](#cb968-1)let prop;
[](#cb968-2)assert.throws(
[](#cb968-3)  () => eval("{prop} = { prop: 'hello' };"),
[](#cb968-4)  {
[](#cb968-5)    name: 'SyntaxError',
[](#cb968-6)    message: 'Unexpected token =',
[](#cb968-7)  });
```

![](media/file5.svg)  **Why `eval()`?**

[`eval()`](#ch026.xhtml_eval) delays parsing (and therefore the `SyntaxError`) until the callback of `assert.throws()` is executed. If we didn’t use it, we’d already get an error when this code is parsed and `assert.throws()` wouldn’t even be executed.

The workaround is to put the whole assignment in parentheses:

```
[](#cb969-1)let prop;
[](#cb969-2)({prop} = { prop: 'hello' });
[](#cb969-3)assert.equal(prop, 'hello');
```

## 37.5 Array-destructuring

*Array-destructuring* lets you batch-extract values of Array elements via patterns that look like Array literals:

```
[](#cb970-1)const [x, y] = ['a', 'b'];
[](#cb970-2)assert.equal(x, 'a');
[](#cb970-3)assert.equal(y, 'b');
```

You can skip elements by mentioning holes inside Array patterns:

```
[](#cb971-1)const [, x, y] = ['a', 'b', 'c']; // (A)
[](#cb971-2)assert.equal(x, 'b');
[](#cb971-3)assert.equal(y, 'c');
```

The first element of the Array pattern in line A is a hole, which is why the Array element at index 0 is ignored.

### 37.5.1 Array-destructuring works with any iterable

Array-destructuring can be applied to any value that is iterable, not just to Arrays:

```
[](#cb972-1)// Sets are iterable
[](#cb972-2)const mySet = new Set().add('a').add('b').add('c');
[](#cb972-3)const [first, second] = mySet;
[](#cb972-4)assert.equal(first, 'a');
[](#cb972-5)assert.equal(second, 'b');
[](#cb972-6)
[](#cb972-7)// Strings are iterable
[](#cb972-8)const [a, b] = 'xyz';
[](#cb972-9)assert.equal(a, 'x');
[](#cb972-10)assert.equal(b, 'y');
```

### 37.5.2 Rest elements

In Array literals, you can have spread elements. In Array patterns, you can have rest elements (which must come last):

```
[](#cb973-1)const [x, y, ...remaining] = ['a', 'b', 'c', 'd']; // (A)
[](#cb973-2)
[](#cb973-3)assert.equal(x, 'a');
[](#cb973-4)assert.equal(y, 'b');
[](#cb973-5)assert.deepEqual(remaining, ['c', 'd']);
```

A rest element variable, such as `remaining` (line A), is assigned an Array with all elements of the destructured value that were not mentioned yet.

## 37.6 Examples of destructuring

### 37.6.1 Array-destructuring: swapping variable values

You can use Array-destructuring to swap the values of two variables without needing a temporary variable:

```
[](#cb974-1)let x = 'a';
[](#cb974-2)let y = 'b';
[](#cb974-3)
[](#cb974-4)[x,y] = [y,x]; // swap
[](#cb974-5)
[](#cb974-6)assert.equal(x, 'b');
[](#cb974-7)assert.equal(y, 'a');
```

### 37.6.2 Array-destructuring: operations that return Arrays

Array-destructuring is useful when operations return Arrays, as does, for example, the regular expression method `.exec()`:

```
[](#cb975-1)// Skip the element at index 0 (the whole match):
[](#cb975-2)const [, year, month, day] =
[](#cb975-3)  /^([0-9]{4})-([0-9]{2})-([0-9]{2})$/
[](#cb975-4)  .exec('2999-12-31');
[](#cb975-5)
[](#cb975-6)assert.equal(year, '2999');
[](#cb975-7)assert.equal(month, '12');
[](#cb975-8)assert.equal(day, '31');
```

### 37.6.3 Object-destructuring: multiple return values

Destructuring is very useful if a function returns multiple values – either packaged as an Array or packaged as an object.

Consider a function `findElement()` that finds elements in an Array:

```
[](#cb976-1)findElement(array, (value, index) => «boolean expression»)
```

Its second parameter is a function that receives the value and index of an element and returns a boolean indicating if this is the element the caller is looking for.

We are now faced with a dilemma: Should `findElement()` return the value of the element it found or the index? One solution would be to create two separate functions, but that would result in duplicated code because both functions would be very similar.

The following implementation avoids duplication by returning an object that contains both index and value of the element that is found:

```
[](#cb977-1)function findElement(arr, predicate) {
[](#cb977-2)  for (let index=0; index < arr.length; index++) {
[](#cb977-3)    const value = arr[index];
[](#cb977-4)    if (predicate(value)) {
[](#cb977-5)      // We found something:
[](#cb977-6)      return { value, index };
[](#cb977-7)    }
[](#cb977-8)  }
[](#cb977-9)  // We didn’t find anything:
[](#cb977-10)  return { value: undefined, index: -1 };
[](#cb977-11)}
```

Destructuring helps us with processing the result of `findElement()`:

```
[](#cb978-1)const arr = [7, 8, 6];
[](#cb978-2)
[](#cb978-3)const {value, index} = findElement(arr, x => x % 2 === 0);
[](#cb978-4)assert.equal(value, 8);
[](#cb978-5)assert.equal(index, 1);
```

As we are working with property keys, the order in which we mention `value` and `index` doesn’t matter:

```
[](#cb979-1)const {index, value} = findElement(arr, x => x % 2 === 0);
```

The kicker is that destructuring also serves us well if we are only interested in one of the two results:

```
[](#cb980-1)const arr = [7, 8, 6];
[](#cb980-2)
[](#cb980-3)const {value} = findElement(arr, x => x % 2 === 0);
[](#cb980-4)assert.equal(value, 8);
[](#cb980-5)
[](#cb980-6)const {index} = findElement(arr, x => x % 2 === 0);
[](#cb980-7)assert.equal(index, 1);
```

All of these conveniences combined make this way of handling multiple return values quite versatile.

## 37.7 What happens if a pattern part does not match anything?

What happens if there is no match for part of a pattern? The same thing that happens if you use non-batch operators: you get `undefined`.

### 37.7.1 Object-destructuring and missing properties

If a property in an object pattern has no match on the right-hand side, you get `undefined`:

```
[](#cb981-1)const {prop: p} = {};
[](#cb981-2)assert.equal(p, undefined);
```

### 37.7.2 Array-destructuring and missing elements

If an element in an Array pattern has no match on the right-hand side, you get `undefined`:

```
[](#cb982-1)const [x] = [];
[](#cb982-2)assert.equal(x, undefined);
```

## 37.8 What values can’t be destructured?

### 37.8.1 You can’t object-destructure `undefined` and `null`

Object-destructuring only fails if the value to be destructured is either `undefined` or `null`. That is, it fails whenever accessing a property via the dot operator would fail too.

```
[](#cb983-1)assert.throws(
[](#cb983-2)  () => { const {prop} = undefined; },
[](#cb983-3)  {
[](#cb983-4)    name: 'TypeError',
[](#cb983-5)    message: "Cannot destructure property `prop` of " +
[](#cb983-6)      "'undefined' or 'null'.",
[](#cb983-7)  }
[](#cb983-8));
[](#cb983-9)assert.throws(
[](#cb983-10)  () => { const {prop} = null; },
[](#cb983-11)  {
[](#cb983-12)    name: 'TypeError',
[](#cb983-13)    message: "Cannot destructure property `prop` of " +
[](#cb983-14)      "'undefined' or 'null'.",
[](#cb983-15)  }
[](#cb983-16));
```

### 37.8.2 You can’t Array-destructure non-iterable values

Array-destructuring demands that the destructured value be iterable. Therefore, you can’t Array-destructure `undefined` and `null`. But you can’t Array-destructure non-iterable objects either:

```
[](#cb984-1)assert.throws(
[](#cb984-2)  () => { const [x] = {}; },
[](#cb984-3)  {
[](#cb984-4)    name: 'TypeError',
[](#cb984-5)    message: '{} is not iterable',
[](#cb984-6)  }
[](#cb984-7));
```

![](media/file7.svg)  **Quiz: basic**

See [quiz app](#ch012.xhtml_quizzes).

## 37.9 (Advanced)

All of the remaining sections are advanced.

## 37.10 Default values

Normally, if a pattern has no match, the corresponding variable is set to `undefined`:

```
[](#cb985-1)const {prop: p} = {};
[](#cb985-2)assert.equal(p, undefined);
```

If you want a different value to be used, you need to specify a *default value* (via `=`):

```
[](#cb986-1)const {prop: p = 123} = {}; // (A)
[](#cb986-2)assert.equal(p, 123);
```

In line A, we specify the default value for `p` to be `123`. That default is used because the data that we are destructuring has no property named `prop`.

### 37.10.1 Default values in Array-destructuring

Here, we have two default values that are assigned to the variables `x` and `y` because the corresponding elements don’t exist in the Array that is destructured.

```
[](#cb987-1)const [x=1, y=2] = [];
[](#cb987-2)
[](#cb987-3)assert.equal(x, 1);
[](#cb987-4)assert.equal(y, 2);
```

The default value for the first element of the Array pattern is `1`; the default value for the second element is `2`.

### 37.10.2 Default values in object-destructuring

You can also specify default values for object-destructuring:

```
[](#cb988-1)const {first: f='', last: l=''} = {};
[](#cb988-2)assert.equal(f, '');
[](#cb988-3)assert.equal(l, '');
```

Neither property key `first` nor property key `last` exist in the object that is destructured. Therefore, the default values are used.

With property value shorthands, this code becomes simpler:

```
[](#cb989-1)const {first='', last=''} = {};
[](#cb989-2)assert.equal(first, '');
[](#cb989-3)assert.equal(last, '');
```

## 37.11 Parameter definitions are similar to destructuring

Considering what we have learned in this chapter, parameter definitions have much in common with an Array pattern (rest elements, default values, etc.). In fact, the following two function declarations are equivalent:

```
[](#cb990-1)function f1(«pattern1», «pattern2») {
[](#cb990-2)  // ···
[](#cb990-3)}
[](#cb990-4)
[](#cb990-5)function f2(...args) {
[](#cb990-6)  const [«pattern1», «pattern2»] = args;
[](#cb990-7)  // ···
[](#cb990-8)}
```

## 37.12 Nested destructuring

Until now, we have only used variables as *assignment targets* (data sinks) inside destructuring patterns. But you can also use patterns as assignment targets, which enables you to nest patterns to arbitrary depths:

```
[](#cb991-1)const arr = [
[](#cb991-2)  { first: 'Jane', last: 'Bond' },
[](#cb991-3)  { first: 'Lars', last: 'Croft' },
[](#cb991-4)];
[](#cb991-5)const [, {first}] = arr;
[](#cb991-6)assert.equal(first, 'Lars');
```

Inside the Array pattern in line A, there is a nested object pattern at index 1.

Nested patterns can become difficult to understand, so they are best used in moderation.

![](media/file7.svg)  **Quiz: advanced**

See [quiz app](#ch012.xhtml_quizzes).

# 38 Synchronous generators (advanced)

* * *

*   38.1 [What are synchronous generators?](#ch039.xhtml_what-are-synchronous-generators)
    *   38.1.1 [Generator functions return iterables and fill them via `yield`](#ch039.xhtml_generator-functions-return-iterables-and-fill-them-via-yield)
    *   38.1.2 [`yield` pauses a generator function](#ch039.xhtml_yield-pauses-a-generator-function)
    *   38.1.3 [Why does `yield` pause execution?](#ch039.xhtml_why-does-yield-pause-execution)
    *   38.1.4 [Example: Mapping over iterables](#ch039.xhtml_example-mapping-over-iterables)
*   38.2 [Calling generators from generators (advanced)](#ch039.xhtml_calling-generators-from-generators-advanced)
    *   38.2.1 [Calling generators via `yield*`](#ch039.xhtml_calling-generators-via-yield)
    *   38.2.2 [Example: Iterating over a tree](#ch039.xhtml_example-iterating-over-a-tree)
*   38.3 [Background: external iteration vs. internal iteration](#ch039.xhtml_external-iteration-internal-iteration)
*   38.4 [Use case for generators: reusing traversals](#ch039.xhtml_reusing-traversals)
    *   38.4.1 [The traversal to reuse](#ch039.xhtml_the-traversal-to-reuse)
    *   38.4.2 [Internal iteration (push)](#ch039.xhtml_internal-iteration-example)
    *   38.4.3 [External iteration (pull)](#ch039.xhtml_external-iteration-example)
*   38.5 [Advanced features of generators](#ch039.xhtml_advanced-features-of-generators)

* * *

## 38.1 What are synchronous generators?

Synchronous generators are special versions of function definitions and method definitions that always return synchronous iterables:

```
[](#cb992-1)// Generator function declaration
[](#cb992-2)function* genFunc1() { /*···*/ }
[](#cb992-3)
[](#cb992-4)// Generator function expression
[](#cb992-5)const genFunc2 = function* () { /*···*/ };
[](#cb992-6)
[](#cb992-7)// Generator method definition in an object literal
[](#cb992-8)const obj = {
[](#cb992-9)  * generatorMethod() {
[](#cb992-10)    // ···
[](#cb992-11)  }
[](#cb992-12)};
[](#cb992-13)
[](#cb992-14)// Generator method definition in a class definition
[](#cb992-15)// (class declaration or class expression)
[](#cb992-16)class MyClass {
[](#cb992-17)  * generatorMethod() {
[](#cb992-18)    // ···
[](#cb992-19)  }
[](#cb992-20)}
```

Asterisks (`*`) mark functions and methods as generators:

*   Functions: The pseudo-keyword `function*` is a combination of the keyword `function` and an asterisk.
*   Methods: The `*` is a modifier (similar to `static` and `get`).

### 38.1.1 Generator functions return iterables and fill them via `yield`

If you call a generator function, it returns an iterable (actually, an iterator that is also iterable). The generator fills that iterable via the `yield` operator:

```
[](#cb993-1)function* genFunc1() {
[](#cb993-2)  yield 'a';
[](#cb993-3)  yield 'b';
[](#cb993-4)}
[](#cb993-5)
[](#cb993-6)const iterable = genFunc1();
[](#cb993-7)// Convert the iterable to an Array, to check what’s inside:
[](#cb993-8)assert.deepEqual([...iterable], ['a', 'b']);
[](#cb993-9)
[](#cb993-10)// You can also use a for-of loop
[](#cb993-11)for (const x of genFunc1()) {
[](#cb993-12)  console.log(x);
[](#cb993-13)}
[](#cb993-14)// Output:
[](#cb993-15)// 'a'
[](#cb993-16)// 'b'
```

### 38.1.2 `yield` pauses a generator function

Using a generator function involves the following steps:

*   Function-calling it returns an iterator `iter` (that is also an iterable).
*   Iterating over `iter` repeatedly invokes `iter.next()`. Each time, we jump into the body of the generator function until there is a `yield` that returns a value.

Therefore, `yield` does more than just add values to iterables – it also pauses and exits the generator function:

*   Like `return`, a `yield` exits the body of the function and returns a value (via `.next()`).
*   Unlike `return`, if you repeat the invocation (of `.next()`), execution resumes directly after the `yield`.

Let’s examine what that means via the following generator function.

```
[](#cb994-1)let location = 0;
[](#cb994-2)function* genFunc2() {
[](#cb994-3)  location = 1; yield 'a';
[](#cb994-4)  location = 2; yield 'b';
[](#cb994-5)  location = 3;
[](#cb994-6)}
```

In order to use `genFunc2()`, we must first create the iterator/iterable `iter`. `genFunc2()` is now paused “before” its body.

```
[](#cb995-1)const iter = genFunc2();
[](#cb995-2)// genFunc2() is now paused “before” its body:
[](#cb995-3)assert.equal(location, 0);
```

`iter` implements [the iteration protocol](#ch031.xhtml_ch_sync-iteration). Therefore, we control the execution of `genFunc2()` via `iter.next()`. Calling that method resumes the paused `genFunc2()` and executes it until there is a `yield`. Then execution pauses and `.next()` returns the operand of the `yield`:

```
[](#cb996-1)assert.deepEqual(
[](#cb996-2)  iter.next(), {value: 'a', done: false});
[](#cb996-3)// genFunc2() is now paused directly after the first `yield`:
[](#cb996-4)assert.equal(location, 1);
```

Note that the yielded value `'a'` is wrapped in an object, which is how iterators always deliver their values.

We call `iter.next()` again and execution continues where we previously paused. Once we encounter the second `yield`, `genFunc2()` is paused and `.next()` returns the yielded value `'b'`.

```
[](#cb997-1)assert.deepEqual(
[](#cb997-2)  iter.next(), {value: 'b', done: false});
[](#cb997-3)// genFunc2() is now paused directly after the second `yield`:
[](#cb997-4)assert.equal(location, 2);
```

We call `iter.next()` one more time and execution continues until it leaves the body of `genFunc2()`:

```
[](#cb998-1)assert.deepEqual(
[](#cb998-2)  iter.next(), {value: undefined, done: true});
[](#cb998-3)// We have reached the end of genFunc2():
[](#cb998-4)assert.equal(location, 3);
```

This time, property `.done` of the result of `.next()` is `true`, which means that the iterator is finished.

### 38.1.3 Why does `yield` pause execution?

What are the benefits of `yield` pausing execution? Why doesn’t it simply work like the Array method `.push()` and fill the iterable with values without pausing?

Due to pausing, generators provide many of the features of *coroutines* (think processes that are multitasked cooperatively). For example, when you ask for the next value of an iterable, that value is computed *lazily* (on demand). The following two generator functions demonstrate what that means.

```
[](#cb999-1)/**
[](#cb999-2) * Returns an iterable over lines
[](#cb999-3) */
[](#cb999-4)function* genLines() {
[](#cb999-5)  yield 'A line';
[](#cb999-6)  yield 'Another line';
[](#cb999-7)  yield 'Last line';
[](#cb999-8)}
[](#cb999-9)
[](#cb999-10)/**
[](#cb999-11) * Input: iterable over lines
[](#cb999-12) * Output: iterable over numbered lines
[](#cb999-13) */
[](#cb999-14)function* numberLines(lineIterable) {
[](#cb999-15)  let lineNumber = 1;
[](#cb999-16)  for (const line of lineIterable) { // input
[](#cb999-17)    yield lineNumber + ': ' + line; // output
[](#cb999-18)    lineNumber++;
[](#cb999-19)  }
[](#cb999-20)}
```

Note that the `yield` in `numberLines()` appears inside a `for-of` loop. `yield` can be used inside loops, but not inside callbacks (more on that later).

Let’s combine both generators to produce the iterable `numberedLines`:

```
[](#cb1000-1)const numberedLines = numberLines(genLines());
[](#cb1000-2)assert.deepEqual(
[](#cb1000-3)  numberedLines.next(), {value: '1: A line', done: false});
[](#cb1000-4)assert.deepEqual(
[](#cb1000-5)  numberedLines.next(), {value: '2: Another line', done: false});
```

The key benefit of using generators here is that everything works incrementally: via `numberedLines.next()`, we ask `numberLines()` for only a single numbered line. In turn, it asks `genLines()` for only a single unnumbered line.

This incrementalism continues to work if, for example, `genLines()` reads its lines from a large text file: If we ask `numberLines()` for a numbered line, we get one as soon as `genLines()` has read its first line from the text file.

Without generators, `genLines()` would first read all lines and return them. Then `numberLines()` would number all lines and return them. We therefore have to wait much longer until we get the first numbered line.

![](media/file6.svg)  **Exercise: Turning a normal function into a generator**

`exercises/sync-generators/fib_seq_test.mjs`

### 38.1.4 Example: Mapping over iterables

The following function `mapIter()` is similar to the Array method `.map()`, but it returns an iterable, not an Array, and produces its results on demand.

```
[](#cb1001-1)function* mapIter(iterable, func) {
[](#cb1001-2)  let index = 0;
[](#cb1001-3)  for (const x of iterable) {
[](#cb1001-4)    yield func(x, index);
[](#cb1001-5)    index++;
[](#cb1001-6)  }
[](#cb1001-7)}
[](#cb1001-8)
[](#cb1001-9)const iterable = mapIter(['a', 'b'], x => x + x);
[](#cb1001-10)assert.deepEqual([...iterable], ['aa', 'bb']);
```

![](media/file6.svg)  **Exercise: Filtering iterables**

`exercises/sync-generators/filter_iter_gen_test.mjs`

## 38.2 Calling generators from generators (advanced)

### 38.2.1 Calling generators via `yield*`

`yield` only works directly inside generators – so far we haven’t seen a way of delegating yielding to another function or method.

Let’s first examine what does *not* work: in the following example, we’d like `foo()` to call `bar()`, so that the latter yields two values for the former. Alas, a naive approach fails:

```
[](#cb1002-1)function* bar() {
[](#cb1002-2)  yield 'a';
[](#cb1002-3)  yield 'b';
[](#cb1002-4)}
[](#cb1002-5)function* foo() {
[](#cb1002-6)  // Nothing happens if we call `bar()`:
[](#cb1002-7)  bar();
[](#cb1002-8)}
[](#cb1002-9)assert.deepEqual(
[](#cb1002-10)  [...foo()], []);
```

Why doesn’t this work? The function call `bar()` returns an iterable, which we ignore.

What we want is for `foo()` to yield everything that is yielded by `bar()`. That’s what the `yield*` operator does:

```
[](#cb1003-1)function* bar() {
[](#cb1003-2)  yield 'a';
[](#cb1003-3)  yield 'b';
[](#cb1003-4)}
[](#cb1003-5)function* foo() {
[](#cb1003-6)  yield* bar();
[](#cb1003-7)}
[](#cb1003-8)assert.deepEqual(
[](#cb1003-9)  [...foo()], ['a', 'b']);
```

In other words, the previous `foo()` is roughly equivalent to:

```
[](#cb1004-1)function* foo() {
[](#cb1004-2)  for (const x of bar()) {
[](#cb1004-3)    yield x;
[](#cb1004-4)  }
[](#cb1004-5)}
```

Note that `yield*` works with any iterable:

```
[](#cb1005-1)function* gen() {
[](#cb1005-2)  yield* [1, 2];
[](#cb1005-3)}
[](#cb1005-4)assert.deepEqual(
[](#cb1005-5)  [...gen()], [1, 2]);
```

### 38.2.2 Example: Iterating over a tree

`yield*` lets us make recursive calls in generators, which is useful when iterating over recursive data structures such as trees. Take, for example, the following data structure for binary trees.

```
[](#cb1006-1)class BinaryTree {
[](#cb1006-2)  constructor(value, left=null, right=null) {
[](#cb1006-3)    this.value = value;
[](#cb1006-4)    this.left = left;
[](#cb1006-5)    this.right = right;
[](#cb1006-6)  }
[](#cb1006-7)
[](#cb1006-8)  /** Prefix iteration: parent before children */
[](#cb1006-9)  * [Symbol.iterator]() {
[](#cb1006-10)    yield this.value;
[](#cb1006-11)    if (this.left) {
[](#cb1006-12)      // Same as yield* this.left[Symbol.iterator]()
[](#cb1006-13)      yield* this.left;
[](#cb1006-14)    }
[](#cb1006-15)    if (this.right) {
[](#cb1006-16)      yield* this.right;
[](#cb1006-17)    }
[](#cb1006-18)  }
[](#cb1006-19)}
```

Method `[Symbol.iterator]()` adds support for the iteration protocol, which means that we can use a `for-of` loop to iterate over an instance of `BinaryTree`:

```
[](#cb1007-1)const tree = new BinaryTree('a',
[](#cb1007-2)  new BinaryTree('b',
[](#cb1007-3)    new BinaryTree('c'),
[](#cb1007-4)    new BinaryTree('d')),
[](#cb1007-5)  new BinaryTree('e'));
[](#cb1007-6)
[](#cb1007-7)for (const x of tree) {
[](#cb1007-8)  console.log(x);
[](#cb1007-9)}
[](#cb1007-10)// Output:
[](#cb1007-11)// 'a'
[](#cb1007-12)// 'b'
[](#cb1007-13)// 'c'
[](#cb1007-14)// 'd'
[](#cb1007-15)// 'e'
```

![](media/file6.svg)  **Exercise: Iterating over a nested Array**

`exercises/sync-generators/iter_nested_arrays_test.mjs`

## 38.3 Background: external iteration vs. internal iteration

In preparation for the next section, we need to learn about two different styles of iterating over the values “inside” an object:

*   External iteration (pull): Your code asks the object for the values via an iteration protocol. For example, the `for-of` loop is based on JavaScript’s iteration protocol:

    ```
    [](#cb1008-1)for (const x of ['a', 'b']) {
    [](#cb1008-2)  console.log(x);
    [](#cb1008-3)}
    [](#cb1008-4)// Output:
    [](#cb1008-5)// 'a'
    [](#cb1008-6)// 'b'
    ```

*   Internal iteration (push): You pass a callback function to a method of the object and the method feeds the values to the callback. For example, Arrays have the method `.forEach()`:

    ```
    [](#cb1009-1)['a', 'b'].forEach((x) => {
    [](#cb1009-2)  console.log(x);
    [](#cb1009-3)});
    [](#cb1009-4)// Output:
    [](#cb1009-5)// 'a'
    [](#cb1009-6)// 'b'
    ```

The next section has examples for both styles of iteration.

## 38.4 Use case for generators: reusing traversals

One important use case for generators is extracting and reusing traversals.

### 38.4.1 The traversal to reuse

As an example, consider the following function that traverses a tree of files and logs their paths (it uses [the Node.js API](https://nodejs.org/en/docs/) for doing so):

```
[](#cb1010-1)function logPaths(dir) {
[](#cb1010-2)  for (const fileName of fs.readdirSync(dir)) {
[](#cb1010-3)    const filePath = path.resolve(dir, fileName);
[](#cb1010-4)    console.log(filePath);
[](#cb1010-5)    const stats = fs.statSync(filePath);
[](#cb1010-6)    if (stats.isDirectory()) {
[](#cb1010-7)      logPaths(filePath); // recursive call
[](#cb1010-8)    }
[](#cb1010-9)  }
[](#cb1010-10)}
```

Consider the following directory:

```
mydir/
    a.txt
    b.txt
    subdir/
        c.txt
```

Let’s log the paths inside `mydir/`:

```
[](#cb1012-1)logPaths('mydir');
[](#cb1012-2)
[](#cb1012-3)// Output:
[](#cb1012-4)// 'mydir/a.txt'
[](#cb1012-5)// 'mydir/b.txt'
[](#cb1012-6)// 'mydir/subdir'
[](#cb1012-7)// 'mydir/subdir/c.txt'
```

How can we reuse this traversal and do something other than logging the paths?

### 38.4.2 Internal iteration (push)

One way of reusing traversal code is via *internal iteration*: Each traversed value is passsed to a callback (line A).

```
[](#cb1013-1)function visitPaths(dir, callback) {
[](#cb1013-2)  for (const fileName of fs.readdirSync(dir)) {
[](#cb1013-3)    const filePath = path.resolve(dir, fileName);
[](#cb1013-4)    callback(filePath); // (A)
[](#cb1013-5)    const stats = fs.statSync(filePath);
[](#cb1013-6)    if (stats.isDirectory()) {
[](#cb1013-7)      visitPaths(filePath, callback);
[](#cb1013-8)    }
[](#cb1013-9)  }
[](#cb1013-10)}
[](#cb1013-11)const paths = [];
[](#cb1013-12)visitPaths('mydir', p => paths.push(p));
[](#cb1013-13)assert.deepEqual(
[](#cb1013-14)  paths,
[](#cb1013-15)  [
[](#cb1013-16)    'mydir/a.txt',
[](#cb1013-17)    'mydir/b.txt',
[](#cb1013-18)    'mydir/subdir',
[](#cb1013-19)    'mydir/subdir/c.txt',
[](#cb1013-20)  ]);
```

### 38.4.3 External iteration (pull)

Another way of reusing traversal code is via *external iteration*: We can write a generator that yields all traversed values (line A).

```
[](#cb1014-1)function* iterPaths(dir) {
[](#cb1014-2)  for (const fileName of fs.readdirSync(dir)) {
[](#cb1014-3)    const filePath = path.resolve(dir, fileName);
[](#cb1014-4)    yield filePath; // (A)
[](#cb1014-5)    const stats = fs.statSync(filePath);
[](#cb1014-6)    if (stats.isDirectory()) {
[](#cb1014-7)      yield* iterPaths(filePath);
[](#cb1014-8)    }
[](#cb1014-9)  }
[](#cb1014-10)}
[](#cb1014-11)const paths = [...iterPaths('mydir')];
```

## 38.5 Advanced features of generators

[The chapter on generators](https://exploringjs.com/es6/ch_generators.html) in *Exploring ES6* covers two features that are beyond the scope of this book:

*   `yield` can also *receive* data, via an argument of `.next()`.
*   Generators can also `return` values (not just `yield` them). Such values do not become iteration values, but can be retrieved via `yield*`.

# 39 Asynchronous programming in JavaScript

* * *

*   39.1 [A roadmap for asynchronous programming in JavaScript](#ch040.xhtml_a-roadmap-for-asynchronous-programming-in-javascript)
    *   39.1.1 [Synchronous functions](#ch040.xhtml_synchronous-functions)
    *   39.1.2 [JavaScript executes tasks sequentially in a single process](#ch040.xhtml_javascript-executes-tasks-sequentially-in-a-single-process)
    *   39.1.3 [Callback-based asynchronous functions](#ch040.xhtml_roadmap-callbacks-for-async)
    *   39.1.4 [Promise-based asynchronous functions](#ch040.xhtml_promise-based-asynchronous-functions)
    *   39.1.5 [Async functions](#ch040.xhtml_roadmap-async-functions)
    *   39.1.6 [Next steps](#ch040.xhtml_next-steps)
*   39.2 [The call stack](#ch040.xhtml_the-call-stack)
*   39.3 [The event loop](#ch040.xhtml_the-event-loop)
*   39.4 [How to avoid blocking the JavaScript process](#ch040.xhtml_how-to-avoid-blocking-the-javascript-process)
    *   39.4.1 [The user interface of the browser can be blocked](#ch040.xhtml_blocking-browsers)
    *   39.4.2 [How can we avoid blocking the browser?](#ch040.xhtml_web-workers)
    *   39.4.3 [Taking breaks](#ch040.xhtml_taking-breaks)
    *   39.4.4 [Run-to-completion semantics](#ch040.xhtml_run-to-completion-semantics)
*   39.5 [Patterns for delivering asynchronous results](#ch040.xhtml_patterns-for-delivering-asynchronous-results)
    *   39.5.1 [Delivering asynchronous results via events](#ch040.xhtml_event-pattern)
    *   39.5.2 [Delivering asynchronous results via callbacks](#ch040.xhtml_callback-pattern)
*   39.6 [Asynchronous code: the downsides](#ch040.xhtml_asynchronous-code-the-downsides)
*   39.7 [Resources](#ch040.xhtml_resources)

* * *

This chapter explains the foundations of asynchronous programming in JavaScript.

## 39.1 A roadmap for asynchronous programming in JavaScript

This section provides a roadmap for the content on asynchronous programming in JavaScript.

![](media/file0.svg)  **Don’t worry about the details!**

Don’t worry if you don’t understand everything yet. This is just a quick peek at what’s coming up.

### 39.1.1 Synchronous functions

Normal functions are *synchronous*: the caller waits until the callee is finished with its computation. `divideSync()` in line A is a synchronous function call:

```
[](#cb1015-1)function main() {
[](#cb1015-2)  try {
[](#cb1015-3)    const result = divideSync(12, 3); // (A)
[](#cb1015-4)    assert.equal(result, 4);
[](#cb1015-5)  } catch (err) {
[](#cb1015-6)    assert.fail(err);
[](#cb1015-7)  }
[](#cb1015-8)}
```

### 39.1.2 JavaScript executes tasks sequentially in a single process

By default, JavaScript *tasks* are functions that are executed sequentially in a single process. That looks like this:

```
[](#cb1016-1)while (true) {
[](#cb1016-2)  const task = taskQueue.dequeue();
[](#cb1016-3)  task(); // run task
[](#cb1016-4)}
```

This loop is also called the *event loop* because events, such as clicking a mouse, add tasks to the queue.

Due to this style of cooperative multitasking, we don’t want a task to block other tasks from being executed while, for example, it waits for results coming from a server. The next subsection explores how to handle this case.

### 39.1.3 Callback-based asynchronous functions

What if `divide()` needs a server to compute its result? Then the result should be delivered in a different manner: The caller shouldn’t have to wait (synchronously) until the result is ready; it should be notified (asynchronously) when it is. One way of delivering the result asynchronously is by giving `divide()` a callback function that it uses to notify the caller.

```
[](#cb1017-1)function main() {
[](#cb1017-2)  divideCallback(12, 3,
[](#cb1017-3)    (err, result) => {
[](#cb1017-4)      if (err) {
[](#cb1017-5)        assert.fail(err);
[](#cb1017-6)      } else {
[](#cb1017-7)        assert.equal(result, 4);
[](#cb1017-8)      }
[](#cb1017-9)    });
[](#cb1017-10)}
```

When there is an asynchronous function call:

```
[](#cb1018-1)divideCallback(x, y, callback)
```

Then the following steps happen:

*   `divideCallback()` sends a request to a server.
*   Then the current task `main()` is finished and other tasks can be executed.
*   When a response from the server arrives, it is either:
    *   An error `err`: Then the following task is added to the queue.

        ```
        [](#cb1019-1)taskQueue.enqueue(() => callback(err));
        ```

    *   A result `r`: Then the following task is added to the queue.

        ```
        [](#cb1020-1)taskQueue.enqueue(() => callback(null, r));
        ```

### 39.1.4 Promise-based asynchronous functions

Promises are two things:

*   A standard pattern that makes working with callbacks easier.
*   The mechanism on which *async functions* (the topic of the next subsection) are built.

Invoking a Promise-based function looks as follows.

```
[](#cb1021-1)function main() {
[](#cb1021-2)  dividePromise(12, 3)
[](#cb1021-3)    .then(result => assert.equal(result, 4))
[](#cb1021-4)    .catch(err => assert.fail(err));
[](#cb1021-5)}
```

### 39.1.5 Async functions

One way of looking at async functions is as better syntax for Promise-based code:

```
[](#cb1022-1)async function main() {
[](#cb1022-2)  try {
[](#cb1022-3)    const result = await dividePromise(12, 3); // (A)
[](#cb1022-4)    assert.equal(result, 4);
[](#cb1022-5)  } catch (err) {
[](#cb1022-6)    assert.fail(err);
[](#cb1022-7)  }
[](#cb1022-8)}
```

The `dividePromise()` we are calling in line A is the same Promise-based function as in the previous section. But we now have synchronous-looking syntax for handling the call. `await` can only be used inside a special kind of function, an *async function* (note the keyword `async` in front of the keyword `function`). `await` pauses the current async function and returns from it. Once the awaited result is ready, the execution of the function continues where it left off.

### 39.1.6 Next steps

*   In this chapter, we’ll see how synchronous function calls work. We’ll also explore JavaScript’s way of executing code in a single process, via its *event loop*.
*   [Asynchronicity via callbacks](#ch040.xhtml_callback-pattern) is also described in this chapter.
*   The following chapters cover [Promises](#ch041.xhtml_ch_promises) and [async functions](#ch042.xhtml_ch_async-functions).
*   This series of chapters on asynchronous programming concludes with [the chapter on asynchronous iteration](#ch043.xhtml_ch_async-iteration), which is similar to [synchronous iteration](#ch031.xhtml_ch_sync-iteration), but iterated values are delivered asynchronously.

## 39.2 The call stack

Whenever a function calls another function, we need to remember where to return to after the latter function is finished. That is typically done via a stack – the *call stack*: the caller pushes onto it the location to return to, and the callee jumps to that location after it is done.

This is an example where several calls happen:

```
[](#cb1023-1)function h(z) {
[](#cb1023-2)  const error = new Error();
[](#cb1023-3)  console.log(error.stack);
[](#cb1023-4)}
[](#cb1023-5)function g(y) {
[](#cb1023-6)  h(y + 1);
[](#cb1023-7)}
[](#cb1023-8)function f(x) {
[](#cb1023-9)  g(x + 1);
[](#cb1023-10)}
[](#cb1023-11)f(3);
[](#cb1023-12)// done
```

Initially, before running this piece of code, the call stack is empty. After the function call `f(3)` in line 11, the stack has one entry:

*   Line 12 (location in top-level scope)

After the function call `g(x + 1)` in line 9, the stack has two entries:

*   Line 10 (location in `f()`)
*   Line 12 (location in top-level scope)

After the function call `h(y + 1)` in line 6, the stack has three entries:

*   Line 7 (location in `g()`)
*   Line 10 (location in `f()`)
*   Line 12 (location in top-level scope)

Logging `error` in line 3, produces the following output:

```
Error: 
    at h (demos/async-js/stack_trace.mjs:2:17)
    at g (demos/async-js/stack_trace.mjs:6:3)
    at f (demos/async-js/stack_trace.mjs:9:3)
    at demos/async-js/stack_trace.mjs:11:1
```

This is a so-called *stack trace* of where the `Error` object was created. Note that it records where calls were made, not return locations. Creating the exception in line 2 is yet another call. That’s why the stack trace includes a location inside `h()`.

After line 3, each of the functions terminates and each time, the top entry is removed from the call stack. After function `f` is done, we are back in top-level scope and the stack is empty. When the code fragment ends then that is like an implicit `return`. If we consider the code fragment to be a task that is executed, then returning with an empty call stack ends the task.

## 39.3 The event loop

By default, JavaScript runs in a single process – in both web browsers and Node.js. The so-called *event loop* sequentially executes *tasks* (pieces of code) inside that process. The event loop is depicted in fig. [30](#ch040.xhtml_fig:event_loop).

![](media/file39.svg)

Figure 30: *Task sources* add code to run to the *task queue*, which is emptied by the *event loop*.

Two parties access the task queue:

*   *Task sources* add tasks to the queue. Some of those sources run concurrently to the JavaScript process. For example, one task source takes care of user interface events: if a user clicks somewhere and a click listener was registered, then an invocation of that listener is added to the task queue.

*   The *event loop* runs continuously inside the JavaScript process. During each loop iteration, it takes one task out of the queue (if the queue is empty, it waits until it isn’t) and executes it. That task is finished when the call stack is empty and there is a `return`. Control goes back to the event loop, which then retrieves the next task from the queue and executes it. And so on.

The following JavaScript code is an approximation of the event loop:

```
[](#cb1025-1)while (true) {
[](#cb1025-2)  const task = taskQueue.dequeue();
[](#cb1025-3)  task(); // run task
[](#cb1025-4)}
```

## 39.4 How to avoid blocking the JavaScript process

### 39.4.1 The user interface of the browser can be blocked

Many of the user interface mechanisms of browsers also run in the JavaScript process (as tasks). Therefore, long-running JavaScript code can block the user interface. Let’s look at a web page that demonstrates that. There are two ways in which you can try out that page:

*   You can [run it online](http://rauschma.github.io/async-examples/blocking.html).
*   You can open the following file inside the repository with the exercises: `demos/async-js/blocking.html`

The following HTML is the page’s user interface:

```
[](#cb1026-1)<a id="block" href="">Block</a>
[](#cb1026-2)<div id="statusMessage"></div>
[](#cb1026-3)<button>Click me!</button>
```

The idea is that you click “Block” and a long-running loop is executed via JavaScript. During that loop, you can’t click the button because the browser/JavaScript process is blocked.

A simplified version of the JavaScript code looks like this:

```
[](#cb1027-1)document.getElementById('block')
[](#cb1027-2)  .addEventListener('click', doBlock); // (A)
[](#cb1027-3)
[](#cb1027-4)function doBlock(event) {
[](#cb1027-5)  // ···
[](#cb1027-6)  displayStatus('Blocking...');
[](#cb1027-7)  // ···
[](#cb1027-8)  sleep(5000); // (B)
[](#cb1027-9)  displayStatus('Done');
[](#cb1027-10)}
[](#cb1027-11)
[](#cb1027-12)function sleep(milliseconds) {
[](#cb1027-13)  const start = Date.now();
[](#cb1027-14)  while ((Date.now() - start) < milliseconds);
[](#cb1027-15)}
[](#cb1027-16)function displayStatus(status) {
[](#cb1027-17)  document.getElementById('statusMessage')
[](#cb1027-18)    .textContent = status;
[](#cb1027-19)}
```

These are the key parts of the code:

*   Line A: We tell the browser to call `doBlock()` whenever the HTML element is clicked whose ID is `block`.
*   `doBlock()` displays status information and then calls `sleep()` to block the JavaScript process for 5000 milliseconds (line B).
*   `sleep()` blocks the JavaScript process by looping until enough time has passed.
*   `displayStatus()` displays status messages inside the `<div>` whose ID is `statusMessage`.

### 39.4.2 How can we avoid blocking the browser?

There are several ways in which you can prevent a long-running operation from blocking the browser:

*   The operation can deliver its result *asynchronously*: Some operations, such as downloads, can be performed concurrently to the JavaScript process. The JavaScript code triggering such an operation registers a callback, which is invoked with the result once the operation is finished. The invocation is handled via the task queue. This style of delivering a result is called *asynchronous* because the caller doesn’t wait until the results are ready. Normal function calls deliver their results synchronously.

*   Perform long computations in separate processes: This can be done via so-called *Web Workers*. Web Workers are heavyweight processes that run concurrently to the main process. Each one of them has its own runtime environment (global variables, etc.). They are completely isolated and must be communicated with via message passing. Consult [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) for more information.

*   Take breaks during long computations. The next subsection explains how.

### 39.4.3 Taking breaks

The following global function executes its parameter `callback` after a delay of `ms` milliseconds (the type signature is simplified – `setTimeout()` has more features):

```
[](#cb1028-1)function setTimeout(callback: () => void, ms: number): any
```

The function returns a *handle* (an ID) that can be used to *clear* the timeout (cancel the execution of the callback) via the following global function:

```
[](#cb1029-1)function clearTimeout(handle?: any): void
```

`setTimeout()` is available on both browsers and Node.js. The next subsection shows it in action.

![](media/file2.svg)  **`setTimeout()` lets tasks take breaks**

Another way of looking at `setTimeout()` is that the current task takes a break and continues later via the callback.

### 39.4.4 Run-to-completion semantics

JavaScript makes a guarantee for tasks:

> Each task is always finished (“run to completion”) before the next task is executed.

As a consequence, tasks don’t have to worry about their data being changed while they are working on it (*concurrent modification*). That simplifies programming in JavaScript.

The following example demonstrates this guarantee:

```
[](#cb1030-1)console.log('start');
[](#cb1030-2)setTimeout(() => {
[](#cb1030-3)  console.log('callback');
[](#cb1030-4)}, 0);
[](#cb1030-5)console.log('end');
[](#cb1030-6)
[](#cb1030-7)// Output:
[](#cb1030-8)// 'start'
[](#cb1030-9)// 'end'
[](#cb1030-10)// 'callback'
```

`setTimeout()` puts its parameter into the task queue. The parameter is therefore executed sometime after the current piece of code (task) is completely finished.

The parameter `ms` only specifies when the task is put into the queue, not when exactly it runs. It may even never run – for example, if there is a task before it in the queue that never terminates. That explains why the previous code logs `'end'` before `'callback'`, even though the parameter `ms` is `0`.

## 39.5 Patterns for delivering asynchronous results

In order to avoid blocking the main process while waiting for a long-running operation to finish, results are often delivered asynchronously in JavaScript. These are three popular patterns for doing so:

*   Events
*   Callbacks
*   Promises

The first two patterns are explained in the next two subsections. Promises are explained in [the next chapter](#ch041.xhtml_ch_promises).

### 39.5.1 Delivering asynchronous results via events

Events as a pattern work as follows:

*   They are used to deliver values asynchronously.
*   They do so zero or more times.
*   There are three roles in this pattern:
    *   The *event* (an object) carries the data to be delivered.
    *   The *event listener* is a function that receives events via a parameter.
    *   The *event source* sends events and lets you register event listeners.

Multiple variations of this pattern exist in the world of JavaScript. We’ll look at three examples next.

#### 39.5.1.1 Events: IndexedDB

IndexedDB is a database that is built into web browsers. This is an example of using it:

```
[](#cb1031-1)const openRequest = indexedDB.open('MyDatabase', 1); // (A)
[](#cb1031-2)
[](#cb1031-3)openRequest.onsuccess = (event) => {
[](#cb1031-4)  const db = event.target.result;
[](#cb1031-5)  // ···
[](#cb1031-6)};
[](#cb1031-7)
[](#cb1031-8)openRequest.onerror = (error) => {
[](#cb1031-9)  console.error(error);
[](#cb1031-10)};
```

`indexedDB` has an unusual way of invoking operations:

*   Each operation has an associated method for creating *request objects*. For example, in line A, the operation is “open”, the method is `.open()`, and the request object is `openRequest`.

*   The parameters for the operation are provided via the request object, not via parameters of the method. For example, the event listeners (functions) are stored in the properties `.onsuccess` and `.onerror`.

*   The invocation of the operation is added to the task queue via the method (in line A). That is, we configure the operation *after* its invocation has already been added to the queue. Only run-to-completion semantics saves us from race conditions here and ensures that the operation runs after the current code fragment is finished.

#### 39.5.1.2 Events: `XMLHttpRequest`

The `XMLHttpRequest` API lets us make downloads from within a web browser. This is how we download the file `http://example.com/textfile.txt`:

```
[](#cb1032-1)const xhr = new XMLHttpRequest(); // (A)
[](#cb1032-2)xhr.open('GET', 'http://example.com/textfile.txt'); // (B)
[](#cb1032-3)xhr.onload = () => { // (C)
[](#cb1032-4)  if (xhr.status == 200) {
[](#cb1032-5)    processData(xhr.responseText);
[](#cb1032-6)  } else {
[](#cb1032-7)    assert.fail(new Error(xhr.statusText));
[](#cb1032-8)  }
[](#cb1032-9)};
[](#cb1032-10)xhr.onerror = () => { // (D)
[](#cb1032-11)  assert.fail(new Error('Network error'));
[](#cb1032-12)};
[](#cb1032-13)xhr.send(); // (E)
[](#cb1032-14)
[](#cb1032-15)function processData(str) {
[](#cb1032-16)  assert.equal(str, 'Content of textfile.txt\n');
[](#cb1032-17)}
```

With this API, we first create a request object (line A), then configure it, then activate it (line E). The configuration consists of:

*   Specifying which HTTP request method to use (line B): `GET`, `POST`, `PUT`, etc.
*   Registering a listener (line C) that is notified if something could be downloaded. Inside the listener, we still need to determine if the download contains what we requested or informs us of an error. Note that some of the result data is delivered via the request object `xhr`. (I’m not a fan of this kind of mixing of input and output data.)
*   Registering a listener (line D) that is notified if there was a network error.

#### 39.5.1.3 Events: DOM

We have already seen DOM events in action in [§39.4.1 “The user interface of the browser can be blocked”](#ch040.xhtml_blocking-browsers). The following code also handles `click` events:

```
[](#cb1033-1)const element = document.getElementById('my-link'); // (A)
[](#cb1033-2)element.addEventListener('click', clickListener); // (B)
[](#cb1033-3)
[](#cb1033-4)function clickListener(event) {
[](#cb1033-5)  event.preventDefault(); // (C)
[](#cb1033-6)  console.log(event.shiftKey); // (D)
[](#cb1033-7)}
```

We first ask the browser to retrieve the HTML element whose ID is `'my-link'` (line A). Then we add a listener for all `click` events (line B). In the listener, we first tell the browser not to perform its default action (line C) – going to the target of the link. Then we log to the console if the shift key is currently pressed (line D).

### 39.5.2 Delivering asynchronous results via callbacks

Callbacks are another pattern for handling asynchronous results. They are only used for one-off results and have the advantage of being less verbose than events.

As an example, consider a function `readFile()` that reads a text file and returns its contents asynchronously. This is how you call `readFile()` if it uses Node.js-style callbacks:

```
[](#cb1034-1)readFile('some-file.txt', {encoding: 'utf8'},
[](#cb1034-2)  (error, data) => {
[](#cb1034-3)    if (error) {
[](#cb1034-4)      assert.fail(error);
[](#cb1034-5)      return;
[](#cb1034-6)    }
[](#cb1034-7)    assert.equal(data, 'The content of some-file.txt\n');
[](#cb1034-8)  });
```

There is a single callback that handles both success and failure. If the first parameter is not `null` then an error happened. Otherwise, the result can be found in the second parameter.

![](media/file6.svg)  **Exercises: Callback-based code**

The following exercises use tests for asynchronous code, which are different from tests for synchronous code. Consult [§11.3.2 “Asynchronous tests in AVA”](#ch012.xhtml_async-tests-ava) for more information.

*   From synchronous to callback-based code: `exercises/async-js/read_file_cb_exrc.mjs`
*   Implementing a callback-based version of `.map()`: `exercises/async-js/map_cb_test.mjs`

## 39.6 Asynchronous code: the downsides

In many situations, on either browsers or Node.js, you have no choice, you must use asynchronous code. In this chapter, we have seen several patterns that such code can use. All of them have two disadvantages:

*   Asynchronous code is more verbose than synchronous code.
*   If you call asynchronous code, your code must become asynchronous too. That’s because you can’t wait synchronously for an asynchronous result. Asynchronous code has an infectious quality.

The first disadvantage becomes less severe with Promises (covered in [the next chapter](#ch041.xhtml_ch_promises)) and mostly disappears with async functions (covered in [the chapter after next](#ch042.xhtml_ch_async-functions)).

Alas, the infectiousness of async code does not go away. But it is mitigated by the fact that switching between sync and async is easy with async functions.

## 39.7 Resources

*   [“Help, I’m stuck in an event-loop”](https://vimeo.com/96425312) by Philip Roberts (video).
*   [“Event loops”](https://www.w3.org/TR/html5/webappapis.html#event-loops), section in HTML5 spec.

# 40 Promises for asynchronous programming

* * *

*   40.1 [The basics of using Promises](#ch041.xhtml_the-basics-of-using-promises)
    *   40.1.1 [Using a Promise-based function](#ch041.xhtml_using-a-promise-based-function)
    *   40.1.2 [What is a Promise?](#ch041.xhtml_what-is-a-promise)
    *   40.1.3 [Implementing a Promise-based function](#ch041.xhtml_implementing-a-promise-based-function)
    *   40.1.4 [States of Promises](#ch041.xhtml_states-of-promises)
    *   40.1.5 [`Promise.resolve()`: create a Promise fulfilled with a given value](#ch041.xhtml_promise.resolve-create-a-promise-fulfilled-with-a-given-value)
    *   40.1.6 [`Promise.reject()`: create a Promise rejected with a given value](#ch041.xhtml_promise.reject-create-a-promise-rejected-with-a-given-value)
    *   40.1.7 [Returning and throwing in `.then()` callbacks](#ch041.xhtml_returning-and-throwing-in-.then-callbacks)
    *   40.1.8 [`.catch()` and its callback](#ch041.xhtml_catch-and-its-callback)
    *   40.1.9 [Chaining method calls](#ch041.xhtml_chaining-method-calls)
    *   40.1.10 [Advantages of promises](#ch041.xhtml_advantages-of-promises)
*   40.2 [Examples](#ch041.xhtml_examples-1)
    *   40.2.1 [Node.js: Reading a file asynchronously](#ch041.xhtml_node.js-reading-a-file-asynchronously)
    *   40.2.2 [Browsers: Promisifying `XMLHttpRequest`](#ch041.xhtml_promisifying-xmlhttprequest)
    *   40.2.3 [Node.js: `util.promisify()`](#ch041.xhtml_node.js-util.promisify)
    *   40.2.4 [Browsers: Fetch API](#ch041.xhtml_browsers-fetch-api)
*   40.3 [Error handling: don’t mix rejections and exceptions](#ch041.xhtml_error-handling-dont-mix-rejections-and-exceptions)
*   40.4 [Promise-based functions start synchronously, settle asynchronously](#ch041.xhtml_promise-based-functions-start-synchronously-settle-asynchronously)
*   40.5 [`Promise.all()`: concurrency and Arrays of Promises](#ch041.xhtml_promise.all-concurrency-and-arrays-of-promises)
    *   40.5.1 [Sequential execution vs. concurrent execution](#ch041.xhtml_sequential-execution-vs.-concurrent-execution)
    *   40.5.2 [Concurrency tip: focus on when operations start](#ch041.xhtml_focus-on-async-start)
    *   40.5.3 [`Promise.all()` is fork-join](#ch041.xhtml_promise-all-is-fork-join)
    *   40.5.4 [Asynchronous `.map()` via `Promise.all()`](#ch041.xhtml_asynchronous-.map-via-promise.all)
*   40.6 [Tips for chaining Promises](#ch041.xhtml_tips-for-chaining-promises)
    *   40.6.1 [Chaining mistake: losing the tail](#ch041.xhtml_chaining-mistake-losing-the-tail)
    *   40.6.2 [Chaining mistake: nesting](#ch041.xhtml_chaining-mistake-nesting)
    *   40.6.3 [Chaining mistake: more nesting than necessary](#ch041.xhtml_chaining-mistake-more-nesting-than-necessary)
    *   40.6.4 [Not all nesting is bad](#ch041.xhtml_not-all-nesting-is-bad)
    *   40.6.5 [Chaining mistake: creating Promises instead of chaining](#ch041.xhtml_chaining-mistake-creating-promises-instead-of-chaining)
*   40.7 [Advanced topics](#ch041.xhtml_advanced-topics-1)

* * *

In this chapter, we explore Promises, yet another pattern for delivering asynchronous results.

![](media/file0.svg)  **Recommended reading**

This chapter builds on [the previous chapter](#ch040.xhtml_ch_async-js) with background on asynchronous programming in JavaScript.

## 40.1 The basics of using Promises

Promises are a pattern for delivering results asynchronously.

### 40.1.1 Using a Promise-based function

The following code is an example of using the Promise-based function `addAsync()` (whose implementation is shown soon):

```
[](#cb1035-1)addAsync(3, 4)
[](#cb1035-2)  .then(result => { // success
[](#cb1035-3)    assert.equal(result, 7);
[](#cb1035-4)  })
[](#cb1035-5)  .catch(error => { // failure
[](#cb1035-6)    assert.fail(error);
[](#cb1035-7)  });
```

Promises are similar to [the event pattern](#ch040.xhtml_event-pattern): There is an object (a *Promise*), where we register callbacks:

*   Method `.then()` registers callbacks that handle results.
*   Method `.catch()` registers callbacks that handle errors.

A Promise-based function returns a Promise and sends it a result or an error (if and when it is done). The Promise passes it on to the relevant callbacks.

In contrast to the event pattern, Promises are optimized for one-off results:

*   A result (or an error) is cached so that it doesn’t matter if we register a callback before or after the result (or error) was sent.
*   We can chain the Promise methods `.then()` and `.catch()` because they both return Promises. That helps with sequentially invoking multiple asynchronous functions. More on that later.

### 40.1.2 What is a Promise?

What is a Promise? There are two ways of looking at it:

*   On one hand, it is a placeholder or container for the final result that will eventually be delivered.
*   On the other hand, it is an object with which we can register listeners.

### 40.1.3 Implementing a Promise-based function

This is an implementation of a Promise-based function that adds two numbers `x` and `y`:

```
[](#cb1036-1)function addAsync(x, y) {
[](#cb1036-2)  return new Promise(
[](#cb1036-3)    (resolve, reject) => { // (A)
[](#cb1036-4)      if (x === undefined || y === undefined) {
[](#cb1036-5)        reject(new Error('Must provide two parameters'));
[](#cb1036-6)      } else {
[](#cb1036-7)        resolve(x + y);
[](#cb1036-8)      }
[](#cb1036-9)    });
[](#cb1036-10)}
```

`addAsync()` immediately invokes the `Promise` constructor. The actual implementation of that function resides in the callback that is passed to that constructor (line A). That callback is provided with two functions:

*   `resolve` is used for delivering a result (in case of success).
*   `reject` is used for delivering an error (in case of failure).

### 40.1.4 States of Promises

![](media/file40.svg)

Figure 31: A Promise can be in either one of three states: pending, fulfilled, or rejected. If a Promise is in a final (non-pending) state, it is called *settled*.

Fig. [31](#ch041.xhtml_fig:promise_states_simple) depicts the three states a Promise can be in. Promises specialize in one-off results and protect us against *race conditions* (registering too early or too late):

*   If we register a `.then()` callback or a `.catch()` callback too early, it is notified once a Promise is settled.
*   Once a Promise is settled, the settlement value (result or error) is cached. Thus, if `.then()` or `.catch()` are called after the settlement, they receive the cached value.

Additionally, once a Promise is settled, its state and settlement value can’t change anymore. That helps make code predictable and enforces the one-off nature of Promises.

![](media/file5.svg)  **Some Promises are never settled**

It is possible that a Promise is never settled. For example:

```
[](#cb1037-1)new Promise(() => {})
```

### 40.1.5 `Promise.resolve()`: create a Promise fulfilled with a given value

`Promise.resolve(x)` creates a Promise that is fulfilled with the value `x`:

```
[](#cb1038-1)Promise.resolve(123)
[](#cb1038-2)  .then(x => {
[](#cb1038-3)    assert.equal(x, 123);
[](#cb1038-4)  });
```

If the parameter is already a Promise, it is returned unchanged:

```
[](#cb1039-1)const abcPromise = Promise.resolve('abc');
[](#cb1039-2)assert.equal(
[](#cb1039-3)  Promise.resolve(abcPromise),
[](#cb1039-4)  abcPromise);
```

Therefore, given an arbitrary value `x`, we can use `Promise.resolve(x)` to ensure we have a Promise.

Note that the name is `resolve`, not `fulfill`, because `.resolve()` returns a rejected Promise if its Parameter is a rejected Promise.

### 40.1.6 `Promise.reject()`: create a Promise rejected with a given value

`Promise.reject(err)` creates a Promise that is rejected with the value `err`:

```
[](#cb1040-1)const myError = new Error('My error!');
[](#cb1040-2)Promise.reject(myError)
[](#cb1040-3)  .catch(err => {
[](#cb1040-4)    assert.equal(err, myError);
[](#cb1040-5)  });
```

### 40.1.7 Returning and throwing in `.then()` callbacks

`.then()` handles Promise fulfillments. It also returns a fresh Promise. How that Promise is settled depends on what happens inside the callback. Let’s look at three common cases.

#### 40.1.7.1 Returning a non-Promise value

First, the callback can return a non-Promise value (line A). Consequently, the Promise returned by `.then()` is fulfilled with that value (as checked in line B):

```
[](#cb1041-1)Promise.resolve('abc')
[](#cb1041-2)  .then(str => {
[](#cb1041-3)    return str + str; // (A)
[](#cb1041-4)  })
[](#cb1041-5)  .then(str2 => {
[](#cb1041-6)    assert.equal(str2, 'abcabc'); // (B)
[](#cb1041-7)  });
```

#### 40.1.7.2 Returning a Promise

Second, the callback can return a Promise `p` (line A). Consequently, `p` “becomes” what `.then()` returns. In other words: the Promise that `.then()` has already returned is effectively replaced by `p`.

```
[](#cb1042-1)Promise.resolve('abc')
[](#cb1042-2)  .then(str => {
[](#cb1042-3)    return Promise.resolve(123); // (A)
[](#cb1042-4)  })
[](#cb1042-5)  .then(num => {
[](#cb1042-6)    assert.equal(num, 123);
[](#cb1042-7)  });
```

Why is that useful? We can return the result of a Promise-based operation and process its fulfillment value via a “flat” (non-nested) `.then()`. Compare:

```
[](#cb1043-1)// Flat
[](#cb1043-2)asyncFunc1()
[](#cb1043-3)  .then(result1 => {
[](#cb1043-4)    /*···*/
[](#cb1043-5)    return asyncFunc2();
[](#cb1043-6)  })
[](#cb1043-7)  .then(result2 => {
[](#cb1043-8)    /*···*/
[](#cb1043-9)  });
[](#cb1043-10)
[](#cb1043-11)// Nested
[](#cb1043-12)asyncFunc1()
[](#cb1043-13)  .then(result1 => {
[](#cb1043-14)    /*···*/
[](#cb1043-15)    asyncFunc2()
[](#cb1043-16)    .then(result2 => {
[](#cb1043-17)      /*···*/
[](#cb1043-18)    });
[](#cb1043-19)  });
```

#### 40.1.7.3 Throwing an exception

Third, the callback can throw an exception. Consequently, the Promise returned by `.then()` is rejected with that exception. That is, a synchronous error is converted into an asynchronous error.

```
[](#cb1044-1)const myError = new Error('My error!');
[](#cb1044-2)Promise.resolve('abc')
[](#cb1044-3)  .then(str => {
[](#cb1044-4)    throw myError;
[](#cb1044-5)  })
[](#cb1044-6)  .catch(err => {
[](#cb1044-7)    assert.equal(err, myError);
[](#cb1044-8)  });
```

### 40.1.8 `.catch()` and its callback

The only difference between `.then()` and `.catch()` is that the latter is triggered by rejections, not fulfillments. However, both methods turn the actions of their callbacks into Promises in the same manner. For example, in the following code, the value returned by the `.catch()` callback in line A becomes a fulfillment value:

```
[](#cb1045-1)const err = new Error();
[](#cb1045-2)
[](#cb1045-3)Promise.reject(err)
[](#cb1045-4)  .catch(e => {
[](#cb1045-5)    assert.equal(e, err);
[](#cb1045-6)    // Something went wrong, use a default value
[](#cb1045-7)    return 'default value'; // (A)
[](#cb1045-8)  })
[](#cb1045-9)  .then(str => {
[](#cb1045-10)    assert.equal(str, 'default value');
[](#cb1045-11)  });
```

### 40.1.9 Chaining method calls

`.then()` and `.catch()` always return Promises. That enables us to create arbitrary long chains of method calls:

```
[](#cb1046-1)function myAsyncFunc() {
[](#cb1046-2)  return asyncFunc1() // (A)
[](#cb1046-3)    .then(result1 => {
[](#cb1046-4)      // ···
[](#cb1046-5)      return asyncFunc2(); // a Promise
[](#cb1046-6)    })
[](#cb1046-7)    .then(result2 => {
[](#cb1046-8)      // ···
[](#cb1046-9)      return result2 || '(Empty)'; // not a Promise
[](#cb1046-10)    })
[](#cb1046-11)    .then(result3 => {
[](#cb1046-12)      // ···
[](#cb1046-13)      return asyncFunc4(); // a Promise
[](#cb1046-14)    });
[](#cb1046-15)}
```

Due to chaining, the `return` in line A returns the result of the last `.then()`.

In a way, `.then()` is the asynchronous version of the synchronous semicolon:

*   `.then()` executes two asynchronous operations sequentially.
*   The semicolon executes two synchronous operations sequentially.

We can also add `.catch()` into the mix and let it handle multiple error sources at the same time:

```
[](#cb1047-1)asyncFunc1()
[](#cb1047-2)  .then(result1 => {
[](#cb1047-3)    // ···
[](#cb1047-4)    return asyncFunction2();
[](#cb1047-5)  })
[](#cb1047-6)  .then(result2 => {
[](#cb1047-7)    // ···
[](#cb1047-8)  })
[](#cb1047-9)  .catch(error => {
[](#cb1047-10)    // Failure: handle errors of asyncFunc1(), asyncFunc2()
[](#cb1047-11)    // and any (sync) exceptions thrown in previous callbacks
[](#cb1047-12)  });
```

### 40.1.10 Advantages of promises

These are some of the advantages of Promises over plain callbacks when it comes to handling one-off results:

*   The type signatures of Promise-based functions and methods are cleaner: if a function is callback-based, some parameters are about input, while the one or two callbacks at the end are about output. With Promises, everything output-related is handled via the returned value.

*   Chaining asynchronous processing steps is more convenient.

*   Promises handle both asynchronous errors (via rejections) and synchronous errors: Inside the callbacks for `new Promise()`, `.then()`, and `.catch()`, exceptions are converted to rejections. In contrast, if we use callbacks for asynchronicity, exceptions are normally not handled for us; we have to do it ourselves.

*   Promises are a single standard that is slowly replacing several, mutually incompatible alternatives. For example, in Node.js, many functions are now available in Promise-based versions. And new asynchronous browser APIs are usually Promise-based.

One of the biggest advantages of Promises involves not working with them directly: they are the foundation of *async functions*, a synchronous-looking syntax for performing asynchronous computations. Asynchronous functions are covered in [the next chapter](#ch042.xhtml_ch_async-functions).

## 40.2 Examples

Seeing Promises in action helps with understanding them. Let’s look at examples.

### 40.2.1 Node.js: Reading a file asynchronously

Consider the following text file `person.json` with [JSON data](#ch046.xhtml_ch_json) in it:

```
[](#cb1048-1){
[](#cb1048-2)  "first": "Jane",
[](#cb1048-3)  "last": "Doe"
[](#cb1048-4)}
```

Let’s look at two versions of code that reads this file and parses it into an object. First, a callback-based version. Second, a Promise-based version.

#### 40.2.1.1 The callback-based version

The following code reads the contents of this file and converts it to a JavaScript object. It is based on Node.js-style callbacks:

```
[](#cb1049-1)import * as fs from 'fs';
[](#cb1049-2)fs.readFile('person.json',
[](#cb1049-3)  (error, text) => {
[](#cb1049-4)    if (error) { // (A)
[](#cb1049-5)      // Failure
[](#cb1049-6)      assert.fail(error);
[](#cb1049-7)    } else {
[](#cb1049-8)      // Success
[](#cb1049-9)      try { // (B)
[](#cb1049-10)        const obj = JSON.parse(text); // (C)
[](#cb1049-11)        assert.deepEqual(obj, {
[](#cb1049-12)          first: 'Jane',
[](#cb1049-13)          last: 'Doe',
[](#cb1049-14)        });
[](#cb1049-15)      } catch (e) {
[](#cb1049-16)        // Invalid JSON
[](#cb1049-17)        assert.fail(e);
[](#cb1049-18)      }
[](#cb1049-19)    }
[](#cb1049-20)  });
```

`fs` is a built-in Node.js module for file system operations. We use the callback-based function `fs.readFile()` to read a file whose name is `person.json`. If we succeed, the content is delivered via the parameter `text` as a string. In line C, we convert that string from the text-based data format JSON into a JavaScript object. `JSON` is an object with methods for consuming and producing JSON. It is part of JavaScript’s standard library and documented [later in this book](#ch046.xhtml_ch_json).

Note that there are two error-handling mechanisms: the `if` in line A takes care of asynchronous errors reported by `fs.readFile()`, while the `try` in line B takes care of synchronous errors reported by `JSON.parse()`.

#### 40.2.1.2 The Promise-based version

The following code uses `readFileAsync()`, a Promise-based version of `fs.readFile()` (created via `util.promisify()`, which is explained later):

```
[](#cb1050-1)readFileAsync('person.json')
[](#cb1050-2)  .then(text => { // (A)
[](#cb1050-3)    // Success
[](#cb1050-4)    const obj = JSON.parse(text);
[](#cb1050-5)    assert.deepEqual(obj, {
[](#cb1050-6)      first: 'Jane',
[](#cb1050-7)      last: 'Doe',
[](#cb1050-8)    });
[](#cb1050-9)  })
[](#cb1050-10)  .catch(err => { // (B)
[](#cb1050-11)    // Failure: file I/O error or JSON syntax error
[](#cb1050-12)    assert.fail(err);
[](#cb1050-13)  });
```

Function `readFileAsync()` returns a Promise. In line A, we specify a success callback via method `.then()` of that Promise. The remaining code in `then`’s callback is synchronous.

`.then()` returns a Promise, which enables the invocation of the Promise method `.catch()` in line B. We use it to specify a failure callback.

Note that `.catch()` lets us handle both the asynchronous errors of `readFileAsync()` and the synchronous errors of `JSON.parse()` because exceptions inside a `.then()` callback become rejections.

### 40.2.2 Browsers: Promisifying `XMLHttpRequest`

We have previously seen the event-based `XMLHttpRequest` API for downloading data in web browsers. The following function promisifies that API:

```
[](#cb1051-1)function httpGet(url) {
[](#cb1051-2)  return new Promise(
[](#cb1051-3)    (resolve, reject) => {
[](#cb1051-4)      const xhr = new XMLHttpRequest();
[](#cb1051-5)      xhr.onload = () => {
[](#cb1051-6)        if (xhr.status === 200) {
[](#cb1051-7)          resolve(xhr.responseText); // (A)
[](#cb1051-8)        } else {
[](#cb1051-9)          // Something went wrong (404, etc.)
[](#cb1051-10)          reject(new Error(xhr.statusText)); // (B)
[](#cb1051-11)        }
[](#cb1051-12)      }
[](#cb1051-13)      xhr.onerror = () => {
[](#cb1051-14)        reject(new Error('Network error')); // (C)
[](#cb1051-15)      };
[](#cb1051-16)      xhr.open('GET', url);
[](#cb1051-17)      xhr.send();
[](#cb1051-18)    });
[](#cb1051-19)}
```

Note how the results and errors of `XMLHttpRequest` are handled via `resolve()` and `reject()`:

*   A successful outcome leads to the returned Promise being fullfilled with it (line A).
*   An error leads to the Promise being rejected (lines B and C).

This is how to use `httpGet()`:

```
[](#cb1052-1)httpGet('http://example.com/textfile.txt')
[](#cb1052-2)  .then(content => {
[](#cb1052-3)    assert.equal(content, 'Content of textfile.txt\n');
[](#cb1052-4)  })
[](#cb1052-5)  .catch(error => {
[](#cb1052-6)    assert.fail(error);
[](#cb1052-7)  });
```

![](media/file6.svg)  **Exercise: Timing out a Promise**

`exercises/promises/promise_timeout_test.mjs`

### 40.2.3 Node.js: `util.promisify()`

`util.promisify()` is a utility function that converts a callback-based function `f` into a Promise-based one. That is, we are going from this type signature:

```
f(arg_1, ···, arg_n, (err: Error, result: T) => void) : void
```

To this type signature:

```
f(arg_1, ···, arg_n) : Promise<T>
```

The following code promisifies the callback-based `fs.readFile()` (line A) and uses it:

```
[](#cb1055-1)import * as fs from 'fs';
[](#cb1055-2)import {promisify} from 'util';
[](#cb1055-3)
[](#cb1055-4)const readFileAsync = promisify(fs.readFile); // (A)
[](#cb1055-5)
[](#cb1055-6)readFileAsync('some-file.txt', {encoding: 'utf8'})
[](#cb1055-7)  .then(text => {
[](#cb1055-8)    assert.equal(text, 'The content of some-file.txt\n');
[](#cb1055-9)  })
[](#cb1055-10)  .catch(err => {
[](#cb1055-11)    assert.fail(err);
[](#cb1055-12)  });
```

![](media/file6.svg)  **Exercises: `util.promisify()`**

*   Using `util.promisify()`: `exercises/promises/read_file_async_exrc.mjs`
*   Implementing `util.promisify()` yourself: `exercises/promises/my_promisify_test.mjs`

### 40.2.4 Browsers: Fetch API

All modern browsers support Fetch, a new Promise-based API for downloading data. Think of it as a Promise-based version of `XMLHttpRequest`. The following is an excerpt of [the API](https://fetch.spec.whatwg.org/#fetch-api):

```
[](#cb1056-1)interface Body {
[](#cb1056-2)  text() : Promise<string>;
[](#cb1056-3)  ···
[](#cb1056-4)}
[](#cb1056-5)interface Response extends Body {
[](#cb1056-6)  ···
[](#cb1056-7)}
[](#cb1056-8)declare function fetch(str) : Promise<Response>;
```

That means we can use `fetch()` as follows:

```
[](#cb1057-1)fetch('http://example.com/textfile.txt')
[](#cb1057-2)  .then(response => response.text())
[](#cb1057-3)  .then(text => {
[](#cb1057-4)    assert.equal(text, 'Content of textfile.txt\n');
[](#cb1057-5)  });
```

![](media/file6.svg)  **Exercise: Using the fetch API**

`exercises/promises/fetch_json_test.mjs`

## 40.3 Error handling: don’t mix rejections and exceptions

Rule for implementing functions and methods:

> Don’t mix (asynchronous) rejections and (synchronous) exceptions.

This makes our synchronous and asynchronous code more predictable and simpler because we can always focus on a single error-handling mechanism.

For Promise-based functions and methods, the rule means that they should never throw exceptions. Alas, it is easy to accidentally get this wrong – for example:

```
[](#cb1058-1)// Don’t do this
[](#cb1058-2)function asyncFunc() {
[](#cb1058-3)  doSomethingSync(); // (A)
[](#cb1058-4)  return doSomethingAsync()
[](#cb1058-5)    .then(result => {
[](#cb1058-6)      // ···
[](#cb1058-7)    });
[](#cb1058-8)}
```

The problem is that if an exception is thrown in line A, then `asyncFunc()` will throw an exception. Callers of that function only expect rejections and are not prepared for an exception. There are three ways in which we can fix this issue.

We can wrap the whole body of the function in a `try-catch` statement and return a rejected Promise if an exception is thrown:

```
[](#cb1059-1)// Solution 1
[](#cb1059-2)function asyncFunc() {
[](#cb1059-3)  try {
[](#cb1059-4)    doSomethingSync();
[](#cb1059-5)    return doSomethingAsync()
[](#cb1059-6)      .then(result => {
[](#cb1059-7)        // ···
[](#cb1059-8)      });
[](#cb1059-9)  } catch (err) {
[](#cb1059-10)    return Promise.reject(err);
[](#cb1059-11)  }
[](#cb1059-12)}
```

Given that `.then()` converts exceptions to rejections, we can execute `doSomethingSync()` inside a `.then()` callback. To do so, we start a Promise chain via `Promise.resolve()`. We ignore the fulfillment value `undefined` of that initial Promise.

```
[](#cb1060-1)// Solution 2
[](#cb1060-2)function asyncFunc() {
[](#cb1060-3)  return Promise.resolve()
[](#cb1060-4)    .then(() => {
[](#cb1060-5)      doSomethingSync();
[](#cb1060-6)      return doSomethingAsync();
[](#cb1060-7)    })
[](#cb1060-8)    .then(result => {
[](#cb1060-9)      // ···
[](#cb1060-10)    });
[](#cb1060-11)}
```

Lastly, `new Promise()` also converts exceptions to rejections. Using this constructor is therefore similar to the previous solution:

```
[](#cb1061-1)// Solution 3
[](#cb1061-2)function asyncFunc() {
[](#cb1061-3)  return new Promise((resolve, reject) => {
[](#cb1061-4)      doSomethingSync();
[](#cb1061-5)      resolve(doSomethingAsync());
[](#cb1061-6)    })
[](#cb1061-7)    .then(result => {
[](#cb1061-8)      // ···
[](#cb1061-9)    });
[](#cb1061-10)}
```

## 40.4 Promise-based functions start synchronously, settle asynchronously

Most Promise-based functions are executed as follows:

*   Their execution starts right away, synchronously (in the current task).
*   But the Promise they return is guaranteed to be settled asynchronously (in a later task) – if ever.

The following code demonstrates that:

```
[](#cb1062-1)function asyncFunc() {
[](#cb1062-2)  console.log('asyncFunc');
[](#cb1062-3)  return new Promise(
[](#cb1062-4)    (resolve, _reject) => {
[](#cb1062-5)      console.log('new Promise()');
[](#cb1062-6)      resolve();
[](#cb1062-7)    });
[](#cb1062-8)}
[](#cb1062-9)console.log('START');
[](#cb1062-10)asyncFunc()
[](#cb1062-11)  .then(() => {
[](#cb1062-12)    console.log('.then()'); // (A)
[](#cb1062-13)  });
[](#cb1062-14)console.log('END');
[](#cb1062-15)
[](#cb1062-16)// Output:
[](#cb1062-17)// 'START'
[](#cb1062-18)// 'asyncFunc'
[](#cb1062-19)// 'new Promise()'
[](#cb1062-20)// 'END'
[](#cb1062-21)// '.then()'
```

We can see that the callback of `new Promise()` is executed before the end of the code, while the result is delivered later (line A).

Benefits of this approach:

*   Starting synchronously helps avoid race conditions because we can rely on the order in which Promise-based functions begin. There is an example [in the next chapter](#ch042.xhtml_fire-and-forget-await), where text is written to a file and race conditions are avoided.

*   Chaining Promises won’t starve other tasks of processing time because before a Promise is settled, there will always be a break, during which the event loop can run.

*   Promise-based functions always return results asynchronously; we can be sure that there is never a synchronous return. This kind of predictability makes code easier to work with.

![](media/file1.svg)  **More information on this approach**

[“Designing APIs for Asynchrony”](http://blog.izs.me/post/59142742143/designing-apis-for-asynchrony) by Isaac Z. Schlueter

## 40.5 `Promise.all()`: concurrency and Arrays of Promises

### 40.5.1 Sequential execution vs. concurrent execution

Consider the following code:

```
[](#cb1063-1)const asyncFunc1 = () => Promise.resolve('one');
[](#cb1063-2)const asyncFunc2 = () => Promise.resolve('two');
[](#cb1063-3)
[](#cb1063-4)asyncFunc1()
[](#cb1063-5)  .then(result1 => {
[](#cb1063-6)    assert.equal(result1, 'one');
[](#cb1063-7)    return asyncFunc2();
[](#cb1063-8)  })
[](#cb1063-9)  .then(result2 => {
[](#cb1063-10)    assert.equal(result2, 'two');
[](#cb1063-11)  });
```

Using `.then()` in this manner executes Promise-based functions *sequentially*: only after the result of `asyncFunc1()` is settled will `asyncFunc2()` be executed.

The static method `Promise.all()` helps execute Promise-based functions more concurrently:

```
[](#cb1064-1)Promise.all([asyncFunc1(), asyncFunc2()])
[](#cb1064-2)  .then(arr => {
[](#cb1064-3)    assert.deepEqual(arr, ['one', 'two']);
[](#cb1064-4)  });
```

Its type signature is:

```
[](#cb1065-1)Promise.all<T>(promises: Iterable<Promise<T>>): Promise<T[]>
```

The parameter `promises` is an iterable of Promises. The result is a single Promise that is settled as follows:

*   If and when all input Promises are fulfilled, the output Promise is fulfilled with an Array of the fulfillment values.
*   As soon as at least one input Promise is rejected, the output Promise is rejected with the rejection value of that input Promise.

In other words: We go from an iterable of Promises to a Promise for an Array.

### 40.5.2 Concurrency tip: focus on when operations start

Tip for determining how “concurrent” asynchronous code is: Focus on when asynchronous operations start, not on how their Promises are handled.

For example, each of the following functions executes `asyncFunc1()` and `asyncFunc2()` concurrently because they are started at nearly the same time.

```
[](#cb1066-1)function concurrentAll() {
[](#cb1066-2)  return Promise.all([asyncFunc1(), asyncFunc2()]);
[](#cb1066-3)}
[](#cb1066-4)
[](#cb1066-5)function concurrentThen() {
[](#cb1066-6)  const p1 = asyncFunc1();
[](#cb1066-7)  const p2 = asyncFunc2();
[](#cb1066-8)  return p1.then(r1 => p2.then(r2 => [r1, r2]));
[](#cb1066-9)}
```

On the other hand, both of the following functions execute `asyncFunc1()` and `asyncFunc2()` sequentially: `asyncFunc2()` is only invoked after the Promise of `asyncFunc1()` is fulfilled.

```
[](#cb1067-1)function sequentialThen() {
[](#cb1067-2)  return asyncFunc1()
[](#cb1067-3)    .then(r1 => asyncFunc2()
[](#cb1067-4)      .then(r2 => [r1, r2]));
[](#cb1067-5)}
[](#cb1067-6)
[](#cb1067-7)function sequentialAll() {
[](#cb1067-8)  const p1 = asyncFunc1();
[](#cb1067-9)  const p2 = p1.then(() => asyncFunc2());
[](#cb1067-10)  return Promise.all([p1, p2]);
[](#cb1067-11)}
```

### 40.5.3 `Promise.all()` is fork-join

`Promise.all()` is loosely related to the concurrency pattern “fork join” – for example:

```
[](#cb1068-1)Promise.all([
[](#cb1068-2)    // Fork async computations
[](#cb1068-3)    httpGet('http://example.com/file1.txt'),
[](#cb1068-4)    httpGet('http://example.com/file2.txt'),
[](#cb1068-5)  ])
[](#cb1068-6)  // Join async computations
[](#cb1068-7)  .then(([text1, text2]) => {
[](#cb1068-8)    assert.equal(text1, 'Content of file1.txt\n');
[](#cb1068-9)    assert.equal(text2, 'Content of file2.txt\n');
[](#cb1068-10)  });
```

`httpGet()` is the promisified version of `XMLHttpRequest` that we implemented [earlier](#ch041.xhtml_promisifying-xmlhttprequest).

### 40.5.4 Asynchronous `.map()` via `Promise.all()`

Array transformation methods such as `.map()`, `.filter()`, etc., are made for synchronous computations – for example:

```
[](#cb1069-1)function timesTwoSync(x) {
[](#cb1069-2)  return 2 * x;
[](#cb1069-3)}
[](#cb1069-4)const arr = [1, 2, 3];
[](#cb1069-5)const result = arr.map(timesTwoSync);
[](#cb1069-6)assert.deepEqual(result, [2, 4, 6]);
```

What happens if the callback of `.map()` is a Promise-based function (a function that maps normal values to Promises)? Then the result of `.map()` is an Array of Promises. Alas, that is not data that normal code can work with. Thankfully, we can fix that via `Promise.all()`: It converts an Array of Promises into a Promise that is fulfilled with an Array of normal values.

```
[](#cb1070-1)function timesTwoAsync(x) {
[](#cb1070-2)  return new Promise(resolve => resolve(x * 2));
[](#cb1070-3)}
[](#cb1070-4)const arr = [1, 2, 3];
[](#cb1070-5)const promiseArr = arr.map(timesTwoAsync);
[](#cb1070-6)Promise.all(promiseArr)
[](#cb1070-7)  .then(result => {
[](#cb1070-8)    assert.deepEqual(result, [2, 4, 6]);
[](#cb1070-9)  });
```

#### 40.5.4.1 A more realistic example

The following code is a more realistic example: in the section on fork-join, there was an example where we downloaded two resources identified by two fixed URLs. Let’s turn that code fragment into a function that accepts an Array of URLs and downloads the corresponding resources:

```
[](#cb1071-1)function downloadTexts(urls) {
[](#cb1071-2)  const promisedTexts = urls.map(httpGet);
[](#cb1071-3)  return Promise.all(promisedTexts);
[](#cb1071-4)}
[](#cb1071-5)
[](#cb1071-6)downloadTexts([
[](#cb1071-7)    'http://example.com/file1.txt',
[](#cb1071-8)    'http://example.com/file2.txt',
[](#cb1071-9)  ])
[](#cb1071-10)  .then(texts => {
[](#cb1071-11)    assert.deepEqual(
[](#cb1071-12)      texts, [
[](#cb1071-13)        'Content of file1.txt\n',
[](#cb1071-14)        'Content of file2.txt\n',
[](#cb1071-15)      ]);
[](#cb1071-16)  });
```

![](media/file6.svg)  **Exercise: `Promise.all()` and listing files**

`exercises/promises/list_files_async_test.mjs`

## 40.6 Tips for chaining Promises

This section gives tips for chaining Promises.

### 40.6.1 Chaining mistake: losing the tail

Problem:

```
[](#cb1072-1)// Don’t do this
[](#cb1072-2)function foo() {
[](#cb1072-3)  const promise = asyncFunc();
[](#cb1072-4)  promise.then(result => {
[](#cb1072-5)    // ···
[](#cb1072-6)  });
[](#cb1072-7)
[](#cb1072-8)  return promise;
[](#cb1072-9)}
```

Computation starts with the Promise returned by `asyncFunc()`. But afterward, computation continues and another Promise is created via `.then()`. `foo()` returns the former Promise, but should return the latter. This is how to fix it:

```
[](#cb1073-1)function foo() {
[](#cb1073-2)  const promise = asyncFunc();
[](#cb1073-3)  return promise.then(result => {
[](#cb1073-4)    // ···
[](#cb1073-5)  });
[](#cb1073-6)}
```

### 40.6.2 Chaining mistake: nesting

Problem:

```
[](#cb1074-1)// Don’t do this
[](#cb1074-2)asyncFunc1()
[](#cb1074-3)  .then(result1 => {
[](#cb1074-4)    return asyncFunc2()
[](#cb1074-5)    .then(result2 => { // (A)
[](#cb1074-6)      // ···
[](#cb1074-7)    });
[](#cb1074-8)  });
```

The `.then()` in line A is nested. A flat structure would be better:

```
[](#cb1075-1)asyncFunc1()
[](#cb1075-2)  .then(result1 => {
[](#cb1075-3)    return asyncFunc2();
[](#cb1075-4)  })
[](#cb1075-5)  .then(result2 => {
[](#cb1075-6)    // ···
[](#cb1075-7)  });
```

### 40.6.3 Chaining mistake: more nesting than necessary

This is another example of avoidable nesting:

```
[](#cb1076-1)// Don’t do this
[](#cb1076-2)asyncFunc1()
[](#cb1076-3)  .then(result1 => {
[](#cb1076-4)    if (result1 < 0) {
[](#cb1076-5)      return asyncFuncA()
[](#cb1076-6)      .then(resultA => 'Result: ' + resultA);
[](#cb1076-7)    } else {
[](#cb1076-8)      return asyncFuncB()
[](#cb1076-9)      .then(resultB => 'Result: ' + resultB);
[](#cb1076-10)    }
[](#cb1076-11)  });
```

We can once again get a flat structure:

```
[](#cb1077-1)asyncFunc1()
[](#cb1077-2)  .then(result1 => {
[](#cb1077-3)    return result1 < 0 ? asyncFuncA() : asyncFuncB();
[](#cb1077-4)  })
[](#cb1077-5)  .then(resultAB => {
[](#cb1077-6)    return 'Result: ' + resultAB;
[](#cb1077-7)  });
```

### 40.6.4 Not all nesting is bad

In the following code, we actually benefit from nesting:

```
[](#cb1078-1)db.open()
[](#cb1078-2)  .then(connection => { // (A)
[](#cb1078-3)    return connection.select({ name: 'Jane' })
[](#cb1078-4)      .then(result => { // (B)
[](#cb1078-5)        // Process result
[](#cb1078-6)        // Use `connection` to make more queries
[](#cb1078-7)      })
[](#cb1078-8)      // ···
[](#cb1078-9)      .finally(() => {
[](#cb1078-10)        connection.close(); // (C)
[](#cb1078-11)      });
[](#cb1078-12)  })
```

We are receiving an asynchronous result in line A. In line B, we are nesting so that we have access to variable `connection` inside the callback and in line C.

### 40.6.5 Chaining mistake: creating Promises instead of chaining

Problem:

```
[](#cb1079-1)// Don’t do this
[](#cb1079-2)class Model {
[](#cb1079-3)  insertInto(db) {
[](#cb1079-4)    return new Promise((resolve, reject) => { // (A)
[](#cb1079-5)      db.insert(this.fields)
[](#cb1079-6)        .then(resultCode => {
[](#cb1079-7)          this.notifyObservers({event: 'created', model: this});
[](#cb1079-8)          resolve(resultCode);
[](#cb1079-9)        }).catch(err => {
[](#cb1079-10)          reject(err);
[](#cb1079-11)        })
[](#cb1079-12)    });
[](#cb1079-13)  }
[](#cb1079-14)  // ···
[](#cb1079-15)}
```

In line A, we are creating a Promise to deliver the result of `db.insert()`. That is unnecessarily verbose and can be simplified:

```
[](#cb1080-1)class Model {
[](#cb1080-2)  insertInto(db) {
[](#cb1080-3)    return db.insert(this.fields)
[](#cb1080-4)      .then(resultCode => {
[](#cb1080-5)        this.notifyObservers({event: 'created', model: this});
[](#cb1080-6)        return resultCode;
[](#cb1080-7)      });
[](#cb1080-8)  }
[](#cb1080-9)  // ···
[](#cb1080-10)}
```

The key idea is that we don’t need to create a Promise; we can return the result of the `.then()` call. An additional benefit is that we don’t need to catch and re-reject the failure of `db.insert()`. We simply pass its rejection on to the caller of `.insertInto()`.

## 40.7 Advanced topics

*   In addition to `Promise.all()`, there is also `Promise.race()`, which is not used often and described in [*Exploring ES6*](https://exploringjs.com/es6/ch_promises.html#_timing-out-via-promiserace).
*   *Exploring ES6* has [a section](https://exploringjs.com/es6/ch_promises.html#sec_demo-promise) that shows a very simple implementation of Promises. That may be helpful if you want a deeper understanding of how Promises work.

# 41 Async functions

* * *

*   41.1 [Async functions: the basics](#ch042.xhtml_async-functions-the-basics)
    *   41.1.1 [Async constructs](#ch042.xhtml_async-constructs)
*   41.2 [Returning from async functions](#ch042.xhtml_returning-from-async-functions)
    *   41.2.1 [Async functions always return Promises](#ch042.xhtml_async-functions-always-return-promises)
    *   41.2.2 [Returned Promises are not wrapped](#ch042.xhtml_returned-promises-are-not-wrapped)
    *   41.2.3 [Executing async functions: synchronous start, asynchronous settlement (advanced)](#ch042.xhtml_executing-async-functions-synchronous-start-asynchronous-settlement-advanced)
*   41.3 [`await`: working with Promises](#ch042.xhtml_await-working-with-promises)
    *   41.3.1 [`await` and fulfilled Promises](#ch042.xhtml_await-and-fulfilled-promises)
    *   41.3.2 [`await` and rejected Promises](#ch042.xhtml_await-and-rejected-promises)
    *   41.3.3 [`await` is shallow (we can’t use it in callbacks)](#ch042.xhtml_await-is-shallow-we-cant-use-it-in-callbacks)
*   41.4 [(Advanced)](#ch042.xhtml_advanced-5)
*   41.5 [Immediately invoked async arrow functions](#ch042.xhtml_immediately-invoked-async-arrow-functions)
*   41.6 [Concurrency and `await`](#ch042.xhtml_concurrency-and-await)
    *   41.6.1 [`await`: running asynchronous functions sequentially](#ch042.xhtml_await-sequentially)
    *   41.6.2 [`await`: running asynchronous functions concurrently](#ch042.xhtml_await-concurrently)
*   41.7 [Tips for using async functions](#ch042.xhtml_tips-for-using-async-functions)
    *   41.7.1 [We don’t need `await` if we “fire and forget”](#ch042.xhtml_fire-and-forget-await)
    *   41.7.2 [It can make sense to `await` and ignore the result](#ch042.xhtml_it-can-make-sense-to-await-and-ignore-the-result)

* * *

Roughly, *async functions* provide better syntax for code that uses Promises. In order to use async functions, we should therefore understand Promises. They are explained in [the previous chapter](#ch041.xhtml_ch_promises).

## 41.1 Async functions: the basics

Consider the following async function:

```
[](#cb1081-1)async function fetchJsonAsync(url) {
[](#cb1081-2)  try {
[](#cb1081-3)    const request = await fetch(url); // async
[](#cb1081-4)    const text = await request.text(); // async
[](#cb1081-5)    return JSON.parse(text); // sync
[](#cb1081-6)  }
[](#cb1081-7)  catch (error) {
[](#cb1081-8)    assert.fail(error);
[](#cb1081-9)  }
[](#cb1081-10)}
```

The previous, rather synchronous-looking code is equivalent to the following code that uses Promises directly:

```
[](#cb1082-1)function fetchJsonViaPromises(url) {
[](#cb1082-2)  return fetch(url) // async
[](#cb1082-3)  .then(request => request.text()) // async
[](#cb1082-4)  .then(text => JSON.parse(text)) // sync
[](#cb1082-5)  .catch(error => {
[](#cb1082-6)    assert.fail(error);
[](#cb1082-7)  });
[](#cb1082-8)}
```

A few observations about the async function `fetchJsonAsync()`:

*   Async functions are marked with the keyword `async`.

*   Inside the body of an async function, we write Promise-based code as if it were synchronous. We only need to apply the `await` operator whenever a value is a Promise. That operator pauses the async function and resumes it once the Promise is settled:

    *   If the Promise is fulfilled, `await` returns the fulfillment value.
    *   If the Promise is rejected, `await` throws the rejection value.
*   The result of an async function is always a Promise:

    *   Any value that is returned (explicitly or implicitly) is used to fulfill the Promise.
    *   Any exception that is thrown is used to reject the Promise.

Both `fetchJsonAsync()` and `fetchJsonViaPromises()` are called in exactly the same way, like this:

```
[](#cb1083-1)fetchJsonAsync('http://example.com/person.json')
[](#cb1083-2).then(obj => {
[](#cb1083-3)  assert.deepEqual(obj, {
[](#cb1083-4)    first: 'Jane',
[](#cb1083-5)    last: 'Doe',
[](#cb1083-6)  });
[](#cb1083-7)});
```

![](media/file5.svg)  **Async functions are as Promise-based as functions that use Promises directly**

From the outside, it is virtually impossible to tell the difference between an async function and a function that returns a Promise.

### 41.1.1 Async constructs

JavaScript has the following async versions of synchronous callable entities. Their roles are always either real function or method.

```
[](#cb1084-1)// Async function declaration
[](#cb1084-2)async function func1() {}
[](#cb1084-3)
[](#cb1084-4)// Async function expression
[](#cb1084-5)const func2 = async function () {};
[](#cb1084-6)
[](#cb1084-7)// Async arrow function
[](#cb1084-8)const func3 = async () => {};
[](#cb1084-9)
[](#cb1084-10)// Async method definition in an object literal
[](#cb1084-11)const obj = { async m() {} };
[](#cb1084-12)
[](#cb1084-13)// Async method definition in a class definition
[](#cb1084-14)class MyClass { async m() {} }
```

![](media/file5.svg)  **Asynchronous functions vs. async functions**

The difference between the terms *asynchronous function* and *async function* is subtle, but important:

*   An *asynchronous function* is any function that delivers its result asynchronously – for example, a callback-based function or a Promise-based function.

*   An *async function* is defined via special syntax, involving the keywords `async` and `await`. It is also called async/await due to these two keywords. Async functions are based on Promises and therefore also asynchronous functions (which is somewhat confusing).

## 41.2 Returning from async functions

### 41.2.1 Async functions always return Promises

Each async function always returns a Promise.

Inside the async function, we fulfill the result Promise via `return` (line A):

```
[](#cb1085-1)async function asyncFunc() {
[](#cb1085-2)  return 123; // (A)
[](#cb1085-3)}
[](#cb1085-4)
[](#cb1085-5)asyncFunc()
[](#cb1085-6).then(result => {
[](#cb1085-7)  assert.equal(result, 123);
[](#cb1085-8)});
```

As usual, if we don’t explicitly return anything, `undefined` is returned for us:

```
[](#cb1086-1)async function asyncFunc() {
[](#cb1086-2)}
[](#cb1086-3)
[](#cb1086-4)asyncFunc()
[](#cb1086-5).then(result => {
[](#cb1086-6)  assert.equal(result, undefined);
[](#cb1086-7)});
```

We reject the result Promise via `throw` (line A):

```
[](#cb1087-1)async function asyncFunc() {
[](#cb1087-2)  throw new Error('Problem!'); // (A)
[](#cb1087-3)}
[](#cb1087-4)
[](#cb1087-5)asyncFunc()
[](#cb1087-6).catch(err => {
[](#cb1087-7)  assert.deepEqual(err, new Error('Problem!'));
[](#cb1087-8)});
```

### 41.2.2 Returned Promises are not wrapped

If we return a Promise `p` from an async function, then `p` becomes the result of the function (or rather, the result “locks in” on `p` and behaves exactly like it). That is, the Promise is not wrapped in yet another Promise.

```
[](#cb1088-1)async function asyncFunc() {
[](#cb1088-2)  return Promise.resolve('abc');
[](#cb1088-3)}
[](#cb1088-4)
[](#cb1088-5)asyncFunc()
[](#cb1088-6).then(result => assert.equal(result, 'abc'));
```

Recall that any Promise `q` is treated similarly in the following situations:

*   `resolve(q)` inside `new Promise((resolve, reject) => { ··· })`
*   `return q` inside `.then(result => { ··· })`
*   `return q` inside `.catch(err => { ··· })`

### 41.2.3 Executing async functions: synchronous start, asynchronous settlement (advanced)

Async functions are executed as follows:

*   The Promise `p` for the result is created when the async function is started.
*   Then the body is executed. There are two ways in which execution can leave the body:
    *   Execution can leave **permanently** while settling `p`:
        *   A `return` fulfills `p`.
        *   A `throw` rejects `p`.
    *   Execution can also leave **temporarily** when awaiting the settlement of another Promise `q` via `await`. The async function is paused and execution leaves it. It is resumed once `q` is settled.
*   Promise `p` is returned after execution has left the body for the first time (permanently or temporarily).

Note that the notification of the settlement of the result `p` happens asynchronously, as is always the case with Promises.

The following code demonstrates that an async function is started synchronously (line A), then the current task finishes (line C), then the result Promise is settled – asynchronously (line B).

```
[](#cb1089-1)async function asyncFunc() {
[](#cb1089-2)  console.log('asyncFunc() starts'); // (A)
[](#cb1089-3)  return 'abc';
[](#cb1089-4)}
[](#cb1089-5)asyncFunc().
[](#cb1089-6)then(x => { // (B)
[](#cb1089-7)  console.log(`Resolved: ${x}`);
[](#cb1089-8)});
[](#cb1089-9)console.log('Task ends'); // (C)
[](#cb1089-10)
[](#cb1089-11)// Output:
[](#cb1089-12)// 'asyncFunc() starts'
[](#cb1089-13)// 'Task ends'
[](#cb1089-14)// 'Resolved: abc'
```

## 41.3 `await`: working with Promises

The `await` operator can only be used inside async functions and async generators (which are explained in [§42.2 “Asynchronous generators”](#ch043.xhtml_async-generators)). Its operand is usually a Promise and leads to the following steps being performed:

*   The current async function is paused and returned from. This step is similar to how `yield` works in [sync generators](#ch039.xhtml_ch_sync-generators).
*   Eventually, the current task is finished and processing of the task queue continues.
*   When and if the Promise is settled, the async function is resumed in a new task:
    *   If the Promise is fulfilled, `await` returns the fulfillment value.
    *   If the Promise is rejected, `await` throws the rejection value.

Read on to find out more about how `await` handles Promises in various states.

### 41.3.1 `await` and fulfilled Promises

If its operand ends up being a fulfilled Promise, `await` returns its fulfillment value:

```
[](#cb1090-1)assert.equal(await Promise.resolve('yes!'), 'yes!');
```

Non-Promise values are allowed, too, and simply passed on (synchronously, without pausing the async function):

```
[](#cb1091-1)assert.equal(await 'yes!', 'yes!');
```

### 41.3.2 `await` and rejected Promises

If its operand is a rejected Promise, then `await` throws the rejection value:

```
[](#cb1092-1)try {
[](#cb1092-2)  await Promise.reject(new Error());
[](#cb1092-3)  assert.fail(); // we never get here
[](#cb1092-4)} catch (e) {
[](#cb1092-5)  assert.equal(e instanceof Error, true);
[](#cb1092-6)}
```

Instances of `Error` (including instances of its subclasses) are treated specially and also thrown:

```
[](#cb1093-1)try {
[](#cb1093-2)  await new Error();
[](#cb1093-3)  assert.fail(); // we never get here
[](#cb1093-4)} catch (e) {
[](#cb1093-5)  assert.equal(e instanceof Error, true);
[](#cb1093-6)}
```

![](media/file6.svg)  **Exercise: Fetch API via async functions**

`exercises/async-functions/fetch_json2_test.mjs`

### 41.3.3 `await` is shallow (we can’t use it in callbacks)

If we are inside an async function and want to pause it via `await`, we must do so directly within that function; we can’t use it inside a nested function, such as a callback. That is, pausing is *shallow*.

For example, the following code can’t be executed:

```
[](#cb1094-1)async function downloadContent(urls) {
[](#cb1094-2)  return urls.map((url) => {
[](#cb1094-3)    return await httpGet(url); // SyntaxError!
[](#cb1094-4)  });
[](#cb1094-5)}
```

The reason is that normal arrow functions don’t allow `await` inside their bodies.

OK, let’s try an async arrow function then:

```
[](#cb1095-1)async function downloadContent(urls) {
[](#cb1095-2)  return urls.map(async (url) => {
[](#cb1095-3)    return await httpGet(url);
[](#cb1095-4)  });
[](#cb1095-5)}
```

Alas, this doesn’t work either: Now `.map()` (and therefore `downloadContent()`) returns an Array with Promises, not an Array with (unwrapped) values.

One possible solution is to use `Promise.all()` to unwrap all Promises:

```
[](#cb1096-1)async function downloadContent(urls) {
[](#cb1096-2)  const promiseArray = urls.map(async (url) => {
[](#cb1096-3)    return await httpGet(url); // (A)
[](#cb1096-4)  });
[](#cb1096-5)  return await Promise.all(promiseArray);
[](#cb1096-6)}
```

Can this code be improved? Yes it can: in line A, we are unwrapping a Promise via `await`, only to re-wrap it immediately via `return`. If we omit `await`, we don’t even need an async arrow function:

```
[](#cb1097-1)async function downloadContent(urls) {
[](#cb1097-2)  const promiseArray = urls.map(
[](#cb1097-3)    url => httpGet(url));
[](#cb1097-4)  return await Promise.all(promiseArray); // (B)
[](#cb1097-5)}
```

For the same reason, we can also omit `await` in line B.

![](media/file6.svg)  **Exercise: Mapping and filtering asynchronously**

`exercises/async-functions/map_async_test.mjs`

## 41.4 (Advanced)

All remaining sections are advanced.

## 41.5 Immediately invoked async arrow functions

If we need an `await` outside an async function (e.g., at the top level of a module), then we can immediately invoke an async arrow function:

```
[](#cb1098-1)(async () => { // start
[](#cb1098-2)  const promise = Promise.resolve('abc');
[](#cb1098-3)  const value = await promise;
[](#cb1098-4)  assert.equal(value, 'abc');
[](#cb1098-5)})(); // end
```

The result of an immediately invoked async arrow function is a Promise:

```
[](#cb1099-1)const promise = (async () => 123)();
[](#cb1099-2)promise.then(x => assert.equal(x, 123));
```

## 41.6 Concurrency and `await`

In the next two subsections, we’ll use the helper function `paused()`:

```
[](#cb1100-1)/**
[](#cb1100-2) * Resolves after `ms` milliseconds
[](#cb1100-3) */
[](#cb1100-4)function delay(ms) {
[](#cb1100-5)  return new Promise((resolve, _reject) => {
[](#cb1100-6)    setTimeout(resolve, ms);
[](#cb1100-7)  });
[](#cb1100-8)}
[](#cb1100-9)async function paused(id) {
[](#cb1100-10)  console.log('START ' + id);
[](#cb1100-11)  await delay(10); // pause
[](#cb1100-12)  console.log('END ' + id);
[](#cb1100-13)  return id;
[](#cb1100-14)}
```

### 41.6.1 `await`: running asynchronous functions sequentially

If we prefix the invocations of multiple asynchronous functions with `await`, then those functions are executed sequentially:

```
[](#cb1101-1)async function sequentialAwait() {
[](#cb1101-2)  const result1 = await paused('first');
[](#cb1101-3)  assert.equal(result1, 'first');
[](#cb1101-4) 
[](#cb1101-5)  const result2 = await paused('second');
[](#cb1101-6)  assert.equal(result2, 'second');
[](#cb1101-7)}
[](#cb1101-8)
[](#cb1101-9)// Output:
[](#cb1101-10)// 'START first'
[](#cb1101-11)// 'END first'
[](#cb1101-12)// 'START second'
[](#cb1101-13)// 'END second'
```

That is, `paused('second')` is only started after `paused('first')` is completely finished.

### 41.6.2 `await`: running asynchronous functions concurrently

If we want to run multiple functions concurrently, we can use the tool method `Promise.all()`:

```
[](#cb1102-1)async function concurrentPromiseAll() {
[](#cb1102-2)  const result = await Promise.all([
[](#cb1102-3)    paused('first'), paused('second')
[](#cb1102-4)  ]);
[](#cb1102-5)  assert.deepEqual(result, ['first', 'second']);
[](#cb1102-6)}
[](#cb1102-7)
[](#cb1102-8)// Output:
[](#cb1102-9)// 'START first'
[](#cb1102-10)// 'START second'
[](#cb1102-11)// 'END first'
[](#cb1102-12)// 'END second'
```

Here, both asynchronous functions are started at the same time. Once both are settled, `await` gives us either an Array of fulfillment values or – if at least one Promise is rejected – an exception.

Recall from [§40.5.2 “Concurrency tip: focus on when operations start”](#ch041.xhtml_focus-on-async-start) that what counts is when we start a Promise-based computation; not how we process its result. Therefore, the following code is as “concurrent” as the previous one:

```
[](#cb1103-1)async function concurrentAwait() {
[](#cb1103-2)  const resultPromise1 = paused('first');
[](#cb1103-3)  const resultPromise2 = paused('second');
[](#cb1103-4) 
[](#cb1103-5)  assert.equal(await resultPromise1, 'first');
[](#cb1103-6)  assert.equal(await resultPromise2, 'second');
[](#cb1103-7)}
[](#cb1103-8)// Output:
[](#cb1103-9)// 'START first'
[](#cb1103-10)// 'START second'
[](#cb1103-11)// 'END first'
[](#cb1103-12)// 'END second'
```

## 41.7 Tips for using async functions

### 41.7.1 We don’t need `await` if we “fire and forget”

`await` is not required when working with a Promise-based function; we only need it if we want to pause and wait until the returned Promise is settled. If we only want to start an asynchronous operation, then we don’t need it:

```
[](#cb1104-1)async function asyncFunc() {
[](#cb1104-2)  const writer = openFile('someFile.txt');
[](#cb1104-3)  writer.write('hello'); // don’t wait
[](#cb1104-4)  writer.write('world'); // don’t wait
[](#cb1104-5)  await writer.close(); // wait for file to close
[](#cb1104-6)}
```

In this code, we don’t await `.write()` because we don’t care when it is finished. We do, however, want to wait until `.close()` is done.

Note: Each invocation of `.write()` starts synchronously. That prevents race conditions.

### 41.7.2 It can make sense to `await` and ignore the result

It can occasionally make sense to use `await`, even if we ignore its result – for example:

```
[](#cb1105-1)await longRunningAsyncOperation();
[](#cb1105-2)console.log('Done!');
```

Here, we are using `await` to join a long-running asynchronous operation. That ensures that the logging really happens *after* that operation is done.

# 42 Asynchronous iteration

* * *

*   42.1 [Basic asynchronous iteration](#ch043.xhtml_basic-asynchronous-iteration)
    *   42.1.1 [Protocol: async iteration](#ch043.xhtml_protocol-async-iteration)
    *   42.1.2 [Using async iteration directly](#ch043.xhtml_using-async-iteration-directly)
    *   42.1.3 [Using async iteration via `for-await-of`](#ch043.xhtml_for-await-of)
*   42.2 [Asynchronous generators](#ch043.xhtml_async-generators)
    *   42.2.1 [Example: creating an async iterable via an async generator](#ch043.xhtml_example-creating-an-async-iterable-via-an-async-generator)
    *   42.2.2 [Example: converting a sync iterable to an async iterable](#ch043.xhtml_example-converting-a-sync-iterable-to-an-async-iterable)
    *   42.2.3 [Example: converting an async iterable to an Array](#ch043.xhtml_asyncIterableToArray)
    *   42.2.4 [Example: transforming an async iterable](#ch043.xhtml_example-transforming-an-async-iterable)
    *   42.2.5 [Example: mapping over asynchronous iterables](#ch043.xhtml_example-mapping-over-asynchronous-iterables)
*   42.3 [Async iteration over Node.js streams](#ch043.xhtml_async-iteration-over-node.js-streams)
    *   42.3.1 [Node.js streams: async via callbacks (push)](#ch043.xhtml_node.js-streams-async-via-callbacks-push)
    *   42.3.2 [Node.js streams: async via async iteration (pull)](#ch043.xhtml_node.js-streams-async-via-async-iteration-pull)
    *   42.3.3 [Example: from chunks to lines](#ch043.xhtml_example-from-chunks-to-lines)

* * *

![](media/file0.svg)  **Required knowledge**

For this chapter, you should be familiar with:

*   [Promises](#ch041.xhtml_ch_promises)
*   [Async functions](#ch042.xhtml_ch_async-functions)

## 42.1 Basic asynchronous iteration

### 42.1.1 Protocol: async iteration

To understand how asynchronous iteration works, let’s first revisit [synchronous iteration](#ch031.xhtml_ch_sync-iteration). It comprises the following interfaces:

```
[](#cb1106-1)interface Iterable<T> {
[](#cb1106-2)  [Symbol.iterator]() : Iterator<T>;
[](#cb1106-3)}
[](#cb1106-4)interface Iterator<T> {
[](#cb1106-5)  next() : IteratorResult<T>;
[](#cb1106-6)}
[](#cb1106-7)interface IteratorResult<T> {
[](#cb1106-8)  value: T;
[](#cb1106-9)  done: boolean;
[](#cb1106-10)}
```

*   An `Iterable` is a data structure whose contents can be accessed via iteration. It is a factory for iterators.
*   An `Iterator` is a factory for iteration results that we retrieve by calling the method `.next()`.
*   Each `IterationResult` contains the iterated `.value` and a boolean `.done` that is `true` after the last element and `false` before.

For the protocol for asynchronous iteration, we only want to change one thing: the values produced by `.next()` should be delivered asynchronously. There are two conceivable options:

*   The `.value` could contain a `Promise<T>`.
*   `.next()` could return `Promise<IteratorResult<T>>`.

In other words, the question is whether to wrap just values or whole iterator results in Promises.

It has to be the latter because when `.next()` returns a result, it starts an asynchronous computation. Whether or not that computation produces a value or signals the end of the iteration can only be determined after it is finished. Therefore, both `.done` and `.value` need to be wrapped in a Promise.

The interfaces for async iteration look as follows.

```
[](#cb1107-1)interface AsyncIterable<T> {
[](#cb1107-2)  [Symbol.asyncIterator]() : AsyncIterator<T>;
[](#cb1107-3)}
[](#cb1107-4)interface AsyncIterator<T> {
[](#cb1107-5)  next() : Promise<IteratorResult<T>>; // (A)
[](#cb1107-6)}
[](#cb1107-7)interface IteratorResult<T> {
[](#cb1107-8)  value: T;
[](#cb1107-9)  done: boolean;
[](#cb1107-10)}
```

The only difference to the synchronous interfaces is the return type of `.next()` (line A).

### 42.1.2 Using async iteration directly

The following code uses the asynchronous iteration protocol directly:

```
[](#cb1108-1)const asyncIterable = syncToAsyncIterable(['a', 'b']); // (A)
[](#cb1108-2)const asyncIterator = asyncIterable[Symbol.asyncIterator]();
[](#cb1108-3)
[](#cb1108-4)// Call .next() until .done is true:
[](#cb1108-5)asyncIterator.next() // (B)
[](#cb1108-6).then(iteratorResult => {
[](#cb1108-7)  assert.deepEqual(
[](#cb1108-8)    iteratorResult,
[](#cb1108-9)    { value: 'a', done: false });
[](#cb1108-10)  return asyncIterator.next(); // (C)
[](#cb1108-11)})
[](#cb1108-12).then(iteratorResult => {
[](#cb1108-13)  assert.deepEqual(
[](#cb1108-14)    iteratorResult,
[](#cb1108-15)    { value: 'b', done: false });
[](#cb1108-16)  return asyncIterator.next(); // (D)
[](#cb1108-17)})
[](#cb1108-18).then(iteratorResult => {
[](#cb1108-19)  assert.deepEqual(
[](#cb1108-20)    iteratorResult,
[](#cb1108-21)     { value: undefined, done: true });
[](#cb1108-22)})
[](#cb1108-23);
```

In line A, we create an asynchronous iterable over the value `'a'` and `'b'`. We’ll see an implementation of `syncToAsyncIterable()` later.

We call `.next()` in line B, line C and line D. Each time, we use `.next()` to unwrap the Promise and `assert.deepEqual()` to check the unwrapped value.

We can simplify this code if we use an async function. Now we unwrap Promises via `await` and the code looks almost like we are doing synchronous iteration:

```
[](#cb1109-1)async function f() {
[](#cb1109-2)  const asyncIterable = syncToAsyncIterable(['a', 'b']);
[](#cb1109-3)  const asyncIterator = asyncIterable[Symbol.asyncIterator]();
[](#cb1109-4) 
[](#cb1109-5)  // Call .next() until .done is true:
[](#cb1109-6)  assert.deepEqual(
[](#cb1109-7)    await asyncIterator.next(),
[](#cb1109-8)    { value: 'a', done: false });
[](#cb1109-9)  assert.deepEqual(
[](#cb1109-10)    await asyncIterator.next(),
[](#cb1109-11)    { value: 'b', done: false });
[](#cb1109-12)  assert.deepEqual(
[](#cb1109-13)    await asyncIterator.next(),
[](#cb1109-14)    { value: undefined, done: true });
[](#cb1109-15)}
```

### 42.1.3 Using async iteration via `for-await-of`

The asynchronous iteration protocol is not meant to be used directly. One of the language constructs that supports it is the `for-await-of` loop, which is an asynchronous version of the `for-of` loop. It can be used in async functions and *async generators* (which are introduced later in this chapter). This is an example of `for-await-of` in use:

```
[](#cb1110-1)for await (const x of syncToAsyncIterable(['a', 'b'])) {
[](#cb1110-2)  console.log(x);
[](#cb1110-3)}
[](#cb1110-4)// Output:
[](#cb1110-5)// 'a'
[](#cb1110-6)// 'b'
```

`for-await-of` is relatively flexible. In addition to asynchronous iterables, it also supports synchronous iterables:

```
[](#cb1111-1)for await (const x of ['a', 'b']) {
[](#cb1111-2)  console.log(x);
[](#cb1111-3)}
[](#cb1111-4)// Output:
[](#cb1111-5)// 'a'
[](#cb1111-6)// 'b'
```

And it supports synchronous iterables over values that are wrapped in Promises:

```
[](#cb1112-1)const arr = [Promise.resolve('a'), Promise.resolve('b')];
[](#cb1112-2)for await (const x of arr) {
[](#cb1112-3)  console.log(x);
[](#cb1112-4)}
[](#cb1112-5)// Output:
[](#cb1112-6)// 'a'
[](#cb1112-7)// 'b'
```

![](media/file6.svg)  **Exercise: Convert an async iterable to an Array**

Warning: We’ll soon see the solution for this exercise in this chapter.

*   `exercises/async-iteration/async_iterable_to_array_test.mjs`

## 42.2 Asynchronous generators

An asynchronous generator is two things at the same time:

*   An async function (input): We can use `await` and `for-await-of` to retrieve data.
*   A generator that returns an asynchronous iterable (output): We can use `yield` and `yield*` to produce data.

![](media/file0.svg)  **Asynchronous generators are very similar to synchronous generators**

Due to async generators and sync generators being so similar, I don’t explain how exactly `yield` and `yield*` work. Please consult [§38 “Synchronous generators”](#ch039.xhtml_ch_sync-generators) if you have doubts.

Therefore, an asynchronous generator has:

*   Input that can be:
    *   synchronous (single values, sync iterables) or
    *   asynchronous (Promises, async iterables).
*   Output that is an asynchronous iterable.

This looks as follows:

```
[](#cb1113-1)async function* asyncGen() {
[](#cb1113-2)  // Input: Promises, async iterables
[](#cb1113-3)  const x = await somePromise;
[](#cb1113-4)  for await (const y of someAsyncIterable) {
[](#cb1113-5)    // ···
[](#cb1113-6)  }
[](#cb1113-7)
[](#cb1113-8)  // Output
[](#cb1113-9)  yield someValue;
[](#cb1113-10)  yield* otherAsyncGen();
[](#cb1113-11)}
```

### 42.2.1 Example: creating an async iterable via an async generator

Let’s look at an example. The following code creates an async iterable with three numbers:

```
[](#cb1114-1)async function* yield123() {
[](#cb1114-2)  for (let i=1; i<=3; i++) {
[](#cb1114-3)    yield i;
[](#cb1114-4)  }
[](#cb1114-5)}
```

Does the result of `yield123()` conform to the async iteration protocol?

```
[](#cb1115-1)(async () => {
[](#cb1115-2)  const asyncIterable = yield123();
[](#cb1115-3)  const asyncIterator = asyncIterable[Symbol.asyncIterator]();
[](#cb1115-4)  assert.deepEqual(
[](#cb1115-5)    await asyncIterator.next(),
[](#cb1115-6)    { value: 1, done: false });
[](#cb1115-7)  assert.deepEqual(
[](#cb1115-8)    await asyncIterator.next(),
[](#cb1115-9)    { value: 2, done: false });
[](#cb1115-10)  assert.deepEqual(
[](#cb1115-11)    await asyncIterator.next(),
[](#cb1115-12)    { value: 3, done: false });
[](#cb1115-13)  assert.deepEqual(
[](#cb1115-14)    await asyncIterator.next(),
[](#cb1115-15)    { value: undefined, done: true });
[](#cb1115-16)})();
```

We wrapped the code in an [immediately invoked async arrow function](#ch042.xhtml_immediately-invoked-async-arrow-functions).

### 42.2.2 Example: converting a sync iterable to an async iterable

The following asynchronous generator converts a synchronous iterable to an asynchronous iterable. It implements the function `syncToAsyncIterable()` that we have used previously.

```
[](#cb1116-1)async function* syncToAsyncIterable(syncIterable) {
[](#cb1116-2)  for (const elem of syncIterable) {
[](#cb1116-3)    yield elem;
[](#cb1116-4)  }
[](#cb1116-5)}
```

Note: The input is synchronous in this case (no `await` is needed).

### 42.2.3 Example: converting an async iterable to an Array

The following function is a solution to a previous exercise. It converts an async iterable to an Array (think spreading, but for async iterables instead of sync iterables).

```
[](#cb1117-1)async function asyncIterableToArray(asyncIterable) {
[](#cb1117-2)  const result = [];
[](#cb1117-3)  for await (const value of asyncIterable) {
[](#cb1117-4)    result.push(value);
[](#cb1117-5)  }
[](#cb1117-6)  return result;
[](#cb1117-7)}
```

Note that we can’t use an async generator in this case: We get our input via `for-await-of` and return an Array wrapped in a Promise. The latter requirement rules out async generators.

This is a test for `asyncIterableToArray()`:

```
[](#cb1118-1)async function* createAsyncIterable() {
[](#cb1118-2)  yield 'a';
[](#cb1118-3)  yield 'b';
[](#cb1118-4)}
[](#cb1118-5)const asyncIterable = createAsyncIterable();
[](#cb1118-6)assert.deepEqual(
[](#cb1118-7)  await asyncIterableToArray(asyncIterable), // (A)
[](#cb1118-8)  ['a', 'b']
[](#cb1118-9));
```

Note the `await` in line A, which is needed to unwrap the Promise returned by `asyncIterableToArray()`. In order for `await` to work, this code fragment must be run inside an async function.

### 42.2.4 Example: transforming an async iterable

Let’s implement an async generator that produces a new async iterable by transforming an existing async iterable.

```
[](#cb1119-1)async function* timesTwo(asyncNumbers) {
[](#cb1119-2)  for await (const x of asyncNumbers) {
[](#cb1119-3)    yield x * 2;
[](#cb1119-4)  }
[](#cb1119-5)}
```

To test this function, we use `asyncIterableToArray()` from the previous section.

```
[](#cb1120-1)async function* createAsyncIterable() {
[](#cb1120-2)  for (let i=1; i<=3; i++) {
[](#cb1120-3)    yield i;
[](#cb1120-4)  }
[](#cb1120-5)}
[](#cb1120-6)assert.deepEqual(
[](#cb1120-7)  await asyncIterableToArray(timesTwo(createAsyncIterable())),
[](#cb1120-8)  [2, 4, 6]
[](#cb1120-9));
```

![](media/file6.svg)  **Exercise: Async generators**

Warning: We’ll soon see the solution for this exercise in this chapter.

*   `exercises/async-iteration/number_lines_test.mjs`

### 42.2.5 Example: mapping over asynchronous iterables

As a reminder, this is how to map over synchronous iterables:

```
[](#cb1121-1)function* mapSync(iterable, func) {
[](#cb1121-2)  let index = 0;
[](#cb1121-3)  for (const x of iterable) {
[](#cb1121-4)    yield func(x, index);
[](#cb1121-5)    index++;
[](#cb1121-6)  }
[](#cb1121-7)}
[](#cb1121-8)const syncIterable = mapSync(['a', 'b', 'c'], s => s.repeat(3));
[](#cb1121-9)assert.deepEqual(
[](#cb1121-10)  [...syncIterable],
[](#cb1121-11)  ['aaa', 'bbb', 'ccc']);
```

The asynchronous version looks as follows:

```
[](#cb1122-1)async function* mapAsync(asyncIterable, func) { // (A)
[](#cb1122-2)  let index = 0;
[](#cb1122-3)  for await (const x of asyncIterable) { // (B)
[](#cb1122-4)    yield func(x, index);
[](#cb1122-5)    index++;
[](#cb1122-6)  }
[](#cb1122-7)}
```

Note how similar the sync implementation and the async implementation are. The only two differences are the `async` in line A and the `await` in line B. That is comparable to going from a synchronous function to an asynchronous function – we only need to add the keyword `async` and the occasional `await`.

To test `mapAsync()`, we use the helper function `asyncIterableToArray()` [(shown earlier in this chapter)](#ch043.xhtml_asyncIterableToArray):

```
[](#cb1123-1)async function* createAsyncIterable() {
[](#cb1123-2)  yield 'a';
[](#cb1123-3)  yield 'b';
[](#cb1123-4)}
[](#cb1123-5)const mapped = mapAsync(
[](#cb1123-6)  createAsyncIterable(), s => s.repeat(3));
[](#cb1123-7)assert.deepEqual(
[](#cb1123-8)  await asyncIterableToArray(mapped), // (A)
[](#cb1123-9)  ['aaa', 'bbb']);
```

Once again, we `await` to unwrap a Promise (line A) and this code fragment must run inside an async function.

![](media/file6.svg)  **Exercise: `filterAsyncIter()`**

`exercises/async-iteration/filter_async_iter_test.mjs`

## 42.3 Async iteration over Node.js streams

### 42.3.1 Node.js streams: async via callbacks (push)

Traditionally, reading asynchronously from Node.js streams is done via callbacks:

```
[](#cb1124-1)function main(inputFilePath) {
[](#cb1124-2)  const readStream = fs.createReadStream(inputFilePath,
[](#cb1124-3)    { encoding: 'utf8', highWaterMark: 1024 });
[](#cb1124-4)  readStream.on('data', (chunk) => {
[](#cb1124-5)    console.log('>>> '+chunk);
[](#cb1124-6)  });
[](#cb1124-7)  readStream.on('end', () => {
[](#cb1124-8)    console.log('### DONE ###');
[](#cb1124-9)  });
[](#cb1124-10)}
```

That is, the stream is in control and pushes data to the reader.

### 42.3.2 Node.js streams: async via async iteration (pull)

Starting with Node.js 10, we can also use asynchronous iteration to read from streams:

```
[](#cb1125-1)async function main(inputFilePath) {
[](#cb1125-2)  const readStream = fs.createReadStream(inputFilePath,
[](#cb1125-3)    { encoding: 'utf8', highWaterMark: 1024 });
[](#cb1125-4)
[](#cb1125-5)  for await (const chunk of readStream) {
[](#cb1125-6)    console.log('>>> '+chunk);
[](#cb1125-7)  }
[](#cb1125-8)  console.log('### DONE ###');
[](#cb1125-9)}
```

This time, the reader is in control and pulls data from the stream.

### 42.3.3 Example: from chunks to lines

Node.js streams iterate over *chunks* (arbitrarily long pieces) of data. The following asynchronous generator converts an async iterable over chunks to an async iterable over lines:

```
[](#cb1126-1)/**
[](#cb1126-2) * Parameter: async iterable of chunks (strings)
[](#cb1126-3) * Result: async iterable of lines (incl. newlines)
[](#cb1126-4) */
[](#cb1126-5)async function* chunksToLines(chunksAsync) {
[](#cb1126-6)  let previous = '';
[](#cb1126-7)  for await (const chunk of chunksAsync) { // input
[](#cb1126-8)    previous += chunk;
[](#cb1126-9)    let eolIndex;
[](#cb1126-10)    while ((eolIndex = previous.indexOf('\n')) >= 0) {
[](#cb1126-11)      // line includes the EOL (Windows '\r\n' or Unix '\n')
[](#cb1126-12)      const line = previous.slice(0, eolIndex+1);
[](#cb1126-13)      yield line; // output
[](#cb1126-14)      previous = previous.slice(eolIndex+1);
[](#cb1126-15)    }
[](#cb1126-16)  }
[](#cb1126-17)  if (previous.length > 0) {
[](#cb1126-18)    yield previous;
[](#cb1126-19)  }
[](#cb1126-20)}
```

Let’s apply `chunksToLines()` to an async iterable over chunks (as produced by `chunkIterable()`):

```
[](#cb1127-1)async function* chunkIterable() {
[](#cb1127-2)  yield 'First\nSec';
[](#cb1127-3)  yield 'ond\nThird\nF';
[](#cb1127-4)  yield 'ourth';
[](#cb1127-5)}
[](#cb1127-6)const linesIterable = chunksToLines(chunkIterable());
[](#cb1127-7)assert.deepEqual(
[](#cb1127-8)  await asyncIterableToArray(linesIterable),
[](#cb1127-9)  [
[](#cb1127-10)    'First\n',
[](#cb1127-11)    'Second\n',
[](#cb1127-12)    'Third\n',
[](#cb1127-13)    'Fourth',
[](#cb1127-14)  ]);
```

Now that we have an asynchronous iterable over lines, we can use the solution of a previous exercise, `numberLines()`, to number those lines:

```
[](#cb1128-1)async function* numberLines(linesAsync) {
[](#cb1128-2)  let lineNumber = 1;
[](#cb1128-3)  for await (const line of linesAsync) {
[](#cb1128-4)    yield lineNumber + ': ' + line;
[](#cb1128-5)    lineNumber++;
[](#cb1128-6)  }
[](#cb1128-7)}
[](#cb1128-8)const numberedLines = numberLines(chunksToLines(chunkIterable()));
[](#cb1128-9)assert.deepEqual(
[](#cb1128-10)  await asyncIterableToArray(numberedLines),
[](#cb1128-11)  [
[](#cb1128-12)    '1: First\n',
[](#cb1128-13)    '2: Second\n',
[](#cb1128-14)    '3: Third\n',
[](#cb1128-15)    '4: Fourth',
[](#cb1128-16)  ]);
```

# 43 Regular expressions (`RegExp`)

* * *

*   43.1 [Creating regular expressions](#ch044.xhtml_creating-regular-expressions)
    *   43.1.1 [Literal vs. constructor](#ch044.xhtml_literal-vs.-constructor)
    *   43.1.2 [Cloning and non-destructively modifying regular expressions](#ch044.xhtml_cloning-regexps)
*   43.2 [Syntax](#ch044.xhtml_syntax)
    *   43.2.1 [Syntax characters](#ch044.xhtml_syntax-characters)
    *   43.2.2 [Basic atoms](#ch044.xhtml_basic-atoms)
    *   43.2.3 [Unicode property escapes ^([ES2018])](#ch044.xhtml_unicode-property-escapes)
    *   43.2.4 [Character classes](#ch044.xhtml_character-classes)
    *   43.2.5 [Groups](#ch044.xhtml_groups)
    *   43.2.6 [Quantifiers](#ch044.xhtml_quantifiers)
    *   43.2.7 [Assertions](#ch044.xhtml_assertions)
    *   43.2.8 [Disjunction (`|`)](#ch044.xhtml_disjunction)
*   43.3 [Flags](#ch044.xhtml_reg-exp-flags)
    *   43.3.1 [Flag: Unicode mode via `/u`](#ch044.xhtml_regexp-unicode-mode)
*   43.4 [Properties of regular expression objects](#ch044.xhtml_properties-of-regular-expression-objects)
    *   43.4.1 [Flags as properties](#ch044.xhtml_flags-as-properties)
    *   43.4.2 [Other properties](#ch044.xhtml_other-properties)
*   43.5 [Methods for working with regular expressions](#ch044.xhtml_methods-for-working-with-regular-expressions)
    *   43.5.1 [In general, regular expressions match anywhere in a string](#ch044.xhtml_in-general-regular-expressions-match-anywhere-in-a-string)
    *   43.5.2 [`regExp.test(str)`: is there a match? ^([ES3])](#ch044.xhtml_RegExp.prototype.test)
    *   43.5.3 [`str.search(regExp)`: at what index is the match? ^([ES3])](#ch044.xhtml_String.prototype.search)
    *   43.5.4 [`regExp.exec(str)`: capturing groups ^([ES3])](#ch044.xhtml_RegExp.prototype.exec)
    *   43.5.5 [`str.match(regExp)`: return all matching substrings ^([ES3])](#ch044.xhtml_String.prototype.match)
    *   43.5.6 [`str.replace(searchValue, replacementValue)` ^([ES3])](#ch044.xhtml_String.prototype.replace)
    *   43.5.7 [Other methods for working with regular expressions](#ch044.xhtml_other-methods-for-working-with-regular-expressions)
*   43.6 [Flag `/g` and its pitfalls](#ch044.xhtml_regexp-flag-g)
    *   43.6.1 [Pitfall: You can’t inline a regular expression with flag `/g`](#ch044.xhtml_pitfall-you-cant-inline-a-regular-expression-with-flag-g)
    *   43.6.2 [Pitfall: Removing `/g` can break code](#ch044.xhtml_pitfall-removing-g-can-break-code)
    *   43.6.3 [Pitfall: Adding `/g` can break code](#ch044.xhtml_pitfall-adding-g-can-break-code)
    *   43.6.4 [Pitfall: Code can break if `.lastIndex` isn’t zero](#ch044.xhtml_pitfall-code-can-break-if-.lastindex-isnt-zero)
    *   43.6.5 [Dealing with `/g` and `.lastIndex`](#ch044.xhtml_dealing-with-g-and-.lastindex)
*   43.7 [Techniques for working with regular expressions](#ch044.xhtml_techniques-for-working-with-regular-expressions)
    *   43.7.1 [Escaping arbitrary text for regular expressions](#ch044.xhtml_escapeForRegExp)
    *   43.7.2 [Matching everything or nothing](#ch044.xhtml_matching-everything-or-nothing)

* * *

![](media/file0.svg)  **Availability of features**

Unless stated otherwise, each regular expression feature has been available since ES3.

## 43.1 Creating regular expressions

### 43.1.1 Literal vs. constructor

The two main ways of creating regular expressions are:

*   Literal: compiled statically (at load time).

    ```
    [](#cb1129-1)/abc/ui
    ```

*   Constructor: compiled dynamically (at runtime).

    ```
    [](#cb1130-1)new RegExp('abc', 'ui')
    ```

Both regular expressions have the same two parts:

*   The *body* `abc` – the actual regular expression.
*   The *flags* `u` and `i`. Flags configure how the pattern is interpreted. For example, `i` enables case-insensitive matching. A list of available flags is given [later in this chapter](#ch044.xhtml_reg-exp-flags).

### 43.1.2 Cloning and non-destructively modifying regular expressions

There are two variants of the constructor `RegExp()`:

*   `new RegExp(pattern : string, flags = '')` ^([ES3])

    A new regular expression is created as specified via `pattern`. If `flags` is missing, the empty string `''` is used.

*   `new RegExp(regExp : RegExp, flags = regExp.flags)` ^([ES6])

    `regExp` is cloned. If `flags` is provided, then it determines the flags of the clone.

The second variant is useful for cloning regular expressions, optionally while modifying them. Flags are immutable and this is the only way of changing them – for example:

```
[](#cb1131-1)function copyAndAddFlags(regExp, flagsToAdd='') {
[](#cb1131-2)  // The constructor doesn’t allow duplicate flags;
[](#cb1131-3)  // make sure there aren’t any:
[](#cb1131-4)  const newFlags = [...new Set(regExp.flags + flagsToAdd)].join('');
[](#cb1131-5)  return new RegExp(regExp, newFlags);
[](#cb1131-6)}
[](#cb1131-7)assert.equal(/abc/i.flags, 'i');
[](#cb1131-8)assert.equal(copyAndAddFlags(/abc/i, 'g').flags, 'gi');
```

## 43.2 Syntax

### 43.2.1 Syntax characters

At the top level of a regular expression, the following *syntax characters* are special. They are escaped by prefixing a backslash (`\`).

```
\ ^ $ . * + ? ( ) [ ] { } |
```

In regular expression literals, you must escape slashs:

```
> /\//.test('/')
true
```

In the argument of `new RegExp()`, you don’t have to escape slashes:

```
> new RegExp('/').test('/')
true
```

### 43.2.2 Basic atoms

*Atoms* are the basic building blocks of regular expressions.

*   *Pattern characters* are all characters *except* syntax characters (`^`, `$`, etc.). Pattern characters match themselves. Examples: `A b %`
*   `.` matches any character. You can use the flag `/s` (`dotall`) to control if the dot matches line terminators or not ([more below](#ch044.xhtml_reg-exp-flags)).
*   *Character escapes* (each escape matches a single fixed character):
    *   Control escapes (for a few control characters):
        *   `\f`: form feed (FF)
        *   `\n`: line feed (LF)
        *   `\r`: carriage return (CR)
        *   `\t`: character tabulation
        *   `\v`: line tabulation
    *   Arbitrary control characters: `\cA` (Ctrl-A), …, `\cZ` (Ctrl-Z)
    *   Unicode code units: `\u00E4`
    *   Unicode code points (require flag `/u`): `\u{1F44D}`
*   *Character class escapes* (each escape matches one out of a set of characters):
    *   `\d`: digits (same as `[0-9]`)
        *   `\D`: non-digits
    *   `\w`: “word” characters (same as `[A-Za-z0-9_]`, related to identifiers in programming languages)
        *   `\W`: non-word characters
    *   `\s`: whitespace (space, tab, line terminators, etc.)
        *   `\S`: non-whitespace
    *   *Unicode property escapes* ^([ES2018]): `\p{White_Space}`, `\P{White_Space}`, etc.
        *   Require flag `/u`.
        *   Described in the next subsection.

### 43.2.3 Unicode property escapes ^([ES2018])

#### 43.2.3.1 Unicode character properties

In the Unicode standard, each character has *properties* – metadata describing it. Properties play an important role in defining the nature of a character. Quoting [the Unicode Standard, Sect. 3.3, D3](http://www.unicode.org/versions/Unicode9.0.0/ch03.pdf):

> The semantics of a character are determined by its identity, normative properties, and behavior.

These are a few examples of properties:

*   `Name`: a unique name, composed of uppercase letters, digits, hyphens, and spaces – for example:
    *   A: `Name = LATIN CAPITAL LETTER A`
    *   `🙂`: `Name = SLIGHTLY SMILING FACE`
*   `General_Category`: categorizes characters – for example:
    *   x: `General_Category = Lowercase_Letter`
    *   $: `General_Category = Currency_Symbol`
*   `White_Space`: used for marking invisible spacing characters, such as spaces, tabs and newlines – for example:
    *   \t: `White_Space = True`
    *   π: `White_Space = False`
*   `Age`: version of the Unicode Standard in which a character was introduced – for example: The Euro sign € was added in version 2.1 of the Unicode standard.
    *   €: `Age = 2.1`
*   `Block`: a contiguous range of code points. Blocks don’t overlap and their names are unique. For example:
    *   S: `Block = Basic_Latin` (range U+0000..U+007F)
    *   `🙂`: `Block = Emoticons` (range U+1F600..U+1F64F)
*   `Script`: is a collection of characters used by one or more writing systems.
    *   Some scripts support several writing systems. For example, the Latin script supports the writing systems English, French, German, Latin, etc.
    *   Some languages can be written in multiple alternate writing systems that are supported by multiple scripts. For example, Turkish used the Arabic script before it transitioned to the Latin script in the early 20th century.
    *   Examples:
        *   α: `Script = Greek`
        *   Д: `Script = Cyrillic`

#### 43.2.3.2 Unicode property escapes

Unicode property escapes look like this:

1.  `\p{prop=value}`: matches all characters whose property `prop` has the value `value`.
2.  `\P{prop=value}`: matches all characters that do not have a property `prop` whose value is `value`.
3.  `\p{bin_prop}`: matches all characters whose binary property `bin_prop` is True.
4.  `\P{bin_prop}`: matches all characters whose binary property `bin_prop` is False.

Comments:

*   You can only use Unicode property escapes if the flag `/u` is set. Without `/u`, `\p` is the same as `p`.

*   Forms (3) and (4) can be used as abbreviations if the property is `General_Category`. For example, the following two escapes are equivalent:

    ```
    \p{Lowercase_Letter}
    \p{General_Category=Lowercase_Letter}
    ```

Examples:

*   Checking for whitespace:

    ```
    > /^\p{White_Space}+$/u.test('\t \n\r')
    true
    ```

*   Checking for Greek letters:

    ```
    > /^\p{Script=Greek}+$/u.test('μετά')
    true
    ```

*   Deleting any letters:

    ```
    > '1π2ü3é4'.replace(/\p{Letter}/ug, '')
    '1234'
    ```

*   Deleting lowercase letters:

    ```
    > 'AbCdEf'.replace(/\p{Lowercase_Letter}/ug, '')
    'ACE'
    ```

Further reading:

*   Lists of Unicode properties and their values: [“Unicode Standard Annex #44: Unicode Character Database”](https://unicode.org/reports/tr44/#Properties) (Editors: Mark Davis, Laurențiu Iancu, Ken Whistler)

### 43.2.4 Character classes

A *character class* wraps *class ranges* in square brackets. The class ranges specify a set of characters:

*   `[«class ranges»]` matches any character in the set.
*   `[^«class ranges»]` matches any character not in the set.

Rules for class ranges:

*   Non-syntax characters stand for themselves: `[abc]`

*   Only the following four characters are special and must be escaped via slashes:
    `^ \ - ]`

    *   `^` only has to be escaped if it comes first.
    *   `-` need not be escaped if it comes first or last.
*   Character escapes (`\n`, `\u{1F44D}`, etc.) have the usual meaning.

    *   Watch out: `\b` stands for backspace. Elsewhere in a regular expression, it matches word boundaries.
*   Character class escapes (`\d`, `\p{White_Space}`, etc.) have the usual meaning.

*   Ranges of characters are specified via dashes: `[a-z]`

### 43.2.5 Groups

*   Positional capture group: `(#+)`
    *   Backreference: `\1`, `\2`, etc.
*   Named capture group ^([ES2018]): `(?<hashes>#+)`
    *   Backreference: `\k<hashes>`
*   Noncapturing group: `(?:#+)`

### 43.2.6 Quantifiers

By default, all of the following quantifiers are *greedy* (they match as many characters as possible):

*   `?`: match never or once
*   `*`: match zero or more times
*   `+`: match one or more times
*   `{n}`: match `n` times
*   `{n,}`: match `n` or more times
*   `{n,m}`: match at least `n` times, at most `m` times.

To make them *reluctant* (so that they match as few characters as possible), put question marks (`?`) after them:

```
> /".*"/.exec('"abc"def"')[0]  // greedy
'"abc"def"'
> /".*?"/.exec('"abc"def"')[0] // reluctant
'"abc"'
```

### 43.2.7 Assertions

*   `^` matches only at the beginning of the input
*   `$` matches only at the end of the input
*   `\b` matches only at a word boundary
    *   `\B` matches only when not at a word boundary

#### 43.2.7.1 Lookahead

**Positive lookahead:** `(?=«pattern»)` matches if `pattern` matches what comes next.

Example: sequences of lowercase letters that are followed by an `X`.

```
> 'abcX def'.match(/[a-z]+(?=X)/g)
[ 'abc' ]
```

Note that the `X` itself is not part of the matched substring.

**Negative lookahead:** `(?!«pattern»)` matches if `pattern` does not match what comes next.

Example: sequences of lowercase letters that are not followed by an `X`.

```
> 'abcX def'.match(/[a-z]+(?!X)/g)
[ 'ab', 'def' ]
```

#### 43.2.7.2 Lookbehind ^([ES2018])

**Positive lookbehind:** `(?<=«pattern»)` matches if `pattern` matches what came before.

Example: sequences of lowercase letters that are preceded by an `X`.

```
> 'Xabc def'.match(/(?<=X)[a-z]+/g)
[ 'abc' ]
```

**Negative lookbehind:** `(?<!«pattern»)` matches if `pattern` does not match what came before.

Example: sequences of lowercase letters that are not preceded by an `X`.

```
> 'Xabc def'.match(/(?<!X)[a-z]+/g)
[ 'bc', 'def' ]
```

Example: replace “.js” with “.html”, but not in “Node.js”.

```
> 'Node.js: index.js and main.js'.replace(/(?<!Node)\.js/g, '.html')
'Node.js: index.html and main.html'
```

### 43.2.8 Disjunction (`|`)

Caveat: this operator has low precedence. Use groups if necessary:

*   `^aa|zz$` matches all strings that start with `aa` and/or end with `zz`. Note that `|` has a lower precedence than `^` and `$`.
*   `^(aa|zz)$` matches the two strings `'aa'` and `'zz'`.
*   `^a(a|z)z$` matches the two strings `'aaz'` and `'azz'`.

## 43.3 Flags

Table 20: These are the regular expression flags supported by JavaScript.

| Literal flag | Property name | ES | Description |
| --- | --- | --- | --- |
| `g` | `global` | ES3 | Match multiple times |
| `i` | `ignoreCase` | ES3 | Match case-insensitively |
| `m` | `multiline` | ES3 | `^` and `$` match per line |
| `s` | `dotall` | ES2018 | Dot matches line terminators |
| `u` | `unicode` | ES6 | Unicode mode (recommended) |
| `y` | `sticky` | ES6 | No characters between matches |

The following regular expression flags are available in JavaScript (tbl. [20](#ch044.xhtml_tbl:reg-exp-flags-table) provides a compact overview):

*   `/g` (`.global`): fundamentally changes how the following methods work.

    *   `RegExp.prototype.test()`
    *   `RegExp.prototype.exec()`
    *   `String.prototype.match()`

    How, is explained in [§43.6 “Flag `/g` and its pitfalls”](#ch044.xhtml_regexp-flag-g). In a nutshell, without `/g`, the methods only consider the first match for a regular expression in an input string. With `/g`, they consider all matches.

*   `/i` (`.ignoreCase`): switches on case-insensitive matching:

    ```
    > /a/.test('A')
    false
    > /a/i.test('A')
    true
    ```

*   `/m` (`.multiline`): If this flag is on, `^` matches the beginning of each line and `$` matches the end of each line. If it is off, `^` matches the beginning of the whole input string and `$` matches the end of the whole input string.

    ```
    > 'a1\na2\na3'.match(/^a./gm)
    [ 'a1', 'a2', 'a3' ]
    > 'a1\na2\na3'.match(/^a./g)
    [ 'a1' ]
    ```

*   `/u` (`.unicode`): This flag switches on the Unicode mode for a regular expression. That mode is explained in the next subsection.

*   `/y` (`.sticky`): This flag mainly makes sense in conjunction with `/g`. When both are switched on, any match must directly follow the previous one (that is, it must start at index `.lastIndex` of the regular expression object). Therefore, the first match must be at index 0.

    ```
    > 'a1a2 a3'.match(/a./gy)
    [ 'a1', 'a2' ]
    > '_a1a2 a3'.match(/a./gy) // first match must be at index 0
    null

    > 'a1a2 a3'.match(/a./g)
    [ 'a1', 'a2', 'a3' ]
    > '_a1a2 a3'.match(/a./g)
    [ 'a1', 'a2', 'a3' ]
    ```

    The main use case for `/y` is tokenization (during parsing).

*   `/s` (`.dotall`): By default, the dot does not match line terminators. With this flag, it does:

    ```
    > /./.test('\n')
    false
    > /./s.test('\n')
    true
    ```

    Workaround if `/s` isn’t supported: Use `[^]` instead of a dot.

    ```
    > /[^]/.test('\n')
    true
    ```

### 43.3.1 Flag: Unicode mode via `/u`

The flag `/u` switches on a special Unicode mode for regular expressions. That mode enables several features:

*   In patterns, you can use Unicode code point escapes such as `\u{1F42A}` to specify characters. Code unit escapes such as `\u03B1` only have a range of four hexadecimal digits (which corresponds to the basic multilingual plane).

*   In patterns, you can use Unicode property escapes such as `\p{White_Space}`.

*   Many escapes are now forbidden. For example: `\a \- \:`

    Pattern characters always match themselves:

    ```
    > /pa-:/.test('pa-:')
    true
    ```

    Without `/u`, there are some pattern characters that still match themselves if you escape them with backslashes:

    ```
    > /\p\a\-\:/.test('pa-:')
    true
    ```

    With `/u`:

    *   `\p` starts a Unicode property escape.
    *   The remaining “self-matching” escapes are forbidden. As a consequence, they can now be used for new features in the future.
*   The atomic units for matching are Unicode characters (code points), not JavaScript characters (code units).

The following subsections explain the last item in more detail. They use the following Unicode character to explain when the atomic units are Unicode characters and when they are JavaScript characters:

```
[](#cb1153-1)const codePoint = '🙂';
[](#cb1153-2)const codeUnits = '\uD83D\uDE42'; // UTF-16
[](#cb1153-3)
[](#cb1153-4)assert.equal(codePoint, codeUnits); // same string!
```

I’m only switching between `🙂` and `\uD83D\uDE42`, to illustrate how JavaScript sees things. Both are equivalent and can be used interchangeably in strings and regular expressions.

#### 43.3.1.1 Consequence: you can put Unicode characters in character classes

With `/u`, the two code units of `🙂` are treated as a single character:

```
> /^[🙂]$/u.test('🙂')
true
```

Without `/u`, `🙂` is treated as two characters:

```
> /^[\uD83D\uDE42]$/.test('\uD83D\uDE42')
false
> /^[\uD83D\uDE42]$/.test('\uDE42')
true
```

Note that `^` and `$` demand that the input string have a single character. That’s why the first result is `false`.

#### 43.3.1.2 Consequence: the dot operator (`.`) matches Unicode characters, not JavaScript characters

With `/u`, the dot operator matches Unicode characters:

```
> '🙂'.match(/./gu).length
1
```

`.match()` plus `/g` returns an Array with all the matches of a regular expression.

Without `/u`, the dot operator matches JavaScript characters:

```
> '\uD83D\uDE80'.match(/./g).length
2
```

#### 43.3.1.3 Consequence: quantifiers apply to Unicode characters, not JavaScript characters

With `/u`, a quantifier applies to the whole preceding Unicode character:

```
> /^🙂{3}$/u.test('🙂🙂🙂')
true
```

Without `/u`, a quantifier only applies to the preceding JavaScript character:

```
> /^\uD83D\uDE80{3}$/.test('\uD83D\uDE80\uDE80\uDE80')
true
```

## 43.4 Properties of regular expression objects

Noteworthy:

*   Strictly speaking, only `.lastIndex` is a real instance property. All other properties are implemented via getters.
*   Accordingly, `.lastIndex` is the only mutable property. All other properties are read-only. If you want to change them, you need to copy the regular expression (consult [§43.1.2 “Cloning and non-destructively modifying regular expressions”](#ch044.xhtml_cloning-regexps) for details).

### 43.4.1 Flags as properties

Each regular expression flag exists as a property with a longer, more descriptive name:

```
> /a/i.ignoreCase
true
> /a/.ignoreCase
false
```

This is the complete list of flag properties:

*   `.dotall` (`/s`)
*   `.global` (`/g`)
*   `.ignoreCase` (`/i`)
*   `.multiline` (`/m`)
*   `.sticky` (`/y`)
*   `.unicode` (`/u`)

### 43.4.2 Other properties

Each regular expression also has the following properties:

*   `.source` ^([ES3]): The regular expression pattern

    ```
    > /abc/ig.source
    'abc'
    ```

*   `.flags` ^([ES6]): The flags of the regular expression

    ```
    > /abc/ig.flags
    'gi'
    ```

*   `.lastIndex` ^([ES3]): Used when flag `/g` is switched on. Consult [§43.6 “Flag `/g` and its pitfalls”](#ch044.xhtml_regexp-flag-g) for details.

## 43.5 Methods for working with regular expressions

### 43.5.1 In general, regular expressions match anywhere in a string

Note that, in general, regular expressions match anywhere in a string:

```
> /a/.test('__a__')
true
```

You can change that by using assertions such as `^` or by using the flag `/y`:

```
> /^a/.test('__a__')
false
> /^a/.test('a__')
true
```

### 43.5.2 `regExp.test(str)`: is there a match? ^([ES3])

The regular expression method `.test()` returns `true` if `regExp` matches `str`:

```
> /bc/.test('ABCD')
false
> /bc/i.test('ABCD')
true
> /\.mjs$/.test('main.mjs')
true
```

With `.test()` you should normally avoid the `/g` flag. If you use it, you generally don’t get the same result every time you call the method:

```
> const r = /a/g;
> r.test('aab')
true
> r.test('aab')
true
> r.test('aab')
false
```

The results are due to `/a/` having two matches in the string. After all of those were found, `.test()` returns `false`.

### 43.5.3 `str.search(regExp)`: at what index is the match? ^([ES3])

The string method `.search()` returns the first index of `str` at which there is a match for `regExp`:

```
> '_abc_'.search(/abc/)
1
> 'main.mjs'.search(/\.mjs$/)
4
```

### 43.5.4 `regExp.exec(str)`: capturing groups ^([ES3])

#### 43.5.4.1 Getting a match object for the first match

Without the flag `/g`, `.exec()` returns the captures of the first match for `regExp` in `str`:

```
[](#cb1168-1)assert.deepEqual(
[](#cb1168-2)  /(a+)b/.exec('ab aab'),
[](#cb1168-3)  {
[](#cb1168-4)    0: 'ab',
[](#cb1168-5)    1: 'a',
[](#cb1168-6)    index: 0,
[](#cb1168-7)    input: 'ab aab',
[](#cb1168-8)    groups: undefined,
[](#cb1168-9)  }
[](#cb1168-10));
```

The result is a *match object* with the following properties:

*   `[0]`: the complete substring matched by the regular expression
*   `[1]`: capture of positional group 1 (etc.)
*   `.index`: where did the match occur?
*   `.input`: the string that was matched against
*   `.groups`: captures of named groups

#### 43.5.4.2 Named capture groups ^([ES2018])

The previous example contained a single positional group. The following example demonstrates named groups:

```
[](#cb1169-1)assert.deepEqual(
[](#cb1169-2)  /(?<as>a+)b/.exec('ab aab'),
[](#cb1169-3)  {
[](#cb1169-4)    0: 'ab',
[](#cb1169-5)    1: 'a',
[](#cb1169-6)    index: 0,
[](#cb1169-7)    input: 'ab aab',
[](#cb1169-8)    groups: { as: 'a' },
[](#cb1169-9)  }
[](#cb1169-10));
```

In the result of `.exec()`, you can see that a named group is also a positional group – its capture exists twice:

*   Once as a positional capture (property `'1'`).
*   Once as a named capture (property `groups.as`).

#### 43.5.4.3 Looping over multiple matches

If you want to retrieve all matches of a regular expression (not just the first one), you need to switch on the flag `/g`. Then you can call `.exec()` multiple times and get one match each time. After the last match, `.exec()` returns `null`.

```
> const regExp = /(a+)b/g;
> regExp.exec('ab aab')
{ 0: 'ab', 1: 'a', index: 0, input: 'ab aab', groups: undefined }
> regExp.exec('ab aab')
{ 0: 'aab', 1: 'aa', index: 3, input: 'ab aab', groups: undefined }
> regExp.exec('ab aab')
null
```

Therefore, you can loop over all matches as follows:

```
[](#cb1171-1)const regExp = /(a+)b/g;
[](#cb1171-2)const str = 'ab aab';
[](#cb1171-3)
[](#cb1171-4)let match;
[](#cb1171-5)// Check for null via truthiness
[](#cb1171-6)// Alternative: while ((match = regExp.exec(str)) !== null)
[](#cb1171-7)while (match = regExp.exec(str)) {
[](#cb1171-8)  console.log(match[1]);
[](#cb1171-9)}
[](#cb1171-10)// Output:
[](#cb1171-11)// 'a'
[](#cb1171-12)// 'aa'
```

Sharing regular expressions with `/g` has a few pitfalls, which are explained [later](#ch044.xhtml_regexp-flag-g).

![](media/file6.svg)  **Exercise: Extract quoted text via `.exec()`**

`exercises/regexps/extract_quoted_test.mjs`

### 43.5.5 `str.match(regExp)`: return all matching substrings ^([ES3])

Without `/g`, `.match()` works like `.exec()` – it returns a single match object.

With `/g`, `.match()` returns all substrings of `str` that match `regExp`:

```
> 'ab aab'.match(/(a+)b/g)
[ 'ab', 'aab' ]
```

If there is no match, `.match()` returns `null`:

```
> 'xyz'.match(/(a+)b/g)
null
```

You can use the Or operator to protect yourself against `null`:

```
[](#cb1174-1)const numberOfMatches = (str.match(regExp) || []).length;
```

### 43.5.6 `str.replace(searchValue, replacementValue)` ^([ES3])

`.replace()` is overloaded – it works differently, depending on the types of its parameters:

*   If `searchValue` is:
    *   Regular expression without `/g`: Replace first match of this regular expression.
    *   Regular expression with `/g`: Replace all matches of this regular expression.
    *   String: Replace first occurrence of this string (the string is interpreted verbatim, not as a regular expression). Alas, there is no way to replace every occurrence of a string. [Later in this chapter](#ch044.xhtml_escapeForRegExp), we’ll see a tool function that converts a string into a regular expression that matches this string (e.g., `'*'` becomes `/\*/`).
*   If `replacementValue` is:
    *   String: Replace matches with this string. The character `$` has special meaning and lets you insert captures of groups and more (read on for details).
    *   Function: Compute strings that replace matches via this function.

The next two subsubsections assume that a regular expression with `/g` is being used.

#### 43.5.6.1 `replacementValue` is a string

If the replacement value is a string, the dollar sign has special meaning – it inserts text matched by the regular expression:

| Text | Result |
| --- | --- |
| `$$` | single `$` |
| `$&` | complete match |
| `` $` `` | text before match |
| `$'` | text after match |
| `$n` | capture of positional group `n` (`n` > 0) |
| `$<name>` | capture of named group `name` ^([ES2018]) |

Example: Inserting the text before, inside, and after the matched substring.

```
> 'a1 a2'.replace(/a/g, "($`|$&|$')")
'(|a|1 a2)1 (a1 |a|2)2'
```

Example: Inserting the captures of positional groups.

```
> const regExp = /^([A-Za-z]+): (.*)$/ug;
> 'first: Jane'.replace(regExp, 'KEY: $1, VALUE: $2')
'KEY: first, VALUE: Jane'
```

Example: Inserting the captures of named groups.

```
> const regExp = /^(?<key>[A-Za-z]+): (?<value>.*)$/ug;
> 'first: Jane'.replace(regExp, 'KEY: $<key>, VALUE: $<value>')
'KEY: first, VALUE: Jane'
```

#### 43.5.6.2 `replacementValue` is a function

If the replacement value is a function, you can compute each replacement. In the following example, we multiply each non-negative integer that we find by two.

```
[](#cb1178-1)assert.equal(
[](#cb1178-2)  '3 cats and 4 dogs'.replace(/[0-9]+/g, (all) => 2 * Number(all)),
[](#cb1178-3)  '6 cats and 8 dogs'
[](#cb1178-4));
```

The replacement function gets the following parameters. Note how similar they are to match objects. These parameters are all positional, but I’ve included how one might name them:

*   `all`: complete match
*   `g1`: capture of positional group 1
*   Etc.
*   `index`: where did the match occur?
*   `input`: the string in which we are replacing
*   `groups` ^([ES2018]): captures of named groups (an object)

![](media/file6.svg)  **Exercise: Change quotes via `.replace()` and a named group**

`exercises/regexps/change_quotes_test.mjs`

### 43.5.7 Other methods for working with regular expressions

`String.prototype.split()` is described [in the chapter on strings](#ch021.xhtml_string-api-extracting). Its first parameter of `String.prototype.split()` is either a string or a regular expression. If it is the latter, then captures of groups appear in the result:

```
> 'a:b : c'.split(':')
[ 'a', 'b ', ' c' ]
> 'a:b : c'.split(/ *: */)
[ 'a', 'b', 'c' ]
> 'a:b : c'.split(/( *):( *)/)
[ 'a', '', '', 'b', ' ', ' ', 'c' ]
```

## 43.6 Flag `/g` and its pitfalls

The following two regular expression methods work differently if `/g` is switched on:

*   `RegExp.prototype.exec()`
*   `RegExp.prototype.test()`

Then they can be called repeatedly and deliver all matches inside a string. Property `.lastIndex` of the regular expression is used to track the current position inside the string – for example:

```
[](#cb1180-1)const r = /a/g;
[](#cb1180-2)assert.equal(r.lastIndex, 0);
[](#cb1180-3)
[](#cb1180-4)assert.equal(r.test('aa'), true); // 1st match?
[](#cb1180-5)assert.equal(r.lastIndex, 1); // after 1st match
[](#cb1180-6)
[](#cb1180-7)assert.equal(r.test('aa'), true); // 2nd match?
[](#cb1180-8)assert.equal(r.lastIndex, 2); // after 2nd match
[](#cb1180-9)
[](#cb1180-10)assert.equal(r.test('aa'), false); // 3rd match?
[](#cb1180-11)assert.equal(r.lastIndex, 0); // start over
```

The next subsections explain the pitfalls of using `/g`. They are followed by a subsection that explains how to work around those pitfalls.

### 43.6.1 Pitfall: You can’t inline a regular expression with flag `/g`

A regular expression with `/g` can’t be inlined. For example, in the following `while` loop, the regular expression is created fresh, every time the condition is checked. Therefore, its `.lastIndex` is always zero and the loop never terminates.

```
[](#cb1181-1)let count = 0;
[](#cb1181-2)// Infinite loop
[](#cb1181-3)while (/a/g.test('babaa')) {
[](#cb1181-4)  count++;
[](#cb1181-5)}
```

### 43.6.2 Pitfall: Removing `/g` can break code

If code expects a regular expression with `/g` and has a loop over the results of `.exec()` or `.test()`, then a regular expression without `/g` can cause an infinite loop:

```
[](#cb1182-1)function countMatches(regExp) {
[](#cb1182-2)  let count = 0;
[](#cb1182-3)  // Infinite loop
[](#cb1182-4)  while (regExp.exec('babaa')) {
[](#cb1182-5)    count++;
[](#cb1182-6)  }
[](#cb1182-7)  return count;
[](#cb1182-8)}
[](#cb1182-9)countMatches(/a/); // Missing: flag /g
```

Why? Because `.exec()` always returns the first result, a match object, and never `null`.

### 43.6.3 Pitfall: Adding `/g` can break code

With `.test()`, there is another caveat: if you want to check exactly once if a regular expression matches a string, then the regular expression must not have `/g`. Otherwise, you generally get a different result every time you call `.test()`:

```
[](#cb1183-1)function isMatching(regExp) {
[](#cb1183-2)  return regExp.test('Xa');
[](#cb1183-3)}
[](#cb1183-4)const myRegExp = /^X/g;
[](#cb1183-5)assert.equal(isMatching(myRegExp), true);
[](#cb1183-6)assert.equal(isMatching(myRegExp), false);
```

Normally, you won’t add `/g` if you intend to use `.test()` in this manner. But it can happen if, for example, you use the same regular expression for testing and for replacing.

### 43.6.4 Pitfall: Code can break if `.lastIndex` isn’t zero

If you match a regular expression multiple times via `.exec()` or `.test()`, the current position inside the input string is stored in the regular expression property `.lastIndex`. Therefore, code that matches multiple times may break if `.lastIndex` is not zero:

```
[](#cb1184-1)function countMatches(regExp) {
[](#cb1184-2)  let count = 0;
[](#cb1184-3)  while (regExp.exec('babaa')) {
[](#cb1184-4)    count++;
[](#cb1184-5)  }
[](#cb1184-6)  return count;
[](#cb1184-7)}
[](#cb1184-8)
[](#cb1184-9)const myRegExp = /a/g;
[](#cb1184-10)myRegExp.lastIndex = 4;
[](#cb1184-11)assert.equal(countMatches(myRegExp), 1); // should be 3
```

Note that `.lastIndex` is always zero in newly created regular expressions, but it may not be if the same regular expression is used multiple times.

### 43.6.5 Dealing with `/g` and `.lastIndex`

As an example of dealing with `/g` and `.lastIndex`, we will implement the following function:

```
[](#cb1185-1)countMatches(regExp, str)
```

It counts how often `regExp` has a match inside `str`. How do we prevent a wrong `regExp` from breaking our code? Let’s look at three approaches.

First, we can throw an exception if `/g` isn’t set or `.lastIndex` isn’t zero:

```
[](#cb1186-1)function countMatches(regExp, str) {
[](#cb1186-2)  if (!regExp.global) {
[](#cb1186-3)    throw new Error('Flag /g of regExp must be set');
[](#cb1186-4)  }
[](#cb1186-5)  if (regExp.lastIndex !== 0) {
[](#cb1186-6)    throw new Error('regExp.lastIndex must be zero');
[](#cb1186-7)  }
[](#cb1186-8) 
[](#cb1186-9)  let count = 0;
[](#cb1186-10)  while (regExp.test(str)) {
[](#cb1186-11)    count++;
[](#cb1186-12)  }
[](#cb1186-13)  return count;
[](#cb1186-14)}
```

Second, we can clone the parameter. That has the added benefit that `regExp` won’t be changed.

```
[](#cb1187-1)function countMatches(regExp, str) {
[](#cb1187-2)  const cloneFlags = regExp.flags + (regExp.global ? '' : 'g');
[](#cb1187-3)  const clone = new RegExp(regExp, cloneFlags);
[](#cb1187-4)
[](#cb1187-5)  let count = 0;
[](#cb1187-6)  while (clone.test(str)) {
[](#cb1187-7)    count++;
[](#cb1187-8)  }
[](#cb1187-9)  return count;
[](#cb1187-10)}
```

Third, we can use `.match()` to count occurrences, which doesn’t change or depend on `.lastIndex`.

```
[](#cb1188-1)function countMatches(regExp, str) {
[](#cb1188-2)  if (!regExp.global) {
[](#cb1188-3)    throw new Error('Flag /g of regExp must be set');
[](#cb1188-4)  }
[](#cb1188-5)  return (str.match(regExp) || []).length;
[](#cb1188-6)}
```

## 43.7 Techniques for working with regular expressions

### 43.7.1 Escaping arbitrary text for regular expressions

The following function escapes an arbitrary text so that it is matched verbatim if you put it inside a regular expression:

```
[](#cb1189-1)function escapeForRegExp(str) {
[](#cb1189-2)  return str.replace(/[\\^$.*+?()[\]{}|]/g, '\\$&'); // (A)
[](#cb1189-3)}
[](#cb1189-4)assert.equal(escapeForRegExp('[yes?]'), String.raw`\[yes\?\]`);
[](#cb1189-5)assert.equal(escapeForRegExp('_g_'), String.raw`_g_`);
```

In line A, we escape all syntax characters. We have to be selective because the regular expression flag `/u` forbids many escapes – for example: `\a \: \-`

The regular expression method `.replace()` only lets you replace plain text once. With `escapeForRegExp()`, we can work around that limitation and replace plain text multiple times:

```
[](#cb1190-1)const plainText = ':-)';
[](#cb1190-2)const regExp = new RegExp(escapeForRegExp(plainText), 'ug');
[](#cb1190-3)assert.equal(
[](#cb1190-4)  ':-) :-) :-)'.replace(regExp, '🙂'), '🙂 🙂 🙂');
```

### 43.7.2 Matching everything or nothing

Sometimes, you may need a regular expression that matches everything or nothing – for example, as a default value.

*   Match everything: `/(?:)/`

    The empty group `()` matches everything. We make it non-capturing (via `?:`), to avoid unnecessary work.

    ```
    > /(?:)/.test('')
    true
    > /(?:)/.test('abc')
    true
    ```

*   Match nothing: `/.^/`

    `^` only matches at the beginning of a string. The dot moves matching beyond the first character and now `^` doesn’t match anymore.

    ```
    > /.^/.test('')
    false
    > /.^/.test('abc')
    false
    ```

# 44 Dates (`Date`)

* * *

*   44.1 [Best practice: avoid the built-in `Date`](#ch045.xhtml_date-libraries)
    *   44.1.1 [Things to look for in a date library](#ch045.xhtml_things-to-look-for-in-a-date-library)
*   44.2 [Time standards](#ch045.xhtml_time-standards)
    *   44.2.1 [Background: UTC vs. Z vs. GMT](#ch045.xhtml_background-utc-vs.-z-vs.-gmt)
    *   44.2.2 [Dates do not support time zones](#ch045.xhtml_dates-have-no-time-zones)
*   44.3 [Background: date time formats (ISO)](#ch045.xhtml_date-time-formats)
    *   44.3.1 [Tip: append a `Z` to make date parsing deterministic](#ch045.xhtml_tip-append-a-z-to-make-date-parsing-deterministic)
*   44.4 [Time values](#ch045.xhtml_time-values)
    *   44.4.1 [Creating time values](#ch045.xhtml_creating-time-values)
    *   44.4.2 [Getting and setting time values](#ch045.xhtml_getting-and-setting-time-values)
*   44.5 [Creating Dates](#ch045.xhtml_creating-dates)
    *   44.5.1 [Creating dates via numbers](#ch045.xhtml_creating-dates-via-numbers)
    *   44.5.2 [Parsing dates from strings](#ch045.xhtml_parsing-dates-from-strings)
    *   44.5.3 [Other ways of creating dates](#ch045.xhtml_other-ways-of-creating-dates)
*   44.6 [Getters and setters](#ch045.xhtml_getters-and-setters)
    *   44.6.1 [Time unit getters and setters](#ch045.xhtml_time-unit-getters-and-setters)
*   44.7 [Converting Dates to strings](#ch045.xhtml_converting-dates-to-strings)
    *   44.7.1 [Strings with times](#ch045.xhtml_strings-with-times)
    *   44.7.2 [Strings with dates](#ch045.xhtml_strings-with-dates)
    *   44.7.3 [Strings with dates and times](#ch045.xhtml_strings-with-dates-and-times)
    *   44.7.4 [Other methods](#ch045.xhtml_other-methods)

* * *

This chapter describes JavaScript’s API for working with dates – the class `Date`.

## 44.1 Best practice: avoid the built-in `Date`

The JavaScript `Date` API is cumbersome to use. Hence, it’s best to rely on a library for anything related to dates. Popular libraries include:

*   [Moment.js](https://momentjs.com)
*   [Day.js](https://github.com/iamkun/dayjs)
*   [Luxon](https://moment.github.io/luxon/)
*   [js-joda](https://js-joda.github.io/js-joda/)
*   [date-fns](https://github.com/date-fns/date-fns)

Consult the blog post [“Why you shouldn’t use Moment.js…”](https://inventi.studio/en/blog/why-you-shouldnt-use-moment-js) for the pros and cons of these libraries.

Additionally, TC39 is working on a new date API for JavaScript: [`temporal`](https://github.com/maggiepint/proposal-temporal).

### 44.1.1 Things to look for in a date library

Two things are important to keep in mind:

*   [*Tree-shaking*](#ch047.xhtml_tree-shaking) can considerably reduce the size of a library. It is a technique of only deploying those exports of a library to a web server that are imported somewhere. Functions are much more amenable to tree-shaking than classes.

*   Support for time zones: As explained [later](#ch045.xhtml_dates-have-no-time-zones), `Date` does not support time zones, which introduces a number of pitfalls and is a key weakness. Make sure that your date library supports them.

## 44.2 Time standards

### 44.2.1 Background: UTC vs. Z vs. GMT

UTC, Z, and GMT are ways of specifying time that are similar, but subtly different:

*   UTC (Coordinated Universal Time) is the time standard that all times zones are based on. They are specified relative to it. That is, no country or territory has UTC as its local time zone.

*   Z (Zulu Time Zone) is a military time zone that is often used in aviation and the military as another name for UTC+0.

*   GMT (Greenwich Mean Time) is a time zone used in some European and African countries. It is UTC plus zero hours and therefore has the same time as UTC.

Sources:

*   [“The Difference Between GMT and UTC”](https://www.timeanddate.com/time/gmt-utc-time.html) at TimeAndDate.com
*   [“Z – Zulu Time Zone (Military Time)”](https://www.timeanddate.com/time/zones/z) at TimeAndDate.com

### 44.2.2 Dates do not support time zones

Dates support the following time standards:

*   The local time zone (which depends on the current location)
*   UTC
*   Time offsets (relative to UTC)

Depending on the operation, only some of those options are available. For example, when converting dates to strings or extracting time units such as the day of the month, you can only choose between the local time zone and UTC.

Internally, Dates are stored as UTC. When converting from or to the local time zone, the necessary offsets are determined via the date. In the following example, the local time zone is Europe/Paris:

```
[](#cb1193-1)// CEST (Central European Summer Time)
[](#cb1193-2)assert.equal(
[](#cb1193-3)  new Date('2122-06-29').getTimezoneOffset(), -120);
[](#cb1193-4) 
[](#cb1193-5)// CET (Central European Time)
[](#cb1193-6)assert.equal(
[](#cb1193-7)  new Date('2122-12-29').getTimezoneOffset(), -60);
```

Whenever you create or convert dates, you need to be mindful of the time standard being used – for example: `new Date()` uses the local time zone while `.toISOString()` uses UTC.

```
> new Date(2077, 0, 27).toISOString()
'2077-01-26T23:00:00.000Z'
```

Dates interpret 0 as January. The day of the month is 27 in the local time zone, but 26 in UTC.

![](media/file2.svg)  **Documenting the time standards supported by each operation**

In the remainder of this chapter, the supported time standards are noted for each operation.

#### 44.2.2.1 The downsides of not being able to specify time zones

Not being able to specify time zones has two downsides:

*   It makes it impossible to support multiple time zones.

*   It can lead to location-specific bugs. For example, the previous example produces different results depending on where it is executed. To be safe:

    *   Use UTC-based operations whenever possible
    *   Use `Z` or a time offset when parsing strings (see the next section for more information).

## 44.3 Background: date time formats (ISO)

Date time formats describe:

*   The strings accepted by:
    *   `Date.parse()`
    *   `new Date()`
*   The strings returned by (always longest format):
    *   `Date.prototype.toISOString()`

The following is an example of a date time string returned by `.toISOString()`:

```
[](#cb1195-1)'2033-05-28T15:59:59.123Z'
```

Date time formats have the following structures:

*   Date formats: Y=year; M=month; D=day

    ```
    YYYY-MM-DD
    YYYY-MM
    YYYY
    ```

*   Time formats: T=separator (the string `'T'`); H=hour; m=minute; s=second and millisecond; Z=Zulu Time Zone (the string `'Z'`)

    ```
    THH:mm:ss.sss
    THH:mm:ss.sssZ

    THH:mm:ss
    THH:mm:ssZ

    THH:mm
    THH:mmZ
    ```

*   Date time formats: are date formats followed by time formats.

    *   For example (longest): `YYYY-MM-DDTHH:mm:ss.sssZ`

Instead of `Z` (which is UTC+0), we can also specify *time offsets* relative to UTC:

*   `THH:mm+HH:mm` (etc.)
*   `THH:mm-HH:mm` (etc.)

### 44.3.1 Tip: append a `Z` to make date parsing deterministic

If you add a `Z` to the end of a string, date parsing doesn’t produce different results at different locations:

*   Without `Z`: Input is January 27 (in the Europe/Paris time zone), output is January 26 (in UTC).

    ```
    > new Date('2077-01-27T00:00').toISOString()
    '2077-01-26T23:00:00.000Z'
    ```

*   With `Z`: Input is January 27, output is January 27.

    ```
    > new Date('2077-01-27T00:00Z').toISOString()
    '2077-01-27T00:00:00.000Z'
    ```

## 44.4 Time values

A *time value* represents a date via the number of milliseconds since 1 January 1970 00:00:00 UTC.

Time values can be used to create Dates:

```
[](#cb1200-1)const timeValue = 0;
[](#cb1200-2)assert.equal(
[](#cb1200-3)  new Date(timeValue).toISOString(),
[](#cb1200-4)  '1970-01-01T00:00:00.000Z');
```

Coercing a Date to a number returns its time value:

```
> Number(new Date(123))
123
```

Ordering operators coerce their operands to numbers. Therefore, you can use these operators to compare Dates:

```
[](#cb1202-1)assert.equal(
[](#cb1202-2)  new Date('1972-05-03') < new Date('2001-12-23'), true);
[](#cb1202-3)
[](#cb1202-4)// Internally:
[](#cb1202-5)assert.equal(73699200000 < 1009065600000, true);
```

### 44.4.1 Creating time values

The following methods create time values:

*   `Date.now(): number` (UTC)

    Returns the current time as a time value.

*   `Date.parse(dateTimeStr: string): number` (local time zone, UTC, time offset)

    Parses `dateTimeStr` and returns the corresponding time value.

*   `Date.UTC(year, month, date?, hours?, minutes?, seconds?, milliseconds?): number` (UTC)

    Returns the time value for the specified UTC date time.

### 44.4.2 Getting and setting time values

*   `Date.prototype.getTime(): number` (UTC)

    Returns the time value corresponding to the Date.

*   `Date.prototype.setTime(timeValue)` (UTC)

    Sets `this` to the date encoded by `timeValue`.

## 44.5 Creating Dates

### 44.5.1 Creating dates via numbers

`new Date(year: number, month: number, date?: number, hours?: number, minutes?: number, seconds?: number, milliseconds?: number)` (local time zone)

Two of the parameters have pitfalls:

*   For `month`, 0 is January, 1 is February, etc.

*   If 0 ≤ `year` ≤ 99, then 1900 is added:

    ```
    > new Date(12, 1, 22, 19, 11).getFullYear()
    1912
    ```

    That’s why, elsewhere in this chapter, we avoid the time unit `year` and always use `fullYear`. But in this case, we have no choice.

Example:

```
> new Date(2077,0,27, 21,49).toISOString() // CET (UTC+1)
'2077-01-27T20:49:00.000Z'
```

Note that the input hours (21) are different from the output hours (20). The former refer to the local time zone, the latter to UTC.

### 44.5.2 Parsing dates from strings

`new Date(dateTimeStr: string)` (local time zone, UTC, time offset)

If there is a `Z` at the end, UTC is used:

```
> new Date('2077-01-27T00:00Z').toISOString()
'2077-01-27T00:00:00.000Z'
```

If there is not `Z` or time offset at the end, the local time zone is used:

```
> new Date('2077-01-27T00:00').toISOString() // CET (UTC+1)
'2077-01-26T23:00:00.000Z'
```

If a string only contains a date, it is interpreted as UTC:

```
> new Date('2077-01-27').toISOString()
'2077-01-27T00:00:00.000Z'
```

### 44.5.3 Other ways of creating dates

*   `new Date(timeValue: number)` (UTC)

    ```
    > new Date(0).toISOString()
    '1970-01-01T00:00:00.000Z'
    ```

*   `new Date()` (UTC)

    The same as `new Date(Date.now())`.

## 44.6 Getters and setters

### 44.6.1 Time unit getters and setters

Dates have getters and setters for time units – for example:

*   `Date.prototype.getFullYear()`
*   `Date.prototype.setFullYear(num)`

These getters and setters conform to the following patterns:

*   Local time zone:
    *   `Date.prototype.get«Unit»()`
    *   `Date.prototype.set«Unit»(num)`
*   UTC:
    *   `Date.prototype.getUTC«Unit»()`
    *   `Date.prototype.setUTC«Unit»(num)`

These are the time units that are supported:

*   Date
    *   `FullYear`
    *   `Month`: month (0–11). **Pitfall:** 0 is January, etc.
    *   `Date`: day of the month (1–31)
    *   `Day` (getter only): day of the week (0–6, 0 is Sunday)
*   Time
    *   `Hours`: hour (0–23)
    *   `Minutes`: minutes (0–59)
    *   `Seconds`: seconds (0–59)
    *   `Milliseconds`: milliseconds (0–999)

There is one more getter that doesn’t conform to the previously mentioned patterns:

*   `Date.prototype.getTimezoneOffset()`

    Returns the time difference between local time zone and UTC in minutes. For example, for Europe/Paris, it returns `-120` (CEST, Central European Summer Time) or `-60` (CET, Central European Time):

    ```
    > new Date('2122-06-29').getTimezoneOffset()
    -120
    > new Date('2122-12-29').getTimezoneOffset()
    -60
    ```

## 44.7 Converting Dates to strings

Example Date:

```
[](#cb1210-1)const d = new Date(0);
```

### 44.7.1 Strings with times

*   `Date.prototype.toTimeString()` (local time zone)

    ```
    > d.toTimeString()
    '01:00:00 GMT+0100 (Central European Standard Time)'
    ```

### 44.7.2 Strings with dates

*   `Date.prototype.toDateString()` (local time zone)

    ```
    > d.toDateString()
    'Thu Jan 01 1970'
    ```

### 44.7.3 Strings with dates and times

*   `Date.prototype.toString()` (local time zone)

    ```
    > d.toString()
    'Thu Jan 01 1970 01:00:00 GMT+0100 (Central European Standard Time)'
    ```

*   `Date.prototype.toUTCString()` (UTC)

    ```
    > d.toUTCString()
    'Thu, 01 Jan 1970 00:00:00 GMT'
    ```

*   `Date.prototype.toISOString()` (UTC)

    ```
    > d.toISOString()
    '1970-01-01T00:00:00.000Z'
    ```

### 44.7.4 Other methods

The following three methods are not really part of ECMAScript, but rather of [the ECMAScript internationalization API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl). That API has much functionality for formatting dates (including support for time zones), but not for parsing them.

*   `Date.prototype.toLocaleTimeString()`
*   `Date.prototype.toLocaleDateString()`
*   `Date.prototype.toLocaleString()`

![](media/file6.svg)  **Exercise: Creating a date string**

`exercises/dates/create_date_string_test.mjs`

# 45 Creating and parsing JSON (`JSON`)

* * *

*   45.1 [The discovery and standardization of JSON](#ch046.xhtml_the-discovery-and-standardization-of-json)
    *   45.1.1 [JSON’s grammar is frozen](#ch046.xhtml_jsons-grammar-is-frozen)
*   45.2 [JSON syntax](#ch046.xhtml_json-syntax)
*   45.3 [Using the `JSON` API](#ch046.xhtml_using-the-json-api)
    *   45.3.1 [`JSON.stringify(data, replacer?, space?)`](#ch046.xhtml_JSON.stringify)
    *   45.3.2 [`JSON.parse(text, reviver?)`](#ch046.xhtml_json.parsetext-reviver)
    *   45.3.3 [Example: converting to and from JSON](#ch046.xhtml_example-converting-to-and-from-json)
*   45.4 [Customizing stringification and parsing (advanced)](#ch046.xhtml_json-replacers-revivers)
    *   45.4.1 [`.stringfy()`: specifying which properties of objects to stringify](#ch046.xhtml_stringfy-specifying-which-properties-of-objects-to-stringify)
    *   45.4.2 [`.stringify()` and `.parse()`: value visitors](#ch046.xhtml_json-value-visitors)
    *   45.4.3 [Example: visiting values](#ch046.xhtml_example-visiting-values)
    *   45.4.4 [Example: stringifying unsupported values](#ch046.xhtml_example-stringifying-unsupported-values)
    *   45.4.5 [Example: parsing unsupported values](#ch046.xhtml_example-parsing-unsupported-values)
*   45.5 [FAQ](#ch046.xhtml_faq)
    *   45.5.1 [Why doesn’t JSON support comments?](#ch046.xhtml_why-doesnt-json-support-comments)

* * *

JSON (“JavaScript Object Notation”) is a storage format that uses text to encode data. Its syntax is a subset of JavaScript expressions. As an example, consider the following text, stored in a file `jane.json`:

```
[](#cb1216-1){
[](#cb1216-2)  "first": "Jane",
[](#cb1216-3)  "last": "Porter",
[](#cb1216-4)  "married": true,
[](#cb1216-5)  "born": 1890,
[](#cb1216-6)  "friends": [ "Tarzan", "Cheeta" ]
[](#cb1216-7)}
```

JavaScript has the global namespace object `JSON` that provides methods for creating and parsing JSON.

## 45.1 The discovery and standardization of JSON

A specification for JSON was published by Douglas Crockford in 2001, at [`json.org`](http://json.org/). He explains:

> I discovered JSON. I do not claim to have invented JSON because it already existed in nature. What I did was I found it, I named it, I described how it was useful. I don’t claim to be the first person to have discovered it; I know that there are other people who discovered it at least a year before I did. The earliest occurrence I’ve found was, there was someone at Netscape who was using JavaScript array literals for doing data communication as early as 1996, which was at least five years before I stumbled onto the idea.

Later, JSON was standardized as [ECMA-404](https://www.ecma-international.org/publications/standards/Ecma-404.htm):

*   1st edition: October 2013
*   2nd edition: December 2017

### 45.1.1 JSON’s grammar is frozen

Quoting the ECMA-404 standard:

> Because it is so simple, it is not expected that the JSON grammar will ever change. This gives JSON, as a foundational notation, tremendous stability.

Therefore, JSON will never get improvements such as optional trailing commas, comments, or unquoted keys – independently of whether or not they are considered desirable. However, that still leaves room for creating supersets of JSON that compile to plain JSON.

## 45.2 JSON syntax

JSON consists of the following parts of JavaScript:

*   Compound:
    *   Object literals:
        *   Property keys are double-quoted strings.
        *   Property values are JSON values.
        *   No trailing commas are allowed.
    *   Array literals:
        *   Elements are JSON values.
        *   No holes or trailing commas are allowed.
*   Atomic:
    *   `null` (but not `undefined`)
    *   Booleans
    *   Numbers (excluding `NaN`, `+Infinity`, `-Infinity`)
    *   Strings (must be double-quoted)

As a consequence, you can’t (directly) represent cyclic structures in JSON.

## 45.3 Using the `JSON` API

The global namespace object `JSON` contains methods for working with JSON data.

### 45.3.1 `JSON.stringify(data, replacer?, space?)`

`.stringify()` converts JavaScript `data` to a JSON string. In this section, we are ignoring the parameter `replacer`; it is explained in [§45.4 “Customizing stringification and parsing”](#ch046.xhtml_json-replacers-revivers).

#### 45.3.1.1 Result: a single line of text

If you only provide the first argument, `.stringify()` returns a single line of text:

```
[](#cb1217-1)assert.equal(
[](#cb1217-2)  JSON.stringify({foo: ['a', 'b']}),
[](#cb1217-3)  '{"foo":["a","b"]}' );
```

#### 45.3.1.2 Result: a tree of indented lines

If you provide a non-negative integer for `space`, then `.stringify()` returns one or more lines and indents by `space` spaces per level of nesting:

```
[](#cb1218-1)assert.equal(
[](#cb1218-2)JSON.stringify({foo: ['a', 'b']}, null, 2),
[](#cb1218-3)`{
[](#cb1218-4) "foo": [
[](#cb1218-5) "a",
[](#cb1218-6) "b"
[](#cb1218-7) ]
[](#cb1218-8)}`);
```

#### 45.3.1.3 Details on how JavaScript data is stringified

**Primitive values:**

*   Supported primitive values are stringified as expected:

    ```
    > JSON.stringify('abc')
    '"abc"'
    > JSON.stringify(123)
    '123'
    > JSON.stringify(null)
    'null'
    ```

*   Unsupported numbers: `'null'`

    ```
    > JSON.stringify(NaN)
    'null'
    > JSON.stringify(Infinity)
    'null'
    ```

*   Other unsupported primitive values are not stringified; they produce the result `undefined`:

    ```
    > JSON.stringify(undefined)
    undefined
    > JSON.stringify(Symbol())
    undefined
    ```

**Objects:**

*   If an object has a method `.toJSON()`, then the result of that method is stringified:

    ```
    > JSON.stringify({toJSON() {return true}})
    'true'
    ```

    Dates have a method `.toJSON()` that returns a string:

    ```
    > JSON.stringify(new Date(2999, 11, 31))
    '"2999-12-30T23:00:00.000Z"'
    ```

*   Wrapped primitive values are unwrapped and stringified:

    ```
    > JSON.stringify(new Boolean(true))
    'true'
    > JSON.stringify(new Number(123))
    '123'
    ```

*   Arrays are stringified as Array literals. Unsupported Array elements are stringified as if they were `null`:

    ```
    > JSON.stringify([undefined, 123, Symbol()])
    '[null,123,null]'
    ```

*   All other objects – except for functions – are stringified as object literals. Properties with unsupported values are omitted:

    ```
    > JSON.stringify({a: Symbol(), b: true})
    '{"b":true}'
    ```

*   Functions are not stringified:

    ```
    > JSON.stringify(() => {})
    undefined
    ```

### 45.3.2 `JSON.parse(text, reviver?)`

`.parse()` converts a JSON `text` to a JavaScript value. In this section, we are ignoring the parameter `reviver`; it is explained [§45.4 “Customizing stringification and parsing”](#ch046.xhtml_json-replacers-revivers).

This is an example of using `.parse()`:

```
> JSON.parse('{"foo":["a","b"]}')
{ foo: [ 'a', 'b' ] }
```

### 45.3.3 Example: converting to and from JSON

The following class implements conversions from (line A) and to (line B) JSON.

```
[](#cb1229-1)class Point {
[](#cb1229-2)  static fromJson(jsonObj) { // (A)
[](#cb1229-3)    return new Point(jsonObj.x, jsonObj.y);
[](#cb1229-4)  }
[](#cb1229-5)
[](#cb1229-6)  constructor(x, y) {
[](#cb1229-7)    this.x = x;
[](#cb1229-8)    this.y = y;
[](#cb1229-9)  }
[](#cb1229-10) 
[](#cb1229-11)  toJSON() { // (B)
[](#cb1229-12)    return {x: this.x, y: this.y};
[](#cb1229-13)  }
[](#cb1229-14)}
```

*   Converting JSON to a point: We use the static method `Point.fromJson()` to parse JSON and create an instance of `Point`.

    ```
    [](#cb1230-1)assert.deepEqual(
    [](#cb1230-2)  Point.fromJson(JSON.parse('{"x":3,"y":5}')),
    [](#cb1230-3)  new Point(3, 5) );
    ```

*   Converting a point to JSON: `JSON.stringify()` internally calls [the previously mentioned method `.toJSON()`](#ch046.xhtml_stringification-details).

    ```
    [](#cb1231-1)assert.equal(
    [](#cb1231-2)  JSON.stringify(new Point(3, 5)),
    [](#cb1231-3)  '{"x":3,"y":5}' );
    ```

![](media/file6.svg)  **Exercise: Converting an object to and from JSON**

`exercises/json/to_from_json_test.mjs`

## 45.4 Customizing stringification and parsing (advanced)

Stringification and parsing can be customized as follows:

*   `JSON.stringify(data, replacer?, space?)`

    The optional parameter `replacer` contains either:

    *   An Array with names of properties. If a value in `data` is stringified as an object literal, then only the mentioned properties are considered. All other properties are ignored.
    *   A *value visitor*, a function that can transform JavaScript data before it is stringified.
*   `JSON.parse(text, reviver?)`

    The optional parameter `reviver` contains a value visitor that can transform the parsed JSON data before it is returned.

### 45.4.1 `.stringfy()`: specifying which properties of objects to stringify

If the second parameter of `.stringify()` is an Array, then only object properties, whose names are mentioned there, are included in the result:

```
[](#cb1232-1)const obj = {
[](#cb1232-2)  a: 1,
[](#cb1232-3)  b: {
[](#cb1232-4)    c: 2,
[](#cb1232-5)    d: 3,
[](#cb1232-6)  }
[](#cb1232-7)};
[](#cb1232-8)assert.equal(
[](#cb1232-9)  JSON.stringify(obj, ['b', 'c']),
[](#cb1232-10)  '{"b":{"c":2}}');
```

### 45.4.2 `.stringify()` and `.parse()`: value visitors

What I call a *value visitor* is a function that transforms JavaScript data:

*   `JSON.stringify()` lets the value visitor in its parameter `replacer` transform JavaScript data before it is stringified.
*   `JSON.parse()` lets the value visitor in its parameter `reviver` transform parsed JavaScript data before it is returned.

In this section, JavaScript data is considered to be a tree of values. If the data is atomic, it is a tree that only has a root. All values in the tree are fed to the value visitor, one at a time. Depending on what the visitor returns, the current value is omitted, changed, or preserved.

A value visitor has the following type signature:

```
[](#cb1233-1)type ValueVisitor = (key: string, value: any) => any;
```

The parameters are:

*   `value`: The current value.
*   `this`: Parent of current value. The parent of the root value `r` is `{'': r}`.
    *   Note: `this` is an implicit parameter and only available if the value visitor is an ordinary function.
*   `key`: Key or index of the current value inside its parent. The key of the root value is `''`.

The value visitor can return:

*   `value`: means there won’t be any change.
*   A different value `x`: leads to `value` being replaced with `x` in the output tree.
*   `undefined`: leads to `value` being omitted in the output tree.

### 45.4.3 Example: visiting values

The following code shows in which order a value visitor sees values:

```
[](#cb1234-1)const log = [];
[](#cb1234-2)function valueVisitor(key, value) {
[](#cb1234-3)  log.push({this: this, key, value});
[](#cb1234-4)  return value; // no change
[](#cb1234-5)}
[](#cb1234-6)
[](#cb1234-7)const root = {
[](#cb1234-8)  a: 1,
[](#cb1234-9)  b: {
[](#cb1234-10)    c: 2,
[](#cb1234-11)    d: 3,
[](#cb1234-12)  }
[](#cb1234-13)};
[](#cb1234-14)JSON.stringify(root, valueVisitor);
[](#cb1234-15)assert.deepEqual(log, [
[](#cb1234-16)  { this: { '': root }, key: '',  value: root   },
[](#cb1234-17)  { this: root        , key: 'a', value: 1      },
[](#cb1234-18)  { this: root        , key: 'b', value: root.b },
[](#cb1234-19)  { this: root.b      , key: 'c', value: 2      },
[](#cb1234-20)  { this: root.b      , key: 'd', value: 3      },
[](#cb1234-21)]);
```

As we can see, the replacer of `JSON.stringify()` visits values top-down (root first, leaves last). The rationale for going in that direction is that we are converting JavaScript values to JSON values. And a single JavaScript object may be expanded into a tree of JSON-compatible values.

In contrast, the reviver of `JSON.parse()` visits values bottom-up (leaves first, root last). The rationale for going in that direction is that we are assembling JSON values into JavaScript values. Therefore, we need to convert the parts before we can convert the whole.

### 45.4.4 Example: stringifying unsupported values

`JSON.stringify()` has no special support for regular expression objects – it stringifies them as if they were plain objects:

```
[](#cb1235-1)const obj = {
[](#cb1235-2)  name: 'abc',
[](#cb1235-3)  regex: /abc/ui,
[](#cb1235-4)};
[](#cb1235-5)assert.equal(
[](#cb1235-6)  JSON.stringify(obj),
[](#cb1235-7)  '{"name":"abc","regex":{}}');
```

We can fix that via a replacer:

```
[](#cb1236-1)function replacer(key, value) {
[](#cb1236-2)  if (value instanceof RegExp) {
[](#cb1236-3)    return {
[](#cb1236-4)      __type__: 'RegExp',
[](#cb1236-5)      source: value.source,
[](#cb1236-6)      flags: value.flags,
[](#cb1236-7)    };
[](#cb1236-8)  } else {
[](#cb1236-9)    return value; // no change
[](#cb1236-10)  }
[](#cb1236-11)}
[](#cb1236-12)assert.equal(
[](#cb1236-13)JSON.stringify(obj, replacer, 2),
[](#cb1236-14)`{
[](#cb1236-15) "name": "abc",
[](#cb1236-16) "regex": {
[](#cb1236-17) "__type__": "RegExp",
[](#cb1236-18) "source": "abc",
[](#cb1236-19) "flags": "iu"
[](#cb1236-20) }
[](#cb1236-21)}`);
```

### 45.4.5 Example: parsing unsupported values

To `JSON.parse()` the result from the previous section, we need a reviver:

```
[](#cb1237-1)function reviver(key, value) {
[](#cb1237-2)  // Very simple check
[](#cb1237-3)  if (value && value.__type__ === 'RegExp') {
[](#cb1237-4)    return new RegExp(value.source, value.flags);
[](#cb1237-5)  } else {
[](#cb1237-6)    return value;
[](#cb1237-7)  }
[](#cb1237-8)}
[](#cb1237-9)const str = `{
[](#cb1237-10) "name": "abc",
[](#cb1237-11) "regex": {
[](#cb1237-12) "__type__": "RegExp",
[](#cb1237-13) "source": "abc",
[](#cb1237-14) "flags": "iu"
[](#cb1237-15) }
[](#cb1237-16)}`;
[](#cb1237-17)assert.deepEqual(
[](#cb1237-18)  JSON.parse(str, reviver),
[](#cb1237-19)  {
[](#cb1237-20)    name: 'abc',
[](#cb1237-21)    regex: /abc/ui,
[](#cb1237-22)  });
```

## 45.5 FAQ

### 45.5.1 Why doesn’t JSON support comments?

Douglas Crockford explains why in [a Google+ post from 1 May 2012](https://web.archive.org/web/20190308024153/https://plus.google.com/+DouglasCrockfordEsq/posts/RK8qyGVaGSr):

> I removed comments from JSON because I saw people were using them to hold parsing directives, a practice which would have destroyed interoperability. I know that the lack of comments makes some people sad, but it shouldn’t.
> 
> Suppose you are using JSON to keep configuration files, which you would like to annotate. Go ahead and insert all the comments you like. Then pipe it through JSMin [a minifier for JavaScript] before handing it to your JSON parser.

# 46 Next steps: overview of web development (bonus)

* * *

*   46.1 [Tips against feeling overwhelmed](#ch047.xhtml_tips-against-feeling-overwhelmed)
*   46.2 [Things worth learning for web development](#ch047.xhtml_things-worth-learning-for-web-development)
    *   46.2.1 [Keep an eye on WebAssembly (Wasm)!](#ch047.xhtml_web-assembly)
*   46.3 [Example: tool-based JavaScript workflow](#ch047.xhtml_example-tool-based-javascript-workflow)
*   46.4 [An overview of JavaScript tools](#ch047.xhtml_overview-of-js-tools)
    *   46.4.1 [Building: getting from the JavaScript you write to the JavaScript you deploy](#ch047.xhtml_building-getting-from-the-javascript-you-write-to-the-javascript-you-deploy)
    *   46.4.2 [Static checking](#ch047.xhtml_static-checking)
    *   46.4.3 [Testing](#ch047.xhtml_testing)
    *   46.4.4 [Package managers](#ch047.xhtml_package-managers)
    *   46.4.5 [Libraries](#ch047.xhtml_libraries)
*   46.5 [Tools not related to JavaScript](#ch047.xhtml_tools-not-related-to-javascript)

* * *

You now know most of the JavaScript language. This chapter gives an overview of web development and describes next steps. It answers questions such as:

*   What should I learn next for web development?
*   What JavaScript-related tools should I know about?

## 46.1 Tips against feeling overwhelmed

Web development has become a vast field: Between JavaScript, web browsers, server-side JavaScript, JavaScript libraries, and JavaScript tools, there is a lot to know. Additionally, everything is always changing: some things go out of style, new things are invented, etc.

How can you avoid feeling overwhelmed when faced with this constantly changing vastness of knowledge?

*   Focus on the web technologies that you work with most often and learn them well. If you do frontend development, that may be JavaScript, CSS, SVG, or something else.
*   For JavaScript: Know the language, but also try out one tool in each of the following categories (which are covered in more detail later).
    *   Compilers: compile future JavaScript or supersets of JavaScript to normal JavaScript.
    *   Bundlers: combine all modules used by a web app into a single file (a script or a module). That makes loading faster and enables dead code elimination.
    *   Static checkers. For example:
        *   Linters: check for anti-patterns, style violations, and more.
        *   Type checkers: type JavaScript statically and report errors.
    *   Test libraries and tools
    *   Version control (usually git)

![](media/file2.svg)  **Trust in your ability to learn on demand**

It is commendable to learn something out of pure curiosity. But I’m wary of trying to learn everything and spreading yourself too thin. That also induces an anxiety of not knowing enough (because you never will). Instead, trust in your ability to learn things on demand!

## 46.2 Things worth learning for web development

These are a few things worth learning for web development:

*   Browser APIs such as the *Document Object Model* (DOM), the browsers’ representation of HTML in memory. They are the foundations of any kind of frontend development.

*   JavaScript-adjacent technologies such as HTML and CSS.

*   Frontend frameworks: When you get started with web development, it can be instructive to write user interfaces without any libraries. Once you feel more confident, frontend frameworks make many things easier, especially for larger apps. Popular frameworks include React, Angular, Vue, Ember, Svelte.

*   Node.js is the most popular platform for server-side JavaScript. But it also lets you run JavaScript in the command line. Most JavaScript-related tools (even compilers!) are implemented in Node.js-based JavaScript and installed via npm. A good way to get started with Node.js, is to use it for shell scripting.

*   JavaScript tooling: Modern web development involves many tools. Later in this chapter, there is an overview of the current tooling ecosystem.

*   Progressive web apps: The driving idea behind *progressive web apps* is to give web apps features that, traditionally, only native apps had – for example: native installation on mobile and desktop operating systems; offline operation; showing notifications to users. Google has published [a checklist](https://developers.google.com/web/progressive-web-apps/checklist) detailing what makes a web app *progressive*. The minimum requirements are:

    *   The app must be served over HTTPS (not the unsecure HTTP).
    *   The app must have a *Web App Manifest file*, specifying metadata such as app name and icon (often in multiple resolutions). The file(s) of the icon must also be present.
    *   The app must have a *service worker*: a base layer of the app that runs in the background, in a separate process (independently of web pages). One of its responsibilities is to keep the app functioning when there is no internet connection. Among others, two mechanisms help it do that: It is a local proxy that supervises all of the web resource requests of the app. And it has access to a browser’s cache. Therefore, it can use the cache to fulfill requests when the app is offline – after initially caching all critical resources. Other capabilities of service workers include synchronizing data in the background; receiving server-sent push messages; and the aforementioned showing notifications to users.

One good resource for learning web development – including and beyond JavaScript – is [MDN web docs](https://developer.mozilla.org/en-US/docs/Learn).

### 46.2.1 Keep an eye on WebAssembly (Wasm)!

[WebAssembly](https://webassembly.org) is a universal virtual machine that is built into most JavaScript engines. You get the following distribution of work:

*   JavaScript is for dynamic, higher-level code.
*   WebAssembly is for static, lower-level code.

For static code, WebAssembly is quite fast: C/C++ code, compiled to WebAssembly, is about 50% as fast as the same code, compiled to native ([source](https://arxiv.org/abs/1901.09056)). Use cases include support for new video formats, machine learning, gaming, etc.

WebAssembly works well as a compilation target for various languages. Does this mean JavaScript will be compiled to WebAssembly or replaced by another language?

#### 46.2.1.1 Will JavaScript be compiled to WebAssembly?

JavaScript engines perform many optimizations for JavaScript’s highly dynamic features. If you wanted to compile JavaScript to WebAssembly, you’d have to implement these optimizations on top of WebAssembly. The result would be slower than current engines and have a similar code base. Therefore, you wouldn’t gain anything.

#### 46.2.1.2 Will JavaScript be replaced by another language?

Does WebAssembly mean that JavaScript is about to be replaced by another language? WebAssembly does make it easier to support languages other than JavaScript in web browsers. But those languages face several challenges on that platform:

*   All browser APIs are based on JavaScript.
*   The runtimes (standard library, etc.) of other languages incur an additional memory overhead, whereas JavaScript’s runtime is already built into web browsers.
*   JavaScript is well-known, has many libraries and tools, etc.

Additionally, many parts of the WebAssembly ecosystem (e.g., debugging) are works in progress.

For dynamic code, JavaScript is comparatively fast. Therefore, for the foreseeable future, it will probably remain the most popular choice for high-level code. For low-level code, compiling more static languages (such as Rust) to WebAssembly is an intriguing option.

Given that it is just a virtual machine, there are not that many practically relevant things to learn about WebAssembly. But it is worth keeping an eye on its evolving role in web development. It is also becoming popular as a stand-alone virtual machine; e.g., supported by the [WebAssembly System Interface](https://github.com/WebAssembly/WASI).

## 46.3 Example: tool-based JavaScript workflow

![](media/file41.svg)

Figure 32: A classic, very simple web app: An HTML file refers to a JavaScript file `code.js`, which imbues the former with interactivity. `code.js` uses the library `library.js`, which must also be loaded by the HTML file.

Fig. [32](#ch047.xhtml_fig:classic_web_app) depicts a classic web app – when web development was less sophisticated (for better and for worse):

*   `index.html` contains the HTML file that is opened in web browsers.
*   `code.js` contains the JavaScript code loaded and used by `index.html`.
*   That code depends on the library `library.js`, a file that was downloaded manually and put next to `code.js`. It is accessed via a global variable. Note that the HTML file needs to load the dependency `library.js` for `code.js`. `code.js` can’t do that itself.

Since then, JavaScript workflows have become more complex. Fig. [33](#ch047.xhtml_fig:webpack_diagram) shows such a workflow – one that is based on the JavaScript bundler *webpack*.

![](media/file42.svg)

Figure 33: This is the workflow when developing a web app with the bundler *webpack*. Our web app consists of multiple modules. We tell webpack, in which one execution starts (the so-called *entry point*). It then analyzes the imports of the entry point, the imports of the imports, etc., to determine what code is needed to run the app. All of that code is put into a single script file.

Let’s examine the pieces (data, tools, technologies) involved in this workflow:

*   The app itself consists of multiple modules, written in *TypeScript* – a language that is a statically typed superset of JavaScript. Each file is an ECMAScript module, plus static type annotations.

*   The library used by the app is now downloaded and installed via [the npm package manager](#ch028.xhtml_npm-packages). It also transparently handles *transitive dependencies* – if this package depends on other packages, etc.

*   All TypeScript files are compiled to plain JS via a *loader*, a plugin for webpack.

*   The tool *webpack* combines all plain JavaScript files into a single JavaScript script file. This process is called *bundling*. Bundling is done for two reasons:

    *   Downloading a single file is usually faster in web browsers.
    *   During bundling, you can perform various optimizations, such as leaving out code that isn’t used.

The basic structure is still the same: the HTML file loads a JavaScript script file via a `<script>` element. However:

*   The code is now modular without the HTML file having to know the modules.
*   `bundle.js` only includes the code that is needed to run the app (vs. all of `library.js`).
*   We used a package manager to install the libraries that our code depends on.
*   The libraries aren’t accessed via global variables but via ES module specifiers.

In modern browsers, you can also deliver the bundle as a module (vs. as a script file).

## 46.4 An overview of JavaScript tools

Now that we have seen one workflow, let’s look at various categories of tools that are popular in the world of JavaScript. You’ll see categories of tools and lots of names of specific tools. The former are much more important. The names change, as tools come into and out of style, but I wanted you to see at least some of them.

### 46.4.1 Building: getting from the JavaScript you write to the JavaScript you deploy

*Building* JavaScript means getting from the JavaScript you write to the JavaScript you deploy. The following tools are often involved in this process:

*   Transpilers: A transpiler is a compiler that compiles source code to source code. Two transpilers that are popular in the JavaScript community are:

    *   Babel compiles upcoming and modern JavaScript features to older versions of the language. That means you can use new features in your code and still run it on older browsers.
    *   TypeScript is a superset of JavaScript. Roughly, it is the latest version of JavaScript plus static typing.
*   Minifiers: A minifier compiles JavaScript to equivalent, smaller (as in fewer characters) JavaScript. It does so by renaming variables, removing comments, removing whitespace, etc.

    For example, given the following input:

    ```
    [](#cb1238-1)let numberOfOccurrences = 5;
    [](#cb1238-2)if (Math.random()) {
    [](#cb1238-3)  // Math.random() is not zero
    [](#cb1238-4)  numberOfOccurrences++
    [](#cb1238-5)}
    ```

    A minifier might produce:

    ```
    [](#cb1239-1)let a=5;Math.random()&&a++;
    ```

    *   Popular minifiers include: [UglifyJS](http://lisperator.net/uglifyjs/), [babel-minify](https://github.com/babel/minify), [Terser](https://github.com/terser-js/terser), and [Closure Compiler](https://developers.google.com/closure/compiler/).
*   Bundlers: compile and optimize the code of a JavaScript app. The input of a bundler is many files – all of the app’s code plus the libraries it uses. A bundler combines these input files to produce fewer output files ([which tends to improve performance](https://medium.com/@asyncmax/the-right-way-to-bundle-your-assets-for-faster-sites-over-http-2-437c37efe3ff)).

    A bundler minimizes the size of its output via techniques such as *tree-shaking*. Tree-shaking is a form of dead code elimination: only those module exports are put in the output that are imported somewhere (across all code, while considering transitive imports).

    It is also common to perform compilation steps such as transpiling and minification while bundling. In these cases, a bundler relies on the previously mentioned tools, packaged as libraries.

    *   Popular bundlers include webpack, browserify, Rollup, and Parcel.

All of these tools and build steps are usually coordinated via so-called *task runners* (think “make” in Unix). There are:

*   Dedicated task runners: grunt, gulp, broccoli, etc.
*   Tools that can be used as simple task runners: npm (via its “scripts”) and webpack (via plugins).

### 46.4.2 Static checking

*Static checking* means analyzing source code *statically* (without running it). It can be used to detect a variety of problems. Tools include:

*   Linters: check the source code for problematic patterns, unused variables, etc. Linters are especially useful if you are still learning the language because they point out if you are doing something wrong.
    *   Popular linters include JSLint, JSHint, ESLint
*   Code style checkers: check if code is formatted properly. They consider indentation, spaces after brackets, spaces after commas, etc.
    *   Example: JSCS (JavaScript Code Style checker)
*   Code formatters: automatically format your code for you, according to rules that you can customize.
    *   Example: Prettier
*   Type checkers: add static type checking to JavaScript.
    *   Popular type checkers: TypeScript (which is also a transpiler), Flow.

### 46.4.3 Testing

JavaScript has many testing frameworks – for example:

*   Unit testing: Jasmine, Mocha, AVA, Jest, Karma, etc.
*   Integration testing: Jenkins, Travis CI, etc.
*   User interface testing: CasperJS, Protractor, Nightwatch.js, TestCafé, etc.

### 46.4.4 Package managers

The most popular package manager for JavaScript is npm. It started as a package manager for Node.js but has since also become dominant for client-side web development and tools of any kind.

There are alternatives to npm, but they are all based in one way or another on npm’s software registry:

*   [Yarn](https://yarnpkg.com/en/) is a different take on npm; some of the features it pioneered are now also supported by npm.
*   [pnpm](https://github.com/pnpm/pnpm) focuses on saving space when installing packages locally.

### 46.4.5 Libraries

*   Various helpers: lodash (which was originally based on the Underscore.js library) is one of the most popular general helper libraries for JavaScript.
*   Data structures: The following libraries are two examples among many.
    *   [Immutable.js](https://github.com/facebook/immutable-js/) provides immutable data structures for JavaScript.
    *   [Immer](https://github.com/mweststrate/immer) is an interesting lightweight alternative to Immutable.js. It also doesn’t mutate the data it operates on, but it works with normal objects and Arrays.
*   Date libraries: JavaScript’s built-in support for dates is limited and full of pitfalls. The chapter on dates [lists libraries](#ch045.xhtml_date-libraries) that you can use instead.
*   Internationalization: In this area, ECMAScript’s standard library is complemented by [the ECMAScript Internationalization API (ECMA-402)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl). It is accessed via the global variable `Intl` and available in most modern browsers.
*   Implementing and accessing services: The following are two popular options that are supported by a variety of libraries and tools.
    *   REST (Representative State Transfer) is one popular option for services and based on HTTP(S).
    *   [GraphQL](https://graphql.org/) is more sophisticated (for example, it can combine multiple data sources) and supports a query language.

## 46.5 Tools not related to JavaScript

Given that JavaScript is just one of several kinds of artifacts involved in web development, more tools exist. These are but a few examples:

*   CSS:
    *   Minifiers: reduce the size of CSS by removing comments, etc.
    *   Preprocessors: let you write compact CSS (sometimes augmented with control flow constructs, etc.) that is expanded into deployable, more verbose CSS.
    *   Frameworks: provide help with layout, decent-looking user interface components, etc.
*   Images: Automatically optimizing the size of bitmap images, etc.

# 47 Index

Symbol

*   [`!x`](#ch048.xhtml_index-entry-106)
*   [`++x`](#ch048.xhtml_index-entry-133)
*   [`x++`](#ch048.xhtml_index-entry-135)
*   [`+x`](#ch048.xhtml_index-entry-129)
*   [`,` (comma operator)](#ch048.xhtml_index-entry-85)
*   [`--x`](#ch048.xhtml_index-entry-137)
*   [`x--`](#ch048.xhtml_index-entry-139)
*   [`-x`](#ch048.xhtml_index-entry-131)
*   [`x && y`](#ch048.xhtml_index-entry-102)
*   [`x + y`](#ch048.xhtml_index-entry-77)
*   [`x - y`](#ch048.xhtml_index-entry-115)
*   [`x / y`](#ch048.xhtml_index-entry-121)
*   [`x << y`](#ch048.xhtml_index-entry-155)
*   [`x === y`](#ch048.xhtml_index-entry-82)
*   [`x >>> y`](#ch048.xhtml_index-entry-159)
*   [`x >> y`](#ch048.xhtml_index-entry-157)
*   [`x & y`](#ch048.xhtml_index-entry-147)
*   [`x ** y`](#ch048.xhtml_index-entry-126)
*   [`x * y`](#ch048.xhtml_index-entry-118)
*   [`x ^ y`](#ch048.xhtml_index-entry-151)
*   [`x ¦ y`](#ch048.xhtml_index-entry-149)
*   [`x ¦¦ y`](#ch048.xhtml_index-entry-104)
*   [`x ٪ y`](#ch048.xhtml_index-entry-124)
*   [`=`](#ch048.xhtml_index-entry-80)
*   [`c ? t : e`](#ch048.xhtml_index-entry-100)
*   [`__proto__`](#ch048.xhtml_index-entry-315)
*   [`~x`](#ch048.xhtml_index-entry-153)

A

*   [accessor (object literal)](#ch048.xhtml_index-entry-277)
*   [addition](#ch048.xhtml_index-entry-78)
*   [AMD module](#ch048.xhtml_index-entry-235)
*   [anonymous function expression](#ch048.xhtml_index-entry-199)
*   [argument](#ch048.xhtml_index-entry-216)
*   [argument vs. parameter](#ch048.xhtml_index-entry-218)
*   [Array](#ch048.xhtml_index-entry-344)
*   [Array hole](#ch048.xhtml_index-entry-356)
*   [Array index](#ch048.xhtml_index-entry-354)
*   [Array literal](#ch048.xhtml_index-entry-349)
*   [Array, dense](#ch048.xhtml_index-entry-358)
*   [Array, multidimensional](#ch048.xhtml_index-entry-353)
*   [Array, roles of an](#ch048.xhtml_index-entry-346)
*   [Array, sparse](#ch048.xhtml_index-entry-360)
*   [Array-destructuring](#ch048.xhtml_index-entry-393)
*   [Array-like object](#ch048.xhtml_index-entry-351)
*   [`ArrayBuffer`](#ch048.xhtml_index-entry-364)
*   [arrow function](#ch048.xhtml_index-entry-209)
*   [ASI (automatic semicolon insertion)](#ch048.xhtml_index-entry-20)
*   [`assert` (module)](#ch048.xhtml_index-entry-29)
*   [assertion](#ch048.xhtml_index-entry-28)
*   [assignment operator](#ch048.xhtml_index-entry-79)
*   [`async`](#ch048.xhtml_index-entry-424)
*   [async function](#ch048.xhtml_index-entry-422)
*   [`async function*`](#ch048.xhtml_index-entry-435)
*   [`async-await`](#ch048.xhtml_index-entry-423)
*   [asynchronous generator](#ch048.xhtml_index-entry-433)
*   [asynchronous iterable](#ch048.xhtml_index-entry-428)
*   [asynchronous iteration](#ch048.xhtml_index-entry-426)
*   [asynchronous iterator](#ch048.xhtml_index-entry-430)
*   [asynchronous programming](#ch048.xhtml_index-entry-407)
*   [attribute of a property](#ch048.xhtml_index-entry-310)
*   [automatic semicolon insertion (ASI)](#ch048.xhtml_index-entry-21)
*   [`await` (async function)](#ch048.xhtml_index-entry-425)
*   [`await` (asynchronous generator)](#ch048.xhtml_index-entry-436)

B

*   [big endian](#ch048.xhtml_index-entry-376)
*   [binary integer literal](#ch048.xhtml_index-entry-108)
*   [binding (variable)](#ch048.xhtml_index-entry-36)
*   [bitwise And](#ch048.xhtml_index-entry-146)
*   [bitwise Not](#ch048.xhtml_index-entry-152)
*   [bitwise Or](#ch048.xhtml_index-entry-148)
*   [bitwise Xor](#ch048.xhtml_index-entry-150)
*   [boolean](#ch048.xhtml_index-entry-89)
*   [`Boolean()`](#ch048.xhtml_index-entry-92)
*   [bound variable](#ch048.xhtml_index-entry-54)
*   [`break`](#ch048.xhtml_index-entry-179)
*   [bundler](#ch048.xhtml_index-entry-462)
*   [bundling](#ch048.xhtml_index-entry-463)

C

*   [call stack](#ch048.xhtml_index-entry-408)
*   [callback (asynchronous pattern)](#ch048.xhtml_index-entry-414)
*   [callback function](#ch048.xhtml_index-entry-219)
*   [camel case](#ch048.xhtml_index-entry-10)
*   [`catch`](#ch048.xhtml_index-entry-192)
*   [`class`](#ch048.xhtml_index-entry-318)
*   [class](#ch048.xhtml_index-entry-317)
*   [class declaration](#ch048.xhtml_index-entry-320)
*   [class definition](#ch048.xhtml_index-entry-319)
*   [class expression](#ch048.xhtml_index-entry-321)
*   [class, mixin](#ch048.xhtml_index-entry-333)
*   [classes, private data for](#ch048.xhtml_index-entry-325)
*   [closure](#ch048.xhtml_index-entry-53)
*   [code point](#ch048.xhtml_index-entry-162)
*   [code unit](#ch048.xhtml_index-entry-163)
*   [coercion](#ch048.xhtml_index-entry-74)
*   [comma operator](#ch048.xhtml_index-entry-84)
*   [CommonJS module](#ch048.xhtml_index-entry-233)
*   [comparing by identity](#ch048.xhtml_index-entry-70)
*   [comparing by value](#ch048.xhtml_index-entry-64)
*   [computed property key](#ch048.xhtml_index-entry-294)
*   [concatenating strings](#ch048.xhtml_index-entry-171)
*   [conditional operator](#ch048.xhtml_index-entry-98)
*   [console](#ch048.xhtml_index-entry-24)
*   [`console.error()`](#ch048.xhtml_index-entry-27)
*   [`console.log()`](#ch048.xhtml_index-entry-26)
*   [`const`](#ch048.xhtml_index-entry-35)
*   [constant](#ch048.xhtml_index-entry-33)
*   [constructor function (role of an ordinary function)](#ch048.xhtml_index-entry-208)
*   [`continue`](#ch048.xhtml_index-entry-181)
*   [Converting to [type]](#ch048.xhtml_index-entry-93)
*   [Coordinated Universal Time (UTC)](#ch048.xhtml_index-entry-446)
*   [copy object deeply](#ch048.xhtml_index-entry-286)
*   [copy object shallowly](#ch048.xhtml_index-entry-283)
*   [currying](#ch048.xhtml_index-entry-227)

D

*   [dash case](#ch048.xhtml_index-entry-13)
*   [`DataView`](#ch048.xhtml_index-entry-365)
*   [date](#ch048.xhtml_index-entry-444)
*   [date time format](#ch048.xhtml_index-entry-451)
*   [decimal floating point literal](#ch048.xhtml_index-entry-113)
*   [decimal integer literal](#ch048.xhtml_index-entry-110)
*   [decrementation operator (prefix)](#ch048.xhtml_index-entry-136)
*   [decrementation operator (suffix)](#ch048.xhtml_index-entry-138)
*   [deep copy of an object](#ch048.xhtml_index-entry-284)
*   [default export](#ch048.xhtml_index-entry-248)
*   [default value (destructuring)](#ch048.xhtml_index-entry-397)
*   [default value (parameter)](#ch048.xhtml_index-entry-221)
*   [`delete`](#ch048.xhtml_index-entry-297)
*   [deleting a property](#ch048.xhtml_index-entry-298)
*   [dense Array](#ch048.xhtml_index-entry-359)
*   [descriptor of a property](#ch048.xhtml_index-entry-312)
*   [destructive operation](#ch048.xhtml_index-entry-362)
*   [destructuring](#ch048.xhtml_index-entry-388)
*   [destructuring an Array](#ch048.xhtml_index-entry-392)
*   [destructuring an object](#ch048.xhtml_index-entry-389)
*   [dictionary (role of an object)](#ch048.xhtml_index-entry-271)
*   [direct method call](#ch048.xhtml_index-entry-330)
*   [dispatched method call](#ch048.xhtml_index-entry-328)
*   [divided by operator](#ch048.xhtml_index-entry-120)
*   [division](#ch048.xhtml_index-entry-122)
*   [`do-while`](#ch048.xhtml_index-entry-185)
*   [dynamic `this`](#ch048.xhtml_index-entry-211)
*   [dynamic vs. static](#ch048.xhtml_index-entry-41)

E

*   [early activation](#ch048.xhtml_index-entry-51)
*   [Ecma](#ch048.xhtml_index-entry-4)
*   [ECMA-262](#ch048.xhtml_index-entry-2)
*   [ECMAScript](#ch048.xhtml_index-entry-3)
*   [ECMAScript module](#ch048.xhtml_index-entry-238)
*   [Eich, Brendan](#ch048.xhtml_index-entry-1)
*   [endianness (Typed Arrays)](#ch048.xhtml_index-entry-375)
*   [enumerability](#ch048.xhtml_index-entry-305)
*   [enumerable (property attribute)](#ch048.xhtml_index-entry-306)
*   [environment (variables)](#ch048.xhtml_index-entry-226)
*   [equality operator](#ch048.xhtml_index-entry-81)
*   [ES module](#ch048.xhtml_index-entry-239)
*   [escaping HTML](#ch048.xhtml_index-entry-175)
*   [`eval()`](#ch048.xhtml_index-entry-225)
*   [evaluating an expression](#ch048.xhtml_index-entry-19)
*   [event (asynchronous pattern)](#ch048.xhtml_index-entry-413)
*   [event loop](#ch048.xhtml_index-entry-409)
*   [exception](#ch048.xhtml_index-entry-189)
*   [exercises, getting started with](#ch048.xhtml_index-entry-31)
*   [exponentiation](#ch048.xhtml_index-entry-127)
*   [`export`](#ch048.xhtml_index-entry-242)
*   [`export default`](#ch048.xhtml_index-entry-250)
*   [export, default](#ch048.xhtml_index-entry-249)
*   [export, named](#ch048.xhtml_index-entry-241)
*   [expression](#ch048.xhtml_index-entry-18)
*   [`extends`](#ch048.xhtml_index-entry-327)
*   [external iteration](#ch048.xhtml_index-entry-405)
*   [extracting a method](#ch048.xhtml_index-entry-288)

F

*   [`false`](#ch048.xhtml_index-entry-90)
*   [falsiness](#ch048.xhtml_index-entry-94)
*   [falsy](#ch048.xhtml_index-entry-95)
*   [`finally`](#ch048.xhtml_index-entry-193)
*   [flags (regular expression)](#ch048.xhtml_index-entry-443)
*   [`Float32Array`](#ch048.xhtml_index-entry-373)
*   [`Float64Array`](#ch048.xhtml_index-entry-374)
*   [floating point literal](#ch048.xhtml_index-entry-112)
*   [`for`](#ch048.xhtml_index-entry-186)
*   [`for-await-of`](#ch048.xhtml_index-entry-432)
*   [`for-in`](#ch048.xhtml_index-entry-188)
*   [`for-of`](#ch048.xhtml_index-entry-187)
*   [free variable](#ch048.xhtml_index-entry-56)
*   [freezing an object](#ch048.xhtml_index-entry-307)
*   [fulfilled (Promise state)](#ch048.xhtml_index-entry-419)
*   [function declaration](#ch048.xhtml_index-entry-198)
*   [function expression, anonymous](#ch048.xhtml_index-entry-200)
*   [function expression, named](#ch048.xhtml_index-entry-202)
*   [function, arrow](#ch048.xhtml_index-entry-210)
*   [function, ordinary](#ch048.xhtml_index-entry-195)
*   [function, roles of an ordinary](#ch048.xhtml_index-entry-205)
*   [function, specialized](#ch048.xhtml_index-entry-197)
*   [`function*`](#ch048.xhtml_index-entry-400)

G

*   [garbage collection](#ch048.xhtml_index-entry-69)
*   [generator, asynchronous](#ch048.xhtml_index-entry-434)
*   [generator, synchronous](#ch048.xhtml_index-entry-399)
*   [getter (object literal)](#ch048.xhtml_index-entry-278)
*   [`global`](#ch048.xhtml_index-entry-48)
*   [global object](#ch048.xhtml_index-entry-44)
*   [global scope](#ch048.xhtml_index-entry-43)
*   [global variable](#ch048.xhtml_index-entry-42)
*   [`globalThis`](#ch048.xhtml_index-entry-45)
*   [GMT (Greenwich Mean Time)](#ch048.xhtml_index-entry-449)
*   [grapheme cluster](#ch048.xhtml_index-entry-169)
*   [Greenwich Mean Time (GMT)](#ch048.xhtml_index-entry-450)

H

*   [heap](#ch048.xhtml_index-entry-68)
*   [hexadecimal integer literal](#ch048.xhtml_index-entry-111)
*   [hoisting](#ch048.xhtml_index-entry-52)
*   [hole in an Array](#ch048.xhtml_index-entry-357)

I

*   [identifier](#ch048.xhtml_index-entry-9)
*   [identity of an object](#ch048.xhtml_index-entry-66)
*   [`if`](#ch048.xhtml_index-entry-182)
*   [IIFE (immediately invoked function expression)](#ch048.xhtml_index-entry-231)
*   [immediately invoked function expression (IIFE)](#ch048.xhtml_index-entry-230)
*   [`import`](#ch048.xhtml_index-entry-245)
*   [`import()`](#ch048.xhtml_index-entry-258)
*   [import, named](#ch048.xhtml_index-entry-244)
*   [import, namespace](#ch048.xhtml_index-entry-247)
*   [`in`](#ch048.xhtml_index-entry-296)
*   [incrementation operator (prefix)](#ch048.xhtml_index-entry-132)
*   [incrementation operator (suffix)](#ch048.xhtml_index-entry-134)
*   [index of an Array](#ch048.xhtml_index-entry-355)
*   [`Infinity`](#ch048.xhtml_index-entry-142)
*   [inheritance, multiple](#ch048.xhtml_index-entry-337)
*   [inheritance, single](#ch048.xhtml_index-entry-335)
*   [`instanceof`](#ch048.xhtml_index-entry-323)
*   [`instanceof`](#ch048.xhtml_index-entry-72)
*   [`Int16Array`](#ch048.xhtml_index-entry-369)
*   [`Int32Array`](#ch048.xhtml_index-entry-371)
*   [`Int8Array`](#ch048.xhtml_index-entry-366)
*   [integer](#ch048.xhtml_index-entry-143)
*   [integer, safe](#ch048.xhtml_index-entry-145)
*   [internal iteration](#ch048.xhtml_index-entry-403)
*   [iterable (asynchronous)](#ch048.xhtml_index-entry-429)
*   [iterable (synchronous)](#ch048.xhtml_index-entry-341)
*   [iteration, asynchronous](#ch048.xhtml_index-entry-427)
*   [iteration, external](#ch048.xhtml_index-entry-406)
*   [iteration, internal](#ch048.xhtml_index-entry-404)
*   [iteration, synchronous](#ch048.xhtml_index-entry-339)
*   [iterator (asynchronous)](#ch048.xhtml_index-entry-431)
*   [iterator (synchronous)](#ch048.xhtml_index-entry-343)

J

*   [JSON (data format)](#ch048.xhtml_index-entry-453)
*   [`JSON` (namespace object)](#ch048.xhtml_index-entry-454)

K

*   [kebab case](#ch048.xhtml_index-entry-14)
*   [keyword](#ch048.xhtml_index-entry-16)

L

*   [label](#ch048.xhtml_index-entry-180)
*   [left shift operator](#ch048.xhtml_index-entry-154)
*   [`let`](#ch048.xhtml_index-entry-34)
*   [lexical `this`](#ch048.xhtml_index-entry-213)
*   [listing properties](#ch048.xhtml_index-entry-300)
*   [little endian](#ch048.xhtml_index-entry-377)
*   [logical And](#ch048.xhtml_index-entry-101)
*   [logical Not](#ch048.xhtml_index-entry-105)
*   [logical Or](#ch048.xhtml_index-entry-103)

M

*   [Map](#ch048.xhtml_index-entry-378)
*   [`Map`](#ch048.xhtml_index-entry-379)
*   [Map vs. object](#ch048.xhtml_index-entry-380)
*   [`Math` (namespace object)](#ch048.xhtml_index-entry-160)
*   [method](#ch048.xhtml_index-entry-287)
*   [method (object literal)](#ch048.xhtml_index-entry-274)
*   [method (role of an ordinary function)](#ch048.xhtml_index-entry-207)
*   [method call, direct](#ch048.xhtml_index-entry-331)
*   [method call, dispatched](#ch048.xhtml_index-entry-329)
*   [method, extracting a](#ch048.xhtml_index-entry-289)
*   [minification](#ch048.xhtml_index-entry-461)
*   [minifier](#ch048.xhtml_index-entry-460)
*   [minus operator (binary)](#ch048.xhtml_index-entry-114)
*   [minus operator (unary)](#ch048.xhtml_index-entry-130)
*   [mixin class](#ch048.xhtml_index-entry-332)
*   [module specifier](#ch048.xhtml_index-entry-256)
*   [module, AMD](#ch048.xhtml_index-entry-236)
*   [module, CommonJS](#ch048.xhtml_index-entry-234)
*   [multidimensional Array](#ch048.xhtml_index-entry-352)
*   [multiple inheritance](#ch048.xhtml_index-entry-336)
*   [multiple return values](#ch048.xhtml_index-entry-395)
*   [multiplication](#ch048.xhtml_index-entry-119)

N

*   [named export](#ch048.xhtml_index-entry-240)
*   [named function expression](#ch048.xhtml_index-entry-201)
*   [named import](#ch048.xhtml_index-entry-243)
*   [named parameter](#ch048.xhtml_index-entry-223)
*   [namespace import](#ch048.xhtml_index-entry-246)
*   [`NaN`](#ch048.xhtml_index-entry-141)
*   [`node_modules`](#ch048.xhtml_index-entry-255)
*   [npm](#ch048.xhtml_index-entry-251)
*   [npm package](#ch048.xhtml_index-entry-252)
*   [`null`](#ch048.xhtml_index-entry-88)
*   [number](#ch048.xhtml_index-entry-107)
*   [`Number()`](#ch048.xhtml_index-entry-140)

O

*   [object](#ch048.xhtml_index-entry-266)
*   [object literal](#ch048.xhtml_index-entry-272)
*   [object vs. Map](#ch048.xhtml_index-entry-381)
*   [object vs. primitive value](#ch048.xhtml_index-entry-61)
*   [`Object()`](#ch048.xhtml_index-entry-75)
*   [object, copy deeply](#ch048.xhtml_index-entry-285)
*   [object, copy shallowly](#ch048.xhtml_index-entry-282)
*   [object, freezing an](#ch048.xhtml_index-entry-308)
*   [object, identity of an](#ch048.xhtml_index-entry-67)
*   [object, roles of an](#ch048.xhtml_index-entry-269)
*   [object-destructuring](#ch048.xhtml_index-entry-390)
*   [`Object.is()`](#ch048.xhtml_index-entry-83)
*   [octal integer literal](#ch048.xhtml_index-entry-109)
*   [ordinary function](#ch048.xhtml_index-entry-194)
*   [ordinary function, roles of an](#ch048.xhtml_index-entry-204)
*   [override a property](#ch048.xhtml_index-entry-316)

P

*   [package, npm](#ch048.xhtml_index-entry-253)
*   [`package.json`](#ch048.xhtml_index-entry-254)
*   [parameter](#ch048.xhtml_index-entry-215)
*   [parameter default value](#ch048.xhtml_index-entry-220)
*   [parameter vs. argument](#ch048.xhtml_index-entry-217)
*   [partial application](#ch048.xhtml_index-entry-228)
*   [passing by identity](#ch048.xhtml_index-entry-65)
*   [passing by value](#ch048.xhtml_index-entry-63)
*   [pattern (regular expression)](#ch048.xhtml_index-entry-442)
*   [pending (Promise state)](#ch048.xhtml_index-entry-418)
*   [plus operator (binary)](#ch048.xhtml_index-entry-76)
*   [plus operator (unary)](#ch048.xhtml_index-entry-128)
*   [polyfill](#ch048.xhtml_index-entry-259)
*   [polyfill, speculative](#ch048.xhtml_index-entry-260)
*   [ponyfill](#ch048.xhtml_index-entry-265)
*   [primitive value](#ch048.xhtml_index-entry-62)
*   [primitive value vs. object](#ch048.xhtml_index-entry-60)
*   [private data for classes](#ch048.xhtml_index-entry-324)
*   [progressive web app](#ch048.xhtml_index-entry-455)
*   [prollyfill](#ch048.xhtml_index-entry-262)
*   [Promise](#ch048.xhtml_index-entry-415)
*   [Promise, states of a](#ch048.xhtml_index-entry-417)
*   [properties, listing](#ch048.xhtml_index-entry-301)
*   [property (object)](#ch048.xhtml_index-entry-267)
*   [property attribute](#ch048.xhtml_index-entry-309)
*   [property descriptor](#ch048.xhtml_index-entry-311)
*   [property key](#ch048.xhtml_index-entry-302)
*   [property key, computed](#ch048.xhtml_index-entry-295)
*   [property key, quoted](#ch048.xhtml_index-entry-293)
*   [property name](#ch048.xhtml_index-entry-303)
*   [property symbol](#ch048.xhtml_index-entry-304)
*   [property value shorthand](#ch048.xhtml_index-entry-273)
*   [property, deleting a](#ch048.xhtml_index-entry-299)
*   [prototype](#ch048.xhtml_index-entry-313)
*   [prototype chain](#ch048.xhtml_index-entry-314)
*   [publicly known symbol](#ch048.xhtml_index-entry-177)

Q

*   [quizzes, getting started with](#ch048.xhtml_index-entry-30)
*   [quoted property key](#ch048.xhtml_index-entry-292)

R

*   [real function (role of an ordinary function)](#ch048.xhtml_index-entry-206)
*   [receiver](#ch048.xhtml_index-entry-275)
*   [record (role of an object)](#ch048.xhtml_index-entry-270)
*   [`RegExp`](#ch048.xhtml_index-entry-440)
*   [regular expression](#ch048.xhtml_index-entry-439)
*   [regular expression literal](#ch048.xhtml_index-entry-441)
*   [rejected (Promise state)](#ch048.xhtml_index-entry-420)
*   [remainder operator](#ch048.xhtml_index-entry-123)
*   [REPL](#ch048.xhtml_index-entry-25)
*   [replica](#ch048.xhtml_index-entry-264)
*   [RequireJS](#ch048.xhtml_index-entry-237)
*   [reserved word](#ch048.xhtml_index-entry-15)
*   [rest element (Array-destructuring)](#ch048.xhtml_index-entry-394)
*   [rest parameter (function call)](#ch048.xhtml_index-entry-222)
*   [rest property (object-destructuring)](#ch048.xhtml_index-entry-391)
*   [return values, multiple](#ch048.xhtml_index-entry-396)
*   [revealing module pattern](#ch048.xhtml_index-entry-232)
*   [roles of an Array](#ch048.xhtml_index-entry-345)
*   [roles of an object](#ch048.xhtml_index-entry-268)
*   [roles of an ordinary function](#ch048.xhtml_index-entry-203)
*   [run-to-completion semantics](#ch048.xhtml_index-entry-412)

S

*   [safe integer](#ch048.xhtml_index-entry-144)
*   [scope of a variable](#ch048.xhtml_index-entry-37)
*   [script](#ch048.xhtml_index-entry-229)
*   [`self`](#ch048.xhtml_index-entry-47)
*   [sequence (role of an Array)](#ch048.xhtml_index-entry-348)
*   [Set](#ch048.xhtml_index-entry-384)
*   [`Set`](#ch048.xhtml_index-entry-385)
*   [setter (object literal)](#ch048.xhtml_index-entry-279)
*   [settled (Promise state)](#ch048.xhtml_index-entry-421)
*   [shadowing](#ch048.xhtml_index-entry-39)
*   [shallow copy of an object](#ch048.xhtml_index-entry-281)
*   [shim](#ch048.xhtml_index-entry-263)
*   [signed right shift operator](#ch048.xhtml_index-entry-156)
*   [single inheritance](#ch048.xhtml_index-entry-334)
*   [sloppy mode](#ch048.xhtml_index-entry-23)
*   [snake case](#ch048.xhtml_index-entry-12)
*   [sparse Array](#ch048.xhtml_index-entry-361)
*   [specialized function](#ch048.xhtml_index-entry-196)
*   [specifier, module](#ch048.xhtml_index-entry-257)
*   [speculative polyfill](#ch048.xhtml_index-entry-261)
*   [spreading (`...`) into a function call](#ch048.xhtml_index-entry-224)
*   [spreading into an Array literal](#ch048.xhtml_index-entry-350)
*   [spreading into an object literal](#ch048.xhtml_index-entry-280)
*   [statement](#ch048.xhtml_index-entry-17)
*   [states of a Promise](#ch048.xhtml_index-entry-416)
*   [`static`](#ch048.xhtml_index-entry-322)
*   [static vs. dynamic](#ch048.xhtml_index-entry-40)
*   [strict mode](#ch048.xhtml_index-entry-22)
*   [string](#ch048.xhtml_index-entry-170)
*   [`String()`](#ch048.xhtml_index-entry-172)
*   [subclass](#ch048.xhtml_index-entry-326)
*   [subtraction](#ch048.xhtml_index-entry-116)
*   [`switch`](#ch048.xhtml_index-entry-183)
*   [symbol](#ch048.xhtml_index-entry-176)
*   [symbol, publicly known](#ch048.xhtml_index-entry-178)
*   [synchronous generator](#ch048.xhtml_index-entry-398)
*   [synchronous iterable](#ch048.xhtml_index-entry-340)
*   [synchronous iteration](#ch048.xhtml_index-entry-338)
*   [synchronous iterator](#ch048.xhtml_index-entry-342)
*   [syntax](#ch048.xhtml_index-entry-8)

T

*   [tagged template](#ch048.xhtml_index-entry-174)
*   [task queue](#ch048.xhtml_index-entry-410)
*   [task runner](#ch048.xhtml_index-entry-465)
*   [TC39](#ch048.xhtml_index-entry-5)
*   [TC39 process](#ch048.xhtml_index-entry-7)
*   [TDZ (temporal dead zone)](#ch048.xhtml_index-entry-50)
*   [Technical Committee 39](#ch048.xhtml_index-entry-6)
*   [template literal](#ch048.xhtml_index-entry-173)
*   [temporal dead zone](#ch048.xhtml_index-entry-49)
*   [ternary operator](#ch048.xhtml_index-entry-99)
*   [`this`](#ch048.xhtml_index-entry-276)
*   [`this`, dynamic](#ch048.xhtml_index-entry-212)
*   [`this`, lexical](#ch048.xhtml_index-entry-214)
*   [`this`, pitfalls of](#ch048.xhtml_index-entry-290)
*   [`this`, values of](#ch048.xhtml_index-entry-291)
*   [`throw`](#ch048.xhtml_index-entry-190)
*   [time value](#ch048.xhtml_index-entry-452)
*   [times operator](#ch048.xhtml_index-entry-117)
*   [to the power of operator](#ch048.xhtml_index-entry-125)
*   [transpilation](#ch048.xhtml_index-entry-459)
*   [transpiler](#ch048.xhtml_index-entry-458)
*   [tree-shaking](#ch048.xhtml_index-entry-464)
*   [`true`](#ch048.xhtml_index-entry-91)
*   [truthiness](#ch048.xhtml_index-entry-96)
*   [truthy](#ch048.xhtml_index-entry-97)
*   [`try`](#ch048.xhtml_index-entry-191)
*   [tuple (role of an Array)](#ch048.xhtml_index-entry-347)
*   [type](#ch048.xhtml_index-entry-58)
*   [type hierarchy](#ch048.xhtml_index-entry-59)
*   [type signature](#ch048.xhtml_index-entry-0)
*   [Typed Array](#ch048.xhtml_index-entry-363)
*   [`typeof`](#ch048.xhtml_index-entry-71)
*   [TypeScript](#ch048.xhtml_index-entry-466)

U

*   [`Uint16Array`](#ch048.xhtml_index-entry-370)
*   [`Uint32Array`](#ch048.xhtml_index-entry-372)
*   [`Uint8Array`](#ch048.xhtml_index-entry-367)
*   [`Uint8ClampedArray`](#ch048.xhtml_index-entry-368)
*   [`undefined`](#ch048.xhtml_index-entry-87)
*   [underscore case](#ch048.xhtml_index-entry-11)
*   [Unicode](#ch048.xhtml_index-entry-161)
*   [Unicode Transformation Format (UTF)](#ch048.xhtml_index-entry-164)
*   [unit test](#ch048.xhtml_index-entry-32)
*   [unsigned right shift operator](#ch048.xhtml_index-entry-158)
*   [UTC (Coordinated Universal Time)](#ch048.xhtml_index-entry-445)
*   [UTF (Unicode Transformation Format)](#ch048.xhtml_index-entry-165)
*   [UTF-16](#ch048.xhtml_index-entry-167)
*   [UTF-32](#ch048.xhtml_index-entry-166)
*   [UTF-8](#ch048.xhtml_index-entry-168)

V

*   [variable, bound](#ch048.xhtml_index-entry-55)
*   [variable, free](#ch048.xhtml_index-entry-57)
*   [variable, scope of a](#ch048.xhtml_index-entry-38)
*   [`void` operator](#ch048.xhtml_index-entry-86)

W

*   [Wasm (WebAssembly)](#ch048.xhtml_index-entry-457)
*   [WeakMap](#ch048.xhtml_index-entry-382)
*   [`WeakMap`](#ch048.xhtml_index-entry-383)
*   [WeakSet](#ch048.xhtml_index-entry-386)
*   [`WeakSet`](#ch048.xhtml_index-entry-387)
*   [Web Worker](#ch048.xhtml_index-entry-411)
*   [WebAssembly](#ch048.xhtml_index-entry-456)
*   [`while`](#ch048.xhtml_index-entry-184)
*   [`window`](#ch048.xhtml_index-entry-46)
*   [wrapper types (for primitive types)](#ch048.xhtml_index-entry-73)

Y

*   [`yield` (asynchronous generator)](#ch048.xhtml_index-entry-437)
*   [`yield` (synchronous generator)](#ch048.xhtml_index-entry-401)
*   [`yield*` (asynchronous generator)](#ch048.xhtml_index-entry-438)
*   [`yield*` (synchronous generator)](#ch048.xhtml_index-entry-402)

Z

*   [Z (Zulu Time Zone)](#ch048.xhtml_index-entry-447)
*   [Zulu Time Zone (Z)](#ch048.xhtml_index-entry-448)