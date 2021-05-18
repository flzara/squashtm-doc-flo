
# Les attributs d’un cas de test

Un cas de test est caractérisé par différents attributs accessibles depuis le bloc **Informations**:

!!! info "Info"
	Il est recommandé de remplir les attributs de manière homogène sur l'ensemble des projets afin d'identifier plus facilement les tests à inclure aux plans d'exécution et d'optimiser la priorisation des exécutions.  
	
## Référence

La référence du cas de test est facultative, néanmoins elle permet d'organiser son référentiel. Des conventions de nommages doivent être définies pour organiser et identifier les cas de test.

## Statut

Le champ 'Statut' permet d'affecter un statut au cas de test. Par défaut, il sera "En cours de rédaction’". Chaque statut est représenté par une couleur facilement identifiable dans la bibliothèque des cas de test grâce à la pastille qui précède la référence ou, s'il n'y a pas de référence, le libellé du cas de test.
Le statut peut être modifié à l'aide de la liste déroulante dont les valeurs sont les suivantes :

- ![En cours de rédaction](resources/en-cours-redactionFR.png)

- ![À approuver](resources/a-approuverFR.png)

- ![Approuvé](resources/approuveFR.png)

- ![Obsolète](resources/obsoleteFR.png)

- ![À mettre à jour](resources/a-mettre-a-jourFR.png)

!!! info "Info"
	Une fois validée, le cas de test peut être passé au statut **'Approuvé'**. Il est alors prêt à être intégré dans une itération pour exécution.
	<br/>Un cas de test peut être passé au statut **'Obsolète'** lorsqu'il n'est plus conforme au système testé. Ce statut permet d'archiver le cas de test dans le référentiel sans le supprimer.
	<br/>Le statut **'À mettre à jour'** est idéal pour identifier les cas de test qui nécessitent une modification suite à l'évolution du système testé.

## Importance

Le champ 'Importance' permet d'affecter un niveau d'importance au cas de test ('Faible' par défaut). La valeur peut être modifiée à l'aide de la liste déroulante dont les options sont les suivantes:

- ![Très haute](resources/importance-tres-hauteFR.png)

- ![Haute](resources/importance-haute-FR.png)

- ![Moyenne](resources/importance-moyenneFR.png)

- ![Faible](resources/importance-faibleFR.png)

!!! warning "Focus" 
	La case "Auto" au niveau de l'importance permet de déterminer automatiquement l'importance du cas de test à partir de la criticité des exigences qu'il vérifie.

L'importance du cas de test peut être utilisé pour organiser et prioriser les exécutions mais aussi pour en analyser les résultats (taux de succès/échec en fonction de l'importance des tests, importance des tests jamais exécutés).

## Nature

Le champ 'Nature' permet de définir la nature du cas de test ('Non définie' par défaut). Elle peut être modifiée à l'aide de la liste déroulante.

 ![Nature d'un cas de test](resources/natureFR.png)

Les tests de nature fonctionnels permettent de valider une fonctionnalité. 
<br/>Les tests métiers relèvent souvent de la responsabilité des clients ou des utilisateurs d'un système. Les objectifs des tests métiers sont de s'assurer que l'outil répond aux besoins exprimés.
<br/>Les tests de performances appartiennent à la famille des tests de robustesse et permettent de tester la qualité du code développé. En effet, un test de performance peut consister à vérifier les temps de réponse d'une application/module/méthode, suivant un chargement de données plus ou moins conséquent.
<br/>Les tests de sécurité portent sur des fonctions liées à la détection de menaces.
<br/>Les tests dits ATDD (Acceptance Test Driven Development) sont des tests d'acceptation qui permettent de valider le fonctionnement du système testé en fonction des attentes des utilisateurs finaux.

Le champ nature permet de classer et d'organiser le patrimoine de test. Les valeurs de ce champ sont personnalisables depuis l'administration de Squash.

## Type

La valeur du champ 'Type' permet de définir le type du cas de test ('Non défini' par défaut). Elle peut être modifiée à l'aide de la liste déroulante. 

![Type d'un cas de test](resources/typeFR.png)

Le champ type peut être utilisé pour classer et organiser le patrimoine de tests mais aussi pour identifier facilement un certain type de cas de test à ajouter à une campagne, par exemple, les tests de non-régression.
<br/>Les valeurs de ce champ sont personnalisables depuis l'administration de Squash.

!!! tip "En savoir plus"
	Pour plus d'informations sur les listes personnalisées, se référer à la page [Les listes personnalisées d'un projet](../lien-vers-page.md)

## Description

Le champ 'Description' permet de décrire l'objectif du cas de test. La description reprend les éléments à vérifier de l'exigence associée au cas de test.
<br/>La description peut débuter par "*Le cas de test vérifie que [action]*".

## Champs personnalisés

Les champs personnalisés peuvent prendre plusieurs formes (texte, case à cocher, date, tag...) et peuvent être ajoutés au niveau d'un dossier de cas de test, d'un cas de test ou d'un pas de test. Ils n'apparaîtront dans les différents blocs que s'ils ont été ajoutés dans la configuration du projet.

!!! tip "En savoir plus"
	Pour plus d'informations sur les champs personnalisés, se référer à la page [Les champs personnalisés d'un projet](../lien-vers-page.md)
