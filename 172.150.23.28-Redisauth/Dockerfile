FROM --platform=amd64 centos:7
COPY rpm /rpm
RUN cd /rpm && rpm -ivh *.rpm
COPY redis-* /usr/local/bin/
COPY redis.conf /etc/
COPY start.sh /start.sh
COPY www/* /var/www/html
RUN chmod -v +x /start.sh
RUN echo 'flag_8_redisauth{ab8b2226055196dae5533b893bba848c}' > /flag
RUN chmod 700 /flag
EXPOSE 80
EXPOSE 6379
CMD ["/start.sh"]
