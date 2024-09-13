# Javascript quickstart - Essential notes by Renato Lins

  JavaScript was initially created by Brendan Eich in 1995 for Netscape with the specific purpose of enabling scripting capabilities in web browsers. The intention was to develop a scripting language that could be executed by browsers to enhance the interactivity of websites. Since then, JavaScript has evolved to become a versatile and widely-used programming language, not only for client-side scripting in browsers but also for server-side development and a variety of other applications.

---

### 1. Considerations: Why to learn Javascript

__Versatility Across Domains:__ JavaScript is a key player in web development, handling tasks for both front-end and back-end operations with ease. Its versatility isn't limited to the web—it's also a popular choice for mobile apps, games, IoT projects, desktop applications, and beyond. This wide-ranging application underscores its universal appeal and practicality across different domains.

__Multi-Paradigm Language:__ JavaScript is a multi-paradigm language, accommodating both object-oriented and functional programming styles, providing flexibility for developers.

__Frameworks and Libraries:__ Robust frameworks and libraries like React, Angular, and Vue.js expedite development, particularly for crafting intricate user interfaces and Single Page Applications (SPAs).

__NPM Ecosystem:__ The Node Package Manager (NPM) hosts a rich ecosystem of open-source packages, providing developers with a treasure trove of tools and resources to accelerate development.

__Easy Start-Up:__ JavaScript is easy to get started with – all you need is a text editor and a browser, tools that are present on almost all computers.

__Productive Development Environment:__ JavaScript facilitates a productive development environment, allowing for rapid prototyping and efficient coding practices.

__Active Community and Job Opportunities:__ JavaScript's vibrant community offers support, tutorials, and a wealth of resources. Proficiency in JavaScript is in high demand, translating to a plethora of job opportunities in the tech industry.

Ps. If you're new to JavaScript and not familiar with coding environments, I recommend starting with __jsfiddle.net__ to write your initial lines of code. To observe your code in action, simply type it in the 'JavaScript' tab and click 'Run.' If you wish to view values outputted to the console (as demonstrated in future examples using the console.log command), press F12, and you'll find the output under the 'Console' tab.

---

### 2. Variables:

A variable is a named storage location in your computer's memory. Think of it as a labeled box where you can store and retrieve information. You create a variable in JavaScript using the ```var```, ```let```, or ```const``` keywords, followed by the variable name.

```javascript
// Example of declaring a variable using 'var'
var message;
message = "Hello, JavaScript!";

// Example of declaring and assigning a variable using 'let'
let number = 42;

// Example of declaring a constant variable using 'const'
const PI = 3.14;
```

Ps. The differences between ```var```, ```let```, and ```const``` will be discussed further once this tutorial has provided the necessary background.

---

### 3. Data types:

JavaScript has several data types, each serving a specific purpose. The main ones include:

__String:__ Represents text and is enclosed in single or double quotes.

```javascript
let greeting = "Hello, World!";
```

__Number:__ Represents numerical values, including integers and floating-point numbers.

```javascript
let age = 25;
```

__Boolean:__ Represents either true or false, often used for logical operations.

```javascript
let isCodingFun = true;
```

__Array:__ Represents a sequentially ordered list of values, where the first value is assigned to position 0, the second to position 1, and so on.

```javascript
let colors = ["red", "green", "blue"];
console.log(colors[0]) // Output: red
```

__Object:__ Represents a collection of key-value pairs.

```javascript
let person = {
  age: 30,
  name: "John",
  isStudent: false
};
```

By now, you don't have to delve into every data type nuance, but it's crucial to understand the separation in JavaScript. Primitive types, such as strings, numbers, booleans, undefined, null, and symbols, are simple and unchangeable. Non-primitive (reference) types, such as objects, arrays, and functions, are a bit more complex in structure and can be created in various formats.

---

### 4. Type conversion:

Type conversion in JavaScript refers to the process of converting a value from one data type to another. This can happen automatically (implicit conversion) or explicitly (when you manually convert a type).

__Implicit Type Conversion (Type Coercion):__ JavaScript automatically converts types during certain operations. This is called coercion.

- Example 1: String to Number: When using the `+` operator with a string and a number, JavaScript will convert the number to a string and then concatenate.

```javascript
let result = "5" + 3;
console.log(result); // "53" (3 is converted to string "3")
```

- Example 2: Boolean to Number: 
When performing arithmetic operations on booleans, JavaScript converts `true` to `1` and `false` to `0`.

```javascript
let result = true + 2;
console.log(result); // 3 (true is converted to 1)
```

__Explicit Type Conversion:__ You can manually convert data types using global JavaScript functions like `Number()`, `String()`, `Boolean()`, and `parseInt()`.

- Example 1: String to Number: You can explicitly convert a string to a number using the `Number()` function.

```javascript
let str = "123";
let num = Number(str);
console.log(num); // 123 (as a number)
```

- Example 2: Number to String: You can convert a number to a string using the `String()` function or `toString()` method.

```javascript
let num = 456;
let str = String(num);
console.log(str); // "456" (as a string)

let str2 = num.toString();
console.log(str2); // "456" (also as a string)
```

- Example 3: String to Boolean: Non-empty strings convert to `true`, and an empty string converts to `false`.

```javascript
let bool1 = Boolean("hello");
console.log(bool1); // true

let bool2 = Boolean("");
console.log(bool2); // false
```

- Example 4: Number to Boolean: Any non-zero number converts to `true`, while `0` converts to `false`.

```javascript
let bool1 = Boolean(1);
console.log(bool1); // true

let bool2 = Boolean(0);
console.log(bool2); // false
```

- Example 5: Parsing Integers and Floats: The `parseInt()` and `parseFloat()` functions are used to parse a string and return an integer or a floating-point number, respectively.

```javascript
let num1 = parseInt("123.45");
console.log(num1); // 123 (integer)

let num2 = parseFloat("123.45");
console.log(num2); // 123.45 (floating-point number)
```

---

### 5. Operators:

Operators in JavaScript are powerful symbols that perform operations on variables and values. They allow you to create expressions, combining and manipulating data. Let's explore some fundamental operators with code examples:

__Assignment Operator (=):__ Assigns a value to a variable (as seen previously).

```javascript
let x = 10;
```

__Arithmetic Operators (+, -, , /, %):__ Perform basic mathematical operations.

```javascript
let sum = 5 + 3;     // Calculate sum: 5 + 3 = 8
let difference = 7 - 2;  // Calculate difference: 7 - 2 = 5
let product = 4 * 6;     // Calculate product: 4 * 6 = 24
let quotient = 10 / 2;   // Calculate quotient: 10 / 2 = 5
let remainder = 15 % 4;  // Calculate remainder: 15 % 4 = 3
```

__Comparison Operators (==, ===, !=, !==, >, <, >=, <=):__ Compare values and return a Boolean result.

```javascript
/* Equality Operator (==): Compares values and perform a implicit conversion 
of data types if needed, which is called 'type coercion' */
let isEqual = (5 == '5');   // true, values are equal after type coercion

// Strict Equality Operator (===): Compares values and data types, no type coercion
let isStrictEqual = (5 === '5');  // false due to different data types

// Inequality Operator (!=): Compares values, performs type coercion if needed
let isNotEqual = (10 != '10');   // false, values are equal after type coercion

// Strict Inequality Operator (!==): Compares values and data types, no type coercion
let isNotStrictEqual = (10 !== '10');  // true, values are not equal due to different data types

// Greater Than Operator (>): Checks if the left operand is greater than the right operand
let isGreaterThan = (15 > 10);   // true, 15 is greater than 10

// Less Than Operator (<): Checks if the left operand is less than the right operand
let isLessThan = (5 < 8);       // true, 5 is less than 8

/* Greater Than or Equal To Operator (>=): Checks if the left operand is greater
than or equal to the right operand */
let isGreaterOrEqual = (20 >= 20);  // true, 20 is equal to 20

/* Less Than or Equal To Operator (<=): Checks if the left operand is less than or equal 
to the right operand */
let isLessOrEqual = (30 <= 25);     // false, 30 is not less than or equal to 25
```

With the knowledge we've gained so far, we can chain operators and variables to craft more elaborate comparisons:

```javascript
const x = 10;
const y = 15;
const z = 5;

// Chaining Comparison Operators
const isInRange = x < y && y > z;  // Evaluates to true if x is less than y and y is greater than z

// Another example
const isValid = x === 10 || (y < 20 && z >= 5);  
/* The expression above evaluates to true if x is exactly 10 or if y is less than 20 
and z is greater than or equal to 5 */
```

In both comparisons above, the expression will be evaluated to __true__.

Best Practice Tip: It's advisable to become accustomed to using strict equality and inequality operators (===, !==). These operators not only compare values but also consider data types, enhancing the robustness of our code.

__Logical Operators (&&, ||, !):__ Combine multiple conditions and perform logical comparisons to determine whether an expression is ```true``` or ```false```.

```javascript
// Logical AND (&&):
let isTrue = (true && false); // false

// Logical OR (||):
let isEitherTrue = (true || false); // true

// Logical NOT (!):
let isNotTrue = !true; // false
```

__Unary Operators (++, --):__ Increment or decrement a variable by 1.

```javascript
let counter = 5;
counter++;     // Increment by 1
counter--;     // Decrement by 1
```

__String Concatenation Operator (+):__ Concatenates two or more strings.

```javascript
let firstName = 'John';
let lastName = 'Doe';
let fullName = firstName + ' ' + lastName;  // 'John Doe'
```

---

### 6. Control flow I - 'if' statement

In JavaScript, the ```if``` statement is used to conditionally execute a block of code. It allows you to specify a condition, and if that condition evaluates to true, the code inside the if block will be executed. If the condition is false, the code inside the if block will be skipped. Let's look at a simple example:

```javascript
let temperature = 25;

if (temperature > 20) {
  console.log("It's a warm day!");
}
```

In this example, if the temperature variable is greater than 20, the message "It's a warm day!" will be logged to the console. You can also use an else statement to specify a block of code that will be executed if the condition in the ```if``` statement is ```false```:

```javascript
let temperature = 25;

if (temperature > 20) {
  console.log("It's a warm day!");
} else {
  console.log("It's a cool day.");
}
```

In this case, if the temperature is not greater than 20, the message "It's a cool day." will be logged. You can also chain multiple conditions using ```else if```:

```javascript
let temperature = 25;

if (temperature > 30) {
  console.log("It's a hot day!");
} else if (temperature > 20) {
  console.log("It's a warm day!");
} else {
  console.log("It's a cool day.");
}
```

Here, if the temperature is greater than 30, the message "It's a hot day!" will be logged. If the temperature is not greater than 30 but is greater than 20, the message "It's a warm day!" will be logged. Otherwise, the message "It's a cool day." will be logged.

Ps. These are just basic examples, and ```if``` statements can become more complex with logical operators, ternary operators, and other JavaScript features.

__Ternary Operators__: In JavaScript, the ternary operator provides a concise way to write simple conditional statements. It's a shorthand for an if-else statement. The syntax is:

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

Here's an example to illustrate its usage:

```javascript
// Example 1: Using Ternary Operator for Assignment
let isSunny = true;
let activity = isSunny ? "Go for a walk" : "Stay indoors";

console.log(activity);  // Output: "Go for a walk"

let number = 15;
let parity = number % 2 === 0 ? "Even" : "Odd";

console.log(parity);  // Output: "Odd"
```

Chaining ternary operators for complex conditions is possible but may result in confusing code if not used carefully. Here's an example that may be considered readable by some and not by others:

```javascript
let age = 25;
let hasLicense = true;

let eligibility = age >= 18
  ? hasLicense
    ? "Allowed to drive"
    : "Cannot drive without a license"
  : "Too young to drive";
```

Explanation: The first ternary operator checks if the age is greater than or equal to 18. If ```true```, it proceeds to the next ternary operator, checking if hasLicense is true.
If both conditions are true, it assigns "Allowed to drive"; otherwise, it assigns "Cannot drive without a license". If the initial age condition is ```false```, it assigns "Too young to drive".

---

### 7. Control Flow II - Falsy and Truthy Values

In JavaScript, values can be broadly categorized into two groups: truthy and falsy.

__Truthy Values:__ A value is truthy if, when used in a condition (like in an if statement), it's treated as ```true```. For example, any non-empty string, any number other than 0, true, or any non-empty object is truthy.

__Falsy Values:__ A value is falsy if, in a condition, it's treated as ```false```. Examples include false, the number 0, an empty string (""), ```null```, ```undefined```, and ```NaN``` (which stands for Not a Number).

Here's are two basic examples:

```javascript
if ("Hello") {
  // This code will run because "Hello" is truthy
  console.log("Truthy!");
}

if (0) {
  // This code won't run because 0 is falsy
  console.log("Falsy!");
}
```

__Default value:__ The "default value" or "fallback pattern" is a concise way to assign a default value to a variable if the initial value is falsy. The pattern typically involves using the logical OR (||) operator. Here's an example to illustrate the concept:

```javascript
// Example 1:
let myVar = "Hello, World!";
let message = myVar || "Default Value";

console.log(message);  // Output: "Hello, World!"
```

---

### 8. Control flow III - Loops

__'for' loop:__ The ```for``` loop is used when you know the number of iterations in advance.

```javascript
// Example: Print numbers from 1 to 5 using a for loop
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

__'while' loop:__ The ```while``` loop is used when the number of iterations is not known in advance, and the loop continues as long as a specified condition is ```true```.

```javascript
// Example: Print numbers from 1 to 5 using a while loop
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

__'do-while' loop:__ Similar to the ```while``` loop, but the condition is checked after the loop block is executed, ensuring that the block is executed at least once.

```javascript
// Example: Print numbers from 1 to 5 using a do-while loop
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);
```

__Looping through arrays:__ While coding, we might often use loops to iterate over the elements of an array. So, the immediate code that comes to mind for doing so is:

```javascript
// Example: Iterate through an array using a for loop
const colors = ['red', 'green', 'blue'];

for (let i = 0; i < colors.length; i++) { // Not recommended, see further explanation ahead.
  console.log(colors[i]);
}
```

But there is a small problem in the code above, especially if we are looping through huge arrays or performing computationally intense tasks on each iteration. When we bring ```colors.length``` into the loop, we are making the JavaScript interpreter check/calculate the length of our array each time an iteration is executed. In some cases, this can impact how performant the code runs. In this case, we can think of something called __code refactoring__, which is nothing more than improving code that is already there but is not solving problems in an optimal way. For that particular case, we better store ```colors.length``` in a ```const``` and then start the loop code:

```javascript
// Example: Iterate through an array using a for loop
const colors = ['red', 'green', 'blue'];
const colorsLength = colors.length; 

for (let i = 0; i < colorsLength ; i++) { 
  console.log(colors[i]); // Same output as before, but potentially with improved performance.
}
```

Even when the performance difference cannot be noticed, approaches like the one explained above are considered to be part of what we call __programming best practices__.

Ps. We can also iterate through arrays using the ```array.map()``` method, which will be covered later in this same tutorial.

__'for...of' loop:__ This loop in JavaScript is used to iterate over iterable objects, such as arrays, strings, and other iterable collections. It provides a more concise syntax for iterating over the values of an iterable compared to the traditional for loop. Check these examples:

```javascript
// Using for...of loop with arrays
const colors = ['red', 'green', 'blue'];

for (const color of colors) {
  console.log(color);
}

// Using for...of loop with strings
const message = 'Hello';

for (const char of message) {
  console.log(char);
}

// Using for...of loop with objects
const person = {
  name: 'John',
  age: 30,
  city: 'New York',
};

// Object entries() method to convert object properties to an iterable
for (const [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}
```

Considerations while using __for...of__:

* Syntax: The ```for``` loop is more general-purpose and has a more complex syntax, allowing for more flexibility in controlling the iteration process. The ```for...of``` loop provides a simpler syntax specifically designed for iterating over iterable elements, making the code more readable and concise.

* Iterating over Values: In a ```for``` loop, you typically use an index to access elements by their position in the array or collection. In a ```for...of``` loop, you directly iterate over the values of the iterable, making it more convenient for scenarios where you are interested in the values themselves rather than their indices.

* Performance: For simple array iteration, the performance difference between the two is negligible. In more complex scenarios or with large datasets, micro-benchmarks might show differences, but these differences are unlikely to be noticeable in typical applications.

* Use cases: If you only need the values and not the indices, a ```for...of``` loop is often more concise and easier to read. If you really need both the index and the value during iteration, using a traditional ```for``` loop might be more appropriate.

__Loop control statements:__ JavaScript provides loop control statements like ```break``` and ```continue``` to alter the flow of a loop. 

```javascript
// Example 1: Use break to exit a loop early
for (let i = 1; i <= 10; i++) {
  if (i === 5) {
    break; // Exit the loop when i is 5
  }
  console.log(i); // Shows 1 to 4
}

// Example 2: Use continue to skip the current iteration
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    continue; // Skip the iteration when i is 3
  }
  console.log(i); // Shows 1 to 5 excluding 3
}
```

__IMPORTANT CONSIDERATION__: Loops are one of the most frequently used features in any programming language, and JavaScript provides these and other ways to loop through values. Having a good understanding of loops (in any language) is never a 'time wasted,' considering how often they are used. That's why I've decided to incorporate some 'best practices' and 'performance' tips into the __loops__ topic, even though this tutorial is tailored for beginners.

---

### 9. Control flow IV - switch-case statements

In JavaScript, the ```switch``` statement allows code to be executed once the ```case``` statement is fulfilled. By using ```switch-case```, we have a concise way to handle multiple scenarios for a given expression. Here's an example:

```javascript
let day = 'Friday';

switch (day) {
  case 'Monday':
    console.log('It\'s the start of the week.');
    break;
  case 'Friday': // Once case statement is fulfilled:
    console.log('It\'s almost the weekend!'); // this is the line that will log the message
    break; // and this line will make the execution to stop
  default:
    console.log('Enjoy your day.');
}
```

Here's a brief explanation of how the switch statement works:

* The expression is evaluated once.
* The value of the expression is compared with the values of each case.
* If there is a match, the corresponding block of code is executed.
* The ```break``` statement is used to exit the switch block after a match. Without break, the control will fall through to the next case, even if it doesn't match.
* If no cases match, the default block (if present) is executed.

__When to use:__ Use ```switch-case``` when you have multiple conditions to check against a single expression. It provides a cleaner alternative to a series of ```if-else``` statements. The ```switch-case``` is suitable when you need to perform strict equality (just like when using ```===```).

__When not to use:__ If your conditions involve complex expressions or ranges, using ```switch-case``` might not be the most suitable choice. In such cases, consider using ```if-else``` statements. If your cases involve non-constant expressions (that will be evaluated), it might lead to unexpected behavior. Also it is important to avoid changing the value of the expression within the ```switch``` block, as it can lead to unpredictable results.

__Performance considerations:__ When checking a small number of conditions, the performance difference between ```switch``` and ```if-else``` is typically negligible. Modern JavaScript engines are optimized to handle both constructs efficiently. In practice, the choice between ```switch``` over ```if-else``` should be based on code readability and maintainability, not aiming to improve the performance by some miliseconds. In some complex scenarios, ```if-else``` statements can be faster than ```switch-case```, but having to worry about this is not considered typical.

Note: In the example provided, the use of ```\``` within the ```console.log``` statement ensures that the JavaScript interpreter does not become confused by the single quotes used to delimitate the string text.

---

### 10. Basics of functions

In JavaScript, functions are blocks of reusable code that can be defined and called upon to perform a specific task. They play a crucial role in organizing and structuring code, promoting reusability, and enhancing maintainability. There are two common ways to define functions in JavaScript: function declarations and function expressions.

__Function Declaration:__ A function declaration is a way to define a function with the function keyword, followed by the function name, a list of parameters enclosed in parentheses, and a block of code enclosed in curly braces.

```javascript
// Defining the function
function add(x, y) {
  // Calculating the sum of x and y
  const sum = x + y;
  
  // Returning the calculated sum
  return sum;
}

// Calling the function and storing the returned value in a 'const'
const mySum = add(3, 7);

// Displaying the result
console.log(mySum) // Output: 10
```

In this example:

* __add__ is the function name
* __(x, y)__ are the parameters or 'placeholders' that represent the data that the function is receiving when called
* __const sum = x + y;__ represents the function body, where the actual code is executed
* __return sum;__ is result returned after the code is executed

In JavaScript, a function declaration must have a name. The syntax for a function declaration includes the ```function``` keyword followed by the name of the function, a list of parameters enclosed in parentheses, and a block of code enclosed in curly braces. This idea is not true for function expressions (they are nameless), as we will see next.

__Function Expression:__ A function expression is another way to define a function by assigning it to a variable. This can be done using the function keyword or the more modern arrow function syntax (=>).

```javascript
// Example 1 - Using function keyword

// Defining the function while storing it as a value (as part of an expression)
const subtract = function(x, y) {
  return x - y;
};

// Calling the function and storing the returned value in a 'const'
const mySubtract = subtract(7, 3);

// Displaying the result
console.log(mySubtract) // Output: 4
```

```javascript
// Example 2 - arrow function with the arrow syntax

// Also defining the function and storing it as a value
const subtract = (x, y) => x - y;

// Calling the arrow function (nothing changes)
const mySubtract = subtract(7, 3);

// Displaying the result
console.log(mySubtract); // Output: 4
```

In both examples, the functions themselves are nameless, yet we can reference them by associating them to values. Consequently, we call ```subtract()``` as if it were a function, while, in reality, it is a variable storing a nameless function expression. The term "nameless" refers to the fact that the functions themselves don't have a separate identifier, but they are effectively named through the variables to which they are assigned.

__Function declaration vs. function expressions:__ For routine programming tasks, functions can be declared using either named or anonymous approaches. Named functions are particularly beneficial for self-referencing, such as in recursive functions, and they contribute to clearer stack traces during debugging, potentially easing the identification of functions causing issues. In the majority of scenarios, there is no substantial performance difference between named and anonymous functions. Modern JavaScript engines are optimized to efficiently handle both types. However, in certain extreme cases, named functions might exhibit a marginal speed advantage due to potential optimizations in specific JavaScript engines. Nevertheless, arrow functions are often preferred not just for their modern and concise syntax but also for their predictability, especially when developers navigate thru intermediary to advanced concepts like __hoisting__ and __context__.

__Types of arrow functions:__ Arrow functions provide a concise syntax for writing functions. There are two main forms of arrow functions: the short syntax for one-liner functions, and the long syntax for functions with multiple statements or requiring a more explicit structure.

* Short Syntax (One-Liner Arrow Functions as seen previously): Here the ```return``` statement is implicit and does not require curly braces.

```javascript
// Short syntax for squaring a number
const square = (x) => x * x;
```

* Long Syntax (Block Body Arrow Functions): The long syntax is used when a function requires multiple statements or a more explicit structure. It involves using curly braces ```{}``` to define a block of code. The ```return``` statement is needed explicitly if the function is expected to return a value.

```javascript
// Long syntax for a function with conditional logic
const greet = (timeOfDay) => {
  if (timeOfDay === 'morning') {
    return 'Good morning!';
  } else {
    return 'Hello!';
  }
};
```

---

### 11. Scope

In JavaScript, scope refers to the visibility and accessibility of variables, functions, and objects within your code. Understanding scope is crucial because it determines where variables and functions are accessible and where they are not. There are primarily three types of scope in JavaScript: block scope, function scope, and global scope (often referred to as window scope in browser environments).

__Block Scope:__ Introduced with ES6 (ECMAScript 2015), block scope allows you to define variables that are limited in visibility to a specific block of code, such as inside an if statement, for loop, or a block denoted by curly braces `{}`. Variables declared with `let` and `const` have block scope, which means they are only accessible within the block in which they are defined. Example of block scope:

```javascript
if (true) {
    let myValue = 10; // block-scoped variable
    console.log(myValue); // 10
}
console.log(myValue); // Uncaught ReferenceError: myValue is not defined
```

__Function Scope:__ In JavaScript, variables declared with var (pre-ES6) are function-scoped. This means they are accessible within the function in which they are defined (including nested functions), but not outside of that function. Function parameters are also function-scoped. Example of function scope:

```javascript
function myFunction() {
    var myValue = 20; // function-scoped variable
    console.log(myValue); // 20
}
myFunction();
console.log(myValue); // Uncaught ReferenceError: myValue is not defined
```

__Global Scope (Window Scope):__ Variables declared outside of any function or block have global scope. They are accessible throughout your entire code, including within functions and blocks. In browser environments, global variables are properties of the window object. Example of global scope:

```javascript
var globalVar = 30; // global variable
function anotherFunction() {
    console.log(globalVar); // 30
}
anotherFunction();
console.log(globalVar); // 30
```

__Hoisting:__ JavaScript hoisting is a behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase, before the code is executed. This means that you can access variables and functions even before they are declared in your code. Here's a short example to illustrate hoisting:

```javascript
console.log(myVar); // undefined
var myVar = 10;
console.log(myVar); // 10

myFunction(); // Hoisted
function myFunction() {
    console.log("Hello, hoisting!");
}
```

In this example:

The variable `myVar` is hoisted, which means the declaration `var myVar;` is moved to the top of the current scope. However, the assignment `myVar = 10;` remains in place. When you try to log `myVar` before its assignment, it prints `undefined` because only the declaration is hoisted, not the initialization. The function `myFunction` is also hoisted entirely, including its definition and implementation. So you can call `myFunction()` before its actual declaration in the code.

Regarding the hoisting behavior in Javascript we have: `var` declarations are hoisted to the top of their scope but remain undefined until initialized. `let` and `const` declarations are hoisted as well but stay inaccessible until their actual declaration, causing a `ReferenceError` if accessed earlier. `Function` declarations are entirely hoisted, allowing their use before declaration. Function expressions are hoisted as variables, meaning that the variable declaration itself is hoisted to the top of its containing scope, but the assignment (which is the actual function expression) remains at its original position in the code. 

It is important to note that hoisting only moves declarations, not initializations or assignments. Understanding hoisting helps in writing cleaner and more predictable JavaScript code while considering the scope of variables and functions.

__Best practices related to scope:__

* Avoid Global Variables: Limit the use of global variables to avoid polluting the global scope. Encapsulate your code within functions or modules to reduce the risk of naming conflicts and improve code maintainability.

* Use Block Scope with `let` and `const`: Avoid using `var` because it can lead to potential bugs in JavaScript code. Instead, leverage block scope with `let` and `const` to confine variables to the smallest possible scope, thereby improving code readability and reducing potential bugs.

* Avoid Creating Implicit Global Variables: Always declare variables using keywords such as `let` and `const` within the appropriate scope. Omitting the declaration keyword can unintentionally create global variables, leading to unexpected behavior and bugs.

* Enable Strict Mode: Use strict mode (`"use strict";`) to enforce stricter rules and catch common coding mistakes related to variable scoping, undeclared variables, etc.

* Use Immediately Invoked Function Expressions (IIFE): In main scripts, especially in traditional JavaScript applications or scripts included directly in HTML files, IIFE is often used to prevent variable and function name clashes with other scripts and libraries. It helps create a private scope where variables and functions defined inside the IIFE are not accessible outside, reducing the risk of conflicts and improving code organization.


```javascript
(function() {
    // Private scope
    var localVar = 10;

    function privateFunction() {
        console.log("Private function");
    }

    // Code inside the IIFE
})();
```

* Avoid using IIFE within ES6 modules: In modern JavaScript development with ES6 modules (import/export), using IIFE can be unnecessary and problematic. ES6 modules inherently offer encapsulation, preventing global scope pollution, with each module having its own scope where variables/functions are only accessible within the module unless explicitly exported/imported. This avoids unnecessary complexity and potential interference with the module system, such as hoisting and module dependencies. 

Example of a module without IIFE:

```javascript
// module.js
var moduleVar = 20;

function moduleFunction() {
    console.log("Module function");
}

export { moduleVar, moduleFunction };
```

```javascript
// main.js
import { moduleVar, moduleFunction } from './module.js';

console.log(moduleVar); // Accessing moduleVar from the module
moduleFunction(); // Calling moduleFunction from the module
```

---

### 12. String manipulation - Useful approaches and methods

__Concatenation:__ Concatenation is the process of combining strings. Example: 

```javascript
const firstName = "John";
const lastName = "Doe";

const fullName = firstName + " " + lastName;

console.log(fullName); // Output: John Doe
```

__Template Literals:__ Template literals provide a more convenient way to create strings with embedded expressions, making concatenation with ```+``` not that necessary for most cases. Example:

```javascript
const name = "Alice";
const age = 30;

const greetingMessage = `Hello, ${name}! You are ${age} years old.`;

console.log(greetingMessage); // Output: Hello, Alice! You are 30 years old. 
```

__.length:__ The ```.length``` is a property of strings in JavaScript that is used to retrieve the number of characters a string has. Example:

```javascript
const greeting = "Hello, JavaScript!";
const lengthOfGreeting = greeting.length;

console.log(`The length of the greeting is ${lengthOfGreeting} characters.`);
```

Note: Under the hood, the ```.length``` property behaves like a function that retrieves the number of characters in a string. Despite being accessed without parentheses like a typical function or method, it involves computation and is not a fixed value. The ```.length``` calculates and returns a value, so we can say we are obtaining a computed property.

__.trim():__ The ```.trim()``` method removes whitespace from both ends of a string.

Example: Removing leading and trailing whitespace

```javascript
const spacedString = "   Trim me!   ";
const trimmedString = spacedString.trim();

console.log(`Original String: "${spacedString}"`);
console.log(`Trimmed String: "${trimmedString}"`);
```

__.substring():__ The ```.substring()``` method extracts a portion of a string between two specified indices.

Example: Extracting a substring

```javascript
const sentence = "This is a sample sentence.";

// Extract a substring from index 5 to 10 (excluding 10)
const substring = sentence.substring(5, 10);

console.log(`Substring: ${substring}`); // Output: Substring: is a 
```

__.toUpperCase() and .toLowerCase():__ These methods are used to convert a string to uppercase or lowercase, respectively. Let's see:

```javascript
// Original mixed-case string
const mixedCase = "My teXt MesSage";

// Convert the string to uppercase
const upperCase = mixedCase.toUpperCase();

// Convert the string to lowercase
const lowerCase = mixedCase.toLowerCase();

// Log the uppercase and lowercase versions to the console
console.log(`Uppercase: ${upperCase}`);
// Output: Uppercase: MY TEXT MESSAGE

console.log(`Lowercase: ${lowerCase}`);
// Output: Lowercase: my text message
```

__.replace():__ This method in JavaScript is used to search for a specified value (searchValue) in a string and replace it with another value (replaceValue). Example:

```javascript
const str = "Hello, World!";
console.log(str.replace("World", "Universe")); // Outputs "Hello, Universe!"
```

In JavaScript, a multitude of string methods, including ```.indexOf()```, ```.charAt()```, ```.slice()```, ```.concat()```, and more, are at your disposal. Remember you can always consult references for the language, such as MDN or W3Schools. 

Ps. If you want to get a more in-depth understanding, you can delve into the ECMAScript Language Specifications (which is normally considered advanced), once it is a series of standards upon which JavaScript is built.

---

### 13. Essential array methods (.map(), .find(), .filter())

In JavaScript, ```.map()```, ```.filter()```, and ```.find()``` are essential array methods, offering concise and expressive ways to transform, filter, and retrieve elements. Often associated with modern coding approaches such as functional programming, they play a crucial role in enhancing code readability and maintainability, making them essential tools for effective JavaScript development.

__.map():__ The ```.map()``` method is used to transform each element of an array by applying a provided function to it. It creates a new array containing the results of applying the function to each element of the original array.

Example: Doubling each element in an array

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map(function (num) {
  return num * 2;
});

console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

In this example, the ```.map()``` method applies the function ```(num) => num * 2``` to each element in the numbers array, resulting in a new array where each element is doubled.

__.find():__ The ```.find()``` method is used to retrieve the first element in an array that satisfies a given condition. It stops iterating once the first matching element is found.

Example: Finding the first even number in an array

```javascript
const numbers = [1, 3, 5, 8, 9];

const firstEvenNumber = numbers.find(function (num) {
  return num % 2 === 0;
});

console.log(firstEvenNumber); // Output: 8
```

Here, the ```.find()``` method searches through the numbers array and returns the first element that satisfies the condition ```(num) => num % 2 === 0```, which is the number ```8```.

__.filter():__ The ```.filter()``` method is used to create a new array containing elements that satisfy a given condition. It creates a new array with all elements for which the provided function returns true.

Example: Filtering out odd numbers from an array

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter(function (num) {
  return num % 2 === 0;
});

console.log(evenNumbers); // Output: [2, 4]
```

In this example, the ```.filter()``` method creates a new array (```evenNumbers```) containing only even numbers as per the condition ```(num) => num % 2 === 0```. That way we will get the following array: ```[2, 4]```.

---

### 14. Built-In JavaScript mathematical features

The JavaScript Math object is a built-in feature that provides a wide range of mathematical functions and constants. It enables developers to perform common mathematical operations efficiently within their JavaScript code, offering shortcuts for tasks such as trigonometry, exponentiation, rounding, and more. This object simplifies complex numerical computations, enhancing the functionality of JavaScript applications.

__Mathematical constants:__ In JavaScript, built-in mathematical constants are predefined values that represent fundamental mathematical quantities. We can access these constants as follows:

```javascript
// Pi (π): Represents the ratio of the circumference of a circle to its diameter
const pi = Math.PI; // Approximately 3.14159

// Euler's number (e): Represents the base of the natural logarithm
const e = Math.E; // Approximately 2.71828

// Square root of 2 (√2): Represents the square root of 2
const sqrt2 = Math.SQRT2; // Approximately 1.41421

// Reciprocal of the square root of 2 (1/√2)
const sqrt1_2 = Math.SQRT1_2; // Approximately 0.70711

// Natural logarithm of 2 (ln(2))
const ln2 = Math.LN2; // Approximately 0.69315

// Natural logarithm of 10 (ln(10))
const ln10 = Math.LN10; // Approximately 2.30259
```

Note: While these constants are typically defined precisely in mathematics, their representations in JavaScript (and many other programming languages) are approximations due to the limitations of floating-point arithmetic and the finite precision of computer systems. Therefore, the values provided in JavaScript for these mathematical constants are approximate, but they are accurate enough for most practical purposes in programming and numerical computations.

__Mathematical functions:__ The Math object in JavaScript offers a suite of built-in functions tailored for common mathematical operations. Here's how we can utilize them:

```javascript
// Exponentiation (Math.pow)
const result = Math.pow(2, 3); // result equals 8 (2 raised to the power of 3)

// Square Root (Math.sqrt)
const squareRoot = Math.sqrt(25); // squareRoot equals 5 (square root of 25)

// Absolute Value (Math.abs)
const absoluteValue = Math.abs(-10); // absoluteValue equals 10 (absolute value of -10)

// Trigonometric Functions: sine (Math.sin), cosine (Math.cos), tangent (Math.tan)
const sineValue = Math.sin(Math.PI / 2); // sineValue equals 1 (sin(π/2) is 1)
const cosineValue = Math.cos(Math.PI); // cosineValue equals -1 (cos(π) is -1)
const tangentValue = Math.tan(0); // tangentValue equals 0 (tan(0) is 0)

// Rounding: Round (Math.round), Ceil (Math.ceil), Floor (Math.floor)
const roundedNumber = Math.round(4.6); // roundedNumber equals 5 (rounds to the nearest integer)
const ceiledNumber = Math.ceil(4.3); // ceiledNumber equals 5 (rounds up to the nearest integer)
const flooredNumber = Math.floor(4.9); // flooredNumber equals 4 (rounds down to the nearest integer)

// Logarithmic Functions: Natural Logarithm (Math.log), Base 10 Logarithm (Math.log10)
const naturalLog = Math.log(Math.E); // naturalLog equals 1 (ln(e) is 1)
const logBase10 = Math.log10(100); // logBase10 equals 2 (log10(100) is 2)
```

---

### 15. Objects and common object methods in JavaScript

In reinforcing a previously mentioned concept in this tutorial, it's worth noting that objects in JavaScript are comprised of key-value pairs. Each key is a string, while each corresponding value can be any data type, encompassing primitive values such as strings, numbers, and booleans, as well as other objects or functions. For instance:

```javascript
// Creating an object with key-value pairs
const person = {
    name: "John",       // key: "name", value: "John"
    age: 30,            // key: "age", value: 30
    address: {          // key: "address", value: an object
        city: "New York",
        country: "USA"
    },
    greet: function() { // key: "greet", value: a function
        console.log("Hello!");
    }
};

// Accessing values using keys
console.log(person.name);          // Output: John
console.log(person.address.city);  // Output: New York

// Calling a function stored as a value
person.greet();  // Output: Hello!
```

__Prototypes and object creation:__ To delve deeper into understanding objects in JavaScript, it's essential to grasp the concept of prototypes and their relationship with objects. Prototypes in JavaScript act as mechanisms enabling objects to inherit properties and methods from other objects. Each object in JavaScript possesses a prototype, functioning as a "template" dictating the object's properties and methods. When accessing a property or method on an object, JavaScript initially checks if the object directly holds that property or method. If not, it traverses the prototype chain to locate the property or method on the object's prototype. Prototypes facilitate code reuse and inheritance in JavaScript, simplifying the creation and management of intricate object structures. Using a constructor function, we can create instances of objects by employing the ```new``` keyword. 

Here's a concise example demonstrating the use of prototypes and object's creation:

```javascript
// Define a function that can be used as a constructor, enabling object creation.
function Person(name) {
  this.name = name;
}

// Add a method to the Person prototype
Person.prototype.greet = function() {
  console.log(`Hello, my name is ${this.name}.`);
};

// Create an instance of Person
const person1 = new Person("John");

// Call the greet method
person1.greet(); // Output: Hello, my name is John.
```

__Common approaches for object creation in Javascript:__ Object Creation in JavaScript involves utilizing different methods to create objects. Here are some common approaches:

1) Object Literals: Objects can be created using object literals, which define the object's properties and values within curly braces {}.

```javascript
const person = {
    name: "John",
    age: 30,
    city: "New York"
};
```

2) Constructor Functions: Constructor functions are used to create multiple objects with similar properties and methods. 

```javascript
function Person(age, name, city) {
    this.age = age;
    this.name = name;
    this.city = city;
}

let person1 = new Person("Alice", 25, "London");
let person2 = new Person("John", 30, "New York");
```

3) Object.create() Method: The ```Object.create()``` method creates a new object with the specified prototype object and properties.

```javascript
let personPrototype = {
    greet: function() {
        console.log("Hello!");
    }
};

let person = Object.create(personPrototype);
```

4) Using classes: In ECMAScript 2015 (ES6) and later versions of JavaScript, the ```class``` keyword was introduced to provide a more familiar syntax for defining classes and constructor functions. This makes object-oriented programming in JavaScript more intuitive, especially for developers transitioning from class-based languages like Java or C++. To create an object using a class in JavaScript (ES6+), we define a class with the ```class``` keyword. 

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

let person1 = new Person("John", 30);
console.log(person1.name); // Output: John
```

These methods provide flexibility in creating and initializing objects in JavaScript to suit different programming needs. So we can consider:

* Object Literals: Perfect for creating simple, static objects with predefined properties.
* Constructor Functions: Best for creating multiple instances of objects with similar properties and behaviors.
* Object.create(): Useful for explicit prototype-based inheritance, allowing properties to be inherited from existing objects.
* ES6 Classes: Offer a clearer and more organized syntax for defining object blueprints and inheritance hierarchies.

NOTE: In JavaScript, when referring to operations that are associated with objects, we typically refer to them as "methods" rather than "functions". This is because they are specifically designed to operate on objects and are accessed using dot notation. However, it's important to note that these methods are still functions in a technical sense—they are just functions that are properties of an object.

__Common object methods in Javascript:__ JavaScript provides a variety of built-in methods designed for object manipulation. Let's explore some common object methods used to handle objects effectively:

1) Object.assign(): Copies properties from one or more source objects to a target object.

```javascript
const target = { number: 10 };
const source = { foo: 1, bar: 2 };
Object.assign(target, source);
console.log(target); // Output: { number: 10, foo: 1, bar: 2 }
```

2) Object.freeze(): Freezes an object, preventing any modifications to its properties.

```javascript
const obj = { prop: 42 };
Object.freeze(obj);
obj.prop = 33; // Attempted modification
console.log(obj.prop); // Output: 42 (no change)
```

3) Object.seal(): Seals an object, preventing new properties from being added and existing properties from being deleted.

```javascript
const obj = { prop: 42 };
Object.seal(obj);
delete obj.prop; // Attempted deletion
console.log(obj.prop); // Output: 42 (property still exists)
```

4) Object.hasOwnProperty(): Checks if an object has a specified property, ignoring properties from the object's prototype chain.

```javascript
const obj = { foo: 1 };
console.log(obj.hasOwnProperty('foo')); // Output: true
console.log(obj.hasOwnProperty('toString')); // Output: false
```

__Constructs and Methods for iterating over objects:__ In JavaScript, there are various methods for iterating over objects:

1) for...in Loop: This loop construct (language built-in feature) helps us to iterates over the enumerable properties of an object, with each iteration providing the property name as the variable ```key```.

```javascript
const persons = {
  person1: { name: 'John', age: 30 },
  person2: { name: 'Alice', age: 25 }
};

// Iterate over object properties
for (let key in persons) {
  console.log(key, persons[key]); // Output: person1 { name: 'John', age: 30 }, person2 { name: 'Alice', age: 25 }
}
```

2) Object.keys(): Returns an array containing the keys of an object.

```javascript
const person = { name: 'John', age: 30 };
const keys = Object.keys(person);
console.log(keys); // Output: ['name', 'age']
```

3) Object.values(): Returns an array containing the values of an object.

```javascript
const person = { name: 'John', age: 30 };
const values = Object.values(person);
console.log(values); // Output: ['John', 30]
```

4) Object.entries(): Returns an array containing arrays of key-value pairs of an object.

```javascript
const person = { name: 'John', age: 30 };
const entries = Object.entries(person);
console.log(entries); // Output: [['name', 'John'], ['age', 30]]
```

These methods provide different ways to iterate over object properties, depending on your specific requirements.

__Object destructuring:__ Object destructuring in JavaScript allows for the extraction of multiple properties from an object and assigns them to variables in a single statement. Example:

```javascript
const person = {
  name: 'John',
  age: 30,
  city: 'New York'
};

// Destructuring assignment
const { name, age, city } = person;

console.log(name); // Output: John
console.log(age); // Output: 30
console.log(city); // Output: New York
```

In this example, object destructuring simplifies the process of extracting properties ```name```, ```age```, and ```city``` from the person object and assigning them to variables of the same name.

__Object merging:__ Object merging in JavaScript can be achieved using the spread syntax (...). This syntax allows you to combine the properties of multiple objects into a single object. Example:

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };

// Merge objects using spread syntax
const mergedObj = { ...obj1, ...obj2 };

console.log(mergedObj); // Output: { a: 1, b: 2, c: 3, d: 4 }
```

In this example, mergedObj contains the combined properties of obj1 and obj2. The spread syntax makes it concise and straightforward to merge objects in JavaScript.

__Javascript Object Notation (JSON) and associated methods:__ JavaScript Object Notation (JSON) is a lightweight and popular data interchange format based on JavaScript object syntax. It's commonly used for transmitting data between a server and client-side applications. Methods associated with the JSON format typically revolve around the concepts of serializing (converting JavaScript objects to JSON strings) and parsing (converting JSON strings back to JavaScript objects) objects that store data. So we have:

1) JSON.stringify(): Converts a JavaScript object into a JSON string.

```javascript
const person = { name: 'John', age: 30 };
const serializedPerson = JSON.stringify(person);
console.log(serializedPerson); // Output the string representation of an object: '{"name":"John","age":30}'
```

2) JSON.parse(): Parses a JSON string and converts it into a JavaScript object.

```javascript
const jsonData = '{"name":"John","age":30}';
const person = JSON.parse(jsonData);
console.log(person.name); // Output: John
console.log(person.age); // Output: 30
```

3) JSON.stringify() with Replacer Function: Allows custom serialization by providing a 'replacer' function.

```javascript
const person = { name: 'John', age: 30, city: 'New York' };

// Convert the object to JSON string, excluding the 'city' property
const jsonData = JSON.stringify(person, (key, value) => (key === 'city' ? undefined : value));

console.log(jsonData); // Output: '{"name":"John","age":30}'
```

4) JSON.parse() with Reviver Function: Allows custom parsing by providing a 'reviver' function.

```javascript
const jsonData = '{"name":"John","age":30}';

// Parse the JSON string doubling the value of 'age' property
const person = JSON.parse(jsonString, (key, value) => (key === 'age' ? value * 2 : value));
console.log(person.age); // Output: 60
```

Note: The replacer function in ```JSON.stringify()``` enables selective serialization, allowing for exclusion or transformation of data. For example, it can be used to convert Date objects to strings. Likewise, the reviver function in ```JSON.parse()``` offers customization during parsing. For example, it can transform string representations of data back into their original formats. These functions provide flexibility in handling JSON data, accommodating various use cases such as data sanitization, transformation, and format compatibility.

---

### 15. A better understanding of null and undefined

In JavaScript, ```null``` and ```undefined``` are both used to represent absence of value, but they have different meanings and use cases. ```null``` is explicitly assigned by developers to indicate that a variable intentionally holds no value. It signifies the absence of any object value. ```undefined```, on the other hand, typically indicates an unintentional absence of value. It is the default value assigned to a variable that has been declared but not yet initialized or assigned a value. Let's say we have a variable ```userName``` that holds the name of a user. If the user hasn't provided their name yet, we might set ```userName``` to ```null``` to indicate the absence of a name intentionally. However, if ```userName``` is ```undefined```, it might indicate a programming error or oversight, such as forgetting to assign a value to userName.

Dealing with ```null``` or ```undefined``` properties within objects in JavaScript requires careful handling to prevent errors. The ```?```, and ```??``` operators provide elegant solutions for this purpose:

 * The ```?``` operator is known as the __optional chaining operator__ and it enables safe access to nested properties within an object. It short-circuits the evaluation if a property along the path is ```null``` or ```undefined```, preventing errors from being thrown.

 ```javascript
 const user = { address: { city: 'New York' } };

// Access the city property within the address object
// If address is null or undefined, no error is thrown
console.log(user.address?.city); // Output: 'New York'
```

 * The ```??``` operator is known as the __nullish coalescing operator__ and it offers a concise way to provide default values for ```null``` or ```undefined``` properties. It returns the right-hand operand if the left-hand operand is ```null``` or ```undefined```, otherwise it returns the left-hand operand.

 ```javascript
 const user = { name: 'John', age: 30, city: null };

// Using ?? for default values
console.log(user.name ?? 'Anonymous'); // Output: 'John'
console.log(user.city ?? 'Unknown'); // Output: 'Unknown' (city is null)
```

Let's illustrate these concepts better with more examples:

```javascript
// Example object with nested properties
const user = {
  id: 1,
  name: "John",
  address: {
    street: "123 Main St",
    city: "New York",
    // comment the line below to see how the code behaves without the null property
    postalCode: null
  }
};

// Using optional chaining and nullish coalescing operators
const postalCode = user.address?.postalCode ?? "N/A";
console.log("Postal code:", postalCode);

// Combining optional chaining with default values using ?? for nested properties
const city = user.address?.city ?? "Unknown City";
console.log("City:", city);
```

It's also important to note that null is an object with a specific type, whereas undefined is a type unto itself. So we will have:

```javascript
console.log(typeof null); // Output: "object"
console.log(typeof undefined); // Output: "undefined"
```

Another important consideration is when defining default values for variables. The ```??``` (nullish coalescing operator) only considers ```null``` or ```undefined``` values, whereas ```||``` (logical OR operator) considers any falsy value. For instance:

```javascript
const result1 = someValue ?? defaultValue; // Uses defaultValue only if someValue is null or undefined
const result2 = someValue || defaultValue; // Uses defaultValue for any falsy value, including null, undefined, 0, false, or empty string
```

Note: The boolean opposite of both ```null``` and ```undefined``` is ```true```. This means that if you use the ```!``` operator on ```null``` or ```undefined```, it will result in ```true```. However, it's important to note that using the ```!``` operator in this context can lead to unintended behavior and is not recommended. It adds unnecessary complexity to the code and can be confusing for others to understand, affecting code readability and increasing the risk of bugs. Here's an example of what NOT to do:

```javascript
// Using the ! operator (NOT recommended for checking null or undefined)
const isPostalCodeNull = !user.address?.postalCode; // This may lead to unintended behavior
console.log("Is postal code null or undefined?", isPostalCodeNull);
```

In that case, the recommended version of the same code would be:

```javascript
// Recommended approach for checking null or undefined
const postalCode = user.address?.postalCode;
const isPostalCodeNull = postalCode === null || postalCode === undefined;
console.log("Is postal code null or undefined?", isPostalCodeNull);
```

### 16. String operations: Manipulation and formatting

JavaScript offers powerful tools for manipulating and formatting strings, essential for tasks like data serialization and text processing. Let's delve into some key string operations and formatting techniques in JavaScript.

1) Concatenation and Interpolation: Concatenation combines strings together, while interpolation embeds expressions within strings for dynamic content.

```javascript
const name = 'Alice';
const greeting = `Hello, ${name}!`; // Using Template Literals for interpolation
console.log(greeting); // Output: Hello, Alice!
```

2) String Length and Accessing Characters: We can determine the length of a string and access individual characters using bracket notation or methods like ```charAt```.

```javascript
const message = 'Welcome!';
console.log(message.length); // Output: 8
console.log(message[0]); // Output: W
console.log(message.charAt(1)); // Output: e
```

3) Case Conversion: Convert strings to uppercase or lowercase using ```toUpperCase``` and ```toLowerCase``` methods.

```javascript
const text = 'Hello, World!';
console.log(text.toUpperCase()); // Output: HELLO, WORLD!
console.log(text.toLowerCase()); // Output: hello, world!
```

4) Substring Extraction: Extract parts of a string using ```substring``` or ```slice``` methods.

```javascript
const sentence = 'JavaScript is amazing!';
console.log(sentence.substring(0, 10)); // Output: JavaScript
console.log(sentence.slice(-8)); // Output: amazing!
```

5) String Search and Replace: Search for substrings and replace them using ```indexOf``` and ```replace``` methods.

```javascript
const phrase = 'Learn JavaScript!';
console.log(phrase.indexOf('JavaScript')); // Output: 6 (index where 'JavaScript' starts)
console.log(phrase.replace('JavaScript', 'Node.js')); // Output: Learn Node.js!
```

6) Formatting Numbers in Strings: Format numbers within strings using ```toFixed``` and ```toLocaleString```. 

```javascript
const price = 19.99;
console.log(`Total: $${price.toFixed(2)}`); // Output: Total: $19.99
const largeNumber = 1000000;
console.log(largeNumber.toLocaleString()); // Output: 1,000,000

// toFixed() is used for decimal formatting, while toLocaleString() adjusts formatting based on the client's language and region settings, including currency symbols and separators.
```

7) Trim Whitespace: We can remove leading and trailing whitespace from strings using the 'trim' methods. So we have:

```trim()```: Removes whitespace characters from both ends of a string.
```trimStart()``` or ```trimLeft()```: Removes whitespace characters from the beginning (left) of a string.
```trimEnd()``` or ```trimRight()```: Removes whitespace characters from the end (right) of a string.

```javascript
const str = '   Hello, World!   ';

// Using trim() to remove whitespace from both ends
const trimmedStr = str.trim();
console.log(trimmedStr); // Output: "Hello, World!"

// Using trimStart() or trimLeft() to remove leading whitespace
const trimmedStartStr = str.trimStart();
console.log(trimmedStartStr); // Output: "Hello, World!   "

// Using trimEnd() or trimRight() to remove trailing whitespace
const trimmedEndStr = str.trimEnd();
console.log(trimmedEndStr); // Output: "   Hello, World!"
```

### 17. JavaScript Naming Conventions

Naming conventions in JavaScript are critical for writing clean, readable, and maintainable code. Following consistent conventions helps in understanding the purpose and scope of variables, functions, classes, and other identifiers. Here are the key conventions:

__Variable Names__: Variable names should be written in __camelCase__. This means the first word is in lowercase and the first letter of each subsequent word is capitalized.

```javascript
let userName = 'Alice';
let totalPrice = 19.99;
```

__Constant Names__: Constants that do not change (often known as "magic numbers" or "configurable values") should be written in uppercase letters with words separated by underscores.

```javascript
const MAX_USERS = 100;
const API_KEY = '12345-abcde';
```

__Function Names__: Function names should also follow __camelCase__ convention.

```javascript
function calculateTotal(price, tax) {
  return price + tax;
}
```

__Class Names__: Class names should be written in __PascalCase__, where each word starts with an uppercase letter.

```javascript
class UserAccount {
  constructor(username, password) {
    this.username = username;
    this.password = password;
  }
}
```

__File Names__: File names should be descriptive and can use kebab-case (all lowercase with hyphens).

```js
user-controller.js
order-service.js
```

__HTML Element IDs and Classes__: IDs and class names in HTML should use kebab-case as well.

```html
<div id="main-container" class="user-profile"></div>
```

__Private Variables and Methods__: While not a true private method, an underscore prefix is often used to indicate that a variable or method is intended for internal use only.

```javascript
class Example {
  constructor() {
    this._privateVariable = 'secret';
  }

  _privateMethod() {
    console.log('This is private');
  }
}
```

These conventions help in understanding the purpose and scope of different identifiers at a glance, making the codebase easier to navigate and maintain. However, there is much more to JavaScript naming conventions than the essentials outlined here. In many situations, naming conventions are defined by team agreements. In other situations, linting (code revision) libraries might suggest or even enforce certain naming conventions. This ensures consistency and adherence to best practices across the entire codebase.

### 18. The NaN Type

 ```NaN``` is a special value in JavaScript that stands for "Not a Number." It indicates that a value is not a legal number. Despite its name, ```NaN``` is considered a type of number. Here are a few concise examples where ```NaN``` is computed in JavaScript:

* Invalid Mathematical Operations:

```javascript
let result = Math.sqrt(-1); // NaN
```

* Operations Involving Non-numeric Values:

```javascript
let result = "hello" / 2; // NaN
```

* Indeterminate Forms:

```javascript
let result = 0 / 0; // NaN
```

* Parsing Failures:

```javascript
let result = parseFloat("text"); // NaN
```

* Using Number Constructor with Non-numeric Strings:

```javascript
let result = Number("text"); // NaN
```

These scenarios highlight common cases where ```NaN``` is produced in JavaScript.

In JavaScript, ```NaN``` itself is considered a value of the number type:

```javascript
console.log(typeof NaN); // "number"
```

```NaN``` is not equal to NaN: One of the most confusing aspects of ```NaN``` is that it is not equal to itself. This behavior is unique and seems a bit counterintuitive:

```javascript
console.log(NaN === NaN); // false
```

The reason why ```NaN``` is not equal to itself (when using ```===```) is because ```NaN``` represents a special value that signifies "Not a Number." It's like saying, "I don't know what this is." So, when JavaScript sees two "I don't knows" (NaN), it doesn't consider them equal. This uniqueness is intentional to differentiate between different instances of NaN and maintain consistency with mathematical operations that result in undefined or unrepresentable values. 

__Verifying ```NaN``` Values in JavaScript:__

The ```isNaN()``` function converts the argument to a number before checking if it is NaN.

```javascript
console.log(isNaN(NaN)); // true
console.log(isNaN("text")); // true (string "text" is converted to NaN)
Number.isNaN Method
```

The ```Number.isNaN()``` checks if the value is ```NaN``` without converting the argument.

```javascript
console.log(Number.isNaN(NaN)); // true
console.log(Number.isNaN("text")); // false (string "text" is not NaN)
```

Side-by-side comparison:

```javascript
// isNaN: Converts to number, less precise.
// Number.isNaN: No conversion, more precise.
console.log(isNaN(10)); // false
console.log(isNaN(NaN)); // true
console.log(isNaN("text")); // true

console.log(Number.isNaN(10)); // false
console.log(Number.isNaN(NaN)); // true
console.log(Number.isNaN("text")); // false
```

Tip: Whenever there's a possibility of JavaScript producing a ```NaN``` value, use ```Number.isNaN()``` for a more precise check of the ```NaN``` type.

### 19. Strict mode

Strict mode helps catch common coding errors and prevents the use of undeclared variables, which can lead to bugs that are harder to identify and fix.

__Enabling Strict Mode:__ To enable strict mode, you can add the following statement at the beginning of your JavaScript file or script:

```javascript
"use strict";
```

Or, if you are using it within a function, you can use:

```javascript
function myFunction() {
  "use strict";
  // Function code
}
```

__Undeclared Variable Error:__ When using strict mode in JavaScript, attempting to assign a value to a variable that has not been declared will result in a ReferenceError. This type of error indicates that the code is trying to reference a variable that does not exist in the current scope.

```javascript
"use strict";
x = 3.14; // Error: x is not defined
```

__Preventing Unsafe Actions:__ It disallows some actions or usage of certain features that are considered unsafe, such as:

- **Assigning values to read-only properties:** Strict mode prevents changes to properties that are not writable.
- **Using the `with` statement:** The `with` statement is not allowed in strict mode due to its potential to introduce ambiguity and confusion.

```javascript
"use strict";
var obj = {};
Object.defineProperty(obj, "prop", { value: 42, writable: false });
obj.prop = 77; // Error: Cannot assign to read-only property 'prop'
```

__Enforcing Better Coding Practices:__ Strict mode enforces stricter parsing and error handling, encouraging better coding practices and making the code more robust. For instance, it requires that all variable names be unique, preventing accidental overwrites:

```javascript
"use strict";
function myFunction(a, a, b) {
  // Error: Duplicate parameter name not allowed in this context
}
```

__Eliminating Silent Errors:__ In non-strict mode, some mistakes might fail silently or not produce errors. Strict mode makes these errors explicit and helps in identifying and fixing them during development. For example:

```javascript
function sum(a, b) {
  "use strict";
  return a + b;
}

sum(10, 20); // 30
sum(10);     // NaN because 'b' is undefined, and 'undefined' + 10 is NaN
```

__Transitioning to Strict Mode__: Always keep in mind that enabling strict mode might cause existing code to behave differently, as it disallows certain actions that were previously allowed. Therefore, it's recommended to test thoroughly when transitioning existing code to strict mode. Additionally, always check for the latest JavaScript language specifications and best practices, as recommendations may evolve over time. By adhering to strict mode, you can write more reliable, maintainable, and secure JavaScript code, making it easier to debug and maintain in the long run.

### 20. Scope I: Types of Scope and Hoisting in JavaScript

Scope in JavaScript defines the context in which variables are accessible. The main types are:

1. **Global Scope**: Variables declared outside any function or block are globally accessible throughout the code.
   
2. **Function Scope**: Variables declared inside a function are only accessible within that function.

3. **Block Scope**: Introduced in ES6, variables declared with `let` and `const` are limited to the nearest set of curly braces `{}`.

Hoisting is a behavior where JavaScript moves variable and function declarations to the top of their scope during compilation. This means variables and functions can be used before they are declared, but only the declarations are hoisted, not the initializations.

Examples:

- Global Scope Example:

```javascript
let globalVar = "I'm global";

function exampleFunction() {
  console.log(globalVar); // Accessible
}

console.log(globalVar); // Accessible
exampleFunction();
```

- Function Scope Example:

```javascript
function localScopeExample() {
  let localVar = "I'm local";
  console.log(localVar); // Accessible
}

localScopeExample();
// console.log(localVar); // Error: localVar is not defined
```

 - Block Scope Example:

```javascript
if (true) {
  let blockVar = "I'm in a block";
  console.log(blockVar); // Accessible
}
// console.log(blockVar); // Error: blockVar is not defined
```

 - Variable Hoisting Example:

```javascript
console.log(hoistedVar); // Outputs: undefined
var hoistedVar = "I'm hoisted";
```

 - Function Hoisting Example:

```javascript
hoistedFunction(); // Works
function hoistedFunction() {
  console.log("I'm a hoisted function");
}
```

- Function Expression Hoisting (Not Hoisted):

```javascript
hoistedExpression(); // Error: hoistedExpression is not a function
var hoistedExpression = function() {
  console.log("I'm not hoisted");
};
```

In Summary: Hoisting affects declarations, not initializations or assignments. Function declarations are hoisted, but function expressions are not. Understanding scope and hoisting helps write more predictable and maintainable JavaScript.

### 21. Scope II: var, let, const

In JavaScript, the keywords `var`, `let`, and `const` are used to declare variables, each with different rules for scope, hoisting, and mutability. Here’s a clearer breakdown with examples:

##### a) `var`:

**Scope**: `var` is either globally scoped (when declared outside a function) or function-scoped (when declared inside a function). It **ignores block scope**.
**Hoisting**: `var` declarations are hoisted to the top of their scope, meaning they are available before the line where they are declared, but the value is `undefined` until initialized. Example:

```javascript
console.log(x); // undefined (due to hoisting)
var x = 10;
console.log(x); // 10

if (true) {
  var y = 20;
}
console.log(y); // 20 (no block scope)
```

##### b) `let`:

**Scope**: `let` is block-scoped, meaning the variable is only accessible within the block in which it’s declared (e.g., inside an `if` statement or loop).
**Hoisting**: `let` is hoisted, but not initialized. Accessing it before initialization throws a `ReferenceError`. Example:

```javascript
// console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a = 30;

if (true) {
  let b = 40;
  console.log(b); // 40 (within block scope)
}
// console.log(b); // ReferenceError: b is not defined (outside block scope)
```

##### c) `const`:

**Scope**: Like `let`, `const` is block-scoped.
**Hoisting**: `const` is hoisted but uninitialized, resulting in a `ReferenceError` if accessed before being defined.
**Immutability**: `const` must be initialized when declared and cannot be reassigned. However, if the value is an object or array, the contents can be modified. Example:

```javascript
const z = 50;
// z = 60; // TypeError: Assignment to constant variable

const arr = [1, 2, 3];
arr.push(4); // Allowed, as the array contents can be changed
console.log(arr); // [1, 2, 3, 4]

// console.log(c); // ReferenceError
const c = 70;
``` 

In summary:

- `var` is function-scoped and hoisted, but not block-scoped.
- `let` and `const` are block-scoped, hoisted but uninitialized before their declaration.
- `const` requires an initial value and can't be reassigned, though objects and arrays can be mutated.

### 22. Scope III: Closures and IIFEs to Prevent Global Scope Pollution

**Closures** and **IIFEs** (Immediately Invoked Function Expressions) are key concepts in JavaScript that help manage scope, especially to avoid polluting the global scope.

A closure is a function that remembers the variables from its outer (enclosing) scope, even after that outer function has finished executing. This allows the inner function to access those variables, creating a "closed" environment where the variables are preserved.

Closures are commonly used to create private variables or to maintain state over time without exposing them globally.

- Example of a Closure:

```javascript
function outerFunction() {
  let counter = 0; // Local variable (not in global scope)

  return function innerFunction() {
    counter++; // Inner function has access to 'counter'
    console.log(counter);
  };
}

const increment = outerFunction();
increment(); // Outputs: 1
increment(); // Outputs: 2
```

In this example, `counter` is not accessible from the global scope, but the inner function can still access and modify it, thanks to the closure.

- IIFEs (Immediately Invoked Function Expressions):

An IIFE is a function that is defined and immediately executed. It creates a local scope to store variables without affecting the global scope, preventing variable leaks into the global environment. IIFEs are especially useful for isolating logic or data, ensuring that variables inside the function don't interfere with other parts of the code. Example:

```javascript
(function() {
  let privateVar = "I'm private";
  console.log(privateVar); // Outputs: "I'm private"
})();

// console.log(privateVar); // Error: privateVar is not defined
```

Here, `privateVar` is confined to the IIFE's local scope, keeping it out of the global scope and preventing unintended conflicts with other parts of the code.

__Why Use Closures and IIFEs?:__

- **Closures** help manage and preserve data privately while allowing functions to access it when needed.
- **IIFEs** are an effective way to structure your code and avoid polluting the global namespace with variables, which can lead to hard-to-trace bugs.

By using closures and IIFEs, you can better manage variable scope and avoid global scope pollution, leading to cleaner, more maintainable code.

### 23. **Scope IV: Context and `this` in JavaScript + Differences Between Regular and Arrow Functions**

In JavaScript, **context** refers to the value of `this`, which represents the object that is executing the function. The behavior of `this` differs between **regular functions** and **arrow functions**.

**`this` in Regular Functions**: 

In regular functions, `this` is determined by how the function is called (the **calling context**). For example:

```javascript
const obj = {
  name: "Alice",
  greet() {
    console.log(this.name); // 'this' refers to obj
  }
};

obj.greet(); // Outputs: "Alice"
```

However, if the function is called independently, `this` may refer to the global object or be `undefined` in strict mode:

```javascript
const greet = obj.greet;
greet(); // 'this' is undefined (strict mode) or global object
```

**`this` in Arrow Functions**:

Arrow functions don’t have their own `this`; they **inherit** `this` from the surrounding scope, making them useful for callbacks or nested functions:

```javascript
const obj = {
  name: "Alice",
  greet() {
    const innerFunc = () => console.log(this.name); // 'this' is inherited
    innerFunc();
  }
};

obj.greet(); // Outputs: "Alice"
```

**Key Differences:**

1. **`this` Binding:**
   - Regular functions: `this` is dynamic and depends on the call.
   - Arrow functions: `this` is lexically inherited from the surrounding scope.

2. **Constructors:**
   - Regular functions can be used as constructors with `new`.
   - Arrow functions cannot be used as constructors.

3. **Arguments Object:**
   - Regular functions have their own `arguments` object.
   - Arrow functions inherit `arguments` from the outer function.

 Example:

```javascript
const obj = {
  method: function() { console.log(this); }, // 'this' refers to obj
  arrowMethod: () => { console.log(this); } // 'this' refers to outer context
};

obj.method();      // Outputs: obj
obj.arrowMethod(); // Outputs: outer context (not obj)
```

In summary, regular functions have dynamic `this`, while arrow functions inherit `this` from their lexical scope. Arrow functions are ideal for callbacks, while regular functions are better suited for object methods.


---

### BONUS - Running Javascript on your machine (using Node.js)

When you install Node.js on your computer, it essentially enables you to use JavaScript to communicate with your system directly. This means you can do things like automate tasks, create servers, manage files, and interact with databases using JavaScript. It expands the reach of JavaScript beyond just web browsers, allowing you to tap into the full potential of the language on your machine. Let's now delve into how we can harness JavaScript's power on our machines with the assistance of Node.js.

1. __Installing Node.js__

To get started with Node.js, follow these steps:

a. Navigate to the official Node.js website at __nodejs.org__.

b. Click on the download button to access the suitable version of Node.js for your operating system (Windows, macOS, or Linux). You'll have the choice between the LTS (Long-Term Support) version, offering the most recent stable release and recommended for most users, and the version with the latest features, suitable for experimental, advanced, or specific needs.

c. Once the download is complete, run the installer and follow the on-screen instructions to install Node.js on your computer.

d. During the installation process, ensure to include the option to add Node.js to your system's PATH. This will make it easier to run Node.js commands from the terminal.

e. After installation, open the terminal (Command Prompt on Windows, Terminal on macOS and Linux) and type ```node --version``` to confirm that Node.js was installed correctly and to check the version.

Now, you can execute Node.js scripts directly from the command line using the node command. This will launch the Node.js interpreter, denoted by the > prompt. From here, you can execute JavaScript commands. For instance, typing console.log('Hello, Node.js!') will output 'Hello, Node.js!' in the terminal. To exit the Node.js interpreter, type ```.exit``` or ```Ctrl + C``` twice.

2. __Installing Visual Studio Code and Essential Plugins for JavaScript Development__

Visual Studio Code (VS Code) is a powerful code editor developed by Microsoft, known for its versatility and lightweight design. To install VS Code, visit __code.visualstudio.com__, download and run the installer for your operating system, then follow the on-screen instructions to complete the installation process.

Essential VS Code Plugins for JavaScript Development:

__Prettier (by Prettier):__ Prettier is a versatile code formatter that supports various languages like JavaScript, HTML, CSS, TypeScript, JSON, Markdown, and more. It can be used directly within code editors with extensions, through command-line tools, as pre-commit hooks in version control systems, or integrated into build tools and CI pipelines. Its purpose is to automate code formatting, ensuring consistency and readability across projects.

__Path Intellisense (by Christian Kohler):__ Path Intellisense offers autocomplete functionality for file paths within import statements and HTML src attributes, aiding in efficient navigation within your project. Its suggestions are automatically populated after installing the plugin, helping you save time by accurately predicting file paths as you type.

__Live Server (by Ritwick Dey):__ Live Server launches a local development server with live reload functionality for HTML, CSS, and JavaScript files. This tool is typically used to create a local server for running front-end projects, especially when JavaScript code is associated with HTML files. Its usage is extremely simple: just right-click on the index.html file (for example) and select 'Open with Live Server'.

__JavaScript (ES6) code snippets (by charalampos karypidis):__ Provides a collection of ES6 code snippets for faster coding. For example, once it is installed, we can type ```mde``` and hit TAB so it will generate the code snippet ```module.exports = { };```

__Code Spell Checker(by Street Side Software)__:  This extension helps maintain clean and error-free code by highlighting spelling mistakes in comments and strings. It assists in avoiding typos and ensuring code professionalism.

General Configuration: Visual Studio Code allows you to customize settings, keybindings, and themes to suit your preferences. Explore the various features provided by VS Code and its plugins to enhance your JavaScript development experience.

3. __Automatic code formatting with Prettier__

To enable automatic code formatting with Prettier upon saving JavaScript files, create a folder named __.vscode__ in the root directory of your project. Inside this folder, include a file named __settings.json__ with the following configuration:

```json
{
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
  }
}
```

Once configured, you'll notice that your JavaScript code is automatically formatted according to Prettier's rules whenever you save a file. This includes consistent indentation, proper spacing, and other style guidelines, leading to cleaner and more maintainable code. These automated adjustments streamline your development process, eliminating the need for manual formatting and ensuring code consistency across your projects. To customize Prettier's rules, you can create a __.prettierrc__ file in your project's root directory. This file allows you to specify your preferred formatting rules for Prettier. Here's an example of a .prettierrc file:

```json
{
  "singleQuote": true,
  "semi": true,
  "tabWidth": 2,
  "printWidth": 100
}
```

In this example: __"singleQuote"__ Configures Prettier to use single quotes instead of double quotes for strings. __"semi"__ specifies whether to add semicolons at the end of statements. __"tabWidth"__ sets the width of a tab character. __"printWidth"__ specifies the maximum number of characters per line before code is wrapped. 

To explore more options and documentation for Prettier, you can visit __prettier.io__

4. __Running Javascript code with Node.js capabilities__

With Visual Studio Code open, navigate to the desired folder (where your project will be), right-click, and select 'New File'. Name it with a .js extension (e.g., __scripts.js__). Inside this file, you can write your JavaScript code, like the following:

```javascript
const num1 = 10;
const num2 = 20;
const result = num1 + num2;
console.log(`The sum of ${num1} and ${num2} is: ${result}`);
```

Once you're in the directory containing your JavaScript file, you can run it using Node.js. Open your terminal, navigate to the directory, and type ```node scripts.js```. This command will execute your JavaScript file and display the output in the terminal. 

Node.js comes with a built-in module called File System (fs), which enables various operations such as dealing with the file system. For instance, if we want to create a .txt file and write to it, we can use the __fs__ module. It provides a way to write to a file while passing a function to handle possible errors. The __fs__ module in Node.js stands for "file system" and allows performing operations like reading from and writing to files, creating directories, deleting files, and more. As one of the core modules in Node.js, it comes pre-installed and doesn't need separate installation via a package manager. In Node.js, we use the ```require``` function to include modules in JavaScript files. When we use ```require('module_name')```, Node.js searches for the specified module in the file system, loads and evaluates it, and returns its exported object. The ```require``` function is part of the CommonJS module system, specifically designed for server-side JavaScript environments like Node.js, where modules are loaded synchronously. With this knowledge, we are fully capable of understanding, writing, and expanding upon code such as the following:

```javascript
// loads the "file system" module
const fs = require('fs');

// Define the file name
const fileName = 'example.txt';

// Text to be written to the file
const textToWrite = 'Hello, world! This is some text written to a file using Node.js.';

// Write to the file
fs.writeFile(fileName, textToWrite, (err) => {
    if (err) {
        console.error('Error writing to file:', err);
    } else {
        console.log('File successfully created and text written.');
    }
});
```

This code loads the built-in "file system" module (fs) in Node.js, defines a file name as example.txt, prepares a string containing some text, writes the content of the string to the file specified by fileName, and logs either an error or success message based on the writing process. To learn more about what can be done with Node.js, including its built-in modules like "file system" (fs), you can refer to the official Node.js documentation available on their website: __https://nodejs.org/docs/latest/api__. Additionally, there are various tutorials, courses, and online resources dedicated to learning Node.js that can provide comprehensive information on its capabilities and usage.

5. __Understanding Node Package Manager (npm)__

Node Package Manager (npm) is a powerful tool used to manage JavaScript packages and dependencies for Node.js projects. npm is the default package manager for Node.js and JavaScript projects. It allows developers to easily install, publish, and manage packages and dependencies for their Node.js projects. These packages contain reusable JavaScript code, libraries, frameworks, and tools that enhance development productivity and extend the functionality of Node.js applications.

Benefits of Using npm:

* Efficient Dependency Management: npm simplifies the process of managing dependencies by automatically installing and updating packages required for your project.

* Large Package Repository: npm provides access to a vast repository of packages, offering a wide range of functionality for various development needs.

* Version Control: npm allows developers to specify and manage package versions, ensuring consistency and compatibility across projects.

* Community Support: Many npm packages are actively maintained by the open-source community, providing continuous improvements, bug fixes, and support.

* Integration with Build Tools: npm integrates seamlessly with popular build tools and task runners like webpack, Gulp, and Grunt, enhancing the development workflow.

Installation of npm: npm typically comes bundled with Node.js installation. When you install Node.js on your computer, npm is automatically installed along with it. Therefore, to install npm, you need to install Node.js first.

6. __Installing and managing dependencies__

To install an npm package, open your terminal or command prompt, navigate to your project directory, and run the command ```npm install <package-name>```. For example, to install a popular 
JavaScript utility library called __lodash__, consider running ```npm install lodash``` or simply ```npm i lodash```. So we have some things to consider:

__Associated files and folders:__ npm automatically manages dependencies for your project by creating a __package.json__ file that lists all installed packages and their versions. You can also specify dependencies manually in this file and use npm install to install them. The __package-lock.json__ file is created by npm to lock down the exact version of each package and its dependencies installed in a project. It ensures consistency across different installations by guaranteeing that everyone working on the project uses the same versions of dependencies. This file is automatically generated and updated whenever npm installs or updates packages in the project. The __node_modules__ folder is where npm installs project dependencies. It contains all the packages and their dependencies specified in the package.json file. Each installed package is stored in its own folder within node_modules, ensuring that the project has access to the required modules. This folder is automatically created and managed by npm when packages are installed using commands like npm install. It's essential for storing and organizing all the external libraries and modules used in a Node.js project.

Note: When uploading your project to GitHub, it's crucial to ignore the 'node_modules' folder. Other developers can re-download this folder on their machines. Additionally, ensure to upload both __package.json__ and __package-lock.json__ files, as they specify the library versions required for the project.

__Using installed packages:__ After installing a package, you can import and use it alongside your JavaScript code. For example, if you installed lodash, you can import it using ```require('lodash')``` for example. With your __scripts.js__ file you can test the installation and usage of lodash with the following code:

```javascript
const _ = require('lodash');

// Sample array
const numbers = [1, 2, 3, 4, 5];

// Double each element using lodash map
const doubledNumbers = _.map(numbers, num => num * 2);

// Output the result
console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

To manage our dependencies we want to consider some key aspects:

__Installing packages for Development:__ When you install a package with the ```--save-dev``` flag or the ```-D``` shorthand, npm adds the package to your __devDependencies__ inside the __package.json__ file. These dependencies are only required for development or testing purposes, not for running the application in a production environment. For instance, if you install a testing framework like Mocha with ```npm i mocha -D```, it will be listed under devDependencies because it's only needed during development, not when deploying the application to a production server. 

Note: In npm v5+, installing a package automatically adds it to package.json. Using ```npm install <package-name>``` saves the package by default. However, if no package.json exists, using ```--save``` is recommended to make sure dependencies are explicitly saved. For example, using ```npm i lodash --save``` can clarify intentions and maintain consistency.

__Uninstalling dependencies:__ We can uninstall dependencies using ```npm uninstall <package-name>``` or ```npm uninstall <package-name1> <package-name2> <package-name3>``` for multiple dependencies. When using ```npm uninstall <package-name>```, npm removes the package from both the node_modules directory and the package.json file by default. 

__Listing installed dependencies:__ You can check all installed packages and their versions by running the command ```npm list```.

With npm, we can incorporate libraries to run alongside our project's automated processes. For example, we can download a specific library and use it as our code linter by running ```npm run lint```. While configuring this type of usage is beyond the scope of this tutorial, it's not difficult to set up and plenty of examples can be found online. Additionally, you can use ```npm help``` to discover more commands enabled by npm. By leveraging npm, you can streamline your Node.js development process, efficiently manage project dependencies, and access a vast ecosystem of JavaScript packages and tools.

7. __Using Yarn or other package managers__

Yarn, developed by Facebook is known for its speed, efficiency, and user-friendly nature. It ensures consistent installations and expedites package management through caching techniques. Yarn also facilitates concurrent task execution and provides clear error messages. npm, a cornerstone since 2010, comes bundled with Node.js and boasts a vast library of packages, valued for its straightforward installation process.

In general, Yarn tends to consume more disk space compared to npm due to its caching mechanism, which locally stores packages to expedite installations. This caching can result in larger overall disk space usage over time, particularly with frequent package installations or updates. Conversely, npm typically uses less disk space by default, though it may also consume additional space if caching features are enabled or if there is a high volume of dependencies.

__Package Management:__ Yarn employs a refined approach to ensure deterministic package version resolutions.

__Speed:__ Yarn often outpaces npm, thanks to its efficient caching mechanism.

__Security:__ While both prioritize security, Yarn offers additional features that bolster security.

__Workspaces:__ Yarn supports workspaces, enabling management of multiple packages within a single repository, particularly beneficial for larger projects.

While Yarn excels in faster installations, better dependency resolution, and enhanced security features, it tends to be favored in larger projects with more complex dependencies. On the other hand, npm is valued for its simplicity and broad adoption, making it a common choice for smaller projects or those with storage constraints.

Installing and using Yarn:

To install Yarn, you can use a package manager like npm or Homebrew (for example). If you're using npm, you can install Yarn globally by running ```npm install -g yarn```. Once installed, you can use Yarn commands in your terminal.

Yarn commands closely mirror npm's functionality. For example, use ```yarn add <package_name>``` to install a package, ```yarn remove <package_name>``` to uninstall, ```yarn list``` to view dependencies, ```yarn add <package_name> --dev``` for development dependencies, ```yarn upgrade <package_name>``` to update a package, ```yarn run <script_name>``` to execute custom scripts from your package.json file, and so on.

If Yarn appears to better suit your project needs, adopting it doesn't necessitate a permanent commitment or an exclusive reliance on it. Certain situations may arise where projects are tightly integrated with package managers tailored to specific operating systems. For instance, on Windows, Chocolatey, or on macOS, Homebrew may be preferred, particularly when managing JavaScript packages system-wide.

Furthermore, it's crucial to recognize that technology continually evolves, leading to the emergence of new package managers with enhanced user-friendly features. An example of this is pnpm, an alternative to npm, boasting benefits such as efficient dependency storage and performance enhancements. Thus, remaining open to such advancements ensures staying abreast of the latest tools and practices in software development.

8. __Adding 'hot reload' with the help of nodemon__

Consider a scenario where you aim to use Yarn and automate the execution of your JavaScript code every time you save a file. Initially, you need to install Yarn globally using the command ```npm install -g yarn```. Next, install a package that monitors file changes and triggers execution using Node.js. You can achieve this by adding nodemon as a development dependency with ```yarn add nodemon -D```. Once the necessary dependencies are installed, configure a 'start' script in your package.json file to watch and execute your scripts upon saving. This can be done by adding a 'scripts' entry to package.json:

```json
"scripts": {
  "start": "nodemon scripts.js"
}
```

Here's where the 'magic' happens: running ```yarn start```. From now on, any changes made to scripts.js and saved will automatically trigger our code to rerun. Pretty neat, right? To stop watching, simply navigate to the terminal and press Ctrl + C.

9. __Installing and Managing Multiple Versions of Node.js with NVM__

In certain scenarios, managing multiple projects with varying Node.js versions can become cumbersome. Reinstalling different Node.js versions or manually updating environment variables for each project switch isn't practical. To address this challenge, tools like Node Version Manager (nvm) provide a solution by simplifying the installation and usage of any Node.js version released to date. Hence, we can explore:

__Installing NVM on Windows:__ Download and run the NVM installer for Windows from the following link: __https://github.com/coreybutler/nvm-windows/releases__. Look for an installer like __nvm-setup.exe__ and proceed with the installation as usual.

__Installing NVM on Linux:__ Visit the NVM project on GitHub: __https://github.com/nvm-sh/nvm__. Follow the instructions in the README file to get the commands for the installation of the latest NVM version.

After the installation, you can verify the NVM Version by running ```nvm --version```. Now we have some possibilities around Node.js installation management:

* Installing the latest version: ```nvm install node```
* Setting the newly installed version as the default one: ```nvm use node```
* Installing a specific version, for example, version 14: ```nvm install 14```
* Using a specific version, for example, version 14: ```nvm use 14```
* Uninstalling a specific version, for example, version 14.21.3: ```nvm uninstall 14.21.3```
* Setting the default version (so that whenever you open a new terminal window the specified version will be activated): ```nvm alias default <version>```
* Checking the Node.js and NPM installation versions: ```node -v``` and ```npm -v```
* Listing the installed versions of Node.js: ```nvm list``` or ```nvm ls``` (The currently active version will be marked with an asterisk)

Note: If the ```nvm use``` command has never been run, no version will be used, even if Node.js has already been installed on your machine.

10. __Documenting shareable projects that use Node.js__

If you intend to upload or share your project on a Git platform, you should instruct others to:

* Download or clone the project repository
* Ensure that Node.js is installed on their machines, which also includes npm
* Install Yarn or any other package manager if the project does not use npm
* Install the dependencies listed in the package.json file. For example, by running ```npm install``` for npm or ```yarn``` for Yarn
* Launch the project. If scripts are not defined in the package.json file, the project is typically executed with ```node <script_name>.js```. However, if a 'start' script is configured and Yarn is being used, the project can be started with the ```yarn start``` command