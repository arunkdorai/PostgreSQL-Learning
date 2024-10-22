# psql --help

`psql` is the PostgreSQL interactive terminal.

## Usage

psql [OPTION]... [DBNAME [USERNAME]]


## General options:
- `-c, --command=COMMAND`    run only single command (SQL or internal) and exit
- `-d, --dbname=DBNAME`      database name to connect to
- `-f, --file=FILENAME`      execute commands from file, then exit
- `-l, --list`               list available databases, then exit
- `-v, --set=, --variable=NAME=VALUE`
                              set psql variable NAME to VALUE (e.g., -v ON_ERROR_STOP=1)
- `-V, --version`            output version information, then exit
- `-X, --no-psqlrc`          do not read startup file (`~/.psqlrc`)
- `-1 ("one"), --single-transaction`
                              execute as a single transaction (if non-interactive)
- `-?`, `--help[=options]`   show this help, then exit
    - `--help=commands`      list backslash commands, then exit
    - `--help=variables`     list special variables, then exit

## Input and output options:
- `-a, --echo-all`           echo all input from script
- `-b, --echo-errors`        echo failed commands
- `-e, --echo-queries`       echo commands sent to server
- `-E, --echo-hidden`        display queries that internal commands generate
- `-L, --log-file=FILENAME`  send session log to file
- `-n, --no-readline`        disable enhanced command line editing (readline)
- `-o, --output=FILENAME`    send query results to file (or |pipe)
- `-q, --quiet`              run quietly (no messages, only query output)
- `-s, --single-step`        single-step mode (confirm each query)
- `-S, --single-line`        single-line mode (end of line terminates SQL command)

## Output format options:
- `-A, --no-align`           unaligned table output mode
- `--csv`                    CSV (Comma-Separated Values) table output mode
- `-F, --field-separator=STRING`
                              field separator for unaligned output (default: "|")
- `-H, --html`               HTML table output mode
- `-P, --pset=VAR[=ARG]`     set printing option VAR to ARG (see `\pset` command)
- `-R, --record-separator=STRING`
                              record separator for unaligned output (default: newline)
- `-t, --tuples-only`        print rows only
- `-T, --table-attr=TEXT`    set HTML table tag attributes (e.g., width, border)
- `-x, --expanded`           turn on expanded table output
- `-z, --field-separator-zero`
                              set field separator for unaligned output to zero byte
- `-0, --record-separator-zero`
                              set record separator for unaligned output to zero byte

## Connection options:
- `-h, --host=HOSTNAME`      database server host or socket directory
- `-p, --port=PORT`          database server port
- `-U, --username=USERNAME`  database user name
- `-w, --no-password`        never prompt for password
- `-W, --password`           force password prompt (should happen automatically)

For more information, type `\?` (for internal commands) or `\help` (for SQL commands) from within `psql`, or consult the psql section in the PostgreSQL documentation.

Report bugs to `<pgsql-bugs@lists.postgresql.org>`.  
PostgreSQL home page: <https://www.postgresql.org/>


To connect to databases in PostgreSQL, you can use the `psql` command-line interface. Here are the steps and options for connecting:

### Connecting via psql

1. **Open your terminal**.

2. **Use the following command** to connect to a database:

   ```bash
   psql -h HOSTNAME -p PORT -U USERNAME -d DBNAME
   ```

   - `HOSTNAME`: The address of the database server (use `localhost` if it’s on your local machine).
   - `PORT`: The port number (default is `5432`).
   - `USERNAME`: Your PostgreSQL username.
   - `DBNAME`: The name of the database you want to connect to.

   **Example**:
   ```bash
   psql -h localhost -p 5432 -U postgres -d mydatabase
   ```

3. **Enter your password** when prompted.

### Connecting Without Explicit Options

If you are connecting to a database on your local machine with the default port and your username matches your system username, you can simplify the command:

```bash
psql DBNAME
```

### Connection Options

- **Database Name**: If you don't specify a database name, `psql` will connect to a database with the same name as your username.
  
- **Environment Variables**: You can set the following environment variables to avoid specifying them every time:
  - `PGHOST`: Hostname
  - `PGPORT`: Port
  - `PGUSER`: Username
  - `PGPASSWORD`: Password

### Example of Connecting

1. To connect to the `testdb` database with the username `admin`:
   ```bash
   psql -U admin -d testdb
   ```

2. If you're already logged in to the `psql` terminal, you can connect to another database using the `\c` command:
   ```sql
   \c new_database_name
   ```