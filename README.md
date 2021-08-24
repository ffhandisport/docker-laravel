# Docker Laravel

## 🛠 Build with

- Docker
  - HTTP server : Nginx
  - PHP 8 with Framework Laravel
  - Node 16
  - Database PostgreSQL 13

## 📖 Documentation

Many commands are in `Makefile` file. Example `start`, `stop`, `build` and many more. Please read 🙏 this file.

### Install Laravel

- Run this command `make laravel-install` for install Laravel with Composer
- Launch the environment with `make start`
- Modifiy environnement file `.env`
- And enjoy 😊 !

### Update and upgrade

Set application in maintenance mode or shutdown with `update` or `upgrade`, this command pull code, install latest composer dependencies,
update Laravel cache, migrate database and set application online.

`make update` or `make upgrade`

## 🧰 Development environment

This project use Docker compose, and a `Makefile` for run a development
environment.

This command build container, install composer dependencies, start environment.

`make install-dev start`

### 🛠 Development tools

#### Database management tool

Adminer equivalent to PHPmyAdmin. All credentials are in `.env` file.

`localhost:8080`

#### Mail capture

MailHog capture all mails form the application.

`localhost:8025`

## 💼 Production environment

This project use Docker compose, and a Makefile for run a production environment.

### First launch

`make install start`

## 📚 List of commands

- `build` : Build docker container
- `composer-install` : Install PHP dependencies with Composer for production
- `composer-install-dev` : Install PHP dependencies with Composer for devellopement
- `composer-update` : Update PHP dependencies
- `database-migrate` : Laravel database migration command
- `database-seed` : Laravel database seeding command
- `down` : Set in maintenance Laravel application
- `ide-helper` : Generate helpers file for IDE (PHPStorm, VS Code ...)
- `git-pull` : Reset stage and git pull
- `install` : Run `build`, `composer-install` `laravel-storage`
- `install-dev` : Run `build`, `composer-install-dev` `laravel-storage`
- `laravel-install` : Install Laravel with Composer
- `laravel-cache` : Generate all cache for Laravel
- `laravel-storage` : Create store link for Laravel
- `pull` : Pull the lastest Docker containers
- `restart` : Restart Docker containers
- `start` : Start Docker containers
- `stop` : Stop Docker containers
- `tinker` : Run Laravel Tinker
- `test` : Run Laravel unit test
- `up` : Set online Laravel application
- `update` : Run `down` `git-pull` `build` `composer-install` `laravel-cache` `database-migrate` `up`
- `update-dev` : Run `down` `git-pull` `build` `composer-install-dev` `database-migrate` `up`
- `upgrade` : Run `stop` `git-pull` `pull` `build` `composer-install` `laravel-cache` `database-migrate` `start`
- `upgrade-dev` : Run `stop` `git-pull` `pull` `build` `composer-install-dev` `database-migrate` `start`
