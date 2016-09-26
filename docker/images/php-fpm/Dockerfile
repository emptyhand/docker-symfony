FROM php:5.6.25-fpm

RUN docker-php-ext-install pdo pdo_mysql

RUN curl -L -o /tmp/redis.tar.gz https://github.com/phpredis/phpredis/archive/2.2.8.tar.gz \
    && tar xfz /tmp/redis.tar.gz \
    && rm -r /tmp/redis.tar.gz \
    && mkdir -p /usr/src/php/ext \
    && mv phpredis-2.2.8 /usr/src/php/ext/redis \
    && docker-php-ext-install redis