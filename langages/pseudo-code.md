# Pseudo-code ENI

Le pseudo-code des cours d'algorithmique a sa propre coloration, aux couleurs de l'école,
identique dans l'aperçu de Polaris, dans les slides et dans les PDF.

[← Tous les langages](README.md)

---

## L'écrire

```
[source,pseudo]
----
ALGORITHME Moyenne
VARIABLES
  Variable total : réel
  Variable i : entier
DEBUT
  total <- 0
  POUR i DE 1 A 10 FAIRE
    total <- total + i
  FINPOUR
  ECRIRE("Moyenne : ", total / 10)
FIN
----
```

- `[source,pseudo]` sur la ligne du dessus, puis le pseudo-code entre deux lignes `----`.
- `pseudocode` et `pseudo-code` sont acceptés aussi ; `pseudo` est celui que Polaris propose.
- **Rien à configurer dans le cours.** La coloration est ajoutée par la publication.
  ⚠️ N'ajoutez **jamais** `pseudo` à la liste des langages de la configuration du cours : le
  support publié chercherait en ligne un fichier qui n'existe pas.

## Ce qui est reconnu

| Catégorie | Mots | Rendu |
|---|---|---|
| Structure | `ALGORITHME` `ALGO` `DEBUT` `DÉBUT` `FIN` `Procédure` `Fonction` `RETOURNE` | gras |
| Boucles | `POUR` `FINPOUR` `FPour` `DE` `A` `à` `PAS` `par` `FAIRE` `TANTQUE` `FINTANTQUE` `FTQ` `REPETER` `Répéter` `FRépéter` `JUSQUA` | gras |
| Conditions | `SI` `ALORS` `SINON` `FINSI` `FSI` `SELON` `CAS` `autre` `FINSELON` `FSelon` | gras |
| Déclarations | `VARIABLES` `Variable` `Constante` | |
| Types | `ENTIER` `REEL` `réel` `CHAINE` `texte` `CARACTERE` `caractère` `BOOLEEN` `booléen` `TABLEAU` | |
| Valeurs | `VRAI` `FAUX` `NUL` | |
| Entrées / sorties | `LIRE` `lire` `ECRIRE` `écrire` `écrireSRC` `saisir` | |
| Opérateurs en lettres | `et` `ou` `non` `div` `mod` `x` | |
| Opérateurs symboliques | `<-` `:=` `<=` `>=` `<>` `!=` `≠` `≤` `≥` `<` `>` `=` `+` `-` `*` `/` `%` `&` `|` `!` `(` `)` | |
| Nombres | `12`, `3.14`, `3,14` | |
| Chaînes | `"…"` et `'…'` | |
| Commentaires | `// …` et `# …`, jusqu'à la fin de la ligne | |

Chaque catégorie a sa couleur. Le gras des structures, boucles et conditions les distingue
aussi sans la couleur.

### Les règles

- **Majuscules ou minuscules, peu importe** : `POUR`, `Pour` et `pour` sont le même mot.
- **Les accents font partie des mots** : `écrire` est reconnu en entier, et le `A`
  d'`Aéroport` n'est pas pris pour un mot-clé.
- **Les opérateurs en lettres ne sont reconnus que comme mots entiers** : le `x` de `index`
  ou de `maximum` n'est pas coloré.

### Deux pièges de la notation

Ils viennent du pseudo-code lui-même, pas de l'outil :

1. **`x` est l'opérateur de multiplication.** Une variable nommée `x`, seule, sera colorée
   comme un opérateur. Préférez `abscisse`, `x1`, `valeur`…
2. **`A` et `à` sont des mots de boucle** (`POUR i DE 1 A 10`). Une variable nommée `a` ou
   `A` sera colorée comme tel. Préférez un nom plus parlant.

## Les couleurs, à l'écran et sur papier

- **À l'écran** — aperçu de Polaris et slides —, le bloc a un **fond sombre**, le même que les
  autres langages des slides. Toutes les couleurs y sont lisibles (contraste d'au moins 4,5:1).
- **Dans les PDF**, le fond est blanc : la palette est adaptée au papier, avec la **même teinte
  par catégorie**. Un mot-clé bleu-vert à l'écran reste bleu-vert sur papier, en plus foncé.

Les couleurs sont fixées par l'école : vous n'avez rien à choisir.

## Ce que Polaris vérifie

- Un bloc `[source,…]` dont le langage n'est pas connu est signalé **en jaune** : il serait
  publié sans coloration. `[source,algo]` ou `[source,pseudocode-eni]`, par exemple, ne sont
  pas reconnus.
- Un bloc jamais refermé est signalé **en rouge**, comme pour tout bloc de code.
