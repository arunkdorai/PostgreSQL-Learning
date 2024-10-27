In this video, the focus is on using **CHECK constraints** in PostgreSQL, which allow you to enforce specific conditions on the data in your tables. Here are the main points covered:

### CHECK Constraints

1. **Purpose**:
   - CHECK constraints ensure that values in a specified column meet certain criteria, which can be defined using boolean expressions.

2. **Example Scenario**:
   - The video uses a `person` table with a `gender` column to illustrate the need for a CHECK constraint. The goal is to restrict this column to only allow "male" or "female".

3. **Identifying Existing Values**:
   - To see the current values in the `gender` column, the query used is:
     ```sql
     SELECT DISTINCT gender FROM person;
     ```

4. **Adding a CHECK Constraint**:
   - To add a CHECK constraint to enforce that `gender` can only be "male" or "female":
     ```sql
     ALTER TABLE person ADD CONSTRAINT gender_check CHECK (gender = 'male' OR gender = 'female');
     ```

5. **Constraint Violation**:
   - If the constraint fails (due to existing data), an error will be thrown. For example, if there’s a gender value of "hello", you must remove it:
     ```sql
     DELETE FROM person WHERE gender = 'hello';
     ```

6. **Successful Constraint Addition**:
   - Once all violating rows are removed, you can successfully add the CHECK constraint.

7. **Enforcing the Constraint**:
   - After adding the constraint, any attempt to insert a record with a gender outside the allowed values will fail:
     ```sql
     INSERT INTO person (name, gender) VALUES ('Fernanda', 'hello');  -- This will fail
     ```

8. **Flexibility of CHECK Constraints**:
   - CHECK constraints can be used for various conditions. For example, you might enforce that a product's price must be greater than zero:
     ```sql
     ALTER TABLE product ADD CONSTRAINT price_check CHECK (price > 0);
     ```

### Conclusion
- CHECK constraints are a powerful way to maintain data integrity in your database by ensuring that all values in a specified column adhere to defined rules.
