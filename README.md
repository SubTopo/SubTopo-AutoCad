# SubTopo-Autocad — Éditeur CAD Web

Éditeur CAD web (AutoCAD-like) pour le projet Brega Airport. Ouvrable directement dans un navigateur, sans installation.

## 🌐 Démo en ligne (GitHub Pages)

L'URL publique suit ce format :

```
https://<TON-USER>.github.io/<CE-REPO>/
```

## 🚀 Déployer sur GitHub Pages (1 minute)

1. **Crée un repo** sur github.com (ex. `brega-airport-cad`)
2. **Push** le contenu de ce dossier :
   ```bash
   git init
   git add .
   git commit -m "Initial commit — SubTopo-Autocad"
   git branch -M main
   git remote add origin https://github.com/<TON-USER>/brega-airport-cad.git
   git push -u origin main
   ```
3. **Settings → Pages** :
   - Source : *Deploy from a branch*
   - Branch : `main` / `(root)`
   - Save
4. **Attends 1-2 min**, l'URL est en haut de la page Settings → Pages

## 📂 Contenu

```
.
├── index.html          ← page d'entrée (chargée par GitHub Pages)
├── .nojekyll           ← désactive Jekyll (sinon GitHub Pages peut bloquer assets/)
└── assets/
    ├── style.css       ← styles (10.8 KB)
    ├── cad.js          ← JavaScript complet (225 KB)
    └── logo.png        ← logo globe + axes + pin GPS (favicon aussi)
```

## ✏️ Renommer / réorganiser

Le HTML charge le JS/CSS/images par chemin relatif — tu peux renommer librement :

```html
<link rel="stylesheet" href="assets/style.css">
<link rel="icon" type="image/png" href="assets/logo.png">
<script src="assets/cad.js"></script>
```

## 🎯 Fonctionnalités

- Lignes, polylignes, cercles, arcs, ellipses, points, textes
- Calques (LAYER), couleurs ACI / true color
- Mesures (longueur, surface)
- Zoom, pan, grille, ortho
- Annuler / Rétablir (Ctrl+Z / Ctrl+Y)
- Enregistrer / Enregistrer sous (JSON, DXF, DWG) avec Ctrl+S / Ctrl+Shift+S
- Roundtrip DXF 100% (678 entités, 11 calques)
