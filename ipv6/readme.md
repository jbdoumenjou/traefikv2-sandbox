# Goal

Manipulate ipv6.  
We can get all needed info by inspecting the traefik network with the following command:

```bash
docker network inspect traefik
```

The file configuration is used to force the ipv6 usage for the backend server.  
 
We can check both the http to https redirection and the internal redirect from "/" to "/dashboard"

To check if the ipv6 works as expected, we can use curl command like:

```bash
curl -v -k -6 -L http://\[2001:3984:3989::2\]/api/rawdata
curl -v -k -6 -L http://\[::1\]:8080/
```
