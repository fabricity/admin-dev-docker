# Admin Dev Docker

- [localhost:8888](http://localhost:8888/) -> traefik
- [https://admin-web.localhost/](https://admin-web.localhost/)
- [https://admin-mail.localhost/](https://admin-mail.localhost/)
- localhost:543**6** root:root -> postgres

**Tip** chrome://flags -> allow-insecure-localhost -> enable

## Add admin code
````ssh
git clone git@github.com:fabricity/admin-demo.git
cd admin-demo && composer install
````

## Docker
````ssh
docker-compose up -d
docker-compose exec admin php -v
````

### Clean commands
````ssh
docker-compose down
docker rm -f $(docker ps -a -q)
docker volume rm $(docker volume ls -q)
docker-compose up -d
````