# 数组的复杂操作，及小技巧

## 循环

 **map\(\)、forEach\(\)、for\(\)**

```javascript
//数组的map方法是有返回值的
var array=[1,2,3,4,5,6,7];
var P = array.map((index, i) => {
    var I = index - 2;
    return I;
})
console.log("P", P) //P [ -1, 0, 1, 2, 3, 4, 5 ] 返回一个新数组 对原数组操作
console.log("Arr", Arr) //  Arr  [1,2,3,4,5,6,7] 原数组不变

//forEach方法是没有返回值得
var array=[1,2,3,4,5,6,7];
var P = array.map((index, i) => {
    var I = index - 2;
    return I;
})
console.log( P) // undefined
console.log("Arr", Arr) //  Arr  [1,2,3,4,5,6,7] 
```

## 过滤

```javascript
//Array.filter(callback) 过滤数组，返回一个满足要求的数组
var array=[1,2,3,4,5,6,7];
let arr1 = array.filter( item => item>3)  // =>[ 4, 5, 6, 7 ]
```

 **arr.every\(callback\)  依据判断条件，数组的元素是否全满足，若满足则返回ture**

```javascript
let arr = [1,2,3,4,5]
let arr1 = arr.every( (i, v) => i < 3)
console.log(arr1)    // false
let arr2 = arr.every( (i, v) => i < 10)
console.log(arr2)    // true
```

  **arr.some\(\) 依据判断条件，数组的元素是否有一个满足，若有一个满足则返回ture**

```javascript
let arr = [1,2,3,4,5]
let arr1 = arr.some( (i, v) => i < 3)
console.log(arr1)    // true
let arr2 = arr.some( (i, v) => i > 10)
console.log(arr2)    // false
```

  **arr.includes\(\) 判断数中是否包含给定的值**

```javascript
let arr = [1,2,3,4,5]
let arr1 = arr.includes(2)  
console.log(arr1)   // ture
let arr2 = arr.includes(9) 
console.log(arr2)    // false
let arr3 = [1,2,3,NaN].includes(NaN)
console.log(arr3)  // true
```

## 小技巧

```javascript
例子:
function test(routeName) {
  if (routeName=== 'login' || routeName=== 'index') {
   console.log(routeName)
  }
}

Array.includes (Array.includes)重写条件语句。

function test(routeName) {
  const routeName= ['login', 'index', 'print', 'setPrint'];
  if (routeName.includes(routeName)) {
    console.log(routeName);
  }
}
```

