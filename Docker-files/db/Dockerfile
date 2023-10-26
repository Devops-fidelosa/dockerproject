FROM mysql:8.0.33
LABEL "Project"="fidevcontainerization"
LABEL "Author"="Fidelosa"

ENV MYSQL_ROOT_PASSWORD="fidevpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
EXPOSE 3306
