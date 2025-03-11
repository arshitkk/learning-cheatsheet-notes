# Index

## 1. **[Basic Foundation](#1-basic-foundation-1)**

1. **[What is Node.js? Why is it usefull](#1-what-is-nodejs-why-is-it-usefull)**
2. **[History of Node JS](#2-history-of-nodejs)**
3. **[JS on a Server](#3-js-on-a-server)**
   1. **[What is a server?](#what-is-a-server)**
   2. **[What is V8?](#what-is-v8)**
4. **[Exporting and Importing Modules in Node.js (using CommonJS)](#4-exporting-and-importing-modules-in-nodejs-using-commonjs)**
5. **[What is `Module.export`?](#5-what-is-moduleexport)**
6. **[How `require()` Works in Node.js](#6-how-require-works-in-nodejs)**
7. **[Exporting and Importing Modules in Node.js (using ES6 Modules)](#7-exporting-and-importing-modules-in-nodejs-using-es6-modules)**

# 1. **Basic Foundation**

## **1. What is Node.js? Why is it usefull?**

**Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript outside the browser.** It is built on Google’s **V8 JavaScript engine** and is designed for **fast, scalable, and non-blocking** applications.

### **Key Features of Node.js:**

- **Asynchronous & Non-Blocking:**

  - Node.js uses an **event-driven** architecture, meaning it can handle multiple requests at the same time without waiting for one to finish before moving to the next.

- **Single-Threaded, Event-Driven:**

  - Uses a **single-threaded event loop** to manage multiple connections efficiently.
  - Instead of creating a new thread for each request (like traditional servers), it handles all requests in a single thread using callbacks and promises.

- **Built on V8 JavaScript Engine:**

  - Uses **Google Chrome’s V8 engine**, which **compiles JavaScript into machine code**, making it **very fast**.

- **NPM (Node Package Manager):**

  - Comes with **NPM**, the **largest package ecosystem**, allowing developers to install and manage libraries easily.

- **Cross-Platform Support:**

  - Works on **Windows, macOS, and Linux**.

- **Used for Backend Development:**

  - Commonly used to build **APIs, web servers, real-time applications (chats, gaming), and microservices**.

### **Why is Node.js Popular?**

- **Uses JavaScript for Backend & Frontend**, making full-stack development easier.
- **High Performance & Scalability**, especially for real-time applications like **chat apps, gaming servers, and streaming services**.
- **Large Community & Rich Ecosystem** with thousands of open-source libraries.

### **Why is it usefull**

Before **Node.js**, JavaScript could only run inside a browser (like Chrome, Firefox) using their **JavaScript engines** which means

- We could use it for:

  - Manipulate the webpage (DOM) using JavaScript.
  - Handle user events (clicks, form submissions).
  - Make API calls (AJAX, Fetch API) to get data from servers.:

- And the Limitaions were:

  🚫 **No Server-Side JavaScript** – JavaScript could only manipulate web pages (HTML, CSS) in the browser.  
   🚫 **No File System Access** – JavaScript in the browser couldn't read or write files on a computer.  
   🚫 **No Direct Database Connection** – JavaScript needed a backend like PHP or Java to interact with databases.  
   🚫 **Limited Networking Capabilities** – Browser JavaScript couldn't create full-fledged web servers.

With **Node.js**, JavaScript is no longer restricted to the browser! It can run on **servers** like other backend languages (**Python, PHP, Java**). Now, we can:

✅ **Run JavaScript Outside the Browser** – Execute JS code directly on a computer/server.  
✅ **Create Web Servers** – Use Node.js to build full-fledged web applications (like Express.js).  
✅ **Read & Write Files** – Access the file system (create, modify, delete files).  
✅ **Connect to Databases** – Directly interact with **MongoDB, MySQL, PostgreSQL**.  
✅ **Handle Real-Time Applications** – Build live chat apps, gaming servers, and streaming services.

[🌻 **NODEJS is a c++ application with v8 embedded into it**]

[Go to top ↑](#index)

---

## **2. History of Node.js**

### **2009**:

- NodeJS was built by **Ryan Daul** in 2009.
- To run the JS, you always need an **JS engine**, Everywhere you write JS code, there is an **JS engine**, that executes the code.
- Initial Ryan used SpiderMonkey (Mozilla’s JS engine JavaScript Engine
- Then **Switched to** V8 (Google’s JS engine) after a 2-3 days because it was faster.
- Apache HTTP Server was a blocking server, so Ryan wanted to a nonblocking server, which is why Node.js is a non-blocking I/O.The advantage of a non-blocking server is that it can handle multiple requests with a smaller number of threads.
- Earlier, Ryan was working independently, but there was a company named Joyent, and this company was working on something similar to NodeJS. and they hire Ryan to work under us, we will fund your project. big contribution to Joyent Company
- The earlier name of Node.js was **Web.js**, but Ryan Dahl later renamed it to **Node.js** because it was intended to be used for more than just web servers.

### **2010**:

- **NPM was created**, allowing developers to easily share and install JavaScript packages.
- This was a game-changer, allowing developers to **reuse** code instead of writing everything from **scratch**.
- Today, NPM has over 1 million packages, making it the largest package manager in the world.
- Without NPM, Node.js might not have become as successful as it is today.

### **2011**:

- Initially, Node.js was optimized for Linux/macOS.
- In **2011**, Windows support was introduced, making it more accessible to developers.

### **2012**:

- **Ryan Dahl left Node.js development.**
- **Isaac Z. Schlueter** (creator of NPM) took over as the lead developer.

### **2014**

- Some developers were unhappy with **Joyent's slow progress** in maintaining Node.js.
- **Fedor Indutny** forked Node.js and created **io.js** as an alternative, which led to controversy within the company.
- io.js had **faster updates** and a more **open governance model** and **Better support for modern JavaScript**.

### **2015: The Merger – Node.js Foundation is Established**

- **io.js merged back** into Node.js.
- **Node.js Foundation** was created to ensure open governance and stable development.

### **2019: OpenJS Foundation is Formed**

- **Node.js Foundation and JS Foundation merged** to form the **OpenJS Foundation**.
- This created a stronger organization for maintaining Node.js and other JavaScript projects.
- This ensured **better collaboration and long-term support** for Node.js and other JS projects.

### **Who Maintains Node.js Today?**

- **Joyent no longer controls Node.js**, and now the **OpenJS Foundation** maintains Node.js.
- **Community-driven development**: A large group of contributors works on it.

[Go to top ↑](#index)

---

## **3. JS on a Server**

1. ### **What is a server?**

   A **server** is a **remote computer** or **system** that provides data, resources, and services to other computers, called **clients**, over a network. It acts as a central machine that processes requests from multiple clients and responds accordingly.

   **Behind the scenes**, when a computer needs to communicate with a server, it
   sends a request to the server using its **IP address**(_An IP address, or Internet Protocol address, is a unique number that identifies
   every device connected to the internet._). Initially, JavaScript could only
   be executed within web browsers, limiting its use to client-side tasks. However,
   with the introduction of **Node.js**, JavaScript can now also be executed on servers,
   allowing developers to use the same language for both client-side and server-side
   programming.

   **Key Characteristics of a Server:**

   - **Remotely Accessible** – Accessed over a network (LAN, WAN, Internet).
   - **Processes Client Requests** – Handles and responds to client requests.
   - **Runs 24/7** – Always on for continuous service.
   - **High Performance & Secure** – Powerful hardware with strong security.
   - **Different Types** – Web, Application, Database, etc.

2. ### **What is V8?**

   V8 is Google’s open source high-performance **JavaScript** and **WebAssembly** Engine, written in **C++**. It is used in **Chrome** and in **Node.js** It implements ECMAScript and WebAssembly, and runs on Windows, macOS, and Linux systems that use x64, IA-32, or ARM processors. V8 can be embedded into any C++ application (like **Node.js**,**Electron.js**,**Game Engine**,**Embedded Systems(IoT Devices)** ).

**Working of a V8 Engine ?**

V8 Engine works in **three phases**:

- **Parser**
- **Compilation**
- **Execution**:

**1. Parser**

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

**2. Compilation Phase**

In this phase, the Abstract Syntax Tree (AST), generated during parsing(after tokenization), is transformed into **machine-readable code**, usually in the form of **bytecode** or \* \*

- **Steps:**

  1. **Bytecode Generation**: The AST is passed to the interpreter, which converts it into bytecode and starts executing it.
  2. **Just-In-Time (JIT) Compilation**(_TurboFan_):
     - The JIT compiler constantly monitors the program while it runs and is watching for "hot code" (i.e., code that is executed frequently).
     - If the JIT compiler detects hot code, it takes the bytecode corresponding to that code and compiles it into optimized machine code which is way faster to execute.

- **Purpose**: The compilation phase ensures the code is fast and efficient during execution.

**3. Execution Phase**

The execution phase in a JavaScript engine refers to the process of actually running the code that has been parsed, compiled, and optimized. This involves managing the call stack and memory heap, which are crucial for how the engine manages function calls and data during execution.

- **Steps:**

  1. The **bytecode** is sent to the **interpreter**(_ignition_), which starts executing the code line by line.
  2. If the JIT compiler has optimized hot code, that optimized machine code is executed instead of the original bytecode.
  3. The **Call Stack** manages function calls and keeps track of the execution order.
  4. The **Memory Heap** is used to store data like objects, arrays, and variables it has memory management components like Garbage Collector.

- **Purpose**: This phase runs your program and produces the desired results (e.g., displaying data, performing calculations, etc.).

[Go to top ↑](#index)

---

## **4. Exporting and Importing Modules in Node.js (using CommonJS)**

In Node.js, keeping all the code in a single file is not a good practice, especially for large projects. To manage our code better, we use **modules**. Modules allow us to split our code into multiple files and reuse them where needed.

**Why Do We Need Modules?**

1. **Code Reusability** – We can write functions or variables in one file and use them in multiple files.
2. **Better Organization** – It keeps the project structure clean and readable.
3. **Maintainability** – Updating or debugging becomes easier as code is separated into logical parts.
4. **Performance** – Loading only necessary code helps optimize performance.

**Exporting in Node.js**

To use a variable, function, or class in another file, we need to **export** it. In Node.js, we use `module.exports` or `exports` to make code available to other files.

**Before that**: If you write `console.log()` statements inside a module file, they will execute when the file is **loaded** using `require()` like (**`require('./math')`**) . However, you **cannot access** variables or functions from the module file unless you **explicitly export** them. Because modules **protect** their variables and functions from leaking by default. So, they are private and they are in the scope of that file.

Example: Exporting a Function and Variable

**`math.js` (Module File)**

```js
console.log(
  "I dont need to be exported, i will execute as soon as this module load in another file"
);
// Define a function
function add(a, b) {
  return a + b;
}

// Define a variable
const PI = 3.1416;

// Exporting functions and variables things
module.exports = { add, PI };
```

### Importing a Module Using `require()`

In Node.js, the `require()` function is a built-in function that allows you to include or
require other modules into your main modules.

#### Example: Importing the Module

**`app.js` (Main File)**

```js
// Import the module
const math = require("./math.js"); // Import the file

console.log(math.add(5, 3)); // Output: 8
console.log(math.PI); // Output: 3.1416
```

Here, `require('./math.js')` loads the `math.js` file, and we can use the exported function `add` and variable `PI`.

### **Important**

**1. Ignoring File Extensions**

- When using `require()`, you can **omit** the file extension for **`.js`** files.
- Node.js automatically assumes it is a JavaScript file.
- Example:

  ```js
  const math = require("./math"); // No need to write './math.js'
  ```

- **BUT**, You **must** specify the extension for **non-JavaScript files** (like `.json`, `.node`).

**2. Using Destructuring Instead of Object Assignment**

- If a module exports multiple things, instead of assigning everything to an object, you can **use destructuring**.

- **Example**

  ```js
  const { add, PI } = require("./math");
  console.log(add(5, 3)); // ✅ Output: 8
  console.log(PI); // ✅ Output: 3.1416
  ```

- **Destructuring makes the code cleaner and avoids unnecessary object references.**

**3. `require()` Caches Modules**

- When you import a module using `require()`, it is **cached** (stored in memory).
- If you require the same module again, Node.js **does not reload** it; instead, it uses the cached version.

**4. Importing JSON Files Directly**

- Node.js allows importing JSON files directly using `require()`.
- The JSON data is automatically **parsed into a JavaScript object**.
- **Important:** If the JSON file has errors (like missing commas), `require()` will throw an error.

**5. `require()` Works for Core Modules, Local Modules, and Third-Party Modules**

- **Core Modules** (Built-in Node.js modules):
  ```js
  const fs = require("fs"); // File System module
  ```
- **Local Modules** (Files you create):
  ```js
  const math = require("./math");
  ```
- **Third-Party Modules** (Installed via npm):
  ```js
  const express = require("express");
  ```

## **5. What is `Module.export`?**

Before passing the code to the **V8 engine**, **Node.js** wraps each module inside an **Immediately Invoked Function Expression (IIFE)**. This is done automatically by Node.js to **encapsulate** the module and provide important features.

When we create a module in Node.js, it is **not** executed as it is. Instead, Node.js **wraps** it inside an **IIFE (Immediately Invoked Function Expression)** before execution.

For example, if we write the following code in `math.js`:

```js
const PI = 3.1416;

function add(a, b) {
  return a + b;
}

module.exports = { add, PI };
```

Internally, **Node.js wraps** this module as:

```js
(function (exports, require, module, __filename, __dirname) {
  const PI = 3.1416;

  function add(a, b) {
    return a + b;
  }

  module.exports = { add, PI };
});
```

---

### **Why Does Node.js Wrap Modules in an IIFE?**

The module wrapping serves several purposes:

- **Encapsulation & Isolation:**

  - The code inside the module does **not pollute the global scope**.
  - Each module has its own scope, so variables/functions inside a module **cannot be accessed** from other modules unless explicitly exported.

- **Provides Important Variables:**

  - The IIFE function receives special parameters:
    - `exports` → Shortcut for exporting values.
    - `require` → Function to import modules.
    - `module` → The object representing the current module.
    - `__filename` → The absolute file path of the current module.
    - `__dirname` → The directory path of the current module.

### **Variables and Functions are Private in Different Modules**

Since each module is wrapped inside a function, **its variables and functions are local to that function** and **cannot be accessed directly** from other files.

### **How Do You Get Access to `module.exports`?**

`module.exports` is the object that a module uses to **share values** (functions, variables, classes) with other modules.

### **Where Does `module` Come From?**

- Node.js **automatically provides** the `module` object as part of the **IIFE wrapping**.
- `module.exports` starts as an **empty object (`{}`)** and we can **assign values to it**.

## **6. How `require()` Works in Node.js**

The `require()` function in Node.js is used to **import modules** into a file. When you use `require()`, Node.js goes through a specific process to **locate, load, and execute** the module.

### **Steps of How `require()` Works**

When you call `require('./math')`, Node.js follows these steps:

**Step 1: Resolve the Module Path**

- If the module is **a built-in module** (like `fs`, `path`), Node.js directly loads it.
- If it is a **custom module** (`./math.js`), Node.js looks for the file in the specified path.
- If no extension is provided, Node.js **tries different file extensions** (`.js`, `.json`, `.node`).
- If the module is **a package**, Node.js looks for `node_modules` and loads it from there.

**Step 2: Load the Module**

- If the module is found, Node.js **reads the file contents**.
- If it's a **JavaScript file (`.js`)**, Node.js wraps it inside an **IIFE (Immediately Invoked Function Expression)** to create a private scope.
- If it's a **JSON file (`.json`)**, Node.js parses it.
- If it's a **C++ addon (`.node`)**, Node.js loads the compiled binary.

**Step 3: Execute the Module**

- The wrapped module code runs inside its **own function scope**.
- Node.js provides special variables like `module`, `exports`, `require`, `__filename`, and `__dirname`.
- The module **sets values** on `module.exports` to be shared with other files.

**Step 4: Cache the Module**

- If the same module is **required again**, Node.js **does not reload** it.
- Instead, it **returns the cached version** from `require.cache`, improving performance.

## **7. Exporting and Importing Modules in Node.js (Using ES6 Modules)**

In Node.js, we can use **ES6 Modules (ECMAScript Modules)** to export and import variables, functions, or classes between different files. ES6 Modules use the `export` and `import` keywords instead of `module.exports` and `require()` (which are used in CommonJS).

### **Setting Up ES6 Modules in Node.js**

By default, Node.js uses **CommonJS (CJS)**, so to enable **ES6 Modules (ESM)**, we must:

- **Option 1:** Add `"type": "module"` in `package.json`

```json
{
  "type": "module"
}
```

- **Option 2:** Use the `.mjs` file extension  
  Example: `math.mjs`

### **Exporting Modules in ES6**

We can **export** values from a module using either **named exports** or **default exports**.

- **Named Exports (Export Multiple Things)**: Use `export` before a variable or function.

  ```js
  // Define functions
  export function add(a, b) {
    return a + b;
  }

  export function subtract(a, b) {
    return a - b;
  }

  // Define a constant
  export const PI = 3.1416;
  ```

  **Named exports allow exporting multiple values, and they must be imported using their exact names.**

- **Default Export (Export One Thing)**: A file can have **only one** default export.

  ```js
  export default function greet(name) {
    return `Hello, ${name}!`;
  }
  ```

  **Default exports can be imported with any name.**

### **Importing Modules in ES6**

we can use `import` statement to import **modules**

```js
import { add, subtract, PI } from "./math.js";

console.log(add(5, 3)); // 8
console.log(subtract(10, 4)); // 6
console.log(PI); // 3.1416
```

## **8. CommonJS vs ES6 Modules (Comparison Table)**

| Feature                  | **CommonJS (CJS)**                                       | **ES6 Modules (ESM)**                                                    |
| ------------------------ | -------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Syntax**               | Uses `require()` and `module.exports`                    | Uses `import` and `export`                                               |
| **File Extension**       | `.js` (default in Node.js)                               | `.mjs` (or set `"type": "module"` in `package.json`)                     |
| **Importing Modules**    | `const math = require('./math');`                        | `import * as math from './math.js';`                                     |
| **Exporting Modules**    | `module.exports = { add, PI };`                          | `export { add, PI };` or `export default`                                |
| **Execution Style**      | **Synchronous (Blocking)** – Code executes line by line  | **Asynchronous (Non-blocking)** – Can use `import()` for dynamic imports |
| **Usage in Node.js**     | Default module system in Node.js                         | Needs `"type": "module"` in `package.json` or `.mjs` extension           |
| **Importing JSON Files** | `const data = require('./data.json');` ✅ Works directly | `import data from './data.json';` ❌ Needs `"json"` import support       |
| **Browser Support**      | ❌ Not supported in browsers                             | ✅ Supported in modern browsers                                          |
| **Code Execution Order** | Modules load **synchronously** (slower)                  | Modules load **asynchronously** (faster)                                 |
| **Flexibility**          | More flexible, works in older projects                   | More structured, better for large-scale projects                         |
| **Strict**               | CommonJS code runs in non-strict mode                    | ES modules execute in strict mode                                        |
| **Best Use Case**        | **Backend (Node.js)** projects                           | **Frontend (Browser)** and **modern Node.js** projects                   |

## **9. What is libuv?**

libuv is a multi-platform support library that provides asynchronous I/O and event-driven capabilities for Node.js. It helps Node.js handle non-blocking operations like file system access, networking, and timers efficiently. libuv is **the backbone of Node.js' asynchronous nature**

**it is written in C because:**

- **Performance** → C is a low-level language, making it fast and efficient.
- **Cross-Platform Compatibility** → Works on Windows, macOS, and Linux.
- **Interoperability** → C can directly interact with system APIs for file I/O, networking, and threads.

**Why do we need libuv in Node.js?**

- It allows asynchronous execution of tasks without blocking the main thread.
- It provides a thread pool for handling CPU-intensive operations.
- It manages event-driven, non-blocking operations in Node.js.
- It helps Node.js work efficiently without needing multiple threads for simple tasks.

**Key Modules/Features Managed by libuv**

1. **File System** → `fs.readFile()`, `fs.writeFile()`, etc.
2. **Timers** → `setTimeout()`, `setInterval()`, `setImmediate()`.
3. **I/O Operations** → Handles file read/write, API calls, DB connections.
4. **Networking** → `http` module (requests, sockets).
5. **DNS Resolution** → Converts domain names (e.g., google.com → IP).
6. **Child Processes** → Runs separate programs without blocking (`child_process.exec()`, `fork()`).
7. **TCP & UDP Sockets** → Send/receive data over the internet.
8. **Thread Pool** → Background threads for CPU-intensive tasks like (`crypto`, `fs`).
9. **Signals Handling** → Captures OS signals.
10. **Event Loop** → Manages task execution order.

## **10. What is the Code Execution Flow with libuv (Non Blocking)?**

**Example:**

```javascript
const fs = require("node:fs");
const https = require("https");

console.log("Hello World");

var a = 1078698;
var b = 20986;

https.get("https://dummyjson.com/products/1", (res) => {
  console.log("Fetched Data Successfully");
});

setTimeout(() => {
  console.log("setTimeout called after 5 seconds");
}, 5000);

fs.readFile("./file.txt", "utf8", (err, data) => {
  console.log("File Data : ", data);
});

function multiplyFn(x, y) {
  const result = a * b;
  return result;
}

var c = multiplyFn(a, b);

console.log("Multiplication result is : ", c);
```

### **The Flow**

1. **Synchronous Code Execution**

   - `console.log("Hello World");`  
     This line runs immediately on the main thread.
   - Variables `a` and `b` are declared and initialized.
   - The multiplication function on the second last line of the code `multiplyFn(a, b)` is defined and then called, computing the result synchronously.
   - `console.log("Multiplication result is : ", c);` logs the computed result.
   - **Output**

   ```bash
   Hello World
   Multiplication result is :  22637556228
   ```

2. **Asynchronous Operations Handled by libuv**

   - **HTTP Request:**

     ```js
     https.get("https://dummyjson.com/products/1", (res) => {
       console.log("Fetched Data Successfully");
     });
     ```

     This initiates a network request. The HTTP request is offloaded to the OS (via libuv) and its callback is queued when the data is received.

   - **Timer:**

     ```js
     setTimeout(() => {
       console.log("setTimeout called after 5 seconds");
     }, 5000);
     ```

     The timer is handled by libuv’s timer phase. After 5 seconds, the callback is queued for execution.

   - **File Read:**
     ```js
     fs.readFile("./file.txt", "utf8", (err, data) => {
       console.log("File Data : ", data);
     });
     ```
     The file system operation is sent to libuv’s thread pool. Once the file is read, its callback is added to the event loop for execution.
     **Output**

   ```bash
   File Data :  This is a file e
   Fetched Data Successfully
   setTimeout called after 5 seconds
   ```

   - `File Read` was executed first because the file data was slow and it got read instantly
   - then `fetch` because in my case its a dummy response so it has low size but it should take time so thats why it was second
   - in the last `setTimeout` because it took the maximum time of 5s

## **11. What Does "Sync" After a Module Name Mean? What Happens When We Use them?**

- When you see **Sync** at the end of a function name (like `crypto.pbkdf2Sync()`, `fs.readFileSync()`), it means that the function is synchronous and block the main thread while it’s running. This is something you should cautious about, especially in performance-sensitive applications.
- **Blocking Behavior**: The synchronous version of modules will block the event loop, preventing any other code from executing until the task is complete. This can application to become unresponsive if used inappropriately.

### **Example Using `crypto.pbkdf2Sync()`**

**What is `crypto` module?**:

- Node.js has a core library known as
  `crypto`, which is used for cryptographic operations like generating secure keys, hashing passwords, and more.
- The crypto module is one of the core modules provided by Node.js, similar to other core modules like `https` , `fs` (file system), and `zlib` (used for compressing files).
- These core modules are built into Node.js, so when you write require('crypto') , you're importing a module that is already present in Node.js
- You can also import it using `require(node:crypto)`to explicitly indicate that it’s a core module, but this is optional.

**Example: Blocking the Event Loop**

```js
const crypto = require("crypto");

console.log("Start");

setTimeout(() => {
  console.log("Timeout callback executed");
}, 0);

// Blocking the main thread
crypto.pbkdf2Sync("password", "salt", 50000000, 50, "sha512");

console.log("End");
```

**Expected Output:**

```
Start
<!-- took around 40s -->
End
Timeout callback executed
```

**Why?**

1. `"Start"` prints first (synchronous).
2. `setTimeout(...)` is scheduled, but it **can't execute** even if the delay is 0, but it is an async function so it'll only run after the callstack is empty.
3. **`pbkdf2Sync` runs and blocks the thread for several(_about 40_) seconds**.
4. Once `pbkdf2Sync` completes, `"End"` prints.
5. Only **after all synchronous code is done, the event loop processes `setTimeout`**, printing `"Timeout callback executed"`.

## **12. List the tasks handled by Libuv and Microtask Queue.**

### **Tasks Handled by libuv**

libuv is responsible for handling asynchronous operations in Node.js, mainly system-level I/O tasks.

1. **File System Operations** → (`fs.readFile()`, `fs.writeFile()`)
2. **Network Requests** → (`http.get()`, `https.request()`)
3. **Timers** → (`setTimeout()`, `setInterval()`, `setImmediate()`)
4. **DNS Lookups** → (`dns.lookup()`)
5. **Crypto Operations** → (`crypto.pbkdf2()`, `crypto.randomBytes()`)
6. **Process Operations** → (`child_process.exec()`, `process.nextTick()`)
7. **TCP/UDP Sockets** → (`net` module, `dgram` module)
8. **Worker Threads** → (`worker_threads` module)

### **Tasks Handled by the Microtask Queue**

Microtasks are JavaScript-level tasks that execute after synchronous code but before I/O and timers.

1. **Promises (`async/await`)** → Executes `.then()` and `.catch()` callbacks.
2. **`fetch()` API (Node.js 18+)** → Fetch responses are handled in the microtask queue.
3. **`queueMicrotask()`** → Manually schedules a microtask.
4. **`process.nextTick()`** → Runs immediately after synchronous code, before microtasks. _(It has even higher priority than microtasks!)_
