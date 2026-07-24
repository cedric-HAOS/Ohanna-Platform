# Roadmap

## Vision

Ohana-Platform constitue le point d’entrée officiel de l’écosystème Ohana.

Le dépôt rassemble la documentation globale, les procédures de déploiement, les outils d’orchestration et les exemples permettant d’installer et d’exploiter Ohana-Agent et Ohana-Vision comme une plateforme cohérente.

---

## Phase 0 — Fondation du dépôt

* [x] Création du dépôt Ohana-Platform.
* [x] Définition de son périmètre.
* [x] Création de l’arborescence documentaire.
* [x] Ajout du README.
* [x] Ajout du CHANGELOG.
* [x] Ajout de la roadmap.
* [x] Ajout de la licence.
* [x] Premier audit transversal de l'écosystème.

---

## Phase 1 — Documentation de la plateforme

* [x] Finaliser la documentation d'architecture.
* [x] Finaliser `docs/Installer-Ohana-Platform.md`.
* [x] Rédiger `docs/Operations.md`.
* [ ] Rédiger `docs/Troubleshooting.md`.
* [x] Ajouter une matrice de compatibilité Agent/Vision.
* [ ] Documenter les ports et flux réseau.
* [ ] Documenter les stratégies de sauvegarde et de restauration.

---

## Phase 2 — Déploiement reproductible

* [x] Ajouter l'installation Linux via Ohana-Installer.
* [ ] Ajouter des scripts d’installation Windows.
* [x] Générer les unités `systemd` via Ohana-Installer.
* [ ] Ajouter les modèles de services Windows.
* [x] Distribuer les fichiers de configuration d’exemple dans les releases.
* [x] Ajouter les vérifications post-installation dans Ohana-Installer.
* [x] Ajouter la désinstallation dans Ohana-Installer.

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
* [ ] Ajouter la supervision d’Ohana par Ohana.
* [ ] Ajouter les diagnostics automatisés.
* [ ] Documenter la maintenance préventive.

---

## Phase 5 — Distribution de la plateforme

* [x] Publier des releases cohérentes de la plateforme.
* [x] Associer les versions compatibles d’Ohana-Agent et d’Ohana-Vision.
* [x] Fournir des sommes de contrôle pour les releases des composants.
* [ ] Fournir des archives de déploiement.
* [x] Ajouter un manifeste de plateforme.
* [x] Fournir un installateur unifié avec Ohana-Installer.

---

## Évolutions futures

* authentification ;
* gestion multi-utilisateur ;
* stockage persistant ;
* notifications ;
* gestion des incidents ;
* haute disponibilité ;
* déploiements distribués ;
* catalogue de plugins ;
* SDK Ohana.
