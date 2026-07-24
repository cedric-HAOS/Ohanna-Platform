# ADR-0003 — Design System

* **Statut** : Accepté
* **Date** : 2026-07-16

---

# Contexte

La plateforme Ohana est composée de plusieurs produits développés indépendamment.

Ces produits partagent une architecture commune, des modèles métier communs et une philosophie de conception identique.

Afin de garantir une expérience cohérente pour les utilisateurs, il est nécessaire d'adopter un Design System commun à l'ensemble de la plateforme.

Cette décision définit le rôle du Design System dans l'écosystème Ohana.

---

# Décision

L'ensemble des produits Ohana utilise un Design System unique.

Ce Design System constitue la référence officielle pour l'identité visuelle, les conventions graphiques et les composants d'interface.

Les produits conservent leur autonomie fonctionnelle mais partagent une même identité graphique.

---

# Objectifs

Le Design System poursuit plusieurs objectifs.

* Assurer une identité visuelle cohérente.
* Offrir une expérience utilisateur homogène.
* Réduire les divergences entre les interfaces.
* Faciliter le développement des nouveaux produits.
* Renforcer l'identité de la plateforme.

---

# Périmètre

Le Design System couvre notamment :

* le logo officiel ;
* les variantes du logo ;
* la palette de couleurs ;
* la typographie ;
* l'iconographie ;
* les espacements ;
* les composants graphiques ;
* les conventions d'interface ;
* les diagrammes officiels.

Les éléments graphiques sont centralisés dans Ohana Platform.

---

# Responsabilités

## Ohana Platform

Ohana Platform maintient le Design System.

Il publie :

* la charte graphique ;
* les ressources officielles ;
* les composants visuels communs ;
* les modèles graphiques ;
* les conventions d'utilisation.

---

## Produits

Chaque produit applique le Design System.

Les produits peuvent adapter leurs interfaces à leurs besoins fonctionnels sans remettre en cause l'identité visuelle commune.

---

# Principes

## Une identité unique

La plateforme possède une seule identité graphique.

Les produits ne disposent pas de logos indépendants.

Ils utilisent le logo officiel de la plateforme.

---

## Cohérence

Les composants graphiques doivent présenter un comportement identique d'un produit à l'autre.

Les utilisateurs retrouvent les mêmes conventions visuelles dans l'ensemble de la plateforme.

---

## Simplicité

Le Design System privilégie des interfaces sobres et lisibles.

Les éléments décoratifs sont limités.

Les informations importantes sont mises en avant.

---

## Accessibilité

Les interfaces doivent rester lisibles dans différents contextes d'utilisation.

Le contraste, la hiérarchie visuelle et les tailles de caractères sont pris en compte dès la conception.

---

## Réutilisation

Les composants graphiques sont conçus pour être réutilisés dans plusieurs produits.

Les duplications sont évitées.

---

## Évolutivité

Le Design System peut évoluer progressivement.

Les évolutions doivent préserver la cohérence de l'ensemble de la plateforme.

---

# Ressources

Les ressources officielles comprennent notamment :

* les logos ;
* les icônes ;
* les couleurs ;
* les typographies ;
* les composants graphiques ;
* les captures d'écran de référence ;
* les diagrammes SVG officiels.

Ces ressources sont versionnées avec la plateforme.

---

# Documentation

Le Design System est documenté dans les documents suivants :

* Charte graphique
* Logos
* Couleurs
* Typographie
* Icônes
* UI Kit

Ces documents constituent la référence officielle pour l'ensemble des interfaces de la plateforme.

---

# Alternatives étudiées

## Design indépendant par produit

Chaque produit aurait pu définir sa propre identité visuelle.

Cette approche aurait entraîné une fragmentation de l'expérience utilisateur et une perte de cohérence.

Elle n'a pas été retenue.

---

## Design spécifique à chaque interface

Une personnalisation importante des interfaces a également été envisagée.

Cette solution aurait compliqué la maintenance et réduit la réutilisation des composants.

Elle a été écartée.

---

## Design System partagé

L'adoption d'un Design System unique offre une identité forte à la plateforme tout en permettant à chaque produit de conserver sa spécialisation fonctionnelle.

Cette approche a été retenue.

---

# Conséquences

Cette décision implique :

* une identité graphique unique ;
* un logo commun ;
* une palette de couleurs partagée ;
* des composants graphiques réutilisables ;
* une documentation graphique centralisée ;
* des diagrammes homogènes ;
* une expérience utilisateur cohérente.

Le Design System devient un élément constitutif de l'architecture de la plateforme.

---

# Évolutions futures

Le Design System pourra évoluer afin d'intégrer de nouveaux supports et de nouveaux produits.

Parmi les évolutions envisagées :

* applications mobiles ;
* interfaces tactiles ;
* thèmes d'affichage ;
* bibliothèques de composants ;
* modèles de présentation ;
* ressources pour la communication.

Ces évolutions devront préserver l'identité visuelle de la plateforme.

---

# Décisions associées

* ADR-0000 — Architecture Decision Records
* ADR-0001 — Architecture de la plateforme
* ADR-0002 — Organisation des produits
