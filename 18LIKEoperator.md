How to use the `LIKE` operator in SQL, including key concepts and examples:

### `LIKE` Operator Overview
- The `LIKE` operator is used to search for a specified pattern in a column, particularly useful for matching text values.

### Wildcards
1. **Percent Sign (%)**:
   - Represents zero or more characters.
   - Example: To find all emails ending in `.com`:
     ```sql
     SELECT * FROM person WHERE email LIKE '%.com';
     ```

2. **Underscore (_)**
   - Represents a single character.
   - Example: To find emails with exactly eight characters before the `@`:
     ```sql
     SELECT * FROM person WHERE email LIKE '_______@%';
     ```

### Pattern Matching Examples
- **Match Emails Ending with Specific Domain**:
  - Find anyone with an email from `bloomberg.com`:
    ```sql
    SELECT * FROM person WHERE email LIKE '%bloomberg.com';
    ```

- **Match Emails from Any Google Domain**:
  - Use wildcards to match emails from Google regardless of the country:
    ```sql
    SELECT * FROM person WHERE email LIKE '%@google.%';
    ```

- **Match Countries Starting with a Specific Letter**:
  - To find countries starting with "P":
    ```sql
    SELECT * FROM person WHERE country_of_birth LIKE 'P%';
    ```

### Case Sensitivity
- The `LIKE` operator is case-sensitive in some SQL dialects. To perform a case-insensitive search, use the `ILIKE` operator (in PostgreSQL):
  ```sql
  SELECT * FROM person WHERE country_of_birth ILIKE 'p%';
  ```

### Conclusion
- The `LIKE` operator is versatile for searching patterns in text fields. Remember to use `%` for multiple characters and `_` for single character matches. Use `ILIKE` for case-insensitive matches when needed.
