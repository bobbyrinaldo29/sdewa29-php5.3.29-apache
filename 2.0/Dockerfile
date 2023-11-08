FROM sdewa29/php5.3.29-apache:1.0

RUN apk update && apk add autoconf g++ make

# install xdebug
RUN pecl install xdebug-2.2.7
RUN docker-php-ext-enable xdebug
RUN echo "error_reporting=E_ALL" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "display_startup_errors=Off" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "display_errors=Off" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

# relevant to this answer
RUN echo "xdebug.idekey=\"XDEBUG_ECLIPSE\"" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_port=9000" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_enable=1" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_autostart=1" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.remote_host=localhost" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini