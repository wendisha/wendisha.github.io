---
layout: post
title:      "SQL: Inner Join!"
date:       2019-11-30 15:44:31 +0000
permalink:  sql_inner_join
---

In SQL we have various powerful clauses that make managing databases possible, but one that usually brings confusion along with it's functionality, is the JOIN clause.

The JOIN clause is used in a relational database to select records from two or more tables that share at least one column in common. There are different ways of joining tables, and in this post we will be discussing, through the use of an example, the one corresponding to the INNER JOIN.

INNER JOIN will compare the specified tables and select those rows that have matching values. It could be considered the default JOIN type, since we would get the same result without specifying the keyword INNER.

It's syntax is the following:

![Inner Join syntax](https://thepracticaldev.s3.amazonaws.com/i/djw2ld9fjvp0pmjlrhv0.png)

In the SELECT clause, we specify the columns we want to select, by chaining them to the table they correspond. Pro-tip: we only do this for columns that are not specific to one table. If we want to select a column that is specific to just one table, we don't have to specify the table name.

Now let's explain how it works, based on an example. The following image shows the tables to be considered.
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/1vausock9nmpr5x2uagc.png)

In this example, we see that in the pets table we have a pet_id column that is common to the checkups table. The pet_id column in the pets table is referred to as [Primary Key](https://www.w3schools.com/sql/sql_primarykey.asp), and the one in the checkups table as [Foreign Key](https://www.w3schools.com/sql/sql_foreignkey.asp).

The next image graphically explains the result of joining these two tables with the INNER clause, referencing the Venn Diagram.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/krn2h7ux7dtbg8l17j27.png)

Now, considering the tables above, if we wanted to get our pets names, their species and the date they had a checkup, the query would look like this:

![Example query](https://thepracticaldev.s3.amazonaws.com/i/dqrfb0j7ulfovfdlgbsu.png)

Let's break it down: We select the columns we want, and since they are unique columns to each of the tables, we don't have to chain them to their tables. We select them from pets, and join the checkups table on the column both tables have in common (remember, the INNER keyword is optional). We could've selected from checkups and joined pets, as long as we join them on their common field, we would be getting the same result.

In a following post, we'll discuss the other ways available to join tables. See you there!

E.T.A.: The following post, where we discuss Outer Joins, can be found [here](https://dev.to/wendisha/sql-outer-joins-2cj7).
