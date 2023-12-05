FROM mysql:5.7

RUN chown -R mysql:root /var/lib/mysql/

ARG MYSQL_DATABASE=
ARG MYSQL_ROOT_PASSWORD=senha123

ADD data.sql /etc/mysql/data.sql

RUN sed -i 's/MYSQL_DATABASE/'$MYSQL_DATABASE'/g' /etc/mysql/data.sql
RUN cp /etc/mysql/data.sql /docker-entrypoint-initdb.d

EXPOSE 3306