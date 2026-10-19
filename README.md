<div align="center">

<img src="polaris-icon.png" alt="" width="112" height="112">

# Polaris IDE

**L'éditeur de cours des formateurs ENI.**<br>
Écrivez votre cours, voyez vos slides telles que les verront vos apprenants,<br>
publiez sur GitHub sans jamais toucher à Git.

[![Dernière version](https://img.shields.io/github/v/release/ENI-Public/polaris_ide_releases?label=version&color=0f3558)](../../releases/latest)
![Windows](https://img.shields.io/badge/Windows-11-0f3558)
![macOS](https://img.shields.io/badge/macOS-Apple%20Silicon-0f3558)
![Linux](https://img.shields.io/badge/Linux-AppImage%20·%20deb%20·%20rpm-0f3558)

### [⬇️ Télécharger la dernière version](../../releases/latest)

[Installer](#-installer) · [Guide du formateur](guide-formateur.md) · [Mises à jour](#-les-mises-à-jour) · [Un problème ?](#-un-problème-)

</div>

---

## ✨ Ce que Polaris fait pour vous

<table>
<tr>
<td width="50%" valign="top">

### 👁️ Vous voyez ce que verront les apprenants
L'aperçu affiche vos slides avec la charte ENI de votre cursus, à côté du texte, et suit
votre curseur. **Cliquez dans l'aperçu**, vous voilà sur la ligne à corriger.

</td>
<td width="50%" valign="top">

### ✅ Le formalisme ENI vérifié au fil de la frappe
Bloc de code jamais refermé, slide sans type, image introuvable, slide trop chargée pour
l'écran… Polaris le signale pendant que vous écrivez, et **corrige d'un clic** quand il le
peut sans risque.

</td>
</tr>
<tr>
<td valign="top">

### 🚀 Publier sans connaître Git
Un seul bouton : **Publier mon travail**. Polaris enregistre, envoie et vous propose de
demander la relecture, en français et sans quitter l'application. Récupérer un cours de
l'école se fait aussi en un clic.

</td>
<td valign="top">

### 🤖 Copilot à vos côtés, jamais à votre place
Proposer la suite d'un cours, **découper une slide trop chargée**, **rédiger les notes
orateur**, suggérer le message de publication. Chaque proposition se lit avant d'être
acceptée : **rien n'est écrit sans votre accord**.

</td>
</tr>
<tr>
<td valign="top">

### 🧩 Le formalisme ENI à portée de main
Les templates ENI, une barre d'outils qui rappelle la syntaxe, la palette `Ctrl+K`, un plan
du cours qui regroupe TP et démos. Et un **affichage confortable** qui masque le code
AsciiDoc si vous préférez ne pas le voir.

</td>
<td valign="top">

### 🛟 Votre travail est protégé
Polaris garde une **copie de secours** sur votre poste et vous la propose si l'application
s'est arrêtée sans prévenir. Une publication qui échoue faute de réseau garde votre travail
enregistré.

</td>
</tr>
<tr>
<td valign="top">

### 📊 Prendre du recul sur son cours
Le **diagnostic du cours** et la frise du **rythme** montrent d'un coup d'œil l'équilibre
entre théorie, démonstrations et travaux pratiques.

</td>
<td valign="top">

### ♿ Pensé pour le confort de chacun
Taille du texte, interligne, espacement des lettres et des mots, taille de l'interface, correcteur orthographique
**local**, souligné en bleu et jamais en rouge. Tout se fait aussi **au clavier**.

</td>
</tr>
</table>

---

## 📦 Installer

Prenez le fichier qui correspond à votre poste dans la section **Assets** de la
[dernière version](../../releases/latest).

| Votre poste | Le fichier à prendre |
|---|---|
| 🪟 **Windows 11** | `Polaris.IDE_x.y.z_x64-setup.exe` (ou le `.msi` si votre service informatique déploie par MSI) |
| 🍎 **macOS**, puce Apple Silicon (M1 et suivantes) | `Polaris.IDE_x.y.z_aarch64.dmg` |
| 🐧 **Linux** | `Polaris.IDE_x.y.z_amd64.AppImage` |

<details>
<summary><b>🪟 Windows : « Éditeur inconnu »</b></summary>

<br>

L'installation se fait **pour votre compte utilisateur seulement** : ni droits
administrateur, ni mot de passe à demander. Les mises à jour non plus.

Windows affiche **« Éditeur inconnu »** : c'est normal, Polaris n'est pas encore signé par un
certificat de l'école. Cliquez sur **Informations complémentaires**, puis sur **Exécuter
quand même**. L'avertissement disparaîtra le jour où l'ENI fournira un certificat.

</details>

<details>
<summary><b>🍎 macOS : l'autoriser une fois</b></summary>

<br>

Les Mac Intel ne sont pas pris en charge.

La première fois, macOS refuse d'ouvrir l'application (« son développeur n'a pas pu être
vérifié »). Allez dans **Réglages Système → Confidentialité et sécurité**, descendez jusqu'au
message concernant Polaris IDE et cliquez sur **Ouvrir quand même**. Une seule fois suffit.

Si vous lisez à la place « **Polaris IDE est endommagé et ne peut pas être ouvert** »,
ouvrez le Terminal et lancez :

```sh
xattr -cr "/Applications/Polaris IDE.app"
```

</details>

<details>
<summary><b>🐧 Linux : AppImage, ou paquet système</b></summary>

<br>

L'AppImage fonctionne sur toutes les distributions, sans installation :

```sh
chmod +x Polaris.IDE_x.y.z_amd64.AppImage
./Polaris.IDE_x.y.z_amd64.AppImage
```

> [!WARNING]
> **Installé par `.deb` ou `.rpm`, Polaris ne peut pas se mettre à jour tout seul.** Il vous
> le dira et vous proposera d'ouvrir la page des versions pour prendre la nouvelle à la main.
> L'AppImage, elle, se met à jour toute seule.

</details>

### Ce qu'il faut sur le poste

- 🌐 **Une connexion internet.** L'aperçu charge la charte graphique ENI en ligne. Sans
  réseau, vous pouvez écrire, mais l'aperçu s'affiche sans les couleurs ni la mise en page
  ENI.
- 🔑 **Git pour Windows, si vous publiez votre travail.** Polaris embarque tout ce qu'il faut
  pour fonctionner, mais il réutilise le gestionnaire d'identifiants installé avec Git pour
  se connecter à GitHub.
- 🪟 **Windows 11 de préférence.** Polaris a besoin de WebView2, présent d'origine sur
  Windows 11.

> [!NOTE]
> Polaris ne stocke **aucun mot de passe** et n'a **aucun serveur** : tout se passe entre
> votre poste, GitHub et le dépôt de votre cours.

---

## 🔄 Les mises à jour

Polaris vérifie s'il existe une nouvelle version quelques secondes après son démarrage, puis
une fois par jour. Quand il en trouve une, un bandeau discret apparaît en bas de la fenêtre,
avec la liste des nouveautés.

> [!IMPORTANT]
> **Rien ne s'installe sans votre accord.**
> - Vous cliquez sur **Installer et redémarrer** quand *vous* le décidez, jamais en pleine
>   séance.
> - **Plus tard** ne la repropose plus. Vous la retrouvez quand vous voulez dans
>   **Réglages** : un point orange apparaît sur la roue crantée.
> - L'installation est refusée tant que votre fichier n'est pas enregistré, puisque Polaris
>   redémarre.

Pour savoir ce qu'apporte la version que vous avez déjà, survolez le **numéro de version** en
bas à droite de la fenêtre, ou atteignez-le au clavier.

---

## 🆘 Un problème ?

1. 📖 **Le [guide du formateur](guide-formateur.md)** répond à la plupart des questions. Sa
   dernière partie, « Quand ça coince », part des symptômes.
2. 💬 **Sinon, signalez-le depuis Polaris** : menu **Réglages → Signaler un problème**. Le
   numéro de version et votre système sont joints pour vous. Vous pouvez aussi vous adresser
   à l'équipe qui vous a transmis Polaris.

---

<div align="center">
<sub>

Ce dépôt ne contient que les installateurs, pas de code source.<br>
Polaris IDE est un logiciel propriétaire d'ENI Ecole Informatique, **gratuit à utiliser** :
voir la [LICENCE](LICENCE).<br>
Il s'appuie sur des composants open source, listés dans [TIERS.md](TIERS.md).

</sub>
</div>
