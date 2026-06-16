---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Magento Web API] de [!UICONTROL Services] &gt ; de l’administrateur Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![Paramètres ](./assets/web-api-soap-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Affichage de la boutique | Détermine le jeu de caractères par défaut. Si vide, UTF-8 est utilisé. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![ Limites d’entrée GraphQl ](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Affichage de la boutique | Détermine si les limites d’entrée sont activées pour les appels GraphQL. Valeur par défaut : `No`. |
| [!UICONTROL Maximum Page Size] | Affichage de la boutique | Définit le nombre maximal d’éléments autorisés dans un résultat de recherche paginé dans la réponse GraphQL. Cette option n’est pas disponible lorsque _Activer les limites d’entrée_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![ Limites D’Entrée De L’Api Web ](./assets/web-api-input-limits.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Affichage de la boutique | Détermine si les limites d’entrée sont activées pour les appels API Web. Valeur par défaut : `No`. |
| Limite de la liste d’entrée | Affichage de la boutique | Définit le nombre maximal d’éléments autorisés dans une propriété de tableau d’entités dans la requête API Web. Cette option n’est pas disponible lorsque _Activer les limites d’entrée_ = `No`. |
| [!UICONTROL Maximum Page Size] | Affichage de la boutique | Définit le nombre maximal d’éléments autorisés dans un résultat de recherche paginé dans la réponse de l’API Web. Cette option n’est pas disponible lorsque _Activer les limites d’entrée_ = `No`. |
| [!UICONTROL Default Page Size] | Affichage de la boutique | Définit le nombre d’éléments par défaut dans un résultat de recherche paginé dans la réponse de l’API Web. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Sécurité des API web](./assets/web-api-security.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Détermine si les invités peuvent accéder anonymement à CMS, au catalogue et stocker des ressources à partir des API SOAP et REST. Par défaut, l’accès anonyme des invités n’est pas autorisé. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![ Authentification JWT ](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Indique le type d’algorithme JWS ou JWE utilisé pour le chiffrement JWT (JSON Web Token) |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Indique le type d’algorithme de chiffrement du contenu utilisé pour le chiffrement JWT lorsque l’algorithme JWE est sélectionné. Cette option est ignorée pour les algorithmes JWS. |
| [!UICONTROL Customer JWT Expires In] | Global | Définit la durée (en minutes) avant l’expiration d’un jeton du porteur JWT client. Le jeton du porteur JWT client expire dans 30 minutes si ce champ est vide ou a une valeur négative. Valeur par défaut : `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Définit la durée (en minutes) avant l’expiration du jeton du porteur JWT d’administration. Le jeton du porteur JWT administrateur expire dans 30 minutes si ce champ est vide ou a une valeur négative. Valeur par défaut : `60` |

{style="table-layout:auto"}
