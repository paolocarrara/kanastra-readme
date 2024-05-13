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

```
cp .env.example .env
```

## Instalando dependencias
Ainda no projeto do kanastra-backend execute o comando de instalação de dependencias:

```
composer install
```

## Docker Compose

### Pronto podemos rodar o docker-compose
Vá para o projeto kanastra-docker-compose e execute o comando:

```
docker-compose up
```

### Visualize os containers em execução:

```
docker ps
```

## Migrations

### Rodar os comando de migração:

Entre no container:
```
docker exec -it <id-do-container> bash
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

## Testar
### Pronto agora é só fazer o teste
Seria só isso se o sistema funcionasse... Ele funcionou quando executado fora do docker, quando eu comecei a passar as coisas para dentro do docker tudo começou a quebrar e infelizmente não tenho mais tempo para resolver os problemas. A idéia geral da solução do problema está contida nos códigos, qualquer dúvida ficarei a disposição para responder, é só me procurar.