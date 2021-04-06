# Admin Dev Docker

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

- [localhost:88**61**](http://localhost:8861) -> admin-web
- [localhost:88**62**](http://localhost:8862) -> admin-mail
- localhost:543**6** root:root -> postgres