# Partie 1 — Anatomie d'un prompt

## Objectif

L'objectif de cette partie est de comprendre les différentes composantes d'un prompt afin de construire une demande claire, précise et efficace destinée à un modèle de langage (LLM).

Avant de rédiger un prompt complet, il est important d'identifier les informations essentielles que le modèle doit recevoir pour produire une réponse pertinente.

---

## 1.1 — Les composantes d'un prompt

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