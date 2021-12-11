```
                     _   ___  ____ 
  _ __ _  _ ___ __ _| | | __||__  |
 | '  \ || (_-</ _` | | |__ \_ / / 
 |_|_|_\_, /__/\__, |_| |___(_)_/  
       |__/       |_|              
```

### Stack ###

L'environnement de dev se repose sur [DOCKER](https://docker.com)


### Acces au service

Service PhpMysqlAdmin
[http://localhost:8082/](http://localhost:8082/)
Login : root
Password : *****

---

### Installation "docker-compose" ###

---

Fonctionnement 

1. Téléchargement du projet

```
$ git clone git@github.com:bfoujols/docker-db-mysql-57.git
$ sudo docker-compose create
$ sudo docker-compose start
$ sudo docker-compose stop
```

---

#### Autres commandes ####

Voir les processus
```
$ sudo docker ps -a
```

Killer un processus 
```
$ sudo docker kill -f f9fa1f1c0d29
```

Voir les images 
```
$ sudo docker ps -a
```

Supprimer un conteneur 
```
$ sudo docker rm -f 1a7a672f0fbd
```

Supprimer une image 
```
$ sudo docker rmi -f 1a7a672f0fbd
```

Entrée en shell : 
```
$ docker exec -it 04d713497315 /bin/bash
```
---