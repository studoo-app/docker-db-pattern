```
                     _  
  _ __ _  _ ___ __ _| | 
 | '  \ || (_-</ _` | |
 |_|_|_\_, /__/\__, |_|  
       |__/       |_|              
```

Proposition d'un environnement de dev sur [DOCKER](https://docker.com) / [MYSQL](https://hub.docker.com/_/mysql) / [PHPMYADMIN](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) / [ADMINER](https://hub.docker.com/_/adminer/) 
Vous avez la possibilité d'avoir Mysql version 5.7 / 8.0

@autor : Benoit Foujols \
@version : 3.2.0 

### Acces au service

#### Service Mysql
mysql://127.0.0.1:3306 \

#### Service d'administation d'une base de donnée
Vous avez la possibilité d'avoir 2 interface d'administration de base de donnée : \

PHPMYADMIN [(docker doc)](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) \
Lien pour d'accès : [http://localhost:8082/](http://localhost:8082/) 

/!\* ADMINER [(docker doc)](https://hub.docker.com/_/adminer/)  \
Lien pour d'accès : [http://localhost:8081/](http://localhost:8081/) \

A vous de choisir le service au moment du docker -> docker-compose create (build) \
/!\* Par defaut, c'est phpmyadmin a vous de décommenter adminer pour l'activer

---

### Installation "docker-compose" ###

---

Fonctionnement 

1. Téléchargement du projet via GITHUB 


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
