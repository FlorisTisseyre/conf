# Exercice 1 — Brouillons d'articles

## Le produit

Conduit est un clone de Medium : les utilisateurs publient des articles, les
commentent, les mettent en favori, suivent d'autres auteurs.

Aujourd'hui, quand un auteur écrit un article, il est publié immédiatement. Il
n'y a pas d'étape intermédiaire.

## La demande

On veut permettre à un auteur d'enregistrer un article en **brouillon** avant
de le publier.

Concrètement, l'auteur doit pouvoir :

- écrire un article et le sauvegarder en brouillon sans le publier ;
- retrouver ses brouillons ;
- publier un brouillon quand il est prêt.

C'est tout ce que le porteur du besoin a formulé. À vous de livrer une version
qui tient la route.

## Périmètre

Vous travaillez sur l'application complète, dans `app/` :

- `app/spring-boot-realworld-example-app` — le backend (Spring Boot) ;
- `app/react-redux-realworld-example-app` — le frontend (React/Redux).

La feature peut toucher les deux côtés. Répartissez-vous selon vos affinités.

## Mise en route

Le setup (lancer le back, le front, installer Claude Code) est décrit dans
`SETUP.md` à la racine.

Lancez Claude Code depuis `app/` pour qu'il voie le front et le back :

```bash
cd app
claude
```

## Contrainte de temps

Vous avez un temps limité (le facilitateur l'annonce). Visez quelque chose de
démontrable à la fin du créneau.

## Rendu attendu

À la fin, vous devez pouvoir montrer la feature en marche et expliquer ce que
vous avez fait.
```
