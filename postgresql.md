# PostgreSQL cheat sheet

## Install / Config (linux)

```
sudo apt install postgresql postgresql-contrib

sudo -u postgres psql template1
# ALTER USER postgres with encrypted password 'your_password';

psql -U postgres -h localhost
-> asked for password and it worked
```

## Installing pgvector

Add postgresql apt repository
```
sudo apt install -y postgresql-common
sudo /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh
```

Install:
```
sudo apt install postgresql-14-pgvector
```

## Allow local user to login without password (trust authentication)

add this line to pg_hba.conf:
```
# TYPE  DATABASE        USER            ADDRESS                 METHOD
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

Dump heroku db:

```pg_dump -Fc --no-acl --no-owner --exclude-table=public.table_to_exclude heroku_database_url > my_dump.dmp```

Restore Local db from dump:

```pg_restore -h localhost -d database_name -C --no-owner filename.bkp```

## Meta Commands

`\d` - List Databases

`\dn` - List Schemas

`\dt` - Describe table

`\dt myschema.*` - List Tables in schema

## Admin commands

Rename database

```postgres=# alter database current_db_name rename to new_db_name;```
