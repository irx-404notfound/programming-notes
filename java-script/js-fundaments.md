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
