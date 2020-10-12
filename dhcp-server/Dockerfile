FROM lanestolen/base-image
LABEL maintainer="Lanestolen"

COPY root/ /

RUN set -xe \
    && apk add --no-cache --purge -uU dhcp \
    && touch /var/lib/dhcp/dhcpd.leases \
    && rm -rf /var/cache/apk/* /tmp/*

EXPOSE 67
ENTRYPOINT ["/init"]
