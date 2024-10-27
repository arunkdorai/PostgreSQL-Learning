In this video, the instructor explains how to use **INNER JOIN** in PostgreSQL to combine data from two tables, specifically the `person` and `car` tables, based on their foreign key relationship. Here’s a summary of the key concepts and steps:

### Key Concepts

1. **INNER JOIN**: This type of join combines records from two tables where there is a match in the foreign key and primary key.
2. **Resulting Table**: The result of an inner join contains only the rows that have matching values in both tables.

### Steps to Perform an INNER JOIN

1. **Basic SELECT with INNER JOIN**:
   - To combine the `person` and `car` tables, the instructor uses the following SQL command:
     ```sql
     SELECT * FROM person
     JOIN car ON person.car_id = car.id;
     ```
   - This query selects all columns from both tables for records where `car_id` in the `person` table matches the `id` in the `car` table.

2. **Expanded View**:
   - To improve readability, the instructor toggles an expanded display in the query tool, making the output clearer.

3. **Verifying Results**:
   - The resulting dataset shows which persons have cars and the details of those cars. If a person doesn't own a car (like Adriana), they won't appear in the result.

4. **Selecting Specific Columns**:
   - Instead of selecting all columns, you can specify which columns to retrieve. For example:
     ```sql
     SELECT person.first_name, car.model, car.price
     FROM person
     JOIN car ON person.car_id = car.id;
     ```
   - This command selects only the first name of the person, the model of the car, and the car's price.

5. **Toggling Display**:
   - The instructor demonstrates how to toggle the expanded display off to revert to the standard view.

### Summary
The video effectively illustrates how to perform an INNER JOIN in PostgreSQL to link records from two related tables. This allows you to extract relevant data based on existing relationships while emphasizing the importance of understanding which columns to include in your results. 
