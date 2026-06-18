# Villa Secret Harbor — site vitrine

Site vitrine one-page (haut de gamme, mobile-first) pour la **Villa Secret Harbor**, villa de prestige en location saisonnière à **Anse Marcel, Saint-Martin**.

Direction artistique & contenu : **SB Intelligence**. Réalisation : statique (HTML / CSS sur-mesure / Vanilla JS).

---

## Stack
- **HTML + CSS sur-mesure + JavaScript Vanilla** — aucun build, aucun framework. Le site s'ouvre directement.
- Libs via CDN : **Lenis** (scroll fluide), **GLightbox** (galerie lightbox), **Lucide** (icônes).
- Polices : **Fraunces** (titres) + **Inter** (texte) via Google Fonts.
- Images réelles dans `assets/photos/` (téléchargées depuis l'annonce, optimisées en `srcset` 1280 / 1920).

```
villa-secret-harbor/
├── index.html              ← page unique (sections ancrées)
├── assets/
│   ├── css/styles.css      ← direction artistique
│   ├── js/main.js          ← scroll, révélations, lightbox, menu
│   └── photos/             ← 9 images réelles + variantes -1280
└── README.md
```

## Lancer en local
Le site est statique. Au choix :
- **Double-clic** sur `index.html` (la galerie lightbox et les polices nécessitent une connexion pour les CDN).
- Ou un petit serveur local (recommandé) :
  ```bash
  cd villa-secret-harbor
  python3 -m http.server 8080
  # puis ouvrir http://localhost:8080
  ```

## Déployer
Hébergement statique gratuit, glisser-déposer du dossier :
- **Netlify** : netlify.com → « Add new site » → déposer le dossier `villa-secret-harbor/`.
- **Vercel** : `vercel` (CLI) ou import du repo Git → framework « Other ».
- **Cloudflare Pages** : connecter le repo, build command vide, output `/`.

> Après mise en ligne sur un vrai domaine, **rendre les balises Open Graph absolues** dans `index.html`
> (remplacer `assets/photos/01-hero.jpeg` par `https://votre-domaine/assets/photos/01-hero.jpeg`).

---

## ⚠️ À COMPLÉTER par la cliente (placeholders visibles dans le site)
Tous marqués `À CONFIRMER` (encadré sable) — **rien n'a été inventé** :
1. **Email de réservation** — section « Réserver » (`index.html`, bloc `.contact-box`).
2. **Téléphone** — idem.
3. **WhatsApp direct** — idem.
4. **Réseaux sociaux** — footer.
5. **Tarif** — volontairement « Tarif sur demande » (l'annonce ne donne pas de prix). Ne pas inventer de montant.

## 📸 Ajouter des photos
La galerie ne contient que les **9 visuels d'aperçu** récupérés. Un beau site « plein de photos » en demande 15–30.
1. Déposer les nouveaux fichiers dans `assets/photos/` (idéalement en `.jpeg`/`.webp`, ≥1600 px de large).
2. Les ajouter dans la grille `#galerie` de `index.html` en copiant un bloc `<a class="gallery__item glightbox" …>` existant (mettre un `alt` descriptif).
3. Suggestions de prises de vue manquantes : intérieurs, salle de bain, cuisine, **bar extérieur**, **douche extérieure**, **jardin tropical**, plage/marina, **couchers de soleil**.

## Bilingue (FR / EN)
Le site est en **français** (langue principale du brief). La structure est prête pour une version anglaise.
⚠️ Les **avis voyageurs** sont affichés **tels quels** (verbatim FR) — ne pas les traduire (ce sont des témoignages réels).
Pour l'anglais : dupliquer les textes statiques en EN et ajouter un sélecteur FR/EN dans le header. (Non fait pour l'instant pour éviter toute traduction approximative.)

---

## Contenu — source unique de vérité
Tout le contenu (description, chambres, équipements, distances, avis, hôte) provient de **l'annonce Airbnb réelle** :
👉 https://www.airbnb.fr/rooms/1197051105797112250

Distinctions affichées (réelles) : « Coup de cœur voyageurs » · 1 % des logements préférés sur Airbnb · **5,0 / 5 sur 25 commentaires** · hôte **Superhôte** depuis 9 ans.

## TODO avant production
- [ ] Compléter les 5 placeholders `À CONFIRMER`.
- [ ] Ajouter le pack photos complet de Cécile.
- [ ] Rendre les balises Open Graph absolues (domaine).
- [ ] Vérifier les conditions d'annulation à jour (Airbnb).
- [ ] (Option) Localiser les libs CDN si besoin d'un site 100 % autonome hors-ligne.
- [ ] (Option) Version anglaise.
