
MySQL is a relational Database Management System, i.e. it deals with tables.

## Creating a Database or Table

### Databases

A database is created by with the `CREATE DATABASE` command.

```mysql
CREATE DATABASE myDB;
```

The database is then selected using the `USE` command.

```mysql
USE MyDB;
```


### Tables


Tables are created using the `CREATE TABLE` command.

```mysql
CREATE TABLE MyTable (col_1 datatype, col_2 datatype, ..., col_n datatype);
```
> [!example]
> ```mysql
> CREATE TABLE MyTable (id INT, name VARCHAR(10), DOB DATE);
> ```
> 

There are different types of datatypes

| <center><font color="#9bbb59">Datatype</font></center> | <center><font color="#9bbb59">Use</font></center>                                                                     |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| `INT`                                                  | Stores an Integer                                                                                                     |
| `DECIMAL(x, y)`                                        | Stores a floating point value. <br>`x` is the total  number of digits,<br>`y` is the  digits after the floating point |
| `VARCHAR(x)`                                           | Stores a string.<br>`x` is the number of characters                                                                   |
| `DATE`                                                 | Stores a date.                                                                                                        |

## Insertion into Tables

To insert a record into the table we use the `INSERT INTO` command.

```mysql
INSERT INTO MyTable VALUE (col_1_value, col_2_value, ..., col_n_value);
```

The above is when we want to insert a singular record into the table. If we want to insert multiple records at once, we'd do the following:

```mysql
INSERT INTO MyTable VALUE (record_1), (record_2), ... , (record_n);
```

> [!error]
> If we enter less values in the `VALUE` argument, it throws an error.
> 
> For example, if Mytable has 2 columns: `id` and `name`, and we write `INSERT INTO MyTable VALUE (1);` that is the only the `id`, it would give us an error.

To overcome the above error, we can write:

```mysql
INSERT INTO MyTable (id) VALUES (1);
```

The first parenthesis are the columns we want to insert the data into, and the second pair are the values of the columns. The remaining columns' value is set to `NULL`.

## Updating Values in a Table

