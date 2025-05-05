---
title: Newsletters et abonnements
description: Découvrez les newsletters et comment activer cette fonctionnalité en tant qu’outil promotionnel à bas coût.
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Newsletters et abonnements

La publication d’une newsletter régulière est considérée comme l’un des outils marketing les plus puissants et les plus abordables disponibles. Commerce vous permet de publier et de distribuer des newsletters aux clients qui se sont abonnés, ainsi que des outils pour produire votre newsletter, créer et gérer votre liste d’abonnés, développer du contenu et diriger le trafic vers votre boutique. Vous pouvez également utiliser [hiérarchie de page](../content-design/page-hierarchy.md) pour créer une archive des problèmes passés.

>[!NOTE]
>
>Vous pouvez ajouter des fonctionnalités en intégrant votre instance Commerce à un fournisseur tiers de services de newsletter et en ajoutant des extensions. Pour en savoir plus, voir [Commerce Marketplace](../getting-started/commerce-marketplace.md).

La première étape de la création de newsletters consiste à configurer les paramètres de newsletter de votre site. Vous pouvez demander aux clients de cliquer sur un lien de confirmation envoyé par email pour confirmer l’inscription. Cette méthode de double opt-in exige que les clients confirment à deux reprises qu’ils souhaitent recevoir votre newsletter et limite la possibilité qu’elle puisse être considérée comme du spam.

## Activation des newsletters

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Newsletter]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL General Options]** .

1. Pour activer les newsletters pour la portée de la vue de magasin, définissez **[!UICONTROL Enabled]** sur `Yes`.

Après avoir activé la fonction de newsletter, la section _[!UICONTROL Subscription Options]_&#x200B;s’affiche.

## Configuration des options d’abonnement

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Newsletter]**.

1. Si nécessaire, [modifiez l’étendue de configuration](../getting-started/websites-stores-views.md#scope-settings) pour appliquer les modifications de configuration de newsletter à une vue de site/magasin spécifique.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Subscription Options]** et procédez comme suit :

   ![Configuration des clients - abonnements à des newsletters](../configuration-reference/customers/assets/newsletter-subscription-options.png){width="600" zoomable="yes"}

   - Confirmez le modèle d&#39;email et l&#39;expéditeur de chacun des emails suivants envoyés aux abonnés :

      - [!UICONTROL Success email]
      - [!UICONTROL Confirmation email]
      - [!UICONTROL Unsubscribe email]

   - Pour utiliser le processus de double opt-in pour confirmer les abonnements, définissez **[!UICONTROL Need to Confirm]** sur `Yes`.

   - Pour permettre aux personnes qui n’ont pas de compte avec votre boutique de s’abonner à la newsletter, définissez **[!UICONTROL Allow Guest Subscription]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
