---
title: Passage en caisse des invités
description: Découvrez comment activer les fonctionnalités de passage en caisse des invités dans votre boutique.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
TQID: 'https://experienceleague.adobe.com/jxrHQ1knuqHBmM1DsVa9NqdV-XNFdQDWjvwW4kHEyYM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8cd50456-5eb0-5364-922a-f14161feb828
    internal-label: Checkout
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9d3fe9829bb5a7f2a75ad3c89edd38010f816a0c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%
---
# Passage en caisse des invités

Votre boutique peut être configurée pour obliger les acheteurs à ouvrir un compte avant d’effectuer un achat. Le paramètre par défaut permet aux invités d’effectuer des achats, avec la possibilité de s’enregistrer pour un compte une fois le processus de passage en caisse terminé.

![Le magasin Luma affiche Extraire en tant qu’invité](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_Pour désactiver le passage en caisse des invités:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > **[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Checkout Options]** .

   ![Options de passage en caisse développées sur la page de configuration](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Options de paiement](../configuration-reference/sales/checkout.md#checkout-options) dans le _Guide de référence de configuration_.

1. Si le paramètre concerne une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Définissez **[!UICONTROL Allow Guest Checkout]** sur `No`.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour activer les modifications apportées à ce paramètre.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Autoriser l’accès aux commandes des invités pour les e-mails enregistrés

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

La configuration facultative au niveau du magasin, désactivée par défaut, permet aux acheteurs invités de suivre leurs commandes passées à l’aide d’une adresse e-mail correspondant à un compte client enregistré.

Lorsqu’elle est activée, les commandes de passage en caisse passées par des invités avec un e-mail enregistré restent accessibles, tout en apparaissant également dans l’historique des commandes du client.

Pour activer cette fonctionnalité, accédez à **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Guest Checkout]** et définissez le paramètre **[!UICONTROL Allow Guest Order Access for Registered Emails]** sur `Yes`.
