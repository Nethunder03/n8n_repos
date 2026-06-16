---
title: Attackers Exploit Three Fortinet FortiSandbox Flaws, One Patched Last Week
description: Trois failles de sécurité majeures, dont la CVE-2026-39813 (score CVSS 9.1), affectent actuellement le produit FortiSandbox de Fortinet. Les attaquants les exploitent activement. Découvrez l'analyse et nos recommandations d'urgence.
date: "2026-06-16T16:00:18.341+00:00"
tags: fortinet,fortisandbox,vulnerabilite,cybersecurite,cve-2026-39813
sources: https://thehackernews.com/2026/06/attackers-exploit-three-fortinet.html
draft: false
---
# Alerte Critique : Fortinet FortiSandbox sous le feu d'exploitations actives

La sécurité des environnements d'analyse de fichiers est aujourd'hui gravement menacée. Selon les récentes informations partagées par la firme de renseignement sur les menaces **Defused Cyber**, plusieurs acteurs malveillants exploitent activement trois vulnérabilités de sécurité critiques au sein de la solution **Fortinet FortiSandbox**. Ces attaques, détectées en conditions réelles, mettent en péril l'intégrité des systèmes de détection des entreprises.

La plus critique de ces failles, enregistrée sous la référence **CVE-2026-39813**, affiche un score de gravité CVSS de **9.1**, ce qui la classe parmi les menaces extrêmement urgentes à traiter.

## Zoom sur les vulnérabilités exploitées

Les attaquants exploitent actuellement une chaîne de vulnérabilités pour compromettre l'outil d'analyse de Fortinet. Les trois failles identifiées par les chercheurs sont :

*   **CVE-2026-39813 (CVSS 9.1)** : Une vulnérabilité de type traversée de chemin (*path traversal*) localisée au niveau de l'API JRPC de FortiSandbox.
*   **CVE-2026-39808** et **CVE-2026-25089** : Deux autres failles de sécurité complémentaires qui facilitent les opérations malveillantes une fois combinées ou utilisées individuellement.

La faille principale, la CVE-2026-39813, permet à un attaquant distant d'envoyer des requêtes forgées à l'API JRPC afin d'accéder à des fichiers et des répertoires sensibles en dehors de la racine Web normalement autorisée. Dans le pire des cas, cela peut mener à la fuite de secrets d'authentification ou à des compromissions plus profondes du système d'exploitation de la sandbox.

## Quel est l'impact pour votre entreprise ?

Une sandbox comme FortiSandbox est un pilier de la stratégie de défense en profondeur. Elle sert à exécuter et analyser des fichiers suspects (courriels, téléchargements) dans un environnement isolé pour détecter d'éventuels comportements malveillants avant qu'ils n'atteignent le réseau de production.

Si un attaquant parvient à compromettre la sandbox elle-même :

1.  Il peut potentiellement s'évader de l'environnement d'analyse pour cibler le réseau interne de l'entreprise.
2.  Il peut obtenir des informations cruciales sur les mécanismes de détection en place afin d'adapter ses futurs malwares pour qu'ils restent indétectables.
3.  Il peut perturber l'analyse des menaces en temps réel, laissant passer d'autres attaques furtives.

L'indice de fiabilité de cette alerte est estimé à **95/100**, ce qui confirme le caractère hautement probable et imminent de la menace pour les organisations n'ayant pas encore sécurisé leur infrastructure.

## Recommandations et mesures d'atténuation immédiates

Face à cette campagne d'exploitation active, les équipes de sécurité et les administrateurs système doivent réagir sans délai. Voici les mesures correctives indispensables à appliquer :

*   **Mettre à jour immédiatement** : Appliquez les derniers correctifs publiés par Fortinet pour FortiSandbox afin de neutraliser ces failles.
*   **Restreindre l'exposition réseau de l'API JRPC** : L'API JRPC ne doit en aucun cas être accessible depuis l'Internet public. Utilisez des règles de pare-feu strictes et des listes d'accès (ACL) pour limiter les connexions aux seuls systèmes d'administration légitimes.
*   **Surveiller activement les logs** : Analysez les journaux de connexion et de requêtes de votre API JRPC. Recherchez des indicateurs de traversée de chemin, tels que des requêtes contenant des séquences de caractères suspectes (par exemple, `../` ou d'autres motifs d'encodage alternatifs).

Pour en savoir plus sur les détails de cette campagne d'exploitation, vous pouvez consulter l'article d'origine sur [The Hacker News](https://thehackernews.com/2026/06/attackers-exploit-three-fortinet.html).