FROM debian:jessie
MAINTAINER damien.duportal@gmail.com

RUN apt-get update && apt-get install -y nano wget dialog net-tools
RUN mkdir /app

RUN apt-get install -y php5-fpm

ADD php.ini /etc/php5/fpm/
ADD php-fpm.conf /etc/php5/fpm/
ADD www.conf /etc/php5/fpm/ppol.d/

EXPOSE 9000
CMD ["/usr/sbin/php5-fpm"]

