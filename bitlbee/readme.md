# Container for bitlbee
Run it by using
```
docker run --rm -it -e BITLBEEPORT='1337' -p 1337:1337 -v $(pwd)/config:/config bitlbee 
```