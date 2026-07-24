# Exploitation de la plateforme

## Mise à jour

Ohana-Installer découvre la dernière release stable d'Ohana-Platform et compare
les versions installées au manifeste :

```bash
sudo ohana update
```

Un composant déjà à la version cible est conservé sans téléchargement, arrêt ni
réinstallation. Ohana-Installer lui-même se met à jour séparément.

## Administration

Ouvrir `http://ADRESSE_DU_SERVEUR:8000`, puis **Configuration**.

- utiliser **Baux DHCP** pour le serveur dnsmasq ;
- utiliser **Architecture > Déplacer** pour organiser la grille ;
- utiliser **Architecture > Relier** pour créer les connexions ;
- cliquer sur un équipement pour gérer ses services ;
- cliquer sur une ligne pour éditer la liaison.

Les modifications ne deviennent persistantes qu'après confirmation de
l'application. Les journaux utiles sont :

```bash
sudo journalctl -u ohana-agent.service -n 100 --no-pager
sudo journalctl -u ohana-vision.service -n 100 --no-pager
```
