---
layout: post
title:  "SQL Bind Variables"
date:   2012-12-10 13:07:09
excerpt: "Please read carefully"
categories: blog
---

### Please read carefully

I hate people who try and tell me that my development techniques are wrong. Everyone is different. It was part of the motivation for my previous post on [ Frameworks](http://molovo.co.uk/blog/frameworks). That said, I'm going to break my golden rule, and give you all a very important instruction:

> #### If you don't know what SQL bind variables are, then do not write any SQL. **Ever**.

This is important. Having come into web development from a database administration background it amazes me how many back end developers are writing SQL without knowing what SQL bind variables are, or how to implement them. So to begin, here's a quick and dirty explanation of what they are, and why they are important.

#### Bind variables

Bind variables essentially reduce the number of times a query needs to be parsed, and reduces the number of queries held in database memory.

Take the following 3 statements:

    SELECT column FROM table WHERE key = 1;
    SELECT column FROM table WHERE key = 2;
    SELECT column FROM table WHERE key = 3;

All three are essentially doing the same thing, but because the values are included literally, each time one of them is run the database will parse the statement, store it in memory and then run it. If either of the three above are run again, it can pick it up from memory without the need to parse. But if I run:

    SELECT column FROM table WHERE key = 4;

the database needs to go through the full procedure again.

If we add a variable ':value' :

    SELECT column FROM table WHERE key = :value;

This gets stored in memory, and we can assign absolutely any value we want before running the statement, and after the first run, it will always be picked up from memory, greatly reducing the load on the database. Also, as the statement is only stored in memory once, the memory usage of the database will also be reduced greatly.

If you need to run the same statement a large number of times, say a login script for an application with 10,000 users, then without bind variables, you would be parsing this statement and storing it in the database memory *10,000 times*. With a bind variable it would be once. 

This is not something that should be left to your database administrator. SQL can be tuned at a database level, and any DBA worth his salt will be doing this for you, but if the application is producing inefficient SQL, no amount of tuning will improve things.

They aren't even that difficult to implement. All server-side languages include ways of applying bind variables to your SQL. In vanilla PHP it would be done as so:

    // prepare the statement
    $stmt = $this->_db->prepare("SELECT column FROM table WHERE key = :value");
    $stmt->bindParam(':value', $value);

    // select one row
    $value = 1;
    $stmt->execute();

    // select another row with a different value
    $value = 2;
    $stmt->execute();

I'm not saying that you should include bind variables for every single statement, but I do thoroughly recommend it for any statement that will be run multiple times. What I *am* saying, is that until you take the time to understand them you cannot know where they would be useful, and you will more than likely end up with a very unhappy database.