# Javascript quickstart - Essential notes by Renato Lins

  JavaScript was initially created by Brendan Eich in 1995 for Netscape with the specific purpose of enabling scripting capabilities in web browsers. The intention was to develop a scripting language that could be executed by browsers to enhance the interactivity of websites. Since then, JavaScript has evolved to become a versatile and widely-used programming language, not only for client-side scripting in browsers but also for server-side development and a variety of other applications.

  ### 1. Considerations - Why to learn Javascript

__Versatility Across Domains:__ JavaScript proves indispensable in web development (front-end and back-end), mobile app creation, game development, and IoT, showcasing its universal applicability.

__Multi-Paradigm Language:__ JavaScript is a multi-paradigm language, accommodating both object-oriented and functional programming styles, providing flexibility for developers.

__Frameworks and Libraries:__ Robust frameworks and libraries like React, Angular, and Vue.js expedite development, particularly for crafting intricate user interfaces and Single Page Applications (SPAs).

__NPM Ecosystem:__ The Node Package Manager (NPM) hosts a rich ecosystem of open-source packages, providing developers with a treasure trove of tools and resources to accelerate development.

__Easy Start-Up:__ JavaScript is easy to get started with – all you need is a text editor and a browser, tools that are present on almost all computers.

__Productive Development Environment:__ JavaScript facilitates a productive development environment, allowing for rapid prototyping and efficient coding practices.

__Active Community and Job Opportunities:__ JavaScript's vibrant community offers support, tutorials, and a wealth of resources. Proficiency in JavaScript is in high demand, translating to a plethora of job opportunities in the tech industry.

Ps. If you're new to JavaScript and not familiar with coding environments, I recommend starting with __jsfiddle.net__ to write your initial lines of code. To observe your code in action, simply type it in the 'JavaScript' tab and click 'Run.' If you wish to view values outputted to the console (as demonstrated in future examples using the console.log command), press F12, and you'll find the output under the 'Console' tab.

### 2. Variables:

A variable is a named storage location in your computer's memory. Think of it as a labeled box where you can store and retrieve information. You create a variable in JavaScript using the var, let, or const keywords, followed by the variable name.

```javascript
// Example of declaring a variable using 'var'
var message;
message = "Hello, JavaScript!";

// Example of declaring and assigning a variable using 'let'
let number = 42;

// Example of declaring a constant variable using 'const'
const PI = 3.14;
```

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

__Array:__ Represents an ordered list of values.

```javascript
let colors = ["red", "green", "blue"];
```

__Object:__ Represents a collection of key-value pairs.

```javascript
let person = {
  name: "John",
  age: 30,
  isStudent: false
};
```

By now, you don't have to delve into every data type nuance, but it's crucial to understand the separation in JavaScript. Primitive types, such as strings, numbers, booleans, undefined, null, and symbols, are simple and unchangeable. Non-primitive (reference) types, such as objects, arrays, and functions, are a bit more complex in structure and can be created in various formats.

### 4. Operators:

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

__Logical Operators (&&, ||, !):__ Combine multiple conditions and perform logical operations.

```javascript
let isTrue = (true && false); // false
let isEitherTrue = (true || false); // true
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

Explanation: The first ternary operator checks if the age is greater than or equal to 18. If true, it proceeds to the next ternary operator, checking if hasLicense is true.
If both conditions are true, it assigns "Allowed to drive"; otherwise, it assigns "Cannot drive without a license". If the initial age condition is false, it assigns "Too young to drive".

### 5. Falsy and Truthy:

In JavaScript, values can be broadly categorized into two groups: truthy and falsy.

__Truthy Values:__ A value is truthy if, when used in a condition (like in an if statement), it's treated as "true." For example, any non-empty string, any number other than 0, true, or any non-empty object is truthy.

__Falsy Values:__ A value is falsy if, in a condition, it's treated as "false." Examples include false, the number 0, an empty string (""), null, undefined, and NaN (which stands for Not a Number).

Here's a simple illustration:

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

__Default value:__ The "default value or fallback" pattern is a concise way to assign a default value to a variable if the initial value is falsy. The pattern typically involves using the logical OR (||) operator. Here's an example to illustrate the concept:

```javascript
// Example 1:
let myVar = "Hello, World!";
let message = myVar || "Default Value";

console.log(message);  // Output: "Hello, World!"
```