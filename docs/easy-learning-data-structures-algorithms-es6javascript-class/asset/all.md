![](Image00180.jpg)

# 读累了记得休息一会哦~

**公众号：古德猫宁李**

*   电子书搜索下载
*   书单分享
*   书友学习交流

**网站：**[沉金书屋 https://www.chenjin5.com](https://www.chenjin5.com)

*   电子书搜索下载
*   电子书打包资源分享
*   学习资源分享

Easy Learning Data Structures Algorithms ES6+ Javascript

![](Image00000.jpg)

YANG HU

The complexity of life, because they do not understand to simplify the complex, to simplify the complexity, simple is the beginning of wisdom.

    From the essence of practice, to briefly explain the concept, and vividly cultivate programming interest, this book deeply analyzes Data Structures Algorithms ES6+ Javascript, combined with the use of scene interpretation in practice, to experience the fun of programming.

[http://en.verejava.com](http://en.verejava.com)

Copyright © 2019 Yang Hu

All rights reserved.

ISBN : 9781070723884

CONTENTS

1. [Bubble Sorting Algorithm](#text00000.html_Bubble_Sorting_Algorithm)

2. [Select Sorting Algorithm](#text00000.html_Select_Sorting_Algorithm)

3. [Insert Sorting Algorithm](#text00000.html_Insert_Sorting_Algorithm)

4. [Dichotomy Binary Search](#text00000.html_Dichotomy_Binary_Search)

5. [Unidirectional Linked List](#text00000.html_Unidirectional_Linked_List)

5.1 [Create and Initialization](#text00000.html_Unidirectional_Linked_List_initialize)

5.2 [Add Node](#text00000.html_Unidirectional_Linked_List_Add)

5.3 [Insert Node](#text00000.html_Unidirectional_Linked_List_Insert)

5.4 [Delete Node](#text00000.html_Unidirectional_Linked_List_Delete)

6. [Doubly Linked List](#text00000.html_Doubly_Linked_List)

6.1 [Create and Initialization](#text00000.html_Doubly_Linked_List_initialize)

6.2 [Add Node](#text00000.html_Doubly_Linked_List_Add)

6.3 [Insert Node](#text00000.html_Doubly_Linked_List_Insert)

6.4 [Delete Node](#text00000.html_Doubly_Linked_List_Delete)

7. [ One-way Circular LinkedList](#text00000.html_Oneway_Circular_LinkedList)

7.1 [Initialization and Traversal](#text00000.html_Oneway_Circular_LinkedList_initialize)

7.2 [Insert Node](#text00000.html_Oneway_Circular_LinkedList_Insert)

7.3 [Delete Node](#text00000.html_Oneway_Circular_LinkedList_Delete)

8. [Two-way Circular LinkedList](#text00000.html_Twoway_Circular_LinkedList)

8.1 [Initialization and Traversal](#text00000.html_Twoway_Circular_LinkedList_initialize)

8.2 [Insert Node](#text00000.html_Twoway_Circular_LinkedList_Insert)

8.3 [Delete Node](#text00000.html_Twoway_Circular_LinkedList_Delete)

9. [Queue](#text00000.html_Queue)

10. [Stack](#text00000.html_Stack)

11. [Recursive Algorithm](#text00000.html_Recursive_Algorithm)

12. [Two-way Merge Algorithm](#text00000.html_Twoway_Merge_Algorithm)

13. [Quick Sort Algorithm](#text00000.html_Quick_Sort_Algorithm)

14. [Binary Search Tree](#text00000.html_Binary_Search_Tree)

    14.1 [Construct a binary search tree](#text00000.html_Binary_Search_Tree)

    14.2 [Binary search tree In-order traversal](#text00000.html_Inorder_traversal)

    14.3 [Binary search tree Pre-order traversal](#text00000.html_Preorder_traversal)

    14.4 [Binary search tree Post-order traversal](#text00000.html_Postorder_traversal)

    14.5 [ Binary search tree Maximum and minimum](#text00000.html_Maximum_and_minimum)

    14.6 [Binary search tree Delete Node](#text00000.html_binary_search_tree_Delete_Node)

15. [Binary Heap Sorting](#text00000.html_Binary_Heap_Sorting)

16. [Hash Table](#text00000.html_Hash_Table)

17. [Graph](#text00000.html_Undirected_Graph_and_DepthFrst_Search)

    17.1 [Undirected Graph and Depth-Frst Search](#text00000.html_Undirected_Graph_and_DepthFrst_Search)

    17.2 [Undirected Graph and Breadth-First Search](#text00000.html_Undirected_Graph_BreadthFirst_Search)

    17.3 [Directed Graph and Depth-Frst Search](#text00000.html_Directed_Graph_and_DepthFrst_Search)

    17.4 [Directed Graph and Breadth-First Search](#text00000.html_Directed_Graph_and_BreadthFirst_Search)

    17.5 [Directed Graph Topological Sorting](#text00000.html_Directed_Graph_Topological_Sorting)

Bubble Sorting Algorithm

Bubble Sorting Algorithm:

the first two elements are compared, if the previous element is larger than the latter element, the position is swapped. Repeat this process, until sorting is completed.

Sort the following numbers from small to large

![](Image00001.jpg)

Explanation:

![](Image00002.jpg) no sorting, ![](Image00003.jpg) Comparing, ![](Image00004.jpg) Already ordered

1 . First sorting:

![](Image00005.jpg)

2 . Second sorting:

![](Image00006.jpg)

3 . Third sorting:

![](Image00007.jpg)

4, 5 And so on like above : we can get the final sorting numbers from small to large

![](Image00008.jpg)

1\. Create a TestBubbleSort.html with Notepad and open it in your browser.

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

Result:

![](Image00009.jpg)

Select Sorting Algorithm

Select Sorting Algorithm:

Select the smallest one of the remaining unordered elements in the array, inserting the one that has been sorted before.

Sort the following numbers from small to large

![](Image00010.jpg)

Explanation:

![](Image00002.jpg) no sorting, ![](Image00003.jpg) Comparing, ![](Image00004.jpg) Already ordered

1 . First sorting:

![](Image00011.jpg)

![](Image00012.jpg)

2 . Second sorting:

![](Image00013.jpg)

![](Image00014.jpg)
3 . Third sorting:

![](Image00015.jpg)

![](Image00016.jpg)

4 . Forth sorting:

![](Image00017.jpg)

5 . Fifth sorting:

![](Image00018.jpg)

1\. Create a TestSelectSort.html with Notepad and open it in your browser.

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

Result:

![](Image00019.jpg)

Insert Sorting Algorithm

Insert Sorting Algorithm:

Take an unsorted new element in the array, compare it with the already sorted element before, insert a new element to the right if the new element is smaller than the sorted element.

Sort the following numbers from small to large

![](Image00010.jpg)

Explanation:

![](Image00002.jpg) no sorting elements, ![](Image00003.jpg) inserting elements, ![](Image00004.jpg) Already ordered elements

1 . First sorting:

![](Image00020.jpg)

2 . Second sorting:

![](Image00021.jpg)

3 . Third sorting:

![](Image00022.jpg)

4 Third sorting:

![](Image00023.jpg)

5 Fifth sorting:

![](Image00024.jpg)

1\. Create a TestInsertSort.html with Notepad and open it in your browser.

<script type = "text/javascript" >

    class InsertSort {

        static sort ( arrays ) {

            for ( var i = 0 ; i < arrays.length ; i ++) {

                var insertElement = arrays [ i ]; //Take unsorted new elements

                var insertPosition = i ; //Inserted position

                for ( var j = insertPosition - 1 ; j >= 0 ; j --) {

                    //If the new element is smaller than the sorted element, shifted to the right

                    if ( insertElement < arrays [ j ]) {

                        arrays [ j + 1 ] = arrays [ j ];

                        insertPosition --;

                    }

                }

                arrays [ insertPosition ] = insertElement ; //Insert the new element

            }

        }

    }

    //////////////////////testing////////////////////

    var scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];

    InsertSort.sort ( scores );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + "," );

    }

</script>

Result:

![](Image00025.jpg)

Dichotomy Binary Search

Dichotomy Binary Search:

Find the index position of a given value from an already ordered array.

    1\. Initialize the lowest index low=0 , the highest index high=scores.length-1

    2\. Find the searchValue of the middle index mid=(low+high)/2 scores[mid]

    3\. Compare the median scores[mid] with searchValue

       If the scores[mid]==searchValue print current mid index,

        If scores[mid]>searchValue indicates that the searchValue will be found is between low and mid-1

    4\. And so on. Repeat step 3 until you find searchValue or find low>=high to terminate the loop.

Example 1 : Find the index of searchValue=40 in the array that has been sorted below.

![](Image00026.jpg)

![](Image00027.jpg)

Example 2 : Find the index of searchValue=90 in the array that has been sorted below.

![](Image00028.jpg) ![](Image00029.jpg)

1\. Create a TestBinarySearch.html with Notepad and open it in your browser.

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

    //////////////////////testing////////////////////

    var scores = [ 30 , 40 , 50 , 70 , 85 , 90 , 100 ];

    var searchValue = 40 ;

    var position = BinarySearch.search ( scores , searchValue );

    document.write ( searchValue + " position:" + position );

    document.write ( "<br>-----------------------------<br>" );

    searchValue = 90 ;

    position = BinarySearch.search ( scores , searchValue );

    document.write ( searchValue + " position:" + position );

</script>

Result:

![](Image00030.jpg)

Unidirectional Linked List

Unidirectional Linked List:

Is a chained storage structure of a linear table, which is connected by a node. Each node consists of data and next pointer to the next node.

![](Image00031.jpg)

UML Diagram

![](Image00032.jpg)

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

1. Unidirectional Linked List initialization .

Example : Construct a San Francisco subway Unidirectional linked list

![](Image00033.jpg)

2. traversal output .

![](Image00034.jpg)

1\. Create a TestUnidirectionalLinkedList.html with Notepad and open it in your browser.

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

    class LinkedList {

        init () {

            // the first node called head node

            this.head = new Node ( "San Francisco" , null );

            var nodeOakland = new Node ( "Oakland" , null );

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" , null );

            nodeOakland.next = nodeBerkeley ;

            // the last node called tail node

            this.tail = new Node ( "Fremont" , null );

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        print ( node ) {

            var p = node ;

            while ( p != null ) // From the beginning to the end

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            }

            document.write ( "End<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var linkedList = new LinkedList ();

    var head = linkedList.init ();

    linkedList.print ( head );

</script>

Result:

![](Image00035.jpg)

3. Append a new node name: Walnut   to the end.

![](Image00036.jpg)

1\. Create a TestUnidirectionalLinkedListAppend.html with Notepad

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

    class LinkedList {

        init () {

            // the first node called head node

            this.head = new Node ( "San Francisco" , null );

            var nodeOakland = new Node ( "Oakland" , null );

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" , null );

            nodeOakland.next = nodeBerkeley ;

            // the last node called tail node

            this.tail = new Node ( "Fremont" , null );

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        add ( newNode ) {

            this.tail.next = newNode ;

            this.tail = newNode ;

        }

        print ( node ) {

            var p = node ;

            while ( p != null ) // From the beginning to the end

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            }

            document.write ( "End<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var linkedList = new LinkedList ();

    var head = linkedList.init ();

    document.write ( "Append a new node name: Walnut  to the end: <br>" );

    linkedList.add ( new Node ( "Walnut" , null ));

    linkedList.print ( head );

</script>

Result:

![](Image00037.jpg)

3. Insert a node Walnut in position 2.

![](Image00038.jpg)

1\. Create a TestUnidirectionalLinkedListInsert.html with Notepad

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

    class LinkedList {

        init () {

            // the first node called head node

            this.head = new Node ( "San Francisco" , null );

            var nodeOakland = new Node ( "Oakland" , null );

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" , null );

            nodeOakland.next = nodeBerkeley ;

            // the last node called tail node

            this.tail = new Node ( "Fremont" , null );

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

            newNode.next = p.next ; // newNode next point to next node

            p.next = newNode ; // current next point to newNode

        }

        print ( node ) {

            var p = node ;

            while ( p != null ) // From the beginning to the end

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            }

            document.write ( "End<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var linkedList = new LinkedList ();

    var head = linkedList.init ();

    document.write ( "Insert a new node Walnut at index = 2 : <br>" );

    linkedList.insert ( 2 , new Node ( "Walnut" , null ));

    linkedList.print ( head );

</script>

Result:

![](Image00039.jpg)

4. Delete the index=2 node.

![](Image00040.jpg)

1\. Create a TestUnidirectionalLinkedListDelete.html with Notepad

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

    class LinkedList {

        init () {

            // the first node called head node

            this.head = new Node ( "San Francisco" , null );

            var nodeOakland = new Node ( "Oakland" , null );

            this.head.next = nodeOakland ;

            var nodeBerkeley = new Node ( "Berkeley" , null );

            nodeOakland.next = nodeBerkeley ;

            // the last node called tail node

            this.tail = new Node ( "Fremont" , null );

            nodeBerkeley.next = this.tail ;

            return this.head ;

        }

        remove ( removePosition ) {

            var p = this.head ;

            var i = 0 ;

            // Move the node to the previous node position that was deleted

            while ( p.next != null && i < removePosition - 1 ) {

                p = p.next ;

                i ++;

            }

            var temp = p.next ; // Save the node you want to delete

            p.next = p.next.next ; // Previous node next points to next of delete the node

            temp.next = null ;

        }

        print ( node ) {

            var p = node ;

            while ( p != null ) // From the beginning to the end

            {

                var data = p.getData ();

                document.write ( data + " -> " );

                p = p.next ;

            }

            document.write ( "End<br><br>" );

        }

    }

    //////////////////////testing////////////////////

    var linkedList = new LinkedList ();

    var head = linkedList.init ();

    document.write ( "Delete a new node Berkeley at index = 2 : <br>" );

    linkedList.remove ( 2 );

    linkedList.print ( head );

</script>

Result:

![](Image00041.jpg)

Doubly Linked List

Doubly Linked List:

It is a chained storage structure of a linear table. It is connected by nodes in two directions. Each node consists of data, pointing to the previous node and pointing to the next node.

![](Image00042.jpg)

UML Diagram

![](Image00043.jpg)

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

1. Doubly Linked List initialization .

Example : Construct a San Francisco subway Doubly linked list

![](Image00044.jpg)

2\. Create a TestDoubleLink.html with Notepad

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

Result:

![](Image00045.jpg)

3. add a node Walnut at the end of Fremont.

![](Image00046.jpg)

Create a TestDoubleLinkAdd.html with Notepad

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

Result:

![](Image00047.jpg)

3. Insert a node Walnut in position 2.

![](Image00048.jpg)

Create a TestDoubleLinkInsert.html with Notepad

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

Result:

![](Image00049.jpg)

4. Delete the index=2 node.

![](Image00050.jpg)

Create a TestDoubleLinkDelete.html with Notepad

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

            // Move the node to the previous node  that was deleted

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

Result:

![](Image00051.jpg)

One-way Circular LinkedList

One-way Circular List:

It is a chain storage structure of a linear table, which is connected by a node in a unidirectional manner, and is connected to form a ring, and each node is composed of data and a pointer next.

![](Image00052.jpg)

UML Diagram

![](Image00053.jpg)

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

1. One-way Circular Linked List initialization and traversal output .

![](Image00054.jpg)

Create a TestSingleCircleLink.html with Notepad

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

Result:

![](Image00055.jpg)

3. Insert a node E in position 2.

![](Image00056.jpg)

![](Image00057.jpg)

Create a TestSingleCircleLinkInsert.html with Notepad

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

    document.write ( "Insert a new node E at index = 2 : <br>" );

    singleCircleLink.insert ( 2 , new Node ( "E" ));

    singleCircleLink.print ( head );

</script>

Result:

![](Image00058.jpg)

4. Delete the index=2 node.

![](Image00059.jpg)

![](Image00060.jpg)

Create a TestSingleCircleLinkDelete.html with Notepad

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

    //////////////////////testing////////////////////

    var singleCircleLink = new SingleCircleLink ();

    singleCircleLink.init ();

    document.write ( "Delete a new node C at index = 2 : <br>" );

    singleCircleLink.remove ( 2 );

    singleCircleLink.print ();

</script>

Result:

![](Image00061.jpg)

Two-way Circular LinkedList

Two-way Circular List:

It is a chain storage structure of a linear table. The nodes are connected in series by two directions, and is connected to form a ring. Each node is composed of data , pointing to the previous node prev and pointing to the next node next .

![](Image00062.jpg)

UML Diagram

![](Image00063.jpg)

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

1. Two-way Circular Linked List initialization and traversal output .

![](Image00064.jpg)

![](Image00065.jpg)

Create a TestDoubleCircleLink.html with Notepad

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

    doubleCircleLink.print ();

</script>

Result:

![](Image00066.jpg)

3. Insert a node E in position 2.

![](Image00067.jpg)

![](Image00068.jpg)

Create a TestDoubleCircleLinkInsert.html with Notepad

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

        insert ( insertPosition , newNode ) {

            var p = this.head ;

            var i = 0 ;

            //Move the node to the insertion position

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

Result:

![](Image00069.jpg)

4. Delete the index=2 node.

![](Image00070.jpg)

![](Image00071.jpg)

Create a TestDoubleCircleLinkDelete.html with Notepad

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

Result:

![](Image00072.jpg)

Queue

Queue:

FIFO (First In First Out) sequence.

![](Image00073.jpg)

UML Diagram

![](Image00074.jpg)

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

1\. Queue initialization and traversal output .

Initialization Insert A

![](Image00075.jpg)

Initialization Insert B

![](Image00076.jpg)

Initialization Insert C

![](Image00077.jpg)

Initialization Insert D

![](Image00078.jpg)

Create a TestQueue.html with Notepad

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

    class Queue {

        constructor (){

            this.head = null ;

            this.tail = null ;

            this.size = 0 ;

        }

        offer ( element ) {

            if ( this.head == null ) {

                this.head = new Node ( element );

                this.tail = this.head ;

            } else {

                var newNode = new Node ( element );

                newNode.next = this.tail ;

                this.tail.prev = newNode ;

                this.tail = newNode ;

            }

            this.size ++;

        }

        poll () {

            var p = this.head ;

            if ( p == null ) {

                return null ;

            }

            this.head = this.head.prev ;

            p.next = null ;

            p.prev = null ;

            this.size --;

            return p ;

        }

        size () {

            return this.size ;

        }

    }

    //////////////////////testing////////////////////

    function print ( queue ) {

        document.write ( "Head " );

        var node = null ;

        while (( node = queue.poll ())!= null ) {

            document.write ( node.getData () + " <- " );

        }

        document.write ( "Tail <br>" );

    }

    var queue = new Queue ();

    queue.offer ( "A" );

    queue.offer ( "B" );

    queue.offer ( "C" );

    queue.offer ( "D" );

    print ( queue );

</script>

Result:

![](Image00079.jpg)

Stack

Stack:

FILO (First In Last Out) sequence.

![](Image00080.jpg)

UML Diagram

![](Image00081.jpg)

    class Node {

        constructor ( data , next ){

            this.data = data ;

            this.next = next ;

        }

        getData (){

            return this.data ;

        }

    }

1\. Stack initialization and traversal output .

Push A into Stack

![](Image00082.jpg)

Push B into Stack

![](Image00083.jpg)

Push C into Stack

![](Image00084.jpg)

Push D into Stack the same:

![](Image00085.jpg)

If pop D from Stack:

![](Image00086.jpg)

Create a TestStack.html with Notepad

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

    class Stack {

        constructor (){

            this.top = null ;

            this.size = 0 ;

        }

        push ( element ) {

            if ( this.top == null ) {

                this.top = new Node ( element );

            } else {

                var newNode = new Node ( element );

                newNode.next = this.top ;

                this.top = newNode ;

            }

            this.size ++;

        }

        pop () {

            if ( this.top == null ){

                return null ;

            }

            var p = this.top ;

            this.top = this.top.next ; // top move down

            p.next = null ;

            this.size --;

            return p ;

        }

        size () {

            return this.size ;

        }

    }

    //////////////////////testing////////////////////

    function print ( stack ) {

        document.write ( "Top " );

        var node = null ;

        while (( node = stack.pop ())!= null ) {

            document.write ( node.getData () + " -> " );

        }

        document.write ( "End <br>" );

    }

    var stack = new Stack ();

    stack.push ( "A" );

    stack.push ( "B" );

    stack.push ( "C" );

    stack.push ( "D" );

    print ( stack );

</script>

Result:

![](Image00087.jpg)

Recursive Algorithm

Recursive Algorithm:

The program function itself calls its own layer to progress until it reaches a certain condition and step by step returns to the end..

1\. Factorial of n : n*(n-1)*(n-2) ...... *2*1

Create a TestRecursive.html with Notepad

    <script type = "text/javascript" >

        function factorial ( n ) {

            if ( n == 1 ) {

                return 1 ;

            } else {

                //Recursively call yourself until the end of the return

                return factorial ( n - 1 ) * n ;

            }

        }

        //////////////////////testing////////////////////

        var n = 5 ;

        var fac = factorial ( n );

        document.write ( "The factorial of 5 is :" + fac );

Result:

![](Image00088.jpg)

Graphical analysis:

![](Image00089.jpg)

![](Image00090.jpg)

Two-way Merge Algorithm

Two-way Merge Algorithm:

The data of the first half and the second half are sorted, and the two ordered sub-list are merged into one ordered list, which continue to recursive to the end.

1\. The scores {50, 65, 99, 87, 74, 63, 76, 100} by merge sort

![](Image00091.jpg)

Create a TestMergeSort.html with Notepad

<script type = "text/javascript" >

    class MergeSort {

        sort ( array ) {

            var temp = new Array ( array.length );

            this.mergeSort ( array , temp , 0 , array.length - 1 );

        }

        mergeSort ( array , temp , left , right ) {

            if ( left < right ) {

                var center = parseInt (( left + right ) / 2 );

                this.mergeSort ( array , temp , left , center ); // Left merge sort

                this.mergeSort ( array , temp , center + 1 , right ); // Right merge sort

                this.merge ( array , temp , left , center + 1 , right ); // Merge two ordered arrays

            }

        }

        /**

         Combine two ordered list into an ordered list

         temp : Temporary array

         left :    Start the subscript on the left

         right :  Start the subscript on the right

         rightEndIndex : End subscript on the right

         */

        merge ( array , temp , left , right , rightEndIndex ) {

            var leftEndIndex = right - 1 ; // End subscript on the left

            var tempIndex = left ; // Starting from the left count

            var elementNumber = rightEndIndex - left + 1 ;

            while ( left <= leftEndIndex && right <= rightEndIndex ) {

                if ( array [ left ] <= array [ right ])

                    temp [ tempIndex ++] = array [ left ++];

                else

                    temp [ tempIndex ++] = array [ right ++];

            }

            while ( left <= leftEndIndex ) { // If there is element on the left

                temp [ tempIndex ++] = array [ left ++];

            }

            while ( right <= rightEndIndex ) { // If there is element on the right

                temp [ tempIndex ++] = array [ right ++];

            }

            // Copy temp to array

            for ( var i = 0 ; i < elementNumber ; i ++) {

                array [ rightEndIndex ] = temp [ rightEndIndex ];

                rightEndIndex --;

            }

        }

    }

    //////////////////////testing////////////////////

    var scores = [ 50 , 65 , 99 , 87 , 74 , 63 , 76 , 100 , 92 ];

    var mergeSort = new MergeSort ();

    mergeSort.sort ( scores );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + "," );

    }

</script>

Result:

![](Image00092.jpg)

Quick Sort Algorithm

Quick Sort Algorithm:

Divide the array into 2 subarrays, then call yourself recursively, sort the subarrays quickly, and continue to the end.

1\. The scores {90, 60, 50, 80, 70, 100} by quick sort

![](Image00093.jpg)

![](Image00094.jpg)

![](Image00095.jpg)

![](Image00096.jpg)

Create a TestQuickSort.html with Notepad

<script type = "text/javascript" >

    class QuickSort {

        sort ( array ) {

            if ( array.length > 0 ) {

                this.quickSort ( array , 0 , array.length - 1 );

            }

        }

        quickSort ( array , low , high ) {

            if ( low > high ) {

                return ;

            }

            var i = low ;

            var j = high ;

            var threshold = array [ low ];

            // Alternately scanned from both ends of the list

            while ( i < j ) {

                // Find the first position less than threshold from right to left

                while ( i < j && array [ j ] > threshold ) {

                    j --;

                }

                //Replace the low with a smaller number than the threshold

                if ( i < j )

                    array [ i ++] = array [ j ];

                // Find the first position greater than threshold from left to right

                while ( i < j && array [ i ] <= threshold ) {

                    i ++;

                }

                //Replace the high with a number larger than the threshold

                if ( i < j )

                    array [ j --] = array [ i ];

            }

            array [ i ] = threshold ;

            // left quickSort

            this.quickSort ( array , low , i - 1 );

            // right quickSort

            this.quickSort ( array , i + 1 , high );

        }

    }

    //////////////////////testing////////////////////

    var scores = [ 90 , 60 , 50 , 80 , 70 , 100 ];

    var quickSort = new QuickSort ();

    quickSort.sort ( scores );

    for ( var i = 0 ; i < scores.length ; i ++) {

        document.write ( scores [ i ] + "," );

    }

</script>

Result:

![](Image00097.jpg)

Binary Search Tree

Binary Search Tree:

1\. If the left subtree of any node is not empty, the value of all nodes on the left subtree is less than the value of its root node;

2\. If the right subtree of any node is not empty, the value of all nodes on the right subtree is greater than the value of its root node;

3\. The left subtree and the right subtree of any node are also binary search trees.

![](Image00098.jpg)

Node UML Diagram

![](Image00099.jpg)

    class Node {

        constructor ( data , left , right ){

            this.data = data ;

            this.left = left ;

            this.right = right ;

        }

        getData (){

            return this.data ;

        }

    }

1.Construct a binary search tree, insert node

The inserted nodes are compared from the root node, and the smaller than the root node is compared with the left subtree of the root node, otherwise, compared with the right subtree until the left subtree is empty or the right subtree is empty, then is inserted.

Insert 60

![](Image00100.jpg)

Insert 40

![](Image00101.jpg)

Insert 20

![](Image00102.jpg)

Insert 10

![](Image00103.jpg)

Insert 30

![](Image00104.jpg)

Insert 50

![](Image00105.jpg)

Insert 80

![](Image00106.jpg)

Insert 70

![](Image00107.jpg)

Insert 90

![](Image00108.jpg)

2. binary search tree In-order traversal

In-order traversal : left subtree -> root node -> right subtree

![](Image00109.jpg)

Result:

![](Image00110.jpg)

Create a TestBinarySearchTreeInOrder.html with Notepad

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

    document.write ( "<br> In-order traversal binary search tree <br>" );

    binaryTree.inOrder ( binaryTree.getRoot ());

</script>

Result:

![](Image00111.jpg)

3. binary search tree Pre-order traversal

Pre-order traversal : root node -> left subtree -> right subtree

![](Image00112.jpg)

Result:

![](Image00113.jpg)

Create a TestBinarySearchTreePreOrder.html with Notepad

<script type = "text/javascript" >

    class BinaryTree {

        getRoot () {

            return this.root ;

        }

        //Preorder traversal binary search tree

        preOrder ( root ) {

            if ( root == null ) {

                return ;

            }

            document.write ( root.getData () + ", " );

            this.preOrder ( root.left ); // Recursive Traversing the left subtree

            this.preOrder ( root.right ); // Recursive Traversing the right subtree

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

    document.write ( "<br> Pre-order traversal binary search tree <br>" );

    binaryTree.preOrder ( binaryTree.getRoot ());

</script>

Result:

![](Image00114.jpg)

4. binary search tree Post-order traversal

Post-order traversal : right subtree -> root node -> left subtree

![](Image00115.jpg)

Result:

![](Image00116.jpg)

Create a TestBinarySearchTreePostOrder.html with Notepad

<script type = "text/javascript" >

    class BinaryTree {

        getRoot () {

            return this.root ;

        }

        //Post-order traversal binary search tree

        postOrder ( root ) {

            if ( root == null ) {

                return ;

            }

            this.postOrder ( root.left ); // Recursive Traversing the left subtree

            this.postOrder ( root.right ); // Recursive Traversing the right subtree

            document.write ( root.getData () + ", " );

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

    document.write ( "<br> Post-order traversal binary search tree <br>" );

    binaryTree.postOrder ( binaryTree.getRoot ());

</script>

Result:

![](Image00117.jpg)

5. binary search tree Maximum and minimum

Minimum value: The small value is on the left child node, as long as the recursion traverses the left child until be empty, the current node is the minimum node.

Maximum value: The large value is on the right child node, as long as the recursive traversal is the right child until be empty, the current node is the largest node.

![](Image00118.jpg)

![](Image00119.jpg)

Create a TestBinarySearchTreeMaxMinValue.html with Notepad

<script type = "text/javascript" >

    class BinaryTree {

        getRoot () {

            return this.root ;

        }

        //Minimum value

        searchMinValue ( node ) {

            if ( node == null || node.getData () == 0 )

                return null ;

            if ( node.left == null ) {

                return node ;

            }

            //Recursively find the minimum from the left subtree

            return this.searchMinValue ( node.left );

        }

        //Maximum value

        searchMaxValue ( node ) {

            if ( node == null || node.getData () == 0 )

                return null ;

            if ( node.right == null ) {

                return node ;

            }

            //Recursively find the minimum from the right subtree

            return this.searchMaxValue ( node.right );

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

    document.write ( "<br> Minimum Value<br> " );

    var minNode = binaryTree.searchMinValue ( binaryTree.getRoot ());

    document.write ( minNode.getData ());

    document.write ( "<br> Maximum Value<br> " );

    var maxNode = binaryTree.searchMaxValue ( binaryTree.getRoot ());

    document.write ( maxNode.getData ());

</script>

Result:

![](Image00120.jpg)

6. binary search tree Delete Node

Binary search tree delete node 3 cases

1\. If there is no child node, delete it directly

2\. If there is only one child node, the child node replaces the current node, and then deletes the current node.

3\. If there are two child nodes, replace the current node with the smallest node from the right subtree, because the smallest node on the right is also larger than the value on the left.

![](Image00121.jpg)

![](Image00122.jpg)

![](Image00123.jpg)

![](Image00124.jpg)

![](Image00125.jpg)

![](Image00126.jpg)

Create a TestBinarySearchTreeDelete.html with Notepad

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

    document.write ( "<br>delete node is:  10 <br>" );

    binaryTree.remove ( binaryTree.getRoot (), 10 );

    document.write ( "<br>In-order traversal binary tree <br>" );

    binaryTree.inOrder ( binaryTree.getRoot ());

    document.write ( "<br>--------------------------------------------<br>" );

    document.write ( "<br>delete node is:  20<br>" );

    binaryTree.remove ( binaryTree.getRoot (), 20 );

    document.write ( "<br>In-order traversal binary tree<br>" );

    binaryTree.inOrder ( binaryTree.getRoot ());

    document.write ( "<br>--------------------------------------------<br>" );

    document.write ( "<br>delete node is:  40<br>" );

    binaryTree.remove ( binaryTree.getRoot (), 40 );

    document.write ( "<br>In-order traversal binary tree<br>" );

    binaryTree.inOrder ( binaryTree.getRoot ());

</script>

Result:

![](Image00127.jpg)

Binary Heap Sorting

Binary Heap Sorting:

The value of the non-terminal node in the binary tree is not greater than the value of its left and right child nodes.

Small top heap : ki <= k2i and ki <= k2i+1

Big top heap :ki >= k2i and ki >= k2i+1

Parent node subscript = (i-1)/2

Left subnode subscript = 2*i+1

Right subnode subscript = 2*i+2

Heap sorting process:

1\. Build a heap

2\. After outputting the top element of the heap, adjust from top to bottom, compare the top element with the root node of its left and right subtrees, and swap the smallest element to the top of the heap; then adjust continuously until the leaf nodes to get new heap.

1. {10, 90, 20, 80, 30, 70, 40, 60, 50} build heap and then heap sort output.

Initialize the heap and build the heap

![](Image00128.jpg)

![](Image00129.jpg)

![](Image00130.jpg)

![](Image00131.jpg)

![](Image00132.jpg)

![](Image00133.jpg)

![](Image00134.jpg)

![](Image00135.jpg)

Complete construction of the heap

2\. Start heap sorting

![](Image00136.jpg)

![](Image00137.jpg)

![](Image00138.jpg)

![](Image00139.jpg)

![](Image00140.jpg)

![](Image00141.jpg)

![](Image00142.jpg)

![](Image00143.jpg)

![](Image00144.jpg)

![](Image00145.jpg)

![](Image00146.jpg)

![](Image00147.jpg)

![](Image00148.jpg)

![](Image00149.jpg)

Heap sort result

![](Image00150.jpg)

Create a TestBinaryHeapSorting.html with Notepad

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

            //2 * currentIndex + 1  Current left subtree subscript

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

Result:

![](Image00151.jpg)

Hash Table

Hash Table:

Access by mapping key => values in the table.

1\. Map {19, 18, 35,40,41,42} to the HashTable mapping rule key % 4

![](Image00152.jpg)

![](Image00153.jpg)

2\. Implement a Hashtable

![](Image00154.jpg)

Create a TestHashtable.html with Notepad

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

Result:

![](Image00155.jpg)

Undirected Graph and Depth-Frst Search

Undirected Graph:

The data structure is represented by an adjacency matrix (that is, a two-dimensional array) and an adjacency list. Each node is called a vertex, and two adjacent nodes are called edges.

Undirected Graph No direction : A -> B = B -> A

![](Image00156.jpg)

1\. The adjacency matrix is described above:

The total number of vertices is a two-dimensional array size, if have value of the edge is 1 , otherwise no value of the edge is 0 .

![](Image00157.jpg)

2\. Depth-Frst Search:

Look for the neighboring edge node B from A and then find the neighboring node C from B and so on until all nodes are found A -> B -> C -> D -> E .

![](Image00158.jpg)

![](Image00159.jpg)

![](Image00160.jpg)

Create a TestUndirectedGraphDepthFrstSearch.html with Notepad

<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {

            return this.data ;

        }

        setData ( data ) {

            this.data = data ;

        }

        isVisited () {

            return this.visited ;

        }

        setVisited ( visited ) {

            this.visited = visited ;

        }

    }

    class Stack {

        constructor (){

            this.stacks = new Array ();

            this.top = - 1 ;

        }

        push ( element ) {

            this.top ++;

            this.stacks [ this.top ] = element ;

        }

        pop () {

            if ( this.top == - 1 ){

                return - 1 ;

            }

            var data = this.stacks [ this.top ];

            this.top --;

            return data ;

        }

        peek () {

            if ( this.top == - 1 ){

                return - 1 ;

            }

            var data = this.stacks [ this.top ];

            return data ;

        }

        isEmpty () {

            if ( this.top <= - 1 ){

                return true ;

            }

            return false ;

        }

    }

    class Graph {

        constructor ( maxVertexSize ){

            this.maxVertexSize = maxVertexSize ; // Two-dimensional array size

            this.vertexs = new Array ( maxVertexSize );

            this.size = 0 ; // Current vertex size

            this.adjacencyMatrix = new Array ( maxVertexSize );

            for ( var i = 0 ; i < maxVertexSize ; i ++) {

                this.adjacencyMatrix [ i ] = new Array ();

                for ( var j = 0 ; j < maxVertexSize ; j ++) {

                    this.adjacencyMatrix [ i ][ j ] = 0 ;

                }

            }

            this.stack = new Stack (); // Stack saves current vertices

        }

        addVertex ( data ) {

            var vertex = new Vertex ( data , false );

            this.vertexs [ this.size ] = vertex ;

            this.size ++;

        }

        // Add adjacent edges

        addEdge ( from , to ) {

            // A -> B = B -> A

            this.adjacencyMatrix [ from ][ to ] = 1 ;

            this.adjacencyMatrix [ to ][ from ] = 1 ;

        }

        depthFirstSearch () {

            // Start searching from the first vertex

            var firstVertex = this.vertexs [ 0 ];

            firstVertex.setVisited ( true );

            document.write ( firstVertex.getData ());

            this.stack.push ( 0 );

            while (! this.stack.isEmpty ()) {

                var row = this.stack.peek ();

                // Get adjacent vertex positions that have not been visited

                var col = this.findAdjacencyUnVisitedVertex ( row );

                if ( col == - 1 ) {

                    this.stack.pop ();

                } else {

                    this.vertexs [ col ]. setVisited ( true );

                    document.write ( " -> " + this.vertexs [ col ]. getData ());

                    this.stack.push ( col );

                }

            }

            this.clear ();

        }

        // Get adjacent vertex positions that have not been visited

        findAdjacencyUnVisitedVertex ( row ) {

            for ( var col = 0 ; col < this.size ; col ++) {

                if ( this.adjacencyMatrix [ row ][ col ] == 1 && ! this.vertexs [ col ]. isVisited ()) {

                    return col ;

                }

            }

            return - 1 ;

        }

        // Clear reset

        clear () {

            for ( var i = 0 ; i < this.size ; i ++) {

                this.vertexs [ i ]. setVisited ( false );

            }

        }

        getAdjacencyMatrix () {

            return this.adjacencyMatrix ;

        }

        getVertexs () {

            return this.vertexs ;

        }

    }

    //////////////////////testing////////////////////

    function printGraph ( graph ) {

        document.write ( "Two-dimensional array traversal output vertex edge and adjacent array :  <br>" );

        for ( var i = 0 ; i < graph.getVertexs (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

        }

        document.write ( "<br>" );

        for ( var i = 0 ; i < graph.getAdjacencyMatrix (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

            for ( var j = 0 ; j < graph.getAdjacencyMatrix (). length ; j ++) {

                document.write ( graph.getAdjacencyMatrix ()[ i ][ j ] + "  " );

            }

            document.write ( "<br>" );

        }

    }

    var graph = new Graph ( 5 );

    graph.addVertex ( "A" );

    graph.addVertex ( "B" );

    graph.addVertex ( "C" );

    graph.addVertex ( "D" );

    graph.addVertex ( "E" );

    graph.addEdge ( 0 , 1 );

    graph.addEdge ( 0 , 2 );

    graph.addEdge ( 0 , 3 );

    graph.addEdge ( 1 , 2 );

    graph.addEdge ( 1 , 3 );

    graph.addEdge ( 2 , 3 );

    graph.addEdge ( 3 , 4 );

    // Two-dimensional array traversal output vertex edge and adjacent array

    printGraph ( graph );

    document.write ( "<br>Depth-first search traversal output : <br>" );

    graph.depthFirstSearch ();

</script>

Result:

![](Image00161.jpg)

Undirected Graph and Breadth-First Search

Breadth-First Search:

Find all neighboring edge nodes B, C, D from A and then find all neighboring nodes A, C, D from B and so on until all nodes are found A -> B -> C -> D -> E .

![](Image00162.jpg)

![](Image00163.jpg)

![](Image00164.jpg)

Create a TestUndirectedGraphBreadthFrstSearch.html with Notepad

<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {

            return this.data ;

        }

        setData ( data ) {

            this.data = data ;

        }

        isVisited () {

            return this.visited ;

        }

        setVisited ( visited ) {

            this.visited = visited ;

        }

    }

    class Queue {

        constructor (){

            this.queues = new Array ();

        }

        add ( element ) {

            this.queues [ this.queues.length ] = element ;

        }

        remove () {

            if ( this.queues.length <= 0 ){

                return - 1 ;

            }

            return this.queues.shift ();

        }

        isEmpty () {

            if ( this.queues.length <= 0 ){

                return true ;

            }

            return false ;

        }

    }

    class Graph {

        constructor ( maxVertexSize ){

            this.maxVertexSize = maxVertexSize ; // Two-dimensional array size

            this.vertexs = new Array ( maxVertexSize );

            this.size = 0 ; // Current vertex size

            this.adjacencyMatrix = new Array ( maxVertexSize );

            for ( var i = 0 ; i < maxVertexSize ; i ++) {

                this.adjacencyMatrix [ i ] = new Array ();

                for ( var j = 0 ; j < maxVertexSize ; j ++) {

                    this.adjacencyMatrix [ i ][ j ] = 0 ;

                }

            }

            this.queue = new Queue (); // Queue  saves current vertices

        }

        addVertex ( data ) {

            var vertex = new Vertex ( data , false );

            this.vertexs [ this.size ] = vertex ;

            this.size ++;

        }

        // Add adjacent edges

        addEdge ( from , to ) {

            // A -> B = B -> A

            this.adjacencyMatrix [ from ][ to ] = 1 ;

            this.adjacencyMatrix [ to ][ from ] = 1 ;

        }

        breadthFirstSearch () {

            // Start searching from the first vertex

            var firstVertex = this.vertexs [ 0 ];

            firstVertex.setVisited ( true );

            document.write ( firstVertex.getData ());

            this.queue.add ( 0 );

            var col = 0 ;

            while (! this.queue.isEmpty ()) {

                var head = this.queue.remove ();

             // Get adjacent vertex positions that have not been visited

                col = this.findAdjacencyUnVisitedVertex ( head );

              //Loop through all vertices connected to the current vertex

                while ( col != - 1 )

                {

                    this.vertexs [ col ]. setVisited ( true );

                    document.write ( " -> " + this.vertexs [ col ]. getData ());

                    this.queue.add ( col );

                    col = this.findAdjacencyUnVisitedVertex ( head );

                }

            }

            this.clear ();

        }

        // Get adjacent vertex positions that have not been visited

        findAdjacencyUnVisitedVertex ( row ) {

            for ( var col = 0 ; col < this.size ; col ++) {

                if ( this.adjacencyMatrix [ row ][ col ] == 1 && ! this.vertexs [ col ]. isVisited ()) {

                    return col ;

                }

            }

            return - 1 ;

        }

        // Clear reset

        clear () {

            for ( var i = 0 ; i < this.size ; i ++) {

                this.vertexs [ i ]. setVisited ( false );

            }

        }

        getAdjacencyMatrix () {

            return this.adjacencyMatrix ;

        }

        getVertexs () {

            return this.vertexs ;

        }

    }

    //////////////////////testing////////////////////

    function printGraph ( graph ) {

        document.write ( "Two-dimensional array traversal output vertex edge and adjacent array :  <br>" );

        document.write ( "&nbsp;&nbsp;&nbsp;" );

        for ( var i = 0 ; i < graph.getVertexs (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "&nbsp;&nbsp;&nbsp;&nbsp;" );

        }

        document.write ( "<br>" );

        for ( var i = 0 ; i < graph.getAdjacencyMatrix (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

            for ( var j = 0 ; j < graph.getAdjacencyMatrix (). length ; j ++) {

                document.write ( graph.getAdjacencyMatrix ()[ i ][ j ] + "&nbsp;&nbsp;&nbsp;&nbsp;" );

            }

            document.write ( "<br>" );

        }

    }

    var graph = new Graph ( 5 );

    graph.addVertex ( "A" );

    graph.addVertex ( "B" );

    graph.addVertex ( "C" );

    graph.addVertex ( "D" );

    graph.addVertex ( "E" );

    graph.addEdge ( 0 , 1 );

    graph.addEdge ( 0 , 2 );

    graph.addEdge ( 0 , 3 );

    graph.addEdge ( 1 , 2 );

    graph.addEdge ( 1 , 3 );

    graph.addEdge ( 2 , 3 );

    graph.addEdge ( 3 , 4 );

    // Two-dimensional array traversal output vertex edge and adjacent array

    printGraph ( graph );

    document.write ( "\nBreadth-First Search traversal output : <br>" );

    graph.breadthFirstSearch ();

</script>

Result:

![](Image00165.jpg)

Directed Graph and Depth-Frst Search

Directed Graph:

The data structure is represented by an adjacency matrix (that is, a two-dimensional array) and an adjacency list. Each node is called a vertex, and two adjacent nodes are called edges.

Directed Graph has direction : A -> B and B -> A are different

![](Image00166.jpg)

1\. The adjacency matrix is described above:

The total number of vertices is a two-dimensional array size, if have value of the edge is 1 , otherwise no value of the edge is 0 .

![](Image00167.jpg)

2\. Depth-Frst Search:

Look for the neighboring edge node B from A and then find the neighboring node C from B and so on until all nodes are found A -> B -> C -> D -> E .

![](Image00168.jpg)

![](Image00169.jpg)

![](Image00170.jpg)

Create a TestDirectedGraphDepthFrstSearch.html with Notepad

<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {

            return this.data ;

        }

        setData ( data ) {

            this.data = data ;

        }

        isVisited () {

            return this.visited ;

        }

        setVisited ( visited ) {

            this.visited = visited ;

        }

    }

    class Stack {

        constructor (){

            this.stacks = new Array ();

            this.top = - 1 ;

        }

        push ( element ) {

            this.top ++;

            this.stacks [ this.top ] = element ;

        }

        pop () {

            if ( this.top == - 1 ){

                return - 1 ;

            }

            var data = this.stacks [ this.top ];

            this.top --;

            return data ;

        }

        peek () {

            if ( this.top == - 1 ){

                return - 1 ;

            }

            var data = this.stacks [ this.top ];

            return data ;

        }

        isEmpty () {

            if ( this.top <= - 1 ){

                return true ;

            }

            return false ;

        }

    }

    class Graph {

        constructor ( maxVertexSize ){

            this.maxVertexSize = maxVertexSize ; // Two-dimensional array size

            this.vertexs = new Array ( maxVertexSize );

            this.size = 0 ; // Current vertex size

            this.adjacencyMatrix = new Array ( maxVertexSize );

            for ( var i = 0 ; i < maxVertexSize ; i ++) {

                this.adjacencyMatrix [ i ] = new Array ();

                for ( var j = 0 ; j < maxVertexSize ; j ++) {

                    this.adjacencyMatrix [ i ][ j ] = 0 ;

                }

            }

            this.stack = new Stack (); // Stack saves current vertices

        }

        addVertex ( data ) {

            var vertex = new Vertex ( data , false );

            this.vertexs [ this.size++ ] = vertex ;

        }

        addEdge ( from , to ) {

            this.adjacencyMatrix [ from ][ to ] = 1 ; // A -> B  and B -> A are different

        }

        depthFirstSearch () {

            var firstVertex = this.vertexs [ 0 ]; // Start searching from the first vertex

            firstVertex.setVisited ( true );

            document.write ( firstVertex.getData ());

            this.stack.push ( 0 );

            while (! this.stack.isEmpty ()) {

                var row = this.stack.peek ();

                // Get adjacent vertex positions that have not been visited

                var col = this.findAdjacencyUnVisitedVertex ( row );

                if ( col == - 1 ) {

                    this.stack.pop ();

                } else {

                    this.vertexs [ col ]. setVisited ( true );

                    document.write ( " -> " + this.vertexs [ col ]. getData ());

                    this.stack.push ( col );

                }

            }

            this.clear ();

        }

        // Get adjacent vertex positions that have not been visited

        findAdjacencyUnVisitedVertex ( row ) {

            for ( var col = 0 ; col < this.size ; col ++) {

                if ( this.adjacencyMatrix [ row ][ col ] == 1 && ! this.vertexs [ col ]. isVisited ()) {

                    return col ;

                }

            }

            return - 1 ;

        }

        // Clear reset

        clear () {

            for ( var i = 0 ; i < this.size ; i ++) {

                this.vertexs [ i ]. setVisited ( false );

            }

        }

        getAdjacencyMatrix () {

            return this.adjacencyMatrix ;

        }

        getVertexs () {

            return this.vertexs ;

        }

    }

    //////////////////////testing///////////////////

    function printGraph ( graph ) {

        document.write ( "Two-dimensional array traversal output vertex edge and adjacent array :  <br>" );

        document.write ( "&nbsp;&nbsp;&nbsp;" );

        for ( var i = 0 ; i < graph.getVertexs (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "&nbsp;&nbsp;&nbsp;&nbsp;" );

        }

        document.write ( "<br>" );

        for ( var i = 0 ; i < graph.getAdjacencyMatrix (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

            for ( var j = 0 ; j < graph.getAdjacencyMatrix (). length ; j ++) {

                document.write ( graph.getAdjacencyMatrix ()[ i ][ j ] + "&nbsp;&nbsp;&nbsp;&nbsp;" );

            }

            document.write ( "<br>" );

        }

    }

    var graph = new Graph ( 5 );

    graph.addVertex ( "A" );

    graph.addVertex ( "B" );

    graph.addVertex ( "C" );

    graph.addVertex ( "D" );

    graph.addVertex ( "E" );

    graph.addEdge ( 0 , 1 );

    graph.addEdge ( 0 , 2 );

    graph.addEdge ( 0 , 3 );

    graph.addEdge ( 1 , 2 );

    graph.addEdge ( 1 , 3 );

    graph.addEdge ( 2 , 3 );

    graph.addEdge ( 3 , 4 );

    // Two-dimensional array traversal output vertex edge and adjacent array

    printGraph ( graph );

    document.write ( "<br>Depth-first search traversal output : <br>" );

    graph.depthFirstSearch ();

</script>

Result:

![](Image00171.jpg)

Directed Graph and Breadth-First Search

Breadth-First Search:

Find all neighboring edge nodes B, C, D from A and then find all neighboring nodes A, C, D from B and so on until all nodes are found A -> B -> C -> D -> E .

![](Image00172.jpg)

![](Image00173.jpg)

![](Image00174.jpg)

Create a TestDirectedGraphBreadthFrstSearch.html with Notepad

<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {

            return this.data ;

        }

        setData ( data ) {

            this.data = data ;

        }

        isVisited () {

            return this.visited ;

        }

        setVisited ( visited ) {

            this.visited = visited ;

        }

    }

    class Queue {

        constructor (){

            this.queues = new Array ();

        }

        add ( element ) {

            this.queues [ this.queues.length ] = element ;

        }

        remove () {

            if ( this.queues.length <= 0 ){

                return - 1 ;

            }

            return this.queues.shift ();

        }

        isEmpty () {

            if ( this.queues.length <= 0 ){

                return true ;

            }

            return false ;

        }

    }

    class Graph {

        constructor ( maxVertexSize ){

            this.maxVertexSize = maxVertexSize ; // Two-dimensional array size

            this.vertexs = new Array ( maxVertexSize );

            this.size = 0 ; // Current vertex size

            this.adjacencyMatrix = new Array ( maxVertexSize );

            for ( var i = 0 ; i < maxVertexSize ; i ++) {

                this.adjacencyMatrix [ i ] = new Array ();

                for ( var j = 0 ; j < maxVertexSize ; j ++) {

                    this.adjacencyMatrix [ i ][ j ] = 0 ;

                }

            }

            this.queue = new Queue (); // Queue  saves current vertices

        }

        addVertex ( data ) {

            var vertex = new Vertex ( data , false );

            this.vertexs [ this.size ] = vertex ;

            this.size ++;

        }

        // Add adjacent edges

        addEdge ( from , to ) {

            // A -> B  and B -> A are different

            this.adjacencyMatrix [ from ][ to ] = 1 ;

        }

        breadthFirstSearch () {

            // Start searching from the first vertex

            var firstVertex = this.vertexs [ 0 ];

            firstVertex.setVisited ( true );

            document.write ( firstVertex.getData ());

            this.queue.add ( 0 );

            var col = 0 ;

            while (! this.queue.isEmpty ()) {

                var head = this.queue.remove ();

             // Get adjacent vertex positions that have not been visited

                col = this.findAdjacencyUnVisitedVertex ( head );

              //Loop through all vertices connected to the current vertex

                while ( col != - 1 )

                {

                    this.vertexs [ col ]. setVisited ( true );

                    document.write ( " -> " + this.vertexs [ col ]. getData ());

                    this.queue.add ( col );

                    col = this.findAdjacencyUnVisitedVertex ( head );

                }

            }

            this.clear ();

        }

        // Get adjacent vertex positions that have not been visited

        findAdjacencyUnVisitedVertex ( row ) {

            for ( var col = 0 ; col < this.size ; col ++) {

                if ( this.adjacencyMatrix [ row ][ col ] == 1 && ! this.vertexs [ col ]. isVisited ()) {

                    return col ;

                }

            }

            return - 1 ;

        }

        // Clear reset

        clear () {

            for ( var i = 0 ; i < this.size ; i ++) {

                this.vertexs [ i ]. setVisited ( false );

            }

        }

        getAdjacencyMatrix () {

            return this.adjacencyMatrix ;

        }

        getVertexs () {

            return this.vertexs ;

        }

    }

    //////////////////////testing////////////////////

    function printGraph ( graph ) {

        document.write ( "Two-dimensional array traversal output vertex edge and adjacent array :  <br>" );

        document.write ( "&nbsp;&nbsp;&nbsp;" );

        for ( var i = 0 ; i < graph.getVertexs (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "&nbsp;&nbsp;&nbsp;&nbsp;" );

        }

        document.write ( "<br>" );

        for ( var i = 0 ; i < graph.getAdjacencyMatrix (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

            for ( var j = 0 ; j < graph.getAdjacencyMatrix (). length ; j ++) {

                document.write ( graph.getAdjacencyMatrix ()[ i ][ j ] + "&nbsp;&nbsp;&nbsp;&nbsp;" );

            }

            document.write ( "<br>" );

        }

    }

    var graph = new Graph ( 5 );

    graph.addVertex ( "A" );

    graph.addVertex ( "B" );

    graph.addVertex ( "C" );

    graph.addVertex ( "D" );

    graph.addVertex ( "E" );

    graph.addEdge ( 0 , 1 );

    graph.addEdge ( 0 , 2 );

    graph.addEdge ( 0 , 3 );

    graph.addEdge ( 1 , 2 );

    graph.addEdge ( 1 , 3 );

    graph.addEdge ( 2 , 3 );

    graph.addEdge ( 3 , 4 );

    // Two-dimensional array traversal output vertex edge and adjacent array

    printGraph ( graph );

    document.write ( "\nBreadth-First Search traversal output : <br>" );

    graph.breadthFirstSearch ();

</script>

Result:

![](Image00175.jpg)

Directed Graph Topological Sorting

Directed Graph Topological Sorting:

Sort the vertices in the directed graph with order of direction

.

Directed Graph has direction : A -> B and B -> A are different

![](Image00166.jpg)

1\. The adjacency matrix is described above:

The total number of vertices is a two-dimensional array size, if have value of the edge is 1 , otherwise no value of the edge is 0 .

![](Image00167.jpg)

Topological sorting from vertex A : A -> B -> C -> D -> E

![](Image00176.jpg)

![](Image00177.jpg)

![](Image00178.jpg)

Create a TestTopologicalSorting.html with Notepad

<script type = "text/javascript" >

    class Vertex {

        constructor ( data , visited ){

            this.data = data ;

            this.visited = visited ; // Have you visited

        }

        getData () {

            return this.data ;

        }

        setData ( data ) {

            this.data = data ;

        }

        isVisited () {

            return this.visited ;

        }

        setVisited ( visited ) {

            this.visited = visited ;

        }

    }

    class Graph {

        constructor ( maxVertexSize ){

            this.maxVertexSize = maxVertexSize ; // Two-dimensional array size

            this.vertexs = new Array ( maxVertexSize );

            this.topologys = new Array ();

            this.adjacencyMatrix = new Array ( maxVertexSize );

            for ( var i = 0 ; i < maxVertexSize ; i ++) {

                this.adjacencyMatrix [ i ] = new Array ();

                for ( var j = 0 ; j < maxVertexSize ; j ++) {

                    this.adjacencyMatrix [ i ][ j ] = 0 ;

                }

            }

            this.size = 0 ;

        }

        addVertex ( data ) {

            var vertex = new Vertex ( data , false );

            this.vertexs [ this.size ] = vertex ;

            this.size ++;

        }

        // Add adjacent edges

        addEdge ( from , to ) {

            // A -> B  and B -> A are different

            this.adjacencyMatrix [ from ][ to ] = 1 ;

        }

        topologySort () {

            while ( this.size > 0 ) {

                var noSuccessorVertex = this.getNoSuccessorVertex (); // Get a no successor node

                if ( noSuccessorVertex == - 1 ) {

                    document.write ( "There is ring in Graph " );

                    return ;

                }

                // Copy the deleted node to the sorted array

                this.topologys [ this.size - 1 ] = this.vertexs [ noSuccessorVertex ];

                this.removeVertex ( noSuccessorVertex ); // Delete no successor node

            }

        }

        getNoSuccessorVertex () {

            var existSuccessor = false ;

            for ( var row = 0 ; row < this.size ; row ++) { // For each vertex

                existSuccessor = false ;

                //If the node has a fixed row, each column has a 1, indicating that the node has a successor, terminating the loop

                for ( var col = 0 ; col < this.size ; col ++) {

                    if ( this.adjacencyMatrix [ row ][ col ] == 1 ) {

                        existSuccessor = true ;

                        break ;

                    }

                }

                if (! existSuccessor ) { // If the node has no successor, return its subscript

                    return row ;

                }

            }

            return - 1 ;

        }

        removeVertex ( vertex ) {

            if ( vertex != this.size - 1 ) { //If the vertex is the last element, the end

                for ( var i = vertex ; i < this.size - 1 ; i ++) { // The vertices are removed from the vertex array

                    this.vertexs [ i ] = this.vertexs [ i + 1 ];

                }

                for ( var row = vertex ; row < this.size - 1 ; row ++) { // move up a row

                    for ( var col = 0 ; col < this.size - 1 ; col ++) {

                        this.adjacencyMatrix [ row ][ col ] = this.adjacencyMatrix [ row + 1 ][ col ];

                    }

                }

                for ( var col = vertex ; col < this.size - 1 ; col ++) { // move left a row

                    for ( var row = 0 ; row < this.size - 1 ; row ++) {

                        this.adjacencyMatrix [ row ][ col ] = this.adjacencyMatrix [ row ][ col + 1 ];

                    }

                }

            }

            this.size --; // Decrease the number of vertices

        }

        // Clear reset

        clear () {

            for ( var i = 0 ; i < this.size ; i ++) {

                this.vertexs [ i ]. setVisited ( false );

            }

        }

        getAdjacencyMatrix () {

            return this.adjacencyMatrix ;

        }

        getVertexs () {

            return this.vertexs ;

        }

        getTopologys () {

            return this.topologys ;

        }

    }

    //////////////////////testing////////////////////

    function printGraph ( graph ) {

        document.write ( "Two-dimensional array traversal output vertex edge and adjacent array :  <br>" );

        document.write ( "&nbsp;&nbsp;&nbsp;" );

        for ( var i = 0 ; i < graph.getVertexs (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "&nbsp;&nbsp;&nbsp;&nbsp;" );

        }

        document.write ( "<br>" );

        for ( var i = 0 ; i < graph.getAdjacencyMatrix (). length ; i ++) {

            document.write ( graph.getVertexs ()[ i ]. getData () + "  " );

            for ( var j = 0 ; j < graph.getAdjacencyMatrix (). length ; j ++) {

                document.write ( graph.getAdjacencyMatrix ()[ i ][ j ] + "&nbsp;&nbsp;&nbsp;&nbsp;" );

            }

            document.write ( "<br>" );

        }

    }

    var graph = new Graph ( 5 );

    graph.addVertex ( "A" );

    graph.addVertex ( "B" );

    graph.addVertex ( "C" );

    graph.addVertex ( "D" );

    graph.addVertex ( "E" );

    graph.addEdge ( 0 , 1 );

    graph.addEdge ( 0 , 2 );

    graph.addEdge ( 0 , 3 );

    graph.addEdge ( 1 , 2 );

    graph.addEdge ( 1 , 3 );

    graph.addEdge ( 2 , 3 );

    graph.addEdge ( 3 , 4 );

    // Two-dimensional array traversal output vertex edge and adjacent array

    printGraph ( graph );

    document.write ( "<br>Depth-First Search traversal output : <br>" );

    document.write ( "Directed Graph Topological Sorting:<br>" );

    graph.topologySort ();

    for ( var i = 0 ; i < graph.getTopologys (). length ; i ++){

        document.write ( graph.getTopologys ()[ i ]. getData ()+ " -> " );

    }

</script>

Result:

![](Image00179.jpg)