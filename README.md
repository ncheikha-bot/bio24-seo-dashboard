# Tableau de bord SEO / GEO — Laboratoire Bio 24

Page web autonome (un seul fichier `index.html`, sans dépendance) qui affiche le suivi SEO/GEO de labobio24.com.

## Déployer sur GitHub Pages

1. **Créer un dépôt** (ex. `bio24-seo-dashboard`) sur github.com.
2. **Y déposer les fichiers** de ce dossier (`index.html` suffit) :
   ```bash
   git init
   git add index.html README.md
   git commit -m "Tableau de bord SEO Bio 24"
   git branch -M main
   git remote add origin https://github.com/<votre-compte>/bio24-seo-dashboard.git
   git push -u origin main
   ```
3. **Activer Pages** : dépôt → **Settings › Pages** → *Source* = `Deploy from a branch` → Branch `main` / dossier `/root` → **Save**.
4. Au bout d'une minute, le tableau est en ligne sur `https://<votre-compte>.github.io/bio24-seo-dashboard/`.

> Astuce : pour une URL plus courte, nommez le dépôt `<votre-compte>.github.io` (il sera servi à la racine).

## Mettre à jour les chiffres chaque semaine

Tout le contenu vit dans un seul objet **`DATA`** en haut du `<script>` de `index.html`.
Modifiez les valeurs (statuts, positions, journal, cases Search Console), commitez, poussez — Pages se met à jour tout seul.

- La routine automatique `suivi-seo-bio24-hebdo` (lundi 8h) régénère le journal texte
  dans `../journal.md` ; reportez son résumé dans `DATA` puis poussez.
- Les 3 chiffres **Search Console** (Impressions / Clics / Position moyenne) se relèvent
  manuellement dans l'onglet *Performances* de Google Search Console.

## Notes techniques
- 100 % statique, aucune librairie externe, aucun traceur → se déploie partout (GitHub Pages, Netlify, un simple hébergement).
- Thème clair/sombre automatique (suit le système) + bouton de bascule.
- Responsive (mobile, tablette, desktop).
