# La Villa Loubésienne — Site officiel

Site web officiel de **La Villa Loubésienne**, restaurant bistronomique aux saveurs exotiques à Saint-Loubès, Gironde.

🌿 **En ligne** : [lavillaloubesienne.com](https://www.lavillaloubesienne.com)

## À propos

Restaurant bistronomique au cœur d'une bâtisse en pierre du XIXe siècle, avec rooftop ensoleillé. Plats gourmands aux saveurs antillaises, cocktails maison signature, ambiance cosy et chaleureuse.

- 📍 92 Avenue de la République, 33450 Saint-Loubès
- ⭐ 8,9/10 sur TheFork · 743 avis
- 🍴 Réservation via [TheFork](https://www.thefork.fr/restaurant/la-villa-loubesienne-r372397)

## Stack technique

- **HTML5** sémantique
- **CSS3** moderne (Grid, Flexbox, custom properties)
- **JavaScript vanilla** (Intersection Observer, smooth scroll)
- **Fonts** : Fraunces (display) + Inter (body) via Google Fonts
- **Images** : Unsplash (en attendant les vrais visuels du restaurant)
- **Réservations** : Widget TheFork intégré

## Structure

```
.
├── index.html              # Site complet single-page
├── assets/
│   └── logos/              # 11 logos SVG vectoriels
│       ├── 01_logo_principal_sauge.svg
│       ├── 02_logo_fond_sombre_or.svg
│       ├── ...
│       └── 11_logo_complet_baseline.svg
└── README.md
```

## Sections du site

1. **Hero** — Accueil avec photo plat signature + sceau logo
2. **Philosophie** — L'esprit Villa, 4 valeurs clés
3. **Galerie** — Mosaïque d'images (ambiance, plats, cocktails)
4. **Carte** — Menu complet (entrées, plats, desserts, bar)
5. **Partenaires** — Cafés Richard, Château de Reignac, HBC Saint-Loubès
6. **Espaces** — Rooftop & Salle principale
7. **Témoignages** — Stats + avis clients
8. **Réservation** — Formulaire + widget TheFork
9. **Infos pratiques** — Adresse, horaires, contact

## Charte graphique

### Palette
- `#FBF9F4` — Crème (fond)
- `#6B8E7F` — Sauge (signature)
- `#C77B58` — Terracotta (accent)
- `#2A2A28` — Encre (texte)

### Typographie
- **Fraunces** — Display, titres, citations
- **Inter** — Corps de texte, navigation

## Déploiement

### GitHub Pages (recommandé — gratuit)

```bash
# Settings → Pages → Source : main branch / root
# Le site sera disponible sur :
# https://<username>.github.io/villa-loubesienne-site/
```

### Netlify (recommandé pour custom domain)

1. Drag & drop le dossier sur netlify.com
2. Connecter le domaine `lavillaloubesienne.com`
3. SSL automatique via Let's Encrypt

### Vercel

```bash
vercel --prod
```

## Roadmap

- [ ] Remplacer photos Unsplash par vrais visuels du restaurant
- [ ] Ajouter section "Notre équipe" avec photos chef + brigade
- [ ] Page dédiée "Privatisations & événements"
- [ ] Intégration Instagram feed live
- [ ] Page "Bons cadeaux" e-commerce
- [ ] Version multilingue (FR / EN)
- [ ] PWA pour usage mobile offline

## Crédits

- **Identité de marque** : Concept La Villa Loubésienne 2026
- **Développement** : Frédéric Bezaradany
- **Photos placeholder** : [Unsplash](https://unsplash.com)

## License

© 2026 La Villa Loubésienne · Tous droits réservés
