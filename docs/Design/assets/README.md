# Assets graphiques — Ohanna Platform

Les ressources de ce dossier constituent la bibliothèque graphique officielle de la plateforme **Ohanna**.

Elles sont partagées par l'ensemble des projets :

* Ohanna-Agent
* Ohanna-Vision
* futurs produits de la plateforme
* documentation officielle
* site web
* démonstrations
* présentations

L'objectif est de garantir une identité visuelle cohérente sur l'ensemble de l'écosystème.

---

# Organisation

```text
assets/
├── logos/
├── icons/
├── favicons/
├── illustrations/
└── sources/
```

Chaque dossier possède une responsabilité unique.

| Dossier       | Contenu                                                |
| ------------- | ------------------------------------------------------ |
| logos         | Logos officiels Ohanna                                 |
| icons         | Icônes SVG utilisées par l'interface                   |
| favicons      | Icônes navigateurs et PWA                              |
| illustrations | Illustrations, états vides et erreurs                  |
| sources       | Fichiers de travail (SVG maîtres, exports, références) |

---

# Principes de conception

Tous les assets doivent respecter les principes suivants :

* simplicité ;
* lisibilité à petite taille ;
* cohérence graphique ;
* style moderne et minimaliste ;
* compatibilité avec les thèmes clair et sombre ;
* homogénéité entre toutes les icônes.

L'identité visuelle doit rester immédiatement reconnaissable.

---

# Format des fichiers

Le format de référence est :

* SVG vectoriel.

Les fichiers SVG doivent être :

* autonomes ;
* sans ressources externes ;
* sans police embarquée ;
* sans bitmap intégré ;
* optimisés ;
* compatibles avec les navigateurs modernes.

---

# Convention de nommage

Les fichiers utilisent exclusivement :

* minuscules ;
* tirets (`-`) ;
* extension `.svg`.

Exemples :

```
switch.svg
raspberry-pi.svg
health-healthy.svg
mqtt.svg
timeline.svg
```

Les espaces sont interdits.

---

# Grille de conception

Toutes les icônes sont dessinées sur une grille commune.

Dimensions de référence :

* 24 × 24 px

Les exports peuvent être générés en :

* 16 px
* 20 px
* 24 px
* 32 px
* 48 px
* 64 px

Le dessin reste centré dans la grille.

---

# Style graphique

Les icônes utilisent exclusivement :

* contours simples ;
* angles légèrement arrondis ;
* épaisseur de trait constante ;
* très peu de remplissage ;
* géométrie sobre.

Le style est inspiré :

* des schémas réseau ;
* des diagrammes d'infrastructure ;
* des interfaces techniques modernes.

---

# Palette

Par défaut, les SVG utilisent :

```
currentColor
```

Leur couleur est donc héritée automatiquement par le thème.

Les variantes colorées utilisent uniquement les couleurs définies dans le Design System.

Aucune couleur codée en dur ne doit être utilisée sans justification.

---

# Logos

Le dossier `logos/` contient uniquement les logos officiels.

Ils ne doivent jamais être modifiés.

Les variantes comprennent notamment :

* logo principal ;
* version sombre ;
* version claire ;
* symbole seul ;
* mot-symbole ;
* monochrome noir ;
* monochrome blanc.

---

# Icônes

Le dossier `icons/` contient toutes les icônes utilisées dans l'interface.

Les catégories sont notamment :

* infrastructure ;
* capacités ;
* technologies ;
* navigation ;
* santé ;
* actions.

Toutes les icônes suivent le même langage graphique.

---

# Illustrations

Les illustrations représentent les écrans et états particuliers :

* aucune donnée ;
* erreur ;
* maintenance ;
* système déconnecté ;
* chargement ;
* état vide.

Le style reste cohérent avec le reste de la plateforme.

---

# Favicons

Le dossier `favicons/` contient les ressources destinées :

* aux navigateurs ;
* aux Progressive Web Apps ;
* aux raccourcis mobiles.

Les tailles normalisées sont :

* favicon.ico
* favicon.svg
* 192 × 192
* 512 × 512
* Apple Touch Icon

---

# Sources

Le dossier `sources/` contient les fichiers de travail.

Exemples :

* exports Inkscape ;
* exports Illustrator ;
* maquettes ;
* variantes de construction.

Ces fichiers ne sont jamais utilisés directement par l'application.

---

# Compatibilité

Les ressources doivent fonctionner avec :

* Chrome
* Edge
* Firefox
* Safari

Aucune dépendance externe n'est autorisée.

---

# Accessibilité

Les icônes utilisées seules doivent toujours être accompagnées :

* d'un intitulé ;
* d'un `title` SVG lorsque nécessaire ;
* ou d'un texte alternatif.

La couleur ne doit jamais être le seul moyen de transmettre une information.

---

# Évolution

Toute nouvelle ressource graphique doit respecter :

* la grille officielle ;
* la palette officielle ;
* les conventions de nommage ;
* le style graphique Ohanna.

Les nouvelles icônes doivent conserver une cohérence visuelle avec les ressources existantes.

---

# Philosophie

Les assets graphiques d'Ohanna poursuivent un objectif unique :

**Rendre une infrastructure complexe immédiatement lisible grâce à une identité visuelle simple, cohérente et durable.**
