## Usage
Setup the repository
```
git clone
cd bookstore
composer install
copy .env.example .env 
php artisan key:generate
php artisan cache:clear && php artisan config:clear 
php artisan serve 
```

## Database Setup
We are going to pull in data from the database so make sure that you have your database setup
```
mysql;
create database apipost;
exit;
```


Setup your database credentials in the .env file
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=apipost
DB_USERNAME={USERNAME}
DB_PASSWORD={PASSWORD}
```

Migrate the tables
```
php artisan migrate
```	

## HTTP Methods
Available HTTP methods on a resource

| **Verb**        | **Path**           | **Action**  | **Route Name**        | **Description**   |
| ------------- |-------------| -----| ------------- |-------------|
| GET         | /authors | index | authors.index | Get all authors |
| POST         | /authors | store | authors.store | Create a new authors |
| GET         | /posts | index | authors.index | Get all posts |
| POST         | /posts | store | authors.store | Create a new posts |