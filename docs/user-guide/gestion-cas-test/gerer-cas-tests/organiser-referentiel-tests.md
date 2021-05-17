# Organiser le référentiel de tests

Squash TM offre plusieurs moyens visuels et méthodologiques permettant d'organiser le référentiel et d'identifier facilement les tests et leurs attributs. 

### Les références

Une référence est un identifiant qui doit être unique. La référence facilite l'identification du cas de test:

- **Dans la bibliothèque**: les cas de test y sont triés par ordre alphanumérique de la référence puis du nom du cas de test.

- **Dans le plan d'exécution**: dans le cas de plusieurs cas de test de noms identiques, la référence permettra de les différencier.

Pour que le référentiel soit organisé de façon cohérente, il est important de définir des conditions de nommage pour les références et les noms des cas de test. 

!!! note "Info"
    La création de dossier(s) et sous-dossier(s) est également un excellent moyen d'organiser le référentiel de tests au sein d'un même projet. 
    Les dossiers peuvent aussi être triés en ajoutant une référence dans le champ du nom.

*Exemple d'utilisation des références pour les dossiers et les cas de test:*

![Exemple d'arborescence avec dossiers](resources/exemple-arbo-dossierFR.png)


### Les icônes et les pastilles

Les icônes et les pastilles permettent, depuis la bibliothèque d'avoir une vision globale sur le statut du référentiel de tests.

Dans la bibliothèque, les cas de test s’affichent dans une capsule blanche où les éléments suivants sont présents :

- 1ère position : Un arrondi coloré correspondant à l'importance du cas de test
- 2ème position : Un icône correspondant à la nature du cas de test
- 3ème position : Un icône correspondant au statut du cas de test, pas de test, exigences vérifiées. 
    - La couleur de la pastille représente le statut du cas de test.
    - Une pastille "vide" ![Pastille !](resources/pastille-videFR.png) signifie qu'aucun pas de test n'est rattaché au cas de test. À l'inverse, une pastille "pleine" ![Les icônes et les pastilles des cas de test](resources/pastille-pleineFR.png) signifie qu'au moins un pas de test est rattaché au cas de test.
    - Une coche s'affiche dans la pastille ![Les icônes et les pastilles des cas de test](resources/pastille-cocheFR.png) lorsqu'au moins une exigence est reliée au cas de test.

Au survol, une infobulle détaille chaque élément.

*Exemple:* 

![Les icônes et les pastilles des cas de test](resources/icone-pastille-cas-de-testFR.png)

- *Le cas de test "CT002 - Fonctionnel" a une importance "Moyenne", est de nature "Fonctionnel", contient des pas de test et est lié à une exigence.*
- *Le cas de test "CT005-Non fonctionnel" a une importance "Haute", est de nature "Non fonctionnel", contient des pas de test mais n'est pas lié à une exigence.*
- *Le cas de test "CT007-Sécurité" a une importance "Moyenne", est de nature "Sécurité" et ne contient pas de pas de test.*


!!! note "Info"
    Pour les cas de test Gerkhin, les pastilles apparaissent toujours pleines car le script est pré-rempli avec la balise de langue et le titre du feature

### Les couleurs

Chaque format de cas de test est représenté par une couleur de police spécifique visible dans la bibliothèque de l'espace Cas de test permettant leur identification rapide:

- Cas de test Classique en noir
- Cas de test Gherkin en bleu
- Cas de test BDD en vert 

![Formats Cas de test](resources/couleurs-cas-de-testFR.png)


### Les capsules

Les capsules sont visibles sur la page de consultation d'un cas de test, sous la référence. Elles indiquent:

- le statut du cas de test
- l'importance
- le statut de la dernière exécution

![Capsules](resources/capsulesFR.png)




