In this video, the instructor demonstrates how to establish a relationship between two tables in PostgreSQL: `person` and `car`. The relationship is defined such that one person can own one car, and each car can belong to only one person. Here’s a summary of the steps taken:

### Steps to Add a Relationship Between Tables

1. **Dropping Existing Tables**:
   - The instructor begins by dropping the existing `person` and `car` tables to clear any previous data.
   - Command: `DROP TABLE person; DROP TABLE car;`

2. **Creating New Tables**:
   - The instructor provides a downloadable SQL file (`person-car.sql`) to create the new structure for the tables.

3. **Defining the Car Table**:
   - A new column, `car_id`, is added to the `person` table to establish a foreign key relationship. 
   - The data type for `car_id` is specified as `BIGINT`, which is appropriate for referencing IDs.

4. **Adding Foreign Key Reference**:
   - The `car_id` column is defined to reference the `id` column in the `car` table.
   - A unique constraint is added to `car_id` to ensure that a car can be associated with only one person.

5. **Executing SQL Commands**:
   - The instructor mentions executing the SQL commands to create the tables and insert initial data.
   - Ensures that the `car` table is created before attempting to reference it in the `person` table.

6. **Inserting Data**:
   - Once the tables are created, the instructor checks the data by selecting from both tables to confirm that the structures are set up correctly.

7. **Next Steps**:
   - The video concludes by mentioning that the next part will involve assigning a car to a person.

### Summary
This video effectively walks through the process of creating a relationship between two tables using foreign keys in PostgreSQL. It emphasizes the importance of proper table creation and the implications of relationships in relational databases.



In this video, the instructor demonstrates how to assign cars to people in a PostgreSQL database, utilizing the foreign key relationship established earlier. Here's a summary of the key steps and concepts covered:

### Steps to Assign Cars to People

1. **Initial State**:
   - The `car_id` column in the `person` table is initially empty for all entries.

2. **Updating Car Assignments**:
   - The instructor updates the `car_id` for two people, **Fernanda** and **Omar**, using SQL `UPDATE` statements.

3. **Assigning Car to Fernanda**:
   - The command to assign the car (GMC) to Fernanda is executed:
     ```sql
     UPDATE person SET car_id = 2 WHERE id = 1;
     ```
   - After executing, the database confirms that Fernanda has been assigned a car.

4. **Attempting to Assign the Same Car to Omar**:
   - The instructor tries to assign the same car (GMC) to Omar:
     ```sql
     UPDATE person SET car_id = 2 WHERE id = 2;
     ```
   - The database throws an error due to the unique constraint on `car_id`, confirming that the constraint is functioning as intended.

5. **Assigning a Different Car to Omar**:
   - Omar is then assigned a different car (Land Rover):
     ```sql
     UPDATE person SET car_id = 1 WHERE id = 2;
     ```
   - This assignment is successful, showing that Omar is now linked to the Land Rover.

6. **Verifying Assignments**:
   - The instructor runs `SELECT` queries to display the updated tables:
     - Checking the `person` table to see which car IDs are assigned to each person.
     - Checking the `car` table to confirm the details of the cars assigned.

7. **Attempting to Assign a Non-Existent Car**:
   - An attempt is made to assign a car ID that does not exist in the `car` table (ID = 3):
     ```sql
     UPDATE person SET car_id = 3 WHERE id = 1;
     ```
   - The database throws a foreign key constraint violation error, reinforcing the importance of ensuring the foreign key must exist in the referenced table.

### Summary
The video effectively illustrates how to manage relationships between tables using foreign keys in PostgreSQL. It highlights the significance of unique constraints and foreign key constraints in maintaining data integrity.