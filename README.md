# Docker - Postgres

Start postgres docker image:

```bash
docker compose up
```

Connect to running psql docker image

```bash
docker exec -it pg_container bash
```

Connect to psql server

```bash
psql --host=pg_container --dbname=test_db --username=root
```

Load data from file

```bash
psql -h pg_container -d test_db -U root -f docker-entrypoint-initdb.d/docker_postgres_init.sql

# or
cd docker-entrypoint-initdb.d
psql -h pg_container -d test_db -U root -f docker_postgres_init.sql
```
