# IA = Ingénieur Augmenté / Ingénieur Aliéné

Contexte de conception et de facilitation d'un atelier/conférence.

Objectif : faire vivre, sur une même codebase et tous ensemble, deux manières
d'utiliser l'IA, en deux phases successives.

- **Phase 1 — capitulation** : on descend un backlog le plus vite possible, on
  délègue à l'agent, la revue devient de plus en plus superficielle.
- **Phase 2 — augmentation** : sur la même codebase, on reprend ce qui a été
  livré et on l'attaque sous tous les angles avec l'IA, en gardant le jugement.

Il n'y a pas deux groupes et pas d'inversion. Tout le monde vit les deux phases
en même temps, en binômes ou petites équipes. Le contraste se joue avant/après,
dans la tête de chaque participant.

## Les deux repos

Ce repo (`conf`) contient **uniquement le contexte facilitateur** : conception,
phénomènes cognitifs, runbook, quiz, fiche d'angles. À ne pas exposer aux
participants.

Le **matériel remis aux participants** — `setup.md`, `backlog.md`, les apps
RealWorld vendorisées sous `app/`, le `install.sh` — vit dans un repo distinct :

- En ligne : https://github.com/FlorisTisseyre/atelier
- En local : `../atelier` (à côté de ce repo)

## Carte de lecture

### `docs/run/` — le jour J (un fichier par étape, ouverts dans l'ordre)

Commence par [`docs/run/README.md`](docs/run/README.md) : déroulé minuté + index.
Puis tu ouvres chaque fichier numéroté au moment où tu attaques l'étape
(`00-accueil` → `06-debrief-phase2`). `03-quiz` et `05-fiche-angles`
sont les deux supports (quiz Kahoot facilitateur, fiche remise aux participants).

### `docs/design/` — le pourquoi (matière conférence, pas nécessaire en live)

| Doc | Rôle |
| --- | --- |
| [`experience-design.md`](docs/design/experience-design.md) | Ce que l'expérience démontre : thèse, hypothèses, mécanismes, critères de réussite/échec. La référence canonique du « pourquoi ». |
| [`cognitive-phenomena.md`](docs/design/cognitive-phenomena.md) | Le cœur intellectuel : phénomènes cognitifs individuels (ch. 1) et collectifs (ch. 2). |
| [`codebase-selection.md`](docs/design/codebase-selection.md) | Pourquoi RealWorld/Conduit, et la feature pivot (les brouillons). |


## Initialisation

```bash
git clone git@github-perso:FlorisTisseyre/conf.git
git clone git@github-perso:FlorisTisseyre/atelier.git
```

Les deux apps RealWorld sont vendorisées (committées) dans le repo `atelier`,
sous `app/`. Son `install.sh` ne clone rien : il installe les dépendances du
front et vérifie que le back compile.
