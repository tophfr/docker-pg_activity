FROM python:3.8-alpine

MAINTAINER toph <toph@toph.fr>

ARG PG_ACTIVITY_VERSION=1.5.0
ENV PG_ACTIVITY_VERSION $PG_ACTIVITY_VERSION

RUN apk add --no-cache postgresql-libs
RUN apk add --no-cache --virtual .build-deps \
        gcc \
        linux-headers \
        postgresql-dev\
        musl-dev \
    && pip3 install pg_activity==$PG_ACTIVITY_VERSION \
    && apk del .build-deps

ENTRYPOINT ["pg_activity"]
