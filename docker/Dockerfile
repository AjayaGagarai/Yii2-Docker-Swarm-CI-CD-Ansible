FROM php:8.1-apache

RUN apt-get update && apt-get install -y \\
    git unzip libzip-dev libpng-dev libonig-dev \\
    && docker-php-ext-install zip pdo_mysql gd mbstring

COPY src /var/www/html

RUN chown -R www-data:www-data /var/www/html

WORKDIR /var/www/html

EXPOSE 80
