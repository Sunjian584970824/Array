# 数组

## Array



```javascript


```

## unshift\(\) 

```javascript
//向数组的开头添加一个或更多元素，并返回新的长度。  
var array=new Array(1,2,3)
array.unshift('a') //=>4   array= ['a',1,2,3]
```

## splice\(\) 

```text
Array.splice(index,howmany,item1,.....,itemX)
index	必需。整数，规定添加/删除项目的位置，使用负数可从数组结尾处规定位置。
howmany	必需。要删除的项目数量。如果设置为 0，则不会删除项目。
item1, ..., itemX	可选。向数组添加的新项目。
会对原数组修改  创建连个不同的实例返回
```

```javascript
//删除元素，并向数组添加新元素。(返回删除的元素)
var array=[1,2,3,4,5,6]
array.splice(0,1)//=>[1]  array=[ 2, 3, 4 ,5,6]  删除指定位置后指定个数元素
array.splice(0,1,'a')//=>[1]  array=[ 'a', 2, 3, 4 ,5,6]  替换对应的元素
array.splice(0,0,'a')//=>[]  array=[ 'a', 1,,2, 3, 4 ,5,6] 在对应的位置后顺序加入一个新的元素
array.splice(0,2,'a')//=>[1,2]  array=[ 'a',  3, 4 ,5,6] 将对应的位置后指定个数的元素替换成新的元素

```

## slice\(\)  

```text
Array.slice(start,end)
start:	必需。规定从何处开始选取。如果是负数，那么它规定从数组尾部开始算起的位置。
也就是说，-1 指最后一个元素，-2 指倒数第二个元素，以此类推。
end:	可选。规定从何处结束选取。该参数是数组片断结束处的数组下标。
如果没有指定该参数，那么切分的数组包含从 start 到数组结束的所有元素。
如果这个参数是负数，那么它规定的是从数组尾部开始算起的元素。 (不包含当前下标元素)
 
```

```javascript
var array = ['a', 'b', 'c', 'd'];
array.slice(0)// =>['a', 'b', 'c', 'd']    数组深拷贝  ===array  =》false   
array.slice(0，1)// =>['a']  截取下标为0~1之间的元素
```

## shift\(\);pop\(\)

```text
Array.shift() 该方法用于把数组的第一个元素从其中删除，并返回第一个元素的值,
且不创建新数组，而是直接修改原有的 arrayObject。
Array.pop()方法用于删除并返回数组的最后一个元素。
```

```javascript
var array = ['a', 'b', 'c', 'd'];
array.shift()// =>['a']    array=>[ 'b', 'c', 'd']
array.pop()// =>['d']    array=>[ 'a','b', 'c']
// 如果数组是空的，那么 shift() 方法将不进行任何操作，返回 undefined 值。   
array[1]=array[array.length-1] 
array.pop()
```

## concat\(\)

```javascript
// 该参数可以是具体的值，也可以是数组对象。可以是任意多个。
var a = [1, 2, 3, 4];
var b = ['a', 'b', 'c', 'd'];
a.concat(b) // => [ 1, 2, 3, 4, 'a', 'b', 'c', 'd' ]   
a.concat(...b) // => [ 1, 2, 3, 4, 'a', 'b', 'c', 'd' ]   
```

## join\(\)

```javascript
join() 方法用于把数组中的所有元素放入一个字符串。
var b = [1,2,3,4,5];
b.join('+') //=> 1+2+3+4+5   String
eval(b.join('+')) //  15 
```

## reverse\(\)

```javascript
颠倒数组中元素的顺序。
var b = [1,2,3,4,5];
b.reverse() // => [5,4,3,2,1]
```

## sort\(\)

```javascript
// Array.sort(sortby)  可选。规定排序顺序。必须是函数。
var a=[5,2,1,3,4]
    a.sort((now,next)=>now -next)   //正序排序  
       a.sort((now,next)=>next -now )   //反序排序  
```

