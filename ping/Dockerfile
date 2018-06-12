FROM ubuntu:xenial
LABEL maintainer "Andrew Delianides <drew@delianides.com>"

RUN apt-get update && apt-get install -y iputils-ping

ENTRYPOINT ["ping"]
