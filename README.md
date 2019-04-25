## Build each service image
```
docker build -b ms-node-a .
```

## Docker run stack service demo
```
docker stack deploy --compose-file=docker-compose.yml demo
```

## Docker dynamically scale the service
```
docker service scale demo_ms-node-a=10
```

## Docker check service tasks status
```
docker service ps demo_ms-node-a
```

## Docker filter for running container tasks
```
docker ps --filter name=demo_ms-node-a
```

## Docker viewing haproy log
```
docker logs -f CONTAINER_ID
```
