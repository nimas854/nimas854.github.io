---
layout: page
title: Unit 5
description: Advanced Database Design
image: assets/images/pic01.jpg
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Unit 5</h1>
		</header>

<!-- Content -->
<h2 id="content">Databases Gone Wild: Lessons 12 & 13 and How to Actually Design Things Right😎</h2>
<br>
<h3 id="Content">Good Database Designs – Or How To Not Destroy Your GPA</h3>
<p>You know what's harder than learning to code?
Making sure your database isn't a chaotic mess where one delete accidentally erases your ENTIRE university.
(Trust me, your professor will notice.)<p>
<h4>Main Goals of a Good Database Design🥅</h4>
<p>Relation per Entity: Each table should describe one thing — don't mix students and courses into one Frankenstein table.🤨</p>
<p>Fewer NULLs: NULLs = bad vibes. If something is often NULL, maybe make a new table for it.</p>
<p>No Spurious Tuples: JOINs shouldn't summon weird ghost data that wasn't there. (Goodbye "spurious tuples" 👻)</p>
<p>No Redundancy: Don't repeat information 10,000 times. Your database isn't a parrot🦜.</p>
<p>No Modification Anomalies: No situations where updating one row messes up everything else.🫠</p>


<h4>Examples You Should Know</h4>
<h5>University Schema Example:</h5>
<p>Tables like classroom(building, roomNumber, capacity), department(dept_name, building, budget), etc., properly separate things.</p>
<p>Bad schema example: in_dep(ID, name, salary, dept_name, building, budget) ← too much crammed into one table = BAD DESIGN.🙂‍↔️</p>


<h5> Decomposition Example:</h5>
<p>If you have a messy student(ID, name, Dept, Prog)</p>
<p>Good decomposition:</p>

<p>student(ID, name)</p>

<p>program(Dept, Prog)</p>


<h5> Anomalies Examples:</h5>
<p>Update anomaly: Change one address, forget the others = inconsistent mess.🤣</p>

<p>Delete anomaly: Delete the only order of a customer, and POOF! the whole customer is gone.😭</p>

<p>Insert anomaly: Can't add a customer unless they already placed an order = weird, right?🤧</p>

<h5>Functional Dependency Theory Basics</h5>
<p>If X → Y, then knowing X tells you Y.🤭</p>

<h6>Armstrong's Axioms:</h6>

<p>Reflexivity: If B is part of A, then A → B.🪬</p>
<p>Augmentation: If A → B, then AC → BC.🪬</p>
<p>Transitivity: If A → B and B → C, then A → C.🪬</p>

<h5>🧹 Normalization Goals</h5>


<p>1NF: No multi-valued attributes (no sets inside a field).1️⃣</p>
<p>2NF: No partial dependency on part of a key.🙅</p>
<p>3NF: No transitive dependency (don't let non-keys depend on non-keys).😶</p>
<p>BCNF: Every determinant must be a superkey.🫨</p>

<h3 id="Content">When Normalization Wasn't Enough — Advanced Chaos Control🎮</h3>
<p>Just when you thought your database was clean...
Multivalued Dependencies burst through the door.<p>

<h5>Multivalued Dependencies (MVD)</h5>


<p>If X →→ Y, knowing X allows multiple independent Y’s.🤔</p>
<h6>Example</h6>
<p>Instructors can have multiple addresses and departments.
inst(ID, dept_name, street, city) → ID →→ (street, city)</p>


<h5>Fourth Normal Form (4NF)</h5>


<p>A table is in 4NF if for every MVD, X is a superkey.</p>
<h6>Example</h6>
<p>From inst(ID, dept_name, street, city), split into:</p>
<p>r1(ID, dept_name)</p>
<p>r2(ID, street, city)</p>
<p>Result? No more repeating addresses for each department. 🎉</p>

<h5> More Normal Forms</h5>


<p>5NF (PJNF): Solves join dependencies where things are still messy after 4NF.</p>
<p>Domain-Key Normal Form (DKNF): "Perfect" design — but so complicated that even database wizards avoid it.</p>


<h5>Atomic Domains & First Normal Form (1NF)</h5>


<p>Fields must be indivisible.</p>
<h6>Example</h6>
<p>❌ One field: "Address: Thimphu, Bhutan"</p>
<p>✅ Three fields: "Street", "City", "Country"</p>

<h5> Database Design Process</h5>


<p>Start from a good E-R diagram.</p>
<p>Normalize cautiously — don't overdo it and kill performance.😗</p>
<p>Sometimes denormalization is fine for speed (e.g., data warehouses).😗</p>

<h5>Modeling Temporal Data</h5>


<p>Adding start_date and end_date columns to track valid periods.</p>
<h6>Example</h6>
<p>course(course_id, title, dept_name, credits, start_date, end_date)</p>

<h3>NOTES</h3>
<p>You can trust me and go through this note because i wrote it🤣.We already learned this in Math so Yeah! i mastered that already🗿 /p>
<img src="IMG_20250427_134219.jpg">
<img src="IMG_20250427_134223.jpg">
<img src="IMG_20250427_134229.jpg">
<img src="IMG_20250427_134231.jpg">
<img src="IMG_20250427_134237.jpg">
<img src="IMG_20250427_134239.jpg">
<h4 id="Content">Why This Matter</h4>
<p> Let's be real:
In your future job, you won't have time to explain why your database forgot half the customers after an update. 🫠</p>
<p>Proper database design means:</p>
<p>Safer updates.</p>
<p>Faster queries.</p>
<p>Less storage wasted.</p>
<p>Happier customers, bosses, and you.</p>
<p>You become the invisible hero of the project when the database Just Works™. 💪</p>
<br>

<h4 id="Content">Personal Growth and Reflection</h4>
<p>At the start of Lesson 12, I thought "Normalization" was just a fancy way to make life harder.
By the end of Lesson 13, I realized database design is like cooking:"🤧</p>
<p>Normalize = chop ingredients neatly.🔪</p>
<p>4NF/5NF = avoid cross-contamination.😲</p>
<p>Temporal modeling = know when things expire!😲</p>
<p>Mastering this stuff not only made me better at databases — it made me think more logically, patiently, and carefully about how I organize everything.
Whether it's planning a database, a vacation, or just my messy room — good structure wins.</p>
