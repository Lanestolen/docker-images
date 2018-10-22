# Setting OS
FROM debian:stretch

# Env
ENV BITLBEEPORT=1337

# install packages
RUN \
    apt-get update &&\
    apt-get install -y --no-install-recommends \
        bitlbee-libpurple

# Installing requirements for bitlbee Facebook
RUN \
    apt install -y --no-install-recommends\
        apt-transport-https wget gnupg2 ca-certificates && \
    echo "deb http://download.opensuse.org/repositories/home:/jgeboski/Debian_9.0 ./" >> /etc/apt/sources.list.d/jgeboski.list &&\
    wget https://jgeboski.github.io/obs.key && \
    apt-key add obs.key &&\
    rm obs.key && \
    apt-get update && \
    apt-get install -y --no-install-recommends \
        bitlbee-facebook

# Installing requirements for bitlbee Slack
RUN \
    apt install -y --no-install-recommends\
        git build-essential libpurple-dev && \
    git clone https://github.com/dylex/slack-libpurple.git && \
    cd slack-libpurple && \
    make install

# Expose of ports and volumes
EXPOSE 1337
VOLUME ["/config"]

# Copy folders
COPY root/ /

ENTRYPOINT ["/start.sh"]
