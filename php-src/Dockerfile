FROM php:7.1-fpm
RUN apt-get update && \
    apt-get install -y \
    curl \
    git \
    zip \
    unzip \
    vim

# install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && php composer-setup.php --install-dir=/usr/local/bin --filename=composer && php -r "unlink('composer-setup.php');"

#install nodejs
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash - && apt-get install -y nodejs

WORKDIR /var/www/html

