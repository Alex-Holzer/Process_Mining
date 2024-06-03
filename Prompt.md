I am working on a process mining project in PySpark using Databricks, with the data stored in a DataFrame in the following format:

Columns:

- CASE_KEY (string): Represents the object to be tracked in the process mining project.
- Datum (datetime): The timestamp indicating when a specific event (Funktion) occurred for the corresponding CASE_KEY.
- Funktion (string): The event that occurred at the specific time indicated by the Datum column.
- Tarifname (string): May contain null values or blanks.

The CASE_KEY column represents the object I want to track in the process mining project.
The Datum column is the timestamp indicating when a specific event (Funktion) occurred for the corresponding CASE_KEY.
The Funktion column represents the event that occurred at the specific time indicated by the Datum column.

Example Dataset:

| CASE_KEY | Datum            | Funktion                  | Tarifname   |
| -------- | ---------------- | ------------------------- | ----------- |
| A1       | 2022-01-23 08:00 | Antrag Start              | AT          |
| A1       | 2022-01-23 08:10 | Fristablauf ext.          | Signatul BU |
| A1       | 2022-01-23 08:15 | Vorschlag                 |             |
| A1       | 2022-01-23 08:22 | Antrag (Papier)           |             |
| A1       | 2022-01-23 08:25 | Vorschlag                 | WK          |
| A1       | 2022-01-23 08:29 | Ext. Signatur Übermittelt |             |
| A1       | 2022-01-23 08:30 | Ext. Signatur erfolgt BU  | null        |
| A2       | 2022-01-23 10:00 | Antrag Start              |             |
| A2       | 2022-01-23 10:20 | Sync                      |             |
| A2       | 2022-01-23 10:50 | Laden                     | None        |
| A2       | 2022-01-23 11:00 | Antrag (VE)               |             |
| A2       | 2022-01-23 11:01 | Geloescht                 |             |

Task:
Write expert-level Python PySpark code with the following requirements:

Requirements:

- The code must be clean, reusable and efficient for large datasets.
- Avoid unnecessary loops and UDFs by leveraging PySpark's internal functions.
- Ensure the code is well-organized, follows naming conventions, and is thoroughly documented.
- Include type hints, docstrings, and examples for clarity and ease of integration.
- The code should be written in a way that is easy to understand and use in a PySpark project.
- Use Input validation and error handling where necessary.
- The code should be scalable and optimized for performance.
- The code should be tested with the provided example dataset to ensure correctness.


