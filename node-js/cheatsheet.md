# Index

## 1. **[Foundation](#1-foundation-1)**

1. **[What is Node.js? Why is it usefull](#1-what-is-nodejs-why-is-it-usefull)**
2. **[History of Node JS](#2-history-of-nodejs)**
3. **[JS on a Server](#3-js-on-a-server)**
   1. **[What is a server?](#what-is-a-server)**
   2. **[What is V8?](#what-is-v8)**
4. **[Exporting and Importing Modules in Node.js (using CommonJS)](#4-exporting-and-importing-modules-in-nodejs-using-commonjs)**
5. **[What is `Module.export`?](#5-what-is-moduleexport)**
6. **[How `require()` Works in Node.js](#6-how-require-works-in-nodejs)**
7. **[Exporting and Importing Modules in Node.js (using ES6 Modules)](#7-exporting-and-importing-modules-in-nodejs-using-es6-modules)**
8. **[CommonJS vs ES6 Modules (Comparison Table)](#8-commonjs-vs-es6-modules-comparison-table)**
9. **[What is libuv?](#9-what-is-libuv)**
10. **[What is the Code Execution Flow with libuv (Non Blocking)?](#10-what-is-the-code-execution-flow-with-libuv-non-blocking)**
11. **[What Does "Sync" After a Module Name Mean? What Happens When We Use them?](#11-what-does-sync-after-a-module-name-mean-what-happens-when-we-use-them)**
12. **[12. List the tasks handled by Libuv and Microtask Queue.](#12-list-the-tasks-handled-by-libuv-and-microtask-queue)**
13. **[How libuv operate and manage the Event loop?](#13-how-libuv-operate-and-manage-the-event-loop)**
14. **[ Thread Pool in Node.js](#14-thread-pool-in-nodejs)**

## 2. **[Server Creation (_Theory_)](#2-server-creation-theory-1)**

1. **[Understanding Servers](#1-understanding-servers)**
2. **[Understanding Client-Server Architecture](#2-understanding-client-server-architecture)**
3. **[How Is Data Sent When You Make a Server Request?](#3-how-is-data-sent-when-you-make-a-server-request)**
4. **[Can We Create Multiple Servers?](#4-can-we-create-multiple-servers)**
5. **[Understanding Distributed Server Architecture Explained](#5-understanding-distributed-server-architecture-explained)**
6. **[Sockets vs Web Socets](#6-sockets-vs-web-socets)**
7. **[How to create a Node.js Server](#7-how-to-create-a-nodejs-server)**

## 3.**[Node JS built-in modules]()**

1. **[File System (fs) Module in Node.js](#1-file-system-fs-module-in-nodejs)**

## 4. **[Express JS - Node JS library](#4-express-js---node-js-library-1)**

1. **[What is Express.js and why is it used?](#1-what-is-expressjs-why-is-it-used)**
2. **[How to Install Express.js in a Node.js Project?](#2-how-to-install-expressjs-in-a-nodejs-project)**
3. **[How to Set Up a Basic Express Server?](#3-how-to-set-up-a-basic-express-server)**
4. **[Define HTTP and Types of HTTP Requests in Express.js](#4-define-http-and-types-of-http-requests-in-expressjs)**
5. **[Routing in Express.js?](#5-routing-in-expressjs)**
6. **[How to read dynamic routes and query parameters?](#6-how-to-read-dynamic-routes-and-query-parameters)**
7. **[Does Order Matter in Route Handling in Express.js?](#7-does-order-matter-in-route-handling-in-expressjs)**
8. **[Difference Between `app.use()` and Other HTTP Methods (`app.get()`, `app.post()`, etc.)?](#8-difference-between-appuse-and-other-http-methods-appget-apppost-etc)**
9. **[What is `next()` in Express.js?](#9-what-is-next-in-expressjs)**
10. **[10. Can We Use Multiple Route Handlers in One Route?](#10-can-we-use-multiple-route-handlers-in-one-route)**
11. **[What are Middlewares in Express.js?](#11-what-are-middlewares-in-expressjs)**
12. **[What is Error Handling in Express?](#12-what-is-error-handling-in-express)**

## 5. **[Database and Database Management System(DBMS)](#5-database-and-database-management-systemdbms-1)**

1. **[Introduction](#1-introduction)**
2. **[Databases](#2-databases)**

## 6. **[Authentications and Authorization](#6-authentications-and-authorization-1)**

1. **[What is Authentication? Why Do We Need It? Explain the working also.](#1-what-is-authentication-why-do-we-need-it-explain-the-working-also)**
2. **[ What is Authorization and Difference between Authentication and Authorization](#2-what-is-authorization-and-difference-between-authentication-and-authorization)**
3. **[Implementing Authentication in Express.js Using Cookies(_Hardcode tokens_)](#3-implementing-authentication-in-expressjs-using-cookieshardcode-tokens)**
4. **[Implementing Authentication in Express.js Using JWT and Cookies](#4-implementing-authentication-in-expressjs-using-jwt-and-cookies)**

# 1. **Foundation**

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

### **How is Node.js Different from PHP or Java (Traditional Languages)**?

| Feature            | Node.js                         | PHP / Java                             |
| ------------------ | ------------------------------- | -------------------------------------- |
| **Execution**      | Single-threaded, non-blocking   | Multi-threaded, blocking               |
| **Speed**          | Fast (V8 engine, non-blocking)  | Slower (handles one request at a time) |
| **Language**       | JavaScript (frontend & backend) | PHP (backend), Java (strict)           |
| **Real-time Apps** | Excellent for real-time apps    | Not ideal for real-time                |
| **Scalability**    | High                            | Moderate                               |
| **Learning Curve** | Easier (if you know JavaScript) | Can be more complex                    |

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

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

[Go to top ↑](#index)

## **13. How libuv operate and manage the Event loop?**

### **The event loop in Node.js runs in multiple phases, managed by libuv Here are the main 4 phases:**

1.  **Timers Phase**: In this phase, all callbacks that were set using setTimeout or setInterval are executed. These timers are checked, and if their time has expired, their corresponding callbacks are added to the callback queue for execution.
2.  **Poll Phase**: After timers, the event loop enters the Poll phase, which is crucial because it handles I/O callbacks. For instance, when you perform a read operation using `fs.readFile` , the callback associated with this I/O operation will be executed in this phase. The Poll phase is responsible for handling all I/Orelated tasks, making it one of the most important phases in the event loop.
3.  **Check Phase**: Next is the Check phase, where callbacks scheduled by the `setImmediate` function are executed. This utility API allows you to execute callbacks immediately after the Poll phase, giving you more control over the order of operations.
4.  **Close Callbacks Phase**: Finally, in the Close Callbacks phase, any callbacks associated with closing operations, such as socket closures, are handled. This phase is typically used for cleanup tasks, ensuring that resources are properly released.

    It fires callbacks for events like:

    - `close` on streams.
    - `disconnect` on network sockets.
    - `exit` events for child processes.

### **Before the event loop moves to each of its main phases (Timers, I/O Callbacks, Poll, Check, and Close Callbacks)**

- it first processes any pending microtasks which include tasks scheduled using `process.nextTick()` and Promise callbacks. This ensures that these tasks are handled promptly before moving on to the next phase.
- `process.nextTick()` is a special function in Node.js that runs the callback immediately after the current operation, before the event loop continues to the next phase.

### **Node.js Event Loop Cycle (Step-by-Step)**

![img](https://res.cloudinary.com/dy3m6ztbp/image/upload/fl_preserve_transparency/v1741718852/diagram-export-3-12-2025-12_16_52-AM_znyc9k.jpg?_s=public-apps)

1. **Start Event Loop Cycle**

2. **Process `process.nextTick()` Callbacks**

   - Execute **all** `process.nextTick()` callbacks (highest priority).

3. **Process Promise Callbacks (Microtasks)**

   - Execute **all** Promise callbacks (`.then()`, `catch()`, `finally()`).

4. **Move to Timers Phase**

   - Execute **timer callbacks** (`setTimeout()`, `setInterval()`).

5. **Move to I/O Callbacks Phase**

   - Execute **I/O callbacks** (e.g., network, fs callbacks from the thread pool).

6. **Move to Poll Phase**

   - Retrieve **new I/O events** and **execute callbacks** (e.g., waiting for incoming connections, reading files).

7. **Move to Check Phase**

   - Execute `setImmediate()` callbacks.

8. **Move to Close Callbacks Phase**

   - Execute `close` callbacks (e.g., socket close, `server.close()`).

9. **Repeat Event Loop Cycle** 🔄

10. Go back to step 1 and **continue the cycle** until there’s no more work to do!

### **Using Example**:

```javascript
const fs = require("fs");

setImmediate(() => console.log("setImmediate")); // A

setTimeout(() => console.log("Timer expired"), 0); // B

Promise.resolve().then(() => console.log("Promise")); // C

fs.readFile("./file.txt", "utf8", () => {
  // D
  setTimeout(() => console.log("Inner timer"), 0); // E
  process.nextTick(() => console.log("Inner nextTick")); // F
  setImmediate(() => console.log("2nd setImmediate")); // G
  console.log("File Reading CB"); // H
});

process.nextTick(() => console.log("next Tick")); // I

console.log("line of the file."); // J
```

**Step-by-Step Execution (With Event Loop Cycle)**

**1. Run the top-level code (Before Event Loop starts)**

This runs immediately (_Synchronous code_):

```
J ➡ "line of the file."
```

**2. Process `process.nextTick()` callbacks**

- Runs **before Promises and Event Loop Phases**.

```
I ➡ "next Tick"
```

**3. Process Promise callbacks (Microtasks)**

- Runs **after process.nextTick()** (_of step 2_).

```
C ➡ "Promise"
```

**😈⚠️ Now the Event Loop Phases Begin!**

**4. Timers Phase**

`setTimeout()` callbacks:

```
B ➡ "Timer expired"
```

**5. I/O Callbacks Phase**

`fs.readFile()` completes (asynchronous I/O), so its callback executes:

```
H ➡ "File Reading CB"
```

- Inside the callback:
  - `process.nextTick()` → Queued immediately.
  - `setTimeout()` → Queued for **next** Timers phase.
  - `setImmediate()` → Queued for **Check** phase.

**6. Process `process.nextTick()` again (after I/O callback)**

```
F ➡ "Inner nextTick"
```

**7. Promise callbacks again?**

_None here_.

**8. Check Phase**

- `setImmediate()` callbacks:

```
A ➡ "setImmediate" // scheduled before the event loop
G ➡ "2nd setImmediate"
```

**Timers Phase (again, for the inner setTimeout)**

- `setTimeout()` callback inside `fs.readFile()`:

```
E ➡ "Inner timer"
```

**No More Tasks! The Event Loop Ends (for now).**
✅ **Final Output Order**

```
line of the file.         (J)
next Tick                 (I)
Promise                   (C)
Timer expired             (B)
File Reading CB           (H)
Inner nextTick            (F)
setImmediate              (A)
2nd setImmediate          (G)
Inner timer               (E)
```

[Go to top ↑](#index)

## **14. Thread Pool in Node.js**

### **What is a Thread Pool?**

- **Thread Pool** = A group of threads (workers) that **handle expensive tasks** in the background, so the **main thread (Event Loop)** stays free.
- It isManaged by **libuv** in Node.js.

_Whenever there's an asynchronous task, **V8** offloads it to libuv. For example, when reading a file, libuv uses one of the threads in its thread pool. The file system (fs) call is assigned to a thread in the pool, and that thread makes a request to the OS. While the file is being read, the thread in the pool is fully occupied and cannot perform any other tasks. Once the file reading is complete, the engaged thread is freed up and becomes available for other operations. For instance, if you're performing a cryptographic operation like hashing, it will be assigned to another thread. There are certain functions for which libuv uses the thread pool._

### **Default Size**

- In Node.js, the **default size** of the thread pool is **4** threads:

  - `UV_THREADPOOL_SIZE = 4`

  - Now, suppose you make 5 simultaneous file reading calls. What happens is that 4 file calls will occupy 4 threads, and the 5th one will wait until one of the threads is free.

- If your production system involves heavy file handling or other tasks that benefit from additional threads, you can **adjust** the thread pool **size** accordingly to better suit your needs.

  - You can set it to 8 like this:

    ```bash
    UV_THREADPOOL_SIZE = 8 node app.js
    ```

    Or in code :

    ```js
    process.env.UV_THREADPOOL_SIZE = 8;
    ```

### **What is it Used For?**

Thread Pool handles **non-blocking** tasks that are **CPU-intensive or I/O intensive**, like:

1. **File System operations** → `fs.readFile`, `fs.writeFile`
2. **DNS lookups** → `dns.lookup`
3. **Cryptography** → `crypto.pbkdf2`, `crypto.scrypt`
4. **Compression** → `zlib` module

_These tasks are **offloaded to worker threads**, not handled by the Event Loop itself._

### **Example of Thread Pool**

```js
const crypto = require("crypto");

console.time("Password Hashing");

for (let i = 0; i < 5; i++) {
  crypto.pbkdf2("password", "salt", 100000, 64, "sha512", () => {
    console.timeEnd("Password Hashing");
  });
}
```

➡️ This runs **5 heavy crypto tasks** using the **Thread Pool**.

- Scenario 1️⃣: **We run 5 tasks, but pool size = 4 (default)**

  - **4 tasks** run **immediately** on **4 threads**
  - The **5th task** **waits in line** until a thread becomes free.
  - **Tasks take longer** to complete (queueing happens).

- Scenario 2️⃣: **Increase Pool Size to 5**

  ```bash
  UV_THREADPOOL_SIZE=5 node app.js
  ```

  - All **5 tasks** run **in parallel**, no waiting.
  - **Faster** completion.

### **Summary**

| **Topic**           | **Details**                          |
| ------------------- | ------------------------------------ |
| **Thread Pool**     | Manages background async tasks       |
| **Default Size**    | 4 threads                            |
| **Max Size**        | 1024                                 |
| **How to Change**   | `process.env.UV_THREADPOOL_SIZE = 8` |
| **Used For**        | fs, dns, crypto, zlib                |
| **If Exceed Limit** | Extra tasks wait in queue            |

[Go to top ↑](#index)

---

# 2. **Server Creation (_Theory_)**

## **1. Understanding Servers**

### **What is a Server?**

The term **server** can refer to both **hardware** and **software**, depending on the context:

1. **Hardware (Physical Server):**

   - A **computer (machine)** that provides **resources** (like files, databases) and **services** (like hosting a website) to other computers (called **clients**) over a **network**.
   - Example: A big computer sitting in a data center.

2. **Software (Server Application):**
   - A **program** or **application** that handles **requests** from clients and sends them **responses** (data or services).
   - Example: A **web server** like **Apache** or a **Node.js app** serving APIs.

### **Deploying an Application on a Server**

When people say "**Deploy your app on a server**", it generally means:

1. **Hardware Part**

   - You need a **physical machine (server)** to run your app.
   - It has **CPU**, **RAM**, **storage**, and **network** connectivity.

2. **Operating System (OS)**

   - The server hardware runs an **OS** like **Linux** or **Windows Server**.
   - Your application runs **on top of this OS**.

3. **Server Software**
   - Software that handles incoming **requests** and sends **responses**.
   - Examples:
     - **Apache**, **Nginx** (web servers)
     - **Node.js application server**

### **AWS and Cloud Computing**

**AWS (Amazon Web Services)** provides **cloud-based servers and resources**.

- **EC2 Instance**

  - An **EC2 instance** is like renting a **virtual server** from AWS.
  - AWS manages the **physical hardware**, and you use the **virtual machine** to deploy your app.

**Benefits of AWS Servers**

- **Scalability**

  - You can easily **scale** (increase) resources like **RAM**, **CPU**, or **storage** with a few clicks.
  - Much easier than upgrading a physical machine (like your laptop).

- **Reliability**
  - AWS servers have:
    - Constant **power backup**
    - **Internet backup**
    - **Redundant systems** (multiple backups)
  - Ensures your app is **always available** (high availability), unlike a personal computer that might shut down.

### **Can You Use Your Own Laptop as a Server?**

**Yes, you can!**  
But... there are **limitations** you should know.

**Limitations of Using Your Laptop as a Server**

1. **Hardware Constraints**

   - Your laptop has **limited resources** like **RAM**, **CPU**, and **storage**.
   - Not suitable for handling **large numbers of requests** from many users at once.
   - It may **slow down** or **crash** under heavy load.

2. **Internet Connectivity**

   - Home internet is usually **less reliable**.
   - Often uses a **dynamic IP address**, which **changes frequently**.  
     🔹 This makes it **hard to keep your server accessible** on the internet.
   - Professional servers use **static IP addresses** that stay the same.

3. **Power and Maintenance**
   - You need to make sure your **laptop is always on**,  
     ✅ Connected to the **internet**  
     ✅ Has **backup power** (like UPS)
   - Managing this can be **difficult and unreliable** at home.
   - **AWS** and other **cloud services** handle these issues automatically.

[Go to top ↑](#index)

## **2. Understanding Client-Server Architecture**

### **Client vs Server**

- **Client**

  - A **client** is the **user** or **device** (like a web browser) that requests data or services from a **server**.
  - Each client has its own **IP address**.

- **Server**

  - A **server** is a **machine or application** that listens for client requests.
  - It **retrieves** the requested **data/files** and **sends** them back to the client.
  - The server also has its own **IP address**.

### **How It Works**

1. The **client** opens a **socket connection** to the **server** (not the same as WebSocket).
2. The **server** application **listens** for incoming requests.
3. The server **processes** the request (like fetching a file).
4. It **responds** by sending the **data back** to the client.

### **Multiple Clients and Socket Connections**

- **Multiple clients** can connect to the server **at the same time**.
- Each client **opens a socket connection** to request data.
- After receiving data, the **connection is closed**.
- For a new request, a **new socket connection** is created.

- **Sockets** use the **TCP/IP protocol** for reliable communication.

### **What is a Protocol?**

- A **protocol** is a set of **rules** that define **how computers communicate** with each other.
- Protocols determine the **format** in which data is sent between devices.

**Common Protocols**

- **FTP (File Transfer Protocol)**: Transfers files between computers.
- **SMTP (Simple Mail Transfer Protocol)**: Sends emails.
- **HTTP (HyperText Transfer Protocol)**: Used by web servers to communicate with clients.

**Web Servers and HTTP**

- A **web server** usually means an **HTTP server**.
- **HTTP** defines how the **client and server exchange data**.
- When we build a server, it's often an **HTTP server** handling these **data exchanges**.

## **3. How Is Data Sent When You Make a Server Request?**

### **Data Is Sent in Chunks (Packets)**

- When data is transmitted over the internet, it is **broken into small units** called **packets**.
- These packets are **sent individually** and **reassembled** at the destination (your computer).
- **Remember:**
  - The **TCP/IP protocol** handles
  - Sending these packets
  - Ensuring data arrives correctly and in order.

### **Streams and Buffers in Node.js**

- In **Node.js**, data **is handled in chunks**, which are processed as **streams**.
- **Buffers** temporarily **store these chunks** until they can be processed.
- Example:  
  ➡️ **Streaming a video** → data comes in small chunks → buffers hold it → video plays.

### **We Use Domain Names, Not IP Addresses**

- Humans don’t remember **IP addresses** (e.g., `142.250.195.206`), so we use **domain names** (like `youtube.com`).

- it's like Saving phone numbers in your contacts with **names** instead of remembering the numbers.

### **What Happens When You Request a Website?**

1. You enter a **URL** like `youtube.com` in your browser.
2. The browser contacts a **DNS server**.
3. **DNS (Domain Name System)** translates the domain name to an **IP address**.
4. The browser sends a **request to the server** at that IP address.
5. The **HTTP server** processes your request and sends **data back**.

### **Data Transfer Behind the Scenes**

- The **response data** (like a video) is sent as **chunks**, also known as **streams**.
- These streams are processed and temporarily held in **buffers**.
- That's why sometimes you see a video **buffering**—it’s collecting enough data in the buffer to continue playback smoothly.

### **Important Terms**

| **Concept**                  | **Simple Definition**                                                                  |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| **Packets**                  | Small pieces of data that travel across the internet to reach their destination.       |
| **TCP/IP Protocol**          | A set of rules that ensures data packets are sent, received, and arranged correctly.   |
| **Streams in Node.js**       | A way or method to handle large amounts of data in small parts instead of all at once. |
| **Buffers in Node.js**       | A temporary storage space for data(_streams_) before it is processed or sent.          |
| **DNS (Domain Name System)** | A system that converts website names (like youtube.com) into IP addresses.             |
| **HTTP Server**              | A program that receives user requests, processes them, and sends back responses.       |

[Go to top ↑](#index)

## **4. Can We Create Multiple Servers?**

**Yes, you can create multiple HTTP servers!**

### **How Multiple Servers Work**

When you create an **HTTP server** in Node.js, you're basically starting an app that listens for requests on a **specific port number**.

- A **port** is like a door to your application.
- Each port has its own number (e.g., `3000`, `3001`).
- A **single computer (server hardware)** can run **multiple applications**.
- You **differentiate servers** using their **port numbers**.

**Example**

- IP Address: `102.209.1.3`
- Port 3000 → React App
- Port 3001 → Node.js App

When someone requests:

- `102.209.1.3:3000` → It goes to the React app.
- `102.209.1.3:3001` → It goes to the Node.js app.

### **Domain Names & Routing**

- When you type a **domain name** like `youtube.com`, a **DNS server** converts it into an **IP address** (e.g., `102.209.1.3`).
- If you specify a **port number**, it tells which application to reach.

**Example**:

- `namastedev.com` → React app on **port 3000**
- `namastedev.com/node` → Node.js app on **port 3001**

By **adding paths (like `/node`)** to your URL, you can **route** requests to different servers or applications.

### **Why This is Useful**

- You can run **multiple services** (React frontend, Node.js backend, etc.) on **different ports** of **one server**.
- Makes your system **scalable** and **organized**.
- In large companies, the architecture is often distributed across **multiple** servers rather than relying on a single server. This approach helps manage different aspects of the application efficiently and ensures **scalability**, **reliability**, and **performance**

[Go to top ↑](#index)

## **5. Understanding Distributed Server Architecture Explained**

Imagine your app (like **youtube.com**) is **big** and **serves millions of users**. You can’t rely on **one server** to do everything! So, companies use a **distributed server architecture**, where different servers handle different tasks.

### **1. Separation of Concerns**

**Frontend Server**

- **What it does**: Handles the **user interface (UI)**—HTML, CSS, JavaScript.
- **Example**: When someone opens **youtube.com**, they get the website’s layout and design from this server.
- **Bonus**: It can also make **API calls** to fetch dynamic data.

**Backend Server**

- **What it does**: Processes **business logic**, **handles requests**, talks to the **database**, and sends **data** to the frontend.
- **Example**: Login forms, search queries, or orders go to the backend server.

In **small apps**, both frontend and backend may run on the **same server**.  
In **big apps**, they are often **separated** for **better performance**, **security**, and **scalability**.

### **2. Dedicated Database Server**

**What it does**: Stores all your **data**—users, orders, comments, etc.

- This server is **optimized for data storage and fast access**.
- The **backend server** talks to the **database server** to fetch or save data.

Example: When you log in to **youtube.com**, your login info is checked in the **database server**.

### **3. Media and File Servers**

**What they do**: Store **large files** like **videos**, **images**, and **documents**.

- These servers are **optimized** to send **big files quickly** to users.
- Often connected to a **CDN (Content Delivery Network)**, which copies files to servers around the world for **faster delivery**.

Example: When you watch a video on **youtube.com**, it streams from a **media server**.  
Images load from a **CDN** close to you (for speed).

### **4. Inter-Server Communication**

**How servers talk to each other**:

- The **frontend** or **backend** may need to **communicate** with other servers (API calls) to get the **right data** or files.
- Example: You click a video on **youtube.com**, the backend **calls** the media server, gets the video link, and sends it back to your browser.

### **Example: youtube.com Architecture**

| **Part** | **Where It’s Hosted / What It Does**                           |
| -------- | -------------------------------------------------------------- |
| Frontend | AWS server → Serves the **website UI** (HTML, CSS, JS)         |
| Backend  | AWS server → Handles **logic**, **API requests**, and **data** |
| Database | Dedicated DB server → Stores **users**, **comments**, etc.     |
| Videos   | Media server → Streams **large videos**                        |
| Images   | CDN → Sends **images** quickly from servers near the user      |

---

### **Why Use Distributed Servers?**

- **Better Performance** (each server does a specific job)
- **Scalability** (easy to add more servers if needed)
- **Security** (sensitive data stays safe in its own server)
- **Reliability** (if one server fails, others can keep working)

[Go to top ↑](#index)

## **6. Sockets vs Web Socets**

### **What is a Socket?**

- A **socket** is a **communication link** between **two systems** (client & server).
- It's how your **browser talks to a server** when you visit a website.

**How It Works (Traditional Socket / HTTP Request)**

1. You open a website (client sends a **request**)
2. The server processes it and **sends a response**
3. The **connection (socket)** is **closed**
4. If you want new data, you have to make **another request**

**One request → One response** → Connection **closes** each time  
**Example**: Visiting **youtube.com**, clicking a link sends a request to the server.

### **What is WebSocket?**

- A **WebSocket** is an **advanced socket connection** that **stays open**!
- Once it’s connected, it **doesn’t close** after sending/receiving data.

**How It Works (WebSocket)**

1. Client and server **open a connection**
2. The connection **stays open** (persistent connection)
3. **Both** client **and** server can send **messages anytime**, **continuously**, without reconnecting

**Real-time communication**  
 **Example**: **Chat apps**, **online games**, **stock tickers**, **live notifications**

### **When to Use What?**

| **Use Traditional Socket (HTTP)** | **Use WebSocket**                         |
| --------------------------------- | ----------------------------------------- |
| Normal websites (static content)  | **Chat apps**, online games               |
| Blog articles, portfolio sites    | **Live stock prices**, notifications      |
| E-commerce product browsing       | **Collaborative apps** (like Google Docs) |

[Go to top ↑](#index)

## **7. How to create a Node.js Server**

```javascript
const http = require("http");

const server = http.createServer(function (req, res) {
  if (req.url === "/getSecretData") {
    res.end("there is no secret data");
    return; // Stop here so it doesn't continue to the next line
  }

  res.end("Hello world");
});

server.listen(3000, () => {
  console.log("Server is running on http://localhost:3000");
});
```

### **How it works:**

- If you open `http://localhost:3000/getSecretData` → You get `there is no secret data`.
- Any other route (like `/`, `/about`) → You get `Hello world`.

### **Terms**:

| **Part**              | **What it does**                        |
| --------------------- | --------------------------------------- |
| `http.createServer()` | Creates the basic Node.js server        |
| `req.url`             | Reads the URL path the user requested   |
| `res.end()`           | Sends the response and ends the request |
| `server.listen(3000)` | Starts the server on port 3000          |

[Go to top ↑](#index)

---

# 3. **Node JS built-in modules**

## **1. File System (fs) Module in Node.js**

Node.js provides a built-in **File System (fs)** module that allows you to interact with the file system on your computer. With this module, you can perform operations like reading, writing, updating, deleting files, and creating directories.

The `fs` module has both **synchronous** and **asynchronous** methods for handling these operations, but the asynchronous ones are commonly used in Node.js to prevent blocking the event loop.

#### how to include `fs`":

- If you're using ES Modules (type: "module")

  ```js
  import fs from "fs";
  ```

- If your project uses CommonJS (type: "commonjs")
  ```js
  let fs = require('fs')'
  ```

### **Commonly Used `fs` Methods**

- **`fs.writeFile()`**: Creates or overwrites a file.
- **`fs.appendFile()`**: Appends data to a file.
- **`fs.rename()`**: Renames a file.
- **`fs.copyFile()`**: Copies a file.
- **`fs.unlink()`**: Deletes a file.
- **`fs.mkdir()`**: Creates a new directory.
- **`fs.rmdir()`**: Deletes a directory.
- **`fs.readFile()`**: Reads the content of a file.

#### 1. **Create a File**

To create a new file, you can use `fs.writeFile()`. If the file already exists, it will overwrite the content.

```javascript
fs.writeFile("name.txt", "Name: Arshit JS", (err) => {
  if (err) console.error(err);
  else console.log("File created successfully!");
});
```

#### 2. **Overwrite (Update) a File**

If you want to overwrite an existing file with new content, you can use the same `fs.writeFile()` method.

```javascript
fs.writeFile("name.txt", "Name: Arshit Html", (err) => {
  if (err) console.error(err);
  else console.log("File overwritten successfully!");
});
```

#### 3. **Append Data to a File**

To append content to an existing file without deleting its current content, use `fs.appendFile()`.

```javascript
fs.appendFile("name.txt", "\nName: Sankruti Html", (err) => {
  if (err) console.error(err);
  else console.log("Content appended successfully!");
});
```

#### 4. **Rename a File**

To rename a file, you can use `fs.rename()`.

```javascript
fs.rename("name.txt", "naam.txt", (err) => {
  if (err) console.error(err);
  else console.log("File renamed successfully!");
});
```

#### 5. **Copy a File**

To copy a file to another location, you can use `fs.copyFile()`.

```javascript
fs.copyFile("name.txt", "./copy/naam2.txt", (err) => {
  if (err) console.error(err);
  else console.log("File copied successfully!");
});
```

#### 6. **Delete a File**

To delete a file, you can use `fs.unlink()`.

```javascript
fs.unlink("name.txt", (err) => {
  if (err) console.error(err);
  else console.log("File deleted successfully!");
});
```

#### 7. **Create a Directory (Folder)**

To create a new folder (directory), use `fs.mkdir()`.

```javascript
fs.mkdir("./copy", (err) => {
  if (err) console.error(err);
  else console.log("Directory created successfully!");
});
```

#### 8. **Delete a Directory**

To delete a directory (folder), use `fs.rmdir()`. Note that if the directory is not empty, it will throw an error.

```javascript
fs.rmdir("./copy/", (err) => {
  if (err) console.error(err);
  else console.log("Directory deleted successfully!");
});
```

##### **Deleting a Directory with Files:**

To delete a directory **even if it contains files**, you can use the `{ recursive: true }` option.

```javascript
fs.rmdir("./copy/", { recursive: true }, (err) => {
  if (err) console.error(err);
  else console.log("Directory and its contents deleted successfully!");
});
```

#### 9. **Read a File**

To read the content of a file, use `fs.readFile()`.

```javascript
fs.readFile("name.txt", (err, data) => {
  if (err) console.error(err);
  else console.log("File content: ", data.toString());
});
```

[Go to top ↑](#index)

# 4. **Express JS - Node JS library**

## **1. What is Express.js? Why is it used?**

**Express.js** is a **fast, minimal, and flexible** web framework for **Node.js** that makes it easier to build web applications and APIs. It is **built on top of Node.js's HTTP module** and provides powerful tools to handle routes, middleware, requests, and responses efficiently.

### **Why is Express.js Used?**

1. **Simplifies Server Creation** 🏗️

   - Without Express, creating a server in Node.js requires writing a lot of boilerplate code using the **`http` module**.
   - Express makes it much easier with just a few lines of code.

2. **Routing Made Easy** 🚦

   - Express allows defining multiple **routes** (URLs) for different parts of your application.
   - Example: Handling `/`, `/about`, `/contact` routes in a simple way.

3. **Middleware Support** 🔄

   - Middleware functions help handle requests, modify responses, authenticate users, and log data.
   - Example: **Logging**, **authentication**, **error handling**, etc.

4. **Supports REST APIs** 🔌

   - It’s widely used for building **RESTful APIs** that allow communication between frontend and backend.

5. **Works with Databases** 💾

   - Easily integrates with databases like **MongoDB (Mongoose), MySQL, PostgreSQL, Firebase**, **Supabase** etc.

6. **Large Community & Libraries** 🌍
   - Thousands of **third-party middleware** are available to extend Express functionality.

[Go to top ↑](#index)

## **2. How to Install Express.js in a Node.js Project?**

### **Install Express.js**

Run this command to install Express:

```bash
npm install express
```

This creates a `node_modules` folder and adds `express` as a dependency in your `package.json` file.

### **Step 5: Verify Installation**

You can check your `package.json` file under **dependencies**:

```json
"dependencies": {
  "express": "^4.18.2"
}
```

[Go to top ↑](#index)

## **3. How to Set Up a Basic Express Server?**

### **Syntax:**

```javascript
app.method_Name(route, callback);
```

### **Explanation:**

- **`app`** – it is your express server.
- **`method_name`** – this is placeholder for request methods eg .get .post etc
- **`route`** – The URL or route where the request is handled (e.g., `/`).
- **`callback`** – A function that gets executed when the route is accessed.
  - It takes two parameters:
    - **`req`** – The request object (contains info about the request).
    - **`res`** – The response object (used to send data back to the client).

```javascript
const express = require("express"); // Importing Express
const app = express(); // Creating an Express app

// Define a simple route
app.get("/", (req, res) => {
  res.send("Hello, Express!");
});

// Start the server
app.listen(3000, () => {
  console.log("Server is running on http://localhost:3000");
});
```

- **When someone visits** `http://localhost:3000/`,

  - The server sends back **"Hello Express"** as a response.

- **Explanation**:
  - `express()` creates an Express app.
  - `app.get()` handles GET requests at the root (`/`).
  - `app.listen()` starts the server on port 3000.
  - `res.send()` is used to send a response to the client.
    It can send strings, objects, arrays, or buffers. It automatically sets the Content-Type based on the data type sent.

[Go to top ↑](#index)

## **4. Define HTTP and Types of HTTP Requests in Express.js**

**HTTP** stands for **HyperText Transfer Protocol**.

It’s the communication protocol used for data exchange between clients (like browsers, Postman, frontend apps) and servers (like your Node.js/Express backend).

- **Client**: Makes a request (e.g., "Give me the data").
- **Server**: Sends a response (e.g., "Here’s the data you asked for").

**HTTP requests** (also called **methods**) are the message sent by the client to request the data from the server or to perform some actions.

**Different HTTP requests are:**

### **1️⃣ GET Request (Read Data)**

- Used to **fetch/read data** from the server.
- Example: Getting a list of users, fetching a product's details.

**Example:**

```javascript
const express = require("express");
const app = express();

app.get("/users", (req, res) => {
  res.send("Fetching all users...");
});

app.listen(3000, () => {
  console.log("Server running on http://localhost:3000");
});
```

- **URL:** `http://localhost:3000/users`
- **Response:** `"Fetching all users..."`

### **2️⃣ POST Request (Create Data)**

- Used to **send data** to the server to create a new resource.
- Example: Adding a new user to a database.

**Example:**

```js
app.use(express.json()); // Middleware to parse JSON body

app.post("/users", (req, res) => {
  const newUser = req.body; // Getting data from the request body
  res.send(`User ${newUser.name} added successfully!`);
});
```

🔹 **Sending Data:**

```json
{
  "name": "Arshit Kumar",
  "email": "arshitkumar222@gmail.com"
}
```

- **Response:** `"User Arshit Kumar added successfully!"`

### **3️⃣ PUT Request (Update Data)**

- Used to **update/modify an existing resource** on the server.
- Example: Updating user details.

**Example:**

```js
app.put("/users/:id", (req, res) => {
  const userId = req.params.id;
  res.send(`User with ID ${userId} has been updated.`);
});
```

- **URL:** `PUT http://localhost:3000/users/123`
- **Response:** `"User with ID 123 has been updated."`

### **4️⃣ PATCH Request (Partial Update)**

- Used to **update only specific fields** of a resource.
- Example: Updating only the email of a user.

**Example:**

```js
app.patch("/users/:id", (req, res) => {
  const userId = req.params.id;
  res.send(`User with ID ${userId} has been partially updated.`);
});
```

- **URL:** `PATCH http://localhost:3000/users/123`
- **Response:** `"User with ID 123 has been partially updated."`

### **5️⃣ DELETE Request (Remove Data)**

- Used to **delete a resource** from the server.
- Example: Deleting a user account.

#### **Example: Handling a DELETE request**

```js
app.delete("/users/:id", (req, res) => {
  const userId = req.params.id;
  res.send(`User with ID ${userId} has been deleted.`);
});
```

- **URL:** `DELETE http://localhost:3000/users/123`
- **Response:** `"User with ID 123 has been deleted."`

### **6️⃣ OPTIONS Request (Check Allowed Methods)**

- Used by browsers or clients to **ask the server what HTTP methods are allowed** on a specific route.

#### **Example: Handling an OPTIONS request**

```js
app.options("/users", (req, res) => {
  res.set("Allow", "GET, POST, PUT, PATCH, DELETE");
  res.send("Allowed methods: GET, POST, PUT, PATCH, DELETE");
});
```

- **Response:** `"Allowed methods: GET, POST, PUT, PATCH, DELETE"`

### **Summary Table**

| **Method**  | **Purpose**                 | **Example Use Case**                  |
| ----------- | --------------------------- | ------------------------------------- |
| **GET**     | Retrieve data               | Get user details (`GET /users/1`)     |
| **POST**    | Create a new resource       | Add a new user (`POST /users`)        |
| **PUT**     | Update an entire resource   | Update user info (`PUT /users/1`)     |
| **PATCH**   | Partially update a resource | Change user email (`PATCH /users/1`)  |
| **DELETE**  | Remove a resource           | Delete a user (`DELETE /users/1`)     |
| **OPTIONS** | Check allowed methods       | Ask server what methods are supported |

You can use **Postman** or **cURL** to send different requests and check responses.

[Go to top ↑](#index)

## **5. Routing in Express.js?**

**Routing** is how your app responds to different **client requests(_HTTP requests_)** (like GET, POST, etc.) made to a **specific URL path**.

Think of it like:

- _"When someone visits `/home`, show them the home page."_
- _"When someone submits a form to `/submit`, save their info."_

### In **Express.js**, we handle routes like this:

```js
app.METHOD(PATH, HANDLER);
```

- `app`: Your Express app.
- `METHOD`: HTTP method (GET, POST, PUT, etc.).
- `PATH`: Route path (URL endpoint).
- `HANDLER`: Callback function (runs when route is hit).

**Example**:

```js
app.get("/home", (req, res) => {
  res.send("Welcome to Home Page!");
});
```

### **Symbols/Characters in Express Route Paths**

These are **special characters** you can use to **define patterns** in your routes.  
They help you create **dynamic** and **flexible** routes.

| Symbol | Meaning                                                              |
| ------ | -------------------------------------------------------------------- |
| `:`    | Named route parameter (dynamic).                                     |
| `?`    | Optional character/segment.                                          |
| `+`    | One or more of the previous token.                                   |
| `*`    | Wildcard (anything can match).                                       |
| `()`   | Grouping for optional or complex matching.                           |
| `&`    | Query parameter separator (not part of route path, but part of URL). |

**1. `:` (Colon) → Route Parameters**

- Defines a **placeholder** in the URL path for **dynamic values**.
- Used for **dynamic routing**, e.g., accessing a user's profile by ID
- You can capture values from the URL using `req.params.id`

```js
app.get("/user/:id", (req, res) => {
  res.send(`User ID is ${req.params.id}`);
});
```

Visiting `/user/101` will respond with `User ID is 101`.

**2. `?` → Optional Character**

- Marks a **character or group as optional**.
- Makes the **previous character** or **group** optional
- Useful for routes where a segment **may or may not** be present.

```js
app.get("/ab?cd", (req, res) => {
  res.send("Matched abcd or acd");
});
```

- here it will make the `b` in `abcd` optional
- accept both `/abcd` and `/acd`.

**3. `+` → One or More**

- Matches **one or more** occurences of the previous character.

```js
app.get("/ab+cd", (req, res) => {
  res.send("Matched abcd, abbcd, abbbbbbcd...");
});
```

`/ab+cd` Matches `/abcd`, `/abbcd`, `/abbbbbbcd` etc.

**4. `*`(_Asterisk_) → Wildcard (Anything Matches)**
ff

- Matches **anything in the place of `*`**.

```js
app.get("/ab*cd", (req, res) => {
  res.send("Matched abANYTHINGcd");
});
```

`/ab*cd` Matches `/abcd`, `/abXcd`, `/abXYfaaewfeqwfZcd`, , `/ab124561cd` etc.

**5. `()` → Grouping for Optional Segments**

- Groups part of the **route** together.
- It often works with `?`, `+`, or `*` to make the whole group optional or repeatable

```js
app.get("/ab(cd)?e", (req, res) => {
  res.send("Matched abe or abcde");
});
```

`/ab(cd)?e` Matches `/abe` and `/abcde`.

**6. `&` (_Ampersand_) → Query Parameters**

- Not part of the **route**, but used in the **URL** to pass extra data.

```url
http://localhost:3000/search?name=arshit&age=23
```

In Express, you get it like:

```js
app.get("/search", (req, res) => {
  const name = req.query.name;
  const age = req.query.age;
  res.send(`Name: ${name}, Age: ${age}`);
});
```

`&` separates multiple **query parameters**.

### **Quick Example: Complex Route**

```js
app.get("/product/:category/:id?", (req, res) => {
  const category = req.params.category;
  const id = req.params.id;
  res.send(`Category: ${category}, ID: ${id || "None"}`);
});
```

- `/product/electronics/101` → `Category: electronics, ID: 101`
- `/product/electronics` → `Category: electronics, ID: None`

[Go to top ↑](#index)

### **Route paths based on regular expressions**

**Example 1**:

```javascript
app.get(/a/, (req, res) => {
  res.send("/a/");
});
```

**This route path will match any URL that contains an "a".**

- It can be **anywhere** in the URL, like `/apple`, `/banana`, `/car`.
- As long as the URL includes the letter **a**, this route will match.

**Example 2**:

```javascript
app.get(/.*fly$/, (req, res) => {
  res.send("/.*fly$/");
});
```

**This route path will match any URL that ends with "fly".**

- It matches **/butterfly**, **/dragonfly**.
- It **does not** match **/butterflyman** or **/dragonflyman** because they **don’t end exactly with "fly"**.
- The `.*` means **anything can come before "fly"**, but `$` means it **must end** right there.

## **6. How to read dynamic routes and query parameters?**

### **Dynamic Routes**

- Dynamic routes use **parameters** in the URL path.
- Syntax: `:`(_Colon_) followed by a **parameter name**.

**Example**:

```javascript
app.get("/users/:userId", (req, res) => {
  res.send(req.params.userId);
});
```

- `:userId` is a **dynamic parameter**.
- If someone visits `/users/5`, then `req.params.userId` will be `5`.
- You can access **dynamic values** from `req.params`, it will return an object.

### **Multiple Dynamic Params**

```javascript
app.get("/users/:userId/books/:bookId", (req, res) => {
  res.send(req.params);
});
```

- This route matches `/users/5/books/20`.
- `req.params.userId` is `5`.
- `req.params.bookId` is `20`.

### **Query Parameters**

- Query params are **key-value pairs** added after a `?` in the URL.

**Example:**

```javascript
app.get("/search", (req, res) => {
  res.send(req.query);
});
```

- If someone visits `/search?name=John&age=25`
- `req.query.name` is `John`
- `req.query.age` is `25`
- Query parameters come after `?` and are separated by `&`.
- You can access **query parameters** from `req.query`, it will return an object.

### **Combining Both**

```javascript
app.get("/users/:userId", (req, res) => {
  const userId = req.params.userId;
  const sort = req.query.sort;
  res.send(`User ID: ${userId}, Sort: ${sort}`);
});
```

**Example Request**:  
`/users/10?sort=asc`

- `userId` is `10`
- `sort` is `asc`

[Go to top ↑](#index)

## **7. Does Order Matter in Route Handling in Express.js?**

**Yes**, the **order matters** in Express.js route handling! ✅

- Express checks routes **from top to bottom**, and **runs the first matching route it finds**.
- If a **more general route** (like `/`) is defined **before** specific routes (like `/about`), it will **catch everything first**, and other routes **won’t get a chance to run**.

### **Why Does Order Matter?**

- Express processes routes **in the order** they are defined.

- If you put a **general route first**, it will **match all paths**, even ones you don’t want it to.  
  _(For example: `app.use("/")` matches everything, so if it’s placed first, it will catch `/about`, `/contact`, or any other route.)_

- More **specific routes** should be defined **before** general ones.  
  _(For example: write `app.use("/about")` before `app.use("/")`)_.  
  Otherwise, the general route will **block** them!  
  _(Because Express finds `/` first, it doesn’t check the routes written below it.)_

### **Example**

```javascript
import express from "express";

const app = express();

// General route first (this is a problem!)
app.use("/", (req, res) => {
  res.send("Hello this is homepage");
});

app.use("/about", (req, res) => {
  res.send("Hello this is about page");
});

app.use("/contact", (req, res) => {
  res.send("Hello this is contact page");
});

app.listen(3000, () => {
  console.log("Server started at port 3000");
});
```

1. The route `app.use("/")` **matches everything** starting from `/`.
2. So when you visit `/about` or `/contact`, Express **stops** at `/` route and returns "Hello this is homepage".
3. `/about` and `/contact` **never get executed**.

### **Correct Order: Specific Routes First**

```javascript
import express from "express";

const app = express();

// More specific routes first!
app.use("/about", (req, res) => {
  res.send("Hello this is about page");
});

app.use("/contact", (req, res) => {
  res.send("Hello this is contact page");
});

// General route after the specific ones!
app.use("/", (req, res) => {
  res.send("Hello this is homepage");
});

app.listen(3000, () => {
  console.log("Server started at port 3000");
});
```

1. Visiting `/about` will show: `"Hello this is about page"`
2. Visiting `/contact` will show: `"Hello this is contact page"`
3. Visiting `/` will show: `"Hello this is homepage"`

### **In short**

- Start with routes that are **exact** and **clear**, like `/about` or `/contact`. Put routes that catch everything, like `/` or `\*`, at the end.
- Express **runs from top to bottom** and stops at the **first match**.

[Go to top ↑](#index)

## **8. Difference Between `app.use()` and Other HTTP Methods (`app.get()`, `app.post()`, etc.)?**

### `app.use()`

- Runs for **any type** of HTTP request (`GET`, `POST`, etc.).
- Commonly used for **middleware** like authentication, logging, or parsing data.

- Example:
  ```javascript
  app.use("/api", (req, res, next) => {
    console.log("API route hit");
    next(); // Move to the next handler
  });
  ```

### **Other HTTP Methods (`app.get()`, `app.post()`, etc.)**

- Runs for **specific** HTTP requests.
- Example:

  ```javascript
  app.get("/about", (req, res) => {
    res.send("About Page");
  });

  app.post("/contact", (req, res) => {
    res.send("Contact form submitted");
  });
  ```

### **When to Use What?**

| **Use `app.use()`**                         | **Use `app.get()`, `app.post()`**                                              |
| ------------------------------------------- | ------------------------------------------------------------------------------ |
| For middleware: logger, auth, parsers.      | For building routes that respond to requests.                                  |
| If you need to handle **all** HTTP methods. | If you only want to handle a **specific** request (like only `GET` or `POST`). |

[Go to top ↑](#index)

## **9. What is `next()` in Express.js?**

`next()` is a **function** that you call to **pass control** to the **next middleware** or **route handler** in the stack.

### **Why Do We Use `next()`?**

- It tells Express:
  - "I'm done with this part. Move to the next function!"
- Without calling `next()`, the **next handler won't run**, and the request will be in an **infinite loop** (no response).

### **How It Works:**

- Express runs your middleware and route handlers **in order** (top to bottom).
- If you use `next()`, Express moves to the **next matching** function.
- If you **don't** use `next()`, the request **stops there** unless you send a response (`res.send()`, `res.json()`).

### **Simple Example:**

```javascript
import express from "express";
const app = express();

// First middleware (NO RESPONSE)
app.use((req, res, next) => {
  console.log("Step 1");
  next(); // Move to the next middleware/route
});

// Second middleware (NO RESPONSE)
app.use((req, res, next) => {
  console.log("Step 2");
  next(); // Move to the next middleware/route
});

// Final route handler(HAS RESPONSE)
app.get("/", (req, res) => {
  console.log("Step 3");
  res.send("Hello from the homepage");
});

app.listen(3000, () => {
  console.log("Server running on 3000");
});
```

### **What if You Don’t Call `next()`?**

```javascript
app.use((req, res, next) => {
  console.log("Step 1");
});
```

- Express stops there, because there is no response returning and it will be in the infinite loop until the server timeouts.
- You **must** call `next()` if you **don't** send a response.

### **When to Use `next()`?**

| **Use `next()` when...**                                                        |
| ------------------------------------------------------------------------------- |
| You are writing **middleware** that should **pass control** to another handler. |
| You **don't** want to **end** the request-response cycle yet.                   |
| You are **checking/authenticating** but want to continue to the next route.     |

[Go to top ↑](#index)

## **10. Can We Use Multiple Route Handlers in One Route?**

Yes! You **can** use **multiple route handlers** in one route in Express.js. It's also called **middlewares**.

- They run **one after the other**, **in order**, if you call `next()` properly.
- But… it's **not always recommended**, because if you don’t handle things carefully—like with `next()`—you can run into **bugs** and **unexpected behavior**.

There are **two ways** to use multiple handlers:

1. **Pass them as separate arguments**

   ```javascript
   app.get("/example", handler1, handler2, handler3);
   ```

2. **Pass an array of handlers**

   ```javascript
   app.get("/example", [handler1, handler2, handler3]);
   ```

_They have **No functional difference**!, They both work the same way, it's just about **code style** and **readability**_

**Example (working fine)**:

```javascript
import express from "express";
const app = express();

app.get(
  "/",
  (req, res, next) => {
    console.log("First handler");
    next(); // Pass control to the next handler
  },
  (req, res, next) => {
    console.log("Second handler");
    res.send("Hello from second handler");
  }
);

app.listen(3000, () => {
  console.log("Server running on 3000");
});
```

**Output**:

```
First handler
Second handler
```

### **Common Errors & Issues With this approach**

### 1. **Missing `next()`**

```javascript
app.get(
  "/about",
  (req, res, next) => {
    console.log("First handler");
    // Forgot next(), second handler will NEVER run
    // No response sent! The request will hang forever.
  },
  (req, res) => {
    console.log("Second handler");
    res.send("About Page");
  }
);
```

**Problem**:

- You never called `next()`.
- The second handler will never run.
- Client **waits forever** (request hangs).

### 2. **Calling `next()` after `res.send()`**

```javascript
app.get(
  "/contact",
  (req, res, next) => {
    res.send("Contact Page");
    next(); // ❌ BAD! You already sent the response.
  },
  (req, res) => {
    res.send("Second contact handler"); // ❌ CRASH! Error: Cannot set headers after they are sent
  }
);
```

**Problem**:

- You called `res.send()` first, then `next()`.
- Express goes to the next handler (_cuz you used `next()`_), which tries to send **another** response.
- Leads to this error:

```
Error: Can't set headers after they are sent.
```

### **Note**

- Always use such handlers in separate functions, which are called **middlewares.**

[Go to top ↑](#index)

## **11. What are Middlewares in Express.js?**

**Middleware** in Express.js is a **function** that runs **between** the **request** and the **response**.  
It has access to the **request** (req), **response** (res), and a **next()** function.

Middleware functions can perform the following tasks:

- Execute any code.
- Make changes to the request and the response objects.
- End the request-response cycle.
- Call the next middleware function in the stack.

### **Why Do We Need Middleware?**

Middleware helps in **reusing logic** for:

- Authentication
- Logging
- Validation
- Error handling
- Any repeated tasks

⚠️ Without middleware, you'd have to **repeat the same code** in every route.  
This makes your code **messy**, **hard to read**, and **difficult to maintain**.

### **Example**

```javascript
import express from "express";
const app = express();
// Middleware
app.use("/admin", (req, res, next) => {
  const token = "arsh!t";
  const isAuthourized = token === "arsh!t";
  if (!isAuthourized) {
    res.status(401).send("Unauthorized Request");
  } else {
    next();
  }
});

//  All  Routes
app.get("/admin/getAllData", (req, res) => {
  res.send("This is all the data");
});
app.get("/about/deleteUser", (req, res) => {
  res.send("Deleted A user");
});
app.listen(3000, () => {
  console.log("Server started at port 3000");
});
```

This middleware checks if a user is **authorized** before they can access any `/admin` routes.  
You only write the logic **once** in `app.use("/admin", ...)`, and it automatically works for:

- `/admin/getAllData`
- `/admin/deleteUser`
- Any future `/admin` route you add!

### **Example (Without Middleware)**

If there was **no middleware**, you'd have to **copy-paste** the authorization logic in **every route handler** like this:

```javascript
app.get("/admin/getAllData", (req, res) => {
  const token = "arsh!t";
  const isAuthourized = token === "arsh!t";

  if (!isAuthourized) {
    res.status(401).send("Unauthorized Request");
    return;
  }

  res.send("This is all the data");
});

app.get("/admin/deleteUser", (req, res) => {
  const token = "arsh!t";
  const isAuthourized = token === "arsh!t";

  if (!isAuthourized) {
    res.status(401).send("Unauthorized Request");
    return;
  }

  res.send("Deleted A user");
});
```

This makes your code:

- Repetitive
- Hard to maintain (if the logic changes, you have to update **every route**)
- Error-prone (you might forget to add it in one of your route)

### **Common Built-in Middleware in Express**

- **express.json()** – Parses JSON data from incoming requests.
- **express.urlencoded()** – Parses URL-encoded data (like form submissions).
- **express.static()** – Serves static files (like CSS, JS, images).

[Go to top ↑](#index)

## **12. What is Error Handling in Express?**

**Error handling** in Express means catching and responding to errors that happen during request processing in your server app, like:

- Server issues
- Database connection failures
- Code bugs
- Resources not found (404)

### **Why Do We Need Error Handling?**

1. **Prevent server crashes**: Errors can shut down your server if not handled properly.
2. **User-friendly messages**: Instead of showing ugly system errors (_which may reveal personal information along wiht the error message_), you can send clean responses like "Something went wrong!"
3. **Debugging**: Log errors for developers to fix issues later.
4. **Security**: Don't leak sensitive data (like stack traces) to users.

### **Types of Error Handling in Express**

1. **Error Handling inside Individual Routes (Try-Catch)**

You handle specific errors within a route, especially useful for async code.

**Example**:

```javascript
app.get("/user/:id", async (req, res) => {
  try {
    const user = await findUserById(req.params.id);
    if (!user) {
      return res.status(404).json({ message: "User not found" });
    }
    res.json(user);
  } catch (error) {
    console.error(error);
    res.status(500).json({ message: "Server error!" });
  }
});
```

- You have more **control** over the specific route logic.
- Customize response for specific scenarios (e.g., "User not found").

2. **Error Handling Middleware (Global Error Handler)**

There may be a scenario that you forgot to write the try-catch so,
You catch **all unhandled errors** in one place instead of writing try-catch in every route.

**Example:**

```javascript
// Error handling middleware function
app.use("/", (err, req, res, next) => {
  // Order matter (err, req, res, next)
  console.error("Error middleware:", err.stack);
  //here you can log your errors for later debugging
  res.status(err.status || 500).json({
    message: err.message || "Something went wrong!",
  });
});

// Route that triggers an error
app.get("/error-test", (req, res, next) => {
  const error = new Error("This is a test error!");
  error.status = 400;
  next();
});
```

- Handles **unforeseen errors** you forgot to catch in routes.
- Makes the code **DRY** (Don’t Repeat Yourself).
- Centralized error logging and response formatting.

[Go to top ↑](#index)

---

# 5. **Database and Database Management System(DBMS)**

## **1. Introduction**

- ### For intro to Databases go to [This Page](../Database/Intro_to_databases.md)

## **2. Databases**

- ### For MongoDB go to [This Page](../Database/mongo-db.md)

---

# 6. **Authentications and Authorization**

## **1. What is Authentication? Why Do We Need It? Explain the working also.**

### **What is Authentication?**

**Authentication** is the process of verifying the identity of a user, system, or application before granting access to resources. It ensures that the entity trying to access a system is who they claim to be.

### **Why Do We Need Authentication?**

1. **Security** 🔒 – Prevents unauthorized access to sensitive data.
2. **User Privacy** 🛡 – Ensures personal information stays confidential.
3. **Access Control** 🚪 – Allows different users to access only permitted resources.
4. **Prevents Identity Theft** 🛑 – Stops malicious actors from impersonating users.
5. **Protects APIs & Services** ⚡ – Ensures only legitimate requests are processed.

### **Types of Authentication Methods**

🔹 **Password-based Authentication** – Users provide a username & password.  
🔹 **Token-based Authentication (JWT, OAuth)** – Secure tokens grant access.  
🔹 **Biometric Authentication** – Fingerprint, facial recognition, etc.  
🔹 **Multi-Factor Authentication (MFA)** – Combines multiple methods for extra security.

### **How Does Authentication Work?**

1. **User Logs In** 🔑

   - The user provides a valid email and password.
   - The server verifies the credentials against the database.
   - If correct, the server generates a **token** (JWT or session token).
   - The token is sent to the user and stored in a **cookie** or **localStorage**.

2. **User Makes Requests** 🌍

   - The client (browser or mobile app) sends API requests.
   - The **token is attached** to each request (usually in headers or cookies).
   - Example: `Authorization: Bearer <token>` in headers.

3. **Server Validates the Token** ✅

   - The server checks if the token is valid.
   - If valid, the request is processed.
   - If **invalid or expired**, the request is rejected.

4. **User Remains Logged In** 🔄

   - Until the token expires, the user can continue making requests.
   - If the token expires, the user must **log in again** to get a new token.

5. **When user Logs Out** 🚪
   - The token is deleted from storage (cookies/localStorage).
   - The user must re-authenticate to access protected routes again.

### **Authentication Flow Diagram**

```
User ➡ Login Request ➡ Server Verifies ➡ Generates Token ➡ Returns Token to User
User ➡ Makes Request (with Token) ➡ Server Validates Token ➡ Grants Access (or Denies)
```

[Go to top ↑](#index)

## **2. What is Authorization and Difference between Authentication and Authorization**

**Authorization** is the process of granting or restricting access to resources or actions based on a user's **permissions**. It determines **what a user is allowed to do** after authentication.

**Example:**

- A user logs in (authentication), but only an **admin** can delete users (authorization).
- In an API, `admin` can access `/delete-user`, but `guest` cannot.

- **Common Methods:** Role-based access control (RBAC), OAuth, JWT tokens, API keys.

### **Authentication vs. Authorization**

| Feature               | Authentication 🆔                           | Authorization 🔑                                      |
| --------------------- | ------------------------------------------- | ----------------------------------------------------- |
| **Definition**        | Verifies **who** the user is.               | Determines **what** the user can do.                  |
| **Process**           | Checks credentials (email, password, etc.). | Checks permissions for accessing resources.           |
| **Example**           | Logging into an account.                    | Accessing admin-only pages.                           |
| **How it Works**      | Uses passwords, OTPs, or biometric data.    | Uses roles, policies, or access control lists (ACLs). |
| **When?**             | First step in security.                     | Happens after authentication.                         |
| **Implemented Using** | JWT, OAuth, Sessions.                       | Role-based access control (RBAC), API keys.           |

🔹 **Authentication** = "Are you a valid user?"  
🔹 **Authorization** = "What are you allowed to do?"

[Go to top ↑](#index)

## **3. Implementing Authentication in Express.js Using Cookies(_Hardcode tokens_)**

### **What is a Cookie?**

A **cookie** is a small piece of data stored in the user's browser. It helps in maintaining user sessions by saving authentication tokens or other information.

- **Purpose of Cookies**:
  - Maintain user sessions
  - Store authentication tokens
  - Track user preferences

### **Implementing Authentication in Express.js Using Cookies**

**Example Code:**

```javascript
const express = require("express");
const bcrypt = require("bcrypt");
const mongoose = require("mongoose");
const cookieParser = require("cookie-parser");

const app = express();
app.use(express.json()); // Middleware to parse JSON request body
app.use(cookieParser()); // Middleware to parse cookies

// LOGIN Route
app.post("/login", async (req, res) => {
  try {
    const { email, password } = req.body;
    const user = await User.findOne({ email: email });

    if (!user) {
      throw new Error("Invalid Credentials");
    }

    const isPassValid = await bcrypt.compare(password, user.password);

    if (isPassValid) {
      res.cookie("token", "b34h38hfdu3dn39dj"); // Hardcoded token for practice
      res.send("Login Successful");
    } else {
      throw new Error("Invalid Credentials");
    }
  } catch (error) {
    res.status(400).send("ERROR: " + error.message);
  }
});

// PROFILE Route (Protected Route)
app.get("/profile", (req, res) => {
  console.log(req.cookies); // Debugging: Check if cookies are being received

  const { token } = req.cookies;

  if (token) {
    res.send("Profile fetched successfully");
  } else {
    res.status(400).send("Access denied. Please log in.");
  }
});

// Start Server
app.listen(5000, () => {
  console.log("Server running on port 5000");
});
```

### **How Authentication Works in This Code**

1. **User Login (`/login` route)**

   - The user provides an `email` and `password`.
   - The server checks if the `email` exists in the database.
   - The `password` is verified using `bcrypt.compare()`.
   - If correct, a **token** is set in a cookie (`res.cookie("token", "b34h38hfdu3dn39dj")`).
     - _i'm using a hardcoded token for practice_
   - The user receives a "Login Successful" response and the `token` which is attached to cookies in the browser.

2. **Accessing Profile (`/profile` route)**
   - The client sends a request to `/profile`, including the cookies(_which has the token_))
   - The server checks for the request and the `token` inside `req.cookies`.
   - If the token exists and valid then the server will send the response.
   - If the token is missing it will denied the request.

### **Why Does `req.cookies` Print `Undefined`? How to Fix It?**

When accessing or try to print the `req.cookies` in an Express.js application, it might return **undefined** because Express does not parse cookies by default. This happens when the **`cookie-parser`** middleware is missing.

**What is `cookie-parser`?**

- **`cookie-parser`** is an Express.js middleware that parses cookies from incoming HTTP requests and makes them accessible and readable via `req.cookies`.

- A **parser** is a tool that reads, interprets, and converts data into a usable format. Here, `cookie-parser` reads the raw `Cookie` header from HTTP requests and transforms it into a JavaScript object, making it easy to access individual cookies.

**How to use `cookie-parser`**

- **Install `cookie-parser` (if not installed):**

  ```sh
  npm install cookie-parser
  ```

- **Import and Use `cookie-parser` in Express App:**

```js
const express = require("express");
const cookieParser = require("cookie-parser");

const app = express();
app.use(cookieParser()); // ✅ Enables cookie parsing

app.get("/profile", (req, res) => {
  console.log(req.cookies); // Now this will work
  res.send("Profile Page");
});

app.listen(3000, () => console.log("Server running on port 3000"));
```

**Note:**

- Ensure `app.use(cookieParser());` is added **before** using `req.cookies`.

[Go to top ↑](#index)

## **4. Implementing Authentication in Express.js Using JWT and Cookies**

### **What is JWT (JSON Web Token)?**

JWT is a compact, self-contained token (_means that the token carries all the necessary information within itself and does not require external dependencies (like a database lookup) to verify its validity._) that securely transmits information between parties as a **JSON object**. It is often used for authentication and authorization.

A **JWT (JSON Web Token)** consists of three parts, separated by a dot (`.`):

1. **Header** (_Defines token metadata like alogorithm used, etc_)

   - Specifies the **algorithm** (e.g., `HS256`) and **token type** (`JWT`).
   - 📌 **Example**:
     ```json
     {
       "alg": "HS256",
       "typ": "JWT"
     }
     ```

2. **Payload** (_Holds user data and claims_)

   - Contains **user info** (e.g., `id`, `email`, `role`).
   - **Example**:
     ```json
     {
       "id": "64d8f9b2e",
       "email": "user@example.com",
       "role": "admin"
     }
     ```

3. **Signature** 🔑 (_Ensures token integrity_)

   - The **signature** in a JWT is created to ensure that the token has not been altered. It works by hashing the **header** + **payload** using a secret key and a cryptographic algorithm (like `HS256`).
   - **Example JWT**:

   ```bash
   eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.
   eyJpZCI6IjY0ZDhmOWIyZSIsImVtYWlsIjoidXNlckBleGFtcGxlLmNvbSIsInJvbGUiOiJhZG1pbiJ9.
   HhJv9Np3Z5F-kh7E5XJ...
   ```

- Each part is **Base64-encoded** and separated by a **dot (`.`)**.

  - **Example:**

    ```
    xxxxx.yyyyy.zzzzz
    ```

### **Steps to Implement JWT Authentication with Cookies**

**1. Install Required Packages**

```sh
npm install express jsonwebtoken cookie-parser
```

**2. Setup Express & Middleware**

```javascript
const express = require("express");
const jwt = require("jsonwebtoken");
const cookieParser = require("cookie-parser");
const User = require("./models/User"); // Assuming you have a User model

const app = express();
app.use(express.json()); // Parse JSON bodies
app.use(cookieParser()); // Parse cookies
```

**3. Implementing Login Route**

```javascript
app.post("/login", async (req, res) => {
  try {
    const { email, password } = req.body;

    // Validate User
    const user = await User.findOne({ email });
    if (!user || user.password !== password) {
      throw new Error("Invalid Credentials");
    }

    // Generate JWT Token
    const token = jwt.sign({ id: user._id }, "arshit@123", { expiresIn: "1h" });

    // Store Token in Cookies
    res.cookie("token", token, { httpOnly: true, secure: true });

    res.send("Login Successful");
  } catch (error) {
    res.status(400).send("ERROR: " + error.message);
  }
});
```

**Syntax:**

```javascript
jwt.sign(payload, secretKey, options);
```

- It creates a **JWT** by encoding a payload and signing it with a **secret key** to prevent tampering.
  - `payload`: Data to encode (e.g., `{ id: user._id }`)
  - `secretKey`: Used to sign and verify the token (e.g., `"arshit@123"`)
  - `options`: Additional configurations like `{ expiresIn: "1h" }`

**4. Implementing Profile Route (Token Verification)**

```javascript
app.get("/profile", async (req, res) => {
  try {
    const { token } = req.cookies;

    if (!token) throw new Error("Invalid Token");

    // Verify Token
    const decoded = jwt.verify(token, "arshit@123");

    // Find User by ID from Token Payload
    const user = await User.findOne({ _id: decoded.id });

    res.json(user);
  } catch (error) {
    res.status(400).send("ERROR: " + error.message);
  }
});
```

**Syntax:**

```javascript
jwt.verify(token, secretKey);
```

- Decodes and **validates** a JWT using the secret key to check authenticity and expiration.

  - `token`: The JWT token received from cookies
  - `secretKey`: The same key used for signing the token

**In short**

- **JWT** is used for secure authentication by embedding user data.
- **Cookies** store the JWT token to maintain session authentication.
- **`jwt.sign()`** creates the token, and **`jwt.verify()`** validates it.

[Go to top ↑](#index)
