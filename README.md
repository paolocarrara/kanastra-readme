# Setup
Não é necessário fazer download deste repositório, ele é apenas um guia para executar o projeto.

## Estrutura de diretórios
Para que o projeto funcione ele precisa estar organizado da seguinte forma:

    projetos
       | - kanastra-backend
       | - kanastra-frontend
       | - kanastra-docker-compose
       | - mysql

### Criar o diretório onde serão colocados os projetos:

```
mkdir projetos
```

Entre nesse diretório e faça o clone dos três projetos:

```
git clone git@github.com:paolocarrara/kanastra-backend.git
```

```
git clone git@github.com:paolocarrara/kanastra-frontend.git
```

```
git clone git@github.com:paolocarrara/kanastra-docker-compose.git
```

### Criar o diretório onde será armazenado o banco de dados:

```
mkdir mysql
```

## Environments

### Criar o .env do projeto kanastra-backend

Criar uma cópia do arquivo .env.example e renomeá-lo para .env.


## Docker Compose

### Pronto podemos rodar o docker-compose:

```
docker-compose up
```

### Visualize os containers em execução:

```
docker ps a
```

## Migrations

### Rodar os comando de migração e link no container de backend:

Entre no container:
```
docker exec -it <id-do-container> sh
```

Rodar as migrações:
```
php artisan migrate
```

## Armazenamento de arquivos

Fazer o link do storage:
```
php artisan storage:link
```

## Frontend

### Rodar o frontend:
O frontend não foi conteinerizado, não deu tempo. Portanto, para rodar o frontend basta entrar no projeto de kanastra-frontend e seguir as instruções do README ali contido.

