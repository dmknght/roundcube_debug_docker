FROM roundcube/roundcubemail:latest

# Setup Xdebug (from my test, image has pre-installed packages
RUN docker-php-ext-install pdo pdo_mysql \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

# COpy xdebug to correct position inside docker
COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

WORKDIR /var/www/html
