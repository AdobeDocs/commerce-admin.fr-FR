---
title: Paramètres d'expédition
description: Découvrez comment configurer les paramètres d’expédition qui définissent le point d’origine et la politique d’expédition de votre magasin.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Paramètres d&#39;expédition

La configuration de l’expédition établit le point d’origine de tous les envois, votre politique d’expédition et le traitement des envois à plusieurs adresses.

## Point d’origine

Le point d’origine sert à calculer les frais pour les envois effectués à partir de votre magasin ou de votre entrepôt, ainsi qu’à déterminer le taux de taxe pour les produits vendus. Lors du calcul des [taxes européennes](international-tax-guidelines.md#eu-tax-configuration), assurez-vous que le [calcul de destination fiscale par défaut](../configuration-reference/sales/tax.md) pour chaque vue de magasin correspond au point d’origine Paramètres d’expédition.

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et complétez les éléments suivants :**[!UICONTROL Origin]**

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (et ligne 2, si nécessaire)

1. Cliquez sur **[!UICONTROL Save Config]**.

## Politique d&#39;expédition

Une politique d’expédition doit expliquer les règles commerciales et les directives de votre société concernant les envois. Par exemple, si des règles de prix entraînent la livraison gratuite, vous pouvez expliquer les conditions de votre politique de livraison.

![Règles d’expédition lors du passage en caisse](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Pour afficher votre politique de livraison lors du passage en caisse, renseignez les Paramètres de la politique de livraison dans la configuration. Le texte s’affiche lorsque les clients cliquent sur _Voir notre politique d’expédition_ lors du passage en caisse.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Shipping Policy Parameters]** .

1. Définissez **[!UICONTROL Apply Custom Shipping Policy]** sur `Yes`.

1. Collez ou entrez votre **[!UICONTROL Shipping Policy]** dans la zone de texte.

   >[!NOTE]
   >
   >Si vous utilisez un traitement de texte pour composer le texte, veillez à enregistrer le document sous la forme d’un fichier .txt afin de supprimer les caractères de contrôle du texte. Ensuite, copiez et collez le texte dans la zone de texte Politique de livraison .

   ![Paramètres de politique de livraison](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Plusieurs adresses

Les options d’expédition multi-adresses permettent aux clients d’envoyer une commande à plusieurs adresses lors de l’extraction et de déterminer le nombre maximal d’adresses auxquelles une commande peut être expédiée.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Multishipping Settings]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Options]** .

   ![Options d’expédition multi-adresses](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Allow Shipping to Multiple Addresses]** sur `Yes`.

1. Saisissez le **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![&#x200B; Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Pour les commandes avec plusieurs adresses de livraison, le mode de paiement [&#x200B; Paiement sur compte](../b2b/enable-basic-features.md#configure-payment-on-account), même s’il est activé, n’est pas disponible pendant le passage en caisse.
