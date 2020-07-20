# 401-11 Readings

1. Do some research on what a Database Schema is.
  ![Source](http://www.databaseguides.com/what-is-a-database-schema#:~:text=Database%20schema%20refers%20to%20the%20layout%20of%20the,the%20existing%20relationship%20between%20the%20fields%20and%20tables.)
  - What is a Schema? 
    - A document that describes the organization and structure of a database.
  - Why do we use them?
    -  Primarily to handle organization/structure of the database as well as establish permissions.
  - What do they look like?
    - They contain objects like tables, columns, data types, views, stored procedures, relationships, primary keys, foreign keys, etc.
2. What are the different types of Database Keys?
  ![Source](https://www.techopedia.com/7/32101/storage/what-is-the-difference-between-a-composite-key-primary-key-and-foreign-key)
  - What is a Primary Key?
    - A uniquely identified field that is used as a reference for relating tables in the database.
  - What is a Foreign Key?
    - Non-unique field connected to the primary key of a different table in the same database.
  - What is a Composite Key?
    - A combination of 2 or more attributes/columns to form a primary key for a table.
  - How are they different? When do you use 1 over the others?
    - Foreign keys are used to tie two tables together, a primary key is the standard for most tables, it's like an index in an enumerable, it should be used for standard tables that need a simple, unique identifier. Composite keys should be used when two pieces of information are needed to uniquely identify items in a database.
3. What are Relationships in a relational database?
  ![Source 1](https://www.tech-recipes.com/rx/56738/one-to-one-one-to-many-table-relationships-in-sql-server/)
  ![Source 2](https://www.datanumen.com/blogs/3-main-types-relationships-access-databases/)
  - What is a 1:1 relationship?
    - A relationship wherein one row of a table is linked to only one row in another table and vice versa, which means it's created using a Primary Key - Unique foreign key relationship.
  - What is a Many:Many relationship?
    - A relationship wherein a parent row in one table contains several child rows in a second table and vice - versa.
  - How about a 1: Many or a Many:1?
    - These are a relationship between two tables wherein a row from one table can have several matching rows in another table, it's created using a Primary Key - Foreign key relationship.