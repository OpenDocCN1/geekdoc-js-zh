

# Ember.js 强制加载数据

Ember 提供了默认的缓存 `store`。当界面需要获取某个数据时，Ember 首先会在 `store` 中查询；如果没有，才发请求；如果有，则不发送请求。

但是，对于一次实时性很强的项目，这种方式不可行，必须每次都发送请求获取实时数据。这种情况下要如何处理呢？

## 调用 `findXxx` 方法

如果你看过 API，应该知道获取数据有 2 种方法：一种是调用 `peekRecord`、`peekAll`，另一种是调用 `findRecord`、`findAll`。后两个方法每次都会发请求，避免使用缓存数据。

## 设置 `reload` 为 `true`

通常我们会通过 `{{link-to}}` 进入到某个路由，并通过 `id` 查询。此时可以设置查询参数，让每次查询都发请求。

```js
// app/routes/auction.js

export default Ember.Route.extend({

  model(params) {
    return this.store.findRecord('auction', params.id, { reload: true });
  }

}); 
```

但是，并不是每次都会执行 `model` 回调。只有强制刷新页面才会执行 `model` 回调，此时只能通过控制缓存来实现。

## 缓存控制

可以通过重写适配器来实现缓存控制。

```js
// app/adapters/application.js

export default DS.RESTAdapter.extend({

  shouldReloadRecord: function(store, snapshot) {
    return false;
  },

  shouldReloadAll: function(store, snapshot) {
    return false;
  },

  shouldBackgroundReloadRecord: function(store, snapshot) {
    return true;
  },

  shouldBackgroundReloadAll: function(store, snapshot) {
    return true;
  }
}); 
```

以上是所知道的几种强制加载数据的方法。如果你有其他的方法，欢迎留言补充！

