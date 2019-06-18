---
title: "Post: JavaScript Functional Programming"
categories:
  - JavaScript
tags:
  - JavaScript
---

# 1007 JavaScript Functional Programming- Functions 01
## Assignment
### Status: Final 20190501

**Instruction**
 1. Write a JavaScript function to compute the sum of an array of integers.

The following number is the input for the array: `12, 11, 10, 9, 8, 7`

**Solution**

```JavaScript
// function declaration
function arraySum01(myArray) {
	return  myArray.reduce( function(accumulator, currentValue) {
		return accumulator + currentValue;
	}, 0);
}

// function expression anonymous
let arraySum02A = function(myArray) {
	return  myArray.reduce( function(accumulator, currentValue) {
		return accumulator + currentValue;
	}, 0);
};

// function expression named
let arraySum02B = function arraySum02(myArray) {
	return  myArray.reduce( function(accumulator, currentValue) {
		return accumulator + currentValue;
	}, 0);
};

// function constructor anonymous
let arraySum03 = new Function('myArray',
	'return myArray.reduce( function(accumulator, currentValue) { \
		return accumulator + currentValue; \
	}, 0);'
);

console.log(arraySum01([12, 11, 10, 9, 8, 7]));
console.log(arraySum02A([12, 11, 10, 9, 8, 7]));
console.log(arraySum02B([12, 11, 10, 9, 8, 7]));
console.log(arraySum03([12, 11, 10, 9, 8, 7]));
```

Reference:
- [Function declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)
- [Function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function)
- [Function constructor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function)

> Written with [StackEdit](https://stackedit.io/).
