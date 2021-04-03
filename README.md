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

- http://localhost:88**61**/ -> web
- http://localhost:88**62**/ -> mailhog
- localhost:543**6** root:root -> postgres