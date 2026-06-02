# IA = Ingénieur Augmenté / Ingénieur Aliéné

Ce dossier contient le contexte de conception d’un atelier/conférence.

Objectif : concevoir une expérience pratique où deux groupes utilisent l’IA différemment :
- un groupe optimise la vitesse de production ;
- un groupe optimise l’apprentissage et la compréhension.

Les groupes inversent ensuite leurs rôles.

Le support technique envisagé est RealWorld :
- spring-boot-realworld-example-app
- react-redux-realworld-example-app

## Initialisation du projet

Les deux apps RealWorld ne sont pas versionnées dans ce repo (ce sont des repos
externes). Après avoir cloné ce repo, clone-les à l'intérieur :

```bash
git clone git@github-perso:FlorisTisseyre/conf.git
cd conf
git clone https://github.com/gothinkster/spring-boot-realworld-example-app.git
git clone https://github.com/gothinkster/react-redux-realworld-example-app.git
```
