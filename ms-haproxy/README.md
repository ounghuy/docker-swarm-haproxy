# HAproxy with rsyslog

This docker container provides highly efficient load balancer which is HAproxy however to enrich logging of details
it also provides syslog information. 

```
## Running container 
In order to run container (assuming you have an haproxy config file) you can just run the following 
```
docker run -d -P -v ${PWD}/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg {Name of docker image}
```

This is of course only basic example since you will for sure need to adjust it to your requirements like ports/networks/volumes etc.




