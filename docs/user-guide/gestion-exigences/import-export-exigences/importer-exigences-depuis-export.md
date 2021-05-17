
# Import d'exigences à partir d’un export

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
	   Pour compléter un fichier d'import, consulter la page "[Renseigner un fichier d'import d'exigences](Lien vers2.6.1. Renseigner un fichier d'import)" 
