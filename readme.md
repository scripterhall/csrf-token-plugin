# Spring Boot Application avec Filtre CSRF Personnalisé

Ce projet est une application Spring Boot avec un filtre CSRF personnalisé. Le projet utilise Spring Security pour gérer les configurations de sécurité, y compris la protection CSRF.

## Prérequis

Ce projet nécessite la dépendance `spring-security`. Assurez-vous de l'ajouter à votre fichier `pom.xml` ou `build.gradle` pour que le projet fonctionne correctement. Sans cette dépendance, les configurations de sécurité, y compris la protection CSRF, ne pourront pas être appliquées.

### Exigences

- **Java 8 ou supérieur**
- **Spring Boot 2.6 ou supérieur**
- **Spring Security**

## Installation

1. Clonez le dépôt :
    ```bash
    git clone <URL_DU_DÉPÔT>
    cd <NOM_DU_DOSSIER>
    ```

2. Assurez-vous que les dépendances sont installées. Dans le fichier `pom.xml`, ajoutez les dépendances nécessaires pour Spring Boot et Spring Security :

    ```xml
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>
    ```

3. Compilez et lancez l'application :
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

## Filtre CSRF Personnalisé

Ce projet implémente un filtre CSRF personnalisé pour ajouter une couche supplémentaire de sécurité aux requêtes entrantes. Le filtre vérifie la présence d'un token CSRF valide dans chaque requête.

### Classe de configuration de sécurité

La configuration de sécurité est gérée dans la classe `SecurityConfig`. Cette classe active le filtre CSRF personnalisé et intègre Spring Security pour authentifier les requêtes.

