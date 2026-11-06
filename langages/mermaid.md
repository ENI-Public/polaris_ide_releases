# Mermaid — les diagrammes écrits en texte

Un schéma — étapes d'un processus, échanges entre un navigateur et un serveur, classes d'un
programme, planning… — peut s'écrire en texte avec la syntaxe **Mermaid**, au lieu d'être
dessiné dans un autre logiciel puis collé en image. Il est dessiné à la publication, aux
couleurs de l'école, **dans les slides et dans les PDF**. L'aperçu de Polaris le dessine de la
même façon pendant que vous écrivez.

[← Tous les langages](README.md)

---

## L'écrire

Le template **Diagramme Mermaid** (menu **Templates ENI**, ou tapez `eni-mermaid`) pose la
forme attendue :

```
.Chaîne de valeur des Jardins de Garance
[mermaid, target=chaine-de-valeur, alt="Chaîne de valeur en trois étapes : production, préparation des paniers, vente."]
----
flowchart LR
  P[Production] --> C[Préparation des paniers] --> V[Vente]
----
```

| Élément | Rôle |
|---|---|
| `.Chaîne de valeur…` | le titre, affiché sous le diagramme (« Figure N. ») — facultatif |
| `mermaid` | demande le **dessin** du diagramme |
| `target=chaine-de-valeur` | un **nom propre à ce diagramme** dans le cours : lettres, chiffres et tirets |
| `alt="…"` | le **texte alternatif** : ce que le diagramme apprend à qui ne le voit pas |
| entre les `----` | le diagramme, en syntaxe Mermaid |

## Dessiner ou montrer le code : deux écritures

| Vous écrivez | Résultat |
|---|---|
| `[mermaid, target=…, alt="…"]` | le **diagramme dessiné** |
| `[source,mermaid]` | le **code Mermaid affiché** tel quel, jamais dessiné |

La seconde sert quand le code **est** le contenu : un TP où les apprenants doivent saisir le
diagramme, un cours sur Mermaid lui-même. Polaris la signale en jaune, au cas où vous auriez
voulu le dessin, et vous donne l'autre écriture.

## Les règles — sans elles, le cours n'est pas publié

> **Un diagramme fautif bloque la publication de tout le cours**, slides et PDF compris. La
> dernière version publiée reste en ligne, et rien de cassé n'arrive aux apprenants. C'est
> volontaire : un support où un message d'erreur remplace le schéma ne doit jamais partir.

| Règle | Ce que fait Polaris |
|---|---|
| **`alt="…"` obligatoire**, et non vide | ligne soulignée **en rouge** |
| **`target` unique** dans le cours | ligne soulignée **en rouge**, avec la ligne du premier diagramme de ce nom |
| **pas de rendu `inline`** (`%inline`, `opts=inline`) | ligne soulignée **en rouge** |
| **syntaxe Mermaid correcte** | le diagramme est remplacé dans l'aperçu par un **encadré rouge** qui cite l'erreur |
| **un libellé mis en forme en entier, ou pas du tout** | encadré rouge dans l'aperçu |

Sur le dernier point : un seul mot en gras dans une étiquette (`` "`**Gras** et normal`" ``)
ferait se superposer les mots dans les PDF. Mettez tout le libellé en gras, ou rien.

## Le texte alternatif

- Il est **lu par les lecteurs d'écran** sur les slides. Écrivez ce que le schéma *apprend*,
  pas « schéma » ou « diagramme » : « Le navigateur envoie la requête au serveur, qui
  interroge la base puis renvoie la page. »
- **Les PDF n'ont pas de texte alternatif**, pour aucune image. Si le diagramme porte beaucoup
  d'information, **décrivez-le aussi dans un paragraphe ou une liste juste à côté** : c'est la
  seule description qui atteint les PDF.
- Pas de case « image décorative » ici : un schéma de cours porte toujours une information.

## Les types de diagrammes

Tous les types de Mermaid 11 sont dessinés. Ceux-ci ont été vérifiés dans les slides **et**
dans les PDF :

| Type | Commence par | Pour |
|---|---|---|
| Organigramme | `flowchart LR` (ou `TD`) | un processus, un algorithme, un enchaînement |
| Séquence | `sequenceDiagram` | des échanges entre acteurs dans le temps |
| Classes | `classDiagram` | un modèle objet |
| États | `stateDiagram-v2` | les états d'un objet et ses transitions |
| Entité-association | `erDiagram` | un modèle de données |
| Carte mentale | `mindmap` | une arborescence d'idées |
| Camembert | `pie` | une répartition |
| Gantt | `gantt` | un planning |
| Frise | `timeline` | une chronologie |
| Branches Git | `gitGraph` | un historique de branches |
| Parcours utilisateur | `journey` | les étapes vécues par un utilisateur |
| Graphique | `xychart` | des courbes ou des barres |
| Flux | `sankey` | des volumes qui se répartissent |
| Blocs | `block` | une architecture en blocs |
| Architecture | `architecture-beta` | des services et leurs liaisons |
| Exigences | `requirementDiagram` | des exigences et leurs liens |
| Kanban | `kanban` | un tableau de tâches |
| Quadrant | `quadrantChart` | un positionnement sur deux axes |
| Radar | `radar-beta` | une comparaison sur plusieurs critères |
| C4 | `C4Context` | une architecture logicielle (modèle C4) |
| Paquet | `packet` | la structure d'une trame réseau |

La syntaxe de chaque type est décrite dans la
[documentation de Mermaid](https://mermaid.js.org/intro/syntax-reference.html) (en anglais).

> **Moins lisibles sur papier** : le quadrant (titre et axes en partie rognés), le radar
> (courbes très pâles), C4 et paquet (petits caractères). Ils sont dessinés, mais préférez un
> autre type quand c'est possible.

## Conseils

- **Les accents sont permis**, dans les libellés comme dans les titres.
- **Évitez les flèches, symboles et émojis dans les libellés** : un caractère absent de la
  police des diagrammes peut déborder de sa case. Pour une flèche, utilisez celles de Mermaid
  (`-->`), pas un caractère `→`.
- **Ne choisissez ni thème ni couleurs** : la publication applique ceux de l'école, et l'aperçu
  de Polaris aussi.
- **Gantt** : la ligne rouge « aujourd'hui » serait celle du jour de la publication, pas du
  cours. Ajoutez `todayMarker off` dans le diagramme pour la retirer.
- **Un diagramme par bloc**, et un bloc par diagramme : deux diagrammes demandent deux
  `target` différents.
- **Pas de diagramme dans un bloc de code** : un `[mermaid, …]` écrit entre deux `----`
  est du texte, il n'est ni dessiné ni contrôlé.
