FROM ubuntu:20.04

RUN apt update && apt install -y curl wget git zip unzip \
    nginx php php-cli php-fpm php-mysql php-xml php-mbstring \
    mariadb-server composer nodejs npm

WORKDIR /var/www/html

COPY . .

RUN composer install && npm install && npm run build
