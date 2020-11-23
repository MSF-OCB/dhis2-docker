FROM postgres:13

RUN apt-get update \
    && apt-get install -y postgresql-contrib-13 postgis \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean
