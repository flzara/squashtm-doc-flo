# Variabiliser et modulariser un cas de test classique

La variabilisation et la modularisation des cas de test classiques ont des objectifs similaires :

- Réduire la charge de création et de maintenance des cas de test
- Faciliter la lisibilité du référentiel de test en diminuant les répétitions et le nombre de cas de test

## Variabiliser un cas de test classique

Squash TM permet de variabiliser les prérequis et les pas de test d'un cas de test classique avec des paramètres et des jeux de données.

Cette fonctionnalité est particulièrement utile dans le cas où l'on souhaite tester différentes combinaisons de valeurs pour un même scénario. Au lieu de dupliquer le cas de test, il suffit de l'écrire une fois et de le variabiliser.

### Paramètres 

Pour être considéré comme tel, un paramètre doit être renseigné sous la forme : **${‘Nom_du_parametre’}** dans les prérequis ou dans les pas de test d'un cas de test.

![Paramètre dans un pas de test](resources/parametres-pas-de-test.png){class="pleinepage"}

!!! warning "Focus"
    Le nom du paramètre doit contenir exclusivement les caractères suivants: [0-9], [a-z], [A-Z] et [-,_] et ne doit comprendre aucun espace, caractère spécial ou accentué.

Les paramètres créés sont automatiquement répertoriés dans la table de l'ancre **Paramètres et jeux de données**  ![Ancre Paramètres et jeux de données](resources/param_et_jdd.png){class="icone"} et le nom de chaque paramètre est repris en en-tête de colonne.

Il est possible d'ajouter de nouveaux paramètres directement depuis cette table via le bouton **[+]** mais ils ne seront pas utilisés s'ils ne sont pas présents dans le prérequis ou les pas de test du cas de test.
Il est donc recommandé de renseigner les paramètres directement dans les prérequis ou les pas de test afin qu'ils soient automatiquement récupérés dans le bloc "Paramètres et jeux de données".

### Jeux de données

Les jeux données représentent des ensembles de valeurs qui vont remplacer les paramètres lors de l'exécution des tests.

L'ajout de jeux de données se fait depuis la table **Paramètres et jeux de données** en cliquant sur le bouton **[Ajouter un jeu de données]** et en renseignant les valeurs associées à chaque paramètre.

![Ajouter un jeu de données](resources/ajouter-jdd.png){class="centre"}

Chaque ligne de la table **Paramètres et jeux de données** représente un jeu de données.

![Table Paramètres et jeux de données](resources/parametres-pas-de-test-completes.png){class="pleinepage"}

Pendant l'exécution du cas de test, les paramètres sont remplacés par les valeurs définies dans les jeux de données.

!!! info "Info"
    Lorsque l'on intègre au Plan d’exécution (Espace Campagnes) un cas de test possédant plusieurs jeux de données, il sera ajouté autant de fois qu'il y a de jeux de données.

## Modulariser les tests avec l'appel de cas de test

L'appel de cas de test permet de mutualiser des étapes de test redondantes au sein d'un même cas de test pour ensuite l'intégrer et le réutiliser dans d'autres cas de test.

Par exemple, au lieu de répéter dans chaque test les étapes de connexion, un test comportant ces étapes est écrit une unique fois et est appelé dans tous les cas de test qui nécessite une action de connexion.

Cette fonctionnalité permet également de construire un cas de test à partir de plusieurs autres cas de test pour constituer des tests de bout-en-bout.

### Appeler un cas de test

L'appel de cas de test se fait depuis les Prérequis et Pas de test ![Prérequis et Pas de test](resources/steps.png){class="icone"} de deux manières différentes :

-	Faire un glisser-déposer depuis la bibliothèque des cas de test avant ou après n'importe quel pas de test. 
-	Cliquer sur le bouton […] en haut à droite du pas de test puis sur l’option « Appeler un cas de test ». Faire un glisser-déposer depuis le volet référentiel des cas de test à l'emplacement choisi.

Un cas de test appelé est vu comme un pas de test du cas de test appelant.

**ajouter capture avec cas de test appelé replié : idéalement, reprendre l'exemple avec le CT Connexion**

Les étapes du cas de test appelé peuvent être visulisées en cliquant sur ![Déplier appel](resources/expand-single.png){class="icone"}

!!! warning "Focus"
    Il n’est pas possible d’appeler un cas de test Gherkin ou BDD.

Les cas de tests appelants sont listés dans le bloc « Cas de test appelé par » du cas de test appelé. Cela permet d'identifier les cas de test impactés par une mise à jour du cas de test appelé.

![Cas de test appelé](resources/cas-de-tes-appeleFR.png){class="pleinepage"}

**Remplacer cette capture par un la capture d'un CT "Connexion" qui est appelé dans plusieurs CT**

!!! warning "Focus"
    Pour supprimer un cas de test appelé, il faut d'abord supprimer les pas de test correspondant dans les cas de test appelant, ce bloc permet de les retrouver facilement

Lors de l'exécution, les pas de test du cas de test appelé sont vus comme des pas de test du cas de test appelant.

**ajouter capture de la page d'exécution d'une exécution avec l'enchaînement des pas de test appelés**

### Choisir un jeu de données

Lors d'un appel de cas de test comportant des jeux de données, Squash TM permet de :

- Reprendre un des jeux de données du cas de test appelé (option *"Choisir un jeu de données parmi ceux du cas de test appelé"*). Lors de l'exécution, le paramètre est automatiquement remplacé par la valeur du jeu de données choisi.

- Définir un nouveau jeu de données dans le cas de test appelant (option *"Ne pas choisir de jeux de données parmi ceux du cas de test appelé (paramètres délégués)"*). Les paramètres issus du cas de test appelé s'affichent comme paramètres du cas de test appelant et peuvent donc être valorisés par des nouveaux jeux de données.