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

Lorsqu’elles sont activées, les demandes RMA peuvent être envoyées par les clients à partir du storefront. Une RMA ne peut être générée que si un élément est disponible pour renvoi dans l’ordre. Les demandes de renvoi d’éléments individuels sont gérées par la variable _Activer RMA_ dans chaque enregistrement de produit. Par défaut, les paramètres de configuration sont appliqués au produit (_[!UICONTROL Use Config Settings]_est sélectionné). If_[!UICONTROL Enable RMA]_ est défini sur `No`, le produit n’apparaît pas dans la liste des éléments qui peuvent être renvoyés. Si vous modifiez la variable _Activer RMA_ , il s’applique aux commandes nouvelles et existantes.

## Activation des RMA pour votre magasin

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL RMA Settings]** .

   ![Paramètres RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enable RMA on Storefront]** to `Yes`.

   Ce paramètre détermine si les clients peuvent créer et afficher des requêtes RMA à partir du storefront. Les RMA peuvent être appliquées aux commandes nouvelles et existantes.

1. Définir **[!UICONTROL Enable RMA on Product Level]** to `Yes`.

   Ce paramètre détermine le comportement de la variable _Activer RMA_ pour les produits individuels sur le storefront :

   - When [!UICONTROL Enable RMA on Product Level] est défini sur `Yes`, les clients du storefront peuvent renvoyer tous les produits individuels. Elle inclut les deux _[!UICONTROL Enable RMA]_= `Yes` et_[!UICONTROL Enable RMA]_ = `No` valeurs d’attribut de produit.
   - When [!UICONTROL Enable RMA on Product Level] est défini sur `No`, les clients du storefront peuvent renvoyer uniquement les produits avec une _[!UICONTROL Enable RMA]_= `Yes` valeur d’attribut de produit.

1. Définir **[!UICONTROL Use Store Address]** à l’une des valeurs suivantes :

   - `Yes` - Envoyez les produits renvoyés à l’adresse du magasin.
   - `No` - Entrez une autre adresse pour les retours de produits.

   ![Paramètres RMA avec autre adresse](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Configuration des méthodes d’expédition pour les retours

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section de l’opérateur que vous souhaitez utiliser pour le service de retour, par exemple : **[!UICONTROL UPS]**.

   ![Activation du service RMA pour l’opérateur](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enabled for RMA]** to `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Modification des RMA autorisées au niveau du produit

Si vous activez les RMA pour votre boutique et que votre catalogue contient des produits qui ne doivent pas être autorisés pour être renvoyés, vous pouvez modifier le paramètre au niveau du produit,

1. Ouvrez le produit en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Autosettings]** .

1. Effacez la variable **[!UICONTROL Use Config Setting]** si nécessaire.

1. Activez/désactivez la variable **[!UICONTROL Enable RMA]** paramètre sur `No`.

   ![Désactivation de la RAM pour un produit](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.
