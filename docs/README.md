# Ohana Platform

![Ohana](Design/assets/logos/logo.svg)

**Ohana Platform** est une plateforme open source d'observabilité et d'administration d'infrastructures, conçue autour d'un modèle déclaratif et pilotée par les capacités (*Capabilities*).

Elle permet de collecter des observations provenant de multiples sources, d'évaluer l'état de santé d'une infrastructure, de conserver son historique et de présenter une vision cohérente de son fonctionnement au travers d'une interface moderne.

La plateforme est composée de plusieurs projets complémentaires partageant une architecture, un modèle de données et une identité visuelle communs.

---

## Les composants

### Ohana-Agent

Agent d'observation chargé d'exécuter les capacités, de collecter les observations et de publier les événements de l'infrastructure.

### Ohana-Vision

Interface web de supervision et d'administration permettant de visualiser l'état de santé, les observations, la topologie et les événements en temps réel.

### Ohana-Installer

Installateur Linux/systemd chargé de déployer, mettre à jour et désinstaller les releases officielles décrites par le manifeste de plateforme.

### Ohana-House

Déploiement de référence documentant l'exploitation réelle de l'écosystème Ohana dans l'infrastructure domestique.

---

## Principes

* Architecture modulaire.
* Configuration entièrement déclarative.
* Modèle de données unifié.
* Calcul de santé indépendant des plugins.
* Historisation des états dans le temps.
* Distribution des événements en temps réel.
* Design System commun à l'ensemble des composants.

---

## Documentation

La documentation officielle est organisée autour des thèmes suivants :

* Architecture
* Installation
* Déploiement
* Développement
* API
* Guides d'utilisation
* Références techniques

---

## État du projet

Ohana Platform est actuellement en développement actif.

Les évolutions prévues sont décrites dans la [roadmap](../ROADMAP.md).

L'historique des versions est disponible dans le [changelog](../CHANGELOG.md).

---

## Licence

Ce projet est distribué sous licence MIT.
