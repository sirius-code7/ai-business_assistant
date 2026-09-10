# Sorties structurées [bloc 4]

## Objectif

L'objectif de cette partie est de produire une réponse au format JSON afin qu'elle puisse être facilement exploitée par une application.

Contrairement à une réponse rédigée en langage naturel, une sortie structurée facilite le traitement automatique des informations.

## 4.1 Création d'une sortie JSON

### Principe

Le modèle doit retourner une réponse au format JSON contenant uniquement les informations demandées.

### Test

Le prompt a été soumis au modèle de langage **Kimi K3**.

**Réponse obtenue :**

```json
{
  "sentiment": "negatif",
  "categorie": "livraison",
  "urgence": "moyenne",
  "probleme": "délai de livraison",
  "confiance": 0.9
}
```

Une capture d'écran du test est conservée dans :

`assets/images/partie_4/p4_4.1_sortie_json_kimi_k3.png`

### Évaluation

Le modèle retourne une réponse au format JSON conforme à la demande.

Les propriétés attendues sont présentes et les valeurs sont correctement renseignées.

Cette structure facilite l'exploitation des résultats par une application, puisqu'elle permet d'accéder directement aux informations sans avoir à analyser un texte rédigé en langage naturel.

## 4.2 — Validation de la sortie JSON

### Principe

Le modèle doit produire un JSON valide respectant des règles de validation afin de garantir que la réponse puisse être utilisée directement par une application.

### Test

Le prompt a été soumis au modèle de langage **Kimi K3**.

**Réponse obtenue :**

```json
{
  "sentiment": "negatif",
  "categorie": "livraison",
  "urgence": "moyenne",
  "probleme": "délai de livraison",
  "confiance": 0.9
}
```

Une capture d'écran du test est conservée dans :

`assets/images/partie_4/p4_4.2_validation_json_kimi_k3.png`

### Évaluation

Le modèle retourne un JSON valide qui respecte l'ensemble des règles définies dans le prompt.

La réponse contient uniquement les propriétés attendues, les valeurs autorisées sont respectées et la valeur de `confiance` est bien comprise entre 0 et 1.

L'ajout de règles de validation permet de garantir une sortie plus fiable et directement exploitable par une application.

---

## Bilan

Cette partie a montré l'intérêt des sorties structurées en Prompt Engineering.

La génération d'un JSON facilite l'intégration des réponses dans une application, tandis que l'ajout de règles de validation garantit un format cohérent, prévisible et exploitable automatiquement.

Cette approche améliore la fiabilité des échanges entre un modèle de langage et une application.