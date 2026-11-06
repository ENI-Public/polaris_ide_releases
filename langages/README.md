# Les langages dans un cours ENI

Ce dossier rassemble, **un document par langage**, ce qu'il faut savoir pour écrire du code,
du pseudo-code ou des diagrammes dans un cours. Le
[guide du formateur](../guide-formateur.md) explique l'outil ; ces pages expliquent
**ce que vous écrivez** et ce que deviendra votre bloc dans les slides et dans les PDF.

| Document | Pour quoi faire |
|---|---|
| [Pseudo-code ENI](pseudo-code.md) | écrire les algorithmes des cours d'algorithmique, colorés aux couleurs de l'école |
| [Mermaid](mermaid.md) | dessiner un diagramme (processus, séquence, classes, Gantt…) en l'écrivant en texte |

Les langages de programmation ordinaires (Python, Java, Bash…) n'ont pas de page à eux : ils
s'écrivent tous de la même façon, décrite ci-dessous.

---

## Écrire un bloc de code

```
[source,python]
----
def moyenne(notes):
    return sum(notes) / len(notes)
----
```

- `[source,<langage>]` sur la ligne du dessus, puis le code entre deux lignes `----`.
- Le template **`eni-code`** (menu **Templates ENI**) pose le bloc pour vous ; tapez
  `Ctrl+Espace` après `[source,` pour choisir le langage dans la liste.
- Le code est affiché **tel quel** : rien n'y est interprété comme de l'AsciiDoc.
- Pour une sortie de console, une arborescence ou un journal, sans coloration, préférez le
  **texte littéral** (template `eni-literal`) : le texte entre deux lignes `....`.

> **Refermez toujours le bloc.** Un `----` oublié fait disparaître tout ce qui suit du
> support publié, parfois des modules entiers. Polaris le signale en rouge.

## Les langages colorés

La coloration des slides est assurée par **highlight.js**, qui ne charge que les langages
déclarés dans la configuration du cours. Ceux du gabarit actuel sont :

| Famille | Langages |
|---|---|
| Scripts et systèmes | `bash`, `powershell`, `dockerfile`, `apache`, `vim` |
| Développement | `python`, `javascript`, `typescript`, `java`, `csharp`, `c`, `cpp`, `kotlin`, `dart`, `php`, `matlab` |
| Web | `html`, `css`, `scss`, `twig`, `django` |
| Données et requêtes | `sql`, `tsql`, `json`, `yaml`, `xml`, `graphql`, `excel` |
| Infrastructure | `hcl`, `terraform`, `gradle` |
| Tests | `gherkin`, `robot` |
| Documents | `markdown`, `asciidoc`, `latex`, `plaintext` |
| Propres à l'école | `pseudo` → [Pseudo-code ENI](pseudo-code.md) |

**Écrivez le nom tel qu'il figure dans ce tableau.** Les abréviations courantes ne sont pas
chargées : Polaris les signale en jaune et vous donne le bon nom.

| Vous avez écrit | Écrivez |
|---|---|
| `js` | `javascript` |
| `ts` | `typescript` |
| `py` | `python` |
| `sh`, `shell`, `zsh` | `bash` |
| `ps1`, `psl` | `powershell` |
| `yml` | `yaml` |
| `docker` | `dockerfile` |
| `cs`, `c#` | `csharp` |
| `c++` | `cpp` |
| `md` | `markdown` |
| `tex` | `latex` |

Un langage absent de la liste est signalé **en jaune** : le bloc sera publié, mais **sans
coloration**. Si un langage vous manque, demandez-le à l'ingénierie pédagogique : il s'ajoute à
la configuration du gabarit.

> **`latex` est le dernier arrivé.** Un cours créé avant son ajout garde l'ancienne
> configuration, qui ne le charge pas : le bloc y sortirait sans coloration. En cas de doute,
> demandez à l'ingénierie pédagogique de mettre la configuration de votre cours à jour.

## Deux cas à part

- **Le pseudo-code** n'est pas un langage de highlight.js : c'est une grammaire de l'école,
  ajoutée par la publication. Il s'écrit `[source,pseudo]` et ne doit **jamais** être ajouté à
  la configuration du cours. → [Pseudo-code ENI](pseudo-code.md)
- **Mermaid** a deux écritures qui ne font pas la même chose : `[mermaid, …]` **dessine** le
  diagramme, `[source,mermaid]` **affiche son code**. → [Mermaid](mermaid.md)
