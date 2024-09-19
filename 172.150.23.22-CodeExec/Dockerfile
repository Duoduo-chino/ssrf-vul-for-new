FROM --platform=amd64 vulhub/php:5.5-apache

COPY --chown=www-data:www-data flag /

COPY --chown=www-data:www-data index.php /var/www/html/

COPY --chown=www-data:www-data phpinfo.php /var/www/html/

COPY --chown=www-data:www-data shell.php /var/www/html/