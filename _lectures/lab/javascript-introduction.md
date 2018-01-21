---
title:            JavaScript Introduction
subtitle:         An introduction to the web's programming language
lecture_date:     2017-03-29 00:00:00 -0500
section:          Lab
---

### Separation of Concerns

So far we've looked at how to create content with HTML and style it with CSS. Now, we'll learn how
to transform and manipulate our content dynamically using JavaScript.

| HTML | CSS | Javascript |
| --- |---| ---|
| Content | Style | Behavior |
| _What it says_ | _What it looks like_ | _What it does_ |

---

### Writing JavaScript in your browser

Chrome's Web Inspector has a powerful JavaScript console built into it. You can access the console by
going to View > Developer > JavaScript Console, or by selecting the Console tab when Dev Tools is open.

![Javascript console](/assets/lectures/lab/javascript-introduction/console.png)

With the console open, you can execute JavaScript directly in your browser and see the updates live.

![Javascript console](/assets/lectures/lab/javascript-introduction/console-update.png)

---

### Adding JavaScript to your website

Adding JavaScript to your website can be done either directly inline in your HTML document, in between
`<script></script>` tags, or preferably in an external JavaScript file, similar to how you link an external
CSS file.

```html
<script src="/js/main.js"></script>
```

The JavaScript file can be linked from anywhere in the `<head>` or `<body>` element, but usually you will add it in the
`<head>`, right after your CSS file, or at the very end of your document, before the closing `</body>` tag. It's a good
practice to [add it to the end of your document](http://stackoverflow.com/questions/5329807/benefits-of-loading-js-at-the-bottom-as-opposed-to-the-top-of-the-document) so that downloading the script doesn't block the rendering of your HTML page.

- [Including JavaScript in your page](https://www.w3schools.com/js/js_whereto.asp)

```html
<!DOCTYPE html>
<html>
<head>
  <title>Document</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
<!-- Your HTML goes here. At the very end of the document,
     right before the closing </body> tag, include your javascript. -->
  <script src="/js/main.js"></script>
</body>
</html>
```

---

### Data Types

A data type in programming languages is an important concept as it means that a particular piece of data can
be acted upon with a particular set of actions. For example, adding two `numbers` together will lead to obvious
results, but adding two `strings` together lead to a different results.

```js
1 + 1         // 2
'cat' + 'dog' // 'catdog'
'1' + '1'     // '11'
```

Some common data types that we will be using are `strings` `numbers` `booleans` and `arrays`.

```js
'core interaction'         // String
16                         // Number
true                       // Boolean
false                      // Boolean
[1, 2, 'three', 'four', 5] // Array
```

- [JavaScript Data Types](https://www.w3schools.com/js/js_datatypes.asp)

---

### Strings

A string in JavaScript is text wrapped in single or double quotes. In JavaScript you can use either single or double
quotes, but you should be consistent throughout your code.

```js
// Single quotes
'Garden as though you will live forever.'

// Double quotes
"A rose is a rose is a rose."
```

To add quotes within a string, use the inverse quote within the string, or escape the quotes using a backslash.

```js
// Double quotes inside single quoted string
'William Kent said, "Garden as though you will live forever"'

// A backslash is used to escape a quote of the same type as the string
'Dylan\'s favorite website is Hacker News'

// Single quotes inside double quoted string
"Nika's favorite color is pink"
```

- [Read more](https://www.w3schools.com/js/js_strings.asp)

---

### Numbers

JavaScript has only one type of number data type, which can be written with or without decimals.

```js
100    // A number without decimals
100.00 // A number with decimals
```

- [Read more](https://www.w3schools.com/js/js_numbers.asp)

---

### Booleans

A boolean value is one that is either true or false.

```js
true  // A boolean value true
false // A boolean value false

// Strings that look like boolean values aren't actually boolean values
'true'  // A string with the text 'true'
'false' // A string with the text 'false'
```

- [Read more](https://www.w3schools.com/js/js_booleans.asp)

---

### Arrays

Arrays are collections of values. Think of an array as a list. You can add and remove items from the list, in addition
to a number of other functions that make working with arrays easier.

An array is defined as a series of comma-separated values inside brackets

```js
// An empty array
[]

// An array with one item in it
['hello world']

// An array with many items in it.
// The type of data in an array can vary.
['hello', 'world', 1, 2, true, false, 'lorem ipsum']
```

To refer to an item in an array, use the index of that item.

```js
var myArray = ['apple', 'orange', 'banana', 'peach'];
var firstItem = myArray[0]; // 'apple'
var lastItem = myArray[3];  // 'peach'

// A better way to get the last item in an array is to
// use the length of the array itself
lastItem = myArray[myArray.length - 1]; // 'peach'
```

- [Read more](https://www.w3schools.com/js/js_arrays.asp)

---

### Variables

Variables in javascript are defined using the keyword `var`. Without this keyword, the variable becomes _global_,
which is [very bad](https://www.google.com/search?q=global+variables+javascript+bad&oq=global+variables+javascript+bad).

```js
// Create and set a variable to any value you want
var labTeacher = 'Dylan';
var studioTeacher = 'Nika';
var currentWeekNumber = 9;
var stayInSchool = true;
var myArray = [1, 2, 3, 4];

// Re-set a previous variable to a new value.
// Notice that no var keyword is necessary here
// since the variable has already been defined.
myArray = [5, 6, 7, 8];
```

Naming conventions in JavaScript follow the [camelCase](https://www.w3schools.com/js/js_conventions.asp) formatting.

- [Read more](https://www.w3schools.com/js/js_variables.asp)

---

### Debugging

Use `console.log()` in your JavaScript files to log messages to your dev tools console. You can log any type of data, including
variables. This can be very helpful when you are writing code and need to identify why a particular piece of it isn't working
as expected. Log the values and identify what the problem is.

```js
console.log('hello world');

var today = Date();

console.log('Today is', today);
```

You should also always have the dev tools console open when writing JavaScript so that you can identify any errors in your code.

![Javascript console](/assets/lectures/lab/javascript-introduction/console-error.png)

---

### Operators

Similar to algebra, you can do arithmetic and perform other operations with JavaScript.

```js
10 + 100    // 110
7 * 7       // 49
3 * 1 + 2   // 5
3 * (1 + 2) // 9
99 / 5      // 19.8

4 > 3       // true
4 > 3 * 3   // false
10 <= 10    // true

var x = 1;     // assign the value 1 to x
var y = 2;     // assign the value 2 to y
var z = x + y; // assign the value 3 to z (x + y)

// Equality
10 == 10  // true
45 != 46  // true
'5' == 5  // true
'5' === 5 // false (equal value and equal type)
```

[Read more](https://www.w3schools.com/js/js_operators.asp)

---

### Conditional Statements

```js
// If statement
if ( condition ) {
  // block of code to be executed if the condition is true
}

// Else statement
if ( condition ) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}

// Else if statement
if ( condition1 ) {
  // block of code to be executed if condition1 is true
} else if ( condition2 ) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

```js
// If else example with multiple conditions
var date = new Date;
var hour = date.getHours();

if ( hour == 0 ) {
  console.log("woah, it's midnight");
} else if ( hour > 0 && hour < 9 ) {
  console.log("it's too early, go back to bed");
} else {
  console.log("carpe diem");
}
```

[Read more](https://www.w3schools.com/js/js_if_else.asp)

---

### For loops

```js
for ( var i = 0; i < 10; i++ ) {
  console.log('The index is', i);
}
```

```js
// An example
var students = [
  'Carol Chong',
  'Gaurika Milan Dalal',
  'Vitoria Feitosa Di Iulio',
  'Nafisa Afrin Iqbal',
  'Moonnyung Jo',
  'Ana Sofia Murillo',
  'Gyuri Nam',
  'Jissaura Taveras Hernandez',
  'Elizabeth Tsai',
  'Kyle Yu'
];

for ( var i = 0; i < students.length; i++ ) {
  console.log( students[i] + ' is in index ' + i );
}
```

[Read more](https://www.w3schools.com/js/js_loop_for.asp)
