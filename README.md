# PHP 8 Sandbox

This is a PHP 8 Sandbox for CLI things. It requires that you have installed on your system both Docker and Docker Compose.

It includes a shared volume between the current folder and the home folder of the system user inside the container, so you can edit files from your IDE on the host system and they will be reflected in the container. Vim is also installed on the container for quick edits.

## Setting Up

First clone this repository, then run:

```shell
docker-compose up -d
```

Once the container is up, you can access the system  with:

```shell
docker-compose exec app bash
```

This will give you a shell on the PHP 8 sandbox. It has Composer pre installed, and a few other PHP extensions. To include extensions and customize the image that is built, you can edit the included Dockerfile.

You can also execute scripts directly from your host system with:

```shell
docker-compose exec app php myscript.php
```

