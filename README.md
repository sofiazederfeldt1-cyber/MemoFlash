# 🌿 MemoFlash

**Application d'apprentissage gratuite et open source — alternative à Quizlet**

> Apprends plus vite, retiens plus longtemps.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/HTML-only-orange.svg)]()
[![No backend](https://img.shields.io/badge/Backend-aucun-blue.svg)]()

---

## ✨ Fonctionnalités

- 🃏 **Flashcards** — recto/verso avec animation flip
- 🧠 **Révision espacée** — algorithme SM-2 (comme Anki)
- ✅ **Quiz QCM** — 4 options générées automatiquement
- ✏️ **Mode écrit** — tape la réponse et vérifie
- 📦 **Import/Export JSON** — partage tes decks
- 📋 **Import en lot** — format `question;réponse`
- 🏆 **Classement** — compare tes scores
- 🔥 **Streak** — jours consécutifs de révision
- 💾 **100% local** — aucun serveur, données dans le navigateur

---

## 🚀 Utiliser l'application

### En ligne
👉 **[memoflash.github.io](https://ton-pseudo.github.io/memoflash)** *(remplace par ton URL)*

### En local
1. Clone ce dépôt :
   ```bash
   git clone https://github.com/ton-pseudo/memoflash.git
   ```
2. Ouvre `index.html` dans ton navigateur — c'est tout !

Aucune installation, aucun npm, aucun serveur requis.

---

## 📁 Structure du projet

```
memoflash/
├── index.html        # Application complète (HTML/CSS/JS)
├── README.md         # Ce fichier
├── LICENSE           # Licence MIT
└── .github/
    └── workflows/
        └── deploy.yml  # Déploiement automatique GitHub Pages
```

---

## 🛠️ Modifier le code

Le projet est un **fichier HTML unique** — pas de build, pas de framework.

Pour modifier :
1. Ouvre `index.html` dans VS Code (ou n'importe quel éditeur)
2. **CSS** : dans la balise `<style>` (variables en haut du fichier)
3. **HTML** : structure des pages dans le `<body>`
4. **JavaScript** : dans la balise `<script>` en bas du fichier

### Variables CSS principales
```css
--terra: #C4622D;      /* couleur principale (boutons, accents) */
--sage: #7A9E7E;       /* couleur secondaire (succès, facile) */
--cream: #F7F3EE;      /* fond général */
--ink: #2C2416;        /* texte principal */
```

### Ajouter une fonctionnalité
Chaque mode d'étude suit le même pattern :
- `startMode(mode)` — initialise le mode
- `showXxxQ()` — affiche la question courante
- `nextXxx()` — passe à la suivante
- `showEnd()` — affiche l'écran de fin

---

## 🌐 Déployer sur GitHub Pages (gratuit)

### Méthode automatique (recommandée)
Le fichier `.github/workflows/deploy.yml` déploie automatiquement à chaque push.

1. Va dans **Settings → Pages** de ton dépôt GitHub
2. Source : **GitHub Actions**
3. C'est tout ! Chaque `git push` met à jour le site.

### Méthode manuelle
1. **Settings → Pages**
2. Source : **Deploy from a branch**
3. Branch : `main`, dossier : `/ (root)`
4. Ton site sera disponible sur `https://ton-pseudo.github.io/memoflash`

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

1. Fork ce dépôt
2. Crée une branche : `git checkout -b feature/ma-fonctionnalite`
3. Commit tes changements : `git commit -m "Ajout de ma fonctionnalité"`
4. Push : `git push origin feature/ma-fonctionnalite`
5. Ouvre une **Pull Request**

### Idées de contributions
- [ ] Mode nuit / thème sombre
- [ ] Support des images dans les cartes
- [ ] Partage de decks via lien URL
- [ ] Statistiques détaillées par deck
- [ ] Export PDF d'un deck
- [ ] Support multilingue
- [ ] PWA (installation sur mobile)

---

## 📊 Format d'export/import

Les decks sont exportés en JSON :
```json
{
  "decks": [
    {
      "id": "abc123",
      "name": "Capitales du monde",
      "icon": "🌍",
      "cards": [
        {
          "front": "Capitale de la France ?",
          "back": "Paris",
          "level": 3,
          "interval": 7,
          "ef": 2.5,
          "nextReview": 1234567890
        }
      ]
    }
  ]
}
```

---

## 📄 Licence

MIT — fais-en ce que tu veux, c'est gratuit pour toujours.

---

*Fait avec ❤️ comme alternative gratuite à Quizlet*
