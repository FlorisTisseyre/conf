# IA = Ingénieur Augmenté / Ingénieur Aliéné

Ce dossier contient le contexte de conception d’un atelier/conférence.

Objectif : faire vivre, sur une même codebase et tous ensemble, deux manières
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

## L'atelier (repo participant)

Ce repo (`conf`) contient uniquement le contexte de conception et de
facilitation. Le matériel remis aux participants — `setup.md`, `backlog.md`,
les apps RealWorld dans `app/`, le script d'installation — vit dans un repo
distinct :

- En ligne : https://github.com/FlorisTisseyre/atelier
- En local : `../atelier` (à côté de ce repo)

## Structure

- `docs/` — conception et facilitation. Réservé au facilitateur, à ne pas
  exposer aux participants.
- La fiche d'angles de la phase 2 vit dans `docs/facilitation-guide.md`
  (facilitateur). Le `setup.md` et le `backlog.md` côté participant sont dans
  le repo `atelier` (voir ci-dessus).

## Initialisation du projet

```bash
git clone git@github-perso:FlorisTisseyre/conf.git
git clone git@github-perso:FlorisTisseyre/atelier.git
```

Les deux apps RealWorld sont vendorisées (committées) dans le repo `atelier`,
sous `app/`. Son `install.sh` ne clone rien : il installe les dépendances du
front et vérifie que le back compile.
