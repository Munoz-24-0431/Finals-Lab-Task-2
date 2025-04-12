# [Finals-Lab-Task-2](https://github.com/user-attachments/files/19718896/LAB.TASK.2.docx)- Transforming ER Model to Relational Tables
A step-by-step SQL project that transforms an ER model into relational tables. It includes the creation of **student**, **assignment**, and **submission** tables with proper primary keys, foreign keys, and relationships. 
The submission table tracks multiple versions, modeling a many-to-many relationship between students and assignments.

## Step by Step Process
**1. Create the student table:**
- Define username as a VARCHAR(50)
- Set username as the Primary Key

**2. Create the assignment table:**
- Define shortname as a VARCHAR(50) and set it as the Primary Key
- Define due_date as a DATE NOT NULL
- Define url as a VARCHAR(255), which can be null

**3. Create the submission table:** 
- Define username and shortname both as VARCHAR(50)
- Define version as an INT
- Define submit_date as a DATE NOT NULL
- Define data as TEXT
- Set a composite primary key of (username, shortname, version)
- Add foreign keys referencing the student and assignment tables

## Table Relationships
**1. student table**
- Primary Key: username
- Relationships:
- One-to-Many with submission: One student (username) can have many submissions.
  
**2. assignment table**
- Primary Key: shortname
- Relationships:
- One-to-Many with submission: One assignment (shortname) can have many submissions.

**3. submission table**
- Composite Primary Key: (username, shortname, version)
- Relationships:
- Many-to-One with student: Each submission belongs to one student.
- Many-to-One with assignment: Each submission is for one assignment.
- This models a Many-to-Many relationship between students and assignments, with version tracking multiple submissions.

## QUERY STATEMENT, TABLE STRUCTURES, AND ERD (SCREENSHOTS)

**1. Student Table - Query Statement and Table Structue**

![stu sq](https://github.com/user-attachments/assets/0ce8dffa-989c-4424-949d-665cb4f00e15)

![stu tbl](https://github.com/user-attachments/assets/7ba23ca6-88e8-4de0-9e3b-c8b265f58300)

**2. Assignment Table - Query Statement and Table Structue**

![asss sq](https://github.com/user-attachments/assets/5893a6fc-d642-4af6-a096-7efa86581baa)

![asss tbl](https://github.com/user-attachments/assets/f0e0a2a6-344f-407f-862f-931c1e0f4da1)

**3. Submission Table - Query Statement and Table Structue**

![sub sq](https://github.com/user-attachments/assets/ebdbe876-e568-4235-a939-03369a95250c)

![sub tbl](https://github.com/user-attachments/assets/21702915-e26d-4c8a-9b81-cc6d5bb385c5)

- **EER Diagram**

![eer finals 2](https://github.com/user-attachments/assets/c0c40b37-ed6a-461f-94d4-53117141d43f)

- **The Basis for the Creation of the Relational Tables:**

![eer b](https://github.com/user-attachments/assets/ea53264c-e53e-4698-a3a3-4baa40521064)
