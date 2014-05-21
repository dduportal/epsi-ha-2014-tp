FROM debian:wheezy
MAINTAINER damien.duportal@gmail.com

RUN apt-get update && apt-get install -y nano wget dialog net-tools procps inetutils-telnet vim curl
RUN mkdir /app

RUN apt-get install -y nginx-full

RUN rm -v /etc/nginx/nginx.conf
RUN mkdir -p /app/conf /app/docs
#RUN echo "<h1>Hello World</h1>" > /app/docs/index.html

ADD index.html /app/docs/
ADD nginx.conf /app/conf/

EXPOSE 80
CMD nginx -c /app/conf/nginx.conf

