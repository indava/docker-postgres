# docker-postgres
latest postgreSQL + postGIS 

# docker-compose.yml

version: '3.8'

services:
  psql:
    build: build/psql
    restart: always
    shm_size: 32M
    environment:
      - POSTGRES_DB=
      - POSTGRES_USER=
      - POSTGRES_PASSWORD=
