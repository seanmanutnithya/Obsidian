[[System analyze and design/Course/chapter 1|Database Design]]
+ 7 functions of a DBMS
	1. Date definition 
	2. Data manipulation 
	3. Data security
	4. Backup and recovery
	5. Concurrency control : many database manager can manipulate DB at the same time
	6. Data integrity : consistence data
	7. Performance optimization : Indexing, query optimization and caching improve speed
- Different types of database
	1. Relational 
	2. NoSQL
	3. Hierarchical
	4. Network
	5. Object-oriented 
	6. Time series 
- Relational database
	- structure data
	- support SQL for querying and managing data
	- Ex: MySQL, PostgreSQL, Microsoft SQL
- NoSQL database 
		- non relational database 
		- Designed for scalability, flexible and speed
		- use in large scale
	- Types 
		- Document-oriented 
		- Key-value stores 
		- Column family stores
		- Graph database
- Hierarchical database
	- data is organized in a tree-like structure (parent-child relationship)
- Network database
	- more flexible than hierarchical DB
- Object-oriented DB
	- store data in the form of objects, similar to OOP
	- contains both data and methods
- Time-series database 
	- optimize for storing and querying timestamped data, ideal for tracking changes over time
	- Examples: Influx DB, Prometheus, Timescale DB
	- use case: IOT data monitoring, financial market data, application performance monitoring (APM), energy grid monitoring 
- Database design 
	- Efficiency 
	- Integrity
	- Scalability 
- Data modeling 
	- structuring the data requirements systematically 
	- ER (Entity-relation) modeling
- Normalization
	- reduce redundancy and improve data integrity 
	- the most common normal form are 1NF, 2NF, 3NF,BCNF
	- structures data according to a series of rule called ...
	- 1NF, 2NF, 3NF,BCNF
		- 1NF : one value per cell : no repeating group 
		- 2NF : Depend on the whole key : 
		- 3NF : Depend on nothing but the key
		- BCNF : Every determinant is a key
- Denormalization : opposite from Normalization and apply its rules
	- process of intentionally introducing redundancy into a database design for performance optimization
	- It can be impro1d performance by reducing the number of join required in queries 
	- often use in data warehousing and reporting system, where read performance is prioritized over write performance 
- indexing 
	- technique that improves the speed of data retrieval operations on a DB table
	- is a data structure that allows quick lookup of rows based on the values of one more columns
- partitioning in database 
	- divide large table into smaller, more manageable segment, which can be process independently to improve performance
	- horizontal partitioning
	- vertical partitioning  
- Replication in database 
	- Replication is the process of copying and maintaining in database object, such as tables, across multiple database servers
	- create copies of data in multiple locations
- Master-Slave replication
	- write in master -> read in slave
	- master and slave has same data but can only write in master
	- 10 servers -> 10 slaves 
- Master-master replication 
	- handle both read and write 
	- change on one master are replicated to the other master
	- for improves availability but can lead complexity 