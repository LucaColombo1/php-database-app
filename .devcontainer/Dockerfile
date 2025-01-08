# Usa un'immagine di base con PHP e Apache
FROM php:8.1-apache

# Installa estensioni PHP necessarie per MySQL
RUN docker-php-ext-install pdo pdo_mysql mysqli

# Abilita moduli Apache
RUN a2enmod rewrite

# Installa Composer per la gestione delle dipendenze PHP
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Copia il codice del progetto nella cartella di lavoro del container
COPY . /var/www/html/

# Espone la porta 80 per Apache
EXPOSE 80
