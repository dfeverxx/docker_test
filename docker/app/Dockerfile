  
FROM php:fpm-alpine
#RUN docker-php-ext-install pdo pdo_mysql
# Install Composer
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
#RUN apk --update add wget \ 
#		     curl \
#		     git \
#		     php7 \
#		     php7-curl \
#		     php7-openssl \
#		     php7-iconv \
#		     php7-json \
#		     php7-mbstring \
#		     php7-phar \
#		     php7-dom --repository http://nl.alpinelinux.org/alpine/edge/testing/ && rm /var/cache/apk/*

#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer 

#RUN mkdir -p /var/www

#WORKDIR /var/www

#COPY . /var/www

#VOLUME /var/www

#CMD ["/bin/sh"]

#ENTRYPOINT ["/bin/sh", "-c"]
RUN apt-get update && apt-get install -y libmcrypt-dev \
    mysql-client libmagickwand-dev --no-install-recommends \
    && pecl install imagick \
    && docker-php-ext-enable imagick \
    && docker-php-ext-install mcrypt pdo_mysql
