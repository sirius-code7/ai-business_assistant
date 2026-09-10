# Prompt Engineering et raisonnement [bloc 3]

## Objectif

L'objectif de cette partie est de comprendre comment améliorer la fiabilité des réponses d'un modèle de langage en utilisant une approche de raisonnement et de vérification.

---

## 3.1 Décomposition d'un prompt

### Prompt proposé

> Analyse ces avis clients et donne-moi les problèmes les plus importants ainsi que les recommandations.

### Décomposition

| Composante | Contenu |
|------------|----------|
| Rôle | Non précisé |
| Contexte | Des avis clients doivent être analysés. |
| Tâche | Identifier les principaux problèmes et proposer des recommandations. |
| Contraintes | Aucune contrainte n'est indiquée. |
| Format de sortie | Non précisé. |

### Observation

Ce prompt est compréhensible mais reste assez général. L'absence d'un rôle, de contraintes et d'un format de sortie peut conduire à des réponses variables selon le modèle utilisé.