# Créer des cas de test à partir des exigences

Pour gagner en temps et maximiser la couverture de tests, il est possible de créer des cas de test à partir des exigences.

Pour cela, il faut :

- Sélectionner la ou les exigence(s) dans l'espace Exigences. Il est possible de sélectionner un ou plusieurs dossiers d'exigences
- Cliquer sur le bouton **[Copier]** ![Copier](resources/copy.png)
- Dans l'espace Cas de test, sélectionner l'emplacement de destination des cas de test puis cliquer sur le bouton **[Importer/Exporter]** ![Importer/Exporter](resources/import-export.png)
- Sélectionner l'option 'Ajouter des cas de test à partir des exigences sélectionnées' et choisir le format du ou des cas de test qui seront créé(s)
- Une arborescence de cas de test identique à l’arborescence d’exigences sélectionnée est créée dans le format choisi.

Le cas de test créé à partir de l'exigence reprend : 

- Le nom de l'exigence
- Sa référence
- Sa description 
- Son importance en 'auto' à partir de sa criticité

Le cas de test est automatiquement associé à cette exigence et aura par défaut le statut 'En cours de rédaction'.

!!! note "Info"
	La création de cas de test à partir d’exigences prend en compte le lien mère/filles entre exigences. Un cas de test est créé à l'identique de l'exigence mère ainsi qu'un dossier reprenant la référence et le nom de l'exigence mère contenant les cas de test issus des exigences filles.
