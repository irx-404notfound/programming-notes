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

### Naming conventions for functions

-Use camelCase.

function `printCopyright`() {
  console.log("Iraia - 2026");
}

- Use descriptive names.
- Avoid spaces.
- Avoid unnecessary numbers.
- Avoid punctuation marks.
  
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
