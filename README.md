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

ex.
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

It's important to accurately define data types in your database. For example, consider a table of:
Ex.
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

Lines of SQL code are called statements or queries (executing SQL, running a query).
Syntactically, reserved words are used in combinations.
Ex.
SELECT * FROM books; will take all of the information from the table books.
Keywords SELECT tells SQL to choose specifics, and FROM tells SQL where to look. The semicolon acts as an ending, telling the program to stop running a query.

Note: querying large datasets will hurt performance for the user and others, hence the need for specific and confined querying.