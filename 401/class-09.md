# 401-09 Readings

## LINQ:
- Language-Integrated Query is a set of technologies based on integrating query capabilities into C#. It provides a consistent query experience for objects, relational databases and XML.
- As an example, a single query can retrieve data from an SQL database and produce an XML stream as an output.
- The two forms LINQ queries can take are query syntax and method syntax, there's no semantic or performance difference though it's just for readability.
- "Query expressions can be compiled to expression trees or to delegates, depending on the type that the query is applied to. IEnumerable<T> queries are compiled to delegates. IQueryable and IQueryable<T> queries are compiled to expression trees. For more information, see Expression trees."

## Intro to LINQ Queries:
- A LINQ query is broken into three parts: Obtain the data source, create the query and execute the query, this is shown below in the diagram.
![Complete query operation](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/media/introduction-to-linq-queries/linq-query-complete-operation.png)
- "A queryable type requires no modification or special treatment to serve as a LINQ data source. If the source data is not already in memory as a queryable type, the LINQ provider must represent it as such. For example, LINQ to XML loads an XML document into a queryable XElement type"
- The query specifies what info it wants from the sources and optionally how it should be sorted, grouped or shaped. Similar to SQL, it has three clauses: from, where and select.
- A foreach statement is used to iterate over the query variable and actually execute the query.
- Basic LINQ Query operations: Obtaining a source, Filtering, Ordering, Grouping, Joining, Selecting.
