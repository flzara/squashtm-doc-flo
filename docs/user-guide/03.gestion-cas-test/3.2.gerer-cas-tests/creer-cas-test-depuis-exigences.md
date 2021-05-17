# Créer des cas de test à partir des exigences

Pour gagner du temps et maximiser la couverture de test, il est possible de créer des cas de test à partir des exigences.

Pour cela, il faut dans un premier temps sélectionner la ou les exigence(s) depuis l'espace Exigences et les copier ![Copier](resources/copy.png). Puis, depuis l'espace Cas de test il faut les importer en cliquant sur le bouton [Importer/Exporter] ![Importer/Exporter](resources/import-export.png) et sélectionner l'option 'Ajouter des cas de test à partir des exigences sélectionnées'. Il est obligatoire à cette étape de sélectionner le format du ou des cas de test qui seront créé(s).

Le cas de test créé à partir de l'exigence reprend : 

- Le nom de l'exigence
- Sa référence
- Sa description 
- Son importance à partir de sa criticité

Le cas de test sera automatiquement associé à cette exigence et aura par défaut un statut 'En cours de rédaction'.

!!! note "Info"
	La création de cas de test à partir d’exigences prend en compte le lien mère/filles entre exigences. Un cas de test est créé à l'identique de l'exigence mère ainsi qu'un dossier reprenant la référence et le nom de l'exigence mère contenant les cas de test issus des exigences filles.
