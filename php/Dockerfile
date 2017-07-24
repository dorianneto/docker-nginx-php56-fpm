FROM php:5.6-fpm

MAINTAINER Dorian Neto <doriansampaioneto@gmail.com>

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
        libcurl3-dev \
        libtidy-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt mysqli pdo pdo_mysql mbstring curl tidy \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd