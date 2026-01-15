---
title: Paramètres d’expédition
description: Découvrez comment configurer les paramètres d’expédition qui définissent le point d’origine et la politique d’expédition de votre boutique.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Paramètres d’expédition

La configuration d&#39;expédition établit le point d&#39;origine de toutes les expéditions, votre politique d&#39;expédition et la gestion des expéditions à plusieurs adresses.

## Point d’origine

Le point d’origine est utilisé pour calculer les frais pour les expéditions effectuées à partir de votre magasin ou entrepôt et détermine également le taux de taxe pour les produits vendus. Lors du calcul de [taxes UE](international-tax-guidelines.md#eu-tax-configuration), assurez-vous que le [Calcul de la destination de la taxe par défaut](../configuration-reference/sales/tax.md) pour chaque vue de magasin correspond au point d’origine des paramètres d’expédition.

![Origine](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Origin]** et effectuez les opérations suivantes :

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (et ligne 2, si nécessaire)

1. Cliquez sur **[!UICONTROL Save Config]**.

## Politique d&#39;expédition

Une politique d&#39;expédition doit expliquer les règles commerciales et les directives de votre entreprise en matière d&#39;expédition. Par exemple, si vous avez des règles de prix qui déclenchent la livraison gratuite, vous pouvez expliquer les termes dans votre politique de livraison.

![Politique D&#39;Expédition Lors Du Passage En Caisse](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Pour afficher votre politique d&#39;expédition lors du passage en caisse, complétez les paramètres de la politique d&#39;expédition dans la configuration. Le texte s’affiche lorsque les clients cliquent sur _Voir notre politique d’expédition_ lors du passage en caisse.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Shipping Policy Parameters]** .

1. Définissez **[!UICONTROL Apply Custom Shipping Policy]** sur `Yes`.

1. Collez ou saisissez votre **[!UICONTROL Shipping Policy]** dans la zone de texte.

   >[!NOTE]
   >
   >Si vous utilisez un traitement de texte pour composer le texte, veillez à enregistrer le document en tant que fichier .txt pour supprimer tous les caractères de contrôle du texte. Copiez et collez ensuite le texte dans la zone de texte Politique d&#39;expédition.

   ![Paramètres de la stratégie d&#39;expédition](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Adresses multiples

Les options d’expédition à adresses multiples permettent aux clients d’envoyer une commande à plusieurs adresses au cours du passage en caisse et de déterminer le nombre maximal d’adresses vers lesquelles une commande peut être envoyée.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Multishipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Options]** .

   ![Options d’expédition à adresses multiples](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Allow Shipping to Multiple Addresses]** sur `Yes`.

1. Saisissez le **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Pour les commandes avec plusieurs adresses d’expédition, le mode de paiement [Paiement en compte](../b2b/enable-basic-features.md#configure-payment-on-account), même s’il est activé, n’est pas disponible lors du passage en caisse.

## URL de tracking des expéditions par e-mail

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

[!BADGE &#x200B; Sandbox &#x200B;]{type=Caution tooltip="Les éléments répertoriés ne sont actuellement disponibles que dans les environnements Sandbox. Adobe commence par rendre les nouvelles versions disponibles dans les environnements Sandbox afin que vous disposiez du temps nécessaire pour tester les modifications à venir avant que la version ne soit disponible dans les environnements de production."}

Par défaut, les numéros de suivi des expéditions envoyés dans les e-mails des acheteurs sont en texte brut. Vous pouvez convertir ces numéros de suivi en liens cliquables en activant la fonctionnalité d’URL de suivi personnalisée. Cette fonctionnalité permet de définir un modèle pour le suivi des URL de différents transporteurs. Chaque modèle comprend l’URL complète du site web de suivi et un espace réservé pour le numéro de suivi. Commerce remplace l’espace réservé par le numéro de suivi réel dans l’e-mail.

Les transporteurs suivants sont pris en charge :

- Service postal des États-Unis (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

Pour activer ou modifier les URL de tracking personnalisées :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Shipment Tracking URLs]** .

1. Définissez **[!UICONTROL Enable Custom Tracking URLs]** sur `Yes`.

1. Des modèles d’URL par défaut sont fournis pour chaque opérateur pris en charge. Si vous devez modifier l’une de ces valeurs, saisissez un nouveau modèle d’URL dans le champ correspondant. Utilisez `{{tracking_number}}` comme espace réservé pour le numéro de suivi réel. Si, par exemple, UPS modifie son URL en `https://www.ups.com/newtracker?tracknumber`, le nouveau modèle d’URL de tracking peut ressembler à ceci :

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Cliquez sur **[!UICONTROL Save Config]**.
