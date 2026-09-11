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