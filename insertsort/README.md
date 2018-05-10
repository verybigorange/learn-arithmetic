## 插入排序 ##
### 算法复杂度：O(n^2)

这种排序方式理论是比选择排序快。首先从数组的第二个元素开始，让元素依次和它前面的元素做比较，如果满足条件则与它前面元素交换位置，直到不满足条件（此时该元素到达了合适的位置）。

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