# Supprimer ou dissocier un objet

## Bouton [Supprimer] ![icone de suppression](resources/delete.png)

Le bouton **[Supprimer]** est à la fois disponible dans la bibliothèque et dans certaines tables.

Lors d'une sélection simple, multiple continue ou discontinue, le bouton **[Supprimer]** est actif. Lorsque la sélection comporte un élément ne pouvant être supprimé, le bouton est grisé (un projet, une exigence dont le statut n'autorise pas sa suppression par exemple). Il est également possible de supprimer une sélection en utilisant le raccourci clavier **Suppr**.

Dans la bibliothèque, la suppression d'un objet ou répertoire parent entraîne la suppression de tous les éléments qu'il contient. Par exemple, la suppression d'un dossier de cas de test entraîne la suppression des cas de test qu'il contient et la suppression d'une campagne entraîne la suppression de ses itérations et des exécutions contenues dans celles-ci.

!!! danger "Attention"
	Toute suppression est définitive et il n'existe pas de moyen de récupérer ce qui a été supprimé. D'une manière générale nous recommandons d'être vigilant quant à l'attribution des profils et habilitations aux utilisateurs et de faire des sauvegardes régulières du patrimoine (exports et/ou sauvegarde de la base de données) afin de faciliter une restauration partielle ou complète.

![Supprimer plusieurs objets](resources/suppression-fr.png)


## Bouton [Dissocier] ![icone de dissociation](resources/unlike.png)
Dans les différentes tables de Squash, il est possible de supprimer une association via le bouton présent en bout de ligne pour une dissociation simple ou via le bouton présent au dessus de la table lors d'une sélection multiple.

![Supprimer des associations](resources/dissociation-fr.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkyNTEzNzk5LDEyMjQwNzc3MCwxMjUxNT
M5MDkyLC04MzY4MjE5OTVdfQ==
-->
