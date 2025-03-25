# **INDEX**

## **0. How JavaScript Works**

- 0.1 [How JavaScript Work](#0-how-javascript-works-1)

## **1.Basics**

- 1.1 [Differences Between Java and JavaScript](#11-differences-between-java-and-javascript)
- 1.2 [Define JavaScript and Its Features](#12-define-javascript-and-its-features)
- 1.3 [Data Types in JavaScript](#13-data-types-in-javascript)
- 1.4 [What is NULL in JavaScript?](#14-what-is-null-in-javascript)
- 1.5 [What are Not Defined and Undefined Variables?](#15-what-are-not-defined-and-undefined-variables)
- 1.6 [What is Alert & Prompt Functions](#16-what-is-alert--prompt-functions)
- 1.7 [What are Web APIs?](#17-what-are-web-apis)
- 1.8 [What is `localStorage` and `sessionStorage`?](#18-what-is-localstorage-and-sessionstorage)

## **2. Functions and Classes**

- 2.1 [Different Ways of Writing Functions in JavaScript](#21-different-ways-of-writing-functions-in-javascript)
- 2.2 [Different Types of Functions in JavaScript](#22-different-types-of-functions-in-javascript)
- 2.3 [What is a Closure?](#23-what-is-a-closure)
- 2.4 [what are the Advantages and Disadvantages of Closures](#24-what-are-the-advantages-and-disadvantages-of-closures)
- 2.5 [What is the First-Class Function?](#25-what-is-the-first-class-function)
- 2.6 [What are Constructor Function with an Example.](#26-what-are-constructor-function-with-an-example)
- 2.7 [Define First Class Citizens, First Class Function, First Order Function(HOF)](#27-define-first-class-citizens-first-class-function-first-order-functionhof)
- 2.8 [What is a Callback in JavaScript?](#28-what-is-a-callback-in-javascript)
- 2.9 [What is Callback Hell? How to avoid it?](#29-what-is-callback-hell-how-to-avoid-it)
- 2.10 [IIFE (Immediately Invoked Function Expression)](#210-iife-immediately-invoked-function-expression)
- 2.11 [What Are Classes in JavaScript?](#211-what-are-classes-in-javascript)
- 2.12 [What Is a Prototype?](#212-what-is-a-prototype)
- 2.13 [Factory Function vs Constructor Function](#213-factory-function-vs-constructor-function)
- 2.14 [What is this in JavaScript ](#214-what-is-this-in-javascript)
- 2.15 [What are call, apply, and bind in JavaScript](#215-what-are-call-apply-and-bind-in-javascript)
- 2.16 [What is Optional Chaining (`?.`) in JavaScript?](#216-what-is-optional-chaining--in-javascript)

## **3. Scope and Hoisting**

- 3.1 [What are Scopes in JavaScript?](#31-what-are-scopes-in-javascript)
- 3.2 [Define Lexical Scope and Lexical Environment](#32-define-lexical-scope-and-lexical-environment)
- 3.3 [What is Hoisting in JavaScript?](#33-what-is-hoisting-in-javascript)

## **4. Event Loop & JS Runtime Environment**

- 4.1 [Define Event Loop)](#41-define-event-loop)
- 4.2 [Working of Event Loop (without micro-task queue)](#42-working-of-event-loop-without-micro-task-queue)
- 4.3 [Working of Event Loop (with micro-task queue)](#43-working-of-event-loop-with-micro-task-queue)
- 4.4 [What is JavaScript Runtime Environment?](#44-what-is-javascript-runtime-environment)
- 4.5 [List & Explain the Components of JS Runtime Environment.](#45-list--explain-the-components-of-js-runtime-environment)
- 4.6 [What is a JavaScript Engine and How it works?](#46-what-is-a-javascript-engine-and-how-it-works)
- 4.7 [JavaScript Runtime Environment QUESTIONS](#47-javascript-runtime-environment-questions)
  - i) [What is the difference between JavaScript Engine and JavaScript Runtime?](#i-what-is-the-difference-between-javascript-engine-and-javascript-runtime)
  - ii) [What is the difference between **call stack** and **memory heap**?](#ii-what-is-the-difference-between-call-stack-and-memory-heap)
  - iii) [What is the role of the garbage collector in JavaScript? How does it work?](#iii-what-is-the-role-of-the-garbage-collector-in-javascript-how-does-it-work)
  - iv) [Why do we need both an interpreter and a JIT compiler in modern JavaScript engines?](#iv-why-do-we-need-both-an-interpreter-and-a-jit-compiler-in-modern-javascript-engines)
  - v) [What are "hot code" and "cold code" in JavaScript execution?](#v-what-are-hot-code-and-cold-code-in-javascript-execution)

## **5. Async Operations**

- 5.1 [What are Promises? What are Promise Chaining.](#51-what-are-promises-what-are-promise-chaining)
- 5.2 [Types of Promise Concurrency Methods](#52-types-of-promise-concurrency-methods)

## **6. Miscellaneous**

- 6.1 [Who Developed JavaScript?](#61-who-developed-javascript)
- 6.2 [What is the Use of `isNaN` Function](#62-what-is-the-use-of-isnan-function)
- 6.3 [What would be the result of `3 + 2 + "7"`?](#63-what-would-be-the-result-of-3--2--7)
- 6.4 [Does JavaScript Support Automatic Type Conversion?](#64-does-javascript-support-automatic-type-conversion)
- 6.5 [Why is JavaScript a dynamically typed language?](#65-why-is-javascript-a-dynamically-typed-language)
- 6.6 [Compiler vs Interpreter vs JIT Compiler](#66-compiler-vs-interpreter-vs-jit-compiler)
- 6.7 [What is the difference between "compilation" in C++ and "compilation" in JavaScript?](#67-what-is-the-difference-between-compilation-in-c-and-compilation-in-javascript)
- 6.8 [What are memory leaks in JavaScript, and how can they occur?](#68-what-are-memory-leaks-in-javascript-and-how-can-they-occur)
- 6.9 [What are the different types of garbage collection strategies?](#69-what-are-the-different-types-of-garbage-collection-strategies)
- 6.10 [Why is JavaScript often called non-blocking?](#610-why-is-javascript-often-called-non-blocking)
- 6.11 [What are the advantages and disadvantages of using a single-threaded model in JavaScript?](#611-what-are-the-advantages-and-disadvantages-of-using-a-single-threaded-model-in-javascript)
- 6.12 [What happens if a long-running synchronous task blocks the call stack? How does it affect the event loop?](#612-what-happens-if-a-long-running-synchronous-task-blocks-the-call-stack-how-does-it-affect-the-event-loop)
- 6.13 [Chrome's V8 Engine Architecture Diagram](#613-chromes-v8-engine-architecture-diagram)
- 6.14 [Why You Can't Fully Trust `setTimeout`](#614-why-you-cant-fully-trust-settimeout)
- 6.15 [What is Destructuring in JavaScript?](#615-what-is-destructuring-in-javascript)
- 6.16 [Implicit vs Explicit Typing in JavaScript](#616-implicit-vs-explicit-typing-in-javascript)
- 6.17 [Define Parameter, Argument, Expression, Statement and Method.](#617-define-parameter-argument-expression-statement-and-method)
- 6.18 [JSON vs JavaScript Object](#618-json-vs-javascript-object)

---

# **0. How JavaScript Works**

## 0.1 How JavaScript Works?

Everything in JavaScript happens inside an **Execution Context**, which is created when a program runs.

- When the program starts, the **Global Execution Context (GEC)** is created and put in a storage container called **Call Stack**.
- **Call Stack**, a data structure that keeps track of which exution context is currently running (GEC or FEC).
- When a function is called, JavaScript creates a new Function **Execution Context (FEC)** specifically for that function.

### **Steps in Execution Context:**

#### **Global Execution Context (GEC):**

- The first context created when JavaScript starts.
- It has **two phases**:
  1. **Memory Creation Phase (Hoisting):**
     - Allocates memory for variables and functions.
     - Variables are set to `undefined`.
     - Function declarations are stored in memory.
  2. **Code Execution Phase:**
     - Executes the code line by line.
     - Assigns and replace the actual values to variables and executes functions.

#### **Function Execution Context (FEC):**

- it is Created whenever a function inside an execution context is called then it creates a **FEC** for that specific function and put it into the call stack .
- It also has two phases (Memory Creation and Code Execution).
- Once the function finishes executing, its context is **popped off the Call Stack**.

### **Call Stack:**

- A **data structure** that keeps track of which execution context is currently running.
- When JavaScript starts, the **GEC** is pushed onto the call stack.
- When a function is called, its **FEC** is pushed onto the stack.
- Once a function finishes, its context is **removed (popped)** from the stack.
- Once the whole code is executed the **GEC** also **popped** from the stack

### **Example**

```javascript
function greet() {
  console.log("Hello, " + name);
}

function sayGoodbye() {
  console.log("Goodbye!");
}

var name = "John"; //Variable

greet(); // Function call
sayGoodbye(); // Function call
```

#### **Step-by-Step Execution:**

1. **Memory Creation Phase (Global Execution Context):**: it will identify all the variables and functions and list them in memory execution phase:

   - `name` → `undefined`.
   - `greet` → Stores the `greet` function.
   - `sayGoodbye` → Stores the `sayGoodbye` function.

2. **Code Execution Phase:** assign values and execute code line by line
   - Assigns `"John"` to `name`.
   - Calls `greet()`, creating a **Function Execution Context (FEC)**:
     - `greet()` is pushed onto the Call Stack.
     - Logs `"Hello, John"`.
     - Pops `greet()` off the stack.
   - Calls `sayGoodbye()`, creating another **Function Execution Context (FEC)**:
     - `sayGoodbye()` is pushed onto the Call Stack.
     - Logs `"Goodbye!"`.
     - Pops `sayGoodbye()` off the stack.

### **Call Stack at Each Step:**

1. **Start:**

   - Call Stack: `[Global Execution Context]`

2. **When `greet()` is called:**

   - Call Stack:

     ```bash
     [greet()(Function Execution Context)]
     [Global Execution Context]
     ```

3. **After `greet()` finishes:**

   - Call Stack: `[Global Execution Context]`

4. **When `sayGoodbye()` is called:**

   - Call Stack:

     ```bash
     [sayGoodbye Function Execution Context]
     [Global Execution Context]

     ```

5. **After `sayGoodbye()` finishes:**

   - Call Stack: `[Global Execution Context]`

6. **End of Program:**
   - Call Stack is empty.

[Go to top ↑](#index)

---

# **1. Basics**

## 1.1) **Differences Between Java and JavaScript**

**Java** is an Object-Oriented Programming (OOP) language, while **JavaScript** is a client-side scripting language.

### **Java**:

- Object-oriented programming language.
- Runs on a virtual machine, allowing it to execute compiled programs across platforms.
- Follows the philosophy: _"Write Once, Run Anywhere."_

### **JavaScript**:

- Lightweight scripting language for creating interactive web pages.
- Can dynamically insert text into HTML elements.
- Also known as the **browser's language**.

[Go to top ↑](#index)

## 1.2) **Define JavaScript and Its Features**

JavaScript is a lightweight single-threaded, dynamically typed aprogramming language with object-oriented capabilities used for creating dynamic web content.
**Main Points**:

- **Lightweight**: Easy to learn and execute with minimal syntax.
- **Single-threaded**: Executes one task at a time in sequence.
- **Dynamically typed**: Variable types are determined at runtime.
- **Asynchronous support**: Manages API calls, timeouts, and other tasks without blocking the main thread.
- **DOM manipulation**: Modifies web page elements dynamically.

[Go to top ↑](#index)

## 1.3) **Data Types in JavaScript**

JavaScript data types are divided into two categories:

### **Primitive Data Types** (Built-in types):

The predefined data types provided by JavaScript language are known as primitive data type. Primitive data types are also known as in-built data types.They are immutable(you can't directly change their values).

1. **Number**: Represents numeric values.

   - Example: `let age = 25;`
   - **Meaning**: Used for integers or floating-point numbers.

2. **String**: Represents a sequence of characters (text).

   - Example: `let name = "John";`
   - **Meaning**: Used to store and manipulate text.

3. **Boolean**: Represents a true or false value.

   - Example: `let isActive = true;`
   - **Meaning**: Used to represent truthy or falsy values.

4. **Symbol**: Represents a unique identifier.

   - Example: `let sym = Symbol('id');`
   - **Meaning**: Often used for unique keys in objects.

5. **Undefined**: Represents a variable that has been declared but not assigned a value.

   - Example: `let x;` // `x` is undefined
   - **Meaning**: Indicates a variable has no value or has not been initialized.

6. **Null**: Represents an intentional absence of any object value.

   - Example: `let person = null;`
   - **Meaning**: Used to represent a 'no value' or 'empty' value.

7. **BigInt**: Represents integers with arbitrary precision.
   - Example: `let bigNumber = 1234567890123456789012345678901234567890n;`
   - **Meaning**: Used for very large integers beyond the safe range of `Number`.

### **Non-Primitive Data Types** (Reference types):

The data types that are derived from primitive data types are known as non-primitive data types. It is also known as derived data types or reference data types.They are mutabla.

1. **Object**: Represents a collection of key-value pairs.

   - Example: `let person = { name: "John", age: 25 };`
   - **Meaning**: Used to store collections of data and more complex structures.

2. **Function**: Represents a block of code that can be called and executed.

   - Example: `function greet() { console.log("Hello!"); }`
   - **Meaning**: Used to define reusable blocks of code that perform tasks.

3. **Array**: Represents a list-like structure that can hold multiple values.
   - Example: `let numbers = [1, 2, 3, 4];`
   - **Meaning**: Used to store multiple values in a single variable, often in an ordered collection.

[Go to top ↑](#index)

## 1.4) **What is NULL in JavaScript?**

`NULL` represents an intentional absence of any object value. It is different from `undefined`, which means a variable has been declared but not assigned a value.

[Go to top ↑](#index)

## 1.5) **What are not defined and undefined variables?**

- **Undefined:** A variable declared but not assigned a value.
- **Not Defined:** A variable not declared but accessed in the code.

Example:

```javascript
let x; // undefined
console.log(y); // not defined
```

[Go to top ↑](#index)

## 1.6) **What is Alert & Prompt Functions**

### **Prompt Box**

A prompt box collects user input. It shows a dialog with a text field and returns the input as a string or `null` if canceled.

**Example**:

```javascript
const name = prompt("What is your name?", "Guest");
console.log(`Hello, ${name}!`);
```

### **Alert Function**

The alert function displays a message in a dialog box with an "OK" button.

**Example**:

```javascript
alert("Welcome to the website!");
```

[Go to top ↑](#index)

## 1.7) **What are Web APIs?**

Web APIs (Application Programming Interfaces) are built-in tools provided by the browser that allow developers to interact with the browser or perform tasks like fetching data, manipulating the DOM, or handling user interactions. They save time and effort for developers.

They make it easier to perform complex tasks without writing everything from scratch.

### **Important Web APIs in JavaScript**

#### 1. **DOM API (Document Object Model)**

- Used to manipulate HTML and CSS.
- Example: Add, remove, or modify elements dynamically.
  ```javascript
  document.getElementById("myDiv").style.color = "blue";
  ```

#### 2. **Fetch API**

- Used to make HTTP requests (like getting or sending data to a server).
  ```javascript
  fetch("https://api.example.com/data")
    .then((response) => response.json())
    .then((data) => console.log(data));
  ```

#### 3. **Geolocation API**

- Used to get the user's current location.
  ```javascript
  navigator.geolocation.getCurrentPosition((position) => {
    console.log(position.coords.latitude, position.coords.longitude);
  });
  ```

#### 4. **Canvas API**

- Used to draw graphics, animations, or charts on a webpage.
  ```javascript
  const canvas = document.getElementById("myCanvas");
  const ctx = canvas.getContext("2d");
  ctx.fillStyle = "red";
  ctx.fillRect(10, 10, 100, 100);
  ```

#### 5. **Web Storage API**

- Used to store data in the browser (localStorage and sessionStorage).
  ```javascript
  localStorage.setItem("key", "value");
  console.log(localStorage.getItem("key"));
  ```

#### 6. **Audio/Video API**

- Used to control audio and video elements on a webpage.
  ```javascript
  const video = document.getElementById("myVideo");
  video.play();
  ```

#### 7. **Clipboard API**

- Used to copy or read text from the clipboard.
  ```javascript
  navigator.clipboard.writeText("Copied text!");
  ```

#### 8 **setTimeout and setInterval**

These are part of the **Timers API** and are used to delay or repeat actions.

- **setTimeout**: Executes a function after a specified time.

  ```javascript
  setTimeout(() => {
    console.log("Executed after 2 seconds");
  }, 2000);
  ```

- **setInterval**: Executes a function repeatedly after a fixed interval.
  ```javascript
  setInterval(() => {
    console.log("Repeats every 3 seconds");
  }, 3000);
  ```

#### 9. **EventListener API**

Used to attach events to elements like `click`, `mouseover`, etc.

```javascript
document.getElementById("btn").addEventListener("click", () => {
  console.log("Button clicked!");
});
```

These APIs extend JavaScript's capabilities, allowing you to:

- Perform time-based tasks (`setTimeout`, `setInterval`).
- Interact with users (`EventListener`, `Drag-and-Drop`).
- Handle advanced functionality (`Web Workers`, `Crypto`, `Speech`).

[Go to top ↑](#index)

## 1.8) **What is `localStorage` and `sessionStorage`?**

Both are **Web Storage APIs** used to store data in a user's browser. They help in saving data **without using a database**.

| Feature           | `localStorage` 🏪                                  | `sessionStorage` 🚪                                           |
| ----------------- | -------------------------------------------------- | ------------------------------------------------------------- |
| **Data Lifespan** | **Forever** (until manually deleted)               | **Only while the tab is open**                                |
| **Scope**         | Shared across all tabs/windows                     | Only available in the same tab                                |
| **Size Limit**    | ~5MB per domain                                    | ~5MB per domain                                               |
| **When to Use?**  | For **long-term storage** (e.g., user preferences) | For **temporary storage** (e.g., form data before submission) |

**How They Work in JavaScript?**

**1️⃣ Storing Data**

```js
localStorage.setItem("username", "Arshit");
sessionStorage.setItem("theme", "dark");
```

**2️⃣ Retrieving Data**

```js
console.log(localStorage.getItem("username")); // "Arshit"
console.log(sessionStorage.getItem("theme")); // "dark"
```

**3️⃣ Removing Data**

```js
localStorage.removeItem("username"); // Deletes "username"
sessionStorage.clear(); // Clears all session storage data

// note: you can use removeItem and clear() in both local and session storage
```

**In Simple Terms:**

✔ **`localStorage`** = Saves data **permanently** until deleted.  
✔ **`sessionStorage`** = Saves data **only while the tab is open**.

[Go to top ↑](#index)

---

# **2. Functions and Classes**

## 2.1) **Different Ways of Writing Functions in JavaScript**

JavaScript provides different ways to define functions, each with its own syntax and use case.

Below are the ways of writing functions in JavaScript:

1. **Function Declaration**:
   A Function Declaration is the traditional way to define a function. It starts with the `function` keyword, followed by the function name and any parameters the function needs.

   Example:

   ```javascript
   // Function declaration
   function add(a, b) {
     console.log(a + b);
   }
   // Calling a function
   add(2, 3);
   ```

2. **Function Expression**:
   A function that is assigned to a variable.

   ```javascript
   const greet = function () {
     console.log("Hello, World!");
   };
   greet();
   ```

3. **Arrow Functions**:
   A shorter syntax for writing functions.
   Arrow Functions were introduced in ES6 (a newer version of JavaScript).

   They provide a shorter syntax for writing functions. Instead of using the function keyword, you use an arrow (=>).

   Example:

   ```javascript
   const greet = () => {
     console.log("Hello, World!");
   };
   greet();
   ```

4. **Anonymous function**
   It is a function that is defined without a name. It is often used as an argument to another function or for short, temporary use.

   Example:

   ```javascript
   //how to Define
   function () {
     console.log("Hello");
   }

   // Using inside the setTimeout
   setTimeout(function () {
     console.log("Hello");
   }, 1000);
   // In this example, the function inside `setTimeout` is **anonymous** because it doesn't have a name.

    // Using in a function expression
   const hello = function () {
     console.log("Hello");
   }
   ```

[Go to top ↑](#index)

## 2.2) **Different Types of Functions in JavaScript**

1. **Function Statement (Function Declaration)**  
   A function that is defined using the `function` keyword and has a name. It is hoisted, meaning it can be called before its definition in the code.

   ```javascript
   function greet() {
     console.log("Hello!");
   }
   ```

2. **Function Expression**  
   A function assigned to a variable. It is not hoisted, so it can only be called after its definition.

   ```javascript
   const greet = function () {
     console.log("Hello!");
   };
   ```

3. **Arrow Function**  
   A shorter syntax for writing functions, introduced in ES6. Arrow functions do not have their own `this` or `arguments` and are commonly used for callbacks or concise logic.

   ```javascript
   const greet = () => {
     console.log("Hello!");
   };
   ```

4. **Anonymous Function**  
   A function without a name, often used as an argument for other functions or for temporary purposes.

   ```javascript
   setTimeout(function () {
     console.log("This is an anonymous function.");
   }, 1000);
   ```

5. **Named Function Expression**  
    A function expression with a name. This name is only accessible inside the function itself, making it useful for recursion or debugging.

   ```javascript
   const factorial = function fact(n) {
     if (n === 0) return 1; // Base case
     return n * fact(n - 1); // Recursive call using 'fact'
   };
   console.log(factorial(5)); // Output: 120
   ```

6. **Immediately Invoked Function Expression (IIFE)**
   A function that executes immediately after it is defined. It is often used to create a private scope or to avoid polluting the global scope.

   ```javascript
   //(_Function_)()
   (function () {
     console.log("IIFE is executed!");
   })();
   ```

7. **Constructor Function**  
   A **constructor function** in JavaScript is a special function used to create new objects. It is called with the `new` keyword, and it sets up the properties and methods that the new object will have.

   ```javascript
   let count = 0;
   function Counter() {
     this.increment = () => {
       count++;
       console.log(count);
     };
     this.decrement = () => {
       count--;
       console.log(count);
     };
   }
   const counter1 = new Counter();
   counter1.increment();
   counter1.decrement();
   ```

8. **Async Function**  
    A function that handles asynchronous operations using `async` and `await`. It allows you to write asynchronous code that looks synchronous.

   ```javascript
   async function fetchData() {
     const response = await fetch("https://api.example.com");
     console.log(await response.json());
   }
   ```

[Go to top ↑](#index)

## 2.3) **What is a Closure?**

A closure is created when a function is defined inside another function, and the inner function has access to the variables from the **lexical environment** of the outer(parent) function, even after the outer function has finished executing.

### Example:

```javascript
function outerFunction() {
  let outerVar = "I am from outer function"; // Outer variable

  function innerFunction() {
    console.log(outerVar); // Inner function accessing outerVar
  }

  return innerFunction; // Returning inner function
}

const closureExample = outerFunction(); // Step 1: outerFunction executes
closureExample(); // Step 2: innerFunction executes and still has access to outerVar
```

#### Explaination

1. **`outerFunction()` is called:** (_const closureExample = outerFunction()_)

   - When you call `outerFunction()`, a new **execution context** for `outerFunction` is created.
   - Inside that function, you have the variable `outerVar` and the inner function `innerFunction`.
   - Once `outerFunction` finishes executing, it is removed from the call stack, and **its execution context is destroyed**. Normally, this would mean that `outerVar` is no longer accessible.

2. **Returning `innerFunction`**:

   - However, when `outerFunction()` returns `innerFunction`, the **inner function** is **stored in the variable `closureExample`**.
   - Even though `outerFunction` has finished and its context is removed, **the `innerFunction` still "remembers"** the lexical environment where it was created (i.e., the variables like `outerVar` that were in `outerFunction`'s scope).

3. **Now calling `closureExample()`:** (_closureExample()_)
   - When you later call `closureExample()` (which is actually `innerFunction`), it executes, and **even though the outer function has finished**, the inner function still has access to `outerVar` because it retains a reference to the **lexical environment** where `outerVar` was defined.

### Key Points

1. **Access to Outer Variables**: Closures allow an inner function to access variables from its outer function's scope, even after the outer function has finished executing.

2. **Lexical Environment**: Closures preserve the lexical environment, keeping the outer function's variables alive.

3. **Created by Inner Functions**: Closures are created whenever a function is defined inside another function.

4. **Memory Efficiency**: Closures maintain state between function calls, preserving data even after the outer function is executed.

5. **Access to Enclosing Scopes**: Closures can access variables from any enclosing scope, not just their immediate parent, means that a closure has access to all variables from any outer function, including grandparents, great-grandparents, and so on — not just the function directly enclosing it..

6. **Independence from Invocation**: Closures do not rely on when a function is called but on where it was created.

7. **Private Variables**: Closures are used to encapsulate data, creating private variables that can’t be accessed outside their scope.

8. **Memory Leak Risk**: Improper use of closures can lead to memory leaks by retaining unnecessary references to outer scope variables.This means that if a closure keeps holding onto variables from its outer function even after it's no longer needed, it prevents those variables from being garbage collected, causing memory to be used up unnecessarily.

9. **Passable as Arguments**: Closures can be passed as arguments or returned from functions, enabling powerful functional patterns.

   - Passed as an argument:

     ```javascript
     function outer() {
       let name = "Arshit";
       return function inner() {
         console.log(name);
       };
     }

     // Passing the closure (inner function) as an argument
     function executeClosure(func) {
       func(); // It can access 'name' from outer function
     }

     const closure = outer(); // closure is the inner function
     executeClosure(closure); // This will print 'Arshit'
     ```

   - Returned from Functions:

     ```javascript
     function createAdder(x) {
       return function add(y) {
         return x + y; // 'x' is from the outer function's scope
       };
     }
     const addFive = createAdder(5); // Returns a closure
     console.log(addFive(10)); // Output: 15, because 'x' is 5, and 'y' is 10
     ```

### An interview Question

Certainly! Here's the example code and the breakdown in bullet points:

### Example Code:

```javascript
function counter() {
  for (var i = 0; i <= 5; i++) {
    // Using 'var'
    setTimeout(function inner() {
      console.log(i); // Prints 'i' after delay
    }, i * 1000); // Delay is 0ms, 1000ms, 2000ms, etc.
  }
}
counter();
```

- Why it prints `6 6 6 6 6 6`:

  - The value of `i` is **not frozen** for each `setTimeout`; it’s **shared across all iterations**.
  - The loop does not wait for the timeouts to finish, it keeps running and reaches the last iteration, where `i = 6` after the loop ends.
  - **After the loop finishes**, all the `setTimeout` functions are executed, each logging the current value of `i`.
  - Since `i` was incremented to `6` by the time the loop finished, **each `setTimeout` function** prints `6`.

- Why the delays are correct:

  - **`setTimeout` registers a delay** for each iteration based on `i * 1000`.
  - Even though the loop finishes quickly, each `setTimeout` keeps track of its respective delay and executes after that specific time, **not affected by the loop's immediate execution**.
  - **`setTimeout` keeps track of the delay** (like 0ms, 1000ms, 2000ms, etc.) for each iteration.
  - However, **it doesn’t keep track of the variable `i`** because `i` is shared across all iterations when declared with `var`.

**To fix the it we can use `let` instead of `var`**

[Go to top ↑](#index)

## 2.4) **What are the Advantages and DisAdvantages of Closures?**

### **Advantages of Closures**:

- **Data Privacy**: Closures allow you to keep variables private and prevent them from being accessed outside the function.

- **Maintains State**: Closures can remember values even after the function finishes execution, helping to keep track of state.

  - **Real-life Example**: A counter that remembers the number it was last at even after it’s been called multiple times.

- **Cleaner Code**: They help in writing modular code by hiding implementation details and exposing only necessary functionality.It means only giving access to the functions that are needed to perform specific tasks, while hiding the internal details or variables that the user doesn’t need to see or interact with directly. This ensures better control and avoids unnecessary interference.

### **Disadvantages of Closures**:

- Closures can lead to increased memory usage because they keep references to variables even after the function has completed.
- The variables declared inside a closure are not garbage collected.
- Sometimes closures can make it harder to track values, especially when there are many nested functions.

- Too many closures can slow down your application. This is actually caused by duplication of code in the memory.

[Go to top ↑](#index)

## 2.5) **What is the First-Class Function?**

In JavaScript, **first-class functions** mean that functions are treated like any other value, which makes JavaScript very flexible.

### Key Features:

1. **Assign to Variables**: Functions can be stored in variables or constants.

   ```javascript
   const greet = function () {
     console.log("Hello!");
   };
   ```

2. **Pass as Arguments**: Functions can be passed as arguments to other functions.

   ```javascript
   function sayHello(callback) {
     callback();
   }
   sayHello(() => console.log("Hi!"));
   ```

3. **Return from Functions**: Functions can return other functions.

   ```javascript
   function createMultiplier(factor) {
     return function (num) {
       return num * factor;
     };
   }
   const double = createMultiplier(2);
   console.log(double(5)); // 10
   ```

4. **Stored in Data Structures**: Functions can be stored in arrays or objects.
   ```javascript
   const funcs = [() => console.log("A"), () => console.log("B")];
   funcs[0](); // A
   ```

[Go to top ↑](#index)

## 2.6) **What are Constructor Function with an Example.**

A **constructor function** in JavaScript is a special type of function used to create and initialize objects. When you create a new object using a constructor function, it allows you to set up properties and methods for that object.

### Key Points:

- Constructor functions are typically used with the `new` keyword.
- They help define the structure and behavior (methods) of objects created from them.

### Example of a Constructor Function:

```javascript
function Person(name, age) {
  // The constructor function assigns properties to the object
  this.name = name;
  this.age = age;

  // Adding a method to the object
  this.greet = function () {
    console.log(
      `Hello, my name is ${this.name} and I am ${this.age} years old.`
    );
  };
}

// Creating an object using the constructor function
const person1 = new Person("Arshit", 25);
const person2 = new Person("Surya", 30);

// Accessing the properties and calling the method
person1.greet(); // "Hello, my name is Arshit and I am 25 years old."
person2.greet(); // "Hello, my name is Surya and I am 30 years old."
```

### Explanation:

- `Person` is a constructor function. It takes `name` and `age` as parameters.
- Inside the constructor, `this.name` and `this.age` refer to the properties of the newly created object.
- `greet` is a method that belongs to the object, which we can call on any object created with the `Person` constructor.

### Why Use Constructor Functions?

- **Reuse Code**: Constructor functions allow you to create many objects with the same structure (properties and methods), but with different values for those properties.

[Go to top ↑](#index)

## 2.7) **Define First Class Citizens, First Class Function, First Order Function(HOF)**

### 1. **First-Class Citizen (First-Class Entity)**

In programming, a "first-class citizen" means something that can be:  
✅ **Stored in a variable**  
✅ **Passed as an argument to a function**  
✅ **Returned from a function**

In JavaScript, **functions** are first-class citizens because they can do all of the above.

### 2. **First-Class Function**

Since functions are **first-class citizens**, they are called **first-class functions** in JavaScript.

It simply means **functions are treated like values** (like numbers or strings).

### 3. **Higher-Order Function (HOF)**

A **higher-order function** is a function that:  
✅ **Takes another function as an argument** OR  
✅ **Returns a function**

[Go to top ↑](#index)

## 2.8) **What is a Callback in JavaScript?**

A **callback** is a function that is **passed as an argument** to another function and is **executed later**.

💡 **Why use callbacks?**

- They help **handle asynchronous tasks** (e.g., fetching data, reading files).
- Helps JavaScript remain **non-blocking**.
- They allow functions to be **more flexible and reusable**.
- Callbacks are commonly used in setTimeout, setInterval, event listeners, and fetching data (like APIs) and other Higher Order Functions.

**Types of Callbacks**

- **Synchronous Callbacks** (Executed immediately inside the function)
- **Asynchronous Callbacks** (Executed later when an operation completes, used in setTimeout etc.)

### **Simple Example:**

```javascript
function greet(name, callback) {
  console.log("Hello, " + name);
  callback(); // Executing the callback function
}

function sayGoodbye() {
  console.log("Goodbye!");
}

// Passing sayGoodbye as a callback to greet
greet("Arshit", sayGoodbye);
```

**Output:**

```
Hello, Arshit
Goodbye!
```

Here, `sayGoodbye` is passed as a **callback**, so it runs **after** `greet()` finishes.

### **Callback in Asynchronous Code (setTimeout Example):**

```javascript
console.log("Start");

setTimeout(() => {
  console.log("This runs after 2 seconds");
}, 2000);

console.log("End");
```

**Output:**

```
Start
End
This runs after 2 seconds
```

Even though `setTimeout` runs **after 2 seconds**, the rest of the code **keeps running** without waiting.

### **Advantages of Callbacks**

- Efficient Handling of Asynchronous Code
- Makes JavaScript Non-Blocking
- Reduces Code Duplication
- Helps in Event-Driven Programming

### **Disadvantages of Callbacks**

- Callback Hell (Too many nested callbacks make code hard to read)
- Difficult Debugging (Errors inside a callback may not be easily caught)
- Inversion of Control (You rely on another function to call your callback correctly)

[Go to top ↑](#index)

## 2.9) **What is Callback Hell? How to avoid it?**

**Callback Hell** happens when multiple callback functions are **nested inside each other**, making the code **hard to read, debug, and maintain**. It usually occurs in **asynchronous** code when one function depends on the result of another.

### **Why Does Callback Hell Happen?**

- JavaScript handles **asynchronous tasks** using callbacks.
- When multiple tasks depend on each other, callbacks get deeply **nested**.
- This makes the code **messy, hard to follow, and difficult to debug**.

### **Example of Callback Hell**

Imagine you want to:  
1️⃣ Get user data from a database.  
2️⃣ Fetch their orders.  
3️⃣ Process the payment.  
4️⃣ Send a confirmation message.

With callbacks, it looks like this:

```javascript
// Get user data by user ID
getUserData(1, function (user) {
  // Once user data is fetched, get the orders for that user
  getOrders(user.id, function (orders) {
    // Once orders are fetched, process the payment for those orders
    processPayment(orders, function (payment) {
      // Once payment is processed, send the confirmation
      sendConfirmation(payment, function () {
        // Finally, confirm that the order has been processed
        console.log("Order confirmed!");
      });
    });
  });
});
```

### **Why is This Bad?**

- The **code goes deeper and deeper** (pyramid shape 🏔️).
- Hard to **read and understand**.
- Difficult to **debug or modify** if something changes.

### **How to Avoid Callback Hell?**

✅ **Use Promises**

```javascript
getUserData(1)
  .then((user) => getOrders(user.id))
  .then((orders) => processPayment(orders))
  .then((payment) => sendConfirmation(payment))
  .then(() => console.log("Order confirmed!"))
  .catch((error) => console.log(error));
```

🔹 **Cleaner, readable, and avoids deep nesting!**

✅ **Use Async/Await (Best Approach)**

```javascript
async function placeOrder() {
  try {
    let user = await getUserData(1);
    let orders = await getOrders(user.id);
    let payment = await processPayment(orders);
    await sendConfirmation(payment);
    console.log("Order confirmed!");
  } catch (error) {
    console.log(error);
  }
}
```

🔹 **Even cleaner and easier to read!**

[Go to top ↑](#index)

## 2.10) **IIFE (Immediately Invoked Function Expression)**

An **IIFE** is a function that is defined and executed immediately after its creation. It is used to create a local scope to avoid polluting the global scope with variables or functions.

### **Syntax:**

```javascript
(function () {
  // Code here
})();
```

- The function is wrapped in parentheses to make it an expression.
- The second set of parentheses `()` immediately invokes (executes) the function.

### **Example:**

```javascript
(function () {
  let message = "Hello, IIFE!";
  console.log(message); // Output: Hello, IIFE!
})();
```

### **Key Points:**

1. **Avoids Global Scope Pollution**: The variables defined inside an IIFE are not accessible outside, making it safer for handling variables.
2. **Encapsulates Code**: Helps group code that doesn’t need to be reused and avoids side effects from polluting the global namespace.

### **IIFE with Parameters Example:**

```javascript
(function (name) {
  console.log("Hello, " + name);
})("Arshit Kumar"); // Output: Hello, Arshit Kumar
```

[Go to top ↑](#index)

## 2.11) **What Are Classes in JavaScript?**

- **Template for Objects:**  
  A class is like a blueprint for creating objects. It defines the properties (data) and methods (functions) that the created objects will have.

- **Syntactic Sugar Over Prototypes:**  
  Underneath, JavaScript uses prototypes for inheritance. Classes provide a cleaner, more familiar syntax for creating and managing these objects.

### Key Components of a Class

1. **Class Declaration:**

   - You use the `class` keyword to declare a class.
   - **Example:**
     ```javascript
     class Person {
       // class body goes here
     }
     ```

2. **Constructor Method:**

   - The `constructor` is a special method for initializing new objects.
   - It is automatically called when you create a new instance of the class.
   - **Example:**
     ```javascript
     class Person {
       constructor(name, age) {
         this.name = name;
         this.age = age;
       }
     }
     ```

3. **Methods:**

   - Methods are functions defined inside a class.
   - They describe the behaviors (actions) that objects created from the class can perform.
   - **Example:**

     ```javascript
     class Person {
       constructor(name, age) {
         this.name = name;
         this.age = age;
       }

       // A method to greet
       greet() {
         console.log(`Hi, I'm ${this.name} and I'm ${this.age} years old.`);
       }
     }
     ```

4. **Creating Instances:**

   - Use the `new` keyword to create a new instance of a class.
   - **Example:**
     ```javascript
     const person1 = new Person("Alice", 30);
     person1.greet(); // Outputs: Hi, I'm Alice and I'm 30 years old.
     ```

5. **Inheritance:**

   - A class can extend another class using the `extends` keyword. This means it inherits the properties and methods of the parent class.
   - **Example:**

     ```javascript
     class Student extends Person {
       constructor(name, age, grade) {
         // Call the parent class constructor
         super(name, age);
         this.grade = grade;
       }

       // A method specific to Student
       study() {
         console.log(`${this.name} is studying.`);
       }
     }

     const student1 = new Student("Bob", 20, "A");
     student1.greet(); // Inherited from Person
     student1.study(); // Outputs: Bob is studying.
     ```

[Go to top ↑](#index)

## 2.12 **What Is a Prototype?**

- **Prototype:**  
  Every object in JavaScript has a hidden property called its **prototype**. The prototype is essentially another object that the original object can "borrow" properties and methods from.

- **Analogy:**  
  Think of a prototype like a parent from whom an object (the child) can inherit traits. If the child doesn't have a certain property, it looks to its parent (prototype) to see if it's there.

- **Example:**

  ```javascript
  // Create a simple object
  const animal = {
    eats: true,
    walk() {
      console.log("Walking...");
    },
  };

  // Create another object that uses 'animal' as its prototype
  const rabbit = Object.create(animal);
  rabbit.hops = true;

  console.log(rabbit.eats); // true (inherited from animal)
  rabbit.walk(); // Walking... (method inherited from animal)
  ```

### What Is Prototypal Inheritance?

- **Prototypal Inheritance:**  
  This is the mechanism where objects inherit properties and methods from their prototype. When you try to access a property or method on an object, JavaScript will look for it on the object itself. If it isn't found, JavaScript will automatically check the object's prototype, and then the prototype's prototype, and so on. This chain is called the **prototype chain**.

- **How It Works:**
  1. **Lookup:** When you access `rabbit.eats`, JavaScript first checks if the `rabbit` object has the property `eats`.
  2. **Prototype Chain:** If it doesn’t, JavaScript looks at `rabbit`’s prototype (which is the `animal` object in our example). Since `animal` has the property `eats`, the value `true` is returned.
- **Example with Inheritance:**

  ```javascript
  // Define an object that serves as a prototype
  const vehicle = {
    wheels: 4,
    start() {
      console.log("Vehicle started");
    },
  };

  // Create another object with 'vehicle' as its prototype
  const car = Object.create(vehicle);
  car.brand = "Toyota";

  console.log(car.wheels); // 4 (inherited from vehicle)
  car.start(); // Vehicle started (inherited method)
  ```

### `__proto__` vs prototype

**`prototype`:** A property on constructor functions (or classes) that serves as a blueprint for creating objects, providing shared properties and methods to all instances.

**`__proto__`:** An internal property of every object that points to its actual prototype, representing the object from which it inherits properties and methods.

[Go to top ↑](#index)

## 2.13) **Factory Function vs Constructor Function**

### `Factory Function` Example

```javascript
function createPerson(name, age) {
  return {
    name: name,
    age: age,
    greet() {
      console.log(`Hello, my name is ${this.name}`);
    },
  };
}

const person1 = createPerson("Arshit", 22);
person1.greet(); // Output: Hello, my name is Arshit
```

### `Constructor Function` Example

```javascript
function createPerson(name, age) {
  return {
    name: name,
    age: age,
    greet() {
      console.log(`Hello, my name is ${this.name}`);
    },
  };
}

const person1 = createPerson("Arshit", 22);
person1.greet(); // Output: Hello, my name is Arshit
```

### Difference

| **Aspect**            | **Factory Function**                                            | **Constructor Function**                                 |
| --------------------- | --------------------------------------------------------------- | -------------------------------------------------------- |
| **Definition**        | Regular function that creates an object                         | Special function to create objects                       |
| **Syntax**            | Normal function call: `createPerson()`                          | Called with `new`: `new Person()`                        |
| **Returns**           | Explicitly returns an object                                    | Doesn’t explicitly return (returns `this` automatically) |
| **Use of `this`**     | Doesn’t usually use `this`                                      | Uses `this` to assign properties                         |
| **Private Variables** | Can create private variables (using closures)                   | Can’t create private variables easily                    |
| **Prototype Use**     | No direct use of prototypes                                     | Can use prototypes for shared methods                    |
| **Memory Efficiency** | Less efficient for methods (each object gets its own copy)      | More efficient with prototypes (shared methods)          |
| **Flexibility**       | More flexible — can return different things based on conditions | Less flexible — always returns an instance of itself     |
| **Error Handling**    | No need to worry about `new` keyword                            | Might misbehave without `new` keyword                    |

**Note:**

- **Use Factory Functions** when you need flexibility, private variables, or simple object creation.
- **Use Constructor Functions** when you want better memory efficiency with shared methods (prototypes).

[Go to top ↑](#index)

## 2.14) **What is `this` in JavaScript**

The `this` in JavaScript refers to the object to which it belongs. Its value depends on **how and where** the function is called, making it a dynamic reference

### **1️⃣ `this` in the Global Scope 🌍**

In the global execution context:

- In the **browser**, `this` refers to the `window` object.
- In **Node.js**, `this` refers to `global`.

```javascript
console.log(this); // In browser: window | In Node.js: global
```

### **2️⃣ `this` in a Regular Function 🤔**

In a normal function, `this` depends on how the function is called.

- In **strict mode (`"use strict"`)**, `this` is `undefined`.
- Otherwise, `this` refers to the **global object** (`window`).

```javascript
function show() {
  console.log(this); // In browser: window | In strict mode: undefined
}
show();
```

### **3️⃣ `this` in an Object Method 🏠**

When used inside an object method, `this` refers to **the object that owns the method**.

```javascript
const person = {
  name: "Arshit",
  greet: function () {
    console.log(this.name); // 'this' refers to 'person' object
  },
};
person.greet(); // Output: "Arshit"
```

### **4️⃣ `this` in an Arrow Function 🎯**

Arrow functions **do not have their own `this`**. Instead, they inherit `this` from their **surrounding scope** (lexical `this`).

```javascript
const person = {
  name: "Arshit",
  greet: () => {
    console.log(this.name); // 'this' does NOT refer to 'person', it refers to window/global
  },
};
person.greet(); // Output: undefined (or error in strict mode)
```

✅ **Use regular functions in objects, NOT arrow functions, when using `this` inside methods.**

### **5️⃣ `this` in a Constructor Function 🏗️**

In constructor functions, `this` refers to the **newly created object**.

```javascript
function Person(name) {
  this.name = name;
}

const p1 = new Person("Arshit");
console.log(p1.name); // Output: "Arshit"
```

### **6️⃣ `this` in Class Methods 📚**

In JavaScript classes, `this` behaves similarly to constructor functions.

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(this.name); // 'this' refers to the instance
  }
}

const p1 = new Person("Arshit");
p1.greet(); // Output: "Arshit"
```

### **7️⃣ `this` in Callbacks & Event Listeners 🎭**

- In event listeners, `this` refers to the **element that triggered the event**.
- If using an **arrow function**, `this` refers to the outer (lexical) scope, **not the element**.

```javascript
document.querySelector("button").addEventListener("click", function () {
  console.log(this); // 'this' refers to the button element
});

document.querySelector("button").addEventListener("click", () => {
  console.log(this); // 'this' refers to window/global, NOT the button
});
```

### **8️⃣ `this` with `bind()`, `call()`, `apply()` 📌**

- `bind()` creates a new function with a specific `this` value.
- `call()` and `apply()` immediately call a function with a specific `this` value.

```javascript
const obj = {
  name: "Arshit",
};

function greet() {
  console.log(this.name);
}

const boundGreet = greet.bind(obj);
boundGreet(); // Output: "Arshit"

greet.call(obj); // Output: "Arshit"
greet.apply(obj); // Output: "Arshit"
```

### **🔹 Summary of `this` in Different Scenarios**

| Scenario                  | `this` Refers To                                 |
| ------------------------- | ------------------------------------------------ |
| **Global Scope**          | `window` (browser) or `global` (Node.js)         |
| **Regular Function**      | `window` (non-strict), `undefined` (strict mode) |
| **Object Method**         | The object that owns the method                  |
| **Arrow Function**        | Inherits `this` from its surrounding scope       |
| **Constructor Function**  | The new instance of the object                   |
| **Class Method**          | The instance of the class                        |
| **Event Listener**        | The element that triggered the event             |
| **bind()/call()/apply()** | The explicitly set `this` value                  |

### **💡 When and Why to Use `this`?**

✅ Use **`this` in object methods** to refer to the object properties.  
✅ Use **`this` in constructors/classes** to assign values to instances.  
✅ Be **careful with `this` in arrow functions**, as it does NOT refer to the calling object.  
✅ Use **`bind()`, `call()`, or `apply()`** when you need to explicitly set `this`.

Would you like more examples or explanations on any part? 😊🚀

[Go to top ↑](#index)

## 2.15) **What are `call`, `apply`, and `bind` in JavaScript**

These three methods (`call`, `apply`, and `bind`) are used to **control the `this` keyword** in JavaScript and allow us to call a function with a specific context (object).

### **1️⃣ `call()` Method**

👉 Calls a function **immediately** and allows passing arguments **individually**.

**🔹 Syntax**

```js
functionName.call(thisArg, arg1, arg2, ...);
```

- `thisArg` → The object to use as `this` inside the function.
- `arg1, arg2, ...` → Arguments passed **individually**.

  **🔹 Example**

```js
const person = {
  name: "Arshit",
};

function greet(age, city) {
  console.log(
    `Hello, my name is ${this.name}, I am ${age} years old and from ${city}.`
  );
}

greet.call(person, 22, "Delhi");

// Output: Hello, my name is Arshit, I am 22 years old and from Delhi.
```

### **2️⃣ `apply()` Method**

👉 Calls a function **immediately**, but arguments are passed as an **array**.

**🔹 Syntax**

```js
functionName.apply(thisArg, [arg1, arg2, ...]);
```

- `thisArg` → The object to use as `this` inside the function.
- `[arg1, arg2, ...]` → Arguments passed as an **array**.

  **🔹 Example**

```js
greet.apply(person, [22, "Delhi"]);
// Output (Same as call): Hello, my name is Arshit, I am 22 years old and from Delhi.
```

### **3️⃣ `bind()` Method**

👉 Returns a **new function** that you can call later with a fixed `this` value.

**🔹 Syntax**

```js
const newFunction = functionName.bind(thisArg, arg1, arg2, ...);
```

- `thisArg` → The object to use as `this` inside the function.
- `arg1, arg2, ...` → Arguments that will be pre-set (optional).

  **🔹 Example**

```js
const newGreet = greet.bind(person, 22, "Delhi");
newGreet(); // Calling later
// Output (Same as call): Hello, my name is Arshit, I am 22 years old and from Delhi.
```

### **📌 Key Differences Between `call`, `apply`, and `bind`**

| Method  | Calls Function Immediately? | Arguments Format                      | Returns New Function? |
| ------- | --------------------------- | ------------------------------------- | --------------------- |
| `call`  | ✅ Yes                      | **Individually** (`arg1, arg2, ...`)  | ❌ No                 |
| `apply` | ✅ Yes                      | **As an array** (`[arg1, arg2, ...]`) | ❌ No                 |
| `bind`  | ❌ No (later)               | **Individually** (`arg1, arg2, ...`)  | ✅ Yes                |

---

### **💡 When to Use What?**

- Use `call()` when you know the exact arguments
- Use `apply()` if you receive data as an array (e.g., from user input or API), you don’t have to manually extract values.
- Use bind() when you want to save the function for later with a fixed this.

[Go to top ↑](#index)

---

## 2.16) **What is Optional Chaining (`?.`) in JavaScript?**

- **Optional Chaining (`?.`)** is a feature in JavaScript that helps **safely access deeply nested properties** without causing an error if a property is `undefined` or `null`.

- **Why Use Optional Chaining?**

  - 🔴 **Without Optional Chaining:**  
    If a nested property **does not exist**, accessing it **throws an error**.

  ```javascript
  const user = {};
  console.log(user.address.city); // ❌ ERROR: Cannot read properties of undefined
  ```

  - 🟢 **With Optional Chaining (`?.`):**

    It **stops** execution **if a property is missing** and returns `undefined` instead of throwing an error.

  ```javascript
  const user = {};
  console.log(user.address?.city); // ✅ undefined (No Error)
  ```

- **Where Can You Use Optional Chaining?**

  - **1. Accessing Nested Objects:**

    ```javascript
    const user = { name: "Arshit", address: { city: "Delhi" } };
    console.log(user.address?.city); // ✅ Delhi
    console.log(user.address?.pincode); // ✅ undefined (No Error)
    ```

  - **2. Accessing Nested Arrays:**

  ```javascript
  const users = [{ name: "Arshit" }, null];
  console.log(users[1]?.name); // ✅ undefined (No Error)
  ```

  - **3. Calling Functions Safely:**

  ```javascript
  const obj = { greet: () => "Hello" };
  console.log(obj.greet?.()); // ✅ Hello
  console.log(obj.sayHi?.()); // ✅ undefined (No Error)
  ```

[Go to top ↑](#index)

# **3. Scope and Hoisting**

## 3.1) **What are Scopes in JavaScript?**

**Scope** in JavaScript refers to the visibility and accessibility of variables in different parts of your code.

There are mainly three types of scope in JavaScript:

- **Block Scope**: Variables declared with `let` or `const` inside a block (e.g., within loops or conditionals) are only accessible within that block.

- **Function Scope**: Variables declared with `var` inside a function are only accessible within that function.

- **Global Scope**: Variables declared outside any function or block are accessible anywhere in the code. They are inside **Global Execution Context (GEC)**.

[Go to top ↑](#index)

## 3.2) **Define Lexical Scope and Lexical Environment**

1. **Lexical Scope**

   - Lexical scope refers to the **rules** or **structure** that determine where a variable can be accessed based on where it is declared in the source code.
   - it means that functions are able to access variables from their parent functions based on where they were defined, not where they were called.
   - The scope of a variable is determined by its location within the code, and functions can access variables from their outer (parent) scopes, but not the other way around.
   - **Example:**

     ```javascript
     function outer() {
       let outerVar = "I'm from outer";

       function inner() {
         console.log(outerVar); // Can access outerVar because of lexical scope
       }

       inner();
     }

     outer();
     ```

2. **Lexical Environment** is the actual internal structure that holds the variable bindings and their references to outer environments.

[Go to top ↑](#index)

## 3.3) **What is Hoisting in JavaScript?**

**Hoisting** is JavaScript's default behavior of moving **declarations** (variables and functions) to the top of their scope during the **Memory Creation Phase**.

- **In the Memory Creation Phase**:  
  Variables (`var`) are initialized as `undefined`, and function declarations are fully stored in memory.

- **During Code Execution Phase**:  
  The code runs line by line, using these hoisted declarations.

### **Example:**

```javascript
console.log(name); // Outputs: undefined (hoisted as undefined)
var name = "John";

greet(); // Outputs: "Hello"
function greet() {
  console.log("Hello");
}
```

### **How It Works:**

1. **Memory Creation Phase (Hoisting):**

   - `var name` → Allocates memory, sets it to `undefined`.
   - `function greet` → Stores the entire function.

2. **Code Execution Phase:**
   - `console.log(name)` → Uses `undefined` from memory.
   - `name = "John"` → Updates the value.
   - `greet()` → Executes the hoisted function.

### IMPORTANT

- **Variables declared with `var`** are fully hoisted, and you can access them before the declaration, but their value will be `undefined`.
- **Variables declared with `let` and `const`** are hoisted but not initialized (_We can say let and const are hoisted, but their behavior makes it feel like they are not_). They stay in the Temporal Dead Zone (TDZ), so you can’t access them before their declaration without getting a ReferenceError.
- **Function delared with `Function Declaration` syntax (eg: _Function abcd(){....}_)** are fully hoisted, and you can call them before it is declared.
- **Function expressions and arrow functions** are not fully hoisted. Only the variable is hoisted (with `var` as `undefined`), but the function itself is not available until after the assignment. so it will give refferenceError.

[Go to top ↑](#index)

---

# **4. Event Loop & JS Runtime Environment**

## 4.1) **Define Event Loop.**

The event loop is a core part of JavaScript, which ensures that non-blocking operations, like asynchronous tasks, don't interfere with the main code execution.

here are the key components:

### 1. **Call Stack**:

- It's a data structure, where the code gets added and removed in a **Last In, First Out (LIFO)** order.
- When a function is called, it gets added to the call stack. When the function finishes, it gets removed.
- It's where **synchronous code** (code that runs one after the other) is executed.

### 2. **Web API Environment**:

- Web APIs are built-in browser features like `setTimeout`, `fetch`, and `DOM events` that allow asynchronous tasks.4
- When JavaScript runs an asynchronous task (like a `setTimeout` or `fetch`), it hands it over to the Web API environment instead of blocking the call stack.
- The Web API runs these tasks outside the call stack and handles them when the task is ready to be processed.

### 3. **Callback Queue**:

- This is like a waiting room where callback functions (from asynchronous tasks like `setTimeout` or `fetch`) wait until the call stack is empty.
- Once the call stack is empty, the event loop picks up these tasks from the callback queue and adds them back to the call stack for execution.

### 4. **Micro-task Queue**:

- This queue holds **micro-tasks**, which are high-priority tasks. These are typically promises (like `.then()` or `async/await`).
- The micro-task queue gets priority over the callback queue. So, before the event loop picks a callback function from the callback queue, it checks and processes any tasks in the micro-task queue first.

### 5. **Event Loop**:

- The event loop is the mechanism that makes JavaScript single-threaded but capable of handling asynchronous operations.
- It constantly checks if the call stack is empty. If it is, it checks the **micro-task queue** and processes those tasks first. Once that's done, it checks the **callback queue** and processes those tasks.
- The event loop allows JavaScript to run asynchronous code without blocking the main thread of execution.

[Go to top ↑](#index)

## 4.2) **Working of Event Loop (without micro-task queue)**

<img src="https://res.cloudinary.com/dy3m6ztbp/image/upload/fl_preserve_transparency/v1738008673/EventLoop1_fmnxuh.jpg?_s=public-apps" alt="Google Drive Image">

### **Taking an example of `setTimout` code**:

```javascript
console.log("start");
setTimeout(function cb() {
  console.log("Callback");
}, 5000);
console.log("end");
```

### Explanation:

1. **`console.log("start");`**

   - This is a **synchronous** statement, so it gets immediately pushed onto the **call stack**.
   - It executes and prints **"start"** to the console.
   - After execution, it is **popped** from the call stack.

2. **`setTimeout(...)`**

   - The `setTimeout` function is also **synchronous** at first, so it gets pushed onto the call stack and executes immediately.
   - However, inside `setTimeout`, the **callback function** (which is `cb()` here) is **not executed** immediately. Instead:
     - The browser registers the callback in the **Web APIs environment** (due to the timeout).
     - After **5 seconds**, the callback will be moved to the **callback queue** (or task queue).
   - **Important**: The `setTimeout` itself (the function call) is **popped** from the call stack immediately after registration,while the callback waits in the callback queue.

3. **`console.log("end");`**

   - This is another **synchronous** statement, so it gets pushed onto the call stack.
   - It executes and prints **"end"** to the console.
   - After execution, it is **popped** from the call stack.

4. **Now the Call Stack is Empty**
   - At this point, the **call stack is empty**, and there is no other synchronous code left.
   - The **event loop** checks the **callback queue**.
   - If the timer of 5 seconds has passed, the callback (`cb()`) is now in the callback queue.
   - The event loop **pushes** the callback from the callback queue onto the call stack.
   - The callback executes and prints **"Callback"** to the console.
   - After execution, the callback is **popped** from the call stack.

### Final Output:

```
start
end
Callback
```

**Important**

- The callback will still **not** execute immediately. Even though the delay is `0`, the callback will be placed in the **callback queue**.This is because JavaScript is single-threaded, and the event loop ensures that only one thing runs at a time.
- The callback won't be executed until the **call stack is empty**, meaning any synchronous code in the call stack (like `console.log()`) needs to finish before the event loop moves the callback from the callback queue to the call stack.

[Go to top ↑](#index)

## 4.3) **Working of Event Loop (with Micro-task Queue)**

<img src="https://res.cloudinary.com/dy3m6ztbp/image/upload/fl_preserve_transparency/v1738008673/EventLoop1_fmnxuh.jpg?_s=public-apps">

### **Taking an example with `setTimeout` and `fetch`**:

```javascript
console.log("start");
setTimeout(function cb() {
  console.log("Callback");
}, 5000);

fetch("https://api.netflix.com").then(console.log("Fetched!"));

console.log("end");
```

### Explanation:

1. **`console.log("start");`**

   - This is a **synchronous** statement, so it gets immediately pushed onto the **call stack**.
   - It executes and prints **"start"** to the console.
   - After execution, it is **popped** from the call stack.

2. **`setTimeout(...)`**

   - The `setTimeout` function is also **synchronous** at first, so it gets pushed onto the call stack and executes immediately.
   - The **callback function** (`cb()`) is registered in the **Web APIs environment** with a timer of `5 seconds`.
   - Once the timer expires, the callback (`cb()`) is moved to the **callback queue** (also called the **task queue**).
   - After registration, the `setTimeout` call is **popped** from the call stack.

3. **`fetch(...)`**

   - The `fetch` function is also a **synchronous** call initially, so it gets pushed onto the **call stack** and executes immediately.
   - It sends the request to the server in the **Web APIs environment** and registers a `Promise` with a `.then()` callback in the **micro-task queue**.
   - The `fetch` call itself is **popped** from the call stack immediately after execution.

4. **`console.log("end");`**

   - This is another **synchronous** statement, so it gets pushed onto the call stack.
   - It executes and prints **"end"** to the console.
   - After execution, it is **popped** from the call stack.

5. **Now the Call Stack is Empty**

   - Once all synchronous code is finished, the **call stack** becomes empty.
   - The **event loop** checks the **micro-task queue** first (higher priority than the callback queue).
   - The `.then()` callback from the `fetch` is moved to the call stack.
   - It executes and prints **"Fetched!"** to the console.
   - After execution, the `.then()` callback is **popped** from the call stack.

6. **Checking the Callback Queue**
   - Once the **micro-task queue** is empty, the event loop moves to the **callback queue** (task queue).
   - If 5 seconds have passed, the callback (`cb()`) from `setTimeout` is moved to the call stack.
   - It executes and prints **"Callback"** to the console.
   - After execution, the callback is **popped** from the call stack.

### Final Output:

```
start
end
Fetched!
Callback
```

### Important:

1. **Micro-task Queue**:

   - The `.then()` of a `Promise` (like `fetch`) is placed in the **micro-task queue**, which has **higher priority** than the callback queue.
   - Micro-tasks always execute before moving to the callback queue, even if the callback queue has tasks waiting.

2. **Callback Queue**:
   - The `setTimeout` callback is placed in the **callback queue (task queue)** after the timer expires.
   - It only runs **after all micro-tasks** (like `Promise.then()`) are completed and the call stack is empty.

[Go to top ↑](#index)

## 4.4) **What is JavaScript Runtime Environment?**

#### **1. Runtime Environment**

- A **Runtime environment** is where your code runs. It includes all the tools and features necessary to execute your program, like:
  - **Language interpreter** (for JavaScript, the JS engine like V8 or SpiderMonkey).
  - **APIs** (browser or Node.js-specific features like `fetch`, `setTimeout`, etc.).
  - **Memory management** and other execution resources.

---

#### **3. JavaScript Runtime Environment**

JavaScript runtime environment is like a container, that has all the things to run a JavaScript Code.There are two types of JavaScript runtime environment:

1. The runtime environment of a Browser (like Google Chrome).
2. The Node runtime environment.

It handles:

- **Synchronous code**: Directly runs in the call stack.
- **Asynchronous code**: Uses Web APIs, queues, and the event loop.

[Go to top ↑](#index)

## 4.5) **List & Explain the Components of JS Runtime Environment.**

**Components of JS Runtime Environment in the Browser:**

1.  **Call Stack**
2.  **Web APIs**
3.  **Callback Queue**
4.  **Microtask Queue**
5.  **Event Loop**

### 1. **JavaScript Engine**

- It is the **brain** of the JavaScript, responsible for **executing your code**.
  Operating in a single-threaded manner,it executes tasks one at a time, following a specific order. There are a lot of steps involved in doing that, but essentially executing JavaScript code is what an engine does.

### 2. **Web/Global APIs or Web API Environment**

- These are **extra features provided by the browser**, like:
  - Timers (`setTimeout`, `setInterval`).
  - HTTP requests (`fetch`, `XMLHttpRequest`).
  - DOM manipulation (`document`).
- These tasks **don’t run directly in the JavaScript engine**. They are handled by the browser in the background.

### 3. **Callback Queue**

- This is like a waiting room where callback functions (from asynchronous tasks like `setTimeout` or `fetch`) wait until the call stack is empty.
- Once the call stack is empty, the event loop picks up these tasks from the callback queue and adds them back to the call stack for execution.

### 4. **Microtask Queue**

- This queue holds **micro-tasks**, which are high-priority tasks. These are typically promises (like `.then()` or `async/await`).
- The micro-task queue gets priority over the callback queue. So, before the event loop picks a callback function from the callback queue, it checks and processes any tasks in the micro-task queue first.

### 5. **Event Loop**

- The event loop is the mechanism that makes JavaScript single-threaded but capable of handling asynchronous operations.
- It constantly checks if the call stack is empty. If it is, it checks the **micro-task queue** and processes those tasks first. Once that's done, it checks the **callback queue** and processes those tasks.
- The event loop allows JavaScript to run asynchronous code without blocking the main thread of execution.

[Go to top ↑](#index)

## 4.6) **What is a JavaScript Engine and How it works?**

A **JavaScript Engine** is a program or interpreter that executes JavaScript code. Its main job is to read (parse) your code, optimize it, and execute it efficiently.

Think of it as the "brain" behind running JavaScript in browsers or other environments like Node.js. Every major browser has its own JavaScript engine.

### **Types of JavaScript Engines**

Here are the major JavaScript engines used in popular environments:

| **Engine Name**            | **Browser/Environment** | **Developed By** |
| -------------------------- | ----------------------- | ---------------- |
| **V8**                     | Google Chrome, Node.js  | Google           |
| **SpiderMonkey**           | Mozilla Firefox         | Mozilla          |
| **Chakra**                 | Microsoft Edge (Legacy) | Microsoft        |
| **JavaScriptCore (Nitro)** | Safari                  | Apple            |

### **Working of a JavaScript Engine ?**

JavaScript Engine works in **three phases**:

- **Parser**
- **Compilation**
- **Execution**:

### **1. Parser**

The JavaScript engine starts by reading your JavaScript code (source code) and breaking it down into smaller parts to understand it.

- **Steps:**

  1. **Tokenization**: The code is split into small pieces called **tokens** (e.g., keywords, variables, symbols, etc.).
     Example: `let x = 5;` becomes tokens like `let`, `x`, `=`, `5`, `;`, then,

     - `let` (keyword)
     - `x` (identifier)
     - `=`(operator)
     - `10` (numeric literal)
     - `;` (semicolon)

  2. **Parsing**: Tokens are structured into a tree-like representation called the **Abstract Syntax Tree (AST)**.
     - The AST is a detailed map of the code’s structure and logic.
     - The engine reads the tokens and applies JavaScript grammar rules to group them into meaningful constructs (e.g., expressions, statements).
     - Errors like "unexpected token" or syntax errors are detected at this stage if the tokens don’t align with the grammar rules.

- **Purpose**: The AST acts as a blueprint for the next phases.

([_see the AST for this code example_ ](https://astexplorer.net/#/gist/5d452502d743d878f7c008ec6591992c/0506cb28312af2f78ca63163eac0163830e2ddec))

### **2. Compilation Phase**

In this phase, the Abstract Syntax Tree (AST), generated during parsing(after tokenization), is transformed into **machine-readable code**, usually in the form of **bytecode** or \* \*

- **Steps:**

  1. **Bytecode Generation**: The AST is passed to the interpreter, which converts it into bytecode and starts executing it.
  2. **Just-In-Time (JIT) Compilation**:
     - The JIT compiler constantly monitors the program while it runs and is watching for "hot code" (i.e., code that is executed frequently).
     - If the JIT compiler detects hot code, it takes the bytecode corresponding to that code and compiles it into optimized machine code which is way faster to execute.

- **Purpose**: The compilation phase ensures the code is fast and efficient during execution.

### **3. Execution Phase**

The execution phase in a JavaScript engine refers to the process of actually running the code that has been parsed, compiled, and optimized. This involves managing the call stack and memory heap, which are crucial for how the engine manages function calls and data during execution.

- **Steps:**

  1. The **bytecode** is sent to the **interpreter**, which starts executing the code line by line.
  2. If the JIT compiler has optimized hot code, that optimized machine code is executed instead of the original bytecode.
  3. The **Call Stack** manages function calls and keeps track of the execution order.
  4. The **Memory Heap** is used to store data like objects, arrays, and variables it has memory management components like Garbage Collector.

- **Purpose**: This phase runs your program and produces the desired results (e.g., displaying data, performing calculations, etc.).

### **Summary of Flow:**

1. **Parser Phase**:  
   Code → Tokens → AST (Blueprint).

2. **Compilation Phase**:  
   AST → Bytecode → Optimized Machine Code (via JIT for hot code).

3. **Execution Phase**:  
   Bytecode/Machine Code → Execution (with Call Stack and Memory Heap management).

[Go to top ↑](#index)

## 4.7) **Javascript Runtime Environment QUESTIONS**

### i) **What is the difference between JavaScript Engine and JavaScript Runtime?**

- **JavaScript Engine**: This is the component that reads and executes JavaScript code (e.g., V8 engine in Chrome).
- **JavaScript Runtime**: It includes the JavaScript engine along with additional tools, such as the **web APIs** (like `setTimeout` or DOM), the **event loop**, and other features needed to run JavaScript in a browser or server (e.g., Node.js).

[Go to top ↑](#index)

### ii) **What is the difference between **call stack** and **memory heap**?**

- **Call Stack**: It stores the function calls that are currently being executed. It's like a to-do list of tasks that need to be completed in order. Each function call is added to the top of the stack.
- **Memory Heap**: This is where JavaScript stores objects, arrays, and other data that can change in size during program execution. It's a more flexible space for dynamic memory allocation.

[Go to top ↑](#index)

### iii) **What is the role of the garbage collector in JavaScript? How does it work?**

- **Garbage Collector**: It automatically manages memory by removing unused data (like objects that are no longer referenced or which typically means they are out of scope or have become temporarily created (like in loops or function calls). However, there are some exceptions, like closures ) from the memory heap. It runs periodically to free up space and prevent memory leaks.

  ```javascript
  function createUserProfile() {
    let userProfile = {
      name: "Alice",
      age: 25,
    };

    // Doing some work with userProfile
    console.log(userProfile.name); // Alice
  }

  // Here, after the function execution, userProfile goes out of scope
  createUserProfile();

  // The 'userProfile' object is no longer accessible after the function call
  // Now, the garbage collector can clean up the 'userProfile' object from memory
  ```

[Go to top ↑](#index)

### iv) **Why do we need both an interpreter and a JIT compiler in modern JavaScript engines?**

- **Interpreter**: It runs code immediately, which helps the program start faster.
- **JIT Compiler**: It optimizes code during execution, converting it to machine code for better performance, especially for frequently used code (hot code).

**Why Not Just Use an Interpreter or JIT Alone?**

1. **Interpreter Only**:

   - **Pros**: Fast startup (immediate execution), simpler, and easier to implement.
   - **Cons**: Slower execution over time, especially for frequently executed code. The lack of optimization makes it less efficient for larger applications.

2. **JIT Compiler Only**:

   - **Pros**: High performance for hot code by converting it to machine code, resulting in faster execution.
   - **Cons**: Slower startup time because it needs to first analyze the code and identify **hot code** before optimization begins. This introduces a delay before the program actually starts running efficiently.

**Why Use Both?**

- **Fast Startup with Interpreter**: The interpreter allows for **quick startup** because it doesn’t require waiting for the full program to be analyzed or compiled. The code can start executing right away.
- **Efficient Execution with JIT Compiler**: As the program runs, the JIT compiler identifies **hot code** (frequently used parts) and compiles it into optimized machine code. This boosts performance for the long run.

By combining both, JavaScript engines ensure that programs can **start fast** and **run efficiently**.

[Go to top ↑](#index)

### v) **What are "hot code" and "cold code" in JavaScript execution?**

- **Hot Code**: Code that is executed frequently (e.g., a function or loop that runs many times). This is optimized by the JIT compiler for better performance.
- **Cold Code**: Code that is executed less frequently. The interpreter may run this code without much optimization because it doesn't impact performance significantly.

[Go to top ↑](#index)

# **5. Async Operations**

## 5.1) **What are Promises? What are Promise Chaining.**

A Promise is like a placeholder for a value that you expect to get later from an asynchronous operation. JavaScript Promises make handling asynchronous operations like API calls, file loading, or time delays easier.
A promise waits (pending), then either delivers a result (fulfilled) or an error (rejected).

A promise can be in one of several states:

1. **Pending**:
   - The initial state. The asynchronous operation has just started and it's neither fulfilled nor rejected.
2. **Fulfilled (Resolved)**:
   - The operation completed successfully, and the promise has a resulting value.
3. **Rejected**:
   - The operation failed and produced an error.
4. **Settled**:
   - Once a promise is either fulfilled or rejected, it’s considered **settled**.

### **How to Create a Promise:**

A promise is created with the `new Promise()` constructor. It takes an **executor function** with two arguments: `resolve` (for success) and `reject` (for failure).

```javascript
// Creating a promise
let promise = new Promise((resolve, reject) => {
  // Do some asynchronous work, e.g., fetch data or wait
  // If successful, call resolve(data);
  // If failed, call reject(error);
});
```

- **resolve:** Pass the data you want when the operation is successful.
- **reject:** Pass the error if something goes wrong.

### **How to Use a Promise:**

To **use** the promise, you call `.then()` for success and `.catch()` for failure.

```javascript
// Using the promise
promise
  .then((data) => {
    // Handle success: `data` is what was passed in resolve()
  })
  .catch((error) => {
    // Handle failure: `error` is what was passed in reject()
  });
```

- **.then()**: This runs when the promise is resolved (success). It receives the value passed in `resolve()`.
- **.catch()**: This runs if the promise is rejected (failure). It receives the value passed in `reject()`.

### **How to Chain Promises:**

You can **chain** multiple `.then()` calls, where each `.then()` can return a new promise.

```javascript
// Chaining promises
promise
  .then((data) => {
    // Handle first success, return a new promise or value
    return anotherPromise; // This could be another promise
  })
  .then((newData) => {
    // Handle second success
  })
  .catch((error) => {
    // Handle errors at any point in the chain
  });
```

- **What is passed inside `.then()` callback:** It receives the data returned by the previous promise (either from resolve or another `.then()`).
- **How to return data in promise chain:** You can either return a value or another promise. When you return something inside a `.then()` callback, it passes that value to the next .`then().`

If you return a new promise (a different promise), the next .then() will wait for that promise to resolve, and it will receive the resolved value of that promise.

### **How to Handle Errors:**

Errors are handled using `.catch()`. If any promise in the chain fails, `.catch()` will handle it.

```javascript
// Handling errors
promise
  .then((data) => {
    // Handle success
  })
  .catch((error) => {
    // Handle any error from the promise or chain
    console.log(error); // This will catch errors from the promise or any .then()
  });
```

- **Error Handling:** `.catch()` will catch errors from any part of the promise chain (either from the initial promise or subsequent `.then()` calls).

### **Easy Example**

```javascript
// Creating a promise named "weather"
let weather = new Promise((resolve, reject) => {
  // Sending a request to the OpenWeather API
  fetch(
    "https://api.openweathermap.org/data/2.5/weather?lat=32.6823931&lon=74.861494&appid=0bb053195ba3bbf768ea5a1be35c176e"
  )
    // Handling the response from the API
    .then((response) => {
      // If the response is not OK (status code not in the range of 200-299)
      if (!response.ok) {
        // If the response is not OK, parse the error and reject the promise
        return response.json().then((err) => {
          // Rejecting with the error message (or a fallback message if the message is not found)
          reject(err.message || "API error occurred");
        });
      }
      // If the response is OK, we return the data in JSON format
      return response.json();
    })
    .then((data) => {
      // When the data is successfully fetched, we resolve the promise with the data
      // "data" is the parsed JSON data from the API, which will be passed to the next .then() in the chain
      resolve(data);
    })
    // Catching any errors in the promise chain
    .catch((error) => {
      // If any error occurs in the fetch or promise chain, reject the promise with the error
      reject(error);
    });
});

// Handling the result of the weather promise
weather
  .then((response) => {
    // "response" is the resolved value from the promise, which will be the data we got from the API
    // This will log the successful data (e.g., weather information) from the API
    console.log("response ", response);
  })
  .catch((error) => {
    // "error" is the error message that was passed into reject()
    // If the promise is rejected, this will log the error (e.g., network issues or API error)
    console.error(error);
  });
```

### **Step-by-Step Explanation:**

- **Creation (Pending):**

  - When you create the `weather` promise, it starts in the **pending** state. This means the code inside it starts running right away.

- **Fulfill/Resolve:**

  - If everything goes well (the weather data is received), the promise is **fulfilled** with the data. This means the API returned the information successfully.
  - The `.then()` part of the code handles this success. It runs once the data is successfully received and logs the result.

- **Rejection:**

  - If something goes wrong (e.g., the API fails or the response is not OK), the promise is **rejected** with an error message.
  - The `.catch()` part of the code handles any errors. If there's a problem, it logs the error message.

- **Settled:**
  - Once the promise either resolves (successful) or rejects (error), it is considered **settled**.
  - A settled promise means the request is finished and the code has either logged the data or an error.

[Go to top ↑](#index)

## 5.2) **Types of Promise Concurrency Methods**

Promise concurrency methods allow handling multiple promises together. Using your `walking` example, let's explore these methods:

### **1. `Promise.all()`**

- Waits for all promises in an array to resolve.
- If any promise rejects, the entire `Promise.all()` fails.

```javascript
let walking = new Promise((res, rej) => {
  let walk = false; //Rejects
  if (walk) {
    res("Walking successfully");
  } else {
    rej(new Error("Error Occurred while Walking"));
  }
});

let running = Promise.resolve("Running successfully"); //resolve
let jumping = Promise.resolve("Jumping successfully"); //Resolve

// Using Promise.all() to execute multiple promises together
Promise.all([walking, running, jumping])
  .then((results) => {
    console.log(results); // Logs all successful results as an array
  })
  .catch((error) => {
    console.error(error); // If any promise fails, the whole chain fails
  });
// output: [rejected]
```

🔹 **Key Point:** If `walking` fails, the whole `Promise.all()` rejects immediately.

### **2. `Promise.allSettled()`**

- Waits for all promises to settle (resolve or reject).
- Returns an array with results (either `{ status: "fulfilled", value: ... }` or `{ status: "rejected", reason: ... }`).

```javascript
Promise.allSettled([walking, running, jumping]).then((results) => {
  console.log(results); // Logs an array showing both successes and failures
});
// output:[rejected, fullfilled, fulfilled]
```

🔹 **Key Point:** Unlike `Promise.all()`, it doesn’t stop on failure; it waits for all promises to complete.

### **3. `Promise.race()`**

- Resolves or rejects as soon as the first promise settles.

```javascript
Promise.race([walking, running, jumping])
  .then((result) => {
    console.log(result); // Logs the first resolved promise
  })
  .catch((error) => {
    console.error(error); // If the first settled promise rejects, it logs the error
  });
// output: [rejected]
```

🔹 **Key Point:** The fastest promise (whether resolved or rejected) determines the outcome.

### **4. `Promise.any()`**

- Resolves as soon as **any** promise resolves.
- If all promises reject, it returns an `AggregateError`.

```javascript
Promise.any([walking, running, jumping])
  .then((result) => {
    console.log(result); // Logs the first successful result
  })
  .catch((error) => {
    console.error(error); // If all promises fail, logs an AggregateError
  });
// output: [resolved(running)]
```

🔹 **Key Point:** Similar to `race()`, but it only resolves when at least one promise succeeds.

### **Summary of Promise Concurrency Methods**

| Method                     | What Happens?                                                  | When It Fails?                                    |
| -------------------------- | -------------------------------------------------------------- | ------------------------------------------------- |
| **`Promise.all()`**        | Waits for **all** to finish, returns results in an array.      | If **any** promise fails, it rejects immediately. |
| **`Promise.allSettled()`** | Waits for **all**, gives success & failure results separately. | Never fails, always returns results for all.      |
| **`Promise.race()`**       | Returns the **first** promise to finish (success or failure).  | If the first promise fails, it rejects.           |
| **`Promise.any()`**        | Returns the **first** successful promise.                      | Fails only if **all** promises fail.              |

[Go to top ↑](#index)

---

# **6. Miscellaneous**

## 6.1) **Who developed JavaScript?**

**JavaScript** was developed by **Brendan Eich** while working at **Netscape Communications Corporation** in **1995**. Netscape later became a part of Mozilla.

[Go to top ↑](#index)

## 6.2) **What is the Use of `isNaN` Function**

The `isNaN` function checks if a value is not a number.  
Example:

```javascript
console.log(isNaN("hello")); // true
console.log(isNaN(123)); // false
```

## 6.3) **What would be the result of `3 + 2 + "7"`?**

- **3** and **2** are treated as numbers, so `3 + 2 = 5`.
- `"7"` is a string, so `5 + "7"` results in `"57"` ( Since one of the operands is a string ("7"), JavaScript will convert the number 5 to a string and then concatenate the two strings.).

[Go to top ↑](#index)

##65.4) **Does JavaScript support automatic type conversion?**

Yes, JavaScript supports **automatic type conversion**, also called _type coercion_.

Example:

```javascript
console.log("5" + 2); // "52"
console.log("5" - 2); // 3
```

[Go to top ↑](#index)

## 6.5) **Why is JavaScript a dynamically typed language?**

JavaScript is dynamically typed because you don't have to specify the type of a variable when you declare it. The type is determined at runtime, and it can change during the program's execution. For example:

```javascript
let x = 10; // x is a number
x = "hello"; // now x is a string
```

[Go to top ↑](#index)

## 6.6) **Compiler vs Interpreter vs JIT Compiler**

### **Compiler**:

- Translates the entire code into machine code **before** running.
- Executes **fast** once compiled, but has a **slower startup**.
- **Uses more memory** because it stores the compiled machine code.

### **Interpreter**:

- Translates and runs the code **line by line** during execution.
- **Starts immediately**, but the execution is **slower**.
- **Uses less memory** since it doesn’t store compiled code.

### **JIT Compiler**:

- Translates code **while running** and compiles frequently used parts(hot codes) for better performance.
- **Faster** than an interpreter, but takes a bit longer to start (compilation happens during execution).

- **Mix of Both**: JIT combines two approaches — **interpretation** (running code directly without full compilation) and **compilation** (turning code into optimized machine code for faster execution).
- **Keeps Frequently Used Code in Memory**: The JIT compiler detects which parts of the code are used often (called "hot code"). These frequently used sections are then **compiled into machine code** and stored in memory, so they don’t need to be re-interpreted every time they're run.

- **Faster Execution**: By storing the compiled machine code in memory, the program can **reuse this optimized code** on future executions, speeding up performance since the JIT doesn't need to interpret the code again or recompile it.

[Go to top ↑](#index)

## 6.7) **What is the difference between "compilation" in C++ and "compilation" in JavaScript?**

Here’s the comparison in a table format:

| **Aspect**                  | **C++**                                                  | **JavaScript**                                            |
| --------------------------- | -------------------------------------------------------- | --------------------------------------------------------- |
| **Compilation**             | Code is compiled ahead of time (before running).         | Code is interpreted or compiled just-in-time (JIT).       |
| **Execution**               | The machine code is executed directly after compilation. | Code is executed after interpretation or JIT compilation. |
| **Compilation Requirement** | Must be fully compiled before execution.                 | Doesn’t require full compilation before execution.        |
| **Speed**                   | May have a longer startup time due to full compilation.  | Starts executing faster due to JIT compilation.           |

[Go to top ↑](#index)

## 6.8) **What are memory leaks in JavaScript, and how can they occur?**

A memory leak happens when a program keeps using memory without releasing it. In JavaScript, it happens when you create objects or variables that are no longer needed but are still referenced, preventing them from being garbage collected. For example:

```javascript
let obj = { name: "John" };
// If 'obj' is no longer used, but not deleted, it causes a memory leak.
```

[Go to top ↑](#index)

## 6.9) **What are the different types of garbage collection strategies?**

Garbage collection in JavaScript usually works by periodically freeing up memory that's no longer needed. There are different strategies:

- **Mark-and-Sweep**: The engine marks objects that are still being used and then removes the ones that aren’t.
  - **Example**: If an object `obj1` is no longer referenced in the code, it gets removed after the mark phase.
- **Reference Counting**: The engine tracks how many references point to an object. If no references are left, the object is deleted.

  - **Example**: If `obj2` was referenced by two variables and both are set to `null`, `obj2` will be removed.

- **Generational**: Objects are divided into "young" (recently created) and "old" (long-lived) generations. Young objects are collected more frequently for deletion.
  - **Example**: If a variable `obj3` is frequently updated, it stays in the young generation for faster collection. If it lives long enough, it moves to the old generation and is collected less often for deletion.

[Go to top ↑](#index)

## 6.10) **Why is JavaScript often called non-blocking?**

JavaScript is non-blocking because it uses an **event-driven** model, where tasks like I/O operations (e.g., reading files or fetching data) don’t block the rest of the code from running. Instead of waiting for these tasks to complete, JavaScript schedules them to be processed later, allowing the program to continue executing other tasks in the meantime.

[Go to top ↑](#index)

## 6.11) **What are the advantages and disadvantages of using a single-threaded model in JavaScript?**

- **Advantages**:
  - **Simplicity**: It’s easier to write and manage code because there’s only one execution thread.
  - **Avoids race conditions**: Since only one task is running at a time, it avoids issues that arise from multiple threads accessing the same data.
- **Disadvantages**:
  - **Blocking operations**: Long-running tasks (like reading large files or performing complex calculations) can block the entire thread. This makes the app unresponsive since the single thread can’t process other tasks, like user input or updating the UI, while it's busy with the long task.
  - **Limited concurrency**: JavaScript can only execute one task at a time in the same thread. If multiple tasks need to be processed at once, they will have to wait, leading to delays or slower performance, especially in CPU-intensive applications.

[Go to top ↑](#index)

## 6.12) **What happens if a long-running synchronous task blocks the call stack? How does it affect the event loop?**

If a long-running synchronous task (like a heavy calculation or infinite loop) blocks the call stack, JavaScript can't process other tasks (like user input or UI updates) until it's done. This makes the app unresponsive. The event loop waits for the call stack to be empty before it processes events, so the app will freeze if the stack is blocked.

### How to fix or avoid:

1. **Use async code**: Break tasks into smaller chunks using `setTimeout`, `Promises`, or `async/await` to allow the event loop to run.
2. **Optimize tasks**: Ensure tasks are efficient or split into smaller steps to avoid long blocks.

[Go to top ↑](#index)

## 6.13) **Chrome's V8 Engine Architecture Diagram**

<img src="https://miro.medium.com/v2/resize:fit:828/format:webp/0*ISypeZUo6NggTMff.png">

[Go to top ↑](#index)

## 6.14) **Why You Can't Fully Trust `setTimeout`**

You can't fully trust `setTimeout` because JavaScript is **single-threaded** and follows an **event-driven** model. This means `setTimeout` doesn’t always execute exactly when you expect it to.

### **Why is `setTimeout` unreliable?**

1. **Event Loop Delay 🚦**

   - The `setTimeout` callback will only run when the **call stack is empty**.
   - If there’s a long-running task before it, the execution will be delayed.

2. **Minimum Time, Not Exact Time ⏳**

   - The time you pass (e.g., `setTimeout(fn, 1000)`) is the **minimum wait time**, not the exact execution time.
   - If the event loop is busy, the actual delay might be longer.

3. **Drift Issues in Loops 🔄**
   - If you use `setTimeout` repeatedly (like for animations or intervals), small delays can **add up over time** and cause drift.

### **Example 1: Delay Due to a Blocking Task**

```js
console.log("Start");

setTimeout(() => {
  console.log("This should run after 2 seconds...");
}, 2000);

// Simulating a long-running task (blocking the call stack)
let startTime = Date.now();
while (Date.now() - startTime < 5000) {} // This blocks for 5 seconds

console.log("End");
```

#### **Expected Output:**

```
Start
End
(This should run after 2 seconds...)  <-- But it runs **after 5+ seconds** instead!
```

**Why?**

- The `while` loop blocks the main thread for 5 seconds.
- `setTimeout` was supposed to run after 2 seconds, but it had to **wait** for the blocking task to finish first.

[Go to top ↑](#index)

## 6.15) **What is `Destructuring` in JavaScript?**

**Destructuring** is a way to **extract values** from arrays or objects and store them in variables **easily**. It makes the code shorter and cleaner.

### **Destructuring an Array**

Instead of accessing elements using indexes, you can directly assign them to variables.

#### ✅ **Example:**

```javascript
const numbers = [10, 20, 30];
let [first, second] = numbers;

console.log(first, second); // 10 20
```

- This saves time and makes the code **cleaner**.

### **Destructuring an Object**

Instead of using dot notation (`object.key`), you can extract values **directly**.

#### ✅ **Example:**

```javascript
const person = { name: "Arshit", age: 22 };

let { name, age } = person;

console.log(name, age); // Arshit 22
```

[Go to top ↑](#index)

## 6.16) **Implicit vs Explicit Typing in JavaScript**

1. **Implicit Typing (or Type Coercion)**:

   This occurs when JavaScript automatically converts one data type to another when required. For instance, JavaScript might convert a string to a number during an arithmetic operation. While this can simplify some code, it can also lead to unexpected results if not handled carefully.

   **Example:**

   ```javascript
   let x = 10; // Implicitly, x is a number.
   x = "Hello"; // Now x is a string, JavaScript changes its type automatically.
   ```

2. **Explicit Typing**:

   Unlike implicit typing, explicit typing involves manually converting a value from one type to another using functions like Number(), String(), or Boolean().

   **Example**:

   ```javascript
   let x = 10; // Implicitly a number
   x = String(x); // Explicitly convert it to a string
   ```

[Go to top ↑](#index)

## 6.17) **Define Parameter, Argument, Expression, Statement and Method.**

### **1️⃣ Parameter**

A **parameter** is a variable inside the function definition that **receives values** when the function is called. It is like a placeholder.

```js
function greet(name) {
  // "name" is a parameter
  console.log("Hello, " + name);
}
```

### **2️⃣ Argument**

An **argument** is the actual value you pass when calling a function.(_in place of Placeholder_)

```js
greet("Arshit"); // "Arshit" is an argument
```

### **3️⃣ Attribute**

An **attribute** is a property of an HTML element or an object.

#### 🔹 In HTML:

```html
<img src="image.jpg" alt="Sample Image" />
```

- `src` and `alt` are **attributes** of the `<img>` tag.

#### 🔹 In JavaScript Objects:

```js
const user = { name: "Arshit", age: 21 };
console.log(user.name); // "name" is an attribute of "user"
```

### **4️⃣ Expression**

An **expression** is any valid JavaScript code that **produces a value**. Expressions can be assigned to variables, passed as arguments, or used inside other expressions.

#### **Examples of Expressions:**

```js
5 + 3; // ✅ Expression (Evaluates to 8)
10 > 5; // ✅ Expression (Evaluates to true)
"Hello" + " World"; // ✅ Expression (Evaluates to "Hello World")
Math.max(5, 10); // ✅ Expression (Evaluates to 10)
```

**Key Rule:** Expressions always **return a value**.

### **5️⃣ Statement**

A **statement** is a complete instruction that **performs an action** but does not necessarily return a value. Statements often contain expressions inside them.

#### **Examples of Statements:**

```js
let sum = 5 + 3; // ✅ Statement (Declares a variable and assigns a value)
if (10 > 5) {
  // ✅ Statement (Conditional statement)
  console.log("True"); // ✅ Statement (Performs an action)
}
for (let i = 0; i < 3; i++) {
  // ✅ Statement (Loop)
  console.log(i); // ✅ Statement inside a loop
}
```

**Key Rule:** Statements **do something**, but they **don’t always return a value**.

#### **IMPORTANT⚠️: Expressions Inside Statements**

Sometimes, expressions are part of a statement.

```js
console.log("Hello" + " World");
```

- `"Hello" + " World"` **(expression, returns `"Hello World"`)**
- `console.log(...)` **(statement, performs an action but returns `undefined`)**

🔹 **Expression = Produces a Value**  
 🔹 **Statement = Performs an Action**

### **6️⃣ Method**

A **method** is a function that is **defined inside an object** and can be called using the object.

```js
const person = {
  name: "Arshit",
  greet: function () {
    console.log("Hello, " + this.name);
  },
};

person.greet(); // Output: Hello, Arshit
```

- Here, `greet` is a **method** inside the `person` object.

[Go to top ↑](#index)

## 6.18) **JSON vs JavaScript Object**

### **Definition**

| **JSON (JavaScript Object Notation)**                               | **JavaScript Object**                                             |
| ------------------------------------------------------------------- | ----------------------------------------------------------------- |
| A lightweight **data format** used for storing and exchanging data. | A **data structure** used in JavaScript to store key-value pairs. |

### **Syntax Difference**

**JSON (String Format)**

- Data is stored as a **string**.
- **Keys and values** must be in **double quotes (`""`)** (except numbers & booleans).
- No functions or undefined values.

```json
{
  "name": "Arshit",
  "age": 23,
  "isStudent": true
}
```

**JavaScript Object (Key-Value Pair)**

- Data is stored in **object literal** format.
- **Keys don’t need quotes** unless required.
- Supports **functions, `undefined`, and symbols**.

```javascript
const user = {
  name: "Arshit",
  age: 23,
  isStudent: true,
  greet: function () {
    console.log("Hello!");
  },
};
```

### **Key Differences**

| Feature               | JSON                                           | JavaScript Object                            |
| --------------------- | ---------------------------------------------- | -------------------------------------------- |
| **Data Type**         | String format                                  | Object format                                |
| **Keys Syntax**       | Must be in **double quotes**                   | Can be without quotes                        |
| **Values**            | Strings, numbers, booleans, arrays, objects    | Can have functions, `undefined`, and symbols |
| **Usage**             | Data transfer (APIs, config files)             | Programming within JavaScript                |
| **Parsing Required?** | Needs `JSON.parse()` to convert into an object | Directly usable                              |

### **Converting Between JSON & JavaScript Object**

**Convert JSON to JavaScript Object (`JSON.parse`)**

```javascript
const jsonString = '{"name": "Arshit", "age": 23}';
const jsObject = JSON.parse(jsonString);
console.log(jsObject.name); // Output: Arshit
```

**Convert JavaScript Object to JSON (`JSON.stringify`)**

```javascript
const user = { name: "Arshit", age: 23 };
const jsonString = JSON.stringify(user);
console.log(jsonString); // Output: '{"name":"Arshit","age":23}'
```

_JSON is a **string** format for storing and transferring data, while a JavaScript object is a **data structure** used in code. JSON requires parsing before use in JavaScript._

[Go to top ↑](#index)

---
