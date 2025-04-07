# React JS Cheatsheet

## **Index**

0. ### **[Part 0 (Starting fundamentals)](#part-0-starting-fundamentals-1)**

   1. **[What is Emmet?](#1-what-is-emmet)**
   2. **[What is a CDN? Why do we use it?](#2-what-is-a-cdn-why-do-we-use-it)**
   3. **[What is `crossorigin` in the `<script>` tag?](#3-what-is-crossorigin-in-the-script-tag)**
   4. **[Difference between a Library and a Framework?](#4-difference-between-a-library-and-a-framework)**
   5. **[Why is React known as React?](#5-why-is-react-known-as-react)**
   6. **[What is the difference between React and ReactDOM?](#6-what-is-the-difference-between-react-and-reactdom)**
   7. **[What is CORS? Why does it matter?](#7-what-is-cors-why-does-it-matter)**
   8. **[Define SPA?](#8-define-spa)**
   9. **[What is Client-Side Routing (CSR) & Server-Side Routing (SSR)?](#9-what-is-client-side-routing-csr--server-side-routing-ssr)**
   10. **[Debounce in React (with Example)](#10-debounce-in-react-with-example)**
   11. **[What is Throttling in ReactJS?](#11-what-is-throttling-in-reactjs)**
   12. **[Difference between `fetch` and `axios`?](#12-difference-between-fetch-and-axios)**

1. ### **[Part 1 (NPM, Vite & Build Tools)](#part-1-npm-vite--build-tools-1)**

   1. **[What is NPM?](#1-what-is-npm)**
   2. **[What is `npx`?](#2-what-is-npx)**
   3. **[What is a Bundler? Types](#3-what-is-a-bundler-types)**
   4. **[What is Vite, and why do we need](#4-what-is-vite-and-why-do-we-need-it)**
   5. **[What is `.vite` (Vite's cache folde](#5-what-is-vite-vites-cache-folder)**
   6. **[Difference Between `dependencies` and `devDependencies](#6-difference-between-dependencies-and-devdependencies)**
   7. **[What is Tree Shaking in Vite](#7-what-is-tree-shaking-in-vite)**
   8. **[What is Hot Module Replacement (HMR) in Vite](#8-what-is-hot-module-replacement-hmr-in-vite)**
   9. **[List 5 main features of `Vite](#9-list-5-main-features-of-vite)**
   10. **[Difference Between package.json and package-lock.json](#10-difference-between-packagejson-and-package-lockjson)**
   11. **[What is `.gitignore`? What should we add and not add into it?](#11-what-is-gitignore-what-should-we-add-and-not-add-into-it)**
   12. **[What is node_module and dist folder](#12-what-is-node_module-and-dist-folder)**

2. ### **[Part 2 (React js - Core Concepts)](#part-2-react-js---core-concepts-1)**

   1. **[What is JSX? How it works](#1-what-is-jsx-how-it-works)**
   2. **[What is `React.createElement()`?](#2-what-is-reactcreateelement)** 3.** [Define Babel?](#3-define-babel)**
   3. **[What are React Components? Functional vs Class Components](#4-what-are-react-components-functional-vs-class-components)**
   4. **[What is the Virtual DOM?](#5-what-is-the-virtual-dom)**
   5. **[What is the Diffing Algorithm in React?](#6-what-is-the-diffing-algorithm-in-react)**
   6. **[What is Reconciliation in React?](#7-what-is-reconciliation-in-react)**
   7. **[What are Keys in React?](#8-what-are-keys-in-react)** 9.**[What is React Fiber?](#9-what-is-react-fiber)**
   8. **[What are Props in React?](#10-what-are-props-in-react)**
   9. **[What is State in React? Difference between state & props](#11-what-is-state-in-react-difference-between-state--props)**
   10. **[What is a Composite Component in React?](#12-what-is-a-composite-component-in-react)**
   11. **[Named Export vs Default Export vs \* as Export](#13-named-export-vs-default-export-vs--as-export)**

3. ### **[Part 3 (React js - Advanced React Concepts)](#part-3-react-js---advanced-react-concepts-1)**
   1.**[What is Lifting State Up in React](#1-what-is-lifting-state-up-in-react)** 2. **[Controlled vs Uncontrolled Components in Reac](#2-controlled-vs-uncontrolled-components-in-react)** 3. **[What is React.StrictMode & Why Use It?](#3-what-is-reactstrictmode--why-use-it)** 4.**[What is Lazy Loading in React & `React.Suspense`](#4-what-is-lazy-loading-in-react--reactsuspense)** 5. **[What is React.Fragment?](#5-what-is-reactfragment)** 6. **[React Hooks & Their Types (with Examples)](#6-react-hooks--their-types-with-examples)** 7. **[What is a Custom Hook in React?](#7-what-is-a-custom-hook-in-react)** 8. **[What is Microservices and Monolithic Architecture?](#8-what-is-microservices-and-monolithic-architecture)** 9. **[What is React Router?](#9-what-is-react-router)** 10. **[What is Redux Toolkit (RTK)](#10-what-is-redux-toolkit-rtk)** 11. **[What are Higher Order Component (HOC) in React ](#11-what-are-higher-order-component-hoc-in-react)**

---

## **Part 0 (Starting fundamentals)**

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

### **2. What is a CDN? Why do we use it?**

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

### **3. What is `crossorigin` in the `<script>` tag?**

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

### **4. Difference between a Library and a Framework?**

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

### **5. Why is React known as React?**

React is called **React** because it **reacts** to changes in data efficiently.

🔹 It uses a **virtual DOM** to detect changes and update only those component which are needed to update, making apps fast and responsive.

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

### **7. What is CORS? Why does it matter?**

#### **🔹 What is CORS?**

CORS (**Cross-Origin Resource Sharing**) is a **security rule** that stops web pages from making requests to a **different domain** unless the server allows it.

For example, if your React app (`http://localhost:3000`) tries to fetch data from `https://api.example.com`, the browser **blocks** the request if CORS is not set up properly.

#### **When Does a Request Fail Due to CORS?**

A request fails due to CORS if:

- **Different Origins (Cross-Origin Requests)**

  - Your site: `https://myapp.com`
  - API: `https://api.example.com` (Different domain → CORS issue)

- **Different Ports**

  - Frontend running on `http://localhost:3000`
  - Backend running on `http://localhost:5000` (Same domain, but **different port** → CORS issue)

- **Different Protocols**

- Example:

  - Your site: `https://myapp.com` (HTTPS)
  - API: `http://api.example.com` (HTTP) (**Different protocol** → CORS issue )

- **Subdomains Treated as Different Origins**

- Example:
  - `https://app.example.com` vs `https://api.example.com` (Different subdomains → CORS issue 🚨)

#### **🔹 Why does CORS matter?**

- **Security:** Prevents malicious websites from accessing sensitive data from another site.
- **Prevents Unauthorized Requests:** Stops unauthorized domains from using APIs without permission.
- **Ensures Data Privacy:** Protects users' data from being stolen by other sites.

#### **How to Fix CORS Errors?**

**1. Enable CORS on the Server** (Recommended)

- The server owner should allow requests from specific domains using **CORS headers**.
- Example header for allowing all origins:
  ```bash
  Access-Control-Allow-Origin: *
  ```

**2. Use a Proxy Server**

- If you don’t control the API, use a **proxy** to send requests through your own backend.
- Example in a `package.json` (for local dev):

  ```json
  "proxy": "https://api.example.com"
  ```

**3. Use Browser Extensions** (Temporary Fix)

- Chrome extensions like **CORS Unblock** can bypass restrictions for testing purposes.

[Go to top ↑](#index)

### **8. Define SPA?**

In web development, **SPA (Single Page Application)** is a type of web app that loads a single HTML page and dynamically updates content without refreshing the page. It provides a smooth, fast user experience similar to a mobile app.

**Key Features of SPA:**

- **No full-page reloads** – Only required content updates dynamically.
- **Fast performance** – Loads once, then fetches data as needed.
- **Uses JavaScript frameworks** – Commonly built with React, Angular, or Vue.js.
- **Improved user experience** – Feels more like a native app.

Examples of SPAs: Gmail, Facebook, Twitter, and Google Maps.

[Go to top ↑](#index)

### **9. What is Client-Side Routing (CSR) & Server-Side Routing (SSR)?**

Routing is the process of navigating between different pages or views in a website or application.

**1. Client-Side Routing (CSR)**

- Client-side routing happens in the **browser** using JavaScript. Instead of loading a new page from the server, JavaScript changes the content dynamically.

- **Example:**  
  Think of **Netflix**. When you click on a movie, the page doesn’t refresh; the content just changes. That’s client-side routing!

- **Pros:**

  - Faster navigation (no full reload)
  - Smooth, app-like experience
  - Reduces server load

- **Cons:**

  - Slower initial load (needs JavaScript)
  - Can cause SEO issues (search engines may not see all content)

**2. Server-Side Routing (SSR)**

- Server-side routing means the **server processes each request** and sends a new page. Every time you click a link, the browser requests a new HTML page from the server.

- **Example:**  
  Think of **a library**. Every time you need a new book, you go to the counter (server), ask for a book (request a page), and get a new one every time.

- **Pros:**

  - Better for SEO (search engines see full pages)
  - No JavaScript dependency
  - Works even if JavaScript is disabled

- **Cons:**

  - Slower navigation (page reloads each time)
  - More server load

- **Key Differences:**

| Feature         | Client-Side Routing (CSR) | Server-Side Routing (SSR) |
| --------------- | ------------------------- | ------------------------- |
| Where it runs   | Browser (JavaScript)      | Server                    |
| Page Load Speed | Faster after first load   | Slower (full reloads)     |
| SEO             | Can be tricky             | Better SEO                |
| User Experience | Smooth, app-like          | Slower transitions        |
| Example         | Netflix, Gmail            | Traditional websites      |

- **Which One Should You Use?**

  - Use **Client-Side Routing** for interactive apps like **React, Angular, Vue apps**.
  - Use **Server-Side Routing** for SEO-focused sites like **blogs, news websites**.
  - Some apps use **both (Hybrid Approach)** for best performance (Next.js does this).

[Go to top ↑](#index)

### **10. Debounce in React (with Example)**

- Debouncing is a way of delaying the execution of a function until a certain amount of time has passed since the last time it was called. This can be useful for scenarios where we want to avoid unnecessary or repeated function calls that might be expensive or time-consuming.

- Imagine we have a search box that shows suggestions as the user types. If we call a function to fetch suggestions on every keystroke, we might end up making too many requests to the server, which can slow down the application and waste resources. Instead, we can use debouncing to wait until the user has stopped typing for a while before making the request.

**Example (ReactJs)**

```jsx
import React, { useRef, useState } from "react";

export default function CounterApp() {
  const [count, setCount] = useState(0);
  const [trigger, setTrigger] = useState(0);
  const debounceRef = useRef(null);

  function countHandler() {
    setCount((p) => p + 1); // Increase count immediately

    if (debounceRef.current) {
      clearTimeout(debounceRef.current); // Clear previous timeout
    }

    debounceRef.current = setTimeout(() => {
      setTrigger((p) => p + 1); // Update trigger after 800ms
    }, 800);
  }

  return (
    <div>
      <h2>Count: {count} </h2>
      <h2>Triggered: {trigger} </h2>
      <button onClick={countHandler}>Button</button>
    </div>
  );
}
```

1️⃣ **States (`count` & `trigger`)**:

- `count`: Increases immediately when the button is clicked.
- `trigger`: Updates **after a delay (800ms)** using debounce.

2️⃣ **`useRef` (`debounceRef`)**:

- Stores the timeout ID to manage and clear the delay.

3️⃣ **Function `countHandler()` Execution**:

- **Increases `count` immediately** when the button is clicked.
- **Clears any existing timeout** (to prevent multiple updates).
- **Starts a new `setTimeout()`** to update `trigger` after 800ms.

4️⃣ **Debounce Effect**:

- If the button is clicked again **within 800ms**, the old timeout is **cleared** and restarted.
- `trigger` only updates **after the user stops clicking for 800ms**.

**Why Use Debounce?**

- **Prevents unnecessary re-renders** or state updates.
- **Useful for optimizing API calls**, search inputs, button clicks, etc.
- **Improves performance** by reducing frequent updates.

[Go to top ↑](#index)

### **11. What is Throttling in ReactJS?**

- **Throttling** is a technique used to **limit how often a function runs** within a given time frame, even if it is triggered continuously.

- Unlike **debouncing**, which waits for inactivity, **throttling ensures a function runs at most once in a set interval**.

**Example in ReactJS**

Let's say we have a button that increases a counter. If a user clicks it rapidly, we **want to limit the updates** to once every 1000ms.

```jsx
import React, { useState, useRef } from "react";

export default function CounterApp() {
  const [count, setCount] = useState(0);
  const throttleRef = useRef(false); // To track whether throttling is active

  function countHandler() {
    if (throttleRef.current) return; // If throttling is active, do nothing

    setCount((prev) => prev + 1); // Increase count immediately
    throttleRef.current = true; // Block further clicks

    setTimeout(() => {
      throttleRef.current = false; // Allow clicks after 1s
    }, 1000);
  }

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={countHandler}>Increase</button>
    </div>
  );
}
```

**Dry Run:**

#### **1️⃣ Initial State**

- `count` starts at **0**.
- `throttleRef.current` is **false** (throttling is not active).
- The button is **clickable**.

#### **2️⃣ First Click (`countHandler` Runs)**

- `if (throttleRef.current) return;`  
  ✅ **Passes the condition** (because `throttleRef.current` is **false**).
- `setCount((prev) => prev + 1);`  
  ✅ **Increases count** by 1.
- `throttleRef.current = true;`  
  ✅ **Blocks further clicks** for 1000ms.

#### **3️⃣ Before 1000ms (Rapid Clicking)**

- If the user clicks again **before** 1000ms:  
  ❌ `if (throttleRef.current) return;` stops execution.  
  ✅ The `count` **does not update**.

#### **4️⃣ After 1000ms**

- `setTimeout(() => { throttleRef.current = false; }, 1000);`  
  ✅ **Resets** `throttleRef.current` back to `false`.  
  ✅ **Now clicks are allowed again.**

#### **Use Cases of Throttling in ReactJS**

- **Handling scroll events** (to avoid too many re-renders).
- **Limiting API calls** (like search suggestions).
- **Reducing rapid button clicks** (like in our example).

[Go to top ↑](#index)

### **12. Difference between `fetch` and `axios`?**

#### **Axios**:

**Axios** is a **promise-based HTTP client** for JavaScript. It's a **library** that helps you send requests (like GET, POST) to APIs easily. It works in the browser and Node.js and handles many things like JSON parsing, timeouts, and errors automatically.

You need to install it:

```bash
npm install axios
```

#### **Fetch**:

**Fetch** is a **built-in JavaScript function** (no need to install) that is used to make network requests like GET, POST, etc. It's part of modern browsers and returns **promises**, but you need to handle things like JSON parsing and errors **manually**.

#### **Difference Between Axios and Fetch**

| Feature             | **Axios**                         | **Fetch**                               |
| ------------------- | --------------------------------- | --------------------------------------- |
| Install Needed?     | Yes (`npm install axios`)         | No (built into JavaScript)              |
| JSON Handling       | Auto parses response to JSON      | You must use `response.json()` manually |
| Error Handling      | Catches HTTP errors automatically | You need to manually check `res.ok`     |
| Timeout Support     | Built-in timeout option           | Needs manual timeout setup              |
| Request Cancelation | Easy with `CancelToken`           | Needs `AbortController`                 |
| Base URL & Headers  | Easy to set defaults globally     | You set them every time manually        |
| Simplicity          | Cleaner and shorter code          | More boilerplate (extra code)           |

#### **Example - Axios:**

```js
import axios from "axios";

axios
  .get("https://api.example.com/users")
  .then((res) => console.log(res.data))
  .catch((err) => console.log(err));
```

#### **Example - Fetch:**

```js
fetch("https://api.example.com/users")
  .then((res) => {
    if (!res.ok) throw new Error("Something went wrong");
    return res.json();
  })
  .then((data) => console.log(data))
  .catch((err) => console.log(err));
```

- Use **Axios** when you want **cleaner code, easy error handling, timeouts, and more features**.
- Use **Fetch** if you want **zero dependencies** and are okay writing more code for handling things.

[Go to top ↑](#index)

---

## **Part 1 (NPM, Vite & Build Tools)**

### **1. What is NPM?**

**NPM** is a tool to **manage packages** (reusable code, libraries, frameworks, tools) for JavaScript projects. It helps you to install, update, and manage libraries and dependencies in your projects.

- **Example**:  
   When you want to use a library like React, you use NPM to install it.

[Go to top ↑](#index)

### **2. What is `npx`?**

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

### **3. What is a Bundler? Types**

A **Bundler** is a tool that takes multiple files (JavaScript, CSS, HTML) and combines them into a single file (or a few files), making it easier and faster for the browser to load. It helps optimize the project by minimizing file size.

- **Types**:
  - **Webpack**: A powerful bundler used in many large projects.
  - **Parcel**: An easy-to-use bundler with automatic configuration.
  - **Rollup**: Good for libraries and optimizing code for production.

[Go to top ↑](#index)

### **4. What is Vite, and why do we need it?**

**Vite** is a modern build tool and bundler that focuses on spe**ed and **performance\*\*. It uses native ES modules to speed up the development environment and optimizes for production with fast build times. This means that Vite only transforms the files that change, rather than rebuilding everything every time you make a change. This reduces the wait time and makes the development process almost instant.

**Why do we need it?**

- **Faster Development**: Vite uses native ES modules to speed up the development environment.
- **Hot Module Replacement (HMR)**: Instant updates to the page without refreshing, improving the developer experience.
- **Optimized for Modern Frameworks**: Built with React, Vue, and other modern JavaScript frameworks in mind.

[Go to top ↑](#index)

### **5. What is `.vite` (Vite's cache folder)?**

The `.vite` folder is where Vite stores temporary files to make the development process faster. When you're working on your project, Vite processes things like JavaScript, CSS, and images, and saves the results in this folder. This way, it doesn't have to process the same files every time you make a change, which helps speed up development.

**Why do we need it?**

- Stores compiled code, cache data, and other temporary files.
- Helps reduce build time by reusing files instead of re-compiling everything.
- You can delete the .vite folder if it becomes too large or causes issues, as it will be recreated on the next build.

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

### **10. Difference Between `package.json` and `package-lock.json`**

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

### **11. What is `.gitignore`? What should we add and not add into it?**

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

### **12. What is `node_module` and `dist` folder**

1. The `node_modules` folder is where all the dependencies (libraries and packages) that your project needs are installed when you run `npm install`. These dependencies are listed in your `package.json` file under `dependencies` or `devDependencies`. This folder contains the code of the packages your project relies on.

2. The `dist` folder is typically used for **distribution**. It usually contains the bundled and optimized output of your project that is ready for deployment. When you run build commands like `npm run build` or use bundlers like Webpack or Vite, they generate the `dist` folder containing the final version of your application, which is typically minified and optimized for performance.

#### Key Differences:

- **`node_modules`**: Contains all the libraries and packages that your project depends on.
- **`dist`**: Contains the optimized and bundled output of your project, ready to be deployed.

[Go to top ↑](#index)

### **13. What are `tailwind.config.js` Keys**

In **Tailwind CSS**, the `tailwind.config.js` file is used to customize styles, colors, breakpoints, and more. Here’s what each key means:

**1️. `content`**

- This tells Tailwind **where** to look for class names in your project. If a file isn't listed here, Tailwind **won't generate styles** for its classes.

- **Example:**

```js
module.exports = {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
};
```

- Tailwind scans all `.html`, `.js`, `.jsx`, `.ts`, `.tsx` files in the `src/` folder.
- It **removes unused classes** (purging CSS) to keep the final CSS file small.

**2️. `theme`**

- Defines the default design system for your project. You can modify or extend colors, fonts, spacing, etc.

- **Example:**

```js
module.exports = {
  theme: {
    colors: {
      primary: "#1E40AF",
      secondary: "#9333EA",
    },
    fontFamily: {
      sans: ["Inter", "sans-serif"],
    },
  },
};
```

- Customizes Tailwind's **default styles** (e.g., custom colors, fonts).

**3️. `extend`**

Instead of **overriding** Tailwind’s default styles, `extend` **adds new values** without removing defaults.

- **Example:**

```js
module.exports = {
  theme: {
    extend: {
      spacing: {
        128: "32rem",
        144: "36rem",
      },
      colors: {
        neonGreen: "#39ff14",
      },
    },
  },
};
```

- Adds **new values** while keeping Tailwind's built-in styles.
- `spacing.128` (`w-128`) → Now available as `width: 32rem`.
- Adds a **new custom color** (`text-neonGreen`).

**4️. `plugins`**

- Used to **add extra functionality** to Tailwind, like forms, typography, or custom utilities.

- **Example:**

```js
module.exports = {
  plugins: [require("@tailwindcss/forms"), require("@tailwindcss/typography")],
};
```

- Adds Tailwind’s **official plugins** for styling forms & typography.

🚀 **Summary of Each Key**  
| Key | Purpose |
|----------|---------|
| `content` | Defines which files Tailwind should scan for class names (purging unused styles). |
| `theme` | Modifies Tailwind’s default design system (colors, fonts, spacing, etc.). |
| `extend` | Adds new styles **without removing defaults**. |
| `plugins` | Adds extra Tailwind features using official or custom plugins. |

[Go to top ↑](#index)

---

## **Part 2 (React js - Core Concepts)**

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

### **7. What is Reconciliation in React?**

**Reconciliation** is the process **React uses to update the UI efficiently** when the state or props change. Instead of re-rendering the entire page, React **compares the Virtual DOM with the previous version** and updates only the changed parts.

#### **How Reconciliation Works**

1️⃣ **Render Phase** – React **creates a new Virtual DOM** based on the updated state/props.  
2️⃣ **Diffing Algorithm** – React **compares** the new Virtual DOM with the old one to find differences.  
3️⃣ **Updating the DOM** – React updates **only the changed elements** in the actual DOM.

#### **Why is Reconciliation Important?**

✅ **Optimized Performance** – React **avoids unnecessary updates** to the real DOM.  
✅ **Faster UI Updates** – Only the **modified parts** of the page are re-rendered.

[Go to top ↑](#index)

### **8. What are Keys in React?**

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

---

## **Part 3 (React js - Advanced React Concepts)**

### **1. What is Lifting State Up in React**

In React, **Lifting State Up** means **moving the state from a child component to its parent** so that multiple child components can share and use the same state.

**Why is it needed? 🤔**

- React is built around the idea of components and unidirectional data flow, meaning data flows down from parent to child through props.
- However, sometimes two or more sibling components need to share the same state. If each component manages its own version of the state, inconsistencies can arise.

- **Example**

Let's say we have **two buttons**:

    - One **increases** the counter.
    - One **decreases** the counter.

Both buttons should update the **same counter value**, but they are in different components.

**❌ Without Lifting State Up**

Each button has its **own state**, so they work **independently** and don't sync.

```jsx
function IncreaseButton() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}

function DecreaseButton() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count - 1)}>Decrease</button>
    </div>
  );
}

export default function CounterApp() {
  return (
    <div>
      <IncreaseButton />
      <DecreaseButton />
    </div>
  );
}
```

👉 **Problem:**

- Both buttons **maintain their own count separately**, instead of sharing a single value.

**✅ With Lifting State Up**

We **move the state to the parent** and pass it to both buttons as **props**.

```jsx
import React, { useState } from "react";

function CounterApp() {
  const [count, setCount] = useState(0); // State in Parent

  return (
    <div>
      <h2>Count: {count}</h2>
      <IncreaseButton count={count} setCount={setCount} />
      <DecreaseButton count={count} setCount={setCount} />
    </div>
  );
}

function IncreaseButton({ count, setCount }) {
  return <button onClick={() => setCount(count + 1)}>Increase</button>;
}

function DecreaseButton({ count, setCount }) {
  return <button onClick={() => setCount(count - 1)}>Decrease</button>;
}

export default CounterApp;
```

- **How It Works? 🛠️**

  1. **State (`count`) is lifted up** to `CounterApp` (the parent component).
  2. The **same state is passed as props** to both `IncreaseButton` and `DecreaseButton`.
  3. Clicking **either button updates the shared state**, keeping them in sync.

- **Why is Lifting State Up Important?**

  - Helps **share state** between multiple components.
  - Avoids **duplicate state**, making the app more efficient.
  - Ensures **consistent updates** across components.

[Go to top ↑](#index)

### **2. Controlled vs Uncontrolled Components in React**

In React, form inputs can be **Controlled** or **Uncontrolled** based on how they manage their values.

#### **1️⃣ Controlled Components**

- In **Controlled Components**, React controls the form input values using **state** (`useState`).

- **Example**

```jsx
import React, { useState } from "react";

function ControlledInput() {
  const [text, setText] = useState(""); // React controls the input value

  return (
    <div>
      <input
        type="text"
        value={text} // Controlled by React state
        onChange={(e) => setText(e.target.value)}
      />
      <p>Typed Text: {text}</p>
    </div>
  );
}

export default ControlledInput;
```

- The **input value is controlled by React state (`text`)**.
- Every keystroke updates **state**, and the input re-renders with the new value.

**Advantages**

- **Better Control:** React has **full control** over the input value.
- **Validation:** Easy to **validate** input as the user types.
- **Predictability:** Input value is always in **sync** with React state, making the UI consistent.
- **Dynamic Behavior:** Allows implementing features like **conditional rendering** and **input manipulation** easily.

**Disadvantages**

- **Performance Issues:** May cause **performance problems** if you manage **too many inputs** (because of frequent re-renders).
- **More Code:** Requires **more boilerplate code** to manage state and event handlers.
- **Complexity:** Becomes **complex** when handling **large** and **multiple forms**.

**2️⃣ Uncontrolled Components**

- In **Uncontrolled Components**, the form input manages its own state using **ref (`useRef`)**, instead of React state.

- **Example**

```jsx
import React, { useRef } from "react";

function UncontrolledInput() {
  const inputRef = useRef(); // Reference to the input field

  const handleSubmit = () => {
    alert(`Typed Text: ${inputRef.current.value}`); // Directly access input value
  };

  return (
    <div>
      <input type="text" ref={inputRef} /> {/* controlled by ref */}
      <button onClick={handleSubmit}>Show Input</button>
    </div>
  );
}

export default UncontrolledInput;
```

- The input value is **not stored in React state**.
- We use `useRef()` to **directly access the input value** when needed.

**Advantages**

- **Better Performance:** No **re-renders** on input change, making it faster for **large forms**.
- **Simpler Code:** Less React code since the input **handles its own state**.
- **External Control:** Ideal for working with **third-party** components and **form libraries**.

**Disadvanatages**

- **Harder Validation:** Complex to perform **real-time** input validation.
- **Less Control:** React does **not track** input changes, making it harder to manage state centrally.
- **Inconsistent State:** Input values may go **out of sync** with React’s view if not handled carefully.

#### **When to Use What?**

- **Use Controlled Components** when:

  - You need **real-time updates** (e.g., live search).
  - You want **validation & error handling** in forms.

- **Use Uncontrolled Components** when:
  - You only need input value **on form submission**.
  - You are working with **third-party libraries** that manage their own state (e.g., file uploads).

[Go to top ↑](#index)

### **3. What is React.StrictMode & Why Use It?**

`React.StrictMode` is a special wrapper in React that helps identify potential issues in your code during development. It does not affect production but helps catch common mistakes early.

#### **Advantages**

✅ **Accidental Side Effects:**

- Helps catch cases where your code runs **extra times** by mistake (e.g., duplicate API calls).

✅ **Old & Unsafe Code:**

- Warns if you're using outdated React features that may break in future updates.

✅ **Forgetting to Clean Up Effects:**

- Detects cases where `useEffect` runs **unnecessarily** or causes memory leaks.

✅ **Finding Unexpected Behaviors:**

- Runs certain parts of your code **twice** in development to highlight hidden problems (but only in dev mode).

[Go to top ↑](#index)

### **4. What is Lazy Loading in React & `React.Suspense`**

Lazy loading means **loading a component only when needed**, instead of loading everything at once. This helps **reduce the initial load time** and improves performance.

#### **Example**

Imagine you are building an **e-commerce website** like **Amazon**.  
When a user **lands on the homepage**, they only need to see:

- Featured products
- Search bar
- Categories

But pages like **Order History, Cart, or Product Reviews** **aren’t needed immediately**.  
Using **Lazy Loading**, these pages load **only when the user clicks on them** instead of loading everything at once.

This makes the **homepage load super fast**, improving **user experience** and **performance**! 🚀

#### **🔹 What is `React.lazy()`?**

`React.lazy()` is a function that helps **dynamically import** components **only when required**. Instead of importing a component at the top of the file, it is **loaded when needed**.

✅ **Without Lazy Loading (Component loads immediately)**

```js
import MyComponent from "./MyComponent"; // Loaded immediately
```

❌ Even if the user **never** visits the page, this component is loaded.

✅ **With Lazy Loading (Component loads only when required)**

```js
import React, { lazy, Suspense } from "react";

const MyComponent = lazy(() => import("./MyComponent")); // Loaded only when needed
```

---

#### **🔹 What is `React.Suspense`?**

When using `lazy()`, React doesn’t **immediately** know what to display **while loading** the component.  
`React.Suspense` helps by showing a **fallback (like a loader or text or like a placeholder)** while waiting for the component to load.

✅ **Example of Lazy Loading with Suspense**

```js
import React, { lazy, Suspense } from "react";

const Profile = lazy(() => import("./Profile")); // Lazy loading

function App() {
  return (
    <div>
      <h1>My App</h1>
      <Suspense fallback={<h2>Loading Profile...</h2>}>
        <Profile /> {/* This loads only when needed */}
      </Suspense>
    </div>
  );
}

export default App;
```

⏳ **While `Profile` is loading, "Loading Profile..." is displayed.**  
🎯 **Once loaded, `Profile` is shown on the page.**

- Benefits of Lazy Loading & Suspense\*\*

  - **Faster Initial Load** – Loads only the necessary components.
  - **Improves Performance** – Reduces unnecessary resource usage.
  - **Better User Experience** – Only loads when required, avoiding long initial waits.

[Go to top ↑](#index)

### **5. What is React.Fragment?**

- `React.Fragment` is a built-in wrapper that allows grouping multiple JSX elements without adding extra HTML elements (like `<div>`).
- We can Use `<>...</>` as a shortcut for `<React.Fragment></React.Fragment>`

**🚀 Why use it?**

- **Avoids Extra `<div>`s**
- **Better Performance** – No unnecessary DOM nodes
- **Works in Tables** – Group `<tr>`s without breaking layout
- **✅ Example:**

```jsx
return (
  <>
    <h2>Hello</h2>
    <p>Welcome to React!</p>
  </>
);
```

[Go to top ↑](#index)

### **6. React Hooks & Their Types (with Examples)**

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

### **7. What is a Custom Hook in React?**

- A **Custom Hook** is a **reusable function** (_just like reusable component_) in React that lets you **share logic** between components.
- It’s a **JavaScript function** whose name **starts with `use`** (e.g., `useFetchData`, `useToggle`).
- It helps **avoid duplicate code** and **keep components clean** by separating logic.

#### **Why Use Custom Hooks?**

- To **reuse stateful logic** (like fetching data, form handling).
- To **organize complex components** by separating concerns.
- To **keep your code DRY** (_Don’t Repeat Yourself_).

#### **How to Create a Custom Hook?**

- **Step 1:** Name it starting with `use` (e.g., `useCounter`).
- **Step 2:** Write it as a **JavaScript function**.
- **Step 3:** You can use **React hooks** inside it (like `useState`, `useEffect`).
- **Step 4:** Your custom hook should return **state**, **functions**, or **values** that components need, such as fetched data, loading state, or error messages.

**Important**: They **do not** return JSX; they only return **data or functions**.

#### **Example: Custom Hook for Counter (`useCounter`)**

Creating Custom Hook:

```jsx
// Step 1: Create the custom hook
function useCounter(initialValue = 0) {
  const [count, setCount] = useState(initialValue);

  // Step 2: Define logic
  const increment = () => setCount(count + 1);
  const decrement = () => setCount(count - 1);

  // Step 3: Return the state and functions
  return { count, increment, decrement };
}
```

Using the Custom Hook in a Component

```jsx
import { useState } from "react";

function CounterComponent() {
  //Use custom hook just like built-in hooks
  const { count, increment, decrement } = useCounter(5);

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
}

export default CounterComponent;
```

[Go to top ↑](#index)

### **8. What is Microservices and Monolithic Architecture?**

#### **1. Microservices**:

- Microservices is a way of building software where an application is **split into small, independent services** that **work together**.

Each service:

- **Does one specific job** (like handling payments, user authentication, or notifications).
- **Runs separately** from other services, so if one part fails, the rest of the app keeps working.
- Can be **developed, deployed, and scaled** independently, making it easier to update or add new features.

For example, in an **e-commerce** site:

- One microservice handles **product listings**.
- Another manages **user accounts**.
- A different one processes **payments**.

This makes the system **more flexible, easier to maintain**, and **scalable** compared to traditional monolithic applications, where everything is tightly connected.

#### **2. Monolithic Architecture**

- Monolithic Architecture is a way of building software where **all parts of an application are combined into one big unit**.

In this structure:

- The **frontend, backend, and database** are all tightly connected.
- If one part fails or needs an update, **the entire application** might need to be rebuilt or redeployed.
- It's **harder to scale** because you can't separately grow just one part of the app.

For example, in an e-commerce site:

- **Product listings, user accounts, and payments** are all in one codebase.
- If you update the payment system, you must **re-deploy the whole application**.

While it’s **easier to develop and test** in the beginning, it becomes **hard to maintain and scale** as the app grows.

#### **Monolithic Architecture vs Microservices Architecture**

| **Aspect**          | **Monolithic Architecture**                         | **Microservices Architecture**                                                   |
| ------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------- |
| **Architecture**    | Single-tier architecture                            | Multi-tier architecture                                                          |
| **Size**            | Large, all components tightly coupled               | Small, loosely coupled components                                                |
| **Deployment**      | Deployed as a single unit                           | Individual services can be deployed independently                                |
| **Scalability**     | Horizontal scaling can be challenging               | Easier to scale horizontally                                                     |
| **Development**     | Simpler initially                                   | Complex due to managing multiple services                                        |
| **Technology**      | Limited technology choices                          | Freedom to choose the best technology for each service                           |
| **Fault Tolerance** | Entire application may fail if a part fails         | Individual services can fail without affecting others                            |
| **Maintenance**     | Easier to maintain due to its simplicity            | Requires more effort to manage multiple services                                 |
| **Flexibility**     | Less flexible as all components are tightly coupled | More flexible as components can be developed, deployed, and scaled independently |
| **Communication**   | Communication between components is faster          | Communication may be slower due to network calls                                 |

[Go to top ↑](#index)

### **9. What is React Router?**

- React Router is a library for **handling navigation** in React applications. It allows users to switch between pages **without a full page reload**, making the app **fast and dynamic**.

- **Latest Version Uses `createBrowserRouter()` Instead of `BrowserRouter`** which provides a **better API for defining routes, loaders, error handling, etc.**

  **Core Components of React Router**

1. **`createBrowserRouter()`** – Defines the route structure.
2. **`RouterProvider`** – Provides routing to the app.
3. **`Route Object`** – Defines paths, components, loaders, and error handlers.
4. **`Link`** – Used for navigation (instead of `<a>`).
5. **`NavLink`** – Similar to `Link`, but allows active styling.
6. **`Error Page Handling`** – `path: "*"`, `errorElement`, or `useRouteError()` to catch invalid pages.
7. **Dynamic Routes (`useParams()`)** - The `/profile/:username` route uses `useParams()` to get the dynamic value.
8. **`Outlet` for Nested Routes** - The `Outlet` component **renders child routes** inside `App.jsx`. This allows components like **Home, About, and Contact** to load inside `App`.

   - **`Outlet`** is like a **placeholder** in a parent component where the **child route components** will be rendered in nested routing.

**1️⃣ Install React Router**

```sh
npm install react-router-dom
```

**2️⃣ Create the Router (`main.jsx` or seprate file)**

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import { createBrowserRouter, RouterProvider } from "react-router-dom";
// Pages
import App from "./App";
import About from "./pages/About";
import Contact from "./pages/Contact";
import Home from "./pages/Home";
import NotFound from "./pages/NotFound";
import Profile from "./pages/Profile";

const router = createBrowserRouter([
  {
    path: "/",
    element: <App />, // Parent component
    children: [
      {
        path: "",
        element: <Home />,
      }, // Renders at "/"
      {
        path: "about",
        element: <About />,
      }, // "/about"
      {
        path: "contact",
        element: <Contact />,
      }, // "/contact"
      {
        path: "profile/:username",
        element: <Profile />,
      }, // Dynamic Route "/profile/:username"
    ],
    errorElement: <NotFound />, // Handles invalid routes
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <RouterProvider router={router} />
);
```

**3️⃣ Defining the Component with Navigations (NavBar.jsx)**

```jsx
import { Outlet, Link, NavLink } from "react-router-dom";

export default function App() {
  return (
    <div>
      <h1>My React Router App</h1>
      <nav>
        {/* Navigation using Link */}
        <Link to="/">Home</Link> |<NavLink to="/about" activeClassName="active">
          About
        </NavLink>
        <NavLink to="/contact" activeClassName="active">
          Contact
        </NavLink>
        <NavLink to="/profile/Arshit">Profile</NavLink>
      </nav>

      {/* Renders nested components */}
      <Outlet />
    </div>
  );
}
```

[Go to top ↑](#index)

### **10. What is Redux Toolkit (RTK)**

Redux Toolkit (RTK) is the **official, recommended way to write Redux logic**. It simplifies state management in React by providing a **faster, less boilerplate** approach.

**Main Components of Redux Toolkit**

- **`configureStore()`**

  - Creates the Redux store and automatically sets up good defaults like built-in middleware (`redux-thunk` for async actions) and Redux DevTools support.

- **`createSlice()`**

  - A function that combines **state, reducers, and actions** in one place, making Redux code more concise.

- **`Provider`**

  - A React component that wraps the entire app, allowing all components to access the Redux store.

- **`useSelector()`**

  - A React Hook that **selects and retrieves** specific data from the Redux store inside a component.

- **`useDispatch()`**

  - A React Hook that provides the `dispatch` function, allowing components to **trigger actions** to update the store.

- **`reducer`**

  - A function inside `createSlice()` that modifies the **state** based on the received **action**.

- **`actions`**

  - Auto-generated from `createSlice()`, these are functions that return action objects, which are dispatched to update the store.

- **`slice`**

  - A **module** in Redux that contains a specific part of the state, along with its reducers and actions. Created using `createSlice()`.

- **`createAsyncThunk()`**

  - A helper function for handling **async operations** like API calls. It manages three states: **pending, fulfilled, and rejected**.

- **`store`**

  - The **centralized state container** in Redux, holding all reducers and making state accessible throughout the app.

- **`dispatch`**
  - A function provided by Redux that **sends actions to reducers**, triggering state updates.

EXAMPLE (Counter)

**1️⃣ Install Redux Toolkit & React-Redux**
Run this command in your terminal:

```sh
npm install @reduxjs/toolkit react-redux
```

**2️⃣ Create an Empty Redux Store**

```jsx
import { configureStore } from "@reduxjs/toolkit";

// Creating an empty Redux store (No reducers added yet)
export const store = configureStore({
  reducer: {}, // Empty object (will add reducers later)
});
```

🔹 **Why?**

- First, we create an **empty store** so that our application is set up.
- We will **later add slices (reducers)** to manage state.

**3️⃣ Wrap App with Redux**

Modify `index.js` to **connect Redux to React**.

📝 **`index.js`**

```jsx
import React from "react";
import ReactDOM from "react-dom";
import { Provider } from "react-redux";
import { store } from "./app/store"; // Import store
import App from "./App";

ReactDOM.render(
  <Provider store={store}>
    {" "}
    {/* Wraps the app to give access to Redux */}
    <App />
  </Provider>,
  document.getElementById("root")
);
```

- `Provider` **connects Redux with React** and makes the store accessible to components.

  **4️⃣ Create a Slice**

Now, let's **create our first slice (counterSlice)**.

```jsx
import { createSlice } from "@reduxjs/toolkit";

// Step 1: Create a slice with name, initial state, and reducers
const counterSlice = createSlice({
  name: "counter", // Slice name
  initialState: { count: 0 }, // Initial state object
  reducers: {
    increment: (state) => {
      state.count += 1; // Increase count by 1
    },
    decrement: (state) => {
      state.count -= 1; // Decrease count by 1
    },
    reset: (state) => {
      state.count = 0; // Reset count to 0
    },
  },
});

// Step 2: Export the actions (to be used in components)
export const { increment, decrement, reset } = counterSlice.actions;

// Step 3: Export the reducer (to be added to store)
export default counterSlice.reducer;
```

- `createSlice()` creates a **Redux slice** with:
  - `initialState`: Defines the **starting state** `{ count: 0 }`
  - `reducers`: Functions that **modify the state**
- **Auto-generated actions** (`increment`, `decrement`, `reset`) allow **state updates**.

**IMPORTANT**

- **`counterSlice` is the slice** → It groups everything related to the counter (state, actions, reducers).
- **`increment`, `decrement`, `reset` from `counterSlice.actions` are actions** → They describe **what should happen** (but don’t modify the state themselves).
- **The functions inside `reducers: { ... }` are reducers** → They **actually modify the state** based on the dispatched action.

**5️⃣ Add Reducers to the Store**

Now, let's **add the counter slice** to our store.

```jsx
import { configureStore } from "@reduxjs/toolkit";
import counterReducer from "../features/counterSlice"; // Import reducer

// Creating store with reducers
export const store = configureStore({
  reducer: {
    counter: counterReducer, // Register the counter slice reducer
  },
});
```

- The store now **contains the `counterReducer`**, making it available in the app.

**6️⃣ Create a UI Component (`components/Counter.js`)**

Now, let’s **create the Counter component**.

```jsx
import React from "react";
import { useSelector, useDispatch } from "react-redux";
import { increment, decrement, reset } from "../features/counterSlice"; // Import actions

export default function Counter() {
  // Step 1: Get state from Redux store
  const count = useSelector((state) => state.counter.count);

  // Step 2: Get the dispatch function
  const dispatch = useDispatch();

  return (
    <div>
      <h2>Count: {count}</h2>

      {/* Dispatch actions on button click */}
      <button onClick={() => dispatch(increment())}>+</button>
      <button onClick={() => dispatch(decrement())}>-</button>
      <button onClick={() => dispatch(reset())}>Reset</button>
    </div>
  );
}
```

🔹 **What’s Happening?**

- `useSelector()`: Accesses the **count** value from Redux state.
- `useDispatch()`: Sends **actions** (`increment`, `decrement`, `reset`) to update the store.

  **7️⃣ Use `Counter` Component in `App.js`**

Finally, modify `App.js` to include the `Counter` component.

```jsx
import React from "react";
import Counter from "./components/Counter"; // Import Counter component

function App() {
  return (
    <div>
      <h1>Redux Toolkit Counter</h1>
      <Counter />
    </div>
  );
}

export default App;
```

** Summary**

1️⃣ Install Redux Toolkit.  
2️⃣ **Create an empty store.**  
3️⃣ **Wrap the app with `Provider`.**  
4️⃣ **Create a slice (`counterSlice`).**  
5️⃣ **Add reducers to the store.**  
6️⃣ **Create a `Counter` component.**  
7️⃣ **Use `Counter` in `App.js`.**

[Go to top ↑](#index)

### **11. What are Higher Order Component (HOC) in React**

- A **Higher Order Component (HOC)** is a **function** that takes a component as input and returns a new enhanced component. It is used for **code reusability** and **adding extra functionality** without modifying the original component.

**Example**

**1️⃣ Create a Simple Component (Wrapped Component)**

- Let's say we have a basic component that displays a message:

```jsx
import React from "react";

function Message({ text }) {
  return <h2>Hi, {text}</h2>;
}

export default Message;
```

**2️⃣ Create the Higher Order Component (HOC)**

- A HOC is just a function that **takes a component as input and returns a new component** with added functionality.

```jsx
import React from "react";

function withBorder(WrappedComponent) {
  return function EnhancedComponent(props) {
    return (
      <div style={{ border: "2px solid red", padding: "10px" }}>
        <WrappedComponent {...props} />
      </div>
    );
  };
}

export default withBorder;
```

- `withBorder` is our HOC function.
- It **takes a component (`WrappedComponent`) as input**.
- It **returns a new component (`EnhancedComponent`)** that wraps `WrappedComponent` inside a `div` with a red border.

**3️⃣ Use the HOC to Enhance the Component**

- Now, we apply `withBorder` to the `Message` component.

```jsx
import Message from "./Message";
import withBorder from "./withBorder";

const EnhancedMessage = withBorder(Message);

function App() {
  return <EnhancedMessage text="Arshit" />;
}

export default App;
```

- `withBorder(Message)` creates a new component (`EnhancedMessage`) that adds a border to `Message`.
- `App` renders `EnhancedMessage` with the text **"Hello, I'm an HOC!"**.

- The message **"Hi, Arshit"** appears inside a box with a **red border**.

** When to Use HOCs?**

- **Reusing logic** (e.g., authentication, logging, styling).
- **Adding functionality** (e.g., adding a loader, tracking user actions).

**Example Use Cases:**

1. `withAuth(Component)` → Only show a component if the user is logged in.
2. `withLoading(Component)` → Show a **loading spinner** before displaying data.

[Go to top ↑](#index)
