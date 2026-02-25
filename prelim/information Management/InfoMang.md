# Info Management. Fck this sht I'm out

![Flandre](https://media.tenor.com/2c_Cn00iO3wAAAAi/scarlet-touhou.gif)

> Flandre Flandre

- [Info Management. Fck this sht I'm out](#info-management-fck-this-sht-im-out)
  - [Part 1](#part-1)
    - [Data information](#data-information)
    - [Informations needed to](#informations-needed-to)
    - [Knowledge](#knowledge)
    - [FPS(File processing system)](#fpsfile-processing-system)
      - [Advantages](#advantages)
      - [Disadvantages](#disadvantages)
    - [Problem with data dependencies](#problem-with-data-dependencies)
    - [problems with data redundancy](#problems-with-data-redundancy)
      - [Solutions](#solutions)
    - [Database system Management](#database-system-management)
      - [advantages of database systems](#advantages-of-database-systems)
      - [Risks](#risks)
  - [ER Diagram Overview](#er-diagram-overview)
    - [Purpose of ER Diagrams](#purpose-of-er-diagrams)
    - [Core Components](#core-components)
      - [Entities](#entities)
      - [Attributes](#attributes)
      - [Relationships](#relationships)
    - [Keys in ER Model](#keys-in-er-model)
    - [Cardinality \& Participation](#cardinality--participation)
    - [Advantages of ER Diagrams](#advantages-of-er-diagrams)
    - [Disadvantage](#disadvantage)
    - [Common Design Problems](#common-design-problems)
      - [Poor Entity Design](#poor-entity-design)
      - [Relationship Errors](#relationship-errors)
      - [Redundancy Issues](#redundancy-issues)
    - [Solutions / Best Practices](#solutions--best-practices)
    - [ER Diagram vs Relational Schema](#er-diagram-vs-relational-schema)
    - [Quick Review Summary](#quick-review-summary)
  - [Credits](#credits)
    - [AlieeLinux(Bazar, Cyrus troy C)](#alieelinuxbazar-cyrus-troy-c)
  - [Peace out](#peace-out)

## Part 1

### Data information

- Computer Data = Like Files
- Data = Plain facts
- Information = processed data

### Informations needed to

- To gain knowledge
- Keep the system up to date
- Know about the rules

### Knowledge

- Facts based or information based knowledge
- Heuristic knowledge

### FPS(File processing system)

- payroll system, student records

#### Advantages

- Simplicity
- Low cost

#### Disadvantages

- Data dependence
- duplication of data
- Limited data sharing
- lengthy development
- excessive program maintenance

### Problem with data dependencies

- must maintain its own data
- needs to include code for the metadata for each file
- Lock of coordination

### problems with data redundancy

- waste of space
- more maintenance
- Data changes
- Compromises in data integrity

#### Solutions

- Central repository
- data is managed by controlling agent
- Stored in convenient Form

### Database system Management

- Database system: Used to create maintain controlled access
- relational database: organizin data into tables with rows by use of foreign and primary key

#### advantages of database systems

- Program data independence
- Planned data redundancy
- Improve data consistency
- Improve data shharing

#### Risks

- New Specialized personel
- Installation and management are complex
- COnversion cost
- need for explicit backup
- Organize conflict

---

## ER Diagram Overview

- ER Diagram = Visual representation of database structure
- Entity = Object or concept with data (e.g., Student, Product)
- Attribute = Property of an entity (e.g., Name, ID)
- Relationship = Connection between entities

---

### Purpose of ER Diagrams

- Understand database structure clearly
- Design databases before implementation
- Identify relationships between data
- Reduce redundancy and errors

---

### Core Components

#### Entities

- Represent real-world objects
- Can be --Strong Entity-- (independent)
- Or --Weak Entity-- (depends on another entity)

#### Attributes

- Simple = indivisible value
- Composite = can be split (Full Name → First + Last)
- Multivalued = multiple values (Phone Numbers)
- Derived = calculated (Age from Birthdate)

#### Relationships

- Shows how entities interact
- Can have attributes
- Types:

  - One-to-One (1:1)
  - One-to-Many (1:M)
  - Many-to-Many (M:N)

- Image for god sake

![alt text](./src/InformationERD.png)

---

### Keys in ER Model

- Primary Key = Unique identifier for entity
- Candidate Key = Possible primary keys
- Composite Key = Combination of attributes
- Foreign Key = Attribute referencing another entity

---

### Cardinality & Participation

- Cardinality = Number of entity instances involved
- Participation:

  - Total = Entity must participate
  - Partial = Participation optional

---

### Advantages of ER Diagrams

- Easy visualization of database design
- Improves communication between developers
- Helps detect design flaws early
- Simplifies database documentation

---

### Disadvantage

- Can become complex for large systems
- Requires practice to interpret properly
- Not suitable for representing procedural logic

---

### Common Design Problems

#### Poor Entity Design

- Missing attributes
- Wrong primary key choice

#### Relationship Errors

- Incorrect cardinality
- Missing relationships

#### Redundancy Issues

- Duplicate data storage
- Inconsistent updates

---

### Solutions / Best Practices

- Normalize database structure
- Clearly define keys
- Avoid duplicate attributes
- Validate relationships with requirements

---

### ER Diagram vs Relational Schema

- ER Diagram = Conceptual design stage
- Relational Schema = Implementation stage
- ER → Converted into tables with rows and columns

---

### Quick Review Summary

- Entities = Objects
- Attributes = Properties
- Relationships = Connections
- Keys = Identifiers
- Cardinality = Quantity rules

👉 If you understand those five, you understand ER modeling.

## Credits

### AlieeLinux(Bazar, Cyrus troy C)

- who made this entire reviewer

---

## Peace out

![Flandre 5](https://media1.tenor.com/m/6yDx9i4-FWgAAAAC/flandre-scarlet-touhou.gif)
