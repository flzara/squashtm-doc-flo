# La page de consultation d'une exigence

La page de consultation d'une exigence s'affiche lorsque l'exigence est sélectionnée dans la bibliothèque des exigences.

![Page de consultation d'une exigence](resources/consultation_exigence_fr.png)

La page de consultation de l'exigence est constituée :

- du nom et de la référence
- de capsules indiquant le statut, la criticité et le numéro de version de l'exigence
- des attributs de l'exigence et de ses associations dans des blocs dédiés rétractables

!!! info "Info"
	Le nom et la référence (facultative) sont déterminés lors de la création de l’exigence. Avoir une exigence avec une référence est fortement conseillé afin d'organiser son référentiel. Il est possible de modifier la référence et le nom depuis la page de consultation d'une exigence. 

L'ajout d'une nouvelle version de l'exigence ou d'une pièce jointe est possible via les boutons situés en haut à droite de la page : [Icone_attachement et La barre des ancres à gauche, permet au clic sur une ancre, d'accéder au bloc correspondant :

### ![Ancre Informations](resources/icone_information.png) Informations

Le bloc 'Informations' affiche notamment les attributs de l'exigence : 'Statut', 'Criticité', 'Catégorie' et 'Description' ainsi que ses champs personnalisés.

### ![Ancre Indicateur de couverture](resources/icone_coverage_indicators.png) Indicateur de couverture

Le bloc 'Indicateur de couverture' présente les indicateurs suivants :

- 'Taux de couverture' : indique le pourcentage de cas de test au statut 'À approuver' ou 'Approuvé', parmi tous les cas de test couvrant l'exigence ou l'une de ses descendantes.
- 'Taux de vérification' : indique le pourcentage de cas de test exécutés, en ne tenant compte que de la dernière exécution, parmi les cas de couvrant l'exigence ou l'une de ses descendantes
- 'Taux de validation' : indique le pourcentage de cas de test ayant un statut d'exécution concluant (Succès ou Arbitré), en ne tenant compte que la dernière exécution, parmi les cas de test exécutés couvrants l'exigence ou l'une de ses descendantes.

!!! tip "En savoir plus"
	Pour plus de détails, consulter la partie [Calculs des indicateurs de couverture](../suivi-couverture/calculs-indicateurs-couverture.md)


### ![Ancre cas de test verifiant cette exigence](resources/icone_linked_test_cases.png) Cas de test vérifiant cette exigence

Le bloc 'Cas de test vérifiant cette exigence' permet d'associer des cas de test à l'exigence. Une table affiche les informations des cas de test associés.

### ![Ancre Exigences lies](resources/icone_linked_requierement.png) Exigences liées

Le bloc 'Exigences liées' permet d'associer des exigences à l'exigence consultée. Une table affiche les informations des exigences liées.

### ![Ancre Historique des modifications](resources/icone_history.png) Historique des modifications

La table 'Historique des modifications' liste toutes les modifications apportées à une exigence dès lors que son statut passe de 'En cours de rédaction' à 'A approuver'.

### ![Ancre Anomalies connues](resources/icone_issues.png) Anomalies connues

La table de l'ancre 'Anomalie connues' <sup id="fnref:1"><a href="#fn:1" rel="footnote">1</a></sup> liste les anomalies déclarées lors de l’exécution des tests liés à l'exigence. La table est alimentée automatiquement et en temps réel par le bugtracker et ne peut être modifiée.
Trois liens cliquables permettent à l'utilisateur d'accéder à :

- la page de consultation de l’anomalie dans le bugtracker
- la page de consultation de l’exécution durant laquelle l’anomalie a été relevée
- la page de consultation de l’exigence

Dans le cas où il existe plusieurs versions de l’exigence, seules les anomalies associées à la version courante de l’exigence sont affichées.
Dans le cas où il existe une hiérarchie d’exigences, la table 'Anomalies connues' de l’exigence mère liste à la fois toutes les anomalies associées  à l’exigence mère et à ses descendantes.

<div class="footnotes">
<hr/>
<ol>
<li id="fn:1">
<p>Cette ancre s'affiche uniquement lorsqu'un bugtracker est associé au projet de l'exigence.<a href="#fnref:1" rev="footnote">&#8617;</a></p></li>
</ol>
</div>
