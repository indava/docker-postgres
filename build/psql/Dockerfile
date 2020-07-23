FROM postgres:12

RUN apt-get update && apt-get install -y apt-utils make gcc postgresql-server-dev-12 postgis postgresql-12-postgis-3
COPY pg_hashids /tmp/pg_hashids
COPY permuteseq /tmp/permuteseq
RUN cd /tmp/pg_hashids/ && make; make install
RUN cd /tmp/permuteseq/ && make; make install
RUN rm -rf /tmp/pg_hashids
RUN rm -rf /tmp/permuteseq
