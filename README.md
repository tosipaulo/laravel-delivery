# Curso de Laravel + Ionic
Sistema com Back-End em Laravel + Ionic, para gerar build para smartphones, aplicativo de delivery.

###Instalação do Laravel
Lembrando que a precisar esta instalado o **Composer**
Exemplo para instalação para Linux. Versão que estou documentando é a 5.1
* Obs: Recomendo sempre usar a documentação do [Laravel](http://laravel.com/docs/5.1)

```sh

$ composer global require "laravel/installer=~1.1"

```

Esse comando vai facilitar alguns códigos nativo do Laravel, para criação do projeto.

Em seguinta precisa setar variavel de ambiente.


```sh

$ export PATH="$PATH:~/.composer/vendor/bin"

```

###Criando o projeto
```sh

$ laravel new < nome do projeto >

```

###Configuração básica
Final da instalação edite o arquivo .ENV que fica na raiz do projeto, ele é responsável por toda configuração da aplicação.

```sh

APP_KEY=SomeRandomString

DB_HOST=localhost
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret


```

Muitas vezes o ***APP_KEY*** não é criado, como o exemplo acima, para solucionar esse problema.

```sh

$ php artisan key:generate


```

Recomenda mudar o namespace do projeto, assim ele não conflita com outras aplicações.

```sh

$ php artisan app:name < nome >


```

O arquivo auth.php nem sempre muda com o comando, sempre é bom verificar.

* 'config/auth.php'


Criamos um diretório, chamado ***"Models"***, dentro do diretório "app/".

Editamos o arquivo auth.php para setar o novo valor.


* Valor antigo
```php

'model' => NovoValor\User::class,

```
* Novo valor
```php

'model' => NovoValor\Models\User::class,

```
