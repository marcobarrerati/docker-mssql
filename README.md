
# SQL Server - Docker

1. crear ssl 

```sh
openssl req -newkey rsa:2048 -nodes -keyout server.key -x509 -days 365 -out server.crt
```

2. levantar docker 

```
docker-compose up -d
```