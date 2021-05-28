# Exporter un cas de test

## Exporter des cas de test depuis la bibliothèque

Squash TM permet d’exporter au format .xls ou .csv une arborescence de cas de test. Cette fonctionnalité est très souvent utilisée pour la sauvegarde de données ou la [modification de données en masse](#importer-des-cas-de-test-a-partir-dun-export).

!!! info "Info"
	Si le format .csv est sélectionné pour l'export, seuls les attributs du cas de test et les pas de test sont exportés. <br/>Les paramètres, les jeux de données et les associations avec des exigences ne sont pas exportés.

Le nom du fichier d'export est par défaut  « export-cas-de-test_aaaammjj_hhmmss » mais peut être modifié.

Sélectionner les éléments (projets, dossiers et/ou cas de test) à exporter dans la bibliothèque (en sélection simple ou multiple) puis cliquer sur le bouton **[Exporter]**. La sélection peut porter sur des éléments de plusieurs projets. 

Deux options sont disponibles au moment de l'export : 

- Les cas de test appelés peuvent également être exportés même s'ils ne font pas partie de la sélection, en cochant la case "Inclure les cas de test appelés". Cependant, le droit d'export sur le projet contenant les cas de test appelés est nécessaire pour que les cas de test soient exportés.
- La mise en forme des champs de type "texte riche" avec leurs balises HTML peut être exportés en cochant la case "Conserver le format des textes riches". Cette dernière peut être décochée, dans le but de faciliter la lecture des champs dans  l’export.


**Exporter des cas de test avec des paramètres et des jeux de données**

L'ensemble des paramètres, et des jeux de données associés aux cas de test sont exportés et se trouvent respectivement dans les onglets "PARAMETERS" et "DATASETS"

**Exporter des cas de test avec des associations aux exigences**

Les associations avec les exigences sont exportées et se trouvent dans l'onglet "LINK_REQ_TC".

!!! warning "Focus"
	Lors d'un export de cas de test BDD, les pas de test ne sont pas présents dans le fichier.
	
!!! tip "En savoir plus"
	Il est également possible d'[exporter des scripts](#exporter-les-scripts-des-cas-de-test-bdd-et-gherkin) BDD et Gherkin


## Importer des cas de test à partir d’un export

Squash TM permet d'importer un fichier précédemment exporté depuis l'outil. Cette technique est utile lorsque l'on souhaite modifier en masse des données ou faire une restauration de données.

**Pour importer un fichier d'export d'exigences, voici la marche à suivre :**

 1. Exporter la sélection souhaitée (Projets, dossiers, cas de test) au format .xls
 2. Ouvrir le fichier exporté et ajouter la colonne "ACTION" dans les onglets "TEST_CASES", "STEPS", "PARAMETERS" et "DATASETS". En première position dans le fichier, elle doit contenir la valeur
	 - "C" pour créer un nouveau cas de test / pas de test / paramètres / jeux de données
	 - "U" pour mettre à jour un nouveau cas de test / pas de test / paramètres / jeux de données
 3. Apporter les modifications voulues en respectant la syntaxe pour chaque colonne
 4. Importer le nouveau fichier
 
 Pour importer les cas de test dans un nouveau projet ou à un autre emplacement dans l'arborescence, la colonne "TC_PATH" est à modifier dans chacun des onglets.

!!! warning "Focus" 
	Si le libellé des objets contient le caractère '/' il faut  l'échapper dans le chemin du cas de test (dans la colonne "TC_PATH") au moment de l'import. <br/>L’échappement est indiqué par le caractère ‘\’. 
	<br/>**Par exemple:** <br/>le nom du projet est "Projet1/Appli" et le nom du cas de test est "CT1/Android". La colonne "TC_PATH" doit être renseignée ainsi: "/Projet1\/Appli/CT1\/Android"

	
!!! tip "En savoir plus" 
	   Pour compléter un fichier d'import, consulter la page "[Renseigner un fichier d'import de cas de test](./importer-cas-test.md#renseigner-un-fichier-dimport-de-cas-de-test)" 


## Exporter les scripts des cas de test BDD et Gherkin
