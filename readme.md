# YLP業務管理システム

## Requirements
- PHP 7.1.3+
- Mysql 5.7
- Nodejs 8.0+

## Coding conventions
- [PRS-2](https://www.php-fig.org/psr/psr-2/)

## PHP extension requirements
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension
- Ctype PHP Extension
- JSON PHP Extension

## Clone repository
```
git clone git@github.com:beeanz/ylp.bm.git
```

## Install [composer](https://getcomposer.org/)
```
curl -s https://getcomposer.org/installer | php
```

## Create application config file, edit .env file to add config (Database, API key, ...)
```
cp .env.example .env
```

## Install dependencies
```
composer install
```

## Generate APP_KEY
```
php artisan key:generate
```

## Create tables, seed data for database
```
php artisan migrate
php artisan db:seed
```

## Install npm package
```
sudo apt-get install npm
sudo npm install
```

## Config webpack
Edit file `./webpack.mix.js`
```
mix.js('resources/assets/js/app.js', 'public/js')
  .sass('resources/assets/sass/app.scss', 'public/css')
  .version();
```

## Running Mix
```
// Run all Mix tasks...
npm run dev

// Run all Mix tasks and minify output...
npm run production
```

### Watching Assets For Changes

```
npm run watch
```

## Check coding conventions
[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
[PHPmd](https://github.com/phpmd/phpmd)
```
//check conventions
vendor/bin/phpcs
vendor/bin/phpmd app,database,routes,tests text phpmd.xml

//auto fix convention for phpcs
vendor/bin/phpcbf

```