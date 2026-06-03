# IA = Ingénieur Augmenté / Ingénieur Aliéné

Ce dossier contient le contexte de conception d’un atelier/conférence.

Objectif : faire vivre, sur un seul sujet et tous ensemble, deux manières
d’utiliser l’IA, en deux phases successives.

- Phase 1 — capitulation : on descend un backlog le plus vite possible, on
  délègue à l’agent, la revue devient de plus en plus superficielle.
- Phase 2 — augmentation : sur la même codebase, on reprend ce qui a été livré
  et on l’attaque sous tous les angles avec l’IA, en gardant le jugement.

Il n’y a pas deux groupes et pas d’inversion. Tout le monde vit les deux phases
en même temps, en binômes ou petites équipes. Le contraste se joue avant/après,
dans la tête de chaque participant.

Le support technique est RealWorld :
- spring-boot-realworld-example-app
- react-redux-realworld-example-app

## Structure

- `docs/` — conception et facilitation. Réservé au facilitateur, à ne pas
  exposer aux participants.
- `SETUP.md` — parcours d'installation côté participant.
- `exercices/` — briefs remis aux participants : `phase1.md` (le backlog) et
  `phase2.md` (la fiche d'augmentation, remise seulement à la phase 2).
- `app/` — les deux apps RealWorld, non versionnées ici (repos externes).

## Initialisation du projet

Les deux apps RealWorld ne sont pas versionnées dans ce repo (ce sont des repos
externes). Après avoir cloné ce repo, clone-les dans `app/` :

```bash
git clone git@github-perso:FlorisTisseyre/conf.git
cd conf
mkdir -p app && cd app
git clone https://github.com/gothinkster/spring-boot-realworld-example-app.git
git clone https://github.com/gothinkster/react-redux-realworld-example-app.git
cd ..
```
