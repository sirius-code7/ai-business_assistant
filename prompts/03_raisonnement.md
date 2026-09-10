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

Le prompt a été soumis au modèle de langage **Kimi K3**.

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

### Évaluation

La réponse produite par Kimi K3 est pertinente et respecte les contraintes définies dans le prompt.

Le modèle identifie correctement les principaux problèmes, propose des recommandations adaptées et met également en évidence les points positifs à préserver.

L'analyse est claire, structurée et fondée sur les informations fournies dans les avis clients.

## 3.3 — Vérification de la réponse

### Principe

Un second prompt est utilisé pour contrôler la qualité de la réponse précédente. Son objectif est d'identifier les éventuelles erreurs, omissions ou hallucinations avant de valider le résultat.

### Test

Le prompt de vérification a été soumis au modèle de langage **Kimi K3** en utilisant la réponse obtenue lors de l'étape précédente.

--------------------------------------------------------------
### Prompt

"Voici l'audit de la réponse précédente.

**1. Informations justifiées par les avis**

L'essentiel est bien ancré dans les avis :
- Le plantage de l'application lors de la validation d'une commande provient directement de l'avis 2.
- Le problème non résolu malgré une réponse rapide provient de l'avis 4.
- Le temps d'attente trop long provient de l'avis 1.
- Les points positifs (personnel aimable, réponse rapide, produit conforme) correspondent aux avis 1, 4 et 3.

Remarque mineure : qualifier le plantage de « bloquant » et dire qu'il « empêche directement une action client » est une interprétation. L'avis dit que l'application « plante lors de la validation », ce qui rend l'inférence plausible, mais il s'agit d'un jugement d'analyste et non d'une information littérale.

**2. Contradictions**

Aucune contradiction interne. La réponse ne dit pas à la fois qu'un point est positif et négatif de manière incohérente. La nuance « réponse rapide mais problème non résolu » reflète fidèlement la structure de l'avis 4.

**3. Informations oubliées**

Les quatre avis sont couverts. L'avis 3, purement positif, est pris en compte dans la section « points positifs à préserver ». Rien d'important n'est omis.

**4. Hallucinations ou informations inventées**

Aucune hallucination factuelle détectée : pas de causes inventées (serveurs, bug technique précis), pas de fréquence extrapolée, pas de segments de clientèle supposés. Les recommandations sont génériques mais découlent logiquement des problèmes cités, ce qui est le rôle attendu de l'analyste.

**5. Respect des contraintes du prompt initial**

- Utilisation uniquement des informations des avis : respecté, à part l'interprétation mineure sur le caractère « bloquant ».
- Aucune information inventée : respecté.
- Regroupement des problèmes similaires : partiellement respecté. Les trois problèmes étant distincts par nature (plantage technique, non-résolution, attente), aucune fusion n'était vraiment nécessaire, mais la réponse aurait pu expliciter davantage la parenté entre les avis 1 et 4 (insuffisance du service malgré un point positif).
- Classement par ordre d'importance : respecté, avec justification pour chaque niveau.
- Format en deux sections numérotées : respecté.

**Conclusion**

La réponse est **fiable**. Aucune correction majeure n'est nécessaire. Deux améliorations mineures possibles : (a) marquer explicitement le caractère interprétatif du mot « bloquant », et (b) rendre le regroupement des avis 1 et 4 plus explicite pour répondre pleinement à la contrainte de regroupement."

--------------------------------------------------------------

Le modèle a contrôlé la cohérence de la réponse, identifié les éventuelles interprétations, vérifié le respect des contraintes et recherché d'éventuelles hallucinations.

Une capture d'écran du test est conservée dans :

`assets/images/partie_3/p3_3.3_verification_kimi_k3.png`

### Évaluation

Le modèle conclut que la réponse précédente est globalement **fiable**.

L'audit confirme que les informations proviennent bien des avis clients, qu'aucune contradiction majeure ni hallucination n'a été détectée et que les contraintes du prompt initial sont globalement respectées.

Le modèle identifie toutefois deux pistes d'amélioration :

- préciser que le terme « bloquant » constitue une interprétation et non une information explicitement présente dans les avis ;
- rendre le regroupement des problèmes plus explicite afin de répondre pleinement à la consigne.

Cette étape montre l'intérêt d'utiliser un second prompt pour contrôler la qualité d'une première réponse avant son exploitation.

---

## Bilan

Cette partie a montré qu'un prompt ne sert pas uniquement à obtenir une réponse.

L'utilisation d'un second prompt permet de vérifier la qualité du résultat produit par le modèle, d'identifier les éventuelles interprétations, les omissions ou les hallucinations et de s'assurer que les contraintes initiales ont bien été respectées.

Cette approche améliore la fiabilité des réponses et constitue une bonne pratique en Prompt Engineering.