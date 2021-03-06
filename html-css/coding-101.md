![Status: Draft](https://camo.githubusercontent.com/997591db1749880b8b23c96b8f788e69af09c04d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7374617475732d64726166742d6461726b7265642e737667)

# Coding 101

**What we will learn today?**

- Getting started with JavaScript
-
## Getting started with JavaScript

We will spend most of this lesson in Codepen. To get started, go to [codepen.io/pen/](codepen.io/pen/) to create a new Pen. On the bottom left, click the "Console" button to open the console.

![Codepen console](assets/codepen-console.png)

You can place your cursor right behind the `>` sign. Type a simple expression, such as `2 + 2` and hit enter. You will see expression, as well as its result, in the window above.

![Entering expressions in the Codepen console](assets/repl.gif)

You will be able to follow most of this session along just entering expressions in the console like this.

## Simple data types & Expressions

### Numbers

Let’s start with something seemingly simple - numbers. Here are some:

```js
1
15
3195803798
1.4
0.0000005
0
-23
```

You will see that there are whole numbers (no decimal point) and real numbers (decimal point), which in JavaScript are so-called “floating point” numbers. Numbers can be positive or negative and they support all the basic math operators that you would expect:

```js
2 + 2 // 4
2 - 5 // -3
2 * 3 // 6
10 / 2 // 5
3 * -2 // -6
```

Operators have the same precedence as in algebra: `*` and `/` have higher precedence than `+` and `-`.

- **TODO:** Do math exercise
- **TODO:** What about Infinity, Math.PI, IEEE floating point bullshit, NaN

### Strings

Strings represent any sort of text. They are delimited by single quotes (`'`) or double quotes (`”`) and can be of any length.

```
'' // empty string
"" // empty string
'Hello'
'I am learning JavaScript'
'It\'s been a great journey so far!'
"Double quotes work as well"
```

> If you need single or double quotes *inside the string*, you need to “escape” them by putting a backslash in front of them. If you don’t do this, the JavaScript engine will think the string ends here, because it encounters a quote.

The most common operation on strings is to append one string to another. This is called *string concatenation*. It’s achieved by the plus (`+`) operator:

```
"Hello" + "World" // "HelloWorld"
```

- **TODO:** Introduce string concatenation
- **TODO:** What about basic string functions, like substr, replace etc?

### Booleans

[Booleans](https://en.wikipedia.org/wiki/Boolean_data_type) are a data type that can only have two values: `true` and `false`.

Like numbers, they can be combined using operators, but there are different operators for booleans (analoguous to [Boolean algebra](https://en.wikipedia.org/wiki/Boolean_algebra)). The most important ones are:

- `!` (NOT), which negates a value:
```js
!true // false
!false // true
```
- `&&` (AND), which is only true if both operands are true:
```js
false && false // false
true && false // false
false && true // false
true && true // true
```
- `||` (OR), which is true if at least one of the operands is true:
```js
false && false // false
true && false // true
false && true // true
true && true // true
```

**TODO:** When to introduce truthiness and falsiness? Probably in `comparisons`?

* * *

> **Exercise**: Put simple mathematical expressions into the console: `2 * 2`, `2 + 2`, `5 * 7 - 13`
> **Exercise**: Calculate the area of a circle (`r * r * pi`). Do a quick Google search on how to use PI in JavaScript.

> See what happens when you "add" two strings together

> Research the JS Math library. sqrt, floor, ceil, round

> Write an expression that outputs the percentage of students who are female. Make it so it outputs it as `58%`, and make sure you use the actual numbers of women and the total number of students.
> Solution: `console.log(Math.round(7 / 17 * 100) + "%");`

### From REPL to console.log

- Single expressions are not very useful, you want to write applications
- More than one statement? Move it to the `JS` box in Codepen
- Now you don't get any immediate feedback
- Use `console.log` to print to the console: `console.log(3 + 3);`
- Write statements below each other

> **THOUGHT:** Codepen does not have a "run" button, so it's quite intransparent when it actually re-runs a program. Maybe a different tool is better? A simple jsbin configuration, maybe?
