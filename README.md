## Logical Operators
| Operator | Definition | Syntax | Example |
|--------|------------|--------|----------------|
| AND | The AND operator allows the existence of multiple conditions in an SQL statement's WHERE clause. | SELECT col1<br>FROM table<br>WHERE col1=VALUE AND col2=VALUE | SELECT *<br>FROM Contact<br>WHERE LastName = 'Adams' AND FirstName = 'Mary' |
| OR | The OR operator is used to combine multiple conditions in an SQL statement's WHERE clause. | SELECT col1<br>FROM table<br>WHERE col1=VALUE OR col2=VALUE | SELECT *<br>FROM Contact<br>WHERE LastName = 'Adams' OR FirstName = 'Mary' |
| AND / OR (Parentheses) | Example of using both AND and OR in a WHERE clause, with parentheses | -- | SELECT * <br>FROM Contact<br>WHERE LastName = 'Adams' AND (FirstName='Carla' OR FirstName='Mary') |
| BETWEEN | The BETWEEN operator selects a range of data between two values (a minimum and maximum). The values can be numbers, text, or dates. | SELECT colname<br>FROM table<br>WHERE colname BETWEEN value1 AND value2 | SELECT *<br>FROM BillOfMaterials<br>WHERE PerAssemblyQty BETWEEN 2 AND 4 |
| IN | The IN operator is used to compare a value to a list of literal values that have been specified. | SELECT colname<br>FROM table<br>WHERE colname IN (value1, value2) | SELECT *<br>FROM Contact<br>WHERE LastName IN ('Abel','Smith') |
| NOT | The NOT operator reverses the meaning of the logical operator with which it is used. Eg: NOT EXISTS, NOT BETWEEN, NOT IN, etc. This is a negate operator. | SELECT colname<br>FROM table<br>WHERE colname NOT IN (value1, value2) | SELECT ProductID, VendorID, StandardPrice<br>FROM ProductVendor<br>WHERE ProductID NOT IN (317, 318)* |
| IS NULL | The NULL operator is used to compare a value with a NULL value. | -- | SELECT *<br>FROM table<br>WHERE column IS NULL; |
| LIKE | LIKE (is technically not an operator, but a predicate) is used to compare a value to similar values using wildcard operators (i.e., LIKE is used to search for a specified pattern in a column). | SELECT colname<br>FROM table<br>WHERE colname LIKE [pattern] | SELECT colname<br>FROM table<br>WHERE colname LIKE 'A%'; |
