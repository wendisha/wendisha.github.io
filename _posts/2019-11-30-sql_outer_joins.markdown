---
layout: post
title:      "SQL: Outer Joins"
date:       2019-11-30 15:48:11 +0000
permalink:  sql_outer_joins
---


In our second part of learning how to work with the SQL Join clause, we will focus on the Outer Joins. The first part, where we talk about Inner Joins, can be found [here](https://dev.to/wendisha/sql-inner-join-4eb2).

So, what is an Outer Join? Just like an Inner Join, an Outer Join is used to query databases combining tables based on a related column. Different from an Inner Join, an Outer Join could be used to return data that is not common among tables.

There are various types of Outer Joins, and we will explain them based on examples. For said examples, let's consider the same two tables of our previous post:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/5dls2zpfi2twd3vi43md.png)

**Full Outer Join:** This version of the Join clause will return all records from both tables, adding ``null`` where a match isn't present. In the next image we use the Venn Diagram to graphically explain the result of joining these two tables with the Full Outer Join clause, or simply called Full Join.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/cllik0rma34djo89z3st.png)

Let's say we want to know which doctor checked our pets, and the date they were seen. In this case, we would want to perform an Outer Join on these tables to return this information, and the syntax would look like the following:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ae52xzs7qw6ose7bfj6m.png)

Since Full Joins are not supported on MySQL, here's the syntax to be used in this [DBMS](https://www.techopedia.com/definition/24361/database-management-systems-dbms):

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/v6mwalyfsbsu4qtsr60e.png)

The results would be the following:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/yubf2mstzxgc2s05qyk6.png)

As you can see, we have two rows for our cat Daisy, who was seen by two different doctors and/or on two different dates. Our fish Jules has not been seen, that's why it doesn't return any information about a doctor or date, and these fields are filled with ``null``.

**Left Outer Join:** This Join, also known as Left Join, returns all records from the first table (or the **left** table) with the matches from the second table (or **right** table), adding ``null`` where no matches are found.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/r9ksuftac6qpvp1eq3rr.png)

If we want to see which species have been seen by which doctors, we can query our database with a Left Join to return these results.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/e9ov953z7sffts877ccl.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/9idh4hinhu6s0y2ktnnz.png)

We see all records from our pets table with it's corresponding matches from the checkups table, and blank spaces for those records from pets without a match in checkups. Remember, these blank spaces are to be considered as ``null``.

The **Right Outer Join** works the same as the Left Join, but inverting the tables: it will return all records of the right or second table, with matches from the left or first table, and ``null`` values where no match is found. If we were to replace the previous query with a Right Join, it would return the same results, except for the last row, because the ``null`` value corresponds to the checkups table.

**Left Outer Join with WHERE clause:** Remember when we mentioned at the beginning of this post that one difference between the Inner Join and the Outer Join is that the last one allows us to return values that are not matches between both tables? This can be achieved by adding a WHERE statement to our query.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/2s6o5v7leg053eoep7em.png)

So let's say we want to see which of our pets has not had a checkup. We know, from our previous examples, that for our fish Jules we received ``null`` values when trying to return similar data. We could use this value to comform our new query, so that the result will show that Jules has not been checked:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/a7jylcx4qmz0pk2ca555.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/621gev3fne6u1817bnof.png)

Pretty cool, huh? And the same goes for the **Right Outer Join with a WHERE clause**.

**Full Outer Join with WHERE clause:** This is the type of Join that allows us to  return the records unique to both tables. In other words, we would be getting everything but the matches.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/eru1bkd2v9jwov0ags50.png)
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/pnnk2z8sv8538yby1b63.png)

We select the columns of our interest from the **pets**  table, Full Outer Joining **checkups** on the column they both have in common, WHERE these column's records are ``null``, meaning where they don't have a value.

Again, MySQL does not support Full Joins, so the query would be:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/uz37fvjsl8ig6p21tpd5.png)

And our results:

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/otdbr14luuqt5oxzu9yj.png)

Our tiny example only includes one record that is unique to one of the tables, the **pets** table to be exact, so this is the reason for our result.

Outer Joins are a powerful tool at our disposal, and hopefully these lines brought some clarity on the matter.
