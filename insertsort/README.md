## 插入排序 ##
### 算法复杂度：O(n^2)

由于循环有额外的限制条件，不满足条件会跳过当前循环，所以理论上这种排序方式是比选择排序快。如果传入数组越有序，这种算法的复杂度将越接近于O(n)的效率。
### 未改进的插入排序算法

首先从数组的第二个元素开始，让元素依次和它前面的元素做比较，如果满足条件则与它前面元素交换位置，直到不满足条件（此时该元素到达了合适的位置）。

```js
     //从小到大
    function insertsort(arr) {
            for (let i = 1; i < arr.length; i++) {
                for (let j = i; j > 0 && arr[j] < arr[j - 1]; j--) {
                    [arr[j], arr[j - 1]] = [arr[j - 1], arr[j]]
                }
            }
            return arr
    }
```
### 改进后的插入排序算法

改进的算法避免每次循环交换位置（多次赋值），将当前元素与它前面的元素依次做比较，如果满足条件，将前面的元素往后移，当j为0或者不满足条件时，j就是当前元素的最终位置。

```js
    //从小到大
    function insertsort(arr) {
            for (let i = 1; i < arr.length; i++) {
                const ele = arr[i]; //当前元素
                let j; //当前元素应该插入的位置
                for (j = i; j > 0 && ele < arr[j - 1]; j--) {
                    arr[j] = arr[j - 1];
                }
                arr[j] = ele;
            }
            return arr
    }
```