**Software Development Security**

![[Pasted image 20240521060212.png]]

**SYSTEM DEVELOPMENT LIFECYCLE**

- Conceptual Definition - It is a 2 paragraph of information about the project being developed which will provide a high level understanding of what it is 
- Functional Requirement determination - In this phase specific team functions are listed and developers begin to think about how the parts of the system should be interoperated and they create this FRD document which consists of, Input - Behavior - Output.
- Control specification development - This document talks about the security requirement needed and which should be implemented at the time of development and ensure that the security is being tightly integrated within the development process. 
- Design Review - Post FRD and Control specification the Design team proposes the design for the development and the tasks for the difference teams will be allotted and the software designing will be laid out
- Coding - The development team will be developing the application based on the design provided by the designing team and they will ensure that the secure coding guidelines will be followed to ensure that the system is secure from threat and vulnerabilities.
- Code review walk-through - Project managers should ensure that the code review walkthrough is being performed for each and every milestone and the stage of the development.
- System test review - Post the development the system will be tested for the basic functionalities aligned in the FRD and they will also perform Regression testing to ensure the same is being performed and all of the test has to be performed in a UAT environment. 
- Maintenance and change management - Post development any bugs, updates should be pushed via change management. 

*LifeCycle Models* - 
- Waterfall Model - It is also known as feedback loop characteristic of the waterfall model
	- ![[Pasted image 20240601180638.png]]
	- This waterfall model was one of the first comprehensive attempts to model the software development process while taking into account the necessity of returning to previous phases to correct system faults. However, one of the major criticisms of this model is that it allows the developers to step back only one phase in the process.
- The Spiral Model - It is a meta model of waterfall model where the each and every build goes through the same level of initial planning, designing and development 
- ![[Pasted image 20240601181029.png]]

- Agile Software Development Model - 
	- This model has 12 principles which talks and values about customer satisfaction and Changes in middle of project. 
	- Agile is a Philosophy and not a specific methodology
- Capability Maturity Model (CMM)
	- It is also known as Software Capability Maturity Model (SW-CMM). 
	- It has a total of 5 Levels, 
		- L1 - Initial
		- L2 - Repeatable
		- L3 - Defined
		- L4 - Managed
		- L5 - Optimizing 
- SAMM - Software assurance Maturity Model 
	- Open source project maintained by OWASP 
	- It has 5 Business Functions
		- Governance
		- Design
		- Implementation 
		- Verification 
		- Operations
		- ![[Pasted image 20240601214547.png]]

*Types of Software Testing*
 - **White-Box Testing** - White box testing examines the internal logical structure of a program and steps through the code line by line.
 - **Black-Box Testing** - This examines the program from a user perspective by providing a wide variety of input scenarios and inspecting the output. 
 - **Grey-Box Testing** - This is a combination of both types of testing which is popular for software validation. In this approach the software from a user perspective analyzing inputs and outputs. They also have access to the source code and use it to help design their tests. 

**Code Repository** - A Place where the code will be hosted and the teams can collaborate and work together to develop the code and implemented it there are multiple code repository like GitHub, Bitbucket & Source Forge etc. 

**SLA** - SLA are a popular way to ensure that organizations providing services to internal and or external customers maintain an appropriate level of service agreed on by both th service provider and the Vendor. 
- System uptime
- Maximum Consecutive Downtime
- Peak Load
- Average Load
- Responsibility for Diagnostics
- Failover time

* COTS - Commercial Of-The-Self Software* 

**Databases** - There are 2 types of DB's
- Hierarchical - (*One to many*), but with a single parent.
- Distributed - Distributed into more than one database and interconnected over a network, Each field can have numerous children as well as numerous parents thus having multiple parents and multiple children, Data Mapping for distributed system is *many to many*

**Relational Databases** - 
*Tuple* - The row nor a record in a table
*Cardinality* - The entire count of rows in a table
*Degree* - The entire column set in a table

*Candidate Keys* - A unique key for any record in a table, No two records in the same table will ever contain the same values for all attributes 

*Primary Key* - A primary key is selected from the set of candidate keys for a table to uniquely identify the records in a table. The RDBMS enforces the uniqueness of primary key by disallowing the insertion of multiple records with the same primary key.

*Alternate Key* - Any candidate key that is not selected as the primary key is referred to as alternate key. (Again this should be a unique candidate key)

*Foreign Key* - A foreign key is used to enforce relationships between two tables, also known as referential integrity. (Linking Customer Table with Sales table with the Sales Rep ID)

*ACID MODEL*
- Atomicity - Atomicity guarantees that all of the commands that make up a transaction are treated as a single unit an either succeed or fail together.  
- Consistency - Consistency guarantees that changes made within a transaction are consistent with database constraints. This includes all rules, constraints, and triggers. If the data gets into an illegal state, the whole transaction fails.
- Isolation - Isolation ensures that all transaction run in an isolated environment. That enables running transactions concurrently because transactions don't interfere with each other. 
- Durability - Durability guarantees that once the transaction completes and charges are written to the database, they are persisted. This ensures that data within the system will persist even in the case of system failure like crashes or power outages.

*NoSQL* - The databases are a class of database that models use other than the relational model to store data, There are different types of data of NoSQL database.
- Key/Value
- Graph Databases
- Document Stores 

**Knowledge Based Systems**
- Expert System - It works on a combination of if/then statements, they have a set of knowledge base which has prefilled data from experts on the subject matter, based on the situation the interference engine decides what can be the suggestion provided based on the Data which is inside the system. The expert system is good as good as its data is. 

- Machine Learning - Machine learning techniques use analytic capabilities to develop knowledge from datasets without the direct application of human insight. The core approach of machine learning is to allow the computer to analyze and learn directly from data, developing and updating models of activity.
	- *Supervised Learning* - In this learning the machine is provided with a dataset and a human helps it to identify a pattern and then the machine learns it.
	- *Unsupervised Learning* - The dataset provided to the algorithm does not contain the correct answers instead the algorithm is asked to develop  a model independently, then an analyst checks the groups of data which has been created by the algorithm.
	