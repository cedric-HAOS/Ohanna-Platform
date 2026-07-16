# Icons.md

# Ohanna — Iconography System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Les icônes facilitent l'identification rapide des actions, des objets et des états.

Elles complètent le texte mais ne le remplacent pas.

Une icône ne doit jamais être utilisée uniquement pour décorer une interface.

Chaque icône possède une signification précise et constante dans l'ensemble de la plateforme.

---

# 2. Bibliothèque officielle

L'unique bibliothèque d'icônes utilisée par Ohanna est :

```text
Lucide
```

Toutes les applications utilisent cette bibliothèque.

Le mélange de plusieurs bibliothèques est interdit.

---

# 3. Style

Les icônes utilisent exclusivement :

* style outline ;
* traits réguliers ;
* formes simples ;
* géométrie cohérente.

Les variantes remplies ("filled") ne sont pas utilisées dans l'interface.

---

# 4. Dimensions officielles

| Taille | Usage                 |
| ------ | --------------------- |
| 16 px  | texte, tableaux       |
| 20 px  | boutons, navigation   |
| 24 px  | cartes, panneaux      |
| 32 px  | illustrations légères |
| 48 px  | états vides           |

Aucune autre taille n'est recommandée.

---

# 5. Épaisseur

L'épaisseur des traits reste celle fournie par Lucide.

Elle ne doit pas être modifiée.

---

# 6. Couleurs

Les icônes utilisent les couleurs définies dans **Colors.md**.

Par défaut :

* `--color-text`
* `--color-text-secondary`

Les couleurs métier sont réservées aux états.

---

# 7. Espacement

Une icône est toujours séparée de son texte par :

```text
8 px
```

Deux icônes adjacentes sont espacées de :

```text
12 px
```

---

# 8. Accessibilité

Les icônes purement décoratives sont masquées aux technologies d'assistance.

Les icônes interactives possèdent :

* un libellé accessible ;
* un état Focus visible ;
* une zone cliquable suffisante.

---

# 9. Navigation

| Fonction        | Icône           |
| --------------- | --------------- |
| Accueil         | House           |
| Tableau de bord | LayoutDashboard |
| Infrastructure  | Network         |
| Services        | Server          |
| Capacités       | Boxes           |
| Timeline        | Clock3          |
| Observations    | Eye             |
| Événements      | Activity        |
| Administration  | Settings        |

Cette correspondance reste identique dans tous les produits.

---

# 10. Actions

| Action      | Icône       |
| ----------- | ----------- |
| Ajouter     | Plus        |
| Modifier    | Pencil      |
| Supprimer   | Trash2      |
| Dupliquer   | Copy        |
| Actualiser  | RefreshCw   |
| Télécharger | Download    |
| Envoyer     | Upload      |
| Rechercher  | Search      |
| Filtrer     | Filter      |
| Trier       | ArrowUpDown |

---

# 11. États système

| État     | Icône         |
| -------- | ------------- |
| Healthy  | CircleCheck   |
| Warning  | TriangleAlert |
| Critical | CircleX       |
| Unknown  | CircleHelp    |

L'icône accompagne toujours la couleur et le texte.

---

# 12. Infrastructure

| Objet           | Icône     |
| --------------- | --------- |
| Infrastructure  | Network   |
| Nœud            | HardDrive |
| Service         | Server    |
| Plugin          | Puzzle    |
| Connecteur      | Plug      |
| Base de données | Database  |
| Stockage        | HardDrive |
| Réseau          | Network   |
| Internet        | Globe     |
| Cloud           | Cloud     |

---

# 13. Observabilité

| Élément       | Icône      |
| ------------- | ---------- |
| Observation   | Eye        |
| Historique    | History    |
| Timeline      | Clock3     |
| Disponibilité | Gauge      |
| Santé         | HeartPulse |
| Latence       | Timer      |
| Journal       | ScrollText |
| Activité      | Activity   |

---

# 14. Administration

| Fonction       | Icône     |
| -------------- | --------- |
| Paramètres     | Settings  |
| Utilisateurs   | Users     |
| Sécurité       | Shield    |
| Journalisation | FileText  |
| Sauvegarde     | Archive   |
| Déploiement    | Rocket    |
| Mise à jour    | RefreshCw |

---

# 15. États d'interaction

Les icônes suivent les mêmes états que les composants :

* Default
* Hover
* Focus
* Active
* Disabled

Aucune animation spécifique n'est appliquée.

---

# 16. Boutons d'icône

Les boutons composés uniquement d'une icône :

* utilisent une taille minimale de 40 × 40 px ;
* disposent d'un tooltip ;
* présentent un état Focus visible.

Ils ne doivent jamais être ambigus.

---

# 17. États vides

Les écrans sans données utilisent des icônes simples de grande taille.

Exemples :

* Inbox
* Search
* Database
* FolderOpen

La taille recommandée est :

```text
48 px
```

---

# 18. Illustrations

Les icônes peuvent être assemblées pour créer des illustrations simples.

Les illustrations complexes doivent être réalisées sous forme de SVG dédiés.

---

# 19. Icônes spécifiques à Ohanna

Certaines représentations sont propres à la plateforme :

* Infrastructure Map
* Capability Matrix
* Timeline
* Health Ring
* Dependency Graph

Lorsqu'une icône standard n'est pas adaptée, un pictogramme SVG spécifique peut être créé.

Il doit respecter le style graphique de Lucide :

* traits fins ;
* géométrie simple ;
* absence de remplissage ;
* proportions cohérentes.

---

# 20. Bonnes pratiques

* Associer une icône à un libellé lorsque cela améliore la compréhension.
* Utiliser la même icône pour représenter le même concept dans toute la plateforme.
* Limiter le nombre d'icônes différentes sur une même vue.
* Préserver une taille cohérente entre les composants.

---

# 21. Pratiques interdites

Il est interdit :

* d'utiliser plusieurs bibliothèques d'icônes ;
* de modifier l'épaisseur des traits ;
* d'étirer ou de déformer une icône ;
* d'utiliser des icônes uniquement comme décoration ;
* de coder une couleur directement dans les composants.

---

# 22. Principe fondamental

Les icônes constituent un langage visuel partagé.

L'utilisateur doit pouvoir reconnaître immédiatement une action, un état ou un élément d'infrastructure sans avoir à réapprendre leur signification d'un écran à l'autre.

La cohérence de l'iconographie contribue directement à la rapidité de lecture et à l'efficacité de l'interface.
