FROM php:7.4-apache
RUN apt update \
        && apt install -y \
            g++ \
            libicu-dev \
            libpq-dev \
            libzip-dev \
            zip \
            zlib1g-dev \
        && docker-php-ext-install \
            intl \
            opcache \
            pdo \
            pdo_mysql

RUN docker-php-ext-install pdo_mysql
RUN a2enmod rewrite
WORKDIR /var/www/MOVIES-SENA
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
