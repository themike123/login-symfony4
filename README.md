## Descripción
Login automático en symfony 4.3

## Requerimientos
 * PHP 7.2
 * Mariadb 10.3.15
 * Composer 1.8.6

Extensiones  de PHP(que están instaladas y habilitadas en la mayoría de las instalaciones de PHP 7 o superior ) para que Symfony funcione:  [Ctype](https://www.php.net/book.ctype), [iconv](https://www.php.net/book.iconv), [JSON](https://www.php.net/book.json), [PCRE](https://www.php.net/book.pcre), [Session](https://www.php.net/book.session), [SimpleXML](https://www.php.net/book.simplexml), and [Tokenizer](https://www.php.net/book.tokenizer);


## Instalación
	// Directorio donde se quiere instalar
	$ git clone https://github.com/themike123/gtifac2
	$ cd login-symfony4
	$ composer install	

## Cofiguración necesaria

### Doctrine
Configurar la conexión a base de datos

	// .env
	DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name
```bash
$ php bin/console doctrine:migrations:migrate
```

Cargar el usuario Admin
```bash
$ php bin/console doctrine:fixtures:load
```


### Server
En el composer.json viene especificado que se instalará [symfony/web-server-bundle](https://symfony.com/doc/current/setup/built_in_web_server.html) en modo desarrollo, por lo que se usará ese como servidor web. Es libre de optar por usar el server de [Symfony CLI](https://symfony.com/doc/current/setup/symfony_server.html). 

```bash
$ php bin/console serve:run
```
