FROM ubuntu:trusty
RUN apt-get update && \
apt-get install -y apache2 && \
apt-get install -y ntp && \
apt-get install -y default-jdk && \
apt-get clean

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

RUN mkdir web && \
mkdir web/etc && \
mkdir web/www;

EXPOSE 8081
WORKDIR /var/www/site
ENTRYPOINT ["apachectl", "-D", "FOREGROUND"]


