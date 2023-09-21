---
slug: loopoverarray
title: How to loop over an array
---

## What is an Array ?

An array is a special variable, which can hold more than one value. An array is helpful to store same type of data in a single variable.

```js
// Don't do this ❌
let animal1 = "tiger";
let animal2 = "lion";
let animal3 = "panther";

// Do this ✅
let animals = ["tiger", "lion", "pather"];
```

for more info about [visit this link](https://www.w3schools.com/js/js_arrays.asp)

## How to loop over an array ?

Getting directly into the point let's discuss how to loop over an array.

There are multiple way to loop over an array in javascript and each way have its own some feature, pros and cons.

Let's discuss few of them one by one

<div class="note">One thing I should clearify first, I will not go depth of each loops. This post is not about js loops this is about how can you use that loops to interate over an array. Here you will find data which are only relevant to array </div>

1. ### Traditional for-loop:

Let's loop over our `animals` array using **_traditional for-loop_**.

```js
for (let i = 0; i < animals.length; ++i) {
	console.log(animals[i]);
}
```

#### Pros:

- **Familarity**: This is the basic `for` loop so most of the js developer know this. Even beginners too.

- **Versatility**: The traditional `for` loop is extremely versatile. You can initialize multiple variables, have multiple conditions, and increment or decrement your counter variable by any amount.

- **Control over Index**: In this `for` loop, you have direct access to the index of the array. This can be useful when you need to reference the position of an element within the array.

- **Break and Continue**: The `for` loop allows you to use `break` and `continue` statements to control the flow of your loop.

#### Cons

- **Verbose Syntax**: Compared to other looping methods in JavaScript, such as `forEach`, `map`, `filter`, etc., the syntax of a `for` loop is more verbose.

- **Immutable Data**: If you're working with immutable data structures, a `for` loop might not be the best choice. Other methods like `map` or `reduce` are more suited to these types of data structures.

- **Support to Frameworks**: `for` loops can not be used in the return statements. So developer of `react` like frameworks love to use other methods like map, filter, reduce etc in the return statement as well as every where.
  (**I personally do**)

In conclusion, while the traditional `for` loop in JavaScript is a powerful tool, it's important to understand its strengths and weaknesses. Depending on the situation, other looping methods might be more appropriate.

2. ### For-in loop:

This is basically **_traditional for-loop_** in a different outfit. Let's try this too.

```js
for (let i in animals) {
	console.log(animals[i]);
}
```

#### Pros

- **Simplicity**: The `for-in` loop has a simple and clean syntax, which makes it easy to read and understand.

- **Access to indices**: In a `for-in` loop, you have direct access to the indices (or key if you are loop over object) of the array. This can be useful when you need to reference the position of an element within the array.

- **Works with Objects**: The `for-in` loop can also be used to iterate over the properties of an object, not just arrays.

#### Cons

- **Enumerates Prototype Properties**: The `for-in` loop will also enumerate over all enumerable properties in the prototype chain. This can lead to unexpected results if the array's prototype has enumerable properties.
  (**This is a intermediate level concept**)

- **Performance**: `for-in` loops are generally slower than traditional `for` loops or other array methods like `forEach`, `map`, etc.

- **Order Not Guaranteed**: I don't use this loop in js. So I can not confirm this. But I read this some many places that the `for-in` loop does not guarantee the order of elements in the array. I can not provide more detail about this topic.

In conclusion, while the `for-in` loop in JavaScript can be a handy tool, it's important to understand its strengths and weaknesses. Depending on the situation, other looping methods might be more appropriate.

3. ### For-of loop:

This is not like the **_traditional for-loop_** . It has some different feature. Let's try this too.

```js
for (let animal of animals) {
	console.log(animal);
}
```

Previous 2 `for` loops gives you the indices then you have to get the value at that index by doing this `animals[i]`. But `for-of` loop gives you the value instead of index.

#### Pros

- **Simplicity**: The `for-of` loop is straightforward and easy to understand. It automatically iterates over each item in the array without the need for an index.

<div class="note">This <code>for</code> loop is similar to <code>python</code>'s <code>for</code> loop. 
If you know <code>python</code> then it would not be hard for you. </div>

- **Works with Different Data Types**: Unlike `for-in`, `for-of` can iterate over array-like objects and data types like strings, maps, sets, and more.

- **Avoids Out-of-index Error**: Since `for-of` doesn't rely on indices, there is less chance to face _out-of-index_ error.

#### Cons

- **No Access to Index**: In a `for-of` loop, you don't have direct access to the index of the current element. If you need the index, you'd have to use a different loop.

- **Inefficiency**: `for-of` can be less efficient than traditional `for` or `while` loops, especially for large arrays, because it involves more overhead due to the iterator protocol.

- **Compatibility Issues**: `for-of` is a part of ECMAScript 6 (ES6) and may not be supported in older browsers or environments that do not support ES6.

In conclusion, while the `for-of` loop provides a simple and versatile way to iterate over arrays in JavaScript, it's important to consider its limitations and potential performance implications. Always choose the right tool for the job based on your specific needs and the characteristics of your data.
