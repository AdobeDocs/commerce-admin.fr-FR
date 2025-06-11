---
title: Widget Commandes et retours
description: Découvrez comment utiliser le widget Commandes et retours pour permettre aux clients de vérifier le statut de leurs commandes, d’imprimer des factures et de suivre les expéditions.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Widget Commandes et retours

Le widget _Commandes et retours_ permet aux clients de vérifier le statut de leurs commandes, d’imprimer des factures et de suivre les expéditions. Lorsque le widget est ajouté au storefront, il est visible uniquement pour les invités et pour les clients qui ne sont pas connectés à leurs comptes. Vous pouvez rechercher des commandes en indiquant l’ID de commande, le nom de facturation et l’adresse e-mail ou le code postal.

![Widget Commandes et retours dans la barre latérale du storefront](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Le widget Commandes et retours sur le storefront

1. Le client peut utiliser l&#39;option **[!UICONTROL Find Order By]** pour choisir un des paramètres suivants à utiliser pour retrouver la commande :

   - Adresse e-mail
   - Code postal

1. Le client entre les **[!UICONTROL Order ID]** et les **[!UICONTROL Billing Last Name]**.

1. Saisit le **[!UICONTROL Email Address]** de facturation ou le **[!UICONTROL ZIP Code]** associé à la commande.

1. Clique sur **[!UICONTROL Search]** pour récupérer la commande.

   ![Informations de commande affichées dans le storefront](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configurer le widget Commandes et retours

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_, procédez comme suit :

   - Définissez **[!UICONTROL Type]** sur `Orders and Returns`.

   - Choisissez le **[!UICONTROL Design Theme]** utilisé par le magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Par **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement par l’administrateur.

   - Par **[!UICONTROL Assign to Store Views]**, sélectionnez les vues du magasin où le widget est visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

   - (Facultatif) Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**&#x200B;et procédez comme suit :

   - Définissez **[!UICONTROL Display On]** sur le type de page sur lequel vous souhaitez que le widget apparaisse.

   - Pour déterminer où le widget est affiché sur la page, renseignez le reste des informations de mise à jour de la mise en page.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le lien du message en haut de la page et suivez les instructions.
