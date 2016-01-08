# Composer Docker Container
FROM php:5.6-cli
MAINTAINER Rob Loach <robloach@gmail.com>

RUN apt-get update && apt-get install -y libzip-dev \
    && docker-php-ext-install zip
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
WORKDIR /var/www/app
RUN chmod -R 755 .*
