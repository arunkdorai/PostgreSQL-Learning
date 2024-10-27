
### Handling Nulls with COALESCE function in PostgreSQL

1. **Introduction to COALESCE**:
   - The `COALESCE` function returns the first non-null value from the provided list of arguments.
   - Useful for providing default values when a column may contain nulls.

2. **Basic Usage**:
   - Syntax:
     ```sql
     SELECT COALESCE(value1, value2, ...);
     ```
   - Example:
     ```sql
     SELECT COALESCE(1, 2); -- Result: 1
     ```

3. **Handling Null Values**:
   - If the first value is null, `COALESCE` checks the next value:
     ```sql
     SELECT COALESCE(NULL, 10, 20); -- Result: 10
     ```

4. **Applying COALESCE with a Dataset**:
   - Use `COALESCE` to handle null emails in a `person` table:
     ```sql
     SELECT email FROM person;
     ```
   - To replace null emails with a default value:
     ```sql
     SELECT COALESCE(email, 'Email not provided') FROM person;
     ```

5. **Result**:
   - This will return "Email not provided" for any person without an email, ensuring no null values in the output.

6. **Practical Example**:
   - For individuals without emails:
     - The output will now display "Email not provided" in place of nulls.

7. **Conclusion**:
   - The `COALESCE` function is powerful for managing nulls in datasets, providing a way to ensure meaningful output instead of null values.
