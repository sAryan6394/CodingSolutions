# Revising Aggregations - The Count Function

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Query a *count* of the number of cities in **CITY** having a *Population* larger than $100,000$. 

**Input Format**

The **CITY** table is described as follows:
<img src="https://s3.amazonaws.com/hr-challenge-images/8137/1449729804-f21d187d0f-CITY.jpg" title="CITY.jpg" />

**Constraints**

 

**Output Format**

## Solution

**Language:** SQL  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-07T13:45:43.033Z  

```sql
SELECT COUNT(id)
FROM CITY
WHERE population > 100000;

```

---

[View on HackerRank](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem)