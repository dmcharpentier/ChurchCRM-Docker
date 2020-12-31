FROM mydarkfire/alpine-apache-php7
MAINTAINER ChurchCRM

RUN apk update
RUN apk upgrade

RUN rm -rf /var/cache/apk/*

RUN mkdir /web/churchcrm

COPY ./build-files/httpd.conf /etc/apache2
COPY ./build-files/60-churchcrm /etc/run_always

RUN chmod +x /etc/run_always/60-churchcrm

# Enable Terminal
ENV TERM xterm
