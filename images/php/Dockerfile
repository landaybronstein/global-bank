FROM php:8.1-fpm-alpine

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions gd pdo pdo-mysql mysqli xdebug

RUN install-php-extensions @composer

WORKDIR /var/www/public_html

ENTRYPOINT [ "php-fpm" ]