# Configuration minimale et prérequis 

## Dimensionnement minimal et recommandé

Pour l'installation et le déploiement de Squash TM, le tableau ci-dessous indique le dimensionnement minimal et celui recommandé :

|  | CPU | RAM | HDD | OS | Navigateur |
|--|--|--|--|--|--|
| Minimum (pour essai) | Mono-core | 1 Go dédié | 120 Mo | Linux, Windows, Mac | Firefox ESR, Chrome 13+ |
 Recommandé | Bi-core | 2 Go dédiés | 5 Go | Linux | Firefox ou Chrome |

L’espace disque (HDD) servira à stocker les journaux applicatifs (logs) et la base de données si cette dernière est sur le même serveur.
L’application en elle-même et ses fichiers de configuration pèsent 130Mo.


!!! warning "Focus"
    Ces éléments sont donnés à titre indicatif et ne sauraient remplacer une étude complète prenant en compte le contexte cible.

## Prérequis

Tableau des versions des intergiciels compatibles avec Squash TM : 

|  | Minimal pour environnement de production | Recommandé |
|--|--|--|
| Système d’exploitation | Tout système Linux ou Windows | Debian 10, Centos 7 |
| Java | JVM version 8 LTS | JVM version 11 |
| Base de données | Postgresql 9.6+, Mariadb 10.2 | Potgresql 11+, Mariadb 10.5 |

Précisions sur les intergiciels.

- Système d’exploitation : tout système en mesure d’exécuter une JVM.
- Mise en service/daemon de l’application : un fichier de service systemd est fourni pour les systèmes Linux compatibles et un script Windows créant le service est fourni également.
- Machine virtuelle : Une JVM Hotspot est suffisante pour exécuter Squash TM. La version 8 est compatible mais du fait de sa fin de vie proche, une version 11 est recommandée.
Squash TM fonctionne très bien avec une JDK.
OPenJ9 fonctionne avec Squash TM et consomme moins de mémoire vive, cependant la compatibilité avec certains plugins n’est pas assurée. L’usage d’une JVM OpenJ9 n’est pas supporté par Henix bien que compatible dans certains cas.
Henix utilise principalement la JVM Hotspot distribuée par Oracle.
- Serveur applicatif : 
Aucun serveur applicatif n’est nécessaire, Squash TM embarquant son propre Apache Tomcat.
SI vous souhaitez déployer Squash TM dans votre propre serveur applicatif c’est possible mais Henix ne recommande pas cette méthode.
- Base de données : 
    - Henix recommande l’usage de PostgreSQL 11. La version minimale de postgresql compatible avec Squash TM est la version 9.6 minimum.
    - Henix préconise aussi l’usage de Mariadb. Mariadb 10.1 et les versions antérieures ne sont pas compatibles avec Squash TM, c’est pourquoi il est nécessaire d’utiliser Mariadb 10.2 à minima.
    - A partir de la version 1.21 de Squash TM, MySQL n’est plus officiellement supportée. Pour les versions antérieures de Squash TM, MySQL est supportée dans les versions 5.7.17 à 5.7.x (les versions antérieures et postérieures ne sont pas ou plus supportées par l’applicatif).

!!! warning "Focus"
    Squash TM est livré avec une base embarquée (H2) utilisable à des fins d’évaluation. Nous déconseillons son utilisation dans un contexte de production.
    <br/>Consulter la page [Installation de la base de données](./installation-bdd.md) pour savoir comment utiliser une base de données autre que H2.

- Autres composants recommandés :
    - Mantis 2.x+ ou Jira 8
    - Apache HTTPD (frontal web) dans sa dernière version


## Architecture possible

Pour des faibles volumétries et un nombre contenu d’utilisateurs (moins de 50), Henix préconise une architecture « trois-tiers » telle que : sur une machine virtuelle / conteneur, on installe les trois services :

•	Application
•	SGBD
•	Frontal web

Pour un déploiement dans une infrastructure mutualisée, il est tout à fait possible d’avoir les trois services sur trois systèmes différents et de les interconnecter via le réseau.

Le mandataire inverse (reverse proxy) est facultatif mais nous recommandons son usage afin de séparer les logs d’accès des logs applicatif d’une part, et pour confier le chiffrement TLS à un autre processus/service que l’application Squash TM bien que le serveur Tomcat embarqué en soit capable.



**Questions à poser aux admins sys et aux devs:**

**Quelle type d'archi est préconnisée dans le cas d'une forte volumétrie ?**

**Nous ne mentionnons pas dans les pré-requis la possibilité de déployer via docker (voir même K8s) et donc les pré-requis de ce déploiement. Est-ce un choix volontaire ?**

**Recommandations si on installe TM avec AUTOM et DEVOPS : Modif d'isntall ? ou dimensionnement plus elevé ? ou priviligié install Docker ?**
