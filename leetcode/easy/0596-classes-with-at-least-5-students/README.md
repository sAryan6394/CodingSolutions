# Classes With at Least 5 Students

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Table: `Courses`

```
+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| student     | varchar |
| class       | varchar |
+-------------+---------+
(student, class) is the primary key (combination of columns with unique values) for this table.
Each row of this table indicates the name of a student and the class in which they are enrolled.

```

 

Write a solution to find all the classes that have  **at least five students**.

Return the result table in  **any order**.

The result format is in the following example.

 

 **Example 1:** 

```
Input: 
Courses table:
+---------+----------+
| student | class    |
+---------+----------+
| A       | Math     |
| B       | English  |
| C       | Math     |
| D       | Biology  |
| E       | Math     |
| F       | Computer |
| G       | Math     |
| H       | Math     |
| I       | Math     |
+---------+----------+
Output: 
+---------+
| class   |
+---------+
| Math    |
+---------+
Explanation: 
- Math has 6 students, so we include it.
- English has 1 student, so we do not include it.
- Biology has 1 student, so we do not include it.
- Computer has 1 student, so we do not include it.

```

## Solution

**Language:** Python  
**Runtime:** 350 ms (beats 5.09%)  
**Memory:** 66.9 MB (beats 99.17%)  
**Submitted:** 2026-10-27T10:46:41.725Z  

```py
import pandas as pd

def find_classes(courses: pd.DataFrame) -> pd.DataFrame:
    df = courses.groupby('class')['student'].count().reset_index()
    return df[df['student'] >= 5][['class']]
```

---

[View on LeetCode](https://leetcode.com/problems/classes-with-at-least-5-students/)