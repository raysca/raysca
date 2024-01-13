---

draft: false
date: 2021-01-01T00:00:00+00:00
showToc: true
title: "isNaN is like gambling"
showDescription: false
description: "isNaN is a nice function that checks if a value is not a number but has been the source of many sleepless nights and wasted weekends for developers. The reason for this is that isNaN is not a reliable way to check if a value is not a number. Let me show you some examples:"

cover:
  image: "images/programmers.jpeg"
  alt: "gambling programmers"
---

`isNaN` is a nice function that checks if a value is not a number but has been the source of many sleepless nights and wasted weekends for developers. The reason for this is that `isNaN` is not a reliable way to check if a value is not a number. Let me show you some examples:

## Example 1

This is the expected behavior of isNaN. It returns true if the value is not a number and false if it is a number. In this case, 'hello' is not a number so isNaN returns true. So far so good.

```js
isNaN('hello') // true
```

## Example 2

This is where things start to get weird. The value is not a number but `isNaN` returns false.

```js
isNaN('123') // false
```

This is because `isNaN` converts the value to a number before checking if it is not a number. In this case, '123' is converted to 123 which is a number so `isNaN` returns false. So if you want to check if a value is not a number, you can use the following function:

## Example 3

How about `null`? It is not a number so `isNaN` should return true right? Wrong. It returns false.

```js
isNaN(null) // false
```

`null` is converted to 0 before checking if it is not a number. Since 0 is a number, `isNaN` returns false.

## Example 4

What if your value happens to be `undefined`?

```js
isNaN(undefined) // true
```

This is because `undefined` is converted to `NaN` before checking if it is not a number. Since `NaN` is not a number, isNaN returns true. In this case, `isNaN` works as expected.

## Example 5

What if your value happens to be `true` or `false` which are not numbers or so you thought?

```js
isNaN(true) // false
isNaN(false) // false
```

isNaN will "helpfully" convert `true` to 1 and `false` to 0 before checking if they are not numbers. Since 1 and 0 are numbers, `isNaN` returns false.

## Example 6

Have you ever mistakenly passed in `""` or `" "` to `isNaN`? You are in for a surprise.

```js
isNaN("") // false
isNaN(" ") // false
```

The "brilliant" `isNaN` function will convert `""` and `" "` to 0 before checking if they are not numbers. Since 0 is a number, isNaN returns false.

Example 7:

So for whatever reason, you find yourself checking if a Date object is not a number. What do you think will happen?

```js
isNaN(new Date()) // false
```

That's right. `isNaN` will convert the Date object to a number before checking if it is not a number. Since the Date object is converted to the number of milliseconds since January 1, 1970, 00:00:00 UTC, it is definitely a number so isNaN returns false.

## Example 8

`[]` and `{}` behave differently when passed to `isNaN` further adding to the confusion.

```js
isNaN({}) // true
isNaN([]) // false
```

`{}` is converted to `NaN` before checking if it is not a number. Since `NaN` is not a number, `isNaN` returns true. On the other hand, `[]` is converted to 0 before checking if it is not a number. Since 0 is a number, `isNaN` returns false.

Conclusion:

If you want to save yourself from a lot of headaches, you should know that `isNaN` is a very unreliable way to check if a value is not a number. If you want to check if a value is not a number, you can use the following function:

```js
function isNotANumber(value) {
  return typeof value === 'number' && isNaN(value);
}
```

This function checks if the value is a number and if it is, it checks if it is `NaN`. If it is `NaN`, it returns true. Otherwise, it returns false.

```js
isNotANumber('hello') // true
isNotANumber('123') // true
isNotANumber(null) // true
isNotANumber(undefined) // true
isNotANumber(true) // true
isNotANumber(false) // true
isNotANumber("") // true
isNotANumber(" ") // true
isNotANumber(new Date()) // true
isNotANumber({}) // true
isNotANumber([]) // true
```
