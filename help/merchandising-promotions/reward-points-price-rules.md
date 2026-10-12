---
title: Points de récompense dans les règles de prix
description: Découvrez comment attribuer des points de récompense aux clients selon une règle de prix de panier.
exl-id: 6e23b56d-64e4-435d-9f4c-ee3f400b0250
feature: Rewards, Promotions/Events, Customers
TQID: 'https://experienceleague.adobe.com/amQYBXl5evC-BUqmb5SyGR97iOAMIPv5UxqCFfOkGmQ'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4069cee6-4dc8-5a83-81de-232af6a7c9e9
    internal-label: Rewards
  - id: 19d9b313-1a3c-5bed-9da7-4364f71c3a28
    internal-label: Promotions/Events
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%
---
# Points de récompense dans les règles de prix

{{ee-feature}}

Des points de récompense peuvent être attribués aux clients selon une [ règle de prix de panier ](price-rules-cart.md). L’attribution de points peut être la seule action de la règle de prix ou peut être utilisée avec une remise.

>[!NOTE]
>
>La configuration [Taux de change de récompense](reward-exchange-rates.md) est requise pour l’échange de points de récompense par les clients et les utilisateurs administrateurs lors du passage en caisse.

## Ajouter des points de récompense à une règle de prix

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Cliquez sur **[!UICONTROL Add New Rule]** pour créer une règle de prix de panier ou cliquez sur une règle de prix de panier existante pour l’ouvrir.

1. Faites défiler vers le bas, développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Actions]**, définissez les conditions et saisissez le nombre de points dans le champ **[!UICONTROL Add Reward Points]**.

   ![Règle de prix du panier - Points de récompense](./assets/reward-points-price-rule-actions.png){width="600" zoomable="yes"}

1. Suivez les instructions standard pour terminer la [règle de prix de panier](price-rules-cart-create.md).

   Lorsque la règle de prix est activée, un message s’affiche dans le panier pour informer les clients du nombre de points qu’ils peuvent gagner en passant la commande. Cela s’applique uniquement aux utilisateurs enregistrés et peut varier lorsqu’un utilisateur est connecté.
