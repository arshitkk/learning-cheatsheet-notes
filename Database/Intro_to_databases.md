# **index**

1. **[What is a Database?](#1-what-is-a-database)**
2. **[What are the Types of Databases](#2-what-are-the-types-of-databases)**
3. **[Brief about RDMS(MySQL, PstgreSQL)](#3-brief-about-rdmsmysql-pstgresql)**
4. **[Breif about on NoSQL and MongoDB](#4-breif-about-on-nosql-and-mongodb)**
5. **[RDBMS vs NoSQL (Document Database)](#5-rdbms-vs-nosql-document-database)**

# **1. What is a Database?**

A **database** is an organized collection of data that is stored and managed electronically. It allows data to be easily accessed, managed, and updated. Databases are typically managed by software called a **Database Management System (DBMS)**.

The **DBMS** acts as an bridge between the users, applications, and the actual data in the database. It helps in storing, retrieving, and managing the data efficiently. In addition to managing data, the DBMS also provides tools for **database administration**, such as backup, security, and performance management.

Together, the **database**, the **DBMS**, and the related applications make up the **database system**.

Sometimes, the word **"database"** is used to refer to just the **DBMS**, the **database system**, or the **applications** connected to the database.

[Go to top ↑](#index)

# **2. What are the Types of Databases**

Databases can be categorized based on how they store, manage, and process data. Here are some of the main types:

## **1. Relational Database (RDBMS)**

- **Example**: MySQL, PostgreSQL
- Stores data in **tables** with **predefined schemas** (structure).
- Ideal for handling **complex queries** and **transactions**.
- Ensures **data integrity** through **ACID properties** (Atomicity, Consistency, Isolation, Durability).
- Commonly used in applications that require **robust and structured data models**, like banking systems and enterprise applications.

## **2. NoSQL Database**

- **Example**: MongoDB
- Stores data in **flexible, JSON-like documents** with **dynamic schemas**.
- Suitable for handling **large amounts of unstructured or semi-structured data**.
- Highly **scalable**, making it ideal for **modern web applications** and **big data systems**.

## **3. In-Memory Database**

- **Example**: Redis
- Stores data **directly in memory (RAM)** for **fast access**.
- Supports various **data structures** like strings, hashes, and lists.
- Best for **caching**, **real-time analytics**, and **message brokering**.

## **4. Distributed SQL Database**

- **Example**: CockroachDB
- A **relational database** that is **distributed across multiple nodes**.
- Provides **strong consistency**, **ACID transactions**, and **horizontal scaling**.
- Ideal for applications needing **high availability** and **geographical distribution**.

## **5. Time Series Database**

- **Example**: InfluxDB
- Specially designed for **time-stamped data**.
- Optimized for **high write and query loads**.
- Used in **monitoring systems**, **real-time analytics**, and **IoT applications**.

## **6. Object-Oriented Database**

- **Example**: db4o
- Stores data as **objects**, matching the structure of **object-oriented programming languages**.
- Simplifies development by allowing **direct storage and retrieval of objects** without converting them into tables.

## **7. Graph Database**

- **Example**: Neo4j
- Uses **graph structures** with **nodes** and **relationships** to represent data.
- Excellent for managing **complex relationships**, such as in **social networks**, **recommendation engines**, and **fraud detection** systems.

## **8. Hierarchical Database**

- **Example**: IBM IMS
- Organizes data in a **tree-like structure** with **parent-child relationships**.
- Mainly used in **legacy(_outdated_) systems** for **high-performance transaction processing**.
- Known for handling **large-scale and mission-critical applications**.

## **9. Network Database**

- **Example**: IDMS
- Represents data using a **graph of record types** and **set relationships**.
- More flexible than hierarchical databases in handling **complex data relationships**.
- Often used in **legacy(_outdated_) systems** that need **high performance**.

## **10. Cloud Database**

- **Example**: Amazon RDS
- A **managed database service** hosted in the **cloud**.
- Supports multiple **relational database engines** like MySQL, PostgreSQL, and Oracle.
- Automates tasks like **backups**, **patching**, and **scaling**, making it easy to manage databases without manual effort.

## **Most Commonly Used Databases**

1. **Relational Databases** (e.g., MySQL, PostgreSQL)
2. **NoSQL Databases** (e.g., MongoDB)

[Go to top ↑](#index)

# **3. Brief about RDMS(MySQL, PstgreSQL)**

## **E.F. Codd and Codd’s 12 Rules**

- **E.F. Codd** was a computer scientist who introduced the **Relational Database Model** in **1970**.
- He proposed **Codd’s 12 Rules** to define what a **Relational Database Management System (RDBMS)** should follow.
- Although they are called **12 Rules**, they are actually **13 rules**, numbered from **0 to 12**.

The rules specify that:

- A **relational database** should organize data into **tables**.
- There must be **relationships** between these tables.
- It must follow principles like **data integrity**, **logical data independence**, and **systematic treatment of null values**.

_Any database that satisfies these rules can be considered a **true relational database**._

## **The Story of MySQL**

- **MySQL** was developed by **Michael Widenius**.
- The name "**MySQL**" comes from his daughter’s name "**My**".
- Later, he named another database **MaxDB** after his son, Max, and a fork of MySQL as **MariaDB**, named after his daughter Maria.

**Ownership Timeline:**

- **MySQL** was first released in **1995**.
- It was acquired by **Sun Microsystems** in **2008**.
- Later, **Oracle Corporation** acquired Sun Microsystems in **2010**, and currently, **Oracle** manages **MySQL**.
- After Oracle’s acquisition, Michael Widenius and his team created **MariaDB**, which is an **open-source fork** of **MySQL**.

## **The Story of PostgreSQL**

- **PostgreSQL** was developed as an advanced version of the **Ingres** project at the **University of California, Berkeley** in the **1980s**.
- It was initially called **POSTGRES**, referring to "post-Ingres".
- Later, it was renamed **PostgreSQL** to reflect its support for **SQL (Structured Query Language)**.
- PostgreSQL is known for its focus on **standards compliance**, **extensibility**, and support for **advanced data types** like JSON and XML.
- It is an **open-source**, **object-relational** database system widely used for **complex applications**.

[Go to top ↑](#index)

# **4. Breif about on NoSQL and MongoDB**

## **NoSQL Databases**

- **NoSQL** stands for "**Not Only SQL**." (_much more than that_)
- These databases are designed to handle **large volumes of unstructured or semi-structured data**.
- Unlike **Relational Databases (RDBMS)**, NoSQL databases do **not require fixed schemas** or complex **JOIN** operations.

### **Types of NoSQL Databases:**

1. **Document Databases**
   - Store data as **documents**, often in formats like **JSON** or **BSON**.
   - Example: **MongoDB**.
2. **Key-Value Databases**
   - Store data as **key-value pairs**.
   - Example: **Redis**.
3. **Graph Databases**
   - Store data in **nodes** and **edges**, representing entities and their relationships.
   - Example: **Neo4j**.
4. **Wide-Column Databases**
   - Store data in **tables**, but columns can vary by row and are grouped into **column families**.
   - Example: **Apache Cassandra**.
5. **Multi-Model Databases**
   - Support **multiple data models** in one integrated backend.
   - Example: **ArangoDB**.

### **MongoDB**

- **MongoDB** is a **Document-Oriented NoSQL Database**.
- It was developed by a company called **10gen** in **2009**.
- The name "**MongoDB**" comes from "**humongous**," highlighting its ability to manage **large-scale data**.
- Later, **10gen** changed its name to **MongoDB Inc.**, which continues to maintain the database today.

#### **Key Features of MongoDB:**

- Stores data in **flexible, JSON-like documents**.
- Supports **dynamic schemas**, making it easier to adapt to changing data structures.
- Highly **scalable**, with **horizontal scaling** capabilities.
- It works exceptionally well with **JavaScript** and **Node.js**, as both use **JSON** for data exchange.
- Known for **increasing developer productivity**, due to its simplicity and flexibility.

[Go to top ↑](#index)

# **5. RDBMS vs NoSQL (Document Database)**

## **1. Structure**

- **RDBMS**:
  - Uses **tables** made of **rows and columns** (like an Excel sheet).
  - Each **row** represents a record, and each **column** is a field (attribute).
  - Example: A **Users** table with columns like `ID`, `Name`, `Email`.
- **NoSQL (Document Database)**:
  - Stores data as **documents** (like JSON objects).
  - Documents are grouped in **collections** (similar to tables).
  - Each document can have a **flexible structure** and **nested fields**.
  - Example: A user document with their `Name`, `Email`, and an **array of hobbies**.

## **2. Relationships**

- **RDBMS**:

  - Uses **foreign keys** to link tables.
  - Requires **joins** to fetch related data.
  - Example: Separate `Users` and `Hobbies` tables, linked by `UserID`.

- **NoSQL (Document Database)**:
  - Related data is often **embedded** inside a single document.
  - No need for complex joins.
  - Example: User document includes their **hobbies inside the same document**.

## **3. Schema**

- **RDBMS**:

  - Requires a **fixed schema**.
  - Structure must be **defined in advance** (strict).
  - Changing structure (adding/removing columns) can be **complex**.

- **NoSQL (Document Database)**:
  - **Schema-less** or **dynamic schema**.
  - Each document can have **different fields and structures**.
  - Easy to **add or remove fields** without affecting other documents.

## **4. Data Organization**

- **RDBMS**:

  - Data is **normalized** (spread across multiple tables).
  - Focus on **reducing redundancy** and **maintaining integrity**.
  - **Complex joins** are common to get complete information.

- **NoSQL (Document Database)**:
  - Data is often **denormalized** (stored together in one document).
  - Reduces the need for joins and makes **data retrieval faster**.

## **5. Query Language**

- **RDBMS**:

  - Uses **SQL (Structured Query Language)**.
  - SQL is **standardized**, with fixed rules and structure.

- **NoSQL (Document Database)**:
  - Uses **custom query languages**, often similar to **JSON** commands.
  - Example: MongoDB uses queries like `db.users.find({ name: "John" })`.

## **6. Scalability**

- **RDBMS**:

  - Generally **vertically scalable** (upgrade the existing server).
  - **Horizontal scaling** (adding more servers) is **difficult**.

- **NoSQL (Document Database)**:
  - Designed for **horizontal scaling** (easily distribute data across many servers).
  - Good for **big data** and **real-time applications**.

## **7. Use Cases**

- **RDBMS**:

  - Best for **complex transactions** and **strong consistency**.
  - Ideal for systems that need **ACID compliance** (banks, ERPs).
  - Example: **Banking systems**, **inventory management**, **HR databases**.

- **NoSQL (Document Database)**:
  - Best for **flexible data models** and **high-performance needs**.
  - Ideal for **real-time applications**, **content management systems**, and **big data analytics**.
  - Example: **Social media platforms**, **CMS**, **real-time analytics**.

## **8. Examples**

- **RDBMS**:

  - **MySQL**, **PostgreSQL**, **Oracle Database**, **SQL Server**.

- **NoSQL (Document Database)**:
  - **MongoDB**, **CouchDB**, **Amazon DocumentDB**.

## **Quick Summary Table**

| **Feature**        | **RDBMS**               | **NoSQL (Document)**              |
| ------------------ | ----------------------- | --------------------------------- |
| **Structure**      | Tables (rows & columns) | Collections (documents)           |
| **Schema**         | Fixed schema            | Flexible / Schema-less            |
| **Relationships**  | Foreign keys & joins    | Embedded or referenced data       |
| **Query Language** | SQL                     | Custom (JSON-like queries)        |
| **Scalability**    | Vertical                | Horizontal                        |
| **Use Cases**      | Banking, ERP, CRM       | CMS, Social Media, Real-time apps |
| **Examples**       | MySQL, PostgreSQL       | MongoDB, CouchDB                  |

[Go to top ↑](#index)
