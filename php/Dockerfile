ARG PHP_VER
ARG REGION
ARG COUNTRY
FROM php:${PHP_VER}-fpm-alpine
ARG PHP_INI_DIR=/usr/local/etc/php/
RUN apk update && apk upgrade;
RUN apk add \
    libmcrypt-dev \
    -U tzdata;
RUN cp /usr/share/zoneinfo/${REGION}/${COUNTRY} /etc/localtime && echo "${REGION}/${COUNTRY}" > /etc/timezone
RUN docker-php-ext-install mysqli pdo pdo_mysql;
# Copy the custom php.ini to the php container
COPY ./conf/php-ini-overrides.ini $PHP_INI_DIR/conf.d/
