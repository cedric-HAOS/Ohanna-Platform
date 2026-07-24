    # Spacing.md

# Ohana — Spacing System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Le système d'espacement d'Ohana repose sur une grille de **4 pixels**.

Tous les espacements de l'interface sont des multiples de cette unité.

Cette règle garantit :

* une interface harmonieuse ;
* un alignement cohérent ;
* une maintenance simplifiée ;
* une meilleure lisibilité.

Aucun espacement arbitraire ne doit être introduit dans les composants.

---

# 2. Unité de base

L'unité fondamentale est :

```text
4 px
```

Tous les espacements dérivent de cette valeur.

---

# 3. Échelle officielle

| Variable     | Valeur | Usage                  |
| ------------ | -----: | ---------------------- |
| `--space-1`  |   4 px | séparation minimale    |
| `--space-2`  |   8 px | petits espaces         |
| `--space-3`  |  12 px | champs rapprochés      |
| `--space-4`  |  16 px | espacement standard    |
| `--space-5`  |  20 px | composants importants  |
| `--space-6`  |  24 px | sections               |
| `--space-8`  |  32 px | groupes                |
| `--space-10` |  40 px | panneaux               |
| `--space-12` |  48 px | grandes séparations    |
| `--space-16` |  64 px | changement de contexte |

---

# 4. Espacement entre composants

## Deux champs d'un formulaire

```text
16 px
```

---

## Deux boutons

```text
8 px
```

---

## Deux cartes

```text
24 px
```

---

## Deux panneaux

```text
32 px
```

---

## Deux sections

```text
48 px
```

---

# 5. Marges internes

## Boutons

Padding :

```text
8 px 16 px
```

---

## Champs de saisie

Padding :

```text
12 px 16 px
```

---

## Cartes

Padding :

```text
24 px
```

---

## Dialogues

Padding :

```text
32 px
```

---

## Sidebar

Padding :

```text
24 px
```

---

# 6. Structure des cartes

Toutes les cartes suivent la même structure.

```text
+--------------------------------------+

24 px

Titre

12 px

Description

24 px

Contenu

24 px

Actions

24 px

+--------------------------------------+
```

Les espacements internes restent constants.

---

# 7. Structure des pages

Une page standard suit la hiérarchie suivante :

```text
Header

32 px

Titre

24 px

Sous-titre

32 px

Contenu principal
```

Les marges extérieures sont constantes.

---

# 8. Grille

Le contenu principal utilise une grille de **12 colonnes**.

Espacement entre colonnes :

```text
24 px
```

Les cartes s'alignent systématiquement sur cette grille.

---

# 9. Listes

Espacement vertical :

```text
8 px
```

Entre groupes :

```text
24 px
```

---

# 10. Tableaux

Padding horizontal :

```text
16 px
```

Padding vertical :

```text
12 px
```

Hauteur minimale d'une ligne :

```text
44 px
```

---

# 11. Formulaires

Entre deux champs :

```text
16 px
```

Entre deux groupes :

```text
32 px
```

Entre une section et les boutons :

```text
32 px
```

---

# 12. Sidebar

Marge supérieure :

```text
24 px
```

Entre deux éléments :

```text
4 px
```

Entre deux groupes :

```text
24 px
```

---

# 13. Navigation

Les éléments de navigation utilisent :

Padding :

```text
12 px 16 px
```

Espacement entre icône et texte :

```text
12 px
```

---

# 14. Icônes

Entre une icône et un texte :

```text
8 px
```

Entre deux icônes :

```text
12 px
```

---

# 15. Widgets Dashboard

Entre les KPI :

```text
24 px
```

Entre les graphiques :

```text
32 px
```

Entre les groupes de widgets :

```text
48 px
```

---

# 16. Responsive

Les espacements diminuent progressivement sur les petits écrans.

| Taille  | Multiplicateur |
| ------- | -------------: |
| Desktop |          100 % |
| Tablet  |           90 % |
| Mobile  |           75 % |

La hiérarchie reste identique.

---

# 17. Variables CSS officielles

```css
:root {

    --space-1: 4px;
    --space-2: 8px;
    --space-3: 12px;
    --space-4: 16px;
    --space-5: 20px;
    --space-6: 24px;
    --space-8: 32px;
    --space-10: 40px;
    --space-12: 48px;
    --space-16: 64px;

}
```

---

# 18. Bonnes pratiques

Toujours utiliser les variables officielles.

Préférer les espacements réguliers.

Aligner les composants sur la grille.

Conserver des marges identiques pour des éléments de même niveau.

Utiliser davantage d'espace pour séparer des groupes que pour séparer des éléments d'un même groupe.

---

# 19. Pratiques interdites

Il est interdit :

* d'utiliser des valeurs arbitraires (`7 px`, `13 px`, `19 px`, etc.) ;
* de coder directement des marges dans les composants sans passer par les variables ;
* de réduire les espacements pour faire "rentrer" davantage de contenu ;
* de mélanger plusieurs logiques d'espacement sur une même vue.

---

# 20. Principe fondamental

L'espacement fait partie intégrante de l'interface.

L'espace vide n'est jamais considéré comme une perte de place.

Il sert à organiser l'information, à guider le regard et à améliorer la compréhension de l'état de l'infrastructure.

Une interface respirant correctement est plus rapide à lire, moins fatigante et plus efficace au quotidien.
