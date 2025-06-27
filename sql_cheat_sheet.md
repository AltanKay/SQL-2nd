
# ✅ SQL Cheat Sheet

---

## 🔹 Basic Query

```sql
SELECT column1, column2
FROM table_name;
```

---

## 🔹 Rename Columns or Tables

```sql
SELECT column_name AS alias_name
FROM table_name AS alias_table;
```

---

## 🔹 Remove Duplicates

```sql
SELECT DISTINCT column_name
FROM table_name;
```

---

## 🔹 Filter Rows

```sql
SELECT *
FROM table_name
WHERE condition;
```

---

## 🔹 Pattern Matching (`LIKE`)

```sql
SELECT *
FROM table_name
WHERE column_name LIKE 'A%'; -- starts with A

-- Wildcards:
-- % = any sequence of characters
-- _ = any single character
```

---

## 🔹 Range Filter (`BETWEEN`)

```sql
SELECT *
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

---

## 🔹 Combine Conditions (`AND` / `OR`)

```sql
SELECT *
FROM table_name
WHERE condition1 AND condition2;

SELECT *
FROM table_name
WHERE condition1 OR condition2;
```

---

## 🔹 Sort Results (`ORDER BY`)

```sql
SELECT *
FROM table_name
ORDER BY column_name ASC; -- ascending
ORDER BY column_name DESC; -- descending
```

---

## 🔹 Limit Rows (`LIMIT`)

```sql
SELECT *
FROM table_name
LIMIT number;
```

---

## 🔹 Conditional Output (`CASE`)

```sql
SELECT column_name,
  CASE
    WHEN condition THEN result1
    WHEN condition THEN result2
    ELSE default_result
  END AS alias_name
FROM table_name;
```

---

## ⚡ Example Putting It All Together

```sql
SELECT 
  name AS student_name,
  age,
  CASE
    WHEN age >= 18 THEN 'Adult'
    ELSE 'Minor'
  END AS age_group
FROM students
WHERE age BETWEEN 18 AND 25
  AND name LIKE 'A%'
ORDER BY age DESC
LIMIT 5;
```

---

## ✔️ Handy SQLite Commands

```sql
.tables         -- List tables
.schema TABLE   -- Show table structure
.headers ON     -- Show column headers
.mode column    -- Pretty output
.exit           -- Quit SQLite
```

---

**Happy Querying!**
