ARG COMPOSER_VERSION=2.6.5

FROM composer:${COMPOSER_VERSION} as composer_stage

FROM debian:bookworm

# Install Composer
COPY --from=composer_stage /usr/bin/composer /usr/bin/composer

# Install zip
RUN apt-get update && apt-get install -y zip unzip

# Install PHP
RUN apt-get update && apt-get install -y php php-cli php-fpm php-json php-pdo php-mysql php-zip php-gd php-mbstring php-curl php-xml php-pear php-bcmath

WORKDIR /app

COPY php.ini /etc/php/8.1/cli/conf.d/99-custom.ini

CMD ["composer"]