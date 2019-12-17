FROM php:7.4-fpm-alpine

MAINTAINER duonganhtuan

COPY ./php.ini /usr/local/etc/php/

RUN apk --update add mariadb-client libzip-dev unzip\
  && docker-php-ext-install pdo_mysql mysqli zip

#Composer install (latest version)
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
      && php -r "if (hash_file('SHA384', 'composer-setup.php') === trim(file_get_contents('https://composer.github.io/installer.sig'))) { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" \
      && php composer-setup.php\
      && php -r "unlink('composer-setup.php');" \
      && mv composer.phar /usr/sbin/composer

ENV COMPOSER_ALLOW_SUPERUSER 1

ENV COMPOSER_HOME /composer

ENV PATH $PATH:/composer/vendor/bin

WORKDIR /var/www/html

RUN composer global require "laravel/installer"