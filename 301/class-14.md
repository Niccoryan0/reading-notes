# Day 14 Readings

## Database Normalization Explained in Simple English
- DB Normalization is a process by which a database is organized into tables and columns, and each table should be a *specific* topic, with only related columns included. 
- Reasons to do so: minimize duplicate data, minimize or avoid data modification issues, and to simplify queries. 
- Modification anomalies: insert anomaly, facts that cant be recorded until information for the entire row is known. Update anomaly, occurs from having the same info in several rows and if all rows arent updated inconsistencies occur. Deletion anomaly, deletion of a row causes removal of more than one set of facts.
- Taken directly from article:
"There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. 

There are several additional forms, such as BCNF, but I consider those advanced, and not too necessary to learn in the beginning.

The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form. Before we discuss the various forms and rules in detail, let’s summarize the various forms:

First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary"

## 