# SQL Social Network 👨‍👩‍👧‍👦
<!--
*Difficulty:* ★★★★☆  
*Runtime:* **2.5 hours**  
-->

### Release 0. Design
Let's design a social network database where users **(id, name)** can give each other likes. Create tables for storing necessary information, fill them with test data (at least 10-15 lines), and save the result in an .sql file.

This can be done using the **[pg_dump:](https://postgrespro.ru/docs/postgresql/9.6/app-pgdump#pg-dump-examples) (rus)** ```pg_dump database > database.sql ```  
or find the tables' creation commands and copy them into a new file.
```
SHOW CREATE TABLE `Users`;
SHOW CREATE TABLE `Likes`;
```

### Release 1. Obtain data
Write queries to display all of the following in different lines:
-   user-id
-   name
-   number of received likes
-   number of likes given
-   mutual likes  

Save the resulting code to an sql file.

### Release 2. Mutual likes
For **release 0**'s schema, write an sql-query, which displays a list of all users who liked users **A** and **B** (with arbitrarily assigned ids) but not user **C**. Save the resulting script to an sql file.

### Release 3. Let's complicate the structure

Add **"Photo"** and **"Comments on Photo"** entities. Think about how to connect then and implement this relationship using external keys. 
Change your database's structure so you can like not only users but also photos and their comments. 

Consider the following restrictions:
-   users cannot like the same entity twice
-   users have the right to remove likes
-   you should know an entity's number of likes and display a list of likers (users)
-   in the future, you may need to add new likable entities

Save the resulting code in a sql file.

### Release 4* Mutual likes?!

For **release 3**'s schema, write an sql-query, which displays a list of all users who liked users 
**A** and **B** (with arbitrarily assigned ids), but not user **C**. Consider not only users but also their photos and comments. Save the resulting code to an sql file.
**This release is optional.*

### Release 5*. Hater 80lvl
Adjust your database's structure so that users can give each other not only likes but also dislikes. 
Consider the following restrictions:
-   users cannot dislike themselves
-   users cannot dislike the same entity twice
-   users have the right to remove their dislikes
-   like and dislike are mutually exclusive (users' entities can have only one of two)
-   you should know an entity's number of dislikes and display a list of dislikers (users)
-   in the future, you may need to add new dislikable entities 

Save the resulting code to an sql file.
**This release is optional.*
