# Composants tiers inclus dans Polaris IDE

Polaris IDE est propriétaire (voir [LICENCE](LICENCE)), mais il est bâti sur des
composants open source. Ils restent soumis à leur propre licence, que la licence de
Polaris ne restreint pas. Leur texte complet est disponible à l'adresse indiquée.

## Interface et rendu

| Composant | Licence | Source |
|---|---|---|
| Asciidoctor.js | MIT | https://github.com/asciidoctor/asciidoctor.js |
| CodeMirror 6 | MIT | https://codemirror.net |
| highlight.js | BSD-3-Clause | https://github.com/highlightjs/highlight.js |
| Mermaid | MIT | https://github.com/mermaid-js/mermaid |
| Dépendances de Mermaid : D3 (ISC), dagre-d3-es, Cytoscape.js, KaTeX, marked, Rough.js (MIT), DOMPurify | MIT, ISC ; DOMPurify : MPL-2.0 ou Apache-2.0 | https://github.com/mermaid-js/mermaid/blob/develop/packages/mermaid/package.json |
| React, React DOM | MIT | https://github.com/facebook/react |
| Zustand | MIT | https://github.com/pmndrs/zustand |
| nspell | MIT | https://github.com/wooorm/nspell |

## Dictionnaires du correcteur orthographique

| Composant | Licence | Source |
|---|---|---|
| Dictionnaire français Grammalecte (Olivier R. et contributeurs), via `dictionary-fr` | MPL-2.0 | https://grammalecte.net — https://github.com/wooorm/dictionaries/tree/main/dictionaries/fr |
| Dictionnaire anglais SCOWL / Hunspell en_US, via `dictionary-en` | MIT et BSD | http://wordlist.sourceforge.net — https://github.com/wooorm/dictionaries/tree/main/dictionaries/en |

Les fichiers du dictionnaire français sont inclus **sans modification**. Leur forme
source, sous licence MPL-2.0, est disponible aux adresses ci-dessus.

## Application et Git

| Composant | Licence | Source |
|---|---|---|
| Tauri et ses plugins officiels (fs, dialog, updater, process, opener, log) | MIT ou Apache-2.0 | https://github.com/tauri-apps/tauri |
| libgit2, via `git2` | GPLv2 avec exception de liaison | https://github.com/libgit2/libgit2 |
| OpenSSL (version macOS uniquement) | Apache-2.0 | https://www.openssl.org |
| reqwest, rustls, tokio, serde, flate2, tar, sha2, log | MIT ou Apache-2.0 | https://crates.io |

## Non inclus

Le serveur **GitHub Copilot** n'est pas inclus dans les installateurs. Il est téléchargé
depuis GitHub quand vous activez l'assistance à la rédaction, et il est soumis aux
conditions d'utilisation de GitHub.
