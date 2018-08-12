FROM ubuntu:16.04

LABEL maintainer="Sheldon Rupp <me@shel.io>"

LABEL \
  org.label-schema.name="millecoin-daemon" \
  org.label-schema.url="https://github.com/NurdTurd/Testing.git" \
  org.label-schema.vcs-url="https://github.com/NurdTurd/Testing.git"

RUN apt-get update && apt-get install -y \
  build-essential \
  python-dev \
  gcc \
  g++ \
  git \
  cmake \
  libboost-all-dev \
  librocksdb-dev \
  libreadline-dev

WORKDIR /app

RUN git clone https://github.com/NurdTurd/Testing.git

RUN chmod +x /app/Testing/external/rocksdb/build_tools/build_detect_platform

RUN chmod +x /app/Testing/external/rocksdb/build_tools/version.sh

WORKDIR /app/Testing

RUN mkdir build

WORKDIR /app/Testing/build

RUN cmake ..

RUN make -j $(nproc)