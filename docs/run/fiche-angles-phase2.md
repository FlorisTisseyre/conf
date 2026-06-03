# Fiche d'angles — Phase 2 (support participant)

C'est le support remis aux participants pour la phase 2. Tu le distribues **au
lancement de la phase 2, pas avant**. Le runbook qui encadre sa remise est dans
[`facilitation-guide.md`](facilitation-guide.md).

## Le principe

Même produit, même code. Mais cette fois, l'objectif n'est plus le débit.

Vous reprenez ce que l'équipe vient de livrer en phase 1 et vous l'attaquez sous
tous les angles avec l'IA. Le but : comprendre, dérisquer, décider.

Une règle tient toute la phase : à chaque sortie d'agent, c'est vous qui
tranchez. Vous ne tamponnez pas. L'agent élargit ce que vous voyez ; il ne
décide pas à votre place.

## La différence avec la phase 1

En phase 1, vous demandiez à l'agent de produire et vous validiez vite. Ici,
vous lui demandez de vous rendre plus lucides, et vous gardez le jugement.
Mêmes outils. Intention opposée.

## La fiche d'angles

Piochez, combinez, lancez plusieurs pistes en parallèle. Puis synthétisez
vous-mêmes.

### Comprendre le système

- Faire cartographier l'architecture (back + front) et le flux d'une feature de
  bout en bout.
- Faire expliquer un morceau de code livré en phase 1, puis demander à l'agent
  de VOUS interroger dessus pour tester ce que vous avez vraiment compris.
- Retracer où un article devient visible : feed, tag, profil, URL directe,
  favoris.

### Découvrir le métier

- Faire expliciter les règles métier implicites et les invariants du produit.
- Demander : qu'est-ce qu'un vrai Medium ferait ici que notre version ne fait
  pas ?

### État de l'art

- Lancer une recherche web sur les patterns du domaine : brouillon/publication,
  gestion de visibilité, archivage / soft-delete, slug stable.
- Comparer ce que vous avez livré à ces patterns.

### Risques et criticité

- Demander la criticité et les risques des modifs de la phase 1.
- Faire lister les fuites possibles : qu'est-ce qui apparaît là où ça ne devrait
  pas ? Qu'est-ce qui casse si on renomme, archive, bloque ?
- Faire chercher les régressions introduites.

### Revue

- Lancer un agent de revue de code sur le diff de la phase 1.
- Lancer un agent qualité : lisibilité, duplication, cohérence.
- Lancer un agent sécurité / droits d'accès : qui peut voir ou modifier quoi ?

### Preuve par les tests

- Faire générer des tests qui PROUVENT un comportement attendu, ou qui RÉVÈLENT
  une fuite.
- Faire tourner, lire les résultats, décider quoi corriger.

### Paralléliser

- Lancez plusieurs de ces analyses en même temps (plusieurs agents ou onglets).
- Le travail à forte valeur, c'est ce que vous faites de leurs sorties :
  arbitrer, recouper, prioriser.

## Le fil rouge

À la fin, vous devez pouvoir dire, sur ce que l'équipe a livré :

- ce qui est risqué, et pourquoi ;
- ce que vous corrigeriez en premier ;
- ce que vous avez compris que vous ne compreniez pas en phase 1.
