# 面试中最常见的 50 道 JavaScript 编程题






## 关于我
**Rahul Chaurasia**
**2 年经验 React 开发者**
**计算机应用硕士 (MCA), NIT Raipur**

**与我联系**
- [Topmate:](https://topmate.io/rahul_chaurasia12)
- [LinkedIn](https://www.linkedin.com/in/rahul-chaurasia-997a56186/)

## 第 1 部分 - 数字

### Q-1 写一个 JS 程序找到任意给定数字的阶乘。（常问）
方法 :-
```javascript
let number = 7; // 要计算阶乘的数字
// 计算给定数字阶乘的函数
function findFactorial(num) {
  // 0 的阶乘定义为 1
  if (num === 0) {
    return 1;
  }
  // 初始化阶乘结果为 1
  let factorial = 1;
  // 通过乘以从 1 到 num 的每个整数来计算阶乘
  for (let i = 1; i <= num; i++) {
    factorial *= i;
  }
  return factorial;
}
const result = findFactorial(number);
console.log(result); // 输出: 5040
```
**输出:** 7 的阶乘是 5040。
**时间复杂度:** O(n)
**解释：** 该程序计算数字 7 的阶乘。`findFactorial` 函数首先检查数字是否为 0，如果是则返回 1（因为 0! = 1）。对于大于 0 的数字，它将 factorial 初始化为 1，并乘以从 1 到 7 的每个整数。最终结果 5040 是 7 的阶乘。时间复杂度为 O(n)，其中 n 是 num 的值，因为涉及多次乘法运算。

### Q-2 写一个 JS 程序检查给定的数字是否为质数。（常问）
方法 :-
```javascript
let number = 13; // 要检查质数性的数字
// 检查给定数字是否为质数的函数
function isPrime(num) {
  // 处理特殊情况：0、1 和负数不是质数
  if (num <= 1) {
    return false;
  }
  // 从 2 到 num/2 检查可整除性
  for (let i = 2; i <= num/2; i++) {
    if (num % i === 0) {
      return false; // 如果被 i 整除则不是质数
    }
  }
  return true; // 如果没有找到除数，则返回 true
}
const result = isPrime(number);
console.log(result); // 输出: true（因为 13 是质数）
```
**输出:** 输出为 true，因为 13 是质数。
**时间复杂度:** O(n)
**解释：** `isPrime` 函数检查从 2 到 num/2 的整除性。如果找到除数，则返回 false。该方法判断给定数字的质数性。

### Q-3 写一个 JS 程序反转给定数字的数字。（常问）
方法 :-
```javascript
let num = 34567; // 要反转的数字
// 反转数字数字的函数
function reverseDigits(num) {
  let s = num.toString(); // 将数字转换为字符串
  return s.split("").reverse().join(""); // 反转字符串并重新拼接
}
const result = reverseDigits(num);
console.log(result); // 输出: 76543
```
**输出:** 数字 34567 的数字反转后是 76543。
**时间复杂度:** O(n)
**解释：** 该函数将数字转换为字符串，反转字符串，然后重新拼接。

### Q-4 写一个 JS 程序返回给定数字的斐波那契数列。（常问）
方法 :-
```javascript
// 生成斐波那契数列的函数
function fibonacci(n) {
  if (n <= 0) return [];
  if (n === 1) return [0];
  let fib = [0, 1];
  for (let i = 2; i < n; i++) {
    fib.push(fib[i - 1] + fib[i - 2]);
  }
  return fib;
}
const n = 5;
const result = fibonacci(n);
console.log(result); // 输出: [0, 1, 1, 2, 3]
```
**输出:** 前 5 个斐波那契数是 [0, 1, 1, 2, 3]。
**时间复杂度:** O(n)
**解释：** 该函数通过不断累加前两个数来生成斐波那契数列，时间复杂度为 O(n)。

### Q-5 写一个 JS 程序在不使用临时变量的情况下交换变量。（常问）
方法 :-
```javascript
// 在不使用临时变量的情况下交换变量的函数
function swap(a, b) {
  a = a + b;
  b = a - b;
  a = a - b;
  console.log(`a=${a}, b=${b}`);
}
swap(10, 20); // 输出: a=20, b=10
```
**输出:** a=20, b=10
**复杂度:** O(1)
**解释：** 该方法使用算术加减法在不使用额外空间的情况下交换两个值。

## 第 2 部分 - 数组

### Q-6 写一个 JS 程序计算数组中所有元素的和。（常问）
```javascript
function sumArray(arr) {
  return arr.reduce((sum, num) => sum + num, 0);
}
const numbers = [10, 20, 30, 40, 50];
const total = sumArray(numbers);
console.log(total); // 输出: 150
```
该函数使用 `reduce` 方法遍历数组，并从值 0 开始累加。

### Q-7 写一个 JS 程序在排序数组上进行二分查找。（常问）
方法 :-
```javascript
let arr = [1, 3, 7, 8, 9, 34, 56];
let k = 9; // 要查找的值
// 执行二分查找函数
function binarySearch(arr, k) {
  let start = 0;
  let end = arr.length - 1;
  while (start <= end) {
    let mid = Math.floor((start + end) / 2);
    // 如果 k 小于中间元素，在左半部分查找
    if (k < arr[mid]) {
      end = mid - 1;
    }
    // 如果 k 大于中间元素，在右半部分查找
    else if (k > arr[mid]) {
      start = mid + 1;
    }
    // 如果 k 等于中间元素，返回索引
    else if (k === arr[mid]) {
      return mid;
    }
  }
  return -1; // 未找到元素
}
const result = binarySearch(arr, k);
console.log(result); // 输出: 4（因为 9 在索引 4 ）
```
**输出:** 元素 9 在索引 4。
**时间复杂度:** O(log n)
**解释：** 该程序实现了二分查找算法，用于在排序数组中查找元素。算法反复将搜索范围减半。如果搜索值小于中间元素，则将范围缩小到下半部分，否则缩小到上半部分。时间复杂度为 O(log n)，其中 n 是数组中的元素个数。

### Q-8 写一个 JS 程序找到数组中的最大元素。（常问）
方法 :-


面试中最常的 50 道 JavaScript 编码题

8

let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9]; // 检查的数组

// 查找数组中最大元素的函数
function findMaxElement(arr) {
  let max = -Infinity; // 初始化 max 为最小可能的值
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i]; // 如果当前元素大于 max，则更新 max
    }
  }
  return max;
}
let result = findMaxElement(arr);
console.log(result); // 输出: 9

**输出：** 数组 `[1, 2, 3, 4, 5, 6, 7, 8, 9]` 中的最大元素是 `9`。

**时间复杂度：** *O(n)*

**解析：** 该函数遍历数组以找到最大值。时间复杂度为 *O(n)*，其中 `n` 是数组的长度。

**Q-9** **编写一个 JS 程序来找出数组中的偶数。**

方法 :-

let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; // 数组

// 查找数组中偶数的函数
function evenNumbers(arr) {
  return arr.filter((ele) => ele % 2 === 0); // 过滤数组得到偶数
}

let result = evenNumbers(arr);
console.log(result); // 输出: [2, 4, 6, 8, 10]

**输出：** 数组 `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` 经过过滤后仅返回偶数 `[2, 4, 6, 8, 10]`。

**时间复杂度：** *O(n)*

**解析：** 函数 `evenNumbers` 过滤原始数组，只返回偶数元素（`ele % 2 === 0`）。时间复杂度为 *O(n)*，其中 `n` 是数组中的元素个数。

**Q-10** **编写一个 JS 程序反转数组。（最常问）**

方法 :-

let originalArray = [1, 2, 3, 4, 5, 6, 7];

// 反转数组的函数
function reverseArray(array) {
  let reversedArray = [];
  for (let i = array.length - 1; i >= 0; i--) {
    reversedArray.push(array[i]);
  }
  return reversedArray;
}
const reversed = reverseArray(originalArray);
console.log(reversed); // 输出: [7, 6, 5, 4, 3, 2, 1]

**输出：** 反转后的数组是 `[7, 6, 5, 4, 3, 2, 1]`。

**时间复杂度：** *O(n)*

**解析：** 该程序实现了 `reverseArray` 来反转 `originalArray` 中元素的顺序。它使用索引 `i` 从数组末尾开始遍历，将每个元素推入新数组 `reversed` 中。时间复杂度为 O(n)，其中 `n` 是数组中的元素个数，因为每个元素恰好被处理一次。

**Q-11** **编写一个 JS 程序按升序排序数组（泡泡排序）**

方法 :-

let arr = [4, 7, 5, 3, 8, 9, 6];

// 执行泡泡排序的函数
function bubbleSort(arr) {
  // 外层循环遍历数组
  for (let i = 0; i < arr.length; i++) {
    // 内层循环比较相邻元素
    for (let j = 0; j < arr.length - i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        // 交换元素
        let temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
    }
  }
  return arr;
}
const result = bubbleSort(arr);
console.log(result); // 输出: [3, 4, 5, 6, 7, 8, 9]

**输出：** 排序后的数组是 `[3, 4, 5, 6, 7, 8, 9]`。

**时间复杂度：** *O(n²)*

**解析：** 泡泡排序通过嵌套循环比较并交换相邻元素来排序。时间复杂度为 O(n²)，其中 `n` 是数组的长度。

**Q-12** **编写一个 JS 程序检查数组是否升序排序。**

方法 :-

function isSorted(arr) {
  for (let i = 0; i < arr.length - 1; i++) {
    if (arr[i] > arr[i + 1]) {
      return false;
    }
  }
  return true;
}
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = isSorted(arr);
console.log(result); // 输出: true

**输出：** true

**时间复杂度：** *O(n)*

**解析：** 该函数遍历数组并检查当前元素是否大于后一个元素。如果是，则返回 `false`。时间复杂度为 *O(n)*，其中 `n` 是数组中的元素个数。

**Q-13** **编写一个 JS 程序检查两个数组是否相等。**

方法 :-

function arraysAreEqual(arr1, arr2) {
  if (arr1.length !== arr2.length) {
    return false;
  }
  for (let i = 0; i < arr1.length; i++) {
    if (arr1[i] !== arr2[i]) {
      return false;
    }
  }
  return true;
}
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [1, 2, 3, 4, 5];
const result = arraysAreEqual(arr1, arr2);
console.log(result); // 输出: true

**输出：** true

**时间复杂度：** *O(n)*

**解析：** 该函数首先检查两个数组的长度，如果不同则返回 `false`。然后，它遍历数组并比较对应位置的元素。如果任何元素不同，则返回 `false`。时间复杂度为 *O(n)*。

**Q-14** **编写一个 JS 程序统计数组中每个元素的出现次数。**

方法 :-

let arr = [4, 7, 5, 3, 8, 9, 6];

// 统计每个元素出现次数的函数
function numberOfOccurence(arr) {
  let obj = {};
  for (let i = 0; i < arr.length; i++) {
    // 如果元素已在对象中，增加计数
    if (arr[i] in obj) {
      obj[arr[i]] += 1;
    } else {
      // 如果元素不在对象中，将其计数置为1
      obj[arr[i]] = 1;
    }
  }
  return obj;
}
const result = numberOfOccurence(arr);
console.log(result); // 输出: { '4': 1, '7': 1, '5': 1, '3': 1, '8': 1, '9': 1, '6': 1 }

**输出：** 数组中每个元素的出现次数为 `{ '4': 1, '7': 1, '5': 1, '3': 1, '8': 1, '9': 1, '6': 1 }`。

**时间复杂度：** *O(n)* 其中 *n* 是数组中的元素个数。

**解析：** 该程序遍历一次数组，并使用对象存储每个元素的计数。

**Q-15** **编写一个 JS 程序将数组循环旋转 K 个位置。**

方法 :-

let arr = [1, 2, 3, 4, 5, 6, 7];
let k = 3; // 需要旋转的位置数





## 面试中最常的 50 道 JavaScript 编码题

```javascript
// 将数组向右旋转 k 位的函数
function rotateArray(arr, k) {
  // 获取数组的最后 k 个元素
  let firstSlice = arr.slice(arr.length - k, arr.length);
  // 获取从开始到倒数 k 个元素的元素
  let secondSlice = arr.slice(0, arr.length - k);
  // 合并 firstSlice 和 secondSlice形成旋转后的数组
  let rotatedArray = [...firstSlice, ...secondSlice];
  return rotatedArray;
}
const result = rotateArray(arr, k);
console.log(result); // 输出: [5, 6, 7, 1, 2, 3, 4]
```

**输出：** 旋转后的数组为 `[5, 6, 7, 1, 2, 3, 4]`。

**时间复杂度：** O(n)

**解释：** 该程序将 `arr` 向右旋转 `k` 个位置。函数 `rotateArray` 将数组切分为两部分：`firstSlice` 包含最后 `k` 个元素；`secondSlice` 包含从开始到倒数 `k` 个元素的剩余元素。这些切片被合并以创建旋转后的数组。时间复杂度为 O(n)，其中 n 是数组中的元素数量，因为切片和合并需要线性时间。

### Q-16 编写一个 JS 程序移除数组中的重复元素。（最常问）

方法 :-

```javascript
let arr = [1, 2, 3, 4, 5, 4, 6, 7, 3]; // 包含重复元素的数组
// 移除数组中重复元素的函数
function removeDuplicates(arr) {
  let uniqueArray = [];
  for (let i = 0; i < arr.length; i++) {
    // 检查元素是否已在 uniqueArray 中
    if (uniqueArray.indexOf(arr[i]) === -1) {
      uniqueArray.push(arr[i]); // 将唯一元素加入数组
    }
  }
  return uniqueArray;
}
let result = removeDuplicates(arr);
console.log(result); // 输出: [1, 2, 3, 4, 5, 6, 7]
```

**输出：** 数组 `[1, 2, 3, 4, 5, 4, 6, 7, 3]` 在移除重复元素后为 `[1, 2, 3, 4, 5, 6, 7]`。

**时间复杂度：** O(n²)

**解释：** 该函数遍历数组，检查每个元素是否已存在于 `uniqueArray` 中。如果不存在，则添加该元素。由于在 `for` 循环内部嵌套了 `indexOf`，时间复杂度为 O(n²)。

### Q-17 编写一个 JS 程序返回数组中的重复元素。

方法 :-

```javascript
let arr = [8, 9, 34, 56, 1, 3, 7, 8, 9, 5, 5];
// 查找数组中重复元素的函数
function findDuplicates(arr) {
  let duplicates = [];
  let unique = new Set();
  for (let i = 0; i < arr.length; i++) {
    // 如果元素已在集合中，则它是重复元素
    if (unique.has(arr[i])) {
      // 如果未包含，则将其加入 duplicates 数组
      if (!duplicates.includes(arr[i])) {
        duplicates.push(arr[i]);
      }
    } else {
      // 否则，将元素加入集合
      unique.add(arr[i]);
    }
  }
  return duplicates;
}
const result = findDuplicates(arr);
console.log(result); // 输出: [8, 9, 5]
```

**输出：** 数组中找到的重复元素为 `[8, 9, 5]`。

**时间复杂度：** O(n)

**解释：** 该程序通过遍历每个元素并使用 Set 跟踪唯一元素来找到重复元素。如果在 Set 中发现了元素，它就是重复的，如果不在 duplicates 数组中，则将其加入。时间复杂度为 O(n)，其中 n 是元素的数量。

### Q-18 编写一个 JS 程序找到数组中的最大元素。

方法 :-

```javascript
let arr = [4, 65, 32, 7, 4, 6, 88, 87];
// 找到数组中最大元素的函数
function findLargest(array) {
  // 假设第一个元素是最大的
  let largest = array[0];
  // 遍历数组找到最大值
  for (let i = 1; i < array.length; i++) {
    if (array[i] > largest) {
      largest = array[i];
    }
  }
  return largest;
}
const result = findLargest(arr);
console.log(result); // 输出: 88
```

**输出：** 数组 `[4, 65, 32, 7, 4, 6, 88, 87]` 中的最大元素是 88。

**时间复杂度：** O(n)

**解释：** 该函数遍历数组一次，比较每个元素以找到最大值。最终结果为88，它是数组中的最大元素。时间复杂度为 O(n)，对于此任务非常高效。

### Q-19 编写一个 JS 程序找到数组中的第二大元素。（最常问）

方法 :-

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9]; // 寻找第二大元素的数组
// 找到第二大元素的函数
function secondLargestElement(arr) {
  let largest = -Infinity;
  let secondLargest = -Infinity;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > largest) {
      secondLargest = largest;
      largest = arr[i];
    } else if (arr[i] > secondLargest && arr[i] !== largest) {
      secondLargest = arr[i];
    }
  }
  return secondLargest;
}
const result = secondLargestElement(arr);
console.log(result); // 输出: 8
```

**输出：** 数组 `[1, 2, 3, 4, 5, 6, 7, 8, 9]` 中的第二大元素是 8。

**时间复杂度：** O(n)

**解释：** 该函数遍历数组一次，根据需要更新 `largest` 和 `secondLargest` 变量。最终结果是第二大元素，该过程高效，时间复杂度为 O(n)。

### Q-20 编写一个 JS 程序找到序列中的缺失数字。（最常问）

方法 :-

```javascript
let arr = [1, 2, 3, 5, 6]; // 缺少数字的序列
// 找到序列中缺失数字的函数
function findMissingNumber(arr) {
  let n = arr.length + 1; // 序列的长度
  let totalSum = (n * (n + 1)) / 2; // 前 n 个自然数的和
  let arrSum = arr.reduce((acc, curr) => acc + curr, 0); // 数组元素之
  return totalSum - arrSum; // 差值即为缺失数字
}
const result = findMissingNumber(arr);
console.log(result); // 输出: 4
```

**输出：** 序列中缺失的数字是 4。

### Q-21 编写一个 JS 程序展平嵌套数组。

方法 :-

```javascript
let arr = [[12, [4, 5]], [7, 9], 3];
// 展平嵌套数组的函数
function flattenArray(arr) {
  return arr.reduce((preVal, currentVal) => {
    // 如果当前值是数组，递归展平
    if (Array.isArray(currentVal)) {
      return preVal.concat(flattenArray(currentVal));
    }
    return preVal.concat(currentVal);
  }, []);
}
```





## 面试中频率最高的 50 道 JavaScript 编码题

```javascript
else {
  // 否则，将当前值推入结果数组
  preVal.push(currentVal);
}
return preVal;
}, []);
const result = flattenArray(arr);
console.log(result); // 输出: [12, 4, 5, 7, 3]
```

**输出：** 展平数组为 `[12, 4, 5, 7, 3]`。

**时间复杂度：** *O(n)*

**解释：** 该程序通过 `reduce` 方法递归检查每个元素，并将展平后的值累加到单个数组中。时间复杂度为 O(n)，其中 n 是嵌套数组中的元素总数。

方法 2：

```javascript
let arr = [[12, [4, 5]], [7, 9], 3];
// 使用 flat() 方法展平嵌套数组
function flattenArray(arr) {
  return arr.flat(Infinity); // 展平到任意深度
}
const result = flattenArray(arr);
console.log(result); // 输出: [12, 4, 5, 7, 3]
```

**输出：** 展平数组为 `[12, 4, 5, 7, 3]`。

**时间复杂度：** *O(n)*

**解释：** 该程序使用内置函数 `flat()` 展平嵌套数组。通过传递 `Infinity` 作为参数。时间复杂度为 O(n)，其中 n 是数组中的元素总数。

### Q-22 编写一个 JS 程序合并两个排序数组（高频题）

方法：

```javascript
function mergeSortedArrays(arr1, arr2) {
  let i = 0;
  let j = 0;
  let sortedArr = [];
  // 比较两个数组的元素
  while (i < arr1.length && j < arr2.length) {
    if (arr1[i] < arr2[j]) {
      sortedArr.push(arr1[i]);
      i++;
    } else {
      sortedArr.push(arr2[j]);
      j++;
    }
  }
  // 添加 arr1 中的剩余元素
  while (i < arr1.length) {
    sortedArr.push(arr1[i]);
    i++;
  }
  // 添加 arr2 中的剩余元素
  while (j < arr2.length) {
    sortedArr.push(arr2[j]);
    j++;
  }
  return sortedArr;
}
const arr1 = [1, 3, 5, 7];
const arr2 = [2, 4, 6, 8];
const result = mergeSortedArrays(arr1, arr2);
console.log(result); // 输出: [1, 2, 3, 4, 5, 6, 7, 8]
```

**输出：** 合并后的数组为 `[1, 2, 3, 4, 5, 6, 7, 8]`。

**时间复杂度：** *O(n + m)*

**解释：** 该程序通过比较两个数组的元素并将较小的元素添加到结果数组。如果一个数组耗尽，则添加另一个数组的剩余元素。时间复杂度为 O(n+m)，其中 n 和 m 是两个数组的长度。

### Q-23 编写一个 JS 程序查找数组中指定和的所有数字对

方法：

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9]; // 检查的数组
let pairValue = 10; // 目标和
// 查找和等于给定值的对
function findPairs(arr, pairValue) {
  let pairs = []; // 用于存储结果的数组
  let seen = new Set(); // 用于存储已出现元素的
  for (let i = 0; i < arr.length; i++) {
    const complement = pairValue - arr[i]; // 计算补数
    if (seen.has(complement)) {
      pairs.push([complement, arr[i]]); // 如果补数存在，则添加对
    }
    seen.add(arr[i]); // 将当前元素添加到集合
  }
  return pairs;
}
const result = findPairs(arr, pairValue);
console.log(result); // 输出: [7, 3], [6, 4], [5, 5], [4, 6], [3, 7]
```
（注：根据逻辑，提供的输出 `[7, 3], [6, 4], [5, 5], [4, 6], [3, 7]` 表明了一种特定的迭代或集合行为）。

**输出：** 数组 `[1, 2, 3, 4, 5, 6, 7, 8, 9]` 中和为 `10` 的对为 `[7, 3], [6, 4], [5, 5], [4, 6], [3, 7]`。

**时间复杂度：** *O(n)*

**解释：** 该函数遍历数组并维护一个已出现元素的集合。对于每个元素，它检查其补数之前是否出现过。如果是，则将该对添加到结果中。由于对数组进行了单循环，时间复杂度为 O(n)。

### Q-24 编写一个 JS 程序检查一个数组是否是另一个的子集

方法：

```javascript
let arr1 = [1, 2, 3, 4, 5, 6, 7, 8, 9]; // 超集
let arr2 = [4, 5, 6]; // 子集
// 检查 arr2 是否是 arr1 的子集的函数
function isSubset(arr1, arr2) {
  return arr2.every(ele => arr1.includes(ele));
}
const result = isSubset(arr1, arr2);
console.log(result); // 输出: true
```

**输出：** `true`（因为 `arr2` 中的所有元素都存在于 `arr1` 中）。

**时间复杂度：** *O(n * m)*

**解释：** 函数使用 `every` 方法检查 `arr2` 中的每个元素是否包含在 `arr1` 中。该检查使用了 `includes` 方法。时间复杂度为 O(n * m)，其中 n 是 `arr1` 的长度，m 是 `arr2` 的长度。

### Q-25 编写一个 JS 程序查找两个数组的交集

方法：

```javascript
let arr1 = [1, 2, 3, 4, 5]; // 第一个数组
let arr2 = [3, 4, 5, 6, 7]; // 第二个数组
// 两个数组交集的函数
function intersection(arr1, arr2) {
  return arr1.filter(ele => arr2.includes(ele));
}
const result = intersection(arr1, arr2);
console.log(result); // 输出: [3, 4, 5]
```

**输出：** 数组 `[1, 2, 3, 4, 5]` 和 `[3, 4, 5, 6, 7]` 的交集为 `[3, 4, 5]`。

**时间复杂度：** *O(n * m)*

**解释：** 函数过滤 `arr1` 中存在于 `arr2` 中的元素。该检查使用了 `includes` 方法，时间复杂度为 O(n * m)，其中 n 是 `arr1` 的长度，m 是 `arr2` 的长度。

### Q-26 编写一个 JS 程序返回在 arr1 中但不在 arr2 中的元素

方法：

```javascript
let arr1 = [1, 2, 3, 4, 5]; // 第一个数组
let arr2 = [3, 4, 5, 6, 7]; // 第二个数组
// 查找 arr1 中不在 arr2 中的元素的函数
function elementsNotInSecondArray(arr1, arr2) {
  return arr1.filter(ele => !arr2.includes(ele)); // 过滤不在 arr2 中的元素
}
const result = elementsNotInSecondArray(arr1, arr2);
console.log(result); // 输出: [1, 2]
```

**输出：** 元素 `[1, 2]` 存在于 `arr1` 中但不在 `arr2` 中。

**时间复杂度：** *O(n)*

**解释：** 该函数 `elementsNotInSecondArray` 过滤 `arr1` 的元素，返回不在 `arr2` 中找到元素。时间复杂度为 O(n)，其中 n 是 `arr1` 中的元素个数。





## 面试高频 50 JavaScript 编码题

let result = reverseStr(str);
console.log(result); // 输出: "elpmaxe"

**输出：** 打印反转后的字符串为 "elpmaxe"。

**时间复杂度：** *O(n)*

**解释：** 该程序通过遍历每个字符并将其添加到新字符串的前面来反转给定字符串。时间复杂度为 (O(n)，其中 (n) 是字符串的长度。

方法 2:-

```javascript
let str = "hello";
function reverseStr(str) {
  return str.split("").reverse().join("");
}
let result = reverseStr(str);
console.log(result); // 输出: "olleh"
```

**输出：** 打印反转后的字符串为 "olleh"。

**时间复杂度：** *O(n)*

**解释：** 该程序通过遍历每个字符并将其添加到新字符串的前面来反转给定字符串。时间复杂度为 (O(n))，其中 (n) 是字符串的长度。

### Q-28 编写一个 JS 程序反转字符串中的单词。

方法 :-

```javascript
let str = "my name is rahul chaurasia"; // 需要反转单词的字符串
// 反转字符串中单词的函数
function reverseWordsInString(str) {
  let words = str.split(" ").reverse().join(" "); 分割、反转并合并单词
  return words;
}
let result = reverseWordsInString(str);
console.log(result); // 输出: "chaurasia rahul is name my"
```

**输出：** 字符串 "my name is rahul chaurasia" 中的单词反转后为 "chaurasia rahul is name my"。

**时间复杂度：** *O(n)*

**解释：** 该函数将字符串拆分为单词数组，反转数组，然后将单词重新组合字符串。时间复杂度为 *O(n)*，其中 n 是字符串中字符的数量。

## Q-29 编写一个 JS 程序找到字符串中最长长的单词。

方法 :-

```javascript
let str = "My name is Rahul Chaurasia";
let words = str.split(" ");
function longestWord(words) {
  let longestWord = "";
  for (let i = 0; i < words.length; i++) {
    if (words[i].length > longestWord.length) {
      longestWord = words[i];
    }
  }
  return longestWord;
}
let result = longestWord(words);
console.log(result);
```

**输出：** 最长的单词是 "Chaurasia"。

**时间复杂度：** *O(n)*

**解释：** 该程序通过将字符串拆分为单词，然后遍历单词找到最长的一个。时间复杂度为 O(n)，其中 n 是字符串中单词的数量。

### Q-30 编写一个 JS 程序检查字符串是否为回文。

方法 :-

```javascript
let str = "racecar";
// 检查是否为回文的函数
function isPalindrome(str) {
  let reversed = str.split("").reverse().join(""); // 反转字符串
  return str === reversed; 
}
let result = isPalindrome(str);
console.log(result); // 输出: true
```

**输出：** 字符串 "racecar" 是回文：true。

**时间复杂度：** *O(n)*

**解释：** 该程序通过反转字符串并与原始字符串比较来检查是否为回文。时间复杂度为 O(n)，其中 n 是字符串的长度。

### Q-31 编写一个 JS 程序检查两个字符串是否为异位词。

方法 :-

```javascript
let str1 = "listen";
let str2 = "silent";
// 检查是否异位词的函数
function isAnagram(str1, str2) {
  let sorted1 = str1.split("").sort().join("");
  let sorted2 = str2.split("").sort().join("");
  return sorted1 === sorted2;
}
let result = isAnagram(str1, str2);
console.log(result); // 输出: true
```

**输出：** 异位词：true。

**时间复杂度：** *O(n log n)*

**解释：** 该程序通过对字符串进行排序并比较来检查它们是否为异位词。由于使用了排序，时间复杂度取决于排序算法。

### Q-32 编写一个 JS 程序返回字符串中未重复的字符。

方法 :-

```javascript
let str = "algorithm";
// 返回未重复字符的函数
function firstRepeated(str) {
  for (let i = 0; i < str.length; i++) {
    if (str.indexOf(str[i]) === str.lastIndexOf(str[i])) {
      return str[i];
    }
  }
  return null; // 如果没有未重复字符返回 null
}
let result = firstRepeated(str);
console.log(result); // 输出: "g"
```

**输出：** "algorithm" 中未重复的字符是 "g"。

**时间复杂度：** *O(n^2)*

**解释：** 该函数使用 `indexOf` 和 `lastIndexOf` 查找出现一次的字符。嵌套的查找导致了平方复杂度。

### Q-33 编写一个 JS 程序返回给定字符串中元音的数量。

方法 :-

```javascript
let str = "Rajat";
// 统计给定字符串元音数量的函数
function countVowels(str) {
  const vowels = ["a", "e", "i", "o", "u"];
  let count = 0; // 初始化计数器
  for (let char of str.toLowerCase()) { // 遍历字符串的每个字符
    if (vowels.includes(char)) { // 如果是元音则加1
      count++;
    }
  }
  return count; // 返回元音总数
}
let result = countVowels(str);
console.log(result); // 输出: 2
```

**输出：** "Rajat" 中有 2 个元音。

**时间复杂度：** *O(n)*

**解释：** 该程序通过遍历字符串并检查字符是否在 `vowels` 数组中来统计元音数量。

### Q-34 编写一个 JS 程序移除字符串中的所有空格字符。

方法 :-

```javascript
function removeWhitespace(str) {
  let result = "";
  for (let i = 0; i < str.length; i++) {
    if (str[i] !== " ") { // 检查字符是否不是空格
      result += str[i]; // 将非空格字符添加到结果中
    }
  }
  return result;
}
```





面试中最常见的 50 个 JavaScript 编码题

`const inputString = " Hello World! How are you?";`
`const result = removeWhitespace(inputString);`
`console.log(result);`

**输出**: `"HelloWorld!Howareyou?"`

**时间复杂度**: *O(n)*，其中 *n* 是输入字符串的长度。程序精确地遍历字符串中的每个字符一次。

**解释**: 程序遍历字符串中的每个字符，并检查它是否不是空格。如果该字符不是空格，则将其添加到 `result` 字符串中。

### Q-35 编写一个 JS 程序统计字符串中某个字符出现的次数。（最常问）

方法:-

`let str = "Chaurasia"; // 待搜索的字符串`
`let char = "a"; // 要计数的字符`
`// 用于查找字符串中某个字符出现次数的函数`
`function numberOfOccurrences(str, char) {`
`  let count = 0;`
`  for (let i = 0; i < str.length; i++) {`
`    if (str[i] === char) {`
`      count++;`
`    }`
`  }`
`  return count;`
`}`
`let result = numberOfOccurrences(str, char);`
`console.log(result); // 输出: 3`

**输出**: 字符串 "Chaurasia" 中 'a' 出现的次数为 `3`。

**时间复杂度**: *O(n)*

**解释**: 该函数遍历字符串并统计指定字符出现的次数。时间复杂度为 *O(n)*，其中 *n* 是字符串的长度。变量 `char` 用于指定要计数的字符。

### Q-36 编写一个 JS 程序将字符串中每个单词的首字母转换为大写字母。

方法:-

`let str = "i am a frontend developer"; // 原始字符串`
`// 将每个单词的首字母大写化的函数`
`function capitalizeFirstLetter(str) {`
`  return str`
`    .split(" ") // 将字符串分成单词`
`    .map((word) => word.charAt(0).toUpperCase() + word.slice(1)) // 首字母大写`
`    .join(" "); // 将单词重新组合字符串`
`}`
`const result = capitalizeFirstLetter(str);`
`console.log(result); // 输出: "I Am A Frontend Developer"`

**输出**: 字符串 `"i am a frontend developer"` 被转换为 `"I Am A Frontend Developer"`。

**时间复杂度**: *O(n)*

**解释**: 该函数将字符串 `"i am a frontend developer"` 分分成单词数组，将每个单词的首字母大写，然后将单词重新组合成单个字符串。结果是 `"I Am A Frontend Developer"`。时间复杂度为 *O(n)*，其中 *n* 是字符串中的字符数。

## Section 4- 对象

### Q-37 编写一个 JS 程序创建一个具有动态键以及一个使用 `this` 返回字符串方法的对象。

方法:-

`let key = "profession";`
`let user = {`
`  name: "Alice",`
`  age: 28,`
`  [key]: "Developer",`
`  getDetails: function() {`
`    return \`User: ${this.name}, Profession: ${this.profession}\`;;`
`  },`
`};`
`console.log(user.getDetails());`

**输出**: `User: Alice, Profession: Developer`

**时间复杂度**: *O(1)*

**解释**: 此题测试了对对象中动态属性名的知识，以及在对象方法中使用 `this` 引用对象属性。

### Q-38 编写一个 JS 程序根据条件更新对象属性并添加嵌套对象。

方法:-

`let user = {`
`  name: "Alice",`
`  age: 28,`
`  isDeveloper: true,`
`};`
`// 条件更新属性`
`if (user.age > 25) {`
`  user.status = "Senior";`
`}`
`// 添加嵌套对象`
`user.address = {`
`  city: "New York",`
`  zip: 10001,`
`};`
`console.log(user);`

**输出**: `{ name: 'Alice', age: 28, isDeveloper: true, status: 'Senior', address: { city: 'New York', zip: 10001 } }`

**时间复杂度**: *O(1)*

**解释**: 此问题展示了如何条件地更新和嵌套对象。

### Q-39 编写一个 JS 程序删除深度嵌套属性并检查是否存在。

方法:-

`let user = {`
`  name: "Alice",`
`  age: 28,`
`  details: {`
`    city: "New York",`
`    zip: 10001,`
`  },`
`};`
`// 删除嵌套属性`
`delete user.details.zip;`
`// 检查是否存在`
`console.log("zip" in user.details);`

**输出**: `false`

### Q-40 编写一个 JS 程序遍历对象并计算值。

方法:-

`let employeeSalaries = {`
`  Alice: 50000,`
`  Bob: 60000,`
`  Carol: 70000,`
`};`
`let totalSalary = 0;`
`let count = 0;`
`for (let key in employeeSalaries) {`
`  totalSalary += employeeSalaries[key];`
`  count++;`
`}`
`let averageSalary = totalSalary / count;`
`console.log(`Total Salary: ${totalSalary}, Average Salary: ${averageSalary}`);`

**输出**: `Total Salary: 180000, Average Salary: 60000`

### Q-41 编写一个 JS 程序合并对象并处理重复键。

方法:-

`let user1 = {`
`  name: "Alice",`
`  age: 28,`
`  profession: "Developer",`
`};`
`let user2 = {`
`  age: 30,`
`  city: "New York",`
`  profession: "Senior Developer",`
`};`
`// 合并对象，冲突时以 user2 优先`
`let mergedUser = {...user1, ...user2};`
`console.log(mergedUser);`

**输出**: `{ name: 'Alice', age: 30, profession: 'Senior Developer', city: 'New York' }`

### Q-42 编写一个 JS 程序查找对象的唯一键。

方法:-

`let obj = {`
`  name: "Rahul",`
`  name: "Rajat", // 这会覆盖之前的 'name' 键`
`  age: 27,`
`};`
`function uniqueKeys(obj) {`
`  return new Set(Object.keys(obj));`
`}`
`let result = uniqueKeys(obj);`
`console.log(result); // { 'name', 'age' }`





## 面试中最常见的 50 道 JavaScript 编码题

```javascript
const obj = {
  "b": 20,
  "c": {
    "d": 30,
    "e": {
      "f": 40,
      "g": 50,
    },
  },
  "h": 60,
};

function sumValues(obj) {
  let sum = 0;
  function recursiveSum(o) {
    for (let key in o) {
      if (typeof o[key] === "object" && o[key] !== null) {
        recursiveSum(o[key]); // 递归处理嵌套对象
      } else if (typeof o[key] === "number") {
        sum += o[key]; // 将数值加到和中
      }
    }
  }
  recursiveSum(obj);
  return sum;
}
let result = sumValues(obj);
console.log(result); // 输出: 210
```

**输出**: `210`

**时间复杂度**: *O(n)*

**解释**: 该程序计算对象中所有数值的和，包括嵌套对象中的数值。它使用递归函数来遍历该对象及其嵌套对象。

## 第 5 节-Promises 和 Async Await

### Q-44 编写一个 JS 程序实现 Promise 并处理它的解析。（最常问）

方法:-

```javascript
function handlePromise() {
  const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Promise resolved successfully");
    }, 1000); // 模拟 1 秒延迟
  });
  promise
    .then((result) => {
      console.log(result); // 打印解析后的值
    })
    .catch((error) => {
      console.error(error); // 处理任何潜在的拒绝（此处未使用）
    });
}
handlePromise();
```

**输出**: `Promise resolved successfully`

**时间复杂度**: 对于处理处理本身为 *O(1)*，但由于 `setTimeout` 有 1 秒的异步延迟。

**解释**: 该程序演示了 JavaScript 中 Promise 的创建和解析。Promise 在 1 秒后带有成功消息解析，该消息通过 `.then()` 方法打印到控制台。包含了 `.catch()` 方法以处理任何潜在错误，尽管在此示例中没有触发它。

### Q-45 编写一个 JS 程序，使用 Promise.race、Promise.all 和 Promise.allSettled 演示 Promise 处理。（最常问）

方法:-

```javascript
function handlePromise() {
  let promise1 = new Promise((resolve) => {
    setTimeout(() => {
      resolve("promise1 resolved");
    }, 1000);
  });
  let promise2 = new Promise((resolve) => {
    setTimeout(() => {
      resolve("promise2 resolved");
    }, 500);
  });
  let promise3 = new Promise((resolve) => {
    setTimeout(() => {
      resolve("promise3 resolved");
    }, 1500);
  });

  // 使用 Promise.race: 返回执行 promise 的结果
  Promise.race([promise1, promise2, promise3])
    .then((result) => {
      console.log("Promise.race result:", result);
    })
    .catch((error) => {
      console.log("Promise.race caught error:", error);
    });

  // 使用 Promise.all: 等待所有 promise 解析
  Promise.all([promise1, promise2, promise3])
    .then((results) => {
      console.log("Promise.all results:", results);
    })
    .catch((error) => {
      console.log("Promise.all caught error:", error);
    });

  // 将一个拒绝的 promise 添加到 Promise.allSettled
  let promise4 = new Promise((resolve, reject) => {
    setTimeout(() => {
      reject("promise4 encountered an error");
    }, 700);
  });

  // 使用 Promise.allSettled: 无论是否解析或拒绝，都返回所有结果
  Promise.allSettled([promise1, promise2, promise3, promise4])
    .then((results) => {
      console.log("Promise.allSettled results:", results);
    });
}
// 注意：此处原文代码逻辑在结尾处有些错乱，已按要求翻译结构
// 这里的 Promise 链式调用在原文中是分开的
```
*(注：由于原文文本中 Q-45 的结尾代码存在排版/逻辑混乱（多个 `.then` 悬挂在函数定义外），我严格遵循“不要漏掉任何一行”的原则进行了对应位置翻译。)*

**输出**:
Promise.race result: promise2
Promise.all results: ["promise1 resolved", "promise2 resolved", "promise3 resolved"]
Promise.allSettled results: [
  { status: "fulfilled", value: "promise1 resolved" },
  { status: "fulfilled", value: "promise2 resolved" },
  { status: "fulfilled", value: "promise3 resolved" },
  { status: "rejected", reason: "promise4 encountered an error" }
]
*(由于原文 Q-45 的代码块结构异常，以下为基于原文顺序的翻译：)*

### Q-46 编写一个 JS 程序，在 JavaScript 示例中解释 Async/Await。

方法:-

```javascript
async function fetchData() {
  try {
    const response = await new Promise((resolve) => {
      setTimeout(() => {
        resolve("Data fetched successfully!");
      }, 1000);
    });
    console.log(response);
  } catch (error) {
    console.log("Error occurred:", error);
  }
}
fetchData();
```

**输出**: `Data fetched successfully!`

**时间复杂度**: *O(1)*（不考虑延迟持续时间）。

**解释**: 此示例演示了如何使用 `async/await` 处理异步操作。`fetchData` 函数等待 Promise 解析并打印结果。如果发生错误，它会被 `catch` 块捕获。

### Q-47 编写一个 JS 程序，通过 API 演示 Async/Await。（最常问）

方法:-

```javascript
async function fetchTodoItem() {
  try {
    // 等待 fetch 请求完成
    const response = await fetch("https://jsonplaceholder.typicode.com/todos/1");
    // 等待响应转换为 JSON
    const data = await response.json();
    // 打印 JSON 数据
    console.log(data);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}
fetchTodoItem();
```

**输出**:
```json
{
  "userId": 1,
  "id": 1,
  "title": "delectus aut autem",
  "completed": false
}
```

**时间复杂度**: 等待操作为 *O(1)*。复杂度受网络延迟和服务器响应时间的影响。

**解释**:
- 第一个 await：`await fetch(...)` 等待 HTTP 请求完成并接收 `Response` 对象。
- 第二个 await：`await response.json()` 等待 `Response` 对象转换为 JSON 格式。
这两个 `await` 调用对于顺序处理异步操作是必要的。

## 第 6 节-其他问题

 Q-48 编写一个 JS 程序，通过 JavaScript 示例解释 call、apply 和 bind 方法。

```javascript
const personA = {
  firstName: "Alice",
  lastName: "Johnson",
  getFullName: function(city, country) {
    return `${this.firstName} ${this.lastName} ${city} ${country}`;
  },
};
```





## 面试中最常见的50道 JavaScript 编码题

```javascript
const personB = {
  firstName: "Bob",
  lastName: "Smith",
};

// Using call
console.log(personA.getFullName.call(personB, "Los Angeles", "USA"));

// Using apply
console.log(personA.getFullName.apply(personB, ["Los Angeles", "USA"]));

// Using bind
const boundGetFullName = personA.getFullName.bind(personB, "Los Angeles", "USA");
console.log(boundGetFullName());
```

**输出**:
`Bob Smith Los Angeles USA`
`Bob Smith Los Angeles USA`
`Bob Smith Los Angeles USA`

**时间复杂度**: *O(1)*。这些操作是常数时间，因为它们涉及上下文切换和参数传递，不依赖于输入规模的大小。

**解释**:
1. **call 方法**：调用 `personA` 的 `getFullName` 方法，并将 `this` 设置为 `personB`，同时传入城市和国家的单独参数。
2. **apply 方法**：与 `call` 类似，但参数以数组的形式提供。
3. **bind 方法**：创建一个新函数，其中 `this` 绑定到 `personB` 并带有预定义的参数。然后调用该新函数。

### Q-49 编写一个 JS 程序解释 JavaScript 中的高阶函数。

方法:-
1. **将函数作为参数**

```javascript
// 将数字翻倍的函数
function double(num) {
  return num * 2;
}

// 将函数应用到数组每个元素上的高阶函数
function applyFunction(arr, func) {
  return arr.map(func);
}

const numbers = [2, 4, 6, 7, 8];
const doubledNumbers = applyFunction(numbers, double);
console.log(doubledNumbers);
```

**输出**: `[4, 8, 12, 14, 16]`

**时间复杂度**: *O(n)*，其中 *n* 是数组中元素的数量。该函数对每个元素应用了 `double` 函数。

**解释**:
- **double(num)**：一个简单的函数，将其输入值翻倍。
- **applyFunction(arr, func)**：一个高阶函数，接收一个数组和一个函数作为参数，并使用 `map` 将函数应用到数组的每个元素上。

2. **返回另一个函数**

```javascript
// 返回另一个函数以向其参数添加一个数字
function adder(x) {
  return function(y) {
    return x + y;
  };
}

const add = adder(11);
console.log(add(5));
```

**输出**: `16`

**时间复杂度**: 创建和调用函数的时间均为 *O(1)*，因为它们是常数时间复杂度的简单操作。

**解释**:
- **adder(x)**：一个返回另一个函数的。返回的函数接收一个参数，并将其与值 `x` 相加。
- **add**：通过调用 `adder(11)` 创建，结果是一个在其参数基础上加11的函数。

## Q-50 编写一个 JS 程序通过示例解释 JavaScript 中的闭包。（最常）

方法:-
```javascript
function multiplier(factor) {
  // 'factor' 被内部函数捕获
  return function(number) {
    // 内部函数将 'number' 乘以捕获的 'factor'
    return factor * number;
  };
}

const triple = multiplier(3); // multiplier 返回一个 factor 设置为 3 的函数
console.log(triple(7)); // 输出: 21，内部函数将 7 乘以 3
```

**输出**: `21`

**时间复杂度**: *O(1)*，因为内部函数内部的操作是常数时间。

**解释**: 这个示例演示了 JavaScript 中闭包是如何工作的。内部函数可以访问其外部词法作用域中的 `factor` 变量，即使在 `multiplier` 执行完毕后也是。当你调用 `triple(7)` 时，它将 `7` 乘以 `3`（即被捕获的 `factor` 值）。

