## Nginx http proxy for docker containers


#### Create an external bridge network
```
docker network create nginx-proxy
```

#### Start docker container
```
docker-compose up -d
```

#### To enable in other nginx containers, add an environment variable in "web container" service in another docker-compose.yml
```
 environment:
    VIRTUAL_HOST: 'mydomain.local'
```
