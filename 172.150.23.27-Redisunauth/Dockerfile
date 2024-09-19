FROM --platform=amd64 centos:7
COPY rpm /rpm
RUN cd /rpm && rpm -ivh *.rpm
COPY redis-* /usr/local/bin/
COPY redis.conf /etc/
COPY start.sh /start.sh
RUN chmod -v +x /start.sh
RUN echo 'flag_7_redisunauth{ceb0b893263523a7d1591f0006f333d1}' > /flag
EXPOSE 6379
CMD ["/start.sh"]