

### Using Aliases for Column Names in PostgreSQL

1. **Default Behavior**:
   - When using functions in a query without specifying a column name, PostgreSQL defaults to using the function name or assigns `?column?` as the column name.

2. **Using the Alias Keyword**:
   - The `AS` keyword is used to provide a custom name (alias) for columns in your query.
   - Syntax:
     ```sql
     SELECT column_name AS alias_name FROM table;
     ```

3. **Renaming Columns in the Previous Query**:
   - Example of renaming columns for clarity:
     - **Original Price**:
       ```sql
       SELECT price AS "Original Price", 
              ROUND(price * 0.10, 2) AS "10% Value",
              ROUND(price - (price * 0.10), 2) AS "Discount After 10%"
       FROM car;
       ```

4. **Result**:
   - The output will display:
     - `Original Price` for the original car price.
     - `10% Value` for the calculated discount.
     - `Discount After 10%` for the final discounted price.

5. **Consistency in Naming**:
   - Ensure that names are consistent and clear for better readability.

6. **Conclusion**:
   - Using aliases improves the clarity of query results and makes it easier to understand the output.

