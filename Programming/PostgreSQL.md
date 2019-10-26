# PostgreSQL

## Commands

-   `psql -d database -U user -W` -
-   `psql -h localhost -p 5432 -U postgres -W` -
-   `\l` - List all databases (can be used with +)
-   `\dn` - List all schemas
-   `\df` - List all stored procedures and functions
-   `\dv` - List all views
-   `\dt` - List all tables in current database
-   `\dt+` - List detailed information on tables
-   `\d+ table_name` - Get detailed information on table
-   `\du` - List all users
-   `CREATE ROLE role_name;` -
-   `SET ROLE new_role;` - Change the role for the current session
-   `CREATE DATABASE db_name;` - Create database if not exist
-   `DROP DATABASE db_name;` - Delete database if exist

```sql
CREATE [TEMP] TABLE [IF NOT EXISTS] table_name(
   pk SERIAL PRIMARY KEY,
   c1 type(size) NOT NULL,
   c2 type(size) NULL,
   ...
);
```
