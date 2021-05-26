# Installation de la base de données 

**Texte pour recommander d'isntaller une BDD et introduire les deux SGBD compatibles avec Squash**

## PostgreSQL

Créer une nouvelle base de données en UTF8 pour l'application Squash TM, avec un utilisateur ayant les pleins pouvoir sur cette base.

    CREATE DATABASE squashtm WITH ENCODING='UTF8';
    CREATE USER squash-tm WITH PASSWORD 'initial_pw';
    GRANT ALL PRIVILEGES ON DATABASE squashtm TO squash-tm;

!!! warning "Focus"
    **Pour les bases de données PostgreSQL, les actions sur la base de données telles que les sauvegardes, les restaurations et les passages de scripts sont à effectuer avec l’utilisateur 'squash-tm' et non avec l’utilisateur 'postgres'. <br/>S'assurer que l'utilisateur 'squash-tm' dispose des droits superutilisateur lors du passage des scripts et des sauvegardes.**

!!! info "Info"
    La suppression de large object (comme les pièces jointes) dans PostgreSQL ne supprime pas les données (seulement le lien vers les données). 
    <br/>Pour supprimer les données, il est nécessaire d’utiliser la fonction vacuumlo (voir la documentation de PostgreSQL) pour nettoyer la base de données. 

## MariaDB et MySQL

Créer une nouvelle base de données en UTF8 pour l'application Squash TM, avec un utilisateur ayant les pleins pouvoirs sur cette base :

    CREATE DATABASE IF NOT EXISTS squashtm CHARACTER SET utf8 COLLATE utf8_bin;
    CREATE USER 'squash-tm'@'localhost' IDENTIFIED BY 'initial_pw';
    GRANT ALL ON squashtm.* TO 'squash-tm'@'localhost';
    FLUSH PRIVILEGES;

!!! danger "Attention"
    Utiliser impérativement InnoDB
    Le moteur de la base de données doit être impérativement être un moteur transactionnel. 
    Le moteur MyISAM par exemple n’est pas transactionnel et risque de corrompre vos données. Son utilisation est déconseillée et Henix ne saurait être responsable des anomalies engendrées par son utilisation.

!!! info "Info"
    Configuration de MySQL et MariaDB
    A partir de la version 5.7 de MySQL, ou pour MariaDB, la variable @@sql_mode doit contenir les tags suivants :

        NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES

    Les variables doivent être définies dans le fichier de configuration my.ini, dans la section[mysqld].


**Evoquer ici le passage du script de full-install dans le bon type de based e données**