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


+ ### E-R Diagram:
  + Developed by Dr. Peter Chen in 1976, this is a conceptual-level method, grounded in real-world perceptions, facilitates diagrammatic data representation, simplifying comprehension for non-technical users.
  + The E-R Diagram data model, central to database design, encapsulates entities and their attributes within an enterprise schema, serving as a clear, standardized tool for translating real-world enterprise interactions into a conceptual schema.
  + **Entity**: An entity is a thing or an object in the real world that is distinguishable from other objects based on the values of the attributes it possesses.
  + An entity may be concrete, such as a person or a book, or it may be abstract, such as course, a course offering, or a flight reservation.

+ **Multivalued attribute:** Here we represent data in seperate Table. (Double ellipse)
+ **Composite attribute:** Here we represent data in seperate column. (Single ellipse)
+  **Stored and Derived attributes:** From stored attributes we get derived attribute especially at runtime, from DOB we calculate age. (Stored: Single ellipse, derived: dotted ellipse)
+  **Descriptive attributes:** Instead of relating to entity sets, it relates with relationships.
+  **Realtionships:**
    + One to One
    + One to Many
    + Many to Many

+ __Strong and Weak Entity Sets:__ Weak Entity sets will always have Total participation in realtionship while Strong Entity sets might have partial participation.

+ **Coversion from ER-Diagram to Relational Model**
    + **Entity Set:** Converts every strong, weak entity set into a separate table. In weak entity set we make it dependent onto one strong entity set (identifying or owner entity set).
    + **Relationship:**
        + If Unary: No separate table is required, add a new column as fk which refer the pk of the same table.
        + If 1:1, No separate table is required, take pk of one side and put it as fk on other side, priority must be given to the side having total participation.
        + If 1:1 or n:1 No separate table is required, modify n side by taking pk of 1 side a foreign on n side.
        + If m-n separate table is required take pk of both table and declare their combination as a pk of new table.
        + (3 or mode) Take the pk of all participating entity sets as fk and declare their combinations as pk in the new table.
    + **Attributes:**
        + Multivalued - A separate table must be taken for all multivalued attributes, where we take pk of the main table as fk and declare combinations of fk and multivalued attributes are pk in the new table.
        + Composite Attributes - A separate column must be taken for all simple attributes of the composite attribute.
  + **Normalization:**
      + Normalization may be simply defined as refinement proccess. Which includes creating tables and establishing relationships between those tables according to rules designed both to protect data and make the database more flexible by eliminating two factors.
          + Redundancy
          + Inconsistent dependency
  + **Integrity constraints:**
      + **Domain:** Type of data or limit check.
      + **Entity integrity:** Primary key != null.
      + **Refrential integrity:** Foreign key.
      + **Key:** Uniquiness
  + **Candidate keys:** Collection of attributes that can uniquily identify each record or entity in the database.
  + **Primary key:** As per the scenario we select the most eligible key as primary key out of all Candidate keys.
  + **Foreign key:** 
