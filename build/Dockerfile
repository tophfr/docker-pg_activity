FROM python:3.11-alpine

MAINTAINER toph <toph@toph.fr>

RUN apk add --no-cache postgresql-libs

ARG PG_ACTIVITY_VERSION=3.0.1
ENV PG_ACTIVITY_VERSION $PG_ACTIVITY_VERSION

RUN apk add --no-cache --virtual .build-deps \
        gcc \
        linux-headers \
        postgresql-dev\
        musl-dev \
    && pip3 install psycopg2-binary \
    && pip3 install pg_activity==$PG_ACTIVITY_VERSION \
    && apk del .build-deps

ENTRYPOINT ["pg_activity"]
