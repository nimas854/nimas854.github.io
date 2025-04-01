---
layout: page
title: Unit 3
description: PostgreSQL
image: assets/images/pic03.jpg
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Unit 3</h1>
		</header>

<!-- Content -->
<h2 id="content">Databases: Where ACID 🧪 Isn’t Just About Chemistry 😁</h2>
<p>Ever wondered what keeps your database from turning into a chaotic mess? Meet ACID properties—no, not the kind that melts your desk 🤧, but the ones that keep your transactions safe and sound. Let’s break it down before your brain crashes like a badly handled transaction.🫨</p>

<br>
<h4 id="Content"> ACID: The Four Horsemen of Database Integrity</h4>
<p>1. Atomicity – All or Nothing! 🤝
A transaction is like ordering a pizza🍕. If the delivery guy forgets the toppings (or worse, the pizza), you reject the whole thing. In databases, if one part of a transaction fails, nothing gets saved. No half-baked pizzas here.🤧</p>
<p>2. Consistency – Keeping Things Real🫨
Ever played Jenga? Imagine if after every turn, the game magically repaired itself to avoid collapse. That’s consistency. No matter what happens, the database stays in a valid state—no floating records or random data ghosts.🤯
</p>
<p>3. Isolation – Stay in Your Lane 🧐
Multiple transactions working together can be a nightmare. It’s like two people trying to edit the same Google Doc at once—someone’s changes might get overwritten. Isolation makes sure each transaction happens independently, no unwanted collisions.🐼
</p>
<p>4. Durability – No Takebacks! 😀
Once a transaction is committed, it’s permanent. Think of it like posting an embarrassing tweet—no power outage or system crash can take it back.😨</p>
<br>
<h4 id="Content"> SQL: The Language of Databases (and Frustration)</h4>
<p>SQL (Structured Query Language) is the magic spell you chant to communicate with databases. It comes in different flavors:</p>

<p>DDL (Data Definition Language) – Creates and structures your tables (like the architect).</p>

<p>DML (Data Manipulation Language) – Edits, deletes, and adds data (like the handyman).</p>

<p>Constraints – The rules that keep your data from turning into nonsense (like a strict teacher).</p>
<br><br>


<h4 id="Content">🎭 SQL Constraints: Because Rules Matter</h4>
<p>Databases have rules, just like real life. Here are a few that keep your data from going wild:</p>

<p>NOT NULL – No empty seats at the table. Every column needs data!</p>

<p>UNIQUE – No clones allowed! Every entry must be different.</p>

<p>PRIMARY KEY – The one unique ID that makes each row special (like your CID number).</p>

<p>FOREIGN KEY – Connecting tables like social networks (but with fewer cat videos).</p>

<p>CHECK – “Are you sure?” This ensures valid data (e.g., age can’t be -5).</p>

<h4 id="Content">FACTS</h4>
<p>Database Schema: The logical design of the database (the architect's plan).</p>
<p>Database Instance: A snapshot of the database at a given time (like a messy dorm room before cleaning day).</p>

<h4 id="Content">So, we are given a taask to make ER Module to a Relational Scheme </h4>
<img src="Screenshot 2025-03-21 224615.png">
<p>Here is my ER model and I have converted it to relational scheme in a perfect way 😎😎 litterly this is the hardest ER module where other got simple ER model 🤣(i'm the only one with hardest question)</p>b
<img src="4288c1c6-d844-4aec-986f-7e67dcfaf045.jpg"><br>

<h2 id="Content">Relational Algebra: The Secret Code of Databases!🤫</h2>
<p>Imagine you’re at a restaurant. You ask the waiter for all pizzas on the menu, but only the ones with extra cheese. That’s basically what relational algebra does—it’s the secret language databases use to filter, combine, and organize data! Let’s break it down in the most entertaining way possible.</p>


<h4 id="Content">What is Relational Algebra?</h4>
<p>It’s a functional query language that helps databases understand what information you want. Think of it like a menu of commands you give to get specific data.</p>

<h3 id="content">The Main Operations (a.k.a. Superpowers!)<h3>
<h4 id="Content">1. Selection (σ) – The picky eater 🍕</h4>
<p>This operation picks only the rows (tuples) that meet a certain condition.
📌 Example: "Give me all students whose ID is 12345."
💻 Code: σstudentNo=12345(Student)
(Sounds fancy, but it’s just SQL's SELECT * FROM Student WHERE StudentNo = 12345)</p>
<h4 id="Content">2. Projection (π) – The minimalist 🎭</h4>
<p>It chooses only specific columns (attributes), ignoring the rest.
📌 Example: "I just need names and IDs, no addresses!"
💻 Code: πName, StudentNo(Student)
(Like SQL’s SELECT Name, StudentNo FROM Student)</p>
<h4 id="Content">3. Union (∪) – The friendly merger 🤝</h4>
<p>It combines two tables by stacking all unique rows together.
📌 Example: "Show me all students from Class A and Class B."
💻 Code: ClassA ∪ ClassB
(Same as SQL’s SELECT * FROM ClassA UNION SELECT * FROM ClassB)</p>
<h4 id="Content">4. Intersection (∩) – The common ground ✋</h4>
<p>Finds the rows that appear in both tables.
📌 Example: "Show me students who are in both Football and Basketball teams."
💻 Code: Football ∩ Basketball
(Like SQL’s SELECT * FROM Football INTERSECT SELECT * FROM Basketball)</p>
<h4 id="Content">5. Difference (-) – The eliminator 🚫</h4>
<p>Finds rows that exist in one table but not in another.
📌 Example: "Show me students who are in Football but not in Basketball."
💻 Code: Football - Basketball
(Like SQL’s SELECT * FROM Football EXCEPT SELECT * FROM Basketball)</p>
<h4 id="Content">6. Cartesian Product (×) – The chaotic mixer 🎲</h4>
<p>It combines every row from one table with every row from another. (Warning: Can get messy fast!)
📌 Example: "Match all students with all courses."
💻 Code: Students × Courses
(Like SQL’s SELECT * FROM Students CROSS JOIN Courses)</p>
<h4 id="Content">7. Join (⋈) – The power couple 💑</h4>
<p>It combines two tables based on a common column.
📌 Example: "Match students to their departments."
💻 Code: Students ⋈ DeptID=Dept.ID Departments
(Like SQL’s SELECT * FROM Students JOIN Departments ON Students.DeptID = Departments.ID)</p>

<h3>Writing SQL Queries Like a Pro (Or at Least Not Like a Noob)😎</h3>

<p>1. Selecting All Entries (Because We’re Nosy!)🫨</p>
<p>SELECT * FROM Users;</p>

<p>2. Selecting Specific Columns (For When You’re Picky)🤧</p>
<p>SELECT Username, F_Name, L_Name FROM Users WHERE Gender = 'Male';</p>


<p>3. Filtering Data Like a Pro😁</p>
<p>SELECT * FROM Users WHERE Gender = 'Male' AND DOB > '1990-01-01';</p>

<p>4. Ordering Data (Because We Love Organization!)🙂</p>
<p>SELECT * FROM Users ORDER BY L_Name DESC;</p>



<h3>Aggregate Functions: Ignoring NULL Like an Ex😏</h3>
<p>When SQL performs aggregate functions like SUM() or AVG(), it straight-up ignores NULL values. Imagine counting the number of people in a room but ignoring anyone who’s standing in a corner. That’s SQL for you.</p>



<h3>The Group By Clause: SQL’s Way of Sorting the Party😁</h3>
<p>Ever been at a party where people naturally group themselves? The tech nerds, the food lovers, the ones glued to their phones? That’s what the GROUP BY clause does—it neatly sorts data into groups, making it easier to analyze.</p>


<h3>The HAVING Clause: Like a Bouncer at the Club🔐</h3>
<p>The HAVING clause filters groups the way a bouncer filters people at a nightclub. If you don’t meet the conditions (e.g., average salary > $42,000), you’re not getting in. Sorry, SQL has standards.</p>

<h3>Subqueries: SQL’s Inception Moment😀</h3>
<p>A subquery is a query inside a query. It’s like ordering a burger and getting a surprise mini burger inside. Subqueries help SQL find answers in layers, making sure your data is exactly what you need (or more complicated than necessary).</p>

<h3>Modifying Databases: The Power Moves</h3>
<p>DELETE: Like throwing out old clothes you no longer need.🤧

INSERT: Like adding new clothes to your wardrobe.🧐

UPDATE: Like giving your favorite t-shirt a fresh coat of fabric paint.🖌️</p>

<h3>Window Functions: SQL’s CCTV👀</h3>
<p>Window functions let you analyze data while still keeping all rows visible—kind of like having CCTV footage of every transaction. Unlike regular aggregate functions, they don’t lump data together but allow you to peek at trends over a dataset.</p>

<h4 id="Content">Why This Matter</h4>
<p>Understanding SQL isn't just about writing queries; it’s about thinking logically🤔, solving problems🤯, and handling complexity like a pro😎. In the real world, everything is about data—from your Netflix recommendations to your bank transactions. Mastering SQL gives you a superpower🦸: the ability to make sense of the digital world around you.🕷️

Plus, let’s be honest, being able to troubleshoot a database issue makes you look like a wizard to non-tech folks🧙‍♂️. And who wouldn’t want that? </p><br>


<h4 id="Content">Personal Growth and Reflection</h4>
<p>Thanks to Miss! 😀 With the help of this unit, I can now use PostgreSQL like a pro (thanks to Miss’s notes and ChatGPT 😉). Not only that, but I also know how to create ER diagrams, convert them into schemas, and write SQL queries with ease. 😊</p><br/>

