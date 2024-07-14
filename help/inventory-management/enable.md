---
title: "Enable [!DNL Inventory Management]"
description: Découvrez comment activer  [!DNL Inventory Management] au niveau du magasin global ou du produit.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Activer [!DNL Inventory Management]

Pour gérer l’inventaire de vos produits, activez [!DNL Inventory Management] au niveau du magasin global ou du produit. Lorsque l’option _Gérer les stocks_ est activée, [!DNL Inventory Management] effectue automatiquement le suivi des quantités de produits disponibles pour le site par le biais des stocks et des sources configurés. Chaque fonctionnalité et option commence le suivi et la création de rapports lorsqu’elle est activée, sans configuration supplémentaire.

Vos activités commerciales et mises à jour de l’inventaire à la vitesse des ventes. En tant que clients qui font leurs achats, vous recevez des informations exactes et mises à jour sur les stocks disponibles par canal et source de vente. Les quantités vendables disponibles sont mises à jour par stock lorsque les clients ajoutent des produits au panier et effectuent des achats, et lorsque et lorsque vous gérez les commandes, créez des envois et effectuez des remboursements. Arrivées de mises à jour de stock nouvelles ou transférées à vos sources, immédiatement disponibles pour les ventes en ligne. Les commandes d’arrière-plan atteignent des seuils spécifiés sans commandes infinies ni configurations supplémentaires. De plus, vous saisissez et complétez des envois partiels ou complets à travers une ou plusieurs sources avec des recommandations, ce qui vous permet de contrôler entièrement l’exécution des commandes et l’inventaire disponible.

>[!NOTE]
>
>Par défaut, [!DNL Inventory Management] est activé lors de l&#39;installation ou de la mise à niveau de [!DNL Commerce]. Selon les besoins de votre entreprise, vous pouvez activer ou désactiver le suivi [!DNL Inventory Management] dans [!DNL Commerce].

Fonctionnement de ce paramètre dans les stocks à source unique et multi-source :

- Pour utiliser [!DNL Inventory Management], activez _[!UICONTROL Manage Stock]_.

- Les paramètres [!UICONTROL Manage Stock] de la configuration au niveau du produit remplacent la configuration du magasin.

- Pour utiliser Order Management ou des services tiers (tels que ERP), désactivez [!UICONTROL Manage Stock].

- Si la configuration au niveau du produit utilise la valeur par défaut du système, la configuration du magasin remplace .

Lorsque [!DNL Inventory Management] est activé, voir les sections suivantes pour configurer tous les paramètres :

- [Configuration des options globales](global-options.md) - Paramètres qui affectent l’ensemble de votre catalogue, considérés comme les paramètres par défaut du système.

- [Configuration des options de produit](product-options.md) - Paramètres d’un produit spécifique qui remplace les options globales.

## Activer ou désactiver [!DNL Inventory Management]

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) __ et configurez :

   ![Options Stock de produits](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Pour gérer l’inventaire et utiliser toutes les fonctionnalités [!DNL Commerce], définissez **[!UICONTROL Manage Stock]** sur `Yes` (par défaut).

   - Pour désactiver [!DNL Inventory Management], décochez la case **[!UICONTROL Use system value]** et définissez **[!UICONTROL Manage Stock]** sur `No`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Gérer le stock pour un magasin

Voir [Configuration des options globales](global-options.md).

## Gestion du stock d’un produit

Voir [Configuration des options de produit](product-options.md).
