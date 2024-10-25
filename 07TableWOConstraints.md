
Creating a table without constraints:

1. **Connect to the Database**:
   - Use the command: `\c test` to connect to the database named "test".

2. **Clear the Screen**:
   - Use `Ctrl + L` to clear the terminal screen.

3. **Create a Table**:
   - Use the command structure:
     ```sql
     CREATE TABLE person (
       ID INT,
       first_name VARCHAR(50),
       last_name VARCHAR(52),
       gender VARCHAR(7),
       date_of_birth DATE
     );
     ```
   - Ensure to end the command with a semicolon.

4. **Data Types**:
   - Use `INT` for integers.
   - Use `VARCHAR(n)` for variable character strings, where `n` is the maximum length.
   - Use `DATE` for date values.

5. **Viewing Tables**:
   - To list all tables in the database, use: `\d`.
   - To describe a specific table (e.g., `person`), use: `\d person`.

6. **Table Description Output**:
   - Shows columns and their data types.
   - Includes additional information like constraints (e.g., nullable).