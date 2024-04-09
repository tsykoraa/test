## Toto je jahodka

Jahodka nie je:
nove riadky pre commit s local PC

## Toto je SQL masticka:

```sql
-- Define the schema variable
SET @target_schema = 'pamstg';

-- Retrieve and display the sizes of all tables in the specified schema in megabytes
SELECT 
    table_schema AS `Database`, 
    table_name AS `Table`, 
    table_rows AS `Number of Rows`,
    ROUND(((data_length + index_length) / 1024 / 1024), 2) AS `Total Size in MB` 
FROM information_schema.TABLES 
WHERE table_schema = @target_schema
ORDER BY (data_length + index_length) DESC;
```
