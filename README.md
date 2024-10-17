# 0x00. MySQL advanced

# Project Overview

The goal of this project is to design and implement a database system capable of efficiently managing user data. The database focuses on a `names` table that stores user names, scores, and optional meeting dates. The project progresses through a series of tasks, including data insertion, retrieval, filtering, manipulation, and optimization using indexing. Additionally, stored procedures and error-handling functions are introduced to automate complex operations and ensure data integrity.

Each task is designed to enhance the database's functionality and performance, moving from basic CRUD operations to more advanced optimizations like indexing and stored procedures.

## Task 0: Create `names` Table
**Goal**: Create a `names` table with the following fields:
- `id`: an integer primary key.
- `name`: a string.
- `score`: an integer.
- `last_meeting`: a date field (optional).

**Requirements**:
- Define the table with the specified fields.
- `id` should be the primary key.
- `last_meeting` can be `NULL`.

---

## Task 1: Insert 1000 Names
**Goal**: Insert 1000 random names into the `names` table, along with a random score between 0 and 100.

**Requirements**:
- Use a script or query to generate and insert 1000 names with random scores.
- Ensure the script runs efficiently.

---

## Task 2: Select All Ordered
**Goal**: Write a query to select all names from the `names` table, ordered by `score` in descending order.

**Requirements**:
- Retrieve all rows, ordering by the `score` column in descending order.

---

## Task 3: Select Top 100
**Goal**: Write a query to select the top 100 names by score, ordered by `score` in descending order.

**Requirements**:
- Limit the query to return only the top 100 results.
- Sort by `score` in descending order.

---

## Task 4: Select Specific User
**Goal**: Write a query to select a specific user from the `names` table based on their `id`.

**Requirements**:
- Retrieve a user by their `id`.
- Ensure the query returns the correct user details.

---

## Task 5: Select and Filter
**Goal**: Write a query to select all users with a `score` between 50 and 70, ordered by `score`.

**Requirements**:
- Retrieve all users with a `score` in the range of 50 to 70.
- Order the results by `score` in ascending order.

---

## Task 6: Update User Score
**Goal**: Write a query to update the `score` of a specific user in the `names` table, identified by their `id`.

**Requirements**:
- Update a user's `score` based on their `id`.
- Ensure only the target user’s score is updated.

---

## Task 7: Delete Low Scores
**Goal**: Write a query to delete all users from the `names` table where the `score` is below 20.

**Requirements**:
- Delete all users whose score is less than 20.

---

## Task 8: Optimize Simple Search
**Goal**: Create an index `idx_name_first` on the `names` table to index only the first letter of `name`.

**Requirements**:
- Use `LIKE 'a%'` to perform searches.
- Index only the first letter of the `name` field.

---

## Task 9: Optimize Search and Score
**Goal**: Create an index `idx_name_first_score` on the `names` table to index the first letter of `name` and the `score` column.

**Requirements**:
- Index both the first letter of `name` and the `score`.
- Optimize search performance for queries involving both fields.

---

## Task 10: Safe Divide
**Goal**: Write a function `SafeDiv` that returns `a / b`, but returns `0` if `b` is `0`.

**Requirements**:
- Input: two integers `a` and `b`.
- If `b == 0`, return `0` instead of dividing by zero.

---

## Task 11: No Table for a Meeting
**Goal**: Create a view `need_meeting` that lists students with a score under 80 and no `last_meeting` or a `last_meeting` more than one month ago.

**Requirements**:
- Check if the `score` is under 80.
- Check if `last_meeting` is either `NULL` or older than one month.

---

## Task 12: Average Weighted Score
**Goal**: Create a stored procedure `ComputeAverageWeightedScoreForUser` that calculates the average weighted score for a user based on their project scores and weights.

**Requirements**:
- The procedure should take one input: `user_id`.
- Calculate the weighted average using the project `weight` and score.

