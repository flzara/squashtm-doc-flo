# Exporter des exigences

## Exporter des exigences depuis la bibliothèque

Squash TM permet d’exporter au format .xls une arborescence d'exigences. Cette fonctionnalité est très souvent utilisée pour la sauvegarde de données ou la [modification de données en masse](#importer-des-exigences-a-partir-dun-export).

Le nom du fichier d'export est par défaut  « export-exigences_aaaammjj_hhmmss » mais peut être modifié.

Sélectionner les éléments (projets, dossiers et/ou exigences) à exporter dans la bibliothèque (en sélection simple ou multiple) puis cliquer sur le bouton **[Exporter]**. La sélection peut porter sur des éléments de plusieurs projets. 


!!! info "Info"
	Il est possible d’exporter les champs de type "texte riche" avec leurs balises HTML (afin de conserver la mise en forme lors d’un futur import) en cochant la case « Conserver le format des textes riches ». Cette dernière peut être décochée, dans le but de faciliter la lecture des champs dans  l’export.


**Exporter des exigences avec des associations entres exigences et cas de test**

Les associations avec d'autres exigences et avec des cas de test sont également exportées et se trouvent respectivement dans les onglets "LINK_REQ_REQ" et "LINK_REQ_TC".

## Importer des exigences à partir d’un export

Squash permet d'importer un fichier précédemment exporter depuis l'outil. Cette technique est utile lorsque l'on souhaite modifier en masse des données ou faire une restauration de données.

**Pour importer un fichier d'export d'exigences, voici la marche à suivre :**

 1. Exporter la sélection souhaitée (Projets, dossiers, exigences) au format .xls
 2. Ouvrir le fichier exporté et ajouter la colonne "ACTION" dans l'onglet "REQUIREMENT". En première position dans le fichier, elle doit contenir la valeur :
	 - "C" pour créer une nouvelle exigence
	 - "U" pour mettre à jour une exigence  
 3. Apporter les modifications voulues en respectant la syntaxe pour chaque colonne
 4. Importer le nouveau fichier
 
 Pour importer les exigences dans un nouveau projet ou à un autre emplacement dans l'arborescence, la colonne "REQ_PATH" est à modifier.

!!! warning "Focus" 
	Si le libellé des objets contient le caractère '/' il faut l'échapper dans le chemin de l'exigence (dans la colonne "REQ_PATH") au moment de l'import. <br/>L’échappement est indiqué par le caractère ‘\’. 
	<br/>**Par exemple:** <br/>le nom du projet est "Projet1/Appli" et le nom de l'exigence est "Exi1/Android". La colonne "REQ_PATH" doit être renseignée ainsi : "/Projet1\/Appli/Exi1\/Android"

	
!!! tip "En savoir plus" 
	   Pour compléter un fichier d'import, consulter la page "[Renseigner un fichier d'import d'exigences](./importer-exigences.md#renseigner-un-fichier-dimport-dexigences)". 