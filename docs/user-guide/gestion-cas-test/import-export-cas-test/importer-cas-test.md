# Importer des cas de test


Squash permet d’importer une arborescence de cas de test depuis un fichier au format .xls ou .zip 

Pour réaliser cet import, il  faut renseigner un fichier Excel en respectant les recommandations faites dans [Renseigner un fichier d'import de cas de test](lien à mettre vers la partie) puis l'importer via l'option **[Importer]** de l'espace Cas de test. Il est possible de simuler l'import pour vérifier la cohérence du fichier d'import avant de l'importer.

!!! tip "En savoir plus"
	Pour plus de détails sur la procédure à suivre pour réaliser un import, consulter la page [Importer/Exporter un objet](lien à ajouter).

L'import permet de créer des cas de test avec toutes les fonctionnalités disponibles dans l'espace Cas de test:

## Créer une arborescence de cas de test

L'arborescence est très importante car elle permet d'**organiser le référentiel de tests**. L'import offre la possibilité de créer une arborescence précise des dossiers et cas de test à importer et ce dans plusieurs projets à la fois.

![Importer une arborescence de cas de test ](resources/import-arbo-ct-fr.png)

Si les dossiers sont inexistants dans Squash au moment de l'import, ceux-ci sont créés par l'import. 

**Par exemple :**

Pour le chemin:  /Projet1/Dossier1/Sousdossier1/Casdetest1
<br/>Le cas de test Casdetest1 est ajouté dans le projet Projet1, dans le dossier Sousdossier1, sous-dossier de Dossier1.



## Importer des cas de test avec une liste personnalisée
Si une liste personnalisée est configurée pour la nature et/ou le type des cas de test sur le projet, dans le fichier d'import, **le code de l'option** souhaitée est à renseigner dans la colonne "TC_NATURE" et/ou "TC_TYPE"

**Par exemple :**

1. Avoir une liste personnalisée avec plusieurs options, dont une des options est "Nature2" associée au code "N2".

![Page de consultation d'une liste personnalisée](resources/liste-nature-CT.jpg)

2. Dans le fichier Excel, renseigner la valeur du code de l'option dans la colonne "TC_NATURE" : ici "N2"

3. Lorsque le fichier est importé, le cas de test est créée et le champ 'Nature' est renseigné par "Nature2"

## Importer des cas de test avec des champs personnalisés

Si des champs personnalisés (CUF) sont configurés pour les cas de test du projet, dans le fichier d'import, la colonne "TC_CUF_<code du cuf\>" peut être renseignée, à raison d'une colonne par champ personnalisé. L'entête de la colonne doit comporter le code du champ personnalisé présent sur sa page de consultation.

Contenu de la colonne "TC_CUF_<code du cuf\>" :

| Type de champ personnalisé | Valeur attendue |
|--|--|
| Tag | Tag1\|Tag2 |
| Case à cocher| 'true' ou 'false' |
| Liste déroulante | Libellé de l'option |
| Numérique| Par exemple : '50', '12,8' |
| Date| 'AAAA-MM-JJ'  |
| Texte simple| Texte avec 255 caractères maximum sans mise en forme  |
| Texte riche| Pour importer de la mise en forme, le texte doit être en HTML  |

<br/>

## Importer des cas de test avec des associations à des exigences

L'onglet "LINK_REQ_TC" du fichier d'import est à compléter avec le chemin de l'exigence, le numéro de la version ainsi que le chemin du cas de test à associer. Pour que l'association fonctionne, l'exigence doit au préalable exister dans le référentiel.

Les informations sont visibles après l'import dans l'ancre **Exigences vérifiées par ce cas de test**  du cas de test.

## Importer des pas de test
L'onglet "STEPS" permet d'importer des pas de test pour un cas de test Classique. Le numéro du pas, l'action et le résultat attendu sont renseignés dans le fichier.

![Importer des pas de test pour un cas de test classique](resources/importpasdetest.png)


## Importer avec des paramètres et des jeux de données

Les onglets "PARAMETERS" et "DATASETS" permettent d'importer des paramètres et des jeux de données pour un cas de test. Il est également possible d'ajouter le paramètre directement dans le pas de test, via l'onglet "STEPS".

**Par exemple :**
<br/>Pour un cas de test de connexion à une application, il est possible d'importer les 2 paramètres "Login" et "Motdepasse", ainsi que les 3 jeux de données, correspondant à la connexion de 3 profils différents : "Admin", "Chef de projet et "Invité".

![Importer un cas de test avec des paramètres et des jeux de données (partie 1)](resources/import-param-jdd-pt1.png)
<br/>

![Importer un cas de test avec des paramètres et des jeux de données (partie 2)](resources/import-param-jdd-pt2.png)

!!! tip "En savoir plus"
	Pour en savoir plus sur le fonctionnement des paramètres et jeux de données, consulter la page [Variabiliser un cas de test classique](lien vers la page)

## Importer un cas de test faisant appel à un autre cas de test


Renseigner le cas de test appelant dans l'onglet "TEST_CASES", puis dans l'onglet "STEPS" renseigner les colonnes suivantes :

1. La colonne "TC_STEP_IS_CALL_STEP" est à valoriser par le chiffre "1" pour indiquer que ce pas de test est un appel de cas de test.
2. La colonne "TC_STEP_ACTION" est à valoriser avec les informations suivantes "CALL <chemin du cas de test appelé\>. (Par exemple : CALL /projet/dossier/ct-appelé)
3. La colonne "TC_STEP_EXPECTED_RESULT" n'est pas à renseigner.

!!! note "Info"
    Si le cas de test appelé n'est pas présent dans le référentiel de test, il doit être présent dans l'onglet "TEST_CASES" dans le fichier d'import .


!!! tip "En savoir plus"
	Pour en savoir plus sur le fonctionnement d'appel de cas de test, consulter la page [Factoriser : Appeler un cas de test tiers](lien vers la page).

## Importer un cas de test Gherkin avec un script

Pour importer un cas de test Gherkin avec son script, des colonnes spécifiques au format Gherkin sont à renseigner, dans l'onglet "TEST_CASES":

- Colonne "TC_KING" : GHERKIN
- Colonne "TC_SCRIPTING_LANGUAGE" : Le script gherkin du cas de test

![Importer un cas de test gherkin avec un script](resources/import-script-gherkin.png)

!!! warning "Focus" 
	Il n'est pas possible d'importer des cas de test BDD
