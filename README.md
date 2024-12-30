## 🚀🚀🚀 Dev Commands 🚀🚀🚀

```
docker compose -p staucktion build postgresql
docker compose -p staucktion up -d postgresql
docker compose -p staucktion up --build -d postgresql
docker stop staucktion-postgresql-container
docker rm staucktion-postgresql-container

docker compose -p staucktion build pg-admin
docker compose -p staucktion up -d pg-admin
docker compose -p staucktion up --build -d pg-admin
docker stop staucktion-pg-admin-container
docker rm staucktion-pg-admin-container

docker compose -p staucktion build database-initializer
docker compose -p staucktion up -d database-initializer
docker compose -p staucktion up --build -d database-initializer
docker stop staucktion-database-initializer-container
docker rm staucktion-database-initializer-container

docker compose -p staucktion build bank-api
docker compose -p staucktion up -d bank-api
docker compose -p staucktion up --build -d bank-api
docker stop staucktion-bank-api-container
docker rm staucktion-bank-api-container

docker compose -p staucktion build test-bank-api
docker compose -p staucktion up -d test-bank-api
docker compose -p staucktion up --build -d test-bank-api
docker stop staucktion-test-bank-api-container
docker rm staucktion-test-bank-api-container

docker compose -p staucktion build
docker compose -p staucktion up -d
docker compose -p staucktion up -d --build
docker compose -p staucktion down
```

```
docker exec -it staucktion-bank-api-container /bin/sh
docker inspect staucktion-bank-api-container
docker logs staucktion-bank-api-container
cls
```