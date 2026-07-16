# Roadmap

## Vision

Ohanna-Platform constitue le point d’entrée officiel de l’écosystème Ohanna.

Le dépôt rassemble la documentation globale, les procédures de déploiement, les outils d’orchestration et les exemples permettant d’installer et d’exploiter Ohanna-Agent et Ohanna-Vision comme une plateforme cohérente.

---

## Phase 0 — Fondation du dépôt

* [x] Création du dépôt Ohanna-Platform.
* [x] Définition de son périmètre.
* [x] Création de l’arborescence documentaire.
* [x] Ajout du README.
* [x] Ajout du CHANGELOG.
* [x] Ajout de la roadmap.
* [ ] Ajout de la licence.
* [ ] Premier audit du dépôt.

---

## Phase 1 — Documentation de la plateforme

* [ ] Finaliser `docs/Architecture.md`.
* [ ] Finaliser `docs/Installer-Ohanna-Platform.md`.
* [ ] Rédiger `docs/Operations.md`.
* [ ] Rédiger `docs/Troubleshooting.md`.
* [ ] Ajouter une matrice de compatibilité Agent/Vision.
* [ ] Documenter les ports et flux réseau.
* [ ] Documenter les stratégies de sauvegarde et de restauration.

---

## Phase 2 — Déploiement reproductible

* [ ] Ajouter des scripts d’installation Linux.
* [ ] Ajouter des scripts d’installation Windows.
* [ ] Ajouter les unités `systemd`.
* [ ] Ajouter les modèles de services Windows.
* [ ] Ajouter les fichiers de configuration d’exemple.
* [ ] Ajouter les vérifications post-installation.
* [ ] Ajouter une procédure de désinstallation.

---

## Phase 3 — Orchestration

* [ ] Étudier Docker Compose.
* [ ] Séparer les volumes de configuration et de données.
* [ ] Ajouter les contrôles de santé.
* [ ] Ajouter la gestion des secrets.
* [ ] Ajouter un reverse proxy optionnel.
* [ ] Ajouter le support HTTPS.
* [ ] Préparer les procédures de mise à jour et de rollback.

---

## Phase 4 — Exploitation

* [ ] Ajouter une procédure de sauvegarde automatisée.
* [ ] Ajouter une procédure de restauration complète.
* [ ] Ajouter la rotation des journaux.
* [ ] Ajouter la supervision d’Ohanna par Ohanna.
* [ ] Ajouter les diagnostics automatisés.
* [ ] Documenter la maintenance préventive.

---

## Phase 5 — Distribution de la plateforme

* [ ] Publier des releases cohérentes de la plateforme.
* [ ] Associer les versions compatibles d’Ohanna-Agent et d’Ohanna-Vision.
* [ ] Fournir des sommes de contrôle.
* [ ] Fournir des archives de déploiement.
* [ ] Ajouter un manifeste de plateforme.
* [ ] Étudier un installateur unifié.

---

## Évolutions futures

* authentification ;
* gestion multi-utilisateur ;
* stockage persistant ;
* notifications ;
* gestion des incidents ;
* administration de l’infrastructure ;
* haute disponibilité ;
* déploiements distribués ;
* catalogue de plugins ;
* SDK Ohanna.
