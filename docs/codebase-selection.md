# codebase-selection.md

# Sélection de la codebase support

## Pourquoi une codebase, pas un benchmark

La codebase ne sert pas à mesurer les performances d'un LLM. Elle sert à révéler
la différence entre obtenir une solution et construire un modèle mental du
système.

Elle doit permettre une implémentation superficielle qui semble correcte, mais
qui échoue dès qu'une nouvelle contrainte apparaît.

---

# Critères

- compréhensible rapidement ;
- réaliste, front + back ;
- assez petite pour être explorée en atelier ;
- assez riche pour contenir des implications cachées ;
- exécutable facilement en local ;
- modifiable sur plusieurs couches ;
- compatible avec une feature apparemment simple mais réellement transverse.

---

# Support retenu : RealWorld (Conduit)

- spring-boot-realworld-example-app pour le backend (Spring Boot, Java 21, MyBatis) ;
- react-redux-realworld-example-app pour le frontend (React / Redux).

Clone de Medium standardisé : utilisateurs, authentification, articles,
commentaires, profils, favoris, tags. Domaine compréhensible vite, application
complète, taille raisonnable, architecture assez riche pour exiger de la
compréhension.

C'est exactement le type de contexte où l'IA produit rapidement une solution qui
semble correcte tout en masquant une incompréhension du système.

Le repo participant (`../atelier`, https://github.com/FlorisTisseyre/atelier) est
la version préparée et figée : les deux apps y sont vendorisées sous `app/`,
`install.sh` installe les deps, `setup.md` documente le lancement (back `:8080`,
front `:4100`). La friction technique des repos RealWorld bruts (dépendances
datées, Redux pré-hooks, setup fragile) y est neutralisée en amont.

---

# La feature pivot : les brouillons

Les brouillons sont l'item 1 du backlog (`atelier/backlog.md`), placé en tête et
abordé en premier (consigne « de haut en bas ») pour qu'ils soient l'item le plus
probablement traité. C'est sur eux que s'appuie le quiz du débrief
(`docs/quiz-phase1.md`).

Chemin naïf : un booléen draft / published, « ça marche ».

Chemin profond : les règles de visibilité implicites —

> Un brouillon est visible par son auteur dans son profil, mais invisible pour
> les autres utilisateurs. Il n'apparaît jamais dans le feed global ni dans les
> résultats par tag. Il peut être publié sans changer d'URL.

C'est ce qui teste si les participants ont compris les règles de visibilité, les
routes, les filtres, les queries, le modèle de domaine et les impacts front/back.

Le piège « quelque chose apparaît là où il ne devrait pas » n'est pas propre aux
brouillons : il se rejoue dans d'autres items du backlog (articles réservés aux
abonnés, archivage, blocage). Les brouillons en sont seulement l'exemple le plus
propre, d'où leur place en tête.
