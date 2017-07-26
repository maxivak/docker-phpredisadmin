# Overview

* Run PhpRedisAdmin

* container requires redis server



# Build

* build from github

```
docker build -t my-phpredisadmin github.com/maxivak/docker-phpredisadmin.git
```

* or download and build locally
```
docker build -t my-phpredisadmin .
```


# Run

* connect to redis container 'my-redis'

```
docker run -d --name my-phpredisadmin -p 8080:80 \
--link my-redis:redis \
-e REDIS_0_HOST=redis -e REDIS_0_PORT=6379 -e REDIS_0_NAME="my redis server" \
-e ADMIN_USER=admin -e ADMIN_PASS=mypass \
my-phpredisadmin

```

## Config

* Environment variables

* ADMIN_USER, ADMIN_PASS - admin username and password


* REDIS_i_HOST

* REDIS_0_HOST
* REDIS_0_NAME
* REDIS_0_PORT

