
# Web 应用开发：Ember.js 指南

![](img/00001.jpeg)

## 免责声明

尽管我们已尽力核实书中提供的信息，但作者对其中包含的主题的错误、遗漏或相反的解释不承担任何责任。书中提供的信息仅供教育和娱乐之用。读者对其自己的行为负责，作者对因使用这些信息而导致的任何实际或感知的责任或损害不承担任何责任。

书中使用的商标均未经任何许可，且这些商标的发布未获得商标所有者的许可或支持。书中所有商标和品牌仅用于说明目的，其所有权归所有所有，与本文无关联。

## 介绍

市场对 Web 应用的需求正在增加。Ember JS 是一种可以辅助开发此类应用的 JavaScript。该框架很容易学习，特别是对于 JavaScript 专家来说。然而，即使你完全不熟悉 JavaScript，也不必担心，因为书中的解释非常易理解。通过这种 JavaScript，你可以创建具有高度交互用户界面的 Web 应用，你的用户一定会喜欢你的应用。

## 第 1 章 控制器

控制器非常组件，人们认为它们未来将由组件取代。

在大多数当前的应用程序中，控制器并不经常使用。当使用它们时，它们承担以下职责：

1. 用于根据当前使用的路由维护状态。
2. 当用户操作从组件传递到路由时，它们必须通过控制器。

我们需要通过使用路由来演示这一点，这可以帮助我们显示博客文章。

模板将绑定到模板中的以下属性：

```html
<h1>{{model.title}}</h1>
<h2>by {{model.author}}</h2>
<div class="intro">
  {{model.intro}}
</div>
<hr>
<div class="body">
  {{model.body}}
</</div>
```

如上面的示例所示，我们没有特定的属性或操作需要显示。

假设我们需要添加一个功能，允许用户在正文部分的显示之间切换。为了实现这一点，我们将代码修改为如下：

```html
<h1>{{model.title}}</h1>
<h2>by {{model.author}}</h2>
<div class='intro'>
  {{model.intro}}
</div>
<hr>

{{#if isExpanded}}
  <button {{action "toggleBody"}}>隐藏正文</button>
  <div class="body">
    {{model.body}}
  </div>
{{else}}
  <button {{action "toggleBody"}}>显示正文</button>
{{/if}}
```

在控制器的“actions”钩子中，我们可以定义动作的操作，就像我们在组件中可以做的那样。下面的代码所示：

```javascript
export default Ember.Controller.extend({
  actions: {
    toggleBody() {
      this.toggleProperty('isExpanded');
    }
  }
});
```

### 控制器之间的依赖关系管理

有时，当我们嵌套资源时，通常需要在两个控制器之间建立连接。考虑下方的路由器：

```javascript
Router.map(function() {
  this.route('post', { path: '/p/:post_id' }, function() {
    this.route('comments', { path: '/comments' });
  });
});
```

访问 URL `/posts/1/comments` 时，模型 `post` 将加载到 `PostController` 的模型中。然而，与其相关的某些信息可能会显示在 `comments` 的模板中。

为了实现这一点，我们必须将 `pController` 注入到 `CommentsController` 中。如下所示：

```javascript
export default Ember.Controller.extend({
  pController: Ember.inject.controller('post')
});
```

我们的注释将能够访问 `PController`，这是一个只读别名，可以从控制器中读取模型。考虑下面的代码：

```javascript
export default Ember.Controller.extend({
  pController: Ember.inject.controller('post'),
  post: Ember.computed.reads('pController.model')
});
```

考虑下一个 `.hbs` 文件：

```html
<h1>针对 {{post.title}} 的评论</h1>
<ul>
  {{#each model as |comment|}}
    <li>{{comment.text}}</li>
  {{/each}}
</ul>
```

## 第 2 章 模型

构建 Web 应用程序的方法之一是实现与数据获取高度耦合的人机界面组件。

考虑你正在创建一个博客应用的情况。如果你正在创建应用程序的管理员部分，你可能被迫让组件承担获取和存储数据的责任。考虑下面的代码：

```html
<h1>针对 {{post.title}} 的评论</h1>
<ul>
  {{#each model as |comment|}}
    <li>{{comment.text}}</li>
  {{/each}}
</ul>
```

模板包含的草稿列表随后就可以显示出来。下面的代码演示了这一点：

```html
<ul>
  {{#each drafts key="id" as |draft|}}
    <li>{{draft.title}}</li>
  {{/each}}
</ul>
```

注意，应用是由许多组件组成的。你可能希望将所有草稿放在另一个页面。这可能需要将旧代码复制并粘贴到新组件中：

```javascript
export default Ember.Component.extend({
  willRender() {
    $.getJSON('/myDrafts').then(data => {
      this.set('drafts', data);
    });
  }
});
```

按钮的 `.hbs` 文件如下：

```html
{{#link-to 'drafts' tagName="button"}}
s ({{drafts.length}})
{{/link-to}}
```

通过上述方法，我们的应用程序将产生两次请求。

在 Ember 数据中，模型的表示是通过一个子类完成的，定义了关系、属性以及呈现用户的行为。通过模型，可以定义服务器提供我们的数据类型。考虑下面名为 `human` 的示例：

```javascript
export default DS.Model.extend({
  fName: DS.attr('string'),
  birthday: DS.attr('date')
});
```

模型还可以描述自身与其他模型之间的关系。考虑下面的示例，展示了如何这样做：

```javascript
export default DS.Model.extend({
  lItems: DS.hasMany('line-item')
});
```

上面的代码用于一个订单。`line.js` 的代码如下：

```javascript
export default DS.Model.extend({
  order: DS.belongsTo('order')
});
```

你必须注意，模型本身没有数据，但它们被用于定义称为 `records` 的特定实例的行为。

### 创建记录

当你需要创建记录时，只需在 store 上调用 `createRecord()` 方法。考虑下面的代码：

```javascript
store.createRecord('post', {
  title: 'Ember 是一个很棒的框架',
  body: 'Lorem ipsum'
});
```

存储的对象可以通过 `this.store` 可控制器和路由器。

### 更新记录

可以通过设置需要更改的属性来修改 Ember JS 数据记录。如下代码所示：

```javascript
this.store.findRecord('human', 1).then(function(myfunction) {
  // ...一旦记录加载
});
```

```javascript
myfunction.set('fName', "John");

});
```

所有 Ember.js 的便利方法始终可以修改属性。这可以像下面所示：

```javascript
human.incrementProperty('age'); // Happy birthday!
```

### 持久化记录

在 Ember JS 中，记录是基于每个实例进行持久化的。当你对任何 `DS.Model` 实例调用 `save()` 方法时，将发送一个网络请求。

默认情况下，EmberJS 中新创建的记录将提交到 Ember data 中其类型 URL。如下面的代码所示：

```javascript
var p = store.createRecord('post', {
  title: 'Ember is Great',
  body: 'Lorem ipsum'
});

p.save(); // => POST to '/posts'
```

后端已存在的记录将通过使用 HTTP `PATCH` 动词进行更新。下方的代码所示：

```javascript
store.findRecord('post', 1).then(function(p) {
  p.get('title'); // => "Ember JS is Great"
  p.set('title', 'New post');
  p.save(); // => PATCH to '/posts/1'
});
```

考虑下方的代码：

```javascript
human.get('isAdmin');            //=> false
human.get('hasDirtyAttributes'); //=> false
human.set('isAdmin', true);
human.get('hasDirtyAttributes'); //=> true
human.changedAttributes();      //=> { isAdmin: [false, true] }
```

人们可以通过检查其属性 `hasDirtyAttributes` 来判断一个待处理记录是否有某些尚未保存的更改。

在上述节点，你可以通过调用 `save()` 方法来保存更改，或者直接将它们回滚。考虑下方的代码：

```javascript
human.get('hasDirtyAttributes'); //=> true
human.changedAttributes();      //=> { isAdmin: [false, true] }
human.rollbackAttributes();

human.get('hasDirtyAttributes'); //=> false
human.get('isAdmin');            //=> false
human.changedAttributes();      //=> {}
```

### 处理验证错误

如果你的后端服务器在你尝试保存时返回了验证错误，模型的 `errors` 属性将包含这些错误。错误可以像下面所示显示：

```handlebars
{{#each p.errors.title as |err|}}
  <div class="error">{{err.message}}</</div>
{{/each}}

{{#each p.errors.body as |err|}}
  <div class="error">{{err.message}}</</div>
{{/each}}
```

### Promises

`save()` 方法将返回一个 promise，这将使我们能够处理成功或失败的情况。考虑下面所示的常见模式：

```javascript
var p = store.createRecord('post', {
  title: 'Ember is Great',
  body: 'Lorem ipsum'
});
var self = this;

function transitionToPost(p) {
  self.transitionToRoute('posts.show', p);
}

function failure(reason) {
  // handling the error
}

p.save().then(transitionToPost).catch(failure);
// => POST to '/posts'
// => transitioning to posts.show route
```

### 删除记录

记录删除可以与创建记录相同的方式进行。可以在 `DS.Model` 实例上调用 `deleteRecord()` 方法。这将记录标记为 `isDeleted`。随后应该调用 `save()` 方法来保存记录的删除。考虑下方的代码：

```javascript
store.findRecord('post', 1).then(function(p) {
  p.deleteRecord();
  p.get('isDeleted'); // => true
  p.save(); // => DELETE to /posts/1
});

// OR
store.findRecord('post', 2).then(function(post) {
  p.destroyRecord(); // => DELETE to /posts/2
});
```

## 关系

Ember 有几种内置关系，定义了模型之间如何关联。

### 一对一

如果你需要在两个模型之间声明这种类型的关系，请使用下面的代码：

这是文件 `myuser.js` 的代码：

```javascript
export default DS.Model.extend({
  profile: DS.belongsTo('profile')
});
```

那么 `profile.js` 文件应该如下：

```javascript
export default DS.Model.extend({
  user: DS.belongsTo('myuser')
});
```

### 一对多关系

这种类型的关系可以在两个模型之间如下声明：

考虑文件 `myposts.js` 的如下代码：

```javascript
export default DS.Model.extend({
  comments: DS.hasMany('comment')
});
```

这里应该是文件 `ourcomments.js` 的代码：

```javascript
export default DS.Model.extend({
  post: DS.belongsTo('p')
});
```

### 显式反向

Ember JS 会尽力发现组件之间存在的关系类型。有时，你可能对同一类型有许多不同的关系类型。

考虑下方的代码：

```javascript
export default DS.Model.extend({
  firstPost: DS.belongsTo('myuser'),
  secondPost: DS.belongsTo('myuser')
});
```

有时你可能对同一类型有许多不同的关系类型。考虑下方的代码：

```javascript
export default DS.Model.extend({
  firstPost: DS.belongsTo('myuser'),
  secondPost: DS.belongsTo('myuser')
});
```

这是文件 `mypost.js` 的代码：

```javascript
export default DS.Model.extend({
  comments: DS.belongsTo('comment')
});
```

### 自引用关系

为了定义自引用关系，你应该已经有了反向关系。下面的示例展示了一对一自引用关系：

```javascript
export default DS.Model.extend({
  children: DS.belongsTo('folder')
});
```

### 创建记录

假设我们有两个模型，`myposts` 和 `comments`。它们的关系如下：

```javascript
export default DS.Model.extend({
  comments: DS.hasMany('comment')
});
```

文件 `comment.js` 如下：

```javascript
export default DS.Model.extend({
  post: DS.belongsTo('post')
});
```

### 更新现有记录

有时，我们可能需要为已记录设置关系。这简单地通过使用 `belongsTo` 关系即可完成。下方的代码所示：

```javascript
let p = this.store.peekRecord('post', 1);
let comm = this.store.peekRecord('comment', 1);
comm.set('post', p);
comm.save();
```

或者，可以将记录推入 `hasMany` 关系以更新它。如下所示：



```javascript
 let p = this.store.peekRecord('post', 1);
let comm = this.store.peekRecord('comment', 1);
p.get('comments').pushObject(comm);
p.save();
```

## 关系

要移除一个 `belongsTo` 关系，我们只需要将其设置为 `null`。这将将其从 `hasMany` 关系的一侧移除。考虑下面的代码，它最直观地演示了这一点：

```javascript
let comm = this.store.peekRecord('comment', 1);
comm.set('post', null);
comm.save();
```

记录也可以从 `hasMany` 关系中移除。考虑下面的代码，它很好地展示了如何实现：

```javascript
let p = this.store.peekRecord('post', 1);
let comm = this.store.peekRecord('comment', 1);
p.get('comments').removeObject(comm);
p.save();
```

### 作为 Promise 的关系

每当你处理关系时，最好始终记住这些关系将返回 promise（承诺）。假设我们要处理某篇文章的异步评论，我们应该等待直到 promise 已完成（fulfilled）。考虑下面的代码：

```javascript
let p = this.store.peekRecord('post', 1);
p.get('comments').then((comments) => {
  // 我们现在可以处理这些评论了
});
```

同样的规则也适用于 `hasMany` 关系，如下所示：

```javascript
let comm = this.store.peekRecord('comment', 1);
comm.get('post').then((p) => {
  // 文章在这里将可用
});
```

Handlebars 模板会自动更新，以反映已解析的 promise。如下所示，文章中显示评论列表：

```html
<ul>
  {{#each p.comments as |comm|}}
    <li>{{comm.id}}</li>
  {{/each}}
</ul>
```

## 将记录推入 Store（存储器）

Store 可以被看作是一个缓存，包含了应用已加载的所有记录。

要将记录推入 store，你只需要调用 `push()` 方法。考虑这样一种情况：在应用首次启动后，我们需要向 store 中预加载一些数据。这可以通过 `route:application` 轻松实现。考虑下面的代码：

```javascript
export default DS.Model.extend({
  title: DS.attr(),
  artist: DS.attr(),
  songCount: DS.attr()
});
```

考虑接下来这段代码：

```javascript
export default Ember.Route.extend({
  model() {
    this.store.push({
      data: [
        {
          id: 1,
          type: 'album',
          attributes: {
            title: 'Very Few Moving Parts',
            artist: 'John Joel',
            songCount: 5
          },
          relationships: {}
        }, {
          id: 2,
          type: 'album',
          attributes: {
            title: 'Our God is Great all the time',
            artist: 'Steve John',
            songCount: 3
          },
          relationships: {}
        }
      ]
    });
  }
});
```

如果数据在推入 store 之前需要通过模型的默认序列化器（serializer）进行归一化，可以使用 `store.pushPayload()` 方法。下面的代码对此这一点：

```javascript
export default DS.RestSerializer.extend({
  normalize(typeHash, hash) {
    hash['songCount'] = hash['song_count']
    delete hash['song_count']
    return this._super(typeHash, hash);
  }
})
```

接下来的代码应该如下：

```javascript
export default Ember.Route.extend({
  model() {
    this.store.pushPayload({
      albums: [
        {
          id: 1,
          title: 'Very Fever Moving Parts',
          artist: 'John Joel',
          song_count: 5
        },
        {
          id: 2,
          title: 'Our God is Great all the time',
          artist: 'Steve John',
          song_count: 2
        }
      ]
    });
  }
});
```

在处理复杂的端点（endpoints）时，`push()` 方法非常重要。你的应用程序可能有一个端点负责执行某些业务逻辑并创建多条记录。下面的代码最好地演示了这一点：

```javascript
export default Ember.Route.extend({
  actions: {
    confirm: function(d) {
      $.ajax({
        data: d,
        method: 'POST',
        url: 'process-payment'
      }).then((digInventory) => {
        this.store.pushPayload(digInventory);
        this.transitionTo('Thanks');
      });
    }
  }
});
```

## 处理元数据（MetaData）

除了从 store 返回的记录外，还需要处理某种形式的元数据。元数据只是伴随特定模型或类型（而非特定记录）的一种数据。

分页是元数据的一种常用方式。考虑一个有很多文章的博客，它们无法一次性显示。可以如下所示进行查询：

```javascript
let res = this.store.query('post', {
  limit: 10,
  offset: 0
});
```

为了获取不同页的数据，可以更改 offset。为了让我们获取元数据，期望格式如下：

```json
{
  "post": {
    "links": {
      "user": "/posts"
    },
    "meta": {
      "total": 100
    }
  }
}
```

无论使用哪种序列化器，都可以使用 `.get('meta')`。这可以应用于 `query()` 调结果。示例所示：

```javascript
// 设置查询
store.query('post', {
  limit: 10,
  offset: 0
}).then((res) => {
  let meta = res.get('meta');
});
```

如果我们有一个 `belongsTo` 关系，可以这样做：

```javascript
let p = this.store.peekRecord('post', 1);
p.get('author').then((author) => {
  let meta = author.get('meta');
});
```

在 `hasMany` 关系上，可以这样做：

```javascript
let p = this.store.peekRecord('post', 1);
p.get('comments').then((comments) => {
  let meta = comments.get('meta');
});
```

## 适配器（Adapters）的自定义

在 Ember data 中，适配器（Adapter）负责数据如何持久化，例如 URL 格式和头部。

对于具有一致规则的端点，可以定义 `adapter:application`。它的优先级高于默认适配器，但会被特定模型的适配器所覆盖。如下代码所示：

```javascript
export default DS.JSONAPIAdapter.extend({
  // 应用特定的重写写在这里
});
```

对于在通信方面具有特定规则的模型，可以通过执行命令 `ember generate adapter name` 创建特定模型的适配器。一个很好的例子是当你运行 `ember generate adapter post` 时，将创建以下文件：

```javascript
export default DS.JSONAPIAdapter.extend({
  namespace: 'api/v1'
});
```

默认情况下，Ember data 自带多个适配器。如果你需要创建自定义适配器，可以使用这些作为起点。

### URL 规范

`JSONAPIAdapter` 适配器在根据模型类型确定通信使用的 URL 方面非常好。考虑下面通过 ID 请求文章的示例：

```javascript
store.find('post', 1).then(function(p) {

});
```

### 复数自定义

有时，在生成路由 URL 时，你可能需要处理模型名称的复数化。可以使用反射器（reflector）来实现此目的。这是一个用于单复数形式之间转换的库。对于不可数或不规则的复数，可以使用 `Ember.Inflector.inflector`。如下所示 easily 实现：

```javascript
// 设置 Ember.Inflector
import './models/custom-inflector-rules';
```

接下来的代码如下：

```javascript
import Inflector from 'ember-inflector';

const inflect = Inflector.inflector;

inflect.irregular('formula', 'formulae');

inflect.uncountable('advice');

// 符合 Ember Inspector 导出的期望
export default {};
```

### 自定义端点路径

`namespace` 属性将用于为具有特定 URL 命名空间的请求添加前缀。

```javascript
export default DS.JSONAPIAdapter.extend({
  namespace: 'api/1'
});
```

这就是实现方法。

## 主机自定义 (Host Customizations)

适配器默认指向当前域名。如果你需要指定新域名，只需在新适配器上设置 `host` 属性即可。下面的代码很好地展示了如何实现：

```javascript
export default DS.JSONAPIAdapter.extend({
  host: 'https://api.sample.com'
});
```

就是这样。

## 路径自定义 (Path Customizations)

可以像下面的代码一样覆盖 `pathForType` 方法：

```javascript
export default DS.JSONAPIAdapter.extend({
  pathForType: function(type) {
    return Ember.String.underscore(type);
  }
});
```

在上述情况下，我们不需要对模型名称进行复数化，并且需要使用下线命名而不是驼峰命名（camelCase）。

## 请求头自定义 (Headers Customizations)

某些 API 需要 HTTP 请求头，一个很好的例子是需要提供 API key。可以将任意请求头作为键值对设置在 `JSONAPIAdapter` 的 `header` 对象上，Ember data 将在我们的每一个 Ajax 请求中发送它们。考虑下面的代码：

```javascript
export default DS.JSONAPIAdapter.extend({
  headers: {
    'API_KEY': 'secret key',
    'ANOTHER_HEADER': 'A header value'
  }
});
```

可以使用 `headers` 作为计算属性（computed property）来支持动态请求头。考虑下面的示例，请求头将根据 session 服务通过计算属性生成。以下是该示例的代码：

```javascript
export default DS.JSONAPIAdapter.extend({
  session: Ember.inject.service('session'),
  headers: Ember.computed('session.authToken', function() {
    return {
      'API_KEY': this.get('session.authToken'),
      'ANOTHER_HEADER': 'A header value'
    };
  })
});
```

在某些情况下，动态请求头需要来自 Ember 观察者系统之外对象的数据。`volatile` 函数也可以用于将属性设置为非缓存模式，这将导致每次请求时都重新计算请求头。下文代码所示：

```javascript
export default DS.JSONAPIAdapter.extend({
  headers: Ember.computed(function() {
    return {
      'API_KEY': Ember.get(document.cookie.match(/apiKey\=([^;]*)/), '1'),
      'ANOTHER_HEADER': 'A header value'
    };
  }).volatile()
});
```

## 编写适配器 (Authoring Adapters)

`defaultSerializer` 属性将用于指定适配器使用的序列化器。这仅在没有指定 `serializer:application` 或特定模型的适配器时才使用。在任何应用程序中指定 `serializer:application` 都非常简单。考虑下面的示例，了如何实现：

```javascript
export default DS.JSONAPIAdapter.extend({
  defaultSerializer: '-default'
});
```

## 自定义序列化器 (Customizing Serializers)

在 Ember data 中，序列化器（serializers）用于格式化发送到和从后端存储接收的数据。默认设置是 Ember data 将使用 JSON API 格式进行数据序列化。

## JSON API 文档 (JSON API Document)

考虑我们请求的如下响应：

```json
{
  "data": {
    "type": "people",
    "id": "567",
    "attributes": {
      "first-name": "John",
      "last-name": "Joel"
    }
  }
}
```

在上述示例中，我们对 `/people/567.` 的请求得到了响应。包含多个记录的响应可以在 `data` 属性中有一个数组，如下所示：

```json
{
  "data": [{
    "type": "people",
    "id": "567",
    "attributes": {
      "first-name": "John",
      "last-name": "Joel"
    }
  }, {
    "type": "people",
    "id": "345",
    "attributes": {
      "first-name": "Mercy",
      "last-name": "Donald"
    }
  }]
}
```

## 侧载数据 (Sideloaded Data)

这类数据不是主请求的一部分，但具有一些关联关系，这些关系应该被添加到 `included` 键下的数组中。考虑下面的代码：



```
json {
  "data": {
    "type": "blogs",
    "id": "1",
    "attributes": {
      "title": "I really like and enjoy blogging!"
    },
    "links": {
      "self": "http://mysite.com/blogs/1"
    },
    "relationships": {
      "comments": {
        "data": [
          { "type": "comments", "id": "5" },
          { "type": "comments", "id": "12" }
        ]
      }
    }
  },
  "included": [{
    "type": "comments",
    "id": "5",
    "attributes": {
      "body": "First!"
    },
    "links": {
      "self": "http://mysite.com/comments/5"
    }
  }, {
    "type": "comments",
    "id": "12",
    "attributes": {
      "body": "Ember is very easy to learn"
    },
    "links": {
      "self": "http://mysite.com/comments/12"
    }
  }]
}
```

在上面的示例中，我们请求了`/blogs/1`，用户也给了我们与人员相关的评论。上面的代码展示了我们得到的响应。

## 自定义序列化器（Customizing Serializers）

在 Ember data 中，默认使用`Serializer`，但也可以为此目的自定义序列化器。自定义序列化器可以通过两种方式定义。人们可以选择为整个`application`定义一个序列化器。

```javascript
import DS from 'ember-data';

export default DS.Serializer.extend({
  serialize(snapshot, opts) {
    var json = this._super(...arguments);
    json.data.attributes.cost = {
      amount: json.data.attributes.amount,
      currency: json.data.attributes.currency
    };
    delete json.data.attributes.amount;
    delete json.data.attributes.currency;
    return json;
  },
});
```

人们也可以为特定模型定义序列化器。

```javascript
import DS from 'ember-data';

export default DS.Serializer.extend({
  serialize(snapshot, opts) {
    var json = this._super(...arguments);
    json.data.attributes.cost = {
      amount: json.data.attributes.amount,
      currency: json.data.attributes.currency
    };
    delete json.data.attributes.amount;
    delete json.data.attributes.currency;
    return json;
  },
});
```

数据可以如下所示更改。

假设服务器向我们提供如下数据：

```json
{
  "data": {
    "attributes": {
      "id": "1",
      "name": "The Product",
      "cost": {
        "amount": 200,
        "currency": "USD"
      }
    },
    "type": "product"
  }
}
```

上述内容应该更改为：

```json
{
  "data": {
    "attributes": {
      "id": "1",
      "name": "The Product",
      "amount": 200,
      "currency": "USD"
    },
    "type": "product"
  }
}
```

这应该如下所示实现：

```javascript
import DS from 'ember-data';

export default DS.JSONSerializer.extend({
  normalizeResponse(store, primModelClass, payload, id, reqType) {
    payload.data.attributes.amount = payload.data.attributes.cost.amount;
    payload.data.attributes.currency = payload.data.attributes.cost.currency;
    delete payload.data.attributes.cost;
    return this._super(...arguments);
  },
});
```

如果你需要跟踪存储（store）中包含的唯一记录，Ember data 要求每个记录在负载（payload）中应该有一个唯一的`id`属性。对于特定类型的每条记录，`id`也应该是唯一的。如果后端使用的键不是`id`，则可以使用序列化器（serializer）的主键属性，以便在数据的序列化和反序列化过程中正确转换`id`。下文代码所示：

```javascript
export default DS.JSONSerializer.extend({
  primaryKey: '_id'
});
```

### 属性名称（Attribute Names）

Ember data 的约定是将特定模型上的属性名称驼峰命名化（camelize）。考虑下面的示例：

```javascript
export default DS.Model.extend({
  fName: DS.attr('string'),
  lName: DS.attr('string'),
  isPersonOfTheYear: DS.attr('boolean')
});
```

`JSONAPISerializer`期望服务器返回的文档负载中的属性是短横线命名法（dasherized）的。下文代码所示：

```json
{
  "data": {
    "id": "44",
    "type": "people",
    "attributes": {
      "first-name": "John",
      "last-name": "Joel",
      "is-person-of-the-year": true
    }
  }
}
```

如果服务器返回的属性使用了非常不同的约定，可以使用序列化器的`keyForAttribute()`方法将模型中的属性名转换为 JSON 负载中的键。考虑下面的代码：

```javascript
export default DS.JSONAPISerializer.extend({
  keyForAttribute: function(attribute) {
    return Ember.String.underscore(attribute);
  }
});
```

可以使用自定义序列化器来映射不规则的键。对象`attrs`可用于在`DS`的不同属性名之间声明一个简单的映射。考虑下面的示例代码：

```javascript
export default DS.Model.extend({
  lName: DS.attr('string')
});
```

我们所做的是为我们的模型创建了一个自定义序列化器，然后覆盖了`attrs`属性。接下来的代码应该如下：

```javascript
export default DS.JSONAPISerializer.extend({
  attrs: {
    lName: 'lastNameOfPerson'
  }
});
```

### 关系（Relationships）

`ID`属性应用于引用其他记录。考虑你的模型具有所示的`hasMany`关系：

```javascript
export default DS.Model.extend({
  comments: DS.hasMany('comment', { async: true })
});
```

此时 JSON 应该将关系编码为类型和 ID 的数组。下文代码所示：

```json
{
  "data": {
    "type": "posts",
    "id": "1",
    "relationships": {
      "comments": {
        "data": [
          { "type": "comments", "id": "5" },
          { "type": "comments", "id": "12" }
        ]
      }
    }
  }
}
```

考虑你拥有如下所示模型的情况：

```javascript
export default DS.Model.extend({
  origPost: DS.belongsTo('post')
});
```

那么该关系应该被 JSON 编码为另一个记录的 ID。下文代码所示：

```json
{
  "data": {
    "type": "comment",
    "id": "1",
    "relationships": {
      "original-post": {
        "data": { "type": "post", "id": "5" },
      }
    }
  }
}
```

如果需要这些命名约定，则可以使用`keyForRelationship`方法进行覆盖。下文代码最清楚地演示了这一点：

```javascript
export default DS.JSONAPISerializer.extend({
  keyForRelationship: function(key, relship) {
    return key + 'Ids';
  }
});
```

### 创建自定义转换（Creation of Custom Transformations）

在某些情况下，内置类型（如 string、`Boolean`等）可能不足以让我们实现我们所需的内容。一个很好的例子是特定的服务器给你提供了非标准的日期格式。

在 Ember data 中，我们可能有新的 JSON 转换被注册用于作为属性。下文代码最好地描述了这一点：

```javascript
export default DS.Transform.extend({
  serialize: function(val) {
    return [value.get('a'), value.get('b')];
  },
  deserialize: function(val) {
    return Ember.Object.create({ a: value[0], b: value[1] });
  }
});
```

接下来的代码应该如下：

```javascript
export default DS.Model.extend({
  position: DS.attr('coordinate-point')
});
```

从 API 接收到`coordinatePoint`后，预期是一个如下所示的数组：

```json
{
  "cursor": {
    "position": [5, 9]
  }
}
```

一旦它加载到模型实例上，它将像下面所示作为一个对象：

```javascript
var c = store.findRecord('cursor', 1);
```

对于那些需要创建自定义序列化器的人，我们建议从`JSONAPISerializer`或`JSONSerializer`开始，然后扩展其中之一以匹配我们的需求。然而，如果有效负载（payload）与其中一个序列化器不同，请考虑你给定的下所示“posts”模型的情况：

```javascript
export default DS.Model.extend({
  title: DS.attr('string'),
  tag: DS.attr('string'),
  comments: hasMany('comment', { async: false }),
  relatedPosts: hasMany('blogs')
});
```

此时`store.push`将接受如下格式的对象：

```json
{
  data: {
    id: "1",
    type: 'post',
    attributes: {
      title: "Ember is easy to Learn",
      tag: "ember",
    },
    relationships: {
      comments: {
        data: [
          { id: "1", type: 'comment' },
          { id: "2", type: 'comment' }
        ],
      },
      relatedPosts: {
        data: {
          related: "/api/v1/blogs/1/related-posts/"
        }
      }
    }
  }
}
```

为了让每个序列化的记录都能转换为 Ember 数据记录，必须遵循上述格式。

## 第 3 章：应用关注点

### 依赖注入

该技术在 EmberJS 中用于对象类的声明、实例化以及它们之间的依赖关系。应用程序及其实例将在 Ember 的依赖注入（DI）实现中发挥作用。

### 工厂注册（Factory Registrations）

工厂可以用于表示应用的一部分，例如模板、路由或自定义类。一个很好的例子是使用键名`template:index`注册的索引模板。

注意，工厂注册必须在应用程序内部或应用实例初始化器（application instance initializers）中完成，但前者更为常见。

考虑下文的示例，它展示了应用初始化如何使用键名`logger:main`注册一个“logger”工厂：

```javascript
export function initialize(app) {
  var Logger = Ember.Object.extend({
    log(n) {
      console.log(n);
    }
  });
  app.register('logger:main', Logger);
}

export default {
  name: 'logger',
  initialize: initialize
};
```

### 实例化对象的注册（Registering Instantiated Objects）

默认设置是 Ember 会在查找后尝试实例化已注册的工厂。在特定类对象的注册过程中，你必须使用`instantiate: false`选项，以避免在查找期间被重复实例化。在下面的示例中，`logger`是一个 JavaScript 对象，在查找时应原样返回。代码如下：

```javascript
export function initialize(app) {
  var logger = {
    log(n) {
      console.log(n);
    }
  };
  app.register('logger:main', logger, { instantiate: false });
}

export default {
  name: 'logger',
  initialize: initialize
};
```

### 单例与非单例注册（Singletons vs. Non-Singletons Registration）

在 Ember data 中，注册被视为单例。这意味着在查找后必须创建一个实例，并且同一个实例将被缓存并在随后的查找中返回。在下例示例中，`message`将注册为非单例：

```javascript
export function initialize(app) {
  var Msge = Ember.Object.extend({
    text: ''
  });
  app.register('notification:message', Msge, { singleton: false });
}

export default {
  name: 'notification',
  initialize: initialize
};
```

### 工厂注入（Factory Injections）

一旦完成工厂注册，我们可以在需要时对其注入。工厂注入可以针对整个类型的工厂进行。考虑下例示例：



```javascript
export function initialize(app) {
  var Logger = Ember.Object.extend({
    log(n) {
      console.log(n);
    }
  });
  app.register('logger:main', Logger);
  app.inject('route', 'logger', 'logger:main');
}

export default {
  name: 'logger',
  initialize: initialize
};
```

由于这种类型注入，类型为`route`的工厂将使用已注入的`logger`进行实例化。`logger`值将从名为`logger:main`的工厂中获取。考虑下例，展示了如何通过注入的`logger`访问应用。示例如下：

```javascript
export default Ember.Route.extend({
  activate() {
    // 属性 logger 被注入到所有路由中
    this.get('logger').log('Entered your route!');
  }
});
```

当使用完整键时，可以像下面所示对完整键进行注入：

`app.inject('route:index', 'logger', 'logger:main');`

### 临时注入 (Ad Hoc Injections)

依赖注入通过使用`Ember.inject`直接在 Ember 类上声明。目前，该属性支持服务和控制器的注入。考虑下代码，它展示了如何将`shopping-cart`服务作为`cart`属性注入到组件`cart-contents`中。代码如下：

```javascript
export default Ember.Component.extend({
  cart: Ember.inject.service('shopping-cart')
});
```

如果你需要根据`audioType`播放不同的音频服务，可以参考以下代码：

```javascript
import Ember from 'ember';
const {
  Component,
  computed,
  getOwner
} = Ember;

// 使用方法：
// {{play-audio song=song}}
export default Component.extend({
  audioService: computed('song.audioType', function() {
    let appInstance = getOwner(this);
    let audioType = this.get('song.audioType');
    return appInstance.lookup(`service:${audioType}`);
  }),
  click() {
    let p = this.get('audioService');
    p.play(this.get('file'));
  }
});
```

### 初始化器 (Initializers)

初始化器允许我们在启动过程中配置应用。存在两种类型：应用实例初始化器和应用初始化器。

应用初始化器在启动期间执行，提供了配置依赖注入的方法。另一种初始化器在加载应用实例时配置，允许我们设置应用的初始状态并 Setup 本地实例。

### 应用初始化器 (Application Initializers)

应用初始化器使用 Ember CLI 的初始化器生成器创建。下述命令展示了这一操作：

`ember generate initializer shopping-cart`

随后我们可以自定义`shopping-cart`初始化器，将`cart`属性注入到应用中的所有路由。代码如下：

```javascript
export function initialize(app) {
  app.inject('route', 'cart', 'service:shopping-cart');
}

export default {
  name: 'shopping-cart',
  initialize: initialize
};
```

### 应用实例初始化器 (Application Instance Initializers)

这些初始化器使用`instance-initializer`生成器创建。下述代码展示了如何实现简单的日志记录，以指示实例已启动：

```javascript
export function initialize(appInstance) {
  let logger = appInstance.lookup('logger:main');
  logger.log('Hello from an instance initializer!');
}
```

```javascript
logger.log('Hi from our instance initializer!');

}

export default {
  name: 'logger',
  initialize: initialize
};
```

### 指定初始化器顺序

如果你需要控制初始化器的运行顺序，可以使用`before`和`after`选项。请考虑下面的代码：

```javascript
export function initialize(app) {
  // ...在此此处添加你的代码 ...
};

export default {
  name: 'configReader',
  before: 'websocketInit',
  initialize: initialize
};
```

接下来的代码应该如下：

```javascript
export function initialize(application) {
  // ... 在此处添加你的代码...
};

export default {
  name: 'websocketInit',
  after: 'configReader',
  initialize: initialize
};
```

## 服务 (Services)

`Ember.service`属性是 Ember 中的一个对象，可以在应用的各个部分使用并调用。以下是服务领域：

*   `Geolocation`。

*   `User/session`身份验证。

*   `Web Sockets`。

*   无法放入`Ember Data`的`Server-backed API calls`。

*   `Third-party APIs`。

*   `Server-sent events`或通知`Logging`。

### 服务的定义

Ember CLI 中的`service`生成器可以用于生成服务。考虑以下命令，它可以用于创建一个`shoppingCart`服务：

```bash
ember generate service shopping-cart
```

服务必须扩展基类`Ember.Service`。如下代码所示：

```javascript
export default Ember.Service.extend({
});
```

就像 Ember 中的对象一样，服务必须经过初始化，并且它应该拥有自己的方法和属性。考虑下面所示的购物车服务，它最好地展示了其工作原理：

```javascript
export default Ember.Service.extend({
  items: null,
  init() {
    this._super(args);
    this.set('items', []);
  },
  add(item) {
    this.get('items').pushObject(item);
  },
  remove(item) {
    this.get('items').removeObject(item);
  },
  empty() {
    this.get('items').setObjects([]);
  }
});
```

### 访问服务

为了访问服务，可以选择通过`Ember.inject.service`函数将其注入到任何由容器解析的对象中，例如另一个服务或组件。该函数有两种用法方式：你可以选择不带参数地调用它，或者将你的服务的注册名称传递给它。

在不传递参数的情况下，服务必须根据其变量键名进行加载。要不带参数加载购物车服务，请如下所示：

```javascript
export default Ember.Component.extend({
  // 想在文件 /app/services/shopping-cart.js 中加载服务
  shoppingCart: Ember.inject.service()
});
```

另一种方法是使用服务的名称作为参数。如下代码所示：

```javascript
export default Ember.Component.extend({
  // 想在文件 /app/services/shopping-cart.js 中加载我们的服务
  cart: Ember.inject.service('shopping-cart')
});
```

通过上述代码，购物车服务将尽注入到我们的组件中，然后可以通过`cart`属性可用。被注入的属性是懒加载的，这意味着在显式调用该属性之前，不会对服务进行实例化。这意味着必须使用`get`函数来访问特定组件的服务，否则你将得到 undefined 错误。

加载后，服务将持续到服务退出。

考虑下面的代码：

```javascript
export default Ember.Component.extend({
  cart: Ember.inject.service('shopping-cart'),
  actions: {
    remove(item) {
      this.get('cart').remove(item);
    }
  }
});
```

在上述代码中，我们为组件`cart-contacts`添加了`remove`动作。一旦被注入到组件中，该服务将在模板中使用。注意下面的代码中使用了`cart`从购物车中获取数据：

```html
<ul>
  {{#each cart.items as |item|}}
    <li>
      {{item.name}}
      <button {{action "remove" item}}>Remove</button>
    </li>
  {{/each}}
</ul>
```

### 运行循环 (The Run Loop)

我们在 Ember 中为应用编写的大部分内部机制和代码都发生在运行循环中。运行循环的目的是以更高效、更有效的方式对工作进行批处理和排序。

下面的代码所示：

```html
<div id="foo"></div>
<div id="bar"></div>
<div id="baz"></div>
```

该框架具有许多我们可以利用来增强我们应用程序的特性。

在 Ember JS 中，控制器（controllers）非常重要，大多数人会将它们与组件（components）混淆。很快，人们认为控制器将由组件所取代。

控制器用于控制状态，这取决于当前正在使用的路由类型。在将信息从组件传递到路由时，也会使用控制器，因为信息必须通过它传递。控制器之间需要建立依赖关系。

当我们需要嵌套资源时，通常会遇到这种情况。我们必须想出一种机制，在控制器之间建立连接。

了解如何在 Ember JS 中创建自定义转换（custom transformations）对你很有帮助。因为可能提供的数据类型可能不足以满足你的需求。Ember JS 中的自定义转换可以在这方面为你提供帮助。我希望这本书能够帮助你理解如何在 Ember JS 中构建应用程序。祝用得愉快！
