# SQLPrac

A repo wherein I am refreshing my knowledge of SQL and querying.

Querying in SQL is powerful and relatively flexible. It also leaves data untouched, which allows for data to be parsed in many different ways.

## Components in SQL
There are two important components in SQL databases.
1) Data - information
2) Schema - establishes how information should be stored/divided and relates to others. 

Databases organize information into structures that are called "tables".

Typically, tables are similar to spreadsheets with rows and columns.
Often or not, data is stored individually.

Rows are defined individually, and are singular entries on a table/column. Rows can be manipulated and parsed at will, allowing for flexible querying.

Ex. <br>

| Product       | Price | Quantity  |
| ------------- |:-----:|----------:|
| Shirt         |  M    |  1        |
| Cap           |  M    |  2        |
| Shoes         |  11   |  3        |

## Types of Data
TEXT
Typically store names / descriptions. 
Usually "strings" or the sort

NUMERIC
Usually store quantities in numbers, such as "integer"/"float"

DATE 
Only store anything time-related
Always stores in chronological order

### The 'id' Identifier

'id' is a unique identifier for some database entry. This specifies that each entry is not a duplicate, and can be isolated when needed.

---

It's important to accurately define data types in your database. For example, consider a table of:
Ex. <br>

| Product       | Price | Quantity  |
| ------------- |:-----:|----------:|
| Xbox One      | 350   |  11       |
| PS4           | 400   |  21       |
| Wii U         | 300   |  192      |


Where datatypes are:
Txt.   Num.    Num.

If all the datatypes were "TEXT", a query that sorts the items in descending order would result in a confusing result of:
Quantity
21
192
11

To avoid confusion, it's important to accurately define data types. Additionally, numeric operations can never be done with "TEXT" datatypes. A logical approach towards storing numbers assumes that some kind of operation will be done later. Otherwise, this could not be done. Data can be parsed accurately, safely, and efficiently when named properly.

# A Note on Querying

### Vocabulary/Syntax/Keywords

```
SELECT * FROM <some_table>;
```

Lines of SQL code are called statements or queries (executing SQL, running a query).
Syntactically, reserved words are used in combinations.

Ex.<br>
SELECT * FROM books; will take all of the information from the table books.
Keywords SELECT tells SQL to choose specifics, and FROM tells SQL where to look. The semicolon acts as an ending, telling the program to stop running a query.

Note: querying large datasets will hurt performance for the user and others, hence the need for specific and confined querying.

### Commenting
In order to single out lines of code to be reviewed internally (perhaps as notes or instructions), add two dashes:
```
-- this is a commented-out SQL line and won't be executed, but the next line will
SELECT * FROM table;
```

# Specific Querying Methods
We can retrieve small portions by changing the syntax of the query to choose specific columns. This will return all data in default order.

### Single Column
```
SELECT <some_column> FROM <some_table>;
```

Ex.<br>
SELECT * FROM x #-> Gets all Data <br>
whereas: <br>
SELECT y FROM x #-> Gets only y

### Multi-Column
We can select multiple pieces of data with one query by separating the names of the columns with a ','. The order of the columns dictate the order of the information returned.
Ex.<br>
SELECT y, z FROM x #-> Gets only y and z

# Aliasing
We can change the names of columns in SQL by using the "AS" keyword. This will never change the actual name of the column - only the report displays the alias.
Ex. <br>
SELECT <some_column> AS <New_column> FROM <some_table>; #-> returns New_column




# Reserved Words/'Commands' in SQL

### SELECT
Choose some specific column title.
Ex.<br>
SELECT * FROM table; #-> returns all info in table

### FROM
Choose a specific table to be queried.
Ex.<br>
SELECT * FROM <table> #-> retusn info from <table>

### AS
Allows the aliasing of column names. Multiple words are not allowed - they must be strung together in quotes "<alias>".
Ex.<br>
SELECT x AS X FROM table; #-> returns X