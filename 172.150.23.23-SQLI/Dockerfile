FROM medicean/vulapps:base_lamp


COPY --chown=www-data:www-data attachs /var/www/html/attachs/

COPY --chown=www-data:www-data phpMyAdmin /var/www/html/phpMyAdmin/

COPY db.sql /tmp/db.sql

COPY --chown=www-data:www-data index.php /var/www/html/

RUN rm -rf /var/www/html/index.html

RUN chmod 777 /var/www/html

RUN sed -i '110i\secure_file_priv=' /etc/mysql/my.cnf

RUN sed -i '47s/.*/bind-address = 0.0.0.0/' /etc/mysql/my.cnf

RUN sed -i '5i\mysql -u root -proot -e "source /tmp/db.sql"' /start.sh
