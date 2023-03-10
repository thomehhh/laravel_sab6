# Development container

Standard containers with Apache, PHP v8.1, Laravel v8.83.15, Vue 2, MongoDb, MySQL and PostgreSQL.

| App  | Name  | Port  |
|---|---|---|
|  MongoDb  | mongo | 27019 |
|  MongoExpress | mexpress | 8091 |
|  MariaDB 10.2 (~MySql 5.7) | mydb | 3309 |
|  PhpMyAdmin | myadmin | 8089 |
|  PgDb | pgdb | 5439 |
|  PgAdmin | pgadm | 5059 |

# Getting started

## Configuration file

cp docker-compose.example.yaml docker-compose.yaml

## Run containers

docker compose up -d --build

### Check if they are running

docker ps

### Install Laravel dependencies

docker exec -it lara bash
composer install

### Install node dependencies inside Laravel container

npm install
npm run dev

### Set Laravel environment variables

cp .env.example .env
php artisan key:generate

### Create database schema and populate with data

php artisan migrate
php artisan db:seed

### User and permission settings

chmod -R 777 storage

After creating files with artisan, run the following command to avoid permission issues

chown -R www-data:1000 .

## Vue app

<https://www.positronx.io/create-laravel-vue-js-crud-single-page-application/>

## React

<https://techvblogs.com/blog/build-crud-app-with-laravel-and-reactjs>

https://blog.codeexpertslearning.com.br/dockerizando-uma-aplica%C3%A7%C3%A3o-react-js-f6a22e93bc5d
https://stackoverflow.com/questions/987142/make-gitignore-ignore-everything-except-a-few-files

# MacOS

# Changelog

Setting up SSH keys

# WSL

## Setting up environment

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

wsl --set-default-version 2

Choose your Linux distro from Windows Store

https://github.com/codeedu/wsl2-docker-quickstart
https://www.youtube.com/watch?v=rdp7xwziQtU
https://github.com/argentinaluiz/my-vscode-settings
https://github.com/argentinaluiz/ambiente-dev-produtivo


## Troubleshooting

https://pureinfotech.com/uninstall-wsl2-windows-10/

## Tested by me 29121648