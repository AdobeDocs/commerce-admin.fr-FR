---
title: Paramètres du produit - [!UICONTROL Gift Options]
description: Pour un produit, les paramètres de [!UICONTROL Gift Options] déterminent si un message cadeau peut être inclus ou si des options d’emballage cadeau sont disponibles lors du passage en caisse.
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Gift Options]

Dans la section _[!UICONTROL Gift Options]_, vous pouvez définir les options de message cadeau et d’emballage-cadeau lors du passage en caisse au niveau du produit. Pour remplacer le paramètre de configuration par défaut, désélectionnez la case **[!UICONTROL Use Config Settings]**.

![Options de cadeau](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## Définir des options de cadeau pour un seul produit

1. Ouvrez le produit en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _[!UICONTROL Gift Options]_, puis procédez comme suit :

   - Pour remplacer le paramètre par défaut, désélectionnez la case **[!UICONTROL Use Config Settings]**.

   - Définissez **[!UICONTROL Allow Gift Message]** selon les besoins pour le produit.

   - ![](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) uniquement) Définissez les **[!UICONTROL Allow Gift Wrapping]** nécessaires pour le produit.

   - ![](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) uniquement) Le cas échéant, saisissez le **[!UICONTROL Price for Gift Wrapping]**.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Activer les messages cadeaux pour votre boutique

Par défaut, Commerce permet aux clients d’ajouter un message cadeau personnalisé à leurs commandes et produits pendant le processus de passage en caisse.

Vous pouvez fournir cette fonctionnalité aux clients en activant _message cadeau_ pour votre boutique :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** sur la page.

1. Par **[!UICONTROL Allow Gift Messages on Order Level]**, sélectionnez `Yes` pour activer un message cadeau unique pour l’ensemble de la commande.

1. Par **[!UICONTROL Allow Gift Messages for Order Items]**, sélectionnez `Yes` pour activer l’ajout distinct de messages cadeau à des articles individuels dans le panier du client.

1. Cliquez sur **[!UICONTROL Save Config]**.

Avec cette configuration, les clients peuvent ajouter un message cadeau à la page du panier à partir du storefront, comme illustré dans l’exemple suivant :

![Message cadeau](./assets/gift-message.png){width="600" zoomable="yes"}
