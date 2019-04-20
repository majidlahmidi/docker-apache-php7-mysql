FROM php:7.2-apache

RUN curl -OL https://github.com/composer/composer/releases/download/1.7.2/composer.phar && \
mv composer.phar /usr/local/bin/composer && \
chmod +x /usr/local/bin/composer

RUN apt-get update && \
apt-get -y install git \
zlib1g-dev \
libzip-dev

RUN a2enmod rewrite

RUN docker-php-ext-install zip

#CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]