FROM postgres:9.3

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends \
        postgresql-9.3-postgis-2.2 \
        postgresql-9.3-postgis-2.2-scripts \
        && rm -rf /var/lib/apt/lists/*

COPY create_extension_postgis.sh /docker-entrypoint-initdb.d/
