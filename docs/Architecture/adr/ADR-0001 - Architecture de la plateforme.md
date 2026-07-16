# ADR-0001 — Architecture de la plateforme

* **Statut** : Accepté
* **Date** : 2026-07-16

---

# Contexte

La plateforme Ohanna a pour objectif de superviser, visualiser et administrer une infrastructure de manière modulaire, observable et extensible.

Au cours de sa conception, plusieurs architectures ont été envisagées.

La première consistait à regrouper l'ensemble des fonctionnalités au sein d'une application unique.

Une seconde approche consistait à séparer les responsabilités entre plusieurs produits spécialisés.

Compte tenu des objectifs de la plateforme, la seconde approche a été retenue.

---

# Décision

La plateforme Ohanna est organisée comme un écosystème de produits indépendants, chacun possédant une responsabilité clairement définie.

Les produits communiquent exclusivement au travers d'interfaces publiques et de modèles partagés.

Chaque produit possède :

* son propre dépôt ;
* son propre cycle de développement ;
* sa propre documentation technique ;
* ses propres Architecture Decision Records (ADR) ;
* ses propres tests.

Les décisions ayant un impact sur l'ensemble de la plateforme sont documentées dans Ohanna Platform.

---

# Organisation des produits

La plateforme est composée des produits suivants.

## Ohanna Platform

Référentiel officiel de la plateforme.

Il rassemble :

* l'architecture ;
* les principes de conception ;
* les guides de déploiement ;
* les ressources graphiques ;
* les décisions transversales.

Il constitue la source de vérité de l'écosystème.

---

## Ohanna Agent

Moteur d'observation.

Il supervise les capacités, collecte les observations, orchestre les plugins et expose les informations produites par le runtime.

Il ne possède aucune responsabilité de présentation.

---

## Ohanna Vision

Interface de visualisation et d'administration.

Il transforme les informations produites par Ohanna Agent en représentations graphiques adaptées aux utilisateurs.

Il ne participe pas à la production des observations.

---

## Ohanna House

Déploiement de référence de la plateforme.

Il permet de valider les choix architecturaux dans une infrastructure réelle.

Il sert également de référence pour les guides d'installation et les scénarios de démonstration.

---

# Principes

Cette architecture respecte plusieurs principes fondamentaux.

## Séparation des responsabilités

Chaque produit possède un domaine fonctionnel clairement identifié.

Aucune responsabilité n'est partagée entre plusieurs produits.

---

## Faible couplage

Les produits restent indépendants.

Ils ne connaissent que les interfaces publiques nécessaires à leur fonctionnement.

---

## Forte cohésion

Chaque produit rassemble des fonctionnalités ayant un objectif commun.

Les composants internes restent spécialisés.

---

## Évolution indépendante

Chaque produit peut évoluer selon son propre rythme.

Une évolution locale ne doit pas imposer une modification des autres composants lorsque les interfaces publiques restent compatibles.

---

## Documentation distribuée

Chaque produit documente son propre fonctionnement.

Ohanna Platform documente uniquement les éléments transversaux à l'ensemble de l'écosystème.

---

# Alternatives étudiées

## Application monolithique

Une architecture monolithique aurait simplifié le démarrage du projet.

En revanche, elle aurait progressivement augmenté le couplage entre les différentes responsabilités.

Cette approche a été écartée.

---

## Bibliothèque unique

La création d'une bibliothèque unique regroupant l'ensemble des fonctionnalités a également été étudiée.

Cette solution aurait limité l'indépendance des différents produits et rendu leur évolution plus complexe.

Elle n'a pas été retenue.

---

## Écosystème de produits spécialisés

Cette approche permet :

* une séparation claire des responsabilités ;
* une meilleure maintenabilité ;
* une évolution indépendante des composants ;
* une documentation spécialisée ;
* une architecture plus lisible.

Cette solution a été retenue.

---

# Conséquences

Cette décision implique que :

* chaque produit possède son propre dépôt ;
* chaque produit est versionné indépendamment ;
* les interfaces publiques deviennent les contrats entre les composants ;
* les dépendances directes restent limitées ;
* la documentation est répartie entre les différents projets ;
* les évolutions sont plus simples à maîtriser.

Elle favorise également la réutilisation de composants dans des contextes différents.

---

# Évolutions futures

L'architecture retenue permet l'ajout de nouveaux produits sans remettre en cause l'organisation générale de la plateforme.

De futurs composants pourront être intégrés, tels que :

* une interface d'administration dédiée ;
* des services cloud ;
* des applications mobiles ;
* des outils d'analyse avancée ;
* des extensions spécialisées.

Chaque nouveau produit devra respecter les principes définis par cette décision d'architecture.

---

# Décisions associées

* ADR-0000 — Architecture Decision Records
* ADR-0002 — Organisation des produits
* ADR-0003 — Design System
