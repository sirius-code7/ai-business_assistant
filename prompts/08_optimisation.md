# Évaluation et optimisation des prompts (bloc 8)

## Objectif

L'objectif de cette partie est de montrer comment l'ajout progressif de composants et de contraintes améliore la qualité d'un prompt.

Trois versions de prompt seront testées sur le même texte afin de comparer leurs résultats.

## 8.1 Prompt A : instruction simple

### Principe

Le premier prompt est volontairement minimaliste. Il contient uniquement l'instruction principale, sans contrainte particulière.

> Résume ce texte.

`L'intelligence artificielle transforme progressivement les entreprises. Elle permet d'automatiser certaines tâches, d'analyser rapidement de grandes quantités de données et d'améliorer la prise de décision. Cependant, son adoption nécessite également une formation des employés, une réflexion sur la sécurité des données et une utilisation responsable des technologies. Les entreprises doivent donc trouver un équilibre entre innovation, efficacité et respect des principes éthiques.`

## Évaluation du Prompt A

### Résultat obtenu

Le modèle a presque entièrement repris le texte original au lieu de produire un résumé véritablement synthétique.

### Analyse

- Compréhension du texte : bonne.
- Fidélité au texte : excellente.
- Concision : faible.
- Respect de la consigne : insuffisant.
- Qualité du résumé : insuffisante.

Une capture d'écran du test est conservée dans :

`assets/images/partie_7/p8_8.1_prompt_a_kimi_k3.png`

### Conclusion

Le Prompt A est trop vague. Il demande simplement de résumer le texte, sans préciser la longueur ni le niveau de synthèse attendu.

Cette absence de contraintes laisse le modèle libre de reprendre une grande partie du contenu original.git 

## 8.2 Prompt B : ajout d'une contrainte de longueur

### Principe

Le deuxième prompt ajoute une contrainte concernant la longueur du résumé. Cela permet de mieux contrôler la quantité d'informations produites.

> Résume ce texte en 150 mots maximum.

## Évaluation du Prompt B

### Résultat obtenu

Le modèle a produit un véritable résumé d'environ 135 mots.

### Analyse

- Compréhension du texte : bonne.
- Fidélité au texte : bonne.
- Concision : bonne.
- Respect de la longueur maximale : excellent.
- Qualité du résumé : bonne.

Une capture d'écran du test est conservée dans :

`assets/images/partie_7/p8_8.2_prompt_b_kimi_k3.png`

### Conclusion

L'ajout d'une contrainte de longueur améliore nettement le résultat. Le modèle comprend mieux la quantité d'informations attendue.

Cependant, certaines formulations comme « démarche globale » ou « implications humaines » vont légèrement au-delà des informations explicitement présentes dans le texte source.