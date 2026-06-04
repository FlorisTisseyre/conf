# 03 · Quiz — débrief delivery

Support facilitateur. **Ne pas montrer avant le débrief.** Kahoot, individuel, ~12 Q.
Ordre voulu : **production → ressenti → compréhension → solution**.

- **Parties 1-2** : déclaratif (production, ressenti). Ouvrent le quiz, non scorées.
- **Partie 3** (scorée) : compréhension du système. Commune à tous.
- **Partie 4** (sondage, non scoré) : ce que fait *leur* code. « Je ne sais pas » toujours proposé.

---

## Partie 1 — Production *(déclaratif, ouvre le quiz)*

**Q1. Combien de tickets avez-vous **finalisés** (ça marche + démontrable) ?** *(une réponse)*
0 · 1–2 · 3–4 · 5–6 · 7+

**Q2. Combien en avez-vous **analysés ou démarrés en plus**, sans les finir ?** *(une réponse)*
0 · 1–2 · 3–4 · 5+

## Partie 2 — Ressenti à chaud

**Q3. Là, tout de suite, vous vous sentez plutôt :** *(une réponse)*
Lancé / productif · Confiant · Dans le flou · Frustré · Épuisé

---

## Partie 3 — Compréhension *(✓ = bonne réponse)*

**Q4. Un article publié devient visible où dans Conduit ?** *(plusieurs réponses)*
Feed global ✓ · Liste par tag ✓ · Accès direct par URL/slug ✓ · Page des paramètres du compte

**Q5. Où est filtrée la liste du feed, côté back ?** *(une réponse)*
Composant React · **Requête / mapper côté base ✓** · Nulle part · Fichier de config

**Q6. Le slug d'un article est :** *(une réponse)*
**Généré à partir du titre ✓** · UUID aléatoire · L'id numérique en base · Saisi à la main

**Q7. Comment le back authentifie un endpoint protégé ?** *(une réponse)*
**Token JWT dans l'en-tête Authorization ✓** · Session serveur en base · Cookie auto navigateur · Rien

**Q8. Côté front, une fois connecté, le token est conservé :** *(une réponse)*
**Dans le localStorage ✓** · En mémoire React (perdu au refresh) · Cookie httpOnly du back · Pas conservé

---

## Partie 4 — Votre solution *(sondage, sans bonne réponse)*

**Q9. Un brouillon apparaît-il dans le feed global ?**
Oui · Non · Je ne sais pas · Pas de brouillon qui tourne

**Q10. … dans la liste par tag ?**
Oui · Non · Je ne sais pas

**Q11. … visible par un autre utilisateur qui a son URL ?**
Oui · Non · Je ne sais pas

**Q12. Confiance que votre visibilité est correcte ?** *(échelle 1–5)*

---

## Lire les résultats *(sur la salle, jamais en désignant quelqu'un)*

- **Production (Q1 vs Q2)** : beaucoup de finalisés + peu d'analysés-en-plus = **signature du délestage** (on a produit, pas exploré). À recroiser en fin de phase méta-cognition.
- **Q4 + Q6 ratées** = transversalité de la visibilité pas vue.
- **Q7 + Q8** : modèle du système, valable même sans avoir touché aux brouillons.
- **Taux de « je ne sais pas »** (P4) = signal le plus honnête d'absence de modèle mental.
- **Croisement clé : Q12 confiance élevée + « je ne sais pas » = surestimation.**
