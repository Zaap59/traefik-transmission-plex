# traefik-transmission-plex

## REQUIREMENTS

Edit your /etc/hosts file and add :

````shell
$ sudo vim /etc/hosts
...
127.0.0.1       traefik.local.org
127.0.0.1       plex.local.org
127.0.0.1       transmission.local.org
````

## HOW IT'S WORK

Pull the projet and move on directory:

````shell
$ cd traefik-transmission-plex/
````

Create directory for downloads content: 

```shell
$ mkdir -p downloads/{movies,tvshows}
```

Create docker network for traefik:

```shell
$ docker network create traefik
```

Launch docker-compose:

```shell
$ docker-compose up -d
```

## LOGIN / PASSWORD

### DASHBOARD TRAEFIK

Go on [traefik.local.org](http://traefik.local.org)

* Login : admin
* Password : admin_secure

### TRANSMISSION

Go on [transmission.local.org](http://transmission.local.org)

* Login : admin
* Password : admin_secure
