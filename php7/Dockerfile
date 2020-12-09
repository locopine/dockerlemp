FROM php:7.4.12-fpm

MAINTAINER zhoukan "zkshpro@163.com"

ENV LANG C.UTF-8

RUN apt-get update \
	&& apt-get install vim -qqy \
	&& apt-get install git -qqy \
	&& apt-get install zip -qqy \
	&& apt-get install unzip -qqy \
	&& apt-get install procps -qqy \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install pdo_mysql \
    && pecl install redis && docker-php-ext-enable redis \
    && pecl install mongodb && docker-php-ext-enable mongodb \
    && pecl install xdebug && docker-php-ext-enable xdebug

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN echo "alias ll='ls -lh --color=auto'" >> ~/.bashrc

