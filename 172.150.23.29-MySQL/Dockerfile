FROM --platform=amd64 medicean/vulapps:base_lamp

COPY flag.sql /tmp/flag.sql

COPY flag /flag

RUN sed -i '110i\secure_file_priv=' /etc/mysql/my.cnf

RUN sed -i '47s/.*/bind-address = 0.0.0.0/' /etc/mysql/my.cnf

RUN sed -i '5i\chown -R  mysql:mysql /usr/lib/mysql/plugin' /start.sh 

RUN sed -i '6i\mysql -u root -proot -e "source /tmp/flag.sql"' /start.sh




