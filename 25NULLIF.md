
### Handling Division by Zero in PostgreSQL

1. **Understanding Division by Zero**:
   - Attempting to divide by zero results in an error:
     ```sql
     SELECT 10 / 0; -- This will throw an error: division by zero
     ```

2. **Using the `NULLIF` Function**:
   - The `NULLIF` function takes two arguments and returns `NULL` if they are equal; otherwise, it returns the first argument.
   - This can be used to avoid division by zero errors:
     ```sql
     SELECT NULLIF(dividend, divisor);
     ```

3. **Example of `NULLIF`**:
   - If you want to prevent division by zero:
     ```sql
     SELECT 10 / NULLIF(0, 0); -- Returns NULL instead of an error
     ```

4. **Using `COALESCE` with Division**:
   - Combine `NULLIF` with `COALESCE` to provide a default value if a division by zero occurs:
     ```sql
     SELECT COALESCE(10 / NULLIF(0, 0), 0); -- Returns 0 instead of NULL
     ```

5. **Example Queries**:
   - If you have a non-zero divisor:
     ```sql
     SELECT 10 / NULLIF(2, 0); -- Returns 5
     ```
   - If you have a zero divisor:
     ```sql
     SELECT COALESCE(10 / NULLIF(0, 0), 'Division by zero'); -- Returns 'Division by zero'
     ```

6. **Conclusion**:
   - Using `NULLIF` allows for safe division operations without throwing errors, and `COALESCE` can be used to provide meaningful output when division by zero is attempted.
