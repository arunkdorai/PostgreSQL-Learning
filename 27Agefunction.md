
### Using the AGE Function in PostgreSQL

1. **Overview of the Table**:
   - The `person` table contains columns: first name, last name, gender, email, date of birth, and country of birth.

2. **Basic Select Query**:
   - To retrieve basic information:
     ```sql
     SELECT first_name, last_name, gender, country_of_birth, date_of_birth FROM person;
     ```

3. **Adding the Age Column**:
   - To include an additional column for age, use the `AGE` function.

4. **AGE Function Syntax**:
   - The `AGE` function takes two arguments:
     - The current timestamp (or any reference date).
     - The date of birth.
   - Example:
     ```sql
     SELECT first_name, last_name, gender, country_of_birth, date_of_birth, AGE(NOW(), date_of_birth) AS age FROM person;
     ```

5. **Result**:
   - The query will return a new column showing the age, which includes years, months, and days.

6. **Extracting Specific Components**:
   - You can extract specific parts of the age (like just years) if needed.

7. **Conclusion**:
   - The `AGE` function is useful for calculating and displaying age based on date of birth, enhancing data insights in your application.
