# IA = Ingénieur Augmenté / Ingénieur Aliéné
## Guide de facilitation de l'atelier

# Intention

L'objectif de cet atelier n'est pas de comparer les performances des modèles d'IA.

L'objectif est de faire vivre aux participants deux modes d'utilisation radicalement différents de l'IA afin de mettre en évidence leurs effets sur :

- la vitesse de production ;
- la compréhension du système ;
- l'apprentissage ;
- l'autonomie ;
- la capacité à faire évoluer une solution.

L'atelier doit permettre aux participants de ressentir eux-mêmes les bénéfices et les limites de chaque approche.

L'expérience doit être vécue avant d'être expliquée.

---

# Hypothèse centrale

L'IA peut :

- augmenter un ingénieur ;
- aliéner un ingénieur.

La différence ne dépend pas principalement du modèle utilisé.

Elle dépend principalement de la manière dont l'humain choisit d'interagir avec celui-ci.

---

# Principe de l'expérience

Deux groupes travaillent sur exactement la même tâche.

## Groupe A : Optimisation de la vitesse

Objectif :

Produire la fonctionnalité demandée le plus rapidement possible.

Les participants sont encouragés à :

- déléguer un maximum à l'IA ;
- copier les solutions proposées ;
- privilégier le résultat visible ;
- minimiser le temps consacré à la compréhension.

Le critère de réussite est la production.

---

## Groupe B : Optimisation de l'apprentissage

Objectif :

Maximiser la compréhension du système et l'apprentissage.

Les participants sont encouragés à :

- comprendre le domaine ;
- cartographier l'architecture ;
- questionner les réponses de l'IA ;
- demander plusieurs approches ;
- générer des hypothèses ;
- produire des tests ;
- challenger les solutions proposées ;
- explorer différentes stratégies de collaboration avec l'IA.

Le critère de réussite est la compréhension.

---

# Inversion des groupes

Après une première phase de travail :

- le groupe A devient le groupe B ;
- le groupe B devient le groupe A.

Objectif :

Faire vivre les deux modes de fonctionnement à chaque participant.

Cette inversion est essentielle.

Elle évite que les participants rationalisent uniquement la position de leur groupe initial.

---

# Point pédagogique important

Il ne faut pas présenter initialement les groupes comme :

- les bons ;
- les mauvais.

Le vocabulaire recommandé au lancement :

- Groupe Production
- Groupe Apprentissage

Les notions d'ingénieur augmenté et d'ingénieur aliéné peuvent être introduites après l'expérience.

---

# Support technique

Support envisagé :

- spring-boot-realworld-example-app
- react-redux-realworld-example-app

Pourquoi ce choix :

- application réaliste ;
- domaine compréhensible rapidement ;
- front + back ;
- taille raisonnable ;
- architecture suffisamment riche pour nécessiter de la compréhension.

Le repository doit être préparé à l'avance.

---

# Nature des exercices

Les exercices doivent :

- être réalisables en moins d'une heure ;
- nécessiter des modifications sur plusieurs couches ;
- permettre une implémentation superficielle ;
- récompenser la compréhension profonde du système.

Critères recherchés :

- ambiguïté métier ;
- impact transverse ;
- possibilité de produire une solution qui semble correcte ;
- présence de compromis de conception.

---

# Exemple de feature candidate

Ajouter la notion de draft d'article.

Impacts potentiels :

- création ;
- édition ;
- publication ;
- visibilité ;
- API ;
- listes ;
- profils ;
- droits d'accès ;
- tests.

La fonctionnalité paraît simple mais possède de nombreuses implications métier.

---

# Ce qui doit être observé

Pendant l'atelier, noter :

- vitesse de progression ;
- volume de code produit ;
- qualité des discussions ;
- compréhension du domaine ;
- dépendance à l'IA ;
- capacité à expliquer les changements réalisés.

---

# Moment clé de l'expérience

Après la première phase :

poser une modification surprise.

Exemple :

"Les règles métier ont changé."

ou

"Ajoutez maintenant cette contrainte supplémentaire."

L'objectif est de mesurer :

- qui possède réellement le modèle mental du système ;
- qui possède seulement une implémentation produite par l'IA.

---

# Questions de débriefing

Pour le groupe Production :

- Comprenez-vous complètement ce qui a été implémenté ?
- Pourriez-vous refaire la même modification sans IA ?
- Quels choix de conception ont été réalisés ?
- Quels risques avez-vous identifiés ?

Pour le groupe Apprentissage :

- Avez-vous terminé ?
- Qu'avez-vous appris ?
- Que comprenez-vous maintenant du système ?
- Que pourriez-vous faire plus rapidement lors d'une deuxième itération ?

---

# Messages clés à faire émerger

L'IA n'est pas intrinsèquement augmentante ou aliénante.

Une même IA peut :

- accélérer l'apprentissage ;
- empêcher l'apprentissage.

Une même personne peut alterner entre les deux modes dans une même journée.

Le véritable enjeu n'est pas l'adoption de l'IA.

Le véritable enjeu est la gestion consciente de son investissement cognitif.

Le futur n'oppose probablement pas :

- les humains ;
- les IA.

Il opposera davantage :

- les humains qui savent orchestrer leur cognition avec l'IA ;
- les humains qui délèguent progressivement leur cognition à l'IA.
