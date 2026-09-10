# Prompts pour les applications métier [bloc 5]

## Objectif

L'objectif de cette partie est de concevoir des prompts adaptés à différents besoins rencontrés en entreprise.

Chaque prompt est construit en tenant compte des contraintes fonctionnelles afin d'obtenir une réponse exploitable, fiable et adaptée au contexte métier.

## 5.1 — Résumer un document

Tu es un assistant spécialisé dans l'analyse documentaire.

Résume le document fourni en respectant les contraintes suivantes :

- Maximum 250 mots.
- Conserver uniquement les informations factuelles.
- Identifier clairement les objectifs.
- Identifier les principaux résultats.
- Identifier les recommandations.
- N'inventer aucune information.

Présente le résultat avec les sections suivantes :

- Résumé
- Objectifs
- Résultats
- Recommandations

## 5.2 — Traduire un document

Tu es un traducteur professionnel.

Traduis le document suivant du français vers l'anglais.

Contraintes :

- Conserver le sens.
- Conserver la structure.
- Conserver les termes techniques.
- Ne pas résumer.
- Ne rajouter aucune information.

Retourne uniquement la traduction.

## 5.3 — Classifier un ticket informatique

Tu es un technicien du support informatique.

Analyse le ticket suivant et classe-le dans une seule des catégories suivantes :

- réseau
- logiciel
- matériel
- sécurité
- accès
- autre

Retourne uniquement un JSON valide contenant :

- categorie
- justification

## 5.4 — Extraire les informations d'une facture

Tu es un assistant spécialisé dans l'analyse de documents.

À partir de la facture fournie, retourne uniquement un objet JSON valide contenant les propriétés suivantes :

- numero_facture
- date
- client
- montant_ht
- tva
- montant_ttc

Si une information est absente, attribue la valeur null.

Ne retourne aucun texte avant ou après le JSON.

Une capture d'écran du test est conservée dans :

`assets/images/partie_5/p5_5.4_extraction_info_kimi_k3.png`

## 5.5 — Rédiger un email

Tu es un conseiller du service client.

Rédige un email destiné à un client dont la livraison a pris du retard.

Objectifs :

- reconnaître le retard ;
- présenter des excuses ;
- expliquer la situation sans inventer de cause ;
- proposer une solution.

Contraintes :

- ton professionnel ;
- ton courtois ;
- ton rassurant ;
- maximum 150 mots.

Une capture d'écran du test est conservée dans :

`assets/images/partie_5/p5_5.5_redaction_email_kimi_k3.png`

---

## Bilan

Cette partie a permis de concevoir plusieurs prompts adaptés à des besoins métiers courants.

Chaque prompt est construit en tenant compte du contexte, de la tâche à réaliser et des contraintes spécifiques afin d'obtenir des réponses fiables, structurées et directement exploitables dans un environnement professionnel.