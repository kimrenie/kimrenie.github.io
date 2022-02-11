---
layout: post
title:  "S0. DynamoDB Basics"
date:   2022-02-10 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# What is DynamoDB?

![dynamo-db](/images/dynamo-db.png)

Amazon DynamoDB is an AWS service that allows users to create key-value NoSQL databases that are fully managed by AWS. These databases use a serverless framework because they work in conjunction with AWS's resources and only require the client to pay for the services that are actively used.

# Comparisons to MongoDB

| | MongoDB | DynamoDB |
| ---------- | ---------- | ---------- |
| Basics | Uses a traditional, server-based database | Uses a service-based database |
| Security | Data security relies on keeping up a consistent TCP connection in order to protect the database from the public internet | database access is processed through the DynamoDB API rather than HTTPS network connection. This method uses AWS Identity and Access Management (IAM) permissions in order to authorize connection with clients. This process also reduces latency. |
| Operations model | Mongo requires its software to be installed on each instance that it is used on on. Subsequently, this increases the memory and storage that is needed overall. | Dynamo handles the instance management and the user is only responsible for the ammount of usage that their application actively uses. |

# Important Concepts

Similar to MongoDB, DynamoDB make use of concepts such as tables, items, and attributes. "Tables" would be used to group together related data, "Items" would refer to the individual data records that can be found inside of a table, and "Attributes" is another piece of data that is stored with an Item.

> A partition is an portion of storage for a table that is automatically created across Availibility Zones within an AWS Region. The management of this internal storage system is completely done by Amazon and DynamoDB, therefore the user does not need to regulate it themselves.  

![dynamodb-partitions](/images/dynamodb-partitions.jpeg) 

# Schema and Table Design

The schema of our database serves to direct where our data is located and how to go about accessing/working with our data. As a NoSQL database, DynaoDB is considered to be schema-less because the structure of the tables is less strict than traditional databases and instead uses primary keys and indexes. 

## Primary Keys

When you create a table, the following paramaters need to be provided:

- `TableName` - name of table
- `KeySchema` - attributes used for the primary key
- `AttributeDefinitions` - data types ...
- `ProvisionedTheoughout` - RCU and WCUs ...

> The KeySchema defines data elements that follow a table's required Primary Key (which is composed of either one partition key OR a partition key and sort key pairing).

![dynamodb-primarykey](/images/dynamodb-primarykey.jpeg)

# References

MongoDB [https://en.wikipedia.org/wiki/MongoDB](https://en.wikipedia.org/wiki/MongoDB)

Core Components [https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.PrimaryKey]

Basics [https://nordcloud.com/5-things-to-know-when-starting-to-use-dynamodb-nosql-databases/#:~:text=DynamoDB%2C%20like%20most%20other%20NoSQL,to%20any%20of%20your%20items]

Mongo vs Dynamo [https://www.dynamodbguide.com/mongo-db-vs-dynamo-db]

Concepts [https://www.dynamodbguide.com/key-concepts]

Schema [https://www.prisma.io/dataguide/intro/intro-to-schemas]

Primary Keys [https://aws.amazon.com/blogs/database/choosing-the-right-dynamodb-partition-key/]