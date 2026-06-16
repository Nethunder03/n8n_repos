---
title: New Rokarolla Android Malware Steals PINs, SMS Codes, and Crypto Wallet Funds
description: Découvrez Rokarolla, le nouveau cheval de Troie Android ciblant 217 applications de finance et crypto. Nos conseils d'experts pour protéger vos données.
date: "2026-06-16T16:49:52.399+00:00"
tags: Android,Malware,Rokarolla,Cybersécurité,Zimperium
sources: https://thehackernews.com/2026/06/new-rokarolla-android-malware-steals.html
draft: false
---
Le paysage des menaces mobiles sur Android s'assombrit à nouveau avec la découverte d'un logiciel malveillant particulièrement sophistiqué. Les chercheurs en sécurité de la cellule zLabs de **Zimperium** ont récemment mis au jour un nouveau cheval de Troie bancaire baptisé **Rokarolla**. Ce malware redoutable se distingue par un arsenal de fonctionnalités offensives hors norme, visant à dévaliser les comptes bancaires et les portefeuilles de cryptomonnaies de ses victimes.

Avec une capacité de ciblage étendue et un contrôle quasi-absolu sur les appareils infectés, Rokarolla s'impose déjà comme une menace de premier plan pour la sécurité des terminaux mobiles.

---

## Qu'est-ce que le malware Rokarolla ?

Rokarolla est un cheval de Troie (Trojan) spécifiquement conçu pour le système d'exploitation Android. Contrairement à des malwares plus génériques, Rokarolla est ultra-spécialisé dans la fraude financière. Selon l'analyse publiée par les équipes de Zimperium, ce programme malveillant cible de manière très précise **217 applications bancaires et de cryptomonnaies** à travers le monde.

Pour parvenir à ses fins, les opérateurs derrière Rokarolla disposent d'un serveur de commande et de contrôle (C2) capable d'envoyer pas moins de **137 commandes distantes** distinctes à l'appareil infecté. Cette polyvalence offre aux cybercriminels un contrôle presque illimité sur le smartphone de leur victime, transformant l'appareil en un outil d'espionnage et de vol automatisé.

---

## Analyse technique : Un arsenal redoutable

La dangerosité de Rokarolla réside dans sa capacité à contourner les mécanismes de sécurité traditionnels d'Android et à abuser des fonctionnalités légitimes du système.

### 1. Interception des codes PIN et verrouillages d'écran
L'une des fonctionnalités les plus préoccupantes de Rokarolla est sa capacité à récupérer le code PIN, le schéma ou le mot de passe de déverrouillage de l'appareil. En enregistrant les saisies de l'utilisateur ou en superposant de fausses fenêtres d'authentification (attaques par overlay), le troyen subtilise ces précieuses informations, facilitant un accès physique ou logique ultérieur.

### 2. Lecture et envoi de SMS (Contournement de la 2FA)
Pour valider des transactions frauduleuses, les banques s'appuient encore massivement sur l'envoi de codes de validation par SMS (Authentification à Double Facteur ou 2FA). Rokarolla résout ce problème pour les attaquants en s'octroyant les permissions de lecture et d'envoi de SMS. Les cybercriminels peuvent ainsi intercepter les codes de validation à l'insu de la victime et valider des virements bancaires non autorisés.

### 3. Détournement du presse-papier (Clipboard Hijacking)
Le vol de cryptomonnaies s'effectue de manière extrêmement subtile. Rokarolla surveille en permanence le presse-papier d'Android. Lorsqu'il détecte qu'une adresse de portefeuille crypto (Bitcoin, Ethereum, etc.) a été copiée, il la remplace instantanément par une adresse appartenant aux attaquants. Au moment où la victime colle l'adresse pour effectuer un transfert, les fonds sont directement redirigés vers le portefeuille des pirates.

### 4. Désactivation de Google Play Protect
Pour assurer sa persistance et éviter d'être détecté par les outils d'analyse de Google, Rokarolla est capable de désactiver silencieusement **Google Play Protect**, la barrière de sécurité native d'Android. Privé de cette défense, l'appareil devient vulnérable à l'installation d'autres charges utiles malveillantes.

---

## Comment le malware s'infiltre-t-il ?

Le vecteur d'infection principal repose, comme souvent, sur l'ingénierie sociale et le téléchargement d'applications en dehors du Google Play Store officiel, un procédé appelé **sideloading**. Les attaquants dissimulent le troyen sous l'apparence d'applications légitimes, de mises à jour système fictives ou de lecteurs multimédias.

Une fois installée, l'application malveillante demande à l'utilisateur d'activer les **Services d'Accessibilité** d'Android. Conçus à l'origine pour aider les personnes en situation de handicap, ces services permettent à une application d'interagir avec l'écran, de lire le contenu affiché et de simuler des clics. En accordant ce privilège, l'utilisateur donne involontairement les clés du système à Rokarolla.

---

## Recommandations de sécurité pour se prémunir de Rokarolla

Face à cette menace de niveau élevé, les experts en cybersécurité recommandent d'adopter des mesures de cyberhygiène strictes, tant au niveau individuel qu'en entreprise pour la gestion des flottes mobiles (MDM) :

*   **Proscrivez le sideloading :** Ne téléchargez jamais de fichiers APK ou d'applications provenant de sources tierces ou de sites web non officiels. Restez exclusivement sur le Google Play Store.
*   **Vigilance sur les services d'accessibilité :** N'accordez jamais les autorisations relatives à l'accessibilité à des applications qui ne le justifient pas de manière évidente.
*   **Surveillez l'activité réseau et la batterie :** Une surconsommation de batterie ou des ralentissements anormaux peuvent indiquer l'activité en arrière-plan d'un logiciel malveillant communiquant avec un serveur C2.
*   **Déployez une solution MTD (Mobile Threat Defense) :** Pour les entreprises, l'intégration d'une solution de sécurité dédiée aux flottes mobiles permet de détecter en temps réel les comportements suspects et les applications malveillantes.
*   **Gardez votre système à jour :** Appliquez systématiquement les correctifs de sécurité d'Android pour corriger les vulnérabilités exploitées par ce type de troyen.

---

## Conclusion

Rokarolla illustre parfaitement la sophistication croissante des troyens bancaires sur Android. En combinant le détournement de SMS, le vol de PIN, la manipulation du presse-papier et la désactivation des protections système, il offre un contrôle total de l'appareil aux attaquants. La prudence lors de l'installation de nouvelles applications et le contrôle strict des privilèges accordés demeurent vos meilleures armes pour faire barrage à cette menace.

*Pour consulter l'analyse technique complète de Zimperium, visitez la source officielle : [The Hacker News](https://thehackernews.com/2026/06/new-rokarolla-android-malware-steals.html).*