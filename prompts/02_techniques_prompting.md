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