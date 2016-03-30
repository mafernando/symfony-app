Symfony App: A Simple Symfony MySQL ToDo List
===============================

Usage
-----

Generate `Dockerfile` and `docker-compose.yml` and add them to the directory containing the app code. 

Run `docker-compose up` to prepare the environment.

Use `docker exec -it symfonyapp_app_1 /bin/bash` to attach a shell to the app container.

Then execute the following to prepare the MySQL database. 

```bash
rm -rf app/cache/
composer install
chown -R www-data:www-data /app 
php app/console assetic:dump
php app/console doctrine:schema:create
```

