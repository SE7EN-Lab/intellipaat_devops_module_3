FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
ENV APACHE_RUN_USER=www-data
ENV APACHE_RUN_GROUP=www-data
ENV APACHE_LOG_DIR=/var/log/apache2
ENV APACHE_LOCK_DIR=/var/lock/apache2
ENV APACHE_PID_FILE=/var/run/apache2.pid

RUN apt-get update -y && apt-get install -y apache2 apache2-utils libcap2-bin procps curl && chown -R www-data:www-data /var/www/html/ \
    && curl https://raw.githubusercontent.com/hshar94/helloworld/master/index.html -o /var/www/html/index.html

EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]