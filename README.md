## Rewrite

```bash
docker-compose up
```

- http://localhost/jw
- http://localhost/alfresco
- http://localhost/share



## Development

- https://github.com/Alfresco/acs-community-packaging/blob/8411ce5aa224fc88131a1dd7b58d4ae59215b7df/tests/tas-integration/src/test/resources/default.properties


*Restart*

```
docker-compose stop joget
docker-compose stop proxy
docker-compose stop share
docker-compose stop alfresco
docker-compose stop nginx

docker-compose up -d proxy
docker-compose up -d share
docker-compose up -d joget
docker-compose up -d nginx
docker-compose up -d alfresco
```

*Compy nginx.conf*

```bash
docker run --rm --entrypoint cat alfresco/acs-community-ngnix:1.0.0 /etc/nginx/nginx.conf > nginx/proxy.conf
```