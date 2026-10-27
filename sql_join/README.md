# SQL - Joins & Subqueries

## Description
This project covers querying data spread across several related tables using SQL joins (`INNER JOIN`, `LEFT JOIN`), aggregation with `GROUP BY` / `HAVING`, and subqueries. The queries model a small school/library domain: authors and books, students and courses, instructors, registrations and assignments.

Every task is a standalone `.sql` file containing a single query. Tasks 1 to 7 run against the bundled `library.db`.

## 📝 Learning Objectives
* Combine tables with `INNER JOIN` and keep unmatched rows with `LEFT JOIN`.
* Traverse a many-to-many relationship through a junction table (`enrollments`, `registrations`).
* Count and group related rows with `COUNT`, `GROUP BY` and `HAVING`.
* Use subqueries (`IN`, scalar subquery for an average) to filter on computed values.
* Remove duplicates with `DISTINCT` and control output with `ORDER BY` and column aliases.

## 🛠️ Requirements & Engineering Constraints
* **OS:** Ubuntu 20.04 LTS
* **Database:** SQLite 3
* **Files:** Each `.sql` file contains a single query and ends with a new line.
* **Dataset:** `library.db` contains the tables `authors`, `books`, `students`, `courses` and `enrollments`.
* **Note:** Tasks 8 to 15 reference additional tables (`instructors`, `registrations`, `assignments`, and `courses.instructor_id`) that are **not** present in the bundled `library.db`; they target the extended schema provided with those tasks.

## 📁 File List & Tasks Directory

| File | Task Title | Description |
| :--- | :--- | :--- |
| `1-books-with-authors.sql` | Books with authors | `INNER JOIN` listing each book title with its author's name, sorted by title. |
| `2-authors-with-books.sql` | Authors with books | `LEFT JOIN` listing every author with their books, including authors without any. |
| `3-students-and-courses.sql` | Students and courses | Lists each student with the courses they are enrolled in, through `enrollments`. |
| `4-courses-and-students.sql` | Courses and students | Lists every course with its students, including courses with no enrollment. |
| `5-students-with-enrollments.sql` | Enrolled students | Lists students that have at least one enrollment, using an `IN` subquery. |
| `6-courses-above-average.sql` | Popular courses | Lists courses whose enrollment count is above the average enrollment count. |
| `7-course-enrollment-count.sql` | Enrollment count | Counts enrollments per course (zero included), sorted from most to least popular. |
| `8-courses-and-instructors.sql` | Courses and instructors | Lists each course with its instructor. |
| `9-instructors-and-courses.sql` | Instructors and courses | Lists every instructor with their courses, including instructors without courses. |
| `10-students-and-registered-courses.sql` | Registered courses | Lists each student with the courses they registered for, through `registrations`. |
| `11-course-registration-count.sql` | Registration count | Counts registrations per course (zero included), sorted from most to least registered. |
| `12-students-with-registrations.sql` | Registered students | Lists distinct students with at least one registration. |
| `13-courses-above-average-assignments.sql` | Heavy courses | Lists courses with more assignments than the average number of assignments per course. |
| `14-courses-and-assignments.sql` | Courses and assignments | Lists every course with its assignments, including courses with none. |
| `15-instructors-with-active-courses.sql` | Active instructors | Lists distinct instructors whose courses have at least one registration. |
| `library.db` | Dataset | SQLite database used by tasks 1 to 7. |

---

## 🚀 Execution

```bash
sqlite3 library.db < 1-books-with-authors.sql
```

To explore the dataset interactively:

```bash
sqlite3 library.db
sqlite> .tables
sqlite> .schema enrollments
```

---

## 👤 Author
* **Student:** [RebornLPB](https://github.com/RebornLPB)
* **GitHub:** [https://github.com/RebornLPB](https://github.com/RebornLPB)
* **School:** [Holberton School](https://www.holbertonschool.com/)
