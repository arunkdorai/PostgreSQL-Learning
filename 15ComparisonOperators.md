Comparison operators:

1. **Purpose of Comparison Operators**:
   - Allow you to compare values and return `true` or `false`.

2. **Types of Comparison Operators**:
   - **Equal to**: `=`  
     Example: `SELECT 1 = 1;` (Returns `true`)
   - **Not equal to**: `<>` or `!=`  
     Example: `SELECT 1 <> 2;` (Returns `true`)

3. **Relational Operators**:
   - **Less than**: `<`  
     Example: `SELECT 1 < 2;` (Returns `true`)
   - **Less than or equal to**: `<=`  
     Example: `SELECT 1 <= 1;` (Returns `true`)
   - **Greater than**: `>`  
     Example: `SELECT 2 > 1;` (Returns `true`)
   - **Greater than or equal to**: `>=`  
     Example: `SELECT 1 >= 1;` (Returns `true`)

4. **Logical Reminder**:
   - The shape of the less-than symbol `<` resembles an "L," which can help remember its meaning.

5. **Using Comparison Operators with Different Data Types**:
   - You can use these operators with numbers, strings, dates, etc.
   - Example with strings:  
     - `SELECT 'Amigos Code' <> 'amigos code';` (Returns `true`)
     - `SELECT 'Amigos Code' = 'Amigos Code';` (Returns `true`)

6. **Combining with WHERE Clause**:
   - Use comparison operators in the `WHERE` clause to filter data.  
     Example:  
     `SELECT * FROM person WHERE age > 18;`

7. **Conclusion**:
   - Comparison operators are fundamental for data filtering and conditional logic in SQL queries.

These points should provide a solid overview of comparison operators in PostgreSQL!