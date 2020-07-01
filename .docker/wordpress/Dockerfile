FROM wordpress:5.3.2-php7.2-apache

# Fix permissions
RUN usermod -u 1000 www-data && chown -R www-data:www-data /var/www/html
