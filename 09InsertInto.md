
### Inserting Records into Tables

1. **Basic Structure**:
   - Use the `INSERT INTO` statement followed by the table name.
   - Specify the columns you want to insert values into.

   ```sql
   INSERT INTO person (first_name, last_name, gender, date_of_birth) VALUES ('Jane', 'Smith', 'female', '1988-01-09');
   ```

2. **Omitting Columns**:
   - If a column (e.g., email) is not included in the insert, it will be set to its default value (e.g., NULL if no default is defined).

3. **Auto Incrementing IDs**:
   - For the ID column defined as `SERIAL`, you do not need to specify a value; PostgreSQL automatically increments it.

4. **Inserting Multiple Records**:
   - You can insert multiple records in a single command by separating the value sets with commas.

   ```sql
   INSERT INTO person (first_name, last_name, gender, date_of_birth, email) VALUES 
   ('Jake', 'Jones', 'male', '1990-01-10', 'jake@example.com'),
   ('Alice', 'Brown', 'female', '1992-05-15', 'alice@example.com');
   ```

5. **Date Format**:
   - Use the format `YYYY-MM-DD` when specifying dates in SQL commands.

6. **Example of Inserting Without Email**:
   - If inserting a record without an email:

   ```sql
   INSERT INTO person (first_name, last_name, gender, date_of_birth) VALUES ('Mary', 'Johnson', 'female', '1985-03-22');
   ```

7. **Auto Increment Behavior**:
   - IDs will increment automatically (1, 2, 3, ...) with each new insertion.

By keeping these points in mind, you'll have a solid understanding of how to insert records into your PostgreSQL database!




### Working with psql Commands

1. **Listing Relations**:
   - Use `\d` to list all relations (tables, views, sequences).
   - Use `\dt` to show only tables.

2. **Inserting Records**:
   - Command structure: `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`
   - For example:
     ```sql
     INSERT INTO person (first_name, last_name, gender, date_of_birth) VALUES ('An', 'Smith', 'female', '1988-01-09');
     ```

3. **Omitting Auto-Incremented ID**:
   - Do not include the ID column in the insert statement; it is managed automatically by the sequence.

4. **Date Format**:
   - Use the format `YYYY-MM-DD` for dates when inserting.

5. **Ending Commands**:
   - Commands must end with a semicolon (`;`) to execute them.

6. **Reusing Commands**:
   - Use the up arrow key to retrieve and reuse the last command in the terminal.

7. **Example of Inserting Another Record**:
   - For a male person with an email:
     ```sql
     INSERT INTO person (first_name, last_name, gender, date_of_birth, email) VALUES ('Jake', 'Jones', 'male', '1990-12-31', 'jake@gmail.com');
     ```

8. **Confirmation of Insert**:
   - Upon successful insertion, psql returns a message indicating how many rows were affected (e.g., `INSERT 0 1`).

### Next Steps
- The next video will cover how to perform read operations on the `person` table, so be prepared to learn about querying data. 
