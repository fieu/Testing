FROM ubuntu:16.04

LABEL maintainer="Sheldon Rupp <me@shel.io>"

LABEL \
  org.label-schema.name="millecoin-daemon" \
  org.label-schema.url="https://github.com/NurdTurd/Testing.git" \
  org.label-schema.vcs-url="https://github.com/NurdTurd/Testing.git"

WORKDIR /app

CMD ["/app/Millecoind", "--enable-cors='*'", "--enable_blockexplorer", "--rpc-bind-ip=0.0.0.0", "--rpc-bind-port=31238"]