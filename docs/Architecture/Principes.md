# Principes architecturaux de la plateforme Ohana

## 1. Introduction

La plateforme Ohana repose sur un ensemble de principes d'architecture qui guident la conception, le développement et l'évolution de l'ensemble de l'écosystème.

Ces principes constituent un cadre de décision commun à tous les projets de la plateforme.

Ils garantissent la cohérence de l'architecture, la simplicité des composants et la pérennité des interfaces.

Toute évolution importante de la plateforme doit respecter ces principes ou faire l'objet d'une Architecture Decision Record (ADR).

---

# 2. Principes fondamentaux

## Capability First

La capacité est l'unité fonctionnelle fondamentale de la plateforme.

Une infrastructure est décrite par les capacités qu'elle fournit plutôt que par les technologies qu'elle utilise.

Chaque capacité possède une responsabilité clairement définie et produit des observations exploitables par les autres composants de la plateforme.

---

## Observable by Design

Tout comportement significatif doit être observable.

Aucun état critique ne doit rester implicite ou inaccessible.

Les observations constituent la source de vérité de la plateforme.

Les décisions sont prises à partir des observations et non d'états internes invisibles.

---

## Declarative Configuration

Le comportement d'un composant est décrit par sa configuration.

Les fichiers de configuration expriment l'intention plutôt que l'implémentation.

Une modification de comportement doit pouvoir être réalisée sans modifier le code lorsque cela est raisonnablement possible.

---

## Event Driven

Les composants communiquent principalement au travers d'événements.

Les événements représentent les changements d'état observables du système.

Cette approche favorise le découplage entre les différents composants.

---

## Plugin First

Les fonctionnalités spécifiques sont implémentées sous forme de plugins.

Le runtime ne dépend jamais d'une implémentation particulière.

Les plugins peuvent être ajoutés, remplacés ou supprimés sans modifier le cœur de la plateforme.

---

## API First

Toute information produite par la plateforme doit pouvoir être exposée par une interface stable.

Les API constituent le contrat officiel entre les composants.

Les interfaces publiques doivent rester cohérentes et versionnées.

---

## Documentation First

La documentation fait partie intégrante du projet.

Toute fonctionnalité importante doit être documentée.

La documentation évolue en même temps que le logiciel.

---

## Test First

Chaque comportement observable doit être couvert par des tests automatisés.

Les tests constituent une garantie de stabilité de la plateforme.

---

# 3. Principes d'architecture

## Responsabilité unique

Chaque composant possède une responsabilité clairement définie.

Une fonctionnalité ne doit exister qu'à un seul endroit.

---

## Faible couplage

Les composants ne doivent connaître que les interfaces nécessaires à leur fonctionnement.

Les dépendances directes sont limitées au strict nécessaire.

---

## Forte cohésion

Les responsabilités proches sont regroupées.

Les composants restent spécialisés.

---

## Séparation des responsabilités

Le domaine métier reste indépendant :

* des interfaces utilisateur ;
* des protocoles réseau ;
* des mécanismes de persistance ;
* des frameworks utilisés.

---

## Composition avant héritage

La composition est privilégiée lorsque plusieurs solutions sont possibles.

Elle favorise la modularité et les tests.

---

## Immutabilité

Les modèles représentant une observation, un événement ou une période d'état sont immuables lorsque cela est pertinent.

L'immutabilité facilite le raisonnement, les tests et la traçabilité.

---

# 4. Principes du runtime

Le runtime constitue le cœur de la plateforme.

Son fonctionnement respecte plusieurs invariants.

Le runtime orchestre les traitements mais ne réalise pas les implémentations spécifiques.

Les plugins restent indépendants les uns des autres.

Les composants internes communiquent au travers d'interfaces explicites.

Les observations ne sont jamais modifiées après leur publication.

Les traitements sont déterministes autant que possible.

---

# 5. Principes des API

Les API constituent les contrats publics de la plateforme.

Les principes suivants s'appliquent.

Les modèles sont stables.

Les ruptures de compatibilité sont exceptionnelles.

Les API sont versionnées lorsque cela devient nécessaire.

Les erreurs suivent un format cohérent.

Les opérations sont documentées.

Les interfaces temps réel utilisent WebSocket lorsque cela apporte une valeur fonctionnelle.

---

# 6. Principes des interfaces utilisateur

Les interfaces privilégient la compréhension de l'infrastructure.

La représentation graphique doit toujours refléter l'état réel de la plateforme.

Les tableaux de bord mettent en avant :

* la santé globale ;
* les alertes ;
* les chronologies ;
* les capacités ;
* la topologie.

Les interactions doivent rester simples, cohérentes et accessibles.

Le temps réel ne doit jamais compromettre la lisibilité.

---

# 7. Principes de documentation

La documentation est considérée comme un composant de la plateforme.

Les documents sont rédigés en Markdown.

Les décisions importantes sont documentées dans des ADR.

Les diagrammes officiels sont réalisés au format SVG.

Les concepts métier sont définis dans le glossaire de référence.

Les guides décrivent les procédures.

Les documents d'architecture expliquent les choix de conception.

Chaque document possède une responsabilité clairement définie.

---

# 8. Principes d'évolution

La plateforme est conçue pour évoluer progressivement.

Les nouvelles fonctionnalités doivent privilégier l'extension de l'architecture existante plutôt que sa remise en cause.

Les interfaces publiques doivent rester compatibles autant que possible.

Les composants doivent pouvoir évoluer indépendamment.

Les décisions d'architecture importantes sont conservées dans les ADR afin de préserver l'historique du projet.

La simplicité reste un objectif permanent de la plateforme.

---

# 9. Conclusion

Les principes définis dans ce document constituent le socle architectural commun à l'ensemble de l'écosystème Ohana.

Ils assurent la cohérence entre les différents produits, facilitent leur évolution et garantissent une architecture stable, modulaire et durable.

Toute évolution majeure de la plateforme doit être évaluée à la lumière de ces principes avant d'être adoptée.
