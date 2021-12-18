```
                     _   ___  ____ 
  _ __ _  _ ___ __ _| | | __||__  |
 | '  \ || (_-</ _` | | |__ \_ / / 
 |_|_|_\_, /__/\__, |_| |___(_)_/  
       |__/       |_|              
```

### Stack ###

L'environnement de dev se repose sur [DOCKER](https://docker.com) / [MYSQL](https://hub.docker.com/_/mysql) / [PHPMYADMIN](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) 

@autor : benoit@foujols.com \
@version : 3.0.0 

### Acces au service

Service PhpMysqlAdmin [(docker doc)](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) \
[http://localhost:8082/](http://localhost:8082/) \
Login : root \
Password : *****

---

### Installation "docker-compose" ###

---

Fonctionnement 

1. Téléchargement du projet
```
$ git clone git@github.com:bfoujols/docker-db-mysql-57.git
```
2. Creation de l'environnement docker
```
$ sudo docker-compose create
```
3. Demarrer l'environnement docker
```
$ sudo docker-compose start
```
4. Stop l'environnement docker
```
$ sudo docker-compose stop
```
5. Rebuild l'environnement docker
```
$ sudo docker-compose rm
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