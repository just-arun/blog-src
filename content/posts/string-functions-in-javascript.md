---
title: "String Functions in Javascript"
description: learn about javascript string class and commonly used methods which will help developer more productive and achieve required functionality
summary: learn about javascript string class and commonly used methods which will help developer more productive and achieve required functionality
date: 2021-06-06T22:32:48+05:30
author: Arun v
draft: true
---

Useful operations we can do on strings with built-in methods, such as finding the length of a text string, joining and splitting strings, substituting one character in a string for another, and more.

## Length
length is used to count the number of characters in string

```js
let str = "this is a string"
console.log(str.length)
// output
16
```

## Split
split helps turn sting to array, it accepts a parameter based on which the string is split

```js
let str = "this is a string element"
console.log(str.split(" "))
// output
["this", "is", "a", "string", "element"]
```

## ToLowerCase
__toLowerCase__ is used to turn all the characters in the string to lowercase

```js
let str = "This is String"
console.log(str.toLowerCase())
// output
this is string
```

## ToUpperCase
__toUpperCase__ is used to turn all the characters  in the string to capital case
```js
let str = "This is String"
console.log(str.toUpperCase())
// output
THIS IS A STRING
```

## IndexOf
__indexOf__ is used to find index of the specified characters in string
```js
let str  = "what is the index";
console.log(str.indexOf("t"))
// output
8
```


## CharAt
__charAt__ is used for finding character using 