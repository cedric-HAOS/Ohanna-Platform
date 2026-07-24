# Colors.md

# Ohana — Color System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

La palette d'Ohana repose sur un principe simple :

* fond sombre pour réduire la fatigue visuelle ;
* contraste élevé pour favoriser la lisibilité ;
* une couleur d'accent unique pour guider le regard ;
* des couleurs métier réservées exclusivement à l'état des services.

Chaque couleur possède un rôle précis.

Une couleur ne doit jamais être utilisée en dehors de son usage défini.

---

# 2. Palette principale

## Background

Couleur principale de l'application.

| Variable             | Valeur    |
| -------------------- | --------- |
| `--color-background` | `#08131D` |

Utilisation :

* fond de l'application
* sidebar
* arrière-plan général

---

## Surface

Surface principale des panneaux.

| Variable          | Valeur    |
| ----------------- | --------- |
| `--color-surface` | `#0F2231` |

Utilisation :

* cartes
* widgets
* tableaux
* panneaux

---

## Surface secondaire

Utilisée pour créer de la profondeur.

| Variable                    | Valeur    |
| --------------------------- | --------- |
| `--color-surface-secondary` | `#16384C` |

Utilisation :

* panneaux internes
* éléments sélectionnés
* groupes

---

## Surface active

Surface d'un composant actif.

| Variable                 | Valeur    |
| ------------------------ | --------- |
| `--color-surface-active` | `#1E4860` |

Utilisation :

* élément sélectionné
* ligne active
* menu actif

---

# 3. Couleur d'accent

Le turquoise est la signature graphique d'Ohana.

Il représente :

* l'observabilité ;
* la connectivité ;
* les flux ;
* les données en temps réel.

| Variable          | Valeur    |
| ----------------- | --------- |
| `--color-primary` | `#2ED3D6` |

---

## Accent clair

| Variable                | Valeur    |
| ----------------------- | --------- |
| `--color-primary-light` | `#6DE6E8` |

Utilisation :

* hover
* focus
* survol

---

## Accent foncé

| Variable               | Valeur    |
| ---------------------- | --------- |
| `--color-primary-dark` | `#18B2B5` |

Utilisation :

* bouton actif
* états pressés

---

# 4. Couleurs métier

## Healthy

| Variable          | Valeur    |
| ----------------- | --------- |
| `--color-success` | `#37D67A` |

Utilisation :

* healthy
* available
* opérationnel

---

## Warning

| Variable          | Valeur    |
| ----------------- | --------- |
| `--color-warning` | `#FFB547` |

Utilisation :

* dégradation
* attention
* maintenance

---

## Critical

| Variable        | Valeur    |
| --------------- | --------- |
| `--color-error` | `#FF5C70` |

Utilisation :

* panne
* erreur
* critique

---

## Unknown

| Variable          | Valeur    |
| ----------------- | --------- |
| `--color-unknown` | `#6F7D8A` |

Utilisation :

* état inconnu
* non observé
* indisponible

---

# 5. Texte

## Texte principal

| Variable       | Valeur    |
| -------------- | --------- |
| `--color-text` | `#F4F7FA` |

Utilisation :

* titres
* contenu principal

---

## Texte secondaire

| Variable                 | Valeur    |
| ------------------------ | --------- |
| `--color-text-secondary` | `#B8C4CF` |

Utilisation :

* descriptions
* métadonnées
* informations secondaires

---

## Texte désactivé

| Variable                | Valeur    |
| ----------------------- | --------- |
| `--color-text-disabled` | `#748392` |

---

# 6. Bordures

## Bordure standard

| Variable         | Valeur    |
| ---------------- | --------- |
| `--color-border` | `#214258` |

---

## Bordure active

| Variable                | Valeur    |
| ----------------------- | --------- |
| `--color-border-active` | `#2ED3D6` |

---

## Bordure discrète

| Variable                | Valeur    |
| ----------------------- | --------- |
| `--color-border-subtle` | `#183140` |

---

# 7. États d'interaction

## Hover

Utilise toujours :

`--color-primary-light`

ou

`--color-surface-active`

---

## Focus

Le focus est représenté par :

* contour turquoise ;
* contraste élevé ;
* visibilité clavier.

Aucun autre style de focus n'est autorisé.

---

## Disabled

Les composants désactivés utilisent :

* texte désaturé ;
* fond légèrement assombri ;
* aucune couleur métier.

---

# 8. Couleurs interdites

Les couleurs suivantes ne doivent jamais être utilisées comme couleur principale :

* rouge vif saturé
* bleu électrique
* jaune fluorescent
* vert néon
* violet saturé
* rose vif

Ces couleurs perturbent la hiérarchie visuelle de l'application.

---

# 9. Dégradés

Les dégradés sont interdits sur les composants standards.

Ils peuvent être utilisés uniquement :

* dans le logo ;
* dans certains visuels marketing ;
* dans les illustrations.

---

# 10. Transparence

Les transparences sont limitées aux cas suivants :

* overlays ;
* tooltips ;
* menus flottants ;
* dialogues.

Les composants métier utilisent toujours des couleurs opaques.

---

# 11. Variables CSS officielles

```css
:root {

  --color-background: #08131D;

  --color-surface: #0F2231;
  --color-surface-secondary: #16384C;
  --color-surface-active: #1E4860;

  --color-primary: #2ED3D6;
  --color-primary-light: #6DE6E8;
  --color-primary-dark: #18B2B5;

  --color-success: #37D67A;
  --color-warning: #FFB547;
  --color-error: #FF5C70;
  --color-unknown: #6F7D8A;

  --color-text: #F4F7FA;
  --color-text-secondary: #B8C4CF;
  --color-text-disabled: #748392;

  --color-border: #214258;
  --color-border-active: #2ED3D6;
  --color-border-subtle: #183140;

}
```

---

# 12. Règles fondamentales

* Les couleurs sont utilisées exclusivement via les variables CSS officielles.
* Aucune valeur hexadécimale ne doit être codée directement dans les composants.
* Les couleurs métier (`success`, `warning`, `error`, `unknown`) sont réservées à la représentation de l'état des capacités et des services.
* Le turquoise (`primary`) constitue la signature visuelle d'Ohana et ne doit jamais être remplacé par une autre couleur d'accent.
* Toute nouvelle couleur doit être ajoutée à ce document avant son utilisation dans le projet.
