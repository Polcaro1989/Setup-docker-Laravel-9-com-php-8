
# Setup Docker Para Projetos Laravel
<div style="display: flex; align-items: center;">
<img src="https://github.com/abraao69/abraao69/blob/main/Navy%20Blue%20Geometric%20Technology%20LinkedIn%20Banner%20(2).png" alt="Logo">
  <br><br>
</div>
<img src="https://laravelnews.s3.amazonaws.com/images/laravel9-1645586911.jpg" alt="Logo" width="1000" height="400">
### Passo a passo
Clone Repositório
```https://github.com/abraao69/Setup-docker-Laravel-9-com-php-8.git
```
```sh
cd my-project/
```


Alterne para a branch laravel 9.x
```sh
git checkout laravel-9-com-php-8
```


Remova o versionamento (opcional)
```sh
rm -rf .git/
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="Laravel-9"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acesse o container app com o bash
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```


Gere a key do projeto Laravel
```sh
php artisan key:generate
```


Acesse o projeto
[http://localhost:8989](http://localhost:8989)
