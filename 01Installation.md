Here's a concise summary of the steps to download and install PostgreSQL on Windows:

### Downloading and Installing PostgreSQL on Windows

1. **Open Google**:
   - Search for "Postgres download."

2. **Select the Correct Link**:
   - Click on the first link to the PostgreSQL download page.

3. **Choose Operating System**:
   - Select **Windows** for the operating system.

4. **Download the Installer**:
   - Click on **Download the Installer**.
   - Choose the latest version (e.g., 11.2 or above) and select the **64-bit** version.

5. **Run the Installer**:
   - Save the installer and double-click to open it.

6. **Installation Steps**:
   - Click **Next** on the welcome screen.
   - Leave the installation folder as default.
   - Select the following components:
     - SQL Server
     - PG Admin (GUI client)
     - Stack Builder (optional drivers)
     - Command-line tools
   - Click **Next** after making selections.

7. **Set Superuser Password**:
   - Enter a password for the superuser (remember this for later).

8. **Default Port**:
   - Leave the default port as **5432** and click **Next**.

9. **Finish Installation**:
   - Click through until the installation completes.
   - Uncheck any additional options (like Stack Builder) if not needed.
   - Click **Finish**.

10. **Create Desktop Shortcuts**:
    - Search for PostgreSQL in the Windows menu and create shortcuts for:
      - PSQL (command line)
      - PG Admin (GUI client)
    - Drag them to the desktop for easy access.

Here’s a summary of the key points for getting started with PostgreSQL:

### Setting Up PostgreSQL on Windows

1. **Install PostgreSQL**: Ensure PostgreSQL is installed on your Windows machine.

2. **Launch PSQL (Interactive Shell)**:
   - Click on the PSQL shortcut to open the command line interface.

3. **Connect to Database**:
   - **Server**: Enter `localhost` to connect to the local server.
   - **Database**: By default, use the database named `Postgres`.
   - **Port**: Default is `5432`.
   - **Username**: Default is `Postgres`.
   - **Password**: Enter the password you set during installation.

4. **Error Handling**:
   - If you attempt to connect to a non-existent database (e.g., `test`), you will receive an error indicating that the database does not exist.

5. **Using PG Admin (Graphical Interface)**:
   - Open PG Admin and connect by entering the same password.
   - You can view your databases and their contents.

### Course Focus
- The course will primarily utilize PSQL (the shell) rather than PG Admin (the GUI).
- Commands will be consistent across different operating systems (Windows and Mac).