FROM php:7.1.8-fpm

RUN apt-get update \
	&& apt-get install libcurl3-dev \
	&& yes | apt-get install libxml2-dev

RUN docker-php-ext-install curl \
    && docker-php-ext-install pdo pdo_mysql \
    && pecl install xdebug-2.5.5 \
	&& pecl install redis-3.1.3 \
	&& pecl install solr-2.4.0 \	
    && docker-php-ext-enable redis xdebug curl solr

RUN mkdir -p /usr/local/bin \
    && curl -LsS https://symfony.com/installer -o /usr/local/bin/symfony \
    && chmod a+x /usr/local/bin/symfony

WORKDIR /application
