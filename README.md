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

### 5. Control flow I - 'if' statement

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

### 6. Control Flow II - Falsy and Truthy Values

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

__Default value:__ The "default value or fallback" pattern is a concise way to assign a default value to a variable if the initial value is falsy. The pattern typically involves using the logical OR (||) operator. Here's an example to illustrate the concept:

```javascript
// Example 1:
let myVar = "Hello, World!";
let message = myVar || "Default Value";

console.log(message);  // Output: "Hello, World!"
```

### 7. Control flow III - Loops

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

### 8. Control flow IV - switch-case statements

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

### 9. Basics of functions

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

// Calling the function and storing the returned value on a 'const'
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

// Calling the function and storing the returned value on a 'const'
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

__Function declaration vs. function expressions:__ For routine programming tasks, functions can be declared using either named or anonymous approaches. Named functions are particularly beneficial for self-referencing, such as in recursive functions, and they contribute to clearer stack traces during debugging, potentially easing the identification of functions causing issues. In the majority of scenarios, there is no substantial performance difference between named and anonymous functions. Modern JavaScript engines are optimized to efficiently handle both types. However, in certain extreme cases, named functions might exhibit a marginal speed advantage due to potential optimizations in specific JavaScript engines. Nevertheless, arrow functions are often preferred not just for their modern and concise syntax but also for their predictability, especially when developers navigate thru concepts like __hoisting__ and __context__ as we will see later on.

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

### 10. String manipulation - Useful approaches and methods

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

### 11. Essential array methods (.map(), .find(), .filter())

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

### BONUS - Running Javascript on your machine (using Node.js)

When you install Node.js on your computer, it essentially enables you to use JavaScript to communicate with your system directly. This means you can do things like automate tasks, create servers, manage files, and interact with databases using JavaScript. It expands the reach of JavaScript beyond just web browsers, allowing you to tap into the full potential of the language on your machine. Let's now delve into how we can harness JavaScript's power on our machines with the assistance of Node.js.

1. __Installing Node.js:__

To get started with Node.js, follow these steps:

a. Navigate to the official Node.js website at __nodejs.org__.

b. Click on the download button to access the suitable version of Node.js for your operating system (Windows, macOS, or Linux). You'll have the choice between the LTS (Long-Term Support) version, offering the most recent stable release and recommended for most users, and the version with the latest features, suitable for experimental, advanced, or specific needs.

c. Once the download is complete, run the installer and follow the on-screen instructions to install Node.js on your computer.

d. During the installation process, ensure to include the option to add Node.js to your system's PATH. This will make it easier to run Node.js commands from the terminal.

e. After installation, open the terminal (Command Prompt on Windows, Terminal on macOS and Linux) and type ```node --version``` to confirm that Node.js was installed correctly and to check the version.

Now, you can execute Node.js scripts directly from the command line using the node command. This will launch the Node.js interpreter, denoted by the > prompt. From here, you can execute JavaScript commands. For instance, typing console.log('Hello, Node.js!') will output 'Hello, Node.js!' in the terminal. To exit the Node.js interpreter, type ```.exit``` or ```Ctrl + C``` twice.

2. __Installing Visual Studio Code and Essential Plugins for JavaScript Development:__

Visual Studio Code (VS Code) is a powerful code editor developed by Microsoft, known for its versatility and lightweight design. To install VS Code, visit __code.visualstudio.com__, download and run the installer for your operating system, then follow the on-screen instructions to complete the installation process.

Essential VS Code Plugins for JavaScript Development:

__Prettier (by Prettier):__ Prettier is a versatile code formatter that supports various languages like JavaScript, HTML, CSS, TypeScript, JSON, Markdown, and more. It can be used directly within code editors with extensions, through command-line tools, as pre-commit hooks in version control systems, or integrated into build tools and CI pipelines. Its purpose is to automate code formatting, ensuring consistency and readability across projects.

__Path Intellisense (by Christian Kohler):__ Path Intellisense offers autocomplete functionality for file paths within import statements and HTML src attributes, aiding in efficient navigation within your project. Its suggestions are automatically populated after installing the plugin, helping you save time by accurately predicting file paths as you type.

__Live Server (by Ritwick Dey):__ Live Server launches a local development server with live reload functionality for HTML, CSS, and JavaScript files. This tool is typically used to create a local server for running front-end projects, especially when JavaScript code is associated with HTML files. Its usage is extremely simple: just right-click on the index.html file (for example) and select 'Open with Live Server'.

__JavaScript (ES6) code snippets (by charalampos karypidis):__ Provides a collection of ES6 code snippets for faster coding. For example, once it is installed, we can type ```mde``` and hit TAB so it will generate the code snippet ```module.exports = { };```

__Code Spell Checker(by Street Side Software)__:  This extension helps maintain clean and error-free code by highlighting spelling mistakes in comments and strings. It assists in avoiding typos and ensuring code professionalism.

General Configuration: Visual Studio Code allows you to customize settings, keybindings, and themes to suit your preferences. Explore the various features provided by VS Code and its plugins to enhance your JavaScript development experience.

3. __Automatic code formatting with Prettier:__

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

4. __Running Javascript files:__

With Visual Studio Code open, navigate to the desired folder (where your project will be), right-click, and select 'New File'. Name it with a .js extension (e.g., __scripts.js__). Inside this file, you can write your JavaScript code, like the following:

```javascript
const num1 = 10;
const num2 = 20;
const result = num1 + num2;
console.log(`The sum of ${num1} and ${num2} is: ${result}`);
```

Once you're in the directory containing your JavaScript file, you can run it using Node.js. Open your terminal, navigate to the directory, and type ```node scripts.js```. This command will execute your JavaScript file and display the output in the terminal.

5. __Understanding Node Package Manager (npm):__

Node Package Manager (npm) is a powerful tool used to manage JavaScript packages and dependencies for Node.js projects. npm is the default package manager for Node.js and JavaScript projects. It allows developers to easily install, publish, and manage packages and dependencies for their Node.js projects. These packages contain reusable JavaScript code, libraries, frameworks, and tools that enhance development productivity and extend the functionality of Node.js applications.

Benefits of Using npm:

* Efficient Dependency Management: npm simplifies the process of managing dependencies by automatically installing and updating packages required for your project.

* Large Package Repository: npm provides access to a vast repository of packages, offering a wide range of functionality for various development needs.

* Version Control: npm allows developers to specify and manage package versions, ensuring consistency and compatibility across projects.

* Community Support: Many npm packages are actively maintained by the open-source community, providing continuous improvements, bug fixes, and support.

* Integration with Build Tools: npm integrates seamlessly with popular build tools and task runners like webpack, Gulp, and Grunt, enhancing the development workflow.

Installation of npm: npm typically comes bundled with Node.js installation. When you install Node.js on your computer, npm is automatically installed along with it. Therefore, to install npm, you need to install Node.js first.

6. __Installing and managing dependencies:__

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

* Uninstalling dependencies: We can uninstall dependencies using ```npm uninstall <package-name>``` or ```npm uninstall <package-name1> <package-name2> <package-name3>``` for multiple dependencies. When using ```npm uninstall <package-name>```, npm removes the package from both the node_modules directory and the package.json file by default. 

* Listing installed dependencies: You can check all installed packages and their versions by running the command ```npm list```.

With npm, we can incorporate libraries to run alongside our project's automated processes. For example, we can download a specific library and use it as our code linter by running ```npm run lint```. While configuring this type of usage is beyond the scope of this tutorial, it's not difficult to set up and plenty of examples can be found online. Additionally, you can use ```npm help``` to discover more commands enabled by npm. By leveraging npm, you can streamline your Node.js development process, efficiently manage project dependencies, and access a vast ecosystem of JavaScript packages and tools.

7. __Using Yarn or other package managers:__

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

8. __Adding 'hot reload' with the help of nodemon:__

Consider a scenario where you aim to use Yarn and automate the execution of your JavaScript code every time you save a file. Initially, you need to install Yarn globally using the command ```npm install -g yarn```. Next, install a package that monitors file changes and triggers execution using Node.js. You can achieve this by adding nodemon as a development dependency with ```yarn add nodemon -D```. Once the necessary dependencies are installed, configure a 'start' script in your package.json file to watch and execute your scripts upon saving. This can be done by adding a 'scripts' entry to package.json:

```json
"scripts": {
  "start": "nodemon scripts.js"
}
```

Here's where the 'magic' happens: running ```yarn start```. From now on, any changes made to scripts.js and saved will automatically trigger our code to rerun. Pretty neat, right? To stop watching, simply navigate to the terminal and press Ctrl + C.

9. __Installing and Managing Multiple Versions of Node.js with NVM:__

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