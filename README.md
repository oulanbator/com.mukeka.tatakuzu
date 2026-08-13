# Politique de confidentialité — Tatakuzu

**Éditeur :** MUKEKA

**Application :** Tatakuzu (Android)

**Dernière mise à jour :** 13 août 2026

---

## 1. En bref

Tatakuzu est un jeu de logique **entièrement jouable hors ligne**. Il n'y a
**aucun compte à créer**, aucune inscription, aucun identifiant à fournir.

L'essentiel de ce que tu produis en jouant — progression, étoiles, succès,
séries, réglages — reste **sur ton appareil** et ne nous est jamais transmis.

Deux fonctionnalités **facultatives** font exception, parce qu'elles ont besoin
d'un serveur pour exister : le **duel entre amis** et le **classement**. Ce
document explique précisément ce qu'elles transmettent, pourquoi, où, combien de
temps, et comment le faire supprimer. Si tu n'y touches pas, **rien de tout cela
ne se produit**.

## 2. Données stockées sur ton appareil

Les informations suivantes sont enregistrées **localement** et ne nous sont
**pas** transmises :

- ta progression de jeu (niveaux terminés, étoiles, succès, séries) ;
- tes réglages (volumes audio, thème, langue, préférences de saisie) ;
- le **nom de joueur** que tu saisis (il n'est transmis que si tu joues un duel,
  voir §3) ;
- le journal de tes duels sur cet appareil.

Tu peux les effacer à tout moment depuis l'Application (Réglages →
« Réinitialiser ma progression » et « Supprimer mes données ») ou en la
désinstallant.

## 3. Duel entre amis — ce qui transite par notre serveur

Le duel te permet de défier un ami : tu joues une grille, tu lui envoies un
lien, il joue la même grille, et chacun voit le résultat de l'autre.

Le lien de défi voyage par **le moyen que tu choisis** (messagerie, e-mail…) et
ne passe pas par nous : quand c'est toi qui lances le défi, ton résultat est
dans ce lien, pas sur notre serveur.

C'est quand tu **relèves** le défi d'un ami que ton résultat est déposé sur
notre serveur, pour qu'il te revienne **sans que tu aies à lui renvoyer un
lien**. Son appareil vient l'y chercher.

**Ce qui est déposé, dans ce cas :**

| Donnée | Détail |
|---|---|
| Le **nom de joueur** que tu as saisi | Pour que ton ami sache qui a relevé son défi. C'est un pseudonyme libre : rien ne t'oblige à utiliser ton vrai nom |
| Le **résultat de la manche** | Temps, nombre de fautes, aides utilisées, étoiles obtenues |
| La **référence de la grille** jouée | Un identifiant technique de la grille du jeu |
| Un **identifiant de défi** | Un code aléatoire, créé sur l'appareil, qui sert de clé au duel |

**Finalité, et elle seule :** faire aboutir le duel que tu as lancé ou accepté.
Ces données ne servent **à aucune finalité publicitaire**, ne sont croisées avec
aucune donnée publicitaire, et ne sont transmises à personne d'autre.

**Aucun compte n'est créé pour un duel.** Un duel n'est rattaché à aucune
identité : il n'existe, sur le serveur, que le code aléatoire du défi. C'est un
choix de conception, et il a une conséquence directe sur la suppression (§6).

## 4. Classement — ce qui transite par notre serveur

Quand tu joues le **Défi quotidien**, l'Application transmet le nécessaire pour
établir ton rang :

| Donnée | Détail |
|---|---|
| Un **identifiant anonyme** | Créé par Firebase Authentication (connexion anonyme). C'est une clé technique : elle n'est rattachée à aucun e-mail, aucun compte Google, aucun numéro, et elle n'est jamais affichée ni partagée |
| Le **résultat du défi du jour** | Temps, fautes, aides, étoiles, et la date du défi |

**Finalité, et elle seule :** établir ton rang. Là encore, **aucune finalité
publicitaire**.

**Aucun pseudo n'est transmis au classement, et aucun nom n'y est affiché.** Le
classement ne montre qu'un **rang** (« 3 / 750 ») : pas de liste de joueurs, pas
de profil, pas de pseudonyme public. C'est la façon la plus simple de ne pas
publier ce dont personne n'a besoin.

## 5. Où ces données sont hébergées

Sur **Google Firebase** (Firestore), agissant comme notre sous-traitant
d'hébergement, dans une région **multi-régionale européenne** (`eur3`, Belgique
et Pays-Bas). Les données de duel et de classement sont donc **stockées dans
l'Union européenne**, et transitent **chiffrées** (HTTPS/TLS).

## 6. Durées de conservation, et suppression

### Ce que tu peux supprimer toi-même

Réglages → **« Supprimer mes données »** efface :

- le **journal de tes duels** sur cet appareil ;
- les **résultats en attente d'envoi** — donc des données qui n'ont pas encore
  quitté ton appareil, et qui ne partiront plus ;
- si tu participes au classement, tes **entrées de classement** et
  l'**identifiant anonyme** qui leur est associé.

### Ce que ce bouton ne peut pas supprimer, et pourquoi

Un résultat de duel **déjà déposé** n'est rattaché à aucune identité (§3) : il
n'existe aucun moyen, pour nous comme pour quiconque, de retrouver « les duels
d'un joueur donné ». C'est une protection — personne ne peut dresser la liste de
tes parties — et c'est aussi la raison pour laquelle ces documents ne sont pas
supprimables à la demande depuis l'Application.

Ils **s'effacent d'eux-mêmes** : chaque dépôt porte une échéance fixée à
**90 jours**, et une purge périodique supprime ceux qui l'ont dépassée.

### Durées

| Donnée | Conservation |
|---|---|
| Résultats de duel déposés | Échéance à **90 jours** après le dépôt, puis effacement par la purge périodique |
| Entrées de classement et identifiant anonyme | **12 mois** glissants, ou jusqu'à ta demande de suppression |
| Données locales (progression, réglages, journal) | Tant que l'Application est installée, ou jusqu'à ce que tu les effaces |

### Par e-mail

Pour toute demande que l'Application ne peut pas satisfaire — y compris
l'effacement d'un duel précis dont tu nous donnerais le lien — écris-nous à
**mukeka.studio@gmail.com**. Nous répondons dans le délai légal d'un mois.

## 7. Base légale (RGPD)

- **Duel et classement** : notre **intérêt légitime** à fournir la
  fonctionnalité que tu as toi-même déclenchée. Elles sont **facultatives** : le
  jeu est intégralement jouable sans jamais lancer un duel ni soumettre un défi
  du jour, et tu peux demander la suppression à tout moment (§6).
- **Publicité** : ton **consentement** lorsqu'il est requis (§8).
- **Rapports de plantage** : **intérêt légitime**, avec opt-out (§10).

⚠️ **Ces bases sont distinctes et ne se remplacent pas.** En particulier, le
consentement publicitaire (§8) **ne couvre pas** les données de duel ni de
classement : ce sont des finalités différentes, traitées séparément.

## 8. Publicité (Google AdMob) et consentement

L'Application est gratuite et financée par la publicité, fournie par **Google
AdMob**. Pour diffuser des annonces, AdMob et ses partenaires peuvent collecter
et traiter certaines données, notamment :

- l'**identifiant publicitaire** de ton appareil (Android Advertising ID) ;
- des informations techniques (type d'appareil, système d'exploitation, adresse
  IP approximative, interactions avec les annonces).

Ces données servent à afficher des publicités (personnalisées ou non, selon ton
consentement), mesurer leur performance et prévenir la fraude.

Si tu résides dans l'**Espace économique européen**, au **Royaume-Uni** ou en
**Suisse**, un **écran de consentement** (Google User Messaging Platform, UMP)
t'est présenté au premier lancement. Tu peux **modifier ton choix à tout
moment** via Réglages → « Gérer mon consentement ». Tu peux également
réinitialiser ou désactiver ton identifiant publicitaire dans les paramètres
Android (Paramètres → Confidentialité → Annonces).

- Fonctionnement et confidentialité de Google :
  https://policies.google.com/privacy
- Comment Google utilise les données de ses partenaires :
  https://policies.google.com/technologies/partner-sites

## 9. Publicités récompensées

L'Application propose des publicités **récompensées** facultatives (par exemple
pour obtenir un indice ou protéger une série). Les regarder est toujours **à ton
initiative** ; elles relèvent du même traitement AdMob décrit au §8.

## 10. Rapports de plantage et diagnostics (Firebase Crashlytics)

Pour améliorer la stabilité de l'Application, nous utilisons **Firebase
Crashlytics**, un service fourni par Google. En cas de plantage ou d'anomalie
technique, ce service peut collecter et nous transmettre des **données de
diagnostic non personnelles**, notamment :

- un **identifiant d'installation** (propre à l'installation de l'Application,
  non rattaché à ton identité) ;
- le **type d'appareil**, la **version du système d'exploitation**, la langue et
  la région ;
- l'**état technique au moment de l'incident** (rapport d'erreur /
  « stacktrace », écran en cours, difficulté, taille de grille).

Nous **ne collectons aucune donnée permettant de t'identifier** (ni e-mail, ni
nom de joueur, ni contenu de tes parties) via ce service.

Cette collecte ne s'active qu'**après ton passage par l'écran de consentement**
(§8), et uniquement si celui-ci l'autorise. Tu peux la **désactiver à tout
moment** via Réglages → « Rapports de plantage ».

- Firebase et confidentialité : https://firebase.google.com/support/privacy

## 11. Ce que nous ne faisons pas

- **Aucun analytics comportemental** : nous ne suivons pas tes actions dans le
  jeu, nous ne construisons aucun profil, aucun entonnoir de conversion.
- **Aucune vente ni location** de tes données, à personne.
- **Aucun partage** des données de duel ou de classement avec un tiers. Google
  les héberge pour notre compte (§5) ; c'est un hébergement, pas un partage.
- **Aucun classement nommé** : aucun pseudonyme n'est exposé publiquement (§4).
- **Aucun usage publicitaire** des données de jeu (§3, §4).

## 12. Enfants

L'Application convient à un large public. Elle est destinée à un public de
13 ans et plus, et ne collecte pas sciemment de données personnelles concernant
des enfants en deçà de cet âge. Les publicités diffusées sont soumises aux
règles de Google AdMob.

## 13. Tes droits

Selon ta juridiction (notamment le RGPD), tu disposes de droits d'accès, de
rectification, d'effacement, de limitation, d'opposition et de portabilité.

- Pour les données **locales** : tu les contrôles directement (§2).
- Pour les données de **duel et de classement** : voir §6.
- Pour les données traitées par **Google dans le cadre publicitaire** :
  réfère-toi aux liens du §8 et aux paramètres Android de ton appareil.
- Pour toute autre demande, ou pour introduire une réclamation :
  **mukeka.studio@gmail.com**. Tu peux également saisir l'autorité de
  protection des données de ton pays (en France, la CNIL).

## 14. Modifications

Cette politique peut être mise à jour. La date de « Dernière mise à jour » en
tête de document reflète la version en vigueur. Les changements importants
seront signalés via la fiche de l'Application sur le Google Play Store.

## 15. Contact

Pour toute question relative à cette politique ou à tes données :
**mukeka.studio@gmail.com**

