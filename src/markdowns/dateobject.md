---
slug: dateobjectjs
title: JavaScript Date Object
---

## Introduction

In JavaScript, Date Objects are used to work with Date and Time.

### Application

You can use this Date object in different ways but the mostly used ways are

- Get current date or time from the user's system
- Format the date and time

### Creating Date Objects

Date Objects are created with this snippet `new Date()`. We can also store the object in variable to use it later. Like this -

```javascript
var dateObject = new Date();
let d = new Date();
const date = new Date();
```

<div class="note"><p>In JavaScript, `new` keyword is used to create a new object. The general syntax of creating new object is `new &lt;name of the object&gt;()`</p>
<p>All letters of the keyword <code>new</code> are in small letter and the "D" of the <code>Date</code> is in capital letter. <b>Don't mixed up this</b></p>
</div>

If you now display or `console.log` this date object you will get output something like this

`2023-09-16T15:07:21.989Z`

## Methods of Date Object

Date Object provides you alot of methods to use for different things. Few of them are

`const d = new Date();`

### getDate()

`getDate()` method of the Date Object is used to get current date as per user's system.
It returns the current date as a integer (1 to 31)

```js
let date = d.getDate();
console.log(date);
```

### getMonth()

`getMonth()` method of the Date Object is used to get current month as per user's system.
It returns the current month as a integer (0 to 11) where `o` means **January** and `11` means **December**.

If you are going to just display the number then add +1 to it other wise use array

```js
let month = d.getMonth();

console.log(month + 1);

const months = [
	"January",
	"February",
	"March",
	"April",
	"May",
	"June",
	"July",
	"August",
	"September",
	"October",
	"November",
	"December",
];

console.log(months[month]);
```

### getFullYear()

`getFullYear()` method of the Date Object is used to get current year as per user's system.
It returns the current month as a four digit integer (1000 to 9999)

```js
let fullYear = d.getFullYear();

console.log(fullYear);
```

<div class="warning"> Previously <code>getYear()</code> method was used in place of  <code>getFullYear()</code>. This <code>getYear()</code> does not support any more, if you use it you might not get right output. Use <code>getFullYear()</code> instead.</div>

### getHours()

`getHours()` method of the Date Object is used to get current hour as per user's system.
It returns the current hour as a integer (0 to 23)

Similar to `getMonths`, add +1 to it before displaying it.

```js
let hour = d.getHours();

console.log(hour + 1);
```

### getHours()

`getHours()` method of the Date Object is used to get current hour as per user's system.
It returns the current hour as a integer (0 to 23), i.e. it returns hours in **24 hours format**.

```js
let hour = d.getHours();

console.log(hour);
```

### getMinutes()

`getMinutes()` method of the Date Object is used to get current minute as per user's system.
It returns the current hour as a integer (0 to 59).

```js
let minute = d.getMinutes();

console.log(minute);
```

### getSeconds()

`getSeconds()` method of the Date Object is used to get current second as per user's system.
It returns the current second as a integer (0 to 59).

```js
let second = d.getSeconds();

console.log(second);
```

### getMilliseconds()

`getMilliseconds()` method of the Date Object is used to get current milliseconds as per user's system.
It returns the current millisecond as a integer (0 to 999).

```js
let millisecond = d.getMilliseconds();

console.log(millisecond);
```

<div class="note">If you don't know <b>1 second = 1000 milliseconds</b></div>

### getDay()

`getDay()` method of the Date Object is used to get current day of the week.
It returns the current day as a integer (0 to 6) where `o` means **Sunday** and `6` means **Saturday**.

If you are going to just display the number then add +1 to it other wise use array

```js
let day = d.getDay();

console.log(day + 1);

const nameOfDay = [
	"Sunday",
	"Monday",
	"Tuesday",
	"Wednesday",
	"Thursday",
	"Friday",
	"Saturday",
];

console.log(nameOfDay[day]);
```

### getTime()

`getTime()` method of the Date Object is used to get the number of milliseconds since **January 1, 1970 00:00:00** (also known as **_Epoch_**)

```js
let time = d.getTime();

console.log(time);
```

<div class="note">For more infomation about <b>Epoch</b> visit this link :- <a href="https://en.wikipedia.org/wiki/Epoch">wikipedia of Epoch</a></div>

more will be added later
