# Polaris IDE

Éditeur AsciiDoc pour les cours ENI. Il permet d'écrire un cours, d'en voir le rendu
en direct au formalisme ENI, et de le publier sur GitHub sans quitter l'application.

> **Ce dépôt ne contient pas de code source.** Il héberge uniquement les fichiers
> d'installation et le manifeste utilisé par la mise à jour automatique. Le code de
> l'application vit dans un dépôt interne ENI.

## Télécharger

**→ [Dernière version](../../releases/latest)**

| Système | Fichier à prendre |
|---------|-------------------|
| Windows | `Polaris.IDE_x.y.z_x64-setup.exe` |
| macOS (Apple Silicon) | `Polaris.IDE_x.y.z_aarch64.dmg` |
| Linux | `Polaris.IDE_x.y.z_amd64.AppImage` |

Les fichiers `.sig` à côté ne s'installent pas : ce sont les signatures que
l'application vérifie avant d'appliquer une mise à jour.

⚠️ Dans la liste des versions, ne prenez que celle marquée **Latest**. Une version
marquée **Pre-release** est en cours de validation et n'est pas destinée à être
installée.

## Windows

Prenez le **`-setup.exe`**, pas le `.msi` : c'est le format utilisé par les mises à
jour automatiques, et mélanger les deux crée deux installations distinctes.

**Windows affichera un avertissement** au lancement : « Windows a protégé votre
ordinateur — Éditeur : Inconnu ». C'est attendu. Il ne s'agit pas d'une détection de
virus mais d'un contrôle de réputation : l'application n'est pas accompagnée d'un
certificat d'éditeur commercial. Pour continuer :

1. cliquez sur **Informations complémentaires** ;
2. puis sur **Exécuter quand même**.

Cet avertissement n'apparaît **qu'à la première installation**. Les mises à jour
suivantes se font sans aucune alerte.

L'installation se fait dans votre profil utilisateur : elle ne demande pas de droits
administrateur.

## macOS

Uniquement pour les Mac **Apple Silicon** (M1 et suivants). Les Mac Intel ne sont pas
pris en charge.

L'application n'étant pas notariée auprès d'Apple, macOS refusera de l'ouvrir au
premier lancement. Faites un **clic droit sur l'application → Ouvrir**, puis
confirmez : le système mémorise ensuite votre choix.

## Linux

L'**AppImage** est le format recommandé : c'est le seul qui reçoive les mises à jour
automatiques. Rendez-le exécutable avant de le lancer :

```bash
chmod +x Polaris.IDE_*.AppImage
./Polaris.IDE_*.AppImage
```

Les paquets `.deb` et `.rpm` sont également fournis, mais ils devront être mis à jour
manuellement.

## Mises à jour

Polaris IDE vérifie s'il existe une nouvelle version au démarrage, puis une fois par
jour. Quand une version est disponible, un bandeau discret apparaît en bas de la
fenêtre.

Trois choses à savoir :

- **rien ne s'installe sans votre accord** — vous choisissez le moment, et vous
  pouvez reporter ;
- une version reportée **n'est plus reproposée** ; seule la suivante le sera ;
- l'installation est **refusée tant qu'un fichier n'est pas enregistré**, car
  l'application redémarre à la fin.

Si votre poste n'a pas accès à Internet, Polaris fonctionne normalement : la
vérification échoue en silence.

## Signaler un problème

Passez par les canaux internes ENI. Précisez le **numéro de version**, affiché en
permanence en bas à droite de la fenêtre — c'est l'information la plus utile pour
comprendre ce qui se passe sur votre poste.
