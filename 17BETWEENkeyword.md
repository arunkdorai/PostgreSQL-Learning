Notes on using the `BETWEEN` keyword:

1. **Purpose of BETWEEN**:
   - The `BETWEEN` keyword is used to select records within a specified range.

2. **Basic Syntax**:
   - The syntax for using `BETWEEN` is as follows:
     ```sql
     SELECT * FROM person 
     WHERE date_of_birth BETWEEN '2000-01-01' AND '2015-01-01';
     ```

3. **Date Format**:
   - Ensure the dates are in the correct format (YYYY-MM-DD).
   - The start date is inclusive, and the end date is also inclusive.

4. **Example Use Case**:
   - To find everyone born between 2000 and 2015:
     ```sql
     SELECT * FROM person 
     WHERE date_of_birth BETWEEN '2000-01-01' AND '2015-12-31';
     ```

5. **Exclusion**:
   - Records with a date of birth earlier than 2000 or later than 2015 will not be included in the results.

6. **Conclusion**:
   - The `BETWEEN` keyword is a powerful tool for filtering results based on a range of values, particularly for dates.

These points should help you effectively use the `BETWEEN` keyword in your PostgreSQL queries!