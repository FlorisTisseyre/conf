# Quiz — Débrief de la phase 1

Document facilitateur. C'est l'instrument central du débrief de la phase 1 : il
rend tangible l'écart entre ce que chacun croit avoir livré et ce que son code
fait réellement. Ne pas exposer aux participants avant le débrief.

La partie 1 mesure le modèle mental du système : trois questions sur la
visibilité (proches des brouillons) et deux questions plus génériques (auth de
bout en bout) qui tiennent quel que soit l'item traité. Même un binôme qui n'a
pas touché aux brouillons est concerné. La partie 2 s'appuie sur les brouillons,
l'item le plus probablement traité ; s'ils n'y ont pas touché, elle se répond en
"on n'a pas de brouillon qui tourne".

## Ce que ce quiz mesure (et ce qu'il ne mesure pas)

Il ne dit pas qui est "augmenté" ou "aliéné". On ne le devient pas en un
exercice. Il fait sentir une direction : vers quoi le comportement de chacun
l'a incliné pendant la phase 1. À répéter aux participants en l'ouvrant.

Deux parties :

- Partie 1 — Compréhension du système. Factuel, commun à tous, indépendant de
  ce qu'ils ont codé. Mesure le modèle mental brut.
- Partie 2 — Comportement de votre solution. Autoévaluation. Ils s'engagent sur
  ce que leur code fait, avec un "je ne sais pas" assumé.

## Format

- Outil : Kahoot. Individuel.
- ~9 questions, 4-5 min.
- Dégainé en plein débrief de la phase 1, entre le ressenti à chaud et le
  re-ressenti (capture l'état "je crois que c'est bon" puis le confronte).
- Plan B si Kahoot plante : mêmes questions à l'oral, réponse à main levée.
  Moins fin mais robuste. Pour la partie 2, compter les mains qui NE se lèvent
  pas ("qui ne sait pas dire ce que fait son code ?") : c'est déjà le signal.

Note Kahoot : sers-toi de la distribution des réponses par question pour le
récap, pas du classement. Le leaderboard récompense la vitesse individuelle et
risque de recréer un "bon élève" — exactement ce qu'on veut éviter.

---

# Partie 1 — Compréhension (questions scorées)

## Q1. Un article publié devient visible à quels endroits dans Conduit ?

(plusieurs bonnes réponses)

- Dans le feed global  ✓
- Dans la liste par tag  ✓
- En accès direct par son URL / slug  ✓
- Dans la page des paramètres du compte

Ce qu'on cherche : voient-ils que la visibilité a plusieurs portes, dont
l'accès direct par slug qu'on oublie souvent.

## Q2. Où est filtrée la liste des articles renvoyée par le feed, côté back ?

(une seule réponse)

- Dans le composant React
- Dans la requête / le mapper côté base  ✓
- Nulle part : tout est renvoyé, le tri est aléatoire
- Dans un fichier de configuration

Ce qu'on cherche : savent-ils où se décide réellement la visibilité.

## Q3. Dans Conduit, le slug d'un article (son identifiant dans l'URL) est :

(une seule réponse)

- Généré à partir du titre  ✓
- Un identifiant aléatoire (UUID)
- L'id numérique en base
- Saisi à la main par l'auteur

Ce qu'on cherche : comprennent-ils que le slug dérive du titre. C'est une des
portes de visibilité qu'on oublie le plus souvent.

## Q4. Comment le back authentifie-t-il une requête sur un endpoint protégé ?

(une seule réponse)

- Un token JWT envoyé dans l'en-tête Authorization  ✓
- Une session serveur stockée en base
- Un cookie posé automatiquement par le navigateur
- Rien : tous les endpoints sont publics

Ce qu'on cherche : ont-ils un modèle de l'auth, indépendamment de l'item traité.
Question système : valable même pour un binôme qui n'a pas fait les brouillons.

## Q5. Côté front, une fois connecté, le token de l'utilisateur est conservé :

(une seule réponse)

- Dans le localStorage du navigateur  ✓
- Uniquement en mémoire React, perdu au refresh
- Dans un cookie httpOnly posé par le back
- Il n'est pas conservé, on se reconnecte à chaque page

Ce qu'on cherche : ont-ils un modèle de l'auth de bout en bout. Deuxième question
système, indépendante de l'item traité.

---

# Partie 2 — Comportement de votre solution (sondage, non scoré)

Pas de bonne réponse : ils déclarent ce que fait leur code. En Kahoot, monter
ces slides en "sondage" (sans points). Le "je ne sais pas" doit toujours être
proposé.

## Q6. Avec votre implé actuelle, un brouillon apparaît-il dans le feed global ?

- Oui
- Non
- Je ne sais pas
- On n'a pas encore de brouillon qui tourne

## Q7. ... apparaît-il dans la liste par tag ?

- Oui
- Non
- Je ne sais pas

## Q8. ... est-il visible par un autre utilisateur qui a son URL ?

- Oui
- Non
- Je ne sais pas

## Q9. Confiance : à quel point êtes-vous sûr que votre visibilité est correcte ?

(échelle, sans bonne réponse)

- 1 — pas du tout
- 2
- 3
- 4
- 5 — totalement sûr

---

# Grille de lecture au récap

Lecture sur l'ensemble de la salle, jamais en désignant quelqu'un.

- Partie 1 : la distribution des réponses = niveau de modèle mental collectif.
  Regarde surtout Q1 (les portes de visibilité) et Q3 (le slug). Les rater,
  c'est ne pas avoir vu la transversalité.
- Partie 2 : le taux de "je ne sais pas" est le signal le plus honnête d'une
  absence de modèle mental. Ne pas savoir ce que fait son propre code en dit
  long.
- Questions système (Q4 auth back, Q5 token front) : elles isolent le modèle
  mental du système de l'item traité. Les rater alors qu'on se dit confiant, c'est
  le même écart, sur un terrain que personne ne peut esquiver.
- Croisement clé : confiance (Q9) élevée + beaucoup de "je ne sais pas" ou
  d'autoéval qu'on sait fausse = surestimation. C'est H4 de experience-design,
  rendu visible et chiffré.

Tu ne conclus pas "untel a mal fait". Tu montres que produire vite et savoir ce
qu'on a produit ne vont pas automatiquement ensemble. C'est exactement ce que la
phase 2 va permettre de rattraper.
