<h1>[Mini] Filter an SQL Query</h1>

<h2>Description</h2>
In this lab example, I run through how to filter an SQL query. I'll be applying basic filters to SQL queries to retrieve information from a MariaDB database. <br/>
MariaDB is a popular open source relational database that is compatible with MySQL.
<br/>
<Br/>
At the end of this lab, I have practical experience in using SQL to: <br/>
- apply the "WHERE" clause to filter what a SQL query returns, and <br/>
- use the "LIKE" operator to filter for patterns.

<h2>Languages and Utilities Used</h2>

- <b>MariaDB database</b> 
- <b>Oracle VM Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
For this scenario, I need to get specific information about employees, their machines, and the departments they're in. <br/>
My team needs this data to perform task suchs as running updates, posting a privacy notice in certain departments, <br/>
 and sending an alert to an employee with an issue on a machine. <br/>
First, I'll list all organization machines and their operating systems. <br/>
Next, I'll list all machines with the operating system OS 2. <br/>
Third, I'll list all the employees in the Finance and Sales department. <br/>
Finally, I'll obtain information about machines. <br/>

<img src="https://i.imgur.com/ZChRTsk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. For this task, I need to get a list of all organization machines and their operating system: <br/>
To do so, type in: <br/>
SELECT * <BR/>
FROM machines <br/>
ORDER BY device_id, operating_system;
<img src="https://i.imgur.com/Oo3ixiT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. For this task, I need to obtain a list of all machines with the "OS 2" operating system because these machines need an update: <br/>
To get this information, I run an SQL query with a filter: <br/>
SELECT device_id, operating_system <Br/>
FROM machines <br/>
WHERE operating_system = 'OS 2';
<img src="https://i.imgur.com/cZyh3JK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. For this task, I want to list employees specifically from the FINANCE deparment: <br/>
To do so, type in: <br/>
SELECT * <Br/>
FROM employees <br/>
WHERE department = 'Finance';

<img src="https://i.imgur.com/APUuAj0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. Now in relation to the above task, do the same but list employees from the SALES department:  <br/>
<img src="https://i.imgur.com/WbBt8a8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. For this task, I need to obtain certain employee and computer information, specifically from the South building:  <br/>
I've identified that a machine in 'South-109' has an issue. I need to determine which employee uses the computer <br/>
so I can send them an alert. <br/>
The query I would write would be: <br/>
SELECT * <BR/>
FROM employees
WHERE office = 'South-109';
<img src="https://i.imgur.com/KcjoDMa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. Just the same as the above task, but this time I use the "LIKE" operator with the "%" wildcard:  <br/>
<img src="https://i.imgur.com/Uxba9sg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
