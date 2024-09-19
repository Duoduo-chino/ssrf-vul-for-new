FROM --platform=amd64 vulhub/php:7.1-apache

COPY --chown=www-data:www-data attachs /var/www/html/attachs/

COPY --chown=www-data:www-data flag /

COPY --chown=www-data:www-data index.php /var/www/html/

COPY --chown=www-data:www-data phpinfo.php /var/www/html/