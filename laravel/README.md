# docker-laravel

create an app

```bash
composer create-project --prefer-dist laravel/laravel app
```

or

```bash
laravel new app
```

Run command in app folder.

```bash
docker-compose up
```

modify `.env`

```bash
DB_HOST=db
DB_DATABASE=app
DB_USERNAME=root
DB_PASSWORD=password
```

```bash
docker-compose exec app php artisan list
```
