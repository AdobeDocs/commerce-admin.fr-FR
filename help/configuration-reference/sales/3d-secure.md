---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL 3D Secure] de [!UICONTROL Sales] &gt ; de l’administrateur Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
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
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] a été développé par [!DNL Visa] pour promouvoir des transactions en ligne sécurisées. Des exemples de solutions [!DNL 3-D Secure] créées par des réseaux de cartes sont vérifiées par [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] et [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] est un leader mondial de l&#39;authentification des transactions numériques et une filiale à part entière de [!DNL Visa].

La version 2.0 d’[!DNL 3-D Secure] prend en charge de nombreuses améliorations, notamment des méthodes d’authentification et un flux d’authentification avancés, ainsi qu’un partage de données amélioré entre le commerçant et l’émetteur.

>[!NOTE]
>
>La passerelle de paiement [&#128279;](../../stores-purchase/braintree.md) prend également en charge la vérification [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Environment] | Site internet | Indique le mode de fonctionnement de votre compte [!DNL CardinalCommerce]. Si vous exécutez dans un environnement de test, choisissez « Sandbox ». Options : Sandbox / Production (Par Défaut) |
| [!UICONTROL Org Unit ID] | Site internet | ID d’unité d’organisation de votre compte marchand [!DNL CardinalCommerce]. |
| [!UICONTROL API Key] | Site internet | Clé API de votre compte marchand [!DNL CardinalCommerce]. |
| [!UICONTROL API Identifier] | Site internet | Identifiant d’API de votre compte marchand [!DNL CardinalCommerce]. |
| [!UICONTROL Debug] | Site internet | Options : `Yes` / `No` |

{style="table-layout:auto"}
