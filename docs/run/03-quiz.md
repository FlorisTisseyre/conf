# 03 · Quiz — débrief phase 1

Support facilitateur. **Ne pas montrer avant le débrief.** Lancé entre le ressenti
et le re-ressenti (voir [`02`](02-debrief-phase1.md)). Kahoot, individuel, ~9 Q, ~5 min.

- **Partie 1** (scorée) : compréhension du système. Commune à tous.
- **Partie 2** (sondage, non scoré) : ce que fait *leur* code. « Je ne sais pas » toujours proposé.

---

## Partie 1 — Compréhension *(✓ = bonne réponse)*

**Q1. Un article publié devient visible où dans Conduit ?** *(plusieurs réponses)*
Feed global ✓ · Liste par tag ✓ · Accès direct par URL/slug ✓ · Page des paramètres du compte

**Q2. Où est filtrée la liste du feed, côté back ?** *(une réponse)*
Composant React · **Requête / mapper côté base ✓** · Nulle part · Fichier de config

**Q3. Le slug d'un article est :** *(une réponse)*
**Généré à partir du titre ✓** · UUID aléatoire · L'id numérique en base · Saisi à la main

**Q4. Comment le back authentifie un endpoint protégé ?** *(une réponse)*
**Token JWT dans l'en-tête Authorization ✓** · Session serveur en base · Cookie auto navigateur · Rien

**Q5. Côté front, une fois connecté, le token est conservé :** *(une réponse)*
**Dans le localStorage ✓** · En mémoire React (perdu au refresh) · Cookie httpOnly du back · Pas conservé

---

## Partie 2 — Votre solution *(sondage, sans bonne réponse)*

**Q6. Un brouillon apparaît-il dans le feed global ?**
Oui · Non · Je ne sais pas · Pas de brouillon qui tourne

**Q7. … dans la liste par tag ?**
Oui · Non · Je ne sais pas

**Q8. … visible par un autre utilisateur qui a son URL ?**
Oui · Non · Je ne sais pas

**Q9. Confiance que votre visibilité est correcte ?** *(échelle 1–5)*

---

## Lire les résultats *(sur la salle, jamais en désignant quelqu'un)*

- **Q1 + Q3 ratées** = transversalité de la visibilité pas vue.
- **Q4 + Q5** : modèle du système, valable même sans avoir touché aux brouillons.
- **Taux de « je ne sais pas »** (P2) = signal le plus honnête d'absence de modèle mental.
- **Croisement clé : Q9 confiance élevée + « je ne sais pas » = surestimation.**
