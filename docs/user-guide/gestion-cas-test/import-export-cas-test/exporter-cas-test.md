
# Exporter des cas de test depuis la bibliothèque 


Squash TM permet d’exporter au format .xls ou .csv une arborescence de cas de test. Cette fonctionnalité est très souvent utilisée pour la sauvegarde de données ou la [modification de données en masse](lien vers la partie 2.7.4. Importer des cas de test à partir d'un export).

!!! note "Info"
	Si le format .csv est sélectionné pour l'export, un seul onglet est exporté contenant les attributs du cas de test et les pas de test. <br/>Les paramètres, les jeux de données et les associations avec des exigences ne sont pas exportés.

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
	Il est également possible d'exporter des [scripts Gherkin](Lien vers 3.5.6. Exporter le script d’un cas de test Gherkin) et des [scripts BDD](Lien vers : 3.6.5. Exporter le script d’un cas de test BDD)
