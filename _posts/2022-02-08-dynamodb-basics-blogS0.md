---
layout: post
title:  "S0. DynamoDB Basics"
date:   2022/0-08 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# What is DynamoDB?

![dynamo-db](/images/dynamo-db.png)

Amazon DynamoDB is an AWS service that allows users to create key-value NoSQL databases that are fully managed by AWS. These databases use a serverless framework because they work in conjunction with AWS's resources and only require the client to pay for the services that are actively used.  (48 words)

# Comparisons to MongoDB

Mongo 
1. 
- traditional, server based database
- security relies on consistent TCP connection to protect the database from the public interent

2. operations model
- mongo requires its software to be installed on each instance that it is used on on , this increases the memory and storage that is needed overall.

Dynamo
1. 
- service-based database
- database access is processed through the DynamoDB API rather than HTTPS network connection
- isntead uses AWS IAM permissions to authorize connection with clients
- therefore uses up less latency 

2. operations model
- dynamo handles the instance management and the user is only responsible for the ammount of usage that their application uses up. 

# Documents? Collections? ??

- tables items attributes
-(collections of items, items, columns)

    ---- partitions?
        C+P 
        
        A partition is an allocation of storage for a table that is automatically replicated across multiple AZs within an AWS Region.

        Partition management is handled entirely by DynamoDB—you never have to manage partitions yourself.     

![dynamodb-partitions](/images/dynamodb-partitions.jpeg) 

# schema ???? model????

Some of the relevant operations that can be used when working with the mongo shell are as follows:

    > mongo                     # this connects the server to mongo shell
    > help
    > show dbs                  # this displays all the of the available databases 

# Prerequisites

In order to properly run DynamoDB on your machine, the following softwares need to be installed:

- Node.js
' # node -v '
- an AWS profile
- serverless framework

# References

MongoDB [https://en.wikipedia.org/wiki/MongoDB](https://en.wikipedia.org/wiki/MongoDB)
Mongo vs Dynamo [https://www.dynamodbguide.com/mongo-db-vs-dynamo-db]