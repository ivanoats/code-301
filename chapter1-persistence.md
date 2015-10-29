# Persistence

It would be frustrating and disappointing if all your data kept disappearing!  Web applications need a way to store data. This process is also called persistence. Persistence is typically on the server, but can also be in the browser.

---
# What is a Database?

A database is an organized collection of data. Database Management Systems (DBMS) have a wide variety of internal architectures, but typically they are composed of tables of data. Another rapidly growing alternative are documents. We will stick to table based databases because they are still the most common.

## Database Tables

A table has columns and rows, like this:

**Employees**:

| id | Name   | Age | Billing Rate | Hours |
|----|--------|-----|-------------:|-------|
| 01 | Keesha | 28  | 75.00        | 40 |
| 02 | Mark   | 42  | 100.00       | 20 |
| 03 | Pam    | 35  | 123.35       | 10 |

Each column is a particular type of data, like name, or age. The types may be anything, but usually they are specific, like text, or numbers. In our example above, the billing rate is a floating point number, and the age is an integer.

Each row is also called a record. It contains each individual or particular value. It is usually best practice for each record to have a unique identifier. In our example above, it is the 'id' column.


---
# Structured Query Language (SQL)

Structured Query Language (SQL) is a special-purpose programming language designed for managing data. Developers use SQL for inserting new data, retrieving data, updating data, and deleting data. 

SQL statments are made up of clauses, expressions, and predicates as you can see in the image below:

![sql update statement](images/SQL_ANATOMY_wiki.svg)

## Queries
A query retrieves data from one or more tables, or expressions.

```sql
SELECT isbn,
       title,
       price,
       price * 0.06 AS sales_tax
 FROM  Book
 WHERE price > 100.00
 ORDER BY title;
 ```
---

## Data Definition Language

Data Definition Language (DDL) manages the table and index structure.

The most basic items of DDL are the CREATE, ALTER, RENAME, DROP and TRUNCATE statements. Here's an example of create:

```sql
CREATE TABLE example(
 column1 INTEGER,
 column2 VARCHAR(50),
 column3 DATE NOT NULL,
 PRIMARY KEY (column1, column2)
);
```

## Data types


# What is a Model?

Models are, in essence, a simplified description of a real world object. A database table is a simple model.

In object-oriented code, models are objects. The columns correspond to properties. Here's an example constructor in JavaScript:

```javascript
function Employee(name, age, billingRate, hours) {
  this.name        = name;
  this.age         = age;
  this.billingRate = billingRate;
  this.hours       = hours;
}
```

Models can also have behavior. In our example, you could have a function (method) that calculates the amount owned per employee. It would be Billing Rate times Hours. In JavaScript it looks like:
```javascript
Employee.prototype.amountOwed = function (billingRate, hours) {
  return billingRate * hours
}
```

---

# Modeling your Data with SQL

---


