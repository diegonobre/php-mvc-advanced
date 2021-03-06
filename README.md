# PHP-MVC-ADVANCED

*Atenção: Este é um projeto de tradução da versão original existente em [panique/php-mvc-advanced](https://github.com/panique/php-mvc-advanced).*

*Nota: Este projeto é igual ao projeto [panique/php-mvc](https://github.com/panique/php-mvc), mas com alguns recursos adicionais.*
*Estamos em desenvolvimento, há mais por vir...*

### Novo na versão avançada:

1. Twig
2. SASS-compiler in PHP ! A compilação utilizando SASS é opcional, você pode apagar o diretório scss e usar apenas o .css clássico também.
   Usei o https://github.com/panique/laravel-sass aqui.

Uma aplicação em PHP utilizando MVC extremamente simples e fácil de entender, reduzida ao máximo.
Tudo é o mais **simples possível**, mais **manualmente possível** e o mais legível possível.

O projeto - intencionalmente - NÃO é um framework completo, é uma estrutura crua, escrita em
PHP puro nativo ! O php-mvc skeleton tenta ser extremamente magro ("seco") ao contrário de framworks
como Zend2, Symphoby ou Laravel.

### Objetivos do projeto:

- disponibilizar uma estrutura básica em PHP utilizando MVC
- ensinar o básico da arquitetura Model-View-Controller
- encorajar a codificação de acordo com os padrões PSR 1/2
- promover o uso do PDO
- promover o uso de bibliotecas externas usando Composer
- promover desenvolvimento com o máximo de controle de exceção
- promover códigos comentados
- promover o uso de PHP Orientado a Objeto
- usar apenas PHP nativo para que as pessoas não sejam obrigadas a aprender um framework

## Instalação

1. First, install Composer ([How to install Composer on Ubuntu, Debian or Windows 7/8](http://www.dev-metal.com/install-update-composer-windows-7-ubuntu-debian-centos/)).
That's some kind of PHP standard now and there's no reason to work without Composer. If you think "I don't need/want
Composer" then you are doing something seriously wrong!

2. Copy this repo into a public accessible folder on your server.
Common techniques are a) downloading and extracting the .zip / .tgz by hand, b) cloning the repo with git (into var/www)

```
git clone https://github.com/panique/php-mvc-advanced.git /var/www
```

or c) getting the repo via Composer (here we copy into var/www)

```
composer create-project panique/php-mvc-advanced /var/www dev-master
```

3. Install mod_rewrite, for example by following this guideline:
[How to install mod_rewrite in Ubuntu](http://www.dev-metal.com/enable-mod_rewrite-ubuntu-12-04-lts/)

4. Run the SQL statements in the *application/_install* folder.

5. Change the .htaccess file from
```
RewriteBase /php-mvc-advanced/
```
to where you put this project, relative to the web root folder (usually /var/www). So when you put this project into
the web root, like directly in /var/www, then the line should look like or can be commented out:
```
RewriteBase /
```
If you have put the project into a sub-folder, then put the name of the sub-folder here:
```
RewriteBase /sub-folder/
```

6. Edit the *application/config/config.php*, change this line
```php
define('URL', 'http://127.0.0.1/php-mvc-advanced/');
```
to where your project is. Real domain, IP or 127.0.0.1 when developing locally. Make sure you put the sub-folder
in here (when installing in a sub-folder) too, also don't forget the trailing slash !

7. Edit the *application/config/config.php*, change these lines
```php
define('DB_TYPE', 'mysql');
define('DB_HOST', '127.0.0.1');
define('DB_NAME', 'php-mvc');
define('DB_USER', 'root');
define('DB_PASS', 'mysql');
```
to your database credentials. If you don't have an empty database, create one. Only change the type `mysql` if you
know what you are doing.

8. Run `composer install` on the command line while being in the root of your project.

## A quickstart tutorial

You can also find these tutorial pictures in the *_tutorial* folder.
**Note:** **These files are not up-to-date, as Twig and SASS support are not mentioned here. I'll update the tutorial
when there's time.**

![php-mvc introduction tutorial - page 1](_tutorial/tutorial-part-01.png)
![php-mvc introduction tutorial - page 2](_tutorial/tutorial-part-02.png)
![php-mvc introduction tutorial - page 3](_tutorial/tutorial-part-03.png)
![php-mvc introduction tutorial - page 4](_tutorial/tutorial-part-04.png)
![php-mvc introduction tutorial - page 5](_tutorial/tutorial-part-05.png)

## You like what you see ?

Then please also have a look on ...

#### My other project php-login

A collection of 4 similar login scripts for PHP, from a super-simple one-file
script with a SQLite one-file to a highly professional MVC frameworks solution. All scripts use the most advanced
hashing algorithms possible in PHP, exactly like the PHP core developers want you to use them.

https://github.com/panique/php-login (full MVC framework)

https://github.com/panique/php-login-minimal (minimal)

https://github.com/panique/php-login-advanced (advanced)

https://github.com/panique/php-login-one-file (one-file)

#### My PHP and frontend blog

Lots of non-boring development stuff and tutorials there.

http://www.dev-metal.com

## Useful information

1. SQLite does not have a rowCount() method (!). Keep that in mind in case you use SQLite.

2. Don't use the same name for class and method, as this might trigger an (unintended) *__construct* of the class.
   This is really weird behaviour, but documented here: [php.net - Constructors and Destructors](http://php.net/manual/en/language.oop5.decon.php).

## Add external libraries via Composer

To add external libraries/tools/whatever into your project in an extremely clean way, simply add a line with the
repo name and version to the composer.json! Take a look on these tutorials if you want to get into Composer:
[How to install (and update) Composer on Windows 7 or Ubuntu / Debian](http://www.dev-metal.com/install-update-composer-windows-7-ubuntu-debian-centos/)
and [Getting started with Composer](http://www.dev-metal.com/getting-started-composer/).

## License

This project is licensed under the MIT License.
This means you can use and modify it for free in private or commercial projects.

## Contribute

Please commit into the develop branch (which holds the in-development version), not into master branch
(which holds the tested and stable version).

## Support / Donate

If you think this script is useful and saves you a lot of work, then think about supporting the project:

1. Donate via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=P5YLUK4MW3LDG) or [GitTip](https://www.gittip.com/Panique/)
2. Rent your next server at [A2 Hosting](http://www.a2hosting.com/4471.html) or [DigitalOcean](https://www.digitalocean.com/?refcode=40d978532a20).
3. Contribute to this project. Feel free to improve this project with your skills.
4. Spread the word: Tell others about this project.

## Linked music tracks in the demo application

The linked tracks in this naked application are just some of my personal favourites of the last few months.
I think it's always a good idea to fill boring nerd-code stuff with quality culture.
