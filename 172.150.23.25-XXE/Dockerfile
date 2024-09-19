FROM --platform=amd64 vulhub/php:5.5-apache

COPY --chown=www-data:www-data attachs /var/www/html/attachs/

COPY --chown=www-data:www-data index.php /var/www/html/

COPY --chown=www-data:www-data doLogin.php /var/www/html/

RUN echo 'flag_5_xxe{93dfcaf3d923ec47edb8580667473987}' > /flag