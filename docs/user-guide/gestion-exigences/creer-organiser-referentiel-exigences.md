# Créer et Organiser le référentiel d’exigences

## Créer une exigence 

La création d'une exigence se fait depuis l'espace Exigences via la popup 'Ajouter une exigence' :

![Ajouter une exigence](resources/ajouter-exigence-s-fr.png)

Il est possible de créer une exigence à la racine d'un projet, dans un dossier ou sous une exigence.

Lors de la création, il est obligatoire de renseigner, à minima, une valeur pour le champ 'Nom'. 

Il est recommandé de renseigner une référence et une description à l'exigence même si ces champs sont facultatifs. 
<br> En l'absence de sélection dans les champs 'Criticité' et 'Catégorie' la valeur par défaut sera appliquée.

Si des champs personnalisés obligatoires sont associés à l'entité Exigences, ils apparaissent également dans la popup.

## Les attributs d’une exigence 

Une exigence est caractérisée par différents attributs accessibles sur la page de consultation de l'exigence, en particulier depuis le bloc **Informations**.

### Référence
La référence d'une exigence est facultative, néanmoins elle permet d'organiser son référentiel. Des conventions de nommages doivent être définies pour organiser et identifier les exigences.

### N° version
Le numéro de version de l'exigence (nombre entier positif), positionné automatiquement par le système, est un lien cliquable qui permet d’accéder à la page de 'Gestion des versions de l'exigence', sur laquelle la liste des versions de l'exigence est disponible.

###  Statut

Le champ 'Statut' permet d'affecter un statut à une exigence (‘En cours de rédaction’ par défaut). Le statut peut-être modifié à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- ![Pastille En cours de rédaction](resources/pastille-redaction-en-cours.png) En cours de rédaction 
- ![Pastille À approuver](resources/pastille-approuver-a.png) À approuver  
- ![Pastille Approuvée](resources/pastille-approuvee.png) Approuvée
- ![Pastille Obsolète](resources/pastille-obsolete.png) Obsolète

###  Criticité
Le champ 'Criticité' permet d'affecter une criticité à une exigence ('Mineure' par défaut). La criticité peut-être modifiée à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- ![Icone Critique](resources/icone-critique.png) Critique
- ![Icone Majeure](resources/icone-majeure.png) Majeure
- ![Icone Majeure](resources/icone-mineure.png) Mineure
- ![Icone Non définie](resources/icone-non-definie.png) Non définie

!!! info "Info"
    Par exemple, la valeur 'Critique' pourra être sélectionnée dans le champ 'Criticité' d'une exigence qui traduit les spécifications d'une fonctionnalité/sous-fonctionnalité critique d'une application à tester.

###  Catégorie
Le champ 'Catégorie' permet d'affecter une catégorie à une exigence (‘Non définie’ par défaut). La catégorie peut-être modifiée à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- Fonctionnelle
- Non fonctionnelle
- Cas d’utilisation
- Métier
- Exigence de test
- Non définie
- Ergonomique
- Performance
- Technique
- User story
- Sécurité

!!! info "Info"
    Par exemple, la valeur 'Technique' pourra être sélectionnée dans le champ 'Catégorie' d'une exigence qui traduit les spécifications d'une fonctionnalité/sous-fonctionnalité technique d'une application à tester. 'Fonctionnelle' pourra être sélectionné pour une exigence relevant de la partie fonctionnelle de l'application à tester.

Les valeurs de ce champ sont personnalisables depuis l'administration de Squash à l'aide d'une liste personnalisée.

!!! tip "En savoir plus"
	Pour plus d'informations sur les listes personnalisées, se référer à la page [Les listes personnalisées d'un projet](../../admin-guide/gestion-projets/configurer-projet.md#les-listes-personnalisees) du guide administrateur.

### Jalons

Lorsque l'utilisation des jalons est activée, le champ 'Jalons' permet d'associer l'exigence à un ou plusieurs jalons via le bouton **[Ajouter]** ![Bouton ajouter jalon](resources/icone-add.png). L'association a un ou plusieurs jalons permettra notamment d'organiser le référentiel d'exigences.

###  Description
Le champ 'Description' permet de décrire l'exigence. La description peut-être complétée en détaillant le comportement attendu.
Elle peut être rédigée sous la forme : "L'application doit permettre de [action]".

### ID exigence et Id version
Les numéros d'identifiant technique prennent pour valeur un entier strictement positif déterminé automatiquement par le système. Le premier est le numéro d'identifiant technique de l'exigence. Une même exigence pouvant exister sous différentes versions, le second identifiant est le numéro d'identifiant technique de la version d'exigence.
<br/>Les 2 champs ne sont pas éditables. 

### Création et Modification
Le champ 'Création' affiche automatiquement la date de création avec le login de l'utilisateur qui a créé l'exigence.
<br/>Le champ 'Modification' affiche automatiquement la date de dernière modification avec le login du dernier utilisateur a avoir modifié l'exigence.
<br/>Les 2 champs ne sont pas éditables.

### Champs personnalisés
Les champs personnalisés peuvent prendre plusieurs formes (texte simple ou riche, case à cocher, liste déroulante, date, tag ou numérique) et peuvent être ajoutés au niveau de l'entité 'Exigence'. Une fois paramétré, sur la page de consultation d'une exigence, ils apparaissent sous le champ 'Jalons' du bloc **Informations**.

!!! tip "En savoir plus"
	Pour plus d'informations sur les champs personnalisés, se référer à la page [Les champs personnalisés d'un projet](../../admin-guide/gestion-projets/configurer-projet.md#les-champs-personnalises) du guide administrateur.


## Workflow exigence 

Le workflow d'attribution du statut d'une exigence conseillé est le suivant : 

1. Le statut **'En cours de rédaction'** est le statut par défaut d'une exigence
2. Une fois rédigée, une exigence est passée au statut **'À approuver'**
3. Le statut **'Approuvée'** est attibué à l'exigence après validation, elle est alors prête à être associée à un ou plusieurs cas de test 

Une exigence peut être passée au statut **'Obsolète'**, lorsqu'elle est considérée comme non utile pour le référentiel d'exigences sans pour autant être supprimée.

!!! danger "Attention"
    L'édition des attributs d'une exigence ayant les statuts **'Approuvée'** ou '**'Obsolète'**' est impossible. Il convient de repasser au statut **'A approuver'** pour éditer les attributs.

## Historique des modifications

La table 'Historique des modifications' d'une exigence liste toutes les modifications apportées à une exigence dès lors que son statut passe de 'En cours de rédaction' à 'À approuver'.

Par exemple, la modification de la référence d'une exigence au statut 'À approuver', apparait dans cette table avec la référence d'origine, et la nouvelle référence ainsi que la date, heure et login du modificateur.

## Organisation du référentiel d’exigences

A faire

## Hiérarchie d’exigences

A faire

## Liens entre exigences

A faire
