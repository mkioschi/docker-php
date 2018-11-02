# Docker PHP

Ambiente Docker para desenvolvimento em PHP. Utilizando Nginx e PHP-7.1.

## Visão Geral

1. [Instalar Pré Requisitos](#pre-requisitos)

    Antes de executar o projeto, tenha certeza que os pré requisitos são atendidos.

2. [Clonar Projeto](#clonar-projeto)

    Baixe o código deste repositório no GitHub. 

3. [Rodar Projeto](#rodar-projeto)

    Com todos requisitos atendidos, aqui iniciamos o projeto.

___

## Pré Requisitos

Este projeto foi criado e testado no sistema operacional `MacOS Mojave 10.14`. Entretando pode funcionar normalmente no Windows e Linux.

Os requisitos abaixo devem estar disponíveis em seu sistema operacional:

* [Git](https://git-scm.com/downloads)
* [Docker](https://docs.docker.com/engine/installation/)
* [Docker Compose](https://docs.docker.com/compose/install/) `[Somente Windows]`

Confira se o `docker-compose` está instalado usando o comando abaixo: 

```sh
which docker-compose
```

Confira a compatibilidade do Docker Compose:

* [Referência do Docker Compose versão 3](https://docs.docker.com/compose/compose-file/)

### Imagens Usadas

* [Nginx](https://hub.docker.com/_/nginx/)
* [PHP](https://hub.docker.com/_/php/)

Este projeto funciona nas seguintes portas:

| Servidor   | Porta |
|------------|-------|
| Nginx      | 80    |
| PHP-FPM    | 9000  |

___

## Clonar Projeto

Com o [Git](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git) instalado, clone o projeto com o comando abaixo:

```sh
git clone https://github.com/mkioschi/docker-php.git
```

Acesse o diretório do projeto:

```sh
cd docker-php
```

### Estrutura do Projeto

```sh
.
├── etc
│   ├── nginx
│   │   └── Dockerfile
│   └── php-fpm
│       └── Dockerfile
├── src
│   └── public
│       └── index.php
├── .gitignore
├── docker-compose.yml
└── README.md
```

___

## Rodar Projeto

1. Iniciar aplicação:

    ```sh
    sudo docker-compose up -d # Roda a aplicação em background
    ```

    **Aguarde, pode demorar vários minutos.**

    ```sh
    sudo docker-compose logs -f # Imprime os logs da aplicação no terminal
    ```

2. Acesse no seu navegador:

    * [http://localhost](http://localhost/)

4. Parar e limpar serviços:

    ```sh
    sudo docker-compose down -v
    ```