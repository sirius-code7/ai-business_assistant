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

## 3.2 — Analyse d'avis clients

### Texte à analyser

- "Le personnel est très aimable, mais le temps d'attente est beaucoup trop long."
- "L'application mobile plante lorsque je valide une commande."
- "Le produit est conforme à mes attentes."
- "Le service client répond rapidement, mais mon problème n'a pas été résolu."

### Test

>Le prompt a été soumis au modèle de langage **Kimi K3**.

>Tu es un analyste spécialisé dans la satisfaction client.

>Analyse les avis clients suivants :

>- "Le personnel est très aimable, mais le temps d'attente est beaucoup trop long."
>- "L'application mobile plante lorsque je valide une commande."
>- "Le produit est conforme à mes attentes."
>- "Le service client répond rapidement, mais mon problème n'a pas été résolu."

>Contraintes :

>- Utilise uniquement les informations présentes dans les avis.
>- N'invente aucune information.
>- Regroupe les problèmes similaires.
>- Classe les problèmes par ordre d'importance.

>Présente la réponse avec les sections suivantes :

>1. Principaux problèmes
>2. Recommandations

**Réponse obtenue :**

Le modèle a identifié les principaux problèmes, proposé des recommandations et mis en évidence les points positifs à conserver.

Une capture d'écran du test est conservée dans :

`assets/images/partie_3/p3_3.2_analyse_kimi_k3.png`