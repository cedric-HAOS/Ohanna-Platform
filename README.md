# Ohanna Platform

Ohanna Platform est une plateforme modulaire de supervision d’infrastructure.

Elle collecte des observations techniques, construit une représentation de l’état des services et présente ces informations dans une interface Web temps réel.

La plateforme repose sur deux composants indépendants :

* **Ohanna-Agent**, responsable de la collecte et de l’export des observations ;
* **Ohanna-Vision**, responsable de leur ingestion, de leur traitement et de leur visualisation.

## Architecture

```text
Infrastructure
      │
      ▼
Ohanna-Agent
      │
Observations REST
      │
      ▼
Ohanna-Vision
      │
      ▼
Dashboard Web
```

## Composants

### Ohanna-Agent

Ohanna-Agent exécute les plugins de supervision, planifie les vérifications et produit des observations normalisées.

Dépôt :

```text
https://github.com/cedric-HAOS/Ohanna-Agent
```

### Ohanna-Vision

Ohanna-Vision reçoit les observations, construit les timelines métier, calcule l’état de santé de l’infrastructure et alimente le tableau de bord temps réel.

Dépôt :

```text
https://github.com/cedric-HAOS/Ohanna-Vision
```

## Documentation

La documentation principale de la plateforme est disponible dans le répertoire [`docs`](docs/).

Documents de référence :

* [Architecture](docs/Architecture.md)
* [Installation de la plateforme](docs/Installer-Ohanna-Platform.md)
* [Exploitation](docs/Operations.md)
* [Dépannage](docs/Troubleshooting.md)
* [Feuille de route](ROADMAP.md)
* [Historique des versions](CHANGELOG.md)

## Installation

La procédure complète de déploiement d’Ohanna-Agent et d’Ohanna-Vision est décrite dans :

```text
docs/Installer-Ohanna-Platform.md
```

## Statut

La première génération de la plateforme comprend :

* le runtime et le système de plugins d’Ohanna-Agent ;
* l’infrastructure déclarative ;
* la production et l’export d’observations ;
* l’API d’ingestion d’Ohanna-Vision ;
* le moteur de timeline ;
* le moteur de santé ;
* la topologie interactive ;
* le tableau de bord temps réel ;
* la diffusion WebSocket.

## Licence

Le projet est distribué selon les conditions décrites dans le fichier [LICENSE](LICENSE).
