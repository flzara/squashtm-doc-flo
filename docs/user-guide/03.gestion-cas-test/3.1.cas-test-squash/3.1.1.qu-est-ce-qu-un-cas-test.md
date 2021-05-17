# Qu’est ce qu’un cas de test ?

Un cas de test est "un ensemble de valeurs d‘entrée, de pré-conditions d‘exécution, de résultats attendus et de post-conditions d‘exécution, développé pour un objectif ou une condition de test particulier, tel qu‘exécuter un chemin particulier d‘un programme ou vérifier le respect d‘une exigence spécifique" (ISTQB) <sup id="fnref:1"><a href="#fn:1" rel="footnote">1</a></sup>.

Chaque cas de test a pour objectif à minima de vérifier le résultat attendu spécifié par une exigence.

Dans Squash, un cas de test est un objet de l’Espace **Cas de test**. Il est définit par un prérequis de départ, des jeux de données à constituer, des actions à réaliser et des résultats attendus. L'exécution d'un cas de test doit permettre de vérifier, étape par étape, la conformité d'un comportement attendu d'un système testé et ainsi d'identifier d'éventuelles anomalies. 

!!! info "Info"
    Pour que la couverture de test soit optimale, il est important disposer d’une description précise du cas de test indiquant son objectif : "*Le cas de test vérifie que [action]*". Une exigence peut parfois être vérifiée par différents chemins possibles, il doit donc y avoir autant de cas de test que de scénarios identifiés.
    
<div class="footnotes">
<hr/>
<ol>
<li id="fn:1">
<p>En anglais "International Software Testing Qualifications Board", l'ISTQB est le Comité international de qualification du test logiciel.<a href="#fnref:1" rev="footnote">&#8617;</a></p></li>
</ol>
</div>
