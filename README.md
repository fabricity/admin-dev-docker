# Admin Dev Docker

- [localhost:8888](http://localhost:8888/) -> traefik
- [https://admin-web.localhost/](https://admin-web.localhost/)
- [https://admin-mail.localhost/](https://admin-mail.localhost/)
- localhost:543**6** root:root -> postgres

**Tip** chrome://flags -> allow-insecure-localhost -> enable

## Admin demo code
By default, the admin-web container will attach a volume from local path **./../admin-demo**.
You can change the path in the .env file.

## Docker
````ssh
docker-compose up -d
docker-compose exec admin php -v
docker-compose exec admin php bin/console doctrine:database:create
docker-compose exec admin php bin/console doctrine:schema:update --force 
docker-compose exec admin php bin/console doctrine:fixtures:load
````

### Clean commands
````ssh
docker-compose down
docker rm -f $(docker ps -a -q)
docker volume rm $(docker volume ls -q)
docker-compose up -d --force-recreate 
````

  