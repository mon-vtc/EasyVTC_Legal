# EazyVTC — Pages légales

Site minimal servant la politique de confidentialité d'EasyVTC, hébergé publiquement pour la soumission Google Play Console / App Store Connect (les deux exigent une URL publique de politique de confidentialité).

## Contenu

- `public/index.html` — politique de confidentialité (HTML statique)
- `server.js` — petit serveur Express qui sert `public/` (+ `/health` pour Railway)

## Lancer en local

```bash
npm install
npm start
```

Ouvrir http://localhost:3000

## Déploiement Railway

1. Créer un nouveau projet Railway → "Deploy from GitHub repo" → sélectionner ce repo
2. Railway détecte Node automatiquement (Nixpacks) et utilise `railway.toml`
3. Générer un domaine public (Settings → Networking → Generate Domain)
4. Renseigner cette URL dans :
   - Google Play Console → Fiche du store → Politique de confidentialité
   - App Store Connect → Distribution → Politique de confidentialité

## Mettre à jour le contenu

Éditer directement `public/index.html`, commit + push sur `main` → Railway redéploie automatiquement.
