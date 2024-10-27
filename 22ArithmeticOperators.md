
### Arithmetic Operators in PostgreSQL

1. **Purpose**:
   - Used to perform mathematical operations on numerical data.
   - Useful for generating statistics and calculating results from datasets.

2. **Basic Operators**:
   - **Addition**: 
     - Syntax: `SELECT 10 + 2;`
     - Result: `12`

   - **Subtraction**: 
     - Syntax: `SELECT 10 - 2;`
     - Result: `8`

   - **Multiplication**: 
     - Syntax: `SELECT 10 * 2;`
     - Result: `20`

   - **Division**: 
     - Syntax: `SELECT 10 / 2;`
     - Result: `5`

   - **Power**: 
     - Syntax: `SELECT 10 ^ 2;`
     - Result: `100`
     - Example: `10 ^ 3;` results in `1000`.

3. **Factorial**:
   - To calculate the factorial of a number:
     - Syntax: `SELECT factorial(5);`
     - Result: `120`

4. **Modulus**:
   - To find the remainder of a division:
     - Syntax: `SELECT 10 % 3;`
     - Result: `1` (since 3 goes into 10 three times with a remainder of 1).
   - Example: 
     - `SELECT 10 % 4;` results in `2`.
     - `SELECT 10 % 5;` results in `0`.
     - `SELECT 10 % 6;` results in `4`.

5. **Renaming Result Columns**:
   - Result columns are shown with `?column?` by default; can be renamed for clarity (explained in the video).

6. **Conclusion**:
   - Arithmetic operators in PostgreSQL are straightforward and similar to other programming languages (e.g., Java, C#, Python).

### Next Steps
- Upcoming video will demonstrate using arithmetic operators with a car table.



### Using Arithmetic Operators with a Car Table

1. **Selecting All Cars**:
   - To retrieve all cars from the car table:
     ```sql
     SELECT * FROM car;
     ```

2. **Calculating Discounts**:
   - **Goal**: Apply a 10% discount on the original price of each car.
   - **Query Structure**:
     - Select relevant columns (ID, Make, Model, Price) and calculate the discount:
     ```sql
     SELECT id, make, model, price FROM car;
     ```

3. **Calculating 10% of Price**:
   - To calculate 10% of the price for each car:
     ```sql
     SELECT price * 0.10 FROM car;
     ```

4. **Rounding Values**:
   - Use the `ROUND` function to round the calculated discount to two decimal places:
     ```sql
     SELECT ROUND(price * 0.10, 2) FROM car;
     ```

5. **Calculating Discounted Price**:
   - To find the price after applying the 10% discount:
     ```sql
     SELECT ROUND(price - (price * 0.10), 2) FROM car;
     ```
   - This calculates the discounted price by subtracting the 10% value from the original price.

6. **Results**:
   - Each result will show the price after the discount is applied, rounded to two decimal places.

7. **Complex Calculations**:
   - The example demonstrates basic arithmetic operations. More complex calculations can also be performed using similar methods.

### Conclusion
- The video illustrates how to use arithmetic operators to manipulate and analyze data from a PostgreSQL table.