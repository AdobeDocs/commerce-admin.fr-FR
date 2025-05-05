---
title: Configurer les retours
description: Découvrez comment activer les retours pour votre magasin et configurer les méthodes d’expédition prises en charge.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Configurer les retours

{{ee-feature}}

Lorsqu’elles sont activées, les demandes RMA peuvent être envoyées par les clients à partir du storefront. Une RMA ne peut être générée que si un élément est disponible pour renvoi dans l’ordre. Les demandes de renvoi d’éléments individuels sont gérées par l’attribut _Enable RMA_ dans chaque enregistrement de produit. Par défaut, les paramètres de configuration sont appliqués au produit (_[!UICONTROL Use Config Settings]_&#x200B;est sélectionné). Si&#x200B;_[!UICONTROL Enable RMA]_ est défini sur `No`, le produit n’apparaît pas dans la liste des éléments qui peuvent être renvoyés. Si vous modifiez le paramètre _Activer RMA_ , il s’applique aux commandes nouvelles et existantes.

## Activation des RMA pour votre magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL RMA Settings]** .

   ![Paramètres RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable RMA on Storefront]** sur `Yes`.

   Ce paramètre détermine si les clients peuvent créer et afficher des requêtes RMA à partir du storefront. Les RMA peuvent être appliquées aux commandes nouvelles et existantes.

1. Définissez **[!UICONTROL Enable RMA on Product Level]** sur `Yes`.

   Ce paramètre détermine le comportement de l’attribut _Activer RMA_ pour les produits individuels sur le storefront :

   - Lorsque [!UICONTROL Enable RMA on Product Level] est défini sur `Yes`, les clients du storefront peuvent renvoyer tous les produits individuels. Elle inclut les valeurs d’attribut de produit _[!UICONTROL Enable RMA]_= `Yes` et&#x200B;_[!UICONTROL Enable RMA]_ = `No`.
   - Lorsque [!UICONTROL Enable RMA on Product Level] est défini sur `No`, les clients du storefront peuvent renvoyer uniquement les produits avec une valeur d’attribut de produit _[!UICONTROL Enable RMA]_= `Yes`.

1. Définissez **[!UICONTROL Use Store Address]** sur l’une des valeurs suivantes :

   - `Yes` - Envoyez les produits renvoyés à l’adresse du magasin.
   - `No` - Entrez une autre adresse pour les retours de produits.

   ![Paramètres RMA avec autre adresse](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Configuration des méthodes d’expédition pour les retours

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section de l’opérateur que vous souhaitez utiliser pour le service de retour, par exemple **[!UICONTROL UPS]**.

   ![Activer le service RMA pour l’opérateur](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled for RMA]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Modification des RMA autorisées au niveau du produit

Si vous activez les RMA pour votre boutique et que votre catalogue contient des produits qui ne doivent pas être autorisés pour être renvoyés, vous pouvez modifier le paramètre au niveau du produit,

1. Ouvrez le produit en mode d’édition.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Autosettings]** .

1. Décochez la case **[!UICONTROL Use Config Setting]** si nécessaire.

1. Définissez le paramètre **[!UICONTROL Enable RMA]** sur `No`.

   ![Désactiver RMA pour un produit](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.
