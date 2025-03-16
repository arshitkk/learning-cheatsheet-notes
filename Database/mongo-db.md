# **Index**

## **1. [Mongo DB Setup](#1-mongo-db-setup-1)**

1. **[MongoDB Atlas Setup & Connection Guide](#1-mongodb-atlas-setup--connection-guide)**
2. **[MongoDB Compass Setup](#2-mongodb-compass-setup)**
3. **[Connecting to the Database Server](#3-connecting-to-the-database-server)**

## **2. [MongoDB Core Concepts & Operations](#2-mongodb-core-concepts--operations-1)**

1. **[ Introduction to CRUD Operations in MongoDB](#1-introduction-to-crud-operations-in-mongodb)**

# **1. Mongo DB Setup**

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

# **2. MongoDB Core Concepts & Operations**

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
