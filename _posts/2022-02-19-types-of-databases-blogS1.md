---
layout: post
title:  "S1. Types of Databases"
date:   2022-02-19 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# Different Types of Databases?

![database-icon](/images/database-icon.jpg)

Each different type of database holds a different schema which helps detail its logical structure. Some of the most commonly used types of databases are: `hierarchical`, `network`, `object-oriened`, `relatational`, `NoSQL`, etc. 

## Hierarchical databases

The concept of a hierachical database was initially introduced in the 1960s in order to continue development in database management. In this concept, the database resembles a tree-like structure and every entry would be organized in accordance to a common parent entry. This organization concept would branch out continuously and every parent entry would have the potential to have multitudes of child entries. This organizational structure can be seen in ther egular day through a computer's internal file system.

![hierarchical-file-system](/images/hierarchical-file-system.png)

The image above displays a Windows Operating System file structure. At the top of the tree is the C drive (`C:\`) which serves as the entire system's parent entry. Nested underneath this entry are child-branches subsequently named `WINDOWS`, `My Documents`, and `Program Files`. These entries are child-branches to the C Drive, BUT at the same time they are parent-branches to the rest of the data in the tree structure. This mapping structure has a simple design and thus limited the user from creating more complex methods of organzing or traversing though data.

> Some examples of Hierachal Databases are filessytems, DNS, etc.

## Network databases

![network-database](/images/network-database.png)

A network database has the same fundamentals and can look similar to the tree schema but holds some flexibility differences. One of these major changes was the ability for entries to have more than one parent entry. This connection changed the structre from a tree with limitations to a more graph-like structure with the ability to create more compex relationships. One flaw with this structure is the limitations associated with having to follow network paths up to one common parent entry. 

## Relational databases

![relational-database](/images/relational-database.jpg)

Relational databases are in active use today and are fundamental in many organization's products. This database organizes entries with the use of tables and this schema involves the usage of columns that contain a name and data type. Each row in this table schema contains each entry and its values. These databases are highly organized but also have a strict schema that is difficult to alter.

> Some examples of Relational Databases are MySQL, PostgreSQL, etc.

## NoSQL databases

![NoSQL](/images/NoSQL.png)

A NoSQL database stands for No Stuctured Query Language. This database type can support other database types such as the following:

- Key Value Databases: Use key pairs in order to access and store different kinds of data.
- Document databases: Have the same concept as key-value access but each document can have its own individual schema structure. This flexibility allows a data structure that can change as an organization's plans change.
- Graph databses
- Column-family databases
- Time series databases

## Object-oriented databases

Object-oriented databases store data as 'objects' and is used to replicated the data conections that are seen in object-oriented programming and languages.

> Some examples of NoSQL Databases are mongoDB, redis, AmazonDynamoDB, etc.


# References

MongoDB [https://en.wikipedia.org/wiki/MongoDB](https://en.wikipedia.org/wiki/MongoDB)

-----
https://en.wikipedia.org/wiki/Database
https://www.geeksforgeeks.org/types-of-databases/
https://www.educba.com/types-of-database/
https://www.prisma.io/dataguide/intro/comparing-database-types