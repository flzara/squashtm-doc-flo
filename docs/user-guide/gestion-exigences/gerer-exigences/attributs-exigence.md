# Les attributs d’une exigence

Une exigence est caractérisée par différents attributs accessibles sur la page de consultation de l'exigence, en particulier depuis le bloc **Informations**.

## Référence
La référence d'une exigence est facultative, néanmoins elle permet d'organiser son référentiel. Des conventions de nommages doivent être définies pour organiser et identifier les exigences.

## N° version
Le numéro de version de l'exigence (nombre entier positif), positionné automatiquement par le système, est un lien cliquable qui permet d’accéder à la page de 'Gestion des versions de l'exigence', sur laquelle la liste de versions est disponible.

##  Statut

Le champ 'Statut' permet d'affecter un statut à l’exigence (‘En cours de rédaction’ par défaut). Le statut peut-être modifié à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- ![Pastille En cours de rédaction](resources/pastille-redaction-en-cours.png) En cours de rédaction 
- ![Pastille À approuver](resources/pastille-approuver-a.png) À approuver  
- ![Pastille Approuvée](resources/pastille-approuvee.png) Approuvée
- ![Pastille Obsolète](resources/pastille-obsolete.png) Obsolète

!!! note "Info"
    Une fois validée, une exigence pourra être passée au statut **'Approuvée'**, elle sest alors prête à être associée à un ou plusieurs cas de test. 
    <br/>Une exigence pourra être passée au statut **'Obsolète'**, lorsqu'elle sera considérée comme non utile pour le référentiel d'exigence sans pour autant être supprimée.
    <br/>L'édition des attributs d'une exigence ayant l'un de ces 2 statuts est impossible. Il conviendra de repasser au statut **'A approuver'** pour éditer un attribut.

##  Criticité
Le champ 'Criticité' permet d'affecter une criticité à une exigence ('Mineure' par défaut). La criticité peut-être modifiée à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- [Icone ] Critique
- [Icone ] Majeure
- [Icone ] Mineure
- [Icone ] Non définie

!!! note "Info"
    Par exemple, la valeur 'Critique' pourra être sélectionnée dans le champ 'Criticité' d'une exigence qui traduit les spécifications d'une fonctionnalité/sous-fonctionnalité critique d'une application à tester.

##  Catégorie
Le champ 'Catégorie' permet d'affecter une catégorie à une exigence (‘Non définie’ par défaut). La catégorie peut-être modifiée à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- Cas d’utilisation
- Ergonomique
- Exigence de test
- Fonctionnelle
- Métier
- Non définie
- Non fonctionnelle
- Performance
- Sécurité
- Technique
- User story

!!! note "Info"
    Par exemple, la valeur 'Technique' pourra être sélectionnée dans le champ 'Catégorie' d'une exigence qui traduit les spécifications d'une fonctionnalité/sous-fonctionnalité technique d'une application à tester. 'Fonctionnelle' pourra être sélectionné pour une exigence relevant de la partie fonctionnelle de l'application à tester.

Les valeurs de ce champ sont personnalisables depuis l'administration de Squash à l'aide d'une liste personnalisée.

!!! tip "En savoir plus"
	Pour plus d'informations sur les listes personnalisées, se référer à la page [Les listes personnalisées d'un projet](../lien-vers-page.md)

## Jalons

Lorsque l'utilisation des jalons est activée, le champ 'Jalons' permet d'associer l'exigence à un ou plusieurs jalons via le bouton [Ajouter] ![Bouton ajouter jalon](resources/icone-add.png). L'association a un ou plusieurs jalons permettra notamment d'organiser son référentiel d'exigence.

##  Description
Le champ 'Description' permet de décrire l'exigence. La description peut-être complétée en détaillant le comportement attendu.
Elle peut être rédigé sous la forme : "L'application doit permettre de [action]".

## ID exigence et Id version
Les numéros d'identifiant prennent pour valeur un entier strictement positif déterminé automatiquement par le système. Le premier est le numéro d'identifiant de l'exigence. Une même exigence pouvant exister sous différentes versions, le second identifiant est le numéro d'identifiant de la version d'exigence.
<br/>Les 2 champs ne sont pas éditables. 

## Création et Modification
Le champ 'Création' affiche la date de création avec le login de l'utilisateur qui a créé l'exigence.
<br/>Le champ 'Modification' affiche la date de dernière modification avec le login du dernier utilisateur a avoir modifié l'exigence.
<br/>Les 2 champs ne sont pas éditables.

## Champs personnalisés
Les champs personnalisés peuvent prendre plusieurs formes (texte simple ou riche, case à cocher, liste déroulante, date, tag ou numérique) et peuvent être ajoutés au niveau d'un dossier d'exigences ou d'une exigence. Sur la page de consultation d'une exigence, ils apparaîtront sous le champ 'Jalons' du bloc 'Informations'.

!!! tip "En savoir plus"
	Pour plus d'informations sur les champs personnalisés, se référer à la page [Les champs personnalisés d'un projet](../lien-vers-page.md)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk5NDQyNDg3LDg1NTMyMDIwNCwtODQwOD
M4Nzk3LC0xMjcyOTIzMjcxLC0xMDM5MTI2MzQsMTM0MDcxOTAy
LC05MTk1NTIyMzJdfQ==
-->
