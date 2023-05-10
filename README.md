<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://github.com/ehsanSepahi/toDo/assets/71543126/fd20f62f-50dc-47aa-9f0a-c55740d5142a" width="150" alt="Laravel Logo"></a></p>

<!-- <p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://github.com/ehsanSepahi/toDo/assets/71543126/cee10d3e-41d0-42fd-ae15-8a0c77d24b54" width="20" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p> -->


# Getting started

## Installation

Please check the official laravel installation guide for server requirements before you start. [Official Documentation](https://laravel.com/docs/5.4/installation#installation)

Alternative installation is possible without local dependencies relying on [Docker](#docker). 

Clone the repository

    git clone git@github.com:ehsanSepahi/chirp.git

Switch to the repo folder

    cd chirp

Install all the dependencies using composer

    composer install

Copy the example env file and make the required configuration changes in the .env file

    cp .env.example .env

Generate a new application key

    php artisan key:generate
    
Install node.js

    npm install
    
Build script

    npm run build 

Edit env file

    nano .env

Run the database migrations (**Set the database connection in .env before migrating**)

    php artisan migrate

Start the local development server

    php artisan serve

You can now access the server at http://localhost:8000

**TL;DR command list**

    git clone git@github.com:ehsanSepahi/chirp.git
    cd chirp
    composer install
    cp .env.example .env
    php artisan key:generate
    npm install
    npm run build
    nano .env
    
**Make sure you set the correct database connection information before running the migrations** [Environment variables](#environment-variables)

    php artisan migrate
    php artisan serve
    
    
## Docker

To install with [Docker](https://www.docker.com), run following commands:

```
git clone git@github.com:ehsanSepahi/chirp.git
cd chirp
cp .env.example.docker .env
docker run -v $(pwd):/app composer install
cd ./docker
docker-compose up -d
docker-compose exec php php artisan key:generate
docker-compose exec php php artisan migrate
docker-compose exec php php artisan serve --host=0.0.0.0
```

The chirp can be accessed at [http://localhost:8000](http://localhost:8000).

## chirp Specification

In this guide we will walk through building a modern Laravel application from scratch. 
You can login into system and make a chirp

----------

## Folders

- `app` - Contains all the Eloquent models
- `config` - Contains all the application configuration files
- `database/migrations` - Contains all the database migrations
- `routes` - Contains all the api routes defined in api.php file
- `tests` - Contains all the application tests

## Environment variables

- `.env` - Environment variables can be set in this file

***Note*** : You can quickly set the database information and other variables in this file and have the application fully working.

----------

# Testing

Run the laravel development server

    php artisan serve

The api can now be accessed at

    http://localhost:8000
