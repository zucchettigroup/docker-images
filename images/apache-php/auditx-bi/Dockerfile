FROM php:7.2-apache

# Required to build on linux non interactive system.
ENV DEBIAN_FRONTEND=noninteractive
# Use the default production configuration
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
# Enable extensions for CakePHP & Auditx APP (System Dependencies)
RUN apt-get -y update && apt-get install -y libicu-dev libzip-dev zip libpng-dev
# Configure Extensions.
RUN docker-php-ext-configure intl && docker-php-ext-install intl; \ 
	docker-php-ext-configure pdo_mysql && docker-php-ext-install pdo_mysql; \
	docker-php-ext-configure zip --with-libzip && docker-php-ext-install zip; \ 
	docker-php-ext-configure gd && docker-php-ext-install gd
# Wkhtmltopdf
RUN apt-get install -y wget; \ 
	wget --no-check-certificate https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb -P /usr/local/bin; \
	apt-get install -y build-essential fontconfig libfontconfig libjpeg62-turbo libpng16-16 libxrender1 xfonts-75dpi xorg xvfb; \
	dpkg -i /usr/local/bin/wkhtmltox_0.12.5-1.buster_amd64.deb && rm /usr/local/bin/wkhtmltox_0.12.5-1.buster_amd64.deb