## 冒泡排序 ##

### 算法复杂度：O(n^2)

冒泡排序适合数据规模小，效率比较低，用的相对比少，属于入门级的算法。

从小到大：从一个元素开始与它后面的元素依次作比较，如果遇到自己小的元素则交换位置。


```js
    //从小到大
    function sort(arr) {
        for(let i=0;i<arr.length-1;i++){
            for(let j=i+1;j<arr.length;j++){
                if(arr[i]>arr[j]){
                    [arr[i],arr[j]] = [arr[j],arr[i]]
                }
            }
        }
        return arr
    }
```