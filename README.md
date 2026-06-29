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
5. CTE with JOIN
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
