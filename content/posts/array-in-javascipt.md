---
title: "Array in Javascipt"
description: "An array is a special variable, which can hold more than one value at a time. we can access elements in array using the index which starts from 0,1,2..."
keywords: ["javascript array", "techguide blog", "array in javascript"]
summary: "An array is a special variable, which can hold more than one value at a time. we can access elements in array using the index which starts from 0,1,2..."
author: "Arun v"
tags: ["array", "javascript"]
date: 2021-06-08T20:34:46+05:30
draft: true
---

An array is a special variable, which can hold more than one value at a time. anything can be value of array including string, number, object, array etc..., the element in a array is accessed using it's index and the index won't be constant as the length of the array tends to changes 

example of array of strings
```js
let arr = ["one", "two", "three"];
console.log(arr);
// output
// ["one", "two", "three"]
```
## Index in array
the array index starts with 0 so if we want to access the second element in the array then it will have the index of 1
```js
let arr = ["one", "two", "three"];
console.log(arr[1]);
// output
// two
```
## Length of a array
Length of the array can be access by the length property sets or returns the number of elements in an array
```js
let arr = ["one", "two", "three"];
console.log(arr.length);
// output
// 3
```
## Sort array
sorting array can be done easier with the build in sort, by default it sort the items in ascending order
```js
let arrStr = ["cat", "elephant", "dog"];
let arrNum = [5, 2, 1];
console.log(arrStr.sort());
console.log(arrNum.sort());
// output
// ["cat", "dog", "elephant"]
// [1,2,3]
```
sort array in descending order
```js
let arrNum = [5, 2, 1, 4, 8, 6, 7, 3, 9, 0];
let sortedArr = arrNum.sort((a, b) => {
    if (a > b) {
        return -1
    } else {
        return 1
    }
})
console.log(sortedArr);
// output
// [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```
## Reduce method
The __reduce__ method executes a reducer function (that you provide) on each element of the array, resulting in a single output value.
```js
let arrNum = [5, 2, 1, 4, 8, 6, 7, 3, 9, 0];
let reduceValue = arrNum.reduce((accumulator, currentValue) => {
    return accumulator + currentValue;
})
console.log(reduceValue);
// output
// 45
```
## Cycle through array
common way for cycling through array using for loop
```js
let arr = ["one", "two", "three"];
for (let i = 0;  i < arr.length; i++) {
    console.log(arr[i]);
}
// output
// one
// two
// three
```
## ForEach 
This method is used to cycle through array, this will accept ac callback method which will be called for every element in a array with that element as it parameter with index as it's second parameter
```js
let arrStr= ["cat", "dog", "elephant"]
arrStr.forEach((el, i) => {
    console.log("Element: " + el + ", index: " + i)
})
// output
// Element: cat, index: 0
// Element: dog, index: 1
// Element: elephant, index: 2
```
## Map
__Map__ method will cycle through array similar to __forEach__ method but this will return a new modified array
```js
let arrStr = ["cat", "dog", "elephant"]
let newArr = arrStr.map((el, i) => {
    return el + "-" + i
})
console.log(newArr)
// output
// ["cat-0", "dog-1", "elephant-2"]
```
## Includes
__Includes__ method is used to check a value present in a array
```js
let arr = ["one", "two", "three"]
console.log(arr.includes("two"))
console.log(arr.includes("four"))
// output
// true
// false
```

## Find 
__Find__ method return one item in a array using the condition inside the callback method
```js
let arr = [
    {
        id: 1,
        name: "john"
    },
    {
        id: 2,
        name: "joe"
    },
];
let result = arr.filter(re => {
    return (re.id == 1) 
});
console.log(result);
// output
// { id: 1, name: "john" }
```

## Filter 
__Filter__ method will return new array with elements which satisfies the condition inside the callback function 
```js
let arr = ["one", "two", "three"];
let result = arr.filter((ele) => {
    // this regular express checks for 'e' in the string 
    return /e/gi.test(ele)
})
// output
// [ 'one', 'tree' ]
```

## Splice
__Splice__ method will accept a callback function with two parameter starting and ending index, this will remove the elements between these index from the original array and return it on the method
```js
let arr = ["one","two","three", "four", "five"]
let result = arr.splice(1, 3)
console.log(arr)
console.log(result)
// output
// [ 'one', 'five' ]
// [ 'two', 'three', 'four' ]
```

## Join
__Join__ method is used to convert a array to string with the given parameter string
```js
let arr = ["one", "two", "three"];
let result = arr.join(' ');
let result1 = arr.join(',');
console.log(result);
console.log(result1);
// output
// one two three
// one, two, three
```

## IndexOf
The __indexOf__ method returns the first index at which a given element can be found in the array, or -1 if it is not present.
```js 
let arr = ["one", "two", "three"]
console.log(arr.indexOf("two"))
// output
// 1
```

## Every
__Every__ method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
```js
const arr = [1, 30, 39, 29, 10, 13];
let result = arr.every((currentValue) => {
    return currentValue < 40
})
console.log(result);
// output
// true
```

## Flat
__Flat__ method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
```js
let arr1 = [
    0,
    1,
    2,
    [3, 4, 5],
    [6, 7, 
        [8, 9,
            [10, 11]
        ]
    ]
];
console.log(arr1.flat());
console.log(arr1.flat(2));
// output
// [ 0, 1, 2, 3, 4, 5, 6, 7, [ 8, 9, [ 10, 11 ] ] ]
// [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, [ 10, 11 ] ]
```




