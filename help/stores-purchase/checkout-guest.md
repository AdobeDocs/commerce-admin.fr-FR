---
title: Passage en caisse des invités
description: Découvrez comment activer les fonctionnalités de passage en caisse des invités dans votre boutique.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Passage en caisse des invités

Votre boutique peut être configurée pour obliger les acheteurs à ouvrir un compte avant d’effectuer un achat. Le paramètre par défaut permet aux invités d’effectuer des achats, avec la possibilité de s’enregistrer pour un compte une fois le processus de passage en caisse terminé.

![Le magasin Luma affiche Extraire en tant qu’invité](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_Pour désactiver le passage en caisse des invités:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

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

Pour activer cette fonctionnalité, accédez à **Magasins** > Paramètres > **Configuration** > Ventes > **Ventes** > **Passage en caisse des invités** et définissez le paramètre **Autoriser l’accès aux commandes des invités pour les e-mails enregistrés** sur `Yes`.
