
# Node.js：基于 JavaScript 的框架快速上手指南

![](img/00001.jpeg)

# 引言

NodeJS 是一个非常实用的框架。它可以帮助你开发具有高扩展性的网络应用程序。它也非常适用于 Web 开发。如果你是 JavaScript 专家，那么学习 Node 对你来说非常容易。本书简化了学习 Node.JS 的过程。

# 第 1 章 概览

NodeJS 的开发目的是帮助程序员开发可扩展的网络应用程序。它是一个事件驱动和异步框架，构建在 Chrome 的 JavaScript 引擎之上。为了让你熟练掌握它，你应该精通 JavaScript。它非常适合 Web 应用程序开发。由于其非阻塞运行模式，程序不需要强制等待其他程序的执行，而是创建一个回调函数。在 Node 中等待响应时，允许继续执行其他任务。所有的 Node 库都设计为可以在非阻塞模式下运行。

Node 应用程序的数据完全不在内存中进行缓冲。相反，这些数据是通过分块（chunk-by-chunk）输出的。由于这些特性，与其他框架相比差异巨大，因此日益流行。

# 第 2 章 模块依赖管理

某些应用程序高度依赖于要使用的 NPM 模块数量。这些模块可以在 `package.json` 文件中指定，如下所示：

```json
"dependencies": {
  "express": "2.3.12",
  "jade": ">= 0.0.1",
  "redis": "0.6.0"
}
```

一旦完成上述操作，每当你的项目需要刷新时，都需要像下面一样整理依赖：

```bash
$ npm install
```

通过这种方式，允许指定特定版本的模块或他们所需的最小模块版本。这可以使用符号 `>=` 在数字前缀来实现。有时，你可能有一些与开发相关的依赖。你可能不希望在生产环境中包含这些依赖，可以通过使用 `devDependencies` 属性来指定。示例所示：

```json
"devDependencies": {
  "vows": ">= 0.4.x"
}
```

我们通过 `npm install --production` 进行生产构建可以确保不安装依赖。如果你正在开发私有模块，可以添加 `"private": true` 属性。

# 第 3 章 Require 和 Exports

考虑一个具有以下内容的模块：

```javascript
var p = 10;
var addP = function(value) {
  return value + p;
};
```

当我们在另一个文件中时，可以访问 `p` 或 `addP`。注意这里使用了 `require` 函数。为了暴出某些内容，我们使用 `module.exports`：

```javascript
var p = 8;
var addP = function(value) {
  return value + p;
};

module.exports.p = p;
module.exports.addP = addP;
```

加载后的模块可以按如下方式使用：

```javascript
var myVar = require('./misc');
console.log("Addition of %d to 10 gives us %d", myVar.p, myVar.addP(10));
```

或者，模块的内容可以暴露为：

```javascript
var MyUser = function(name, email) {
  this.name = name;
  this.email = email;
};

module.exports = MyUser;
```

以下两者之间的区别：

```javascript
module.exports.MyUser = MyUser;
```

和

```javascript
module.exports = MyUser;
```

区别仅在于用法如下：

```javascript
var myuser = require('./user');
var user = new myuser.User(); // 第一种情况
```

```javascript
var myuser = require('./user');
var user = new myuser(); // 第二种情况
```

你还应该考虑直接导出函数时会发生什么。这在 `plevel` 示例中所示：

```javascript
var pLevel = function(level) {
  return level > 9000 ? "it is over 9000!!!" : level;
};

module.exports = pLevel;
```

每当需要上述函数时，返回值将是函数本身。这意味着我们可以执行以下操作：

```javascript
require('./plevel')(9050);
```

上述代码是以下代码的精简版本：

```javascript
var pLevel = require('./plevel');
pLevel(9050);
```

# 第 4 章 使用 Promise 进行异步流控制

Promise（承诺）是一个代表异步函数调用结果的实例。在某些社区中，它们被称为“Futures（期约）”。在 NodeJS 中，有许多 CommonJS Promise，我们将在本书的这一章中进行探讨。

它们曾经是基于 Node 框架一部分的 `EventEmitters`。它们当时的样式如下：

```javascript
var promise = fs.stat("test");

promise.addListener("success", function (value) {
    // ok
});

promise.addListener("error", function (err) {
    // the error
});
```

使用这种风格所需的内存分配比必要的要多。此外，由于没有履行所有提倡使用 Promise 的合约，这也引发了一些政治性问题。因此，人们不得不放弃这种使用 Promise 的风格，转而采用使用回调函数（callbacks）的新方法。可以使用如下代码所示：

```javascript
fs.stat("test", function (err, value) {
    if (err) {
        // the error
    } else {
        // ok
    }
});
```

## 术语

与 Promise 使用相关的术语有很多。下面将进行讨论：

- **Fulfillment（履行）**：一旦成功的 Promise 被履行，回调函数将带有该值被调用。如果将来注册了更多回调，它们都将使用相同的值被调用。履行意味着返回特定值的异步类比过程。
- **Rejection（拒绝）**：当 Promise 无法被履行时，该 Promise 会被“拒绝”，这将触发等待的 `errbacks`，并记住被拒绝的错误，以供后续绑定的 `errbacks` 使用。它代表了抛出异常的异步类比。
- **Progressback（进度回调）**：这是一个已执行的函数，用于显示在解决 Promise 方面取得了进展。
- **Callback（回调函数）**：这是一个在 Promise 被赋予值后后执行的函数。
- **Resolution（解析）**：这是一个已解析的 Promise，然后它向履行或拒绝迈进。Promise 的解析只能执行一次，并且可以通过 Promise 代替履行或拒绝来完成。
- **Errback（错误回调）**：这是一个在 Promise 被拒绝并带有异常时执行的函数。

Node 的 CommonJS Promise 主要可以通过两种方式实现。下面将对其进行讨论：

### Q 库

可以使用 `npm` 命令安装此库，如下所示：

```bash
npm install q
```

之后在 NodeJS 程序中可以这样使用：

```javascript
var q = require('q');
```

### Promised-IO

同样可以使用 `npm` 命令进行安装，如下所示：

```bash
npm install promised-io
```

根据你正在使用的版本，使用以下命令引入：

```javascript
var q = require('promised-io');
```

大多数采用 Node 回调风格的函数都可以轻松地封装在 promise 中。任何接收 Node 风格回调且仅调用一次回调的回调函数，都是封装的候选对象。考虑下面的函数，它演示了如何实现这一操作：

```javascript
function myFunction(nodeAsyncFn, context) {
  return function() {
    var defer = q.defer()
      , args = Array.prototype.slice.call(arguments);
    args.push(function(error, value) {
      if (error !== null) {
        return defer.reject(error);
      }
      return defer.resolve(value);
    });
    nodeAsyncFn.apply(context || {}, args);
    return defer.promise;
  };
};
```

上面的函数可以与其他 Node 函数（如 `fs.readFile`）一起使用，如下所示：

```javascript
var rFile = promisify(fs.readFile);

rFile('file.txt').then(function(d) {
  console.log(d);
});
```

通过 PromisedIO 和 `Q`，可以提供用于调用或包装 Node 风格函数的工具函数。如下所示：

```javascript
var rFile = q.convertNodeAsyncFunction(fs.readFile);

rFile('file.txt')
.then(function (d) { });

// 或者

q.execute(fs.readFile, 'file.txt')
.then(function (d) { });
```

上面的案例展示了如何使用 `PromisedIO` 来。当使用 `Q` 时，可以如下所示操作：

```javascript
var rFile = q.node(fs.readFile);

rFile('file.txt')
.then(function (d) { });

// 或者

q.ncall(fs.readFile, fs, 'file.txt')
.then(function (d) { });

// 或者

var deferred = q.defer();

fs.readFile('file.txt', deferred.node());

return deferred.promise;
```

# 第 5 章 管理 Node.js 回调地狱

考虑下面的代码：

```javascript
doAsync1(function () {
  doAsync2(function () {
    doAsync3(function () {
      doAsync4(function () {
      })
    })
  })
})
```

这就是回调地狱。在处理回调地狱时，你必须知道它是主观的。其原因在于，当使用深度嵌套的代码时，它可能运行得良好。在异步代码中，当流程管理变得过于复杂时，问题就会变得像地狱一样。为了让你知道自己正在经历怎样的地狱，请考虑你需要进行的重构工作。

我们想通过一个示例来演示这一点。考虑一种情况：我们感兴趣查找特定目录中最大的文件。下面提供的模块可以用于此操作：

```javascript
var fLargest = require('./findLargest');

fLargest('./path/to/dir', function (error, filename) {
  if (error) return console.error(error);
  console.log('The largest file is:', filename);
});
```

可以遵循以下步骤来实现上述所需工作：

*   读取提供目录中的所有可用文件。
*   获取目录中每个可用文件的状态 (statics)。
*   在可用文件中确定最大的文件（如果有多个大小相同的文件，只需任选其一）。
*   使用最大文件的名称进行回调。

如果在过程中的任何点产生错误，应通过该错误完成回调。同样，回调不应调用超过一次。

## 嵌套方法

首先，我们应该使用嵌套方法来处理。下面是一个如何实现此点的示例：

```javascript
var fs = require('fs');
var path = require('path');
module.exports = function (direct, callb) {
  fs.readdir(direct, function (error, files) { // [1]
    if (error) return callb(error);
    var counter = files.length;
    var errored = false;
    var statistics = [];
    files.forEach(function (file, index) {
      fs.stat(path.join(direct, file), function (error, stat) { // [2]
        if (errored) return;
        if (error) {
          errored = true;
          return callb(error);
        }
        statistics[index] = stat; // [3]
        if (--counter == 0) { // [4]
          var largest = statistics
            .filter(function (statistic) { return statistic.isFile(); }) // [5]
            .reduce(function (prev, next) { // [6]
              if (prev.size > next.size) return prev;
              return next;
            });
          callb(null, files[statistics.indexOf(largest)]); // [7]
        }
      });
    });
  });
};
```

## 异步方法

该模块被广泛使用，它将采取 node 执行操作时采取的方式。async 模块可以如下所示的使用：

```javascript
var fs = require('fs');
var async = require('async');
var path = require('path');
module.exports = function (directory, callb) {
  async.waterfall([ // [1]
    function (next) {
      fs.readdir(directory, next);
    },
    function (files, next) {
      var paths = files.map(function (file) { return path.join(directory, file); });
      async.map(paths, fs.stat, function (error, statistics) { // [2]
        next(error, files, statistics);
      });
    },
    function (files, statistics, next) {
      var largest = statistics
        .filter(function (statistic) { return statistic.isFile(); })
        .reduce(function (prev, next) {
          if (prev.size > next.size) return prev;
          return next;
        });
      next(null, files[statistics.indexOf(largest)]);
    }
  ], callb); // [3]
};
```

通过 `async.map` 函数，我们能够并行运行 `fs.stat`，这些操作将通过一个包含结果的数组进行回调。你还注意到了 `callb` 函数。当过程中发生错误或最后一步完成后，该函数将被调用。且该调用只会执行一次。

使用 `async` 模块，可以保证只有一个回调函数会被触发。它在错误传播和代表我们管理并行性方面也很有用。

## 基于 Promise 的方法

在 NodeJS 中使用 Promise，可以获得函数式编程和错误处理方面的优势。我知道你可能在好奇如何实现任何 Promise 的用途。让我们使用 `Q` 模块来展示如何实现它。如下所示：

```javascript
var fs = require('fs');
var path = require('path');
var Q = require('q');

var fs_readdir = Q.denodeify(fs.readdir); // [1]
var fs_stat = Q.denodeify(fs.stat);

module.exports = function (directory) {
  return fs_readdir(directory)
    .then(function (files) {
      var promises = files.map(function (file) {
        return fs_stat(path.join(directory, file));
      });
      return Q.all(promises).then(function (statistics) { // [2]
        return [files, statistics]; // [3]
      });
    })
    .then(function (data) { // [4]
      var files = data[0];
      var statistics = data[1];
      var largest = statistics
        .filter(function (statistic) { return statistic.isFile(); })
        .reduce(function (prev, next) {
          if (prev.size > next.size) return prev;
          return next;
        });
      return files[statistics.indexOf(largest)];
    });
};
```

注意，Node 的核心功能并不感知 Promise，但我们可以让它感知。所有的统计操作都将通过 `Q.all` 并行运行，并且结果数组的顺序将保持。我们的目标是将文件和统计信息传递给我们的 `next` 函数，这将是最后返回的内容。注意，在 Promise 对象内部抛出的任何异常都将被捕获，这与我们之前的示例不同。客户端的 API 也将被修改，以变得以 Promise 为中心。如下所示：

```javascript
var fLargest = require('./findLargest');

fLargest('./path/to/directory')
  .then(function (fname) {
    console.log('The largest file is:', fname);
  })
  .catch(console.error);
```

从上面的设计中可以看出，在这种情况下你不需要暴露一个 Promise 接口。对于大多数 Promise 库，都提供了一种机制，让我们能够暴露一种 Node 回调风格。

## 基于生成器的方法

生成器只是在 JavaScript 中使用的轻量级协程。通过这些，人们可以使用 `yield` 关键字来挂起然后恢复特定的函数。生成器函数使用一种看起来像 `function*()` 的特殊语法。异步操作也可以通过使用 thunk 或 Promise 等对象被挂起和恢复，这可以导致看起来像同步代码的异步代码。Thunk 只是一个函数，它在被调用时会返回一个回调函数。在这种情况下，回调的签名与典型的 Node 回调函数相似，这意味着错误将作为第一个参数。

我们需要创建一个示例，演示如何将生成器用于异步流控制。实现方法如下：

```javascript
var co = require('co');
var thunkify = require('thunkify');
var fs = require('fs');
var path = require('path');

var readdir = thunkify(fs.readdir); // [1]
var stat = thunkify(fs.stat);

module.exports = co(function* (directory) { // [2]
  var files = yield readdir(directory); // [3]
  var statistics = yield files.map(function (file) { // [4]
    return stat(path.join(directory, file));
  });

  var largest = statistics
    .filter(function (statistic) { return statistic.isFile(); })
    .reduce(function (prev, next) {
      if (prev.size > next.size) return prev;
      return next;
    });

  return files[statistics.indexOf(largest)]; // [5]
});
```

Node 核心功能并不感知 thunk，但我们应该让它感知。通过变量 `co`，我们将接收一个生成器函数，其中可以使用 `yield` 关键字来挂起它。生成器函数将一直挂起直到 `readdir` 返回。由此产生的结果将从 `files` 变量返回。变量 `co` 还可以处理一组并行操作将执行的数组。顺序保持的结果数组将赋值给变量 `statistics`。在此之后，将返回最终结果。

该生成器函数也可以使用我们在本章开头指定的相同回调 API 进行消费。通过 `co`，将实现适当错误处理机制，任何产生的错误（包括抛出的异常）都将传递给我们的回调函数。在 `yield` 语句周围，生成器允许我们使用常用的 `try/catch` 块或语句来处理错误和异常。底部的示例所示：

```javascript
try {
  var files = yield readdir(directory);
} catch (error) {
  console.error('something went wrong while reading the directory');
}
```

Co 为我们提供了一种如何处理数组、嵌套生成器、对象、Promise 等的机制。其他生成器模块也随着实现不断出现。通过 `Q` 模块，有一个名为 `Q.async` 的方法，其行为与使用生成器的 `co` 类似。

## 总结

有很多方法可以帮助你控制应用程序的流转。生成器思想是实现此点的可用方法之一。通过模块化方法，人们可以应用于他们正在使用的任何流控制库。流控制库的示例包括 async、promises 和 generators。

# 第 6 章 Promise 方法

对于大多数 Promise 对象，我们通常在主对象 `Q` 中有其静态对应方法，该方法通常接受 Promise 对象或非 Promise 对象，然后会先创建一个已就绪（fulfilled）的 Promise。对于其他所有，你将拥有与 Promise 对象命名类似的静态对应方法。

对于某些方法，使用的名称与 JavaScript 中的保留关键字相同。这些示例包括 `try`、`catch` 和 `finally`。通过这种，将展示异步 Promise 操作与标准语言构造之间的清晰并行关系。

## 主要的 Promise 方法

### promise.then(onFulfilled, onRejected, onProgress)

这只是带有额外进度处理器的 `then` 方法。

## 回调转 Promise

考虑下面的异步 Node 回调：

```javascript
readFile(function (error, data) {
  if (error) return console.error(error);
  console.log(data);
});
```

如果 `readFile` 函数向我们返回了一个 Promise，那么我们可以这样做：

```javascript
var p = readFile();
p.then(console.log, console.error);
```

当你浅层地观察时，你会发现我们只改变了外观。然而，在此时我们拥有了一个可以用于表示异步操作的值，即 Promise。该 Promise 然后可以被传递，任何访问该 Promise 的人无论异步操作是否完成，都可以通过 `then` 来消费它。我们以某种方式保证了异步操作不会改变，因为 Promise 只会被解析一次，这意味着它要么被就绪（fulfilled），要么被拒绝（rejected）。

`then` 应该被视为一个函数，可以用于解包（unwrapping）promise，以揭示异步操作发生了什么。避免将其仅仅视为一个只接受 `onFulfilled` 和 `onRejected` 两个回调函数的函数。只要你能访问它，就可以通过使用 `then` 来解包它。

### Promise 的嵌套与链式调用

`then` 方法可以返回一个 promise。如下所示：

```javascript
var p1 = readFile();
var p2 = p1.then(readAnotherFile, console.error);
```

该 promise 仅代表其可能指定的 `onRejected` 和 `onFulfilled` 处理器的返回值。请注意，我们可能只有一个解析（resolution），而该 promise 将代理任何被调用的解析，如所示所示：

```javascript
var p1 = readFile();
var p2 = p1.then(function (data) {
  return readAnotherFile(); // 如果 readFile 运行成功，让我们读取 readAnotherFile
}, function (error) {
  console.error(error); // 如果 readFile 运行失败，让我们记录它，但我们仍然会读取 readAnotherFile
  return readAnotherFile();
});

p2.then(console.log, console.error); // readAnotherFile 的结果
```

注意 `then` 返回一个 promise，这表明 promise 可以进行链式调用，以避免回调地狱。如下所示：

```javascript
readFile()
  .then(readOtherFile)
  .then(performSomethingElse)
  .then(...);
```

如果你需要保持一个闭包（closure），可以像下面这样嵌套 promise：

```javascript
readFile()
  .then(function (d) {
    return readOtherFile().then(function () {
      // 对 `data` 执行某些操作
    });
  });
```

### 同步函数与 Promise

有多种方法可以使用 promise 进行同步函数的建模。其中一个示例是使用 `return` 函数来调用另一个函数。在我们之前的示例中，我们一直在使用 `readAnotherFile()` 函数来指示在 `readFile` 函数之后要执行什么。

一旦你返回了一个 promise，一旦同步操作完成，下一个 `then` 就会收到信号。也可以返回其他类型的的值，下一个 `onFulfilled` 将该值作为参数传递给它。如下所示：

```javascript
readFile()
  .then(function (buffer) {
    return JSON.parse(buffer.toString());
  })
  .then(function (data) {
    // 对 `data` 执行某些操作
  });
```

这就是这种实现方法。

### Promise 与错误处理

除了 `return` 关键字外，还可以使用其他关键字如 `throw` 和 `try/catch`，它们在处理错误和异常时非常有用。这展示了 promise 在 Node 中是多么强大。我们希望同步这种实现方式。考虑以下这段同步代码的情况：

```javascript
try {
  doThis();
  doThat();
} catch (error) {
  console.error(error);
}
```

通过上面的示例，`doThis()` 和 `doThat()` 函数将返回错误。我们的目标是捕获并记录此错误。通过 `try/catch` 块，可以将许多操作组合在一起。这意味着可以很大程度上避免对我们的每个操作进行显式错误处理的过程。这可以通过 promise 异步完成。如下所示：

```javascript
doThisAsync()
  .then(doOtherAsync)
  .then(null, console.error);
```

如果函数 `doThisAsync` 运行失败，promise 将被拒绝，链中带有 `onRejected` 处理器的下一个 `then` 将被调用。在我们的示例中，这个函数是 `console.error`。注意，就像 `try/catch` 块一样，这个函数将永远不会被调用。这就是我们所证明的程度，因为使用原始回调时，我们每一步都在显式地处理错误。当抛出异常时（无论是隐式的还是显式的），只要它来自 `then` 回调，它将由 promise 处理。一个示例如下所示：

```javascript
doThisAsync()
  .then(function (d) {
    d.test.baz = 'bar'; // 因为 test 未定义，将抛出 ReferenceError
  })
  .then(null, console.error);
```

产生了一个错误。在上述情况下抛出的 `ReferenceError` 将由链中的下一个 `onRejected` 处理器处理。上述方法也适用于显式流程。一个示例如下所示：

```javascript
doThisAsync()
  .then(function (d) {
    if (!d.baz) throw new Error('预期那里应该有一个 baz');
  })
  .then(null, console.error);
```

如你所知，promise 的工作方式与 `try/catch` 块相同。通过该块，可以掩盖错误而无需显式地处理它。一个示例如下所示：

```javascript
try {
  throw new Error('永远不会意识到这件事发生了');
} catch (ex) {}
```

同样的情况也适用于 promise，如下所示：

```javascript
readFile()
  .then(function (d) {
    throw new Error('永远不会意识到这件事发生了');
  });
```

为了暴露被掩盖的错误，我们应该使用 `.then(null, onRejected)` 子句来结束 promise 链。一个示例如下所示：

```javascript
readFile()
  .then(function (d) {
    throw new Error('现在我意识到这件事发生了');
  })
  .then(null, console.error);
```

有些库有其他机制来暴露被掩盖的错误。一个很好的例子是 `Q` 模块，它为我们提供了名为 `done` 的方法，可以向上抛出错误。

### 回调转换为 Promise

你可能不知道 promise 是如何生成的。创建 promise 的 API 规范并没有在 `Promise/A+` 中完成，因为对于互操作性这不是必要的。这表明 promise 库的实现总是不同的。

注意，在 Node 核心异步函数中，无法返回 promise。然而，通过使用 `Q` 模块，我们可以实现这一点。如下所示：

```javascript
var fs_rFile = Q.denodeify(fs.readFile);
var p = fs_rFile('file.txt');
p.then(console.log, console.error);
```

通过 `Q`，提供了许多辅助函数用于适配环境，使其能够感知 promise。

### 原始 Promise 的创建

你可以使用 `Q.defer` 来创建原始 promise。假设我们想让 `fs.readFile` 感知 promise。如下所示：

```javascript
function fs_rFile (file, encoding) {
  var deferred = Q.defer();
  fs.readFile(file, encoding, function (error, data) {
    if (error) deferred.reject(error); // 以 `error` 为原因拒绝 promise
    else deferred.resolve(data); // 以 `data` 为值解析 promise
  });
  return deferred.promise; // 返回 promise
}

fs_rFile('file.txt').then(console.log, console.error);
```

人们还可以创建同时支持 API 和回调的 API。你现在知道如何将回调代码转换为 promise 代码了。可以开发提供回调和 promise 接口的 API。一个示例是我们希望将 `fs.readFile` 转换为支持 promise 和回调的 API。这可以很容易完成。下面的代码演示了在 Node 中如何实现：

```javascript
function fs_rFile (file, encoding, callback) {
  var deferred = Q.defer();
  fs.readFile(file, encoding, function (error, d) {
    if (error) deferred.reject(error); // 以 `error` 为原因拒绝 promise
    else deferred.resolve(d); // 以 `d` 为值解析 promise
  });
  return deferred.promise.nodeify(callback); // 返回 promise
}
```

一旦提供了回调，在 promise 解析或拒绝后，将使用标准的 Node 参数风格调用它。标准的 Node 风格参数格式为 `(err, result)`。一个示例如下所示：

```javascript
fs_rFile('file.txt', 'utf8', function (error, data) {
  // ...
});
```

Promises 也可以用于执行并行操作。你现在已经了解了 Node.JS 中顺序异步操作是如何运行的。当使用 `Q` 模块来处理并行操作时，我们使用 `Q.all` 方法。该方法通常接收一个 promise 数组，然后返回一个它创建的新的 promise。一旦所有必要的操作都成功完成，这个新的 promise 就会完成。如果单个或多个操作失败或运行不成功，则新的 promise 将被拒绝。下面是一个示例：

```javascript
var aPromise = Q.all([ fs_rFile('myfile1.txt'), fs_rFile('myfile2.txt') ]);
aPromise.then(console.log, console.error);
```

这就是实现方法。你还应该意识到，promise 的功能模拟了函数。函数始终有一个返回值。而使用 promise，在异步部分具有高度的一致性。为了将结果扩展到多个参数中，可以使用 `Q.spread`。

# 第 7 章 单进程中执行多个实例

Node 经常被要求集成到其他应用程序中。例如，当我们需要将它与其他事件循环集成，并为 Node 支持多个执行上下文时。当我们谈论同一个上下文时，我们的意思是能够在同一个应用程序中和平存在多个 Node 实例的能力。

目前，使用 Node `v0.12`，可以在同一个事件循环中使用多个执行上下文。Node 内部也应该意识到多个执行上下文的存在。考虑下面提供的示例，它展示了如何实现：

```javascript
function myconnect() {
  this.write('GET / HTTP/1.1\r\n' +
  'Host: strongloop.com\r\n' +
  '\r\n');
  this.pipe(process.stdout);
}

require('net').connect(80, 'strongloop.com', myconnect);
```

从执行角度来看，过程如下：

```
<enter VM>
connect(80, 'strongloop.com'); // 内核在此报告 EINPROGRESS
<leave VM>
<等待 TCP 握手完成>
<enter VM>
myconnect();
<leave VM>
```

执行上下文可以在我们对 vm 的调用之间发生变化。这就是为什么 `connect()` 函数必须记住当前上下文，而对 `myconnect()` 的调用应该恢复它的原因。如果你未能做到这一点，你可能会发现很难追踪你程序中任何存在的 bug。

然而，在 Node 中，这会被自动处理。这意味着你不需要担心这个问题。

对于那些需要插件作者且你需要制作插件的人，请注意上下文，可以如下所示进行：

*   不要使用 `NODE_MODULE()`，而是使用 `NODE_MODULE_CONTEXT_AWARE()`。之前：

```cpp
void Initialize(v8::Handle<v8::Object> exports) {
  // ...
}
NODE_MODULE(test, Initialize)
```

之后，按照如下方式操作：

```cpp
void Initialize(v8::Handle<v8::Object> exports,
  v8::Handle<v8::Value> module,
  v8::Handle<v8::Context> context) {
  // ...
}
NODE_MODULE_CONTEXT_AWARE(test, Initialize)
```

# 第 8 章 扩展操作符

其次，当从代码调用 `update` 方法时，可以在选项对象中进行标记设置，如下所示：

```javascript
User.updateAll(
  { name: 'Joel' },
  { '$rename': { name: 'fname' }},
  { allowExtendedOperators: true }
);
```

# 第 9 章 事件循环监控

通过 Node 中的事件循环，我们拥有了处理高并发请求的能力，同时运行这些请求是单线程的。处理工作被交给了操作系统本身，并通过 POSIX 接口完成，因为新的回调函数和事件仍在被处理中。

## 阻塞事件循环

在 Node 应用中执行此操作时，可能会导致灾难性的影响。我们将演示如何通过外部事件产生阻塞。

在函数调用中，当当前线程的执行流必须等待函数执行完毕才能继续时，就称为发生了阻塞。大多数人将“I/O”看作是阻塞的。一个例子是你调用函数 `socket.read()` 时。程序必须等待我们的调用结束才能继续。这就是你可能需要通过返回值执行的操作。

请注意，在 Node 中，调用 CPU 任务的函数始终会阻塞。考虑下文所示的 `fibonacci` 函数，由于它需要使用 CPU，目前会阻塞线程的执行。以下是该函数：

```javascript
function fibonacci (j) {
  if (j < 2)
    return 1;
  else
    return fibonacci(j-2) + fibonacci(j-1);
}
```

在 Node 中，我们不会为 Fibonacci 创建服务器。然而，有时 Node 会变成 CPU 限制。考虑下面的示例：

```javascript
function requestHandler(request, response) {
  var body = request.rawBody; // 包含 POST 体
  try {
    var json = JSON.parse(body);
    response.end(json.user.username);
  }
  catch(ex) {
    response.end("FAIL");
  }
}
```

通过上述示例，请求体将被获取并解析。此流程运行得非常良好，直到执行一个大小为 15MB 的文件。当对 15MB 文件执行 `JSON.parse()` 调用时，处理需要大约 1.5 秒。

对于需要监控并发连接的人，可以使用 [StrongLoop Arc](https://strongloop.com/node-js/build-deploy-and-scale/)。它还可以让你监控所创建的 Node 应用的吞吐量。

# 结论

可以得出，NodeJS 是一个非常有用且强大的库，为 Web 应用开发提供了帮助。该框架以其在规模和性能上的高度可扩展性而闻名。这就是为什么在需要高可扩展性的网络应用开发中被广泛使用。

该框架是事件驱动异步的，构建在 Chrome 的 JavaScript 引擎之上。JavaScript 开发者和专家通常发现学习使用 Node 非常容易，因为它们之间关系紧密。事实上，Node 基于 JavaScript 的，因为它是 JavaScript 的可用库之一。

在 Node 中，你的程序不会被强制等待某些操作完成。当你等待响应可用时，你可以继续执行其他任务。这是因为 Node 是非阻塞的，并可以支持执行并发操作。大多数人都理解数据缓冲的概念，即将其存储在一种名为 buffer 的内存中以便快速方便地访问。在 Node 中，完全不支持这种内存类型或过程。发生的是数据以分块（chunk-by-chunk）的形式提供或输出给用户。

该框架拥有强大的特性，这解释了它在 Web 开发者中日益流行的原因。与相关的框架或可以补充它的框架相比，它更受欢迎。此类框架的一个例子是 Ruby on rails。该框架拥有许多模块，可以用于完成应用中的不同任务。学习如何使用这个框架对你将很有帮助，以便在你的开发过程中获得支持。这本书对你是一份极佳的指南。
