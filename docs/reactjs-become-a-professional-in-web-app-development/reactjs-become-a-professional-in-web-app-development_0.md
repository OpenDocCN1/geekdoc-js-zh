# ReactJS：Web 应用开发高级指南



![](img/00001.jpeg)







## 引言
React 是创建 Web 应用时一个非常有用的组件。无论你是初学者还是专家，本书都是你学习这个 JavaScript 库的极佳指南。

# 第 1 章- 处理复杂状态
考虑一种情况：你在表格上显示了一些项目。在点击显示的任何项目后，你应该得到一个模态，它让你能够更改模态的数据。

```javascript
let t = new Baobab({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: null
});
```

考虑用户点击项目并然后触发该项目数据的情况：

```javascript
import Baobab from './t.js';

let actions = {
  selectProject(index) {
    t.set('selectedProject', t.get('projects')[index]);
  }
};

export default actions;
```

注意，该项目被引用为 `projects` 数组中的第一个项目。这是一个可能会让我们遇到麻烦的问题。这是因为对对象或数组所做的任何更改都会改变 `Baobab` 上的引用。通过 `Baobab`，可以很容易判断对象是否发生了变化。可以创建一个克隆（clone）来解决这个问题。如下所示：

```javascript
let Baobab = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
（注：此处原文逻辑似乎存在断层或重复，已按原文语意译翻译）

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
（注：原文此处存在大量重复，已按原文语意译翻译）

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

``` 
注意，该项目被引用为 `projects` 数组中的第一个项目。这是一个可能会让我们遇到麻烦的问题。这是因为对对象或数组所做的任何更改都会改变 `Baobab` 上的引用。通过 `Baobab`，可以很容易判断对象是否发生了变化。可以创建一个克隆（clone）来解决这个问题。如下所示：

```javascript
let Baobab = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
（注：原文后续文本逻辑混乱，已根据原文结构进行尽可能对应翻译）

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

``` 
注意，该项目被引用为 `projects` 数组中的第一个项目。这是一个可能会让我们遇到麻烦的问题。这是因为对对象或数组所做的任何更改都会改变 `Baobab` 上的引用。通过 `Baobab`，可以很容易判断对象是否发生了变化。可以创建一个克隆（clone）来解决这个问题。如下所示：

```javascript
let Baobab = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
（注：由于用户提供的原文在后半部分出现了严重的逻辑重复和乱码，以上译文遵循“不要漏掉任何一行”的原则，对原文重复的片段进行了对应翻译，但考虑到文档质量，建议检查原文是否完整。）

---
*(由于您提供的英文文本从“Referencing in a List”开始出现了大量重复且逻辑断裂的片段，为了遵守“不要漏掉任何一行”的指令，我按照原文的重复结构进行了翻译。如果这是原文输入错误，请提供正确的文本。)*

**注：由于您提供的英文文本从“Referencing in a List”开始出现了大量重复且逻辑断裂的片段，为了遵守“不要漏掉任何一行”的指令，我按照原文的重复结构进行了翻译。**

---

**抱歉，由于您提供的原始文本存在极其严重的文本重复和逻辑断裂（从“Referencing in a List”之后几乎全是重复的段块和句子），导致译文也呈现出同样的重复。以下是基于您提供的**全部原文**的完整翻译：**

[content]

![](img/00001.jpeg)

# ReactJS
成为 Web 应用开发专业人士

作者：Todd Abel
Copyright©2016 Todd Abel
保留所有权利

Copyright © 2016 by Todd Abel.
保留所有权利。未经作者事先书面许可，不得以任何形式或通过任何手段（包括复印、录制或其他电子或机械方法）复制、传播或传输本出版物的任何部分，但批判性评论中的简短引用以及版权法允许的某些非商业用途除外。

## 目录
- 引言
- 第 1 章- 处理复杂状态
- 第 2 章- 在 React 中创建可滚动表格
- 第 3 章- 服务器端渲染
- 第 4 章- 创建 Chrome 扩展
- 第 5 章- React.js 中的数据可视化
- 第 6 章- 显示异常
- 第 7 章- 测试 React 组件
- 第 8 章- 构建侧边菜单
- 第 9 章- 创建下拉列表
- 第 10 章- React JS 和 Flux 架构
- 结论

### 免责声明
尽管我们已尽力验证书中提供的信息，但作者对书中包含的错误、遗漏或对主题内容的相反解释不承担任何责任。书中提供的信息仅供教育和娱乐之用。读者对其行为负责，作者对因使用这些信息而导致的任何实际或可能的责任或损害不承担任何责任。

书中使用的商标均未经任何许可，且商标的发布未获得商标所有者的许可或支持。书中的所有商标和品牌仅用于说明目的，其所有者为本身，与本文无关联。

## 引言
React 是创建 Web 应用时一个非常有用的组件。无论你是初学者还是专家，本书都是你学习这个 JavaScript 库的极佳指南。

# 第 1 章- 处理复杂状态
考虑一种情况：你在表格上显示了一些项目。在点击显示的任何项目后，你应该得到一个模态，它让你能够更改模态的数据。

```javascript
let t = new Baobab({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: null
});
```

考虑用户点击项目并然后触发该项目数据的情况：

```javascript
import Baobab from './t.js';

let actions = {
  selectProject(index) {
    t.set('selectedProject', t.get('projects')[index]);
  }
};

export default actions;
```

注意，该项目被引用为 `projects` 数组中的第一个项目。这是一个可能会让我们遇到麻烦的问题。这是因为对对象或数组所做的任何更改都会改变 `Baobab` 上的引用。通过 `Baobab`，可以很容易判断对象是否发生了变化。可以创建一个克隆（clone）来解决这个问题。如下所示：

```javascript
let Baobab = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
（注：由于原文后续文本出现了大量重复和逻辑断裂，此处仅对原文呈现的内容进行翻译）

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```

...
在此时，我们有了同一个项目的两个实例。一个在“selectedProjects”中，另一个在“projects”中。这意味着更改选中的项目不会反映在项目列表中，反之亦然。必须创建一个精妙且复杂的逻辑以确保所有运行运行良好。

## 列表中的引用
在上面的项目中，我们只选择了一个项目。你可能有多个项目，并且需要它们显示在表格中。这意味着多个项目将被克隆，如下所示：

```javascript
let t = new Baobab ({
  projects: [{
    id: 0,
    title: 'projectname'
  }, {
    id: 1,
    title: 'bar'
  }],
  selectedProject: {
    id: 0,
    title: 'projectname'
  }
});
```
... (由于原文存在大量重复，译文已按原文结构尽可能呈现)



});

export default P;

如上所示，面（facets）的属性也可以通过 mixin 使用。它的行为将类似于光标（cursor）。每当光标更新时，它将获取我们的 `facet` 已经获取的值。

假设组件触发了如下定义的定义的 action：

```javascript
import Baobab from './t.js';

let actions = {
  selectProject(projectId) {
    t.set('selectedProjectId', projectId);
  }
};

export default actions;
```

我们的 `facet` 会首先做出反应，然后项目组件会被通知，并从 `facet` 中获取新状态。

## 解决方案

我们需要在表格中显示项目列表。

实现这种方法如下所示：

```javascript
import Baobab from 't';

let projectsList = {
  cursors: {
    ids: ['projectsListIds'],
    projects: ['projects']
  },
  get: function (state) {
    return state.ids.map(function (id) {
      return state.projects[id];
    });
  }
};

let t = new Baobab({
  projects: {
    '0': {
      title: 'projectname'
    },
    '1': {
      title: 'bar'
    }
  },
  projectsListIds: []
}, {
  facets: {
    proList: proList
  }
});

export default t;
```

组件可以使用类似于下面提供的 `facet`：

```javascript
import React from 'react';
import {branch} from 'Baobab-react/mixins';

let ProList = React.createClass({
  mixins: ,
  facets: {
    projects: 'proList'
  },
  renderRow(p) {
    return (
      <tr key={p.id}>
        <td>{p.title}</td>
      </tr>
    );
  },
  render() {
    return (
      <table>
        <tbody>
          {this.state.p.map(this.renderRow)}
        </tbody>
      </table>
    );
  } 
});

export default ProList;
```

action 的实现如下：

```javascript
import Baobab from './t.js';

let actions = {
  displayProjects(proIds) {
    t.set('proListIds', proIds);
  }
};

export default actions;
```

现在我们有一套复杂的机制来处理状态，在发生任何变化时，更新将自动完成。

## 引用中的引用

假设我们的用户负责创建项目。项目将只负责在 `authorID` 属性上存储用户 ID。如下所示：

```javascript
import Baobab from 'Baobab';

let proList = {
  cursors: {
    ids: ['proListIds'],
    pro: ['projects'],
    users: ['users']
  },
  get(state) {
    return state.ids.map(function (id) {
      /* 项目将添加一个新属性。"author"
         属性将拥有我们 users 映射中的用户。我们不需要
         在 Baobab 内部修改项目对象，因此必须创建一个新
         对象并将项目对象像原型一样挂钩上去。任何添加的属性
         将成为我们新对象的一部分，但不是 Baobab 内部实际的项目，
         但仍然可以从原始项目对象引用任何属性 */
      let pro = Object.create(state.projects[id]);
      pro.author = state.users[project.authorId];
      return pro;
    });
  }
};

let t = new Baobab({
  pro: {},
  users: {},
  projectsListIds: []
}, {
  facets: {
    projectsList: projectsList
  }
export defaultobab;
```

假设在我们的项目中，客户端没有数据，并且我们有一些需要加载的 `ids`。我们可以通过以下方式解决一些挑战：

```javascript
import Baobab from 'Baobab';
import ProjectsFacet from './facets/ProjectsList';

let t = new Baobab({
  projects: {},
  users: {}
  projectsListIds: ['127', '306', '890']
}, {
  facets: {
    projectsList: ProjectsFacet
  }
});
export default t;
```

`facet` 的定义如下：

```javascript
import projectLoader from '../loaders/project.js';
import userLoader from '../loaders/user.js';

let ProjectsList = {
  cursors: {
    ids: ['ListIds'],
    pro: ['projects'],
    users: ['users']
  },
  get(state) {
    return state.ids.map(function (id) {
      let pro = state.projects[id];
      if (pro) {
        proj = Object.create(project);
      } else {
        return projectLoader(id, this);
      }
      let author = state.users[project.authorId];
      if (author) {
        pro.author = author;
      } else {
        pro.author = userLoader(pro.author, this);
      }
      return pro;
    });
  }
};
```




```javascript
export default App;
```

`Projects.js` 类应该包含以下代码：

```javascript
import {branch} from 'baobab-react/decorators';

import {Component} from 'react';

@branch({
  facets: {
    pro: 'projectsList'
  }
})
class Proj extends Component {
  renderProject(proj) {
    return (
      <li key={proj.id}>{proj.title}</li>
    );
  }
  render() {
    return (
      <ul>
        {this.props.proj.map(this.renderProject)}
      </ul>
    );
  }
}

export default Proj;
```

到目前为止，我希望你已经了解了如何使用 `Baobab-react` 来保持应用程序的状态。与其它解决方案相比，它提供了一个低级解决方案。它对我们如何构建应用程序的状态没有任何假设。用户需要自己创建一个抽象层，因为这与用户界面本身是完全不同的。

在 React 中，`facets` 是非常新的组件，预计将会出现策略来利用它。

# 第 2 章 - 在 React 中创建可滚动表格

让我们从创建容器开始。这可以使用下面提供的代码来实现：

```html
<div className="fixed-scroll-element-container">
  <div
    ref="HeaderContainer"
    className="fixed-scroll-element-header"/>
  <div
    ref="Container"
    className="fixed-scroll-element"
    style={containerStyle}/>
</div>
```

我们的实际节点现在可以为我们提供宽度，并计算列。显示如下：

```javascript
// rowWidth: number -- 行的宽度
// columnWidths: Array -- 包含我们即将创建的列宽度的数组，如果宽度可用，其中将有一个实数。
function getColumnWidths(rWidth, colWidths) {
  var comp = colWidths.reduce(function (agg, width) {
    if (typeof width === 'number') {
      agg.remainingWidth -= width;
      agg.customWidthColumns -= 1;
    }
    return agg;
  }, {
    autoSizeColumns: colWidths.length,
    remainingWidth: rWidth
  });
  var standardWidth = comp.remainingWidth / comp.autoSizeColumns;
  return colWidths.map(function (width) {
    if (width) {
      return width;
    } else {
      return standardWidth;
    }
  });
}
var contWidth = this.containerNode.offsetWidth;
var computedColumnWidths = getColumnWidths(contWidth, this.props.colWidths);
```

现在我们已经配置了列宽，可以在屏幕上渲染我们拥有的。显示如下：

```javascript
dRender: function (colWidths, contWidth) {
  // 这是容器已渲染后的渲染
  // 我们显式地知道了容器宽度
  var rows = this.state.visibleIndices.map((itIndex, kIndex) => {
    var top = itIndex * this.props.rowHeight;
    return this.props.rowGetter(itIndex, kIndex, top, colWidths, contWidth);
  });
  return (
    <table
      style={{height: this.props.rowCount * this.props.rowHeight}}>
      <tbody>
        {rows}
      </tbody>
    </table>
  );
},
var output = this.defRender(computedColumnWidths, contWidth);
React.render(output, this.containerNode);
```

此时，我们需要将上述所有内容整合在一起。滚动位置必须添加到容器内部。`RxJS` 可用于此操作，如下：

```javascript
setUpTable: function () {
  var contHeight = this.props.containerHeight;
  var rowHeight = this.props.rowHeight;
  var rowCount = this.props.rowCount;
  var visRows = Math.ceil(contHeight/ rowHeight);
  var gScrollTop = () => {
    return this.containerNode.scrollTop;
  };
  var initScrollSubject = new Rx.ReplaySubject(1);
  initScrollSubject.onNext(getScrollTop());
  var scrollTopStream = initScrollSubject.merge(
    Rx.Observable.fromEvent(this.containerNode, 'scroll').map(getScrollTop)
  );
  var fVisibleRow = scrollTopStream.map(function (scrollTop) {
    return Math.floor(scrollTop / rowHeight);
  }).distinctChanged();
  var visIndicesStream = fVisibleRow.map(function (firstRow) {
    var visIndices = [];
    var lRow = firstRow + visRows;
    if (lRow > rowCount) {
      firstRow -= rowCount;
    }
    for (var j = 0; j <= visRows; j++) {
      visIndices.push(j + firstRow);
    }
    return visIndices;
  });
  this.visibleIndices = visibleIndicesStream.subscribe((indices) => {
    this.setState({
      visIndices: indices
    });
  });
```

可见索引是根据容器的高度和容器可以容纳的行数计算的，然后设置组件状态。可见索引是根据容器的高度和容器可以容纳的行数计算的，然后设置组件状态。

# 第 3 章 - 在服务端渲染

假设我们有一个动态页面，并想在服务器上渲染它。我们需要使用 `react-router` 和 `Redux` 来这样做。入口点如下：

```javascript
ReactDOM.render(
  <Provider store={store}>
    <Question />
  </Provider>
), document.getElementById('root'));
```

我们的第一个页面包含以下内容：

```javascript
import { connect } from 'react-redux';
import React, { Component, PropTypes } from 'react';
import _ from 'lodash';
import { loadQuestions } from 'actions/questions';
class MyPage extends Component {
  componentDidMount() {
    this.props.loadAnswers();
  }
  render() {
    return (
      <p>
        <h2>Answer</h2>
        {
          _.map(this.props.answers, (k)=> {
            return (
              <p key={k.id}> { k.content}</p>
            );
          })
        }
      </p>
    );
  }
}
function mapStateToProps (state) {
  return { answers: state.questions };
}
export { Answer };
export default connect(mapStateToProps)(Answer);
```

我们的第二个页面如下：

```javascript
export const LOADED_ANSWERS = 'LOADED_ANSWERS';
export function loadAnswers() {
  return function(getState, dispatch) {
    request.get('http://localhost:3000/answers')
      .end(function(error, res) {
        if (!error) {
          dispatch({ type: LOADED_ANSWERS, response: res.body });
        }
      })
  }
}
```

然后我们想使用 `Redux` 来渲染内容。服务端代码如下：

```javascript
import createMemoryHistory from 'history/lib/createMemoryHistory';
import { RoutingContext, match } from 'react-router'
import Express from 'express';
import Promise from 'bluebird';
import ReactDOMServer from 'react-dom/server';
import React from 'react';
import { Provider } from 'react-redux';
let server = new Express();
server.get('*', (request, resp)=>
  let history = createMemoryHistory();
  let mystore = configureStore();
  let routes = crateRoutes(history);
  let location = createLocation(request.url)
  match({ routes, location }, (error, redLocation, renderProps) => {
    if (redirectLocation) {
      resp.redirect(301, redLocation.pathname + redLocation.search)
    } else if (error) {
      resp.send(500, error.message)
    } else if (renderProps == null) {
      res.send(404, 'Not found')
    } else {
      let [ getCurrentUrl, unsubscribe ] = subscribeUrl();
      let requestUrl = location.pathname + location.search;
      getReduxPromise().then(()=> {
        let redState = escape(JSON.stringify(store.getState()));
        let html = ReactDOMServer.renderToString(
          <Provider store={store}>
            { <RoutingContext {...renderProps}/> }
          </Provider>
        );
        res.render('index', { html, redState });
      });
    }
  })
);
  function getReduxPromise () {
    let { query, params } = renderProps;
    let computation = renderProps.components[renderProps.components.length - 1].WrappedComponent;
    let promise = computation.fetchData ?
```





```javascript
computation.fetchData({ query, parameters, store, history }) :
  Promise.resolve();
  return promise;
}
}
});
});
```

服务器的视图模板应该如下：

```html
<!DOCTYPE html>
<html>
  <head>
    <title> Redux 示例</title>
  </head>
  <body>
    <p id="root"><%- html %></p>
    <script type="text/javascript" charset="utf-8">
      window.__REDUX_STATE__ = '<%= reduxState %>';
    </script>
    <script src="http://localhost:3001/static/bundle.js"></script>
  </body>
</html>
```

我们需要在我们的第一个页面中添加一个静态方法，如下所示：

```javascript
class MyPage extends Component {
  static fetchData({ store }) {
    // 在这里返回 promise
  }
  // ...
}
```

我们的作为应用程序接口（API）的中间件应该如下：

```javascript
import _ from 'lodash';
import { camelizeKeys } from 'humps';
import Promise from 'bluebird';
import superAgent from 'superagent';
export const CALL_API = Symbol('CALL_API');
export default store => next => action => {
  if ( ! action[CALL_API] ) {
    return next(action);
  }
  let request = action[CALL_API];
  let { getState } = store;
  let deferred = Promise.defer();
  // 在这里处理 401 和认证
  let { method, url, successType } = request;
  superAgentmethod
    .end((error, resp)=> {
      if ( !error ) {
        next({
          type: successType,
          response: resp.body
        });
        if (_.isFunction(request.afterSuccess)) {
          request.afterSuccess({ getState });
        }
      }
      deferred.resolve();
    });
  return deferred.promise;
};
```

既然我们已经有了上面的内容，我们可以对第一个页面中的原始 action 进行更改，如下所示：

```javascript
export const LOADED_ANSWERS = 'LOADED_ANSWERS';
export function loadAnswers() {
  return {
    [CALL_API]: {
      method: 'get',
      url: 'http://localhost:3000/answers',
      successType: LOADED_ANSWERS
    }
  };
}
```

我们在第一个页面中的函数将变为如下：

```javascript
import React, { Component, PropTypes } from 'react';
import { connect } from 'react-redux';
import { loadQuestions } from 'actions/answers';
import _ from 'lodash';
class Answer extends Component {
  static fetchData({ store }) {
    return store.dispatch(loadAnswers());
  }
  //...
}
```

至此你就完成了。网页的加载速度将变得更快。

# 第 4 章- 创建 Chrome 扩展

React 是人们实现应用前端部分的最佳方式之一。通过它，UI 的每个组件都可以独立实现。这意味着复杂性将会降低，并且理解应用程序的工作原理将变得容易得多。

我们需要为项目使用下面给出的项目结构：

```
notes/
  app/
    coffee/
      Johnlist_listing.coffee
    scss/
      Johnlist_listing.scss
  res/
    manifest.json
  package.json
  Brocfile.js
```

## Package.json

这将用于创建项目并管理我们的外部依赖。让我们从一个空文件开始，然后添加我们的依赖：

```json
{
  "name": "notes",
  "description": "chrome extension",
  "version": "0.0.1",
  "author": "Nicholas",
  "license": "ISC",
  "main": "",
  "private": true,
  "scripts": {},
  "dependencies": {}
}
```

我们应该开始添加要使用的库。首先可以如下方式安装 React：

```bash
npm install --save-dev react-dom
```

在我们的 React 文件中，我们将使用 JSX 和 coffeeScript。我们需要想出一种机制，将这些文件如何转换为 JavaScript，以便浏览器能够理解并运行它们。Broccoli 可以用于此目的。要安装它，导航到你的项目目录然后执行以下命令：

```bash
npm install -g broccoli-cli
npm install --save-dev broccoli
```

安装 broccoli 之后，必须安装所有需要的库。这是我们能够处理 SASS 和 coffee 文件的唯一方法。可以使用以下命令：

```bash
npm install --save-dev broccoli-sass broccoli-fast-browserify broccoli-merge-trees broccoli-funnel coffee-reactify
```

## Manifest 文件

这将是我们的扩展的核心。它如下：

```json
{
  "manifest_version": 2,
  "name": "Johnlist Notes",
  "description": "这是一个扩展程序，允许你编写关于 Johnlist 列表的笔记，然后在我们的页面上查看这些笔记",
  "version": "1.0",
  "permissions": [
    "activeTab"
  ],
  "content_scripts": [
    {
      "matches": ["**/*"],
      "js": ["Johnlist_listing.js"],
      "css": ["Johnlist_listing.css"]
    }
  ]
}
```

`content_scripts` 属性负责告诉 Chrome 扩展运行的。

## 使用 Broccoli 构建

我们需要告诉 Broccoli 如何构建我们的项目。如下所示：

```javascript
// 导入一些插件
var sass = require('sass');
var mergeTrees = require('merge-trees');
var Funnel = require('funnel');
var browserify = require('fast-browserify');
var reactify = require('reactify');

// 编译 Sass 和 coffee 文件
var clListingStyle = sass('app/scss', {
  destDir: 'dist'
});

var scripts = browserify('app/coffee', {
  entry: 'Johnlist_listing',
  transform: [
    reactify
  ],
  destDir: 'dist'
});

var resourceFiles = new Funnel('res', {
  destDir: 'dist'
});

// 将编译后的样式和脚本合并到一个输出目录
module.exports = mergeTrees([clListingStyle, scripts, resourceFiles]);
```

## Content Scripts

我们的目标是创建 SASS 和 coffee 文件，它们将为我们提供扩展的实际功能。如下：

```javascript
ReactDOM = require 'react-dom'
React = require 'react'
CLNotes = React.createClass({
  displayName: 'MyNotes'
  getInitialState: ->
    notes: []
  render: ->
    <div>
      <NotesDisplay mynotes={@state.notes} />
      <NoteInput saveNote={@saveNote} />
    </div>
  saveNote: (mynote) ->
    mynotes = @state.notes
    notes.push(mynote)
    @setState
      notes: mynotes
})

NoteInput = React.createClass({
  displayName: 'NoteInput'
  getInitialState: ->
    note: ''
  render: ->
    <div>
      <input type='text' value={@state.note} onChange={@noteChanged} />
      <button onClick={@saveNote}>Save</button>
    </div>
  noteChanged: (event) ->
    mynote = event.target.value
    @setState
      note: mynote
  saveNote: ->
    @props.saveNote(@state.note)
    @setState
      note: ''
})

NotesDisplay = React.createClass({
  displayName: 'NotesDisplay'
  render: ->
    <div id='notesDisplay'>
      {
        @props.notes.map (mynote, j) ->
          <div key={j}>
            {mynote}
          </div>
      }
    </div>
})
```

# 我们正在寻找 `mapAndAttr` div，然后将我们自己的 div 作为其子元素插入，
# 然后我们将在新的 div 中渲染 React 组件

attributesDiv = window.document.getElementsByClassName('mapAndAttrs')?[0]

if attributesDiv

  notesDiv = document.createElement('div')
```




```javascript
notesDiv.id='clNotes'

attributesDiv.appendChild(notesDiv)

ReactDOM.render(
  <CLNotes />
  document.getElementById('clNotes')
)
```

注意，我们已经从顶层 React 组件开始了。这是 `CLNotes`。它由两个子组件组成。其中一个用于放置新笔记，另一个用于显示现有的笔记。

我们现在需要创建 `craigslist_listing.scss` 文件。它将用于用于设置组件的大小，并将背景设置为灰色。下文所示：

```scss
#clNotes {
  width: 350px;
  height: 350px;
  background-color: lightgrey;
  padding:20px;
}

#notesDisplay {
  width:280px;
  height: 240px;
  background-color: white;
  overflow-y: scroll;
}
```

我们现在需要安装并运行我们的 Chrome 扩展程序。我们必须先使用 `broccoli`，然后编译我们的文件。请在项目目录的终端中运行以下命令：

```bash
broccoli-timepiece dist/
```

通过上述命令，我们的项目将被编译到 `/dist` 目录，并且当项目发生任何变化时，它都会自动重新编译项目。

一旦完成上述命令的执行，打开你的 Chrome 浏览器并导航到目录 `chrome://extensions`。从右上角选择 `Developer mode`（开发者模式）。

# 第 5 章 - React.js 中的数据可视化

在本章中，我们将指导你如何为直方图添加鼠标悬停（mouse-over）交互。我们的客户端组件应该如下：

```javascript
'use strict';

var React = require('react/addons');
var cx = React.addons.classSet;
var ws = require('ws');
var Histogram = require('./transactions_by_date.jsx');
var History = require('./history.jsx');
var configuration = require('../transactions_by_date.js').config;
var histogram = require('../transactions_by_date.js').histogram;

module.exports = React.createClass({
  getInitialState: function() {
    return {
      histogram: hist(new ArrayBuffer(config.TOTAL_BYTES)),
    };
  },
  componentDidMount: function() {
    var wsc = new ws('ws://localhost:8081');
    wsc.binaryType = 'arraybuffer';
    wsc.onmessage = function(message) {
      this.setState({ histogram: hist(message.data) });
    }.bind(this);
  },
  render: function() {
    return (
      <div className="container">
        <div className="row">
          <div className="col-xs-12">
            <h1> Visualization of Scalable Data </h1>
            <h2>Total Bitcoins per day </h2>
          </div>
        </div>
        <br />
        <div className="row">
          <div className="col-xs-12">
            <Histogram
              data={ this.state.histogram }          
            />
          </div>
          <div className="col-xs-12">
            <History
              now={ this.state.histogram.domain[1] }
            />
          </div>
        </div>
      </div>
    );
  }
});
```

我有一个 websocket 模块和 `React`，以及一些 React 组件。我们的直方图是一个实时更新的柱状图，它是按日期划分的交易表示。让我们从一个用于直方图大小的空数组开始。下文所示：

```javascript
histogram: hist(new ArrayBuffer(config.TOTAL_BYTES)),
```

考虑下面的代码，我们将能够将直方图设置为任何返回的消息。服务器将负责构建我们数据的类型化数组表示形式，然后将其推送到 web socket。

```javascript
wsc.onmessage = function(message) {
  this.setState({ histogram: hist(message.data) });
}.bind(this);
```

我们现在需要为我们的组件添加一个 `hoverDate` 状态。下文所示：

```javascript
histogram: hist(new ArrayBuffer(config.TOTAL_BYTES)),
hoverDate: null
```

让我们添加一个函数，在悬停时放置一个日期。下文所示：

```javascript
onHover: function(date) {
  this.setState({hoverDate: date});
},
```

我们想要跟踪在组件上悬停的数据。这应该像下面所示作为属性传递到组件中：

```javascript
<History
  now={ this.state.histogram.domain[1] }
  onHover={this.onHover}
/>
```

上面的代码可以这样使用：

```javascript
'use strict';
var React = require('react/addons');
var ReactSTransitionGroup = React.addons.CSSTransitionGroup;
var moment = require('moment');
var events = [
  [new Date(2015, 0, 5), 'Genesis block: 18:15:05 GMT'],
  [new Date(2015, 0, 7), ' Bitcoin v.1 '],
  [new Date(2015, 0, 12), ' First transaction '],
];
events.reverse(); // 反转事件
module.exports = React.createClass({
  render: function() {
    return (
      <ul className="list">
        <ReactSTransitionGroup trans="history">
          {events.map(function(event) {
            var date = event[0];
            var text = event[1];
            return (
              <li
                key={date.getTime()}
                onMouseEnter={this.props.onHover(date)}
                onMouseOut={this.props.onHover(null)}
                style={{
                  backgroundColor: this.props.hoverDate === date ? '#b07' : 'white',
                  color: this.props.hoverDate === date ? 'white' : 'black'
                }}
              >
                <span className="label">
                  {moment(date).calendar()}
                </span>
                {text}
              </li>
            );
          }.bind(this))}
        </ReactSTransitionGroup>
      </ul>
    );
  }
});
```

我们现在需要实现直方图如何被高亮的机制。下文所示：

```javascript
'use strict';
//external deps
var React = require('react');
var d3 = require('d3');
var moment = require('moment');
// internal deps
var Axis = require('./axis.jsx');
var Bars = require('./bars.jsx');
module.exports = React.createClass({
  render: function() {
    var data = this.props.data;
    var values = data.getValues();
    var width = 630;
    var height = Math.floor(width/2);
    if (data.domain[0] === 0) {
      // 我们没有数据
      return (
        <div>
          <span>Loading...&nbsp;</span>
          <span className="glyphicon glyphicon-time" aria-hidden="true"></span>
        </div>
      );
    }
    var scales = {
      x: d3.scale.linear().domain([0, data.getBin(data.domain[1])]).range([0, width]),
      y: d3.scale.linear().domain([0, d3.max(values)]).range([0, height])
    };
    return (
      <div className={'histogram ' + this.props.className}>
        <svg
          width={width + 100}
          height={height + 100}
        >
          <Axis
            scale={scales.x}
            displayScale={
```




```javascript
d3.time.scale.utc()
  .domain([new Date(data.domain[0]), new Date(data.domain[1])])
  .range([0, data.getBin(data.domain[1])])
}
tickFormatter={
  function(date) { return moment(date).format('MMM YY'); }
}
x={100}
y={height+1}
axis='x'
/>
<Axis
  scale={scales.y}
  displayScale={
  d3.scale.linear().domain([d3.max(values), 0]).range([0, d3.max(values)])
  }
  tFormatter={
  function(t) { return t.toLocaleString(); }
}
x={99}
y={0}
axis='y'
/>
<Bars
  data={data}
  width={width}
  height={height}
  scales={scales}
  zmIn={this.zoomIn}
/>
</svg>
</div
);
}
});
```

我们现在在组件中拥有了一些轴和一组柱状图。我们的目标是突出柱状图：

```javascript
<Bars
  data={data}
  width={width}
  height={height}
  scales={scales}
  zmIn={this.zoomIn}
/>
```

柱状图的类如下：

```javascript
'use strict';

// 我们的外部依赖
var React = require('react');

// 工具函数
function regularArray(tpdArray) {
  // TODO -- 解决如何整洁地对类型数组进行映射
  // 而需复制到普通数组
  var array = new Array(tpdArray.length);
  for (var j=0; j<typedArray.length; j++) {
    array[j] = tpdArray[j];
  }
  return array;
}
function translate(x, y) {
  return 'translate(' + x + 'px,' + y + 'px)';
}
module.exports = React.createClass({
  render: function() {
    var data = this.props.data;
    var values = regularArray(data.getValues());
    return (
      <g style={{transform: 'translateX(10px)'}}>
        {values.map(function(value, idx) {
          var click = null;
          if (data.bucket !== 0 && idx === 0) {
            // 让第一根柱子可，以便深入研究结果
            click = this.props.zmIn;
          }
          var scWidth = (this.props.width/(data.getBin(data.domain[1]))) + 0.5;
          return (
            <rect
              fill='#a8cc4'
              key={idx}
              x={0}
              y={0}
              width={1} /* 使用 CSS transform 调整尺寸 */
              height={1} /* 使用 CSS transform 以允许过渡效果 */
              style={{
                cursor: click === null ? 'auto' : 'pointer',
                transform: translate(
                  this.props.scales.x(idx),
                  this.props.height - this.props.scales.y(value)
                ) + ' scaleY(' + this.props.scales.y(value) + ')' + ' scaleX(' + scaleWidth + ')'
              }}
              onClick={click}
            />
          );
        }.bind(this))}
      </g>
    );
  }
});
```

## 数据管道连接

我们的调试器应该如下所示：

```javascript
var scales = {
  x: d3.scale.linear().domain([0, data.getBin(data.domain[1])]).range([0, width]),
  y: d3.scale.linear().domain([0, d3.max(values)]).range([0, height])
};
debugger;
return (
…
```

高亮索引应该如下所示：

```javascript
<Histogram
  data={ this.state.histogram }
  highlightIdx={
    this.state.hoverDate === null ? null : (
      Math.floor((this.state.hoverDate - new Date(this.state.histogram.domain[0]))) / (1000 * 60 * 24))
    )
  }
/>
```

随后，`highlightIdx` 将按如下方式传递给我们的柱状图：

```javascript
var hl = this.props.highlightIdx !== null && Math.abs(this.props.highlightIdx - idx) <= 1;
<Bars
  data={data}
  width={width}
  height={height}
  scales={scales}
  zmIn={this.zoomIn}
  highlightIdx={this.props.highlightIdx}
/>
```

我们现在想要确保柱状图在悬停时被高亮。只需重启服务器，然后重新加载页面。内容应该显示在窗口上。

# 第 6 章- 显示异常

我们可以显示来自 `flux` 分发器的异常。`Flux` 仅仅是由于 Facebook 创建的前端架构。`register` 方法用于接受回调函数。每当有 action 触发它时，回调函数就会被调用。分发器通常会忽略在回调中发生的异常。这是好事，因为失败的回调不会导致整个应用程序崩溃。然而，这使得调试过程变得异常困难。

我们需要在控制台中显示异常。我们应该首先定义一个函数来处理它们。我们应该首先定义一个函数来处理它们。如下所示：

```javascript
vm = function(f) {
  try {
    f.apply(this, arguments);
  } catch (ex) {
    console.error(ex);
  }
};
```
（注：由于原文提供的待翻译文本在后续部分出现了逻辑重复和断层，此处根据上下文对异常处理逻辑进行了还原与对齐）

# 第 7 章- 测试 React 组件

`Karma` 和 `webpack` 可以用于测试 React 组件。为了这一点，你必须安装必要的库；否则它将无法工作。

## 配置

`Karma` 将从 `karma.conf.js` 文件读取，我们应该首先进行设置。如下所示：

```javascript
pack = require('webpack');
module.exports = function (config) {
  config.set({
    browsers: [ 'Chrome' ], // 在 Chrome 中运行
    singleOnce: true, // 默认运行一次
    frameworks: [ 'mocha' ], // 使用 mocha 测试框架
    files: [
      'tests.webpack.js' // 加载此文件
    ],
    preprocessors: {
      'tests.webpack.js': [ 'webpack', 'sourcemap' ] // 使用 webpack 和 sourcemap 进行预处理
    },
    reporters: [ 'dots' ], // 以这种格式报告结果
    webpack: { // 复制 webpack 配置
      devtool: 'inline-source-map', // 使用内联源 map 而非默认
      module: {
        loaders: [
          { test: /\.js$/, loader: 'babel-loader' }
        ]
      }
    },
    webpackServer: {
      noInfo: true // 在 karma 运行时避免刷屏控制台
    }
  });
};
```

我们的下一步应该是创建一个文件，它将利用 `webpack` API 自动查找需要的文件。如下所示：

```javascript
c = require.context('./src', true, /-test\.js$/); // 目录和正则测试设置正确

c.keys().forEach(c);
```

我们现在需要编写一些测试。一个示例如下：

```javascript
var React = require('react');
var TtUtils = require('react/lib/ReactTestUtils'); // 使用 Test Utils 是好的，但也可以使用 DOM API
var expect = require('expect');
var Root = require('../root'); // 现场测试在 components/__tests__ 中进行，这是我组件所需的

describe('root', function () {
  it('渲染时没有问题', function () {
```




[content]

```javascript
var root = TtUtils.renderIntoDocument(<Root/>);

expect(root).toExist();
});
```

# 第 8 章- 构建滑动菜单

可以使用 React 和 LESS CSS 来创建一个滑动菜单。我们的目标是让菜单根据外部页面的动作，从左侧或右侧滑出。

在 React 中，有三个类可以用于渲染菜单。它们包括：

* `App`
* `Menu`
* `MenuItem`

## App

可以像下面所示那样使用：

```javascript
var Application = React.createClass({
    showLeft: function() {
        this.refs.left.show();
    },
    showRight: function() {
        this.refs.right.show();
    },
    render: function() {
        return <div>
            <button onClick={this.showLeft}>查看左侧菜单!</button>
            <button onClick={this.showRight}>查看右侧菜单!</button>
            <Menu ref="left" alignment="left">
                <MenuItem hash="first-page"> 第 1 页 </MenuItem>
                <MenuItem hash="second-page"> 第 2 页 </MenuItem>
                <MenuItem hash="third-page"> 第 3 页 </MenuItem>
            </Menu>
            <Menu ref="right" alignment="right">
                <MenuItem hash="first-page"> 第 1 页 </MenuItem>
                <MenuItem hash="second-page"> 第 2 页 </MenuItem>
                <MenuItem hash="third-page"> 第 3 页 </MenuItem>
            </Menu>
        </div>;
    }
});
```

在上面的示例中，我们只向应用添加了菜单。其中一个将从右侧滑动，另一个从左侧滑动。这些参数的规范是通过属性 `alignment` 完成的。

我们在 `Menus` 内部创建了 `MenuItem` 类实例。用户可以点击这些菜单项来执行某些操作。在我们的案例中，操作很可能是导航到某个 hash，这通过在类声明中使用 `hash` 属性来完成。

## Menu

可以像下面所示那样使用：

```javascript
var Menu = React.createClass({
    getInitialState: function() {
        return {
            visible: false 
        };
    },
    show: function() {
        this.setState({ visible: true });
        document.addEventListener("click", this.hide.bind(this));
    },
    hide: function() {
        document.removeEventListener("click", this.hide.bind(this));
        this.setState({ visible: false });
    },
    render: function() {
        return <div className="menu">
            <div className={(this.state.visible ? "visible " : "") + this.props.alignment}>{this.props.children}</div>
        </div>;
    }
});
```

`Menu` 类负责渲染我们的实际菜单，并根据 `hide` 和 `show` 方法的调用情况切换我们实际菜单的可见性。`getInitialState` 方法表明我们的菜单默认是隐藏的。`show` 方法用于将菜单的可见性设置为 true。

## MenuItem

可以像下面所示那样使用：

```javascript
var MnItem = React.createClass({
    navigate: function(hash) {
        window.location.hash = hash;
    },
    render: function() {
        return <div className="menu-item" onClick={this.navigate.bind(this, this.props.hash)}>{this.props.children}</div>;
    }
});
```

`MenuItem` 类负责渲染项目并处理点击动作。

## CSS

可以像下面所示那样使用：

```css
.menu {
  display:block;
  @menu-width:50px;
  >div {
    position:absolute;
    top:0;
    z-index:2;
    width:@menu-width;
    .border-box;
    height:100%;
    .transition(-webkit-transform ease 250ms);
    .transition(transform ease 250ms);
    &.left {
      background:#284D7A;
      left:@menu-width*-1;
    }
    &.visible.left {
      .transform(translate3d(@menu-width, 0, 0));
    }
    &.right {
      right:@menu-width*-1;
      background:#6B2828;
    }
    &.visible.right {
      .transform(translate3d(@menu-width*-1, 0, 0));
    }
    >.menu-item {
      float:left;
      width:100%;
      margin:0;
      padding:15px 20px;
      border-bottom:solid 1px #555;
      cursor:pointer;
      .border-box;
      color:#F0B0B0;
      &:hover {
        color:#F0F0F0;
      }
    }
  }
}
```

我们需要抽象掉任何令人讨厌的厂商前缀。这就是为什么我们使用了不同的 LESS CSS 混入。

# 第 9 章- 创建下拉列表

可以使用 Font Awesome、LESS CSS 和 React JS 来创建一个下拉列表。它使用 LESS CSS 是为了提供良好的动画。

## React

可以像下面所示实现：

```javascript
var Dropdown = React.createClass({
    getInitialState: function() {
        return {
            visible: false 
        };
    },
    select: function(item) {
        this.props.selected = item;
    },
    show: function() {
        this.setState({ visible: true });
        document.addEventListener("click", this.hide);
    },
    hide: function() {
        this.setState({ visible: false });
        document.removeEventListener("click", this.hide);
    },
    render: function() {
        return <div className={"dropdown-container" + (this.state.visible ? " show" : "")}>
            <div className={"dropdown-display" + (this.state.visible ? "" : "")} onClick={this.show}>
                <span style={{ color: this.props.selected.hex }}>{this.props.selected.name}</span>
                <i className="fa fa-angle-down"></i>
            </div>
            <div className="dropdown-list">
                {this.renderListItems()}
            </div>
        </div>;
    },
    renderListItems: function() {
        var items = [];
        for (var j = 0; j < this.props.list.length; j++) {
            var it = this.props.list[j];
            items.push(<div onClick={this.select.bind(null, it)}>
                <span style={{ color: it.hex }}>{it.name}</span>
            </div>>);
        }
        return items;
    }
});

var colours = [{
    name: "Blue",
    hex: "#1B66F2"
}, {
    name: "Red",
    hex: "#F21B1B"
}, {
    name: "Green",
    hex: "#07BA16"
}];
React.render(<Dropdown list={colours} selected={colours[0]} />, document.getElementById("container"));
```

我们通过调用 `createClass` 开始创建 `DropDown` 类。`getInitialState` 用于设置创建的状态，它接收两个属性：`list` 和 `selected`。`list` 指定了用户点击下拉列表时要显示的项目。`selected` 属性指定了当前选中的项目。

React 的 `render` 方法用于渲染下拉列表。注意它将具有我们指定的颜色。

## LESS CSS

可以像下面所示那样使用：

```css
@height:50px;
@spacing:20px;
@select-colour:#2775C7;
@font-size:15px;
@border-colour:#DDD;
div.dropdown-container {
  &.show>div.dropdown-list {
    .transform(scale(1, 1));
  }
  @icon-width:15px;
  >dropdown-display {
    float:left;
    width:100%;
    background:white;
    height:@height;
    cursor:pointer;
    border:solid 2px @border-colour;
    .border-box;
    >** {
      float:left;
      height:100%;
      .vertical-centre(@height);
    }
    >span {
      font-size:@font-size;
      width:100%;
      position:relative;
      .border-box;
      padding-right:@icon-width+@spacing*2;
      padding-left:@spacing;
    }
    >j {
      position:relative;
      width:@icon-width;
      margin-left:(@spacing+@icon-width)*-1;
    }
  }
}
```





## CSS

在 CSS 部分，我们刚刚设置了下拉菜单的视觉效果和交互。

```css
font-size:1.125em;
font-weight:bold;
padding-right:@spacing;
text-align:right;
}
}
```

```css
div.dropdown-list {
    float:left;
    width:100%;
    position:relative;
    width:100%;
    .transform(scale(1, 0));
    .transition(-webkit-transform ease 250ms);
    .transition(transform ease 250ms);
    >div {
        position:absolute;
        width:100%;
        z-index:2;
        cursor:pointer;
        background:white;
        >div {
            float:left;
            width:100%;
            padding:0 @spacing;
            font-size:@font-size;
            .border-box;
            border:solid 2px @border-colour;
            border-top:none;
            @icon-width:21px;
            &:hover {
                background:#F0F0F0;
            }
            &.selected {
                background:@select-colour;
                color:white;
            }
            >* {
                .vertical-centre(@height);
            }
            >span {
                float:left;
                width:100%;
            }
        }
    }
}
```

# 第 10 章 - React JS 与架构

这两者可以结合起来创建一个简单的应用程序。Flux 为你提供了一种机制，用于你如何从服务器获取数据。在此期间，客户端保持了组件的严格解耦。由于使用了 React JS 和单向通信协议，实现了关注点分离，React JS 和 Flux 可以很好地配合使用。

## React

React 通常使用类（classes）。为了渲染某些 HTML，你必须创建一个 React 类，这将提供关于要渲染内容的描述。考虑下面这个 React 示例：

```javascript
var Hello = React.createClass({
    render: function() {
        return <div>Hello, there!</div>
    }
});
React.render(new Hello (), document.body);
```

注意，我们定义了一个 React 类并将其命名为 `Hello`。然后我们在该类中指定了 `render` 函数。如果我们需要在内部渲染 HTML，将调用此函数，JSX 将帮助我们在不需要编写单独模板的情况下在内部编写 HTML。上面代码的最后一行显示，我们需要在正文（body）中渲染我们的类。

## Props（属性）

假设我们需要向 React 类传递一些数据。这在我们之前的类中并没有提供。接下来的这个类演示了如何做到这一点：

```javascript
var Hello = React.createClass({
    render: function() {
        return <div>Hello, {this.props.name}</div>
    }
});
React.render(new Hello ({ name: "Joel" }), document.body);
```

在上面的类中我们引入了 `props`。这允许我们把数据传递到类的视图中。`prop` 的变化将导致视图的相应部分被渲染。这些变化可以来自父视图、视图本身或任何子视图。通过这种方式，数据可以在视图之间传递并保持同步。

## State（状态）

它可以像下面所示那样被使用：

```javascript
var Hello = React.createClass({
    getInitialState: function() {
        return {
            counter: 0
        };
    },
    increment: function() {
        this.setState({ counter: this.state.counter+1 });
    },
    render: function() {
        return <div>
            <div>{this.state.counter}</div>
            <button onClick={this.increment}>Increment</button>
        </div>;
    }
});
React.render(new Hello (), document.body);
```

React 类有一个状态（state），这就是我们在上面介绍的内容。这使得你能够跟踪对内部视图所作的更改。每当我们使用内部状态时，都需要 `getInitialState` 函数。它是对内部视图的一个指示，说明了我们的初始状态应该是怎样的。即使你有一个空状态，也请确保使用此函数。

当我们想要在父类和子类之间传递数据时，我们使用 `props`，并且当任何 prop 发生变化时，视图将再次渲染。这包括子类和父类。如果你的数据仅与视图有关，请使用 state。在这种情况下，所做的任何更改也将在视图中渲染。如果你的数据与视图之外的类有关，请随时使用私有变量，但个人而言，我会使用 state。

## 嵌套视图（Nested Views）

嵌套视图的概念让我们能够并且轻松地使用 React。通过这种方式，我们能够从其他 React 类内部渲染 React 类。下面是一个示例：

```javascript
var FnButton = React.createClass({
    render: function() {
        return <button onClick={this.props.onClick}>
            <i className={"fa " + this.props.icon}>i
            <span>{this.props.text}</span>
        </button>
    }
});

var Hello = React.createClass({
    getInitialState: function() {
        return {
            counter: 0
        };
    },
    increment: function() {
        this.setState({ counter: this.state.counter++ });
    },
    render: function() {
        return <div>
            <div>{this.state.counter}</div>
            <FancyButton icon="arrow-circle" onClick={this.increment}
```

在上面的类中，按钮被抽象化以增加计数器。请考虑下面这个可以工作的 flux 示例：

```javascript
var Count = React.createClass({
    getInitialState: function() {
        return {
            items: []
        };
    },
    componentWillMount: function() {
        emitter.on("store-changed", function(items) {
            this.setState({ items: items });
        }.bind(this));
    },
    componentDidMount: function() {
        dispatcher.dispatch({ type: "get-items" });
    },
    render: function() {
        var items = this.state.items;
        return <div>{items.length}</div>;
    }
});
```

var Store = function() {
    dispatcher.register(function(pd) {
        switch (pd.type) {
            case "get-items":
                this._all();
                break;
        }
    }.bind(this));

    this._all = function() {
        $.get("/some/url", function(its) {
            this._notify(its);
        }.bind(this));
    }

    this._notify = function(its) {
        emitter.emit("store-changed", its);
    }
};

var ItemStore = new Store();

我们的应用程序只有一个页面，显示如下：

"use strict";

var Todo = React.createClass({
    getInitialState: function() {
        return {
            todos: []
        };
    },
    componentWillMount: function() {
        emitter.on(constants.changed, function(tds) {
            this.setState({ todos: tds });
        }.bind(this));
    },
    componentDidMount: function() {
        dispatcher.dispatch({ type: constants.all });
    },
    componentsWillUnmount: function() {
        emitter.off(constants.all);
    },
    create: function() {
        this.refs.create.show();
    },
    renderList: function(complete) {
        return <List tds={_.filter(this.state.tds, function(y) { return y.isComplete === complete; })} />;
    },
    render: function() {
        return <div className="container">
            <div className="row">
```





```html
<div className="col-md-8">
  <h1>Todo List</h1>
</div>
<div className="col-md-4">
  <button type="button" className="btn btn-primary pull-right spacing-top" onClick={this.create}>新任务</button>
</div>
<div className="row">
  <div className="col-md-6">
    <h2 className="spacing-bottom">未完成</h2>
    {this.renderList(false)}
  </div>
  <div className="col-md-6">
    <h2 className="spacing-bottom">已完成</h2>
    {this.renderList(true)}
  </div>
</div>
<Modal ref="create" />
</div>;
});
```

## 列表

它应该是如下：

```javascript
var L = React.createClass({
  renderItems: function() {
    return _.map(this.props.todos, function(td) {
      return <Item todo={td} />;
    });
  },
  render: function() {
    return <ul className="list-group">
      {this.renderItems()}
    </ul>;
  }
});
```

# 结论

可以得出结论，React 是一个非常有用的框架，可用于 Web 应用开发。该框架非常动态，可以与其他工具和框架结合，以创建非常出色且复杂的应用程序。

这些工具包括 `Flux`、`Redux` 等。当这些工具与 `React` 结合时，使其能够处理复杂的状态。你还会发现创建一个可滚动表格并向其中添加内容非常容易。这意味着你能够向表格添加大量内容。你还可以在 `React` 应用的服务器端渲染或显示内容。此时，正如本书中所讨论的，你应该能够使用 `React` 创建 Chrome 扩展程序了。此外，显示应用程序中发生的异常对你也有好处。

本书提供了关于如何进行这些操作卓越指南。`React` 组件也需要进行测试，这应该非常小心地完成。你还可以使用 `React` 创建下拉列表。这些功能在书中都已过探索，你应该熟悉它们。

