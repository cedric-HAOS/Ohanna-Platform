# Installer et mettre à jour Ohana-Platform

La composition 1.0.3 installe Ohana-Agent 1.2.0 et Ohana-Vision 1.2.0.
Ohana-Installer 1.0.1 est recommandé afin de préparer automatiquement le canal
d'administration local et de ne pas réinstaller un composant déjà à jour.

## Mise à jour d'une installation existante

Mettre d'abord à jour Ohana-Installer depuis sa release officielle, puis lancer :

```bash
sudo ohana update
```

L'installateur découvre Ohana-Platform 1.0.3, vérifie les sommes SHA-256,
compare les versions et demande confirmation.

## Vérification

```bash
ohana --version
/opt/ohana-agent/venv/bin/ohana-agent --version
/opt/ohana-vision/venv/bin/ohana-vision --version
sudo systemctl is-active ohana-agent.service ohana-vision.service
```

Les versions attendues sont respectivement 1.0.1, 1.2.0 et 1.2.0.
