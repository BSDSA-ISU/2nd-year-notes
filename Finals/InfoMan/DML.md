# 📖 Data manipulation Language

> "I love Touhou" - By a BSDSA Student

![toe hoe yuri](https://media1.tenor.com/m/LIL19xdK9XEAAAAC/hop-on-gensou-skydrift-gensou-skydrift.gif)

---

- [📖 Data manipulation Language](#-data-manipulation-language)
  - [⬇️ Insert statement](#️-insert-statement)
  - [⬆️ Update Statement](#️-update-statement)
  - [❌ Delete Statement](#-delete-statement)

---

**A dml staement is executed when:**

- add new rows to a table
- Modify existing table
- Remove existing table

## ⬇️ Insert statement

Add new rows to a table by using the INSERT statement

```sql
INSERT INTO table_name (column1, column2) 
VALUES (value1, value2);
```

**Example:**

```sql
INSERT INTO Sales(sales_id, customer_name, product, category, price, quantity, sales_date)
VALUES (4, "Koishi Komeiji", "Satori Fumo", "Fumo", 102.4, 1, "2026-04-01");

-- Multiple
INSERT INTO Sales(sales_id, customer_name, product, category, price, quantity, sales_date)
VALUES (5, "Koishi Komeiji", "Satori Fumo", "Fumo", 102.4, 1, "2026-04-01"), (6, "Satori Komeiji", "Koishi Fumo", "Fumo", 102.4, 1, "2026-04-02");
```

| sales_id | customer_name | product | category | price | quantity | sales_date |
| - | - | - | - | - | - | - |
| 4 | Koishi Komeiji | Satori Fumo | Fumo | 102.4 | 1 | 2026-04-01 |
| 5 | Satori Komeiji | Koishi Fumo | Fumo | 102.4 | 1 | 2026-04-01 |

> with this syntax, only one row is inserted

## ⬆️ Update Statement

Modify existing value in a table with the **UPDATE** statement

```sql
UPDATE table
SET column1 = value1, column2 = value2, ...
[WHERE condition];
```

update more than one row at a time (If required).

```sql
-- statement 1
UPDATE sales
SET price =  price + 5000
WHERE product = 'Phone';

-- statement 2
UPDATE sales
SET quantity = 3
WHERE customer_name = 'Koishi komeiji';
```

## ❌ Delete Statement

You can remove existing rows from a table by using the DELETE statement

Removes rows from a table

```sql
-- Delete certain rows
DELETE FROM sales
WHERE prducts = 'Mouse';

DELETE FROM sales
WHERE catigory = 'Furniture';

-- delete all rows
DELETE FROM sales;
```
