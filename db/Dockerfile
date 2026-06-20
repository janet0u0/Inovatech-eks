FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD=admin123
COPY init.sql /docker-entrypoint-initdb.d/init.sql
EXPOSE 3306