<h1 id="top" align="center">Docker Config</h1>

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

```
docker compose -p staucktion build
docker compose -p staucktion up -d --build
docker compose -p staucktion down
```

## 🚀🚀🚀 Dev Commands 🚀🚀🚀

### PostgreSQL

```
docker compose -p staucktion build postgresql
docker compose -p staucktion up -d postgresql
docker compose -p staucktion up --build -d postgresql
docker stop staucktion-postgresql-container
docker rm staucktion-postgresql-container
```

### pgAdmin

```
docker compose -p staucktion build pg-admin
docker compose -p staucktion up -d pg-admin
docker compose -p staucktion up --build -d pg-admin
docker stop staucktion-pg-admin-container
docker rm staucktion-pg-admin-container
```

### Database Initializer

```
docker compose -p staucktion build database-initializer
docker compose -p staucktion up -d database-initializer
docker compose -p staucktion up --build -d database-initializer
docker stop staucktion-database-initializer-container
docker rm staucktion-database-initializer-container
```

### Bank API

```
docker compose -p staucktion build bank-api
docker compose -p staucktion up -d bank-api
docker compose -p staucktion up --build -d bank-api
docker stop staucktion-bank-api-container
docker rm staucktion-bank-api-container
```

### Bank UI

```
docker compose -p staucktion build bank-ui
docker compose -p staucktion up -d bank-ui
docker compose -p staucktion up --build -d bank-ui
docker stop staucktion-bank-ui-container
docker rm staucktion-bank-ui-container
```

### Test Bank API

```
docker compose -p staucktion build test-bank-api
docker compose -p staucktion up -d test-bank-api
docker compose -p staucktion up --build -d test-bank-api
docker stop staucktion-test-bank-api-container
docker rm staucktion-test-bank-api-container
```

## Inspection

```
docker exec -it staucktion-bank-api-container /bin/sh
docker inspect staucktion-bank-api-container
docker logs staucktion-bank-api-container
cls
```
