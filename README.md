# Notes philosophiques — blog Jekyll

Blog minimaliste en crème/sauge, pensé pour poster des articles de philosophie avec des tags (libellés). Aucune page inutile : juste la liste des articles, une page d'article, et une page tags générée automatiquement.

## 1. Tester en local (optionnel mais recommandé)

Il te faut Ruby installé sur ta machine (macOS et Linux l'ont souvent déjà ; sur Windows, installe [RubyInstaller](https://rubyinstaller.org/)).

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Le site sera visible sur `http://localhost:4000`. À chaque modification d'un fichier, il se recharge automatiquement (sauf `_config.yml`, qui demande de relancer la commande).

Si tu veux juste mettre en ligne sans jamais tester en local, tu peux sauter cette étape.

## 2. Mettre le site sur GitHub

1. Crée un compte sur [github.com](https://github.com) si tu n'en as pas.
2. Crée un nouveau dépôt (repository), public, nommé par exemple `philo-blog`.
3. Depuis ce dossier, en local :

```bash
git init
git add .
git commit -m "Premier commit du blog"
git branch -M main
git remote add origin https://github.com/TON-PSEUDO/philo-blog.git
git push -u origin main
```

## 3. Activer GitHub Pages

1. Sur GitHub, va dans ton dépôt → **Settings** → **Pages**.
2. Dans "Build and deployment", choisis **Deploy from a branch**.
3. Sélectionne la branche `main` et le dossier `/ (root)`.
4. Sauvegarde. Le site est en ligne en 1-2 minutes à l'adresse :
   `https://TON-PSEUDO.github.io/philo-blog/`

## 4. Adapter la configuration

Ouvre `_config.yml` et remplace :

```yaml
url: "https://TON-PSEUDO.github.io"
baseurl: "/philo-blog"
```

Sans ça, certains liens internes (flux RSS, sitemap) seront mal générés une fois en ligne.

## 5. Écrire un nouvel article

Crée un fichier dans `_posts/`, nommé **impérativement** au format `AAAA-MM-JJ-titre-du-slug.md`, par exemple :

```
_posts/2026-07-15-le-mythe-de-sisyphe.md
```

Avec ce contenu :

```markdown
---
layout: post
title: "Le mythe de Sisyphe et l'absurde chez Camus"
date: 2026-07-15
tags: [absurde, camus, existentialisme]
---

Ton article ici, en Markdown normal.

## Un sous-titre

Du texte, des **gras**, des *italiques*, des listes, etc.

> Une citation mise en avant, si tu veux souligner un passage.
```

Ajoute, commit, push :

```bash
git add .
git commit -m "Nouvel article : Sisyphe et l'absurde"
git push
```

Le site se met à jour automatiquement en 1-2 minutes.

## 6. Modifier le design

Toute l'apparence est dans un seul fichier : `assets/css/style.css`. Les variables de couleur sont en haut du fichier (`:root { ... }`) — tu peux changer les teintes de crème et de sauge sans toucher au reste.

Les polices utilisées (Google Fonts, gratuites) :
- **Fraunces** pour les titres
- **Newsreader** pour le texte courant
- **JetBrains Mono** pour les dates, tags et éléments techniques

## 7. Nom de domaine

Par défaut ton site est accessible via `TON-PSEUDO.github.io/philo-blog` — gratuit, illimité, aucune expiration. Si tu veux un vrai nom de domaine (`.com`, `.fr`...) plus tard, GitHub Pages le permet aussi, mais l'achat du domaine reste payant (quelques euros par an) : il n'existe pas d'option de nom de domaine personnalisé réellement gratuite et fiable à ce jour.
