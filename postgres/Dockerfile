FROM postgres:17.5-alpine3.22

LABEL org.opencontainers.image.source="https://github.com/Sunlit-Garden/containerized"
LABEL org.opencontainers.image.licenses="PostgreSQL"
LABEL org.opencontainers.image.version=17.5
LABEL org.opencontainers.image.description="Using multiple databases with the official PostgreSQL Docker image"

# Copied from https://github.com/mrts/docker-postgresql-multiple-databases
COPY create-multiple-postgresql-databases.sh /docker-entrypoint-initdb.d/
RUN chmod +x /docker-entrypoint-initdb.d/create-multiple-postgresql-databases.sh
