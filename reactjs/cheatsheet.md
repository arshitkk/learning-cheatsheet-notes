# React JS Cheatsheet

## **Index**

0. ### [Level 0](#level-0-1)

   1. **[What is Emmet?](#1-what-is-emmet)**
   2. **[Difference between a Library and a Framework?](#2-difference-between-a-library-and-a-framework)**
   3. **[What is a CDN? Why do we use it?](#3-what-is-a-cdn-why-do-we-use-it)**
   4. **[Why is React known as React?](#4-why-is-react-known-as-react)**
   5. **[What is `crossorigin` in the `<script>` tag?](#5-what-is-crossorigin-in-the-script-tag)**
   6. **[What is the difference between React and ReactDOM?](#6-what-is-the-difference-between-react-and-reactdom)**

1. ### [Level 1](#level-1-1)

   1. **[What is NPM?](#1-what-is-npm)**
   2. **[What is a Bundler? Types](#2-what-is-a-bundler-types)**
   3. **[What is Vite, and why do we need it?](#3-what-is-vite-and-why-do-we-need-it)**
   4. **[What is `.vite` (Vite's cache folder)?](#4-what-is-vite-vites-cache-folder)**
   5. **[What is `npx`?](#5-what-is-npx)**
   6. **[Difference Between `dependencies` and `devDependencies`](#6-difference-between-dependencies-and-devdependencies)**
   7. **[What is Tree Shaking in Vite?](#7-what-is-tree-shaking-in-vite)**
   8. **[What is Hot Module Replacement (HMR) in Vite?](#8-what-is-hot-module-replacement-hmr-in-vite)**
   9. **[List 5 main features of `Vite`](#9-list-5-main-features-of-vite)**
   10. **[What is `.gitignore`? What should we add and not add into it?](#10-what-is-gitignore-what-should-we-add-and-not-add-into-it)**

---

## **Level 0**

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

## **Level 1**

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
