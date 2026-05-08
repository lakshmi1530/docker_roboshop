FROM redis:7

RUN sed -i \
    -e 's/bind 127.0.0.1 -::1/bind 0.0.0.0/g' \
    -e 's/protected-mode yes/protected-mode no/g' \
    /usr/local/etc/redis/redis.conf

EXPOSE 6379

CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]