# Docker image for pg_activity, a top like application for PostgreSQL server activity monitoring

Cf. https://github.com/julmon/pg_activity

It is a very small image (~129MB uncompressed) available on [docker hub][dockerhubpage] based on [Alpine Linux][alpinehubpage] and using the last available release from the official PyPI repo of [pg_activity][pg_activity].


# How to use it

    docker run --rm -it tophfr/pg_activity --help
    docker run --rm -it -e PGHOST=mypghost -e PGUSER=mypguser tophfr/pg_activity


  [pg_activity]: https://pypi.org/project/pg_activity/ "pg_activity"
  [dockerhubpage]: https://hub.docker.com/r/tophfr/pg_activity "pg_activity docker hub page"
  [alpinehubpage]: https://hub.docker.com/_/alpine/ "A minimal Docker image based on Alpine Linux with a complete package index and only 5 MB in size!"
