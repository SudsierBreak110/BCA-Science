
## <font color="#4bacc6">What is a file system?</font>
A file system is a method used by an operating system to **store, organize, manage, and
retrieve data in files** on a storage device such as a hard disk, SSD, pen drive, or memory card.

> [!info]- Defination
> A **File System** is an approach in which data is stored and managed as individual files
> using the operating system's file management facilities.

## <font color="#4bacc6">Advantages of file system</font>
File systems are still useful in many situations, especially for small and simple applications.

1. **Easy to understand** - Files are easy for beginners to understand. They don't have to learn database concepts like Keys, Tables, SQL, etc.

2. **Easy to implement** - For a smaller application, creating a file is much simpler than creating a database. It requires very less infrastructure.

3. **Low cost** - A simple file-based application does not require a dedicated database server. For small applications, this can reduce: **Software and Server requirements, Administration, Maintenance costs.**

4. **Suitable for small applications** - Files systems work well when:
     - Data is small in size
     - Only one or a few users access the data
     - Relationships between data are simple
     - Security requirements are limited

5. **Easy backup** - Individual files can be copied easily.

## <font color="#4bacc6">Disadvantages of file system</font>

1. **Data redundancy** - There might exist <font color="#f79646">duplicate data</font>
	- The same data might be stored in different files.
	- This <font color="#f79646">wastes storage space, increases maintenance and may lead to inconsistencies</font>

2. **Data inconsistency** - There might be <font color="#f79646">conflicting data</font>
	- Different copies of the same data has different values.

3. **Difficult Data Access & Isolation** - Data might be difficult to search
	- Information may be<font color="#f79646"> distributed across multiple files and different formats</font>, making it difficult to retrieve and combine data.

4. **Integrity Problems** - Data might be incorrect

5.  **Atomicity & Recovery Problems** - Updates might not happen resulting in loss of data
	- An <font color="#f79646">operation should be completed or not done at all</font>. This does not happen in a file system and might cause problems.
	- After a crash, <font color="#f79646">restoring files to a consistent state can be difficult</font>.

6. **Multi-User Problems** - Problems might arise when <font color="#f79646">multiple users access the data simultaneously</font>

7. **Security Problems** - Limited access control
	- File systems only <font color="#f79646">provide basic file permissions</font> and achieving total control over specific data can be difficult.
	- Only authorized users should be able to access data

8. **Program–Data Dependence** - Application depends on file structure

---

## <font color="#4bacc6">What is a Database Management System?</font>

> [!info]- Defination
> A Database Management System (DBMS) is software that provides an interface for
> creating, storing, organizing, retrieving, updating, and managing data in a database.


<font color="#c0504d">User --> DBMS --> Database</font>

- The database contains the actual data, while the DBMS manages access to that data.
- The important point is that the <font color="#f79646">user does not need to directly manipulate the physical storage files.</font>
- The DBMS provides a controlled way to interact with the database.

## <font color="#4bacc6">Advantages of DBMS</font>

1. **Reduced Data Redundancy** - Minimizes unnecessary duplicate data

2. **Improved Data Consistency** - Keeps <font color="#f79646">data accurate and consistent</font>

3. **Data Sharing & Centralized Management** - <font color="#f79646">Multiple users</font> can access shared data

4. **Data Security** - Controls who can access data

5. **Data Integrity** - <font color="#f79646">Maintains accuracy and validity of data</font>
	- Data stored is accurate, valid and follows defined rules

6. **Concurrent Access** - <font color="#f79646">Supports multiple users</font> accessing data simultaneously

7. **Backup & Recovery** - <font color="#f79646">Protects data against failures</font> and restores it when required

8. **Data Independence** - Separates applications from physical data storage
	- Data independence means that <font color="#f79646">changes in the way data is stored or organized do not necessarily require changes to application programs.</font>

## <font color="#4bacc6">Disadvantages of DBMS</font>

1. **High Cost** - Requires software, hardware, and infrastructure

2. **Complexity** -<font color="#f79646"> DBMS is more complex</font> than simple files

3. **Requires Skilled Personnel** -<font color="#f79646"> Specialized people may be required</font>

4. **High Resource Requirement**s - <font color="#f79646">Requires more memory, storage, and processing power</font>

5. **Performance Overhead** - <font color="#f79646">Uses extra resources</font> to manage the database

6. **Single Point of Failure** - Central database<font color="#f79646"> failure can affect many users</font>

7. **Maintenance & Administration** - <font color="#f79646">Requires regular monitoring</font> and maintenance

8. **Security Risks** - Centralized data can become a valuable target


## <font color="#4bacc6">Applications of DBMS</font>

![[applications of dbms.png]]



### Sources
[[Unit 1_Introduction to Database Management System.pdf]]






