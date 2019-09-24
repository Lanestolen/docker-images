FROM eyjhb/alpine-base:3.7
LABEL maintainer="Lanestolen"

ENV VERSION 1
ENV TRANSMISSION_VERSION 2.92-r8

# Install packages needed for transmission
RUN \
apk add --no-cache \
    transmission-daemon=$TRANSMISSION_VERSION \
    transmission-cli=$TRANSMISSION_VERSION

COPY root / /

# RUN \
# chmod +x root/start.sh

EXPOSE 9091 51413
VOLUME ["/config", "/downloads", "/watch"]
