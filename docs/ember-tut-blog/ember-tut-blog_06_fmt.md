

# Ember.js 入门指南之五：绑定（binding）

正如其他框架一样，`Ember`也有它特有的数据绑定方式，并且可以在任何一个对象上使用绑定。然而，数据绑定大多数情况下都是使用在`Ember`框架本身，对于开发者来说，最好还是使用计算属性，更为简单方便。

## 双向绑定

```js
// 双向绑定
Wife = Ember.Object.extend({  
  householdIncome: 800
});
var wife = Wife.create();

Hasband = Ember.Object.extend({  
  // 使用 alias 方法实现绑定
  householdIncome: Ember.computed.alias('wife.householdIncome')
});

hasband = Hasband.create({  
  wife: wife
});

console.log('householdIncome = ' + hasband.get('householdIncome'));  // output > 800
// 可以双向设置值

// 在 wife 方设置值
wife.set('householdIncome', 1000);  
console.log('householdIncome = ' + hasband.get('householdIncome'));  // output > 1000
// 在 hasband 方设置值
hasband.set('householdIncome', 10);  
console.log('wife householdIncome = ' + wife.get('householdIncome')); 
```

![run result](img/142caed7d5803f63d752f8388f3a9e34.jpg)

需要注意的是，绑定并不会立刻更新对应的值，`Ember`会等待直到程序代码运行完成，并且是在同步改变之前，所以你可以多次改变计算属性的值。由于绑定是很短暂的，所以也不需要担心开销问题。

## 单向绑定

单向绑定只会在一个方向上传播变化。相对双向绑定来说，单向绑定做了性能优化。对于双向绑定来说，如果你只是在一个方向上设置关联，其实就是一个单向绑定。

```js
var user = Ember.Object.create({  
  fullName: 'Kara Gates'
});

UserComponent = Ember.Component.extend({  
  userName: Ember.computed.oneWay('user.fullName')
});

userComponent = UserComponent.create({  
  user: user
});

console.log('fullName = ' + user.get('fullName'));  
// 从 user 可以设置
user.set('fullName', "krang Gates");  
console.log('component>> ' + userComponent.get('userName'));  
// UserComponent 设置值，user 并不能获取，因为是单向的绑定
userComponent.set('fullName', "ubuntuvim");  
console.log('user >>> ' + user.get('fullName')); 
```

![run result](img/76f1e768dcff5c09effcb4d8c9a7966c.jpg)

关于数据绑定的知识点不多，相对来说不是重点，毕竟对象之间的关联关系是越少、越简单越好。关联关系多了反而难以维护。

博文完整代码放在[Github](https://github.com/ubuntuvim/my_emberjs_code)（博文经过多次修改，博文上的代码与 GitHub 代码可能又出入，不过影响不大！）。如果你觉得博文对你有点用，在 GitHub 项目上给我个`star`吧。您的肯定对我来说是最大的动力！！

