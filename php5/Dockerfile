FROM php:5.6.40-fpm

MAINTAINER zhoukan "zkshpro@163.com"

ENV LANG C.UTF-8

RUN apt-get update \
	&& apt-get install vim -qqy \
	&& apt-get install git -qqy \
	&& apt-get install zip -qqy \
	&& apt-get install unzip -qqy \
	&& apt-get install procps -qqy \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install pdo_mysql

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN echo "alias ll='ls -lh --color=auto'" >> ~/.bashrc
