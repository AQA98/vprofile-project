FROM mysql:8.0.33
LABEL "Project"="Vprofile"
LABEL "Author"="Imran"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

#according to the documentation we have to put the .sql file in the following location when initiallizing a fresh instance
ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql

#We also dont need to explicitly put port no as its already in the image as per docs