# PostgreSQL cheat sheet

## Backup / Restore

Dump Local db:

```pg_dump -h localhost -d database_name -f filename.bkp -Fc```

Restore Local db from dump:

```pg_restore -h localhost -d database_name -C --no-owner filename.bkp```

## Meta Commands

`\d` - List Databases

`\dn` - List Schemas

## Admin commands

Rename database

```postgres=# alter database current_db_name rename to new_db_name;```
