
# Learning TypeScript 5：超越 JavaScript，为大型项目构建更具维护性和健壮性的 Web

## 前言

熟悉 JavaScript 且希望进一步了解 TypeScript 5.0 的程序员会发现这本书是一本非常有价值的资源。对于想要提高前端编程技能并将 TypeScript 与 `Angular` 和 `React` 等流行框架集成的开发者来说，这本书是理想的。通过清晰的解释和实践示例，本书让 JavaScript 到 TypeScript 的过渡变得简单且愉快。

本书涵盖了静态类型、类型检查和类型推断等基础概念，这些将帮助你编写更可靠、更易维护的代码。你将学习如何使用 TypeScript 的特性来改进开发流程、减少 Bug 并提高代码质量。你将通过实践示例学习 TypeScript 的高级特性，如接口、模块和类型收窄技术。为了帮助你编写更高效、更洁的代码，本书还涵盖了如何使用 `async/await` 和 `Promises` 来处理异步操作。

TypeScript 为开发者面临的最常见 TypeScript 挑战提供了解决方案和排错技巧。你将发现如何为不同的情况创建自己的错误类，以及如何使用 TypeScript 的 `try/catch` 块来有效管理错误。书中还涵盖了 TypeScript 与现有 JavaScript 程序的集成、配置 TypeScript 编译器以及设置 TypeScript 项目的内容。

完成本书后，你将拥有使用 TypeScript 创建可扩展应用程序的知识和能力，并轻松与 `Angular` 和 `React` 等框架协作。无论是启动新项目还是升级现有项目，“学习 TypeScript 5”都提供了实用的见解和实践知识，帮助你提高开发技能并将你的编程水平提升到新的高度。

在书中，你将学习如何：

- 学习 TypeScript 的静态类型，让你的 JavaScript 代码更可靠、更不容易出错。

- 得益于详细说明和大量的示例，轻松从 JavaScript 切换到 TypeScript。

- 在 `Angular` 和 `React` 中使用 TypeScript 创建扩展、可靠的 Web 应用。

- 使用 TypeScript 的类型收窄和控制流分析创建完美的代码。

- 通过将 TypeScript 与 `Angular` 和 `React` 集成，实现开发生产力和应用速度。

- 使用 `Promises` 和 `async/await` 编写更简洁、更易读的脚本。

- 使用 `try/catch` 和其他错误处理方法实现健壮的错误管理系统。

- 掌握 TypeScript 的联合类型、接口和模块以进行代码组织。

- 使用 TypeScript 健壮的测试策略和强大的类型检查能力实现代码质量最大化。

## 序言

像我这样花费多年磨练 JavaScript 技能的开发者，深知制作用户喜爱的应用的快乐。我也经历过追踪由动态类型导致的晦涩 Bug 的挫败感。这就是为什么我决定深入 TypeScript，看看它如何同时改进我们的开发流程和最终产品。

有一天，在处理一个复杂的 JavaScript 项目时，我发现自己埋首在了一堆代码中，试图解决一个让团队抓狂的 Bug。那种 Bug 特别于当你观察它时它会消失，而当你认为它已经消失时它又会再次。经过几个小时的调试，我发现那是由于一个简单的类型不匹配。一个微小的错误导致了严重的后果。那就是我的“豁然开朗”时刻。我意识到我一个工具帮助我在开发早期识别这些问题。

当我开始学习 TypeScript 时，我既兴奋又好奇。起初，静态类型的概念似乎令人生畏，但我很快就意识到它在产生更可靠、更易维护的代码方面的价值。TypeScript 像一个得力的助手，引导你编写更有结构、更可预测的代码。它使你能够在开发期间识别错误，而不是等待它们在生产环境中意外出现。这意味着花更少的时间修复 Bug，而花更多的时间在创建用户喜欢的功能上。

我开始在一个侧边项目中使用 TypeScript，那是一个用于跟踪个人目标的小型 Web 应用。它最初只是一个提醒我跟进任务的简单工具，但随着我的开发，我意识到 TypeScript 正在帮助我编写更整洁、更有组织的代码。应用程序变得越来越复杂，TypeScript 帮助我管理这种复杂性，因为它允许我定义清晰的接口和数据结构。代码变得更易读、更易理解，不仅对我，对那些看它的人也是如此。

这个项目的经历教会了我如何使用 TypeScript 将一个杂乱的代码库组织成一件精美的艺术品。我在添加新功能时感到很有信心，而不必担心破坏现有功能。我的应用不仅仅是个人的成功；它展示了 TypeScript 的力量。当我与朋友和同事分享这个应用时，我意识到它也可以帮助其他人改进他们的项目。这激励我去分享我的所学并撰写了这本书。

在《学习 TypeScript 5》这本书中，我想让从 JavaScript 到 TypeScript 的过渡尽可能顺利。这本书不仅仅是一本技术指南，更是你我之间关于 TypeScript 如何提高你的编码技能和项目结果的对话。我们将从基础知识开始：配置你的环境和理解语法。然后我们将介绍更高级的主题，如类型收窄和异步编程。每一章都建立在前章的基础上，确保你对 TypeScript 的能力有彻底的理解。

我写这本书是为了让 TypeScript 更容易习得且更有趣。无论你是经验丰富的 JavaScript 开发者还是编程新手，你都能在这里找到实用的示例和现实应用，展示出 TypeScript 的优势。这本书将为你提供编写更高效、无错误代码所需的工具和知识。

## 第 1 章：TypeScript 简介

### 章节概述

`TypeScript` 是 JavaScript 的健壮超集，是我们本章第一个学习的主。我们将开始学习 `TypeScript` 是什么，以及它为什么成为现代 Web 开发中如此重要的工具。本节将强调使用 `TypeScript` 的主要优点，例如提高代码质量、更好的开发者体验以及在过程中检浀错误的能力。接下来，我们将引导你完成设置环境、安装 `Node.js`、配置 TypeScript 编译器以及设置 TypeScript 项目。在本节结束时，你应该已经准备好了功能齐全的环境。

### 理解 TypeScript 及其优势

`TypeScript` 是由 Microsoft 在 2012 年引入的，由 Anders Hejberg 牵头。考虑到 JavaScript 开发者所面临的局限性，Microsoft 旨在创建一个 JavaScript 的超集，提供了静态类型和高级工具支持。

### TypeScript 的历史与演变

从最初发布以来，`TypeScript` 在开发者社区中迅速获得了关注。早期版本专注于提供强大的类型系统和工具支持，但随着语言的成熟，它包含了更复杂的特性，如 `async/await`。与 `Angular` 等框架的集成使其不可或缺。

### TypeScript 的关键特性和能力

`TypeScript` 的主要优势在于其提供静态类型的能力。与 JavaScript 不同，类型相关问题通常在运行时发现，而 `TypeScript` 的类型系统有助于在开发阶段捕捉这些问题。集成开发环境提供了丰富的支持，包括代码补全和重构。这增强了开发体验，使代码更易编写和维护。`TypeScript` 还提供了高级特性，如泛型（允许创建可重用且类型安全的组件）以及装饰器（为类和方法添加元数据的方法）。这些特性使得构建大型复杂应用程序保持整洁、可维护且可扩展。

### 为什么选择 TypeScript 而不是 JavaScript?

`TypeScript` 比 `JavaScript` 具有若干优势，主要通过其类型系统。静态类型有助于防止由于类型不匹配引起的常见错误。这导致了更可靠和健壮的代码。接口和类型别名的使用促进了更好的设计模式和代码组织。另一个重大的优势是 `TypeScript` 与现有 `JavaScript` 代码的兼容性。`TypeScript` 文件可以无缝集成 `JavaScript` 文件，允许项目从 `JavaScript` 逐渐迁移到 `TypeScript`。这意味着团队可以在不需要重写整个代码库的情况下开始采用 `TypeScript`。

### 经典案例：Airbnb 迁移到 TypeScript

Airbnb 是一个著名的在线市场平台，其大型 JavaScript 代码遇到了严重问题。随着应用程序的增长，复杂性和 Bug 的数量也随之增加，许多是在运行时检测到的类型错误。这导致了维护工作增加和开发周期变慢。为了解决这些问题，Airbnb 选择从 `JavaScript` 切换到 `TypeScript`。迁移的动力是对更可靠和易维护代码库的需求。Airbnb 打算使用 TypeScript 的静态类型检查和增强工来提高代码质量和开发者生产力。

Airbnb 的迁移过程是渐进的。团队从转换代码库的关键组件开始，逐渐过渡到全面采用。这种方法最小化了干扰，让开发者在继续交付功能和更新的同时熟悉 TypeScript。在过渡期间，Airbnb 使用 TypeScript 与 `JavaScript` 的互操作性来确保迁移过程顺利高效。迁移后最显著的优点之一是类型错误显著减少。TypeScript 的静态类型系统在开发早期识别了许多问题，导致到达生产环境的 Bug 减少。这不仅提高了应用程序的整体稳定性，还提高了开发者体验，使得调试和排错变得更加高效。

## 第 2 章：使用基本类型

### 章节概述

构建强大且类型安全的应用程序依赖于对 TypeScript 核心数据类型的理解，这是本章的重点。我们首先查看基本类型：`number`、`string` 和 `boolean`。理解这些基本类型很重要，它们是任何 TypeScript 程序的 string，允许你有效地处理数值数据、文本信息和布尔逻辑。

接下来，我们将查看数组（arrays）和元组（tuples）。数组允许你存储多个相同类型的值，而元组可以存储固定数量的不同类型的元素。掌握这些数据结构将提高你在应用程序中管理和使用大量数据的能力。我们将查看 TypeScript 类型系统在安全和结构方面如何优于 `JavaScript`。之后，我们将查看枚举（enum）类型，它允许你定义一组命名常量。枚举通过为值集赋予有意义的名称提高了代码的可读性和维护性。

最后，我们将学习更高级的类型，如 `any`、`unknown` 和 `void`。这些类型在需要更大的活性或表示值缺失的情况下有用。

### 数字、字符串和布尔类型

从本章开始，我们将通过一个名为“Anna's Coaching”的现场项目学习 TypeScript 的所有概念。在本节中，我们将从包含基本类型开始：`number`、`string` 和 `boolean`。这些类型帮助我们管理数值数据、文本信息和布尔逻辑。

### 声明变量

使用 `let` 和 `const` 声明变量。

```typescript
let message: string = "Hello";
let count: number = 42;
let isAvailable: boolean = true;
```

### 数据类型

我们将探索 `any`、`unknown` 和 `void` 类型。

```typescript
let randomValue: any = 10;
let unknownValue: unknown = "Hello";
let result: void;
```

### 数组和元组

数组可以持有特定类型的多个值。元组允许存储具有固定数量元素的数组，其中每个元素可以是不同的类型。

```typescript
let scores: number[] = [90, 85, 88];
let user: [number, string] = [1, "John Doe"];
```

### 枚举

枚举提供了一种定义命名常量的方法。

```typescript
enum Color {
  Red,
  Green,
  Blue
}
let c: Color = Color.Green;

enum Status {
  Active = "Active",
  Inactive = "Inactive",
  Graduated = "Graduated"
}
```

## 第 3 章：TypeScript 中的函函数

### 章节概述

在本章中，我们将学习 TypeScript 函数，这是开发应用程序的重要部分。函数允许我们封装逻辑，使代码模块化和可重用。我们将从函数类型和签名开始。

### 函数类型

函数根据其声明和返回类型进行分类。我们将涵盖普通函数、函数表达式和箭头函数。

```typescript
function calculateGrade(score: number): string {
  // ...
  return "F";
}
```

### 函数表达式

函数表达式允许将函数赋值给变量。

```typescript
const greetStudent = function(name: string): string {
  return `Hello, ${name}! Welcome to Anna's Coaching.`;
};
```

### 箭头函数

箭头函数为编写函数提供了简洁的语法并自动绑定 `this` 上下文。

```typescript
const calculateCourseDuration = (hoursPerDay: number, totalHours: number): number => {
  return Math.ceil(totalHours / hoursPerDay);
};
```

### 函数重载

函数重载允许你为同一个函数名定义多个签名。

```typescript
function getStudentInfo(id: number): { id: number; name: string };
function getStudentInfo(name: string): string; 
```

## 第 4 章：复杂类型和联合类型

### 章节概述

在本章中，我们将查看联合类型和复杂类型，它们实现了更准确、灵活的数据建模。我们将从联合类型和交叉类型开始。

### 联合类型和交叉类型

联合类型允变量持有超过一种类型。它们使用管道符号 `|` 定义，代表逻辑上的“或”。

```typescript
type StudentID = number | string;
let studentId1: StudentID = 12345;
let studentId2: StudentID = "A1234";
```

### 交叉类型

交叉类型允许将多个类型合并为单一类型。它们使用符号 `&` 定义。

```typescript
type EnrolledStudent = Enrollment & Profile;
```

## 第 5 章：类和接口

### 章节概述

类和接口是 TypeScript 的主要面向对象特性。本章将帮助你理解如何结构和组织代码，使其模块化和可重用。

### 创建类

在 TypeScript 中，类使用 `class` 关键字定义。

```typescript
class Course {
  title: string;
  duration: number;
  displayCourseInfo() {
    console.log(`Course Title: ${this.title}`);
  }
}
```

### 类构造函数和方法

`constructor` 是一个用于从类创建对象的特殊方法。

```typescript
class Course {
  title: string;
  duration: number;
  constructor(title: string, duration: number) {
    this.title = title;
    this.duration = duration;
  }
}
```

### 公有、私有修饰符

修饰符控制类成员的可见性和访问权限。

- `public`: 随处可访问（默认）。

- `private`: 限制访问类本身。

- `protected`: 允许在类及其子类中访问。

### 接口实例

接口定义了类或对象必须遵守的契约。

```typescript
interface ICourseMember {
  id: number;
  name: string;
  displayRoleInfo(): void;
}
```

## 第 6 章：模块和命名空间

### 章节概述

在本章中，我们将进一步研究 TypeScript 的模块和命名空间概念。模块和命名空间提供了结构和封装。

### 使用命名空间

命名空间通过提供相关功能的逻辑分组来组织代码并避免命名冲突。

```typescript
namespace MathUtils {
  namespace Geometry {
    export function calculateCircleArea(radius: number): number {
      return Math.PI * radius * radius;
    }
  }
}
```

## 第 7 章：实践实践

### 章节概述

在这里查看 TypeScript 的几个真实世界用途，例如从 JavaScript 迁移到 TypeScript 以及将其与流行的前端框架和工具集成。

### 与 Angular 集成 TypeScript

`Angular` 是用于构建动态和健壮 Web 应用的流行框架。`Angular` 的关键特性之一是与 TypeScript 的集成。

## 欢迎来到 Anna 的 TS 培训！

<app-student-list></app-student-list> 当你重新加载应用时，`StudentListComponent` 将渲染并显示学生列表。

## 在 Angular 服务中使用 TypeScript

Angular 中的服务用于封装业务逻辑和共享用性。它们通常被用于管理数据、处理 HTTP 请求以及执行需要在组件间共享的操作。TypeScript 的特性（如接口 `interfaces` 和装饰器 `decorators`）增强了 Angular 服务的开发和组织。

### 创建一个 Angular 服务

要创建一个新的 Angular 服务，请使用 Angular CLI 的 `generate` 命令：

```bash
ng generate service student
```

此命令将在 `src/app/student/` 目录下生成一个名为 `StudentService` 的新服务。该服务由单个文件组成：

- 定义服务逻辑的 `TypeScript` 文件。

### 使用 TypeScript 定义服务

我们将探索生成的 `student.service.ts` 文件并添加一些逻辑：

```typescript
// student.service.ts
import { Injectable } from '@angular/core';
interface Student {
  id: number;
  name: string;
}
@Injectable({
  providedIn: 'root'
})
export class StudentService {
  private students: Student[] = [
    { id: 1, name: 'Liam' },
    { id: 2, name: 'Sophia' },
    { id: 3, name: 'Olivia' }
  ];
  constructor() {}
  getStudents(): Student[] {
    return this.students;
  }
  addStudent(student: Student): void {
    this.students.push(student);
  }
}
```

在上述代码中，我们定义了一个使用 `@Injectable` 装饰器装饰的 `StudentService` 类，表示该服务可以注入到其他组件和服务。`students` 数组被定义为 `private` 属性，将学生数据封装在服务内部。`Student` 接口定义了学生的形状，在处理学生数据时提供了类型安全。

`getStudents` 方法返回学生列表，而 `addStudent` 方法向数组中添加新学生。TypeScript 的静态类型和接口 `interfaces` 通过强制执行数据结构和方法的正确用法，增强了服务。

### 在 Angular 组件中使用服务

要在组件中使用 `StudentService`，请将其注入到组件的构造函数并使用其方法。

```typescript
// student-list.component.ts
import { Component, OnInit } from '@angular/core';
import { StudentService } from '../student/student.service';
@Component({
  selector: 'app-student-list',
  templateUrl: './student-list.component.html',
  styleUrls: ['./student-list.component.css']
})
export class StudentListComponent implements OnInit {
  students: { id: number; name: string; }[] = [];
  constructor(private studentService: StudentService) {}
  ngOnInit(): void {
    this.students = this.studentService.getStudents();
  }
  addStudent(id: number, name: string): void {
    this.studentService.addStudent({ id, name });
    this.students = this.studentService.getStudents(); // 刷新列表
  }
}
```

在上述代码中，`StudentService` 通过构造函数注入到 `StudentListComponent`，允许组件访问服务的方法。`ngOnInit` 生命周期钩子通过通过服务的服务的 `getStudents` 来初始化 `students` 数组。`addStudent` 方法使用服务添加新学生，并通过获取更新的学生数据来刷新列表。

## 将 TypeScript 与 Angular 特性集成

Angular 丰富的生态系统提供了与 TypeScript 无缝集成的各种特性，增强了开发过程和代码质量。

### 在 Angular 指令中的 TypeScript

Angular 指令是为 DOM 元素添加行为的类。TypeScript 的类型注解和装饰器 `decorators` 增强了指令的创建和管理。

```typescript
// highlight.directive.ts
import { Directive, ElementRef, Renderer2, HostListener } from '@angular/core';
@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
  constructor(private el: ElementRef, private renderer: Renderer2) {}
  @HostListener('mouseenter') onMouseEnter() {
    this.renderer.setStyle(this.el.nativeElement, 'background-color', 'yellow');
  }
  @HostListener('mouseleave') onMouseLeave() {
    this.renderer.setStyle(this.el.nativeElement, 'background-color', 'transparent');
  }
}
```

在上述代码中，我们定义了一个 `HighlightDirective`，当鼠标进入和离开元素时更改元素的背景颜色。该指令使用 `@Directive` 装饰器指定其选择器，并使用 TypeScript 的类型注解来管理如 `ElementRef` 等依赖。`@HostListener` 装饰器用于将方法绑定到 DOM 事件。

### 在 Angular 管道中使用 TypeScript

Angular 中的管道（Pipes）在数据显示于视图之前对其进行转换。TypeScript 通过提供类型安全和改进的工具支持来增强管道 `pipes`。

```typescript
// capitalize.pipe.ts
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({
  name: 'capitalize'
})
export class CapitalizePipe implements PipeTransform {
  transform(value: string): string {
    if (!value) return '';
    return value.charAt(0).toUpperCase() + value.slice(1).toLowerCase();
  }
}
```

在上述代码中，我们定义了一个 `CapitalizePipe` 将字符串的首字母大写。管道使用 `@Pipe` 装饰器指定其名称并实现 `PipeTransform`。

## 在 React 中使用 TypeScript

React 是用于构建用户界面的流行 JavaScript 库。TypeScript 通过提供类型安全和改进的工具支持来增强 React。

### 在 React 组件中使用 TypeScript

我们将通过一个名为“Anna's TS Training”的现场项目学习 TypeScript 的所有概念。在本节中，我们将使用 TypeScript 接口（interfaces）来定义学生对象的形状以及组件期望的 props。使用 `useState` hook 来管理学生列表，而 TypeScript 确保了状态和相关函数遵循定义的类型。

```typescript
// src/components/StudentList.tsx
import React from 'react';
// 使用 interface 定义学生对象的形状
interface Student {
  id: number;
  name: string;
}
// 为组件定义 props 接口
interface StudentListProps {
  initialStudents: Student[];
}
const StudentList: React.FC<StudentListProps> = ({ initialStudents }) => {
  const [students, setStudents] = useState<Student[]>(initialStudents);
  const addStudent = (id: number, name: string) => {
    setStudents([...students, { id, name }]);
  };
  const removeStudent = (id: number) => {
    setStudents(students.filter(student => student.id !== id));
  };
  return (
    <div>
      {students.map(student => (
        <div key={student.id}>
          {student.name}
        </div>
      ))}
    </div>
  );
};
export default StudentList;
```

在上面的代码中，我们使用 `React.FC` 类型定义了一个 `StudentList` 组件，以表示这是一个函数组件。我们使用 TypeScript 接口（interfaces）来定义学生对象的形状以及组件期望的 props。使用 `useState` hook 来管理学生列表，而 TypeScript 确保了状态和相关函数遵循定义的类型。

## 在应用程序中使用组件

将 `StudentList` 组件添加到 `App.tsx` 文件中：

```typescript
// src/App.tsx
import React from 'react';
import StudentList from './components/StudentList';
// Initial 学生数据
const initialStudents = [
  { id: 1, name: 'Liam' },
  { id: 2, name: 'Sophia' },
  { id: 3, name: 'Olivia' }
];
const App: React.FC = () => {
  return (
    <StudentList initialStudents={initialStudents} />
  );
};
export default App;
```

在上面的代码中，`App` 组件导入并使用了 `StudentList` 组件，并将 `initialStudents` 数组作为 prop 传递。TypeScript 确保了 prop 类型匹配预期的形状，提供了类型安全并提升了开发体验。

## 在 React Hooks 中利用 TypeScript

React hooks 是允许你在函数组件中使用状态和生命周期特函数。TypeScript 通过提供类型安全和清晰度增强了 hooks。

### 在 useState Hook 中使用 TypeScript

我们已经已经在 `StudentList` 组件中看到了结合 TypeScript 使用 `useState` hook 的示例。我们将通过创建一个自定义 hook 来管理学生数据，进一步探索 TypeScript 如何与 hooks 配合。为此，我们先创建一个新的 hook 文件：`useStudentManager.ts`。

```typescript
// src/hooks/useStudentManager.ts
import { useState } from 'react';
// 使用 interface 定义学生对象的形状
interface Student {
  id: number;
  name: string;
}
export const useStudentManager = (initialStudents: Student[]) => {
  const [students, setStudents] = useState<Student[]>(initialStudents);
  const addStudent = (name: string) => {
    const newStudent: Student = { id: students.length + 1, name };
    setStudents([...students, newStudent]);
  };
  const removeStudent = (id: number) => {
    setStudents(students.filter(student => student.id !== id));
  };
  return { students, addStudent, removeStudent };
};
```

在上面的代码中，`useStudentManager` hook 管理一个学生列表，提供了添加和删除学生的函数。TypeScript 确保了 hook 的状态和函数类型正确，增强了代码的可靠性。

### 在组件中使用自定义 Hook

更新 `StudentList` 组件以使用 `useStudentManager` hook：

```typescript
// src/components/StudentList.tsx
import React from 'react';
import { useStudentManager } from '../hooks/useStudentManager';
// 使用 interface 定义学生对象的形状
interface Student {
  id: number;
  name: string;
}
// 为组件定义 props 接口
interface StudentListProps {
  initialStudents: Student[];
}
const StudentList: React.FC = ({ initialStudents }) => {
  const { students, addStudent, removeStudent } = useStudentManager(initialStudents);
  return (
    <div>
      {students.map(student => (
        <div key={student.id}>
          {student.name}
        </div>
      ))}
    </div>
  );
};
export default StudentList;
```

在这个更新后的示例中，`StudentList` 组件使用 `useStudentManager` hook 来管理学生数据。该 hook 提供了添加和删除学生所需的状态和函数，展示了 TypeScript 如何通过类型安全增强 hooks。

## 在 React Context 中利用 TypeScript

React Context 提供了一种在组件树中透传数据的方法，而无需在每一层手动传递 props。TypeScript 可以通过为管理的数据和函数提供清晰的类型来增强 Context。

### 使用 TypeScript 创建 Context

我们将创建一个新的 context 文件 `ThemeContext.tsx` 来管理应用的主题（theme）。

```typescript
// src/context/ThemeContext.tsx
import React, { createContext, useContext, useState } from 'react';
// 定义主题上下数据的形状
interface ThemeContextType {
  theme: string;
  toggleTheme: () => void;
}
// 创建带有初始值的 context
const ThemeContext = createContext<ThemeContextType | undefined>(undefined);

export const ThemeProvider: React.FC<{ children: React.ReactNode }> = ({ children }) => {
  const [theme, setTheme] = useState<string>('light');
  const toggleTheme = () => {
    setTheme(prevTheme => (prevTheme === 'light' ? 'dark' : 'light'));
  };
  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};

// 使用 ThemeContext 的自定义 hook
export const useTheme = ThemeContextType => {
  const context = useContext(ThemeContext);
  if (!context) {
    throw new Error('useTheme must be used within a ThemeProvider');
  }
  return context;
};
```

在上面的代码中，我们定义了一个包含主题状态和 `toggleTheme` 函数的 `ThemeContext`。`ThemeProvider` 组件包裹了应用程序，为其子组件提供了主题上下文。`useTheme` hook 提供了一种访问主题上下文的便捷方式，确保其被正确使用。

### 在组件中使用 Context

更新 `App` 组件以使用：

```tsx
// src/App.tsx
import React from 'react';
import { ThemeProvider } from './context/ThemeContext';
import { useTheme } from './context/ThemeContext';
import StudentList from './components/StudentList';
// Initial 学生数据
const initialStudents = [
  { id: 1, name: 'Liam' },
  { id: 2, name: 'Sophia' },
  { id: 3, name: 'Olivia' }
];
const App: React.FC = () => {
  const { theme, toggleTheme } = useTheme();
  return (
    <ThemeProvider>
      <div>
        <button onClick={toggleTheme}>Toggle Theme</button>
        <StudentList initialStudents={initialStudents} />
      </div>
    </ThemeProvider>
  );
};
export default App;
```

在上述代码中，`App` 组件封装了它的子组件，使得主题上下文（theme context）对 `ThemeToggleButton` 组件可用。`ThemeToggleButton` 使用 `useTheme` 钩子来访问并切换主题，展示了 `TypeScript` 和 `React Context` 如何协作来管理应用范围的状态。

## 将 JavaScript 应用迁移到 TypeScript

将 JavaScript 应用程序迁移到 TypeScript 可以带来许多好处，包括提高代码质量、提供更好的工具支持以及增强可维护性。然而，迁移过程需要仔细的规划和执行，以确保平稳过渡。在本主题中，我们将概述一个经过验证的逐步流程，用于将 JavaScript 应用迁移到 TypeScript，并为迁移过程中可能出现的常见问题提供排错建议。

## 迁移过程

将 JavaScript 应用程序迁移到 TypeScript 涉及多个阶段，从在项目中设置 TypeScript 到逐渐转换 JavaScript 文件。下面是一个分步的实践操作指南，旨在帮助你完成这一过程。

### 准备项目

在开始迁移之前，确保你的项目处于稳定状态，并且你已经有了完整的备份。这一预防措施将帮助你在需要时恢复到原始代码。

* 确保你的项目依赖是最新的。

* 移除任何未使用的或已弃的库。

* 解决现有的 bug 或问题。

### 安装 TypeScript

使用 `npm` 或 `yarn` 将 TypeScript 作为开发依赖添加到你的项目中。

#### 使用 npm

```bash
npm install --save-dev typescript
```

#### 使用 yarn

```bash
yarn add --dev typescript
```

### 初始化 TypeScript 配置

在项目根目录中创建一个 `tsconfig.json` 文件来配置 TypeScript 设置。

```bash
npx tsc --init
```

此命令生成一个默认的 `tsconfig.json` 文件，你可以根据项目需求进行自定义。需要考虑的关键配置：

* 指定 JavaScript 版本（例如 `ES6`）。

* 定义模块系统（例如 `"commonjs"` 或 `"ESNext"`）。

* 启用严格类型检查选项以获得更好的类型安全。

* 定义要包含的文件或目录（例如 `"src"`）。

* 定义要排除的文件或目录（例如 `"node"`）。

### 重命名 JavaScript 文件

通过将文件后缀从 `.js` 改为 `.ts` 开始迁移文件。从简单的、隔离的文件开始，以尽量减少潜在问题。

```bash
mv src/example.js src/example.ts
```

`TypeScript` 可以编译 JavaScript 文件，因此你可以增量重命名，确保应用继续运行。

### 启用类型检查

运行 TypeScript 编译器以对重命名后的文件启用类型检查。

```bash
npx tsc
```

TypeScript 编译器将报告任何类型错误或问题，允许你在继续之前解决它们。

### 添加类型注解

逐渐为你的 TypeScript 文件添加类型注解，以提高类型安全性和代码可读性。

* 为函数参数和返回类型添加注解。

* 为复杂数据结构定义 `interfaces` 或类型别名。

* 使用 `TypeScript` 的内置类型，如 `string` 和 `number`。

查看以下示例以理解如何添加类型注解：

```typescript
// 迁移前 (JavaScript)
function greet(name) {
  return "Hello, " + name;
}

// 迁移后 (TypeScript)
function greet(name: string): string {
  return "Hello, " + name;
}
```

### 迁移复杂文件

继续处理带有类（classes）、`interfaces` 或外部依赖的更复杂的文件。逐渐将 JavaScript 特有的结构替换为 TypeScript 的等效物。查看以下代码以理解如何迁移类。

```typescript
// 迁移前 (JavaScript)
class Person {
  constructor(name) {
    this.name = name;
  }
  sayHello() {
    console.log(`Hello, my name is ${this.name}`);
  }
}

// 迁移后 (TypeScript)
class Person {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  sayHello(): void {
    console.log(`Hello, my name is ${this.name}`);
  }
}
```

### 处理第三方库

对于缺少 TypeScript 定义的第三方库，你可以从 `DefinitelyTyped` 安装类型定义或创建你自己的类型声明。

#### 为库安装类型定义

```bash
npm install --save-dev @types/library-name
```

如果没有可用的类型定义，你可以创建一个 `.d.ts` 文件来定义自己的。

```typescript
// custom-types.d.ts
declare module 'library-name' {
  export function someFunction(param: string): void;
}
```

### 更新项目配置

一旦迁移完成，更新构建脚本、检查器（linters）和 IDE 设置以确保它们支持 TypeScript。

* 更新 `package.json` 脚本使用 `tsc` 进行编译。

* 配置如 `ESLint` 等检查器以与 `TypeScript` 工作。

* 确保你的 IDE 已配置好处理 TypeScript 文件。

## 常见迁移问题排错

尽管经过了仔细规划，你可能在迁移过程中遇到挑战。以下是一些常见问题及其解决方案：

### 编译错误

认为 `typeScript` 编译失败并带有错误。现在，为了解决这个问题，我们将通过完善类型注解、修复类型不匹配或解决依赖来处理每个错误。

以下是类型不匹配（Type Mismatch）的示例错误：

```typescript
// Error: 类型 'number' 无法赋值给类型 'string'。
let name: string = 1;
```
