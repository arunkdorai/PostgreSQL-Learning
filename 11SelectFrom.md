
### Reading Records from a Table

1. **Basic Select Statement**:
   - To retrieve records from a table, use the `SELECT` statement.
   - Syntax:
     ```sql
     SELECT * FROM person;
     ```
   - The asterisk (`*`) means to select all columns from the table.

2. **Selecting Specific Columns**:
   - You can specify particular columns you want to retrieve.
   - For example, to select only the first name and last name:
     ```sql
     SELECT first_name, last_name FROM person;
     ```

3. **Handling Missing Values**:
   - If a column contains NULL (or empty) values, it will return an empty result for that row.
   - For instance, selecting the email column for a person without an email will show NULL for that entry.

4. **Executing the Command**:
   - After typing your SQL command, end it with a semicolon (`;`) and press ENTER to execute.
   - You can clear the screen before executing commands for better visibility.

5. **Example Commands**:
   - Retrieve all records:
     ```sql
     SELECT * FROM person;
     ```
   - Retrieve only first names:
     ```sql
     SELECT first_name FROM person;
     ```
   - Retrieve first names and last names:
     ```sql
     SELECT first_name, last_name FROM person;
     ```

### Summary
You learned how to perform basic read operations in PostgreSQL using the `SELECT` statement, how to retrieve specific columns, and how to handle records with NULL values.