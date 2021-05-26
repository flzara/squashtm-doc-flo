# Configuration générale de Squash

**Texte de présentation à écrire pour introduire la configuration générale**

## Changer le port d’accès à Squash TM

Le port par défaut du serveur est modifiable dans le fichier \bin\startup. Rechercher la ligne suivante et remplacer le port 8080 par celui souhaité :

    [...]
    set HTTP_PORT=8080 
    [...]

!!! info "Info"
    Notez que le système ne vérifiera pas si le port choisi est disponible (à moins que vous n'utilisiez le script de lancement Debian), assurez-vous donc auprès de l'administrateur que c'est bien le cas.

## Gestion du fichier de configuration Squash 

Dans le fichier de configuration de Squash TM \conf\squash.tm.cfg.properties, il est possible de configurer un certains nombre de propriétés.

Le timeout de session de Squash est configuré par défaut sur 1h. En effet, si un utilisateur connecté à Squash TM n'effectue aucune action, il est déconnecté au bout d'une heure. Pour allonger ou diminuer cette durée, modifier la propriété suivante en renseignant une valeur en secondes:

    server.servlet.session.timeout=3600


Il est possible de modifier le context path de Squash en ajoutant la propriété suivante avec le nouveau context:

    server.servlet.context-path=/test

Suite à cette modification les utilisateurs Squash TM peuvent se connecter en renseigner cette url dans leur navigateur : 

    <url-squash>/test


Le pool size de connexion à la base de données est par défaut configurer à 20. Il est possible de l'augmenter en décommentant la ligne après avoir modifié la valeur :

    spring.datasource.hikari.maximumPoolSize = 20


Le timeout de connexion au bugtracker est par défaut configuré à 15 secondes. Pour le modifier, renseigner une nouvelle valeur puis enregistrer le fichier : 

    squashtm.bugtracker.timeout=15

Les encarts d'erreur dans Squash sont par défaut caché aux utilisateurs. Pour activer l'affichage du détail des erreurs aux utilisateurs Squash TM modifier la valeur de cette propriété à 'true' :
    
    stack.trace.control.panel.visible=true
    
