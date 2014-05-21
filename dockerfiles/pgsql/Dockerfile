FROM debian:wheezy
MAINTAINER damien.duportal@gmail.com

RUN apt-get update && apt-get install -y nano wget dialog net-tools procps inetutils-telnet vim curl
RUN mkdir /app

RUN apt-get install -y postgresql-9.1

RUN mkdir -p /app/conf /app/data

ADD postgresql.conf /app/conf/
ADD pg_hba.conf /app/conf/

RUN chown -R postgres:postgres /app

USER postgres

RUN  /usr/lib/postgresql/9.1/bin/initdb -D /app/data/

EXPOSE 5432
CMD ["/usr/lib/postgresql/9.1/bin/postgres","--config-file=/app/conf/postgresql.conf"]
