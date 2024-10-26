Selecting unique values:

1. **Selecting Data**:
   - Start by selecting a column: `SELECT country_of_birth FROM person;`

2. **Sorting Data**:
   - Use `ORDER BY` to sort results: `ORDER BY country_of_birth;`

3. **Identifying Duplicates**:
   - Initial query may return duplicate entries (e.g., multiple instances of the same country).

4. **Using DISTINCT**:
   - To get unique values, use the `DISTINCT` keyword:  
     `SELECT DISTINCT country_of_birth FROM person ORDER BY country_of_birth;`
   - This removes duplicates, showing each country only once.

5. **Sorting Unique Results**:
   - You can still apply sorting to the distinct results:  
     `ORDER BY country_of_birth;`

6. **Application of DISTINCT**:
   - The `DISTINCT` keyword can be used for any column, including dates and emails.

7. **Final Count**:
   - After using `DISTINCT`, you can see the total unique entries (e.g., 124 unique countries).

8. **Conclusion**:
   - The `DISTINCT` keyword is essential for filtering out duplicate records in your queries.

These points should help solidify your understanding of using `DISTINCT` in PostgreSQL!