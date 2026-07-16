# Layout.md

# Ohanna — Layout System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Le système de mise en page d'Ohanna organise l'information de manière claire, stable et prévisible.

Chaque écran doit permettre à l'utilisateur de :

* comprendre rapidement l'état général de l'infrastructure ;
* identifier les informations prioritaires ;
* naviguer sans effort ;
* retrouver les mêmes repères visuels dans tous les produits.

Le layout privilégie la lisibilité à la densité d'information.

---

# 2. Structure générale

Toutes les applications Ohanna utilisent la structure suivante :

```text
+-----------------------------------------------------------+
| Header                                                    |
+-----------+-----------------------------------------------+
|           |                                               |
| Sidebar   |                                               |
|           |               Content                         |
|           |                                               |
|           |                                               |
+-----------+-----------------------------------------------+
```

Cette organisation est commune à tous les produits.

---

# 3. Hiérarchie des zones

Chaque page suit la hiérarchie suivante :

```text
Application

├── Header
├── Sidebar
└── Content
    ├── Page Header
    ├── Sections
    │   ├── Panels
    │   │   ├── Cards
    │   │   └── Widgets
    │   └── Panels
    └── Footer (optionnel)
```

Chaque niveau possède une responsabilité clairement définie.

---

# 4. Header

Le Header est toujours visible.

Il contient généralement :

* titre de l'application ;
* navigation globale (si nécessaire) ;
* recherche ;
* notifications ;
* informations utilisateur.

Hauteur recommandée :

```text
64 px
```

---

# 5. Sidebar

La Sidebar constitue la navigation principale.

Contenu recommandé :

* logo ;
* navigation ;
* groupes fonctionnels ;
* informations système.

Largeur standard :

```text
280 px
```

Version réduite :

```text
72 px
```

La largeur reste constante sur l'ensemble de l'application.

---

# 6. Zone de contenu

Le contenu principal occupe tout l'espace restant.

Structure :

```text
Page Header

↓

KPI

↓

Sections

↓

Panels

↓

Cards

↓

Widgets
```

Les informations les plus importantes apparaissent en premier.

---

# 7. Page Header

Chaque page commence par un en-tête.

Il contient :

* titre ;
* description (facultative) ;
* actions principales.

Exemple :

```text
Infrastructure

Vue d'ensemble de l'état des services.

[Actualiser]   [Exporter]
```

---

# 8. Sections

Une page est découpée en sections logiques.

Exemples :

* Santé globale
* Topologie
* Timeline
* Observations
* Administration

Chaque section possède un titre clair.

---

# 9. Panels

Les Panels regroupent plusieurs composants autour d'une même fonctionnalité.

Exemples :

* panel Topology ;
* panel Timeline ;
* panel Incidents.

Un panel ne mélange pas plusieurs domaines fonctionnels.

---

# 10. Cards

Les Cards présentent une information autonome.

Une carte ne contient qu'une seule idée principale.

Exemples :

* KPI ;
* service ;
* capacité ;
* plugin.

---

# 11. Widgets

Les widgets représentent les composants métier.

Exemples :

* Timeline ;
* Infrastructure Map ;
* Incident Feed ;
* Health Ring.

Ils sont placés à l'intérieur des Cards ou des Panels selon leur complexité.

---

# 12. Grille

Le contenu repose sur une grille de **12 colonnes**.

Espacement entre colonnes :

```text
24 px
```

Les composants doivent s'aligner sur cette grille.

---

# 13. Largeurs recommandées

| Élément         |            Largeur |
| --------------- | -----------------: |
| Sidebar         |             280 px |
| Sidebar réduite |              72 px |
| Carte KPI       |       280 à 360 px |
| Panel           | largeur disponible |
| Dialogue        |       480 à 720 px |
| Formulaire      |       480 à 640 px |

---

# 14. Dashboard

La page d'accueil suit toujours la même organisation :

```text
Page Header

↓

KPI

↓

Alertes actives

↓

Topologie

↓

Timeline

↓

Observations récentes

↓

Événements
```

Cette hiérarchie reste identique dans toutes les installations.

---

# 15. Détails d'un équipement

La vue détaillée d'un équipement est organisée ainsi :

```text
Résumé

↓

État actuel

↓

Historique

↓

Timeline

↓

Observations

↓

Dépendances
```

Les informations les plus récentes apparaissent en premier.

---

# 16. Pages d'administration

Les interfaces d'administration suivent la structure :

```text
Liste

↓

Filtres

↓

Détails

↓

Actions
```

Les actions destructrices sont regroupées en fin de page.

---

# 17. Responsive

## Desktop

Sidebar visible.

Grille complète.

---

## Tablet

Sidebar repliable.

Réduction du nombre de colonnes.

---

## Mobile

Sidebar masquée.

Navigation par tiroir.

Les widgets sont affichés sur une seule colonne.

---

# 18. Alignement

Tous les composants sont alignés sur la grille.

Les éléments de même niveau partagent :

* la même marge ;
* le même padding ;
* les mêmes espacements.

Les alignements approximatifs sont interdits.

---

# 19. Densité

Le contenu doit rester aéré.

La densité visuelle ne doit jamais empêcher la lecture.

Une page très chargée doit être découpée en plusieurs sections ou vues.

---

# 20. Défilement

Le défilement vertical est privilégié.

Le défilement horizontal doit être évité.

Seuls les tableaux volumineux peuvent utiliser un défilement horizontal.

---

# 21. États vides

Lorsqu'une section ne contient aucune donnée, elle affiche :

* une illustration simple ;
* un message explicite ;
* une action éventuelle.

La structure générale de la page reste inchangée.

---

# 22. Gestion des erreurs

Une erreur ne doit jamais modifier la structure du layout.

Le composant concerné affiche son propre état d'erreur.

Le reste de la page continue de fonctionner normalement.

---

# 23. Cohérence

Toutes les applications de la plateforme utilisent :

* la même grille ;
* les mêmes marges ;
* les mêmes largeurs ;
* les mêmes règles de composition.

Le passage d'un produit Ohanna à un autre doit être naturel.

---

# 24. Évolutivité

Le layout est conçu pour accueillir de nouveaux modules sans remettre en cause sa structure.

De nouvelles sections ou de nouveaux widgets peuvent être ajoutés sans modifier les principes fondamentaux définis dans ce document.

---

# 25. Principe fondamental

Le layout doit guider naturellement le regard de l'utilisateur.

En quelques secondes, celui-ci doit pouvoir :

1. identifier l'état global de l'infrastructure ;
2. repérer les anomalies éventuelles ;
3. accéder rapidement aux informations détaillées ;
4. agir sans avoir à rechercher les fonctions essentielles.

La mise en page n'est pas un élément décoratif : elle constitue un outil de compréhension et de pilotage de l'infrastructure.
