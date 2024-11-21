# MongoDB

This guide provides comprehensive information on how to work with MongoDB, including common operations, best practices, and tips for managing your NoSQL database. Whether you're a beginner or an experienced user, this guide will help you make the most out of MongoDB.

## Table of Contents

- [Introduction to MongoDB](#introduction-to-mongodb)  
  Overview of MongoDB, its features, and how to set it up.

- [Connecting to MongoDB](#connecting-to-mongodb)  
  How to connect to MongoDB using various methods.

- [Basic MongoDB Operations](#basic-mongodb-operations)  
  Common MongoDB operations such as CRUD operations (Create, Read, Update, Delete).

- [Advanced MongoDB Queries](#advanced-mongodb-queries)  
  Complex queries like aggregation, indexing, and advanced filtering.

- [Performance Optimization](#performance-optimization)  
  Tips and best practices for optimizing MongoDB performance.

- [Error Handling and Debugging](#error-handling-and-debugging)  
  How to handle errors and debug queries in MongoDB.

---

## Introduction to MongoDB

MongoDB is a popular NoSQL database system that stores data in flexible, JSON-like documents. Unlike traditional relational databases, MongoDB allows you to store data without requiring a predefined schema, making it ideal for applications that need scalability and flexibility.

### Key Features of MongoDB:
- Schema-less design: Store data in flexible documents that can change over time.
- Horizontal scaling: Easily scale applications by distributing data across multiple servers.
- Rich query capabilities: Support for indexing, aggregation, and real-time analytics.
- Geospatial indexing: Manage and query location-based data.
- Built-in replication and high availability with replica sets.
- Distributed architecture with automatic sharding for large-scale deployments.

---

## Connecting to MongoDB

You can connect to MongoDB in various ways, depending on the environment and programming language you're using. Below are examples for different tools and languages.

### Example using **Mongo Shell**:

1. Open your terminal or command prompt.
2. Run the following command to connect to MongoDB:

   ```bash
   mongo --host <host> --port <port> -u <username> -p <password> --authenticationDatabase <auth_db>
   ```

3. After connecting, you can execute MongoDB commands directly in the shell.

### Example using **Node.js** with Mongoose:

```javascript
const mongoose = require('mongoose');

mongoose.connect('mongodb://<username>:<password>@<host>:<port>/<database>', {
  useNewUrlParser: true,
  useUnifiedTopology: true
}).then(() => {
  console.log('Connected to MongoDB');
}).catch(err => {
  console.error('Error connecting to MongoDB', err);
});
```

### Example using **MongoDB Compass**:

1. Open MongoDB Compass and click on "New Connection."
2. Enter your connection details, such as hostname, port, and authentication information.
3. Once connected, you can visualize your collections and execute queries using the GUI.

---

## Basic MongoDB Operations

Here are some common MongoDB operations that you will frequently use.

### Inserting Documents
To insert a new document into a collection:

```javascript
db.collection('employees').insertOne({
  name: 'John Doe',
  position: 'Software Engineer',
  salary: 75000
});
```

### Retrieving Documents
To retrieve all documents from a collection:

```javascript
db.collection('employees').find();
```

To retrieve documents with a specific condition:

```javascript
db.collection('employees').find({ position: 'Software Engineer' });
```

### Updating Documents
To update a document in the collection:

```javascript
db.collection('employees').updateOne(
  { name: 'John Doe' },
  { $set: { salary: 80000 } }
);
```

### Deleting Documents
To delete a document from a collection:

```javascript
db.collection('employees').deleteOne({ name: 'John Doe' });
```

---

## Advanced MongoDB Queries

MongoDB supports complex queries, including aggregation, indexing, and filtering.

### Aggregation Framework
MongoDB’s aggregation framework allows you to perform complex data transformations.

Example of using aggregation to group data:

```javascript
db.collection('employees').aggregate([
  { $group: { _id: "$position", totalSalary: { $sum: "$salary" } } }
]);
```

### Indexing
Indexes help improve the performance of read operations.

Create an index on the `name` field:

```javascript
db.collection('employees').createIndex({ name: 1 });
```

### Projection
You can limit the fields returned by a query using projections.

```javascript
db.collection('employees').find({}, { name: 1, position: 1 });
```

### Sorting
Sort documents based on a specific field.

```javascript
db.collection('employees').find().sort({ salary: -1 });
```

---

## Performance Optimization

Here are some tips to optimize MongoDB performance:

- **Use Indexes**: Create indexes on fields that are frequently used in queries to speed up data retrieval.

```javascript
db.collection('employees').createIndex({ position: 1 });
```

- **Sharding**: Distribute data across multiple servers to handle large datasets efficiently.

- **Use Aggregation Pipeline**: Aggregation operations are more efficient than manual processing in your application code.

- **Optimize Queries**: Make sure your queries are using indexed fields and minimize the number of documents returned.

---

## Error Handling and Debugging

MongoDB provides various tools to help you handle errors and debug your queries.

### Handling Errors in Node.js:

```javascript
db.collection('employees').insertOne(data)
  .catch(err => {
    console.error('Error inserting document:', err);
  });
```

### Using Explain Plan to Analyze Queries:

The `explain()` method returns information about how MongoDB executes a query, helping you identify bottlenecks.

```javascript
db.collection('employees').find().explain('executionStats');
```

This will give you insights into the performance of the query, such as whether it used an index.

### Enabling Profiler:

MongoDB’s profiler tracks slow queries, allowing you to identify inefficient operations.

```javascript
db.setProfilingLevel(2);
```

To view slow queries:

```javascript
db.system.profile.find();
```

