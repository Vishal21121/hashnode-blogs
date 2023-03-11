---
title: "MongoDB - A complete reference"
seoTitle: "MongoDB"
seoDescription: "MongoDB is a NoSQL document database system. It is made to be extremely versatile and scalable, enabling developers to create and maintain complex systems."
datePublished: Tue Mar 07 2023 14:16:57 GMT+0000 (Coordinated Universal Time)
cuid: cleyc4kob000t0al54kj1h4bg
slug: mongodb-a-complete-reference
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678170378675/92c04663-e8e6-48e6-92b6-5f6a950efe26.png
tags: mongodb, mongoshell, mongodbshell, coderscommunity, mongod

---

## Introduction

A well-liked open-source **NoSQL** document database system is **MongoDB**. It is made to be extremely versatile and scalable, enabling developers to create and maintain complex systems with ease.

In contrast to conventional relational databases, which store data in tables with a fixed structure, MongoDB stores data in collections of adaptable **JSON-like documents**. This makes it a good fit for applications that call for quick and effective querying of significant amounts of unstructured data.

Several businesses and organisations, from small startups to huge corporations, employ MongoDB, which has emerged as a popular option for developing contemporary web applications. It has a thriving user and developer community, and there are many tools and frameworks available to aid with creation and administration.

## Comparing MongoDB and SQL

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678171778513/23df915c-fb0a-4beb-80a3-b6a741269b83.png align="center")

If you know SQL then you will know the following terms **database**, **tables**, **rows** and **columns** and these are compared to MongoDB in the following ways for example the term **database** is called **database** in MongoDB, **tables** in SQL is similar to **collections** in MongoDB, **rows** in SQL is similar to **documents** and **columns** in SQL is similar to **fields** in MongoDB.

## Mongo shell and Mongod

**Mongo Shell:** Through the command line, you can communicate with instances of MongoDB using the interactive JavaScript interface known as Mongo Shell. The shell is useful for manipulating data. administrative tasks like database instance maintenance.

**Mongod:** The main daemon process for the MongoDB system is called Mongod. It monitors data access, responds to data requests, and runs administration tasks in the background.

## Commands

Before heading towards commands let's understand some basic terms:

* **Database**: Storage space for collections. In SQL, this is equivalent to a database, and often each project will have a separate database with a variety of collections.
    
* **Collection:** A collection of documents in a database. Each sort of data (users, posts, and products) will often have its collection, which is the same as a table in SQL.
    
* **Document**: A file included within a collection. There will typically be one document for each object in the collection, which is equivalent to a row in SQL. A document is just a JSON object as well.
    
* **Field**: An internal key-value pair for a document. This is equivalent to a SQL column. Each document will have a certain number of fields with data like name, address, interests, etc. in them. One significant distinction between SQL and MongoDB is that a field can contain values other than characters, numbers, booleans, etc., such as arrays and JSON objects.
    

### Basic Commands

* ```plaintext
        mongosh
    ```
    
    Connect to your personal MongoDB instance locally. The mongosh connection will be used for all subsequent commands.
    
* ```plaintext
        show dbs
    ```
    
    Shows all the databases in the current MongoDB instance
    
* ```plaintext
        use dbName
    ```
    
    Switch to the database provided by dbName
    
* ```plaintext
        db
    ```
    
    Shows the current database name.
    
* ```plaintext
        cls
    ```
    
    Clears the terminal screen
    
* ```plaintext
        show collections
    ```
    
    Shows all collections in the current database.
    
* ```plaintext
        db.dropDatabase()
    ```
    
    Deletes the current database.
    
* ```plaintext
        exit
    ```
    
    Exits the current mongosh session.
    

### Create operation

All the commands are related to a specific collection **users**

* ```plaintext
        db.users.insertOne({name:"Vishal"})
    ```
    
    Creates a document in the **users** collection.
    
* ```plaintext
        db.users.insertMany([{name:"Vishal"},{age:21}])
    ```
    
    Creates multiple documents in the **users** collections and documents are created with fields **name** and **age**.
    

### Read Operation

All the commands are related to a specific collection **users**

* ```plaintext
        db.users.find()
    ```
    
    Returns all the documents of the **users** collection
    
* ```plaintext
        db.users.find({ name: "Vishal"})
    ```
    
    Returns all the documents that match the filter object.
    
* ```plaintext
        db.users.find({age:21},{name:1,age:1})
    ```
    
    Returns all the documents that match the filter object and shows the name, age and id of the documents.
    
* ```plaintext
        db.users.find({age:21},{age:0})
    ```
    
    Returns all the documents that match the filter object and shows all the fields except age from the documents.
    
* ```plaintext
        db.users.findOne({name:"Vishal"})
    ```
    
    It's similar to **db.users.find()** but only returns the first document that matches the filter object.
    
* ```plaintext
        db.users.countDocuments({name:"Vishal"})
    ```
    
    Returns the count of documents that match the filter object passed to it.
    
* **Complex filter object**
    
* ```plaintext
        db.users.find({name:{$eq:"Vishal"}})
    ```
    
    This command checks for equality and returns all documents in which the name field is equal to **Vishal.**
    
* ```plaintext
        db.users.find({name:{$ne:"Vishal"}})
    ```
    
    This command checks for not equal and returns all documents in which the name field is not equal to **Vishal.**
    
* ```plaintext
        db.users.find({age:{$gt:12}})
    ```
    
    Returns all the documents in which the age field value is greater than 12
    
* ```plaintext
        db.users.find({age:{$gte:12}})
    ```
    
    Returns all the documents in which the age field value is greater than or equal to 12
    
* ```plaintext
        db.users.find({age:{$lt:22}})
    ```
    
    Returns all the documents in which the age field value is less than 22
    
* ```plaintext
        db.users.find({age:{$lte:22}})
    ```
    
    Returns all the documents in which the age field value is less than or equal to 22
    
* ```plaintext
        db.users.find({name:{$in:["Vishal","Arshdeep","Subhrajit"]}})
    ```
    
    Checks if a value is one of many values passed and returns all documents in which the name field is either **Vishal**, **Arshdeep** or **Subhrajit.**
    
* ```plaintext
        db.users.find({name:{$nin:["Vishal","Arshdeep","Subhrajit"]}})
    ```
    
    Checks if a value is not one of the many values passed and returns all documents in which the name field is neither among **Vishal**, **Arshdeep** and **Subhrajit.**
    
* ```plaintext
        db.users.find({$and:[{name:"Vishal Singh"},{age:21}]})
    ```
    
    It checks that multiple conditions are true and will return all the documents in which **name** is Vishal Singh and **age** is 21
    
* ```plaintext
        db.users.find({$or:[{name:"Vishal Singh"},{age:21}]})
    ```
    
    It checks that one among the multiple conditions is true and will return all the documents in which either **name** is Vishal Singh or **age** is 21
    
* ```plaintext
        db.users.find({name:{$not:{$eq:"Vishal"}}})
    ```
    
    It will return all the documents in which the **name** field is **not equal** to Vishal
    
* ```plaintext
        db.users.find({name:{$exists:true}})
    ```
    
    It checks whether the field exits or not and here it will return all the documents in which the name field exists.
    
* ```plaintext
        db.users.find({$expr:{$gt:["$balance","$debt"]}})
    ```
    
    It compares two different fields and here it will return the documents in which the balance is **greater than** the debt
    
* **Read Modifiers**
    
* ```plaintext
        db.users.find().sort({name:1,age:-1})
    ```
    
    Sorts the results of a find by the given fields and here it sorts the results in alphabetical order by name and if the name is same then it sorts by the age in reverse order.
    
* ```plaintext
        db.users.find().limit(2)
    ```
    
    Only returns the given number of documents, here it will return 2 documents after the find operation is performed.
    
* ```plaintext
        db.users.find().skip(2)
    ```
    
    Skips a specific number of documents from the beginning and here it will skip 2 documents from the beginning.
    

### Update Operation

All the commands are related to a specific collection **users**

* ```plaintext
        db.users.updateOne({name:"Vishal",age:21},{$set:{name:"Vishal Singh"}})
    ```
    
    In this, the second parameter is the update object which will update the name field as **Vishal Singh** in the first document that matches the filter object passed.
    
* ```plaintext
        db.users.updateMany({age:21},{$set:{age:41}})
    ```
    
    This command will set the age as 41 in all the documents that match the filter object in **users** collection.
    
* ```plaintext
        db.users.replaceOne({ age: 12 }, { age: 13 })
    ```
    
    Replaces the first document that matches the filter object with the exact object passed as the second parameter. **Note** it will overwrite the entire object and not just update the individual field.
    
* **Complex Update Operation**
    
* ```plaintext
        db.users.updateOne({ age: 21 }, { $set: { name: "hi" } })
    ```
    
    Updates the field passed to $set only and it will not affect the other fields of the document.
    
* ```plaintext
        db.users.updateOne({ age: 21 }, { $inc: { age: 2 } })
    ```
    
    Increments the age field of the document which is got by the filter object.
    
* ```plaintext
        db.users.updateMany({}, { $rename: { age: "years" } })
    ```
    
    It renames the **age** field to **years** and here it is doing for all users.
    
* ```plaintext
        db.users.updateOne({ years: 23 }, { $unset: { years: "" } })
    ```
    
    Removes the **years** field from the first document.
    
* ```plaintext
        
        db.users.updateMany({}, { $push: { friends: "Ram" } })
    ```
    
    It will add Ram to the friend array for all documents.
    
* ```plaintext
        db.users.updateMany({}, { $pull: { friends: "Ram" } })
    ```
    
    It will remove the Ram from the friend array for all documents.
    

### Delete operation

All the commands are related to a specific collection **users**

* ```plaintext
        db.users.deleteOne({years:21})
    ```
    
    It will delete the first document which matches the filter object
    
* ```plaintext
        db.users.deleteMany({ years: 21 })
    ```
    
    It will delete all the documents that match the filter object.