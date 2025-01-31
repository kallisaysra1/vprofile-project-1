FROM mysql:8.0.33
#the above versions informations anything should be gathered from the developers 
LABEL "project"="Vprofile"
LABEL "Author"="Kalyan"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
# We are tryihg to ADD the db_backup.sql in this location "docker-entrypoint-initdb.d/db_backup.sql", any .sql or .sh file is copied in that said location then it will be considered as executable, it is clearly mentioned in the documentation
#the sql file contains the sql queries that will get executed and which will create a schema.

