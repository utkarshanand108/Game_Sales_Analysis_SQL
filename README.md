# DataScienceCourse4_Assignment2
**Analyzing Game Sales Across Regions and Platforms — DS PGC Course 4 Assignment 2**

---

## 📘 Assignment Overview
Analyze global **game-sales data** to understand performance across platforms and regions using SQL operations.  
This assignment involves **inserts, updates, deletes, joins, and aggregate queries** to extract business insights.

---

## 🧩 Tasks (Summary)
1. **Insert** a new game “Future Racing” (Genre = Racing, Developer = Speed Studios).  
2. **Update** the price of GameID 2 on PlayStation to 60.  
3. **Delete** record of GameID 5 from `GameSales`.  
4. **Aggregate** total units sold for each game across platforms and regions.  
5. **Identify** top game by units sold in North America.  
6. **Join** tables to list titles, platforms, regions, and units sold.  
7. **Left Join** to include games without sales records.  
8. **Find** sales records with missing game details.  
9. **Retrieve** unique sales records for North America and Europe (`UNION`, `IN`).  
10. **Retrieve** all sales for those regions without removing duplicates (`UNION ALL`).

---

## 🧰 Tools & Approach
- **SQL Engine:** MySQL / MariaDB  
- **Tables:** `Games`, `GameSales`  
- **Key Concepts:**  
  - `INSERT INTO`, `UPDATE`, `DELETE`  
  - `INNER JOIN`, `LEFT JOIN`  
  - `GROUP BY`, `SUM()`, `MAX()`, `COUNT()`  
  - `UNION`, `UNION ALL`, `COALESCE()`  
- **Focus:** data manipulation and regional sales analysis with aggregates and joins.

---

## 📂 Files Included
- `DataScienceCourse4Assignment2Question.pdf` — Assignment brief / problem statement.  
- `DataScienceCourse4Assignment2Solution.pdf` — Final SQL solution with queries and outputs.

---

## 🧮 Example Queries (From Solution)
```sql
-- Insert a new game
INSERT INTO Games (GameTitle, Genre, ReleaseDate, Developer)
VALUES ('Future Racing', 'Racing', '2024-10-01', 'Speed Studios');

-- Update price of GameID 2 on PlayStation to 60
UPDATE GameSales SET Price = 60 WHERE GameID = 2 AND Platform = 'PlayStation';

-- Delete GameID 5
DELETE FROM GameSales WHERE GameID = 5;

-- Total units sold for each game
SELECT g.GameTitle, SUM(gs.UnitsSold) AS TotalUnits
FROM Games g
JOIN GameSales gs ON g.GameID = gs.GameID
GROUP BY g.GameTitle;
```

---

## 🧭 How to Review
1. Open `DataScienceCourse4Assignment2Solution.pdf`.  
2. Copy each query to your SQL client (MySQL Workbench / DBeaver / VS Code extension).  
3. Execute and compare outputs with the PDF screenshots.  
4. Verify joins, aggregations, and regional filters match assignment tasks.

---

## 👤 Author
**Utkarsh Anand**  
DS PGC Course 4 — Internshala Trainings
