# Architecture de déploiement de la plateforme Ohanna

## 1. Introduction

La plateforme Ohanna est conçue pour être déployée de manière modulaire.

Chaque composant possède une responsabilité clairement définie et peut évoluer indépendamment des autres.

L'architecture de déploiement privilégie la simplicité, la résilience et l'observabilité.

Ce document décrit les principes d'organisation des composants de la plateforme.

Les procédures d'installation sont documentées dans les guides de déploiement.

---

# 2. Objectifs

L'architecture de déploiement poursuit plusieurs objectifs.

* Simplifier l'installation de la plateforme.
* Permettre une évolution progressive.
* Favoriser la modularité.
* Réduire les dépendances entre composants.
* Faciliter la maintenance.
* Autoriser différents scénarios de déploiement.

---

# 3. Les composants

La plateforme est composée de plusieurs produits indépendants.

## Ohanna Platform

Référentiel documentaire.

Il ne participe pas à l'exécution de la plateforme.

---

## Ohanna Agent

Moteur d'observation.

Il supervise les capacités, collecte les observations et expose les informations nécessaires aux autres composants.

---

## Ohanna Vision

Interface utilisateur.

Elle consomme les données produites par l'agent afin d'offrir une représentation graphique de l'infrastructure.

---

## Infrastructure supervisée

L'infrastructure représente l'ensemble des équipements, services et ressources observés par la plateforme.

Elle reste indépendante des composants Ohanna.

---

# 4. Architecture logique

La plateforme est organisée selon plusieurs couches.

* Infrastructure
* Plugins
* Runtime
* Interfaces
* Visualisation
* Utilisateurs

Chaque couche dépend uniquement des services fournis par la couche inférieure.

Cette organisation favorise le découplage des composants.

---

# 5. Scénarios de déploiement

La plateforme peut être déployée selon différents scénarios.

## Déploiement minimal

Le déploiement minimal comprend :

* un Ohanna Agent ;
* une infrastructure supervisée.

Ce scénario permet de produire des observations sans interface graphique.

---

## Déploiement standard

Le déploiement standard comprend :

* un Ohanna Agent ;
* un Ohanna Vision ;
* une infrastructure supervisée.

Il constitue le scénario recommandé.

---

## Déploiement de référence

Le déploiement de référence correspond au projet Ohanna House.

Il rassemble :

* Ohanna Agent ;
* Ohanna Vision ;
* l'infrastructure réelle ;
* les configurations de référence.

Ce déploiement sert de validation permanente de la plateforme.

---

## Déploiement étendu

L'architecture permet d'ajouter :

* plusieurs agents ;
* plusieurs infrastructures ;
* plusieurs interfaces ;
* des composants complémentaires.

Ces évolutions ne remettent pas en cause les principes fondamentaux de la plateforme.

---

# 6. Communication entre composants

Les composants communiquent uniquement au travers d'interfaces clairement définies.

Les observations sont publiées par Ohanna Agent.

Les interfaces exposent les informations nécessaires aux autres produits.

Ohanna Vision consomme ces informations sans intervenir dans leur production.

Cette séparation garantit l'indépendance des composants.

---

# 7. Configuration

Chaque composant possède sa propre configuration.

Les configurations sont déclaratives.

Les composants ne modifient jamais directement la configuration des autres produits.

La plateforme privilégie les formats ouverts et lisibles.

---

# 8. Résilience

L'architecture favorise la continuité de fonctionnement.

Une défaillance d'un composant ne doit pas entraîner l'arrêt de l'ensemble de la plateforme.

Les responsabilités étant clairement séparées, chaque produit peut être redémarré, remplacé ou mis à jour indépendamment.

---

# 9. Évolutivité

L'architecture de déploiement est conçue pour accompagner la croissance de la plateforme.

De nouveaux produits peuvent être ajoutés.

Les composants existants peuvent évoluer indépendamment.

Les interfaces publiques assurent la compatibilité entre les différentes versions.

Cette approche permet une évolution progressive sans remise en cause de l'architecture.

---

# 10. Sécurité

Les composants de la plateforme communiquent exclusivement au travers d'interfaces prévues à cet effet.

Chaque produit reste responsable de ses propres mécanismes d'authentification, d'autorisation et de protection des données.

La plateforme privilégie la réduction de la surface d'exposition et la séparation des responsabilités.

Les aspects de sécurité spécifiques à chaque composant sont documentés dans leurs projets respectifs.

---

# 11. Bonnes pratiques de déploiement

Les recommandations suivantes s'appliquent à tous les déploiements de la plateforme.

* Déployer chaque produit indépendamment.
* Conserver des configurations déclaratives.
* Versionner les fichiers de configuration.
* Superviser les composants de la plateforme.
* Sauvegarder les configurations.
* Documenter les personnalisations locales.
* Tester les mises à jour avant leur mise en production.

Ces pratiques contribuent à la stabilité et à la maintenabilité de la plateforme.

---

# 12. Évolutions futures

L'architecture de déploiement permet d'intégrer progressivement de nouveaux scénarios.

Parmi les évolutions envisagées :

* supervision distribuée ;
* infrastructures multi-sites ;
* haute disponibilité ;
* orchestration par conteneurs ;
* services cloud ;
* administration centralisée.

Ces évolutions s'inscrivent dans les principes architecturaux définis par la plateforme.

---

# 13. Conclusion

L'architecture de déploiement d'Ohanna repose sur une séparation claire des responsabilités entre les différents produits.

Cette organisation garantit une plateforme modulaire, extensible et adaptée à des contextes de déploiement variés.

Les guides de déploiement décrivent les procédures d'installation et de configuration correspondant à cette architecture.
