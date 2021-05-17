# Déplacer un objet

Il est possible de déplacer une sélection d'objets au sein d'un même projet ou vers un autre projet. Pour cela :
 
 1. Effectuer une sélection simple ou multiple, continue ou discontinue via les touches **[Maj]+clic** ou **[Ctrl]+clic**
 2. Glisser/déposer la sélection vers l'emplacement de destination. Il est marqué par un indicateur visuel.

Lors d'un déplacement d'objet d'un projet à un autre : 

 - si les deux projets présentent des configurations différentes, les valeurs de tous les champs sont conservés à l'identique sauf pour les champs personnalisés, listes personnalisées et jalons
 - si les deux projets présentent la même configuration, les champs personnalisés, listes personnalisés et les jalons sont repris à l'identique
 - toutes les associations de l'objet sont conservées : liens exigence/exigence, lien exigence/cas de test, appel de cas de test, etc
 - lorsque la sélection comporte un élément ne pouvant être déplacé, il est impossible de visualiser un emplacement de destination

<br/>
![répertoire cible](resources/deplacer-cible-fr.png)
<br/>

!!! warning "Focus"
	Lorsque la bibliothèque est en ordre positionnel, la position cible du ou des éléments déplacés devient la position définitive.
