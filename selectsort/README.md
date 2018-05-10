## 选择排序 ##

### 算法复杂度：O(n^2)

遍历数组，让数组每个元素的索引初始为最小（最大）的索引，然后最小（最大）元素与它后面的元素做比较，如果有比它小（大）的元素就将该元素的索引记为最小（最大），比较完一轮后交换元素位置。

```js
     //从小到大
     function sort(arr){
            for(let i=0;i<arr.length-1;i++){
                let minindex = i;
                for(let j=i+1;j<arr.length;j++){
                    if(arr[minindex]>arr[j]){
                        minindex = j
                    }
                }
                //交换数组两个元素的位置
                [arr[minindex],arr[i]] = [arr[i],arr[minindex]]
            }
            return arr
        }
```