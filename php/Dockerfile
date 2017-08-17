FROM php:7.1.8-fpm

RUN apt-get update \
	&& apt-get install libcurl3-dev \
	&& apt-get install libxml2-dev

RUN docker-php-ext-install curl \
    && docker-php-ext-install pdo pdo_mysql \
    && pecl install xdebug-2.5.5 \
	&& pecl install redis-3.1.3 \
	&& pecl install solr-2.4.0 \	
    && docker-php-ext-enable redis xdebug curl solr 
	
COPY ./workspace /usr/src/myapp
WORKDIR /usr/src/myapp
