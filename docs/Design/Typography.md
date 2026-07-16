# Typography.md

# Ohanna — Typography System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

La typographie d'Ohanna poursuit trois objectifs :

* lisibilité maximale ;
* hiérarchie visuelle claire ;
* cohérence entre tous les produits.

Le texte est un élément fonctionnel de l'interface.

Il ne doit jamais devenir un élément décoratif.

---

# 2. Police officielle

La famille de caractères officielle d'Ohanna est :

```text
Inter
```

Elle est utilisée dans l'ensemble des applications :

* Ohanna-Agent
* Ohanna-Vision
* documentation web
* site internet
* tableaux de bord
* interfaces d'administration

Aucune autre police ne doit être utilisée pour l'interface utilisateur.

---

# 3. Police de secours

En cas d'indisponibilité d'Inter :

```css
font-family:
    "Inter",
    "Segoe UI",
    "Helvetica Neue",
    Arial,
    sans-serif;
```

---

# 4. Police monospace

Le texte technique utilise exclusivement :

```text
JetBrains Mono
```

Utilisations :

* identifiants
* chemins
* commandes
* logs
* adresses IP
* DNS
* YAML
* JSON
* code source

Police de secours :

```css
font-family:
    "JetBrains Mono",
    "Cascadia Code",
    Consolas,
    monospace;
```

---

# 5. Échelle typographique

## Display

| Nom        | Taille | Poids | Usage                 |
| ---------- | -----: | ----: | --------------------- |
| Display XL |  40 px |   700 | Pages exceptionnelles |
| Display L  |  36 px |   700 | Écrans d'accueil      |

---

## Titres

| Nom | Taille | Poids |
| --- | -----: | ----: |
| H1  |  32 px |   700 |
| H2  |  28 px |   700 |
| H3  |  24 px |   600 |
| H4  |  20 px |   600 |
| H5  |  18 px |   600 |
| H6  |  16 px |   600 |

---

## Texte courant

| Nom     | Taille | Poids |
| ------- | -----: | ----: |
| Large   |  18 px |   400 |
| Body    |  16 px |   400 |
| Small   |  14 px |   400 |
| Caption |  13 px |   400 |
| Tiny    |  12 px |   400 |

---

# 6. Poids autorisés

Seuls les poids suivants sont utilisés.

| Poids | Utilisation   |
| ----- | ------------- |
| 400   | texte courant |
| 500   | boutons       |
| 600   | sous-titres   |
| 700   | titres        |

Les poids 100, 200, 300, 800 et 900 sont interdits.

---

# 7. Hauteur de ligne

| Taille | Line Height |
| ------ | ----------: |
| 40 px  |       48 px |
| 36 px  |       44 px |
| 32 px  |       40 px |
| 28 px  |       36 px |
| 24 px  |       32 px |
| 20 px  |       28 px |
| 18 px  |       26 px |
| 16 px  |       24 px |
| 14 px  |       20 px |
| 13 px  |       18 px |
| 12 px  |       16 px |

Une hauteur de ligne généreuse améliore la lisibilité sur les tableaux de bord.

---

# 8. Espacement des lettres

Par défaut :

```text
0
```

Les seuls ajustements autorisés sont :

Display :

```text
-0.02em
```

Titres :

```text
-0.01em
```

Texte :

```text
0
```

Ne jamais augmenter artificiellement l'espacement des lettres.

---

# 9. Couleurs du texte

Le système de couleurs est défini dans **Colors.md**.

Utilisation :

| Variable                 | Usage            |
| ------------------------ | ---------------- |
| `--color-text`           | texte principal  |
| `--color-text-secondary` | texte secondaire |
| `--color-text-disabled`  | texte désactivé  |

Aucune couleur codée en dur n'est autorisée.

---

# 10. Alignement

Par défaut :

* texte aligné à gauche ;
* titres alignés à gauche.

Le texte centré est réservé :

* aux pages d'accueil ;
* aux états vides ;
* aux écrans de bienvenue.

Le texte justifié est interdit.

---

# 11. Longueur des lignes

Pour conserver une excellente lisibilité :

* idéal : 60 à 80 caractères ;
* maximum : 100 caractères.

Les paragraphes très larges doivent être évités.

---

# 12. Hiérarchie

Chaque écran doit suivre la hiérarchie suivante :

```text
Titre principal

Sous-titre

Section

Carte

Texte

Légende
```

Il ne doit jamais y avoir plusieurs niveaux H1 sur une même vue.

---

# 13. Utilisation du gras

Le gras sert uniquement à mettre en évidence une information importante.

Il ne doit pas remplacer une couleur ou une icône.

Éviter les paragraphes entiers en gras.

---

# 14. Utilisation de l'italique

L'italique est réservé :

* aux citations ;
* aux notes.

Il ne doit jamais servir à hiérarchiser l'interface.

---

# 15. Majuscules

Les titres utilisent une casse naturelle.

Exemple :

```text
Infrastructure
```

et non :

```text
INFRASTRUCTURE
```

Les majuscules complètes sont réservées :

* aux acronymes ;
* aux codes techniques.

---

# 16. Nombres

Les valeurs numériques importantes utilisent des chiffres tabulaires lorsque la police le permet.

Exemples :

* temps de réponse ;
* pourcentages ;
* latence ;
* disponibilité ;
* compteurs.

Cela évite les déplacements visuels lors des mises à jour.

---

# 17. Code

Les blocs de code utilisent toujours :

* JetBrains Mono ;
* fond `--color-surface-secondary` ;
* bordure `--color-border`.

Le code n'est jamais affiché avec la police principale.

---

# 18. Accessibilité

Le texte doit respecter les principes suivants :

* contraste conforme aux recommandations WCAG AA ;
* taille minimale de 14 px pour le texte courant ;
* taille minimale de 12 px uniquement pour les légendes ou métadonnées ;
* aucune information critique ne repose uniquement sur la couleur.

---

# 19. Variables CSS officielles

```css
:root {

    --font-family:
        "Inter",
        "Segoe UI",
        "Helvetica Neue",
        Arial,
        sans-serif;

    --font-family-mono:
        "JetBrains Mono",
        "Cascadia Code",
        Consolas,
        monospace;

    --font-size-display-xl: 40px;
    --font-size-display-l: 36px;

    --font-size-h1: 32px;
    --font-size-h2: 28px;
    --font-size-h3: 24px;
    --font-size-h4: 20px;
    --font-size-h5: 18px;
    --font-size-h6: 16px;

    --font-size-large: 18px;
    --font-size-body: 16px;
    --font-size-small: 14px;
    --font-size-caption: 13px;
    --font-size-tiny: 12px;

}
```

---

# 20. Règles fondamentales

* Inter est la seule police utilisée pour l'interface utilisateur.
* JetBrains Mono est réservée au contenu technique.
* Les tailles et les poids sont limités à ceux définis dans ce document.
* La hiérarchie typographique doit rester identique dans tous les produits Ohanna.
* La lisibilité prévaut toujours sur les effets visuels.
* Toute évolution de la typographie doit être validée au niveau du Design System avant son adoption.
