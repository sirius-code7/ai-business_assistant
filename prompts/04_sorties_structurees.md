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