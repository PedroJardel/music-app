# 🎵 Sistema de Favoritos de Músicas - Laravel API

Este projeto é uma API desenvolvida em **Laravel 12.x** com **PHP 8.4.2**, que permite aos usuários visualizar, filtrar e favoritar músicas. Administradores têm permissões adicionais para gerenciar músicas e usuários cadastrados.

---

## 🚀 Tecnologias Utilizadas

- PHP 8.4.2
- Laravel 12.x
- PostgreSQL
- Docker
- PHPUnit (testes automatizados)

---
## 🛠️ Instalação

1. Clone o repositório:

```
git clone https://github.com/PedroJardel/music-app.git
```

2. Instale as dependências:

```
docker compose run --rm composer install
```

3. Copie o .env de exemplo o configure:

```
composer run post-root-package-install
```

4. Gere a chave da aplicação:

```
php artisan key:generate --ansi
```

5. Suba os containers com Docker:

```
docker-compose up --build -d
```

> Ao final esses comandos garantem que as dependências do projeto e os containers sejam construídos corretamente, as migrações são feitas e a aplicação esteja disponível em localhost:8000 

## 🧩 Funcionalidades

### 👥 Usuário Comum

- Acesso ao sistema via login (e-mail e senha).
- Visualizar lista de músicas com:
  - Título da música
  - Banda/Cantor
  - Data de lançamento
  - Tipo da música (Ex: Regional, Rock, Pop, Funk, Pagode, etc)
  - Quantidade de vezes que a música foi favoritada
  - Data de inserção pelo admin
- Filtrar músicas por:
  - Título
  - Banda/Cantor
  - Tipo da música
  - Data de lançamento
- Favoritar/Desfavoritar músicas
- Listar músicas favoritadas
- Editar nome e senha
- Deletar sua conta

### 🔐 Administrador

Além das funcionalidades de usuário comum, o administrador pode:

- Adicionar novas músicas
- Deletar músicas
- Visualizar e filtrar usuários por nome e e-mail
- Ver perfil detalhado de cada usuário:
  - Informações pessoais
  - Lista de músicas favoritadas
- Editar nome e senha de qualquer usuário
- Deletar usuários

---

## 🧪 Testes

Este projeto contém testes automatizados com PHPUnit. Para executá-los:

```bash
php artisan test
