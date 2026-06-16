---
title: Activer  [!DNL Inventory Management]
description: Découvrez comment activer au niveau  [!DNL Inventory Management]  magasin global ou du produit.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Activer le [!DNL Inventory Management]

Pour gérer votre inventaire de produits, activez [!DNL Inventory Management] au niveau du magasin ou du produit. Lorsque l’option _Gérer les stocks_ est activée, [!DNL Inventory Management] effectue automatiquement le suivi des quantités de produits disponibles pour le site par le biais des stocks et des sources configurés. Chaque fonctionnalité et option commence le suivi et le compte rendu des performances lorsqu’elles sont activées, sans configuration supplémentaire.

Votre entreprise fonctionne et met à jour ses stocks à la vitesse des ventes. Lorsque les clients font leurs achats, vous recevez des informations exactes et mises à jour sur le stock disponible par canal de vente et par source. Les quantités vendables disponibles sont mises à jour par stock lorsque les clients ajoutent des produits au panier et effectuent des achats, et lorsque vous gérez des commandes, créez des livraisons et émettez des remboursements. Les arrivées de nouvelles stocks ou de stocks transférés à vos sources, immédiatement disponibles pour les ventes en ligne. Les reliquats se terminent jusqu&#39;aux seuils spécifiés sans commandes infinies ni configurations supplémentaires. Vous entrez et effectuez des livraisons partielles ou complètes à travers une ou plusieurs sources avec des recommandations, ce qui vous donne un contrôle complet sur l&#39;exécution des commandes et le stock disponible.

>[!NOTE]
>
>Par défaut, [!DNL Inventory Management] est activé lors de l’installation ou de la mise à niveau de [!DNL Commerce]. Selon les besoins de votre entreprise, vous pouvez activer ou désactiver les [!DNL Inventory Management] suivies dans [!DNL Commerce].

Fonctionnement de ce paramètre dans les inventaires à source unique et multi-sources :

- Pour utiliser [!DNL Inventory Management], activez _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] paramètres au niveau de la configuration du produit remplacent la configuration du magasin.

- Pour utiliser Order Management ou des services tiers (comme ERP), désactivez [!UICONTROL Manage Stock].

- Si la configuration au niveau du produit utilise la valeur système par défaut, la configuration du magasin est remplacée.

Lorsque [!DNL Inventory Management] est activé, consultez les sections suivantes pour configurer tous les paramètres :

- [Configuration des options globales](global-options.md) - Paramètres affectant l’ensemble du catalogue, considérés comme les paramètres par défaut du système.

- [Configuration des options du produit](product-options.md) - Paramètres d’un produit spécifique qui remplacent les options globales.

## Activer ou désactiver le [!DNL Inventory Management]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) _Options de stock de produits_ et configurez les éléments suivants :

   ![Options de stock de produits](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Pour gérer l’inventaire et utiliser toutes les fonctionnalités [!DNL Commerce], définissez **[!UICONTROL Manage Stock]** sur `Yes` (par défaut).

   - Pour [!DNL Inventory Management] désactiver, décochez la case **[!UICONTROL Use system value]** et définissez **[!UICONTROL Manage Stock]** sur `No`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Gestion des stocks d’un magasin

Voir [Configuration des options globales](global-options.md).

## Gestion du stock d’un produit

Voir [Configuration des options du produit](product-options.md).
