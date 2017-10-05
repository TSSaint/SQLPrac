# SQLPrac

A repo wherein I am refreshing my knowledge of SQL and querying.

Querying in SQL is powerful and relatively flexible. It also leaves data untouched, which allows for data to be parsed in many different ways.

## Components in SQL
There are two important components in SQL databases:
1) Data - information
2) Schema - establishes how information should be stored/divided and relates to others. These are called "tables".

Typically, tables are similar to spreadsheets with rows and columns.
Often or not, data is stored individually.

Rows are defined individually. Rows can be manipulated and parsed at will, allowing for flexible querying.

ex.
Product | Size | Quantity
Shirt      M        1      
Cap        M        2
Shoes      11       3

## Types of Data
TEXT
Typically store names / descriptions

NUMERIC
Usually store quantities in numbers

DATE 
Only store anything time-related

It's important to accurately define data types in your database. For example, consider a table of:
Ex.
Name | Price | Quantity
Xbox   350     11
PS4    400     21
Wii U  300     192

Where datatypes are:
Txt.   Num.    Num.

If all the datatypes were "TEXT", a query that sorts the items in descending order would result in:
Quantity
21
192
11

To avoid confusion, it's important to accurately define data types. 
This way, data can be parsed accurately, safely, and efficiently.