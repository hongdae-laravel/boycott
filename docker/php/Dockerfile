FROM php:7.1-apache

RUN apt-get update
RUN apt-get install libxml2-dev
RUN docker-php-ext-install pdo_mysql xml

COPY boycott.dev.conf /etc/apache2/sites-available/boycott.dev.conf

RUN a2ensite boycott.dev
RUN a2enmod rewrite

RUN mkdir /codes; mkdir /codes/boycott

WORKDIR /codes/boycott