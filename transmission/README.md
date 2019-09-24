# Container for transmission
```
transmission:
    image: transmission
    container_name: transmission
    environment:
      - USER=
      - PASS=
      - PUID=1000
      - PGID=1000
      - TZ=
    volumes:
      - ${USERDIR}/docker/transmission/config:/config
      - ${USERDIR}/docker/transmission/downloads:/downloads
      - ${USERDIR}/docker/transmission/watch:/watch
    ports:
      - 9091:9091
      - 51413:51413
      - 51413:51413/udp
    restart: unless-stopped
```
