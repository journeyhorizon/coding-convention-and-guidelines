# coding-convention
This is the coding convention for Journey Horizon developers. Please read it kindly and carefully.


## Variable names & naming convention

- We use *camelCase* for identifier names (variables and functions)

- Function name must always start with a *verb* if they stand alone and is not a property of any object

- All names start with a *letter*.

- Global const should always have every letters capitalized and words separte by a *_*

- Unless when we are modifying a template that have different file naming convention, we should always use *camelCase* to name a file

```js
const foo = 'foo';
const ALLOWED_STATUS = ['pending', 'cancel'];
```
## Spaces Around Operators

Always put spaces around operators ( = + - * / ), and after commas:

```js
const total = preTax + tax;
const ALLOWED_STATUS = ['pending', 'cancel'];
```
## Code Indentation

Always use 2 spaces for indentation of code blocks:

```js
const doSth = () => {
  return true;
};
```
## Statement Rules

General rules for simple statements:

- Always end a simple statement with a semicolon

```js
const foo = 'foo';
const doSth = () => {
  return true;
};
```

General rules for complex (compound) statements:

- Put the opening bracket at the end of the first line.
- Use one space before the opening bracket.
- Put the closing bracket on a new line, without leading spaces.
- Always statements with a semicolon
- Do not end a complex statement with a semicolon.

*Loops:*
```js
for (i = 0; i < 100 i++) {
  x++;
}
```
*Conditionals:*
```js
if (good) {
  return 'Good day';
} else {
  return 'Bad day';
}
```
## Object Rules

General rules for object definitions:

- Place the opening bracket on the same line as the object name.
- Use colon plus one space between each property and its value.
- Use \` or ', " around string values, not around numeric values.
- Place the closing bracket on a new line, without leading spaces.
- Always end an object definition with a semicolon.

```js
const company = {
  name: 'JH',
  fullName: 'Journey Horizon',
  location: {
    lat: 15.45,
    lng: 16.45
  },
  age: 1
};
```

Always use a space between the properties and the object's brackets:

```js
const company = { name: 'JH', age: 1 };
```

## Line Length < 80

For readability, avoid lines longer than 80 characters.

If a JavaScript statement does not fit on one line, the best place to break it, is after an operator or a comma.

```js
document.getElementById('demo').innerHTML =
'Hello';
```

## Variable declaring

You should always declare a new variable using `const` instead of `let` or `var`. In the worst case scenarior when there are no other way, you can use `let` but `var` is not allowed.

```js
const foo = 'foo';
let demoStr = '';
for (i = 0; i < 5; i++) {
    demoStr = demoStr + 'test';
}
```
