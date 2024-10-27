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

If you have any specific questions or need clarification on any of the steps, feel free to ask!