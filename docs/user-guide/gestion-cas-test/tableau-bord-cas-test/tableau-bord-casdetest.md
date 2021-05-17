
# Tableau de bord des cas de test

En sélectionnant des éléments dans la bibliothèque des cas de test, un tableau de bord s'affiche dans la partie droite. Il est possible d’afficher un tableau de bord par défaut ou un tableau de bord personnalisé.

Le bouton **[Rafraîchir]** en haut à droite permet de rafraîchir les graphiques du tableau de bord.
<br/>Le bouton **[Favori]** en haut à droite permet d’afficher un tableau de bord favori personnalisé à la place du tableau de bord par défaut

!!! tip "En savoir plus"
    Pour plus de renseignements sur le tableau de bord personnalisé, consulter la page "[Les tableaux de bord personnalisés]( 7.5. Les tableaux de bord personnalisés)"

## Les différents graphiques

Le tableau de bord se divise en 4 graphiques :

- **Graphique 'Associations aux exigences'**

Répartition des cas de test en fonction de leur association à aucune, une ou plusieurs exigences. Ce graphique est très utile pour vérifier la couverture fonctionnelle de l'application. 

- **Graphique 'Statut'**

Répartition des cas de test en fonction de leur statut de rédaction. Ce graphique permet d'avoir une vue d'ensemble de l'avancement de la rédaction des cas de test.

- **Graphique 'Importance'** 

Répartition des cas de test en fonction de leur importance. 

- **Graphique 'Pas de test'** 

Répartition des cas de test en fonction du nombre de pas de test. Ce graphique permet de visualiser rapidement si certains cas de test n'ont pas de pas de test. Pour rappel, un cas de test sans pas ne peut pas être exécutés


![Tableau de bord par défaut de l'espace Cas de test](./resources/tableaubord-CT.jpg)

!!! note "Info"
    Les cas de test Gherkin sont considérés comme n'ayant aucun de pas de test, et sont donc présents dans la portion "CT avec aucun pas de test"

## Accès à la page de recherche

Au clic sur les portions d'un graphique du tableau de bord par défaut, une page de recherche s'affiche, avec les critères présélectionnés correspondant à la portion de graphique.

**Par exemple:**
<br/><br/> Au clic sur la portion de graphique "CT avec aucun pas de test" du graphique "Pas de test", une page de recherche s'affiche avec le critère "Nombre de pas de test : Egal 0". 
<br/> En cliquant sur le bouton ![Bouton d'édition](./resources/edit1.png) ou le bouton ![Bouton dossier](./resources/dossier.png) il est possible de modifier directement le cas de test en y ajoutant des pas de test.

