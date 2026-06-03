# Quizz — Exercice 1 (Brouillons)

Document facilitateur. Ne pas exposer aux participants : la clé de réponses et
la grille révèlent une partie de la modif surprise.

## Ce que ce quizz mesure (et ce qu'il ne mesure pas)

Il ne dit pas qui est "augmenté" ou "aliéné". On ne le devient pas en un
exercice. Il fait sentir une direction : vers quoi le comportement de chacun
l'a incliné pendant la phase 1. À répéter aux participants avant et après.

Deux parties :

- Partie 1 — Compréhension du système. Factuel, commun à tous, indépendant de
  ce qu'ils ont codé. Mesure le modèle mental brut.
- Partie 2 — Comportement de votre solution. Autoévaluation. Ils s'engagent sur
  ce que leur code fait, avec un "je ne sais pas" assumé.

## Format

- Outil : Kahoot. Individuel.
- ~7 questions, 3-4 min.
- Dégainé juste avant la modif surprise (capture l'état "je crois que c'est
  bon"). Les bonnes réponses de la partie 1 portent sur le système existant,
  pas sur la contrainte surprise : ça ne spoile pas.
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

Ce qu'on cherche : comprennent-ils que le slug dérive du titre. C'est ce qui
rendra "publier sans changer l'URL" non trivial — sans le dire encore.

---

# Partie 2 — Comportement de votre solution (sondage, non scoré)

Pas de bonne réponse : ils déclarent ce que fait leur code. En Kahoot, monter
ces slides en "sondage" (sans points). Le "je ne sais pas" doit toujours être
proposé.

## Q4. Avec votre implé actuelle, un brouillon apparaît-il dans le feed global ?

- Oui
- Non
- Je ne sais pas
- On n'a pas encore de brouillon qui tourne

## Q5. ... apparaît-il dans la liste par tag ?

- Oui
- Non
- Je ne sais pas

## Q6. ... est-il visible par un autre utilisateur qui a son URL ?

- Oui
- Non
- Je ne sais pas

## Q7. Confiance : à quel point êtes-vous sûr que votre visibilité est correcte ?

(échelle, sans bonne réponse)

- 1 — pas du tout
- 2
- 3
- 4
- 5 — totalement sûr

---

# Grille de lecture au récap

À comparer entre groupes, sans désigner de gagnant.

- Partie 1 : score moyen par groupe = niveau de modèle mental. Regarde surtout
  Q1 (les portes de visibilité) et Q3 (le slug). Les rater, c'est ne pas avoir
  vu la transversalité.
- Partie 2 : le taux de "je ne sais pas" est le signal le plus honnête d'une
  absence de modèle mental. Ne pas savoir ce que fait son propre code en dit
  long.
- Croisement clé : confiance (Q7) élevée + beaucoup de "je ne sais pas" ou
  d'autoéval qu'on sait fausse = surestimation. C'est H6 de experience-design,
  rendu visible et chiffré.
- Pour percer les "Non, ça ne fuite pas" qui sont faux : 1 ou 2 vérifications
  live au curl sur le back d'un groupe. "Vous avez dit non, on regarde ?". Ça
  suffit à rendre le réel tangible sans suite de tests automatisée.

Tu ne conclus pas "ce groupe est meilleur". Tu montres que produire vite et
savoir ce qu'on a produit ne vont pas automatiquement ensemble.
