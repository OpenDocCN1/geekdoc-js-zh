
# 轻松学习数据结构与算法 ES6+JavaScript

## ES6+ JavaScript 中的经典数据结构与算法

## 读累了记得休息一会哦~

**公众号：古德猫宁李**

- 电子书搜索下载
- 书单分享
- 书友学习交流

**网站：**[沉金书屋](https://www.chenjin5.com)

- 电子书搜索下载
- 电子书打包资源分享
- 学习资源分享

## 冒泡排序算法

冒泡排序算法：比较前两个元素，如果前一个元素大于后一个元素，则交换位置。重复此过程，直到排序完成。

将以下数字从小到大排序。

![](img/Image00001.jpg)

说明：

![](img/Image00002.jpg) 未排序，![](img/Image00003.jpg) 比较中，![](img/Image00004.jpg) 已排序。

1. 第一次排序：

   ![](img/Image00005.jpg)

2. 第二次排序：

   ![](img/Image00006.jpg)

3. 第三次排序：

   ![](img/Image00007.jpg)

4. 第四、五次以此类推：我们可以得到最终从小到大的排序数字。

   ![](img/Image00008.jpg)

5. 使用记事本创建一个 `TestBubbleSort.html` 文件，并在浏览器中打开它。

```javascript
<script type = "text/javascript" >
    class BubbleSort {
        static sort ( arrays ) {
            for ( var i = 0 ; i < arrays.length - 1 ; i ++) {
                for ( var j = 0 ; j < arrays.length - 1 ; j ++) {
                    //swap
                    if ( arrays [ j ] > arrays [ j + 1 ]) {
                        var flag = arrays [ j ];
                        arrays [ j ] = arrays [ j + 1 ];
                        arrays [ j + 1 ] = flag ;
                    }
                }
            }
        }
    }
    //////////////////////testing////////////////////
    var scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];
    BubbleSort.sort ( scores );
    for ( var i = 0 ; i < scores.length ; i ++) {
        document.write ( scores [ i ] + "," );
    }
</script>
```

结果：

![](img/Image00009.jpg)

## 选择排序算法

选择排序算法：从数组中剩余的无序元素中选择最小的一个，插入到已排序序列的前面。

将以下数字从小到大排序。

![](img/Image00010.jpg)

说明：

![](img/Image00002.jpg) 未排序，![](img/Image00003.jpg) 比较中，![](img/Image00004.jpg) 已排序。

1. 第一次排序：

   ![](img/Image00011.jpg)

   ![](img/Image00012.jpg)

2. 第二次排序：

   ![](img/Image00013.jpg)

   ![](img/Image00014.jpg)

3. 第三次排序：

   ![](img/Image00015.jpg)

   ![](img/Image00016.jpg)

4. 第四次排序：

   ![](img/Image00017.jpg)

5. 第五次排序：

   ![](img/Image00018.jpg)

6. 使用记事本创建一个 `TestSelectSort.html` 文件，并在浏览器中打开它。

```javascript
<script type = "text/javascript" >
    class SelectSort {
        static sort ( arrays ) {
            var len = arrays.length - 1 ;
            var minIndex ; // Save the index of the selected minimum
            for ( var i = 0 ; i < len ; i ++) {
                minIndex = i ;
                //Save the minimum value of each loop as the first element
                var minValue = arrays [ minIndex ];
                for ( var j = i ; j < len ; j ++) {
                    // Compare with each element if it is less than the minimum value, exchange the minIndex
                    if ( minValue > arrays [ j + 1 ]) {
                        minValue = arrays [ j + 1 ];
                        minIndex = j + 1 ;
                    }
                }
                //if the minimum index changes, the current minimum is exchanged with the minIndex
                if ( i != minIndex ){
                    var temp = arrays [ i ];
                    arrays [ i ] = arrays [ minIndex ];
                    arrays [ minIndex ] = temp ;
                }
            }
        }
    }
    //////////////////////testing////////////////////
    var scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];
    SelectSort.sort ( scores );
    for ( var i = 0 ; i < scores.length ; i ++) {
        document.write ( scores [ i ] + "," );
    }
</script>
```

结果：

![](img/Image00019.jpg)

## 插入排序算法

插入排序算法：从数组中取出一个未排序的新元素，与前面已排序的元素进行比较，如果新元素小于已排序元素，则将新元素插入到其右侧。

将以下数字从小到大排序。

![](img/Image00010.jpg)

说明：

![](img/Image00002.jpg) 未排序的元素，![](img/Image00003.jpg) 插入元素，![](img/Image00004.jpg) 已排序的元素。

1. 第一次排序：

   ![](img/Image00020.jpg)

2. 第二次排序：

   ![](img/Image00021.jpg)

3. 第三次排序：

   ![](img/Image00022.jpg)

4. 第四次排序：

   ![](img/Image00023.jpg)

5. 第五次排序：

   ![](img/Image00024.jpg)

6. 使用记事本创建一个 `TestInsertSort.html` 文件，并在浏览器中打开。

```javascript
<script type = "text/javascript" >

    class InsertSort {

        static sort ( arrays ) {

            for ( var i = 0 ; i < arrays.length ; i ++) {

                var insertElement = arrays [ i ]; //取未排序的新元素

                var insertPosition = i ; //插入位置

                for ( var j = insertPosition - 1 ; j >= 0 ; j --) {

                    //如果新元素小于已排序元素，则右移

                    if ( insertElement < arrays [ j ]) {

                        arrays [ j + 1 ] = arrays [ j ];

                        insertPosition --;

                    }

                }

                arrays [ insertPosition ] = insertElement ; //插入新元素

            }

        }

    }

    //////////////////////测试////////////////////

    var scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];

    InsertSort.sort ( scores );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + "," );

    }

</script>
```

结果：

![](img/Image00025.jpg)

## 二分查找

从已排序的数组中查找给定值的索引位置。

1. 初始化最低索引 `low=0`，最高索引 `high=scores.length-1`。
2. 找到中间索引 `mid=(low+high)/2` 对应的值 `scores[mid]`。
3. 将中间值 `scores[mid]` 与 `searchValue` 比较：
   - 如果 `scores[mid]==searchValue`，则输出当前 `mid` 索引。
   - 如果 `scores[mid]>searchValue`，说明要查找的 `searchValue` 位于 `low` 和 `mid-1` 之间。
4. 依此类推。重复步骤 3，直到找到 `searchValue` 或 `low>=high` 时终止循环。

### 示例 1

在下面已排序的数组中查找 `searchValue=40` 的索引。

![](img/Image00026.jpg)

![](img/Image00027.jpg)

### 示例 2

在下面已排序的数组中查找 `searchValue=90` 的索引。

![](img/Image00028.jpg)

![](img/Image00029.jpg)

1. 使用记事本创建一个 `TestBinarySearch.html` 文件，并在浏览器中打开。

```javascript
<script type = "text/javascript" >

    class BinarySearch {

        static search ( arrays , searchValue ) {

            var low = 0 ;

            var high = arrays.length - 1 ;

            var mid = 0 ;

            while ( low <= high ) {

                mid = ( low + high ) / 2 ;

                if ( arrays [ mid ] == searchValue ) {

                    return mid ;

                } else if ( arrays [ mid ] < searchValue ) {

                    low = mid + 1 ;

                } else if ( arrays [ mid ] > searchValue ) {

                    high = mid - 1 ;

                }

            }

            return - 1 ;

        }

    }

    //////////////////////测试////////////////////

    var scores = [ 30 , 40 , 50 , 70 , 85 , 90 , 100 ];

    var searchValue = 40 ;

    var position = BinarySearch.search ( scores , searchValue );

    document.write ( searchValue + " 的位置:" + position );

    document.write ( "<br>-----------------------------<br>" );

    searchValue = 90 ;

    position = BinarySearch.search ( scores , searchValue );

    document.write ( searchValue + " 的位置:" + position );

</script>
```

结果：

![](img/Image00030.jpg)

## 单向链表

是线性表的链式存储结构，由节点连接而成。每个节点由 `data` 和指向下一个节点的 `next` 指针组成。

![](img/Image00031.jpg)

### UML 图

```javascript
    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }
```

1. 单向链表初始化。

   示例：构建一个旧金山地铁单向链表。

   ![](img/Image00033.jpg)

2. 遍历输出。

   ![](img/Image00034.jpg)

3. 使用记事本创建一个 `TestUnidirectionalLinkedList.html` 文件，并在浏览器中打开。



```javascript
<script type="text/javascript">

    class Node {

        constructor(data, next) {
            this.data = data;
            this.next = next;
        }

        getData() {
            return this.data;
        }
    }

    class LinkedList {

        init() {
            // 第一个节点称为头节点
            this.head = new Node("San Francisco", null);

            var nodeOakland = new Node("Oakland", null);
            this.head.next = nodeOakland;

            var nodeBerkeley = new Node("Berkeley", null);
            nodeOakland.next = nodeBerkeley;

            // 最后一个节点称为尾节点
            this.tail = new Node("Fremont", null);
            nodeBerkeley.next = this.tail;

            return this.head;
        }

        print(node) {
            var p = node;

            while (p != null) // 从头到尾
            {
                var data = p.getData();
                document.write(data + " -> ");
                p = p.next;
            }

            document.write("End<br><br>");
        }
    }

    //////////////////////测试////////////////////

    var linkedList = new LinkedList();
    var head = linkedList.init();

    linkedList.print(head);

</script>
```

结果：

![](img/Image00035.jpg)

### 3. 在末尾追加一个名为 Walnut 的新节点

![](img/Image00036.jpg)

1. 使用记事本创建一个 `TestUnidirectionalLinkedListAppend.html` 文件。

```javascript
<script type="text/javascript">

    class Node {

        constructor(data, next) {
            this.data = data;
            this.next = next;
        }

        getData() {
            return this.data;
        }
    }

    class LinkedList {

        init() {
            // 第一个节点称为头节点
            this.head = new Node("San Francisco", null);

            var nodeOakland = new Node("Oakland", null);
            this.head.next = nodeOakland;

            var nodeBerkeley = new Node("Berkeley", null);
            nodeOakland.next = nodeBerkeley;

            // 最后一个节点称为尾节点
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

            while (p != null) // 从头到尾
            {
                var data = p.getData();
                document.write(data + " -> ");
                p = p.next;
            }

            document.write("End<br><br>");
        }
    }

    //////////////////////测试////////////////////

    var linkedList = new LinkedList();
    var head = linkedList.init();

    document.write("在末尾追加一个名为 Walnut 的新节点: <br>");
    linkedList.add(new Node("Walnut", null));
    linkedList.print(head);

</script>
```

结果：

![](img/Image00037.jpg)

### 3. 在位置 2 插入一个节点 Walnut

![](img/Image00038.jpg)

1. 使用记事本创建一个 `TestUnidirectionalLinkedListInsert.html` 文件。

```javascript
<script type="text/javascript">

    class Node {

        constructor(data, next) {
            this.data = data;
            this.next = next;
        }

        getData() {
            return this.data;
        }
    }

    class LinkedList {

        init() {
            // 第一个节点称为头节点
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

            // Move the node to the insertion position
            while (p.next != null && i < insertPosition - 1) {
                p = p.next;
                i++;
            }

            newNode.next = p.next; // newNode next point to next node
            p.next = newNode; // current next point to newNode
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

    //////////////////////testing////////////////////

    var linkedList = new LinkedList();
    var head = linkedList.init();

    document.write("Insert a new node Walnut at index = 2 : <br>");
    linkedList.insert(2, new Node("Walnut", null));
    linkedList.print(head);

</script>
```

结果：

![](img/Image00039.jpg)

### 4. 删除 `index=2` 的节点

![](img/Image00040.jpg)

1. 用记事本创建 `TestUnidirectionalLinkedListDelete.html`。

```javascript
<script type="text/javascript">

    class Node {

        constructor(data, next) {
            this.data = data;
            this.next = next;
        }

        getData() {
            return this.data;
        }
    }

    class LinkedList {

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

            // Move the node to the previous node position that was deleted
            while (p.next != null && i < removePosition - 1) {
                p = p.next;
                i++;
            }

            var temp = p.next; // Save the node you want to delete
            p.next = p.next.next; // Previous node next points to next of delete the node
            temp.next = null;
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

    //////////////////////testing////////////////////

    var linkedList = new LinkedList();
    var head = linkedList.init();

    document.write("Delete a new node Berkeley at index = 2 : <br>");
    linkedList.remove(2);
    linkedList.print(head);

</script>
```

结果：

![](img/Image00041.jpg)

## 双向链表

双向链表：

它是线性表的一种链式存储结构，由节点在两个方向上连接而成。每个节点由数据、指向前一个节点的指针和指向后一个节点的指针组成。

![](img/Image00042.jpg)

### UML 图

![](img/Image00043.jpg)

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

### 1. 双向链表初始化

示例：构建一个旧金山地铁双向链表。

![](img/Image00044.jpg)

### 2. 用记事本创建 `TestDoubleLink.html`



```javascript
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleLinkList {

        init () {

            this.head = new Node ( "San Francisco" );

            this.head.prev = null ;

            this.head.next = null ;

            var nodeOakland = new Node ( "Oakland" );

            nodeOakland.prev = this.head ;

            nodeOakland.next = null ;

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" );

            nodeBerkeley.prev = nodeOakland ;

            nodeBerkeley.next = null ;

            nodeOakland.next = nodeBerkeley ;

            this.tail = new Node ( "Fremont" );

            this.tail.prev = nodeBerkeley ;

            this.tail.next = null ;

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        print ( node ) {

            var p = node ;

            var end = null ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                end = p ;

                p = p.next ;

            }

            document.write ( "End <br><br>" );

            p = end ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            }

            document.write ( "Start<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleLinkList = new DoubleLinkList ();

    var head = doubleLinkList.init ();

    doubleLinkList.print ( head );

</script>
```

结果：

![](img/Image00045.jpg)

### 3. 在 Fremont 末尾添加一个节点 Walnut

![](img/Image00046.jpg)

用记事本创建 `TestDoubleLinkAdd.html`。

```javascript
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleLinkList {

        init () {

            this.head = new Node ( "San Francisco" );

            this.head.prev = null ;

            this.head.next = null ;

            var nodeOakland = new Node ( "Oakland" );

            nodeOakland.prev = this.head ;

            nodeOakland.next = null ;

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" );

            nodeBerkeley.prev = nodeOakland ;

            nodeBerkeley.next = null ;

            nodeOakland.next = nodeBerkeley ;

            this.tail = new Node ( "Fremont" );

            this.tail.prev = nodeBerkeley ;

            this.tail.next = null ;

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        add ( newNode ) {

            this.tail.next = newNode ;

            newNode.prev = this.tail ;

            this.tail = newNode ;

        }

        print ( node ) {

            var p = node ;

            var end = null ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                end = p ;

                p = p.next ;

            }

            document.write ( "End <br><br>" );

            p = end ;

            while ( p != null )

            {
                var data = p.getData ();
                document.write ( data + " -> " );
                p = p.prev ;
            }

            document.write ( "Start<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleLinkList = new DoubleLinkList ();

    var head = doubleLinkList.init ();

    doubleLinkList.add ( new Node ( "Walnut" ));

    doubleLinkList.print ( head );

</script>
```

结果：

![](img/Image00047.jpg)

### 3. 在位置 2 插入一个节点 Walnut

![](img/Image00048.jpg)

使用记事本创建 `TestDoubleLinkInsert.html`。

```javascript
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleLinkList {

        init () {

            this.head = new Node ( "San Francisco" );

            this.head.prev = null ;

            this.head.next = null ;

            var nodeOakland = new Node ( "Oakland" );

            nodeOakland.prev = this.head ;

            nodeOakland.next = null ;

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" );

            nodeBerkeley.prev = nodeOakland ;

            nodeBerkeley.next = null ;

            nodeOakland.next = nodeBerkeley ;

            this.tail = new Node ( "Fremont" );

            this.tail.prev = nodeBerkeley ;

            this.tail.next = null ;

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        insert ( insertPosition , newNode ) {

            var p = this.head ;

            var i = 0 ;

            // Move the node to the insertion position

            while ( p.next != null && i < insertPosition - 1 ) {

                p = p.next ;

                i ++;

            }

            newNode.next = p.next ;

            p.next = newNode ;

            newNode.prev = p ;

            newNode.next.prev = newNode ;

        }

        print ( node ) {

            var p = node ;

            var end = null ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                end = p ;

                p = p.next ;

            }

            document.write ( "End <br><br>" );

            p = end ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            }

            document.write ( "Start<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleLinkList = new DoubleLinkList ();

    var head = doubleLinkList.init ();

    document.write ( "Insert a new node Walnut at index = 2 : <br>" );

    doubleLinkList.insert ( 2 , new Node ( "Walnut" ));

    doubleLinkList.print ( head );

</script>
```

结果：

![](img/Image00049.jpg)

### 4. 删除索引为 2 的节点

![](img/Image00050.jpg)

使用记事本创建 `TestDoubleLinkDelete.html`。



```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleLinkList {

        init () {

            this.head = new Node ( "San Francisco" );

            this.head.prev = null ;

            this.head.next = null ;

            var nodeOakland = new Node ( "Oakland" );

            nodeOakland.prev = this.head ;

            nodeOakland.next = null ;

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" );

            nodeBerkeley.prev = nodeOakland ;

            nodeBerkeley.next = null ;

            nodeOakland.next = nodeBerkeley ;

            this.tail = new Node ( "Fremont" );

            this.tail.prev = nodeBerkeley ;

            this.tail.next = null ;

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        remove ( removePosition ) {

            var p = this.head ;

            var i = 0 ;

            // Move the node to the previous node  that was deleted

            while ( p.next != null && i < removePosition - 1 ) {

                p = p.next ;

                i ++;

            }

            var temp = p.next ; // Save the node you want to delete

            p.next = p.next.next ;

            p.next.prev = p ;

            temp.next = null ; // Set the delete node next to null

            temp.prev = null ; // Set the delete node prev to null

        }

        print ( node ) {

            var p = node ;

            var end = null ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                end = p ;

                p = p.next ;

            }

            document.write ( "End <br><br>" );

            p = end ;

            while ( p != null )

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            }

            document.write ( "Start<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleLinkList = new DoubleLinkList ();

    var head = doubleLinkList.init ();

    document.write ( "Delete a new node Berkeley at index = 2 : <br>" );

    doubleLinkList.remove ( 2 );

    doubleLinkList.print ( head );

</script>
```

结果：

![](img/Image00051.jpg)

## 单向循环链表

### 单向循环链表

它是线性表的一种链式存储结构，通过节点单向连接，并首尾相连形成一个环，每个节点由数据和指针 `next` 组成。

![](img/Image00052.jpg)

### UML 图

![](img/Image00053.jpg)

```javascript
class Node {

    constructor ( data , next ){

        this.data = data ;

        this.next = next ;

    }

    getData (){

        return this.data ;

    }

}
```

### 1. 单向循环链表的初始化与遍历输出

![](img/Image00054.jpg)

使用记事本创建 `TestSingleCircleLink.html`。

```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class SingleCircleLink {

        init () {

            // the first node called head node

            this.head = new Node ( "A" );

            this.head.next = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeB.next = nodeC ;

            // the last node called tail node

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            nodeC.next = this.tail ;

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var singleCircleLink = new SingleCircleLink ();

    var head = singleCircleLink.init ();

    singleCircleLink.print ( head );

</script>
```

结果：

![](img/Image00055.jpg)

### 3. 在位置 2 插入一个节点 E

![](img/Image00056.jpg)

![](img/Image00057.jpg)

使用记事本创建 `TestSingleCircleLinkInsert.html`。

```javascript
<script type = "text/javascript" >

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class SingleCircleLink {

        init () {

            // 第一个节点称为头节点

            this.head = new Node ( "A" );

            this.head.next = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeB.next = nodeC ;

            // 最后一个节点称为尾节点

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            nodeC.next = this.tail ;

        }

        insert ( insertPosition , newNode ) {

            var p = this.head ;

            var i = 0 ;

            // 将节点移动到插入位置

            while ( p.next != null && i < insertPosition - 1 ) {

                p = p.next ;

                i ++;

            }

            newNode.next = p.next ;

            p.next = newNode ;

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////测试////////////////////

    var singleCircleLink = new SingleCircleLink ();

    var head = singleCircleLink.init ();

    document.write ( "在索引 2 处插入新节点 E：<br>" );

    singleCircleLink.insert ( 2 , new Node ( "E" ));

    singleCircleLink.print ( head );

</script>
```

结果：

![](img/Image00058.jpg)

### 4. 删除 `index` = 2 的节点

![](img/Image00059.jpg)

![](img/Image00060.jpg)

使用记事本创建 `TestSingleCircleLinkDelete.html`。

```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class SingleCircleLink {

        init () {

            // 第一个节点称为头节点

            this.head = new Node ( "A" );

            this.head.next = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeB.next = nodeC ;

            // 最后一个节点称为尾节点

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            nodeC.next = this.tail ;

        }

        remove ( removePosition ) {

            var p = this.head ;

            var i = 0 ;

            while ( p.next != null && i < removePosition - 1 ) {

                p = p.next ;

                i ++;

            }

            var temp = p.next ;

            p.next = p.next.next ;

            temp.next = null ;

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////测试////////////////////
```



```javascript
var singleCircleLink = new SingleCircleLink ();

singleCircleLink.init ();

document.write ( "在索引 2 处删除节点 C：<br>" );

singleCircleLink.remove ( 2 );

singleCircleLink.print ();

</script>
```

结果：

![](img/Image00061.jpg)

## 双向循环链表

双向循环链表是一种线性表的链式存储结构。节点通过两个方向串联起来，并连接成环。每个节点由 `data`、指向前一个节点的 `prev` 和指向后一个节点的 `next` 组成。

![](img/Image00062.jpg)

### UML 图

![](img/Image00063.jpg)

```javascript
class Node {

    constructor ( data , prev , next ){

        this.data = data ;

        this.prev = prev ;

        this.next = next ;

    }

    getData (){

        return this.data ;

    }

}
```

### 1. 双向循环链表的初始化与遍历输出

![](img/Image00064.jpg)

![](img/Image00065.jpg)

使用记事本创建 `TestDoubleCircleLink.html`。

```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleCircleLink {

        init () {

            // 第一个节点称为头节点

            this.head = new Node ( "A" );

            this.head.next = null ;

            this.head.prev = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            nodeB.prev = this.head ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeC.prev = nodeB ;

            nodeB.next = nodeC ;

            // 最后一个节点称为尾节点

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            this.tail.prev = nodeC ;

            nodeC.next = this.tail ;

            this.head.prev = this.tail ;

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

            p = this.tail ;

            do {

                data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            } while ( p != this.tail );

            data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////测试////////////////////

    var doubleCircleLink = new DoubleCircleLink ();

    doubleCircleLink.init ();

    doubleCircleLink.print ();

</script>
```

结果：

![](img/Image00066.jpg)

### 2. 在位置 2 插入节点 E

![](img/Image00067.jpg)

![](img/Image00068.jpg)

使用记事本创建 `TestDoubleCircleLinkInsert.html`。

```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleCircleLink {

        init () {

            // 第一个节点称为头节点

            this.head = new Node ( "A" );

            this.head.next = null ;

            this.head.prev = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            nodeB.prev = this.head ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeC.prev = nodeB ;

            nodeB.next = nodeC ;

            // 最后一个节点称为尾节点

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            this.tail.prev = nodeC ;

            nodeC.next = this.tail ;

            this.head.prev = this.tail ;

        }

        insert ( insertPosition , newNode ) {

            var p = this.head ;

            var i = 0 ;

            // 将节点移动到插入位置

            while ( p.next != null && i < insertPosition - 1 ) {

                p = p.next ;

                i ++;

            }

            newNode.next = p.next ;

            p.next = newNode ;

            newNode.prev = p ;

            newNode.next.prev = newNode ;

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

            p = this.tail ;

            do {

                data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            } while ( p != this.tail );

            data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleCircleLink = new DoubleCircleLink ();

    doubleCircleLink.init ();

    document.write ( "Insert a new E at index = 2 : <br>" );

    doubleCircleLink.insert ( 2 , new Node ( "E" ));

    doubleCircleLink.print ();

</script>
```

结果：

![](img/Image00069.jpg)

### 3. 删除索引为 2 的节点

![](img/Image00070.jpg)

![](img/Image00071.jpg)

使用记事本创建一个 `TestDoubleCircleLinkDelete.html` 文件。

```html
<script type = "text/javascript" >

    class Node {

        constructor ( data , prev , next ){

            this.data = data ;

            this.prev = prev ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

    class DoubleCircleLink {

        init () {

            // the first node called head node

            this.head = new Node ( "A" );

            this.head.next = null ;

            this.head.prev = null ;

            var nodeB = new Node ( "B" );

            nodeB.next = null ;

            nodeB.prev = this.head ;

            this.head.next = nodeB ;

            var nodeC = new Node ( "C" );

            nodeC.next = null ;

            nodeC.prev = nodeB ;

            nodeB.next = nodeC ;

            // the last node called tail node

            this.tail = new Node ( "D" );

            this.tail.next = this.head ;

            this.tail.prev = nodeC ;

            nodeC.next = this.tail ;

            this.head.prev = this.tail ;

        }

        remove ( removePosition ) {

            var p = this.head ;

            var i = 0 ;

            while ( p.next != null && i < removePosition - 1 ) {

                p = p.next ;

                i ++;

            }

            var temp = p.next ;

            p.next = p.next.next ;

            p.next.prev = p ;

            temp.next = null ; //Set the delete node next to null

            temp.prev = null ; // Set the delete node prev to null

        }

        print () {

            var p = this.head ;

            do {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            } while ( p != this.head );

            var data = p.getData ();

            document.write ( data + "<br><br>" );

            p = this.tail ;

            do {

                data = p.getData ();

                document.write ( data + " -> " );

                p = p.prev ;

            } while ( p != this.tail );

            data = p.getData ();

            document.write ( data + "<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var doubleCircleLink = new DoubleCircleLink ();

    doubleCircleLink.init ();

    document.write ( "Delete a node C at index = 2 : <br>" );

    doubleCircleLink.remove ( 2 );

    doubleCircleLink.print ();

</script>
```

结果：

![](img/Image00072.jpg)

## 队列

队列是一个 FIFO（先进先出）序列。

![](img/Image00073.jpg)

### UML 图

![](img/Image00074.jpg)

```javascript
class Node {

    constructor ( data , prev , next ){

        this.data = data ;

        this.prev = prev ;

        this.next = next ;

    }

    getData (){

        return this.data ;

    }

}
```



# 1. 队列初始化与遍历输出

初始化插入 A。

![](img/Image00075.jpg)

初始化插入 B。

![](img/Image00076.jpg)

初始化插入 C。

![](img/Image00077.jpg)

初始化插入 D。

![](img/Image00078.jpg)

使用记事本创建一个 `TestQueue.html` 文件。

```html
<script type="text/javascript">
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

    class Queue {
        constructor() {
            this.head = null;
            this.tail = null;
            this.size = 0;
        }

        offer(element) {
            if (this.head == null) {
                this.head = new Node(element);
                this.tail = this.head;
            } else {
                var newNode = new Node(element);
                newNode.next = this.tail;
                this.tail.prev = newNode;
                this.tail = newNode;
            }

            this.size++;
        }

        poll() {
            var p = this.head;

            if (p == null) {
                return null;
            }

            this.head = this.head.prev;
            p.next = null;
            p.prev = null;
            this.size--;

            return p;
        }

        size() {
            return this.size;
        }
    }

    //////////////////////testing////////////////////

    function print(queue) {
        document.write("Head ");

        var node = null;

        while ((node = queue.poll()) != null) {
            document.write(node.getData() + " <- ");
        }

        document.write("Tail <br>");
    }

    var queue = new Queue();

    queue.offer("A");
    queue.offer("B");
    queue.offer("C");
    queue.offer("D");

    print(queue);
</script>
```

结果：

![](img/Image00079.jpg)

# 栈

栈：

FILO（先进后出）序列。

![](img/Image00080.jpg)

## UML 图

![](img/Image00081.jpg)

```javascript
class Node {
    constructor(data, next) {
        this.data = data;
        this.next = next;
    }

    getData() {
        return this.data;
    }
}
```

## 1. 栈初始化与遍历输出

将 A 压入栈。

![](img/Image00082.jpg)

将 B 压入栈。

![](img/Image00083.jpg)

将 C 压入栈。

![](img/Image00084.jpg)

同样将 D 压入栈：

![](img/Image00085.jpg)

如果从栈中弹出 D：

![](img/Image00086.jpg)

使用记事本创建一个 `TestStack.html` 文件。

```html
<script type="text/javascript">
    class Node {
        constructor(data, next) {
            this.data = data;
            this.next = next;
        }

        getData() {
            return this.data;
        }
    }

    class Stack {
        constructor() {
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
            this.top = this.top.next; // top move down
            p.next = null;
            this.size--;

            return p;
        }

        size() {
            return this.size;
        }
    }

    //////////////////////testing////////////////////

    function print(stack) {
        document.write("Top ");

        var node = null;

        while ((node = stack.pop()) != null) {
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

![](img/Image00087.jpg)

# 递归算法

递归算法：

程序函数自身调用自身，层层递进，直到满足某个条件，再逐步返回至结束。

## 1. n 的阶乘

`n*(n-1)*(n-2) ...... *2*1`

使用记事本创建 `TestRecursive.html`。

```html
<script type="text/javascript">
    function factorial(n) {
        if (n == 1) {
            return 1;
        } else {
            // 递归调用自身，直到返回结束
            return factorial(n - 1) * n;
        }
    }

    //////////////////////测试////////////////////

    var n = 5;
    var fac = factorial(n);

    document.write("5 的阶乘是：" + fac);
</script>
```

结果：

![](img/Image00088.jpg)

图解分析：

![](img/Image00089.jpg)

![](img/Image00090.jpg)

# 二路归并算法

二路归并算法：

将前半部分和后半部分的数据分别排序，再将两个有序子列表合并成一个有序列表，如此递归直至结束。

## 1. 对分数 {50, 65, 99, 87, 74, 63, 76, 100} 进行归并排序

![](img/Image00091.jpg)

使用记事本创建 `TestMergeSort.html`。

```html
<script type="text/javascript">
    class MergeSort {
        sort(array) {
            var temp = new Array(array.length);
            this.mergeSort(array, temp, 0, array.length - 1);
        }

        mergeSort(array, temp, left, right) {
            if (left < right) {
                var center = parseInt((left + right) / 2);

                this.mergeSort(array, temp, left, center); // 左半部分归并排序
                this.mergeSort(array, temp, center + 1, right); // 右半部分归并排序
                this.merge(array, temp, left, center + 1, right); // 合并两个有序数组
            }
        }

        /**
         将两个有序列表合并成一个有序列表

         temp : 临时数组
         left :    左侧起始下标
         right :  右侧起始下标
         rightEndIndex : 右侧结束下标
         */

        merge(array, temp, left, right, rightEndIndex) {
            var leftEndIndex = right - 1; // 左侧结束下标
            var tempIndex = left; // 从左侧开始计数
            var elementNumber = rightEndIndex - left + 1;

            while (left <= leftEndIndex && right <= rightEndIndex) {
                if (array[left] <= array[right]) {
                    temp[tempIndex++] = array[left++];
                } else {
                    temp[tempIndex++] = array[right++];
                }
            }

            while (left <= leftEndIndex) { // 如果左侧还有元素
                temp[tempIndex++] = array[left++];
            }

            while (right <= rightEndIndex) { // 如果右侧还有元素
                temp[tempIndex++] = array[right++];
            }

            // 将 temp 复制回 array
            for (var i = 0; i < elementNumber; i++) {
                array[rightEndIndex] = temp[rightEndIndex];
                rightEndIndex--;
            }
        }
    }

    //////////////////////测试////////////////////

    var scores = [50, 65, 99, 87, 74, 63, 76, 100, 92];
    var mergeSort = new MergeSort();

    mergeSort.sort(scores);

    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }
</script>
```

结果：

![](img/Image00092.jpg)

# 快速排序算法

快速排序算法：

将数组分成两个子数组，然后递归调用自身，对子数组进行快速排序，直至结束。

## 1. 对分数 {90, 60, 50, 80, 70, 100} 进行快速排序

![](img/Image00093.jpg)

![](img/Image00094.jpg)

![](img/Image00095.jpg)

![](img/Image00096.jpg)

使用记事本创建 `TestQuickSort.html`。

```html
<script type="text/javascript">
    class QuickSort {
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
                // 从右向左找到第一个小于阈值的位置
                while (i < j && array[j] > threshold) {
                    j--;
                }

                // 将比阈值小的数替换到低位
                if (i < j) {
                    array[i++] = array[j];
                }

                // 从左向右找到第一个大于阈值的位置
                while (i < j && array[i] <= threshold) {
                    i++;
                }
```



```javascript
}

                // 将比阈值大的数替换到高位
                if (i < j)
                    array[j--] = array[i];

            }

            array[i] = threshold;

            // 左侧快速排序
            this.quickSort(array, low, i - 1);

            // 右侧快速排序
            this.quickSort(array, i + 1, high);

        }

    }

    //////////////////////测试////////////////////

    var scores = [90, 60, 50, 80, 70, 100];

    var quickSort = new QuickSort();

    quickSort.sort(scores);

    for (var i = 0; i < scores.length; i++) {
        document.write(scores[i] + ",");
    }

</script>
```

结果：

![](img/Image00097.jpg)

## 二叉搜索树

二叉搜索树：

1. 若任意节点的左子树不为空，则左子树上所有节点的值均小于其根节点的值；
2. 若任意节点的右子树不为空，则右子树上所有节点的值均大于其根节点的值；
3. 任意节点的左、右子树也分别为二叉搜索树。

![](img/Image00098.jpg)

节点 UML 图：

![](img/Image00099.jpg)

```javascript
class Node {
    constructor(data, left, right) {
        this.data = data;
        this.left = left;
        this.right = right;
    }

    getData() {
        return this.data;
    }
}
```

### 1. 构建二叉搜索树，插入节点

插入的节点从根节点开始比较，若小于根节点则与根节点的左子树比较，否则与右子树比较，直到左子树为空或右子树为空，然后插入。

插入 60：

![](img/Image00100.jpg)

插入 40：

![](img/Image00101.jpg)

插入 20：

![](img/Image00102.jpg)

插入 10：

![](img/Image00103.jpg)

插入 30：

![](img/Image00104.jpg)

插入 50：

![](img/Image00105.jpg)

插入 80：

![](img/Image00106.jpg)

插入 70：

![](img/Image00107.jpg)

插入 90：

![](img/Image00108.jpg)

### 2. 二叉搜索树的中序遍历

中序遍历：左子树 -> 根节点 -> 右子树

![](img/Image00109.jpg)

结果：

![](img/Image00110.jpg)

使用记事本创建 `TestBinarySearchTreeInOrder.html`。

```html
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

            // 递归左子树，继续查找插入位置
</script>
```

### 3. 中序遍历二叉搜索树

使用记事本创建一个 `TestBinarySearchTreeInOrder.html` 文件。

```html
<script type="text/javascript">
    class BinaryTree {
        getRoot() {
            return this.root;
        }

        //In-order traversal binary search tree
        inOrder(root) {
            if (root == null) {
                return;
            }

            this.inOrder(root.left); // Recursive Traversing the left subtree
            document.write(root.getData() + ", ");
            this.inOrder(root.right); // Recursive Traversing the right subtree
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
            } else if (compareValue > 0) {
                ////Recursive right subtree, continue to find the insertion position
                if (node.right == null) {
                    node.right = new Node(newData, null, null);
                } else {
                    this.insert(node.right, newData);
                }
            }
        }
    }

    class Node {
        constructor(data, left, right) {
            this.data = data;
            this.left = left;
            this.right = right;
        }

        getData() {
            return this.data;
        }
    }

    //////////////////////testing////////////////////

    var binaryTree = new BinaryTree();

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

    document.write("<br> In-order traversal binary search tree <br>");
    binaryTree.inOrder(binaryTree.getRoot());
</script>
```

结果：

![](img/Image00111.jpg)

### 4. 二叉搜索树前序遍历

前序遍历：根节点 -> 左子树 -> 右子树

![](img/Image00112.jpg)

结果：

![](img/Image00113.jpg)

使用记事本创建一个 `TestBinarySearchTreePreOrder.html` 文件。

```html
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
            } else if (compareValue > 0) {
                ////Recursive right subtree, continue to find the insertion position
                if (node.right == null) {
                    node.right = new Node(newData, null, null);
                } else {
                    this.insert(node.right, newData);
                }
            }
        }
    }

    class Node {
        constructor(data, left, right) {
            this.data = data;
            this.left = left;
            this.right = right;
        }

        getData() {
            return this.data;
        }
    }

    //////////////////////testing////////////////////

    var binaryTree = new BinaryTree();

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

结果：

![](img/Image00114.jpg)

### 5. 二叉搜索树后序遍历

后序遍历：右子树 -> 根节点 -> 左子树

![](img/Image00115.jpg)

结果：

![](img/Image00116.jpg)

使用记事本创建一个 `TestBinarySearchTreePostOrder.html` 文件。

```html
<script type="text/javascript">
    class BinaryTree {
        getRoot() {
            return this.root;
        }

        //Post-order traversal binary search tree
        postOrder(root) {
            if (root == null) {
                return;
            }



```javascript
this.postOrder(root.left); // Recursive Traversing the left subtree

this.postOrder(root.right); // Recursive Traversing the right subtree

document.write(root.getData() + ", ");
}

insert(node, newData) {
    if (this.root == null) {
        this.root = new Node(newData, null, null);
        return;
    }

    var compareValue = newData - node.getData();

    // Recursive left subtree, continue to find the insertion position
    if (compareValue < 0) {
        if (node.left == null) {
            node.left = new Node(newData, null, null);
        } else {
            this.insert(node.left, newData);
        }
    } else if (compareValue > 0) {
        // Recursive right subtree, continue to find the insertion position
        if (node.right == null) {
            node.right = new Node(newData, null, null);
        } else {
            this.insert(node.right, newData);
        }
    }
}
}

class Node {
    constructor(data, left, right) {
        this.data = data;
        this.left = left;
        this.right = right;
    }

    getData() {
        return this.data;
    }
}

// Testing
var binaryTree = new BinaryTree();

// Constructing a binary search tree
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
```

结果：

![](img/Image00117.jpg)

### 4. 二叉搜索树的最大值和最小值

最小值：较小的值位于左子节点，只要递归遍历左子节点直到为空，当前节点即为最小节点。

最大值：较大的值位于右子节点，只要递归遍历右子节点直到为空，当前节点即为最大节点。

![](img/Image00118.jpg)

![](img/Image00119.jpg)

使用记事本创建一个`TestBinarySearchTreeMaxMinValue.html`文件。

```html
<script type="text/javascript">
class BinaryTree {
    getRoot() {
        return this.root;
    }

    // Minimum value
    searchMinValue(node) {
        if (node == null || node.getData() == 0) {
            return null;
        }

        if (node.left == null) {
            return node;
        }

        // Recursively find the minimum from the left subtree
        return this.searchMinValue(node.left);
    }

    // Maximum value
    searchMaxValue(node) {
        if (node == null || node.getData() == 0) {
            return null;
        }

        if (node.right == null) {
            return node;
        }

        // Recursively find the minimum from the right subtree
        return this.searchMaxValue(node.right);
    }

    insert(node, newData) {
        if (this.root == null) {
            this.root = new Node(newData, null, null);
            return;
        }

        var compareValue = newData - node.getData();

        // Recursive left subtree, continue to find the insertion position
        if (compareValue < 0) {
            if (node.left == null) {
                node.left = new Node(newData, null, null);
            } else {
                this.insert(node.left, newData);
            }
        } else if (compareValue > 0) {
            // Recursive right subtree, continue to find the insertion position
            if (node.right == null) {
                node.right = new Node(newData, null, null);
            } else {
                this.insert(node.right, newData);
            }
        }
    }
}

class Node {
    constructor(data, left, right) {
        this.data = data;
        this.left = left;
        this.right = right;
    }

    getData() {
        return this.data;
    }
}

// Testing
var binaryTree = new BinaryTree();

// Constructing a binary search tree
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

结果：

![](img/Image00120.jpg)

### 6. 二叉搜索树删除节点

二叉搜索树删除节点有三种情况：

1. 如果没有子节点，直接删除。
2. 如果只有一个子节点，子节点替换当前节点，然后删除当前节点。
3. 如果有两个子节点，用右子树中最小的节点替换当前节点，因为右边最小的节点也大于左边的值。

![](img/Image00121.jpg)

![](img/Image00122.jpg)

![](img/Image00123.jpg)

![](img/Image00124.jpg)

![](img/Image00125.jpg)

![](img/Image00126.jpg)

用记事本创建`TestBinarySearchTreeDelete.html`。



```javascript
<script type = "text/javascript" >

    class BinaryTree {

        getRoot () {
            return this.root ;
        }

         // In-order traversal binary search tree
        inOrder ( root ) {
            if ( root == null ) {
                return ;
            }
            this.inOrder ( root.left ); // Traversing the left subtree
            document.write ( root.getData () + ", " );
            this.inOrder ( root.right ); // Traversing the right subtree
        }

        remove ( node , newData ) {
            if ( node == null )
                return node ;
            var compareValue = newData - node.getData ();
            if ( compareValue > 0 ) {
                node.right = this.remove ( node.right , newData );
            } else if ( compareValue < 0 ) {
                node.left = this.remove ( node.left , newData );
            } else if ( node.left != null && node.right != null ) {
                //Find the minimum node of the right subtree to replace the current node
                node.setData ( this.searchMinValue ( node.right ). getData ());
                node.right = this.remove ( node.right , node.getData ());
            } else {
                node = ( node.left != null ) ? node.left : node.right ;
            }
            return node ;
        }

        //Search minimum
        searchMinValue ( node ) {
            if ( node == null || node.getData () == 0 )
                return null ;
            if ( node.left == null ) {
                return node ;
            }
            //Recursively find the minimum from the left subtree
            return this.searchMinValue ( node.left );
        }

        insert ( node , newData ) {
            if ( this.root == null ) {
                this.root = new Node ( newData , null , null );
                return ;
            }
            var compareValue = newData - node.getData ();
            //Recursive left subtree, continue to find the insertion position
            if ( compareValue < 0 ) {
                if ( node.left == null ) {
                    node.left = new Node ( newData , null , null );
                } else {
                    this.insert ( node.left , newData );
                }
            } else if ( compareValue > 0 ) { ////Recursive right subtree, continue to find the insertion position
                if ( node.right == null ) {
                    node.right = new Node ( newData , null , null );
                } else {
                    this.insert ( node.right , newData );
                }
            }
        }

    }

    class Node {

        constructor ( data , left , right ){
            this.data = data ;
            this.left = left ;
            this.right = right ;
        }

        getData (){
            return this.data ;
        }

        setData ( data ){
            this.data = data ;
        }

    }

    //////////////////////testing////////////////////

    var binaryTree = new BinaryTree ();

    //Constructing a binary search tree
    binaryTree.insert ( binaryTree.getRoot (), 60 );
    binaryTree.insert ( binaryTree.getRoot (), 40 );
    binaryTree.insert ( binaryTree.getRoot (), 20 );
    binaryTree.insert ( binaryTree.getRoot (), 10 );
    binaryTree.insert ( binaryTree.getRoot (), 30 );
    binaryTree.insert ( binaryTree.getRoot (), 50 );
    binaryTree.insert ( binaryTree.getRoot (), 80 );
    binaryTree.insert ( binaryTree.getRoot (), 70 );
    binaryTree.insert ( binaryTree.getRoot (), 90 );

    document.write ( "<br>delete node is:  10 <br>" );
    binaryTree.remove ( binaryTree.getRoot (), 10 );
    document.write ( "<br>In-order traversal binary tree <br>" );
    binaryTree.inOrder ( binaryTree.getRoot ());
    document.write ( "<br>--------------------------------------------<br>" );
    document.write ( "<br>delete node is:  20<br>" );
    binaryTree.remove ( binaryTree.getRoot (), 20 );
    document.write ( "<br>In-order traversal binary tree<br>" );
    binaryTree.inOrder ( binaryTree.getRoot ());
    document.write ( "<br>--------------------------------------------<br>" );
    document.write ( "<br>delete node is:  40<br>" );
    binaryTree.remove ( binaryTree.getRoot (), 40 );
    document.write ( "<br>In-order traversal binary tree<br>" );
    binaryTree.inOrder ( binaryTree.getRoot ());

</script>
```

结果：

![](img/Image00127.jpg)

## 二叉堆排序

二叉树中非终端节点的值不大于其左右子节点的值。

小顶堆：`ki <= k2i` 且 `ki <= k2i+1`

大顶堆：`ki >= k2i` 且 `ki >= k2i+1`

父节点下标 = `(i-1)/2`

左子节点下标 = `2*i+1`

右子节点下标 = `2*i+2`

## 堆排序过程

1. 构建堆
2. 输出堆顶元素后，从上到下调整，将堆顶元素与其左右子树的根节点比较，将最小的元素交换到堆顶；然后不断调整直到叶子节点，得到新堆。

`{10, 90, 20, 80, 30, 70, 40, 60, 50}` 构建堆，然后进行堆排序输出。

### 初始化堆并构建堆

![](img/Image00128.jpg)

![](img/Image00129.jpg)

![](img/Image00130.jpg)

![](img/Image00131.jpg)

![](img/Image00132.jpg)

![](img/Image00133.jpg)

![](img/Image00134.jpg)

![](img/Image00135.jpg)

### 堆构建完成

### 开始堆排序

![](img/Image00136.jpg)

![](img/Image00137.jpg)

![](img/Image00138.jpg)

![](img/Image00139.jpg)

![](img/Image00140.jpg)

![](img/Image00141.jpg)

![](img/Image00142.jpg)

![](img/Image00143.jpg)

![](img/Image00144.jpg)

![](img/Image00145.jpg)

![](img/Image00146.jpg)

![](img/Image00147.jpg)

![](img/Image00148.jpg)

![](img/Image00149.jpg)

### 堆排序结果

![](img/Image00150.jpg)

使用记事本创建 `TestBinaryHeapSorting.html`

```javascript
<script type = "text/javascript" >

    class HeapSort {

        constructor (){

            this.array = [];

        }

        //Initialize the heap

        createHeap ( array ) {

            this.array = array ;

            // Build a heap, (array.length - 1) / 2 scan half of the nodes with child nodes

            for ( var i = ( array.length - 1 ) / 2 ; i >= 0 ; i --) {

                this.adjustHeap ( i , array.length - 1 );

            }

        }

        //Adjustment heap

        adjustHeap ( currentIndex , maxLength ) {

            var noLeafValue = this.array [ currentIndex ]; // Current non-leaf node

            //2 * currentIndex + 1  Current left subtree subscript

            for ( var j = 2 * currentIndex + 1 ; j <= maxLength ; j = currentIndex * 2 + 1 ) {

                if ( j < maxLength && this.array [ j ] < this.array [ j + 1 ]) {

                    j ++; // j Large subscript

                }

                if ( noLeafValue >= this.array [ j ]) {

                    break ;

                }

                this.array [ currentIndex ] = this.array [ j ]; // Move up to the parent node

                currentIndex = j ;

            }

            this.array [ currentIndex ] = noLeafValue ; // To put in the position

        }

        heapSort () {

            for ( var i = this.array.length - 1 ; i > 0 ; i --) {

                var temp = this.array [ 0 ];

                this.array [ 0 ] = this.array [ i ];

                this.array [ i ] = temp ;

                this.adjustHeap ( 0 , i - 1 );

            }

        }

    }

    //////////////////////testing////////////////////

    var heapSort = new HeapSort ();

    var scores = [ 10 , 90 , 20 , 80 , 30 , 70 , 40 , 60 , 50 ];

    document.write ( "Before building a heap : <br>" );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + ", " );

    }

    document.write ( "<br><br>" );

    ////////////////////////////////////////////////////////////

    document.write ( "After building a heap : <br>" );

    heapSort.createHeap ( scores );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + ", " );

    }

    document.write ( "<br><br>" );

    ////////////////////////////////////////////////////////////

    document.write ( "After heap sorting : <br>" );

    heapSort.heapSort ();

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + ", " );

    }

</script>
```

结果：

![](img/Image00151.jpg)

## 哈希表

通过映射键 => 值来访问表中的数据。



1. 将 `{19, 18, 35,40,41,42}` 映射到`HashTable`，映射规则为`key % 4`

![](img/Image00152.jpg)

![](img/Image00153.jpg)

2. 实现一个`Hashtable`

![](img/Image00154.jpg)

使用记事本创建`TestHashtable.html`：

```javascript
<script type = "text/javascript" >

    class Node {

        constructor ( key , value , hash , next ){

            this.key = key ;

            this.value = value ;

            this.hash = hash ;

            this.next = next ;

        }

        getKey () {

            return this.key ;

        }

        setKey ( key ) {

            this.key = key ;

        }

        getValue () {

            return this.value ;

        }

        setValue ( value ) {

            this.value = value ;

        }

        getHash () {

            return this.hash ;

        }

        setHash ( hash ) {

            this.hash = hash ;

        }

    }

    class Hashtable {

        constructor (){

            this.capacity = 16 ;

            this.table = new Array ( this.capacity );

            this.size = 0 ;

        }

        size () {

            return this.size ;

        }

        isEmpty () {

            return this.size == 0 ? true : false ;

        }

        hash ( key ) {

            var hash = 0 ;

            for ( var i = 0 ; i < key.length ; i ++) {

                hash += key.charCodeAt ( i );

            }

            return hash % 37 ;

        }

        //Calculate the hash value according to the key hash algorithm

        hashCode ( key ) {

            var avg = this.hash ( key ) * ( Math.pow ( 5 , 0.5 ) - 1 ) / 2 //hash policy for middle-square method

            var numeric = avg - Math.floor ( avg )

            return parseInt ( Math.floor ( numeric * this.table.length ))

        }

        put ( key , value ) {

            if ( key == null ) {

                throw new IllegalArgumentException ();

            }

            var hash = this.hashCode ( key );

            var newNode = new Node ( key , value , hash , null );

            var node = table [ hash ];

            while ( node != null ) {

                if ( node.getKey (). equals ( key )) {

                    node.setValue ( value );

                    return ;

                }

                node = node.next ;

            }

            newNode.next = this.table [ hash ];

            this.table [ hash ] = newNode ;

            this.size ++;

        }

        get ( key ) {

            if ( key == null ) {

                return null ;

            }

            var hash = this.hashCode ( key );

            var node = this.table [ hash ];

            while ( node != null ) { //Get value according to key

                if ( node.getKey () == key ) {

                    return node.getValue ();

                }

                node = node.next ;

            }

            return null ;

        }

    }

    //////////////////////testing////////////////////

    var table = new Hashtable ();

    table.put ( "david" , "Good Boy Keep Going" );

    table.put ( "grace" , "Cute Girl Keep Going" );

    document.write ( "david => " + table.get ( "david" ) + "<br>" );

    document.write ( "grace => " + table.get ( "grace" ) + "<br>" );

</script>
```

结果：

![](img/Image00155.jpg)

## 无向图与深度优先搜索

### 无向图

数据结构通过邻接矩阵（即二维数组）和邻接表来表示。每个节点称为顶点，两个相邻节点称为边。

无向图无方向：`A -> B = B -> A`

![](img/Image00156.jpg)

1. 邻接矩阵如上所述：顶点总数是二维数组的大小，如果有边则值为`1`，否则无边值为`0`。

![](img/Image00157.jpg)

2. 深度优先搜索：从`A`开始寻找相邻边节点`B`，然后从`B`寻找相邻节点`C`，依此类推，直到找到所有节点`A -> B -> C -> D -> E`。

![](img/Image00158.jpg)

![](img/Image00159.jpg)

![](img/Image00160.jpg)

使用记事本创建`TestUndirectedGraphDepthFrstSearch.html`：

```javascript
<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {
```



```javascript
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

constructor() {

    this.stacks = new Array();

    this.top = -1;

}

push(element) {

    this.top++;

    this.stacks[this.top] = element;

}

pop() {

    if (this.top == -1) {

        return -1;

    }

    var data = this.stacks[this.top];

    this.top--;

    return data;

}

peek() {

    if (this.top == -1) {

        return -1;

    }

    var data = this.stacks[this.top];

    return data;

}

isEmpty() {

    if (this.top <= -1) {

        return true;

    }

    return false;

}

}

class Graph {

constructor(maxVertexSize) {

    this.maxVertexSize = maxVertexSize; // Two-dimensional array size

    this.vertexs = new Array(maxVertexSize);

    this.size = 0; // Current vertex size

    this.adjacencyMatrix = new Array(maxVertexSize);

    for (var i = 0; i < maxVertexSize; i++) {

        this.adjacencyMatrix[i] = new Array();

        for (var j = 0; j < maxVertexSize; j++) {

            this.adjacencyMatrix[i][j] = 0;

        }

    }

    this.stack = new Stack(); // Stack saves current vertices

}

addVertex(data) {

    var vertex = new Vertex(data, false);

    this.vertexs[this.size] = vertex;

    this.size++;

}

// Add adjacent edges

addEdge(from, to) {

    // A -> B = B -> A

    this.adjacencyMatrix[from][to] = 1;

    this.adjacencyMatrix[to][from] = 1;

}

depthFirstSearch() {

    // Start searching from the first vertex

    var firstVertex = this.vertexs[0];

    firstVertex.setVisited(true);

    document.write(firstVertex.getData());

    this.stack.push(0);

    while (!this.stack.isEmpty()) {

        var row = this.stack.peek();

        // Get adjacent vertex positions that have not been visited

        var col = this.findAdjacencyUnVisitedVertex(row);

        if (col == -1) {

            this.stack.pop();

        } else {

            this.vertexs[col].setVisited(true);

            document.write(" -> " + this.vertexs[col].getData());

            this.stack.push(col);

        }

    }

    this.clear();

}

// Get adjacent vertex positions that have not been visited

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

//////////////////////testing////////////////////

function printGraph(graph) {

document.write("Two-dimensional array traversal output vertex edge and adjacent array: <br>");

for (var i = 0; i < graph.getVertexs().length; i++) {

    document.write(graph.getVertexs()[i].getData() + "  ");

}

document.write("<br>");

for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {

    document.write(graph.getVertexs()[i].getData() + "  ");

    for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {

        document.write(graph.getAdjacencyMatrix()[i][j] + "  ");

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

// Two-dimensional array traversal output vertex edge and adjacent array

printGraph(graph);

document.write("<br>Depth-first search traversal output: <br>");

graph.depthFirstSearch();

</script>
```

结果：

![](img/Image00161.jpg)

# 无向图与广度优先搜索

## 广度优先搜索

从 A 出发找到所有相邻边节点 B、C、D，然后从 B 出发找到所有相邻节点 A、C、D，依此类推，直到找到所有节点 A -> B -> C -> D -> E。

![](img/Image00162.jpg)

![](img/Image00163.jpg)

![](img/Image00164.jpg)

使用记事本创建一个 `TestUndirectedGraphBreadthFrstSearch.html` 文件。

```javascript
<script type="text/javascript">

class Vertex {

constructor(data, visited) {

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

constructor() {

    this.queues = new Array();

}

add(element) {

    this.queues[this.queues.length] = element;

}

remove() {

    if (this.queues.length <= 0) {

        return -1;

    }

    return this.queues.shift();

}

isEmpty() {

    if (this.queues.length <= 0) {

        return true;

    }

    return false;

}

}

class Graph {

constructor(maxVertexSize) {

    this.maxVertexSize = maxVertexSize; // Two-dimensional array size

    this.vertexs = new Array(maxVertexSize);

    this.size = 0; // Current vertex size

    this.adjacencyMatrix = new Array(maxVertexSize);

    for (var i = 0; i < maxVertexSize; i++) {

        this.adjacencyMatrix[i] = new Array();

        for (var j = 0; j < maxVertexSize; j++) {

            this.adjacencyMatrix[i][j] = 0;

        }

    }

    this.queue = new Queue(); // Queue saves current vertices

}

addVertex(data) {

    var vertex = new Vertex(data, false);

    this.vertexs[this.size] = vertex;

    this.size++;

}

// Add adjacent edges

addEdge(from, to) {

    // A -> B = B -> A

    this.adjacencyMatrix[from][to] = 1;

    this.adjacencyMatrix[to][from] = 1;

}

breadthFirstSearch() {

    // Start searching from the first vertex

    var firstVertex = this.vertexs[0];

    firstVertex.setVisited(true);

    document.write(firstVertex.getData());

    this.queue.add(0);

    var col = 0;

    while (!this.queue.isEmpty()) {
```



```javascript
var head = this.queue.remove ();
// Get adjacent vertex positions that have not been visited
col = this.findAdjacencyUnVisitedVertex(head);
// Loop through all vertices connected to the current vertex
while (col != -1) {
    this.vertexs[col].setVisited(true);
    document.write(" -> " + this.vertexs[col].getData());
    this.queue.add(col);
    col = this.findAdjacencyUnVisitedVertex(head);
}
}
this.clear();
}
// Get adjacent vertex positions that have not been visited
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
//////////////////////testing////////////////////
function printGraph(graph) {
    document.write("Two-dimensional array traversal output vertex edge and adjacent array :  <br>");
    document.write("&nbsp;&nbsp;&nbsp;");
    for (var i = 0; i < graph.getVertexs().length; i++) {
        document.write(graph.getVertexs()[i].getData() + "&nbsp;&nbsp;&nbsp;&nbsp;");
    }
    document.write("<br>");
    for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
        document.write(graph.getVertexs()[i].getData() + "  ");
        for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {
            document.write(graph.getAdjacencyMatrix()[i][j] + "&nbsp;&nbsp;&nbsp;&nbsp;");
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
// Two-dimensional array traversal output vertex edge and adjacent array
printGraph(graph);
document.write("\nBreadth-First Search traversal output : <br>");
graph.breadthFirstSearch();
</script>
```

结果：

![](img/Image00165.jpg)

## 有向图与深度优先搜索

### 有向图

数据结构通过邻接矩阵（即二维数组）和邻接表来表示。每个节点称为顶点，两个相邻节点称为边。

有向图具有方向性：`A -> B` 和 `B -> A` 是不同的。

![](img/Image00166.jpg)

### 1. 邻接矩阵如上所述

顶点总数是二维数组的大小，如果有边则值为 `1`，否则无边值为 `0`。

![](img/Image00167.jpg)

### 2. 深度优先搜索

从 `A` 开始寻找相邻的边节点 `B`，然后从 `B` 寻找相邻节点 `C`，依此类推，直到找到所有节点 `A -> B -> C -> D -> E`。

![](img/Image00168.jpg)

![](img/Image00169.jpg)

![](img/Image00170.jpg)

用记事本创建一个 `TestDirectedGraphDepthFrstSearch.html` 文件。

```html
<script type="text/javascript">
    class Vertex {
        constructor(data, visited) {
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

    class Stack {
        constructor() {
            this.stacks = new Array();
            this.top = -1;
        }

        push(element) {
            this.top++;
            this.stacks[this.top] = element;
        }

        pop() {
            if (this.top == -1) {
                return -1;
            }

            var data = this.stacks[this.top];
            this.top--;
            return data;
        }

        peek() {
            if (this.top == -1) {
                return -1;
            }

            var data = this.stacks[this.top];
            return data;
        }

        isEmpty() {
            if (this.top <= -1) {
                return true;
            }

            return false;
        }
    }

    class Graph {
        constructor(maxVertexSize) {
            this.maxVertexSize = maxVertexSize; // Two-dimensional array size
            this.vertexs = new Array(maxVertexSize);
            this.size = 0; // Current vertex size
            this.adjacencyMatrix = new Array(maxVertexSize);

            for (var i = 0; i < maxVertexSize; i++) {
                this.adjacencyMatrix[i] = new Array();

                for (var j = 0; j < maxVertexSize; j++) {
                    this.adjacencyMatrix[i][j] = 0;
                }
            }

            this.stack = new Stack(); // Stack saves current vertices
        }

        addVertex(data) {
            var vertex = new Vertex(data, false);
            this.vertexs[this.size++] = vertex;
        }

        addEdge(from, to) {
            this.adjacencyMatrix[from][to] = 1; // A -> B and B -> A are different
        }

        depthFirstSearch() {
            var firstVertex = this.vertexs[0]; // Start searching from the first vertex

            firstVertex.setVisited(true);
            document.write(firstVertex.getData());
            this.stack.push(0);

            while (!this.stack.isEmpty()) {
                var row = this.stack.peek();

                // Get adjacent vertex positions that have not been visited
                var col = this.findAdjacencyUnVisitedVertex(row);

                if (col == -1) {
                    this.stack.pop();
                } else {
                    this.vertexs[col].setVisited(true);
                    document.write(" -> " + this.vertexs[col].getData());
                    this.stack.push(col);
                }
            }

            this.clear();
        }

        // Get adjacent vertex positions that have not been visited
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

    //////////////////////testing///////////////////
    function printGraph(graph) {
        document.write("Two-dimensional array traversal output vertex edge and adjacent array :  <br>");
        document.write("&nbsp;&nbsp;&nbsp;");

        for (var i = 0; i < graph.getVertexs().length; i++) {
            document.write(graph.getVertexs()[i].getData() + "&nbsp;&nbsp;&nbsp;&nbsp;");
        }

        document.write("<br>");

        for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
            document.write(graph.getVertexs()[i].getData() + "  ");

            for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {
                document.write(graph.getAdjacencyMatrix()[i][j] + "&nbsp;&nbsp;&nbsp;&nbsp;");
            }

            document.write("<br>");
```



```javascript
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

// Two-dimensional array traversal output vertex edge and adjacent array
printGraph(graph);

document.write("<br>Depth-first search traversal output : <br>");

graph.depthFirstSearch();

</script>
```

结果：

![](img/Image00171.jpg)

## 有向图与广度优先搜索

### 广度优先搜索

从 A 出发找到所有相邻边节点 B、C、D，然后从 B 出发找到所有相邻节点 A、C、D，依此类推，直到找到所有节点 A -> B -> C -> D -> E。

![](img/Image00172.jpg)

![](img/Image00173.jpg)

![](img/Image00174.jpg)

用记事本创建一个 `TestDirectedGraphBreadthFrstSearch.html` 文件。

```javascript
<script type="text/javascript">

class Vertex {
    constructor(data, visited) {
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
    constructor() {
        this.queues = new Array();
    }

    add(element) {
        this.queues[this.queues.length] = element;
    }

    remove() {
        if (this.queues.length <= 0) {
            return -1;
        }

        return this.queues.shift();
    }

    isEmpty() {
        if (this.queues.length <= 0) {
            return true;
        }

        return false;
    }
}

class Graph {
    constructor(maxVertexSize) {
        this.maxVertexSize = maxVertexSize; // Two-dimensional array size
        this.vertexs = new Array(maxVertexSize);
        this.size = 0; // Current vertex size
        this.adjacencyMatrix = new Array(maxVertexSize);

        for (var i = 0; i < maxVertexSize; i++) {
            this.adjacencyMatrix[i] = new Array();

            for (var j = 0; j < maxVertexSize; j++) {
                this.adjacencyMatrix[i][j] = 0;
            }
        }

        this.queue = new Queue(); // Queue saves current vertices
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

    breadthFirstSearch() {
        // Start searching from the first vertex
        var firstVertex = this.vertexs[0];

        firstVertex.setVisited(true);
        document.write(firstVertex.getData());

        this.queue.add(0);

        var col = 0;

        while (!this.queue.isEmpty()) {
            var head = this.queue.remove();

            // Get adjacent vertex positions that have not been visited
            col = this.findAdjacencyUnVisitedVertex(head);

            // Loop through all vertices connected to the current vertex
            while (col != -1) {
                this.vertexs[col].setVisited(true);
                document.write(" -> " + this.vertexs[col].getData());
                this.queue.add(col);
                col = this.findAdjacencyUnVisitedVertex(head);
            }
        }

        this.clear();
    }

    // Get adjacent vertex positions that have not been visited
    findAdjacencyUnVisitedVertex(row) {
        for (var col = 0; col < this.size; col++) {
            if (
                this.adjacencyMatrix[row][col] == 1 &&
                !this.vertexs[col].isVisited()
            ) {
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

//////////////////////testing////////////////////

function printGraph(graph) {
    document.write(
        "Two-dimensional array traversal output vertex edge and adjacent array : <br>"
    );

    document.write("&nbsp;&nbsp;&nbsp;");

    for (var i = 0; i < graph.getVertexs().length; i++) {
        document.write(
            graph.getVertexs()[i].getData() + "&nbsp;&nbsp;&nbsp;&nbsp;"
        );
    }

    document.write("<br>");

    for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
        document.write(graph.getVertexs()[i].getData() + "  ");

        for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {
            document.write(
                graph.getAdjacencyMatrix()[i][j] + "&nbsp;&nbsp;&nbsp;&nbsp;"
            );
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

// Two-dimensional array traversal output vertex edge and adjacent array
printGraph(graph);

document.write("\nBreadth-First Search traversal output : <br>");

graph.breadthFirstSearch();

</script>
```

结果：

![](img/Image00175.jpg)

## 有向图拓扑排序

### 有向图拓扑排序

按照方向顺序对有向图中的顶点进行排序。

有向图具有方向性：A -> B 和 B -> A 是不同的。

![](img/Image00166.jpg)

1. 邻接矩阵如上所述：

   顶点总数是二维数组的大小，如果有边则值为 1，否则无边值为 0。

   ![](img/Image00167.jpg)

从顶点 A 开始的拓扑排序：A -> B -> C -> D -> E。

![](img/Image00176.jpg)

![](img/Image00177.jpg)

![](img/Image00178.jpg)

用记事本创建一个 `TestTopologicalSorting.html` 文件。

```javascript
<script type="text/javascript">

class Vertex {
    constructor(data, visited) {
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
```

```javascript
constructor(maxVertexSize) {
    this.maxVertexSize = maxVertexSize; // Two-dimensional array size
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
        var noSuccessorVertex = this.getNoSuccessorVertex(); // Get a no successor node
```



```javascript
if (noSuccessorVertex == -1) {
    document.write("There is ring in Graph");

    return;
}

// Copy the deleted node to the sorted array
this.topologys[this.size - 1] = this.vertexs[noSuccessorVertex];

this.removeVertex(noSuccessorVertex); // Delete no successor node
}
}

getNoSuccessorVertex() {
    var existSuccessor = false;

    for (var row = 0; row < this.size; row++) { // For each vertex
        existSuccessor = false;

        // If the node has a fixed row, each column has a 1, indicating that the node has a successor, terminating the loop
        for (var col = 0; col < this.size; col++) {
            if (this.adjacencyMatrix[row][col] == 1) {
                existSuccessor = true;
                break;
            }
        }

        if (!existSuccessor) { // If the node has no successor, return its subscript
            return row;
        }
    }

    return -1;
}

removeVertex(vertex) {
    if (vertex != this.size - 1) { // If the vertex is the last element, the end
        for (var i = vertex; i < this.size - 1; i++) { // The vertices are removed from the vertex array
            this.vertexs[i] = this.vertexs[i + 1];
        }

        for (var row = vertex; row < this.size - 1; row++) { // Move up a row
            for (var col = 0; col < this.size - 1; col++) {
                this.adjacencyMatrix[row][col] = this.adjacencyMatrix[row + 1][col];
            }
        }

        for (var col = vertex; col < this.size - 1; col++) { // Move left a row
            for (var row = 0; row < this.size - 1; row++) {
                this.adjacencyMatrix[row][col] = this.adjacencyMatrix[row][col + 1];
            }
        }
    }

    this.size--; // Decrease the number of vertices
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

getTopologys() {
    return this.topologys;
}
}

//////////////////////testing////////////////////

function printGraph(graph) {
    document.write("Two-dimensional array traversal output vertex edge and adjacent array :  <br>");
    document.write("&nbsp;&nbsp;&nbsp;");

    for (var i = 0; i < graph.getVertexs().length; i++) {
        document.write(graph.getVertexs()[i].getData() + "&nbsp;&nbsp;&nbsp;&nbsp;");
    }

    document.write("<br>");

    for (var i = 0; i < graph.getAdjacencyMatrix().length; i++) {
        document.write(graph.getVertexs()[i].getData() + "  ");

        for (var j = 0; j < graph.getAdjacencyMatrix().length; j++) {
            document.write(graph.getAdjacencyMatrix()[i][j] + "&nbsp;&nbsp;&nbsp;&nbsp;");
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

// Two-dimensional array traversal output vertex edge and adjacent array
printGraph(graph);

document.write("<br>Depth-First Search traversal output : <br>");
document.write("Directed Graph Topological Sorting:<br>");

graph.topologySort();

for (var i = 0; i < graph.getTopologys().length; i++) {
    document.write(graph.getTopologys()[i].getData() + " -> ");
}
```

结果：

![](img/Image00179.jpg)
