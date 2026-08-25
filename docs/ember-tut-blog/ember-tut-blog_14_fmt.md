

# Ember.js 入门指南之十二：Handlebars 属性绑定

简单讲，属性绑定其实就是在 HTML 标签内（即在一个标签的“<”和“>”中）直接使用`Handlebars`表达式。可以直接用`Handlebars`表达式的值作为 HTML 标签中某个属性的值。

准备工作：

```bash
ember generate route binding-element-attributes
```

## 1. 绑定字符串

```js
<!-- // app/templates/binding-element-attribute.hbs -->

<div id="logo">
    <img src={{model.imgUrl}} alt="logo" />
</div>
```

在对应的`route:binding-element-attributes`里增加测试数据。

```js
import Ember from 'ember';

export default Ember.Route.extend({
    model: function() {
        return { imgUrl: 'http://i1.tietuku.com/1f73778ea702c725.jpg' };
    }
});
```

运行之后，模板会编译成如下代码：

```html
<div id="logo">
    <img alt="logo" src="http://i1.tietuku.com/1f73778ea702c725.jpg">
</div>
```

可以看到`{{model.imgUrl}}`会以字符串的形式绑定到`src`属性上。

## 2. 绑定 Boolean 值

在开发过程中，我们经常会根据某个值判断是否给某个标签增加 CSS 类，或者根据某个值决定按钮是否可用等等……那么`Ember`是怎么做的呢？比如下面的代码演示的是`checkbox`按钮根据绑定的属性`isEnable`的值决定是否可用。

```handlebars
{{! 当 isEnable 为 true 时候，disabled 为 true，不可用；否则可用}}
<input type="checkbox" disabled={{model.isEnable}}>
```

如果在`route`里设置的值是`true`，那么渲染之后的 HTML 如下：

```html
<input type="checkbox" disabled="">
```

否则：

```html
<input type="checkbox">
```

## 3. 绑定`data-xxx`属性

默认情况下，`Ember`不会绑定到`data-xxx`这一类属性上。比如下面的绑定结果就得不到你的预期。

```handlebars
{{! 绑定到 data-xxx 这种属性需要特殊设置}}
{{#link-to "photo" data-toggle="dropdown"}}link-to{{/link-to}}
{{input type="text" data-toggle="tooltip" data-placement="bottom" title="Name"}}
```

模板渲染之后得到下面的 HTML 代码：

```html
<a id="ember455" href="/binding-element-attributes" class="ember-view active">link-to</a>
<input id="ember470" title="Name" type="text" class="ember-view ember-text-field">
```

可以看到`data-xxx`的属性都不见了！现在很多前端框架都会用到`data-xxx`这个属性，比如`Bootstrap`。那怎么办呢？你可以在`view`中指定对应的渲染组件`Ember.LinkComponent`和`Ember.TextField`（个人理解的）。

执行命令得到`view`文件：

```bash
ember generate view binding-element-attributes
```

在`view`中手动绑定，如下：

```js
// app/views/binding-element-attributes.js

import Ember from 'ember';

export default Ember.View.extend({
});

// 下面是官方给的代码，但很明显可以看出来这种使用方式不是 2.0 版本的！
// 2.0 版本的写法还在学习中，后续再补上。现在为了演示模板效果暂时这么写！
// 毕竟本文的重点还是在模板属性的绑定上。

// 绑定 input
Ember.TextField.reopen({
    attributeBindings: ['data-toggle', 'data-placement']
});

// 绑定 link-to
Ember.LinkComponent.reopen({
    attributeBindings: ['data-toggle']
});
```

渲染之后得到的结果符合预期，得到如下 HTML 代码：

```html
<a id="ember398" href="/binding-element-attributes" data-toggle="dropdown" class="ember-view active">link-to</a>
<input id="ember414" title="Name" type="text" data-toggle="tooltip" data-placement="bottom" class="ember-view ember-text-field">
```

可以看到`data-xxx`的属性正常渲染到 HTML 上了。

本文介绍了几个常用的属性绑定方式，非常实用！但是有点遗憾，本人能力有限，还没理解到最后一个实例在`Ember 2.0`版中是怎么使用的。现在的代码是根据个人理解，把指定组件的代码放在`view`中；官方教程给的也不是`Ember 2.0`版的，所以`binding-element-attributes.js`这个文件的代码有点奇怪了……希望读者们不吝赐教！

博文完整代码放在[Github](https://github.com/ubuntuvim/my_emberjs_code)（博文经过多次修改，博文上的代码与 GitHub 代码可能又出入，不过影响不大！）。如果你觉得博文对你有点用，请在 GitHub 项目上给我点个`star`吧。您的肯定对我来说是最大的动力！

