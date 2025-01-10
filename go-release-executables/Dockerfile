FROM debian:latest
RUN DEBIAN_FRONTEND=noninteractive apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install --no-install-recommends -y \
  curl \
  wget \
  git \
  build-essential \
  zip \
  jq \
  ca-certificates \
  bash

ADD main.sh /main.sh
ADD build.sh /build.sh
RUN ["chmod", "+x", "/main.sh"]
RUN ["chmod", "+x", "/build.sh"]
ENTRYPOINT ["/main.sh"]

# GOARCH='386' GOOS=linux SUBDIR=bnr-utils/nz_azConnector EXECUTABLE_NAME=nz_azConnector
