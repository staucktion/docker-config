<h1 id="top" align="center">Docker Config [v1.2.0]</h1>

<h2 id="system-links">🔗 System Links</h2> 

| Service  | URL                                                    |
|----------|--------------------------------------------------------|
| web-ui   | [st.local.net](https://st.local.net)                   |
| bank-ui  | [st.local.net/bank-ui](https://st.local.net/bank-ui)   |
| web-api  | [st.local.net/web-api](https://st.local.net/web-api)   |
| bank-api | [st.local.net/bank-api](https://st.local.net/bank-api) |
| pg-admin | [localhost:900](http://localhost:9001)                 |

<br/>

<h2 id="service-versions">🧩 Service Versions</h2>

| Service              | Version                                                                                                                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| docker-config        | [![.](https://img.shields.io/badge/1.2.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/docker-config/tree/v1.2.0)        |
| reverse-proxy        | [![.](https://img.shields.io/badge/1.1.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/reverse-proxy/tree/v1.1.0)        |
| postgresql           | [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/postgresql/tree/v1.0.0)           |
| bank-api             | [![.](https://img.shields.io/badge/1.0.1-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/bank-api/tree/v1.0.1)             |
| bank-ui              | [![.](https://img.shields.io/badge/1.0.1-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/bank-ui/tree/v1.0.1)              |
| web-api              | [![.](https://img.shields.io/badge/1.2.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/web-api/tree/v1.2.0)              |
| web-ui               | [![.](https://img.shields.io/badge/1.2.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/web-ui/tree/v1.2.0)               |
| database-initializer | [![.](https://img.shields.io/badge/1.2.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/database-initializer/tree/v1.2.0) |
| pg-admin             | [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/pg-admin/tree/v1.0.0)             |
| test-bank-api        | [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/staucktion/test-bank-api/tree/v1.0.0)        |

<br/>

<h2 id="system-preparation">🔒 System Preparation</h2>

- add following line to host file
```
127.0.0.1 st.local.net
```

- host file on OS:
- **Widows:** C:\Windows\System32\drivers\etc\hosts
- **Linux, Mac:** /etc/hosts

- Create new directory and move inside.
- Clone repositories.

```
git clone https://github.com/staucktion/docker-config
git clone https://github.com/staucktion/reverse-proxy
git clone https://github.com/staucktion/postgresql
git clone https://github.com/staucktion/bank-api
git clone https://github.com/staucktion/bank-ui
git clone https://github.com/staucktion/web-api
git clone https://github.com/staucktion/web-ui
git clone https://github.com/staucktion/database-initializer
git clone https://github.com/staucktion/pg-admin
git clone https://github.com/staucktion/test-bank-api
```

- Configure env variables in repositories as stated in each repository.

- Build all images

```
docker compose -p staucktion build
```

- Run `up` commands for the modules which you want to launch.

- You can selectively start the necessary modules. Below is the recommended startup order:

1. Reverse Proxy
2. PostgreSQL
3. Database Initializer
4. Bank API
5. Web API
6. Web UI

- Optional Modules

7. Bank UI
8. pgAdmin
9. Test Bank API

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

```
docker compose -p staucktion build
docker compose -p staucktion up -d --build
docker compose -p staucktion down
```

<br/>

## 🚀🚀🚀 Dev Commands 🚀🚀🚀

### Reverse Proxy

```
docker compose -p staucktion build          reverse-proxy
docker compose -p staucktion up -d          reverse-proxy
docker compose -p staucktion up --build -d  reverse-proxy
docker stop                                 st-reverse-proxy-c
docker rm                                   st-reverse-proxy-c
docker logs -f                              st-reverse-proxy-c
```

### PostgreSQL

```
docker compose -p staucktion build          postgresql
docker compose -p staucktion up -d          postgresql
docker compose -p staucktion up --build -d  postgresql
docker stop                                 st-postgresql-c
docker rm                                   st-postgresql-c
docker logs -f                              st-postgresql-c
```

### Bank API

```
docker compose -p staucktion build          bank-api
docker compose -p staucktion up -d          bank-api
docker compose -p staucktion up --build -d  bank-api
docker stop                                 st-bank-api-c
docker rm                                   st-bank-api-c
docker logs -f                              st-bank-api-c
```

### Bank UI

```
docker compose -p staucktion build         bank-ui
docker compose -p staucktion up -d         bank-ui
docker compose -p staucktion up --build -d bank-ui
docker stop                                st-bank-ui-c
docker rm                                  st-bank-ui-c
docker logs -f                             st-bank-ui-c
```

### Web API

```
docker compose -p staucktion build          web-api
docker compose -p staucktion up -d          web-api
docker compose -p staucktion up --build -d  web-api
docker stop                                 st-web-api-c
docker rm                                   st-web-api-c
docker logs -f                              st-web-api-c
```

### Web UI

```
docker compose -p staucktion build          web-ui
docker compose -p staucktion up -d          web-ui
docker compose -p staucktion up --build -d  web-ui
docker stop                                 st-web-ui-c
docker rm                                   st-web-ui-c
docker logs -f                              st-web-ui-c
```

### Database Initializer

```
docker compose -p staucktion build          database-initializer
docker compose -p staucktion up -d          database-initializer
docker compose -p staucktion up --build -d  database-initializer
docker stop                                 st-database-initializer-c
docker rm                                   st-database-initializer-c
docker logs -f                              st-database-initializer-c
```

### pgAdmin

```
docker compose -p staucktion build         pg-admin
docker compose -p staucktion up -d         pg-admin
docker compose -p staucktion up --build -d pg-admin
docker stop                                st-pgadmin-c
docker rm                                  st-pgadmin-c
docker logs -f                             st-pgadmin-c
```

### Test Bank API

```
docker compose -p staucktion build         test-bank-api
docker compose -p staucktion up -d         test-bank-api
docker compose -p staucktion up --build -d test-bank-api
docker stop                                st-test-bank-api-c
docker rm                                  st-test-bank-api-c
docker logs -f                             st-test-bank-api-c
```

<br/>

## 🔍 Inspect & Monitor

```
docker exec -it st-bank-api-c /bin/sh
docker inspect st-bank-api-c
```
