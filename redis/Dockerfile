ARG REDIS_VERSION=7.4

FROM redis:${REDIS_VERSION}-alpine

ARG REDIS_PASSWORD
ADD redis.conf /usr/local/etc/redis/redis.conf
RUN echo "requirepass $REDIS_PASSWORD" >> /usr/local/etc/redis/redis.conf

EXPOSE 6379

CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]