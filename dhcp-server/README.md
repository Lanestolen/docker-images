# Container for DHCP
This container is primarily created for testing purposes if you wanna use it move the folder dhcpd into root/etc and customize the dhcpd.conf in the config folder 
```
docker run -v "$(pwd)/config/dhcpd.conf":/etc/dhcp/dhcpd.conf lanestolen/dhcp
```
