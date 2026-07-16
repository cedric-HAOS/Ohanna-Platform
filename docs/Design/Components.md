# Components.md

# Ohanna — UI Components

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Les composants constituent les briques fondamentales de toutes les interfaces Ohanna.

Chaque composant doit être :

* simple ;
* réutilisable ;
* accessible ;
* cohérent avec le Design System ;
* indépendant de la logique métier.

Un composant possède une responsabilité unique.

---

# 2. Principes généraux

Tous les composants respectent les documents suivants :

* Brand.md
* Colors.md
* Typography.md
* Spacing.md

Ils utilisent exclusivement :

* les couleurs officielles ;
* les espacements officiels ;
* les rayons officiels ;
* les typographies officielles.

---

# 3. États communs

Tous les composants interactifs possèdent les états suivants lorsqu'ils sont applicables :

* Default
* Hover
* Focus
* Active
* Selected
* Disabled
* Loading
* Error

Aucun état spécifique ne doit être inventé sans validation du Design System.

---

# 4. Button

## Usage

Déclenche une action.

## Variantes

* Primary
* Secondary
* Ghost
* Danger

## États

* Default
* Hover
* Active
* Focus
* Disabled
* Loading

## Règles

* un seul bouton Primary par zone d'action ;
* largeur adaptée au contenu ;
* icône facultative ;
* texte toujours explicite.

---

# 5. Icon Button

## Usage

Action compacte.

Utilisé dans :

* toolbar ;
* tableaux ;
* cartes ;
* panneaux.

Toujours accompagné d'un tooltip.

---

# 6. Card

## Usage

Conteneur principal d'information.

Contient généralement :

* titre ;
* description ;
* contenu ;
* actions.

Toutes les cartes utilisent :

* fond Surface ;
* rayon standard ;
* padding officiel.

---

# 7. Panel

Conteneur de grande taille regroupant plusieurs composants.

Exemples :

* Timeline
* Topology
* Dashboard
* Administration

---

# 8. Section

Sépare les grandes parties d'une page.

Une section possède :

* un titre ;
* éventuellement une description ;
* son contenu.

---

# 9. Badge

Affiche une information courte.

Exemples :

* Version
* Plugin
* Type
* Rôle

Ne doit jamais remplacer un bouton.

---

# 10. Health Badge

Composant spécifique à Ohanna.

Affiche l'état métier.

Valeurs officielles :

* Healthy
* Warning
* Critical
* Unknown

La couleur seule ne doit jamais être le seul indicateur.

Une icône accompagne toujours le texte.

---

# 11. Status Dot

Petit indicateur circulaire.

Utilisé dans :

* listes ;
* tableaux ;
* arbres ;
* topologie.

Toujours associé à un libellé.

---

# 12. Alert

Affiche une information importante.

Variantes :

* Information
* Success
* Warning
* Error

Les alertes restent rares.

---

# 13. Toast

Notification temporaire.

Durée recommandée :

* 3 à 5 secondes.

Ne doit jamais bloquer l'utilisateur.

---

# 14. Dialog

Fenêtre de confirmation.

Utilisée pour :

* suppression ;
* arrêt ;
* redémarrage ;
* validation.

Les actions destructrices sont clairement identifiées.

---

# 15. Modal

Fenêtre contenant un formulaire ou un contenu complexe.

La fermeture est toujours possible sans action destructive.

---

# 16. Tooltip

Affiche une aide contextuelle.

Doit rester concise.

Maximum :

* deux lignes.

---

# 17. Table

Affiche des données structurées.

Fonctionnalités autorisées :

* tri ;
* filtrage ;
* recherche ;
* pagination ;
* sélection.

Les tableaux restent lisibles sur petits écrans.

---

# 18. Timeline

Composant métier Ohanna.

Affiche les périodes d'état.

Chaque période est représentée par :

* une couleur métier ;
* une durée ;
* un intervalle temporel.

La timeline repose exclusivement sur les périodes calculées par le Timeline Engine.

---

# 19. Topology View

Composant métier Ohanna.

Affiche :

* équipements ;
* dépendances ;
* liens.

Fonctionnalités :

* zoom ;
* déplacement ;
* sélection ;
* recentrage.

---

# 20. KPI Card

Affiche un indicateur synthétique.

Structure :

* valeur ;
* libellé ;
* variation éventuelle ;
* icône.

Une KPI Card présente une seule métrique.

---

# 21. Progress

Affiche une progression.

Utilisations :

* synchronisation ;
* import ;
* déploiement ;
* sauvegarde.

Ne représente jamais un état de santé.

---

# 22. Spinner

Indique un chargement.

Il doit disparaître dès que l'information est disponible.

---

# 23. Skeleton

Affichage temporaire avant le chargement.

Préféré au Spinner pour les contenus importants.

---

# 24. Search Field

Champ de recherche.

Peut intégrer :

* filtre ;
* raccourci clavier ;
* effacement rapide.

---

# 25. Dropdown

Sélection parmi plusieurs valeurs.

Lorsque le nombre d'éléments devient important, utiliser une recherche intégrée.

---

# 26. Tabs

Navigation horizontale.

Chaque onglet conserve son état.

---

# 27. Sidebar

Navigation principale.

Contient :

* logo ;
* navigation ;
* informations système.

La largeur reste constante.

---

# 28. Top Bar

Barre supérieure.

Contient généralement :

* titre de la page ;
* recherche ;
* notifications ;
* profil utilisateur.

---

# 29. Breadcrumb

Affiche le chemin de navigation.

Utilisé uniquement lorsque la hiérarchie dépasse deux niveaux.

---

# 30. Empty State

Affiché lorsqu'aucune donnée n'est disponible.

Il comporte :

* une illustration simple ;
* un message clair ;
* une action éventuelle.

---

# 31. Error State

Présenté lorsqu'une opération échoue.

Il indique :

* le problème ;
* les conséquences ;
* l'action possible.

---

# 32. Widgets métier

Les widgets officiels de la plateforme sont :

* Infrastructure Map
* Timeline
* Health Ring
* Capability Matrix
* Service Health
* Node Health
* Incident Feed
* Recent Observations
* Event Stream
* Availability Gauge
* Latency Chart
* Dependency Graph

Ils constituent les composants de plus haut niveau de l'interface.

---

# 33. Composition

Les composants sont conçus pour être assemblés selon la hiérarchie suivante :

```text
Page
└── Section
    └── Panel
        └── Card
            ├── Header
            ├── Content
            └── Actions
```

Chaque niveau possède une responsabilité distincte.

---

# 34. Accessibilité

Tous les composants interactifs doivent :

* être navigables au clavier ;
* disposer d'un état Focus visible ;
* respecter les contrastes définis dans Colors.md ;
* fournir un libellé accessible lorsque nécessaire ;
* fonctionner sans dépendre uniquement de la couleur.

---

# 35. Règles fondamentales

* Un composant répond à une seule responsabilité.
* Un composant est réutilisable dans plusieurs produits Ohanna.
* Les composants métier (Timeline, Topology, Health Badge, KPI Card, etc.) sont spécifiques à l'écosystème Ohanna.
* Les composants génériques (Button, Card, Modal, Table, etc.) peuvent être utilisés dans tous les modules.
* Toute création d'un nouveau composant doit être validée avant son intégration au Design System.
* Les composants existants doivent être enrichis avant d'en créer de nouveaux afin de préserver la cohérence et de limiter la duplication.
