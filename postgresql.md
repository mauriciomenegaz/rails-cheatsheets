# PostgreSQL cheat sheet

## Install / Config (linux)

```
sudo apt install postgresql postgresql-contrib

sudo -u postgres psql template1
# ALTER USER postgres with encrypted password 'your_password';

psql -U postgres -h localhost
-> asked for password and it worked
```

## Allow local user to login without password (trust authentication)

add this line to pg_hba.conf:
```
local   all             mauricio        127.0.0.1/32            trust
```

create role:
```
sudo -u postgres psql
# CREATE ROLE MAURICIO
# ALTER ROLE mauricio WITH LOGIN;
# alter user mauricio with SUPERUSER;
```

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
