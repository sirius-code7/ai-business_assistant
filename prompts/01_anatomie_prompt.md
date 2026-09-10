# Anatomie d'un prompt [bloc 1]

## Objectif

L'objectif de cette partie est de comprendre les différentes composantes d'un prompt afin de construire une demande claire, précise et efficace destinée à un modèle de langage (LLM).

Avant de rédiger un prompt complet, il est important d'identifier les informations essentielles que le modèle doit recevoir pour produire une réponse pertinente.

---

## 1.1 Les composantes d'un prompt

Pour obtenir une réponse de qualité, un prompt doit généralement contenir les éléments suivants :

- **Le rôle** : indique au modèle le rôle qu'il doit adopter.
- **Le contexte** : décrit la situation ou le problème.
- **La tâche** : précise ce que le modèle doit réaliser.
- **Les contraintes** : définissent les règles à respecter.
- **Le format de sortie** : indique la forme attendue de la réponse.

### Exemple

| Composante | Exemple |
|------------|---------|
| Rôle | Tu es un analyste de la satisfaction client. |
| Contexte | Une entreprise souhaite analyser les retours de ses clients. |
| Tâche | Identifier les principaux points positifs et négatifs. |
| Contraintes | Ne pas inventer d'informations et justifier les observations par le texte fourni. |
| Format | Réponse organisée sous forme de liste à puces. |

---

## 1.2 Construction d'un prompt

Après avoir identifié les différentes composantes d'un prompt, il est possible de les assembler afin de produire une demande claire, précise et exploitable par un modèle de langage.

### Prompt proposé

Rôle :
Tu es un analyste spécialisé dans la satisfaction client.

Contexte :
Une entreprise souhaite analyser les retours de ses clients afin d'améliorer la qualité de ses services.

Tâche :
Analyse les commentaires fournis et identifie :
- les principaux points positifs ;
- les principaux points négatifs ;
- les problèmes récurrents ;
- les recommandations d'amélioration.

Contraintes :
- Base-toi uniquement sur les informations présentes dans les commentaires.
- N'invente aucune information.
- Regroupe les remarques similaires.
- Sois clair et objectif.

Format de sortie :
Présente la réponse sous la forme de quatre sections :
1. Points positifs
2. Points négatifs
3. Problèmes récurrents
4. Recommandations

### Analyse du prompt

Ce prompt est construit progressivement à partir des différentes composantes étudiées précédemment.

- Le rôle indique au modèle le métier ou la posture qu'il doit adopter.
- Le contexte explique la situation.
- La tâche décrit précisément ce qui est attendu.
- Les contraintes limitent les risques d'erreur ou d'hallucination.
- Le format de sortie facilite l'exploitation des résultats.

---

## Bilan

Cette première partie permet de mieux comprendre qu'un bon prompt ne consiste pas simplement à poser une question.

Un prompt efficace + efficient précise :
- le rôle du modèle ;
- le contexte ;
- la tâche à réaliser ;
- les contraintes à respecter ;
- le format attendu pour la réponse.

Ces éléments permettent d'obtenir des réponses plus précises, plus fiables et plus faciles à exploiter.