FROM postgres:10

RUN apt-get update \
    && apt-get install -y postgresql-contrib-10 postgresql-10-postgis-2.4 \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean
