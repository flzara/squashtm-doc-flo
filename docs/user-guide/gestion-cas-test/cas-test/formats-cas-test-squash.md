# Les formats de cas de test dans Squash

Trois formats de cas de test sont disponibles dans Squash: Classique, BDD et Gherkin.

![Formats de cas de test](resources/format-ct-fr.png) 

Chaque format est facilement identifiable par sa couleur dans l'espace 'Cas de test'. Dans l'arbre des cas de test, les libellés apparaissent en noir pour le format Classique, en vert pour le format BDD et en bleu pour le format Gherkin.

## Cas de test Classique
Le cas de test classique permet de décrire via des pas de test, les actions à mener et leurs résultats attendus.
Il dispose d'un bloc 'Prérequis' qui recueille les préconditions du cas de test et peut être variabilisé avec des jeux de données et factorisé via des appels de cas de test.
Il est adapté aux tests manuels mais peut également être automatisé.

![Cas de test Classique](resources/format-classique-fr.png)

## Cas de test BDD
Le cas de test BDD permet de décrire un scénario en langage Gherkin via une interface simple et intuitive proposant de l'autocomplétion*. Chaque pas de test est composé d'un mot-clé (Given-When-Then) et d'une phrase d'action pouvant être réutilisée dans d'autres cas de test BDD.
Ce format est particulièrement adapté à l'automatisation. Il permet, sans qu'il n'y ait d'impact sur la rédaction du cas de test, d'exporter le script associé au format attendu par Cucumber ou Robot Framework, Squash se chargeant de faire la traduction. 

![Cas de test BDD](resources/format-bdd-fr.png)

## Cas de test Gherkin
Le cas de test Gherkin consiste en la rédaction d'un ou plusieurs scénarios Gherkin dans un éditeur de texte dédié qui propose une coloration et une vérification syntaxique, sans autocomplétion.
Ce format est adapté à l'automatisation, le script Gherkin est exporté au format Cucumber tel qu'il a été rédigé par l'utilisateur. 

![Cas de test Gherkin](resources/format-gherkin-fr.png)


\* Disponible via le plugin Bibliothèque d'actions.
