# **MagedIn Docker Environment**
> This stack container the following services: Nginx, MySQL and PHP-FPM.

[![Build Status](https://travis-ci.org/magedin-university/docker-environment.svg?branch=master)](https://travis-ci.org/magedin-university/docker-environment)

PHP Dockerized gives you everything you need for developing PHP applications locally. The idea came from the need of having an OS-agnostic and virtualized alternative to the great [MNPP](https://github.com/jyr/MNPP) stack as regular LAMP stacks quite simply can't keep up with the Nginx + PHP-FPM/HHVM combo in terms of performance. I hope you'll find it as useful an addition to your dev-arsenal as I've found it!

## What's Inside
* [Nginx](http://nginx.org/)
* [PHP-FPM](http://php-fpm.org/)
* [Percona](https://www.percona.com/)

## Requirements
* [Docker Engine](https://docs.docker.com/installation/)
* [Docker Compose](https://docs.docker.com/compose/)
* [Docker Machine](https://docs.docker.com/machine/) (Mac and Windows only)

## Running
Set up a Docker Machine and then run in background (inside you docker path):
```sh
$ docker-compose up -d
```

## Enter container
Enter in specific container
```sh
$ docker exec -ti nginx /bin/bash
```

## Rebuild Container
Stop docker containers then rebuild them
```sh
$ docker-compose up -d --build
```

## Customizations
If you need to customize some data in docker-compose.yml, DO NOT CHANGE the file. Instead, create a new file called docker-compose-custom.yml and add your changes to it. The new file will extend default docker-compose.yml file. (See: https://docs.docker.com/compose/extends/). This way you don't need to merge docker-compose.yml when update your php-dockerized files with last updates.

----------
That's it! You can now access your configured sites via the IP address of the Docker Machine or locally if you're running a Linux flavour and using Docker natively.

## License
Copyright &copy; 2017 [MagedIn](http://magedin.com). Licensed under the terms of the [MIT license](LICENSE.md).

## Contributors

* [Tiago Sampaio](http://tiagosampaio.com)
