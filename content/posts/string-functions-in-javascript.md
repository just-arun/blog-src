---
title: "String Functions in Javascript"
description: learn about javascript string class and commonly used methods which will help developer more productive and achieve required functionality
summary: learn about javascript string class and commonly used methods which will help developer more productive and achieve required functionality
tags: ["string", "javascript"]
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
// 16
```

## Split
split helps turn string to array, it accepts a parameter based on which the string is split

```js
let str = "this is a string element"
console.log(str.split(" "))
// output
// ["this", "is", "a", "string", "element"]
```

## ToLowerCase
__toLowerCase__ is used to turn all the characters in the string to lowercase

```js
let str = "This is String"
console.log(str.toLowerCase())
// output
// this is string
```

## ToUpperCase
__toUpperCase__ is used to turn all the characters  in the string to capital case
```js
let str = "This is String"
console.log(str.toUpperCase())
// output
// THIS IS A STRING
```

## IndexOf
__indexOf__ is used to find index of the specified characters in string
```js
let str  = "what is the index";
console.log(str.indexOf("t"))
// output
// 3
```


## CharAt
__charAt__ is used for finding character using the input index to get the character
```js
let str = "find this string"
console.log(str.charAt(3))
// output
// d
```

## CodePointAt
__codePointAt__ is used to get the keyboard character code of the character in the string based on the index
```js
let str = "find this string"
console.log(str.codePointAt(5))
// output
// 116
```

## Includes
__includes__ is used to check the wether given string is present in the target string, this method will accept a search string
```js
let string = "we can search string and return boolean"
console.log(str.includes("can"))
// output
// true
```

## Trim
__trim__ is used to trim out the additional space on start and end of the string
```js
let str = "   this is a string   "
console.log(str.trim())
// output
// this is a string
```

## TrimLeft (TrimStart)
__trimLeft__, and __trimStart__ is used to trim out the white space on the left side of the string
```js
let str = "   this is some string   "
console.log(str.trimLeft())
// output
// this is some string
```


## TrimRight (TrimEnd)
__trimRight__, and __trimEnd__ is used to trim out the white space on the left side of the string
```js
let str = "   this is some string   "
console.log(str.trimLeft())
// output
//    this is some string
```

## Slice
__slice__ will return the string in between the given start and end index
```js
let str = "this is a string"
console.log(str.slice(5, 7))
// output
// is
```

## Replace
__replace__ will replace the selector string with the replace string, it accepts two parameter, first parameter will be the selector to select the string and it also supports regular expression the second parameter will be the replacer string
```js
let str = "this is a string"
console.log(str.replace("is", "was"))
// output
// this was a string
```

## Repeat
__repeat__ is used to repeat the string for the given count
```js
let str = "this is a string"
console.log(str.repeat(3))
// output
// this is a stringthis is a stringthis is a string
```

## Link
__link__ is used to convert the given string to wrap with a tag and point to the given url which we pass as parameter
```js
let str = "techguide"
console.log(str.link("https://techguide.dev"));
// output
// <a href="https://techguide.dev">techguide</a>
```

## Big, Bold, Italics, Sub, Strike, small
__big__, __bold__, __italics__, __sub__, __strike__, __small__ wraps string with the tag of the method name to return as html tag
```js
let str = "this is string"
console.log(str.big());
console.log(str.bold());
console.log(str.italics());
console.log(str.sub());
console.log(str.strike());
// output
// <big>this is string</big>
// <b>this is string</b>
// <i>this is string</i>
// <sub>this is string</sub>
// <strike>this is string</strike>
// <small>this is string</small>
```

## FontColor
__fontcolor__ is used to wrap the string with a font tag and set the color attribute value which we pass as parameter
```js
let str = "this is a string"
console.log(str.fontcolor("red"));
// output
// <font color="red">this is a string</font>
```

## FontSize
__fontsize__ is used to wrap the string with a font tag and set the size attribute value which we pass as parameter
```js
let str = "this is a string"
console.log(str.fontsize(16));
// output
// <font size="16">this is a string</font>
```

















