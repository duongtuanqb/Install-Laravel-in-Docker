# Install Laravel in Docker 🐳
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