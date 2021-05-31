# A propos de Squash

## La suite Squash

La suite Squash (Software QUality ASsurance enHancement) est un projet Open Source initié par HENIX en 2010, qui a pour objet la structuration et l'industrialisation des tests fonctionnels.

La structure de l'application Squash en différents espaces permet alors de créer, organiser et versionner un patrimoine d'exigences; créer, gérer factoriser et variabiliser un référentiel de tests; gérer, planifier et exécuter des campagnes de tests et piloter l'activité de recette.

Squash, de part sa capacité à s'interfacer avec des applications tierces, permet le travail en "cycle en V" ou en Agile.

Squash est un outil multi-projets : une fois connecté, l'utilisateur accède à l'ensemble du patrimoine des projets sur lequel est il est habilité.

## Terminologie

Présentation des notions et concepts abordés dans cette documentation :

|Notion|Définition métier
|--|--|
|Exigence|Extraites des documents de conception et des règles de gestion dont elles découlent, les exigences décrivent les comportements attendus de l’application.
|Cas de test|Chemin fonctionnel à mettre en œuvre pour vérifier la conformité d’une fonctionnalité. Le cas de test se définit par le jeu de données à constituer, le scénario de test à exécuter et les résultats attendus.
|Pas de test|Étape du chemin fonctionnel mis en place dans le cadre d'un cas de test. Chaque pas de test permet de vérifier un résultat attendu.
|Campagne|Établie de manière à vérifier un nombre fini de fonctionnalités, une campagne de tests compte plusieurs étapes : <br/>- définition des objectifs de test (choix des cas de test et des jeux de tests rattachés)<br/>- détermination du nombre d'itérations et de leur contenu en fonction des objectifs de test <br/>- exécution des tests<br/>- identification, analyse et suivi d’anomalies <br/>- exploitation des résultats <br/>- conclusion sur le comportement des fonctionnalités vérifiées.
|Itération|Sélection de cas de tests exécutés de manière successive dans le cadre d'une campagne de test. Chaque itération est un cycle de la campagne qui est définie par un laps de temps entre deux livraisons de développements.
|Suite de tests |Manière d’organiser les cas de test, de les regrouper afin de créer une image d'une partie du plan de test d'une itération. Fonctionnalité permettant d’enchaîner l’exécution des cas de test.
|Plan d'exécution |Table permettant l’organisation et le pilotage des tests de la campagne. Vision proposant différentes informations sur les cas de test comme leur mode d'exécution (automatique ou manuel), leur importance, leur statut, ou encore l’utilisateur assigné à leur exécution.
|Exécution|Il s’agit de la phase de déroulement des cas de test sur le système testé. C'est lors de cette phase que sont identifiés et tracés les anomalies rencontrées.

## Documentation de l'outil Squash

- [Guide d'installation](install-guide/installation-squash/config-mini-prerequis.md)
- [Guide administrateur](admin-guide/presentation-generale/presentation-administration-squash.md)
- [Guide Utilisateur](user-guide/presentation-generale/espaces-squash.md)

## Documentation des plugins Squash

- [Guide LDAP/AD](plugin-guides/ad-ldap-guide/index.md)
- [Guide SAML](plugin-guides/saml-guide/index.md)
- [Guide Bibliothèque d'actions](plugin-guides/action-word-guide/index.md)
- [Guide Assistant Campagne](plugin-guides/campaign-wizard-guide/index.md)
- [Guide Xsquash](plugin-guides/xsquash-guide/index.md)
- [Guide Jira Exigences](plugin-guides/jira-req-guide/index.md)
- [Guide Redmine Exigences](plugin-guides/redmine-req-guide/index.md)
- [Guide Polarion Exigences](plugin-guides/polarion-guide/index.md)
- [Guide Workflow Automatisation Jira](plugin-guides/waj-guide/index.md)
