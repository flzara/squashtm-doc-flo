# Associer les cas de test aux exigences

Le bloc **Exigences vérifiées par ce cas de test**, permet d’associer à chaque cas de test, une ou plusieurs exigences. Cette fonction est capitale pour établir la couverture des exigences par les cas de test.
<br/>Il existe 2 façons de réaliser cette assosciation :

## Associer des exigences à un cas de test en utilisant la bibliothèque

En cliquant sur le bouton ![Ajouter](resources/add.png){class="icone"}, il est possible, via un glisser-déposer depuis le volet 'Référentiel des Exigences' vers la page de consultation du cas de test, d'ajouter une ou plusieurs exigences dans la table 'Exigences vérifiées par ce cas de test'. 

![Associer des exigences à un cas de test](resources/associer-exigence-a-ct.png){class="pleinepage"}

## Associer des exigences à un cas de test en utilisant la recherche

Le bouton ![Rechercher](resources/browse.png){class="icone"} permet d'ajouter à la table 'Exigences vérifiées par ce cas de test' une ou plusieurs exigences via l'outil de recherche :

- Dans la partie gauche, il est possible d'ajouter des filtres et autres critères de recherche.
- Dans la partie droite, la liste des exigences correspondantes s'affiche. Il est alors possible de lier toutes les exigences recherchées via ![Tout associer](resources/link-all.png){class="icone"} ou seulement une sélection via ![Associer la sélection](resources/link-selection.png){class="icone"}.

![Recherche d'exigences](resources/recherche-exigencesFR.png){class="pleinepage"}

Une fois liée au cas de test, l'exigence et ses attributs apparaissent dans la table. Un lien cliquable sur le nom de l'exigence permet d'accéder à la page de consultation de celle-ci.

![Exigences vérifiées par le cas de test](resources/exigences-verifieesFR.png){class="pleinepage"}

L'ancre du bloc 'Exigences vérifiées par ce cas de test' se met automatiquement à jour avec le nombre d'exigences liées :  ![Exigences vérifiées par le cas de test](resources/ancre-exigences-verifiees.png){class="icone"}.

Une fois lié, le cas de test apparaît également dans la table 'Cas de test vérifiant cette exigence' des exigences associées.