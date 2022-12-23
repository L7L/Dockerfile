FROM mysql:8.0.31-oracle
LABEL "project" = "Interior"
LABEL " Author" = "ckc"
ENV Mysql_ROOT_PASSWORD="zaup120"
ENV MYSQL_DATABASE="accounts"


ADD db.backup.sql /docker-entrypoint-initdb.d/db.backup.sql