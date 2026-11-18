# HomeGadgets Price Now : téléchargements

[English](README.md)

Ce dépôt contient les programmes d'installation de HomeGadgets Price Now,
l'application de bureau de HomeGadgets, et rien d'autre. Il ne contient aucun
code source. Chaque version publiée comprend le programme, sa somme de contrôle
et un petit fichier `latest.json` qui la décrit.

## Ce que fait l'application

HomeGadgets compare les prix des détaillants canadiens pour l'électronique et
les électroménagers. Price Now cherche dans ce catalogue et peut vérifier le
prix d'un produit en direct, depuis votre propre ordinateur, au moment où vous
le demandez. Pour en savoir plus : <https://www.homegadgets.ca/fr/apps>

## Installation

**Windows (64 bits), la version publiée :**
<https://github.com/madriz/homegadgets-downloads/releases/latest/download/HomeGadgets-windows-x64-setup.exe>

Cette adresse donne toujours la version publiée la plus récente. Quand aucune
version n'est publiée, elle répond « introuvable » ; c'est voulu, ce n'est pas
un lien brisé.

Les versions marquées **Pre-release** sur la
[page des versions](https://github.com/madriz/homegadgets-downloads/releases)
sont des versions d'essai. Elles servent à tester avant la publication et
peuvent mal fonctionner.

1. Téléchargez `HomeGadgets-windows-x64-setup.exe`.
2. Vérifiez-le (facultatif) : chaque version indique son SHA-256. Dans
   PowerShell,
   `Get-FileHash .\HomeGadgets-windows-x64-setup.exe -Algorithm SHA256` doit
   afficher la même valeur.
3. Lancez-le. Le programme d'installation n'est pas signé avec un certificat de
   développeur payant ; Windows affiche donc « Windows a protégé votre
   ordinateur » la première fois. Choisissez **Informations complémentaires**,
   puis **Exécuter quand même**.

Pour mettre à jour, installez la nouvelle version par-dessus l'ancienne. Pour
la désinstaller : **Paramètres > Applications > Applications installées >
HomeGadgets > Désinstaller**.

## Configuration requise

* Windows 10 ou Windows 11, 64 bits.
* Microsoft Edge WebView2, déjà présent dans Windows 11. S'il manque, le
  programme d'installation le télécharge ; la première installation demande
  donc une connexion Internet.
* De la place pour le programme d'installation, d'environ 90 Mo.
* Une connexion Internet chaque fois que vous utilisez l'application.

Il n'existe aucune version pour Mac ni pour Linux.

## Chaque version cesse de fonctionner à une date fixe

Une version cesse de fonctionner à 0 h, heure locale de votre ordinateur, le
**premier dimanche du mois qui suit le mois où elle a été construite**, et vous
demande alors de télécharger la nouvelle. Une version construite en novembre
2026 cesse de fonctionner le dimanche 6 décembre 2026. La date figure dans les
notes de chaque version et dans `latest.json` (`expires`). Une nouvelle version
est publiée ici avant cette date ; il suffit de l'installer.

Le serveur de HomeGadgets applique la même date au flux de prix (un jour plus
tard, pour qu'aucun fuseau horaire ne soit coupé trop tôt), et HomeGadgets peut
désactiver l'application en tout temps.

## Limites

* C'est un logiciel à ses débuts (une version bêta), fourni tel quel.
* Windows seulement.
* Les vérifications en direct sont limitées à 50 par jour. Les recherches dans
  le catalogue sont limitées à 100 par jour pour chaque installation, puis par
  adresse et au total sur notre serveur.
* Une vérification en direct lit la page du détaillant lui-même. Certains
  détaillants refusent les lectures automatisées ou modifient leurs pages ; la
  vérification échoue alors ou ne trouve rien.
* Un prix du catalogue est un prix que nous avons relevé plus tôt, affiché avec
  sa date. Tout prix peut différer de celui que le détaillant demande au moment
  de payer. Les taxes, la livraison, l'installation et les frais ne sont pas
  inclus, sauf si l'application le précise. La disponibilité n'est pas
  garantie.
* Changer la date de votre ordinateur ne garde pas une version expirée en
  fonction.

## Ce que l'application envoie

Au serveur de HomeGadgets (`mcp.homegadgets.ca`), avec chaque requête :

* ce que vous avez tapé dans la recherche, ou le produit visé par une
  vérification en direct ;
* un identifiant d'installation aléatoire, créé sur votre ordinateur au premier
  lancement ;
* la version de l'application, sa date de construction, un identifiant de
  l'application (ce n'est pas un mot de passe ; il sert seulement à compter les
  recherches de l'application dans sa propre allocation) et le nom de
  l'application.

Il n'y a aucun compte. L'application n'envoie ni nom, ni adresse courriel, ni
emplacement, ni historique de navigation, et la langue que vous choisissez
reste sur votre ordinateur.

Une vérification en direct communique directement avec le site du détaillant,
depuis votre ordinateur et votre connexion Internet, comme le ferait votre
navigateur. Ce détaillant voit votre adresse IP, comme pour toute visite.

## Amazon et liens d'affiliation

Le bouton Amazon n'ouvre jamais Amazon directement : il ouvre la page du
produit sur homegadgets.ca, à sa section Amazon. En tant que Partenaire Amazon,
je réalise un bénéfice sur les achats remplissant les conditions requises. Cela
n'a aucune incidence sur ce que vous payez.

D'autres liens vers des détaillants sont des liens d'affiliation, et
HomeGadgets peut toucher une commission si vous achetez. Cela ne vous coûte
rien de plus et ne change jamais le prix affiché ni l'ordre : le classement se
fait uniquement selon le prix.

## Utilisation à vos risques, aucune garantie

Vous utilisez l'application à vos propres risques. Elle est fournie telle
quelle et selon sa disponibilité, sans garantie d'aucune sorte. Le prix et les
conditions affichés sur la page du détaillant sont ceux qui comptent ;
vérifiez-les avant d'acheter. HomeGadgets ne vend rien et n'est partie à aucun
achat. Les conditions complètes sont dans [TERMS.fr.md](TERMS.fr.md) et
la licence est dans [LICENSE.fr.md](LICENSE.fr.md).

HomeGadgets est indépendant et n'est affilié à aucun détaillant ni fabricant,
ni approuvé par eux.

## Nous joindre

Utilisez le formulaire de contact : <https://www.homegadgets.ca/fr/contact>.
