---
layout: page
title: Unit 7
description: Advanced Database Design
image: assets/images/pic04.jpg
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Unit 7</h1>
		</header>

<h1>🧠 Databases, Deadlocks & Disasters:<br> A Funny Yet Complete Guide to Transactions, Concurrency & Recovery</h1>

<p>Welcome to the crazy world of databases — where transactions are serious, locks are stubborn, and recovery is that one friend who remembers <i>everything you messed up</i>. Let’s dive into the madness of <b>Lessons 18, 19, and 20</b> — with a smile 😄, and some help from emojis.</p>

<h2> Transactions & ACID – "Do Everything or Do Nothing"</h2>

<h3>💼 What is a Transaction?</h3>
<p>A transaction is a group of operations that work as <b>one unit</b>.</p>
<p>Example: Transferring Nu.50 from Account A to B. You must:</p>
<ul>
  <li>Deduct from A</li>
  <li>Add to B</li>
</ul>
<p>If one part fails, the whole thing fails. No partial disasters allowed!</p>

<h3>🧪 ACID Properties</h3>
<ul>
  <li><b>Atomicity</b> 💣: All or nothing.</li>
  <li><b>Consistency</b> 📏: The database must stay logical and correct.</li>
  <li><b>Isolation</b> 🧍: Transactions act like they’re alone.</li>
  <li><b>Durability</b> 💾: Once committed, changes are permanent.</li>
</ul>

<h3>🔁 Simple Transaction Model</h3>
<pre>read(A)
A = A – 50
write(A)
read(B)
B = B + 50
write(B)</pre>

<h3>💾 Storage Types</h3>
<ul>
  <li><b>Volatile (RAM)</b> 🧠 – Fast, but forgets everything on crash</li>
  <li><b>Non-volatile (Disk)</b> 💽 – Survives crashes</li>
  <li><b>Stable Storage</b> 🛡️ – Ultra safe with backups</li>
</ul>

<h3>💥 Transaction Fail States</h3>
<ul>
  <li>Active 🏃</li>
  <li>Partially Committed ✅</li>
  <li>Failed 😵</li>
  <li>Aborted ❌</li>
  <li>Committed 🎉</li>
</ul>

<h3>🔃 Recovery Basics</h3>
<ul>
  <li><b>Undo</b> – Rollback changes</li>
  <li><b>Redo</b> – Re-apply changes</li>
</ul>

<h2>🔐 Concurrency Control – “Sharing is Caring... But With Rules!”</h2>

<h3>🧩 Why Concurrency Is Tricky</h3>
<p>Multiple users working on the same data = possible chaos 😬</p>

<h3>🔒 Locks</h3>
<ul>
  <li><b>Shared Lock (S)</b> 👀: Read only</li>
  <li><b>Exclusive Lock (X)</b> ✍️: Read & Write</li>
</ul>

<h3>⏳ Two-Phase Locking (2PL)</h3>
<ol>
  <li>Growing Phase 🌱 – Grab all needed locks</li>
  <li>Shrinking Phase 🍂 – Release them</li>
</ol>

<h3>😵 Deadlocks</h3>
<p>T1 waits on T2, T2 waits on T1. No one moves. <b>Deadlock 💀</b></p>

<h3>🛠 Deadlock Solutions</h3>
<ul>
  <li><b>Detection:</b> Waits-for graph + kill someone (a transaction) 💔</li>
  <li><b>Prevention:</b> Use timestamps (Wait-Die, Wound-Wait)</li>
</ul>

<h3>🔍 Lock Granularity</h3>
<p>Lock entire table 🏢 or just a row 🧍? Depends on performance needs.</p>

<h3>🔒 Intention Locks</h3>
<ul>
  <li><b>IS</b> – Intend to lock below with S</li>
  <li><b>IX</b> – Intend to lock below with X</li>
  <li><b>SIX</b> – Share now, Exclusive later</li>
</ul>

<h3>🧹 Lock Escalation</h3>
<p>Too many small locks? Upgrade to a bigger one.</p>

<h3>🪙 Concurrency Approaches</h3>
<ul>
  <li><b>Pessimistic</b> ⚔️ – Lock first</li>
  <li><b>Optimistic</b> 🍀 – Run first, validate later</li>
</ul>

<h2>💾 Recovery – When It All Goes Wrong</h2>

<h3>🧾 Logs</h3>
<p>Records every action (transaction ID, old & new value) to enable:</p>
<ul>
  <li><b>Undo</b></li>
  <li><b>Redo</b></li>
</ul>

<h3>📌 Checkpoints</h3>
<ul>
  <li><b>Sharp</b>: Pause and save ⏸️</li>
  <li><b>Fuzzy</b>: Save while running 🏃</li>
</ul>

<h3>💻 Write-Ahead Logging (WAL)</h3>
<p>Log before applying changes = safety first 🔐</p>

<h3>🧬 MVCC (Multi-Version Concurrency Control)</h3>
<ul>
  <li>Writers don't block readers</li>
  <li>Readers don't block writers</li>
</ul>

<h3>🧊 Snapshot Isolation</h3>
<p>Each transaction sees its own "version" of the DB. But beware of <b>Write Skew</b> 🪢</p>

<h3>🧠 Advanced Techniques</h3>
<ul>
  <li><b>Isolation Levels:</b> Serializable, Repeatable Read, Read Committed, Read Uncommitted</li>
  <li><b>Real-Time DBs:</b> Deadlines matter! ⏱️</li>
</ul>

<h2>🌟 Why This Matters</h2>
<ul>
  <li>No transactions → Broken data 💔</li>
  <li>No concurrency control → Data races ⚔️</li>
  <li>No recovery → One crash = total loss 💣</li>
</ul>
<p>These systems protect your data like secret agents 🕵️</p>

<h2>🌱 Personal Growth & Reflection</h2>
<p>Before this, I thought:</p>
<ul>
  <li>Transactions = shopping online 💳</li>
  <li>Locks = just for doors 🚪</li>
  <li>Recovery = therapy 😅</li>
</ul>
<p>Now, I know: Databases are superheroes, and ACID is their power 💥</p>
<p>Life lesson? Plan well, keep receipts (logs), and don’t forget to lock the door (or the row) 😉</p>
<p>Thank you so much for Reading my blog see you next sem 🤗THANK you 3000 miss💗</p>
