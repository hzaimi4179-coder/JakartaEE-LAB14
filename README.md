# TP 14 : Conteneurisation avec Docker

##  Objectifs du TP

-   Rendre une application **Spring Boot** portable et déployable sur
    n'importe quelle machine.
-   Conteneuriser l'application avec **Docker**.
-   Déployer une base de données **MySQL** dans un conteneur.
-   Utiliser **Docker Compose** pour orchestrer l'application et la base
    de données.
  
## Étapes Réalisées

### Préparation de l'application Spring Boot

-   Création d'une application Spring Boot.
-   Configuration des dépendances (Spring Web, Spring Data JPA, MySQL
    Driver).
-   Mise en place du fichier **application.properties** pour la
    connexion MySQL.

### Création du Dockerfile

-   Construction d'une image Docker pour l'application.
-   Utilisation de `maven:3.9.6-eclipse-temurin-17` pour build.
-   Création d'une image finale basée sur `eclipse-temurin:17-jre`.
-   Copie du fichier jar dans le conteneur.

###  Mise en place de Docker Compose

Fichier `docker-compose.yml` contenant : - Un service **spring-app** -
Un service **mysql-db** - Un service **phpmyadmin** - Un réseau Docker
dédié

Commandes utilisées :

``` bash
docker-compose up -d
docker-compose logs -f
```

###  Vérification des conteneurs

-   Vérification du réseau Docker.
-   Vérification du démarrage des services :
    -   Spring Boot (logo Spring visible dans les logs)
    -   MySQL (initialisation du serveur)
    -   phpMyAdmin (accessible via navigateur)

Les captures d'écran montrent :
- Le lancement de `docker-compose up -d`
  
<img width="673" height="209" alt="tp14jee" src="https://github.com/user-attachments/assets/a3ae23b0-533c-4ed7-9a39-4411d96beb43" />

- Les logs de Spring Boot indiquant que l'application a démarré
correctement


<img width="670" height="433" alt="tp14jee2" src="https://github.com/user-attachments/assets/c98f06f9-8520-43ba-ba45-f9959a0e2823" />
