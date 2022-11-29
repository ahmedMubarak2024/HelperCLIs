# Helping Codes

to start PostgreSQL Docker server
docker run --name [docker containr name] -e POSTGRES_USER=[username] -e POSTGRES_PASSWORD=[password] -p 5432:5432 -d postgres
replace all [] and what is in them

to get the network for your database
docker inspect postgresqlNode --format="{{json .NetworkSettings.Networks}}"

to start PgAdmin4 
docker run -p 80:80 \
    -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' \
    -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' \
    -e 'PGADMIN_CONFIG_ENHANCED_COOKIE_PROTECTION=True' \
    -e 'PGADMIN_CONFIG_LOGIN_BANNER="Authorised users only!"' \
    -e 'PGADMIN_CONFIG_CONSOLE_LOG_LEVEL=10' \
    -d dpage/pgadmin4
