# Guia de Instalação e Configuração do Laravel com Docker

## Requisitos

Antes de começar, certifique-se de ter os seguintes softwares instalados:

- PHP
- Composer
- Docker Desktop
- WSL2 (se estiver usando o Windows)

## Instalação

### Usando PowerShell

Abra o PowerShell e execute o seguinte comando:

```bash
bash curl -s https://laravel.build/example-app | bash
```

### Usando WSL2

Abra o terminal WSL2 e execute o comando abaixo:

```bash
curl -s https://laravel.build/example-app | bash
```

> **Nota:** Substitua "example-app" pelo nome desejado do seu projeto, se preferir.

### Navegar para o Diretório do Projeto

Após a instalação, entre no diretório do projeto com:

```bash
cd example-app
```

### Iniciar os Contêineres

Para iniciar os contêineres, execute:

```bash
./vendor/bin/sail up
```

Se preferir executar os contêineres em segundo plano (modo detach), use:

```bash
./vendor/bin/sail up -d
```

### Executar Migrations

Para aplicar as migrations e criar as tabelas no banco de dados, execute:

```bash
./vendor/bin/sail artisan migrate
```

## Acessando o Laravel

O Laravel será iniciado e estará acessível em:

```
http://localhost/
```

## Configuração Adicional

Para acessar a interface do phpMyAdmin e gerenciar seu banco de dados, adicione a seguinte configuração ao seu arquivo `docker-compose.yml` ou instale o app: [TablePlus](https://tableplus.com/):

```yaml
phpmyadmin:
    image: 'phpmyadmin/phpmyadmin:latest'
    restart: always
    ports:
        - '8080:80'
    environment: 
        PMA_HOST: ${DB_HOST}
        PMA_PORT: ${DB_PORT}
        PMA_USER: '${DB_USERNAME}'
        PMA_PASSWORD: '${DB_PASSWORD}'
    networks:
        - sail
```

Com essas configurações, você poderá acessar o phpMyAdmin em http://localhost:8080/
