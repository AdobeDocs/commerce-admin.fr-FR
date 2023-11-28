---
title: Paramètres du produit - [!UICONTROL Gift Options]
description: Pour un produit, la variable [!UICONTROL Gift Options] les paramètres déterminent si un message cadeau peut être inclus ou si des options d’emballage cadeau sont disponibles lors du passage en caisse.
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Gift Options]

Dans le _[!UICONTROL Gift Options]_, vous pouvez définir des options de message cadeau et d’emballage-cadeau lors du passage en caisse au niveau du produit. Pour remplacer le paramètre de configuration par défaut, désélectionnez l’option **[!UICONTROL Use Config Settings]**.

![Options de cadeau](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## Définition d’options de cadeau pour un seul produit

1. Ouvrez le produit en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _[!UICONTROL Gift Options]_et procédez comme suit :

   - Pour remplacer le paramètre par défaut, désélectionnez l’option **[!UICONTROL Use Config Settings]** .

   - Définir **[!UICONTROL Allow Gift Message]** selon les besoins du produit.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) uniquement) Défini **[!UICONTROL Allow Gift Wrapping]** selon les besoins du produit.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) uniquement) Le cas échéant, saisissez la valeur **[!UICONTROL Price for Gift Wrapping]**.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Activation des messages de cadeau pour votre boutique

Par défaut, Commerce permet aux clients d’ajouter un message cadeau personnalisé à leurs commandes et produits pendant le processus de passage en caisse.

Vous pouvez fournir cette fonctionnalité aux clients en activant _message cadeau_ pour votre boutique :

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** sur la page.

1. Pour **[!UICONTROL Allow Gift Messages on Order Level]**, sélectionnez `Yes` pour activer un seul message cadeau pour l’ensemble de la commande.

1. Pour **[!UICONTROL Allow Gift Messages for Order Items]**, sélectionnez `Yes` pour activer l’ajout distinct de messages-cadeaux aux articles individuels dans le panier du client.

1. Cliquez sur **[!UICONTROL Save Config]**.

Avec cette configuration, les clients peuvent ajouter un message cadeau dans la page de panier à partir de storefront, comme illustré dans l’exemple suivant :

![Message du cadeau](./assets/gift-message.png){width="600" zoomable="yes"}
