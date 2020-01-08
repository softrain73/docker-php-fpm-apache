ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine
RUN apk update; \
    apk upgrade \
    && apk add --no-cache libzip-dev libzip libpng libpng-dev;

RUN docker-php-ext-configure zip \
    && docker-php-ext-install mysqli opcache pdo_mysql zip gd

RUN apk del libpng-dev libzip-dev

