FROM php:7.0.33-apache
RUN apt-get update && apt-get install -y

RUN docker-php-ext-install pdo pdo_mysql
#RUN docker-php-ext-install intl
#RUN docker-php-ext-install mbstring
#RUN docker-php-ext-install bcmath
#RUN docker-php-ext-install mcrypt
#RUN docker-php-ext-install zip
#RUN docker-php-ext-install exif
#RUN docker-php-ext-install soap
#RUN docker-php-ext-install opcache
#RUN docker-php-ext-install iconv
#RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
#RUN docker-php-ext-install gd