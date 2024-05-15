ARG PHP_VER

FROM docker.io/wodby/php:${PHP_VER}

ENV LC_ALL nl_NL.UTF-8
ENV LANG nl_NL.UTF-8
ENV PHP_INI_DIR=/usr/local/etc/php 

RUN sudo -E apk update && sudo -E apk add alpine-sdk autoconf gettext gettext-libs libintl icu icu-dev icu-data-full musl musl-libintl musl-locales musl-locales-lang

RUN sudo -E docker-php-ext-install -j32 intl pcntl gettext
