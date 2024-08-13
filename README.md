Claro, aqui está uma versão mais compacta do README:

---

# Guia Rápido de Configuração do Laravel

## Requisitos

- **XAMPP**: Inclui Apache, MySQL, e PHP.
- **Composer**: Gerenciador de dependências PHP.
- **Docker Desktop**: Ferramenta para containers Docker.

## Passos de Instalação

1. **Instalar Laravel Installer**

   ```bash
   composer global require laravel/installer
   ```

2. **Criar um Novo Projeto Laravel**

   ```bash
   laravel new example-app
   ```

3. **Entrar no Diretório do Projeto**

   ```bash
   cd example-app
   ```

4. **Instalar Laravel Sail**

   ```bash
   php artisan sail:install
   ```

5. **Subir os Containers Docker**

   ```bash
   bash ./vendor/bin/sail up
   ```

Agora, sua aplicação Laravel deve estar rodando em `http://localhost`.

## Problemas Comuns

- **Comando `laravel` não encontrado**: Verifique se o diretório global do Composer está no `PATH`.
- **Erro ao iniciar o Sail**: Confirme que o Docker Desktop está em execução.

---

Esse formato mais enxuto cobre os pontos principais de maneira direta e clara.