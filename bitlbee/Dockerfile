# Setting OS
FROM debian:stretch

# Env
ENV BITLBEEPORT=1337

# install packages
RUN \
    apt-get update &&\
    apt-get install -y --no-install-recommends \
    bitlbee-libpurple

# Expose of ports and volumes
EXPOSE 1337
VOLUME ["/config"]

# Copy folders
COPY root/ /

ENTRYPOINT ["/start.sh"]
