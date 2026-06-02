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

---

# Déroulé concret — Exercice 1 (Brouillons)

Cette section opérationnalise tout ce qui précède sur la feature "brouillons".
Le cadre conceptuel (groupes, inversion, révélation) reste valable. Ici c'est le
pas-à-pas du jour J.

## Avant la session

- Le setup est fait en amont par chaque participant via `SETUP.md`.
- Les deux apps sont clonées dans `app/` (back + front).
- Le brief participant est dans `exercices/ex1.md`, volontairement sous-spécifié.
- Toi seul as accès à `docs/`. Les participants ne voient ni la thèse, ni la
  modif surprise.
- Prépare la clé d'API et un canal privé pour la transmettre.

## Constitution des groupes

- Deux groupes : Production et Apprentissage.
- Public mixé front/back : équilibre les profils dans chaque groupe pour
  qu'aucun ne reste bloqué sur une couche.
- Petits effectifs (2-3 par groupe). Au-delà, une personne pilote l'agent et les
  autres décrochent.

## Consignes de mode (à dire à l'oral, pas dans le repo)

Ne mets jamais ces consignes dans un fichier partagé. Si un groupe lit celles de
l'autre, le révélateur tombe. Donne-les à l'oral, ou sur une carte par groupe.

Groupe Production :

> Vous avez X minutes pour livrer la feature. Le seul critère, c'est que ça
> marche et que ce soit démontrable. Déléguez un maximum à l'agent, allez au
> résultat.

Groupe Apprentissage :

> Vous avez X minutes. Le livrable compte moins que votre compréhension du
> système. Servez-vous de l'agent pour cartographier, questionner, tester vos
> hypothèses. À la fin, vous devez pouvoir expliquer chaque choix.

Vocabulaire neutre : "Production" et "Apprentissage", jamais "les bons / les
mauvais".

## Timing indicatif (créneau ~90 min)

- 0-5 : annonce du créneau, rappel que le setup doit déjà tourner.
- 5-10 : remise des consignes de mode (séparément).
- 10-40 : phase 1, les deux groupes travaillent sur `ex1.md`.
- 40-45 : modif surprise (voir plus bas).
- 45-70 : phase 2, chaque groupe absorbe la contrainte. Option : inverser les
  modes ici.
- 70-90 : débrief.

Ajuste les bornes au temps réel dont tu disposes.

## Chemin naïf vs chemin profond

Ce que tu vas probablement voir.

Chemin naïf (souvent Production) :

- un booléen `draft` / `published` sur l'article ;
- la feature "marche" : on sauve, on republie ;
- aucune règle de visibilité pensée. Le draft fuite dans le feed global, par
  tag, dans le profil public, via l'URL directe.

Chemin profond (souvent Apprentissage) :

- repérage des endroits où un article devient visible (feed, tag, profil, slug
  direct, favoris, commentaires) ;
- questions métier posées avant de coder (qui voit quoi ?) ;
- filtres et requêtes ajustés côté back, état géré côté front ;
- quelques tests sur la visibilité.

Le naïf n'est pas "faux" : il satisfait le brief tel qu'il est écrit. C'est
exactement le piège recherché.

## La modif surprise

À lâcher en fin de phase 1, à l'oral, aux deux groupes en même temps :

> Nouvelle contrainte. Un brouillon doit être visible par son auteur dans son
> profil, mais invisible pour tous les autres. Il ne doit jamais apparaître dans
> le feed global ni dans les résultats par tag. Et on doit pouvoir le publier
> sans changer son URL.

C'est elle qui teste le modèle mental. Une implémentation naïve par booléen va
fuiter sur au moins un de ces axes. Le groupe qui a cartographié la visibilité
encaisse vite. L'autre découvre des impacts qu'il n'avait pas vus.

## Ce que tu observes pendant la surprise

- vitesse d'adaptation ;
- est-ce qu'ils savent OÙ chercher, ou est-ce qu'ils redemandent tout à l'agent ;
- confiance affichée vs justesse réelle ;
- capacité à anticiper les fuites (feed, tag, slug) avant que tu les pointes.

## Débrief

Reprends les questions déjà listées plus haut (section Questions de débriefing).
Ordre conseillé :

1. chaque groupe montre où il en est ;
2. tu testes la compréhension réelle : demande d'expliquer un choix, pas de
   remontrer que ça marche ;
3. tu fais émerger l'écart, sans désigner de "bon" groupe ;
4. tu introduis seulement à ce moment les termes augmenté / aliéné.

## Gestion du public mixé

- Front et back dans chaque groupe : la feature touche les deux, c'est voulu.
- Si un groupe est mono-profil, oriente-le. Un profil back peut quand même
  cartographier la visibilité côté front via l'agent.
- Évite qu'une seule personne monopolise le clavier de l'agent. Fais tourner.

## Pièges côté facilitateur

- Ne révèle pas la thèse avant le débrief.
- Ne moralise pas : le chemin naïf est légitime sous contrainte de temps.
- Ne caricature pas le groupe Production, ne sanctifie pas le groupe
  Apprentissage.
- Si le setup coince encore au démarrage, traite-le hors chrono. La friction
  technique n'est pas l'objet.
