# Comparer les techniques de prompting [bloc 2]

## Objectif

L'objectif de cette partie est de comparer différentes techniques de prompting afin d'observer leur impact sur la qualité des réponses d'un modèle de langage.

Le même commentaire sera utilisé pour chaque technique afin de faciliter la comparaison.

---

## Commentaire à analyser

> "Le service est rapide mais l'application plante régulièrement."

Classes possibles :

- positif
- négatif
- neutre

---

## 2.1 Zero-shot

### Principe

Le modèle reçoit uniquement la consigne, sans exemple préalable.

### Test

Le prompt a été soumis au modèle de langage Kimi K3.

**Réponse obtenue :**

> négatif

Une capture d'écran du test est disponible dans :

`assets/images/partie_2/p2_2.1_zero_shot_kimi_k3.png`

---

### Évaluation

La réponse obtenue est cohérente.

Le commentaire comporte un point positif (« Le service est rapide »), mais également un problème important (« l'application plante régulièrement »). Le modèle considère que cet élément négatif a un impact plus fort sur l'expérience globale du client et classe donc le commentaire comme **négatif**.

La réponse respecte la consigne en retournant uniquement une classe.

## 2.2 — One-shot

### Principe

Le One-shot Prompt consiste à fournir un seul exemple au modèle avant de lui confier la tâche. Cet exemple lui permet de mieux comprendre ce qui est attendu en termes de raisonnement et de format de réponse.

### Test

Le prompt a été soumis au modèle de langage **Kimi K3**.

**Réponse obtenue :**

> négatif

Une capture d'écran du test est conservée dans :

`assets/images/partie_2/p2_2.2_one_shot_kimi_k3.png`

### Évaluation

Le modèle classe le commentaire comme **négatif**.

Cette réponse est cohérente, car malgré la présence d'un point positif (« Le service est rapide »), le dysfonctionnement répété de l'application est considéré comme un élément ayant un impact plus important sur l'expérience du client.

Le modèle respecte également la consigne en retournant uniquement la classe demandée.

### Observation

L'ajout d'un exemple avant la demande permet au modèle de mieux comprendre la tâche à réaliser.

Dans ce test, le modèle conserve une réponse cohérente tout en respectant le format demandé.

## 2.3 — Few-shot

### Principe

Le Few-shot Prompt consiste à fournir plusieurs exemples au modèle avant de lui demander d'exécuter la tâche. Ces exemples lui permettent de mieux comprendre le contexte et les critères de classification.

### Test

Le prompt a été soumis au modèle de langage **Kimi K3**.

**Réponse obtenue :**

> négatif

Une capture d'écran du test est conservée dans :

`assets/images/partie_2/p2_2.3_few_shot_kimi_k3.png`

### Évaluation

Le modèle classe le commentaire comme **négatif**.

Cette réponse est cohérente avec les exemples fournis dans le prompt. Les différents exemples permettent au modèle de mieux comprendre la tâche de classification tout en respectant le format attendu.

### Observation

Le Few-shot fournit davantage de contexte au modèle grâce à plusieurs exemples. Cette approche peut améliorer la compréhension de la tâche lorsque celle-ci est plus complexe.