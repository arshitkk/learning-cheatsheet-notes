# React JS Cheatsheet

## **Index**

0. ### [Level 0 (Starting fundamentals)](#level-0-starting-fundamentals-1)

   1. **[What is Emmet?](#1-what-is-emmet)**
   2. **[Difference between a Library and a Framework?](#2-difference-between-a-library-and-a-framework)**
   3. **[What is a CDN? Why do we use it?](#3-what-is-a-cdn-why-do-we-use-it)**
   4. **[Why is React known as React?](#4-why-is-react-known-as-react)**
   5. **[What is `crossorigin` in the `<script>` tag?](#5-what-is-crossorigin-in-the-script-tag)**
   6. **[What is the difference between React and ReactDOM?](#6-what-is-the-difference-between-react-and-reactdom)**

1. ### [Level 1 (NPM & Vite)](#level-1-npm--vite-1)

   1. **[What is NPM?](#1-what-is-npm)**
   2. **[What is a Bundler? Types](#2-what-is-a-bundler-types)**
   3. **[What is Vite, and why do we need](#3-what-is-vite-and-why-do-we-need-it)**
   4. **[What is `.vite` (Vite's cache folde](#4-what-is-vite-vites-cache-folder)**
   5. **[What is `npx`?](#5-what-is-npx)**
   6. **[Difference Between `dependencies` and `devDependencies](#6-difference-between-dependencies-and-devdependencies)**
   7. **[What is Tree Shaking in Vite](#7-what-is-tree-shaking-in-vite)**
   8. **[What is Hot Module Replacement (HMR) in Vite](#8-what-is-hot-module-replacement-hmr-in-vite)**
   9. **[List 5 main features of `Vite](#9-list-5-main-features-of-vite)**
   10. **[What is `.gitignore`? What should we add and not add into it?](#10-what-is-gitignore-what-should-we-add-and-not-add-into-it)**
   11. **[Difference Between package.json and package-lock.json](#11-difference-between-packagejson-and-package-lockjson)**
   12. **[What is node_module and dist folder](#12-what-is-node_module-and-dist-folder)**

2. ### **[Level 2 (React JS - Beginner)](#level-2-react-js---beginner-1)**

   1. [What is JSX? How it works](#1-what-is-jsx-how-it-works)
   2. [What is `React.createElement()`?](#2-what-is-reactcreateelement)
   3. [Define Babel?](#3-define-babel)
   4. [What are React Components? Functional vs Class Components](#4-what-are-react-components-functional-vs-class-components)
   5. [What is the Virtual DOM?](#5-what-is-the-virtual-dom)
   6. [What is the Diffing Algorithm in React?](#6-what-is-the-diffing-algorithm-in-react)
   7. [What are Keys in React?](#7-what-are-keys-in-react)
   8. [What is Reconciliation in React?](#8-what-is-reconciliation-in-react)
   9. [What is React Fiber?](#9-what-is-react-fiber)
   10. [What are Props in React?](#10-what-are-props-in-react)
   11. [What is State in React? Difference between state & props](#11-what-is-state-in-react-difference-between-state--props)
   12. [What is a Composite Component in React?](#12-what-is-a-composite-component-in-react)
   13. [Named Export vs Default Export vs \* as Export](#13-named-export-vs-default-export-vs--as-export)
   14. [React Hooks & Their Types (with Examples)](#14-react-hooks--their-types-with-examples)

## **Level 0 (Starting fundamentals)**

### **1. What is Emmet?**

Emmet is a plugin for code editors that **helps write HTML and CSS faster** using short abbreviations. It expands short codes into full HTML structures automatically.

🔹 **Example:**  
Typing → `ul>li*3`  
Expands to →

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

[Go to top ↑](#index)

### **2. Difference between a Library and a Framework?**

Here’s an **enhanced version** of your table with **better readability, proper explanations, and reasons** for each statement:

---

| **Framework**                                                                                                                | **Library**                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| A framework consists of many components like APIs, compilers, support programs, and built-in libraries.                      | A library is a collection of reusable modules, classes, functions, and pre-written code that helps in development.                 |
| The framework **controls the flow of the application** and decides when and how your code will run.                          | You **call** the library functions when needed, giving you more control over the code structure.                                   |
| Frameworks are difficult to replace because they define the architecture of the entire application.                          | Libraries are easier to replace because they provide specific functionalities without enforcing a structure.                       |
| Developing with a framework requires **more code**, which can **increase load time** and affect performance.                 | Libraries are lightweight and require **less code**, leading to better performance and faster load times.                          |
| Integrating a framework into an existing project is **challenging** because it requires following its specific architecture. | Libraries can be **easily integrated** into existing projects, allowing developers to add specific features without major changes. |
| **Examples:** AngularJS, Spring, Node.js, Django.                                                                            | **Examples:** jQuery, React.js, Lodash.                                                                                            |

#### **Example** 🎭

✅ **Library → A Restaurant Menu** 🍽️

- You **choose what to eat** from the menu (library functions).
- The chef (library) prepares only what you order.
- You have **full control** over your choices.

✅ **Framework → A Buffet System** 🍕🍣

- The buffet (framework) decides the food options.
- You **follow its structure**—you can only take what's available.
- The system controls the flow, and you work within its rules.

[Go to top ↑](#index)

---

### **3. What is a CDN? Why do we use it?**

- **CDN (Content Delivery Network)** is a distributed network of servers that work together to deliver content (like images, videos, CSS and static files) to users faster and more efficiently

- CDNs are used to improve website speed, reliability, and security by reducing the distance between the user and the server.

#### **Example:**

```html
<script src="https://cdn.jsdelivr.net/npm/react@18/umd/react.production.min.js"></script>
<!-- This loads React **directly from a CDN** instead of downloading it manually. -->
```

#### **Without CDN**

When a user requests content from a website without a CDN, the request is sent directly to the origin server where the website is hosted. The origin server processes the request and sends back the requested content to the user's device.

- If the origin server is located far away from the user, it may result in longer loading times due to increased latency.
- High traffic volumes or server overload can lead to slower response times and even server downtime, which will negatively impact the user experience.

[Go to top ↑](#index)

### **4. Why is React known as React?**

React is called **React** because it **reacts** to changes in data efficiently.

🔹 It uses a **virtual DOM** to detect changes and update only those component which are needed to update, making apps fast and responsive.

[Go to top ↑](#index)

### **5. What is `crossorigin` in the `<script>` tag?**

The `crossorigin` attribute in `<script>` allows loading scripts from **other domains** while handling **CORS (Cross-Origin Resource Sharing)**.

When loading a script from a different origin (another website or CDN), the browser may block access to certain data due to** CORS (Cross-Origin Resource Sharing)** policies.

#### **Values:**

- `anonymous` → Default, no credentials sent (cookies, authentication). When loading public scripts from a CDN (React, Bootstrap, etc.) without sending user credentials (cookies, tokens).
- `use-credentials` → Sends credentials (cookies, authentication) with the request. When loading private scripts that need authentication (e.g., APIs that require login, restricted resources).

#### **Example:**

```html
<script src="https://example.com/script.js" crossorigin="anonymous"></script>
```

[Go to top ↑](#index)

### **6. What is the difference between React and ReactDOM?**

- **React.js** is an open-source JavaScript library developed by Facebook for building **user interfaces** (UI), specifically single-page applications (SPAs).

  | **React** 🧠 (Brain)                                   | **ReactDOM** 🏗️ (Builder)                                     |
  | ------------------------------------------------------ | ------------------------------------------------------------- |
  | The core JS library for building UI components.        | A **library** that helps render UI components to the browser. |
  | Manages **UI logic** and component structure.          | Connects **React components** to the **real DOM**.            |
  | Core React features like **components, state, hooks**. | Functions for rendering (e.g., `ReactDOM.createRoot()`).      |
  | Used to **define** UI components.                      | Used to **render** those UI components on the page.           |
  | Inside React components (`.jsx` or `.tsx` files).      | Inside the main/starting point `index.js` or `main.jsx` file. |
  | You can **define** components but can't render them.   | You can't display components in the browser.                  |

- `React` = Makes components.
- `ReactDOM` = Puts components into the webpage.

[Go to top ↑](#index)

---

## **Level 1 (NPM & Vite)**

### **1. What is NPM?**

**NPM** is a tool to **manage packages** (reusable code, libraries, frameworks, tools) for JavaScript projects. It helps you to install, update, and manage libraries and dependencies in your projects.

- **Example**:  
   When you want to use a library like React, you use NPM to install it.

[Go to top ↑](#index)

### **2. What is a Bundler? Types**

A **Bundler** is a tool that takes multiple files (JavaScript, CSS, HTML) and combines them into a single file (or a few files), making it easier and faster for the browser to load. It helps optimize the project by minimizing file size.

- **Types**:
  - **Webpack**: A powerful bundler used in many large projects.
  - **Parcel**: An easy-to-use bundler with automatic configuration.
  - **Rollup**: Good for libraries and optimizing code for production.

[Go to top ↑](#index)

### **3. What is Vite, and why do we need it?**

**Vite** is a modern build tool and bundler that focuses on spe**ed and **performance\*\*. It uses native ES modules to speed up the development environment and optimizes for production with fast build times. This means that Vite only transforms the files that change, rather than rebuilding everything every time you make a change. This reduces the wait time and makes the development process almost instant.

**Why do we need it?**

- **Faster Development**: Vite uses native ES modules to speed up the development environment.
- **Hot Module Replacement (HMR)**: Instant updates to the page without refreshing, improving the developer experience.
- **Optimized for Modern Frameworks**: Built with React, Vue, and other modern JavaScript frameworks in mind.

[Go to top ↑](#index)

### **4. What is `.vite` (Vite's cache folder)?**

The `.vite` folder is where Vite stores temporary files to make the development process faster. When you're working on your project, Vite processes things like JavaScript, CSS, and images, and saves the results in this folder. This way, it doesn't have to process the same files every time you make a change, which helps speed up development.

**Why do we need it?**

- Stores compiled code, cache data, and other temporary files.
- Helps reduce build time by reusing files instead of re-compiling everything.
- You can delete the .vite folder if it becomes too large or causes issues, as it will be recreated on the next build.

[Go to top ↑](#index)

### **5. What is `npx`?**

`npx` is a command-line tool that comes with **npm** (since version 5.2.0). It allows you to **run Node.js packages without installing them globally or locally**. This is useful for running one-off commands or for trying out packages without needing to install them permanently.

**Difference Between `npx` and `npm`:**

| **`npx`**                                                                            | **`npm`**                                                         |
| ------------------------------------------------------------------------------------ | ----------------------------------------------------------------- |
| **Run a package without installing it permanently.**                                 | **Install a package permanently** (either locally or globally).   |
| Instantly executes a package from npm registry, without saving it to `node_modules`. | Downloads the package and saves it in `node_modules` or globally. |
| Ideal for running one-off commands.                                                  | Ideal for managing and installing dependencies in your project.   |
| Does not require a `package.json` to work.                                           | Requires `package.json` to manage dependencies in your project.   |

**Example: Using `cowsay`**

#### 1. **Using `npm` to install and run Cowsay:**

First, you need to install the `cowsay` package locally in your project:

```bash
npm install cowsay
```

After installing it, you can use it:

- in node:

  ```javascript
  const cowsay = require("cowsay");

  console.log(cowsay.say({ text: "Hello from npm!" }));
  ```

- or in CMD:

  ```bash
  cowsay Hello from npm!
  ```

But, if you just wanted to try it out without installing it, you have to use `npx`

#### 2. **Using `npx` to run Cowsay without installing it:**

With `npx`, you can directly run the Cowsay package without installing it:

```bash
npx cowsay "Hello from npx!"
```

This command will **download and run** the package temporarily, showing the output like this:

```
 ________
< Hello from npx! >
 --------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

After executing the command, **it is not saved anywhere** on your system—there’s no need to manage dependencies or install packages.

[Go to top ↑](#index)

### **6. Difference Between `dependencies` and `devDependencies`**

| **Feature**                    | **dependencies**                                     | **devDependencies**                                    |
| ------------------------------ | ---------------------------------------------------- | ------------------------------------------------------ |
| **Definition**                 | Packages required for the app to work in production. | Packages needed only during development.               |
| **Used In**                    | Code that runs in production (live website/app).     | Development tools like testing, linting, and bundling. |
| **Installation Command**       | `npm install package-name`                           | `npm install package-name --save-dev`                  |
| **Location in `package.json`** | Inside `"dependencies"` section                      | Inside `"devDependencies"` section                     |
| **Example Packages**           | `react`, `express`, `axios`                          | `eslint`, `jest`, `vite`, `webpack`                    |
| **Installed on Deployment?**   | ✅ Yes                                               | ❌ No (Not included in production)                     |

Imagine you're **building a car** 🚗:

- **`dependencies`** = **Car Engine, Wheels, Seats** → Needed for the car to run.
- **`devDependencies`** = **Tools like a Wrench, Jack, and Screwdriver** → Needed to build the car but not required when driving.

[Go to top ↑](#index)

### **7. What is Tree Shaking in Vite?**

**Tree shaking** is a process in Vite (and modern bundlers) that removes unused JavaScript code from the final bundle to **reduce file size and improve performance**.  
Vite uses **ES Modules (ESM)**, which supports tree shaking by default.

#### **🛠 How Does It Work?**

- When you import a library or module, **only the used parts** are included in the final build.
- Unused (dead) code is removed during bundling, making the final output smaller and faster.

#### **🌳 Example Without Tree Shaking:**

```js
import { add, subtract, multiply, divide } from "./math";

console.log(add(2, 3)); // Only 'add' is used
```

📌 _Even though we only use `add()`, all functions (`subtract`, `multiply`, `divide`) are included in the final bundle._

#### **✅ Example With Tree Shaking in Vite:**

If `subtract`, `multiply`, and `divide` are **not used**, Vite **removes them** automatically:

```js
import { add } from "./math"; // Only 'add' is included in the final bundle

console.log(add(2, 3));
```

📌 _Now, only `add()` remains in the bundle, making it smaller._

#### **🔹 Why Is Tree Shaking Important?**

- **Reduces bundle size** → Faster page load times 🚀
- **Optimizes performance** → Less unused code in production
- **Improves efficiency** → Only keeps what is necessary

[Go to top ↑](#index)

### **8. What is Hot Module Replacement (HMR) in Vite?**

**Hot Module Replacement (HMR)** in Vite is a feature that allows your web application to update **only the changed modules** in the browser **without refreshing the entire page**.

#### **🔹 How HMR Works in Vite?**

1. **Detects Code Changes** When you update a file (e.g., a React component).
2. **It Updates Only That Module** means Instead of reloading the full page, it updates only the modified part.
3. **It Preserves State** → Since the page doesn’t reload, your app **keeps its current state** (e.g., form inputs, scroll position).

#### **📌 Example: Without HMR vs With HMR**

📌 **Without HMR (Traditional Development)**

- You edit `App.jsx` → The browser **fully reloads** the page.
- Any unsaved form inputs or UI states are **lost**.

📌 **With HMR in Vite**

- You edit `App.jsx` → Only that component **updates instantly**.
- No full reload → **UI state is preserved**.

[Go to top ↑](#index)

### **9. List 5 main features of `Vite`**:

1. **Fast Development Server**: Vite uses **ES modules** for faster file serving, which speeds up the development process significantly.
2. **Hot Module Replacement (HMR)**: Vite updates only the changed module, preserving app state and enhancing the development experience.
3. **Optimized Build with Tree Shaking**: In production, Vite uses **Tree Shaking** to remove unused code and **minimized unused code** to make your build smaller and more efficient.
4. **Framework Agnostic**: Vite supports popular frameworks like **React**, **Vue**, **Svelte**, and more, with zero-config setup.
5. **Pre-Bundling**: Vite uses **esbuild** to pre-bundle dependencies in advance, making it faster than traditional bundlers.

[Go to top ↑](#index)

### **10. What is .gitignore? What should we add and not add into it?**

**`.gitignore`** is a file used in Git to specify which files and directories should **not** be tracked or committed to the repository.

#### What to add:

- **Node_modules**: `node_modules/`
- **Build output**: `dist/`, `build/`
- **Environment files**: `.env`
- **Log files**: `*.log`
- **IDE/Editor files**: `.vscode/`, `.idea/`

#### What not to add:

- **Source code files**: `.js`, `.ts`, `.html`, etc.
- **Configuration files**: `.gitignore`, `.eslintrc`, etc.
- **Documentation**: `.md`, `.txt`

[Go to top ↑](#index)

### **11. Difference Between `package.json` and `package-lock.json`**

#### **`package.json`**

- It is the main configuration file in a Node project which describes the project metadata, dependencies, scripts and other required configurations.
- Uses version ranges to allow flexibility in updates((`^1.2.0`, `~1.2.3`)).
  - `^1.2.3` → Can install `1.3.0`, `1.4.5`, but **not** `2.0.0` -> minor and patched changes allowed
  - `~1.2.3` → Can install `1.2.4`, `1.2.9`, but **not** `1.3.0` -> only patched changes allowed
- It shows the packages and their versions being used in the project.
- It also categorises packages based on usage like dependencies for production, devDependencies for development environment.

#### **Role of `package.json`:**

1. Project Configuration:

   - `package.json` serves as a manifest file for Node projects, containing metadata about the project and its dependencies.
   - It includes information such as the project name, version, entry point, scripts, and dependencies.

2. Dependency Management:

   - Dependencies are listed in the “dependencies” section, specifying the packages required for the project to run.
   - Developers can use the npm install command to install dependencies listed in the package.json.

#### **`package.json`**

- The package.lock file on the other hand provides the snaoshot of all the dependencies and subdependencies with exact versions.
- It locks the exact version of each package.
- It updates only when you install a new package or update an existing package.

#### **Role of `package.json`:**

1. Dependency Locking:

   - `package-lock.json` is an auto-generated file that provides a detailed, deterministic record of the dependency tree.
   - It locks down the specific versions of every installed package, preventing unintended updates.

2. Version Consistency:

   - This file ensures that every developer working on the project, as well as the CI/CD system, uses the exact same versions of dependencies.

   - Guarantees consistent builds across different environments, avoiding “it works on my machine” issues.

[Go to top ↑](#index)

### **12. What is `node_module` and `dist` folder**

1. The `node_modules` folder is where all the dependencies (libraries and packages) that your project needs are installed when you run `npm install`. These dependencies are listed in your `package.json` file under `dependencies` or `devDependencies`. This folder contains the code of the packages your project relies on.

2. The `dist` folder is typically used for **distribution**. It usually contains the bundled and optimized output of your project that is ready for deployment. When you run build commands like `npm run build` or use bundlers like Webpack or Vite, they generate the `dist` folder containing the final version of your application, which is typically minified and optimized for performance.

#### Key Differences:

- **`node_modules`**: Contains all the libraries and packages that your project depends on.
- **`dist`**: Contains the optimized and bundled output of your project, ready to be deployed.

[Go to top ↑](#index)

---

## **Level 2 (React js - Beginner)**

### **1. What is JSX? How it works**

JSX (JavaScript XML) is a syntax extension of JavaScript that allows us to write HTML-like code inside JavaScript. React uses JSX to make the UI code **more readable and maintainable**.

👉 **Example of JSX:**

```jsx
const element = <h1>Hello, Arshit!</h1>;
```

#### **Benefits of JSX:**

1. **Easier to Read & Write:** We can write HTML-like syntax directly in JavaScript.
2. **Faster Performance:** React optimizes JSX internally into efficient JavaScript.
3. **Better Debugging:** JSX provides meaningful error messages.
4. **Works with JavaScript Logic:** We can use variables, functions, and expressions inside JSX.

#### **How it works internally**

If we write this JSX:

```jsx
const element = <h1 className="title">Hello, Arshit!</h1>;
```

Now, `Babel` Convert this JSX into this JavaScript code using `React.createElement()`:

```js
const element = React.createElement(
  "h1", // Type of element (HTML tag).
  { className: "title" }, // Props (attributes) - here, `className` is passed as an object.
  "Hello, Arshit!" // Children (content inside the element)
);
```

React then converts this into a Virtual DOM object:

```js
{
  type: "h1",
  props: {
    className: "title",
    children: "Hello, Arshit!"
  }
}
```

- `type`: Specifies the HTML tag (`h1`).
- `props`: Contains all attributes (like `className`).
- `children`: The content inside the tag (`Hello, Arshit!`).

[Go to top ↑](#index)

### **2. What is `React.createElement()`?**

`React.createElement()` is a core React function used to create **React elements/component**. It is the **JavaScript equivalent of JSX**.

👉 **Syntax:**

```js
React.createElement(type, props, ...children);
```

| Parameter  | Meaning                                                                                        |
| ---------- | ---------------------------------------------------------------------------------------------- |
| `type`     | The HTML tag or React component (e.g., `"div"`, `"h1"`, or `MyComponent`).                     |
| `props`    | An object containing attributes (e.g., `{ className: "title" }`). Use `null` if no attributes. |
| `children` | Content inside the element (text, other elements, or components).                              |

**Example 1: Without Props**

```js
const element = React.createElement("h1", null, "Hello, Arshit!");
```

🔹 **Explanation:**

- `"h1"` → Type (HTML tag).
- `null` → No props/attributes.
- `"Hello, Arshit!"` → Child (content inside the `<h1>` tag).

  **Example 2: With Props (Attributes)**

```js
const element = React.createElement(
  "h1", //  → Type (HTML tag).
  { className: "title" }, //  → Props (attributes).
  "Hello, Arshit!" // → Child (content inside the `<h1>` tag).
);
```

[Go to top ↑](#index)

### **3. Define Babel?**

**Babel** is a **JavaScript compiler** that helps convert modern JavaScript (ES6+) and JSX into **older JavaScript (ES5)** that browsers can understand.

#### **Need:**

React uses **JSX**, but browsers **don’t understand JSX directly**. Babel converts JSX into **pure JavaScript** so that it can run in browsers.

#### **How Babel Works with React?**

When you write JSX code like this:

```jsx
const element = <h1>Hello, Arshit!</h1>;
```

Babel converts it into:

```js
const element = React.createElement("h1", null, "Hello, Arshit!");
```

This **pure JavaScript** code can now run in the browser.

f

**Features**

1. **Converts JSX into JavaScript**
2. **Translates ES6+ features** (like arrow functions, let/const, async/await) into older JavaScript
3. **Optimizes JavaScript code**
4. **Ensures compatibility with older browsers**

#### **How Babel Works Internally?**

Babel follows **three steps**:

1️⃣ **Parsing** – Converts JSX/ES6 code into an Abstract Syntax Tree (AST).  
2️⃣ **Transformation** – Translates new JavaScript syntax into older JavaScript.  
3️⃣ **Generation** – Creates the final JavaScript code that browsers can execute.

---

**Example**

🔹 **ES6 Code (Modern JavaScript)**

```js
const greet = (name) => `Hello, ${name}!`;
console.log(greet("Arshit"));
```

🔹 **Converted by Babel into ES5 (Old JavaScript)**

```js
"use strict";

var greet = function greet(name) {
  return "Hello, " + name + "!";
};
console.log(greet("Arshit"));
```

Now, older browsers that don’t support arrow functions (`=>`) can run this code!

[Go to top ↑](#index)

### **4. What are React Components? Functional vs Class Components**

React components are **building blocks** of a React application. They help in breaking the UI into **reusable** and **independent** pieces.

Each component:  
✅ **Returns JSX** (UI structure)  
✅ **Manages its own data (state) and behavior**  
✅ **Can be reused multiple times**

#### **Types of React Components**

**1. Function Components (Recommended)**

A function component is a **JavaScript function** that returns JSX. It is the **simplest** way to create a component in React.

**Example:**

```jsx
function Greeting() {
  return <h1>Hello, Arshit! 👋</h1>;
}

export default Greeting;
```

#### **Key Features of Function Components:**

✅ **Simple and easy to write** (just a function).  
✅ **Uses React Hooks** (`useState`, `useEffect`) for state and lifecycle.  
✅ **Better performance** (lighter and faster than class components).

**2. Class Components (Older Method)**

A class component is a **JavaScript class** that extends `React.Component` and has a `render()` method that returns JSX.

**Example:**

```jsx
import React, { Component } from "react";

class Greeting extends Component {
  render() {
    return <h1>Hello, Arshit! 👋</h1>;
  }
}

export default Greeting;
```

**Key Features of Class Components:**

✅ Uses `this.state` for managing state.  
✅ Uses lifecycle methods (`componentDidMount`, `componentDidUpdate`).  
✅ More complex than function components.

#### **Function vs. Class Components (Comparison Table)**

Here is the updated comparison table with the additional information about hooks:

| **Feature**           | **Function Component ✅ (Recommended)**                                                  | **Class Component ❌ (Old)**                                                              |
| --------------------- | ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Definition**        | A function component is just a JavaScript function that accepts `props` and returns JSX. | A class component extends `React.Component` and has a `render()` method that returns JSX. |
| **Render Method**     | No `render()` method is needed. JSX is returned directly.                                | Uses a `render()` method to return JSX.                                                   |
| **State Management**  | Uses `useState()` hook. Example: <br> `const [name, setName] = React.useState(' ')`      | Uses `this.state`. Example: <br> `this.state = { name: ' ' }` inside the constructor.     |
| **Lifecycle Methods** | Uses `useEffect()`. Example: <br> `useEffect(() => {}, [])`                              | Uses lifecycle methods like `componentDidMount()`, `componentDidUpdate()`, etc.           |
| **Hooks Support**     | ✅ Hooks can be easily used.                                                             | ❌ Hooks cannot be used directly in class components.                                     |
| **Performance**       | Faster and lightweight.                                                                  | Slower, consumes more memory.                                                             |
| **Recommended?**      | ✅ Yes (Modern React).                                                                   | ❌ No (Only for older projects).                                                          |

[Go to top ↑](#index)

### **5. What is the Virtual DOM?**

The **Virtual DOM (VDOM)** is a **lightweight copy** of the **Real DOM** (HTML DOM). It helps React update the UI **faster and more efficiently**.

#### **Why is the Virtual DOM needed?**

👉 **Problem with the Real DOM**

- The Real DOM updates **slowly** because every change in the UI **re-renders the whole page**.
- Frequent updates (e.g., typing in an input box) can **cause performance issues**.

👉 **Solution: Virtual DOM**

- Instead of changing the Real DOM directly, React **first updates the Virtual DOM**.
- Then, React **compares** the new Virtual DOM with the previous version.
- Only the **changed parts** are updated in the Real DOM (efficient updates).

React follows **three steps** to update the UI efficiently:

#### **1️⃣ Create Virtual DOM**

- When a React component renders, React **creates a Virtual DOM tree** that looks like the Real DOM.

#### **2️⃣ Compare with Previous Virtual DOM (Diffing)**

- When data changes, React **creates a new Virtual DOM** and **compares it with the previous version** (this process is called **diffing**).

#### **3️⃣ Update the Real DOM Efficiently (Reconciliation)**

- React finds **only the changed parts** and updates them in the Real DOM instead of reloading the entire page.

[Go to top ↑](#index)

### **6. What is the Diffing Algorithm in React?**

The **Diffing Algorithm** in React is a smart way to compare the **old Virtual DOM** with the **new Virtual DOM** and update only the changed parts in the Real DOM.

**Why is the Diffing Algorithm Needed?**

- The **Real DOM updates are slow**. Updating the whole page for small changes is inefficient.
- React solves this by **comparing two Virtual DOMs** and updating **only the differences**.

React's Diffing Algorithm works in **two steps**:

#### **1️⃣ Compare Two Virtual DOMs (Old vs. New)**

- Whenever a component updates, React creates a **new Virtual DOM**.
- It then compares this new Virtual DOM with the **previous one**.
- This comparison process is called **"Diffing"**.

#### **2️⃣ Identify Changes and Update the Real DOM (Reconciliation)**

- React **finds only the changed parts** and updates them in the Real DOM.
- Instead of re-rendering the entire UI, only the modified elements get updated.

**Example:**

**Before Update (Old Virtual DOM)**

```jsx
<h1>Hello, World!</h1>
```

**After Update (New Virtual DOM)**

```jsx
<h1>Hello, React!</h1>
```

🔹 React compares both Virtual DOMs and finds that **"World" changed to "React"**.  
🔹 Instead of reloading everything, React **only updates the changed text**.

#### **Optimizations in React’s Diffing Algorithm**

React uses **two key optimizations** for faster updates:

**1️⃣ Element Type Comparison**

- If the **element type is the same**, React updates only its **attributes**.

  ```jsx
  <button className="blue">Click Me</button>
  ```

  👉 If class changes to `"red"`, React only updates the **class**, not the entire button.

- If the **element type is different**, React **destroys the old element and creates a new one**.

  ```jsx
  <p>Hello</p>  ->  <h1>Hello</h1>
  ```

  👉 Here, `<p>` and `<h1>` are different, so React **removes `<p>` and creates `<h1>` anew**.

  **2️⃣ Key Prop Optimization for Lists**

When rendering a list of elements, React uses **keys** to track changes efficiently.

```jsx
{
  items.map((item) => <li key={item.id}>{item.name}</li>);
}
```

🔹 Without a **key**, React may **re-render the entire list**.  
🔹 With a **key**, React updates only the **changed items**, making it much faster.

[Go to top ↑](#index)

### **7. What are Keys in React?**

Keys are **unique identifiers** used by React to **track list items efficiently** it helps to identify which elements are added, updated, and removed from the react list.Then it React only updates the modified items, not the whole list.

**Why Use Keys**

- Without the **Keys** React might re-render entire lists rather than only the changed items.
- Wrong elements might be updated, causing UI bugs when items change position or are added/removed.

#### **Can We Use Index as a Key?**

🔹 **Yes, but only if items don’t change position.**

```jsx
{
  items.map((item, index) => <li key={index}>{item.name}</li>);
}
```

🔴 **Why is using `index` as a key bad?**

- If you add, remove, or rearrange items in the list, React might **mix up elements** because indexes change.
- React tracks elements using keys, so if an index changes, React might **update the wrong item**, causing UI glitches.

✅ **Best Practice:** Always use a **unique `id`** instead of `index`. 🚀

[Go to top ↑](#index)

### **8. What is Reconciliation in React?**

**Reconciliation** is the process **React uses to update the UI efficiently** when the state or props change. Instead of re-rendering the entire page, React **compares the Virtual DOM with the previous version** and updates only the changed parts.

#### **How Reconciliation Works**

1️⃣ **Render Phase** – React **creates a new Virtual DOM** based on the updated state/props.  
2️⃣ **Diffing Algorithm** – React **compares** the new Virtual DOM with the old one to find differences.  
3️⃣ **Updating the DOM** – React updates **only the changed elements** in the actual DOM.

#### **Why is Reconciliation Important?**

✅ **Optimized Performance** – React **avoids unnecessary updates** to the real DOM.  
✅ **Faster UI Updates** – Only the **modified parts** of the page are re-rendered.

[Go to top ↑](#index)

### **9. What is React Fiber?**

**React Fiber** is an **upgrade** of React's reconciliation algorithm, introduced in **React 16**. It was created to make React **faster**, **more flexible**, and **more responsive**. **React Fiber** is an **advanced upgrade** to the **old reconciliation process**.

---

#### **Key Changes and Improvements with React Fiber:**

1️⃣ **Asynchronous Rendering:**

- **Old React:** Rendering was **synchronous**, meaning React would block the entire UI while it was updating, causing delays.
- **With Fiber:** Rendering is **asynchronous**, so React can **pause** and **resume** heavy updates, keeping the app **responsive**.

2️⃣ **Prioritized Updates:**

- **Old React:** React didn't have a way to prioritize updates, so it handled them in the order they came.
- **With Fiber:** React can prioritize important updates (like user interactions) and process them **first**, while less critical updates (like background tasks) are handled later.

3️⃣ **Interruptible Rendering:**

- **Old React:** Once rendering started, it couldn’t be interrupted, meaning it could block UI updates.
- **With Fiber:** React can **pause** and **resume rendering**, allowing it to handle high-priority tasks without freezing the UI.

4️⃣ **Better Handling of Complex Apps:**

- React Fiber can now handle **more complex UI updates** more smoothly, especially when dealing with big applications or animations.

  **In Simple Terms:**

React Fiber makes React **faster** and **smarter** by allowing React to handle updates in **chunks**, **pause** and **resume** work, and **prioritize important tasks**—so your app stays smooth, even when there are lots of updates happening at once.

[Go to top ↑](#index)

### **10. `What are Props in React?**

**Props** (short for **"properties"**) are a way to **pass data** from a **parent component** to a **child component** in React. They are like **arguments** that you pass to a function.

Props are **read-only** (immutable), meaning a child component **cannot modify** the props it receives.

#### **How Props Work in React?**

1️⃣ **Define the props in the parent component**  
2️⃣ **Pass them to the child component as attributes**  
3️⃣ **Use them inside the child component using `props`**

---

**Example: Passing Props in a Functional Component**

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Greeting name="Arshit" />;
}
```

✅ **How it works:**

- The **`App`** component passes `"Arshit"` as a **prop** to the **`Greeting`** component.
- The **`Greeting`** component receives it and displays `"Hello, Arshit!"`.

[Go to top ↑](#index)

### **11. What is State in React? Difference between state & props.**

**State** is a special object in React that **stores data** that can change over time. It is used to **make components dynamic and interactive**.

Unlike **props**, which are passed from a parent, **state is managed within the component itself** and can be updated using the `useState` hook (for functional components) or `this.setState` (for class components).

#### **Difference Between Props and State in React**

| Feature                | **Props (📩 Passed from Parent)**                                             | **State (📦 Managed Inside Component)**                                         |
| ---------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Definition**         | Props are inputs passed from a **parent component** to a **child component**. | State is a **local data storage** inside a component that can change over time. |
| **Who Controls It?**   | Controlled by the **parent component**.                                       | Controlled by the **component itself**.                                         |
| **Can It Be Changed?** | ❌ No, props are **read-only** (cannot be modified by the child).             | ✅ Yes, state can be **updated** using `useState` or `setState()`.              |
| **Where Is It Used?**  | Used to **pass data** from parent to child.                                   | Used to **store and manage dynamic data** within a component.                   |
| **Re-render Trigger?** | Changing props **re-renders the child component**.                            | Updating state **re-renders the component**.                                    |
| **Mutability?**        | **Immutable** (cannot be changed by the component receiving it).              | **Mutable** (can be changed inside the component).                              |
| **Example Usage**      | Passing user data, styling properties, function callbacks.                    | Handling form inputs, toggling UI elements, counters, etc.                      |

**In Simple Terms:**

- **Props** → Like **function arguments**, passed from parent to child **(cannot be changed)**.
- **State** → Like **variables inside a function**, used to **store dynamic data** **(can be changed)**.

[Go to top ↑](#index)

### **12. What is a Composite Component in React?**

A **Composite Component** in React is a component that is made up of multiple smaller components. Instead of having one large component with all the logic, **composite components break down the UI into reusable, smaller components.**

---

#### **🔹 Why Use Composite Components?**

✅ **Reusability** – Smaller components can be reused in different parts of the app.  
✅ **Readability** – Code becomes cleaner and easier to understand.  
✅ **Maintainability** – It's easier to manage and update specific parts of the UI.  
✅ **Separation** – Each component handles only one specific task.

---

#### **🔹 Example of a Composite Component in React**

Let's say we are creating a **Profile Card**. Instead of writing everything in one component, we break it into **smaller components**.

#### **1️⃣ Creating Small Components**

```jsx
// Avatar Component
function Avatar({ src, alt }) {
  return <img src={src} alt={alt} width="100" />;
}

// Name Component
function Name({ fullName }) {
  return <h2>{fullName}</h2>;
}

// Bio Component
function Bio({ bio }) {
  return <p>{bio}</p>;
}
```

#### **2️⃣ Combining Them into a Composite Component**

```jsx
function ProfileCard({ user }) {
  return (
    <div className="card">
      <Avatar src={user.image} alt={user.name} />
      <Name fullName={user.name} />
      <Bio bio={user.bio} />
    </div>
  );
}
```

#### **3️⃣ Using the Composite Component**

```jsx
export default function App() {
  const userData = {
    name: "Arshit Kumar",
    image: "https://via.placeholder.com/100",
    bio: "React Developer & Tech Enthusiast",
  };

  return <ProfileCard user={userData} />;
}
```

[Go to top ↑](#index)

### **13. `Named` Export vs `Default` Export vs `* as` Export**

- **Named Export**: Use it when you need to export multiple things from a file.

  - You must use curly {} while importing.
  - Can rename imports.
  - Example:

    ```js
    export const name = "Arshit";
    export function greet() {
      return "Hello";
    }
    import { name, greet } from "./file";
    ```

- **Default Export**: When exporting only one main thing from a file.

  - No `{}` needed.
  - Can rename while importing.
  - Example:

    ```js
    export default function greet() {
      return "Hello";
    }
    import greet from "./file";
    ```

- **`* as` Export**: When importing everything from a file into an object.

  - Example:

    ```js
    import * as utils from "./file";
    console.log(utils.greet());
    ```

[Go to top ↑](#index)

### **14. React Hooks & Their Types (with Examples)**

React **Hooks** are functions that enable **functional components** to use React **state**, **lifecycle** and other React features. They eliminate the need for class components, making code cleaner and easier to maintain.

**Types of Hooks in React**

#### **1️. State Hook - `useState()`**

- State Hooks like `useState` allow functional components to manage local state.
- `useState` returns an array with two values:

  - Current state value (initially set to `0` in my case).
  - A function to update the state (which triggers re-render).

- **Example:**

```jsx
import React, { useState } from "react";

function Counter() {
  const [cnt, setCnt] = useState(0);
  const increment = () => {
    setCnt(cnt + 1);
    console.log("count: ", cnt);
  };
  return (
    <div>
      <h2>Count: {cnt}</h2>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default Counter;
```

- `useState` initializes `cnt` with `0` and provides `setCnt` to update it.
- Clicking the button updates the state using `setCnt(cnt + 1)`.

  **Why console shows `0` but display shows `1`?**

- **State updates are asynchronous in React.**
- When `setCnt(cnt + 1)` runs, React **schedules** the state update but **does not apply it immediately**.
- `console.log(cnt);` runs **before** React updates the state, so it logs the **old value**.
  - so `console.log(cnt);` and **react's state update schedule** runs together and before the actual re-render(state update/change)
- After the function finishes, React **re-renders** the component, and the updated `cnt`(1) is displayed in the UI. but shows 0 in `console.log(cnt);`

  **This happens because React batches state updates and re-renders after the function execution finishes.**

#### **2. Effect Hook - `useEffect()`**

- Effect Hooks like `useEffect` handle side effects like fetching data, subscriptions, and DOM manipulation.

- **Example:**

```jsx
import { useState, useEffect } from "react";

function DataFetcher() {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/posts/1")
      .then((response) => response.json())
      .then((json) => setData(json));
  }, []); // Empty array means it runs once on mount

  return <div>{data ? data.title : "Loading..."}</div>;
}
```

#### **3️. Context Hook - `useContext()`**

- Context Hooks like `useContext` enable functional components to access the React Context API and share data across the component tree without prop drilling.

- **1. Creating a Context**

  - First, we create a **context** using `createContext()`. This acts as a storage for shared data.

    ```jsx
    const MyContext = React.createContext(); // Creating a Context
    ```

- **2️. Providing a Value to Context (Parent Component)**

  - The **Provider** component **wraps** the components that need access to the shared data. It **provides a `value`** (can be a string, object, function, etc.).

    ```jsx
    function Parent() {
      return (
        <MyContext.Provider value="Hello, World!">
          <Child />
        </MyContext.Provider>
      );
    }
    ```

  - Here, `MyContext.Provider` makes `"Hello, World!"` available to all child components inside it.

- **3️. Consuming Context in a Child Component**

  - Inside the child component, we use `useContext(MyContext)` to **access the value** from the provider.

  ```jsx
  function Child() {
    const value = useContext(MyContext); // Getting the context value
    return <p>{value}</p>; // Output: Hello, World!
  }
  ```

#### **4️. Ref Hook - `useRef()`**

- It creates a **mutable reference** that persists across renders. It can hold values (like DOM elements) without triggering re-renders when the value changes.

✅ **Example: Auto Focus on Input Field**

```jsx
import React, { useRef, useEffect } from "react";

function AutoFocusInput() {
  const inputRef = useRef(); // Create reference

  useEffect(() => {
    inputRef.current.focus(); // Automatically focus input on render
  }, []);

  return (
    <div>
      <input ref={inputRef} type="text" placeholder="Type here..." />
    </div>
  );
}

export default AutoFocusInput;
```

- **Why `useRef`?**

  - If we dont use `useRef` we have to rely on `useState`, then, every change to the input would cause a re-render.
  - `useRef` allows us to access the input (_or any other_) element (_or values, variables_) **without triggering re-renders**.
  - In this example, when the component renders, `useEffect` runs and sets focus on the input field.
  - **If we don’t use `useRef`, we have to rely on `useState` and `useEffect`** to manually manage focus, which is **not optimal** because it causes unnecessary re-renders and requires direct DOM access.

  **With `useRef`, we can directly interact with the DOM efficiently without unnecessary re-renders.** 🚀

#### **5. Memoization(Performance) Hooks**

Performance Hooks like `useMemo` and `useCallback` optimize rendering by memoizing values or functions.

- **What is `useMemo()`?**

- **Definition:**  
  `useMemo` is a React hook that **memorizes** the result of an expensive calculation and **caches** it to avoid unnecessary recalculations. It only recalculates the value when its dependencies change, which improves performance by preventing redundant calculations on every render.

- **When to use it?**  
  Use `useMemo` when you have a **complex calculation** or **large data processing** that doesn't need to be recomputed on every render (_means that it only change once in a while or never_). This can greatly optimize performance by preventing costly operations from being repeated unnecessarily.

- **Example: High Computation Without `useMemo`**

Here’s an example where we process a large dataset (`largeData`) and find a specific value from it on every render:

```jsx
import React, { useState } from "react";

function Counter() {
  const [cnt, setCnt] = useState(0);
  const largeData = new Array(10_000_001).fill().map((_, index) => {
    return {
      id: index,
      isTrue: index === 10_000_000,
    };
  });
  const arrValue = largeData.find((val) => val.isTrue); // Expensive calculation

  const increment = () => {
    setCnt(cnt + 1);
  };

  return (
    <div>
      <h2>Count: {cnt}</h2>
      <h2>Value Found: {arrValue.id}</h2>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default Counter;
```

**What Happens Without `useMemo`?**

- Every time the **component re-renders** (like when the `count` is incremented), the `largeData.find()` method will **re-run** and perform the expensive operation of searching through the entire `largeData` array (10 million items in this case).
- This leads to **performance issues** since the same expensive computation is done repeatedly even though the data (`largeData`) doesn't change on each render.

- **What Happens With `useMemo`?**

Now, we use `useMemo` to **memoize** the calculation, so it only recalculates when the **data** actually changes.

we will change the normal funtion

```jsx
const arrValue = largeData.find((val) => val.isTrue); // Expensive calculation
```

to `useMemo`

```jsx
// Memoize the result of the expensive calculation
const arrValue = useMemo(
  () => largeData.find((val) => val.isTrue),
  [largeData] // dependencies => this expensive function will only run (again) when its dependencies have changed.
);
```

- `useMemo` memorizes the result of `largeData.find()`.
- It **only recalculates** the result if `largeData` changes. Since `largeData` is static (it doesn't change after being created), `useMemo` ensures that the search operation doesn’t get re-executed unnecessarily on every render.
- This improves performance by **avoiding expensive recalculations** when the state (`cnt`) changes.

  **What is `useCallback()`?**

- **Definition:**  
  `useCallback` is a React hook used to **memoize functions** so that they are not recreated on every render. It returns a **memoized version of the callback function** that only changes if one of the dependencies has changed.

- **Why use it?**: In React, **every time a component re-renders**, it **recreates all the functions** defined inside that component. This happens because the functions in JavaScript / Reactjs are treated as new every time the component renders, unless specifically memoized or handled.

  - When you pass a function as a prop to a child component, React **sees it as a new function** every time the parent re-renders, even if the function’s logic hasn't changed. This causes the child component to re-render as well, which might be unnecessary, leading to performance issues.

- **How Does `useCallback` Help?**: When you use **`useCallback`**, it helps React to **remember the function** and only re-create it when its dependencies change. So, if the dependencies (like the `count`) haven't changed, React won't re-create the function and the same instance of the function will be passed to child components.

- **Syntax:**

  ```jsx
  const memoizedFunction = useCallback(() => {
    // function logic
  }, [dependencies]);
  ```

- **Example:**

Let’s say we have a parent component that passes a function to a child component. Without `useCallback`, the function will be recreated on every render of the parent component.

```jsx
import React, { useState, useCallback } from "react";

function Parent() {
  const [count, setCount] = useState(0);

  const handleClick = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h2>Count: {count}</h2>
      {/* Passing the function to the child */}
      <Child onClick={handleClick} />
    </div>
  );
}

function Child({ onClick }) {
  console.log("Child re-rendered");
  return <button onClick={onClick}>Click me</button>;
}

export default Parent;
```

In this case, `handleClick` is recreated every time the `Parent` re-renders, causing unnecessary re-renders of the `Child` component.

Now, if we wrap `handleClick` in `useCallback`:

```jsx
const handleClick = useCallback(() => {
  setCount(count + 1);
}, [count]); // Memoize the function, only recreate when 'count' changes
```

- Now, **`handleClick`** will not be recreated unless `count` changes, preventing unnecessary re-renders of the `Child` component.

**`useMemo` vs `useCallback`:**

- **`useMemo`**:
  - Memoizes a **value** (like a computed result or object).
  - Only recomputes when dependencies change.
  - Use for **expensive calculations**.
- **`useCallback`**:
  - Memoizes a **function**.
  - Only recreates the function when dependencies change.
  - Use for **functions passed to child components** to avoid unnecessary re-renders.

#### **✨ Summary**

| Hook            | Purpose                            |
| --------------- | ---------------------------------- |
| `useState()`    | Manages component state            |
| `useEffect()`   | Handles side effects (API, timers) |
| `useContext()`  | Uses global state without props    |
| `useRef()`      | Directly accesses DOM elements     |
| `useMemo()`     | Memoize Value                      |
| `useCallback()` | Memoize functions                  |

[Go to top ↑](#index)
