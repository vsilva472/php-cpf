# Validar CPF em PHP

[![Build Status](https://travis-ci.org/vsilva472/phpcpf.svg?branch=master)](https://travis-ci.org/vsilva472/phpcpf) [![license](https://img.shields.io/github/license/vsilva472/phpcpf.svg)](https://github.com/vsilva472/phpcpf/blob/master/LICENSE.md) [![Packagist](https://img.shields.io/packagist/v/vsilva472/phpcpf.svg)](https://packagist.org/packages/vsilva472/phpcpf)

## Descrição

phpCPF é uma classe escrita em PHP para validar CPF (independente se o valor possui máscara aplicada 999.999.999-99 ou não) de acordo com as normas estabelecidas pelo governo brasileiro.

## Requisitos
* [PHP](https://php.net) 5.6+

## Instalação
> Nota: Recomendamos a instalação via **Composer**. Você também pode baixar o repositório como arquivo zip ou fazer um clone via Git.

### Instalação via Composer
> Para baixar e instalar o Composer no seu ambiente acesse [https://getcomposer.org/download/](https://getcomposer.org/download/) e caso tenha dúvidas de como utilizá-lo consulte a [documentação oficial do Composer](https://getcomposer.org/doc/). Veja também a seção de como instalá-lo globalmente

+ Executando o comando para adicionar a dependência automaticamente
```php
composer require vsilva472/phpcpf
```

**OU**

* Adicionando a dependência ao seu arquivo composer.json

```php
{
    "require": {
       "vsilva472/phpcpf" : "*"
    }
}
``` 

### Instalação manual
* Baixe o repositório como arquivo [zip](https://github.com/vsilva472/phpcpf/archive/master.zip) ou faça um clone;
* Descompacte os arquivos em seu projeto;
* Execute o comando `composer install` no local onde extraiu os arquivos;

## Como utilizar

```php
<?php

require "path/to/vendor/autoload.php";

// raw cpf
$cpf = '123.456.789-00';

// Make the CPF validator
$validator = new \Vsilva472\phpCPF\CPF();

// @boolean 
$is_cpf_valid = $cpf->validate( $_POST[ 'cpf' ] );

if ( $is_cpf_valid ) {
    // do something with valid CPF
}

else {
    // invalid CPF! Do something
}
?>
```
O diretório "examples" contém exemplos de uso e a pasta "src" contém o código fonte da classe.

## Nota

Esta classe é uma versão em PHP OO (com ligireiras modificações) da função disponibilizada em [http://www.geradorcpf.com/script-validar-cpf-php.htm](http://www.geradorcpf.com/script-validar-cpf-php.htm). 
Todo o crédito na elaboração do algorítimo de validação deve ser dado ao autor da função.

## Laravel
Experimente [Laravel CPF](https://github.com/vsilva472/laravel-cpf) caso precise validar CPF em ambientes [Laravel](https://laravel.com).

## Créditos
Equipe do site [http://www.geradorcpf.com](http://www.geradorcpf.com) por disponibilizar a função em php estruturado.

## Changelog
Para consultar o log de alterações acesse o arquivo [CHANGELOG.md](https://github.com/vsilva472/phpcpf/blob/master/CHANGELOG.md)

### Doação
Contribua para o projeto doando qualquer quantidade de **HTMLCOIN**  
Carteira: **[HqgaiK6T1o2JP4p3p34CZp2g3XnSsSdCXp](htmlcoin:HqgaiK6T1o2JP4p3p34CZp2g3XnSsSdCXp?label=Doa%C3%A7%C3%B5es%20Github)**  
  
![Doar HTMLCoin](https://www.viniciusdesouza.com.br/img/htmlcoin.png)

### Licença
MIT
