
### Creating Your First Table in PostgreSQL

1. **Basic Command Structure**:
   - Command to create a table: `CREATE TABLE table_name (column_definitions);`
   - Example: `CREATE TABLE person (column_definitions);`

2. **Column Definitions**:
   - Each column must have:
     - **Column Name**
     - **Data Type**
     - Optional: **Constraints**

3. **Example Table**: 
   - **Table Name**: `person`
   - **Column Definitions**:
     - `id INT` (integer)
     - `first_name VARCHAR(50)` (up to 50 characters)
     - `last_name VARCHAR(50)` (up to 50 characters)
     - `gender VARCHAR(6)` (up to 6 characters)
     - `date_of_birth DATE` (recommended instead of TIMESTAMP for birthdates)

4. **Data Types in PostgreSQL**:
   - Reference documentation: [PostgreSQL Data Types](https://www.postgresql.org/docs/17/datatype.html)
   - Common Data Types:
     - `BIGINT`: Signed 8-byte integer
     - `BOOLEAN`: True or false
     - `CHAR`, `VARCHAR(n)`: Character types (with length limit)
     - `DATE`: For dates (year, month, day)
     - `DOUBLE`, `JSON`, `MONEY`: Other specific types
     - `DECIMAL`, `NUMERIC`: For exact numeric values
     - `SMALLINT`: Smaller integer
     - `SERIAL`: Auto-incrementing integer
     - `TEXT`: No maximum length
     - `TIME`, `TIMESTAMP`: Includes date and time

5. **Recommendation**:
   - Familiarize yourself with various data types by navigating the provided documentation link.
