# JavaScript Basics: Interview Preparation and Cheat Sheet

## **Topics Covered**

1. [Variables and Constants](#1-variables-and-constants)
2. [Data Types](#2-data-types)
3. [Operators](#3-operators)
4. [Conditional Statements](#4-conditional-statements)
5. [Loops](#5-loops)
6. [Functions](#6-functions)
7. [Scope](#7-scope)
8. [Hoisting](#8-hoisting)

---



## **1. Variables and Constants**

JavaScript provides three ways to declare variables: `var`, `let`, and `const`.

| **Declaration** | **Scope** | **Reassignment** | **Hoisting Behavior**           |
| --------------- | --------- | ---------------- | ------------------------------- |
| `var`           | Function  | Allowed          | Hoisted but **undefined**       |
| `let`           | Block     | Allowed          | Hoisted but **not initialized** |
| `const`         | Block     | Not Allowed      | Hoisted but **not initialized** |

**Example:**

```javascript
var globalVar = "Global"; // Function-scoped
let blockVar = "Block"; // Block-scoped
const constantVar = "Constant"; // Cannot be reassigned
```

---

## **2. Data Types**

### **Primitive Data Types** (immutable values stored in memory):

The predefined data types provided by JavaScript language are known as primitive data type. Primitive data types are also known as in-built data types.

- **String**: `"Hello"`
- **Number**: `42`
- **Boolean**: `true` / `false`
- **Undefined**: Unassigned variable (`let x;`)
- **Null**: Explicitly empty (`let x = null;`)
- **Symbol**: Unique identifier (`let sym = Symbol('id');`)
- **BigInt**: Large integers (`let big = 123n;`)

### **Non-Primitive Data Types** (mutable and stored by reference):

The data types that are derived from primitive data types are known as non-primitive data types. It is also known as derived data types or reference data types.

- **Object**: Collection of key-value pairs (`let obj = { key: "value" };`)
- **Array**: Ordered list of values (`let arr = [1, 2, 3];`)
- **Function**: Executable block of code (`function add(a, b) { return a + b; }`)

---

## **3. Operators**

### **Arithmetic Operators**

`+`, `-`, `*`, `/`, `%`, `++`, `--`

**Example:**

```javascript
let a = 5,
  b = 10;
console.log(a + b); // 15
console.log(b % a); // 0
```

### **Comparison Operators**

- **Loose equality (`==`)**: Compares values, allowing type coercion.
- **Strict equality (`===`)**: Compares both value and type.

**Example:**

```javascript
console.log(5 == "5"); // true
console.log(5 === "5"); // false
```

### **Logical Operators**

- **AND (`&&`)**: Returns true if both operands are true.
- **OR (`||`)**: Returns true if at least one operand is true.
- **NOT (`!`)**: Negates the operand.

---

## **4. Conditional Statements**

### **if-else**

```javascript
if (score > 80) {
  console.log("Excellent");
} else {
  console.log("Keep trying");
}
```

### **switch**

```javascript
switch (grade) {
  case "A":
    console.log("Excellent");
    break;
  case "B":
    console.log("Good");
    break;
  default:
    console.log("Needs Improvement");
}
```

---

## **5. Loops**

### **for loop**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### **while loop**

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### **do-while loop**

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

---

## **6. Functions**

### **Function Declaration**

```javascript
function add(a, b) {
  return a + b;
}
```

### **Function Expression**

```javascript
const multiply = function (a, b) {
  return a * b;
};
```

### **Arrow Function**

```javascript
const subtract = (a, b) => a - b;
```

### **Key Points:**

- Use **declarations** when defining reusable functions.
- Use **expressions** or **arrow functions** for concise inline code.

---

## **7. Scope**

| **Scope Type** | **Access Area**                 | **Keyword Used** |
| -------------- | ------------------------------- | ---------------- |
| **Global**     | Entire program                  | `var` or `let`   |
| **Function**   | Only within a specific function | `var`            |
| **Block**      | Inside `{}` of a block or loop  | `let`, `const`   |

**Example:**

```javascript
let x = 10; // Global scope

function testScope() {
  var y = 20; // Function scope
  if (true) {
    let z = 30; // Block scope
    console.log(z);
  }
}
```

---

## **8. Hoisting**

**Definition:**  
Hoisting is JavaScript's behavior of moving declarations to the top of the current scope.

### **Hoisting with `var`**

Variables declared with `var` are hoisted but not initialized.

```javascript
console.log(x); // undefined
var x = 10;
```

### **Hoisting with `let`/`const`**

Variables declared with `let` or `const` are hoisted but cannot be accessed before initialization (Temporal Dead Zone).

```javascript
console.log(y); // ReferenceError
let y = 20;
```

---

## **Cheat Sheet Summary**

### **Common Interview Questions**

1. Define JavaScript and explain its key features.
2. How does hoisting work in JavaScript?
3. Explain the difference between `let`, `var`, and `const`.
4. What are the different types of functions in JavaScript?
5. Explain `==` vs `===`.
6. Demonstrate the difference between global and block scope.

This guide should help you prepare effectively for JavaScript interviews! 🚀
