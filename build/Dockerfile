FROM debian:stretch-slim

RUN apt update

RUN apt install -y vim nano less
RUN apt install -y apache2
RUN a2enmod proxy
RUN a2enmod proxy_fcgi
RUN a2enmod proxy_http

RUN a2enmod rewrite
RUN a2enmod proxy
RUN a2enmod setenvif
RUN a2enmod headers
RUN a2enmod expires
RUN a2enmod env
RUN a2enmod deflate
RUN a2enmod dir

WORKDIR /var/www/project


EXPOSE 84
EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]

