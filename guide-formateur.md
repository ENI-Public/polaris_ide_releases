# Polaris IDE — guide du formateur

Ce guide suit l'ordre dans lequel vous allez rencontrer les choses : récupérer un cours,
l'écrire, vérifier, publier. Vous n'avez pas besoin de le lire en entier avant de commencer —
les deux premières sections suffisent pour travailler.

> **Vous n'avez pas besoin de connaître Git.** Polaris parle de « ton travail », de
> « télécharger un cours » et de « publier ». Les mots de Git sont là, dans les infobulles,
> pour la personne qui viendra vous dépanner.

**Sommaire**

1. [Récupérer un cours](#1-récupérer-un-cours)
2. [Écrire son cours](#2-écrire-son-cours)
3. [Voir ce que verront les apprenants](#3-voir-ce-que-verront-les-apprenants)
4. [Ce que Polaris vérifie pour vous](#4-ce-que-polaris-vérifie-pour-vous)
5. [Publier son travail](#5-publier-son-travail)
6. [Régler son confort de lecture](#6-régler-son-confort-de-lecture)
7. [Se faire aider par Copilot](#7-se-faire-aider-par-copilot)
8. [Quand ça coince](#8-quand-ça-coince)
9. [Ce que Polaris ne sait pas encore faire](#9-ce-que-polaris-ne-sait-pas-encore-faire)

---

## 1. Récupérer un cours

Un cours ENI vit sur GitHub. On vous a donné un lien vers sa page. Vous n'avez rien à
installer de plus, ni de ligne de commande à taper.

1. Dans le bandeau du haut, cliquez sur **⬇ Télécharger un cours…**
2. Collez le lien qu'on vous a donné.
3. Cliquez sur **Choisir…** pour indiquer où ranger le cours sur votre poste.
   Polaris vous annonce le dossier qu'il va créer, avant de commencer.
4. Cliquez sur **Télécharger le cours**.

Comptez une dizaine de secondes : un cours transporte ses images. Polaris affiche
l'avancement, puis **ouvre le cours tout seul** à la fin. Si le cours ne contient qu'un seul
fichier `.adoc`, il est ouvert aussi : vous pouvez écrire immédiatement.

L'emplacement que vous avez choisi est retenu. Au cours suivant, il est déjà là.

> **Vous avez déjà le cours sur votre poste ?** Utilisez **📂 Ouvrir un cours…** à la place, et
> désignez le dossier.

> **N'importe quel lien de la page du cours fait l'affaire.** Si vous copiez la barre
> d'adresse de votre navigateur en regardant un fichier ou une branche — une adresse du genre
> `.../mon-cours/blob/main/cours.adoc` — Polaris la ramène tout seul au cours lui-même.

**Si le téléchargement échoue**, le message vous dit laquelle des deux situations vous
concerne :

- **votre poste n'a pas d'identifiants GitHub enregistrés** — un `git push` en ligne de
  commande, une fois, suffit à les enregistrer ; demandez à votre référent ;
- **le cours reste introuvable** — soit le lien ne désigne aucun cours, soit il est privé et
  votre compte n'y a pas accès. GitHub répond la même chose dans ces deux cas, pour ne pas
  révéler l'existence d'un dépôt privé : vérifiez le lien avec la personne qui vous l'a
  transmis, et demandez-lui si vous êtes bien membre du dépôt.

---

## 2. Écrire son cours

Un cours ENI, c'est **un seul fichier** `.adoc`. Tout le cours est dedans : modules, slides,
travaux pratiques, démonstrations, notes orateur.

### Si le code AsciiDoc vous gêne : l'affichage confortable

Un cours en AsciiDoc contient des signes qui servent à la mise en forme : `===` devant un
titre, `*mot*` pour du gras, `[.tp-slide]` avant un TP. Rien de compliqué, mais quand on
n'y est pas habitué, ça encombre la lecture.

Au centre de la barre d'outils, un bouton **Vue** propose deux affichages :

| | |
|---|---|
| **AsciiDoc** | le cours tel qu'il est écrit, avec les signes de mise en forme |
| **Texte** | les signes masqués, le texte mis en forme |

En choisissant **Texte**, Polaris **masque ces signes et met votre texte en forme directement
dans l'éditeur** : les titres s'affichent en grand, le gras en gras, les puces en puces, et les
lignes techniques deviennent de petites étiquettes qui disent ce qu'elles font — « Slide de
travaux pratiques », « Code bash », « Support formateur — non projeté ». La police devient
celle d'un document, plus celle d'un fichier de code.

Trois choses à savoir :

- **Votre fichier n'est pas modifié.** C'est seulement un affichage. Vous pouvez cocher et
  décocher autant que vous voulez, le cours reste identique.
- **La ligne où se trouve votre curseur remontre son code.** C'est voulu : c'est comme ça
  qu'on corrige un signe précis — et c'est aussi la façon la plus simple de découvrir la
  syntaxe, en se posant sur une ligne pour voir ce qu'il y a dessous.
- **Les blocs de code et les sorties d'écran ne changent pas.** Leur alignement en colonnes
  fait partie de leur sens.

Si un `**` ou un `*` reste affiché alors que la vue **Texte** est active, ce n'est pas un
bug : c'est que le balisage est mal fermé à cet endroit, et le support publié l'affichera
pareil.

Le même choix existe dans **Réglages → Confort de lecture…**, sous le nom « Affichage
confortable » : c'est le même réglage, celui de la barre d'outils étant plus rapide à
atteindre en cours de rédaction. Votre choix est retenu d'une session à l'autre.

### La barre d'outils

Sous le bandeau, les boutons sont rangés par groupes, chacun surmonté de son titre —
comme un ruban Word :

| Groupe | Ce qu'on y trouve |
|---|---|
| **Texte** | gras, italique, code |
| **Titres** | module, slide, sous-section |
| **Listes** | à puces, numérotée |
| **Insérer** | bloc de code, texte littéral, lien, image, tableau |
| **Encadrés** | note, astuce, important, avertissement |
| **Copilot** | proposer la suite, découper une slide, rédiger les notes orateur |

**Survolez un bouton** : l'infobulle dit ce qu'il fait *et* la syntaxe exacte qu'il produit.
La barre est donc aussi un aide-mémoire.

### Les templates ENI

Le bouton **Templates ENI**, à droite de la barre, insère des blocs complets déjà au
formalisme de l'école :

| Template | Ce qu'il insère |
|---|---|
| `eni-module` | un module entier |
| `eni-slide` | une slide standard |
| `eni-tp` | un travail pratique, avec énoncé et corrigé |
| `eni-demo` | une démonstration, avec son déroulé |
| `eni-code` | un bloc de code coloré |
| `eni-literal` | du texte affiché tel quel (sortie de console, arborescence) |
| `eni-img` | une image |
| `eni-notes` | des notes orateur |
| `eni-step` | une liste à révélation progressive |

Après insertion, appuyez sur **Tab** pour passer d'un emplacement à remplir au suivant.

### Deux raccourcis qui font gagner du temps

- **`Ctrl+K`** ouvre une barre de recherche unique : tapez trois lettres et vous trouvez une
  syntaxe, un template, ou **une slide de votre cours** pour y aller directement. C'est le
  raccourci le plus utile de Polaris.
- **`Ctrl+Espace`** propose des complétions à l'endroit du curseur : les rôles de slide
  (`[.standard-slide]`, `[.tp-slide]`…), les langages de coloration, les métadonnées du cours.
  Elles apparaissent aussi toutes seules en tapant. **Entrée** accepte.

### Ce que Polaris écrit pour vous

- **Le séparateur de slide.** Tapez `== ` ou `=== ` en début de ligne : Polaris insère
  au-dessus la ligne de séparation ENI. Un seul `Ctrl+Z` annule les deux.
- **Le numéro d'image.** Le bouton d'ajout d'image copie votre fichier dans
  `assets/images/` et lui donne le numéro suivant, de dix en dix (10, 20, 30…). Les valeurs
  intermédiaires restent libres pour insérer une image plus tard sans tout renuméroter.

### Se repérer dans un long cours

- **Le plan du cours**, dans le panneau de gauche, liste vos modules et vos slides. Cliquez
  sur une entrée : le curseur y va, et l'aperçu suit.
- **Replier une section** : les petits `▾` dans la marge de gauche de l'éditeur. Replier un
  titre de module masque tout le module.

---

## 3. Voir ce que verront les apprenants

La colonne de droite affiche votre cours **mis en page comme le support publié**, avec la
charte de votre cursus. Elle se met à jour pendant que vous écrivez, et **suit votre
curseur** : vous voyez toujours la slide sur laquelle vous travaillez.

Ce que l'aperçu vous montre en plus du texte :

- **les cartes de slide** au format 16/9, celui des tableaux interactifs de l'école : vous
  voyez tout de suite si une slide est trop chargée ;
- **les notes orateur** sorties de la carte, puisqu'elles ne seront pas projetées ;
- **le contenu de support** (énoncés et corrigés de TP, déroulés de démo) regroupé en annexe,
  sur fond papier : ce qui ne partira **pas** au diaporama se distingue d'un coup d'œil.

> **L'aperçu s'affiche sans les couleurs ENI ?** C'est que le poste n'a pas de réseau : la
> charte graphique est chargée en ligne. Vous pouvez continuer à écrire, le cours n'est pas
> affecté.

---

## 4. Ce que Polaris vérifie pour vous

Le formalisme ENI est plein de pièges silencieux : rien n'échoue, mais le support publié est
faux. Polaris les cherche pendant que vous écrivez et les compte **en bas à droite**.

| Compteur | Ce que ça veut dire |
|---|---|
| **rouge** — « 2 non publiés » | du contenu **va disparaître** du support publié, ou la structure est cassée |
| **jaune** — « 12 mal rendus » | tout est là, mais le rendu sera fautif |
| **bleu** — « 3 slides trop chargées » | la slide déborde de la zone projetée |

**Cliquez sur un compteur** : le curseur va au premier problème. Dans l'éditeur, le passage
concerné est souligné, avec un marqueur dans la marge ; survolez-le pour lire ce qui est en
cause. **F8** ouvre la liste et permet de passer d'un signalement au suivant.

> **Le cas le plus fréquent** : un bloc de code jamais refermé. Il fait disparaître tout ce
> qui suit — parfois des modules entiers. Polaris le signale en tête du plan du cours, parce
> que sinon on croit à un bug de l'outil.

Les mots absents du dictionnaire sont soulignés **en bleu pointillé**, jamais en rouge.
Survolez-les pour voir les corrections proposées, ou pour ajouter le mot à votre dictionnaire.

---

## 5. Publier son travail

Un cours se modifie sur **votre version de travail**, pas directement sur la version commune :
votre travail part ensuite en relecture. Polaris s'occupe de tout ça.

### Enregistrer, ce n'est pas publier

**💾 Enregistrer** (ou `Ctrl+S`) écrit le fichier sur votre poste. C'est tout. Publier, c'est
l'étape suivante, et elle est volontaire.

### Publier

1. En bas à gauche, cliquez sur **🗂 Mon travail**. Le panneau s'ouvre et liste ce que vous
   avez changé — cliquez sur un fichier pour voir précisément quoi.
2. La première fois, Polaris vous demande **comment vous vous appelez**. C'est ce nom qui
   signera vos enregistrements ; il n'est demandé qu'une fois, pour tous vos cours.
3. Écrivez une phrase qui dit ce que vous avez changé — elle est destinée à la personne qui
   relira.
4. Cliquez sur **Publier mon travail**.

Polaris crée votre version de travail si nécessaire, enregistre, puis envoie. Il vous dit
ensuite ce qui s'est passé.

### « Enregistré sur ce poste, mais pas envoyé »

Si le réseau tombe, **votre travail n'est pas perdu** : il est enregistré localement, et
Polaris le dit clairement. Le bouton **↑ Envoyer** apparaît en bas pour réessayer plus tard.

### Et ensuite ? La relecture

Après une publication réussie, le panneau vous dit **sur quelle version de travail** votre
cours est parti — par exemple « publié sur *eloise-menard* ». C'est l'information à
transmettre à votre référent : elle suffit à retrouver votre travail.

**La demande de relecture elle-même se fait sur GitHub, et Polaris ne la fait pas à votre
place.** C'est un choix : remplir ce formulaire — titre, description, choix de la branche
cible, relecteurs — est un travail technique, et un bouton qui prétendrait le régler d'un clic
vous mettrait devant une page que rien ne vous a préparé à lire.

- **Vous ne connaissez pas GitHub ?** Prévenez votre référent que votre travail est publié, en
  lui donnant le nom de votre version de travail. Il s'occupe de la suite.
- **Vous êtes à l'aise avec GitHub ?** Le panneau affiche l'**adresse de la page de demande**,
  toute prête. Un clic dessus la sélectionne entièrement : collez-la dans votre navigateur.
  Le formulaire s'y ouvre déjà déplié ; votre demande n'existe qu'après avoir cliqué sur le
  bouton vert **« Create pull request »**.

### Récupérer les modifications des autres

Le bouton **↓ Récupérer**, en bas, rapatrie ce qui est arrivé pendant votre absence. Si votre
version et la version commune ont divergé, Polaris refuse et vous le dit : ce genre
d'arbitrage se fait à deux, pas tout seul dans un éditeur.

---

## 6. Régler son confort de lecture

**Réglages → Confort de lecture…** Ces réglages ne changent que **votre affichage** : le cours
et ce que verront les apprenants ne bougent pas.

- **Taille du texte**, **interligne**, **espacement des lettres**, **espacement des mots** :
  quatre réglettes pour le texte que vous écrivez. Les seuils recommandés par le référentiel
  d'accessibilité sont indiqués sous chacune, et le bouton **Confort maximal** les applique
  d'un clic.
- **Taille de l'interface** : le bandeau, le plan du cours, la barre du bas et les fenêtres
  suivent. Grossir son texte sans pouvoir lire le nom de son fichier n'avait pas de sens.
- **Affichage confortable** : le même réglage que le bouton **Vue** de la barre d'outils.
  Décrit en détail au chapitre 2.
- **Correcteur orthographique** : à décocher si vous préférez écrire sans.
- **Mots que vous avez ajoutés** : replié par défaut, avec le nombre. Dépliez-le pour retirer
  un mot que vous auriez admis par erreur.

Tout est réglé sur votre poste et retenu d'une session à l'autre. Rien ne part sur le réseau :
les dictionnaires sont embarqués dans Polaris.

---

## 7. Se faire aider par Copilot

Copilot sait faire **trois choses** pour vous, toutes dans le groupe **Copilot** de la barre
d'outils. Il travaille à partir de votre cours : ses propositions lui ressemblent — séparateur,
rôle de slide, titre, liste à puces.

| Bouton | Ce qu'il fait |
|---|---|
| **✨ Proposer la suite** | écrit la slide suivante, à partir de ce qui précède |
| **▭ Découper cette slide** | répartit en deux la slide où est votre curseur |
| **💬 Rédiger les notes orateur** | écrit le bloc de notes de cette slide |

**Aucun des trois n'écrit dans votre cours sans votre accord.** La proposition s'affiche
d'abord, vous la lisez, vous décidez. Une fois insérée, un seul `Ctrl+Z` l'annule.

### L'activer, une fois

1. **Réglages → Autocomplétion Copilot…**
2. **Activer Copilot.** La première fois, comptez une centaine de mégaoctets à télécharger —
   **une seule fois**. Mieux vaut ne pas le faire pendant une séance, le réseau d'une salle
   étant partagé.
3. **Se connecter à GitHub.** Polaris affiche un code à recopier et ouvre la page GitHub dans
   votre navigateur. Recopiez le code, autorisez l'accès : l'écran de Polaris bascule tout
   seul sur « Connecté ».

Aux lancements suivants, Copilot se remet en route sans rien demander. Vous pouvez le
désactiver depuis le même écran.

> Polaris ne conserve **aucun mot de passe**. Votre jeton d'accès est rangé par Windows, au
> même endroit que celui qui vous authentifie déjà auprès de GitHub.

### Proposer la suite du cours

Placez le curseur là où vous en êtes, puis cliquez sur le bouton **✨** de la barre d'outils
(ou `Ctrl+K` puis « proposer »).

Un panneau s'ouvre en bas de la fenêtre. Comptez une à deux secondes, puis la proposition
s'affiche **telle qu'elle entrera dans votre fichier**, avec une ligne qui vous dit si elle
respecte le formalisme ENI.

- **Insérer** l'ajoute à votre cours. Un seul `Ctrl+Z` l'annule.
- **Suivante** fait défiler les autres propositions, quand il y en a plusieurs.
- **Autre proposition** en redemande.
- **Ignorer** ferme sans rien changer.

> **Rien à proposer ?** Ça arrive. Copilot s'appuie sur ce qui précède : il est plus utile
> après un titre de slide ou en fin de liste qu'au milieu d'un paragraphe.

### Découper une slide trop chargée

Quand Polaris signale une slide **trop chargée** (le compteur bleu, en bas à droite), il vous
disait jusqu'ici le problème sans proposer de solution. Placez le curseur **dans la slide**
concernée, puis cliquez sur **▭ Découper cette slide**.

Copilot répartit le contenu en deux slides — mêmes puces, même rôle de slide, séparateurs et
titres compris. Comptez sept à huit secondes : la réponse s'écrit sous vos yeux pendant
qu'elle arrive.

La proposition **remplace la slide entière**, préambule compris. Le panneau vous le dit avant
que vous n'insériez quoi que ce soit.

⚠️ **Vérifiez la répartition.** Copilot ne doit rien inventer ni rien supprimer, seulement
répartir — mais c'est à vous de le constater. Et Polaris ne sait pas encore vous dire si les
deux nouvelles slides tiennent, elles, dans la zone projetée : le compteur se recalcule après
l'insertion.

### Faire rédiger les notes orateur

Placez le curseur dans une slide, cliquez sur **💬 Rédiger les notes orateur**. Copilot écrit
ce que vous direz à l'oral — pas ce qui est déjà écrit sur la slide — dans un bloc `[.notes]`
ajouté **à la fin** de la slide. Rien n'est remplacé.

### Ce qui est envoyé, et ce qui ne l'est pas

**Seule la slide où se trouve votre curseur est envoyée**, jamais votre cours entier. C'est
une règle de construction, pas une intention : Polaris ne sait pas envoyer autre chose.

Ces demandes utilisent votre abonnement GitHub Copilot : il n'y a rien de plus à installer, ni
à configurer, ni à payer. Une demande consomme environ une « interaction premium » sur les
1 500 dont vous disposez chaque mois — soit largement plus d'un millier de demandes.

> **Vous fermez le panneau pendant qu'il travaille ?** La demande est réellement interrompue.
> Rien ne continue à tourner dans votre dos.

---

## 8. Quand ça coince

**L'aperçu est en noir et blanc, sans mise en page ENI.**
Pas de réseau. La charte graphique est chargée en ligne. Vous pouvez écrire, le cours n'est
pas affecté.

**Des modules entiers ont disparu de l'aperçu.**
Un bloc de code n'est pas refermé. Polaris l'annonce en tête du plan du cours, avec le numéro
de ligne : cliquez dessus.

**Toutes les images sont cassées.**
Le fichier de configuration du cours n'est pas trouvé. Vérifiez que vous avez ouvert le
**dossier du cours**, et non un fichier isolé. Le texte de remplacement d'une image affiche le
chemin complet cherché, ce qui distingue « fichier absent » de « mauvais dossier ».

**Un bloc de texte affiche ses quatre points dans l'aperçu.**
Le bloc est décalé d'une espace : en AsciiDoc, une ligne qui commence par une espace n'est plus
un délimiteur, c'est du texte. Le contrôle du document le signale en jaune — collez le
délimiteur contre la marge, sans espace devant.

**Publier échoue en parlant d'identifiants.**
Votre poste n'a pas d'identifiants GitHub enregistrés. Faites un `git push` une fois en ligne
de commande sur ce dépôt : le gestionnaire d'identifiants les retiendra, et Polaris les
réutilisera.

**Polaris refuse de publier sur la version commune.**
C'est voulu. Le panneau vous propose de créer votre version de travail : acceptez, votre
travail en cours la suit.

**Aucun mot n'est souligné, alors que le correcteur est coché.**
Ouvrez **Réglages → Confort de lecture** : si le correcteur n'a pas pu démarrer sur ce poste,
c'est écrit là.

**Copilot dit que le serveur s'est arrêté.**
Rouvrez **Réglages → Autocomplétion Copilot** et cliquez sur **Vérifier à nouveau** : le
serveur se relance.

**Le bandeau de mise à jour ne s'affiche pas alors qu'une version est sortie.**
La vérification a lieu quelques secondes après le démarrage, puis une fois par jour. Fermez
Polaris, rouvrez-le, et attendez cinq secondes.

---

## 9. Ce que Polaris ne sait pas encore faire

Autant le dire :

- **Pas d'export PDF.** Il est conçu — un polycopié tiré du même fichier, pas une capture du
  diaporama — mais pas encore écrit.
- **Après une découpe, Polaris ne sait pas dire si les deux slides tiennent.** Le contrôle
  « slide trop chargée » ne s'applique qu'à votre cours enregistré, pas à une proposition
  affichée : il se recalcule une fois la proposition insérée.
- **Polaris ne crée pas la demande de relecture.** Il vous donne l'adresse de la page ; le
  formulaire se remplit sur GitHub (voir la section 5).
- **Pas de recherche multi-fichiers**, ni de plusieurs onglets ouverts en même temps.
- **Le plan du cours affiche les titres de support comme des slides.** Un titre écrit dans un
  bloc réservé au support formateur (« - Énoncé », « - Solution ») apparaît dans le plan comme
  s'il était projeté. L'aperçu, lui, fait la différence correctement.
- **macOS** : la publication vers GitHub n'a pas encore été vérifiée sur Mac.
- **Linux** : une installation par `.deb` ou `.rpm` ne peut pas se mettre à jour toute seule.
