# Polaris IDE

**L'éditeur de cours de l'ENI.** Vous écrivez votre cours, Polaris vous montre les slides
telles que les verront vos apprenants, vérifie le formalisme ENI au fil de la frappe, et
publie votre travail sur GitHub sans que vous ayez à connaître Git.

Ce dépôt ne contient **que les installateurs**. Il n'y a pas de code source ici.

➡️ **[Télécharger la dernière version](../../releases/latest)**

---

## Installer

Prenez le fichier qui correspond à votre poste dans la section **Assets** de la
[dernière version](../../releases/latest).

### Windows

| Fichier | Quand le choisir |
|---|---|
| `Polaris IDE_x.y.z_x64-setup.exe` | **le cas normal** — c'est celui à prendre |
| `Polaris IDE_x.y.z_x64_en-US.msi` | si votre service informatique déploie par MSI |

L'installation se fait **pour votre compte utilisateur seulement** : ni droits
administrateur, ni mot de passe à demander. Les mises à jour ultérieures non plus.

> **Windows va afficher « Éditeur inconnu ».** C'est normal : Polaris n'est pas encore signé
> par un certificat de l'école. Cliquez sur **Informations complémentaires** puis
> **Exécuter quand même**. Cet avertissement disparaîtra le jour où l'ENI fournira un
> certificat.

### macOS

Prenez le fichier `.dmg`. **Puces Apple Silicon uniquement** (M1 et suivantes) — les Mac Intel
ne sont pas pris en charge.

> **macOS refusera d'ouvrir l'application la première fois**, avec un message du genre
> « Polaris IDE ne peut pas être ouvert car son développeur n'a pas pu être vérifié ».
> Allez dans **Réglages Système → Confidentialité et sécurité**, descendez jusqu'au message
> concernant Polaris IDE, et cliquez sur **Ouvrir quand même**. Une seule fois.
>
> Si à la place vous lisez « **Polaris IDE est endommagé et ne peut pas être ouvert** »,
> ouvrez le Terminal et lancez :
>
> ```
> xattr -cr "/Applications/Polaris IDE.app"
> ```

### Linux

Prenez l'**AppImage** : elle fonctionne sur toutes les distributions, sans installation.
Rendez-la exécutable, puis lancez-la :

```
chmod +x Polaris_IDE_x.y.z_amd64.AppImage
./Polaris_IDE_x.y.z_amd64.AppImage
```

> ⚠️ **Si vous installez par `.deb` ou `.rpm`, la mise à jour automatique ne fonctionnera
> pas.** Polaris vous le dira, et vous proposera d'ouvrir la page des versions pour prendre
> la nouvelle à la main. L'AppImage, elle, se met à jour toute seule.

---

## Ce qu'il faut sur le poste

- **Une connexion internet.** L'aperçu du cours charge la charte graphique ENI en ligne. Sans
  réseau, Polaris fonctionne et vous pouvez écrire, mais l'aperçu s'affiche sans les couleurs
  et la mise en page ENI.
- **Git pour Windows**, si vous publiez votre travail. Polaris n'a pas besoin de Git pour
  fonctionner — il embarque tout ce qu'il faut — mais il réutilise le gestionnaire
  d'identifiants installé avec Git pour se connecter à GitHub. C'est le même que celui qui
  vous authentifie déjà en ligne de commande.
- **Windows 11** de préférence. Polaris a besoin de WebView2, présent d'origine sur Windows 11.

Polaris ne stocke **aucun mot de passe** et n'a **aucun serveur** : tout se passe entre votre
poste, GitHub, et le dépôt de votre cours.

---

## Les mises à jour

Polaris vérifie s'il existe une nouvelle version quelques secondes après son démarrage, puis
une fois par jour. Quand il en trouve une, un bandeau discret apparaît en bas de la fenêtre
avec la liste des nouveautés.

**Rien ne s'installe sans votre accord.** Trois règles :

- vous cliquez sur **Installer et redémarrer** quand *vous* le décidez — jamais en pleine
  séance ;
- si vous cliquez sur **Plus tard**, la version n'est plus reproposée. Vous la retrouvez
  quand vous voulez dans **Réglages** (un point orange apparaît sur la roue crantée) ;
- l'installation est refusée tant que votre fichier n'est pas enregistré, puisque Polaris
  redémarre.

Pour savoir ce qu'apporte la version que vous avez déjà : survolez le **numéro de version**
en bas à droite de la fenêtre.

---

## Un problème ?

- **Le guide d'utilisation** répond à la plupart des questions :
  [guide-formateur.md](guide-formateur.md).
- Sinon, signalez-le à l'équipe qui vous a transmis Polaris, avec **le numéro de version**
  (en bas à droite de la fenêtre) et ce que vous faisiez.
