# DBMS (Database Management System)
+ ### Data:
  - Data are characteristics or attributes that may be numerical, collected through observations, and can be qualitative (descriptive) or quantitative (numerical). Any facts and figures about an entity are called data.

+ ### Information:
  - Data becomes information when analyzed and placed in context, providing a basis for understanding, decision-making, and further analysis. Processed data is called information.

+ ### Database:
  - A database is a structural collection of data, facilitating easy access, management, and updates, generally stored and accessed electronically from computer systems.

+ ### DBMS (Database Management System):
  - A DBMS is software facilitating efficient data storage, retrieval, and management in databases.
  - Ensures data safety and integrity, while offering accessibility and concurrency control it supports functions like data querying, reporting, and analytics for informed decision-making.

+ ### File system v/s DBMS:
    | Aspects | File system | DBMS |
    |---|---|---|
    | Data Access | Slower data retrieval due to unstructured querying capabilities. | Structured querying capabilities allow for quicker data access. |
    | Data isolation | Challenges in correlating data across separate files leading to data isolation. | Facilitates data integration, and reduces data isolation issues. |
    | Data integrity | Risk of inadvertent data alterations or deletions creating integrity problems. | Features to prevent unauthorized data alterations, and maintain integrity.
    | Atomicity Problem | Potential for data inconsistency due to incomplete operations, leading to atomicity problems. | Supports transaction properties like atomicity, ensuring operations are completed fully or not. |
    | Concurrent access anomalies | Conflicts and inconsistencies from simultaneous data access/modifications, causing concurrent access anomalies | Advanced concurrency control to manage multiple users accessing the data simultaneously, reducing anomalies.

+ ### Data abstraction level:
  - **Physical Level**: The internal schema details data storage and access on hardware, featuring the lowest level of data abstraction with complex structures, predominantly managed by the database administrator.
  - **Conceptual Level/Logical Level**: Above the physical level, this level showcases data as entity sets and their relationships, detailing the types and connections between stored data in the database.
  - **View Level**: This is the pinnacle of data abstraction, displaying only a portion of the entire database focusing on user-interest areas. It can represent, multiple views of the same data, allowing users to access information through various applications from the database.

- **Data independence**:
    - Data independence is defined as the capacity to change the schema at one level of the database without having to change the schema of the next higher level.
      - **Physical data independence**: A physical data independence the ability to manage internal schema without changing the conceptual schema. Modification at the physical level is occasionally necessary in order to improve performance. It refers to the immunity of the conceptual schema to change in the internal schema. Examples of physical data independence is reorganization of files, adding a new access path or modifying indexes, etc.
      - **Logical data independence**: A logical data independence is the ability to modify the data at conceptual schema without having to change the external schemas or application programs. It refers to the immunity of the model to change to changes in the conceptual model. Examples of logical data independence are addition/removal of entities.

- ### Instance and Schema:
    - **Instance**: The collection of information stored in the database at a specific moment is known as an instance of database. It is snapshot of database that contains live data at that moment, showing the current state of all records and transactions.
    - **Database Schema**: The database schema refers to the overall design of the database, illustrating the logical structure and organization of data. It defines how data is organised and how relationships between data are handled, essentially serving as the blueprint for how the databases is constructed.

+ ### OLAP (Online Analytical Processing) and OLTP (Online Transaction Processing):
    | Aspects | OLAP (Online Analytical Processing) | OLTP (Online Transaction Processing) |
    |---|---|---|
    | Primary Function | Designed for complex data analysis. | Handles daily transactions of data processing. |
    | Database design | Star or snowflake schema, optimizing for read operations. | Normalised schema, optimizing for write operations. |
    | Query complexity | Complex queries involving aggregations and computations across multiple dimensions. | Simple and standard queries focusing or CRUD operations (CREATE, READ, UPDATE, DELETE). |
    | Data volume | Deals with the large volumes of data for historical analysis. | Processes a high number of small transactions. |
    | Response time | Slower response time due to complex queries. | Fast response time to support high transaction rates. |
