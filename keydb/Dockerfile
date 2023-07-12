FROM docker.io/eqalpha/keydb:alpine_x86_64_v6.3.3
RUN apk add --no-cache su-exec tini
VOLUME /data
WORKDIR /data
ENTRYPOINT ["tini", "--", "docker-entrypoint.sh"]
EXPOSE 6379
CMD ["keydb-server", "/etc/keydb/keydb.conf"]
