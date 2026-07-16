# Assets — Ohanna Design System

Les assets graphiques constituent la bibliothèque visuelle officielle de la plateforme **Ohanna**.

Ils regroupent les logos, icônes, illustrations et ressources utilisées par l'ensemble des produits de l'écosystème.

Les assets sont conçus pour être :

- cohérents ;
- réutilisables ;
- versionnés ;
- indépendants de toute technologie ;
- facilement exportables vers le Web, le mobile et l'impression.

---

# Objectifs

Les assets garantissent :

- une identité graphique unique ;
- une cohérence entre tous les produits ;
- une maintenance simplifiée ;
- une qualité constante des ressources graphiques.

Ils constituent la **source officielle** de tous les éléments visuels utilisés par :

- Ohanna-Agent
- Ohanna-Vision
- Ohanna-House
- documentation
- site web
- présentations
- futures applications.

---

# Organisation

```text
assets/
│
├── logos/
│   ├── master/
│   │   ├── symbol-master.svg
│   │   └── construction-grid.svg
│   │
│   ├── symbol.svg
│   ├── wordmark.svg
│   ├── logo.svg
│   ├── logo-dark.svg
│   ├── logo-light.svg
│   ├── logo-black.svg
│   └── logo-white.svg
│
├── icons/
│
├── favicons/
│   ├── favicon.svg
│   ├── favicon.ico
│   ├── apple-touch-icon.png
│   ├── icon-192.png
│   └── icon-512.png
│
├── illustrations/
│
└── sources/
```

Chaque dossier possède une responsabilité unique.

---

# Source of Truth

Le fichier :

```text
logos/master/symbol-master.svg
```

constitue **la référence absolue** de l'identité graphique d'Ohanna.

Toutes les variantes du logo sont générées à partir de ce fichier.

Aucun autre logo ne doit être modifié directement.

Toute évolution graphique doit être réalisée sur le symbole maître avant d'être propagée aux autres formats.

Cette règle garantit la cohérence de l'ensemble de la plateforme.

---

# Logos

Le dossier `logos/` contient les différentes variantes du logo officiel.

## Symbol

Le symbole seul.

Utilisé notamment pour :

- favicon ;
- PWA ;
- application mobile ;
- avatar ;
- icône de fenêtre.

---

## Wordmark

Version typographique.

Utilisée lorsque le symbole est déjà identifié.

---

## Logo

Version complète :

- symbole
- mot-symbole

C'est la version par défaut.

---

## Variantes

Les variantes disponibles sont :

```text
logo.svg
logo-dark.svg
logo-light.svg
logo-black.svg
logo-white.svg
```

Chaque variante possède un usage spécifique.

---

# Symbol Master

Le symbole maître est construit selon une géométrie unique.

Il définit notamment :

- proportions ;
- courbes ;
- rayons ;
- gradients ;
- espace négatif ;
- grille de construction.

Il n'est jamais utilisé directement dans une application.

---

# Construction Grid

Le fichier :

```text
construction-grid.svg
```

décrit :

- la grille de construction ;
- les axes ;
- les cercles de référence ;
- les proportions du symbole.

Il sert uniquement à documenter la construction du logo.

---

# Icônes

Toutes les icônes sont dessinées dans une grille commune.

Format de référence :

```text
24 × 24 px
```

Les principes sont :

- simplicité ;
- lisibilité ;
- cohérence ;
- faible niveau de détail.

Les icônes utilisent principalement :

```css
currentColor
```

afin d'être automatiquement compatibles avec les thèmes clair et sombre.

---

# Illustrations

Les illustrations représentent des situations particulières :

- erreur ;
- maintenance ;
- absence de données ;
- connexion ;
- chargement.

Le style reste cohérent avec le reste de la plateforme.

---

# Favicons

Les ressources destinées aux navigateurs sont regroupées dans :

```text
favicons/
```

Les fichiers officiels sont :

```text
favicon.svg
favicon.ico
apple-touch-icon.png
icon-192.png
icon-512.png
```

Ils sont générés à partir du symbole maître.

---

# Formats

## SVG

Le SVG est le format de référence.

Chaque fichier doit :

- être autonome ;
- être optimisé ;
- ne contenir aucune ressource externe ;
- ne contenir aucune police embarquée ;
- utiliser un `viewBox` correct ;
- rester parfaitement scalable.

---

## PNG

Les PNG sont exclusivement des exports.

Ils ne constituent jamais une source de modification.

---

## ICO

Le favicon est généré à partir du SVG officiel.

Il ne doit jamais être modifié manuellement.

---

# Palette

Les couleurs proviennent exclusivement du Design System.

Aucune couleur supplémentaire ne doit être introduite dans les assets sans validation.

Les gradients restent :

- subtils ;
- modernes ;
- cohérents entre eux.

---

# Conventions

Les fichiers utilisent :

- minuscules ;
- tirets (`-`) ;
- extension explicite.

Exemples :

```text
symbol.svg
logo-dark.svg
icon-192.png
switch.svg
mqtt.svg
database.svg
```

Les espaces sont interdits.

---

# Pipeline de génération

Toutes les ressources graphiques suivent le pipeline suivant :

```text
symbol-master.svg
        │
        ▼
symbol.svg
        │
        ▼
logo.svg
        │
        ├──────────────┐
        ▼              ▼
logo-dark.svg     logo-light.svg
        │              │
        └──────┬───────┘
               ▼
      logo-black.svg
      logo-white.svg
               │
               ▼
        favicon.svg
               │
               ▼
        favicon.ico
               │
               ▼
apple-touch-icon.png
icon-192.png
icon-512.png
```

Le symbole maître reste toujours la seule source de génération.

---

# Compatibilité

Les assets doivent fonctionner avec :

- Chrome
- Edge
- Firefox
- Safari
- Progressive Web Apps
- applications desktop
- impression haute résolution.

---

# Accessibilité

Les ressources graphiques respectent les principes suivants :

- contraste suffisant ;
- lisibilité à petite taille ;
- compatibilité fond clair / fond sombre ;
- absence de dépendance à la couleur seule.

Lorsqu'une icône est utilisée seule, elle doit être accompagnée d'un libellé ou d'un texte alternatif lorsque le contexte l'exige.

---

# Maintenance

Toute nouvelle ressource graphique doit respecter :

- le Design System ;
- la palette officielle ;
- les conventions de nommage ;
- la grille officielle ;
- le pipeline de génération.

Les modifications doivent toujours préserver la cohérence visuelle de l'ensemble de la plateforme.

---

# Philosophie

Les assets graphiques d'Ohanna ne cherchent pas à impressionner.

Ils cherchent à rendre une infrastructure complexe immédiatement compréhensible.

Chaque ressource graphique doit transmettre les mêmes valeurs que la plateforme :

- simplicité ;
- clarté ;
- fiabilité ;
- élégance ;
- pérennité.