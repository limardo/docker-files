FROM php:8
RUN apt-get update -qq && \
    apt-get install build-essential libmariadb-dev -y --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get install nodejs -y --no-install-recommends
RUN curl -s http://getcomposer.org/installer | php
RUN echo "export PATH=${PATH}:/var/www/vendor/bin" >> ~/.bashrc
RUN mv composer.phar /usr/local/bin/composer
RUN docker-php-ext-install pdo pdo_mysql
WORKDIR /var/www/app
