---
layout: post
title:  "11. MongoDB Basics"
date:   2021-11-30 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img[alt=forward-proxy-flow.png] {width: 50%}</style></html>

# What is MongoDB?

MongoDB is a non-relational database program that is developed by MongoDB Inc. and allows for the storage and retreival of data. Non-relational means that this databases does not use SQL (structured query language) but rather it deals with data through the usage of JSON-like documents that allow our data to to be flexible and change over time. 

An example of MongoDB's document structure can be seen below:
```
{
    "_id": 1,
    "fname": "Kim",
    "email": "kimberly.rebamonte.227@my.csun.edu",
    "likes": [
        "passing",
        "my",
        "classes"
    ],
    "classes": [
        {
           "name": "CIT 480 System Design and Implementation",
           "status": "cry",
        },
        {
           "name": "CIT 384 Web Development and Hosting",
           "status": "cry"
        }
        {
           "name": "COMP 424 Computer System Security",
           "status": "cry"
        }
    ]
}
```
MongoDB's document-oriented database allows for information to be stored within documents that are easier for developers to manage and work with. This scenario is more flexible compared to the alternative of a SQL database with calls for the usage of tables that contain rows and columns that are fixed into place.

> There are multiple different types of NoSQL databases such as document databases, key-value databases, wide-column databases, and graph databases.

Some of the advantages to using Mongo versus a regular RDBMS (relational database management system) are the ability to index fields in documents, use horizontal scaling, and use aggregation operations. 

# Documents? Collections? ??

" MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents. "

A collection is eqivalent to an SQL table. These collections are also what makes up a complete MongoDB document. One document has multple fields that contain name-value pairs. Multiple collections with documents containing multiple key-value pairs are able to be stored in one overall database. 

![mongo-nested-document](/images/mongo-nested-document.png)

Some of the relevant operations that can be used when working with the mongo shell are as follows:

    > mongo                     # this connects the server to mongo shell
    > help
    > show dbs                  # this displays all the of the available databases on your server
    > use <db>                  # this switches the database that is currently in use
    > db.newCollection.insertOne( { x: 1 } )    #this inserts new document data
    > exit                      # this exits and returns the user to their server's shell

# References

MongoDB [https://en.wikipedia.org/wiki/MongoDB](https://en.wikipedia.org/wiki/MongoDB)

Basics [https://www.mongodb.com/basics](https://www.mongodb.com/basics)

Document Databases [https://www.mongodb.com/document-databases](https://www.mongodb.com/document-databases)

Mongo Shell [https://docs.mongodb.com/manual/reference/mongo-shell/](https://docs.mongodb.com/manual/reference/mongo-shell/)

How To Use the MongoDB Shell [https://www.digitalocean.com/community/tutorials/how-to-use-the-mongodb-shell](https://www.digitalocean.com/community/tutorials/how-to-use-the-mongodb-shell)
