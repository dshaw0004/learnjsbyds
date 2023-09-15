---
slug: comparisonoperator
title: Comparison Operators
---

## Introduction

In JavaScript Comparison Operatorsare used to compare two value. The
general form of comparison in JS is

`{first value} {comparison operator} {second value}`

Example :- `a > b`, in this example 'a' is the first value, 'b' is the second value and we are checking whether the 'a' is greater than 'b'. If 'a' is greater than 'b' then it returns `true` otherwise `false`

## Quick List of Comparison Operators

---

|  symbol   | name              | Usage                                                                             |
| :-------: | ----------------- | --------------------------------------------------------------------------------- |
|     >     | greater then      | check whether the first value is greater then second value or not                 |
|    >=     | greater equals to | check whether the first value is greater then or equal to the second value or not |
|     <     | less then         | check whether the first value is less then second value or not                    |
|    <=     | lesser equals to  | check whether the first value is less then or equal to the second value or not    |
| == or === | equals to         | checks whether the both value are same or not                                     |
|    !=     | not equals to     | checks whether the both value are not equal                                       |

---

## Briefing of Each Operator

### Greater Then Operator ( > )

Denoted by greater then or left angular bracket (`>`) symbol. It Checks if the first value is greater than second value or not.
If the first value is greater then it returns `true` else it returns `false`.

#### Example

```javascript
169 > 69; // returns true
308 > 420; // returns false

"whale" > "shark"; // returns true
"car" > "truck"; // returns false

"Tiger" > "tiger"; //returns false
```

<div class="note">
In case of comparing strings, Javascript check their ASCII value
</div>

### Less Then Operator ( < )

Denoted by less then or left angular bracket (`<`) symbol. It Checks if the first value is lesser than second value or not.
If the first value is less then it returns `true` else it returns `false`.

#### Example

```javascript
308 < 420; // returns true
169 < 69; // returns false

"whale" < "shark"; // retunrs false
"car" < "truck"; // returns true

"Tiger" < "tiger"; //returns true
```

### Equals To Operator ( == )

Denoted by two equals to symbols (`==`).
This operator checks whether the first value is equals to the second value or not.
If both values are equal then it returns `true` otherwise it returns `false`

<div class="warning"> `==` and `=`both  are different. don't be mixed up them. </div>

```javascript
69 == 69; // returns true
169 == 196; // returns false

69 == "69"; // returns true

"Tiger" == "tiger"; //returns false
"mango" == "mango"; // retuns true
```

<div class="note">
<p>In case of `69 == "69"`, javascript comverts `"69"` into number then do the comparison.</p>
<p>In case of `"Tiger" == "tiger"`, the <abbr title="American Stanard Code for Information Interchange">ASCII</abbr> value of `T` is less then that of `t`.
Therefore, "tiger" is greater than "Tiger".
</p>
</div>
