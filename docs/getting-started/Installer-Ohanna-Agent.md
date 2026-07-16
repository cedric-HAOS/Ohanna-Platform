# Installer Ohanna-Agent

Ce guide décrit l'installation d'**Ohanna-Agent** en environnement de développement.

À l'issue de cette procédure, vous disposerez d'un agent fonctionnel capable d'exécuter des capacités, de produire des observations et de les publier vers Ohanna-Vision.

---

# Prérequis

Les versions suivantes sont recommandées.

| Logiciel | Version recommandée |
| -------- | ------------------- |
| Git      | 2.45+               |
| Python   | 3.13+               |
| pip      | Dernière version    |

Vérifier les versions installées :

```bash
git --version

python --version

pip --version
```

---

# Étape 1 — Cloner le dépôt

```bash
git clone https://github.com/<organisation>/Ohanna-Agent.git

cd Ohanna-Agent
```

Vérifier le contenu du dépôt :

```bash
dir
```

Vous devez notamment retrouver :

```text
config/
plugins/
src/
tests/
pyproject.toml
README.md
```

---

# Étape 2 — Créer un environnement virtuel

Créer l'environnement Python :

```bash
python -m venv .venv
```

Activation sous Windows :

```powershell
.venv\Scripts\activate
```

Activation sous Linux :

```bash
source .venv/bin/activate
```

Vérifier :

```bash
python --version

pip --version
```

---

# Étape 3 — Installer les dépendances

Mettre pip à jour :

```bash
pip install --upgrade pip
```

Installer Ohanna-Agent :

```bash
pip install -e .
```

Vérifier que l'installation est correcte :

```bash
ohanna-agent --help
```

La commande doit afficher les options disponibles.

---

# Étape 4 — Vérifier l'installation

Exécuter les contrôles qualité.

Analyse statique :

```bash
python -m ruff check
```

Tests unitaires :

```bash
python -m pytest
```

Tous les tests doivent réussir.

---

# Étape 5 — Démarrer Ohanna-Agent

Lancer l'agent avec la configuration fournie :

```bash
ohanna-agent \
    --config config/application.yaml \
    --infrastructure config/infrastructure.yaml
```

Selon les plugins utilisés, des paramètres supplémentaires peuvent être nécessaires, par exemple :

```bash
ohanna-agent \
    --config config/application.yaml \
    --infrastructure config/infrastructure.yaml \
    --dns-config config/plugins/dns.yaml
```

Au démarrage, le journal doit confirmer le chargement de la configuration et l'initialisation des plugins.

---

# Vérification

L'agent doit démarrer sans erreur.

Arrêter l'exécution avec :

```text
CTRL+C
```

---

# Mise à jour

Depuis le répertoire du projet :

```bash
git pull
```

Puis réinstaller la version courante :

```bash
pip install -e .
```

---

# Désinstallation

Désactiver l'environnement virtuel :

```bash
deactivate
```

Supprimer ensuite le répertoire du projet.

---

# Dépannage

## La commande `ohanna-agent` est introuvable

Vérifier que l'environnement virtuel est activé.

Réinstaller le projet :

```bash
pip install -e .
```

---

## Les dépendances ne s'installent pas

Mettre pip à jour :

```bash
pip install --upgrade pip
```

Puis relancer :

```bash
pip install -e .
```

---

## Les tests échouent

Vérifier que vous utilisez une version de Python compatible et que toutes les dépendances ont été installées correctement.

---

## Étape suivante

Une fois l'installation terminée, vous pouvez installer **Ohanna-Vision** afin de visualiser les observations produites par l'agent.
