```
                     _   ___  ____ 
  _ __ _  _ ___ __ _| | | __||__  |
 | '  \ || (_-</ _` | | |__ \_ / / 
 |_|_|_\_, /__/\__, |_| |___(_)_/  
       |__/       |_|              
```

### Stack ###

L'environnement de dev se repose sur [DOCKER](https://docker.com) / [MYSQL](https://hub.docker.com/_/mysql) / [PHPMYADMIN](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) / [ADMINER](https://hub.docker.com/_/adminer/) 

@autor : Benoit Foujols \
@version : 3.1.0 

### Acces au service

Service Mysql 5.7 \
mysql://127.0.0.1:3306 \
Service PhpMysqlAdmin [(docker doc)](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) \
[http://localhost:8082/](http://localhost:8082/) \
/!\* Service Adminer [(docker doc)](https://hub.docker.com/_/adminer/)  \
[http://localhost:8081/](http://localhost:8081/) \
Login : root \
Password : *****

A vous de choisir le service au moment du docker -> create (build) \
/!\* Par defaut, c'est phpmyadmin a vous de décommenter adminer pour l'activer

---

### Installation "docker-compose" ###

---

Fonctionnement 

1. Téléchargement du projet
```
$ git clone git@github.com:bfoujols/docker-db-mysql-57.git
```
2. Modifier le fichier docker-composer.yml
```
$ vim docker-composer.yml
<<<
11      MYSQL_ROOT_PASSWORD: ****
12      MYSQL_DATABASE: app_db
13      MYSQL_USER: ****
14      MYSQL_PASSWORD: ****
>>>
```
3. Creation de l'environnement docker
```
$ sudo docker-compose create
```
4. Demarrer l'environnement docker
```
$ sudo docker-compose start
```
5. Stop l'environnement docker
```
$ sudo docker-compose stop
```
6. Rebuild l'environnement docker
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
