# **Mongo and Mongoose**

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)

## SQL vs NoSQL Database Differences Explaines

* NoSQL database is getting widley adoped

### SQL vs NoSQL: High-Level Differences

#### SQL

* SQL Dbs are called RDBMS(relation database managment system)

* table based, key-value pairs, graph databases, wide-column stores

* respresent data in form of tables consisting of n number of rows

* vertically scalable

* SQL Dbs use SQL(structured query language)

* MySql, Oracle, Sqlite, Postgres, MS-SQL

* good fit for complex query intesice environment

* not best fit for heirarchical data storage

* vertically scalable

* best fit for heavy duty transactional type applications

#### NoSQL

* NoSQL called non-relational or distributed database

* document based

* collection of key-value pairs, documents, graph DBs, etc. which do not have standard schema definitions

* horizontally scalable

* queries focus on collection of documents

* MongoDB, BigTable, Redis, RavenDB, Cassandra, Hbase, Neo4j, CouchDb

* not good fix for complex queries

* fits better for hierarchical data storage

* horizontally scalable

* not comparable or stable in high load complex transactional applications

### MongoDB

* One of the most popular NoSQL DBs

* stores data in JSON like documents

* non-relational database

* dynamic schema

* developed by DoubleClick

* written in C++

**Strengths:**

* Speed - good performace for simple queries

* Scalability - horizontally scalable, reduces workload by increading number o servers in resource pool

* Manageable - easy to use for devs and admins - ability to share DB

* Dynamix Schema - gives flexibility to evolve data schema without modifying existing sata

## Resources

[NoSQL vsSQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

[NoSQL Modeling Techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

### Additional Resources

[Mongoose API](https://mongoosejs.com/docs/api.html#Model)

[Sql vs NoSQL Video](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)
