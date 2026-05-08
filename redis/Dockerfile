FROM redis:7
RUN sed -i -e 's/127.0.0.1/0.0.0.0/g' -e '/protected-mode/ c protected-mode no' /etc/redis/redis.conf
EXPOSE 6379
CMD ["redis-server", "/etc/redis/redis.conf"]