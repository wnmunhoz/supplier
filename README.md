# 📘 Guia de Instalação e Configuração do Projeto PHP/Laravel

Este documento descreve as etapas necessárias para instalar, configurar e executar um projeto desenvolvido em **PHP/Laravel**.

---

## ✅ Requisitos

Antes de iniciar, verifique se seu ambiente possui as seguintes versões:

- **PHP**: 8.3.7  
- **Laravel Installer**: 5.11.0  
- **Composer**: 2.8.2  
- **Node.js**: v20.13.1  
- **NPM**: 10.8.0  
- **MySQL**: 8.0.24  

---

## 📦 Instalação das Dependências

Clone o repositório e instale as dependências do projeto:

```bash
# Dependências PHP
composer install

# Dependências Node.js + build
npm install && npm run build
```

## ⚙️ Configuração do Arquivo .env
Copie o arquivo de exemplo e gere a chave da aplicação:
```
# Criar arquivo de configuração
cp .env.example .env

# Gerar chave da aplicação
php artisan key:generate
```

## 🛠️ Configuração do Banco de Dados

Edite o arquivo .env e ajuste os parâmetros de conexão:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_do_banco
DB_USERNAME=seu_usuario
DB_PASSWORD=sua_senha
```

Execute as migrações e os seeders:
```
# Criar tabelas
php artisan migrate

# Popular tabelas
php artisan db:seed
```
## 🧪 Ambiente de Desenvolvimento

Para rodar o projeto localmente:

```
composer run dev
```
## 🧾 Testes Automatizados

```
php artisan test
```


