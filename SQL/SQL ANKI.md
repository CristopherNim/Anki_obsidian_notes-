TARGET DECK: SQL

 OLAP VS OLTP #flashcard
 ![[Pasted image 20210312135928.png]]
 Key Differences Between OLTP and OLAP
1. The point that distinguishes OLTP and OLAP is that OLTP is an online transaction system whereas, OLAP is an online data retrieval and analysis system.
2. Online transactional data becomes the source of data for OLTP. However, the different OLTPs database becomes the source of data for OLAP.
3. OLTP’s main operations are insert, update and delete whereas, OLAP’s main operation is to extract multidimensional data for analysis.
4. OLTP has short but frequent transactions whereas, OLAP has long and less frequent transaction.
5. Processing time for the OLAP’s transaction is more as compared to OLTP.
6. OLAPs queries are more complex with respect OLTPs.
7. The tables in OLTP database must be normalized (3NF) whereas, the tables in OLAP database may not be normalized.
8. As OLTPs frequently executes transactions in database, in case any transaction fails in middle it may harm data’s integrity and hence it must take care of data integrity. While in OLAP the transaction is less frequent hence, it does not bother much about data integrity.
9. Conclusion
OLTP is an online data modification system while OLAP is an online historical multidimensional data retrieval system, which retrieves the data for analysis that can help in decision making. Which one to use depends upon the users requirement both works for different purpose.
<!--ID: 1614538318874-->

transactions #flashcard 
a transactions symbolizes a unit of word performed within a database. It is often composed of multiple operators (begin and commit)
<!--ID: 1615576350821-->


ACID #flashcard 
 - acid is a set of properties of database transactions intended to guarantee validity even in the event of a system crashess, power failures and others errors
### A -ATOMIC
 - all transactions are treated as as a single unit, which either fails or succeeds
### C- consistent 
 - ensures that a transaction can only bring the database from one valid state to another by preventing the data corruption 
### I- isolation
 - determines how and when changes made by one transaction become visible to the other. 
	 - **serializable and snapshot**
		 - are the top 2 ISOLATION'S level's from a strictness standpoints
			 - A database with serializability (“I” in ACID), provides arbitrary read/write transactions and guarantees consistency (“C” in ACID), or correctness, of the database.
### D - durable 
- ensures that the results of the transactions are permanently stored in the system. The modifications must persist even in case of power loss or system failures
<!--ID: 1615576350899-->


benefits of acid transactions #flashcard 
	- This is especially true when building user-facing applications in verticals such as financial services, retail, and SaaS. Solving these concerns directly at the database layer using the consistency provided by ACID transactions is a much simpler approach.
	- **simplified concurrence control**
	- **intuitive data access logic**
	-  **future proofing database Needs**
<!--ID: 1615576350991-->


what is RDBMS #flashcard 
  # Relational Data Base Management system 
   - are database management systems that maintain data records and indices in tables. 
   - Interdependencies among these tables are expressed by data values rather than by pointers. This allows a high degree of data independence. An RDBMS has the capability to recombine the data items from different files, providing powerful tools for data usage
  
<!--ID: 1615753061592-->

What is a primary key #flashcard 
A PRIMARY KEY constraint is a unique identifier for a row within a database table. ==Every table should have a primary key constraint to uniquely identify each row and only one primary key constraint can be created for each table. The primary key constraints are used to **enforce entity integrity**.==
<!--ID: 1615753126778-->

Describe the job of a unique key constrain #flashcard 
A UNIQUE constraint enforces the uniqueness of the values in a set of columns, so no duplicate values are entered. **The unique key constraints are used to enforce <u>`entity integrity` </u> as the primary key constraints**.
<!--ID: 1615753391013-->

`Foreign key` does what? #flashcard 
A FOREIGN KEY constraint prevents any actions that <u>would destroy links between tables with the corresponding data values.</u> **A foreign key in one table points to a primary key in another table**. Foreign keys prevent actions that would leave rows with foreign key values when there are no primary keys with that value. The foreign key constraints are used to ==enforce referential integrity.==
<!--ID: 1615753752332-->

What is <u> referential integrity </u> #flashcard 
So, referential integrity requires that, whenever a foreign key value is used it must reference a valid, existing primary key in the parent table.
1. So referential integrity will prevent users from:
	- Adding rows to a related table if there is no associated row in the primary table.
	- Changing values in a primary table that result in orphaned records in a related table.
	- Deleting rows from a primary table if there are matching related rows.
# Consequences of a Lack of Referential Integrity
	- A lack of referential integrity in a database can lead to incomplete data being returned, usually with no indication of an error. This could result in records being “lost” in the database, because they’re never returned in queries or reports.
	- It could also result in strange results appearing in reports (such as products without an associated company).
	- Or worse yet, it could result in customers not receiving products they paid for.
Worse still, it could affect life and death situations, such as a hospital patient not receiving the correct treatment, or a disaster relief team not receiving the correct supplies or information.
<!--ID: 1615753993106-->

data integrity #flashcard 
the term data integrity refers to the accuracy and consistency of data
 - for example, a user could accidentally try to enter a phone number into a date field. If the system enforces data integrity, it will prevent the user from making these mistakes.
4 types of data integrity 
 1. entity integrity 
 2. referential integrity
 3. domain integrity 
 4. user-defined integrity
<!--ID: 1615754812021-->

what is entity integrity and how to achieve it #flashcard 
Entity integrity defines each row to be unique within its table. No two rows can be the same.
To achieve this, a primary key can be defined. The primary key field contains a unique identifier – no two rows can contain the same unique identifier.
<!--ID: 1615754868552-->

what is domain integrity and how to enforce it #flashcard 
 - Domain integrity concerns the validity of entries for a given column. Selecting the appropriate data type for a column is the first step in maintaining domain integrity. 
 - Other steps could include, setting up appropriate constraints and rules to define the data format and/or restricting the range of possible values.
 - one way to achieve this is by check constraints 
<!--ID: 1615754982271-->

User-friendly integrity #flashcard 
User-defined integrity allows the user to apply business rules to the database that aren’t covered by any of the other three data integrity types.
<!--ID: 1615755116092-->

Check constraint integrity #flashcard 
A CHECK constraint is used to limit the values that can be placed in a column. The check constraints are used to <B>enforce domain integrity</B>.
<!--ID: 1615755186389-->
	
Not null enforces what integrity #flashcard 
enforces domain integrity
<!--ID: 1615755231694-->

What's the difference between a primary key and a unique key? #flashcard 
Both primary key and unique key enforces uniqueness of the column on which they are defined. ==But by default primary key creates a clustered index on the column, where are unique creates a nonclustered index by default==. Another major difference is that, primary key doesn't allow NULLs, but unique key allows one NULL only.
<!--ID: 1615756020218-->


What is normalization #flashcard 
In relational database design, the process of organizing data to minimize **redundancy**. Normalization usually involves dividing a database into two or more tables and defining relationships between the tables. The objective is to isolate data so that additions, deletions, and modifications of a field can be made in just one table and then propagated through the rest of the database via the defined relationships.
# 1NF
	Eliminate Repeating Groups Make a separate table for each set of related attributes, and give each table a primary key. Each field contains at most one value from its attribute domain.
# 2NF:
	Eliminate Redundant Data If an attribute depends on only part of a multivalued key, remove it to a separate table.
# 3NF:
	Eliminate Columns Not Dependent On Key If attributes do not contribute to a description of the key, remove them to a separate table. All attributes must be directly dependent on the primary key
# BCNF: 
	Boyce-Codd Normal Form If there are non-trivial dependencies between candidate key attributes, separate them out into distinct tables.
<!--ID: 1615756020237-->

**1nf** #flashcard 
1NF (First Normal Form) Rules: 	
- Each table cell should contain a single value.
- Each record needs to be unique.
![[Pasted image 20210314170953.png]]
What do you see here? 
![[Pasted image 20210314172446.png]]
<!--ID: 1615757108492-->

**2nf** #flashcard  
![[Pasted image 20210314172616.png]]
![[Pasted image 20210314172731.png]]
![[Pasted image 20210314172829.png]]
<!--ID: 1615757344109-->

**3nf** #flashcard 
![[Pasted image 20210314173238.png]]
![[Pasted image 20210314173331.png]]
<!--ID: 1615757615898-->

what is stored procedure #flashcard 
![[Pasted image 20210314173640.png]]
<!--ID: 1615757804490-->

What are the advantages of using Stored Procedures? #flashcard 
	- Stored procedure can reduced network traffic and latency, boosting application
	performance.
	- Stored procedure execution plans can be reused, staying cached in SQL Server's memory, reducing server overhead.
      - Stored procedures help promote code reuse.
	- Stored procedures can encapsulate logic. You can change stored procedure code without affecting clients.
	- Stored procedures provide better security to your data.
<!--ID: 1615758176041-->




What is a trigger #flashcard 
- A trigger is a SQL procedure that initiates an action when an event (INSERT, DELETE or UPDATE) occurs. Triggers are stored in and managed by the DBMS. Triggers are used to maintain the referential integrity of data by changing the data in a systematic fashion. A trigger cannot be called or executed; the DBMS automatically fires the trigger as a result of a data modification to the associated table.
- In addition, triggers can also execute stored procedures. Nested Trigger: A trigger can also contain INSERT, UPDATE and DELETE logic within itself, so when the trigger is fired because of data modification it can also cause another data modification, thereby firing another trigger. A trigger that contains modification logic within itself is called a nested trigger.
<!--ID: 1615758144501-->

What is a view #flashcard 
A simple view can be thought of as a subset of a table. It can be used for retrieving data, as well as updating or deleting rows. Rows updated or deleted in the view are updated or deleted in the table the view was created with. It should also be noted that as data in the original table changes, so does data in the view, as views are the way to look at part of the original table. The results of using a view are not permanently stored in the database.
<!--ID: 1615758330359-->

What is Index? #flashcard 
An index is a physical structure containing pointers to the data. Indices are created in an existing table to locate rows more quickly and efficiently.
<!--ID: 1615758375391-->

zzz**What are the difference between clustered and a non-clustered index?** #flashcard 
	- A Clustered index is a special type of index that reorders the way records in the table are physically stored. Therefore table can have only one clustered index. The leaf nodes of a clustered index contain the data pages. 
	- A Non-Clustered index is a special type of index in which the logical order of the index does not match the physical stored order of the rows on disk. The leaf node of a non-clustered index does not consist of the data pages. Instead, the leaf nodes contain index rows.
	![[Pasted image 20210314174834.png]]
	![[Pasted image 20210314174846.png]]
<!--ID: 1615759174903-->

 Difference between Function (UDF) and Stored Procedure (SP)? #flashcard 
 ![[Pasted image 20210314180057.png]]
<!--ID: 1615759454002-->

what is the difference between delete and truncate #flashcard 
![[Pasted image 20210314180537.png]]
<!--ID: 1615760070873-->


Types if sql statements #flashcard 
![[Pasted image 20210314181418.png]]
<!--ID: 1615760070905-->

creating a table with not null and unique constraints #flashcard 
![[Pasted image 20210314181755.png]]
Alter Table persons 
ADD UNIQUE (P_ID)
___
ALTER TABLE persons 
DROP CONSTRAINT uc_personID
<!--ID: 1615760279278-->

Creating a FK key #flashcard 
CREATE TABLE Orders
(
O_Id int NOT NULL PRIMARY KEY,
OrderNo int NOT NULL,
**P_Id int FOREIGN KEY REFERENCES Persons(P_Id)**
)
<!--ID: 1615760607117-->


SQL check constraint #flashcard 
CREATE TABLE Persons
(
**P_Id int NOT NULL CHECK (P_Id>0)**,
LastName varchar(255) NOT NULL,
FirstName varchar(255),
Address varchar(255),
==City varchar(255) DEFAULT 'Sandnes'==
)
<!--ID: 1615763366532-->


how to eliminate duplicates #flashcard 
![[Pasted image 20210314195443.png]]
<!--ID: 1615766891079-->

How to use the null and not null in a query #flashcard 
![[Pasted image 20210314201000.png]]
<!--ID: 1615767005718-->

using filtering data in SQL is like #flashcard 
![[Pasted image 20210314201114.png]]
<!--ID: 1615767236520-->

filtering data in a query #flashcard 
![[Pasted image 20210314201528.png]]
<!--ID: 1615767344948-->


How does a weak correlation and strong correlation in scatter plot look   like #flashcard 
![[Pasted image 20210319184516.png]]
<!--ID: 1616193968564-->

quadratic, power, inverse and logistic #flashcard 
![[Pasted image 20210319184800.png]]
<!--ID: 1616194095530-->

how many data points should you have #flashcard 
As a rule of thumb, correlation coefficients calculated with fewer than 30 data points should be taken with a pinch of salt. Ideally, you should have as many good data points as you can in order to calculate the correlation.
<!--ID: 1616195120114-->

logical fallacy of correlation #flashcard 
That is, just because x and y have a strong correlation does not mean that x causes y.
<!--ID: 1616195537695-->

What can I do with missing data? #flashcard 
- You can delete rows if its less than 5 percent since it will not impact the data
- Mean/Median/Mode Imputation: If 5% to 25% of your data for a variable is missing, another option is to take the mean, median, or mode of that column and fill in the blanks with that value.
- deleting variables if you do not have enough records 
- regression imputation 
<!--ID: 1616196771320-->

How do you test click-through rate? #flashcard 
A/B test baby let's go
<!--ID: 1616196818149-->

Two-sample Z-test #flashcard 
Test: A test for determining whether the average of the two samples is different. This test assumes that both samples are drawn from a normal distribution with a known population standard deviation.
<!--ID: 1616197093427-->

Pearson's chi-squared Test #flashcard 
A test for determining whether the distribution of data points to categories is different than what would be expected due to chance. This is the primary test for determining whether the proportions in tests, such as those in an A/B test, are beyond what would be expected from chance.
<!--ID: 1616197177882-->


creating a table with a select statement #flashcard 
CREATE TABLE products_2014 AS ( SELECT * FROM products WHERE year=2014 );
<!--ID: 1616199760901-->


How do you use the limit clause #flashcard 
Select *  
From Table
order by 1
Limit 5()
<!--ID: 1616272017897-->

What is the syntax for adding and deleting columns #flashcard 
ALTER TABLE {TABLE NAME}
ADD COLUMN (COLUMN_NAME} {DATA_TYPE};
____
ALTER TABLE {TABLE NAME}
DROP COLUMN {COLUMN_NAME};
<!--ID: 1616273812691-->

WHAT IS THE SYNTAX FOR ADDING ROWS #flashcard 
INSERT INTO TABLE_A (COL_A, COL_B....COL_Z)
VALUES (VAL_1, VAL2, ....VAL_Z)
<!--ID: 1616273945837-->

Inserting rows with the select statement #flashcard 
INSERT INTO products 2014( product_id, model, year, product_type, base_msrp, production_start_date, production_end_date ) 
SELECT * 
FROM products
where 
year=2014
<!--ID: 1616274062103-->


Updating existing rows #flashcard 
UPDATE {TABLE_A}
SET {COL} = {COL_VALUE},
       {COL_2} = {COL_VALUE_2}....
WHERE {CONDITIONAL}	
![[Pasted image 20210320170928.png]]
<!--ID: 1616274206300-->

How to delete column values from a row #flashcard 
The easiest way to accomplish this is to update the table and set the columns values to null
____
![[Pasted image 20210320171232.png]]
____
for example let's say we have the wrong email on file for the customer with the customer who has an id equal to 3. 
____
![[Pasted image 20210320171529.png]]
<!--ID: 1616274990860-->


Deleting rows from a table #flashcard 
DELETE FROM {TABLE_A}
WHERE {CONDITIONAL};
_____
DELETE FROM 
   CUSTOMERS
WHERE EMAIL = 'SPAMSSPAM@GMAIL.COM';   
## forgetting to add where will delete all the rows from a table
## If you want to truncate all the data 
- TRUNCATE TABLE TABLE_A;
<!--ID: 1616275284469-->

Deleting tables #flashcard 
DROP TABLE {TABLE_NAME};
<!--ID: 1616275368572-->

what is the keyword when you get asked for valid data? #flashcard 
In order to know that data is valid  (that exist) you have to use not null
<!--ID: 1616371288598-->

Think of an example on how to use inner joins instead of IN                   clause #flashcard 
SELECT *
FROM salespeople
INNER JOIN (
    SELECT *
    FROM dealerships
    WHERE dealerships.state = 'CA'
    ) d
ON d.dealership_id = salespeople.dealership_id
ORDER BY 
_____
--- another query that will yield the same result
SELECT *
FROM salespeople
WHERE dealership_id IN (
    SELECT dealership_id FROM dealerships
    WHERE dealerships.state = 'CA'
    )
ORDER BY 1;
<!--ID: 1616371812486-->

what are the rules to using UNION #flashcard 
The UNION operator is used to combine the result-set of two or more SELECT statements.
___
1. Every SELECT statement within UNION must have the same number of columns
2. The columns must also have similar data types
3. The columns in every SELECT statement must also be in the same order
4. have to use the nickname of the first unions 
![[Pasted image 20210321201659.png]]
![[Pasted image 20210321203820.png]]
<!--ID: 1616372244381-->

What is the main advantage of CTE (common Table                    Expression) #flashcard 
- The main advantage of CTE is that they are recursive 
-  Each auxiliary statement in a WITH clause can be a SELECT, INSERT, UPDATE, or DELETE; 
-  The WITH clause itself is attached to a primary statement that can also be a SELECT, INSERT, UPDATE, or DELETE.
 - auxiliary = in addition 
 - https://www.postgresql.org/docs/9.1/queries-with.html
<!--ID: 1616374158514-->


Naming column aliases in postgre SQL #flashcard 
If the alias is only one word then no quotes is needed, but if the alias has spaces it must be surrounded by double quotes.
<!--ID: 1616439496038-->

How does the coalesce function work #flashcard 
It grabs the first Non Value in the given column
![[Pasted image 20210322151550.png]]
<!--ID: 1616440563184-->

Explain how the NULLIF function works in sql #flashcard 
![[Pasted image 20210322152351.png]]
<!--ID: 1616441034145-->

Explain the greatest and least function #flashcard 
![[Pasted image 20210322153202.png]]
![[Pasted image 20210322153337.png]]
<!--ID: 1616441611693-->

How does the casting function work in Postgre sql #flashcard 
![[Pasted image 20210322153720.png]]
<!--ID: 1616441998777-->

what are the differences between distinct and distinct ON in postgre sql -- #flashcard 
![[Pasted image 20210322154205.png]]
![[Pasted image 20210322154653.png]]
# guarantees that every row has a unique first_name, then if the first_name has duplicates the user that was hired first will be put on the query;
<!--ID: 1616442481534-->

How does the count function work and what can you do with it #flashcard 
count(col_name) **counts only non null values**
count(*) **counts all values including null values**
count(distinct expression) **distinct values** 
<!--ID: 1616444998700-->

What are the major aggregate functions #flashcard 
![[Pasted image 20210322165806.png]]
<!--ID: 1616446708671-->

Why do you have to cast sum in PostGreSQL #flashcard 
Sum treats integer division differently than float division 
![[Pasted image 20210322170119.png]]
<!--ID: 1616446873923-->


What columns go in the group by #flashcard 
The columns that are not used in aggregated functions 
<!--ID: 1616447294356-->


Using group by ({roll up, cube, grouping sets}) #flashcard 
https://www.postgresql.org/docs/10/queries-table-expressions.html#QUERIES-GROUPING-SETS
![[Pasted image 20210322180108.png]]
<!--ID: 1616450472551-->


Describe Mode, percentile_cont, percentile_disc #flashcard 
![[Pasted image 20210322181254.png]]
<!--ID: 1616451177266-->

Why is it important for the median to be in ordered and what do we use to achieve this #flashcard 
The median grabs the median number and it uses ordered set aggregates functions 
SELECT 
{ORDERED SET_FUNCTION} within group (ORDER BY {ORDER COLUMN})
FROM {TABLE};
<!--ID: 1616451369442-->

Using the the set aggregate functions. Imagine an SQL query          example #flashcard 
![[Pasted image 20210322182150.png]]
<!--ID: 1616451725524-->

What is the purpose of Having Clause #flashcard 
In order to filter aggregated function, you need to use the HAVING CLAUSE.
<!--ID: 1616452508425-->

When to delete values in a column, fill them, or delete the                 column #flashcard 
- if (<1% filtering out or delete the missing data from your analysis)
- if (<20%) consider using the mode, median, or mean
- if 20% or more you might just have to just flat out remove the column
<!--ID: 1616452680587-->

how would you calculate for missing values #flashcard 
SELECT 
	SUM(CASE WHEN {column1} IS NULL 
	OR {column1} IN ({missing_values}) 
	THEN 1 ELSE 0 END)::FLOAT/COUNT(*)
FROM {TABLE1}
____
SELECT 
	SUM(CASE WHEN state IS NULL 
	OR state IN ('') 
	THEN 1 ELSE 0 END)::FLOAT/COUNT(*) AS missing_state 
	FROM customers;
![[Pasted image 20210322185447.png]]
<!--ID: 1616453689345-->

How to measure Data quality with aggregates #flashcard 
- variation makes the column useful
	- Select COUNT(DISTINCT {COLUMN_1}) FROM {TABLE1}
- another thing to check if every value in the column is unique 
![[Pasted image 20210322185849.png]]
<!--ID: 1616453936994-->
 
 
what are the ranking functions and explain how each of them work---------- #flashcard 
 Rank – 1,1,3,3,5
		Dense_Rank – 1,1,2,2,3
		Ntile – Breaks up data in random order and ranking
		Row_Number – 1,2,3,4,5 – ranking based on table location going down rows
<!--ID: 1616531026245-->


What are the statistical window functions and describe there functions-----  #flashcard 
**It is important emphasize aggregate functions are allow in window functions ** ==AVG ,sum, count and so on== 
![[Pasted image 20210323192720.png]]
# ROW_NUMBER () OVER (
   PARTITION BY COLS
   ORDER BY COLS
 )
 
<!--ID: 1616542139457-->


Window Frame clause #flashcard 
![[Pasted image 20210323193858.png]]
<!--ID: 1616542796163-->

The difference between range and rows in windows clause #flashcard 
- row actually refers to actual rows and will take the row before and after the current row to calculate values.  
- RANGE differs when two rows have the same values based on the ORDER BY clause used in the window. If the current row that's being used in the window calculation has the same value in the ORDER BY clause as one or more rows, then all of these rows will be added to the window frame.
<!--ID: 1616601452145-->


{frame_start} And {frame_end} in windows clause #flashcard 
![[Pasted image 20210323194331.png]]
<!--ID: 1616601452160-->


SELECT DATE #flashcard 
'1/8/1999' DAY MONTH YEAR IS CONVERTED TO ISO DATES
<!--ID: 1616793645710-->

what is the difference between current_date and now() #flashcard 
current date returns the date of today.
now() returns the date with the UTC time.
<!--ID: 1616793993402-->

how is now() recommend to be used? #flashcard 
SELECT NOW() AT TIME ZONE 'EST'; 
<!--ID: 1616796095778-->

How do we use  extract #flashcard
![[Pasted image 20210326180254.png]]
<!--ID: 1616796180604-->

What is the difference between DOW AND ISODOW #flashcard 
DOW starts at Sunday 0
ISODOW starts at Monday 1
<!--ID: 1616796262120-->

How does date_trunc() work #flashcard 
![[Pasted image 20210326180606.png]]
<!--ID: 1616796374895-->

explain the syntax on subtracting | adding dates, timestamps and intervals--- #flashcard 
![[Pasted image 20210326180812.png]]
<!--ID: 1616796503905-->

How does the POINT function work #flashcard 
![[Pasted image 20210326184905.png]]
<!--ID: 1616798952969-->

what is the output ![[Pasted image 20210326185211.png]] #flashcard 
![[Pasted image 20210326185047.png]] 
<!--ID: 1616799050380-->


Explain what an action, attribute, entity is Entity Relationship diagram -------- #flashcard 
![[Pasted image 20210328135708.png]]
<!--ID: 1616954251089-->

Strong entity vs weak entity #flashcard 
![[Pasted image 20210328140128.png]]
![[Pasted image 20210328140137.png]]
<!--ID: 1616954513195-->

Actions in Entity Relationship diagram #flashcard 
![[Pasted image 20210328140249.png]]
<!--ID: 1616954572295-->

attributes #flashcard 
![[Pasted image 20210328140434.png]]
<!--ID: 1616954679120-->

Connecting lines and cardinality #flashcard 
![[Pasted image 20210328140626.png]]
![[Pasted image 20210328140712.png]]
<!--ID: 1616954890440-->

Chen style #flashcard 
![[Pasted image 20210328140822.png]]
<!--ID: 1616954904188-->

How does SQL read queries #flashcard 
From USA 
where all people are 
group by color 
having so many color people 
select the best color people 
order by white 
limit to no spanish or guatemalan folks
FWGHSOL
<!--ID: 1616955090409-->


The correct syntax for SELECT INTO statement #flashcard 
![[Pasted image 20210328141526.png]]
![[Pasted image 20210328141548.png]]
<!--ID: 1616955328677-->


how do you drop a column who has a foreign key constraint #flashcard 
![[Pasted image 20210328161220.png]]
<!--ID: 1616962345633-->

adding a constrain on a column #flashcard 
![[Pasted image 20210328161250.png]]
<!--ID: 1616962373212-->


how to remove a constraint from a column in postgre #flashcard 
![[Pasted image 20210328161415.png]]
<!--ID: 1616962461580-->

how to change a column default value #flashcard 
![[Pasted image 20210328161500.png]]
<!--ID: 1616962504587-->

changing a column's Data type #flashcard 
![[Pasted image 20210328161542.png]]
<!--ID: 1616962553684-->

what does <@> do in postgresql #flashcard 
calculates the distance in miles using the point function
<!--ID: 1617215670093-->

what does @> do in postgresql #flashcard 
# checks if the array has the same sequence
![[Pasted image 20210331143750.png]]
<!--ID: 1617215871695-->


 what does array_agg do in postgresql #flashcard 
array_agg ( any_non_array ) → any_array
- Collects all the input values, including nulls, into an array.
![[Pasted image 20210331155311.png]]
<!--ID: 1617220403345-->

What is the output for unnest(array[1,2,3]) #flashcard 
![[Pasted image 20210331155424.png]]
<!--ID: 1617220469415-->

string_to_array vs array_to_string #flashcard 
![[Pasted image 20210331155509.png]]
<!--ID: 1617220514285-->

T/F 3= any(array[1,2]) #flashcard 
False
<!--ID: 1617220592784-->

what is the difference between count(*) vs Count(1) #flashcard 
NONE 
<!--ID: 1617220868081-->

![[Pasted image 20210331160259.png]] #flashcard 
makes sense of it
<!--ID: 1617221056761-->

Json Vs JsoNB  #flashcard 
# json 
- parsed (bad)
# JsoNB
- pre-parsed 
	- decomposed in binary format
	- be parsed upfront - improving the query 
		- keys have already been extracted and picked 
- Cannot have more than one key
-  the order is not preserved 
-  no whitespaces are preserved 
<!--ID: 1617223461048-->


![[Pasted image 20210331164755.png]] #flashcard 
![[Pasted image 20210331164735.png]]
<!--ID: 1617223736205-->


how to use regexp_replace() postgresql #flashcard 
regexp_replace(source, pattern, replacement [, flags ]). The flags parameter is an optional text string containing zero or more single-letter flags that change the function's behavior. Flag i specifies case-insensitive matching, while flag g specifies replacement of each matching substring rather than only the first one. Supported flags (though not g)
![[Pasted image 20210331200018.png]]
<!--ID: 1617235220549-->

What does row_to_json do #flashcard 
# it is what the name implies
	-	Make sure you use True to make it pretty
![[Pasted image 20210331200358.png]]
<!--ID: 1617235465063-->


![[Pasted image 20210331200608.png]] #flashcard 
explain what each query is doing
<!--ID: 1617235587213-->

![[Pasted image 20210331200827.png]] #flashcard 
ARRAY['B', '2', 'f']
B is the key
2 is the index location
f is the key
<!--ID: 1617235967963-->

![[Pasted image 20210331202236.png]] #flashcard 
![[Pasted image 20210331202258.png]] 
<!--ID: 1617236588742-->

non_jsonb vs jsonb_pretty #flashcard 
![[Pasted image 20210331202931.png]]
<!--ID: 1617236977207-->

Getting the keys and values from a jsonb #flashcard 
![[Pasted image 20210331203519.png]]
<!--ID: 1617237325002-->

Conceptual model vs logical model vs data model #flashcard 
![[Screen Shot 2021-04-01 at 11.28.08 AM.png]]
<!--ID: 1617547929540-->


Conceptual vs logical model #flashcard 
![[Screen Shot 2021-04-01 at 11.28.15 AM.png]]
<!--ID: 1617547964742-->

Physical Data Model #flashcard 
![[Screen Shot 2021-04-01 at 11.28.26 AM.png]]
<!--ID: 1617547995116-->


SQL VS NOSQL #flashcard 
![[Pasted image 20210405120251.png]]
# benefits of NoSQL
- flexible data models 
	- ![[Pasted image 20210405120348.png]]
- Horizontal scaling
	- Adding floors instead of houses
	- In SQL you add attributes which means you add houses to the neighborhood
- Fast queries 
	- Do not require joins 
	- Json files
- Easy for developers 
- No ACID 
<iframe src="https://giphy.com/embed/l41lNT5u8hCI92nQc" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/rickandmorty-rick-and-morty-adult-swim02x04-l41lNT5u8hCI92nQc">Acid Baby</a></p>
<!--ID: 1617638854320-->

ETL #flashcard 
![[Pasted image 20210405121147.png]]
![[Pasted image 20210405121242.png]]
<!--ID: 1617639167569-->


Data Lake Vs data Warehouse #flashcard 
![[Pasted image 20210405121521.png]]
![[Pasted image 20210405121603.png]]
<iframe src="https://giphy.com/embed/eYFXdUmT5QhyM" width="480" height="243" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/water-guy-lake-eYFXdUmT5QhyM">Data Lake</a></p>
<!--ID: 1617639482487-->

can you call a function from a stored procedure? #flashcard 
True
<!--ID: 1617639809075-->


Can you call a stored procedure from a stored function #flashcard 
Nope
<!--ID: 1617639859624-->
