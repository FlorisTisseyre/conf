# 03 · Quiz — débrief delivery

Support facilitateur. **Ne pas montrer avant le débrief.** Kahoot, individuel, ~11 Q.
Ordre voulu : **production → ressenti → compréhension produit → leur code**.

- **Parties 1-2** : déclaratif (production, ressenti). Ouvrent le quiz, non scorées.
- **Partie 3** (scorée) : compréhension du *produit / système*. Commune à tous.
  Volontairement sur le **non-évident** — pas de la trivia RealWorld qu'on récite sans avoir regardé.
- **Partie 4** (sondage, non scoré) : ce que fait *leur* code. « Je ne sais pas » toujours proposé.

> ⚙ **Compatibilité Kahoot** : **max 4 réponses** par question (respecté ci-dessous),
> **pas de mise en forme** (le gras/italique du doc est pour toi, à ne pas recopier).
> Types à choisir : production / ressenti / partie 4 = **Sondage** (non scoré) ·
> Q4 = **Quiz à plusieurs bonnes réponses** · le reste de la P3 = **Quiz** classique ·
> les échelles sont ramenées à **4 niveaux** (le slider 1–5 est payant).

---

## Partie 1 — Production *(déclaratif, ouvre le quiz)*

**Q1. Combien de tickets avez-vous **finalisés** (ça marche + démontrable) ?** *(une réponse)*
0 · 1–2 · 3–4 · 5+

**Q2. Combien en avez-vous **analysés ou démarrés en plus**, sans les finir ?** *(une réponse)*
0 · 1–2 · 3–4 · 5+

## Partie 2 — Ressenti à chaud

**Q3. Là, tout de suite, vous vous sentez plutôt :** *(une réponse)*
Productif / confiant · Dans le flou · Frustré · Épuisé

> 🔁 On **repose** la jauge de ressenti de Q3 en fin de méta-cognition, orientée futur
> (voir [`06`](06-debrief-phase2.md)) — garde le résultat de Q3 pour montrer le chemin parcouru.
> La clôture du quiz (**Q11**) pose une question distincte : *où ce mode nous mène*.

---

## Partie 3 — Compréhension du produit *(✓ = bonne réponse)*

**Q4. Un article publié devient visible où dans Conduit ?** *(plusieurs réponses)*
Feed global ✓ · Profil de l'auteur ✓ · Accès direct par URL/slug ✓ · Liste par tag

> 🪤 **Piège (à révéler au débrief)** : presque tout le monde coche « liste par tag ».
> Or le système de tags **ne persiste rien** (table `tags` vide → bug B5) : un article
> n'est *jamais* atteignable par tag. On suppose que le produit marche sans l'avoir vérifié.
> Les bonnes réponses sont les **trois autres surfaces** — d'où la transversalité de la visibilité.

**Q5. Où est filtrée la liste des articles (feed global et « Your Feed ») ?** *(une réponse)*
Dans un composant React, côté front · **Dans les requêtes SQL MyBatis (`ArticleReadService.xml`) ✓** · Nulle part, tout est renvoyé · Dans la config Spring

> Le filtrage (tag, auteur, favoris, auteurs suivis) vit dans les requêtes SQL, orchestrées
> par `ArticleQueryService`. Pour cacher un brouillon, il faut **modifier ces requêtes**
> (et leurs équivalents GraphQL) — pas juste poser un flag côté objet.

**Q6. Quand le back liste les articles, qu'est-ce qui détermine si vous avez le droit d'en voir un ?** *(une réponse)*
**Rien : tout article en base est public ✓** · Le token JWT · Un champ de visibilité en base · Les droits liés au profil

> Le produit n'a **aucune notion de « qui peut lire »** : tout article en base est servi.
> C'est *pour ça* qu'un simple booléen `draft` est condamné à fuiter.

---

## Partie 4 — Votre code *(sondage, sans bonne réponse)*

**Q7. Votre brouillon : où avez-vous **vérifié** qu'il n'apparaît pas ?**
Partout (feed, profil, favoris, URL, GraphQL) · Sur le feed seulement · Pas vérifié / le flag suffit · Pas de brouillon qui tourne

**Q8. Pour la feature brouillons (F1), avez-vous fait évoluer l'API **GraphQL** ?**
Oui · Non · « Il y a du GraphQL ?! » · Je ne sais pas

> Le front livré n'utilise **que** REST. Mais une API GraphQL complète (`/graphql`) sert
> les mêmes articles en parallèle : si la feature n'y touche pas, le brouillon y reste
> public. Angle mort quasi total — c'est le révélateur le plus fort de la P4.

**Q9. Combien de bugs ou d'incohérences avez-vous repérés dans la codebase ?**
0 · 1–2 · 3–5 · 6+

**Q10. Êtes-vous sûr que personne d'autre ne peut voir vos brouillons ?**
Certain · Plutôt confiant · Pas sûr · Je ne sais pas

## Clôture — où nous mène ce mode ?

**Q11. Ce mode « delivery » nous mène-t-il vers un avenir souhaitable ?** *(sondage)*
Oui, livrer c'est notre métier · Oui, de toute façon on n'a pas le choix · Non, on va perdre notre travail · Non, on va perdre notre pensée critique

---

## Lire les résultats *(sur la salle, jamais en désignant quelqu'un)*

- **Production (Q1 vs Q2)** : beaucoup de finalisés + peu d'analysés-en-plus = **signature du délestage** (on a produit, pas exploré). À recroiser en fin de phase méta-cognition.
- **Q4** : le taux de « liste par tag » coché = on a **supposé** que le produit marchait. Personne n'a vu que les tags sont cassés (B5) → on n'a pas regardé. Les trois vraies surfaces posent la **transversalité de la visibilité**.
- **Q5 + Q6** : modèle du système. Rater Q5 = on croit qu'un flag objet suffit (alors que le filtrage est en SQL) ; rater Q6 = on ignore qu'il n'y a **aucun contrôle de lecture**. Les deux expliquent pourquoi un brouillon fuite.
- **Q7 + Q8** = le cœur. « Vérifié partout » (Q7) **mais** « il y a du GraphQL ?! » (Q8) = on n'a *pas* vérifié partout sans le savoir.
- **Q9** : un faible nombre face à une codebase qui regorge de défauts (5 bugs au backlog + incohérences) = **défaut d'attention**, pas de la chance.
- **Croisement clé — surestimation rendue visible** : Q10 « certain » + (Q8 « il y a du GraphQL ?! » **ou** Q7 « feed seulement ») = on est sûr d'un code dont on ne connaît pas la moitié des surfaces.
- **Taux de « je ne sais pas »** (P4) = le signal le plus honnête d'absence de modèle mental.
- **Q11 (clôture)** : où ce mode nous mène. Les deux « oui » (*c'est notre métier* / *pas le choix*) sont les **rationalisations** du délestage ; les deux « non » nomment l'enjeu — « perdre notre travail » est la peur naïve de l'IA, **« perdre notre pensée critique » est la vraie cible** (capitulation cognitive → pôle aliéné, qu'on nommera en [`06`](06-debrief-phase2.md)). Ne tranche pas ici : laisse la distribution ouvrir le pivot. Si le « non, pensée critique » domine, le groupe a fait le travail tout seul.

> Tu ne conclus jamais « untel a mal fait ». Tu montres que **produire vite ≠ savoir ce qu'on a produit** — ni le produit en dessous, ni le code posé par-dessus.
