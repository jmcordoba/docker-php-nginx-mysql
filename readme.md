# Docker
## Start project
In order to start the docker container you have to execute the following commands:
```php
cd /project_path/
docker-compose build
docker-compose up -d
```
## List containers:
```php
docker ps -a -q

-a: the option to list all containers, even stopped ones. Without this, it defaults to only listing running containers
-q: the quiet option to provide only container numeric IDs, rather than a whole table of information about containers
```
## Enter to any container
In order to enter the docker container you have to execute the following commands:
```php
docker exec -it demo_nginx_1 sh
```
## Stop containers
Stop container by id:
```php
docker stop <container-id>
```
Stop all running containers:
```php
docker stop $(docker ps -a -q)
```
## Delete containers
Delete all stopped containers:
```php
docker rm $(docker ps -a -q)
```
## Remove images
Remove images by their id:
```php
docker rmi <your-image-id>
```
Remove all images at once:
```php
docker rmi $(docker images -q)
```
## Prune
```
docker system prune -a
```