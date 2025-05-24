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

2. Entra na pasta do projeto:

```
cd music-app
```

3. Instale as dependências via docker:

```
docker compose run --rm composer
```

4. Suba os containers com Docker:

```
docker-compose up --build -d
```

> Ao final esses comandos garantem que as dependências do projeto e os containers sejam construídos corretamente com as migrações e a aplicação disponível em localhost:8000.

> Pode ser que o endereço localhost:8000 demore um pouco para responder por que o docker pode estar construindo a aplicação ainda.

> Não é recomendado ter o composer como serviço dentro do arquivo docker-compose (mas vou entender que o usuário não necessáriamente tem o composer instalado na máquina). O ideal é abstrair isso para um Dockerfile e um entrypont.sh.

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
