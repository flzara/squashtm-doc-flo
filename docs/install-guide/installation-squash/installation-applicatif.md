# Installation de l'applicatif

!!! danger "Attention"
    Il est **IMPERATIF** d’installer une JRE version 8 ou 11 avant toute installation de Squash TM quel que soit l’environnement et quel que soit l’installeur.

## Installation avec le tarball Linux

Pour installer Squash TM avec le tarball Linux :

1. Décompresser l’archive .tar.gz de Squash TM dans /opt

        tar -zxvf archivexsquashtm.tar.gz

2. Créer un utilisateur et un groupe dédiés à Squash TM

        adduser --system --group --home /opt/squash-tm squash-tm

3. Définir squash-tm propriétaire de son dossier et ses fichiers

        chown -R squash-tm:squash-tm /opt/squash-tm

- Peupler la base de données grâce aux scripts présents dans : /opt/squash-tm/database-scripts 
- Rendre startup.sh executable

        chmod+x /opt/squash-tm/bin/startup.sh

- Renseigner dans le fichier bin/startup.sh les informations de connexion à la base de données

        DB_URL="jdbc:mysql://localhost:3306/squashtm" ou  "jdbc:postgresql://localhost:5432/squashtm"
        DB_TYPE="mysql" ou "postgresql"
        DB_USERNAME="squash-tm"
        DB_PASSWORD="initial_pw"

- Démarrer squash-tm via
        
        cd /opt/squash-tm/bin
        nohup ./startup.sh &

- Faire Ctrl + C pour reprendre le contrôle sur votre terminal.

## Installation du service systemd sous Debian

Pour installer Squash TM comme service systemd sous Debian :

1. Copier le fichier de service systemd qui est dans /opt/squash-tm.

        cp /opt/squash-tm/squash-tm.service /etc/systemd/system/

2. Puis recharger les services …

        systemctl daemon-reload

3. … et faites en sorte que Squash-tm démarre avec le système …

        systemctl enable squash-tm

4. … et enfin démarrer le service :
        
        systemctl start squash-tm

Il n’y a pas de fichier de service dans **squash-tm-2.0.x.RELEASE.tar.gz**. Il faut donc créer le fichier de service squash-tm.service et avec le contenu qui suit :

    [Unit]
    Description=Squash-tm daemon
    After=systemd-user-sessions.service time-sync.target

    [Service]
    WorkingDirectory=/opt/squash-tm/bin
    ExecStart=/opt/squash-tm/bin/startup.sh
    ExecStop=/bin/kill $MAINPID
    KillMode=process
    Type=simple
    User=squash-tm
    Group=squash-tm
    Restart=on-failure
    RestartSec=10
    StartLimitInterval=120
    StartLimitBurst=3

    [Install]
    WantedBy=multi-user.target

## Installation standard via le fichier zip en tant que service Windows 

Pour installer Squash TM en tant que service Windows :

1. Installer Squash TM : décompresser l’archive .zip et déplacer le contenu à l’emplacement souhaité (pour la suite on utilisera c:\<rep>). 
    - (Attention : le processus Windows associé à Squash TM doit posséder les droits de lecture et d’écriture sur l’emplacement d’installation de Squash).
2. Peupler la base de données grâce aux scripts présents dans : 

        c:\<rep>\Squash-TM\database-scripts 

3. Il faut renseigner dans le fichier startup.bat les informations de connexion à la base de données

        DB_URL="jdbc:mysql://localhost:3306/squashtm" ou  "jdbc:postgresql://localhost:5432/squashtm"
        DB_TYPE="mysql" ou "postgresql"
        DB_USERNAME="squash-tm"
        DB_PASSWORD="initial_pw"

4. Installer le service Squash TM via :

        c:\<rep>\Squash-TM\bin\squash-tm.exe install



!!! info "Info"
    L’installeur Windows est livré à des fins d’évaluation et son utilisation dans un contexte de production est déconseillée.
    Son installation étant guidée via un installeur, il ne sera pas décrit ici.
