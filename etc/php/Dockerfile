FROM php:7.3-apache
RUN apt-get update > /dev/null && apt-get install -y --no-install-recommends \
    git \
    libzip-dev \
    libicu-dev \
    unzip \
    wget \
    nano > /dev/null

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install intl

COPY ./php.ini /usr/local/etc/phpphp.ini

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer > /dev/null

# Add symfony CLI
RUN wget https://get.symfony.com/cli/installer -O - | bash
RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony

RUN symfony check:requirements

WORKDIR /var/www/html