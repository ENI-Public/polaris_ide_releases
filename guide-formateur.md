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
7. [L'autocomplétion Copilot](#7-lautocomplétion-copilot)
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

**Si le téléchargement échoue**, le message parle de deux causes possibles : le lien est faux,
ou le cours est privé et votre poste n'a pas d'identifiants GitHub. GitHub répond la même
chose dans les deux cas — il ne révèle pas l'existence d'un dépôt privé — d'où l'ambiguïté.

---

## 2. Écrire son cours

Un cours ENI, c'est **un seul fichier** `.adoc`. Tout le cours est dedans : modules, slides,
travaux pratiques, démonstrations, notes orateur.

### La barre d'outils

Sous le bandeau, la rangée de boutons met en forme le texte : gras, italique, code, titres,
listes, blocs de code, liens, images, tableaux, encadrés. **Survolez un bouton** : l'infobulle
dit ce qu'il fait *et* la syntaxe exacte qu'il produit. La barre est donc aussi un
aide-mémoire.

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

| Pastille | Ce que ça veut dire |
|---|---|
| **rouge** | du contenu **va disparaître** du support publié, ou la structure est cassée |
| **jaune** | tout est là, mais le rendu sera fautif |
| **bleue** | une slide est **trop chargée** pour la zone projetée |

**Cliquez sur une pastille** : le curseur va au premier problème. Dans l'éditeur, le passage
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

### Demander la relecture

Après une publication réussie, un bouton **Demander la relecture** apparaît. Il ouvre dans
votre navigateur la page où proposer votre travail à quelqu'un. C'est la dernière étape.

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
- **Correcteur orthographique** : à décocher si vous préférez écrire sans.
- **Mots que vous avez ajoutés** : replié par défaut, avec le nombre. Dépliez-le pour retirer
  un mot que vous auriez admis par erreur.

Tout est réglé sur votre poste et retenu d'une session à l'autre. Rien ne part sur le réseau :
les dictionnaires sont embarqués dans Polaris.

---

## 7. L'autocomplétion Copilot

Copilot propose la suite de votre cours, à partir de ce que vous avez déjà écrit. Ses
propositions ressemblent donc à votre cours : séparateur, rôle de slide, titre, liste à puces.

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

### Demander une proposition

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
- **Copilot propose, il ne réorganise pas.** « Découpe cette slide qui déborde » ou « rédige
  les notes orateur de cette slide » n'existent pas encore.
- **Pas de recherche multi-fichiers**, ni de plusieurs onglets ouverts en même temps.
- **Le plan du cours affiche les titres de support comme des slides.** Un titre écrit dans un
  bloc réservé au support formateur (« - Énoncé », « - Solution ») apparaît dans le plan comme
  s'il était projeté. L'aperçu, lui, fait la différence correctement.
- **macOS** : la publication vers GitHub n'a pas encore été vérifiée sur Mac.
- **Linux** : une installation par `.deb` ou `.rpm` ne peut pas se mettre à jour toute seule.
