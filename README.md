# coding-convention
This is the coding convention for Journey Horizon developers. Please read it kindly and carefully.

## Front-end convention access this 
[Front-end convention](https://github.com/journeyhorizon/coding-convention/blob/master/Front-End-Convention.md)

## Variable names & naming convention

- We use *camelCase* for identifier names (variables and functions)

- Function name must always start with a *verb* if they stand alone and is not a property of any object

```js
• increment() is better than plusOne()
• unzip() is better than filesFromZip()
• filter(isActive, array) is better than activeItemsFromArray(isActive, array)
```

- All names start with a *letter*.

- Global const should always have every letters capitalized and words separte by a *_*

- Unless when we are modifying a template that have different file naming convention, we should always use *camelCase* to name a file

- When you are naming a variable, if it is not a function please name it as a noun or compound noun

```js
const foo = 'foo';
const ALLOWED_STATUS = ['pending', 'cancel'];
```

- Use active voice

```js
• myFunction.wasCalled() is better than myFunction.hasBeenCalled() 
• createUser() is better than User.create()
• notify() is better than Notifier.doNotification()
```

- Name predicates and booleans as if they are yes or no questions

```js
• isActive(user) is better than getActiveStatus(user)
• isFirstRun = false; is better than firstRun = false;
```

## Event Handlers

Event handlers and lifecycle methods are an exception to the verb rule because they’re used as qualifiers; instead of expressing what to do, they express when to do it. They should be named so that they read, `<when to act, <verb>`.

```js
• element.onClick(handleClick) is better than element.click(handleClick)
• component.onDragStart(handleDragStart) is better than component.startDrag(handleDragStart
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

## Ternary Operator

Do not use ternary operator to call for function on one line

```js
const isValid = true;
isValid ? doSth() : null; //Do not do this
```

## Note

- Favor pure functions > factories > functional mixins > classes
- Avoid the creation of is-a relationships between objects, mixins, or data types, favor object composition
