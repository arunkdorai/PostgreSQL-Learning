
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