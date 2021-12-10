# PHP_LaravelBible
Laravel Quick Fix

```
.env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=poc-iot-db
DB_USERNAME=root
DB_PASSWORD=""
```

```
in project folder 

$COMPOSER_MEMORY_LIMIT=-1 composer install

//php artisan config:cache --env=testing

$php artisan key:generate
$php artisan config:cache
$php artisan serve
```

# Fix Memory Limit

$ php --ini
$ cat /usr/local/etc/php/7.4/php.ini

## Modify
```
; Max memory per instance
memory_limit = 128M
;The maximum size of an uploaded file.
upload_max_filesize = 128M
;Sets max size of post data allowed. This setting also affects file upload. To upload large files, this value must be larger than upload_max_filesize
post_max_size = 128M
```
```
memory_limit setting from 128 to -1
```

### MAC OS 
* cp .env.example .env
* To enable extensions php.ini
* composer update
* composer install
* npm install
* php artisan migrate --seed
* php artisan key:generate
* php artisan serve
