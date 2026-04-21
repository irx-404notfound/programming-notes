# JAVASCRIPT FUNDAMENTS

## VARIABLES

> [!NOTE]
> `let` declares a variable that can be reassigned after its initial declaration.

```javascript
let firstName = "Iraia";
let lastName = "Espinosa";
```

> [!NOTE]
> `const` declares a variable that cannot be reassigned after its initial declaration.

```javascript
const fullName = `${firstName} ${lastName}`;
```

Output:

```javascript
console.log(fullName);
```

```bash
Iraia Espinosa
```

### VARIABLE TYPES

#### Dynamic typing: 

> [!NOTE]
> The type of the variable changes during the execution of the code.

Example:

```javascript
let value = 10; // number
value = "hello"; // string
value = true; // boolean
```

#### Casting: 

> [!NOTE]
> This is the process of converting a value from one type to another. In JavaScript, this can happen automatically without you asking, or you can manually force the conversion when needed.

Examples:

JavaScript changes the type without you ask:

> [!NOTE]
> The number `2` value changes to `string`.

```javascript
"5" + 2 // Result: "52"
```

> [!NOTE]
> The string `5` value changes to `number`.

```javascript
"5" - 2 // Result: 3
```

When you manually force the type conversion:

> [!NOTE]
> You explicitly control the conversion.

```javascript
Number("5") // 5
String(10) // "10"
Boolean(0) // false
Boolean(1) // true
```

## FUNCTIONS

> [!NOTE]
> A function is a block of code that performs a specific set of tasks.

```javascript
function printCopyright() {
  console.log("Iraia - 2026");
}
```

To call the function, you need to use this:

> [!WARNING]
> If you don't call the function, it will never run.

```javascript
printCopyright();
```

A function can also return a value, meaning it will give back the value of a variable. 

```javascript
function getCopyright() {
  let copyright = "Iraia - 2026";
  return copyright;
}

getCopyright();
```

### Naming conventions for functions

- Use camelCase. Example: `printCopyright`

```javascript
function printCopyright() {
  console.log("Iraia - 2026");
}
```

- Use descriptive names.
- Avoid spaces.
- Avoid unnecessary numbers.
- Avoid punctuation marks.

### FUNCTION EXPRESSIONS

#### ANONYMOUS FUNCTIONS

> [!NOTE]
> A vaiable can store an anonymous function. This is useful to avoid hoisting issues.

```javascript
let func = function (parameterOne) {
  return parameterOne + ":)";
}
```

##### ANONYMOUS FUNCTIONS IN ARGUMENTS

> [!NOTE]
> A function passed as a parameter is called a callback. The value can be another function, and the callback can also be declared directly in the function call.

Example of a callback from another function:

```javascript
function getCopyright(name, year, callback) {
  let copyright = callback(name, year);
  return copyright;
}

let formatWithPipe = function (name, year) {
  return name + " | " + year;
}

let formatWithHypen = function (name, year) {
  return name + " - " + year;
}

getCopyright("Iraia", 2026, formatWithPipe);
```

Example of a callback declared in the same call:

```javascript
function getCopyright(name, year, callback) {
  let copyright = callback(name, year);
  return copyright;
}

getCopyright("Iraia", 2026, function(name, year) {
  return name + " | " + year;
});
```

#### IMMEDIATELY INVOKED FUNCTION EXPRESSION (IIFE)

> [!NOTE]
> An Immediately Invoked Function Expression (IIFE) is a function that runs immediately after it is defined.

```javascript
(function (name, year) {
  console.log(name + " - " + year);
})("Iraia", 2026);

// --

!function (name, year) {
  console.log(name + " - " + year);
}("Iraia", 2026);
```

Other example:

> [!NOTE]
> `(function () {})` converts the function into an expression.

```javascript
(function () {
  console.log("Hello");
})();
```

## PARAMETERS

A parameter is a value that a function can receive when it is called.

> [!NOTE]
> Parameters are defined inside the `()` of a function.

```javascript
function getCopyright(name, year) { // name and year are parameters.
  let copyright = name + " - " + year;
  return copyright;
}
```

> [!NOTE]
> When you provide values to a function when calling it, those values are called arguments.

```javascript
getCopyright("Iraia", "2026"); // "Iraia" and "2026" are arguments.
```

> [!NOTE]
> You can also define default parameter values.

```javascript
function getCopyright(name = "Iraia", year = "2026") {
  let copyright = name + " - " + year;
  return copyright;
}
```

## CONDITIONS - IF/ELSE

> [!NOTE]
> Conditional statements are used for decision-making in response to a situation.

For example, imagine that you're angry and you want to eat pizza because it's your favourite food. So you ask yourself whether you have pizza at home. If you have pizza, you cook it and then eat it, but if you don't have it, you order it.

Examples:

```javascript
let hasPizza = true;

if (hasPizza == true) {
  cook();
} else {
  orderPizza();
}

eat();
```

```javascript
let hasPizza;

if (hazPizza == true) {
  cook();
} else if (hasPizza == false) {
  orderPizza();
} else {
  openFridge();
}

eat();
```

## OPERATORS

There are two types of operators: comparison operators and logical operators.

### COMPARISON OPERATORS

- Equality: `==`
- Strict equality: `===`
- Inequality: `!=`
- Strict inequality: `!==`
- Greater than: `>`
- Less than: `<`
- Greater than or equal to: `>=`
- Less than or equal to: `<=`

Examples:

> [!NOTE]
> JavaScript compares strings using `Unicode` (numeric character codes).

```javascript
// Inequality example:

let hasPizza;

if (hasPizza != true) { // Is hasPizza different from true?
  orderPizza();
} else {
  cook();
}

eat();

// Strict inequality example:

let hasPizza;

if (hasPizza !== true) { // Is hasPizza different from true and also a different type?
  orderPizza();
} else {
  cook();
}

eat();

// Greater than and less than example:

// Whe can check if one word is greater than or less than another word.

let randomWord = "student";

if (randomWord > "angry") {
  console.log(comes next);
} else if (randomWord < "angry") {
  console.log("go first");
}
```

### LOGYCAL OPERATORS

Logical operators evaluate comparison expressions. There are three types:

- AND: `&&`
- OR: `||`
- NOT: `!`

Examples:

```javascript
// AND && logical operator example:
// AND evaluates the expression and returns true only if both conditions are true.

let randomChar = "a";

if (randomChar => "a" && randomChar < "m") {
  console.log("go first");
}

// OR || logical operator example:
// OR evaluates the expression and returns true if at least one condition is true.

let randomChar = "a";

if (randomChar => "a" || randomChar < "m") {
  console.log("go first");
}

// NOT ! logical operator example:
// NOT negates the expression, converting it into its opposite value.

let randomChar = "n";

if (!(randomChar => "a") || !(randomCHar < "m")) { // randomChar isn't greater or equal than "a", or randomChar isn't less than "m"... 
  console.log("comes next");
}
```

## SCOPES

> [!NOTE]
> Imagine that we are parents and we have a child. In this case, with scopes, children can access the information from their parents, but parents cannot access the information form their children.
> 
> Hierarchy order:
> 1. Global scope
> 2. Function scope
> 3. Block scope

### GLOBAL SCOPE

Everything defined in the global scope is accessible throughout the entire script.

### FUNCTION SCOPE

This refers to the context inside a function. Variables declared inside a function are only accessible within that function.

### BLOQUE SCOPE

This refers to the context inside a block (such has `if`, `for`, etc.). Variables declared with `let` or `const` are only accessible within that block.

Example:

```javascript
let company = "GitHub"; // Global scope 🌍
const year = 2026; // Global scope 🌍

function getAcademyInfo() {
  let format = "Form " + company; // function scope 👶

  if (!year) {
    let format = "Make in " + company; // block scope 🧑
    return format;
  }

  return format + " in " + year;
}
```

## JAVASCRIPT IN THE WEB

How can I use JavaScript on the web?

> To use JavaScript in web development, an HTML page is required. There are two ways to include scripts.

1. Include scripts externally:

   ```html
    <script src='my_script.js'></script> <!-- external file -->
   ```

2. Include scripts inline:

   ```javascript
    <script>
      console.log("Hello web world!"); // in the same file
    </script>
   ```

### WEB API (APLICATION PROGRAMMING INTERFACE)

A Web API is an interface that allows JavaScript to interact with the browser and the web. There are two main parts: JavaScript and the browser.

You can think of a Web API as a translator. For example, if you speak Spanish and another person speaks English, the web API acts like a translator between you. If you say "¿Dónde están los baños?", the translator says "Where are the bathrooms?".

#### DOCUMENT OBJECT MODEL (DOM)

> [!NOTE]
> The DOM is part of the Web API.

- It represents the structure and content of a web page in memory.
- It has a tree structure.
- Each HTML element in the DOM is called a node.
- Using the DOM, you can modify a web page:

  - Modify elements.
  - Add elements.
  - Delete elements.
  - Show or hide elements.

##### DOM INTERFACES

> [!NOTE]
> Allow us to interact with the browser.

**WEB API**: You can consult [here](https://developer.mozilla.org/en-US/docs/Web/API#interfaces) things about the web development.

- Window: Represents a window that have at DOM.
- Document: Represents the DOM itself.
- Event: Represents a event in the DOM
- Element: Represens a node in the DOM.

##### DOM EVENTS // CORREGIR

- Element.Click

  - This event is triggered when you click on an element in the DOM.
  - It's a mouse event.
  - A click means pressing and releasing the main mouse button.
  - It refers to the primary mouse button.
  - It includes event properties such as mouse position (X and Y) and whether a key was pressed during the click.
 
  ```javascript
    let linkRegister = document.querySelector("a.register");

    linkRegister.addEventListener("click", function(event) {
      console.log("You click in the register link");
    });
  ```

- Element.ContextMenu

  - This event is triggered when you right-click on an element.
  - It's a mouse event.
  - A click means pressing and releasing the right-click mouse button.
  - It refers to the secondary mouse button.
  - It also provides properties such as mouse position and pressed keys.

- window.BeforeUnload

  - This event is triggered when the page is about to be unloaded.
  - It's a loading/unloading event.
  - It can be used to warn the user before leaving the page.

- window.Copy

  - This event is triggered when content is copied to the clipboard.
  - It's a clipboard event.
  - It allows you to control copy behavior on a webpage.

  > [!NOTE]
  > This script prevents content from being copied.

    ```javascript
      window.addEventListener("copy", function(event) {
        event.preventDefault();

        console.warn("Attempt to copy content");
      });
    ```

###### EVENT PROPAGATION

> [!NOTE]
> Events propagate upward through the DOM tree (bubbliing). In many cases, it's better to control this behavior.

```javascript
  let linkRegister = document.querySelector("a.register");

  linkregister.addEventListener("click", function (event) {
    console.info(event);
  });

  document.addEventListener("click", function (event) {
    console.warn(event);
  });
```

> [!NOTE]
> To stop event propagation, you can use: `stopPropagation()` and `stopImmediatePropagation()`.

```javascript
  let linkRegister = document.querySelector("a.register");

  linkRegister.addEventListener("click", function (event) {
    event.stopPropagation();

    console.info(event);
  });

  document.addEventListener("event", function (event) {
    event.stopImmediatePropagation();

    console.warn(event);
  });
```
 
## SYNTAX

> [!IMPORTANT]
> All lines of code should end with a `;`. However, if you omit the semicolon and use a line break instead, JavaScript may automatically insert it. Still, it is better to always write semicolons at the end of each line.

### CASE SENSITIVE

> [!IMPORTANT]
> JavaScript is case-sensitive, so you need to be careful with the names you assign.

### READABILITY

> [!IMPORTANT]
> The use of spaces and tabs is very important for better understanding the code you're writing.

### RESERVED WORDS

> [!IMPORTANT]
> In JavaScript, there are some reserved words that cannot be used as variable names, so you need to be careful not to use them.

Here are some reserved words:

- var
- let
- function
- if
- else
- try
- catch
- for
- while

> [!NOTE]
> Code is typically written in English
