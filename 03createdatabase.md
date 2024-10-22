
---

We added `psql` to the path previously, allowing us to run it directly. To start `psql`, just type `psql`, 

**Run the PSQL Command**:
   ```powershell
   psql -U postgres -h localhost -d postgres
   ```
   - Replace `postgres` with your username if different.
   - Replace `localhost` with the server address if connecting remotely.
   - Replace `postgres` at the end with your desired database name.

and you should see a welcome message with the version number.

- To get help, type `help`.
- All commands in `psql` start with a backslash (`\`).
- To exit `psql`, type `\q`.
- To clear screen in windows, you can use `\! cls`.

If you need more help, you can type `\?` for a list of commands. To list all databases, use:

```sql
\l
```

You will see several default databases, including `postgres`, `template0`, and `template1`. 

To create a new database, use the following command:

```sql
CREATE DATABASE test;
```

Make sure to end the command with a semicolon (`;`). After executing, you’ll see a confirmation message. To verify the creation, use `\l` again to list all databases, where you should now see your new database, `test`.

---