get the ipv6 address from traefik by reading the network info
docker network inspect traefik
Then use it in a curl with the follow redirect and insecure option
curl -vv -k -6 -L http://\[2001:3984:3989::2\]/api/rawdata
