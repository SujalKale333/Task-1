CREATE DATABASE StudentDB;
USE StudentDB;

CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(50),
    department VARCHAR(30),
    marks INT
);
INSERT INTO Students VALUES
(1, 'Amit', 'IT', 85),
(2, 'Neha', 'IT', 78),
(3, 'Rahul', 'CSE', 92),
(4, 'Priya', 'CSE', 66),
(5, 'Sonal', 'ENTC', 74);
SELECT * FROM Students;

SELECT student_name, marks
FROM Students
WHERE marks > 75;

SELECT AVG(marks) AS Average_Marks
FROM Students;

SELECT MAX(marks) AS Highest_Marks
FROM Students;

SELECT MIN(marks) AS Lowest_Marks
FROM Students;

SELECT COUNT(*) AS Total_Students
FROM Students;

SELECT department, AVG(marks) AS Avg_Marks
FROM Students
GROUP BY department;

SELECT student_name, marks
FROM Students
ORDER BY marks DESC
LIMIT 1;



