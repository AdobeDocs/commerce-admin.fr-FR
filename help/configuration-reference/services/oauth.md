---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Services] &gt; [!UICONTROL OAuth] de l’administrateur Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Expiration du jeton d’accès](./assets/oauth-token-expire.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Détermine le temps en heures avant l’expiration d’un jeton API client. Le jeton client n’expire jamais si le champ est vide. Valeur par défaut : `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Détermine le temps en heures avant l’expiration d’un jeton API d’administration. Le jeton d’administration n’expire jamais si le champ est vide. Valeur par défaut : `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>Les algorithmes de durée de vie et de chiffrement du jeton de l’API propriétaire et administrateur sont contrôlés par les paramètres de configuration [Authentification JWT](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![Paramètres de nettoyage](./assets/oauth-cleanup.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Indique le nombre de requêtes OAuth avant le lancement du nettoyage. Ne saisissez pas `0` pour désactiver le nettoyage. |
| [!UICONTROL Enable WSDL Cache] | Global | Détermine l’âge des entrées en minutes avant leur nettoyage. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Paramètres du client](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Indique le nombre de secondes nécessaire au système pour que le délai d’expiration de la publication des informations d’identification par les clients soit écoulé. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Indique le nombre maximal de redirections liées à une publication des informations d’identification des consommateurs. |
| [!UICONTROL Expiration Period] | Global | Détermine le nombre de secondes avant l’expiration d’une clé/d’un secret inutilisé après le début de l’exchange du jeton OAuth. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Verrouillage d’authentification](./assets/oauth-locks.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Indique le Nombre maximal d’échecs d’authentification à verrouiller sur un compte. |
| [!UICONTROL Lockout Time (seconds)] | Global | Indique la période en secondes au-delà de laquelle le compte est déverrouillé. |

{style="table-layout:auto"}
