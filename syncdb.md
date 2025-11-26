---
allowed-tools: Bash
description: Update DB from QA to local
---
## Context
Pull db from QA and then follow the steps, using the aws-cli, docker-cli

## Your task
- cd /Users/counterpart/Documents/counterpart 
- pipenv shell
- make runsupport
- ask if the db is already downloaded.
- export POSTGRES_CONTAINER_ID=$(docker ps -aqf "name=counterpart-postgres")
- docker exec -it $POSTGRES_CONTAINER_ID psql -U postgres
- drop database if exists counterpart; drop database if exists qa;
- \q
- docker exec -i $POSTGRES_CONTAINER_ID psql -U postgres -c "CREATE DATABASE qa"
- docker exec -i $POSTGRES_CONTAINER_ID psql -U postgres < ~/Desktop/output.sql
- docker exec -i $POSTGRES_CONTAINER_ID psql -U postgres -c "ALTER DATABASE qa RENAME TO counterpart"
- python manage.py shell_plus
- user = User.objects.create_user(email='admin1@yourcounterpart.com' password='123456', is_staff=True,is_superuser=True, is_active=True);