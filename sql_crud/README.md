# SQL - CRUD Operations

## Description
This project covers the fundamentals of SQL through the four CRUD operations (**C**reate, **R**ead, **U**pdate, **D**elete), applied to a single `books` table in a SQLite database. It goes from creating the table and inserting rows to filtering, sorting, limiting, aggregating and grouping the data.

Every task is a standalone `.sql` file containing one query, meant to be executed against `books_dataset.db`.

## 📝 Learning Objectives
* Create a table with typed columns and constraints (`PRIMARY KEY AUTOINCREMENT`, `NOT NULL`).
* Insert multiple rows with a single `INSERT INTO ... VALUES`.
* Read data with `SELECT`, filter it with `WHERE` (`AND`, `OR`), sort it with `ORDER BY` and cap it with `LIMIT`.
* Modify and remove rows safely with `UPDATE ... SET` and `DELETE FROM` (always with a `WHERE` clause).
* Use aggregate functions (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`) and group results with `GROUP BY`.

## 🛠️ Requirements & Engineering Constraints
* **OS:** Ubuntu 20.04 LTS
* **Database:** SQLite 3
* **Files:** Each `.sql` file contains a single query and ends with a new line.
* **Dataset:** `books_dataset.db` contains a `books` table (`id`, `title`, `author`, `genre`, `price`, `stock`, `published_year`).

## 📁 File List & Tasks Directory

| File | Task Title | Description |
| :--- | :--- | :--- |
| `0-create_table.sql` | Create a table | Creates the `books` table if it does not already exist. |
| `1-insert_data.sql` | Insert data | Inserts five books (Tolkien, Orwell, Martin, Hunt, Herbert) in a single statement. |
| `2-select_all.sql` | Select everything | Lists all columns of every book. |
| `3-select_columns.sql` | Select columns | Lists only the `title` and `price` of every book. |
| `4-filter_by_genre.sql` | Filter by genre | Lists the title and author of all `Tech` books. |
| `4-filter_by_price.sql` | Filter by price | Lists books priced above 20. |
| `4-filter_with_and.sql` | Filter with AND | Lists `Tech` books priced above 30. |
| `4-filter_with_or.sql` | Filter with OR | Lists books that are `Fantasy` **or** cost less than 10. |
| `5-update_by_id.sql` | Update by id | Sets the price of the book with `id = 3` to 35.00. |
| `5-update_by_condition.sql` | Update by condition | Adds 5 units of stock to every book published before 2000. |
| `5-update_with_and.sql` | Update with AND | Applies a 10% discount to `Tech` books with more than 5 in stock. |
| `6-delete_by_id.sql` | Delete by id | Deletes the book with `id = 8`. |
| `6-delete_by_condition.sql` | Delete by condition | Deletes every book that is out of stock. |
| `6-delete_with_and.sql` | Delete with AND | Deletes books published before 1950 and priced under 9. |
| `7-order_by_price_asc.sql` | Sort by price | Lists titles and prices from cheapest to most expensive. |
| `7-order_by_year_desc.sql` | Sort by year | Lists titles and publication years from newest to oldest. |
| `7-limit_results.sql` | Limit results | Lists the 3 cheapest books. |
| `7-order_and_limit.sql` | Order and limit | Lists the 5 books with the highest stock. |
| `8-count_books.sql` | Count rows | Counts the books in the table. |
| `8-average_price.sql` | Average | Computes the average book price. |
| `8-min_price.sql` | Minimum | Finds the lowest price. |
| `8-max_stock.sql` | Maximum | Finds the highest stock value. |
| `8-total_stock.sql` | Sum | Computes the total stock across all books. |
| `9-count_by_genre.sql` | Group by genre | Counts books per genre. |
| `9-count_by_author.sql` | Group by author | Counts books per author. |
| `9-average_price_by_genre.sql` | Average per genre | Computes the average price per genre. |
| `9-total_stock_by_genre.sql` | Stock per genre | Computes the total stock per genre. |
| `10-select_tech_books.sql` | Recent tech books | Lists title, price and stock of `Tech` books published in 2000 or later. |
| `10-cheapest_available.sql` | Cheapest available | Lists the 4 cheapest books that are in stock. |
| `10-increase_stock.sql` | Restock | Adds 3 units to every book with fewer than 5 in stock. |
| `10-delete_zero_stock.sql` | Clean up | Deletes every book that is out of stock. |
| `10-average_price_by_genre.sql` | Average per genre | Computes the average price per genre. |
| `10-stock_by_genre.sql` | Stock per genre | Computes the total stock per genre. |
| `books_dataset.db` | Dataset | SQLite database holding the `books` table used by the queries. |

---

## 🚀 Execution

Run a query against the dataset with the `sqlite3` CLI:

```bash
sqlite3 books_dataset.db < 2-select_all.sql
```

Or build the database from scratch:

```bash
sqlite3 my_books.db < 0-create_table.sql
sqlite3 my_books.db < 1-insert_data.sql
sqlite3 my_books.db < 4-filter_by_genre.sql
```

---

## 👤 Author
* **Student:** [RebornLPB](https://github.com/RebornLPB)
* **GitHub:** [https://github.com/RebornLPB](https://github.com/RebornLPB)
* **School:** [Holberton School](https://www.holbertonschool.com/)
