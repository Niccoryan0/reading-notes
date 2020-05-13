# Day 8 Readings


## SQL Bolt
- Structured Query Language is a language made for technical and non-technical queries as well as manipulation and transformation of data from a relational database. 
- SELECT statements are how we retrieve data from an SQL database, these are known as queries. The most basic query would be a few specific columns (properties) of a table with all their rows (instances). This would produce a 2-d set of rows and columns, copying the specific columns we request. A direct copy cna be made by copying all properties and instances.
- A WHERE clause can help to filter the results we get back, using AND/OR statements to chain together complex logic.
- WHERE clauses can use several operators for comparison, including but not limited to = for strict case-sensitive equals, != or <> for case sensivite inequality, LIKE and NOT LIKE for case insensitive string comparison, % can be used anywhere to match a sequence of characters when LIKE or NOT LIKE is used.
- DISTINCT can be used to discard rows that have a duplicate column value, but will do so blindly.
- ORDER BY is used to order the data with some given parameters, and each row is sorted alpha-numerically based on specified column value. Some databases also allow collations to be specified to better sort data with international languages used.
- LIMIT is used to reduce the number of rows returned by a query, and OFFSET will specify where to begin counting the number of rows to return.