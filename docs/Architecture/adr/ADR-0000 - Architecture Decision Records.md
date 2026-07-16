# ADR-0000 — Architecture Decision Records

* **Statut** : Accepté
* **Date** : 2026-07-16

---

# Contexte

La plateforme Ohanna est composée de plusieurs produits développés et maintenus de manière indépendante.

Son architecture évoluera progressivement afin d'intégrer de nouvelles capacités, de nouveaux composants et de nouveaux scénarios de déploiement.

Afin de garantir la cohérence de cette évolution, les décisions d'architecture doivent être documentées, justifiées et conservées.

Les Architecture Decision Records (ADR) constituent le mécanisme retenu pour répondre à cet objectif.

---

# Décision

La plateforme adopte le format **Architecture Decision Record (ADR)** pour documenter les décisions structurantes.

Un ADR décrit :

* le contexte ayant conduit à la décision ;
* la décision retenue ;
* les conséquences de cette décision.

Les ADR constituent la référence officielle des choix d'architecture de la plateforme.

---

# Portée

Les ADR présents dans **Ohanna-Platform** concernent exclusivement les décisions ayant un impact sur l'ensemble de l'écosystème.

Ils couvrent notamment :

* l'architecture globale ;
* les principes de conception ;
* l'organisation des produits ;
* les conventions communes ;
* les interfaces transversales ;
* les choix structurants de la plateforme.

Les décisions propres à un produit restent documentées dans le dépôt correspondant.

Par exemple :

* les décisions relatives au runtime d'Ohanna Agent sont documentées dans **Ohanna-Agent** ;
* les décisions relatives à l'interface et aux moteurs de visualisation sont documentées dans **Ohanna-Vision** ;
* les décisions propres à une infrastructure restent documentées dans **Ohanna-House**.

---

# Cycle de vie

Chaque ADR possède un statut.

Les statuts utilisés par la plateforme sont :

* **Proposé**
* **Accepté**
* **Remplacé**
* **Obsolète**

Lorsqu'une décision est remplacée, l'ADR d'origine est conservé afin de préserver l'historique architectural.

Le nouvel ADR référence explicitement la décision précédente.

Les ADR ne sont jamais supprimés.

---

# Numérotation

Les ADR sont numérotés séquentiellement.

Exemple :

* ADR-0000
* ADR-0001
* ADR-0002
* ADR-0003

La numérotation ne reflète ni l'importance ni la chronologie des évolutions fonctionnelles.

Elle identifie uniquement les décisions d'architecture.

---

# Format

Tous les ADR de la plateforme utilisent la structure suivante :

* Statut
* Date
* Contexte
* Décision
* Conséquences

Des sections complémentaires peuvent être ajoutées lorsque cela apporte une meilleure compréhension de la décision.

---

# Principes

Un ADR doit répondre à une décision architecturale importante.

Il ne documente pas :

* une correction de bug ;
* un détail d'implémentation ;
* une préférence de style de code ;
* une évolution mineure.

Un ADR explique **pourquoi** une décision a été prise, et non **comment** elle est implémentée.

---

# Conséquences

L'adoption des Architecture Decision Records apporte plusieurs bénéfices :

* conservation de l'historique des décisions ;
* justification des choix d'architecture ;
* meilleure compréhension de la plateforme ;
* cohérence entre les différents produits ;
* facilité d'intégration de nouveaux contributeurs.

Les ADR constituent ainsi la mémoire architecturale officielle de l'écosystème Ohanna.

---

# ADR associés

Les premières décisions documentées dans Ohanna Platform sont les suivantes :

* **ADR-0000** — Architecture Decision Records
* **ADR-0001** — Architecture de la plateforme
* **ADR-0002** — Organisation des produits
* **ADR-0003** — Design System

De nouveaux ADR seront ajoutés à mesure que la plateforme évoluera.
