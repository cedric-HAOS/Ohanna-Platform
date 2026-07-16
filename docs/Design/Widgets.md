# Widgets.md

# Ohanna — Dashboard Widgets

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Les widgets sont les composants métier de haut niveau des interfaces Ohanna.

Ils transforment les données de la plateforme en informations immédiatement compréhensibles.

Chaque widget doit répondre à une question précise.

Exemples :

* L'infrastructure est-elle saine ?
* Quelles capacités sont dégradées ?
* Depuis combien de temps un service est-il indisponible ?
* Quels équipements dépendent d'un nœud critique ?
* Quelles observations viennent d'être reçues ?

Un widget ne doit jamais mélanger plusieurs objectifs sans relation directe.

---

# 2. Principes généraux

Tous les widgets doivent être :

* lisibles ;
* autonomes ;
* accessibles ;
* réutilisables ;
* responsives ;
* cohérents avec le Design System ;
* capables d'afficher leurs états de chargement, d'absence de données et d'erreur.

---

# 3. Structure commune

Un widget suit généralement la structure suivante :

```text
Widget

├── Header
│   ├── Title
│   ├── Description
│   └── Actions
├── Content
├── Legend
└── Footer
```

Tous les éléments ne sont pas obligatoires.

---

# 4. Header

Le Header peut contenir :

* titre ;
* description courte ;
* période affichée ;
* filtre actif ;
* bouton d'actualisation ;
* menu contextuel.

Les actions secondaires sont regroupées dans un menu lorsque leur nombre dépasse trois.

---

# 5. États communs

Chaque widget doit prendre en charge :

* Loading
* Ready
* Empty
* Partial
* Stale
* Error
* Disabled

---

# 6. État Loading

Le contenu utilise un Skeleton lorsque la structure finale est connue.

Le Spinner est réservé :

* aux actions courtes ;
* aux rafraîchissements ponctuels ;
* aux zones compactes.

---

# 7. État Empty

L'état vide indique clairement :

* pourquoi aucune donnée n'est disponible ;
* si la situation est normale ;
* quelle action peut être réalisée.

Exemple :

```text
Aucune observation reçue pour cette période.
```

---

# 8. État Partial

Le widget signale qu'une partie seulement des données est disponible.

Il ne doit pas présenter un résultat incomplet comme une vérité définitive.

---

# 9. État Stale

Une donnée est considérée comme périmée lorsqu'elle n'a pas été actualisée dans le délai attendu.

Le widget affiche :

* l'heure de la dernière mise à jour ;
* un indicateur visuel ;
* une explication accessible.

---

# 10. État Error

L'erreur doit rester locale au widget.

Elle indique :

* la source du problème si elle est connue ;
* la conséquence ;
* l'action possible.

---

# 11. KPI Card

## Objectif

Présenter une seule métrique synthétique.

## Structure

* valeur ;
* libellé ;
* unité ;
* tendance facultative ;
* contexte facultatif.

## Exemples

* 98,7 % de disponibilité ;
* 4 alertes actives ;
* 12 services observés ;
* 18 ms de latence médiane.

## Règles

* une seule métrique principale ;
* pas de graphique complexe ;
* comparaison clairement datée ;
* valeur lisible en quelques secondes.

---

# 12. Health Summary

## Objectif

Présenter la santé globale de l'infrastructure.

## Données

* état global ;
* nombre de capacités Healthy ;
* nombre de capacités Warning ;
* nombre de capacités Critical ;
* nombre de capacités Unknown.

## Règles

La santé globale ne doit jamais être calculée dans le frontend.

Le widget affiche la projection fournie par le Health Engine.

---

# 13. Health Ring

## Objectif

Afficher une répartition synthétique des états.

## Utilisation

* infrastructure ;
* nœud ;
* service ;
* groupe de capacités.

## Règles

* nombre limité de segments ;
* légende obligatoire ;
* couleur toujours accompagnée d'un libellé ;
* aucune représentation 3D.

---

# 14. Availability Gauge

## Objectif

Afficher un taux de disponibilité.

## Données

* valeur ;
* période ;
* objectif éventuel ;
* écart éventuel.

## Règles

Une jauge ne doit pas être utilisée lorsqu'une valeur numérique simple est plus lisible.

---

# 15. Infrastructure Map

## Objectif

Présenter les principaux équipements et leur santé.

## Contenu

* nœuds ;
* types d'équipement ;
* état ;
* regroupements éventuels ;
* sélection.

## Règles

La carte d'infrastructure privilégie la compréhension métier à la précision géographique.

---

# 16. Topology View

## Objectif

Présenter les dépendances et connexions.

## Fonctionnalités

* zoom ;
* déplacement ;
* recentrage ;
* sélection ;
* détails ;
* filtrage ;
* mise en évidence des dépendances.

## Règles

Les liens principaux utilisent l'accent turquoise.

Les relations secondaires utilisent un gris bleuté.

---

# 17. Timeline

## Objectif

Afficher l'évolution des états dans le temps.

## Données

* périodes d'état ;
* début ;
* fin ;
* durée ;
* état ;
* contexte.

## Règles

La Timeline repose exclusivement sur les périodes métier calculées par le Timeline Engine.

Elle ne doit pas reconstruire les périodes à partir des seules observations dans l'interface.

---

# 18. State Period Inspector

## Objectif

Présenter le détail d'une période sélectionnée.

## Données

* état ;
* date de début ;
* date de fin ;
* durée ;
* origine ;
* observations associées ;
* éventuel changement précédent.

---

# 19. Recent Observations

## Objectif

Afficher les dernières observations reçues.

## Colonnes possibles

* heure ;
* capacité ;
* service ;
* nœud ;
* état ;
* latence ;
* source.

## Règles

La liste reste courte.

Une page dédiée gère l'historique complet.

---

# 20. Observation Stream

## Objectif

Afficher les observations en temps réel.

## Règles

* ordre chronologique inverse ;
* ajout visuel discret ;
* limite de rétention dans le navigateur ;
* possibilité de pause ;
* aucun défilement forcé lorsque l'utilisateur consulte une entrée ancienne.

---

# 21. Incident Feed

## Objectif

Présenter les incidents ou anomalies actives.

## Données

* niveau ;
* titre ;
* ressource ;
* début ;
* durée ;
* statut ;
* action possible.

## Règles

Les incidents Critical apparaissent en premier.

Le tri reste explicite.

---

# 22. Event Stream

## Objectif

Présenter les événements internes de la plateforme.

## Exemples

* plugin démarré ;
* observation reçue ;
* état modifié ;
* configuration appliquée ;
* action administrative exécutée.

## Règles

Les événements techniques détaillés peuvent être filtrés.

---

# 23. Capability Matrix

## Objectif

Présenter les relations entre capacités, services et nœuds.

## Représentation

* lignes : capacités ;
* colonnes : services ou nœuds ;
* cellules : état, présence ou niveau de prise en charge.

## Règles

La matrice doit rester navigable au clavier et lisible sans dépendre uniquement de la couleur.

---

# 24. Service Health

## Objectif

Présenter l'état détaillé d'un service.

## Données

* état global ;
* capacités ;
* dernières observations ;
* dépendances ;
* timeline ;
* disponibilité.

---

# 25. Node Health

## Objectif

Présenter l'état détaillé d'un équipement ou nœud.

## Données

* identité ;
* type ;
* état ;
* services hébergés ;
* capacités ;
* dépendances ;
* activité récente.

---

# 26. Dependency Graph

## Objectif

Présenter les dépendances entre éléments.

## Fonctions

* exploration ;
* filtrage ;
* sélection ;
* chemin critique ;
* dépendances entrantes ;
* dépendances sortantes.

## Règles

Le graphe doit éviter la surcharge visuelle.

Les niveaux de détail peuvent être progressifs.

---

# 27. Latency Chart

## Objectif

Afficher l'évolution des temps de réponse.

## Données

* valeur ;
* période ;
* minimum ;
* maximum ;
* médiane ;
* seuil éventuel.

## Règles

L'unité doit toujours être visible.

Les valeurs aberrantes ne doivent pas être masquées.

---

# 28. Availability Chart

## Objectif

Afficher l'évolution de la disponibilité.

## Règles

La période et la méthode de calcul doivent être explicitement indiquées.

---

# 29. Health History

## Objectif

Afficher les changements de santé sur une période.

Ce widget complète la Timeline avec une vue agrégée.

---

# 30. Scheduler Activity

## Objectif

Afficher l'activité du Scheduler.

## Données

* tâches planifiées ;
* tâches exécutées ;
* succès ;
* échecs ;
* prochaine exécution ;
* durée.

---

# 31. Plugin Activity

## Objectif

Afficher l'état et l'activité des plugins.

## Données

* nom ;
* version ;
* état ;
* dernière exécution ;
* nombre d'observations ;
* erreurs éventuelles.

---

# 32. MQTT Activity

## Objectif

Afficher l'activité MQTT.

## Données

* messages reçus ;
* messages publiés ;
* connexions ;
* erreurs ;
* débit ;
* topics principaux.

---

# 33. DNS Resolution History

## Objectif

Afficher l'historique des résolutions DNS.

## Données

* nom ;
* serveur ;
* résultat ;
* latence ;
* code de réponse ;
* heure.

---

# 34. Configuration Status

## Objectif

Présenter l'état de la configuration déclarative.

## Données

* version active ;
* dernière application ;
* validation ;
* erreurs ;
* écarts ;
* source.

---

# 35. Administration Activity

## Objectif

Afficher les opérations administratives récentes.

## Données

* opération ;
* cible ;
* initiateur ;
* résultat ;
* date ;
* durée.

---

# 36. Dimensions

Les widgets utilisent des tailles cohérentes.

## Petit

* KPI ;
* badge synthétique ;
* compteur.

## Moyen

* liste courte ;
* petit graphique ;
* résumé de santé.

## Grand

* Timeline ;
* Topology ;
* matrice ;
* graphe ;
* tableau détaillé.

---

# 37. Responsive

Sur Desktop :

* plusieurs widgets peuvent partager une ligne.

Sur Tablet :

* les widgets moyens occupent généralement une demi-largeur ou une largeur complète.

Sur Mobile :

* chaque widget occupe une seule colonne ;
* les tableaux peuvent devenir des listes ;
* les contrôles secondaires sont regroupés.

---

# 38. Actualisation

Chaque widget doit indiquer clairement :

* s'il est temps réel ;
* sa dernière mise à jour ;
* sa période de référence ;
* son éventuelle fréquence de rafraîchissement.

Les rafraîchissements ne doivent pas provoquer de saut de layout.

---

# 39. Interactions

Les interactions doivent être prévisibles.

Exemples :

* sélectionner un nœud ouvre ses détails ;
* sélectionner une période ouvre son inspecteur ;
* cliquer sur une KPI applique un filtre lorsqu'une destination claire existe ;
* survoler une valeur affiche un Tooltip complémentaire.

---

# 40. Accessibilité

Chaque widget doit :

* posséder un titre accessible ;
* être navigable au clavier si interactif ;
* proposer une alternative textuelle aux graphiques ;
* afficher les unités ;
* ne pas dépendre uniquement de la couleur ;
* conserver un ordre de lecture logique.

---

# 41. Performance

Un widget ne doit pas :

* charger un historique illimité ;
* conserver toutes les observations en mémoire ;
* recalculer les projections métier ;
* rafraîchir inutilement l'ensemble de la page ;
* redessiner un graphique sans changement de données.

---

# 42. Composition recommandée du Dashboard

```text
Dashboard

├── Health Summary
├── KPI Cards
├── Active Incidents
├── Infrastructure Map
├── Topology View
├── Timeline
├── Recent Observations
└── Event Stream
```

Cette composition peut évoluer selon le produit, mais l'ordre de priorité reste :

1. état global ;
2. anomalies ;
3. infrastructure ;
4. évolution temporelle ;
5. activité récente.

---

# 43. Bonnes pratiques

* Faire répondre chaque widget à une question précise.
* Afficher les informations les plus importantes en premier.
* Garder les actions secondaires discrètes.
* Réutiliser les mêmes widgets dans toutes les vues comparables.
* Indiquer systématiquement la période et l'unité.
* Préserver la stabilité visuelle lors des mises à jour temps réel.

---

# 44. Pratiques interdites

Il est interdit :

* de créer deux widgets différents pour le même besoin ;
* de mélanger plusieurs métriques sans hiérarchie ;
* de recalculer la logique métier dans le frontend ;
* d'utiliser des graphiques 3D ;
* d'afficher une couleur sans texte ou icône associée ;
* de masquer l'absence ou l'incomplétude des données ;
* de transformer chaque donnée en graphique ;
* de surcharger le Dashboard avec toutes les informations disponibles.

---

# 45. Principe fondamental

Un widget Ohanna doit réduire le temps nécessaire pour comprendre l'état de l'infrastructure.

S'il ajoute de la complexité sans améliorer la compréhension, il ne doit pas être intégré.
