Databases – SQL

##•	Terminology-
o	Column - downwards
o	Row - to the right
o	Table – entry for columns and rows
o	DBMS (database management system)
•	Databases can relate
o	Each datapoint should have an id
##•	Types of Databases
o	Flat-file database – everything on 1 table
o	Relational database – numerous table that are linked to each other through keys
o	Big data – used for data analytics, business intelligence
	Nosql – not only sql
##•	Relational databases
o	Foreign key – id from another table
o	Primary key – id for the current table
	Uniquely identifies each record in the table
	Most tables must have a primary key
	Each table can have more than one column which is part of its primary key (composite/compound key)
	Primary key constraints
•	Must be unique
•	Must always have an entry
•	The value must not change
o	Foreign key
	Natural relationships exist between tables in most database structures, foreign keys are used to create solid relationships
	Foreign keys ensure that the row of information in table a corresponds to the correct row of information in table b
o	One to many
	Each row in the table can be related to many rows in the relating tables
o	 many to many
	One or more rows in a table can be related to 0,1 or many rows in another table
	Requires a 3rd table called a mapping or link table
o	Primary table
##•	Design your own database
o	Entity relationship diagram
•	Database editions
o	Access
o	Sql server editions
o	Postgresql
o	Sqllite
o	Mysql
o	Redis nosql
o	Mongodb nosql
o	Oracle
•	DML, DDL, DCL, TCL – need to know
o	Select, insert, update, delete
•	DML – data manipulation language
o	Select, insert, update, delete
•	DDL – data definition language
o	Create, alter, stop, truncate
•	DCL – data control language
o	Grant, revoke
•	TCL – transaction control language
o	Commit, rollback, savepoint
•	CRUD -create, read, update, destroy
•	Create your own database
o	USE ‘table or database’ to select table, database to use
o	CREATE TABLE ‘name’
o	VARCHAR – variable character
	Data type. We are telling the database what info will go in the column
	Value represents maximum characters that is allowed
	VARCHAR(MAX) – more than 255 characters
o	CHARACTER or CHAR
	Fixed length data
o	INT
	For numbers and integers. Smallint and tinyint and biginit
o	DATE or TIME or DATETIME
	Stores date,time or both date and time
o	FLOAT
	Very large numbers
o	DECIMAL or NUMERIC
	Fixed precision and scale
	DECIMAL (6,4)- 6 digits, 4 can be decimal
o	BINARY
	Binary data such as image or file
o	BIT
	Equivalent to binary (0,1 or NULL)
o	SP_HELP ‘the table’
	Metadata –
	Information about the table
o	DROP TABLE
	Drop table – deletes table
	Don’t use whenever can
o	ALTER TABLE
	Can be used to RENAME, MODIFY, ADD or DROP columns
•	ALTER TABLE ‘name’
•	Add release_date DATETIME
•	Homework:
o	Create new database
o	Create the 3 tables and:
	Think/evaluate columns
	Use correct data type/specifications
	3*add data to table
o	Create user race_attendees and race tables
o	Columns user:id, first_name,last_name, email,size_legs ,speed
	Race_attendees: id, race_id, user_id
	Race table : id, date, location
•	Containers vs VM
o	Docker is a container – uses virtual OS to ‘fool’ windows
##o	ALTER COLUMN ‘column’ NOT NULL
o	When adding create table ‘table’ (‘column’ VARCHAR(x) NOT NULL)
•	INSERT command
o	INSERT INTO your_table (column_one, column_two)
o	VALUES (val1, val2);
•	DEFAULT
o	E.g (column_table DEC(3,2) NOT NULL DEFAULT(0)); - when no values have been entered, the column will have the DEFAULT value.
•	IDENTITY
o	Increments the primary key automatically when a new row is inserted.
•	UPDATE and DELETE
o	If you need to change the contents of a table, use the UPDATE statement
o	Use SET to set specific column, data value.
o	Beware of leaving out the WHERE clause, this will update the entire table.
o	DELETE works in the same way but without the SET.
##•	Database Considerations
o	Data security
o	Data recovery
o	Data integrity
o	Normal form
•	Normal form
#•	1st normal form – a database is in First Normal form when the following conditions are satisfied:
o	Make everything Atomic
	Data must be presented as small as it can be
o	There should be no repeating groups
	Each row should hold only 1 value
#•	2nd normal form
o	It is in 1NF
o	All non-key attributes are fully functional dependent on the Primary key.
#o	It is in 2NF
o	There is no transitive functional dependency
	A -=- is when a non-key column if functionally dependent on another non-key column, which is functionally dependent on the primary key.
•	FOREIGN KEY
o	Must use REFERENCES ‘primary id table’(id column)
•	JOIN ‘table’ ON table1.column1 = table2.column2
o	Adds the column to the other column whilst linking all the tables other columns
