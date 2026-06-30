 # raghdnasrelddn26334-2024.
04_CTE_Queries.docx
1. Simple CTE
Business Value:
Simple CTE makes SQL queries easier to read and maintain by creating a temporary result set.
2. Multiple CTE
Business Value:
Multiple CTEs divide complex queries into smaller parts, making them easier to understand.
3. Recursive CTE
Business Value:
Recursive CTE is useful for generating sequences and processing hierarchical data.
4. CTE with Aggregation
Business Value:


This query summarizes student grades and helps generate reports.
6. CTE with JOIN
Business Value:
Combining CTE with JOIN retrieves related data from multiple tables in a clear and efficient way.
 05_Window_Functions.docx
ROW_NUMBER()
Interpretation:
Assigns a unique number to each student.
RANK()
Interpretation:
Ranks students based on their grades. Equal grades receive the same rank.
DENSE_RANK()
Interpretation:
Similar to RANK(), but without gaps in the ranking numbers.
PERCENT_RANK()
Interpretation:
Shows the percentage rank of each student.
SUM() OVER()
Interpretation:
Calculates the total grades of all students.
AVG() OVER()
Interpretation:
Calculates the average grade of all students.
MIN() OVER()
Interpretation:
Displays the minimum grade.
MAX() OVER()
Interpretation:
Displays the maximum grade.
LAG()
Interpretation:
Shows the previous student's grade.
LEAD()
Interpretation:
Shows the next student's grade.
NTILE()
Interpretation:
Divides students into equal groups based on grades.


STUDENT INFORMATION SYSTEM

+------------------------------------------------+
|                  Students                      |
+------------------------------------------------+
| PK  StudentID                                  |
|     StudentName                                |
|     Gender                                     |
|     Age                                        |
+------------------------------------------------+
                    |
                    | StudentID (FK)
                    |
                    |
+------------------------------------------------+
|                Enrollments                     |
+------------------------------------------------+
| PK  EnrollmentID                               |
| FK  StudentID                                  |
| FK  CourseID                                   |
|     Grade                                      |
+------------------------------------------------+
                    |
                    | CourseID (FK)
                    |
                    |
+------------------------------------------------+
|                  Courses                       |
+------------------------------------------------+
| PK  CourseID                                   |
|     CourseName                                 |
|     Credits                                    |
+------------------------------------------------+
CUME_DIST()
Interpretation:
Shows the cumulative distribution of student grades.





# Oracle PDB Assignment 2

## Assignment Overview

This assignment demonstrates the Oracle Multitenant Architecture. It focuses on creating and managing Pluggable Databases (PDBs), creating users, granting privileges, and performing administrative operations using Oracle Database 21c.

## Oracle Environment

- Oracle Database: Oracle Database 21c Express Edition (XE)
- Operating System: Windows 11
- Tools Used:
  - SQL*Plus
  - Oracle Enterprise Manager (OEM)

## Task Documentation

### Task 1: Create and Configure Main PDB

1. Connected to Oracle as SYSDBA.
2. Created a PDB named `ra_pdb_26334`.
3. Opened the PDB.
4. Switched session to the PDB.
5. Created a user named `Raghd_plsqlauca_26334`.
6. Granted CONNECT, RESOURCE, and DBA privileges.
7. Connected successfully using the created user.
8. Verified the connection using the SHOW USER command.

### Task 2: Create and Delete Temporary PDB

1. Created a temporary PDB named `ra_to_delete_pdb_26334`.
2. Opened the PDB.
3. Verified its existence using SHOW PDBS.
4. Closed the PDB.
5. Dropped the PDB using INCLUDING DATAFILES.
6. Verified that it no longer appeared in SHOW PDBS.

### Task 3: Oracle Enterprise Manager

1. Accessed Oracle Enterprise Manager through the local web interface.
2. Verified Oracle instance information.
3. Confirmed the availability of the main PDB `ra_pdb_26334`.

## Challenges and Solutions

One challenge encountered was the error ORA-01031 (Insufficient Privileges) while attempting administrative operations. The issue was resolved by reconnecting as SYSDBA and executing the commands with the required administrative privileges.

Another issue occurred during PDB creation because of file path configuration. The problem was solved by configuring the DB_CREATE_FILE_DEST parameter correctly before creating the PDB.

## Lessons Learned

- Understanding Oracle Multitenant Architecture.
- Creating and managing Pluggable Databases.
- Creating database users and granting privileges.
- Connecting to Oracle using SQL*Plus.
- Performing database administration tasks.
- Troubleshooting Oracle errors and privilege issues.

## Integrity Statement

I confirm that this assignment represents my own practical work, screenshots, and documentation. All external resources consulted have been properly acknowledged.


