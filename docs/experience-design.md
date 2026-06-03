# experience-design.md

# IA = Ingénieur Augmenté / Ingénieur Aliéné

## Conception de l'expérience

---

# Statut du document

Document de conception.

Ce document décrit :

- ce que l'expérience cherche à démontrer ;
- les hypothèses de départ ;
- les mécanismes expérimentaux ;
- les observations attendues ;
- les risques de conception.

Ce document est volontairement indépendant :

- du support technique ;
- du déroulé précis ;
- de la conférence elle-même.

---

# Vision

La plupart des discussions autour de l'IA générative opposent :

- optimistes ;
- pessimistes.

Cette conférence cherche à éviter cette opposition.

L'objectif n'est pas de répondre à la question :

> "L'IA est-elle bonne ou mauvaise ?"

L'objectif est d'explorer une question plus intéressante :

> "Comment les choix d'interaction avec l'IA modifient-ils la cognition de l'ingénieur ?"

---

# Intuition fondatrice

L'IA ne remplace pas seulement l'exécution.

Elle modifie la manière dont un individu choisit d'investir son effort cognitif.

Certaines utilisations :

- augmentent l'apprentissage ;
- augmentent la compréhension ;
- augmentent la créativité.

D'autres :

- réduisent l'effort de compréhension ;
- favorisent la dépendance ;
- créent une illusion de maîtrise.

La frontière entre ces deux modes est souvent invisible.

---

# Thèse centrale

L'IA n'est pas intrinsèquement augmentante ou aliénante.

Une même IA peut produire les deux effets.

La différence dépend principalement :

- de l'intention ;
- de la stratégie cognitive ;
- du mode de collaboration humain-IA.

---

# Question de recherche

Question principale :

> Que se passe-t-il dans la tête d'un même ingénieur lorsqu'il passe d'un usage de l'IA optimisé pour le débit à un usage optimisé pour la lucidité, sur le même système ?

Le contraste n'est pas entre deux groupes. Il est intra-personne, avant/après,
entre deux phases successives vécues par tout le monde.

---

# Hypothèses

## H1

Sous pression de débit (phase 1), la revue des sorties de l'IA devient de plus en plus superficielle à mesure que les demandes s'enchaînent.

---

## H2

Cette capitulation est en grande partie invisible à celui qui la vit : il se sent productif.

---

## H3

Le code produit en phase 1 contient des trous (visibilité, droits, cohérence) que ses auteurs n'ont pas vus.

---

## H4

Un quiz qui sépare "ce que je crois" de "ce que fait réellement mon code" rend cet écart tangible et chiffrable.

---

## H5

En phase 2, sur le même code, l'IA peut redevenir un instrument de lucidité — à condition que l'humain garde le jugement à chaque sortie d'agent.

---

## H6

Le risque de la phase 2 est de reproduire la capitulation à plus grande échelle : lancer beaucoup d'agents et tamponner leurs sorties.

---

# Pourquoi une expérience ?

Une simple présentation théorique est insuffisante.

Les phénomènes observés sont :

- subtils ;
- contre-intuitifs ;
- souvent invisibles à leurs propres acteurs.

Les participants doivent les vivre eux-mêmes.

---

# Principe expérimental

Tout le monde reçoit la même chose :

- la même codebase ;
- le même backlog ;
- les mêmes outils ;
- les mêmes modèles d'IA.

Ce qui change, c'est l'intention, et elle change dans le temps : phase 1 puis
phase 2. Le sujet de l'expérience, c'est le même individu à deux moments.

---

# Phase 1 — Capitulation

Cadre : on vient de vous embaucher, descendez le backlog le plus vite possible
avec l'agent.

Mécanisme : le backlog est plus long que le créneau. Sous la pression du nombre,
on délègue à l'agent et on prend ce qu'il propose avec une revue qui s'allège à
chaque item. C'est la capitulation cognitive.

Ce qu'on observe :

- le débit ;
- le moment où la revue décroche ;
- les questions à l'agent qui disparaissent ;
- la sensation affichée : "ça avance".

---

# Phase 2 — Augmentation

Cadre : même code, on reprend ce qui a été livré et on l'attaque sous tous les
angles avec l'IA, en gardant le jugement.

Mécanisme : analyses en parallèle, audit des risques et de la criticité, agents
de revue, de qualité, de découverte métier, de recherche de l'état de l'art. La
règle qui tient toute la phase : à chaque sortie d'agent, l'humain tranche.

Ce qu'on observe :

- est-ce qu'on arbitre les sorties ou est-ce qu'on les tamponne ;
- est-ce qu'on retrouve les trous de la phase 1 ;
- est-ce que la sensation change.

---

# Pourquoi cet ordre ?

Parce qu'il est réaliste, et parce qu'il finit bien.

Dans la pratique, la pression de delivery vient en premier. On la fait vivre,
puis on montre qu'avec le même outil on peut reprendre la main. Finir sur la
reprise en main, pas sur le constat des trous, c'est ce qui permet à chacun de
repartir avec quelque chose.

---

# Révélation différée

Le cœur de l'expérience repose sur une idée simple :

La capitulation est difficile à observer pendant qu'on la vit.

La production est facile à observer.

Il faut donc provoquer une situation où la capitulation devient visible à celui
qui l'a vécue.

---

# Mécanisme de révélation

Le révélateur n'est pas une modif surprise. C'est le débrief de la phase 1, en
trois temps :

1. ressenti à chaud (on se sent productif) ;
2. quiz individuel qui sépare "ce que je crois" de "ce que fait mon code" ;
3. re-ressenti, une fois l'écart vu.

Le croisement confiance élevée + beaucoup de "je ne sais pas" rend la
surestimation tangible et chiffrée.

---

# Pourquoi un quiz plutôt qu'une démo

Une démo en direct désigne un coupable et braque la salle. Le quiz est
individuel : chacun constate son propre écart, sans être exposé. C'est plus
honnête et plus efficace pour faire émerger la prise de conscience.

---

# Ce qui doit émerger

Les participants doivent progressivement réaliser que :

- produire n'est pas comprendre ;
- on peut capituler sans s'en rendre compte ;
- le même outil peut, en phase 2, redevenir un instrument de lucidité.

---

# Observations recherchées

## Pendant la phase 1

Observer :

- le débit ;
- le moment où la revue décroche ;
- les questions à l'agent qui disparaissent ;
- la dépendance au modèle.

---

## Pendant le débrief de la phase 1

Observer :

- l'écart entre confiance affichée et justesse réelle ;
- les réactions au quiz ;
- les prises de conscience.

---

## Pendant la phase 2

Observer :

- est-ce qu'on arbitre les sorties d'agents ou est-ce qu'on les tamponne ;
- est-ce qu'on retrouve les trous de la phase 1 ;
- le changement de sensation.

---

# Critères de réussite

L'expérience est réussie si chaque participant constate lui-même, sur son propre
cas, l'écart entre ce qu'il croyait avoir livré et ce que son code fait
réellement — puis ressent, en phase 2, que le même outil peut le rendre plus
lucide.

Sans que cela lui soit asséné à l'avance.

---

# Critères d'échec

## Échec 1

Le backlog est trop court ou trop simple.

Tout le monde a le temps de bien faire.

La capitulation ne se déclenche pas.

---

## Échec 2

Le backlog est trop difficile.

Personne ne boucle quoi que ce soit, la pression du nombre ne joue pas.

---

## Échec 3

Le quiz est vécu comme un examen.

Les participants se braquent au lieu de constater leur écart.

---

## Échec 4

La phase 1 est moralisée.

Le chemin naïf est présenté comme une faute alors qu'il est légitime sous
pression de débit.

---

## Échec 5

La phase 2 devient une capitulation deluxe.

On lance beaucoup d'agents et on tamponne leurs sorties. Le jugement n'est jamais
repris.

---

# Principe fondamental

L'expérience ne doit jamais chercher à démontrer que :

- l'IA est mauvaise ;
- l'IA rend stupide ;
- les développeurs deviennent inutiles.

L'expérience doit simplement rendre visibles des arbitrages cognitifs qui existaient déjà mais qui sont amplifiés par l'IA.

---

# Insight principal recherché

L'IA transforme progressivement le coût de la compréhension.

Pendant des décennies :

- produire était difficile ;
- comprendre était obligatoire.

Aujourd'hui :

- produire devient de moins en moins coûteux ;
- comprendre devient la ressource rare.

Cette évolution pourrait transformer profondément le métier d'ingénieur.

---

# Question finale laissée ouverte

Après l'expérience, chaque participant devrait repartir avec une question personnelle :

> Dans mon propre usage de l'IA, suis-je en train d'investir ma cognition ou de la déléguer ?

L'objectif n'est pas d'imposer une réponse.

L'objectif est de rendre cette question impossible à ignorer.
