# Container for flexget
```
flexget:
    container_name: flexget
    image: flexget
    restart: always
    volumes:
      - ${USERDIR}/docker/flexget/config:/config
    environment:
      - RSS=
      - USER=
      - PASS=
      - PUID=1000
      - PGID=1000
      - TZ=Europe/Copenhagen
```
