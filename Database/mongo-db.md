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

---

### **Difference Between `findOneAndUpdate()` and `findByIdAndUpdate()`**

- **Use `findOneAndUpdate()`** when searching by fields like `email` or `name`.
- **Use `findByIdAndUpdate()`** when updating a document by `_id`.

[Go to top ↑](#index)
