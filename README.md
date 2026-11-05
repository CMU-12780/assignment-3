# Assignment 3: Concrete Test Reports

Complete a small Python program that stores concrete strength test results in a SQLite database and reports which tests passed. A test passes when its actual strength meets or exceeds its required strength. Strength is measured in pounds per square inch (PSI).

## Your task

Use the three provided scripts:

1. **`create_db.py`** creates `concrete.db` and the `concrete_tests` table. This script is already complete; review it to understand the table's columns.
2. **`insert_data.py`** contains eight test records. Add the code to insert those records into the table, using SQL parameters, and save the changes. The `passed` field uses `1` for a pass and `0` for a failure.
3. **`query.py`** needs three reports generated from SQL queries:
   - **All tests:** Show each project's name, actual strength, and `PASS` or `FAIL`, in insertion order.
   - **Failed tests:** Show each failed test's project, date, required strength, and actual strength, in insertion order.
   - **Tests per project:** Show the number of passing tests and total tests for each project, sorted alphabetically by project name. Use SQL grouping and aggregate functions to calculate the counts.

Use `output.txt` as the reference for report headings, spacing, and formatting. The report values should come from the database.

## Run and check

From the project directory, run:

```sh
python3 create_db.py
python3 insert_data.py
python3 query.py
```

Start with a fresh database and run the insertion script once to avoid duplicate records. Compare the output of `query.py` with `output.txt`: there should be eight tests, two failures, and a summary for each of the three projects.
