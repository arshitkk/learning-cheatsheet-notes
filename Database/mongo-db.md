# **Index**

## **1. [What is MongoDB?](#1-what-is-mongodb-1)**

## **2. [Mongo DB Setup](#2-mongo-db-setup-1)**

1. **[MongoDB Atlas Setup & Connection Guide](#1-mongodb-atlas-setup--connection-guide)**
2. **[MongoDB Compass Setup](#2-mongodb-compass-setup)**
3. **[Connecting to the Database Server](#3-connecting-to-the-database-server)**

## **3. [MongoDB Core Concepts & Operations](#3-mongodb-core-concepts--operations-1)**

1. **[ Introduction to CRUD Operations in MongoDB](#1-introduction-to-crud-operations-in-mongodb)**

## **4. [Mongoose - Library](#4-mongoose---library)**

1. **[What is Mongoose? Why we use it?](#1-what-is-mongoose-why-we-use-it)**
2. **[How to Install, Configure, and Use Mongoose](#2-how-to-install-configure-and-use-mongoose)**
   ``
3. **[What is **Schema** and **Model** in Mongoose?](#3-what-is-schema-and-model-in-mongoose)**
4. **[What is `express.json()` in Express.js](#4-what-is-expressjson-in-expressjs)**
5. **[Creating Sign-up api and creating documents](#5-creating-sign-up-api-and-creating-documents)**
6. **[Reading/Fetching users uisng few methods](#6-readingfetching-users-uisng-few-methods)**
7. **[Update/Patch, and Delete a document](#7-updatepatch-and-delete-a-document)**
8. **[Mongoose Schema Types & Options. How to give Custom error.](#8-mongoose-schema-types--options-how-to-give-custom-error)**
9. **[Mongoose Schema Validations](#9-mongoose-schema-validations)**
10. **[API-Level Validation in Express.js](#10-api-level-validation-in-expressjs)**
11. **[Validator.js Library (NPM)](#11-validatorjs-library-npm)**
12. **[What is `bcrypt` npm Library and why do we need?](#12-what-is-bcrypt-npm-library-and-why-do-we-need)**

# **1. What is MongoDB?**

**MongoDB** is a **NoSQL database**.  
Instead of **tables** and **rows** (like SQL databases), MongoDB stores data in **collections** and **documents**.

- **NoSQL** means "**Not Only SQL**" (_much more than that_)
- It stores data in a **flexible**, **JSON-like** format called **BSON** (Binary JSON).
- These databases are designed to handle **large volumes of unstructured or semi-structured data**.
- Unlike **Relational Databases (RDBMS)**, NoSQL databases do **not require fixed schemas** or complex **JOIN** operations.

## **SQL vs MongoDB Structure Comparison**

| **SQL (Relational Database)** | **MongoDB (NoSQL Database)** |
| ----------------------------- | ---------------------------- |
| Database                      | Database                     |
| Table                         | Collection                   |
| Row                           | Document                     |
| Column                        | Field                        |

### **Example**

**SQL Table**

| id  | name   | email           |
| --- | ------ | --------------- |
| 1   | Arshit | arshit@mail.com |
| 2   | John   | john@mail.com   |

**MongoDB Document (JSON-like)**

```json
{
  "_id": 1,
  "name": "Arshit",
  "email": "arshit@mail.com"
}
```

- This is a **document** inside a **collection** in MongoDB.
- Each document is like **one row** in SQL.

## **Why Use MongoDB?**

1. **Flexible** – no strict table structure.
2. **Scales easily** – works great with large datasets.
3. **Document-oriented** – works like JSON (easy for developers!).
4. **Faster for unstructured data** than traditional SQL.

## **When to Use MongoDB?**

- You have **dynamic data**.
- You want **fast development** (no complex table design).
- You’re building **modern web apps** (Node.js + MongoDB is a common combo).

[Go to top ↑](#index)

---

# **2. Mongo DB Setup**

## **1. MongoDB Atlas Setup & Connection Guide**

### **1. Create MongoDB Atlas Account & Cluster**

- Visit [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
- Sign up/log in → Go to **Atlas Dashboard**.
- Click **Create New Cluster** → Select **M0 Free Tier**.
- Pick a cloud provider (AWS/GCP/Azure) & region → **Create Cluster**.
  > _Cluster creation may take a few minutes._

### **2. Create Database User**

- Go to **Database Access** → **Add New Database User**.
- Enter **Username** & **Password**.
- Role: **Read and write to any database** → **Add User**.

### **3. Set Network Access**

- Go to **Network Access** → **Add IP Address**.
- Choose **Allow access from anywhere** (or specify your IP).
- Click **Confirm**.

### **4. Get Connection String**

- Go to **Clusters** → **Connect** → **Connect your application**.
- Copy the connection string:
  ```bash
  mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority
  ```
  Replace `<username>`, `<password>`, and `<dbname>`.

[Go to top ↑](#index)

## **2. MongoDB Compass Setup**

### **1. Install MongoDB Compass**

- Download from [here](https://www.mongodb.com/products/compass) & install.

### **2. Connect MongoDB Compass**

- Open Compass → Paste connection string.
- Enter your **password** → Click **Connect**.

[Go to top ↑](#index)

## **3. Connecting to the Database Server**

To connect to a MongoDB, first install the MongoDB Node.js driver:

```bash
npm install mongodb
```

Database Connection

```javascript
const { MongoClient } = require("mongodb");
// Connection URL
const url = "mongodb://localhost:27017";
const client = new MongoClient(url);

// Database Name
const dbName = "Namaste-Nodejs";

async function main() {
  await client.connect();
  console.log("Connected successfully to server");
  const db = client.db(dbName);
  const collection = db.collection("User");

  return "done.";
}
main()
  .then(console.log)
  .catch(console.error)
  .finally(() => client.close());
```

[Go to top ↑](#index)

---

# **3. MongoDB Core Concepts & Operations**

## **1 Introduction to CRUD Operations in MongoDB**

**CRUD** refers to the four basic operations you can perform on data in a database:

- **Create**
- **Read**
- **Update**
- **Delete**

While these are the core operations, MongoDB also provides **many other powerful operations** like aggregation, indexing, and transactions,
Here, we will focus on the **essential CRUD** actions.

### **1. Create**

- **Definition**: Adds new documents to a MongoDB collection.
- **Purpose**: To insert new data records into your database.
- **Common Use Cases**: Adding a user, creating a product listing, or saving form data.

**Example:**

```javascript
const data = {
  firstname: "Arshit",
  lastname: "Kumar",
  city: "Jammu",
  phoneNumber: "88526587",
};

// Create
const insertData = await collection.insertMany([data]);
console.log("Data inserted => ", insertData);
```

### **2. Read**

- **Definition**: Retrieves documents from a MongoDB collection.
- **Purpose**: To fetch or query data from the database.
- **Common Use Cases**: Showing user profiles, displaying product lists, or running reports.

**Example:**

```javascript
// Read
const findData = await collection.find({}).toArray();
console.log("All data =>", findData);
```

### **3. Update**

- **Definition**: Modifies existing documents in a MongoDB collection.
- **Purpose**: To change or update specific fields within a document.
- **Common Use Cases**: Updating user details, modifying an order status, or adjusting product prices.

**Example:**

```javascript
// Update
const updateData = await collection.updateOne(
  { _id: new ObjectId("67066d6a3be8f41630d5dae4") },
  { $set: { firstname: "Mint" } }
);
console.log("Updated document =>", updateData);
```

### **4. Delete**

- **Definition**: Removes documents from a MongoDB collection.
- **Purpose**: To delete records that are no longer needed.
- **Common Use Cases**: Removing inactive users, deleting expired deals, or cleaning up old logs.

**Example:**

```javascript
// Delete
const deleteData = await collection.deleteOne({
  _id: new ObjectId("670668562c6bd11e25050c13"),
});
console.log("Deleted data =>", deleteData);
```

### **Summary of CRUD Operations**

| Operation | Description                                 | Common Use Cases              |
| --------- | ------------------------------------------- | ----------------------------- |
| Create    | Adds new documents to a collection          | Adding new user profiles      |
| Read      | Retrieves documents from a collection       | Displaying user details       |
| Update    | Modifies existing documents in a collection | Updating account info         |
| Delete    | Removes documents from a collection         | Deleting old or inactive data |

[Go to top ↑](#index)

---

# **4. Mongoose - Library**

## **1. What is Mongoose? Why we use it?**

**Mongoose** is an **Object Data Modeling (ODM - _maps objects in code to documents in NoSQL databases._) library** for **MongoDB** and **Node.js**.  
It helps you **interact with MongoDB** databases **easily and safely**, by providing **a structured and organized way** to work with data.

### Why Do We Use **Mongoose** with MongoDB?

#### Without Mongoose (Using **MongoDB Native Driver**):

- You **directly interact** with MongoDB.
- You need to **manually write queries**, **validate data**, and **handle schemas**.
- There's **no structure**; MongoDB allows **anything to be stored** inside documents.
- It’s **easy to make mistakes**, like saving the wrong data types (e.g., storing a number in an "email" field).

**Example:**

```js
const { MongoClient } = require("mongodb");

const client = new MongoClient("mongodb://localhost:27017");
await client.connect();

const db = client.db("testdb");
const usersCollection = db.collection("users");

// Insert a user without validation
await usersCollection.insertOne({ name: "John", age: "not-a-number" });
```

- You have **no predefined structure**.
- You manually handle:
  - **Validation** (checking if fields exist, types are correct)
  - **Relationships** (referencing other data)
  - **Default values**
  - **Middleware** (logic before/after saving data)
- More **boilerplate code** (repetitive tasks)
- More room for **bugs and errors**.
  t

#### With **Mongoose**:

- You **define a schema** (rules) for your data, like "name must be a string", "age must be a number".
- It **validates data automatically** (_checks if the data follows the rules you defined in the schema_) before saving to the database.
- You get **powerful features** like **middleware**, **hooks**, **query helpers**, and **virtuals**.
- Code becomes **clean**, **safe**, and **predictable**.
- It works as a **layer** between your code and MongoDB.

**Example:**

```js
const mongoose = require("mongoose");

mongoose.connect("mongodb://localhost:27017/testdb");

const userSchema = new mongoose.Schema({
  name: String,
  age: Number,
});

const User = mongoose.model("User", userSchema);

// This will validate the data before saving
await User.create({ name: "John", age: 25 });
```

- Enforces **data consistency**.
- Reduces **human error**.
- Provides a **clean API** to interact with MongoDB.
- Speeds up **development** with **built-in features**.
- Makes managing **complex relationships** easier.

[Go to top ↑](#index)

## **2. How to Install, Configure, and Use Mongoose**

### **Install Mongoose**

```bash
npm install mongoose
```

### **Basic Mongoose Setup & Connection**

In your `index.js` or `app.js` file:

```javascript
const express = require("express");
const mongoose = require("mongoose");

const app = express();

// Connect to MongoDB using Mongoose
const connectDB = async () => {
  await mongoose.connect("mongodb://localhost:27017/nameOfTheDatabase");
};

connectDB
  .then(() => {
    console.log("Connected to MongoDB!");
    // Start the server **after** DB is connected!
    app.listen(3000, () => {
      console.log("Server is running on port 3000");
    });
  })
  .catch((error) => {
    console.error("MongoDB connection error:", error);
  });
```

### **Why Should You Connect to DB First, Then Start Server?**

Your **Express app** may depend on the **database** for important operations (like fetching users, products, etc.).  
If you start your server (`app.listen()`) **before the DB connects**, and a request comes in that needs the DB, it will **fail** because there’s no DB connection.

**Example Problem**

- User hits `/users` route → Server tries to query MongoDB → DB isn’t connected → **Error occurs.**
- _It’s like **checking the fuel in a car before starting the engine**._

**Safe Practice:**

- **First, ensure DB is connected.**
- **Then, start listening for requests.**

[Go to top ↑](#index)

## **3. What is **Schema** and **Model** in Mongoose?**

### **Schema?**

- A **Schema** defines the **structure** of the **documents** in a MongoDB **collection**.
- It describes **what fields** your documents should have and what **type** of data each field should store.

Think of **Schema** as a **blueprint** or **template** for your data.

**Example**

Imagine you're making **ID cards**.

- Schema tells you:
  - Name must be **text**
  - Age must be **a number**
  - Photo is an **image link**

### **Model?**

- A **Model** is like a **constructor function** or **class** created from the schema.
- It’s used to **create**, **read**, **update**, and **delete** (CRUD) **documents** in the **collection**.

**Example**

- Schema = Design/Blueprint/template for ID cards
- Model = ID Card **Factory** that makes ID cards based on the schema
- Document = A **specific ID card** created by the factory

### **How to Define Schema and Model in Mongoose?**

**Step 1: Require Mongoose**

```javascript
const mongoose = require("mongoose");
```

**Step 2: Define a Schema**

**Example: A **User Schema** with `name`, `email`, and `age`.**

```javascript
const userSchema = new mongoose.Schema({
  name: {
    type: String,
    required: true, // This field must be filled
  },
  email: {
    type: String,
    required: true,
    unique: true, // Email should be unique
  },
  age: {
    type: Number,
  },
});
```

**Step 3: Create a Model from Schema**

This model will interact with the **"users"** collection in MongoDB.

```javascript
const User = mongoose.model("User", userSchema);
```

`"User"` is the name of the model;

- Mongoose automatically creates a collection name based on that:

  -`"User"` becomes `users` (lowercase + plural).

[Go to top ↑](#index)

## **4. What is `express.json()` in Express.js**

`express.json()` is a **built-in middleware** in Express.js that **parses incoming JSON data** in HTTP request bodies.

### **Why Do We Need `express.json()`?**

1. **Handles JSON Data:** When a client (like a frontend app) sends a `POST` or `PUT` request with JSON data, Express **doesn’t understand it by default**.
2. **Parses `req.body`:** Without `express.json()`, `req.body` will be `undefined`.
3. **Makes Data Usable:** Converts JSON into a JavaScript object, making it easy to work with in routes.

### **How Does It Work?**

- `express.json()` **reads the request body**, detects JSON format, and converts it into a JavaScript object before passing it to route handlers.

**Example Without `express.json()` (Problem)**

```javascript
const express = require("express");
const app = express();

app.post("/data", (req, res) => {
  console.log(req.body); // ❌ Output: undefined
  res.send("Data received");
});

app.listen(3000, () => console.log("Server running on port 3000"));
```

- **Issue:** `req.body` will be `undefined` because Express **does not parse JSON automatically**.

**Example With `express.json()` (Solution)**

```javascript
const express = require("express");
const app = express();

app.use(express.json()); // Enables JSON parsing

app.post("/data", (req, res) => {
  console.log(req.body); // Output: { name: "Arshit", age: 23 }
  res.send("Data received successfully!");
});

app.listen(3000, () => console.log("Server running on port 3000"));
```

1. `app.use(express.json())` enables JSON parsing.
2. Client sends JSON data in a `POST` request:
   ```json
   { "name": "Arshit", "age": 23 }
   ```
3. Express converts JSON into a **JavaScript object** and stores it in `req.body`.
4. We can access it like a normal object: `req.body.name` → `"Arshit"`

[Go to top ↑](#index)

## **5. Creating Sign-up api and creating documents**

1. Created an **Express app**
2. Connected to **MongoDB** with `connectDB()`
3. Imported the `User` **Model**
4. Two Methods:
   - **Hardcoded data**
   - **Dynamic data using `req.body`**
5. Saved the document to **MongoDB**

### **Example 1 - Hardcoded Values**

_It is just for learning purpose, this is most dumbass way to add values_

```javascript
const express = require("express");
const app = express();
const connectDB = require("./db/config");
const User = require("./models/users");

// Test route
app.get("/", (req, res) => {
  res.send("Welcome to the app");
});

// Hardcoded Signup Route
app.post("/sign-up", async (req, res) => {
  // Creating a hardcoded user
  const user = new User({
    name: "Arshit Kumar", // Hardcoded Name
    email: "arshit@gmail.com", // Hardcoded Email
    password: "arshit@123", // Hardcoded Password
  });

  try {
    await user.save(); // Save the user in MongoDB
    res.send("User added successfully"); // Success response
  } catch (error) {
    res.status(500).send(error.message); // Error response
  }
});

// Connect to MongoDB first, then run the server
connectDB().then(() => {
  console.log("MongoDB is Connected");

  app.listen(3000, () => {
    console.log("listening on port 3000");
  });
});
```

1. You give the **`POST` request** by **visiting `/sign-up`** using Postman(_if testing_).
2. It **creates a new user** with **hardcoded values**:
   - `name`: "Arshit Kumar"
   - `email`: "arshit@gmail.com"
   - `password`: "arshit@123"
3. `user.save()` saves the **document** to your **MongoDB collection**.
4. It returns:  
   ✅ `"User added successfully"`  
   ❌ If there’s an error, it gives a **500 error** with `error.message`.

### **Example 2- Dynamic Values (_Using `req.body`_)**

- Instead of hardcoded values, we **accept user input dynamically** using `req.body`.
- Requires **Postman** or a client app to send data.

```javascript
const express = require("express");
const app = express();
const connectDB = require("./db/config");
const User = require("./models/users");

// Enable JSON parsing for request bodies - IMPORTANT
app.use(express.json());

app.get("/", (req, res) => {
  res.send("Welcome to the app");
});

// Dynamic Signup Route
app.post("/sign-up", async (req, res) => {
  const user = new User(req.body); // Taking data from req.body
  try {
    await user.save(); // Save user in MongoDB
    res.send("User added successfully");
  } catch (error) {
    res.status(500).send(error.message);
  }
});

// Connect to DB before starting the server
connectDB().then(() => {
  console.log("MongoDB is Connected");
  app.listen(3000, () => {
    console.log("listening on port 3000");
  });
});
```

[Go to top ↑](#index)

## **6. Reading/Fetching users uisng few methods**

### **1. `/getUsers` - Find Users with Filters & Projection**

```javascript
app.get("/getUsers", async (req, res) => {
  const user = await User.find({ name: "Arshit Kumar" }, "email name", {
    limit: 1,
  });
  res.send(user);
});
```

- **Finds all users** with `name: "Arshit Kumar"`.
- **Only selects** the `email` and `name` fields (projection).
- **Limits** results to `1 user`.

### **2.`/getOneUsers` - Find One User**

```javascript
app.get("/getOneUsers", async (req, res) => {
  const user = await User.findOne({ name: "Arshit Kumar" }, "email name");
  res.send(user);
});
```

- **Finds the first matching user** where `name` is `"Arshit Kumar"`.
- **Returns only one document** (unlike `find()` which returns an array).
- **Selects only `email` and `name`**.

### **3.`/getAllUsers` - Get All Users**

```javascript
app.get("/getAllUsers", async (req, res) => {
  const user = await User.find({});
  res.send(user);
});
```

- **Finds all users** in the `users` collection.
- **Returns the entire document** (no filters or projections).

### **Conclusion**

- **`find({})`** → Returns all documents (array).
- **`find({ filter })`** → Returns filtered documents (array).
- **`findOne({ filter })`** → Returns only the first matching document.

### **For more method Visit** - **[Link](https://mongoosejs.com/docs/api/model.html)**

[Go to top ↑](#index)

## **7. Update/Patch, and Delete a document**

### **1. Updating (`PATCH` and `PUT`)**

**PATCH**

```javascript
app.patch("/update", async (req, res) => {
  const detail = req.body.id;
  const user = await User.findByIdAndUpdate(detail, req.body, {
    returnDocument: "after",
  });
  console.log(user);
  res.send("patch applied");
});
```

- **Updates only the fields sent in `req.body`**
- **Does not override the entire document**
- **Uses `returnDocument: "after"`** (returns the updated document)

**PUT (Full Update)**

```javascript
app.put("/update", async (req, res) => {
  const detail = req.body.id;
  const user = await User.findByIdAndUpdate(detail, req.body, {
    returnDocument: "after",
    overwrite: true, // Fully replaces the document
  });
  console.log(user);
  res.send("put applied");
});
```

- **Replaces the entire document**
- **If a field is missing in `req.body`, it will be deleted (_as we have used `overwrite : true`_)**

### **2. Deleting Data (`DELETE`)**

```javascript
app.delete("/delete", async (req, res) => {
  const detail = req.body.id;
  try {
    const user = await User.findByIdAndDelete(detail);
    if (user == null) {
      res.status(404).send("not found the user to delete ");
    } else {
      res.send("deleted succesfully");
    }
  } catch (error) {
    res.status(401).send("not found the user to delete");
  }
});
```

- **Deletes a user based on `id`**
- **If the user doesn't exist, it returns a `404` error**
- **If the deletion is successful, it sends `"deleted successfully"`**

### **Difference Between `PUT` and `PATCH`**

| Feature                      | `PUT` (Full Update)                                                                                         | `PATCH` (Partial Update)             |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| **Purpose**                  | Replaces the whole document (_only if you use `overwrite: true,` otherwise they both will behave the same_) | Updates only specific fields         |
| **Effect on Missing Fields** | Deletes missing fields                                                                                      | Leaves missing fields unchanged      |
| **Use Case**                 | When you want to replace an entire document                                                                 | When you want to update a few fields |

### **Difference Between `findOneAndUpdate()` and `findByIdAndUpdate()`**

- **Use `findOneAndUpdate()`** when searching by fields like `email` or `name`.
- **Use `findByIdAndUpdate()`** when updating a document by `_id`.

[Go to top ↑](#index)

## **8. Mongoose Schema Types & Options. How to give Custom error.**

### **1. Basic Data Types**

These types store simple, primitive values. They are used for text, numbers, booleans, and dates.

- **String:** Stores text data (e.g., names, emails).
- **Number:** Stores numeric values (e.g., age, quantity).
- **Boolean:** Stores true/false values.
- **Date:** Stores date and time values.

**Example:**

```javascript
const userSchema = new mongoose.Schema({
  // Stores text (e.g., "Arshit Kumar")
  name: { type: String },

  // Stores numbers (e.g., 25)
  age: { type: Number },

  // Stores boolean values (e.g., true)
  isActive: { type: Boolean },

  // Stores date and time (e.g., new Date())
  createdAt: { type: Date },
});
```

### **2. Complex Data Types**

They Used for storing more flexible or compound data. They handle arrays, mixed data structures, or restrict values with enums.

- **Array:** Holds multiple values of a specified type.
- **Mixed:** Allows any data type (useful when structure isn’t fixed).
- **Enum:** Restricts the field to one value from a predefined list.

**Example:**

```javascript
const userSchema = new mongoose.Schema({
  // Stores an array of strings (e.g., ["coding", "music", "reading"])
  hobbies: { type: [String] },

  // Allows storage of any type of data (flexible structure)
  metadata: { type: mongoose.Schema.Types.Mixed },

  // Restricts role to only "admin", "user", or "guest"
  role: { type: String, enum: ["admin", "user", "guest"] },
});
```

---

### **3. Relational Types**

They Used for creating relationships between documents in different collections. They store MongoDB ObjectIds that reference other documents.

- **ObjectId:** Represents a unique identifier for a MongoDB document.
- **ref:** Associates the ObjectId with a specific collection/model.

**Example:**

```javascript
const postSchema = new mongoose.Schema({
  // Links to a document in the "User" collection by storing its ObjectId
  userId: { type: mongoose.Schema.Types.ObjectId, ref: "User" },
});
```

### **4. Schema Options**

Options that modify the behavior of a field within a schema. They help transform data automatically or set default values, and even automatically manage common fields like timestamps.

- **default:** Automatically sets a value if none is provided.
- **trim:** Removes leading and trailing whitespace from a string.
- **lowercase:** Converts a string to lowercase before saving.
- **uppercase:** Converts a string to uppercase before saving.
- **timestamps:** Automatically adds and updates the `createdAt` and `updatedAt` fields.

**Example:**

```javascript
const userSchema = new mongoose.Schema(
  {
    // Automatically converts the email to lowercase and trims extra spaces
    email: {
      type: String,
      lowercase: true, // Converts "USER@Example.COM" to "user@example.com"
      trim: true, // Removes extra whitespace
    },

    // Sets the default status to "pending" if no value is provided
    status: {
      type: String,
      default: "pending",
    },

    // Converts the username to uppercase automatically
    username: {
      type: String,
      uppercase: true, // Converts "arshit" to "ARSHIT"
    },
  },
  {
    // Automatically manages createdAt and updatedAt fields
    timestamps: true,
  }
);
```

- **timestamps Option:**
  - **createdAt:** Automatically set when the document is created.
  - **updatedAt:** Automatically updated every time the document is modified.

**Additional Note:**

- You can manually define and set `createdAt` and `updatedAt` fields in your schema if needed. However, this is not recommended because the built-in `timestamps` option handles these fields automatically and reliably. Manual management may lead to inconsistencies or additional boilerplate code.

### **Summary of Categories:**

- **Basic Data Types:**
  - Store primitive values like strings, numbers, booleans, and dates.
- **Complex Data Types:**

  - Handle arrays, flexible data structures (Mixed), and enforce value restrictions (Enum).

- **Relational Types:**

  - Create relationships by storing references (ObjectId) to documents in other collections.

- **Schema Options:**
  - Modify field behavior with default values, automatic case conversion, and trimming of strings or adding timestamps etc.

### **Custom error message**

If you want to add a **custom error message**, just add `, message: "Your custom error message"` inside the validation object.

- **For `required` validation:**

```javascript
name: { type: String, required: [true, "Name cannot be empty!"] }
```

- **For `minlength` validation:**

```javascript
username: { type: String, minlength: [3, "Username must have at least 3 characters!"] }
```

- **For `max` validation:**

```javascript
age: { type: Number, max: [60, "Age cannot exceed 60!"] }
```

- **For `enum` validation:**

```javascript
role: { type: String, enum: { values: ["admin", "user"], message: "Invalid role! Choose 'admin' or 'user'." } }
```

- **For `match` validation (Regex):**

```javascript
email: { type: String, match: [/^\S+@\S+\.\S+$/, "Invalid email format!"] }
```

- **For custom function validation:**

```javascript
age: {
    type: Number,
    validate: {
      validator: (n) => {
        return n >= 18; // only allow above 18
      },
      message: (n) => "Abey chhotu chal nikal " + n.value + " saal ka hai tu",
    },
  },
```

[Go to top ↑](#index)

## **9. Mongoose Schema Validations**

Mongoose provides various validation options to ensure data integrity. These validation rules apply at the **schema level** and prevent invalid data from being stored in MongoDB.

### **1. Required Validation** (Ensures a field is mandatory)

Ensures that a field **must have a value**; otherwise, an error is thrown.

```javascript
const userSchema = new mongoose.Schema({
  name: { type: String, required: true }, // Name is mandatory
});
```

### **2. Default Value** (Sets a default value if none is provided)

If no value is provided for a field, Mongoose automatically assigns a **default value**.

```javascript
const userSchema = new mongoose.Schema({
  status: { type: String, default: "pending" },
});
```

- **If no value is provided:** `{ status: "pending" }` (automatically assigned)

### **3. Enum Validation** (Restricts values to a predefined set)

Restricts a field to **only specific values**. If an invalid value is provided, an error is thrown.

```javascript
const userSchema = new mongoose.Schema({
  role: { type: String, enum: ["admin", "user", "guest"] },
});
```

✔ **Valid Inputs:** `{ role: "admin" }`, `{ role: "user" }`  
❌ **Invalid Input:** `{ role: "manager" }` → `"Error: role must be 'admin', 'user', or 'guest'"`

### **4. Unique Validation** (Ensures no duplicate values)

Ensures that no **duplicate** values exist for a field in the database.

```javascript
const userSchema = new mongoose.Schema({
  email: { type: String, unique: true },
});
```

### **5. Min & Max Validation (For Numbers)** (Limits numeric values)

Restricts **numeric** values to a certain range.

```javascript
const userSchema = new mongoose.Schema({
  age: { type: Number, min: 18, max: 60 }, // Age must be between 18 and 60
});
```

✔ **Valid Inputs:** `{ age: 25 }`, `{ age: 50 }`  
❌ **Invalid Input:** `{ age: 17 }`, `{ age: 65 }` → `"Error: Age must be between 18 and 60"`

### **6. MinLength & MaxLength Validation (For Strings)** (Limits string length)

Limits the **number of characters** a string can have.

```javascript
const userSchema = new mongoose.Schema({
  username: { type: String, minlength: 3, maxlength: 15 }, // 3 to 15 characters
});
```

✔ **Valid Inputs:** `"John"`, `"Arshit123"`  
❌ **Invalid Input:** `"Al"` → `"Error: Minimum length is 3"`  
❌ **Invalid Input:** `"SuperLongUsername123"` → `"Error: Maximum length is 15"`

### **7. Match (Regex) Validation** (Ensures a specific format)

Ensures a string follows a **specific pattern**, such as an email or phone number format.

```javascript
const userSchema = new mongoose.Schema({
  phone: { type: String, match: /^[0-9]{10}$/ }, // Only allows 10-digit numbers
});
```

✔ **Valid Input:** `{ phone: "9876543210" }`  
❌ **Invalid Input:** `{ phone: "98765abcd" }` → `"Error: Invalid phone number format"`

### **8. Custom Validation (Using a Function)**

Allows you to **define your own validation logic** using a function.

```javascript
const userSchema = new mongoose.Schema({
  age: {
    type: Number,
    validate: {
      validator: (n) => {
        return n >= 18; // only allow above 18
      },
      message: (n) => "Abey chhotu chal nikal " + n.value + " saal ka hai tu",
    },
  },
});
```

✔ **Valid Inputs:** `{ age: 24 }`, `{ age: 30 }`  
❌ **Invalid Input:** `{ age: 12 }` → `"Error: Abey chhotu chal nikal 12 saal ka hai tu"`

### **Summary of Mongoose Validations**

1. **`required: true`** → Ensures a field is **mandatory**.
2. **`default: "value"`** → Sets a **default value** if none is provided.
3. **`enum: ["a", "b"]`** → Restricts values to a **specific list**.
4. **`unique: true`** → Prevents **duplicate values** in the database.
5. **`min` & `max`** → Limits **numbers** to a specific range.
6. **`minlength` & `maxlength`** → Limits the **length of strings**.
7. **`match: /regex/`** → Ensures a string **matches a pattern**.
8. **Custom validation** → Uses a function for **custom rules**.

[Go to top ↑](#index)

## **10. API-Level Validation in Express.js**

**Definition:**  
API-level validation is performed within your route handlers or middleware to enforce business rules and data integrity before the data reaches the database. This is especially useful for rules that might not be enforced at the schema level.

### **Example**

Here’s a simple API that prevents updating sensitive fields like `email`, `password`, and `age`:

```javascript
app.patch("/update", async (req, res) => {
  const detail = req.body.id;
  const NOT_ALLOWEDED_VALUES = ["email", "password", "age"];

  // Check if any restricted field is in the request body
  const isNotAllowed = Object.keys(req.body).some((key) =>
    NOT_ALLOWEDED_VALUES.includes(key)
  );

  try {
    if (!isNotAllowed) {
      // Update user if no restricted fields are being modified
      const user = await User.findByIdAndUpdate(detail, req.body, {
        returnDocument: "after",
      });
      console.log(user);
      res.send("Patch applied");
    } else {
      res.status(400).send("Error: Nahi karunga update");
    }
  } catch (error) {
    res.status(400).send("abey ? : " + error.message);
  }
});
```

### **Explanation in Bullet Points**

- **Step-by-step working:**
  1. **Extract `id` from `req.body`** → This identifies the user to update.
  2. **Define `NOT_ALLOWEDED_VALUES` array** → Contains fields that shouldn't be updated.
  3. **Check if the request contains any restricted fields** using `.some()` method.
  4. **If no restricted fields are found**, update the user with `findByIdAndUpdate`.
  5. **If restricted fields are present**, return an error response (`400 Bad Request`).
  6. **If an error occurs in the try block**, catch it and send a `400` response with the error message.

This ensures that even if a user tries to update sensitive fields, the API will block it and return an error.

### **Instead of writing validation logic directly in the route, you can also create a reusable helper validaton functions in a utils/ folder**

[Go to top ↑](#index)

## **11. Validator.js Library (NPM)**

[Validator.js](https://www.npmjs.com/package/validator) is a popular **NPM library** used for validating and sanitizing strings in **Node.js** applications. It provides built-in functions to check for valid email addresses, URLs, numbers, and more.

**Why Use Validator.js?**

- **Easy to use** – Provides simple functions for validation.
- **Prevents invalid input** – Ensures data consistency and correctness.
- **Security** – Helps prevent injection attacks (e.g., XSS, SQL Injection).
- **Lightweight** – No extra dependencies required.

To install Validator.js, use the following command:

```sh
npm install validator
```

### **Example**

```javascript
const validator = require("validator");
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
  email: {
    type: String,
    required: true,
    trim: true,
    lowercase: true,
    validate: {
      validator: (value) => validator.isEmail(value), // Validates email format
      message: "Invalid email format!",
    },
  },
  website: {
    type: String,
    validate: {
      validator: (value) => validator.isURL(value), // Checks if it's a valid URL
      message: "Invalid website URL!",
    },
  },
  age: {
    type: Number,
    validate: {
      validator: (value) => value >= 18, // Ensures age is 18 or above
      message: "Age must be 18 or older!",
    },
  },
});

const User = mongoose.model("User", userSchema);
```

### **Commonly Used Validator.js Functions**

| **Function**                 | **Description**                                  | **Example**                                              |
| ---------------------------- | ------------------------------------------------ | -------------------------------------------------------- |
| `isEmail(str)`               | Checks if the string is a valid email.           | `validator.isEmail("test@example.com") // true`          |
| `isURL(str)`                 | Checks if the string is a valid URL.             | `validator.isURL("https://google.com") // true`          |
| `isNumeric(str)`             | Checks if the string contains only numbers.      | `validator.isNumeric("123") // true`                     |
| `isAlpha(str)`               | Checks if the string contains only letters.      | `validator.isAlpha("hello") // true`                     |
| `isAlphanumeric(str)`        | Checks if the string contains letters & numbers. | `validator.isAlphanumeric("hello123") // true`           |
| `isMobilePhone(str, locale)` | Validates phone numbers for a specific country.  | `validator.isMobilePhone("9876543210", "en-IN") // true` |
| `isStrongPassword(str)`      | Checks if the password is strong.                | `validator.isStrongPassword("Pass@123") // true`         |

[Go to top ↑](#index)

## **12. What is `bcrypt` npm Library and why do we need?**

`bcrypt` is a widely used Node.js library for **hashing passwords** securely. It helps protect user credentials by converting plain text passwords into an irreversible, encrypted format before storing them in the database.

### **Why Do We Need `bcrypt`?**

- **Security:** Storing passwords in plain text is highly insecure. If your database is compromised, all user passwords would be exposed.
- **One-Way Hashing:** bcrypt converts a password into a hashed value that **cannot be reversed** into its original form.
- **Automatic Salting:** It adds a **random "salt"** (extra characters) to each password before hashing, making it resistant to attacks like **rainbow table attacks**.
- **Great protection again attacks:** This makes brute-force attacks (guessing passwords by trying millions of combinations) much harder.

### **How bcrypt Works (with Example)**

A simple example of how bcrypt is used in a **user sign-up API** to hash passwords before storing them in the database.

```javascript
const bcrypt = require("bcrypt");
const express = require("express");
const app = express();
app.use(express.json());

app.post("/sign-up", async (req, res) => {
  try {
    const { firstName, lastName, email, password } = req.body;

    // Hash the password with a salt factor of 10
    const hashedPassword = await bcrypt.hash(password, 10);
    // Save user with hashed password
    const user = new User({
      firstName,
      lastName,
      email,
      password: hashedPassword, // Store the hashed password
    });

    await user.save();
    res.send("User added");
  } catch (error) {
    res.status(500).send(error.message);
  }
});
```

**What happened here ?:**

1. **Extract user data from `req.body`** – The user provides their `firstName`, `lastName`, `email`, and `password`.
2. **Hash the password using bcrypt** – `bcrypt.hash(password, 10)` generates a secure hash with a **salt factor of 10**.
   - **Salt Factor:** The number `10` means bcrypt will run **2^10 (1024) hashing rounds**, making it more secure (_more the value, more the time will be taken_).
3. **Save user details in the database** – Instead of storing the plain text password, we store the hashed password.
   - `e.g - $2b$10$kpwaqdx7yQcK1DvVxbs6DuNRe2glonSkyQ20.//.fC/MgPF4YPq9y`
4. **Send success response** – If everything works fine, `"User added"` is sent.
5. **Handle errors properly** – If anything goes wrong, the server responds with `500` and an error message.

### **How to Verify Passwords with bcrypt?**

Since bcrypt **hashes passwords irreversibly**, we can’t "decrypt" them to compare with user input. Instead, we use `bcrypt.compare()` to check if a given password matches the stored hashed password.

**Example (Login API)**

```javascript
const bcrypt = require("bcrypt");
const express = require("express");
const app = express();
app.use(express.json());

app.get("/login", async (req, res) => {
  try {
    const { email, password } = req.body;

    // Find user by email
    const user = await User.findOne({ email: email });

    if (!user) {
      throw new Error("Invalid Credentials");
    }

    // Compare the entered password with the stored hash
    const isPassValid = await bcrypt.compare(password, user.password);

    if (isPassValid) {
      res.send("Login Successful");
    } else {
      throw new Error("Invalid Credentials");
    }
  } catch (error) {
    res.status(400).send("ERROR: " + error.message);
  }
});
```

**How Does bcrypt Verify Passwords?**

1. **User enters email and password** → Sent in `req.body`.
2. **Find user in the database by email** → `User.findOne({ email })`.
3. **If user doesn’t exist** → Throw `"Invalid Credentials"` error.
4. **Compare entered password with stored hash** → `bcrypt.compare(password, user.password)`.
   - bcrypt internally **rehashes the entered password** with the same salt and checks if the hashes match.
5. **If passwords match**, login is successful.
6. **If passwords don’t match**, throw `"Invalid Credentials"` error.

### **Note:**

- Hashing is a **one-way process**—you cannot decrypt a bcrypt hash back to the original password.
- Always use **async/await** with `bcrypt.compare()` and `bcrypt.hash()` to prevent blocking operations.
- **Never log or expose hashed passwords**, even for debugging.

[Go to top ↑](#index)
