# Installer Ohanna Platform

Ce guide décrit l'installation complète d'une plateforme **Ohanna** en environnement de développement.

À l'issue de cette procédure, vous disposerez des composants suivants :

* Ohanna-Agent
* Ohanna-Vision

---

# Prérequis

Les versions suivantes sont recommandées.

| Logiciel           | Version recommandée     |
| ------------------ | ----------------------- |
| Git                | 2.45+                   |
| Python             | 3.13+                   |
| pip                | Dernière version        |
| Navigateur moderne | Chrome, Edge ou Firefox |

Vérifier les versions installées :

```bash
git --version

python --version

pip --version
```

---

# Étape 1 — Récupérer les projets

Créer un répertoire de travail :

```bash
mkdir Ohanna
cd Ohanna
```

Cloner les dépôts :

```bash
git clone https://github.com/<organisation>/Ohanna-Agent.git

git clone https://github.com/<organisation>/Ohanna-Vision.git
```

Vérifier :

```bash
dir
```

Le dossier doit contenir :

```text
Ohanna-Agent
Ohanna-Vision
```

---

# Étape 2 — Installer Ohanna-Agent

Accéder au dépôt :

```bash
cd Ohanna-Agent
```

Créer un environnement virtuel :

```bash
python -m venv .venv
```

Activer l'environnement :

### Windows

```powershell
.venv\Scripts\activate
```

### Linux

```bash
source .venv/bin/activate
```

Installer les dépendances :

```bash
pip install --upgrade pip

pip install -e .
```

Vérifier :

```bash
ohanna-agent --help
```

Quitter le projet :

```bash
cd ..
```

---

# Étape 3 — Installer Ohanna-Vision

Accéder au dépôt :

```bash
cd Ohanna-Vision
```

Créer un environnement virtuel :

```bash
python -m venv .venv
```

Activer l'environnement :

### Windows

```powershell
.venv\Scripts\activate
```

### Linux

```bash
source .venv/bin/activate
```

Installer les dépendances :

```bash
pip install --upgrade pip

pip install -e .
```

Vérifier :

```bash
ohanna-vision --help
```

Quitter le projet :

```bash
cd ..
```

---

# Étape 4 — Démarrer Ohanna-Agent

Depuis le répertoire **Ohanna-Agent** :

```bash
ohanna-agent \
    --config config/application.yaml \
    --infrastructure config/infrastructure.yaml
```

Le journal doit indiquer que l'agent est démarré.

---

# Étape 5 — Démarrer Ohanna-Vision

Depuis le répertoire **Ohanna-Vision** :

```bash
ohanna-vision \
    --config config/vision.yaml
```

Le serveur démarre par défaut sur :

```text
http://127.0.0.1:8000
```

---

# Étape 6 — Vérifier le fonctionnement

Ouvrir l'interface :

```text
http://127.0.0.1:8000/ui/
```

Contrôler que :

* l'application est accessible ;
* les informations de runtime sont affichées ;
* les observations remontent correctement lorsque l'agent en publie.

---

# Mise à jour

Pour mettre à jour les composants :

```bash
git pull
```

Puis réinstaller le projet :

```bash
pip install -e .
```

Effectuer cette opération dans chacun des dépôts.

---

# Dépannage

## La commande `ohanna-agent` est introuvable

Vérifier que l'environnement virtuel est activé.

Réinstaller ensuite le projet :

```bash
pip install -e .
```

---

## La commande `ohanna-vision` est introuvable

Vérifier que l'environnement virtuel est activé.

Réinstaller ensuite le projet :

```bash
pip install -e .
```

---

## L'interface web n'est pas accessible

Vérifier que **Ohanna-Vision** est démarré et qu'aucune autre application n'utilise le port configuré.

---

## Aller plus loin

Les guides suivants complètent cette procédure :

* Installer-Ohanna-Agent.md
* Installer-Ohanna-Vision.md
* Guide de déploiement
* Guide de développement
* Guide de contribution
