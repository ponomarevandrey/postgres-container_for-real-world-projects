# Postgres Container

Username/password and db name are set in `.env` file. Pass the file (through `docker-compose`) to your app server's container to provide the app with authentication details for db. 


# Environment variables

To use the container, create the `.env` (1) file at the root of the project dir and set the following variables (2):

1. `touch .env`
2. ```
   POSTGRES_USER=yourname
   POSTGRES_PASSWORD=1234

   # Host is the name of your database container in docker-compose.yml
   POSTGRES_HOST=postgres

   POSTGRES_DATABASE=yourname

   # Port should match the one mentioned in docker-compose.yml
   POSTGRES_PORT=5432

   ADMIN_EMAIL=your@email.ru
   ```
   
# Log into psql in container

`psql -h localhost -p 5432 -U username -d db_name --password`
