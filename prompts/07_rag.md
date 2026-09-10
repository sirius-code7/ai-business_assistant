# Prompt Engineering et RAG (bloc 7)

## Objectif

L'objectif de cette partie est de comparer les réponses produites par un modèle de langage lorsque le document de référence est absent, puis présent, avec ou sans contraintes.

Cette approche met en évidence le principe du Retrieval-Augmented Generation (RAG), qui consiste à utiliser un document comme source d'information afin d'améliorer la qualité et la fiabilité des réponses.

## 7.1 — Document utilisé

Le document utilisé pour cette expérimentation est **La Bibliothèque de Babel** de Jorge Luis Borges.

Ce document servira de source de connaissances pour répondre aux questions posées au modèle de langage.

### Prompt A 

> Quel est le rôle de la Bibliothèque dans le récit ?

Une capture d'écran du test est conservée dans :

`assets/images/partie_7/p7_7.2_prompt_a_kimi_k3.png`

### Prompt B 

> À partir du document fourni, réponds à la question suivante :

> Quel est le rôle de la Bibliothèque dans le récit ?

Une capture d'écran du test est conservée dans :

`assets/images/partie_7/p7_7.3_prompt_b_kimi_k3.png + suite`

### Prompt C

> À partir uniquement du document fourni, réponds à la question suivante :

> Quel est le rôle de la Bibliothèque dans le récit ?

> Contraintes :

>- Utiliser uniquement le contexte fourni.
>- Ne pas inventer d'information absente.
>- Signaler lorsqu'une information n'est pas trouvée dans le document.
>- Citer le passage ou la partie du document utilisée pour répondre.

Une capture d'écran du test est conservée dans :

`assets/images/partie_7/p7_7.4_prompt_c_kimi_k3.png + suite`

## 7.5 — Comparaison des résultats

| Prompt | Observation |
|---------|-------------|
| A | À compléter |
| B | À compléter |
| C | À compléter |

### Bilan

Cette expérimentation montre l'intérêt d'utiliser un document de référence dans une approche RAG.

Lorsque le document est fourni et que des contraintes sont ajoutées, les réponses deviennent généralement plus fiables, plus précises et mieux justifiées. Les risques d'hallucination sont également réduits grâce à l'utilisation exclusive des informations contenues dans le document.