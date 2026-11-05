# Cœurs Unis - Plateforme de Rencontres pour Couples

Bienvenue sur **Cœurs Unis**, une plateforme de rencontres dédiée aux couples cherchant à établir des connexions authentiques avec d'autres couples.

## 🎯 À propos

Cœurs Unis est un site statique généré avec [Cecil](https://cecil.app), une application PHP qui fusionne des fichiers Markdown, des images et des modèles Twig pour créer un site web statique.

### ✨ Fonctionnalités

- 📋 Annuaire de profils de couples
- 💬 Page de contact pour nouvelles demandes
- 🔒 Politique de confidentialité stricte
- 🌈 Design inclusif et bienveillant
- 📱 Site responsive

## 🚀 Utilisation

### Aperçu local (avec rechargement en direct)

```bash
php cecil.phar serve
```

### Construire le site (dans le répertoire `_site/`)

```bash
php cecil.phar build
```

### Créer une nouvelle page

```bash
php cecil.phar new:page
```

## 📁 Structure du projet

```
├── cecil.yml              # Configuration du site
├── pages/                 # Contenu en Markdown
│   ├── index.md          # Accueil
│   ├── about.md          # À Propos
│   ├── profiles.md       # Nos Profils
│   ├── contact.md        # Contact
│   ├── privacy.md        # Politique de Confidentialité
│   └── terms.md          # Conditions d'Utilisation
├── layouts/              # Modèles Twig
├── assets/               # Images, CSS, scripts
│   └── css/
│       └── style.scss    # Styles personnalisés
├── data/                 # Fichiers de données (YAML, JSON, etc.)
│   ├── couples.yaml      # Données des couples
│   └── links.yaml        # Liens du pied de page
└── static/               # Fichiers copiés tels quels
```

## 🎨 Personnalisation

### Modifier la configuration

Éditez `cecil.yml` pour changer le titre, la description, les menus, etc.

### Ajouter un profil de couple

1. Mettez à jour `data/couples.yaml` avec les nouvelles informations
2. Les profils seront automatiquement affichés sur la page des profils

### Personnaliser les styles

Les styles sont définis dans `assets/css/style.scss`. Les couleurs principales sont :

- **Primaire** : `#e74c3c` (rouge)
- **Secondaire** : `#f39c12` (orange)
- **Accent** : `#9b59b6` (violet)

## 🔒 Sécurité et Confidentialité

- Consultez notre [Politique de Confidentialité](pages/privacy.md)
- Consultez nos [Conditions d'Utilisation](pages/terms.md)

## 📚 Documentation

Pour plus d'informations sur Cecil, consultez :
- <https://cecil.app/documentation/>

## 💖 Nos valeurs

- **🤝 Respect** : Respecter chacun dans sa singularité
- **💝 Authenticité** : Des profils vrais et des rencontres sincères
- **🔒 Sécurité** : Vos données personnelles sont protégées
- **🌈 Inclusivité** : Un espace bienveillant pour tous

## 📞 Contact

Pour toute question ou pour créer votre profil :

- **E-mail** : [contact@coeurs-unis.fr](mailto:contact@coeurs-unis.fr)

---

**Créé avec ❤️ par la communauté Cœurs Unis**

