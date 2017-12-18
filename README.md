# Dockerised php script

A small miniature example of a php app served by nginx and php-fpm from 2 containers.

see `docker-compose.yml`
- this has 2 containers, php (based on `php:7.1-fpm`) and nginx (based on `nginx:latest`).
- both are on the same network so they can see each other.
- the compose uses volumes to replace the default nginx configuration to facilitate the fastcgi and use the php-fpm port 9000
- the `app` folder is the php application which is 1 `index.php` (html) and a `script.php` which runs the php script.
