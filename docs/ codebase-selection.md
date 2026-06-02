# codebase-selection.md

# Sélection de la codebase support

## Objectif

Choisir une codebase qui permette de faire vivre la tension centrale de l'atelier :

- produire vite avec l'IA ;
- comprendre durablement avec l'IA.

La codebase ne doit pas servir à mesurer les performances d'un LLM.

Elle doit servir à révéler la différence entre :

- obtenir une solution ;
- construire un modèle mental du système.

---

# Critères de sélection

Une bonne codebase pour l'atelier doit être :

- compréhensible rapidement ;
- suffisamment réaliste ;
- suffisamment petite pour être explorée en atelier ;
- suffisamment riche pour contenir des implications cachées ;
- exécutable facilement en local ;
- modifiable sur plusieurs couches ;
- compatible avec une feature apparemment simple mais réellement transverse.

Elle doit permettre une implémentation superficielle qui semble correcte, mais qui échoue lorsqu'une nouvelle contrainte apparaît.

---

# Options envisagées

## DeepSWE

DeepSWE est intéressant parce qu'il s'appuie sur des tâches proches du travail logiciel réel.

Mais il a été écarté comme support brut pour l'atelier.

Raisons :

- conçu pour évaluer des agents, pas pour faciliter une expérience pédagogique ;
- risque de tâches trop longues ;
- risque de complexité excessive ;
- risque de transformer l'atelier en compétition de coding agents ;
- moins de contrôle sur les phénomènes cognitifs observés.

DeepSWE peut rester utile comme source d'inspiration pour trouver des types de tâches.

---

## SWE-Bench

SWE-Bench est également intéressant car il repose sur de vrais bugs issus de projets open source.

Mais il présente des limites similaires.

Raisons :

- tâches souvent orientées bugfix ;
- contexte parfois difficile à comprendre rapidement ;
- forte dépendance au projet choisi ;
- risque de mesurer la capacité à appliquer un patch plutôt que la capacité à apprendre.

SWE-Bench peut servir de banque d'exemples, mais pas nécessairement de support principal.

---

## Codebase artificielle sur mesure

Créer une codebase dédiée serait idéal du point de vue pédagogique.

Avantages :

- contrôle total du domaine ;
- contrôle total des pièges ;
- possibilité de créer une progression parfaite ;
- alignement précis avec le message de la conférence.

Limites :

- coût de conception ;
- risque d'artificialité ;
- nécessité de maintenir une cohérence suffisante pour être crédible.

Cette option reste intéressante, mais pas prioritaire pour une première version de l'atelier.

---

# Option retenue : RealWorld

Support envisagé :

- spring-boot-realworld-example-app pour le backend ;
- react-redux-realworld-example-app pour le frontend.

RealWorld est un clone de Medium standardisé.

Le domaine métier contient notamment :

- utilisateurs ;
- authentification ;
- articles ;
- commentaires ;
- profils ;
- favoris ;
- tags.

---

# Pourquoi RealWorld est un bon support

RealWorld présente un bon équilibre entre simplicité et réalisme.

## Avantages

- domaine compréhensible rapidement ;
- application complète ;
- front + back ;
- API identifiable ;
- architecture suffisamment riche ;
- taille raisonnable ;
- nombreuses features possibles ;
- possibilité de travailler en full-stack ;
- contexte plus réaliste qu'un kata isolé.

## Intérêt pédagogique

RealWorld permet de créer des features qui semblent simples mais touchent plusieurs dimensions :

- modèle de données ;
- API ;
- règles métier ;
- interface ;
- tests ;
- droits utilisateur ;
- visibilité publique ou privée.

C'est exactement le type de contexte où l'IA peut produire rapidement une solution qui semble correcte tout en masquant une incompréhension du système.

---

# Limites de RealWorld

Les repositories RealWorld disponibles peuvent être anciens.

Risques :

- dépendances obsolètes ;
- stack front ancienne ;
- Redux pré-hooks / pré-Redux Toolkit ;
- conventions datées ;
- setup local potentiellement fragile ;
- friction technique parasite.

Ces limites ne sont pas forcément bloquantes, mais elles doivent être maîtrisées avant l'atelier.

---

# Recommandation

Ne pas utiliser les repositories bruts.

Créer un fork préparé.

Le fork doit :

- démarrer facilement ;
- contenir des instructions claires ;
- avoir un jeu de données minimal ;
- avoir quelques tests prêts ;
- éviter les problèmes d'environnement ;
- contenir une branche de départ propre ;
- contenir éventuellement une branche solution pour le facilitateur.

---

# Features candidates

## Feature 1 — Drafts d'articles

Ajouter la possibilité de créer des articles en brouillon.

Questions métier :

- un draft est-il visible publiquement ?
- apparaît-il dans le profil auteur ?
- peut-il être favori ?
- peut-il recevoir des commentaires ?
- peut-il être publié ensuite ?
- peut-il redevenir draft ?
- qui peut le voir ?
- comment l'API expose-t-elle cet état ?

Pourquoi c'est intéressant :

- feature apparemment simple ;
- impacts transverses ;
- forte ambiguïté métier ;
- bon révélateur de compréhension.

C'est la feature candidate principale.

---

## Feature 2 — Modération des commentaires

Ajouter un rôle moderator qui peut supprimer des commentaires.

Questions métier :

- qui peut supprimer quoi ?
- l'auteur peut-il toujours supprimer son commentaire ?
- un moderator peut-il supprimer les commentaires de tous les articles ?
- faut-il conserver une trace ?
- suppression physique ou logique ?
- impact sur le front ?

Intérêt :

- règles d'autorisation ;
- sécurité ;
- UI conditionnelle ;
- tests métier.

---

## Feature 3 — Articles privés

Permettre à un auteur de créer des articles privés.

Questions métier :

- différence entre private et draft ;
- visibilité ;
- partage éventuel ;
- indexation ;
- accès direct par slug ;
- API publique vs API authentifiée.

Intérêt :

- proche des drafts ;
- excellent révélateur de compréhension des règles de visibilité.

---

## Feature 4 — Temps de lecture estimé

Afficher un temps de lecture estimé pour chaque article.

Questions métier :

- calcul côté front ou back ?
- le temps dépend-il du body Markdown ou du rendu final ?
- doit-il être stocké ou calculé à la volée ?
- impact sur les listes et le détail article.

Intérêt :

- plus simple ;
- bon exercice d'échauffement ;
- moins riche cognitivement que les drafts.

---

# Feature recommandée pour l'expérience principale

La meilleure candidate est :

## Drafts d'articles

Raison principale :

Elle est assez simple pour être abordée rapidement, mais assez profonde pour révéler la différence entre :

- ajouter un champ draft;
- comprendre les règles de publication d'un système éditorial.

---

# Twist recommandé

Après une première phase de travail, introduire une nouvelle contrainte.

Exemple :

> Les drafts doivent être visibles par leur auteur dans son profil, mais invisibles pour les autres utilisateurs.  
> Ils ne doivent jamais apparaître dans le feed global, ni dans les résultats par tag.  
> Ils doivent pouvoir être publiés sans changer d'URL.

Objectif :

Tester si les participants ont compris :

- les règles de visibilité ;
- les routes ;
- les filtres ;
- les queries ;
- le modèle de domaine ;
- les impacts front/back.

---

# Ce qu'il faut observer

Pendant l'exercice, observer :

- qui demande à l'IA de coder directement ;
- qui demande à l'IA d'expliquer l'architecture ;
- qui cartographie les impacts ;
- qui écrit des tests ;
- qui valide les hypothèses métier ;
- qui identifie les cas limites ;
- qui sait expliquer la solution produite.

---

# Critère de succès de la codebase

La codebase est adaptée si elle permet d'observer clairement que :

- certains participants vont vite mais comprennent peu ;
- certains participants vont moins vite mais s'adaptent mieux au changement ;
- la modification surprise révèle l'écart de modèle mental ;
- le débat porte sur l'usage de l'IA, pas sur la difficulté technique pure.

---

# Décision actuelle

Utiliser RealWorld comme support principal, sous réserve de validation technique.

Actions à mener :

- vérifier que les deux repositories démarrent en local ;
- créer un fork stable ;
- documenter le setup ;
- choisir la feature principale ;
- préparer une branche de départ ;
- préparer une branche solution ;
- préparer une ou deux contraintes surprises ;
- préparer les questions de débriefing associées.
