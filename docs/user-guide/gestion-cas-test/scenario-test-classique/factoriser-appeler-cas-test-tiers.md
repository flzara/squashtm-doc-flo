# Factoriser : Appeler un cas de test tiers 

(+ choisir un jeu de données pour un cas de test appelé)

Le mécanisme d'appels de tests dans un cas de test permet la construction de bibliothèques modulaires de cas de test. Lors de l'exécution, les pas de test du cas de test appelé sont vu comme des pas de test dans le cas de test appelant.

Ce mécanisme peut également être utilisé pour des tests de bout en bout faisant appel au patrimoine de tests de différents projets.

L'appel de cas de test se fait depuis l'ancre 'Prérequis et Pas de test' ![Prérequis et Pas de test](resources/steps.png) de l'espace **Cas de test** et peut être ajouté avant ou après n’importe quel pas de test.

Il est possible d’appeler un cas de test de deux façons :
-	En le sélectionnant dans la bibliothèque des cas de test puis en faisant un glisser-déposer. 
-	En cliquant sur le bouton […] en haut à droite du pas de test puis en cliquant sur l’option « Appeler un cas de test » et en faisant un glisser-déposer.

!!! note "Info"
    Il n’est pas possible d’appeler un cas de test Gherkin ou BDD.

Les cas de tests appelants sont listés dans le bloc « Cas de test appelé par » dans l'onglet ‘Informations' du cas de test appelé.

*Exemple : 
Le Cas de test B est appelé dans le Cas de test A c'est à dire que les pas de test contenus dans le Cas de test B se retrouvent dans le Cas de test A.*

![Cas de test appelé](resources/appel-de-cas-de-testFR.png)

*Le Cas de test A (cas de test appelant) s'affiche dans le bloc "Cas de test appelé par" dans l'onglet 'Informations' du Cas de test B (cas de test appelé).*

![Cas de test appelé](resources/cas-de-tes-appeleFR.png)