# Holberton School - Data Modeling & Persistence

## 📖 About
This repository gathers the projects completed during the **Data Modeling & Persistence** track at **Holberton School**. It focuses on storing, querying and relating data with SQL: from basic CRUD operations on a single table to joins and subqueries across several related tables.

---

## 🛠️ General Requirements & Environment
* **OS:** Ubuntu 20.04 LTS
* **Database:** SQLite 3 (`sqlite3` CLI)
* **Files:** Each task is a standalone `.sql` file containing a single query.

---

## 📚 Project Overview

| Directory | Core Concepts / Highlights | Key Files |
| :--- | :--- | :--- |
| [`sql_crud`](sql_crud/) | `CREATE TABLE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`, `ORDER BY`, `LIMIT`, aggregates, `GROUP BY` | `0-create_table.sql`, `4-filter_with_and.sql`, `9-count_by_genre.sql` |
| [`sql_join`](sql_join/) | `INNER JOIN`, `LEFT JOIN`, junction tables, `HAVING`, subqueries | `3-students-and-courses.sql`, `6-courses-above-average.sql` |

---

## 🚀 Quick Start

```bash
git clone https://github.com/RebornLPB/holbertonschool-data_modeling_and_persistence.git
cd holbertonschool-data_modeling_and_persistence/sql_crud

# Run a query against the bundled dataset
sqlite3 books_dataset.db < 2-select_all.sql
```

---

## 👤 Author
* **Student:** [RebornLPB](https://github.com/RebornLPB)
* **GitHub:** [https://github.com/RebornLPB](https://github.com/RebornLPB)
* **School:** [Holberton School](https://www.holbertonschool.com/)
