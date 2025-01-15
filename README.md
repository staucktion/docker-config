<h1 id="top" align="center">Docker Config</h1>

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

```
docker compose -p staucktion build
docker compose -p staucktion up -d --build
docker compose -p staucktion down
```

<br/>

## 🚀🚀🚀 Dev Commands 🚀🚀🚀

### PostgreSQL

```
docker compose -p staucktion build postgresql
docker compose -p staucktion up -d postgresql
docker compose -p staucktion up --build -d postgresql
docker stop st-postgresql-c
docker rm st-postgresql-c
```

### pgAdmin

```
docker compose -p staucktion build pg-admin
docker compose -p staucktion up -d pg-admin
docker compose -p staucktion up --build -d pg-admin
docker stop st-pgadmin-c
docker rm st-pgadmin-c
```

### Database Initializer

```
docker compose -p staucktion build database-initializer
docker compose -p staucktion up -d database-initializer
docker compose -p staucktion up --build -d database-initializer
docker stop st-database-initializer-c
docker rm st-database-initializer-c
```

### Bank API

```
docker compose -p staucktion build bank-api
docker compose -p staucktion up -d bank-api
docker compose -p staucktion up --build -d bank-api
docker stop st-bank-api-c
docker rm st-bank-api-c
```

### Web API

```
docker compose -p staucktion build web-api
docker compose -p staucktion up -d web-api
docker compose -p staucktion up --build -d web-api
docker stop st-web-api-c
docker rm st-web-api-c
```

### Web UI

```
docker compose -p staucktion build web-ui
docker compose -p staucktion up -d web-ui
docker compose -p staucktion up --build -d web-ui
docker stop st-web-ui-c
docker rm st-web-ui-c
```

### Bank UI

```
docker compose -p staucktion build bank-ui
docker compose -p staucktion up -d bank-ui
docker compose -p staucktion up --build -d bank-ui
docker stop st-bank-ui-c
docker rm st-bank-ui-c
```

### Test Bank API

```
docker compose -p staucktion build test-bank-api
docker compose -p staucktion up -d test-bank-api
docker compose -p staucktion up --build -d test-bank-api
docker stop st-test-bank-api-c
docker rm st-test-bank-api-c
```

## Inspection

```
docker exec -it st-bank-api-c /bin/sh
docker inspect st-bank-api-c
docker logs st-bank-api-c
cls
```
