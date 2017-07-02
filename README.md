# 🐳 Docker Compose - nginx-php-symfony

This Docker-Compose repository initializes a Docker container system with `nginx`, `php`, `db` (MySQL) and a `pma` (phpmyadmin) container.

The intention behind this project is to have a Docker container system which helps me and you to start easily developing a Symfony project.

## Setup

### File hierarchie

- `Docker-compose.yml` - Definition of the container system.
- `.env` - Defines and configures the env variables for the container system. Has to be created from the `.env-dist` file.
- `.env-dist` - Template file for the `.env` file.
- `.data/` - Data folder for the MySQL database etc.
- `images/` - Folder for the images of the `php` and the `nginx` container.
- `logs/` - Logging folder for Nginx and Symfony.
- `symfony/` - Folder with the source code of the Symfony project.

### New project

There is not much what you have to do. Just copy the three files `Docker-compose.yml`, `.gitignore`, `.env-dist` to your project root. Create an `.env` file from the `.env-dist` and update the constants in their. After that you should register the ip addresses of the Nginx and the phpmyadmin container on your loopback devices.

For MacOS you can run the following command on your terminal (please replace x.x.x.x with the specific ip address):
```
sudo ifconfig lo0 alias x.x.x.x
```

> If you like to use a domain name/hostname to access your container, you have to register them in your `/etc/hosts` file. Normally you need sudo rights to edit this file.

### Existing project

If you have an existing project you need to put your Symfony code into a separated folder called `symfony`. (See [File hierarchie](#file-hierarchie))


# Thank you! 👏

There were a view projects/people which I like to say thank you for their work:

- [maxpou](https://github.com/maxpou) with his [docker-symfony repo](https://github.com/maxpou/docker-symfony).
- [eko](https://github.com/eko) with his [docker-symfony repo](https://github.com/eko/docker-symfony).
- Chris, a good friend and flatmate.