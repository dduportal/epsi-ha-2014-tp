FROM debian:jessie
MAINTAINER damien.duportal@gmail.com

RUN apt-get update && apt-get install -y nano wget dialog net-tools
RUN mkdir /app

RUN apt-get install -y postgresql

ADD pg_hba.conf /etc/postgresql/9.3/main/
ADD postgresql.conf /etc/postgresql/9.3/main/
RUN chown postgres /app
RUN chmod 750 /app

USER postgres
RUN /usr/lib/postgresql/9.3/bin/initdb -D /app

EXPOSE 5432

CMD /usr/lib/postgresql/9.3/bin/postgres -D /app

