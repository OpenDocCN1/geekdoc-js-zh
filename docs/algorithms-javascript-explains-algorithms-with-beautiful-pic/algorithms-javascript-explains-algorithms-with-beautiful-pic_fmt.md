# JavaScript 算法：用精美图片轻松易学地解释算法

# 算法 JavaScript

![](img/4e0bf091f4d81b2977c8fb9210bf9760_1_0.png)

## YANG HU

智慧始简单，实践归于本质。本书旨在简要地阐述概念，生动地培养编程兴趣，深入分析数据结构、算法、JavaScript 以及编程的乐趣。

[http://en.verejava.com](http://en.verejava.com)

# 线性表定义

线性表：元素序列，是一维数组。

## 1. 定义一个存储学生分数的一维数组

![](img/4e0bf091f4d81b2977c8fb9210bf9760_0_0.png)

Algorithms Explain With Beautiful Pictures(用精美图片解释算法)

# 线性表 JavaScript (Linear Table JavaScript)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_4_0.png)

定义一个存储学生分数的一维数组

## 创建 `TestOneArray.html` 文件，使用记事本打开它在浏览器中运行。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_4_1.png)

结果：

# 最大值

整数序列的最大值：<img src='60_50_95_80_70.png'>

## 1. 算法思路 (Algorithmic ideas)

比较 `arrays[i]` 与 `arrays[i + 1]`，如果 `arrays[i] > arrays[i + 1]` 则交换它们。一直继续直到最后一个数字，此时 `arrays[length - 1]` 即为最大值。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_5_0.png)

图片：Maximum of Integer Sequences(整数序列的最大值)

## 1. 创建 `TestMaxValue.html` 使用记事本打开它在浏览器中运行。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_6_0.png)

结果：

# 冒泡排序算法 (Bubble Sorting Algorithm)

## 冒泡排序算法：

比较 `arrays[j]`与`arrays[j + 1]`，如果 `arrays[j] > arrays[j + 1]`则交换。剩余元素重复此过程，直到完成排序。

## 将以下数字从大到小排序（或从小到大） 

*(原文为"from small to large"即从小到大)*

![](img/4e0bf091f4d81b2977c8fb9210bf9760_7_0.png)

图片

**解释：**

- 未排序，
- 比较中，
- 已排序

## 第一步排序： (First sorting:)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_8_0.png)

图片

## Step: Second sorting(第二步排序):

![](img/4e0bf091f4d81b2977c8fb9210bf9760_9_0.png)

图片

## 第三步排序 (Third sorting:)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_10_0.png)

图片

## 无交换则排序：我们可以从小到大获得排序后的数字。

## 创建 `TestBubbleSort.html` 使用记事本打开在浏览器中运行。

```javascript
<script type="text/javascript">
class BubbleSort{
    static sort(arrays) {
        for (var i = 0; i < arrays.length - 1; i++) {
            for (var j = 0; j < arrays.length - i - 1; j++) {
                //swap
                if (arrays[j] > arrays[j + 1]) {
                    var flag = arrays[j];
                    arrays[j] = arrays[j + 1];
                    arrays[j + 1] = flag;
                }
            }
        }
    }
}
var scores = [60, 50, 95, 80, 70 ];
BubbleSort.sort(scores);
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ",");
}
</script>
```

结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_12_0.png)

图片 50,60,70,80,95,(排序后的数组)

# 最小值 (Minimum Value)

搜索整数序列中的最小值：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_13_0.png)

图片

**算法思路：**

初始 `minIndex=0`, `j=1`，比较 `arrays[minIndex]` 与 `arrays[j]`；如果 `arrays[minIndex] > arrays[j]` 则最小索引更新为当前值（`minIndex=j`），否则保持原状。继续遍历末尾元素，此时数组下标 `minIndex`的元素为`Min Value`（最小值）。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_14_0.png)

图片

## 创建 `TestMinValue.html` 使用记事本打开在浏览器中运行。

```javascript
<script type="text/javascript">
function min(arrays){
    var minIndex = 0; //最小值的索引
    for (var j = 1; j < arrays.length; j++) {
        if (arrays[minIndex] > arrays[j]){
            minIndex = j;
        }
    }
    return arrays[minIndex];
}
var scores = [60, 80, 95, 50, 70 ];
var minValue = min(scores);
document.write("Min Value ="minValue);
</script>
```

结果： 

![](img/4e0bf091f4d81b2977c8fb9210bf9760_15_0.png)

图片 (结果显示：Min = 50 )

# 选择排序算法

## 选择排序算法（Select Sorting Algorithm）：

通过重复找出未排序部分的最小元素并将其放在开头，对数组进行排序。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_16_0.png)

图片

**解释：**

- 无交换（未处理），
- 比较中，
- 已排序。

## 第一步：第一组元素的最小值已经找到了！将最小值放在开头。(First sorting:) ![](img/4e0bf091f4d81b2977c8fb9210bf9760_17_0.png)

图片

## Select Sorting Algorithm(选择排序详细步骤)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_18_0.png) (Step 1: Move minimum to front.)

图片

## Select Sorting Algorithm (第二步排序：Second sorting:) ![](img/4e0bf091f4d81b2977c8fb9210bf9760_19_0.png)

图片

## 第三步（Third sorting):

![](img/4e0bf091f4d81b2977c8fb9210bf9760_20_0.png) (Step 3: Move to front)

## 可以从小到大获得排序后的数字

```javascript
<script type="text/javascript">
class SelectSort{
    static sort(arrays) {
        var len = arrays.length - 1;
        var minIndex;// Save the index of selected minimum
        for (var i = 0; i < len; i++) {
            minIndex = i;
            //Save the minimum value of each loop as the first element
            var minValue = arrays[minIndex];
            for (var j = i; j < len; j++) {
                if (minValue > arrays[j]) { // minimum value exchange with minIndex
                    minValue = arrays[j];
                    minIndex = j;
                }
            }
            //if minimum index changes, current minimum is exchanged with minIndex
            if (i != minIndex){
                var temp = arrays[i];
                arrays[i] = arrays[minIndex];
                arrays[minIndex] = temp;
            }
        }
    }
}
var scores = [90, 70, 50, 80, 60, 85 ];
SelectSort.sort(scores);
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ", ");
}
</script>
```

结果：

50,60,70,80,85,90

# 线性表追加

1. 在数组 `scores` 末尾添加分数`75`。

**原始分数数组**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_23_0.png)

## 分析:

- 首先创建一个临时数组`tempArray`，大于`scores`数组的长度
- 将`scores`的每个值复制到`tempArray`
- 将`75`配给`tempArray`的最后索引位置
- 最后将`tempArray`指针引用分配给原始的`scores`;

1. 使用记事本创建一个 `TestOneArrayAppend.html`，然后在浏览器中打开它。

```javascript
<script type="text/javascript">
function append(array, value) {
    //create a new array, length = array.length + 1
    var tempArray = new Array(array.length + 1);
    for (var i = 0; i < array.length; i++) {
        tempArray[i] = array[i];
    }
    tempArray[array.length] = value;
    return tempArray;
}
var scores = new Array(90, 70, 50, 80, 60, 85 );
scores = append(scores, 75);
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ",");
}
</script>
```

结果:

![](img/4e0bf091f4d81b2977c8fb9210bf9760_24_0.png)

# 线性表插入

1. 在任何位置向一维数组`scores`插入学生分数。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_25_0.png)

## 实现说明:

- 首先创建一个临时数组`tempArray`，大于`scores`数组长度
- 将`scores`数组从开始到插入位置之前的每个值复制到`tempArray`
- 将`scores`数组从插入位置到末尾的每个值移动到`tempArray`并返回
- 然后将分数`75`插入到`tempArray`的索引中。
- 最后将`tempArray`指针引用分配给`scores`;

1. 使用记事本创建一个 `TestOneArrayInsert.html`，然后在浏览器中打开它。

```javascript
<script type="text/javascript">
function insert(array, score, insertIndex) {
    var tempArray = new Array(array.length + 1);
    for (var i = 0; i < array.length; i++) {
        if (i < insertIndex) {
            tempArray[i] = array[i];
        } else {
            tempArray[i + 1] = array[i];
        }
    }
    tempArray[insertIndex] = score;
    return tempArray;
}
// 示例调用略...
```

```markdown
![](img/4e0bf091f4d81b2977c8fb9210bf9760_28_0.png)

## 分析:

- 创建一个比 `scores` 短小的临时数组 `tempArray`。
- 将 `i=2` 之前的数据复制到 `tempArray` 的前端
- 复制 `i=2` 之后的数组到 `tempArray` 的末端
- 分配 `tempArray` 指针引用给 `scores`
- 输出 `scores`

## 1. 使用记事本创建一个 `TestOneArrayDelete.html`，然后在浏览器中打开它。

```
<script type="text/javascript">
    function remove(array, index){
        // create a new array, length = array.length - 1
        var tempArray = new Array(array.length - 1);

        for (var i = 0; i < array.length; i++) {
            if (i < index) // Copy the data in front of index to the front of tempArray
                tempArray[i] = array[i];
            if (i > index) // Copy the array after index to the end of tempArray
                tempArray[i - 1] = array[i];
        }
        return tempArray;
    }

    ////////////////////testing////////////////////
    var scores = new Array( 90, 70, 50, 80, 60, 85 );

    scores = remove(scores, 2);//delete score that index = 2

    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }
</script>
```

**结果:**

90,70,80,60,85,

## 插入排序算法

### 插入排序算法:

取数组中一个未排序的新元素，与之前已排序的元素进行比较，如果新元素小于已排序的元素，则插入新元素到正确位置。

**将以下数字从从小到大进行排序**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_31_0.png)

**解释:**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_31_1.png)

### 1. 第一次排序:

![](img/4e0bf091f4d81b2977c8fb9210bf9760_32_0.png)

### 2. 第二次排序:

![](img/4e0bf091f4d81b2977c8fb9210bf9760_32_1.png)

### 3. 第三次排序:

![](img/4e0bf091f4d81b2977c8fb9210bf9760_33_0.png)

### 4. 第四次排序:

![](img/4e0bf091f4d81b2977c8fb9210bf9760_33_1.png)

1. 使用记事本创建一个 `TestInsertSort.html`，然后在浏览器中打开它。

```
<script type="text/javascript">
    class InsertSort{
        static sort(arrays) {
            for (var i = 0; i < arrays.length; i++) {
                var insertElement = arrays[i];//Take unsorted new elements
                var insertPosition = i; //Inserted position
                for (var j = insertPosition - 1; j >= 0; j--) {
                    //If the new element is smaller than the sorted element,
                    // shifted to the right
                    if (insertElement < arrays[j]) {
                        arrays[j + 1] = arrays[j];
                        insertPosition--;
                    }
                }
                arrays[insertPosition] = insertElement;//Insert the new element
            }
        }
    }

    ///////////////////testing/////////////////////

    var scores = [ 90, 70, 50, 80, 60, 85 ];
    InsertSort.sort(scores);
    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }
</script>
```

**结果:**

50,60,70,80,85,90

## 反转数组

有序序列的倒序：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_35_0.png)

### 1. 算法思路

初始 `i = 0`，然后交换第一个元素 `arrays[i]` 与最后一个元素 `arrays[length - i - 1]`。重复直到中间索引 `i == length / 2`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_36_0.png)

### 1. 使用记事本创建一个 `TestReverse.html`，然后在浏览器中打开它。

```
<script type="text/javascript">
  function reverse(arrays) {
    var length = arrays.length;
    var middle = length / 2;
    for (var i = 0; i <= middle; i++) {
      var temp = arrays[i];
      arrays[i] = arrays[length - i - 1];
      arrays[length - i - 1] = temp;
    }
  }

  ///////////////////testing////////////////

  var scores = [ 50, 60, 70, 80, 90 ];
  reverse(scores);
  for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ",");
  }
</script>
```

**结果:**

90,80,70,60,50,

## 线性查找

1. 请输入想要查找的值，例如 `70`，返回索引。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_38_0.png)

2. 使用记事本创建一个 `TestOneArraySearch.html` 文件，并在浏览器中打开。

```javascript
<script type="text/javascript">
    function search(array, value) {
        for (var i = 0; i < array.length; i++) {
            if (array[i] == value) {
                return i;
            }
        }
        return -1;
    }
    ///////////////////testing////////////////
    var scores = new Array( 90, 70, 50, 80, 60, 85 );
    var value = 70;
    var index = search(scores, value);

    if (index > 0) {
        document.write("Found value: " + value + " the index is: " + index);
    }else{
        document.write("The value was not found : " + value);
    }
</script>
```

**结果：**

Found value: 70 the index is: 1

## 折半查找（二分查找）

**折半查找（二分查找）：**从已排序的数组中找到值的位置。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_40_0.png)

1. 初始化最低索引 `low=0`，最高索引 `high=scores.length-1`。
2. 找到中间索引 `mid=(low+high)/2` 的 `scores[mid]` 作为 `searchValue`。
3. 将 `scores[mid]` 与 `searchValue` 进行比较：
   - 如果 `scores[mid]==searchValue`，则打印当前的 `mid` 索引。
   - 如果 `scores[mid]>searchValue`，则 `searchValue` 将在 `low` 到 `mid-1` 之间找到。
4. 依此类推。重复步骤3，直到找到 `searchValue` 或者 `low>=high` 终止循环。

**示例 1：在已排序的数组中查找 `searchValue=40` 的索引。**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_41_0.png)

**示例 2：在已排序的数组中查找 `searchValue=90` 的索引。**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_42_0.png)

1. 使用记事本创建一个 `TestBinarySearch.html` 文件，并在浏览器中打开。

```javascript
<script type="text/javascript">
class BinarySearch{
  static search(arrays, searchValue) {
  var low = 0;
  var high = arrays.length - 1;
  var mid = 0;
  while (low <= high) {
     mid = (low + high) / 2;
     if (arrays[mid] == searchValue) {
     return mid;
     } else if (arrays[mid] < searchValue) {
     low = mid + 1;
     } else if (arrays[mid] > searchValue) {
     high = mid - 1;
     }
     }
     return -1;
  }
}
/////////////////testing//////////////
var scores = [30, 40, 50, 70, 85, 90, 100];
var searchValue = 40;
var position = BinarySearch.search(scores, searchValue);
document.write(searchValue + " position:" + position);

document.write("<br>-----------------------------<br>");

searchValue = 90;
position = BinarySearch.search(scores, searchValue);
document.write(searchValue + " position:" + position);
</script>
```

**结果：**

40 position: 1

90 position: 5

## 希尔排序

**希尔排序：**希尔排序是一种高效的排序算法，基于插入排序算法。该算法避免了插入排序中可能发生的大量数据移动，例如当较小值位于最右侧需要移动到最左侧时的情况。

**通过希尔排序将以下数字从小到大排序**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_45_0.png)

**算法结果：** 根据下标的特定增量对数组分组，并对组进行插入排序。随着增量减小直至1时，整个数据完成排序。

1. 第一次排序：

   `gap = array.length / 2 = 5`

   ![](img/4e0bf091f4d81b2977c8fb9210bf9760_46_0.png)

   - 9 > 7 交换
   - 6 > 4 交换
   - 5 > 3 交换
   - 8 > 1 交换

2. 第二次排序：

   `gap = 5 / 2 = 2`

3. 第三次排序：

   `gap = 2 / 2 = 1`

   ![](img/4e0bf091f4d81b2977c8fb9210bf9760_48_0.png)

1. 使用记事本创建一个 `TestShellSort.html` 文件，并在浏览器中打开。

```javascript
<script type="text/javascript">
    function shellSort(array) {
        var middle = parseInt(array.length / 2);
        for (var gap =middle ; gap > 0; gap = parseInt(gap / 2)) {
            for (var i = gap; i < array.length; i++) {
                var j = i;
                while (j - gap >= 0 && array[j] < array[j - gap]) {
                    swap(array, j, j - gap);
                    j = j - gap;
                }
            }
        }
    }

    function swap(array, a, b) {
        array[a] = array[a] + array[b];
        array[b] = array[a] - array[b];
        array[a] = array[a] - array[b];
    }

    //////////////////testing////////////////
    var scores = [ 9, 6, 5, 8, 0, 7, 4, 3, 1, 2 ];
    shellSort(scores);
    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }
</script>
```

## 单向链表

单向链表（单链表）：是线性表的一种链式存储结构，由节点连接而成。每个节点由数据域和指向下一个节点的指针域组成。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_50_0.png)

### UML 类图

![](img/4e0bf091f4d81b2977c8fb9210bf9760_50_1.png)
```

```javascript
class Node{
    constructor(data, next){
        this.data = data;
        this.next = next;
    }
    
    getData(){
        return this.data;
    }
}
```

### 1. 单向链表初始化。

**示例：构建旧金山地铁单向链表**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_50_2.png)

### 2. 遍历输出。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_51_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_51_1.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_51_2.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_51_3.png)

### 1. 使用`记事本`创建一个`TestUnidirectionalLinkedList.html`文件，并在浏览器中打开。

```javascript
<script type="text/javascript">
    class Node{
            constructor(data, next){
                this.data = data;
                this.next = next;
            }

            getData(){
                return this.data;
            }
        }

        class LinkedList{
            init() {
                // the first node called head node
                this.head = new Node("San Francisco", null);

                var nodeOakland = new Node("Oakland", null);
                this.head.next = nodeOakland;

                var nodeBerkeley = new Node("Berkeley", null);
                nodeOakland.next = nodeBerkeley;

                // the last node called tail node
                this.tail = new Node("Fremont", null);
                nodeBerkeley.next = this.tail;

                return this.head;
            }

            print(node) {
                var p = node;
                while (p != null) // From the beginning to
                // the end
                {
                    var data = p.getData();
                    document.write(data + " -> ");
                    p = p.next;
                }
                document.write("End<br><br>");
            }
        }

        ////////////////////testing////////////////////

        var linkedList = new LinkedList();
        var head = linkedList.init();
        linkedList.print(head);
    </script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_53_0.png)

### 3. 在末尾追加一个名为 `Walnut`的新节点。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_54_0.png)

### 1. 使用`记事本`创建一个`TestUnidirectionalLinkedListAppend.html`文件。

```javascript
<script type="text/javascript">
  class Node{
    constructor(data, next){
      this.data = data;
      this.next = next;
    }

    getData(){
      return this.data;
    }
  }

  class LinkedList{
    init() {
      // the first node called head node
      this.head = new Node("San Francisco", null);

      var nodeOakland = new Node("Oakland", null);
      this.head.next = nodeOakland;

      var nodeBerkeley = new Node("Berkeley", null);
      nodeOakland.next = nodeBerkeley;

      // the last node called tail node
      this.tail = new Node("Fremont", null);
      nodeBerkeley.next = this.tail;

      return this.head;
    }

    add(newNode) {
      this.tail.next = newNode;
      this.tail = newNode;
    }

    print(node) {
        var p = node;
        while (p != null) // From the beginning to the end
        {
            var data = p.getData();
            document.write(data + " -> ");
            p = p.next;
        }
        document.write("End<br><br>");
    }
  }

  ///////////////////testing////

  var linkedList = new LinkedList();
  var head = linkedList.init();

  document.write("Append new node name: Walnut to the end: <br>");
  linkedList.add(new Node("Walnut", null));

  linkedList.print(head);
</script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_56_0.png)

### 3. 在位置2插入`Walnut`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_57_0.png)

### 1. 使用`记事本`创建`TestUnidirectionalLinkedListInsert.html`

```javascript
<script type="text/javascript">
  class Node{
    constructor(data, next){
      this.data = data;
      this.next = next;
    }

    getData(){
      return this.data;
    }
  }

  class LinkedList{
    init() {
      // the first node called head node
      this.head = new Node("San Francisco", null);

      var nodeOakland = new Node("Oakland", null);
      this.head.next = nodeOakland;

      var nodeBerkeley = new Node("Berkeley", null);
      nodeOakland.next = nodeBerkeley;

      // the last node called tail node
      this.tail = new Node("Fremont", null);
      nodeBerkeley.next = this.tail;

      return this.head;
    }

    insert(insertPosition, newNode) {
      var p = this.head;
      var i = 0;
      // Move the node to the position
      while (p.next != null && i < insertPosition - 1) {
        p = p.next;
        i++;
      }
      newNode.next = p.next; // newNode next to next node
      p.next = newNode; // current next to newNode
    }

    print(node) {
      var p = node;
      while (p != null) // From the beginning to the end
      {
        var data = p.getData();
        document.write(data + " -> ");
        p = p.next;
      }
      document.write("End<br><br>");
    }
  }

  //////////////////testing//

  var linkedList = new LinkedList();
  var head = linkedList.init();

  document.write("Insert a new node Walnut at index = 2 : <br>");
  linkedList.insert(2, new Node("Walnut", null));

  linkedList.print(head);
</script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_59_0.png)

### 4. 删除`index=2`的节点。

`p=head`
[可视化：链表以`p`指向`head` 开始，`head` 指向`San Francisco`。]

`p=p.next`
[可视化：`p`从`head` 移动到链表中的`Oakland`。]

`Node temp = p.next`
[可视化：创建了一个新的指针`temp`，指向`Oakland` 之后的节点。]

`p.next=p.next.next`
[可视化：`Oakland` 和`Berkeley` 之间的连接被修改，跳过`temp`指向的节点。]

`temp.next = null`
[可视化：节点`Berkeley` 现在连接到`Fremont` 节点，表明它已隔离或是新结构的一部分。]

### 1. 使用`记事本`创建`TestUnidirectionalLinkedListDelete.html`

```javascript
<script type="text/javascript">
  class Node{
    constructor(data, next){
      this.data = data;
      this.next = next;
    }

    getData(){
      return this.data;
    }
  }

  class LinkedList{
    init() {
      // the first node called head node
      this.head = new Node("San Francisco", null);

      var nodeOakland = new Node("Oakland", null);
      this.head.next = nodeOakland;

      var nodeBerkeley = new Node("Berkeley", null);
      nodeOakland.next = nodeBerkeley;

      // the last node called tail node
      this.tail = new Node("Fremont", null);
      nodeBerkeley.next = this.tail;

      return this.head;
    }

    remove(removePosition) {
      var p = this.head;
      var i = 0;
      // Move the node to the previous position
      while (p.next != null && i < removePosition - 1) {
        p = p.next;
        i++;
      }
      var temp = p.next;// Save the node you want to delete
      p.next = p.next.next;// Previous node points to next of delete the node
      temp.next = null;
    }

    print(node) {
      var p = node;
      while (p != null)
      {
        var data = p.getData();
        document.write(data + " -> ");
        p = p.next;
      }
      document.write("End<br><br>");
    }
  }

  //////////////////testing//

  var linkedList = new LinkedList();
  var head = linkedList.init();

  document.write("Delete a node Berkeley at index = 2 : <br>");
  linkedList.remove(2);

  linkedList.print(head);
</script>
```

## 2. 使用记事本创建 `TestDoubleLink.html`

```javascript
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
        this.data = data;
        this.prev = prev;
        this.next = next;
        }

        getData(){
        return this.data;
        }
    }

    class DoubleLinkList{
        init() {
        this.head = new Node("San Francisco");
        this.head.prev = null;
        this.head.next = null;

        var nodeOakland = new Node("Oakland");
        nodeOakland.prev = this.head;
        nodeOakland.next = null;
        this.head.next = nodeOakland;

        var nodeBerkeley = new Node("Berkeley");
        nodeBerkeley.prev = nodeOakland;
        nodeBerkeley.next = null;
        nodeOakland.next = nodeBerkeley;

        this.tail = new Node("Fremont");
        this.tail.prev = nodeBerkeley;
        this.tail.next = null;
        nodeBerkeley.next = this.tail;
        return this.head;
        }

        print(node) {
        var p = node;
        var end = null;
        while (p != null)
        {
          var data = p.getData();
          document.write(data + " -> ");
          end = p;
          p = p.next;
        }
        document.write("End<br><br>");
        p = end;
        while (p != null)
        {
          var data = p.getData();
          document.write(data + " -> ");
          p = p.prev;
        }
        document.write("Start<br><br>");
        }
    }

    /////////////////////////////////testing/////////////////////////////////
    var doubleLinkedList = new DoubleLinkedList();
    var head = doubleLinkedList.init();
    doubleLinkedList.print(head);
</script>
```

**结果：**

San Francisco -> Oakland -> Berkeley -> Fremont -> End

Fremont -> Berkeley -> Oakland -> San Francisco -> Start

## 3. 在 Fremont末尾添加节点 `Walnut`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_67_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_67_1.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_67_2.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_67_3.png)

## 使用记事本创建 `TestDoubleLinkAdd.html`

```javascript
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
        this.data = data;
        this.prev = prev;
        this.next = next;
        }

        getData(){
        return this.data;
        }
    }

    class DoubleLinkList{
        init() {
        this.head = new Node("San Francisco");
        this.head.prev = null;
        this.head.next = null;

        var nodeOakland = new Node("Oakland");
        nodeOakland.prev = this.head;
        nodeOakland.next = null;
        this.head.next = nodeOakland;

        var nodeBerkeley = new Node("Berkeley");
        nodeBerkeley.prev = nodeOakland;
        nodeBerkeley.next = null;
        nodeOakland.next = nodeBerkeley;

        this.tail = new Node("Fremont");
        this.tail.prev = nodeBerkeley;
        this.tail.next = null;
        nodeBerkeley.next = this.tail;
        return this.head;
        }

        add(newNode) {
            this.tail.next = newNode;
            newNode.prev = this.tail;
            this.tail = newNode;
        }

        print(node) {
            var p = node;
            var end = null;
            while (p != null)
            {
                var data = p.getData();
                document.write(data + " -> ");
                end = p;
                p = p.next;
            }
            document.write("End <br><br>");

            p = end;
            while (p != null)
            {
                var data = p.getData();
                document.write(data + " -> ");
                p = p.prev;
            }
            document.write("Start<br><br>");
        }
    }

    ////////////////////testing////////////////////
    var doubleLinkList = new DoubleLinkList();
    var head = doubleLinkList.init();
    doubleLinkList.add(new Node("Walnut"));
    doubleLinkList.print(head);
</script>
```

**结果：**

旧金山 -> 奥克兰 -> 伯克利 -> 弗里蒙特 -> 核桃城 -> 结束

核桃城 -> 弗里蒙特 -> 伯克利 -> 奥克兰 -> 旧金山 -> 开始

## 3. 在位置 2 插入节点 `桃城`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_71_0.png)

## 使用记事本创建一个 `TestDoubleInsert.html`

```javascript
<script type="text/javascript">
  class Node{
    constructor(data, prev, next){
      this.data = data;
      this.prev = prev;
      this.next = next;
    }

    getData(){
      return this.data;
    }
  }

  class DoubleLinkList{
    init() {
      this.head = new Node("San Francisco");
      this.head.prev = null;
      this.head.next = null;

      var nodeOakland = new Node("Oakland");
      nodeOakland.prev = this.head;
      nodeOakland.next = null;
      this.head.next = nodeOakland;

      var nodeBerkeley = new Node("Berkeley");
      nodeBerkeley.prev = nodeOakland;
      nodeBerkeley.next = null;
      nodeOakland.next = nodeBerkeley;

      this.tail = new Node("Fremont");
      this.tail.prev = nodeBerkeley;
      this.tail.next = null;
      nodeBerkeley.next = this.tail;
      return this.head;
    }

    insert(insertPosition, newNode) {
      var p = this.head;
      var i = 0;
      // Move the node to insertion position
      while (p.next != null && i < insertPosition-1) {
        p = p.next;
        i++;
      }

      newNode.next = p.next;
      p.next = newNode;
      newNode.prev = p;
      newNode.next.prev = newNode;
    }

    print(node) {
      var p = node;
      var end = null;
      while (p != null)
      {
        var data = p.getData();
        document.write(data + " -> ");
        end = p;
        p = p.next;
      }
      document.write("End <br><br>");

      p = end;
      while (p != null)
      {
        var data = p.getData();
        document.write(data + " -> ");
        p = p.prev;
      }
      document.write("Start<br><br>");
    }
  }

  //////////////////testing//
  var doubleLinkedList = new DoubleLinkedList();
  var head = doubleLinkedList.init();
  document.write("Insert a node Walnut at index = 2 : <br>");
  doubleLinkedList.insert(2,new Node("Walnut"));
  doubleLinkedList.print(head);
</script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_74_0.png)

## 4. 删除索引=2 的节点。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_75_0.png)

## 使用记事本创建 `TestDoubleLinkDelete.html`

```javascript
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
            this.data = data;
            this.prev = prev;
            this.next = next;
        }

        getData(){
        return this.data;
    }
}

class DoubleLinkList{

    init() {
      this.head = new Node("San Francisco");
      this.head.prev = null;
      this.head.next = null;

      var nodeOakland = new Node("Oakland");
      nodeOakland.prev = this.head;
      nodeOakland.next = null;
      this.head.next = nodeOakland;

      var nodeBerkeley = new Node("Berkeley");
      nodeBerkeley.prev = nodeOakland;
      nodeBerkeley.next = null;
      nodeOakland.next = nodeBerkeley;

      this.tail = new Node("Fremont");
      this.tail.prev = nodeBerkeley;
      this.tail.next = null;
      nodeBerkeley.next = this.tail;
      return this.head;
    }

    remove(removePosition) {
        var p = this.head;
        var i = 0;

        // Move the node to the previous node that was deleted

        while (p.next != null && i < removePosition - 1) {
            p = p.next;
            i++;
        }

        var temp = p.next;// Save the node you want to delete

        p.next = p.next.next;
        p.next.prev = p;
        temp.next = null;// Set the delete node next to null

        temp.prev = null;// Set the delete node prev to null
    }

    print(node) {
        var p = node;
        var end = null;

        while (p != null)
        {
            var data = p.getData();
            document.write(data + " -> ");
            end = p;
            p = p.next;
        }

        document.write("End <br><br>");

        p = end;

        while (p != null)
        {
            var data = p.getData();
```

```text
San Francisco -> Oakland -> Fremont -> End

Fremont -> Oakland -> San Francisco -> Start
```

```html
<p>
  <img alt="Result screenshot showing San Francisco -> Oakland -> Fremont -> End and reverse" src="img/4e0bf091f4d81b2977c8fb9210bf9760_78_0.png"/>
</p>
```

循环链表：尾节点指回头节点，形成一个环状结构，可以从任何起点无限遍历。

列表初始化创建了A到D的顺序连接节点，最后一个节点的`next`引用指向头节点而不是`null`。

## 单向循环链表

### 单向循环列表：

它是线性表的链式存储结构，连接成环，每个节点由数据和指向下一个节点的指针组成。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_79_0.png)

### UML图

![](img/4e0bf091f4d81b2977c8fb9210bf9760_79_1.png)

```javascript
class Node{
    constructor(data, next){
        this.data = data;
        this.next = next;
    }

    getData(){
        return this.data;
    }
}
```

## 1. 单向循环链表的初始化和遍历输出。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_80_0.png)

使用**记事本**创建一个`TestSingleCircleLink.html`*

```javascript
<script type="text/javascript">
class Node{
  constructor(data, next){
    this.data = data;
    this.next = next;
  }
  getData(){ return this.data; }
}

class SingleCircleLink {
  init() { // the first node called head node
    this.head = new Node("A");
    this.head.next = null;

    var nodeB = new Node("B");
    nodeB.next = null;
    this.head.next = nodeB;

    var nodeC = new Node("C");
    nodeC.next = null;
    nodeB.next = nodeC;

    // the last node called tail node
    this.tail = new Node("D");
    this.tail.next = this.head;
    nodeC.next = this.tail;
  }

  print() {
    var p = this.head;
    do{
      var data = p.getData();
      document.write(data + " -> ");
      p = p.next;
    }while(p != this.head);

    var data = p.getData();
    document.write(data + "<br><br>");
  }
}

///////////////////testing///////////////////

var singleCircleLink = new SingleCircleLink();
var head = singleCircleLink.init();
singleCircleLink.print(head);
</script>
```

结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_82_0.png)

## 3. 在位置2插入节点**E**。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_83_0.png)

```javascript
newNode.next = p.next
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_84_0.png)

```javascript
p.next = newNode
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_84_1.png)

## 使用记事本创建TestSingleCircleLinkInsert.html

```javascript
<script type="text/javascript">
  class Node{
    constructor(data, next){
      this.data = data;
      this.next = next;
    }
    getData(){
      return this.data;
    }
  }

  class SingleCircleLink{
    init() {
      // the first node called head node
      this.head = new Node("A");
      this.head.next = null;

      var nodeB = new Node("B");
      nodeB.next = null;
      this.head.next = nodeB;

      var nodeC = new Node("C");
      nodeC.next = null;
      nodeB.next = nodeC;

      // the last node called tail node
      this.tail = new Node("D");
      this.tail.next = this.head;
      nodeC.next = this.tail;
    }

    insert(insertPosition, newNode) {
      var p = this.head;
      var i = 0;
      while (p.next != null && i < insertPosition - 1) {
        p = p.next;
        i++;
      }
      newNode.next = p.next;
      p.next = newNode;
    }

    print() {
      var p = this.head;
      do{
        var data = p.getData();
        document.write(data + " -> ");
        p = p.next;
      }while(p != this.head);

      var data = p.getData();
      document.write(data + "<br><br>");
    }
  }

  ////////////////////testing////////////////
  var singleCircleLink = new SingleCircleLink();
  var head = singleCircleLink.init();

  document.write("Insert new node E at index = 2 : <br>");
  singleCircleLink.insert(2, new Node("E"));
  singleCircleLink.print();
</script>
```

结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_86_0.png)

索引 2 处插入节点 E：

A -> B -> E -> C -> D -> A

## 4. 删除 index=2 的节点。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_88_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_89_0.png)

## 用记事本创建 TestCircleLinkDelete.html

```javascript
<script type="text/javascript">
class Node{
    constructor(data, next){
        this.data = data;
        this.next = next;
    }

    getData(){return this.data;}
}

class SingleCircleLink{
    init() {
        this.head = new Node("A");
        this.head.next = null;

        var nodeB = new Node("B");
        nodeB.next = null;
        this.head.next = nodeB;

        var nodeC = new Node("C");
        nodeC.next = null;
        nodeB.next = nodeC;

        this.tail = new Node("D");
        this.tail.next = this.head;
        this.head.next = this.tail;
    }

    remove(removePosition){
        var p = this.head;
        var i = 0;
        while (p.next != null && i < removePosition - 1) {
            p = p.next;
            i++;
        }
        var temp = p.next;
        p.next = p.next.next;
        temp.next = null;
    }

    print() {
        var p = this.head;
        do{
            var data = p.getData();
            document.write(data + " -> ");
            p = p.next;
        }while(p != this.head);

        var data = p.getData();
        document.write(data + "<br><br>");
    }
}

/////////////////testing/
var singleCircleLink = new SingleCircleLink();
singleCircleLink.init();

document.write("Delete a new node at index = 2 : <br>");
singleCircleLink.remove(2);
singleCircleLink.print();
</script>
```

结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_92_0.png)

# 双向循环链表

### 双向循环链表：

它是线性表的链式存储结构。节点通过两个方向串联连接，并连接形成环。每个节点由数据、指向前一个节点的 `prev` 和指向下一节点的 `next` 组成。[![UML 图](https://via.placeholder.com/150)](https://example.com/UML_Diagram)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_93_0.png)

```javascript
class Node {
    constructor(data, prev, next) {
        this.data = data;
        this.prev = prev;
        this.next = next;
    }

    getData() {
        return this.data;
    }
}
```

## 1. 双向循环链表的初始化与遍历输出。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_94_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_95_0.png)

## 使用记事本创建 TestDoubleCircleLink.html

```javascript
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
            this.data = data;
            this.prev = prev;
            this.next = next;
        }

        getData(){
            return this.data;
        }
    }

    class DoubleCircleLink{
        init() {
            // the first node called head node
            this.head = new Node("A");
            this.head.next = null;
            this.head.prev = null;

            var nodeB = new Node("B");
            nodeB.next = null;
            nodeB.prev = this.head;
            this.head.next = nodeB;

            var nodeC = new Node("C");
            nodeC.next = null;
            nodeC.prev = nodeB;
            nodeB.next = nodeC;

            // the last node called tail node
            this.tail = new Node("D");
            this.tail.next = this.head;
            this.tail.prev = nodeC;
            nodeC.next = this.tail;
            this.head.prev = this.tail;
        }

        print() {
            var p = this.head;
            do{
                var data = p.getData();
                document.write(data + " -> ");
                p = p.next;
            }while(p != this.head);

            var data = p.getData();
            document.write(data + "<br><br>");

            p = this.tail;
            do{
                data = p.getData();
                document.write(data + " -> ");
                p = p.prev;
            }while(p != this.tail);

            data = p.getData();
            document.write(data + "<br><br>");
        }
    }

    var doubleCircleLink = new DoubleCircleLink();
    doubleCircleLink.init();
    doubleCircleLink.print();
</script>
```

<channel|>`newNode.next = p.next`

```
p.next = newNode
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_100_0.png)

```
newNode.prev = p
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_100_1.png)

```
newNode.next.prev = newNode
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_100_2.png)

# 用记事本创建 TestDoubleCircleLinkInsert.html

```html
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
            this.data = data;
            this.prev = prev;
            this.next = next;
        }

        getData(){
            return this.data;
        }
    }

    class DoubleCircleLink{
        init() {
            // the first node权的头节点
            this.head = new Node("A");
            this.head.next = null;
            this.head.prev = null;

            var nodeB = new Node("B");
            nodeB.next = null;
            nodeB.prev = this.head;
            this.head.next = nodeB;

            var nodeC = new Node("C");
            nodeC.next = null;
            nodeC.prev = nodeB;
            nodeB.next = nodeC;

            // the last node called tail node
            this.tail = new Node("D");
            this.tail.next = this.head;
            this.tail.prev = nodeC;
            nodeC.next = this.tail;
            this.head.prev = this.tail;
        }

        insert(insertPosition, newNode) {
            var p = this.head;
            var i = 0;
            //将节点移动到插入位置
            while (p.next != null && i < insertPosition - 1) {
                p = p.next;
                i++;
            }

            newNode.next = p.next;
            p.next = newNode;
            newNode.prev = p;
            newNode.next.prev = newNode;
        }

        print() {
            var p = this.head;
            do {
                var data = p.getData();
                document.write(data + " -> ");
                p = p.next;
            } while (p != this.head);

            var data = p.getData();
            document.write(data + "<br><br>");

            p = this.tail;
            do {
                data = p.getData();
                document.write(data + " -> ");
                p = p.prev;
            } while (p != this.tail);

            data = p.getData();
            document.write(data + "<br><br>");
        }
    }

    /////////测试/////////

    var doubleCircleLink = new DoubleCircleLink();
    doubleCircleLink.init();

    document.write("在索引 2 处插入新节点 E : <br>");
    doubleCircleLink.insert(2, new Node("E"));

    doubleCircleLink.print();
</script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_103_0.png)

## 4. 删除 index=2 的节点。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_104_0.png)

```
var temp = p.next;
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_104_1.png)

```
p.next = p.next.next
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_105_0.png)

```
p.next.prev = p
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_105_1.png)

```
temp.next = null
temp.prev = null
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_105_2.png)

# 用记事本创建 TestDoubleCircleLinkDelete.html

```html
<script type="text/javascript">
    class Node{
        constructor(data, prev, next){
            this.data = data;
            this.prev = prev;
            this.next = next;
        }

        getData(){
            return this.data;
        }
    }

    class DoubleCircleLink{
        init() {
            // the first node called head node
            this.head = new Node("A");
            this.head.next = null;
            this.head.prev = null;

            var nodeB = new Node("B");
            nodeB.next = null;
            nodeB.prev = this.head;
            this.head.next = nodeB;

            var nodeC = new Node("C");
            nodeC.next = null;
            nodeC.prev = nodeB;
            nodeB.next = nodeC;

            // the last node called tail
            this.tail = new Node("D");
            this.tail.next = this.head;
            this.tail.prev = nodeC;
            nodeC.next = this.tail;
            this.head.prev = this.tail;
        }

        remove(removePosition) {
            var p = this.head;
            var i = 0;
            while (p.next != null && i < removePosition - 1) {
                p = p.next;
                i++;
            }

            var temp = p.next;
            p.next = p.next.next;
            p.next.prev = p;
            temp.next = null // 将删除节点的 next 设为 null
            temp.prev = null // 将删除节点的 prev 设为 null
        }

        print() {
            var p = this.head;
            do {
                var data = p.getData();
                document.write(data + " -> ");
                p = p.next;
            } while (p != this.head);

            var data = p.getData();
            document.write(data + "<br><br>");

            p = this.tail;
            do {
                data = p.getData();
                document.write(data + " -> ");
                p = p.prev;
            } while (p != this.tail);

            data = p.getData();
            document.write(data + "<br><br>");
        }
    }

    ////////////////测试////////////////
    var doubleCircleLink = new DoubleCircleLink();
    doubleCircleLink.init();

    document.write("删除索引 2 处的节点：<br>");
    doubleCircleLink.remove(2);
    doubleCircleLink.print();
</script>
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_108_0.png)

## 队列

**队列：**

后进先出（FIFO）序列。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_109_0.png)

### UML 图

![](img/4e0bf091f4d81b2977c8fb9210bf9760_109_1.png)

```javascript
class Node{
  constructor(data, next){
    this.data = data;
    this.next = next;
  }

  getData(){
    return this.data;
  }
}
```

## 1. 队列的初始化与遍历输出。

初始化 A

```javascript
head = new Node("A");
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_110_0.png)

```javascript
tail = head;
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_110_1.png)

## 初始化 B

```javascript
newNode = new Node("B");
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_111_0.png)

```javascript
newNode.next = tail;
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_111_1.png)

```javascript
tail = newNode;
```


![](img/4e0bf091f4d81b2977c8fb9210bf9760_119_1.png)

```
top = newNode
```

![](img/4e0bf091f4d81b2977c8fb9210bf9760_119_2.png)

## 将 C 压入栈

```
newNode.next = top
```

```
top = newNode
```

## 若从栈中弹出 C：

```
p = top
```

```
top = top.next
```

```
p.next = null
```

## 若从栈中弹出 B：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_122_0.png)

## 若从栈中弹出 A：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_123_0.png)

## 使用记事本创建 TestStack.html

```
<script type="text/javascript">
class Node{
    constructor(data, next){
        this.data = data;
        this.next = next;
    }

    getData(){
        return this.data;
    }
}
class Stack {
    constructor(){
        this.top = null;
        this.size = 0;
    }
    push(element) {
        if (this.top == null) {
            this.top = new Node(element);
        } else {
            var newNode = new Node(element);
            newNode.next = this.top;
            this.top = newNode;
        }
        this.size++;
    }
    pop() {
        if (this.top == null) {
            return null;
        }
        var p = this.top;
        this.top = this.top.next;
        p.next = null;
        this.size--;
        return p;
    }

    size() {
        return this.size;
    }
}

//////////////////////测试//////////////////////

function print(stack) {
    document.write("Top ");
    var node = null;
    while ((node = stack.pop())!=null) {
        document.write(node.getData() + " -> ");
    }
    document.write("End <br>");
}

var stack = new Stack();
stack.push("A");
stack.push("B");
stack.push("C");
stack.push("D");
print(stack);

</script>
```

结果：

Top D -> C -> B -> A -> End

## 递归算法

**递归算法：**

程序函数自身调用自身，层层递进，直到满足某个条件后逐步返回至结束。

+ 1. `n` 的阶乘：`n*(n-1)*(n-2) ...... *2*1`

使用记事本创建 TestRecursive.html

```
<script type="text/javascript">
    function factorial(n) {
        if (n == 1) {
            return 1;
        } else {
            //递归调用自身，直到返回结束
            return factorial(n - 1) * n;
        }
    }

    ////////////////////测试////////////////////

    var n = 5;
    var fac = factorial(n);
    document.write("5 的阶乘为：" + fac);
```

## 结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_127_0.png)

### 图解分析：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_128_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_129_0.png)

## 二路归并算法

**二路归并算法：**

将前半部分和后半部分的数据分别排序，然后将两个有序子列表合并成一个有序列表，持续递归至结束。

+ 1. 对分数 `{50, 65, 99, 87, 74, 63, 76, 100}` 进行归并排序

![](img/4e0bf091f4d81b2977c8fb9210bf9760_130_0.png)

## 使用记事本创建 TestMergeSort.html

```
<script type="text/javascript">
    class MergeSort{
        sort(array) {
            var temp = new Array(array.length);
            this.mergeSort(array, temp, 0, array.length - 1);
        }

        mergeSort(array, temp, left, right) {
            if (left < right) {
                var center = parseInt((left + right) / 2);
                this.mergeSort(array, temp, left, center); // 左侧归并排序
                this.mergeSort(array, temp, center + 1, right); // 右侧归并排序
                this.merge(array, temp, left, center + 1, right); // 合并两个有序数组
            }
        }

        merge(array, temp, left, right, rightEndIndex) {
            var leftEndIndex = right - 1; // 左侧结束
            var tempIndex = left; // 左侧开始
            var elementNumber = rightEndIndex - left + 1;

            while (left <= leftEndIndex && right <= rightEndIndex) {
                if (array[left] <= array[right])
                    temp[tempIndex++] = array[left++];
                else
                    temp[tempIndex++] = array[right++];
            }

            while (left <= leftEndIndex) { // 左侧还有元素
                temp[tempIndex++] = array[left++];
            }

            while (right <= rightEndIndex) { // 右侧还有元素
                temp[tempIndex++] = array[right++];
            }

## 快速排序

**快速排序：**

快速排序是一种流行的算法，在实践中比其他算法更快。它利用分治策略，将大数组分成较小的数组。

1. 使用快速排序对 `{90, 60, 50, 80, 70, 100}` 进行排序

```
while (i < j && array[j] > threshold) {
    j--;
}
```

```
array[i++] = array[j]
```

```
threshold = array[low]

low = 0    j = 4  high = 5
  ↓        ↓     ↓
  90      70  60  50  80   100

while (i < j && array[i] <= threshold) {
    i++;
}



threshold = array[low]

low = 0                    i = 4  high = 5
  ↓                       ↓     ↓
  90   ───────────────── 70   100

array[i] = threshold

threshold = array[low]

low = 0                    i = 4  high = 5
  ↓                       ↓     ↓
  90      70  60  50  80   100

```
quickSort(array, low, i - 1)
```

```
i = 0
```

```
j = 3
```

```
threshold = array[low]
```

```
low = 0
```

```
high = 3
```

```
70
```

```
60
```

```
50
```

```
80
```

```
90
```

```
100
```

```
array[i++] = array[j]
```

# 用记事本创建一个 TestQuickSort.html

```
<script type="text/javascript">
    class QuickSort{
        sort(array) {
            if (array.length > 0) {
                this.quickSort(array, 0, array.length - 1);
            }
        }

        quickSort(array, low, high) {
            if (low > high) {
                return;
            }
            var i = low;
            var j = high;
            var threshold = array[low];
            // 从列表两端交替扫描
            while (i < j) {
                // 从右到左找到小于 threshold 的位置
                while (i < j && array[j] > threshold) {
                    j--;
                }
                // 用一个比 threshold 小的数替换 low 位置的数
                if (i < j)
                    array[i++] = array[j];

                // 从左到右找到大于 threshold 的位置
                while (i < j && array[i] <= threshold) {
                    i++;
                }

                // 用一个比 threshold 大的数替换 high 位置的数
                if (i < j)
                    array[j--] = array[i];
            }
            array[i] = threshold;

            this.quickSort(array, low, i - 1); // 左侧快速排序
            this.quickSort(array, i + 1, high); // 右侧快速排序
        }
    }

    //////////////////////测试//////////////////////

    var scores = [ 90, 60, 50, 80, 70, 100 ];
    var quickSort = new QuickSort();
    quickSort.sort(scores);
    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }
</script>
```

## 结果：

# 二叉搜索树

**二叉搜索树：**

1. 如果任何节点的左子树不为空，其左子树上所有节点的值都小于其根节点的值；
2. 如果任何节点的右子树不为空，其右子树上所有节点的值都大于其根节点的值；
3. 任何节点的左子树和右子树也都是二叉搜索树。

## 节点 UML 图

```
class Node{
    constructor(data, left, right){
        this.data = data;
        this.left = left;
        this.right = right;
    }

    getData(){
        return this.data;
    }
}
```

## 1. 构建二叉搜索树，插入节点

插入节点时，从根节点开始比较，小于根节点的值则与根节点的左子树比较，否则与右子树比较，直到左子树或右子树为空时插入。

**插入 60**

**插入 40**

**插入 20**

**插入 10**

**插入 30**

**插入 50**

**插入 80**

**插入 70**

**插入 90**

## 2. 二叉搜索树中序遍历

**中序遍历**：左子树 -> 根节点 -> 右子树


```javascript
<script type="text/javascript">
  class BinaryTree {
    getRoot() {
      return this.root;
    }

    // 中序遍历二叉搜索树
    inOrder(root) {
      if (root == null) {
        return;
      }
      this.inOrder(root.left); // 遍历左子树
      document.write(root.getData() + ", ");
      this.inOrder(root.right); // 遍历右子树
    }

    insert(node, newData) {
      if (this.root == null) {
        this.root = new Node(newData, null, null);
        return;
      }

      var compareValue = newData - node.getData();

      //递归左子树，继续寻找插入位置
      if (compareValue < 0) {
        if (node.left == null) {
          node.left = new Node(newData, null, null);
        } else {
          this.insert(node.left, newData);
        }
      } else if (compareValue > 0) {////递归右子树，寻找插入位置
        if (node.right == null) {
          node.right = new Node(newData, null, null);
        } else {
          this.insert(node.right, newData);
        }
      }
    }
  }

  class Node{
    constructor(data, left, right){
      this.data = data;
      this.left = left;
      this.right = right;
    }

    getData(){
      return this.data;
    }
  }

  ///////////////测试/////////////

  var binaryTree=new BinaryTree();
  //构建二叉搜索树
  binaryTree.insert(binaryTree.getRoot(), 60);
  binaryTree.insert(binaryTree.getRoot(), 40);
  binaryTree.insert(binaryTree.getRoot(), 20);
  binaryTree.insert(binaryTree.getRoot(), 10);
  binaryTree.insert(binaryTree.getRoot(), 30);
  binaryTree.insert(binaryTree.getRoot(), 50);
  binaryTree.insert(binaryTree.getRoot(), 80);
  binaryTree.insert(binaryTree.getRoot(), 70);
  binaryTree.insert(binaryTree.getRoot(), 90);
  document.write("<br> 中序遍历二叉搜索树 <br>");
  binaryTree.inOrder(binaryTree.getRoot());
</script>
```

**结果**：

## 测试二叉搜索树

中序遍历二叉搜索树

10, 20, 30, 40, 50, 60, 70, 80, 90,

### 3. 二叉搜索树前序遍历

**前序遍历**：根节点 -> 左子树 -> 右子树

**结果：**

#### 用记事本创建 `TestBinarySearchTreePreOrder.html`

```javascript
<script type="text/javascript">
  class BinaryTree {
    getRoot() {
      return this.root;
    }

    //Preorder traversal binary search tree
    preOrder(root) {
      if (root == null) {
        return;
      }
      document.write(root.getData() + ", ");
      this.preOrder(root.left); // Recursive Traversing the left subtree
      this.preOrder(root.right); // Recursive Traversing the right subtree
    }

    insert(node, newData) {
      if (this.root == null) {
        this.root = new Node(newData, null, null);
        return;
      }

      var compareValue = newData - node.getData();
      //Recursive left subtree, continue to find the insertion position
      if (compareValue < 0) {
        if (node.left == null) {
          node.left = new Node(newData, null, null);
        } else {
          this.insert(node.left, newData);
        }
      } else if (compareValue > 0) { //Recursive right subtree, continue to find the insertion position
        if (node.right == null) {
          node.right = new Node(newData, null, null);
        } else {
          this.insert(node.right, newData);
        }
      }
   }
}

class Node{
   constructor(data, left, right){
      this.data = data;
      this.left = left;
      this.right = right;
   }

   getData(){
      return this.data;
   }
}

//////////////////testing///////////////////

var binaryTree=new BinaryTree();
//Constructing a binary search tree
binaryTree.insert(binaryTree.getRoot(), 60);
binaryTree.insert(binaryTree.getRoot(), 40);
binaryTree.insert(binaryTree.getRoot(), 20);
binaryTree.insert(binaryTree.getRoot(), 10);
binaryTree.insert(binaryTree.getRoot(), 30);
binaryTree.insert(binaryTree.getRoot(), 50);
binaryTree.insert(binaryTree.getRoot(), 80);
binaryTree.insert(binaryTree.getRoot(), 70);
binaryTree.insert(binaryTree.getRoot(), 90);

document.write("<br> Pre-order traversal binary search tree <br>");
binaryTree.preOrder(binaryTree.getRoot());
</script>
```

## 结果：

#### 前序遍历二叉搜索树

60, 40, 20, 10, 30, 50, 80, 70, 90,

### 4. 二叉搜索树后序遍历

**后序遍历**：左子树 -> 右子树 -> 根节点

**结果：**

#### 用记事本创建 `TestBinarySearchTreePostOrder.html`

```javascript
<script type="text/javascript">
  class BinaryTree {
    getRoot() {
      return this.root;
    }

    postOrder(root) {
      if (root == null) {
        return;
      }
      this.postOrder(root.left);
      this.postOrder(root.right);
      document.write(root.getData() + ", ");
    }

    insert(node, newData) {
      if (this.root == null) {
        this.root = new Node(newData, null, null);
        return;
      }

      var compareValue = newData - node.getData();
      if (compareValue < 0) {
        if (node.left == null) {
          node.left = new Node(newData, null, null);
        } else {
          this.insert(node.left, newData);
        }
      } else if (compareValue > 0) {
        if (node.right == null) {
          node.right = new Node(newData, null, null);
        } else {
          this.insert(node.right, newData);
        }
      }
    }
  }

  class Node{
    constructor(data, left, right){
      this.data = data;
      this.left = left;
      this.right = right;
    }

    getData(){
      return this.data;
    }
  }

  var binaryTree=new BinaryTree();
  binaryTree.insert(binaryTree.getRoot(), 60);
  binaryTree.insert(binaryTree.getRoot(), 40);
  binaryTree.insert(binaryTree.getRoot(), 20);
  binaryTree.insert(binaryTree.getRoot(), 10);
  binaryTree.insert(binaryTree.getRoot(), 30);
  binaryTree.insert(binaryTree.getRoot(), 50);
  binaryTree.insert(binaryTree.getRoot(), 80);
  binaryTree.insert(binaryTree.getRoot(), 70);
  binaryTree.insert(binaryTree.getRoot(), 90);
  document.write("<br> Post-order traversal binary search tree <br>");
  binaryTree.postOrder(binaryTree.getRoot());
</script>
```

#### 后序遍历二叉搜索树

10, 30, 20, 50, 40, 70, 90, 80, 60,

### 5. 二叉搜索树最大值与最小值

**最小值**：从根节点开始向左不断遍历，直到没有左子节点为止。

**最大值**：从根节点开始向右不断遍历，直到没有右子节点为止。

```javascript
function getMin() {
  var current = this.root;
  if (current == null) return null;
  while (current.left != null) {
    current = current.left;
  }
  return current.data;
}

function getMax() {
  var current = this.root;
  if (current == null) return null;
  while (current.right != null) {
    current = current.right;
  }
  return current.data;
}
```

content]
```javascript
<script type="text/javascript">
  class BinaryTree {
    getRoot() {
      return this.root;
    }

    //Minimum value
    searchMinValue(node) {
      if (node == null || node.getData() == 0)
        return null;
      if (node.left == null) {
        return node;
      }
      //Recursively find the minimum from the left subtree
      return this.searchMinValue(node.left);
    }

    //Maximum value
    searchMaxValue(node) {
      if (node == null || node.getData() == 0)
        return null;
      if (node.right == null) {
        return node;
      }
      //Recursively find the minimum from the right subtree
      return this.searchMaxValue(node.right);
    }
  }

  insert(node, newData) {
    if (this.root == null) {
        this.root = new Node(newData, null, null);
        return;
    }

    var compareValue = newData - node.getData();
    //Recursive left subtree, continue to find the insertion position
    if (compareValue < 0) {
        if (node.left == null) {
            node.left = new Node(newData, null, null);
        } else {
            this.insert(node.left, newData);
        }
    } else if (compareValue > 0) { ///Recursive right subtree, continue to find the insertion position
        if (node.right == null) {
            node.right = new Node(newData, null, null);
        } else {
            this.insert(node.right, newData);
        }
    }
}

class Node{
    constructor(data, left, right){
        this.data = data;
        this.left = left;
        this.right = right;
    }

    getData(){
        return this.data;
    }
}
```

```javascript
/////////////////testing/////////////////

var binaryTree=new BinaryTree();

//Constructing a binary search tree
binaryTree.insert(binaryTree.getRoot(), 60);
binaryTree.insert(binaryTree.getRoot(), 40);
binaryTree.insert(binaryTree.getRoot(), 20);
binaryTree.insert(binaryTree.getRoot(), 10);
binaryTree.insert(binaryTree.getRoot(), 30);
binaryTree.insert(binaryTree.getRoot(), 50);
binaryTree.insert(binaryTree.getRoot(), 80);
binaryTree.insert(binaryTree.getRoot(), 70);
binaryTree.insert(binaryTree.getRoot(), 90);

document.write("<br> Minimum Value<br> ");
var minNode = binaryTree.searchMinValue(binaryTree.getRoot());
document.write(minNode.getData());

document.write("<br> Maximum Value<br> ");
var maxNode = binaryTree.searchMaxValue(binaryTree.getRoot());
document.write(maxNode.getData());
</script>
```


![](img/4e0bf091f4d81b2977c8fb9210bf9760_183_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_184_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_184_1.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_184_2.png)

`根` = 60 和 `尾` = 20 交换

![](img/4e0bf091f4d81b2977c8fb9210bf9760_184_3.png)

### 调整堆

![](img/4e0bf091f4d81b2977c8fb9210bf9760_185_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_186_0.png)

`根` = 50 和 `尾` = 20 交换

![](img/4e0bf091f4d81b2977c8fb9210bf9760_186_1.png)

### 调整堆

![](img/4e0bf091f4d81b2977c8fb9210bf9760_187_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_188_0.png)

`根` = 40 和 `尾` = 10 交换

![](img/4e0bf091f4d81b2977c8fb9210bf9760_188_1.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_189_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_190_0.png)

`根` = 30 和 `尾` = 20 交换

无需调整堆

![](img/4e0bf091f4d81b2977c8fb9210bf9760_191_0.png)

`根` = 20 和 `尾` = 10 交换

![](img/4e0bf091f4d81b2977c8fb9210bf9760_191_1.png)

## 堆排序结果

- 10
- 20
- 30
- 40
- 50
- 60
- 70
- 80
- 90

## 用记事本创建 TestBinaryHeapSorting.html

```javascript
<script type="text/javascript">
  class HeapSort {
    constructor(){
      this.array = [];
    }
    //Initialize the heap
    createHeap(array) {
      this.array = array;
      // Build a heap, (array.length - 1) / 2 scan half of the nodes with child nodes
      for (var i = (array.length - 1) / 2; i >= 0; i--) {
        this.adjustHeap(i, array.length - 1);
      }
    }
    //Adjustment heap
    adjustHeap(currentIndex, maxLength) {
      var noLeafValue = this.array[currentIndex]; // Current non-leaf node
      //2 * currentIndex + 1 Current left subtree subscript
      for (var j = 2 * currentIndex + 1; j <= maxLength; j = currentIndex * 2 + 1) {
        if (j < maxLength && this.array[j] < this.array[j + 1]) {
          j++; // j Large subscript
        }
        if (noLeafValue >= this.array[j]) {
          break;
        }
        this.array[currentIndex] = this.array[j]; // Move up to the
```

```javascript
## parentNode
    currentIndex = j;
}
    this.array[currentIndex] = noLeafValue; // 放置到对应位置
}

heapSort() {
    for (var i = this.array.length - 1; i > 0; i--) {
        var temp = this.array[0];
        this.array[0] = this.array[i];
        this.array[i] = temp;
        this.adjustHeap(0, i - 1);
    }
}

### 测试

var heapSort = new HeapSort();

var scores = [10, 90, 20, 80, 30, 70, 40, 60, 50 ];

document.write("构建堆之前：<br>");
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ", ");
}
document.write("<br><br>");

document.write("构建堆之后：<br>");
heapSort.createHeap(scores);
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ", ");
}
document.write("<br><br>");

document.write("堆排序之后：<br>");
heapSort.heapSort();
for (var i = 0; i < scores.length; i++) {
    document.write(scores[i] + ", ");
}
</script>

## 结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_195_png) # 哈希表

哈希表：通过映射中的键 `值` 访问数据。将 `{key, 18, 35, 40, 42}` 映射到哈希表规则 `key % 47`

![](img/4e0bf091f4d81b2977c8fb9210bf9760_196_png) # 2. 实现哈希表

![](img/4e0bf091f4d81b2977c8fb9210bf9760_198_png) # 用记事创建一个 TestHashtable.html 文件

```html
<script type="text/javascript">

class Node {
    constructor(key, value, hash, next){
        this.key = key;
        this.value = value;
        this.hash = hash;
        this.next = next;
    }

    getKey() {
        return this.key;
    }

    setKey(key) {
        this.key = key;
    }

    getValue() {
        return this.value;
    }

    setValue(value) {
        this.value = value;
    }

    getHash() {
        return this.hash;
    }

    setHash(hash) {
        this.hash = hash;
    }
}

</script>
```

```javascript
class Hashtable {
    constructor(){
        this.capacity = 16;
        this.table = new Array(this.capacity);
        this.size = 0;
    }

    size() {
        return this.size;
    }

    isEmpty() {
        return this.size == 0 ? true : false;
    }

    hash(key) {
        var hash = 0;
        for (var i = 0; i < key.length; i++) {
            hash += key.charCodeAt(i);
        }
        return hash % 37;
    }

    //根据键的哈希算法计算哈希
    hashCode(key) {
        var avg = this.hash(key) * (Math.pow(5, 0.5) - 1) / 2 //平方取中哈希策略
        var numeric = avg - Math.floor(avg)
        return parseInt(Math.floor(numeric * this.table.length))
    }

    put(key, value) {
        if (key == null) {
            throw new IllegalArgumentException();
        }
        var hash = this.hashCode(key);
        var newNode = new Node(key, value, hash, null);
        var node = this.table[hash];
        while (node != null) {
            if (node.getKey().equals(key)) {
                node.setValue(value);
                return;
            }
            node = node.next;
        }
        newNode.next = this.table[hash];
        this.table[hash] = newNode;
        this.size++;
    }

    get(key) {
        if (key == null) {
            return null;
        }
        var hash = this.hashCode(key);
        var node = this.table[hash];
        while (node != null) //根据键获取值
            if (node.getKey() == key) {
                return node.getValue();
            }
            node = node.next;
        }
        return null;
    }
}
```

### 测试

var table = new Hashtable();

table.put("david", "Good Boy Keep Going");
table.put("grace", "Cute Girl Keep Going");

document.write("david => " + table.get("david") + "<br>");
document.write("grace => " + table.get("grace") + "<br>");
</script>

## 结果：

![](img/4e0bf091f4d81b2977c8fb9210bf9760_201_0.png)

# 有向图与深度优先搜索

**有向图：**
该数据结构通过邻接矩阵（即二维数组）和邻接表表示。每个节点称为顶点，两个相邻节点称为边。

**有向图具有方向性：** A -> B 和 B -> A 是

![](img/4e0bf091f4d81b2977c8fb9210bf9760_202_png) # 1. 邻接矩阵描述：顶点的数，如果边存在为1，不存在为0。

| | A | B | C | D | E |
|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 | 0 |
| B | 0 | 0 | 0 | 1 | 0 |
| C | 0 | 0 | 0 | 0 | 1 |
| D | 0 | 0 | 0 | 0 | 0 |
| E | 0 | 0 | 0 | 0 | 0 |

### 2. 深度优先搜索：从A开始寻找相邻B，然后B找到相邻C，依此类推 A -> B -> C -> D

![](img/4e0bf091f4d81b2977c8fb9210bf9760_203_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_203_1.png)

| | A | B | C | D | E |
|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 | 0 |
| B | 0 | 0 | 0 | 1 | 0 |
| C | 0 | 0 | 0 | 0 | 1 |
| D | 0 | 0 | 0 | 0 | 0 |
| E | 0 | 0 | 0 | 0 | 0 |

![](img/4e0bf091f4d81b2977c8fb9210bf9760_204_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_204_1.png)

| | A | B | C | D | E |
|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 | 0 |
| B | 0 | 0 | 0 | 1 | 0 |
| C | 0 | 0 | 0 | 0 | 1 |
| D | 0 | 0 | 0 | 0 | 0 |
| E | 0 | 0 | 0 | 0 | 0 |

![](img/4e0bf091f4d81b2977c8fb9210bf9760_205_0.png)
![](img/4e0bf091f4d81b2977c8fb9210bf9760_205_1.png)

- A -> B -> C -> D

## 用记事创建一个 TestDirectedGraphDepthFrstSearch. 文件

```html
<script type="text/javascript">

class Vertex {

    constructor(data, visited){
        this.data = data;
        this.visited = visited; // 是否访问
    }

    getData() {
        return this.data;
    }

    setData(data) {
        this.data = data;
    }

    isVisited() {
        return this.visited;
    }

    setVisited(visited) {
        this.visited = visited;
    }
}

class Stack {
    constructor(){
        this.stacks = new Array();
        this.top = -1;
    }

    push(element) {
        this.top++;
        this.stacks[this.top] = element;
    }

    pop() {
        if(this.top == -1){
            return -1;
        }
        var data = this.stacks[this.top];
        this.top--;
        return data;
    }

    peek() {
        if(this.top == -1){
            return -1;
        }
        var data = this.stacks[this.top];
        return data;
    }
}
</script>
```


javascript
    }

    isEmpty() {

        if(this.top <= -1){

            return true;

        }

        return false;

    }
}

class Graph {

    constructor(maxVertexSize){

        this.maxVertexSize = maxVertexSize;// 二维数组大小

        this.vertexs = new Array(maxVertexSize);

        this.size = 0; // 当前顶点大小

        this.adjacencyMatrix = new Array(maxVertexSize);

        for (var i = 0; i < maxVertexSize; i++) {

            this.adjacencyMatrix[i] = new Array();

            for (var j = 0; j < maxVertexSize; j++) {

                this.adjacencyMatrix[i][j] = 0;

            }

        }

        this.stack = new Stack();// 栈保存当前顶点

    }

    addVertex(data) {

        var vertex = new Vertex(data, false);

        this.vertexs[this.size++] = vertex;

    }

    addEdge(from, to) {

        this.adjacencyMatrix[from][to] = 1; // A -> B 和 B -> A 是不同的

    }

    depthFirstSearch() {

        var firstVertex = this.vertexs[0]; // 从第一个顶点开始搜索

        firstVertex.setVisited(true);

        document.write(firstVertex.getData());

        this.stack.push(0);

        while (!this.stack.isEmpty()) {

            var row = this.stack.peek();

            // 获取未被访问的相邻顶点位置

            var col = this.findAdjacencyUnVisitedVertex(row);

            if (col == -1) {

                this.stack.pop();
```javascript
```

# 有向图与广度优先搜索

**广度优先搜索：**

从 A 出发，找到所有相邻的边节点 B、C、D，然后从 B 出发找到所有相邻节点 A、C、D，依此类类until所有节点都被找到 `A -> B -> C -> D -> E`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_212_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_212_1.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_213_0.png)

![](img/4e0bf091f4d81b2977c8fb9210bf9760_214_0.png)

|   | A | B | C | D | E |

|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 1 | 0 |
| B | 0 | 0 | 1 | 1 | 0 |
| C | 0 | 0 | 0 | 1 | 0 |
| D | 0 | 0 | 0 | 0 | 1 |
| E | 0 | 0 | 0 | 0 | 0 |

## 队列

- A
- B
- C
- D
- E

null

输出队列

A → B → C → D → E

![](img/4e0bf091f4d81b2977c8fb9210bf9760_214_1.png)

## 使用记事本创建 TestDirectedGraphBreadthFirstSearch.html

```javascript
<script type="text/javascript">
    class Vertex {
        constructor(data, visited){
            this.data = data;
            this.visited = visited; // Have you visited
        }

        getData() {
            return this.data;
        }
        setData(data) {
            this.data = data;
        }

        isVisited() {
            return this.visited;
        }
        setVisited(visited) {
            this.visited = visited;
        }
    }

    class Queue {
        constructor(){
            this.queues = new Array();
        }

        add(element) {
            this.queues[length] = element;
        }

        remove() {
            if(this.queues.length <= 0){
                return -1;
            }
            return this.queues.shift();
        }

        isEmpty() {
            if(this.queues.length <= 0){
                return true;
            }
            return false;
        }
    }

    class Graph {
        constructor(maxVertexSize){
            this.maxVertexSize = maxVertexSize;// 二维数组大小
            this.vertexs = new Array(maxVertexSize);
            this.size = 0; // 当前顶点大小
            this.adjacencyMatrix = new Array(maxVertexSize);
            for (var i = 0; i < maxVertexSize; i++) {
                this.adjacencyMatrix[i] = new Array();
                for (var j = 0; j < maxVertexSize; j++) {
                    this.adjacencyMatrix[i][j] = 0;
                }
            }
            this.queue = new Queue();// Queue current vertices
        }

        addVertex(data) {
            var vertex = new Vertex(data, false);
            this.vertexs[this.size++] = vertex;
        }

        // Add edges
        addEdge(from, to) {
            // A -> B and B -> A are different
            this.adjacencyMatrix[from][to] = 1;
        }

        breadthFirstSearch() {
            // Start from the first vertex
            var firstVertex = this.vertexs[0];
            firstVertex.setVisited(true);
            document.write(firstVertex.getData());
            this.queue.add(0);

            while (!this.queue.isEmpty()) {
                var head = this.queue.remove();
                // Get adjacent vertex that are not visited
                var col = this.findAdjacencyUnVisitedVertex(head);

                // Loop through vertices connected to the current vertex
                while (col != -1) {
                    this.vertexs[col].setVisited(true);
                    document.write(" -> " + this.vertexs[col].getData());
                    this.queue.add(col);
                    col = this.findAdjacencyUnVisitedVertex(head);
                }
            }
        }

        // Get adjacent vertex positions that are not visited
        findAdjacencyUnVisitedVertex(row) {
            for (var col = 0; col < this.size; col++) {
                if (this.adjacencyMatrix[row][col] == 1 && !this.vertexs[col].isVisited()) {
                    return col;
                }
            }
            return -1;
        }

        // Clear reset
        clear() {
            for (var i = 0; i < this.size; i++) {
                this.vertexs[i].setVisited(false);
            }
        }

        getAdjacencyMatrix() {
            return this.adjacencyMatrix;
        }

        getVertexs() {
            return this.vertexs;
        }
    }

    function printGraph(graph) {
        document.write("Two-dimensional array output vertex and adjacent array : <br>");
        document.write("&nbsp;&nbsp;&nbsp;");
        for (var i = 0; i < graph.getVertexs().length; i++) {
            document.write(graph.getVertexs()[i].getData() + "&nbsp;&nbsp;&nbsp;");
        }
        document.write("<br>");
        for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
            document.write(graph.getVertexs()[i].getData() + " ");
            for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {
                document.write(graph.getAdjacencyMatrix()[i][j] + "&nbsp;&nbsp;&nbsp;");
            }
            document.write("<br>");
        }
    }

    var graph = new Graph(5);
    graph.addVertex("A");
    graph.addVertex("B");
    graph.addVertex("C");
    graph.addVertex("D");
    graph.addVertex("E");

    graph.addEdge(0, 1);
    graph.addEdge(0, 2);
    graph.addEdge(0, 3);
    graph.addEdge(1, 2);
    graph.addEdge(1, 3);
    graph.addEdge(2, 3);
    graph.addEdge(3, 4);

    // Two-dimensional array traversal output vertex and adjacent array
    printGraph(graph);

    document.write("<br>Breadth-First Search traversal output : <br>");
    graph.breadthFirstSearch();
</script>
```

**结果：**

![](img/4e0bf091f4d81b2977c8fb9210bf9760_220_0.png)

# 有向图拓扑排序

**有向图拓扑排序：**按照方向顺序对有向图中的顶点进行排序

**有向图**具有方向性：`A -> B` 与 `B -> A` 是不同的

![](img/4e0bf091f4d81b2977c8fb9210bf9760_221_0.png)

**1. 邻接矩阵描述如上：**

顶点总数为二维数组的大小，如果有边则值为 `1`，否则无边则为 `0`。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_221_1.png)

## 从顶点 A 开始拓扑排序：A -> B -> C -> D -> E

找到无后继顶点的 `E`，将其保存到 `topologys` 中，最后从图中移除 `E`

![](img/4e0bf091f4d81b2977c8fb9210bf9760_222_0.png)

找到无后继顶点的 `D`，将其保存到 `topologys` 中，最后从图中移除 `D`

![](img/4e0bf091f4d81b2977c8fb9210bf9760_222_1.png)

未找到后继顶点 `C`，则保存到拓扑序中；最后将 `C` 从图中移除。

![](img/4e0bf091f4d81b2977c8fb9210bf9760_223_0.png)

```
<script type="text/javascript">
  class Vertex {
    constructor(data, visited){
      this.data = data;
      this.visited = visited; // Have you visited
    }

    getData() {
      return this.data;
    }
    setData(data) {
      this.data = data;
    }

    isVisited() {
      return this.visited;
    }
    setVisited(visited) {
      this.visited = visited;
    }
  }

  class Graph {
    constructor(maxVertexSize){
        this.maxVertexSize = maxVertexSize;// Two-dimensional array size
        this.vertexs = new Array(maxVertexSize);
        this.topologys = new Array();
        this.adjacencyMatrix = new Array(maxVertexSize);
        for (var i = 0; i < maxVertexSize; i++) {
            this.adjacencyMatrix[i] = new Array();
            for (var j = 0; j < maxVertexSize; j++) {
                this.adjacencyMatrix[i][j] = 0;
            }
        }
        this.size = 0;
    }

    addVertex(data) {
        var vertex = new Vertex(data, false);
        this.vertexs[this.size] = vertex;
        this.size++;
    }

    // Add adjacent edges
    addEdge(from, to) {
      // A -> B and B -> A are different
        this.adjacencyMatrix[from][to] = 1;
    }

    topologySort() {
        while (this.size > 0) {
            var noSuccessorVertex = this.getNoSuccessorVertex();// Get a no successor node
            if (noSuccessorVertex == -1) {
                document.write("There is ring in Graph ");
                return;
            }
            // Copy the deleted node to the sorted array
            this.topologys[this.size - 1] =
            this.vertexs[noSuccessorVertex];
            this.removeVertex(noSuccessorVertex);// Delete no successor node
        }
    }

    getNoSuccessorVertex() {
        var existSuccessor = false;
        for (var row = 0; row < this.size; row++) {// For each vertex
            existSuccessor = false;
          //If the node has a fixed row, each column has a 1，indicating that the node hassucceedors terminating the loop. 
            for (var col = 0; col < this.size; col++) {
                if (this.adjacencyMatrix[row][col] == 1) {
                    existSuccessor = true;
                    break;
                }
            }

          // If no node has a successor, return its subscript. 
            if (!existSuccessor){
                return row;
              }       
        }
        return -1
      }   

    removeVertex(vertex) {
        if (vertex != this.size - 1) {//If the vertex is not on last element ,then you need move up and forward the others in next positions. 
            for (var i = vertex; i < this.size - 1; i++) {// The vertices are removed from the vertex array
                this.vertexs[i] = this.vertexs[i + 1];
            }
            for (var row = vertex; row < this.size - 1; row++) {// move up a row
                for (var col = 0; col < this.size - 1; col++) {
                    this.adjacencyMatrix[row][col] = 
                    this.adjacencyMatrix[row + 1][col];
                }
            }

            for (var col = vertex; col < this.size - 1; col++) {// move left a column
                for (var row = 0; row < this.size - 1; row++) {
                    this.adjacencyMatrix[row][col] = 
                    this.adjacencyMatrix[row][col + 1];
                }
            }
        }
        this.size--; // Decrease the number of vertices
    }

      // Clear reset. Reset visited status for all nodes before sorting again 
  	clear(){	for(var i=0;i<this.vertexs.length; ++i){
        	this.vertexs[i].setVisited(false);      
        }
    	}   

    getgetAdjacencyMatrix() {
        return this.adjacencyMatrix;
      // Get All Vertices   
	getVertices(){	return(this.vertices);}		
  	  	Get Topological Order    
 	getTopologys(){	returnthis.topologys;}  
}  
```
```

```
  ////////////////testing////////////////

  function printGraph(graph) {
    document.write("Two-dimensional array traversal output vertex edge and adjacent array : <br>"); 
		douments .write('&nbsp;&nbsp;&nbsp;'); 
			for(var i=0;i< graph.getVertexs().length ; i++){document.write(graph.getVertexs()[i].getData()+"\n\n\n")}	
	document  write('<div><h4 class="text-center">Two-dimension al array traversal output vertex edge and adjacent matrix:</h3>'); 
		for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
          document.write(graph.getVertexs()[i].getData() + " ");
          for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {     
          	document.write(graph.getVertexs()[i].getData() + " ");
```

```markdown

# 1. 如果只有一个盘子，将其直接移动到 C (A -> C)。

![](img/4e0bf 09if4 dS|b2g _7c8fb9t O_bf96_2.png)

# 2. 当有两个盘子时，使用 B 作为辅助（**A->B**, **A-C**, **B->C**）。

![](img/4e0bf 91 fgd dSl bZ g7 cS fb9 tO_bfi o_o.png) 

# 3. 如果有超过两个盘子，使用 B 作为辅助（**A->B**, **A->C**, **B->C**），并继续递归过程。

## 1. 用记事本创建一个汉诺塔的 html 并在你的浏览器中打开它

```html
<script type="text/javascript">    
    function hanoi(n,A,B,C) {           
        if (n == 1){              
            document.write("Move"+ n+" Ato+ C+"<br>"); 
       }else{                 
  hanoi(n -1, A,C,B); // Move the'n-1th disc on'he'A throughC to B       
      document.write("Move"+n+" from "+A+"to"+C+"<br>");    
  	hanoi(n-1,B,A,C);//Move the n-l tdisconthe'B'throughAtOC        
        }
         
     }  
 
     
   
    ///////////////testing////////////////////   
    
  document.write("Please thenumberof discs1 <br");      
   var n=1;    
    hanoi(n,A,' B','C');       
   
    document .write ("Please enter the number of disco2<br>")  
     var n =2;        
        hanoi(n, ' A ,'B ,' C') ;     
      document .write("Please enter thenumberofdiscs3 <br>");    
          var n= 3;       
    hanoi (n, 'A',' B',,'C ') ; 
</script>
```

## Result :

Please enter the number of discs I  

Move1 A to C   

Please.enterthe nwmberofdics2      

Move1AtoB        

Move2from Atoc    

MovelBoC   

pleaseenterthenumberofdiscs3     

MoveIAtoc         

Move 2 fromAToB       

MOVEICtOb          

Move 3 fron Altc       

MoveI BA to C             

Movc l A tc  

## 1. **斐波那契定义**

```
if n = 0, 1
fn = n
if n > 1
fn = fn-1 + fn-2
```

# 戴克斯特拉

```
if (n == 1 || n == 2)
```

```
var dijkstra(n) {
    var dijkstra(n)
}
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

``` 

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

# 解决方案：

```
if (flags[w] == 'R')
```

```
var i = 1;
```

```


```javascript
<script type="text/javascript">
    var N = 11;
    var M = 3;

    function joseph(man) {
        var count = 1;
        var i = 0, pos = -1;
        var alive = 0;
        while (count <= N) {
            do {
                pos = (pos + 1) % N; // 环形
                if (man[pos] == 0)
                    i++;
                if (i == M) {
                    i = 0;
                    break;
                }
            } while (true);
            man[pos] = count;
            count++;
        }
    }

    //////////////////测试////////////////
    var man = new Array();
    for (var i = 0; i < N; i++)
        man[i] = 0;

    joseph(man);

    document.write("\n约瑟夫序列：<br>");
    for (var i = 0; i < N; i++)
        document.write(man[i] + " , ");
</script>
```

# 结果:

约瑟夫序列：

4，10，1，7，5，2，11，9，3，6，8，

如果您喜欢这本书并在阅读中有所收获，我希望能收到您的消息，希望您能花点时间在亚马逊上发表评论。您的反馈和支持将极大地帮助我们改进，让这本书变得更好。

您现在可以点击此链接。

[http://www.amazon.com/review/create-review?asin=B08D863KFY]

### 不同国家的评论只需修改链接中的亚马逊域名：

- www.amazon.co.uk
- www.amazon.de
- www.amazon.fr
- www.amazon.es
- www.amazon.it
- www.amazon.ca
- www.amazon.nl
- www.amazon.in
- www.amazon.co.jp
- www.amazon.com.br
- www.amazon.com.mx
- www.amazon.com.au

### 祝您未来一切顺利，取得成功！
