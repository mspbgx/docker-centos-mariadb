# docker-centos-mariadb

[![](https://images.microbadger.com/badges/version/mspbgx/centos-mariadb.svg)](https://microbadger.com/images/mspbgx/centos-mariadb "Get your own version badge on microbadger.com")
[![Docker Pulls](https://img.shields.io/docker/pulls/mspbgx/centos-mariadb.svg)](hub)
[![Docker Stars](https://img.shields.io/docker/stars/mspbgx/centos-mariadb.svg)](hub)

**MAINTAINER:** Maximilian Sparenberg <sparenberg@openenv.de>


## Description
Mariadb in a docker container based on centos image.
```
FROM centos:latest
```

## Usage
### Standalone
```
docker run -d --name mariadb -e MYSQL_ROOT_PASSWORD=ABC123xyz -e MYSQL_DATABASE=nextcloud -e MYSQL_USER=nextcloud -e MYSQL_PASSWORD=ABC123xyz -p 3306:3306 mspbgx/centos-mariadb
```
### Compose
cat docker-compose.yml
```
version: '3.1'

services:

  db:
    image: mspbgx/centos-mariadb
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: ABC123xyz
```
### Variables:
```
MYSQL_ROOT_PASSWORD = <mysql root password>
```
```
MYSQL_DATABASE = <database to be created>
```
```
MYSQL_USER = <user to be created>
```
```
MYSQL_PASSWORD = <password to be created>
```
```
MYSQL_CHARSET = <charset to be used>
```
```
MYSQL_COLLATION = <collation to be used>
```
