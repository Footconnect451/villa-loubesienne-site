# Guide de déploiement — La Villa Loubésienne

## Option 1 — GitHub Pages (gratuit, simple)

### Étape 1 : Créer le repository

1. Va sur https://github.com/new
2. Nom du repo : `villa-loubesienne-site` (ou ce que tu veux)
3. Visibilité : Public ou Private (au choix)
4. **Ne PAS** initialiser avec README (on en a déjà un)
5. Crée le repo

### Étape 2 : Upload des fichiers

**Méthode A — Interface web GitHub (plus simple)**

1. Dans ton nouveau repo vide, clique sur "uploading an existing file"
2. Drag & drop tous les fichiers de ce dossier
3. Message de commit : "Initial commit"
4. Clique "Commit changes"

**Méthode B — Ligne de commande Git**

```bash
cd ~/Downloads/villa-loubesienne-site

git init
git add .
git commit -m "Initial commit — site Villa Loubesienne"
git branch -M main
git remote add origin https://github.com/TON-USERNAME/villa-loubesienne-site.git
git push -u origin main
```

### Étape 3 : Activer GitHub Pages

1. Dans ton repo → Settings → Pages
2. Source : `Deploy from a branch`
3. Branch : `main` / `/ (root)`
4. Save

→ Le site sera disponible sous 1-2 min sur :
`https://TON-USERNAME.github.io/villa-loubesienne-site/`

### Étape 4 (optionnel) — Connecter ton domaine

1. Settings → Pages → Custom domain : `www.lavillaloubesienne.com`
2. Chez ton registrar de domaine, ajouter ces enregistrements DNS :

```
Type   Name   Value
A      @      185.199.108.153
A      @      185.199.109.153
A      @      185.199.110.153
A      @      185.199.111.153
CNAME  www    TON-USERNAME.github.io
```

3. Attendre la propagation DNS (10 min à 24h)
4. Activer "Enforce HTTPS" sur GitHub Pages

---

## Option 2 — Netlify (recommandé pour custom domain)

### Étape 1 : Compte Netlify

1. Crée un compte sur https://netlify.com (gratuit)
2. Connecte ton GitHub

### Étape 2 : Déployer

**Méthode rapide :** Drag & drop le dossier sur netlify.com → Sites → Add new site → Deploy manually

**Méthode Git :** New site from Git → Pick repository → Deploy

### Étape 3 : Domaine personnalisé

1. Domain management → Add custom domain
2. Suis les instructions DNS
3. SSL automatique activé en 1 clic

---

## Option 3 — Vercel

```bash
npm i -g vercel
cd villa-loubesienne-site
vercel --prod
```

Suis les prompts. Site live en 30 secondes.

---

## Configuration domaine lavillaloubesienne.com

Le domaine est probablement déjà géré par Wix actuellement. Lors de la reprise :

1. Récupérer les accès au compte Wix du vendeur
2. Soit transférer le domaine vers un autre registrar (OVH, Gandi)
3. Soit modifier les DNS Wix pour pointer vers la nouvelle solution
4. Tester sur sous-domaine temporaire avant la bascule finale

---

## Tests avant mise en ligne

- [ ] Tester sur desktop (Chrome, Safari, Firefox)
- [ ] Tester sur mobile (iOS Safari, Android Chrome)
- [ ] Vérifier tous les liens
- [ ] Tester le widget TheFork de réservation
- [ ] Vérifier les liens Instagram et Facebook
- [ ] Lancer Google PageSpeed Insights
- [ ] Vérifier l'accessibilité (Lighthouse)
- [ ] SEO basique : title, description, OG tags

---

## Maintenance

Pour modifier le site après déploiement :

```bash
# Modifier les fichiers localement
# Puis :
git add .
git commit -m "Description du changement"
git push

# GitHub Pages / Netlify / Vercel redéploient automatiquement
```
