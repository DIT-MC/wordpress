# docker-wordpress-nginx

A Dockerfile that installs the latest wordpress, nginx, php-apc, php-fpm, mysql.

NB: A big thanks to [jbfink](https://github.com/jbfink/docker-wordpress) and [eugeneware](https://github.com/eugeneware/docker-wordpress-nginx)!

## Usage

To spawn a new instance of wordpress on port 80. The -p 80:80 maps the internal docker port 80 to the outside port 80 of the host machine.

```bash
$ docker run -p 80:80 -d ditmc/wordpress
```

After starting the wordpress container check to see if it started and the port mapping is correct.  This will also report the port mapping between the docker container and the host machine.

```
$ docker ps

0.0.0.0:80 -> 80/tcp
```

You can the visit the following URL in a browser on your host machine to get started. Get the IP of the docker host (docker-machine ip tutorial) and visit it in your brawser:

```
http://192.168.99.100:80
```
