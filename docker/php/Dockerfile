FROM php:7.4-fpm

WORKDIR /usr/local/apache2/htdocs

RUN apt update \
	&& apt-get install -y zlib1g-dev libicu-dev g++
	
RUN	docker-php-ext-configure intl
RUN	docker-php-ext-install intl pdo pdo_mysql

RUN apt-get update \
    && apt-get -y install git

RUN git clone https://github.com/Bencute/testtask.git .

COPY /frontend/ /usr/local/apache2/htdocs/frontend/