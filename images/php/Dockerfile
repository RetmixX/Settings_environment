FROM php:8.1.12-fpm-alpine

COPY ./Images/php/php.ini /usr/local/etc/php/conf.d/php.ini

RUN curl -sSLf \
            -o /usr/local/bin/install-php-extensions \
            https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions
RUN chmod +x /usr/local/bin/install-php-extensions
RUN install-php-extensions \
            pdo \
            pdo_pgsql \
            xdebug

# Clear cache
RUN rm -rf /var/cache/apk/*

COPY ./src /var/www/html

WORKDIR /var/www/html



CMD ["php-fpm"]