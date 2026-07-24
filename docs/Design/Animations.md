# Animations.md

# Ohana — Motion and Animation System

Version : 1.0
Statut : Référence officielle

---

# 1. Philosophie

Les animations d'Ohana améliorent la compréhension de l'interface.

Elles servent à :

* confirmer une action ;
* rendre une transition plus naturelle ;
* montrer un changement d'état ;
* guider l'attention ;
* préserver le contexte visuel.

Une animation ne doit jamais être ajoutée uniquement pour décorer l'interface.

Le mouvement reste discret, rapide et prévisible.

---

# 2. Principes généraux

Toute animation doit être :

* utile ;
* courte ;
* fluide ;
* cohérente ;
* non bloquante ;
* accessible.

L'utilisateur ne doit jamais attendre la fin d'une animation pour continuer à utiliser l'interface.

---

# 3. Durées officielles

| Variable            |  Durée | Usage                              |
| ------------------- | -----: | ---------------------------------- |
| `--motion-instant`  |  80 ms | retour visuel immédiat             |
| `--motion-fast`     | 150 ms | hover, focus, bouton               |
| `--motion-standard` | 200 ms | changement d'état                  |
| `--motion-enter`    | 250 ms | apparition                         |
| `--motion-panel`    | 300 ms | drawer, panneau, modal             |
| `--motion-slow`     | 400 ms | transition complexe exceptionnelle |

Les animations supérieures à 400 ms sont interdites dans l'interface standard.

---

# 4. Courbes d'accélération

## Standard

Utilisée pour la majorité des transitions.

```css
cubic-bezier(0.2, 0, 0, 1)
```

Variable :

```css
--ease-standard: cubic-bezier(0.2, 0, 0, 1);
```

---

## Entrée

Utilisée lorsqu'un élément apparaît.

```css
cubic-bezier(0, 0, 0.2, 1)
```

Variable :

```css
--ease-enter: cubic-bezier(0, 0, 0.2, 1);
```

---

## Sortie

Utilisée lorsqu'un élément disparaît.

```css
cubic-bezier(0.4, 0, 1, 1)
```

Variable :

```css
--ease-exit: cubic-bezier(0.4, 0, 1, 1);
```

---

# 5. Propriétés animables

Les propriétés recommandées sont :

* `opacity`
* `transform`
* `background-color`
* `border-color`
* `box-shadow`

Les propriétés provoquant des recalculs importants de mise en page doivent être évitées.

---

# 6. Hover

Les états Hover utilisent une transition de :

```text
150 ms
```

Propriétés recommandées :

* fond ;
* bordure ;
* couleur du texte ;
* légère translation éventuelle.

La translation maximale autorisée est :

```text
2 px
```

Les effets de zoom sont interdits sur les composants standards.

---

# 7. Focus

Le Focus doit apparaître immédiatement.

Durée recommandée :

```text
80 à 150 ms
```

L'indicateur de Focus ne doit jamais être masqué ou retardé.

---

# 8. Boutons

Les boutons utilisent :

* Hover : 150 ms ;
* Active : 80 ms ;
* Loading : transition immédiate ;
* Disabled : 150 ms.

Un bouton pressé peut utiliser :

```css
transform: translateY(1px);
```

Aucun effet de rebond n'est autorisé.

---

# 9. Cartes

Une carte interactive peut utiliser :

* variation de bordure ;
* légère élévation ;
* translation verticale maximale de 2 px.

Durée :

```text
150 à 200 ms
```

Les cartes non interactives ne doivent pas être animées au survol.

---

# 10. Sidebar

L'ouverture ou la réduction de la Sidebar utilise :

```text
300 ms
```

Propriétés :

* largeur ;
* translation ;
* opacité des libellés.

La navigation doit rester utilisable pendant la transition.

---

# 11. Drawers et panneaux latéraux

Durée :

```text
300 ms
```

Animation recommandée :

* translation horizontale ;
* apparition progressive de l'overlay.

Le contenu du panneau ne doit pas entrer avec un délai artificiel.

---

# 12. Dialogues et modales

Durée d'apparition :

```text
250 ms
```

Durée de disparition :

```text
200 ms
```

Animation recommandée :

* opacité ;
* légère translation verticale ;
* variation d'échelle très limitée.

Échelle minimale autorisée :

```text
0.98
```

Les effets de zoom importants sont interdits.

---

# 13. Toasts

Durée d'apparition :

```text
200 ms
```

Durée de disparition :

```text
150 ms
```

Animation recommandée :

* translation courte ;
* opacité.

Les Toasts ne doivent pas empiler des animations complexes.

---

# 14. Tooltips

Durée d'apparition :

```text
150 ms
```

Délai recommandé avant affichage :

```text
300 à 500 ms
```

Les Tooltips liés à des actions critiques peuvent apparaître sans délai.

---

# 15. Tabs

Le changement d'onglet utilise :

* transition de l'indicateur actif ;
* fondu court du contenu si nécessaire.

Durée :

```text
150 à 200 ms
```

Le contenu ne doit jamais glisser sur une grande distance.

---

# 16. Accordéons

L'ouverture et la fermeture utilisent :

```text
200 à 250 ms
```

L'animation doit préserver la position de lecture de l'utilisateur.

---

# 17. États de chargement

## Spinner

Le Spinner utilise une rotation régulière.

Durée d'un cycle :

```text
800 à 1 000 ms
```

---

## Skeleton

Le Skeleton utilise une animation discrète.

Durée recommandée :

```text
1 200 à 1 600 ms
```

Les contrastes doivent rester faibles afin de ne pas détourner l'attention.

---

# 18. Mises à jour temps réel

Les changements liés aux nouvelles observations doivent rester discrets.

Les composants peuvent utiliser :

* variation temporaire de bordure ;
* fondu ;
* courte mise en évidence du fond.

Durée maximale :

```text
600 ms
```

Aucun clignotement continu n'est autorisé.

---

# 19. Santé et alertes

Un changement de santé peut être signalé par :

* un fondu de couleur ;
* une apparition d'icône ;
* une courte pulsation unique.

Les animations répétées en boucle sont interdites, sauf pour signaler une urgence active explicitement reconnue.

Même dans ce cas, la pulsation doit rester lente et modérée.

---

# 20. Timeline

Les périodes d'état peuvent apparaître progressivement lors du chargement.

Les transitions de sélection peuvent utiliser :

* accentuation de bordure ;
* variation d'opacité ;
* mise en avant du segment sélectionné.

La longueur et la position des périodes ne doivent pas être animées lors des mises à jour fréquentes si cela nuit à la lecture.

---

# 21. Topologie

Les transitions suivantes sont autorisées :

* zoom ;
* déplacement ;
* sélection d'un nœud ;
* recentrage ;
* apparition d'un détail.

Le déplacement de la caméra doit rester fluide et court.

Durée recommandée :

```text
250 à 400 ms
```

Les nœuds ne doivent pas rebondir ou flotter.

---

# 22. Graphiques

Les graphiques peuvent animer leur première apparition.

Les mises à jour temps réel doivent privilégier la stabilité.

Durée recommandée :

```text
300 à 400 ms
```

Les axes, légendes et libellés doivent rester lisibles pendant la transition.

---

# 23. Réduction des animations

Ohana respecte la préférence système :

```css
@media (prefers-reduced-motion: reduce)
```

Lorsque cette préférence est active :

* les translations sont supprimées ;
* les durées sont fortement réduites ;
* les animations décoratives sont désactivées ;
* les chargements restent compréhensibles ;
* les changements d'état restent visibles sans mouvement important.

---

# 24. Variables CSS officielles

```css
:root {
    --motion-instant: 80ms;
    --motion-fast: 150ms;
    --motion-standard: 200ms;
    --motion-enter: 250ms;
    --motion-panel: 300ms;
    --motion-slow: 400ms;

    --ease-standard: cubic-bezier(0.2, 0, 0, 1);
    --ease-enter: cubic-bezier(0, 0, 0.2, 1);
    --ease-exit: cubic-bezier(0.4, 0, 1, 1);
}
```

---

# 25. Bonnes pratiques

* Animer uniquement les changements utiles.
* Maintenir des durées cohérentes entre composants similaires.
* Préserver la stabilité des données en temps réel.
* Favoriser `opacity` et `transform`.
* Tester chaque animation avec la réduction des mouvements activée.
* Garder les transitions plus rapides pour les petites actions et plus longues pour les grands panneaux.

---

# 26. Pratiques interdites

Il est interdit :

* d'utiliser des animations longues ou spectaculaires ;
* d'ajouter des rebonds ;
* d'utiliser des effets élastiques ;
* de faire clignoter continuellement une information ;
* d'animer plusieurs directions simultanément ;
* de bloquer une action pendant une transition ;
* d'utiliser le mouvement pour masquer un temps de chargement anormalement long ;
* d'introduire une animation non documentée dans le Design System.

---

# 27. Principe fondamental

Le mouvement doit aider l'utilisateur à comprendre ce qui vient de se produire.

Une bonne animation est presque imperceptible.

Elle rend l'interface plus naturelle sans attirer l'attention sur elle-même.
