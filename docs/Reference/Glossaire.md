# Glossaire de la plateforme Ohanna

## Introduction

Ce document rassemble les définitions officielles des concepts utilisés dans l'ensemble de la plateforme Ohanna.

Il constitue la référence terminologique de l'écosystème.

Les autres documents de la plateforme utilisent les définitions présentées ici afin de garantir une terminologie cohérente.

Toute nouvelle notion métier introduite dans Ohanna doit être définie dans ce glossaire avant d'être utilisée dans la documentation ou le code.

---

# A

## Administration

Ensemble des opérations permettant de configurer, piloter et maintenir la plateforme.

---

## Agent

Produit chargé d'observer l'infrastructure, d'exécuter les capacités et de produire les observations utilisées par le reste de la plateforme.

Voir également : **Ohanna Agent**.

---

## API

Interface publique permettant aux différents composants de la plateforme d'échanger des informations au travers d'un contrat stable.

---

## Architecture Decision Record (ADR)

Document décrivant une décision d'architecture importante, son contexte et ses conséquences.

---

# C

## Capability

Unité fonctionnelle fondamentale de la plateforme.

Une capacité représente un service observable fourni par une infrastructure.

Chaque capacité produit des observations décrivant son état.

---

## Capability Identifier

Identifiant unique d'une capacité.

Il permet de distinguer une capacité de toutes les autres au sein de la plateforme.

---

## Configuration

Description déclarative du comportement attendu d'un composant.

La configuration exprime l'intention sans décrire l'implémentation.

---

## Connector

Composant assurant les échanges entre Ohanna Agent et un système externe.

---

# D

## Dashboard

Vue synthétique présentant l'état général de la plateforme.

Le tableau de bord rassemble les principaux indicateurs de supervision.

---

## Deployment

Organisation des composants de la plateforme dans un environnement d'exécution.

---

# E

## Event

Information représentant un changement significatif intervenant dans la plateforme.

Les événements permettent aux composants de réagir sans dépendance directe.

---

## Event Bus

Composant chargé de diffuser les événements entre les différentes parties du runtime.

---

# G

## Health

Évaluation synthétique de l'état d'une capacité, d'un service, d'un nœud ou de l'infrastructure.

---

## Health Engine

Composant chargé de calculer l'état de santé à partir des observations.

---

# I

## Infrastructure

Ensemble des équipements, services et ressources supervisés par la plateforme.

L'infrastructure est indépendante des composants Ohanna.

---

## Interface publique

Point d'échange officiel entre deux composants de la plateforme.

Les interfaces publiques constituent les contrats de communication.

---

# N

## Node

Équipement physique ou logique appartenant à l'infrastructure supervisée.

Un nœud peut héberger plusieurs services.

---

## Node Identifier

Identifiant unique d'un nœud.

---

# O

## Observation

Information produite par une capacité afin de décrire son état à un instant donné.

Une observation est immuable après sa publication.

Elle constitue la source de vérité de la plateforme.

---

## Observation Status

État fonctionnel observé pour une capacité.

Les statuts sont définis par le modèle d'observation de la plateforme.

---

## Ohanna Agent

Produit chargé de superviser les capacités et de produire les observations.

---

## Ohanna House

Déploiement de référence de la plateforme.

Il valide les choix d'architecture dans une infrastructure réelle.

---

## Ohanna Platform

Référentiel officiel de la plateforme.

Il regroupe l'architecture, les guides, les ressources communes et les décisions transversales.

---

## Ohanna Vision

Produit chargé de présenter les informations produites par Ohanna Agent.

---

# P

## Plugin

Composant spécialisé implémentant une capacité métier.

Les plugins sont exécutés par le runtime.

---

## Projection

Transformation d'informations techniques en représentations adaptées à une interface utilisateur.

---

# R

## Runtime

Cœur d'exécution d'Ohanna Agent.

Il orchestre les plugins, les événements, les observations et les différents moteurs internes.

---

# S

## Scheduler

Composant chargé de planifier l'exécution des capacités.

---

## Service

Fonction observable fournie par un nœud de l'infrastructure.

Un service peut exposer une ou plusieurs capacités.

---

## Service Identifier

Identifiant unique d'un service.

---

## State Period

Période continue pendant laquelle une capacité conserve le même état.

Une période possède un instant de début, un instant de fin et un statut.

---

# T

## Timeline

Représentation chronologique des périodes d'état d'une capacité, d'un service, d'un nœud ou de l'infrastructure.

---

## Timeline Engine

Composant chargé de construire les périodes d'état à partir des observations successives.

---

# U

## Utilisateur

Personne exploitant la plateforme afin de superviser ou d'administrer une infrastructure.

---

# V

## Vision

Voir **Ohanna Vision**.

---

# Principes terminologiques

Les termes définis dans ce glossaire possèdent une signification unique dans l'ensemble de la plateforme.

Les documents de référence, les guides, les ADR et le code doivent utiliser cette terminologie de manière cohérente.

Lorsqu'un terme possède une définition officielle dans ce glossaire, cette définition prévaut sur toute autre interprétation.

---

# Évolution du glossaire

Le glossaire est un document vivant.

Toute nouvelle notion métier introduite dans l'écosystème Ohanna doit être ajoutée à ce document.

Les modifications importantes de la terminologie peuvent faire l'objet d'un Architecture Decision Record lorsqu'elles impactent plusieurs produits de la plateforme.
