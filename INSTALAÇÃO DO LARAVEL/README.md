# Guia de Instalação do Laravel

## Requisitos

Antes de começar, certifique-se de que você tem os seguintes requisitos instalados:

- **PHP** (versão 8.0 ou superior)
- **Composer** (gerenciador de dependências para PHP)
- **Servidor Web** (por exemplo, Apache ou Nginx)
- **Banco de Dados** (por exemplo, MySQL ou PostgreSQL)
> **Nota:** Para facilitar a configuração do seu ambiente de desenvolvimento, recomendo utilizar um pacote que instale automaticamente todos os componentes necessários, como o XAMPP. Isso simplifica a instalação e a configuração de servidores web, banco de dados e PHP em seu sistema.

## Passo a Passo

### Instalando o Laravel

Para instalar o Laravel, você pode usar o Composer para criar um novo projeto. Abra o terminal e execute o seguinte comando:

```bash
composer create-project laravel/laravel nome-do-projeto
```
ou instale o Laravel CLI na maquina:

```bash
composer global require laravel/installer
```

e execute apenas o comando:

```bash
laravel new nome-do-projeto
```

Substitua `nome-do-projeto` pelo nome desejado para seu projeto.

### Navegando até o Diretório do Projeto

Após a instalação, vá até o diretório do seu projeto:

```bash
cd nome-do-projeto
```

### Configurando o Banco de Dados

Abra o arquivo `.env` e configure as credenciais do seu banco de dados. Exemplo de configuração para MySQL:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_do_banco
DB_USERNAME=usuario
DB_PASSWORD=senha
```

### Rodando Migrações

Se o Laravel veio com migrações, você pode aplicá-las ao seu banco de dados com o comando:

```bash
php artisan migrate
```

### Iniciando o Servidor de Desenvolvimento

Para iniciar o servidor embutido do Laravel, execute:

```bash
php artisan serve
```

O servidor estará disponível em `http://localhost:8000` por padrão.

### Acessando a Aplicação

Abra seu navegador e acesse `http://localhost:8000` para ver sua nova aplicação Laravel em funcionamento.

## Mais Informações

Para mais informações e recursos adicionais sobre o [Laravel](https://laravel.com/), visite o site oficial: Laravel. Aqui você encontrará documentação detalhada, tutoriais e uma comunidade ativa para suporte.