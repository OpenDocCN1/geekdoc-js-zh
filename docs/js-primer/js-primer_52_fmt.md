
# 实现添加 Todo 项目的功能

> 原文：[`jsprimer.net/use-case/todoapp/form-event/`](https://jsprimer.net/use-case/todoapp/form-event/)

接下来，我们将使用 JavaScript 创建 Todo 应用程序的功能。

在这一节中，将实现在前一节中已标记了的 Todo 列表（`#js-todo-list`）上添加 Todo 项目的功能。

## 添加 Todo 项目

首先，我们将看看在 Todo 应用程序中，执行哪些操作会添加 Todo 项目。

在 Todo 应用程序中，当用户执行以下操作时，将添加 Todo 项目。

1. 在输入框中输入 Todo 项目的标题
1. 通过在输入框中按 Enter 键提交
1. 将 Todo 项目添加到 Todo 列表中

要实现这一点，需要：

+ 为了获取 Todo 项目的标题，需要从 `input` 元素（输入框）中获取内容
+ 为了知道已使用 Enter 键进行了提交，需要监视 `form` 元素的 `submit` 事件（提交）
+ 创建以输入内容为标题的 Todo 项目，并将 Todo 项目元素添加到 Todo 列表（`#js-todo-list`）中

首先，从表单元素接收提交事件，并尝试在控制台日志中显示输入内容。

## 将输入内容显示在控制台中

当在表单元素中按下 Enter 键进行提交时，将触发 `submit` 事件。可以使用 HTML 元素的 `addEventListener` 方法来接收此 `submit` 事件。

下面的代码注册了一个回调函数，当指定的表单元素触发 `submit` 事件时调用。

```javascript
// `id="js-form"`の要素を取得
const formElement = document.querySelector("#js-form");
// form 要素から発生したsubmitイベントを受け取る
formElement.addEventListener("submit", (event) => {
    // イベントが発生したときに呼ばれるコールバック関数（イベントリスナー）
});
```

当发生这样的事件时，被调用的回调函数称为**事件监听器**（监听事件的东西）。另外，事件监听器有时也称为事件处理程序，但在本书中，这两个词语具有相同的含义。

要在表单提交时将输入内容显示在控制台中，只需在 `addEventListener` 回调函数内使用 Console API 输出输入内容即可。

可以从 `input` 元素的 `value` 属性中获取输入内容。

```javascript
const inputElement = document.querySelector("#js-form-input");
console.log(inputElement.value); // => "input 要素の入力内容"
```

将这些组合起来，实现在 `App.js` 中将输入内容显示在控制台的功能。定义一个名为 `mount` 的方法，并在其中编写处理逻辑。

下面的代码注册了一个回调函数，当表单（`#js-form`）按 Enter 键提交时，将 `input` 元素（`#js-form-input`）的内容显示在控制台上。

src/App.js

```javascript
export class App {
    mount() {
        const formElement = document.querySelector("#js-form");
        const inputElement = document.querySelector("#js-form-input");
        formElement.addEventListener("submit", (event) => {
            // submitイベントの本来の動作を止める
            event.preventDefault();
            console.log(`入力欄の値: ${inputElement.value}`);
        });
    }
}
```

由于此时尚未调用 App 的 `mount` 方法，因此不会执行任何操作。因此，还需要更改 `index.js` 以调用 `App` 类的 `mount` 方法。

index.js

```javascript
import { App } from "./src/App.js";
const app = new App();
app.mount();
```

在进行这些更改后，刷新页面，将执行 App 的 `mount` 方法。因为已经监听了 `submit` 事件，所以尝试在输入框中输入内容并按 Enter 键提交，该内容将显示在控制台中。

![输入内容在控制台中显示](img/4136a4c8ddc2954ea1cb3c3881e4e949.png)

在上述 App 的 `mount` 方法中，调用了 `event.preventDefault` 方法来取消 `submit` 事件的默认行为。`event.preventDefault` 方法用于取消表单所在的默认操作。

表单的默认行为是将表单内容提交到指定的 URL。由于在这里没有为 `form` 元素指定目标，因此将表单内容提交到当前 URL。但是，由于这种行为会干扰，因此调用 `event.preventDefault` 方法来取消此默认行为。

摘自 src/App.js

```javascript
formElement.addEventListener("submit", (event) => {
    // submitイベントの本来の動作を止める
    event.preventDefault();
    console.log(`入力欄の値: ${inputElement.value}`);
});
```

当表单提交到当前 URL 时，页面将被重新加载。因此，调用了 `event.preventDefault()` 来取消默认行为。如果取消注释 `event.preventDefault()`，则可以确认页面将被重新加载。

示例中摘自 src/App.js 的部分

```javascript
formElement.addEventListener("submit", (event) => {
    // preventDefaultしないとページがリロードされてしまう
    // event.preventDefault();
    console.log(`入力欄の値: ${inputElement.value}`);
});
```

已经在 `todoapp` 目录下做出如下更改。

```
todoapp
├── index.html
├── index.js (Appクラスのmountメソッドの呼び出し)
└── src
    └── App.js (Appクラスのmountメソッドの実装)
```

可以在以下 URL 中查看到此 Todo 应用程序。

+ [`jsprimer.net/use-case/todoapp/form-event/prevent-event/`](https://jsprimer.net/use-case/todoapp/form-event/prevent-event/)

## 将输入内容显示在 Todo 列表中

已经了解到如何获取表单提交时的输入内容，接下来将在 Todo 列表（`#js-todo-list`）中显示这些输入内容。

在 HTML 中，要描述列表项，需要使用 `<li>` 标签。另外，希望包含有表示完成状态的复选框和删除按钮等的 Todo 项目元素。由于从 DOM API 以程序方式创建这些元素会使代码难以阅读，因此创建一个从 HTML 字符串生成 HTML 元素的实用程序模块。

将名为 `html-util.js` 的文件创建在路径 `src/view/html-util.js` 下。

此 `html-util.js` 基于在「ajaxapp: 将 HTML 字符串添加到 DOM」中使用的 `escapeSpecialChars`。在 ajaxapp 中，`escapeHTML` 函数的输出是**HTML 字符串**，而本次创建的 `element` 函数的输出是**HTML 元素**（Element）。

Todoリスト（`#js-todo-list`）というすでに存在する要素に対して要素を**追加**するには、HTML 文字列ではなくHTML 要素が必要になります。また、HTML 文字列に対しては`addEventListener`でイベントをリッスンできません。そのため、チェックボックスの状態が変わったことや削除ボタンが押されたことを知る必要があるTodoアプリではHTML 要素が必要になります。

src/view/html-util.js

```javascript
export function escapeSpecialChars(str) {
    return str
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");
}

/**
 * HTML 文字列からHTML 要素を作成して返す
 * @param {string} html
 */
export function htmlToElement(html) {
    const template = document.createElement("template");
    template.innerHTML = html;
    return template.content.firstElementChild;
}

/**
 * HTML 文字列からDOM Nodeを作成して返すタグ関数
 * @return {Element}
 */
export function element(strings, ...values) {
    const htmlString = strings.reduce((result, str, i) => {
        const value = values[i - 1];
        if (typeof value === "string") {
            return result + escapeSpecialChars(value) + str;
        } else {
            return result + String(value) + str;
        }
    });
    return htmlToElement(htmlString);
}

/**
 * コンテナ要素の中身をbodyElementで上書きする
 * @param {Element} bodyElement コンテナ要素の中身となる要素
 * @param {Element} containerElement コンテナ要素
 */
export function render(bodyElement, containerElement) {
    // containerElementの中身を空にする
    containerElement.innerHTML = "";
    // containerElementの直下にbodyElementを追加する
    containerElement.appendChild(bodyElement);
}
```

`element` 标签函数中，使用了同一文件中定义的 `htmlToElement` 函数从 HTML 字符串创建 HTML 元素。`htmlToElement` 函数中利用的 [template 元素](https://developer.mozilla.org/ja/docs/Web/HTML/Element/template) 是 HTML5 新增的、可从 HTML 字符串片段创建 HTML 元素的元素。

使用此 `element` 标签函数，可以像下面这样从 HTML 字符串创建 HTML 元素。创建的元素可使用 `appendChild` 方法等作为子元素添加到现有元素中。

element 标签函数的示例代码

```javascript
import { element } from "./html-util.js";
// 从 HTML 字符串创建 HTML 元素
const newElement = element`<ul>
    <li>新しい要素</li>
</ul>`;
// 将创建的元素作为子元素添加（appendChild）到 `document.body`
document.body.appendChild(newElement);
```

浏览器提供的 `appendChild` 方法仅用于添加子元素，因此如果已存在其他元素，则会添加到末尾。

`render` 函数是用指定的容器元素（父元素）的子元素进行覆盖的函数。其行为是先清空所有子元素，然后通过 `appendChild` 作为子元素添加。

render 函数的示例代码

```javascript
import { element, render } from "./html-util.js";
// render 之前，将元素添加到 document.body
const oldElement = element`<ul>
    <li>既存の要素</li>
</ul>`;
document.body.appendChild(oldElement);
// 创建新元素
const newElement = element`<ul>
    <li>新しい要素</li>
</ul>`;
// 将 `newElement` 作为 `document.body` 的子元素添加
// `document.body` 下已有的元素将被覆盖
render(newElement, document.body);
```

实际上，使用此 `element` 标签函数和 `render` 函数，将从表单发送的输入内容作为元素添加到 Todo 列表中。

首先，从 `App.js` 导入刚才创建的 `html-util.js` 的 `element` 标签函数和 `render` 函数。接下来，将汇总 Todo 项目的列表定义为 `todoListElement`，将显示的 Todo 项目数量定义为 `todoItemCount`。

在 `submit` 事件的监听器函数中，基于输入的内容更新 Todo 列表和 Todo 项目数量的显示。创建表示 Todo 项目的元素，将其作为子元素添加（`appendChild`）到 Todo 列表，并使用 `render` 函数用 Todo 列表覆盖容器元素的内容。最后将 Todo 项目数量加 1，并更新 Todo 项目数量（`#js-todo-count`）的文本（`textContent`）。

src/App.js

```javascript
import { element, render } from "./view/html-util.js";

export class App {
    mount() {
        const formElement = document.querySelector("#js-form");
        const inputElement = document.querySelector("#js-form-input");
        const containerElement = document.querySelector("#js-todo-list");
        const todoItemCountElement = document.querySelector("#js-todo-count");
        // 汇总 Todo 列表的 List 元素
        const todoListElement = element`<ul></ul>`;
        // Todo 项目数量
        let todoItemCount = 0;
        formElement.addEventListener("submit", (event) => {
            // 停止本来的 submit 事件行为
            event.preventDefault();
            // 创建要添加的 Todo 项目元素 (li 元素)
            const todoItemElement = element`<li>${inputElement.value}</li>`;
            // 将 Todo 项目添加到 todoListElement
            todoListElement.appendChild(todoItemElement);
            // 用汇总 Todo 列表的 List 元素覆盖容器元素的内容
            render(todoListElement, containerElement);
            // Todo 项目数量 +1，更新显示的文本
            todoItemCount += 1;
            todoItemCountElement.textContent = `Todoアイテム数: ${todoItemCount}`;
            // 将输入框重置为空字符串
            inputElement.value = "";
        });
    }
}
```

进行这些更改后，在浏览器中重新加载页面，在表单中输入内容并按 Enter 键，**Todo 项目将被添加**到 Todo 列表中。此外，每次发送输入内容时，`todoItemCount` 都会递增，**Todo 项目数量**的显示也会更新。

![Todo列表へアイテムを追加](img/58a9588c28aa0887c5a618769da1c5fa.png)

本节的更改如下。

```
todoapp
├── index.html
├── index.js
└── src
    ├── App.js (Todoアイテムの表示の実装)
    └── view
        └── html-util.js (新規追加)
```

到目前为止的 Todo 应用可以在以下 URL 确认。

+ [`jsprimer.net/use-case/todoapp/form-event/add-todo-item/`](https://jsprimer.net/use-case/todoapp/form-event/add-todo-item/)

## 总结

本节监听了 `form` 元素的 `submit` 事件，基于输入内容创建 Todo 项目，并实现了将其添加到 Todo 列表的功能。像这次的 Todo 项目添加一样，许多 Web 应用都是监听某种事件并更新显示。这种基于事件发生来推进处理的方法称为**事件驱动**（事件ドリブン）。

在本次 Todo 项目添加中，采用了以 `submit` 事件为输入，直接将 Todo 列表元素**作为 HTML 元素添加**的方法。这种直接更新 DOM 的方法代码量虽少，但存在状态仅保留在 DOM 中、灵活性降低的问题。下一节将介绍实际发生的问题及其解决机制。

## 本节的核对清单

+ 通过 `submit` 事件接收表单提交，并确认了输入内容
+ 实现了从 HTML 字符串创建 HTML 元素的 `html-util.js`
+ 从表单添加了 Todo 项目
+ 根据 Todo 项目的添加更新了 Todo 项目数量

在本节中，实现了向 Todo 应用添加 Todo 项目的功能。

+ 可以添加 Todo 项目

待在 Todo 应用中实现的剩余功能如下。

+ 可以更新 Todo 项目的完成状态
+ 可以删除 Todo 项目
