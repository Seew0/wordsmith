FROM postgres:15.1-alpine

ENV POSTGRES_HOST_AUTH_METHOD=trust

COPY words.sql /docker-entrypoint-initdb.d/ 