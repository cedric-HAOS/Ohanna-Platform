# Examples.md

# Ohana — Design System Examples

Version : 1.0
Statut : Référence officielle

---

# 1. Objectif

Ce document présente des exemples d'application du Design System Ohana.

Il illustre :

* la composition des pages ;
* l'utilisation des composants ;
* la hiérarchie visuelle ;
* les états métier ;
* les bonnes pratiques ;
* les erreurs à éviter.

Ces exemples ne remplacent pas les documents spécialisés.

Ils montrent comment appliquer ensemble :

* Brand.md ;
* Colors.md ;
* Typography.md ;
* Spacing.md ;
* Components.md ;
* Layout.md ;
* Icons.md ;
* Animations.md ;
* Widgets.md.

---

# 2. Exemple de page standard

```text
Application Shell

├── Header
├── Sidebar
└── Content
    ├── Page Header
    ├── Section
    │   ├── Panel
    │   └── Panel
    └── Section
```

Exemple :

```text
Infrastructure

Vue d'ensemble des équipements et services observés.

[Actualiser] [Exporter]

Santé globale

[KPI] [KPI] [KPI] [KPI]

Carte de l'infrastructure

[Infrastructure Map]

Topologie

[Topology View]
```

---

# 3. Exemple de Page Header

```text
Infrastructure

Vue d'ensemble des équipements, services et capacités observés.

[Actualiser] [Exporter]
```

Règles appliquées :

* un seul H1 ;
* description courte ;
* action principale visible ;
* actions secondaires regroupées ;
* alignement constant.

---

# 4. Exemple de Dashboard

```text
Vue d'ensemble

État général de la plateforme Ohana.

┌──────────────────────────────────────────────────────┐
│ Santé globale                                        │
│ Healthy                                              │
└──────────────────────────────────────────────────────┘

┌──────────────┐ ┌──────────────┐ ┌──────────────┐
│ 12           │ │ 3            │ │ 98,7 %       │
│ Services     │ │ Alertes      │ │ Disponibilité│
└──────────────┘ └──────────────┘ └──────────────┘

┌──────────────────────────────────────────────────────┐
│ Alertes actives                                      │
└──────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────┐
│ Carte de l'infrastructure                            │
└──────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────┐
│ Timeline                                             │
└──────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────┐
│ Observations récentes                                │
└──────────────────────────────────────────────────────┘
```

---

# 5. Exemple de KPI Card

```text
98,7 %

Disponibilité

Sur les dernières 24 heures
```

Bonnes pratiques :

* valeur dominante ;
* unité visible ;
* libellé explicite ;
* période précisée ;
* une seule métrique.

Mauvais exemple :

```text
98,7 % / 12 services / 3 alertes / +4,2 %
```

Une KPI Card ne doit pas regrouper plusieurs métriques principales.

---

# 6. Exemple de Health Badge

```text
[CircleCheck] Healthy
```

```text
[TriangleAlert] Warning
```

```text
[CircleX] Critical
```

```text
[CircleHelp] Unknown
```

Le texte et l'icône accompagnent toujours la couleur.

Mauvais exemple :

```text
●
```

Un point coloré seul n'est pas suffisamment explicite.

---

# 7. Exemple de carte de service

```text
DNS primaire

Service réseau

[Healthy]

Serveur
infra-01

Dernière observation
Il y a 12 secondes

Latence
18 ms

[Voir le détail]
```

La carte contient une seule entité et ses informations essentielles.

---

# 8. Exemple de vue détaillée d'un équipement

```text
infra-01

Serveur d'infrastructure principal

[Healthy]

Résumé

Adresse IP
192.168.1.10

Services
DNS, DHCP, NTP

Dernière observation
16 juillet 2026 à 08:24

Santé actuelle

[Health Summary]

Timeline

[Timeline]

Capacités

[Capability Matrix]

Observations récentes

[Recent Observations]

Dépendances

[Dependency Graph]
```

---

# 9. Exemple de Timeline

```text
00:00        06:00        12:00        18:00        24:00

[ Healthy ][ Healthy ][ Warning ][ Critical ][ Healthy ]
```

Chaque segment représente une période métier.

Lorsqu'un segment est sélectionné :

```text
Critical

Début
14:32

Fin
14:47

Durée
15 minutes

Cause observée
Échec de résolution DNS
```

---

# 10. Exemple de Topology View

```text
Internet
   │
Freebox
   │
SW-01 ───── SW-02 ───── SW-03
  │            │           │
AP-01       RPI-LINK    HA-Green
                           │
                       RPI-ZWAVE
```

Dans l'interface réelle :

* les liens principaux utilisent le turquoise ;
* les liens secondaires utilisent le gris bleuté ;
* la santé apparaît sur les nœuds ;
* la sélection ouvre le panneau de détails.

---

# 11. Exemple de liste d'observations

| Heure    | Capacité     | Service     | Nœud     | État    | Latence |
| -------- | ------------ | ----------- | -------- | ------- | ------- |
| 08:24:12 | dns.resolve  | dns-primary | infra-01 | Healthy | 18 ms   |
| 08:24:08 | ntp.sync     | ntp-primary | infra-01 | Healthy | 4 ms    |
| 08:23:59 | mqtt.connect | mqtt-main   | ha-green | Warning | 120 ms  |

Les colonnes utilisent des libellés courts.

Les unités restent visibles.

---

# 12. Exemple d'alerte

```text
[TriangleAlert] Résolution DNS dégradée

Le service dns-primary présente une latence supérieure au seuil depuis 7 minutes.

[Voir le service]
```

L'alerte indique :

* le problème ;
* la cible ;
* la durée ;
* l'action possible.

---

# 13. Exemple d'état vide

```text
[History]

Aucune période disponible

Aucune observation n'a encore permis de construire une timeline pour ce service.
```

Un état vide ne doit jamais laisser une zone entièrement blanche ou silencieuse.

---

# 14. Exemple d'état d'erreur

```text
[CircleX]

Impossible de charger la topologie

L'API de topologie ne répond pas.

[Réessayer]
```

L'erreur reste locale au widget.

Les autres parties de la page continuent de fonctionner.

---

# 15. Exemple d'état périmé

```text
[TriangleAlert] Données potentiellement périmées

Dernière mise à jour : 08:14
Actualisation attendue toutes les 30 secondes.
```

---

# 16. Exemple de bouton

## Primary

```text
[Enregistrer]
```

## Secondary

```text
[Annuler]
```

## Ghost

```text
[Voir le détail]
```

## Danger

```text
[Supprimer]
```

Règle :

```text
[Annuler] [Enregistrer]
```

Le bouton principal se place généralement en dernier dans le sens de lecture.

---

# 17. Exemple de formulaire

```text
Nom du service

[ dns-primary                         ]

Adresse du serveur

[ 192.168.1.10                       ]

Intervalle d'observation

[ 30 secondes                    v   ]

[Annuler] [Enregistrer]
```

Règles :

* libellés toujours visibles ;
* pas de placeholder utilisé comme unique libellé ;
* erreurs affichées près du champ ;
* espacements constants.

---

# 18. Exemple d'erreur de formulaire

```text
Adresse du serveur

[ 192.168.1.999                      ]

[CircleX] Adresse IPv4 invalide.
```

Le message explique précisément le problème.

---

# 19. Exemple de modal de confirmation

```text
Arrêter le service ?

Le service dns-primary ne répondra plus aux requêtes pendant son arrêt.

[Annuler] [Arrêter]
```

Les actions destructrices utilisent un verbe explicite.

Mauvais exemple :

```text
Êtes-vous sûr ?

[Non] [Oui]
```

---

# 20. Exemple de Sidebar

```text
Ohana

Vue d'ensemble
Infrastructure
Timeline
Observations
Événements

Administration
Configuration
Plugins
Système
```

Les groupes restent courts et cohérents.

L'élément actif utilise :

* surface active ;
* bordure ou accent turquoise ;
* icône et texte.

---

# 21. Exemple de navigation active

```text
[Network] Infrastructure
```

L'état actif ne repose pas uniquement sur la couleur.

---

# 22. Exemple de Toast

```text
[CircleCheck] Configuration enregistrée
```

Le Toast confirme une action courte.

Il ne remplace pas une erreur persistante ou une alerte métier.

---

# 23. Exemple de widget temps réel

```text
Observations en direct

[Pause]

08:24:12  dns.resolve    Healthy    18 ms
08:24:08  ntp.sync       Healthy     4 ms
08:23:59  mqtt.connect   Warning   120 ms
```

Lorsqu'une nouvelle ligne apparaît :

* elle utilise un fondu court ;
* le scroll n'est pas forcé si l'utilisateur consulte une entrée ancienne ;
* le nombre d'éléments conservés reste limité.

---

# 24. Exemple de Capability Matrix

| Capacité      | infra-01 | ha-green | rpi-link | rpi-zwave |
| ------------- | -------- | -------- | -------- | --------- |
| dns.resolve   | Healthy  | —        | —        | —         |
| ntp.sync      | Healthy  | Healthy  | Healthy  | Healthy   |
| mqtt.connect  | —        | Healthy  | Warning  | Healthy   |
| zwave.runtime | —        | —        | —        | Healthy   |

Le symbole `—` signifie que la capacité ne s'applique pas.

Il ne doit pas être confondu avec l'état Unknown.

---

# 25. Exemple de responsive Desktop

```text
Sidebar | KPI | KPI | KPI
        | Topology        | Details
        | Timeline                 |
```

---

# 26. Exemple de responsive Tablet

```text
Sidebar réduite

KPI | KPI

Topology

Details

Timeline
```

---

# 27. Exemple de responsive Mobile

```text
Header

KPI

KPI

Topology

Details

Timeline

Observations
```

Chaque widget occupe toute la largeur.

---

# 28. Exemple de hiérarchie correcte

```text
Infrastructure              H1

Santé globale               H2

Services critiques          H3

dns-primary                 H4
```

Mauvais exemple :

```text
Infrastructure              H1

Santé globale               H4

Services critiques          H2

dns-primary                 H6
```

Les niveaux ne doivent pas être choisis selon leur apparence visuelle.

---

# 29. Exemple d'espacement correct

```text
Titre
12 px
Description
24 px
Contenu
24 px
Actions
```

Les espacements suivent l'échelle officielle.

Mauvais exemple :

```text
Titre
7 px
Description
19 px
Contenu
13 px
Actions
```

---

# 30. Exemple de couleurs correctes

```css
color: var(--color-text);
background: var(--color-surface);
border-color: var(--color-border);
```

Mauvais exemple :

```css
color: #ffffff;
background: #102331;
border-color: #23506a;
```

Aucune couleur ne doit être codée directement dans un composant.

---

# 31. Exemple de typographie correcte

```css
font-family: var(--font-family);
font-size: var(--font-size-body);
font-weight: 400;
line-height: 24px;
```

---

# 32. Exemple d'icône correcte

```text
[RefreshCw] Actualiser
```

Mauvais exemple :

```text
🔄 Actualiser
```

Les emojis ne remplacent pas les icônes officielles de l'interface.

---

# 33. Exemple d'animation correcte

```text
Hover bouton : 150 ms
Ouverture panneau : 300 ms
Apparition Toast : 200 ms
```

Mauvais exemple :

```text
Bouton qui rebondit pendant 800 ms
Carte qui grossit au survol
Alerte qui clignote en continu
```

---

# 34. Exemple de composition correcte

```text
Page
└── Section
    └── Panel
        ├── Header
        └── Widget
```

Mauvais exemple :

```text
Page
└── Card
    └── Card
        └── Card
            └── Card
```

L'imbrication excessive de conteneurs nuit à la lisibilité.

---

# 35. Exemple de page Administration

```text
Plugins

Gérez les plugins installés sur la plateforme.

[Installer un plugin]

Filtres

[Recherche] [État] [Type]

Liste des plugins

DNS Plugin
Version 0.14.0
[Healthy]
[Configurer]

MQTT Plugin
Version 0.14.0
[Warning]
[Configurer]
```

---

# 36. Exemple de page Configuration

```text
Configuration

Version active
2026.07.16-01

Dernière application
16 juillet 2026 à 08:12

Statut
[Healthy]

Écarts détectés
0

[Valider] [Appliquer une nouvelle configuration]
```

---

# 37. Exemple de page Incident

```text
Incident DNS

[Critical]

Début
16 juillet 2026 à 08:14

Durée
12 minutes

Élément concerné
dns-primary

Cause probable
Le serveur 192.168.1.10 ne répond plus.

Impact
La résolution locale peut échouer.

Timeline

[Health History]

Observations associées

[Recent Observations]
```

---

# 38. Exemple de bonnes pratiques

Une bonne interface Ohana :

* affiche l'état global immédiatement ;
* hiérarchise clairement les anomalies ;
* limite le nombre d'actions principales ;
* précise les périodes et unités ;
* conserve une mise en page stable ;
* utilise les composants officiels ;
* reste compréhensible sans dépendre uniquement de la couleur.

---

# 39. Exemple de mauvaises pratiques

Une interface Ohana ne doit pas :

* empiler trop de cartes ;
* afficher toutes les données sur une seule page ;
* utiliser plusieurs couleurs d'accent ;
* multiplier les animations ;
* mélanger plusieurs bibliothèques d'icônes ;
* masquer les unités ;
* reconstruire la logique métier dans le frontend ;
* modifier la structure d'une page lors d'une erreur ;
* utiliser des valeurs CSS arbitraires.

---

# 40. Principe fondamental

Les exemples présentés dans ce document doivent être considérés comme des modèles de composition.

Toute nouvelle vue doit reprendre les mêmes principes de hiérarchie, d'espacement, de lisibilité, d'accessibilité et de cohérence.

Le Design System n'a pas pour objectif de rendre toutes les pages identiques.

Il doit leur donner un langage commun immédiatement reconnaissable comme appartenant à Ohana.
