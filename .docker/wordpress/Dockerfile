FROM wordpress:5.3.2-php7.2-apache

# Install WP-CLI
RUN apt update && apt install -y gnupg2 less \
    && curl -sSL https://packages.blackfire.io/gpg.key | apt-key add - \
    && echo "deb http://packages.blackfire.io/debian any main" | tee /etc/apt/sources.list.d/blackfire.list \
    && apt update && apt install -y blackfire-agent blackfire-php \
    && curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
    && chmod +x wp-cli.phar \
    && mv wp-cli.phar /usr/local/bin/wp
    

# Fix permissions
RUN usermod -u 1000 www-data && chown -R www-data:www-data /var/www/html
