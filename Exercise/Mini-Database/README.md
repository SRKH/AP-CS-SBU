# Mini-Database

## Introduction

There are many types of databases which are used around the world to hold and grab data; some popular types are **SQL**, **NoSQL** and **Graph**.

Each of them keep data in a different way; for example, SQLs hold data in **tables**, NoSQLs in **collections** and Graphs in **graphs**.
They might store the data as **files in a hard drive**, as **objects in RAM** or **both**.

Your task is to implement a _**minimal SQL-like database which stores data as files in hard drive**_.

## Definitions

### Database Table
Just like a normal table, it consists of **columns (fields)** and **rows (objects)** where columns show the structure of the table and each row is an information which conforms to that structure.
Each column has a **name**, a **type** and a **fixed size** and at least one these columns must be a [primary key](#primary-key).

A table is similar to a **class** in Object-Oriented programming where each column is a field of that class and each row is an object of it.

### Primary Key

*(TODO primary key definition)*

### Schema
The definition of the columns of each table. Mainly, it defines the **name**, **type** and **size** of each column but there are many other attributes it can define for a column, which we will explain later;
for example, a "User" table with columns "id" of type *Integer (4 bytes)*, "full_name" of type *String (100 bytes or characters)*, "email" of type *String (100 bytes or characters)*, "gender" of type *String (10 bytes or characters)* and "current_age" of type *Integer (4 bytes)*.

The schema of a table, as a result, can also show the size of the **rows** of a table (by adding up all the column sizes);
for example, the size of the rows of the table above will be 4 + 100 + 100 + 10 + 4 = 218 bytes.

A visual example of this schema is shown in figure 1. A sample of resulting table of this example schema is shown in figure 2.

<table>
  <tr>
    <td>
      <img src="https://github.com/SRKH/AP-CS-SBU/raw/exercise-4/Exercise/Mini-Database/database-schema-example.png" alt="Database Schema Example" height="150"/>
    </td>
    <td>
      <img src="https://github.com/SRKH/AP-CS-SBU/raw/exercise-4/Exercise/Mini-Database/database-table-example.png" alt="Database Table Example" height="130"/>
    </td>
  </tr>
  <tr>
    <td>
      Figure 1
    </td>
    <td>
      Figure 2
    </td>
  </tr>
</table>

## Submission Details

This exercise consists of **two phases**, each with their own deadline, and you should submit different components of this task in each of them.

*(TODO explain exactly what they should submit for each phase)*

## Components

Your program needs to have the following components:

### Engine

The main part of your database, also called *engine*, must be able to `create` tables with a specific schema,
and `insert`, `update`, `delete` and `search` data in a particular table.

It should create a file `schemas` to store each table's schema. The way you're going to store the schemas in the file is up to you.

#### Functionality Details

* `create`:
It should receive a table name and a schema definition, and do the following things:

  1) Save the schema in the `schema` file,

  2) Create a folder with the name of the table and creating two files inside the folder, `db` and `index`. These files will be explained later.

* `insert`:
It should receive a table name and some data, and should do the following things:

  1) Validate that the given data conforms to the table schema,

  2) Serialize and insert the given data in the `db` file of the table folder.
     It should write the data **sequentially**; so for example, in the `db` file of the example table above, the first 218 bytes will be the first row, the second 218 bytes will be the second row and so on.
     Note that all rows of a table have the same size (sum of column sizes).

     *(TODO explain the optional db file-splitting for better performance)*

  3) In `index` file of the table folder, write **the primary key of the row** and **the exact position of it's data in the `db` file**.

     *(TODO explain why this is needed)*

* `update`:
*(TODO)*

* `delete`:
*(TODO)*

* `search`:
*(TODO)*

### User Interface

A simple menu needs to be shown to the user in the terminal, asking for an input command.

Commands are **JSON strings**, so your program needs to parse JSON to understand what the user wants.

Different types of commands are described below:

#### Schema
The user gives a **table name** and a **schema definition** and expects **a table with the given name and schema** to be created.

#### Insert [*](#footnote1)
The user gives a **table name** and **some data** and expects **one object** with the given data to be created in that table.

#### Update [*](#footnote1)
The user gives a **table name**, a **primary key** and **some data** and expects **one object** of that table, which has the given primary key, to be updated with the given data.

#### Delete
The user gives a **table name** and a **primary key** and expects **one object** of that table, which has the given primary key, to be deleted.

#### Search
The user gives a table name and either a **primary key** or a **number of results**.

If given a primary key, the user expects **one object* of that table, which has the given primary key, to be printed in the terminal in a **JSON object format**.

If given a number of results, the user expects **the first that number of objects** of the table to be printed in the terminal, in a **JSON list format**. The order of the objects must be the order which they have in the `db` file.

*(TODO command JSON specification)*

<a name="footnote1">*</a> *If the given data did not conform to the table schema, you should print an appropriate error in the terminal.*

## ⏳ Deadline

### Phase 1
May 5th, 2020

### Phase 2
May 12th, 2020

## Bonus Task

* The `search` functionality may receive a column name **other than the primary key** and a value, and return **all** the objects which have the given value for the given column name. *(TODO give an example of such a query)*
