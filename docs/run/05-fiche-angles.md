# 05 · Fiche d'angles — Phase méta-cognition *(remise aux participants)*

> Remise **au lancement de la phase méta-cognition, pas avant.**

Même produit, même code — mais l'objectif n'est plus le débit. Vous reprenez ce
qui a été livré et vous l'attaquez sous tous les angles avec l'IA, pour
**comprendre, dérisquer, décider**.

**La posture : méta-cognition** — *se regarder penser pendant qu'on agit*.
Reprenez la position de l'ingénieur : « comment je m'y prends, est-ce le bon
chemin, qu'est-ce que je n'ai pas encore exploré ? » L'IA est un expert
tous-domaines ; servez-vous-en pour ouvrir les possibles **et apprenez au passage**.

**La règle :** à chaque sortie d'agent, *vous* tranchez. L'agent élargit ce que
vous voyez ; il ne décide pas à votre place.

---

## Les angles *(piochez, combinez, lancez en parallèle, puis synthétisez vous-mêmes)*

**Comprendre le système**
- Cartographier l'architecture (back + front) et le flux d'une feature de bout en bout.
- Faire expliquer un bout de code de la phase delivery, puis demander à l'agent de **vous interroger** dessus.
- Retracer où un article devient visible : feed, tag, profil, URL, favoris.

**Découvrir le métier**
- Faire expliciter les règles métier implicites et les invariants.
- « Qu'est-ce qu'un vrai Medium ferait ici que notre version ne fait pas ? »

**État de l'art**
- Recherche web sur les patterns du domaine : brouillon/publication, visibilité, soft-delete, slug stable.
- Comparer votre livraison à ces patterns.

**Risques & criticité**
- Criticité et risques des modifs de la phase delivery.
- Lister les fuites : qu'est-ce qui apparaît là où ça ne devrait pas ? Qu'est-ce qui casse si on renomme / archive / bloque ?
- Chercher les régressions.

**Revue**
- Agent de revue sur le diff de la phase delivery.
- Agent qualité : lisibilité, duplication, cohérence.
- Agent sécurité / droits : qui peut voir ou modifier quoi ?

**Preuve par les tests**
- Générer des tests qui **prouvent** un comportement ou **révèlent** une fuite. Faire tourner, lire, décider.

---

## Le fil rouge — à la fin, sachez dire :

- ce qui est **risqué**, et pourquoi ;
- ce que vous **corrigeriez en premier** ;
- ce que vous avez **compris que vous ne compreniez pas** en phase delivery.
