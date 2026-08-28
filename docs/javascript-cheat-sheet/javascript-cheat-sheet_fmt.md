
# JavaScript 速查表

## 方法

### DOM 方法

### JavaScript

**Object**

- `toString()`
- `toLocaleString()`
- `valueOf()`
- `hasOwnProperty()`
- `isPrototypeOf()`
- `propertyIsEnumerable()`

**String**

- `charAt()`
- `charCodeAt()`
- `fromCharCode()`
- `concat()`
- `indexOf()`
- `lastIndexOf()`
- `localeCompare()`
- `match()`
- `replace()`
- `search()`
- `slice()`
- `split()`
- `substring()`
- `substr()`
- `toLowerCase()`
- `toUpperCase()`
- `toLocaleLowerCase()`
- `toLocaleUpperCase()`

**RegExp**

- `test()`
- `match()`
- `exec()`

**Array**

- `concat()`
- `join()`
- `push()`
- `pop()`
- `reverse()`
- `shift()`
- `slice()`
- `sort()`
- `splice()`
- `unshift()`

**Number**

- `toFixed()`
- `toExponential()`
- `toPrecision()`

**Date**

- `parse()`
- `toDateString()`
- `toTimeString()`
- `getDate()`
- `getDay()`
- `getFullYear()`
- `getHours()`
- `getMilliseconds()`
- `getMinutes()`
- `getMonth()`
- `getSeconds()`
- `getTime()`
- `getTimezoneOffset()`
- `getYear()`
- `setDate()`
- `setHours()`
- `setMilliseconds()`
- `setMinutes()`
- `setMonth()`
- `setSeconds()`
- `setYear()`
- `toLocaleTimeString()`

### XMLHttpRequest

```javascript
// Safari, Mozilla, Opera:
var req = new XMLHttpRequest();

// Internet Explorer:
var req = new ActiveXObject("Microsoft.XMLHTTP");
```

### 正则表达式 - 格式

JavaScript 中的正则表达式形式如下：

```javascript
var RegEx = /pattern/modifiers;
```

### 正则表达式 - 修饰符

| 修饰符 | 说明 |
|--------|------|
| `/g`   | 全局匹配 |
| `/i`   | 不区分大小写 |
| `/s`   | 单行模式 |
| `/m`   | 多行模式 |

### XMLHttpRequest 对象方法

- `abort()`
- `getAllResponseHeaders()`
- `getResponseHeader(header)`
- `open(method, URL)`
- `send(body)`
- `setRequestHeader(header, value)`

### 正则表达式 - 模式

| 模式 | 说明 |
|------|------|
| `^`  | 字符串开头 |
| `$`  | 字符串结尾 |
| `.`  | 任意单个字符 |
| `(a\|b)` | a 或 b |
| `(...)` | 分组 |
| `[abc]` | 范围内的项（a 或 b 或 c） |
| `[^abc]` | 不在范围内（不是 a 或 b 或 c） |
| `a?` | 零个或一个 a |
| `a*` | 零个或多个 a |
| `a+` | 一个或多个 a |
| `a{3}` | 恰好 3 个 a |
| `a{3,}` | 3 个或更多 a |
| `a{3,6}` | 3 到 6 个 a |
| `!(pattern)` | "非"前缀。当 URL 不匹配模式时应用规则。 |

### XMLHttpRequest 对象属性

- `onreadystatechange`
- `readyState`
- `responseText`
- `responseXML`
- `status`
- `statusText`

### XMLHttpRequest readyState 值

| 值 | 说明 |
|----|------|
| 0  | 未初始化 |
| 1  | 加载中 |
| 2  | 已加载 |
| 3  | 交互中 |
| 4  | 完成 |

### HTML 中的 JAVASCRIPT

```html
<!-- 外部 JavaScript 文件 -->
<script type="text/javascript" src="javascript.js"></script>

<!-- 内联 JavaScript -->
<script type="text/javascript">
<!--
// JavaScript 代码
//-->
</script>
```

### 事件处理器

- `onAbort`
- `onBlur`
- `onChange`
- `onClick`
- `onDblClick`
- `onDragDrop`
- `onError`
- `onFocus`
- `onKeyDown`
- `onKeyPress`
- `onKeyUp`
- `onLoad`
- `onMouseDown`
- `onMouseMove`
- `onMouseOut`
- `onMouseOver`
- `onMouseUp`
- `onMove`
- `onReset`
- `onResize`
- `onSelect`
- `onSubmit`
- `onUnload`

### DOM 方法（续）

**Document**

- `clear()`
- `createDocument()`
- `createDocumentFragment()`
- `createElement()`
- `createEvent()`
- `createEventObject()`
- `createRange()`
- `createTextNode()`
- `getElementsByTagName()`
- `getElementById()`
- `write()`

**Node**

- `addEventListener()`
- `appendChild()`
- `attachEvent()`
- `cloneNode()`
- `createTextRange()`
- `detachEvent()`
- `dispatchEvent()`
- `fireEvent()`
- `getAttributeNS()`
- `getAttributeNode()`
- `hasChildNodes()`
- `hasAttribute()`
- `hasAttributes()`
- `insertBefore()`
- `removeChild()`
- `removeEventListener()`
- `replaceChild()`
- `scrollIntoView()`

**Form**

- `submit()`

**DOM 集合**

- `item()`

**Range**

- `collapse()`
- `createContextualFragment()`
- `moveEnd()`
- `moveStart()`
- `parentElement()`
- `select()`
- `setStartBefore()`

**Style**

- `getPropertyValue()`
- `setProperty()`

**Event**

- `initEvent()`
- `preventDefault()`
- `stopPropagation()`

**XMLSerializer**

- `serializeToString()`

**XMLHTTP**

- `open()`
- `send()`

**XMLDOM**

- `loadXML()`

**DOMParser**

- `parseFromString()`

### 函数

| Window | 内置函数 |
|--------|----------|
| `alert()` | `eval()` |
| `blur()` | `parseInt()` |
| `clearTimeout()` | `parseFloat()` |
| `isNaN()` |  |
| `isFinite()` |  |
| `close()` |  |
| `focus()` | `decodeURI()` |
| `open()` | `decodeURIComponent()` |
| `print()` | `encodeURI()` |
| `setTimeout()` | `encodeURIComponent()` |
| `escape()` |  |
| `unescape()` |  |

### 函数与方法

方法是与对象相关联的一种函数。普通函数不与对象相关联。

免费提供自 AddedBytes.com
