FROM php:7.1-fpm

MAINTAINER Rémi Barbe (aka Remiii) <repository@remibarbe.fr>

RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install -y \
        libicu-dev \
        zlib1g-dev \
        libxml2-dev

RUN apt-get install -y php5-mysql php5-apcu

RUN docker-php-ext-install \
        intl \
        mbstring \
        mysqli \
        zip \
        pdo \
        pdo_mysql \
        soap

RUN php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer \
    && chmod +x /usr/local/bin/composer

RUN apt-get install -y git-core vim

RUN apt-get install -y \
    nodejs \
    npm

RUN apt-get clean

RUN ln -s /usr/bin/nodejs /usr/bin/node

RUN echo 'alias sf-arnaud-molina="php app/console"' >> ~/.bashrc
