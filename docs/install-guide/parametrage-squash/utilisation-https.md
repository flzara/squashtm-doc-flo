# Utilisation du HTTPS

L’utilisation d’une connexion sécurisée HTTPS peut être faite par deux moyens : d’une part la mise en place d’un reverse proxy ou d’autre part via un paramétrage dans Squash. L’option recommandée par Henix est la mise en place d’un reverse proxy.

## Mandataire inverse (Reverse proxy) 

Pour utiliser une connexion HTTPS, nous préconisons d'utiliser un reverse proxy Apache HTTPD installé sur le serveur qui héberge l'application Squash-TM. Nous recommandons la branche 2.2 du serveur apache avec mod_proxy et mod_rewrite (pour forcer la connexion https) configurés.

Voici un exemple à adapter : 

    <VirtualHost *:443>
    SSLEngine on
    SSLProxyEngine on
    ServerName myhost.mydomain.com
    ErrorLog ${APACHE_LOG_DIR}/myhost_error.log
    DocumentRoot /var/www
                # Possible values include: debug, info, notice, warn, error, crit,
                # alert, emerg.
    LogLevel warn
    CustomLog ${APACHE_LOG_DIR}/myhost_access.log combined
    SSLCertificateFile    /etc/ssl/mon-certificat-serveur.crt
    SSLCertificateKeyFile /etc/ssl/private/ma-clef-privee.key

    <IfModulemod_proxy_http.c>
    ProxyPreserveHost On
    ProxyPass /squash http://localhost:8080/squash
    ProxyPassReverse /squash http://localhost:8080/squash
    </ifModule>
    </VirtualHost>

!!! info "Info"
    Si vous utilisez le connecteur Jira, il faut autoriser les flux https entre le serveur Squash et le serveur Jira.
    Il faut également enregistrer le certificat de Jira dans le truststore de la JVM de Squash-TM :

        **Ajouter ICI l'exemple à adapter**

Si certaines URL de Squash persistent en http (Espace Exigences, URL dans les API ou dans le champ description des anomalies), il faut forcer leur réecriture en suivant l'exemple ci-dessous : 

    <IfModulemod_rewrite.c>
    RewriteLog rewrite.log
    RewriteLogLevel 0
    <IfModulemod_ssl.c>
    <Location />
    RewriteEngine on
    RewriteCond %{HTTPS} !^on$ [NC]
    RewriteCond %{HTTP_HOST} (^.*)$ [NC]
    RewriteRule . https://%{HTTP_HOST}%{REQUEST_URI}  [L]
    </Location>
    </IfModule>
    </IfModule>


## Activer le https sur Squash 

Pour activer le https, il faut ajouter les informations suivantes dans le fichier ‘conf\squash.tm.cfg.properties’ :

    server.ssl.key-store=<chemin du keystore>
    server.ssl.key-store-password=<mot de passe du keystore>
    server.ssl.key-password=<mot de passe du certificat serveur>
    server.ssl.key-alias=<mot de passe>

Dans le fichier ‘bin\startup.sh’, il faut positionner la variable HTTP_PORT de la manière suivante :

    HTTP_PORT=8443

!!! warning "Focus"
    Une fois ce paramétrage effectué, l'application ne fonctionne qu'en https c’est à dire que si l'utilisateur saisit http://..., l’URL ne sera pas redirigée automatiquement.

!!! danger "Attention"
    Il faut au préalable créer un keystore.
    Pour générer/manipuler un keystore au format JKS (Java KeyStore), les commandes se trouvent [ici](http://www.lmhproductions.com/37/common-java-keytool-commands/).

## Connecter Squash à une BDD PostgreSQL en mode SSL

Pour que Squash se connecte en mode SSL à une base de données PostgreSQL, il faut ajouter la mention ?sslmode=require à la fin de la ligne DB_URL du fichier de démarrage de Squash que ce soit en installation packagée ou en tarball.

    DB_URL="jdbc:postgresql://localhost:5432/squashtm?sslmode=require"
    DB_TYPE="postgresql"
    DB_USERNAME="squash-tm"
    DB_PASSWORD="initial_pw"

**Qu'est-il si l'on souhaite faire la même chose pour MARIADB ?**