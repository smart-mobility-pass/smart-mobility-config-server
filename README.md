# Spring Cloud Config Server

Ce projet est le serveur de configuration centralisé (Config Server) pour l'architecture microservices du projet **Smart Mobility**. Il utilise **Spring Cloud Config** pour fournir une configuration externe à tous les autres microservices.

## Caractéristiques

- **Nom de l'application :** `spring-cloud-config-server`
- **Port d'exécution :** `8888`
- **Version de Java :** 17
- **Version de Spring Cloud :** 2025.1.0

## Dépôt de Configuration (Git)

Le serveur récupère les fichiers de configuration des autres microservices à partir du dépôt Git suivant :

- **URI du dépôt Git :** `https://github.com/smart-mobility-pass/smart-mobility-configuration.git`
- **Branche par défaut :** `main`

## Prérequis

- **Java 17** ou supérieur
- **Maven** pour la compilation et l'exécution

## Comment lancer le projet ?

Vous pouvez compiler et lancer ce microservice en utilisant Maven :

```bash
./mvnw spring-boot:run
```

Sous Windows, utilisez :
```cmd
mvnw.cmd spring-boot:run
```

Une fois démarré, le serveur de configuration sera accessible à l'adresse : `http://localhost:8888`.

## Tester le serveur

Vous pouvez vérifier que le serveur retourne bien la configuration d'un microservice spécifique (par exemple, un service nommé `mon-service` avec le profil `dev` sur la branche `main`) en accédant à :

```text
http://localhost:8888/mon-service/dev/main
```
