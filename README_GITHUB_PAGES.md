# Qubitcoin - Déploiement sur GitHub Pages

Guide ultra-simple pour déployer le site Qubitcoin sur GitHub Pages.

## 🚀 Déploiement en 3 Étapes

### 1. Uploadez les fichiers sur GitHub

1. **Allez dans votre repository** `QBTC-V2` sur GitHub
2. **Supprimez tous les fichiers** existants (ou créez un nouveau repo)
3. **Décompressez** le fichier `qubitcoin-github-pages.zip`
4. **Uploadez TOUS les fichiers** à la racine du repository :
   - `index.html`
   - `assets/` (dossier)
   - `logo.png`
   - `qubit-chain.png`

### 2. Activez GitHub Pages

1. Allez dans **Settings** → **Pages**
2. **Source** : Sélectionnez `Deploy from a branch`
3. **Branch** : Sélectionnez `main` et `/ (root)`
4. Cliquez sur **Save**

### 3. Attendez le déploiement

- GitHub va automatiquement déployer le site (1-2 minutes)
- Votre site sera accessible sur : `https://votre-username.github.io/QBTC-V2/`

## ✅ Structure Requise

Votre repository doit avoir cette structure **à la racine** :

```
QBTC-V2/  (racine du repo)
├── index.html          ← OBLIGATOIRE à la racine
├── assets/
│   ├── index-xxx.js
│   └── index-xxx.css
├── logo.png
└── qubit-chain.png
```

## 🔧 Personnalisation

### Modifier le contenu

Les fichiers fournis sont **déjà buildés** et optimisés. Pour modifier le contenu :

1. Modifiez les fichiers source du projet
2. Lancez `pnpm build` localement
3. Uploadez le nouveau contenu de `dist/public/` sur GitHub

### Domaine personnalisé

1. Allez dans **Settings** → **Pages**
2. Section **Custom domain**
3. Entrez votre domaine (ex: `qubitcoin.com`)
4. Configurez les DNS selon les instructions GitHub

## 🌐 URL du Site

Une fois déployé, votre site sera accessible sur :

```
https://[votre-username].github.io/QBTC-V2/
```

Ou si vous utilisez un domaine personnalisé :

```
https://qubitcoin.com
```

## 💡 Avantages de GitHub Pages

- ✅ **100% Gratuit**
- ✅ **Pas de mise en veille** (contrairement à Render Free)
- ✅ **HTTPS automatique**
- ✅ **CDN mondial** (rapide partout)
- ✅ **Déploiement automatique** à chaque push

## 🆘 Dépannage

### Le site affiche "404 Not Found"

- Vérifiez que `index.html` est **à la racine** du repo
- Vérifiez que GitHub Pages est activé dans Settings → Pages
- Attendez 2-3 minutes après activation

### Le site affiche une page blanche

- Ouvrez la console du navigateur (F12)
- Vérifiez les erreurs de chargement des assets
- Assurez-vous que le dossier `assets/` est bien uploadé

### Les images ne s'affichent pas

- Vérifiez que `logo.png` et `qubit-chain.png` sont à la racine
- Les chemins sont relatifs, ils doivent être au même niveau que `index.html`

## 📱 Alternatives

Si GitHub Pages ne convient pas :

- **Netlify** : Drag & drop du ZIP → déploiement instantané
- **Vercel** : Connectez le repo GitHub → déploiement automatique
- **Cloudflare Pages** : Similaire à Netlify/Vercel

## 🔄 Mises à Jour

Pour mettre à jour le site :

1. Modifiez les fichiers source
2. Lancez `pnpm build`
3. Uploadez le nouveau contenu de `dist/public/` sur GitHub
4. GitHub Pages redéploie automatiquement

---

© 2025 Qubitcoin. Tous droits réservés.
