FROM php:8.1-fpm

RUN apt-get update -y
RUN docker-php-ext-install pdo pdo_mysql

WORKDIR /var/www
COPY . .

COPY --from=composer:2.1.14 /usr/bin/composer /usr/bin/composer

ENV PORT=8000

CMD /var/www/docker/php/docker-entrypoint.sh
