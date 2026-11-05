# 📖 Guide d'Utilisation - Cœurs Unis

## 🚀 Démarrer le site

### Serveur de développement local

```bash
cd C:\Users\Baraka24\Desktop\site_rencontre
php cecil.phar serve
```

Le site sera accessible à : `http://localhost:8000`

Avec le rechargement automatique, toute modification aux fichiers sera visible immédiatement dans le navigateur.

### Construire le site pour production

```bash
php cecil.phar build
```

Le site généré se trouvera dans le répertoire `_site/`

## 📝 Gérer les profils des couples

### Ajouter un nouveau profil

Éditez le fichier `data/couples.yaml` et ajoutez une nouvelle entrée :

```yaml
- id: 6
  names: "Jean et Marie"
  ages: "40 et 38 ans"
  location: "Nice, Provence-Alpes-Côte d'Azur"
  interests: ["Voile", "Gastronomie", "Yoga", "Voyages"]
  description: "Couple établi passionné par la mer et les voyages. Nous recherchons d'autres couples pour partager nos aventures."
  joined: "2024-06"
```

### Modifier un profil existant

Trouvez le profil dans `data/couples.yaml` et mettez à jour les informations souhaitées.

### Structure d'un profil

```yaml
id: Numéro unique du profil (numérique)
names: Noms des deux partenaires
ages: Âges respectifs (format: "XX et XX ans")
location: Ville et région
interests: Liste d'intérêts (tableau YAML)
description: Description du couple
joined: Date d'adhésion (format YYYY-MM)
```

## 📄 Ajouter ou modifier des pages

### Créer une nouvelle page

Utilisez la commande Cecil :

```bash
php cecil.phar new:page
```

Ou créez manuellement un fichier `pages/nouvelle-page.md` :

```markdown
---
title: Titre de la page
description: Description pour les moteurs de recherche
menu:
  main:
    weight: 50
---

# Titre de la page

Contenu en Markdown...
```

### Front matter disponible

```yaml
title: Titre de la page (obligatoire)
description: Description courte
menu: Configuration du menu
  main: Menu principal
    weight: Position dans le menu (nombre)
layout: Type de mise en page à utiliser
draft: Masquer de la publication (true/false)
date: Date de publication
tags: Étiquettes pour catégoriser
```

## 🎨 Personnaliser les styles

### Fichier CSS principal

Le fichier `assets/css/style.scss` contient tous les styles de la plateforme.

### Couleurs principales

```scss
$primary-color: #e74c3c;        // Rouge
$secondary-color: #f39c12;      // Orange
$accent-color: #9b59b6;         // Violet
$light-color: #ecf0f1;          // Gris clair
```

### Modifier une couleur

1. Ouvrez `assets/css/style.scss`
2. Trouvez la variable de couleur à modifier
3. Changez la valeur hexadécimale
4. Sauvegardez et le site se recompilera automatiquement

Exemple : Changer le rouge primaire en bleu

```scss
$primary-color: #3498db;  // Bleu au lieu du rouge
```

## 📧 Configurer le contact

### Ajouter votre email

Éditez `pages/contact.md` et remplacez l'adresse email :

```markdown
**E-mail** : [votre-email@exemple.fr](mailto:votre-email@exemple.fr)
```

## 🔧 Configuration avancée

### Modifier le titre du site

Éditez `cecil.yml` :

```yaml
title: 'Nouveau titre'
description: 'Nouvelle description'
```

### Ajouter des mots-clés pour SEO

Ajoutez cette ligne dans `cecil.yml` :

```yaml
metatags:
  keywords: "couples, rencontres, réseau social, amitié"
```

### Activer/désactiver le multilinguisme

La plateforme est configurée pour le français. Pour ajouter d'autres langues :

```yaml
languages:
  - code: fr
    name: Français
  - code: en
    name: English
```

Puis créez des traductions dans `translations/messages.en.yaml`

## 📊 Gestion du contenu du blog

### Ajouter un article de blog

Créez un fichier dans `pages/blog/` :

```markdown
---
title: Mon Article
description: Description de l'article
date: 2024-11-05
tags: [rencontres, conseils, couples]
---

Contenu de l'article...
```

## 🔐 Sécurité

### Mettre à jour la politique de confidentialité

Éditez `pages/privacy.md` avec votre propre politique.

### Mettre à jour les conditions d'utilisation

Éditez `pages/terms.md` avec vos conditions spécifiques.

## 📱 Optimisation mobile

Le site est entièrement responsive. Pour tester :

1. Servez le site localement
2. Ouvrez les outils de développement (F12)
3. Activez l'aperçu réactif (Ctrl+Shift+M)

## 🐛 Dépannage

### Le site ne compile pas

```bash
php cecil.phar build --debug
```

Cela affichera des messages d'erreur détaillés.

### Erreur de front matter

Vérifiez que votre YAML est bien formaté avec l'indentation correcte (2 espaces).

### Les styles ne s'appliquent pas

- Assurez-vous d'avoir sauvegardé le fichier SCSS
- Videz le cache du navigateur (Ctrl+Shift+Suppr)
- Reconstruisez le site

## 📤 Déployer le site

### Sur un serveur web

1. Construisez le site : `php cecil.phar build`
2. Transférez le contenu du répertoire `_site/` sur votre serveur
3. Assurez-vous que le répertoire racine web pointe vers `_site/`

### Sur GitHub Pages

1. Poussez votre code sur GitHub
2. Configurez GitHub Pages dans les paramètres du dépôt
3. Configurez le déploiement automatique

### Sur un service d'hébergement statique

Excellents services pour les sites statiques :

- **Netlify** : netlify.com (gratuit avec domaine personnalisé)
- **Vercel** : vercel.com (très rapide)
- **GitHub Pages** : pages.github.com (gratuit)

## 💡 Conseils

- Sauvegardez régulièrement votre contenu
- Testez les modifications localement avant le déploiement
- Utilisez un système de contrôle de version (Git)
- Révisez les traductions pour la qualité
- Assurez-vous que les images sont optimisées
- Testez sur plusieurs navigateurs

## 📚 Ressources utiles

- [Documentation Cecil](https://cecil.app/documentation/)
- [Guide Markdown](https://www.markdownguide.org/)
- [Syntaxe YAML](https://yaml.org/spec/1.2/spec.html)
- [Twig Templates](https://twig.symfony.com/doc/)

## 🆘 Besoin d'aide ?

Consultez la [documentation officielle de Cecil](https://cecil.app/documentation/) pour des informations plus détaillées.

---

**Bonne gestion de votre plateforme ! 💑**
