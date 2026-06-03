# IA = Ingénieur Augmenté / Ingénieur Aliéné
## Guide de facilitation de l'atelier

> **Le runbook du jour J est la section [« Déroulé concret — Jour J »](#déroulé-concret--jour-j).** Tout ce qui précède est le cadrage à avoir en tête.
> Supports à portée de main : [`quiz-phase1.md`](quiz-phase1.md) (débrief phase 1) · [`fiche-angles-phase2.md`](fiche-angles-phase2.md) (remise phase 2) · `backlog.md` (repo `atelier`, remis en phase 1).

### Sommaire

**Cadrage (à lire avant)**
- [Intention](#intention) · [Cadrage à tenir, et à répéter](#cadrage-à-tenir-et-à-répéter) · [Hypothèse centrale](#hypothèse-centrale)
- [Principe de l'expérience](#principe-de-lexpérience) · [Pourquoi cet ordre](#pourquoi-cet-ordre) · [Vocabulaire](#vocabulaire)
- [Support technique](#support-technique) · [Nature du backlog](#nature-du-backlog) · [Ce qui doit être observé](#ce-qui-doit-être-observé)
- [Le moment clé : le débrief de la phase 1](#le-moment-clé--le-débrief-de-la-phase-1) · [Questions de débriefing](#questions-de-débriefing) · [Messages clés](#messages-clés-à-faire-émerger)

**Déroulé concret — Jour J (le runbook live)**
- [Avant la session](#avant-la-session) · [Constitution des équipes](#constitution-des-équipes) · [Consigne de la phase 1](#consigne-de-la-phase-1-à-loral)
- [Timing indicatif (~105 min)](#timing-indicatif-créneau-105-min) · [Variante compressée (~90 min)](#variante-compressée-90-min)
- [Chemin naïf vs profond](#chemin-naïf-vs-chemin-profond) · [Le débrief de la phase 1, en détail](#le-débrief-de-la-phase-1-en-détail)
- [Consigne de la phase 2](#consigne-de-la-phase-2-à-loral--remise-de-la-fiche-dangles) · [Le piège de la phase 2](#le-piège-de-la-phase-2) · [Ce que tu observes en phase 2](#ce-que-tu-observes-en-phase-2)
- [Débrief phase 2 et clôture](#débrief-phase-2-et-clôture) · [Gestion du public mixé](#gestion-du-public-mixé) · [Pièges côté facilitateur](#pièges-côté-facilitateur)

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

# Cadrage à tenir, et à répéter

On ne devient ni augmenté ni aliéné en 30 minutes. Ce n'est pas le propos.
L'atelier fait juste sentir une direction : vers quoi nos comportements nous
inclinent quand on code avec l'IA. Personne n'est étiqueté.

Dis-le explicitement, et redis-le à trois moments : au lancement, juste avant
le quiz de fin de phase 1, et au débrief. Si les participants l'oublient, le quiz
peut être vécu comme un examen. Ce n'est pas un examen.

---

# Hypothèse centrale

L'IA peut :

- augmenter un ingénieur ;
- aliéner un ingénieur.

La différence ne dépend pas principalement du modèle utilisé.

Elle dépend principalement de la manière dont l'humain choisit d'interagir avec celui-ci.

---

# Principe de l'expérience

Il n'y a pas deux groupes. Tout le monde travaille en même temps, en binômes ou
petites équipes, sur la même codebase. Le contraste ne se joue pas entre des
groupes : il se joue avant/après, dans la tête de chaque participant, entre deux
phases successives.

## Phase 1 — Capitulation

Cadre donné aux participants : on vient de vous embaucher, descendez le backlog
le plus vite possible avec l'agent.

Le backlog (backlog.md) est volontairement plus long que le créneau.
L'objectif caché : provoquer la capitulation cognitive. À force d'enchaîner les
petites demandes, on prend ce que l'agent propose avec une revue de plus en plus
superficielle.

Ne dis pas aux participants que c'est le but. Pour eux, c'est juste une pression
de delivery réaliste.

## Phase 2 — Augmentation

Même produit, même code. On reprend ce qui a été livré en phase 1 et on
l'attaque sous tous les angles avec l'IA, en gardant le jugement.

La fiche d'angles ([`fiche-angles-phase2.md`](fiche-angles-phase2.md)) est
remise aux participants. Elle est organisée autour d'une règle : à chaque sortie
d'agent, l'humain tranche.

Point de vigilance central : la phase 2 ne doit pas devenir une "capitulation
deluxe". Lancer dix agents et tamponner leurs sorties, c'est encore déléguer son
jugement. La différence entre les deux phases n'est pas le nombre d'agents.
C'est qui tient le volant.

---

# Pourquoi cet ordre

Capitulation d'abord, augmentation ensuite. On finit sur de la reprise en main,
pas sur le constat des trous. C'est ce qui permet une clôture où chacun repart
avec quelque chose.

---

# Vocabulaire

Au lancement, on ne parle ni d'augmenté ni d'aliéné. On parle de phase 1 et de
phase 2, ou de "vitesse" et de "reprise en main". Les termes ingénieur augmenté
et ingénieur aliéné arrivent au débrief, une fois l'expérience vécue.

---

# Support technique

Support retenu (figé dans le repo `atelier`, voir
[`../design/codebase-selection.md`](../design/codebase-selection.md)) :

- spring-boot-realworld-example-app (back)
- react-redux-realworld-example-app (front)

Pourquoi ce choix :

- application réaliste ;
- domaine compréhensible rapidement ;
- front + back ;
- taille raisonnable ;
- architecture suffisamment riche pour nécessiter de la compréhension.

Le repository participant est déjà préparé (apps vendorisées, `install.sh`,
`setup.md`).

---

# Nature du backlog

Le backlog de la phase 1 (backlog.md) est fait d'items qui :

- semblent triviaux, formulés en une phrase ;
- cachent de la profondeur (visibilité, droits, cohérence, cas limites) ;
- admettent un chemin naïf qui "marche" et un chemin profond ;
- sont plus nombreux que faisable dans le créneau.

C'est important : les trous doivent venir de la revue superficielle, pas
seulement du manque de temps. Chaque item doit pouvoir être bâclé de façon
plausible.

Exemple type : les brouillons. Un booléen draft/published et "ça marche". Mais
le brouillon fuite dans le feed global, par tag, dans le profil public, via
l'URL directe. La feature paraît simple : elle touche création, édition,
publication, visibilité, API, listes, profils, droits, tests.

---

# Ce qui doit être observé

Pendant l'atelier, noter :

- en phase 1 : le débit, le moment où la revue décroche, les questions à l'agent
  qui disparaissent, la sensation affichée ("ça avance") ;
- en phase 2 : est-ce qu'on arbitre les sorties d'agents ou est-ce qu'on les
  tamponne, est-ce que la sensation change, est-ce qu'on retrouve les trous de
  la phase 1.

---

# Le moment clé : le débrief de la phase 1

Le révélateur n'est plus une modif surprise. C'est le débrief de la phase 1,
construit pour rendre les trous tangibles sans les asséner : ressenti à chaud →
quiz individuel → re-ressenti. C'est le pivot de l'atelier.

Le pas-à-pas des trois temps (timing, formulations, plan B Kahoot) est dans la
section « Le débrief de la phase 1, en détail » du déroulé Jour J, plus bas.

---

# Questions de débriefing

Après la phase 1 :

- Comprenez-vous ce que vous avez livré ?
- Sauriez-vous le refaire sans l'agent ?
- Quels choix de conception ont été faits ? Par qui ?
- Où sont les trous que vous n'aviez pas vus ?

Après la phase 2 :

- Qu'est-ce qui a changé dans la sensation par rapport à la phase 1 ?
- Quels angles ont le plus apporté ?
- Qu'avez-vous compris que vous ne compreniez pas avant ?

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

# Déroulé concret — Jour J

Cette section opérationnalise tout ce qui précède en un pas-à-pas. Un seul sujet,
tout le monde en même temps, deux phases successives.

## Avant la session

- Le setup est fait en amont par chaque participant via `SETUP.md`.
- Les deux apps sont clonées dans `app/` (back + front).
- Le brief de la phase 1 est dans `backlog.md` : un backlog volontairement
  plus long que le créneau.
- La fiche de la phase 2 ([`fiche-angles-phase2.md`](fiche-angles-phase2.md)) n'est PAS distribuée au départ.
  Tu la remets seulement au lancement de la phase 2.
- Toi seul as accès à `docs/`. Les participants ne voient ni la thèse, ni le but
  caché de la phase 1.
- Prépare la clé d'API et un canal privé pour la transmettre.

## Constitution des équipes

- Pas de groupes opposés. Tout le monde fait la même chose en même temps.
- Binômes ou petites équipes (2-3). Au-delà, une personne pilote l'agent et les
  autres décrochent.
- Public mixé front/back : équilibre les profils dans chaque binôme pour
  qu'aucun ne reste bloqué sur une couche.

## Consigne de la phase 1 (à l'oral)

> On vient de vous embaucher dans l'équipe qui maintient Conduit. Voici le
> backlog. Descendez-en un maximum avec l'agent. Le seul critère, c'est que ça
> marche et que ce soit démontrable. Le nombre d'items bouclés compte.

Ne dis pas que le but caché est la capitulation. Pour eux, c'est une pression de
delivery réaliste. Le backlog fait le reste.

## Timing indicatif (créneau ~105 min)

- 0-5 : annonce, rappel du cadrage (ni augmenté ni aliéné, on lit une
  direction), rappel que le setup doit déjà tourner.
- 5-8 : consigne de la phase 1, remise du `backlog.md`.
- 8-38 : phase 1, tout le monde descend le backlog.
- 38-55 : débrief phase 1 (ressenti → quiz → re-ressenti, voir plus haut).
- 55-58 : remise de la fiche d'angles, consigne de la phase 2.
- 58-88 : phase 2, reprise en main sur la même codebase.
- 88-100 : débrief phase 2 (ressenti, collecte des idées de tous).
- 100-105 : clôture (chacun repart avec une phrase).

Ajuste les bornes au temps réel dont tu disposes.

## Variante compressée (~90 min)

Si le créneau est juste, c'est cette version qui tient. On rogne sur les deux
phases de travail et sur les débriefs, jamais sur le quiz : c'est lui le pivot.

- 0-4 : annonce + cadrage (ni augmenté ni aliéné).
- 4-6 : consigne phase 1, remise du `backlog.md`.
- 6-31 : phase 1 (25 min suffisent à déclencher la capitulation si le backlog
  est assez long).
- 31-46 : débrief phase 1 (ressenti ~2, quiz ~9, re-ressenti ~4).
- 46-48 : remise de la fiche d'angles, consigne phase 2.
- 48-73 : phase 2.
- 73-85 : débrief phase 2 (collecte resserrée : un angle par binôme).
- 85-90 : clôture (une phrase chacun).

Ce qu'on ne coupe pas : le quiz et son re-ressenti. Ce qu'on coupe en premier si
ça déborde encore : la collecte du débrief phase 2 (passe à 2-3 binômes au lieu
de tous), pas le tour de clôture.

## Chemin naïf vs chemin profond

Ce que tu vas probablement voir en phase 1. Sous pression de débit, presque tout
le monde prend le chemin naïf. C'est voulu.

Chemin naïf :

- un booléen `draft` / `published` sur l'article ;
- la feature "marche" : on sauve, on republie ;
- aucune règle de visibilité pensée. Le draft fuite dans le feed global, par
  tag, dans le profil public, via l'URL directe.

Chemin profond (ce que la phase 2 fait émerger) :

- repérage des endroits où un article devient visible (feed, tag, profil, slug
  direct, favoris, commentaires) ;
- questions métier posées (qui voit quoi ?) ;
- filtres et requêtes ajustés côté back, état géré côté front ;
- tests sur la visibilité.

Le naïf n'est pas "faux" : il satisfait le brief tel qu'il est écrit. C'est
exactement le piège recherché.

## Le débrief de la phase 1, en détail

C'est le pivot de l'atelier. Trois temps (voir aussi la section "Le moment clé").

1. Ressenti à chaud (~3 min). Comment vous vous sentez ? Combien d'items
   bouclés ? Note au tableau le ressenti dominant : ça avance, c'est productif.
2. Quiz individuel (~10 min, [`quiz-phase1.md`](quiz-phase1.md)). Partie 1 : compréhension du
   système. Partie 2 : ce que fait réellement votre code, avec "je ne sais pas"
   assumé. En Kahoot. Plan B si Kahoot plante : mêmes questions à l'oral, à main
   levée (compte les mains qui ne se lèvent pas).
3. Re-ressenti (~4 min). Maintenant que vous avez vu le quiz, comment vous
   sentez-vous ? C'est là que tu nommes le phénomène : capitulation cognitive.
   Pas une perte de compétence, la sensation d'avoir pris sans vérifier dès
   qu'on a enchaîné les demandes.

Tu gardes l'agrégat du quiz pour appuyer le débrief : confiance élevée + beaucoup
de "je ne sais pas" = surestimation rendue visible. Montre la distribution,
jamais un classement.

## Consigne de la phase 2 (à l'oral, + remise de la fiche d'angles)

> Même produit, même code. Cette fois, l'objectif n'est plus le débit. Vous
> reprenez ce que l'équipe vient de livrer et vous l'attaquez sous tous les
> angles avec l'IA. Lancez des analyses en parallèle, demandez la criticité et
> les risques, lancez des agents de revue, de qualité, de découverte métier, de
> recherche de l'état de l'art. Règle unique : à chaque sortie d'agent, c'est
> vous qui tranchez.

## Le piège de la phase 2

La phase 2 ne doit pas devenir une "capitulation deluxe". Lancer dix agents et
tamponner leurs sorties, c'est encore déléguer son jugement. Si tu vois un binôme
empiler des rapports sans les lire, interviens : "qu'est-ce que tu en retiens,
toi ?" La différence entre les deux phases, ce n'est pas le nombre d'agents,
c'est qui tient le volant.

## Ce que tu observes en phase 2

- est-ce qu'ils arbitrent les sorties d'agents ou est-ce qu'ils les tamponnent ;
- est-ce qu'ils retrouvent les trous de la phase 1 (fuites feed, tag, slug) ;
- est-ce que la sensation change ;
- quels angles leur apportent le plus.

## Débrief phase 2 et clôture

Débrief phase 2 :

- ressenti : qu'est-ce qui a changé par rapport à la phase 1 ?
- collecte ouverte : chaque binôme donne un angle qui a payé, une idée. Tu notes
  tout au tableau, sans trier.
- c'est ici que les termes augmenté / aliéné prennent tout leur sens.

Clôture (~5 min) :

- tour de table, une phrase chacun : avec quoi tu repars ?
- laisse la question ouverte : dans mon usage de l'IA, est-ce que j'investis ma
  cognition ou est-ce que je la délègue ?

## Gestion du public mixé

- Front et back dans chaque binôme : le backlog touche les deux, c'est voulu.
- Si un binôme est mono-profil, oriente-le. Un profil back peut quand même
  cartographier la visibilité côté front via l'agent.
- Évite qu'une seule personne monopolise le clavier de l'agent. Fais tourner.

## Pièges côté facilitateur

- Ne révèle pas la thèse ni le but caché de la phase 1 avant le débrief.
- Ne moralise pas : le chemin naïf est légitime sous pression de débit.
- En phase 2, surveille la capitulation deluxe (voir plus haut).
- Si le setup coince encore au démarrage, traite-le hors chrono. La friction
  technique n'est pas l'objet.
