# 00 · Accueil

Cadrage + setup en live. Ne pas courir : c'est ici qu'on embarque les gens. Tant
que le cadre et l'état d'esprit ne sont pas posés, l'atelier ne sert à rien.
Horaires → [`planning.md`](planning.md).

## La réalité à l'arrivée (l'anticiper, pas la subir)

Les participants débarquent d'autres confs. On leur a demandé un ordi, mais la
consigne n'a pas vraiment circulé : **certains n'en auront pas**, et **personne
n'a fait le setup**. C'est OK — c'est même le plan.

- **Pas d'ordi → en binôme avec quelqu'un qui en a un.** De toute façon on
  travaille en équipe : ça ne pénalise personne, ça les place juste côté revue.
- **Setup pas fait → on le fait ensemble, en live** (voir plus bas). C'est voulu :
  ça démarre l'atelier en douceur et ça me laisse le temps de glisser des idées
  pendant que ça installe.

## Checklist animateur (pour moi, à voir avant d'ouvrir la bouche)

- [ ] Clé d'API prête + canal privé pour la transmettre.
- [ ] `backlog.md` prêt à remettre (repo `atelier`) — **pas avant la phase delivery**.
- [ ] Quiz Kahoot chargé ([`03-quiz.md`](03-quiz.md)).
- [ ] Fiche d'angles prête ([`05-fiche-angles.md`](05-fiche-angles.md)) — **pas avant la phase méta-cognition**.

**À garder secret jusqu'au débrief :** la thèse de l'atelier · le but caché de la
phase delivery (**provoquer la capitulation**) · les mots *délestage, émancipation,
augmenté, aliéné*. On nomme **« phase delivery »** dès maintenant ; la **phase
méta-cognition** n'est nommée **qu'au moment de la lancer** (ne pas téléphoner le
contraste). Fil conceptuel complet dans [`README`](README.md).

---

## Ouverture — poser le cadre

À l'oral.

> On va coder ensemble sur une vraie codebase, en deux temps. On ne parle pas de
> performance des modèles — on parle de **notre façon de travailler avec**.

**Le déroulé en clair (ce qu'on annonce) :**

1. **Phase delivery** — on pousse notre delivery avec l'IA, à fond.
2. **Débrief** — on s'arrête, on regarde ensemble ce qui s'est passé.
3. **On rejoue** — autrement, en adaptant ce qu'on a compris au débrief. *(On ne
   nomme pas encore cette phase — son nom vient à son lancement.)*

**Le cadrage à poser (et à redire au quiz et au débrief) :**

- On ne devient ni augmenté ni aliéné en 2 h. On essaie ici de **compresser le temps**.
- L'atelier ne juge personne et ne tranche rien : il fait juste **sentir une direction**.
- Donc on observe **comment on s'y prend** et **ce que ça nous fait** — pas le résultat.

## Le deal — jouez le jeu à fond

Court, mais c'est **le** message. À dire avec insistance.

> Ce n'est pas une démo, c'est une **expérience** — et vous êtes dedans. Elle ne
> donne quelque chose que si vous y allez **à fond**. Si vous trichez avec elle,
> elle ne vous apprend rien, et vous repartez les mains vides.
>
> Surtout : quand une petite voix vous dit *« ce n'est pas comme ça qu'il faut
> faire »* — **foncez quand même**. Ce malaise, c'est exactement la matière qu'on
> ouvrira au débrief. Le retenir, c'est saboter votre propre manche.

## 🎯 À faire passer (avant de coder)

- On parle de **notre façon de travailler avec l'IA**, pas de la perf des modèles.
- **Deux temps** : on pousse à fond (delivery), on débriefe, on rejoue autrement.
- C'est une **expérience pratique** : on n'en retire quelque chose que si on **joue le jeu à fond** — y compris quand ça semble être la mauvaise manière.
- On observe **comment on s'y prend** et **ce que ça nous fait**, pas le résultat. **Personne n'est jugé.**

## Setup ensemble

Écran partagé.

J'affiche la **page GitHub du repo** et on avance ensemble : clone, `install.sh`,
back `:8080` + front `:4100` qui tournent. Pendant que ça installe, **je meuble** :
je redis le cadre, je teste l'état d'esprit, je laisse traîner deux-trois
amorces sans rien dévoiler du piège.

**Composer les équipes pendant ce temps :**

- Binômes ou trios (**2–3 max**).
- **Mélanger front / back** (mono-profil → je l'oriente).
- Faire **tourner le clavier** : personne ne reste spectateur, personne ne
  monopolise.

Quand tout le monde a back + front qui tournent, on enchaîne sur la
[phase delivery](01-phase1.md).
