---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL OAuth] de [!UICONTROL Services] &gt ; de l’administrateur Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![&#x200B; Expiration du jeton d’accès &#x200B;](./assets/oauth-token-expire.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Détermine la durée, en heures, avant l’expiration d’un jeton API client. Le jeton client n’expire jamais si le champ est vide. Valeur par défaut : `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Détermine la durée, en heures, avant l’expiration d’un jeton API d’administration. Le jeton d’administration n’expire jamais si le champ est vide. Valeur par défaut : `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>La durée de vie et les algorithmes de chiffrement du jeton API du porteur et de l’administrateur sont contrôlés par les paramètres de configuration [Authentification JWT](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![Paramètres de nettoyage](./assets/oauth-cleanup.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Indique le nombre de requêtes OAuth avant le lancement du nettoyage. Ne saisissez pas de `0` pour désactiver le nettoyage. |
| [!UICONTROL Enable WSDL Cache] | Global | Détermine l’âge des entrées, en minutes, avant leur nettoyage. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Paramètres du client](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Indique le nombre de secondes nécessaires au système pour expirer lorsque les clients publient leurs informations d’identification. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Spécifie le nombre maximal de redirections associées à une validation des informations d&#39;identification du client. |
| [!UICONTROL Expiration Period] | Global | Détermine le nombre de secondes avant l’expiration d’une clé/d’un secret inutilisé après le début de l’échange de jetons OAuth. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Verrous d’authentification](./assets/oauth-locks.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Indique le nombre maximal d’échecs d’authentification pour verrouiller le compte. |
| [!UICONTROL Lockout Time (seconds)] | Global | Indique la période en secondes au bout de laquelle le compte est déverrouillé. |

{style="table-layout:auto"}
