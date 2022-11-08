FROM php:8.1-alpine

RUN apk add curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN rm -rf /var/cache/apk/*

ENTRYPOINT ["php", "-S", "0.0.0.0:7000", "-t", "/var/www/html"]