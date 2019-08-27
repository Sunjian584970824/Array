---
description: '创建array  new Array(element0, element1, ..., elementn);'
---

# Array 对象方法

## push\(\) 

```javascript
//	向数组的末尾添加一个或更多元素，并返回新的长度。
var array=new Array(1,2,3) //=>3     array=  [1,2,3];
array.push('a') //=>4   array= [1,2,3,'a']
array.push('b','c','d') //=>7   array=[1,2,3,'a','b','c','d'];

//拓展  es6  ...
var test1=new Array(1,2,3)
var test2=new Array(4,5,6)
test1.push(...test2) //=>[1,2,3,4,5,6]

```



