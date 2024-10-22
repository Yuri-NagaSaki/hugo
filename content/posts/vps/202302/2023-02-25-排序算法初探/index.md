---
title: "排序算法初探"
date: "2023-02-25"
categories: 
  - "前端"
---

## 冒泡排序

冒泡排序是一种简单的排序算法。它重复地走访过要排序的数列，一次比较两个元素，如果它们的顺序错误就把它们交换过来。走访数列的工作是重复地进行直到没有再需要交换，也就是说该数列已经排序完成。这个算法的名字由来是因为越小的元素会经由交换慢慢“浮”到数列的顶端。

冒泡排序算法的运作如下：

1. 比较相邻的元素。如果第一个比第二个大，就交换他们两个。
2. 对每一对相邻元素作同样的工作，从开始第一对到结尾的最后一对。这步做完后，最后的元素会是最大的数。
3. 针对所有的元素重复以上的步骤，除了最后一个。
4. 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。  
    

冒泡排序平均时间复杂度 O(n^2)，在最好情况下，即一次排完時复杂度为 O(n)，在最坏情况下复杂度为 O(n^2)。

### 经典冒泡算法

经典冒泡算法：通过双层循环实现排序，外层循环表示当前是第几轮排序，内层循环表示当前轮的第几次排序，通过两两比较交换位置完成排序。

```
function bubbleSort(nums) {
  const len = nums.length
  for (let i = 0; i < len; i++) {
    for (let j = 0; j < len - 1 - i; j++) {
      if (nums[j] > nums[j + 1]) {
        ;[nums[j], nums[j + 1]] = [nums[j + 1], nums[j]] // 交换位置
      }
    }
  }
  return nums
}
```

### 改进冒泡算法

改进冒泡算法：设置一标志性变量 pos，用于记录每轮排序中最后一次进行交换的位置。由于 pos 位置之后的记录均已交换到位，故在进行下一轮排序时只要扫描到 pos 位置即可。

```
function bubbleSort(nums) {
  const len = nums.length
  let i = len - 1
  while (i > 0) {
    let pos = 0
    for (let j = 0; j < i; j++) {
      if (nums[j] > nums[j + 1]) {
        pos = j // 记录交换時的位置
        ;[nums[j], nums[j + 1]] = [nums[j + 1], nums[j]] // 交换位置
      }
    }
    i = pos
  }
  return nums
}
```

### 终极冒泡算法

终极冒泡算法：传统冒泡排序中每一轮排序操作只能找到一个最大值或最小值，可以在每趟排序中进行正向和反向两遍冒泡方法一次得到两个最终值（最大者和最小者），从而使排序轮数几乎减少了一半。

```
function bubbleSort(nums) {
  let low = 0
  let high = nums.length - 1
  let i
  while (low < high) {
    // 正向排序，找出最大值
    for (i = low; i < high; ++i) {
      if (nums[i] > nums[i + 1]) {
        ;[nums[i], nums[i + 1]] = [nums[i + 1], nums[i]] // 交换位置
      }
    }
    --high // 前移一位

    // 反向排序，找出最小值
    for (i = high; i > low; --i) {
      if (nums[i] < nums[i - 1]) {
        ;[nums[i], nums[i - 1]] = [nums[i - 1], nums[i]] // 交换位置
      }
    }
    ++low // 后移一位
  }
  return nums
}
```

## 选择排序

选择排序是一种简单直观的排序算法。首先在未排序序列中找到最小（大）元素，存放到排序序列的起始位置，然后，再从剩余未排序元素中继续寻找最小（大）元素，然后放到已排序序列的末尾。以此类推，直到所有元素均排序完毕。

选择排序算法的运作如下：

1. 初始状态：无序区为 R\[1..n\]，有序区为空。
2. 第 i 轮排序开始时，当前有序区和无序区分别为 R\[1..i-1\] 和 R\[i..n\]。然后从当前无序区中选出最小值，将它与无序区的第一个值交换，使得新增一位有序区和减少一位无序区。
3. n-1 轮排序结束，数组全部变为有序区，从而完成排序。  
    

选择排序的主要优点与数据移动有关。如果某个元素位于正确的最终位置上，则它不会被移动。选择排序每次交换一对元素，它们当中至少有一个将被移到其最终位置上，因此对 n 个元素的表进行排序总共进行至多 n-1 次交换。在所有的完全依靠交换去移动元素的排序方法中，选择排序属于非常好的一种。

选择排序平均时间复杂度稳定在 O(n^2)。

### 经典选择算法

经典选择算法：将数列分为有序区和无序区两部分，在每轮循环中从无序区选择一个最小值并入有序区，新增一位有序区同时减少一位无序区，n - 1 轮排序后全部变为有序区，从而完成排序。

```
function selectionSort(nums) {
  const len = nums.length
  let min = 0
  for (let i = 0; i < len - 1; i++) {
    min = i
    for (let j = i + 1; j < len; j++) {
      if (nums[min] > nums[j]) {
        min = j // 保存最小值的索引
      }
    }
    ;[nums[i], nums[min]] = [nums[min], nums[i]] // 交换位置
  }
  return nums
}
```

## 插入排序

是一种简单的排序算法。它的工作原理是通过构建有序序列，对于未排序数据，在已排序序列中从后向前扫描，找到相应位置并插入。插入排序在实现上，通常采用 in-place 排序，因而在从后向前扫描过程中，需要反复把已排序元素逐步向后挪位，为最新元素提供插入空间。

插入排序算法的运作如下：

1. 从第一个元素开始，该元素可以认为已经被排序。
2. 取出下一个元素，在已经排序的元素序列中从后向前扫描，如果该元素大于新元素，将该元素移到下一位置。
3. 重复步骤 2，直到找到已排序的元素小于或者等于新元素的位置，将新元素插入到该位置后。
4. 重复步骤 2~3，直到完成排序。  
    

插入排序平均时间复杂度 O(n^2)，在最好情况下复杂度为 O(n)，在最坏情况下复杂度为 O(n^2)。

### 经典插入算法

经典选择算法：将数列分为有序区和无序区两部分，在每轮循环中从无序区选择一个最小值并入有序区，新增一位有序区同时减少一位无序区，n - 1 轮排序后全部变为有序区，从而完成排序。

```
function insertionSort(nums) {
  const len = nums.length
  for (let i = 1; i < len; i++) {
    let k = nums[i]
    let j = i - 1
    while (j >= 0 && nums[j].num > k.num) {
      nums[j + 1] = num[j]
      j--
    }
    nums[j + 1] = k
  }
  return nums
}
```

### 二分插入算法

二分插入算法：查找插入位置时使用二分查找的方式，在插入值之前，先在有序区中找到待插入值需要比较的左边界，在数据长度较大时，可以有效减少每轮排序中的查找插入位置的次数。

```
function insertionSort(nums) {
  const len = nums.length
  for (let i = 1; i < len; i++) {
    let k = nums[i]
    let left = 0
    let right = i - 1
    while (left <= right) {
      let middle = ~~((left + right) / 2)
      if (k < nums[middle]) {
        right = middle - 1
      } else {
        left = middle + 1
      }
    }
    for (let j = i - 1; j >= left; j--) {
      nums[j + 1] = nums[j]
    }
    nums[left] = k
  }
  return nums
}
```

## 归并排序

归并排序是创建在归并操作上的一种有效的排序算法。归并操作也叫归并算法，指的是将两个已经排序的序列合并成一个序列的操作。归并排序时间复杂度为 O(nlogn)。该算法是采用分治法的一个非常典型的应用，且各层分治递归可以同时进行。

归并排序算法的运作如下：

1. 将长度为 n 的序列每相邻两个数字进行归并操作，形成 n/2 个序列，排序后每个序列包含二或一个元素。
2. 若此时序列数不是 1 个则将上述序列再次归并，形成 n/4 个序列，每个序列包含三或四个元素。
3. 重复步骤 2，直到所有元素排序完毕，即序列数为 1，即完成排序。
4. 归并排序平均时间复杂度稳定在 O(nlogn)。  
    

### 经典归并算法

经典归并算法：将数列分为两个子序列，如果子序列长度不为一，再将子序列细分，直至子序列长度为一。递归比较两个子序列并排序后，再相互组合成有序数列，最终完成排序。

```
function mergeSort(nums) {
  const len = nums.length
  if (len <= 1) return nums
  let middle = ~~(len / 2)
  let left = nums.slice(0, middle)
  let right = nums.slice(middle)
  return merge(mergeSort(left), mergeSort(right))
}
function merge(left, right) {
  const result = []
  while (left.length && right.length) {
    if (left[0] < right[0]) {
      result.push(left.shift())
    } else {
      result.push(right.shift())
    }
  }
  return result.concat(left, right)
}
```
