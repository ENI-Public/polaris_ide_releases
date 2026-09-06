# Polaris IDE — guide du formateur

Ce guide suit l'ordre dans lequel vous allez rencontrer les choses : ouvrir un cours,
l'écrire, vérifier, publier. Vous n'avez pas besoin de le lire en entier avant de commencer —
les deux premières sections suffisent pour travailler.

> **Vous n'avez pas besoin de connaître Git.** Polaris parle de « ton travail », de
> « télécharger un cours » et de « publier ». Les mots de Git sont là, dans les infobulles,
> pour la personne qui viendra vous dépanner.

**Sommaire**

1. [Ouvrir un cours](#1-ouvrir-un-cours)
2. [Écrire son cours](#2-écrire-son-cours)
3. [Voir ce que verront les apprenants](#3-voir-ce-que-verront-les-apprenants)
4. [Ce que Polaris vérifie pour vous](#4-ce-que-polaris-vérifie-pour-vous)
5. [Publier son travail](#5-publier-son-travail)
6. [Régler son confort de lecture](#6-régler-son-confort-de-lecture)
7. [Se faire aider par Copilot](#7-se-faire-aider-par-copilot)
8. [Tout se fait au clavier](#8-tout-se-fait-au-clavier)
9. [Quand ça coince](#9-quand-ça-coince)
10. [Ce que Polaris ne sait pas encore faire](#10-ce-que-polaris-ne-sait-pas-encore-faire)

---

## 1. Ouvrir un cours

Tout part d'un seul bouton, dans le bandeau du haut : **Ouvrir un cours…**. Quand aucun cours
n'est ouvert, la même chose vous attend directement au milieu de l'écran.

Trois onglets, trois façons d'arriver sur un cours.

### Reprendre un cours

Polaris retient les cours que vous ouvrez, du plus récent au plus ancien, avec leur code et la
date de la dernière ouverture. Un clic suffit pour y revenir.

Si vous avez déplacé ou supprimé le dossier d'un cours, il reste affiché en grisé, avec une
croix pour le retirer de la liste. **Le retirer ne supprime rien sur votre disque** : cela ne
fait que nettoyer la liste.

### Prendre un cours de l'école

L'onglet **Cours de l'école** affiche les cours auxquels votre compte GitHub a accès. Cliquez
sur **Afficher les cours de l'école** la première fois.

- Les boutons **DEV**, **RES** et **TRA** filtrent par filière, et annoncent le nombre de cours
  de chacune.
- Le champ de recherche trouve un cours par son code, son titre ou sa description. Les accents
  n'ont pas d'importance : « methodes » trouve « Méthodes ».
- Cliquez sur un cours, indiquez où le ranger, puis **Télécharger le cours**.

Le **compte utilisé** est affiché au-dessus de la liste. Si celle-ci vous paraît courte, c'est
la première chose à regarder — surtout si vous avez plusieurs comptes GitHub sur ce poste.

> **La liste est gardée sur votre poste.** Elle réapparaît aussitôt la fois suivante, avec sa
> date. Le bouton **Actualiser** la remet à jour quand vous le voulez.

#### Ce que Polaris utilise pour afficher cette liste

Pour savoir à quels cours vous avez accès, Polaris a besoin de s'identifier auprès de GitHub. Il
utilise pour cela les **identifiants déjà enregistrés sur votre poste** — exactement les mêmes
que ceux qui servent à récupérer un cours et à publier votre travail. Vous n'avez rien de plus à
saisir, ni à configurer.

- **Polaris ne conserve aucun mot de passe ni aucun jeton d'accès.** Il les demande à Windows au
  moment de la demande, s'en sert, et les oublie. Ce qui est gardé sur votre poste, c'est
  uniquement la **liste des cours** : leurs noms et leurs dates.
- **Rien n'est envoyé ailleurs qu'à GitHub**, et rien n'est demandé tant que vous n'avez pas
  cliqué. Ouvrir l'onglet ne déclenche rien.
- **Polaris ne lit que la liste des dépôts** auxquels votre compte a accès. Il ne parcourt pas
  leur contenu, et ne voit rien des dépôts auxquels vous n'avez pas accès.

### Ouvrir un dossier de votre poste

Si le cours est déjà chez vous — parce que vous l'avez récupéré avant, ou qu'on vous l'a
copié — l'onglet **Sur mon poste** ouvre son dossier directement.

> **Quelle que soit la façon dont vous arrivez, Polaris ouvre le cours tout seul.** Un cours
> ENI tient dans un seul fichier, `cours.adoc`, et c'est celui-là que vous éditez : vous n'avez
> plus à le désigner. Le nom du cours s'affiche dans le bandeau du haut, et le panneau de
> gauche montre son plan.
>
> Si Polaris vous répond que le dossier **ne contient pas de `cours.adoc`**, c'est presque
> toujours qu'un dossier au-dessus a été désigné : reprenez en choisissant le dossier **du
> cours lui-même**, celui qui porte son code (par exemple `DEV24_0350B-devops`).

### Coller un lien, si le cours n'est pas dans la liste

Sous la liste, un champ attend un lien. Il sert pour un cours tout neuf, qui n'y figure pas
encore, ou pour un lien qu'on vous a transmis.

Collez l'adresse de la page GitHub du cours, indiquez où le ranger, et **Télécharger le cours**.
Comptez une dizaine de secondes : un cours transporte ses images. Polaris affiche l'avancement,
puis **ouvre le cours tout seul** à la fin. Si le cours ne contient qu'un seul fichier `.adoc`,
il est ouvert aussi : vous pouvez écrire immédiatement.

L'emplacement que vous avez choisi est retenu. Au cours suivant, il est déjà là.

> **N'importe quel lien de la page du cours fait l'affaire.** Si vous copiez la barre d'adresse
> de votre navigateur en regardant un fichier ou une branche — une adresse du genre
> `.../mon-cours/blob/main/cours.adoc` — Polaris la ramène tout seul au cours lui-même. Un lien
> collé au milieu d'une phrase, depuis un message ou un mail, fonctionne aussi.

> **Si le lien ne désigne pas un cours**, Polaris vous le dit avant d'essayer, et vous indique à
> quoi ressemble le bon lien. Le lien d'une organisation, celui d'un fichier brut ou celui du
> site publié ne sont pas des liens de cours.

### Si la récupération échoue

Le message vous dit laquelle des situations vous concerne.

**« Ton poste n'a pas encore d'identifiants GitHub enregistrés. »** Une première récupération en
ligne de commande (`git clone`) suffit à les enregistrer ; Polaris les réutilisera ensuite.
Demandez à votre référent si vous ne savez pas comment faire.

**« Pour ce compte-là, ce cours n'existe pas. »** GitHub répond la même chose qu'un cours soit
absent ou simplement invisible pour le compte utilisé : il ne révèle pas l'existence d'un dépôt
privé. Le message **nomme le compte** qui vient d'être utilisé, et il y a trois causes, de la
plus fréquente à la plus rare :

1. **Ce n'est pas le bon compte.** Si vous avez plusieurs comptes GitHub sur ce poste, vérifiez
   que celui qui a été utilisé est bien celui qui a accès aux cours.
2. **Votre compte n'a pas encore accès à ce cours.** Demandez à l'ingénierie pédagogique de vous
   ajouter au dépôt.
3. **Le lien ne désigne pas ce cours.** Vérifiez-le avec la personne qui vous l'a transmis.

### Les informations du cours

Un cours porte des informations que l'école attend : son code, son titre, sa durée, son public,
son niveau, son cursus. Elles servent à la page de garde de votre support, aux thèmes graphiques
et aux traitements automatiques de l'école.

Elles sont écrites en haut de votre fichier, mais **vous n'avez pas à les y taper**. Dans le
bandeau, le bouton **ⓘ Infos du cours…** — celui qui est bleu, à côté du nom de votre cours —
ouvre un formulaire :

- le **code du cours** est déjà rempli, repris du nom du dépôt ;
- le **niveau** et le **cursus** se choisissent dans une liste — impossible de se tromper de
  valeur ;
- les champs **obligatoires** portent la mention « obligatoire » et un liseré orange tant
  qu'ils sont vides.

Une pastille sur le bouton indique combien il en reste à compléter.

> **Sur un cours tout neuf, tout est vide, et c'est normal.** Les cours sont créés à partir
> d'un modèle qui laisse ces informations à remplir. C'est la première chose à faire en
> recevant un cours.

**Tant qu'une information obligatoire manque, vous ne pouvez pas publier.** Le bouton de
publication est alors remplacé par **Compléter les infos du cours**, qui vous y emmène.
Enregistrer votre travail sur votre poste (`Ctrl+S`) reste toujours possible : c'est seulement
l'envoi vers l'école qui attend.

> **Où sont passées ces lignes dans l'éditeur ?** Elles sont **repliées** : le haut de votre
> fichier contient une trentaine de lignes de réglages et d'explications, qui n'ont pas à vous
> encombrer. Votre cours commence donc à son premier module. Cliquez sur le **▸** de la
> première ligne pour les revoir — rien n'est caché, seulement plié.

> **La slide « Public visé » est repliée elle aussi**, pour la même raison : elle ne contient
> pas de texte, mais un **renvoi** vers le public que vous avez saisi ici. Si vous l'ouvriez
> pour y écrire, votre cours cesserait de suivre ce formulaire. Corrigez le public dans les
> infos du cours : la slide se met à jour toute seule.

---

## 2. Écrire son cours

Un cours ENI, c'est **un seul fichier** `.adoc`. Tout le cours est dedans : modules, slides,
travaux pratiques, démonstrations, notes orateur.

### Si le code AsciiDoc vous gêne : l'affichage confortable

Un cours en AsciiDoc contient des signes qui servent à la mise en forme : `===` devant un
titre, `*mot*` pour du gras, `[.tp-slide]` avant un TP. Rien de compliqué, mais quand on
n'y est pas habitué, ça encombre la lecture.

À **droite** de la barre d'outils, sous le titre **Affichage**, deux icônes proposent
deux vues :

| | |
|---|---|
| **¶** | *AsciiDoc* — le cours tel qu'il est écrit, avec les signes de mise en forme |
| **≡** | *Texte* — les signes masqués, le texte mis en forme |

Le **¶** est le même signe que le bouton « Afficher les marques de mise en forme » de Word :
il montre ce qui est habituellement caché. Passez la souris dessus, ou atteignez-les au
clavier, pour voir leur nom.

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
| **Titres** | module, slide standard, sous-section |
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

> **Au centre de la barre**, deux groupes nommés **Recherche** et **Palette** : le premier
> ouvre la recherche par périmètre (section 4), le second la palette de commandes. À droite,
> le groupe **Affichage** réunit le choix de vue et le repli de l'aperçu.

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
- **Le type de la slide.** Le bouton **Titre de slide standard** (groupe *Titres*) ne pose pas
  que le titre : il ajoute aussi le séparateur et la ligne `[.standard-slide]`, sans laquelle
  la slide n'aurait pas de gabarit. Si la ligne du dessus annonce déjà un type — un TP, une
  démo — Polaris le laisse tel quel. Pour les deux autres types, passez par les templates
  `eni-tp` et `eni-demo`, qui apportent en plus l'énoncé ou le déroulé.
- **Le numéro d'image.** Le bouton d'ajout d'image copie votre fichier dans
  `assets/images/` et lui donne le numéro suivant, de dix en dix (10, 20, 30…). Les valeurs
  intermédiaires restent libres pour insérer une image plus tard sans tout renuméroter.

### Citer un ouvrage des Éditions ENI

La slide « Ressources complémentaires » du préambule cite souvent un livre du catalogue des
**Éditions ENI**. Polaris fait le travail mécanique à votre place, depuis la fenêtre
**Infos du cours…** — c'est le moment où vous décrivez votre cours, donc celui où la question
se pose.

1. Sur `editions-eni.fr`, ouvrez la page du livre et **copiez son adresse**.
2. Dans le bandeau du haut, cliquez sur **Infos du cours…** et descendez jusqu'à
   **Ouvrage des Éditions ENI**.
3. Collez l'adresse et cliquez sur **Lire la fiche**. La couverture, le titre, les auteurs et
   l'ISBN s'affichent : vérifiez que c'est bien le bon livre.
4. **Insérer l'ouvrage dans la slide** : la couverture est enregistrée dans les images du
   cours, à la numérotation ENI, et la référence est écrite dans votre slide
   « Ressources complémentaires ».

Trois choses à savoir :

- **Peu importe où est votre curseur.** Polaris retrouve la slide
  « Ressources complémentaires » tout seul et écrit à la fin de celle-ci. Si votre cours n'en
  a pas, la fenêtre vous le dit au lieu d'écrire n'importe où : ajoutez la slide dans le
  préambule, puis revenez.
- **Vous choisissez le livre, pas Polaris.** Il n'y a pas de recherche depuis l'application :
  le site ne permet pas aux outils automatiques de l'interroger, et de toute façon choisir
  l'ouvrage qui va avec votre cours est un jugement qui vous appartient.
- **Un cours publié sur GitHub redistribue la couverture.** L'usage des visuels des Éditions
  dans un support relève d'un accord interne : en cas de doute, demandez-le avant de publier.
  La fenêtre vous le rappelle.

### Coller une capture d'écran

Vous venez de faire une capture — **Impr. écran**, ou **Windows + Maj + S** — et elle est dans
votre presse-papiers. Cliquez à l'endroit voulu dans votre cours et collez : la fenêtre d'ajout
d'image s'ouvre directement avec votre capture. Vous n'avez pas à l'enregistrer d'abord.

Elle reçoit le prochain numéro ENI, comme n'importe quelle image, et le fichier est copié dans
`assets/images/`.

> **Pensez au texte alternatif.** Une capture n'a pas de nom de fichier dont Polaris pourrait
> le déduire : le champ est donc vide, et c'est à vous de dire ce que montre l'image. C'est ce
> texte que liront les apprenants qui ne voient pas l'écran, et celui qui s'affiche si l'image
> se perd.

Si vous collez à l'intérieur d'un bloc de code, Polaris refuse et vous le dit : une image n'a
pas sa place dans un bloc de code, elle s'y afficherait en toutes lettres.

### Se repérer dans un long cours

- **Le plan du cours**, dans le panneau de gauche, liste vos modules et vos slides. Cliquez
  sur une entrée : le curseur y va, et l'aperçu suit.
- **Replier une section** : les petits `▾` dans la marge de gauche de l'éditeur. Replier un
  titre de module masque tout le module.

---

## 3. Voir ce que verront les apprenants

> **Vous pouvez replier l'aperçu.** À droite de la barre d'outils, sous le titre
> **Affichage**, la troisième icône montre une fenêtre coupée en deux. Cliquez : l'aperçu
> disparaît et toute la largeur revient à l'écriture — pratique pour un long bloc de code ou
> un tableau. Recliquez pour le revoir. Votre choix est retenu d'une session à l'autre, et le
> cours n'est pas modifié.

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

> **Certains signalements se corrigent d'un clic.** Quand Polaris sait quoi faire sans risque
> de se tromper, l'infobulle propose des **boutons de correction** sous le message. Par
> exemple, sur une slide à laquelle il manque son type, on vous propose les trois : slide de
> contenu classique, de démonstration, de travaux pratiques. Vous cliquez sur celui qui
> convient, la ligne est écrite au bon endroit et le signalement disparaît. Un `Ctrl+Z` annule
> la correction comme n'importe quelle frappe.

> **Le cas le plus fréquent** : un bloc de code jamais refermé. Il fait disparaître tout ce
> qui suit — parfois des modules entiers. Polaris le signale en tête du plan du cours, parce
> que sinon on croit à un bug de l'outil.

> **Sur un cours tout neuf, le compteur rouge annonce les informations du cours** qui restent
> à remplir. Ce n'est pas que votre cours est cassé : c'est ce par quoi commencer. Voir
> [Les informations du cours](#les-informations-du-cours).

Les mots absents du dictionnaire sont soulignés **en bleu pointillé**, jamais en rouge.
Survolez-les pour voir les corrections proposées, ou pour ajouter le mot à votre dictionnaire.

---

## 5. Publier son travail

Un cours se modifie sur **votre version de travail**, pas directement sur la version commune :
votre travail part ensuite en relecture. Polaris s'occupe de tout ça.

### Enregistrer, ce n'est pas publier

**💾 Enregistrer** (ou `Ctrl+S`) écrit le fichier sur votre poste. C'est tout. Publier, c'est
l'étape suivante, et elle est volontaire.

Le bouton **change de couleur selon ce qu'il propose**, et c'est une escalade :

| | |
|---|---|
| **vert** | Enregistrer — c'est sur votre poste, c'est sans risque |
| **ambre** | Compléter les infos du cours — il manque quelque chose |
| **orange** | Publier mon travail — cette fois, le travail quitte votre poste |

> **Si vous fermez Polaris sans avoir enregistré**, une fenêtre vous prévient et nomme le
> fichier concerné. Vous choisissez : **Enregistrer et fermer**, **Annuler**, ou **Fermer sans
> enregistrer**. Et si l'enregistrement échoue — disque plein, fichier en lecture seule —
> Polaris **ne ferme pas** : votre travail reste là, et le message dit pourquoi.

### Si Polaris s'arrête sans prévenir

La fenêtre ci-dessus vous protège d'un clic sur la croix. Elle ne peut rien contre une coupure
de courant, un plantage, ou un redémarrage imposé par Windows — et une session de formation
dure la semaine, l'app restant ouverte tout du long.

**Toutes les trois secondes, Polaris range donc une copie de votre travail en cours sur votre
poste.** À la réouverture du cours, s'il retrouve du travail plus récent que le fichier, un
bandeau ambre s'affiche au-dessus de l'éditeur :

> Du travail non enregistré a été retrouvé sur ce poste (il y a 12 minutes). Polaris s'est
> peut-être arrêté sans prévenir.

Deux boutons : **Récupérer ce travail**, qui remet le texte retrouvé dans l'éditeur, et
**Ignorer**, qui ferme simplement le bandeau.

Trois choses à savoir :

- **Polaris ne remet jamais rien tout seul.** Il propose, vous décidez. Votre fichier n'est
  écrit que quand vous enregistrez, comme avant.
- **Après récupération, le travail n'est pas enregistré** : le document redevient « modifié »,
  à vous de faire `Ctrl+S` une fois que vous avez vérifié que c'est bien ce que vous vouliez.
- **La copie ne quitte pas votre poste.** Elle n'est ni envoyée, ni publiée, ni partagée, et
  elle est effacée dès que vous enregistrez.

### Publier

> **Avant tout : les infos du cours doivent être complètes.** Si le bouton du bandeau affiche
> **Compléter les infos du cours**, c'est qu'il manque une information obligatoire — cliquez
> dessus, remplissez, revenez. Vous ne perdez rien en attendant : votre travail est enregistré
> sur votre poste, seule la publication patiente.

1. En bas à gauche, cliquez sur **🗂 Mon travail**. Le panneau s'ouvre et liste ce que vous
   avez changé — cliquez sur un fichier pour voir précisément quoi.
2. La première fois, Polaris vous demande **comment vous vous appelez**. C'est ce nom qui
   signera vos enregistrements ; il n'est demandé qu'une fois, pour tous vos cours.
3. Écrivez une phrase qui dit ce que vous avez changé — elle est destinée à la personne qui
   relira.

   > **Si Copilot est activé**, un bouton **Proposer un message** apparaît au-dessus du
   > champ. Copilot lit ce que vous avez modifié et propose une phrase. Elle s'affiche **à
   > côté** du champ, pas dedans : rien n'est retenu tant que vous n'avez pas cliqué sur
   > **Utiliser ce message**, et vous pouvez ensuite la corriger. Ce que Copilot reçoit dans
   > ce cas est décrit à la section 7.
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
  toute prête, avec un bouton **Copier** à droite. Collez-la dans votre navigateur : le
  formulaire s'y ouvre déjà déplié, et votre demande n'existe qu'après avoir cliqué sur le
  bouton vert **« Create pull request »**.
  *(Si la copie échoue sur votre poste, Polaris vous le dit : cliquez alors sur l'adresse
  elle-même, elle se sélectionne en entier, puis `Ctrl+C`.)*

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
- **Mots que tu as ajoutés** (c'est le libellé exact à l'écran) : replié par défaut, avec le
  nombre. Dépliez-le pour retirer un mot que vous auriez admis par erreur.

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

> **Rien à proposer ?** Ça arrive, et Polaris vous dit **à partir de quelle ligne** il a posé
> la question : Copilot continue ce qui précède, il ne devine pas à partir d'une ligne vide.
> Si votre curseur est dans un bloc de code, il vous le dit aussi — il n'y a rien à continuer
> là. Placez-le dans le texte de la slide, puis redemandez.

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

Copilot travaille chez GitHub, pas sur votre poste : pour vous répondre, il faut lui envoyer
du texte. Ce qui part **dépend du bouton**, et il vaut mieux le savoir avant d'activer.

**Tant que Copilot n'est pas activé, rien ne part.** Aucun des trois boutons n'existe, et
l'éditeur ne parle à personne. C'est l'état par défaut d'un poste neuf.

**Une fois Copilot activé, le cours ouvert est envoyé en entier**, dès son ouverture, puis au
fil de vos modifications — sans que vous ayez à cliquer sur quoi que ce soit. C'est ce qui
permet à **✨ Proposer la suite** de connaître ce que vous avez écrit plus haut. C'est aussi
exactement ce que fait Copilot dans VS Code, où beaucoup d'entre vous l'utilisent déjà sur ces
mêmes fichiers. ⚠️ **Un cours entier, cela comprend les énoncés et les corrigés de TP** : ils
sont dans le même fichier.

**Les deux demandes dirigées, elles, n'envoient que la slide de votre curseur.**
**▭ Découper cette slide** et **💬 Rédiger les notes orateur** joignent le texte de cette
seule slide à leur consigne — une quinzaine de lignes, pas votre cours. Là, c'est une règle
de construction : ces deux demandes ne savent pas envoyer autre chose.

**« Proposer un message » envoie ce que vous venez de changer.** Ce bouton, dans le panneau
**Mon travail**, joint à sa consigne la liste des fichiers touchés et le **détail de vos
modifications** — c'est-à-dire du contenu de cours, celui des passages que vous avez
retouchés. Deux limites de construction : les images et les autres fichiers non textuels ne
sont **jamais** envoyés, seulement cités par leur nom ; et le détail est plafonné, une grosse
réorganisation n'expédie donc pas tout le cours.

> **Vous préférez ne rien envoyer du tout ?** Laissez Copilot désactivé, ou désactivez-le
> depuis **Réglages → Autocomplétion Copilot…**. Tout le reste de Polaris — l'aperçu, le
> correcteur, le contrôle du formalisme, Git — fonctionne à l'identique et reste sur votre
> poste.

Ces demandes utilisent votre abonnement GitHub Copilot : il n'y a rien de plus à installer, ni
à configurer, ni à payer. Une demande consomme environ une « interaction premium » sur les
1 500 dont vous disposez chaque mois — soit largement plus d'un millier de demandes.

> **Vous fermez le panneau pendant qu'il travaille ?** La demande est réellement interrompue.
> Rien ne continue à tourner dans votre dos.

---

## 8. Tout se fait au clavier

Si vous n'utilisez pas la souris, ou peu :

- **`Tab` en arrivant** fait apparaître un bouton **Aller à l'éditeur** : il vous place
  directement dans le texte, sans traverser la barre d'outils.
- **La barre d'outils ne coûte qu'un `Tab`.** Une fois dedans, les flèches gauche et droite
  passent d'un bouton à l'autre, `Début` et `Fin` vont aux extrémités.
- **Le plan du cours ne coûte qu'un `Tab`** lui aussi. Les flèches haut et bas parcourent les
  titres, gauche et droite replient et déplient un module ou un TP, `Entrée` va à la slide.
- **Les fenêtres gardent le clavier.** `Tab` y tourne en rond au lieu de partir derrière, et
  `Échap` referme en vous ramenant au bouton d'où vous veniez.
- **La barre d'outils affiche la syntaxe du bouton où vous êtes**, juste en dessous — au
  clavier comme à la souris. C'est l'aide-mémoire AsciiDoc, sans avoir à survoler.

Les raccourcis restent : `Ctrl+S` enregistrer, `Ctrl+F` chercher, `Ctrl+H` remplacer,
`Ctrl+K` la palette, `Ctrl+Espace` l'autocomplétion, `F8` la liste des signalements.

---

## 9. Quand ça coince

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

### Rien de tout cela ? Signalez-le

**Réglages → Signaler un problème…** Une fenêtre vous explique ce qui va se passer, puis ouvre
une page GitHub dans votre navigateur, avec le formulaire déjà rempli de ce que vous ne sauriez
pas donner : la version de Polaris, votre système, et la façon dont il a été installé. Vous
n'avez qu'à raconter ce que vous faisiez et ce qui s'est passé.

Deux choses à savoir :

- **Rien n'est envoyé quand vous cliquez.** La page s'ouvre, et c'est vous qui envoyez, depuis
  GitHub. Tant que vous ne l'avez pas fait, personne ne voit rien.
- **Le signalement est public.** N'y recopiez pas de contenu de cours — ni énoncé, ni corrigé
  de TP. Décrire le problème suffit ; si une slide précise est en cause, dites son titre.

Si votre navigateur ne s'ouvre pas, Polaris affiche l'adresse et un bouton pour la copier.

---

## 10. Ce que Polaris ne sait pas encore faire

Autant le dire :

- **Pas d'export PDF.** Il est conçu — un polycopié tiré du même fichier, pas une capture du
  diaporama — mais pas encore écrit.
- **Après une découpe, Polaris ne sait pas dire si les deux slides tiennent.** Le contrôle
  « slide trop chargée » ne s'applique qu'à votre cours enregistré, pas à une proposition
  affichée : il se recalcule une fois la proposition insérée.
- **Polaris ne crée pas la demande de relecture.** Il vous donne l'adresse de la page ; le
  formulaire se remplit sur GitHub (voir la section 5).
- **Pas de recherche multi-fichiers**, ni de plusieurs onglets ouverts en même temps.
- **En fenêtre très étroite, l'aperçu peut être rogné.** Repliez-le (icône « Affichage », à
  droite de la barre d'outils) : la zone d'écriture reprend toute la place.
- **Les fichiers du panneau « Mon travail » ne s'atteignent pas encore au clavier.** Le reste
  de l'app, si.
- **Pas d'explorateur de fichiers.** Polaris ouvre le `cours.adoc` de votre dossier et n'édite
  que celui-là. Les autres fichiers d'un cours — la configuration, les automatisations — sont
  techniques et ne se modifient pas ici.
- **macOS** : la publication vers GitHub n'a pas encore été vérifiée sur Mac.
- **Linux** : une installation par `.deb` ou `.rpm` ne peut pas se mettre à jour toute seule.
