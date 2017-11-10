# README docker

## Requirments

* Docker
* Docker (ie. http://docker-sync.io/) for macOS

## Update vars files

Marks: `parameters -> host: db`
Marks: `parameters -> mailer_host: mailhog`

## Start / Stop docker

On Linux/Mac/Windows

```sh
$ docker-compose up
$ docker-compose down
```

On Linux/Mac/Windows (DEV version)

```sh
$ docker-compose -f docker-compose-dev.yml -f docker-compose.yml up
$ docker-compose down
```

On macOS with (DEV version) `docker-sync`

```
$ docker-sync-stack start
$ docker-sync-stack clean
```

## Connexion

```sh
$ docker-compose exec engine bash
```

