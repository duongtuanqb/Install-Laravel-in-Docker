# Install Laravel in Docker 🐳
[![GitHub forks](https://img.shields.io/github/forks/duongtuanqb/Install-Laravel-in-Docker?style=flat-square)](https://github.com/duongtuanqb/Install-Laravel-in-Docker/network)
[![GitHub stars](https://img.shields.io/github/stars/duongtuanqb/Install-Laravel-in-Docker?style=flat-square)](https://github.com/duongtuanqb/Install-Laravel-in-Docker/stargazers)
[![GitHub license](https://img.shields.io/github/license/duongtuanqb/Install-Laravel-in-Docker?style=flat-square)](https://github.com/duongtuanqb/Install-Laravel-in-Docker/blob/master/LICENSE)
![GitHub All Releases](https://img.shields.io/github/downloads/duongtuanqb/Install-Laravel-in-Docker/total?style=flat-square)

## Docker compose services:
| Servicer name | Tag |
|-|-|
|php|7.4-fpm-alpine|
|phpmyadmin|latest|
|nginx|alpine|
|mysql|8.0|
|redis|5-alpine|

## Setup:
`` $ cd docker ``
`` $ docker-compose up -d --build ``
`` $ docker-compose exec php /bin/sh ``
`` $ laravel new ``

```
# laravel http://localhost:8080
# phpmyadmin http://localhost:8081
```
