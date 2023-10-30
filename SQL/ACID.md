### transactions 
 - a transactions symbolizes a unit of wor performed within a database. It is often composed of multiple operators (begin and commit)
 - ![[Pasted image 20210220202537.png]]
 # acid 
 - acid is a set of properties of database transactions intended to guarantee validity even in the event of a system crashess, power failures and others errors
 ### A -ATOMIC
 - all transactions are treated as as a single unit, which either fails or succeeds
 ### C- consistent 
 - ensures that a transaction can only bring the database from one valid state to another by preventing the data corruption 
 ### I- isolation
 - determines how and when changes made by one transaction become visible to the other. 
	 - **serializable and snapshot**
		 - are the top 2 isolations leveles from a strictness standpoints
			 - A database with serializability (“I” in ACID), provides arbitrary read/write transactions and guarantees consistency (“C” in ACID), or correctness, of the database.
### D - durable 
- ensures that the results of the transactions are permanently stored in the system. The modifications must persist even in case of power loss or system failures
# benefits of acid transactions 
- This is especially true when building user-facing applications in verticals such as financial services, retail, and SaaS. Solving these concerns directly at the database layer using the consistency provided by ACID transactions is a much simpler approach.
- **simplified concurrenct control**
- **inituitive dat acess logic**
-  **future proofing database Needs**

# how to implement aciD??