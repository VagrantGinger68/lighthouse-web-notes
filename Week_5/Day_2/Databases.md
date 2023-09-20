## Database Normalization

Database normalization allows us to reduce duplicate data. We normalize a database by breaking off repeated information into its own table. We can then join the tables with a query when its needed.
We do this to enforce data integrity, reduce duplication, and make it easier to manage our data.

## One to Many Relationship

An example of a One to Many relationship is cars in a showroom. A car can only have one showroom, but a showroom can have many cars. 

## Many to Many Relationship

A many to many relationship could be students in a class. Students can have many classes, and classes can also have many students. There is no way to show this in a relational database so instead we have to turn the many to many relationship into two one to many relationships with a joining table.
![Many to Many ERD](https://www.datensen.com/blog/wp-content/uploads/2021/10/many-to-many-relationship-1-1024x261.png)

## Foreign Key

A foreign key is a field in one table that refers to a primary key in another table.
This is how we model relationships in a relational database. When we have a one-to-many relationship, the foreign key goes on the many side.

## ERD (Entity Relationship Diagram)

ERDs help us design the schema of a database. 
Always design a database using an ERD before writing any code. 
ERDs must include:
* Names of the entities
* Atrributes / properties for the entities
* The relations between each entity

Naming conventions for ERDs:

* Use "snake_case" for table and column names
* Pluralize tables names, column names should be singular
* Call your primary key "id"
* For most foreign keys use "table_id"